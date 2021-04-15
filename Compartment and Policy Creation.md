<h1>Compartment and Policy Creation</h1>

1. <strong>Compartment Creation: </strong>

   a. To create a compartment in oracle cloud, click on the hamburger menu and navigate/scroll all the way down to Identity as shown below screenshot and click on compartments. 

![image](https://user-images.githubusercontent.com/71814347/114845942-d4f25180-9df9-11eb-9657-49f9c6a56761.png)

   b. Provide Name and description and select the parent compartment as per need. Add Tags as per requirement.  Example:  Name: cicd Parent compartment: root

![image](https://user-images.githubusercontent.com/71814347/114846006-e3d90400-9df9-11eb-8551-9cba6a9d43cd.png)

2. <strong>Policy Creation:</strong>

   a. To create a Policy in oracle cloud, click on the hamburger menu and navigate/scroll all the way down to Identity as shown below screenshot and click on Policy.  
![image](https://user-images.githubusercontent.com/71814347/114846149-05d28680-9dfa-11eb-8445-57b8d4a0064c.png)

   b. Provide the policy name and select the compartment. Using a policy builder or Advanced option write the policies with the respective group name and resource group. 

![image](https://user-images.githubusercontent.com/71814347/114846226-1aaf1a00-9dfa-11eb-8aae-d88c4c1f0057.png)

  c.  Below are the policies that need to be added. 
  
    1. Allow group <groupname> to manage instance-family in compartment <compartmentname>
    2. Allow group <groupname> to use subnets in compartment <compartmentname>	
    3. Allow group <groupname> to manage virtual-network-family in compartment <compartmentname>	
    4. Allow group <groupname> to use vnics in compartment <compartmentname>
    5. Allow group <groupname> to manage cluster-family in compartment <compartmentname>	
    6. Allow group <groupname> to manage repos in compartment <compartmentname>	
    7. Allow group <groupname> to inspect compartments in compartment <compartmentname>	
    8. Allow group <groupname> to inspect metrics in compartment <compartmentname>
    9. Allow group <groupname> to manage load-balancers in compartment <compartmentname>	
    10. Allow group <groupname> to manage mysql-family in compartment <compartmentname>
    11. Allow group <groupname> to manage volume-family in compartment <compartmentname>
    12. Allow group <groupname> to manage file-family in compartment <compartmentname>	
    13. Allow group <groupname> to read autonomous-database-family in compartment <compartmentname>	
    14. Allow group <groupname> to read metrics in compartment <compartmentname>	
    15. Allow group <groupname> to manage instance-pools in compartment <compartmentname>	
    16. Allow group <groupname> to manage auto-scaling-configurations in compartment <compartmentname>	
    17. Allow group <groupname> to manage compute-management-family in compartment <compartmentname>	
    18. Allow group <groupname> to manage compartments in compartment <compartmentname>
    19. Allow group <groupname> to manage vaults in compartment <compartmentname>
    20. Allow group <groupname> to manage keys in compartment <compartmentname>
    21. Allow group <groupname> to manage secret-family in compartment <compartmentname>

   d. Once policies are defined with a valid group name and compartment name, add tags and click on “create”.  Please remember one should have valid permissions to define policy statements.


