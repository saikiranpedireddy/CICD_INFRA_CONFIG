<h1>Security List creation for Jenkins, Jfrog, Load balancer and Worker nodes</h1>

After the creation of VCN, navigate to VCN. Now under the Resources section on the left, click on the security list option. Now you will be able to see <strong>Create Security List</strong> option.

![image](https://user-images.githubusercontent.com/71814347/114847619-83e35d00-9dfb-11eb-994b-8fef59bdf4be.png)

1. <strong> Security list for Jenkins VM subnet:</strong>
 
  a. Click on <strong>Create Security List</strong> option, provide Name for security list. Example: jenkins-sl
  
  b. Select the compartment, recommended to select the same compartment as selected for VCN. 
  
  c. Add the rules as per requirement, click on <strong>Create Security List</strong> option.
  
![image](https://user-images.githubusercontent.com/71814347/114847866-ca38bc00-9dfb-11eb-83cd-09ba6a41256e.png)

2.<strong> Security list for Jfrog VM subnet:</strong>

   a. Click on <strong>Create Security List</strong> option, provide Name for security list. Example: jfrog-sl 
   
   b. Select the compartment, recommended to select the same compartment as selected for VCN. 
      
   c. Add the rules as per requirement, click on <strong>Create Security List</strong> option.
![image](https://user-images.githubusercontent.com/71814347/114848303-30bdda00-9dfc-11eb-8e98-15269bb4e915.png)

3. <strong>Security list for Load balancer subnet:</strong>

    a. Click on <strong>Create Security List</strong> option, provide Name for security list. Example: loadbalancer-sl

    b. Select the compartment, recommended to select the same compartment as selected for VCN. 

    c. Add the rules as per requirement, click on <strong>Create Security List</strong> option.
 ![image](https://user-images.githubusercontent.com/71814347/114848491-5e0a8800-9dfc-11eb-803e-5d1592951cb7.png)

4. <strong>Security list for worker node subnet:</strong>

    a. Click on <strong>Create Security List</strong> option, provide Name for security list. Example: workernode-sl

    b. Select the compartment, recommended to select the same compartment as selected for VCN. 

    c. Add the rules as per requirement, click on <strong>Create Security List</strong> option.

![image](https://user-images.githubusercontent.com/71814347/114848664-8c886300-9dfc-11eb-8e89-d6ad44948cf7.png)




