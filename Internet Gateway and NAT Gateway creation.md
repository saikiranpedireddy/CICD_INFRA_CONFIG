<h1>Internet Gateway and NAT Gateway creation</h1>

1. **Internet Gateway:**
  
    a. Go to VCN created, click on VCN and choose “Internet Gateway” from the left side resources list as shown in the below screenshot, Provide a name and by default, it will take the compartment in which VCN residing. Check if the right compartment is selected. Then click on create. 

![image](https://user-images.githubusercontent.com/71814347/114851336-58fb0800-9dff-11eb-8f58-a7475cf01283.png)

   b. Internet Gateway is used to allow ingress/egress traffic for resources created under public subnet type.  Once Internet Gateway is created, now you can add the routes for public subnets created as shown below screenshot.  Example: Public Load balancer needs a route to Internet Gateway.  

![image](https://user-images.githubusercontent.com/71814347/114851392-6adcab00-9dff-11eb-949b-74cde1147da8.png)

   c. Once the above fields are filled and then click on Add Route Rules. It looks like the below screenshot.

![image](https://user-images.githubusercontent.com/71814347/114851463-7f20a800-9dff-11eb-86f0-9e60eff0a027.png)

   d. After adding route rule in the route table. We need to allow egress traffic in the security list of the same subnet as shown in the below screenshot.

![image](https://user-images.githubusercontent.com/71814347/114851679-b8f1ae80-9dff-11eb-9d4b-21774d599a2c.png)

2.  **NAT Gateway creation:**

    a. Go to VCN created, click on VCN and choose NAT Gateways. Provide a name and check whether the compartment is the same as VCN residing. Select “Ephemeral Public IP Address” and click on create “NAT Gateway”.  

![image](https://user-images.githubusercontent.com/71814347/114851796-d888d700-9dff-11eb-9e43-5fb5a0f1f166.png)

   b. Once NAT Gateway is created. we should add the route rule in Route Table for private subnet resources to access the internet through NAT Gateway. Example: Jenkins, jfrog worker node subnet needs to have NAT gateway route rule as the worker nodes are using private subnet. Add route rule as shown below screenshot for worker node subnet’s Route Table.

![image](https://user-images.githubusercontent.com/71814347/114851927-efc7c480-9dff-11eb-8740-5c49e67fee5e.png)

   c. After adding route rule in the route table. We need to allow egress traffic in the security list of the same subnet as shown in the below screenshot. 

![image](https://user-images.githubusercontent.com/71814347/114852070-0ff78380-9e00-11eb-8823-b9e74234416e.png)


