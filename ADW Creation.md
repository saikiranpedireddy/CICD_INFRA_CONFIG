<h1>ADW Creation</h1>

1. Login to OCI Console.

2. Click on the hamburger menu and select Autonomous Database under Oracle Database section.

![image](https://user-images.githubusercontent.com/71814347/114854629-a75dd600-9e02-11eb-9055-1f7945840179.png)

3. In Autonomous Databases page click on Create Autonomous Database.

![image](https://user-images.githubusercontent.com/71814347/114854712-bd6b9680-9e02-11eb-865c-40c47c0236ee.png)

4. Under Create Autonomous Database screen provide the details of Compartment, Display Name, Database Name and select the workload type as Data Warehouse, Deployment type as Shared Infrastructure.

![image](https://user-images.githubusercontent.com/71814347/114854791-cfe5d000-9e02-11eb-8b1c-9ad0255b2e38.png)

5. Under Configure the database screen select the latest database version, OCPU count and Storage with Auto scaling enabled.

6. Under Create administrator credentials give the username and password for Admin user which will be used for ADW configuration.

![image](https://user-images.githubusercontent.com/71814347/114854879-e8ee8100-9e02-11eb-9137-4762ae53cd0e.png)

7. Under Choose network access select the Access Type as Virtual Cloud network, change the compartment to the one where the VNC is created, select the VCN and subnet.

8. Select the Network security group which is created earlier from the drop down menu.

9. Now select the Choose a license type to BYOL and click on Create Autonomous Database.

![image](https://user-images.githubusercontent.com/71814347/114854975-03c0f580-9e03-11eb-8653-a52159101a94.png)
