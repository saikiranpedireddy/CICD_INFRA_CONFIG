<h1>Subnet creation for Jenkins, Jfrog, Load balancer and Worker nodes</h1>

After the creation of a security list, route tables for Jenkins subnet, Jfrog subnet, load balancer subnet, worker node subnet, navigate to VCN. Under the resources section on the left, click on <strong>Subnets</strong> option.

![image](https://user-images.githubusercontent.com/71814347/114849910-dfaee580-9dfd-11eb-8a19-8649ee91a00b.png)

1. <strong>Subnet creation for Jenkins VM:</strong>

    a. Click on <strong>Create Subnet option</strong>, provide Name. Example: jenkins-sn

    b. Select the compartment, recommended to select the same compartment as selected for VCN.

    c. Select subnet type as <strong>Regional</strong> as recommended.

    d. Provide CIDR block for subnet as per requirement. Example: 10.0.1.0/24

    e. Select route table created in earlier steps for Jenkins subnet using compartment navigation. Example: jenkins-rt created in earlier step.

    f. Select Subnet access as <strong>Private Subnet</strong> as Jenkins should be only accessed through VPN.

    g. Select DHCP option as <strong>default DHCP option</strong> created while creating VCN using compartment navigation.

    h. Select security list created in earlier steps for Jenkins subnet using compartment navigation. Example: jenkins-sl created in earlier step.

    i. Click on <strong>Create Subnet</strong> then subnet will be created which can be select while creating Jenkins VM instance. 

![image](https://user-images.githubusercontent.com/71814347/114850302-3fa58c00-9dfe-11eb-8746-d699ac9a7542.png)

2. <strong>Subnet creation for Jfrog VM:</strong>

    a. Click on <strong>Create Subnet/strong> option, provide Name. Example: jfrog-sn

    b. Select the compartment, recommended to select the same compartment as selected for VCN.

    c. Select subnet type as <strong>Regional</strong> as recommended.

    d. Provide CIDR block for subnet as per requirement. Example: 10.0.2.0/24

    e. Select route table created in earlier steps for Jfrog subnet using compartment navigation. Example: jfrog-rt created in earlier step.

    f. Select Subnet access as <strong>Private Subnet</strong> as Jfrog should be only accessed through VPN.

    g. Select DHCP option as <strong>default DHCP option</strong> created while creating VCN using compartment navigation.

    h. Select security list created in earlier steps for Jfrog subnet using compartment navigation. Example: jfrog-sl created in earlier step.

    i. Click on <strong>Create Subnet </strong>then subnet will be created which can be select while creating Jfrog VM instance. 

![image](https://user-images.githubusercontent.com/71814347/114850582-901ce980-9dfe-11eb-9a00-79b80364a7fa.png)

3.<strong>Subnet creation for worker nodes:</strong>

   a. Click on <strong>Create Subnet</strong> option, provide Name. Example: workernode-sn

   b. Select the compartment, recommended to select the same compartment as selected for VCN.

   c. Select subnet type as <strong>Regional</strong> as recommended.

   d. Provide CIDR block for subnet as per requirement. Example: 10.0.3.0/24

   e. Select route table created in earlier steps for workernode subnet using compartment navigation. Example: workernode-rt created in earlier step.

   f. Select Subnet access as <strong>Private Subnet</strong> as worker nodes should be only accessed through VPN.

   g. Select DHCP option as <strong>default DHCP option</strong> created while creating VCN using compartment navigation.

   h. Select security list created in earlier steps for workernode subnet using compartment navigation. Example: workernode-sl created in earlier step.

   i. Click on <strong>Create Subnet</strong> then subnet will be created which can be select while creating worker node instances. 
![image](https://user-images.githubusercontent.com/71814347/114851025-01f53300-9dff-11eb-8fdf-d0cb0e52a54e.png)

