<h1>Route table creation for Jenkins, Jfrog, Load balancer and Worker nodes</h1>

After the creation of VCN, navigate to VCN. Now under the Resources section on the left, click on the route table. Now you will be able to see the <strong>Create Route Table</strong> option.

![image](https://user-images.githubusercontent.com/71814347/114848842-c6596980-9dfc-11eb-964b-6d1fccfcace8.png)

1.  <strong>Route Table for Jenkins VM Subnet:</strong>

    a. Click on <strong>Create Route Table</strong> option, provide Name for route table. Example: jenkins-rt

    b. Select the compartment, recommended to select the same compartment as selected for VCN.

    c. Add route rules as per requirement, click on <strong>Create</strong> option. 
![image](https://user-images.githubusercontent.com/71814347/114849021-f7d23500-9dfc-11eb-8fe7-7feb972b44af.png)

2.<strong> Route Table for Jfrog VM Subnet:</strong> 

   a. Click on <strong>Create Route Table</strong> option, provide Name for route table. Example: jfrog-rt

   b. Select the compartment, recommended to select the same compartment as selected for VCN.

   c. Add route rules as per requirement, click on <strong>Create</strong> option. 

![image](https://user-images.githubusercontent.com/71814347/114849237-30720e80-9dfd-11eb-9a06-49dc7d461f74.png)

3. <strong>Route Table for load balancer Subnet:</strong>

    a. Click on <strong>Create Route Table</strong> option, provide Name for route table. Example: loadbalancer-rt

    b. Select the compartment, recommended to select the same compartment as selected for VCN.

    c. Add route rules as per requirement, click on <strong>Create</strong> option.
  ![image](https://user-images.githubusercontent.com/71814347/114849443-60b9ad00-9dfd-11eb-9af4-fb3ce01c3960.png)

4. <strong>Route Table for Worker node Subnet:</strong>

    a. Click on <strong>Create Route Table</strong> option, provide Name for route table. Example: workernode-rt

    b. Select the compartment, recommended to select the same compartment as selected for VCN.

    c. Add route rules as per requirement, click on <strong>Create</strong> option. 
![image](https://user-images.githubusercontent.com/71814347/114849632-9199e200-9dfd-11eb-93e7-44de268da1b1.png)


