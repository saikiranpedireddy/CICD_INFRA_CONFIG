<h1>Virtual Cloud Network creation</h1>

1. To create a Virtual Cloud Network (VCN) in oracle cloud, click on the hamburger menu and navigate/scroll to Networking → Virtual Cloud Networks as shown below screenshot and click on Virtual Cloud Networks.

![image](https://user-images.githubusercontent.com/71814347/114846893-c48ea680-9dfa-11eb-94c2-5211c1192325.png)

2. Now you will be able to see <strong>create VCN</strong> option. Click on <strong>create VCN.</strong>

  * Provide the Name as required. (Example: preprodvcn)

  * Select the compartment in which you want VCN to reside. (Example: root/orbitinternal)

  * Provide the CIDR block details which range from /16 to /30 private IP pool. (Example: 10.0.0.0/16)

   - Note: Always get the valid free IP pool from the Infra team in order to avoid overlap networks.

  * Click on Create VCN.

![image](https://user-images.githubusercontent.com/71814347/114847231-1cc5a880-9dfb-11eb-9bd8-61bced8ca37c.png)

3.  Now a VCN will be created in the selected compartment with a default route table, default security list as shown in the below image.
![image](https://user-images.githubusercontent.com/71814347/114847316-349d2c80-9dfb-11eb-954a-b948047bd0a1.png)

