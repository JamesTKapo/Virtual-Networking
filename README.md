# Azure Virtual Networking and DNS Lab

This project showcases hands-on experience designing and deploying Azure virtual networks, subnets, security groups, and DNS zones using both the Azure Portal and ARM templates. The lab demonstrates real-world cloud infrastructure concepts for scalable and secure Azure environments.

## Objectives

- Create and configure Azure virtual networks and subnets (manually and via templates)
- Establish communication between Application Security Groups (ASGs) and Network Security Groups (NSGs)
- Configure public and private DNS zones in Azure for internal and external name resolution

## Key Tasks

### Task 1: Create Virtual Network via Azure Portal
- **Created** a virtual network `CoreServicesVnet` with custom address space `10.20.0.0/16`
- **Defined** subnets `SharedServicesSubnet` and `DatabaseSubnet` with proper CIDR sizing
- **Exported** the network configuration as an ARM template for reuse

### Task 2: Create Virtual Network via ARM Template
- **Modified** and **deployed** a custom `template.json` and `parameters.json` to launch `ManufacturingVnet`
- **Provisioned** `SensorSubnet1` and `SensorSubnet2` with updated IP addressing
- **Verified** deployment via Azure portal and template output

### Task 3: ASG + NSG Configuration
- **Created** an Application Security Group (`<YourName>-asg-web`) and a Network Security Group (`<YourName>-NSGSecure`)
- **Associated** the NSG with a subnet and **configured** an inbound rule to allow traffic from the ASG
- **Implemented** an outbound NSG rule to deny internet access to port 8080

### Task 4: Public & Private DNS
- **Configured** a public DNS zone (`yourName.com`) and **added** A records for external resolution
- **Tested** DNS resolution using `nslookup` with Azure DNS name servers
- **Deployed** a private DNS zone (`private.yourName.com`) and **linked** it to `ManufacturingVnet` for internal VM resolution

## Tools & Services Used

- Microsoft Azure Portal
- Azure Virtual Network (VNet)
- Network Security Groups (NSG)
- Application Security Groups (ASG)
- Azure DNS (Public and Private)
- ARM (Azure Resource Manager) templates
- Visual Studio Code (for editing templates)

## Screenshots

Screenshots of each task (with underlined `odl_user` account) are saved in the `screenshots/` folder and include:
- Virtual network & subnet creation
- Template edits & deployments
- ASG & NSG configuration
- DNS zone setup & testing



