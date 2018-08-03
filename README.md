# Azure-Firewall-with-standard-public-IP-in-AZ

[<img src="http://azuredeploy.net/deploybutton.png"/>](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fykbtest%2FVM-FW-Std-PIP-Azure-AZ%2Fmaster%2FAzureDeploy.json)

- This template was modified from this template: https://github.com/kytx42/Azure/tree/master/Azure-2FW-Public-LB
- This template supports the deployment of a Palo Alto Networks Firewall in an Availability Zone.  It supports the following features:
- The firewall deploys with 3 interfaces.  1 MGMT and 2 data plane. 
- A Standard SKU public IP address is attached to the MGMT interface.
- A Default NSG is applied to the MGMT interface.
- Static private IP addresses are assigned to the interfaces based on the input in the starting ip address fields.
- This template deploys into an existing VNET within the same region.  As a result, the VNET and the subnets must be created before deploying this template.
- A Managed Disk will be created.

        -The following VMs are supported:
                    -Standard_D3
                    -Standard_D4
                    -Standard_D3_v2
                    -Standard_D4_v2
                    -Standard_DS3_v2
                    -Standard_DS4_v2

        -The following VMs Licenses:
             	    -Byol
                    -Bundle1
                    -Bundle2

        -The following PAN OS Options:
                    -Latest
                    -8.1.0
                    -7.1.1 
  	          
                    
        NOTE: Make sure the VMs are supported in the specific Storage Account Type and Azure Region.


# Support Policy 
This template is released under an as-is, best effort, support policy. It should be seen as community supported and Palo Alto Networks will contribute our expertise as and when possible. We do not provide technical support or help in using or troubleshooting the components of the project through our normal support options such as Palo Alto Networks support teams, or ASC (Authorized Support Centers) partners and backline support options. The underlying product used (the VM-Series firewall) by the scripts or templates are still supported, but the support is only for the product functionality and not for help in deploying or using the template or script itself. Unless explicitly tagged, all projects or work posted in this GitHub repository are provided under the best effort policy.
