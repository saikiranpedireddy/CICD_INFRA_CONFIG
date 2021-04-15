<h1>Block volume creation for Jenkins and Jfrog</h1>

1. Login to the OCI console.

2. Click on the hamburger menu and under Block Storage select Block Volumes.

![image](https://user-images.githubusercontent.com/71814347/114853020-fc98e800-9e00-11eb-9a26-c4ce973c841f.png)

3. In the Block Volumes screen click on Create Block Volume.

![image](https://user-images.githubusercontent.com/71814347/114853065-0a4e6d80-9e01-11eb-9087-c3fe645c0590.png)

4. Under the Create Block Volume screen enter the name of the Block Volume, Select the compartment and Availability Domain in which the respective Jenkins or Jfrog instances are created.

![image](https://user-images.githubusercontent.com/71814347/114853131-1a664d00-9e01-11eb-88ba-26447fb1e44e.png)

5. Under the Volume Size and Performance select Custom, Enter the required Block Volume size in GB and select the desired Desired Volume Performance.

6. Under the Backup Policies select the compartment in which compute instance is created and desired backup policy depending on the instance type and click on Create Block Volume.

![image](https://user-images.githubusercontent.com/71814347/114853188-2d791d00-9e01-11eb-8733-763a652cf23d.png)

7. After clicking Create Block Volume button Block Volume Details page will appear. Under the Resources section click on Attached Instances and Click on Attach Instance.

![image](https://user-images.githubusercontent.com/71814347/114853282-408bed00-9e01-11eb-8a29-300113e3f106.png)

8. Under Attach to Instance screen select Attachment type as ISCSI and Access type as Read/Write.

9. under the Instance click on Select Instance, change the compartment to which the Jenkins and Jfrog instances are created, Select the respective Jenkins and Jfrog instances and select the Device Name from drop down menu.

10. Click on Attach.

![image](https://user-images.githubusercontent.com/71814347/114853379-5a2d3480-9e01-11eb-9d74-22955f1538ec.png)

11. Once the Block Volume is attached copy the Device Name and Click the Actions icon (three dots) next to the volume you just attached and then click iSCSI Commands and Information and copy the commands for mounting the volume to the compute instance.

![image](https://user-images.githubusercontent.com/71814347/114853429-66b18d00-9e01-11eb-9e7e-25c8129f1e4f.png)

12. Login to the instance with root user and execute the following command for mounting the block volume.

    a. Paste the copied attach commands list into the instance session window. (Example commands are given below)

        1. sudo iscsiadm -m node -o new -T iqn.2015-12.com.oracleiaas:cd4ca587-6e86-49f9-bfd6-04ce38c2bdfa -p 169.254.2.3:3260
        2. sudo iscsiadm -m node -o update -T iqn.2015-12.com.oracleiaas:cd4ca587-6e86-49f9-bfd6-04ce38c2bdfa -n node.startup -v automatic
        3. sudo iscsiadm -m node -T iqn.2015-12.com.oracleiaas:cd4ca587-6e86-49f9-bfd6-04ce38c2bdfa -p 169.254.2.3:3260 -l
    
    b. To get a list of mountable iSCSI devices on the instance, run the following command.
    
        1. fdisk -l
    
    c. If your disk attached successfully, you'll see it in the returned list as follows.

        1. Disk /dev/sdb: 50.0 GB, 50010783744 bytes, 97677312 sectors
        2. Units = sectors of 1 * 512 = 512 bytes
        3. Sector size (logical/physical): 512 bytes / 512 bytes
        4. I/O size (minimum/optimal): 4096 bytes / 1048576 bytes

    d. Now format the disk using fdisk command and give the Disk Name which is copied from console.

        1. fdisk /dev/oracleoci/oraclevdc

       ![image](https://user-images.githubusercontent.com/71814347/114853900-e2133e80-9e01-11eb-9ead-b20e7f4280fa.png)

    e. Now format the partitioned volume using the below command.

        1. mkfs.ext4 /dev/oracleoci/oraclevdc1
        
       ![image](https://user-images.githubusercontent.com/71814347/114854016-0242fd80-9e02-11eb-8dcd-d4b3243e4a47.png)

    f. Now create the mount point to which the volume need to be mounted.

        1. mkdir /u01

    g. Now open the /etc/fstab file and add the following entry in it.

        1. /dev/oracleoci/oraclevdc1       /u01    ext4    defaults,noatime,_netdev      0      2
        
       ![image](https://user-images.githubusercontent.com/71814347/114854182-2d2d5180-9e02-11eb-9e9d-3b331d762ce2.png)
  
    h. Now give the below command to mount the volume to the given mount point.

        1. mount -a
       
    i. Now verify whether the volume is mounted successfully with the following command. /u01 mount point should present with the given storage.

         1. df -Th

       ![image](https://user-images.githubusercontent.com/71814347/114854332-564de200-9e02-11eb-9c10-0b4da252115c.png)

    j. Now change the permissions of the created /u01 mount point to jenkins user.

          1. chown jenkins:jenkins /u01

