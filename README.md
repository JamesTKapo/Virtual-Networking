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

Screenshots of each task
- Virtual network & subnet creation
  ![Subnets](https://github.com/user-attachments/assets/1d088171-dfe9-472b-b47e-1ba9ed41a4b4)

- Template edits & deployments
![TemplateCreationOfManufacturingVnet](https://github.com/user-attachments/assets/99686eb3-1185-461f-af9e-17e11a911aca)

- ASG & NSG configuration
![DenyRule](https://github.com/user-attachments/assets/7f9e2350-1d99-4e73-b1e0-ded76cd838e9)
![AllowRule](https://github.com/user-attachments/assets/82262423-84ff-413e-99e8-0ff868fae859)

- DNS zone setup & testing
![PrivateDNSRecordSet](https://github.com/user-attachments/assets/3fc7078a-14fb-427c-9144-e641b4e6a6fa)
![NSLookUp](https://github.com/user-attachments/assets/2f88001d-acea-40bc-9360-03a9ee861ba4)




