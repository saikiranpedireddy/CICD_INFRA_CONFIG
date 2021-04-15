<h1>Compute Instance creation for Jenkins and Jfrog</h1>

1. Login to the OCI console.

2. Click on the hamburger menu and under compute select instances.

![image](https://user-images.githubusercontent.com/71814347/114852363-50ef9800-9e00-11eb-9161-d5c8b6cc2ff8.png)

3. In instance page click on Create Instance.

![image](https://user-images.githubusercontent.com/71814347/114852506-767ca180-9e00-11eb-915c-d3d9de5cb2aa.png)

4. In Create Compute Instance page enter the name of the instance and select the compartment in which the instance need to be created.

![image](https://user-images.githubusercontent.com/71814347/114852588-872d1780-9e00-11eb-941c-352e749c2f7f.png)

5. Under the Placement and hardware section select the Availability domain, Image and Share of the Compute instance.

![image](https://user-images.githubusercontent.com/71814347/114852703-a1ff8c00-9e00-11eb-92f5-b0129363a64f.png)

6. Under Networking section click on Select existing virtual cloud network, select the compartment for network where the VCN is created, select the VCN that is created for the CICD, select the compartment for Subnet and select the required subnet.

![image](https://user-images.githubusercontent.com/71814347/114852752-b0e63e80-9e00-11eb-83e8-499a61ad97e6.png)

7. Under Add SSH Keys section select Choose public key files upload the ssh keys.

![image](https://user-images.githubusercontent.com/71814347/114852802-bf345a80-9e00-11eb-8cdb-6e3674e83df8.png)

8. Click on Show advanced options, under Management add the Tags to the instance and click on Create.

![image](https://user-images.githubusercontent.com/71814347/114852878-d07d6700-9e00-11eb-801b-44bb3057a527.png)

