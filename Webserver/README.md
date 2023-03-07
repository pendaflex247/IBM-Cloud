# IBM Cloud VPC WIth SUBNETS project 
Objective: Create and Configure Virtual Private Cloud (VPC)  with 2 subnets.

    0. Create resource group
    1. Create VPC in that resource group
    2. Create 2 subnets with public gatway access
    3. Create SSH keys 
    4. Create ACL and attach subnets (This is about controling access to subnets)
    5. Create SG (This is about controling access to virtual machines)
    6. Create a vm - add to sg - add to subnet - add floating IP

## Network Map

<img src="vpc-image\IBM VPC Diagram-Page-3.png" width="480" >

## Create Resource group

<img src="vpc-image/IB3-Clou2-VPC-04-02_03_17_24.png" width="780" >

<img src="vpc-image/IB3-Clou2-VPC-04-02_03_17_25.png" width="780" >

<img src="vpc-image/IB3-Clou2-VPC-04-02_03_17_26.png" width="780" >

## Create VPC inside the resource group

<img src="vpc-image/IB3-Clou2-VPC-04-02_03_17_23.png" width="780" >

<img src="vpc-image/IB3-Clou2-VPC-04-02_03_18_06.png" width="780" >

<img src="vpc-image/IB3-Clou2-VPC-04-02_03_23_04.png" width="780" >

### Edith and rename the subnet names and create

<img src="vpc-image/IB3-Clou2-VPC-04-02_03_39_48.png" width="780" >
  
<img src="vpc-image/IB3-Clou2-VPC-04-02_03_50_30.png" width="780" >
  
## Create and Configure access control list (ACL)

<img src="vpc-image/IB3-Clou2-VPC-04-02_05_46_15.png" width="780" >

<img src="vpc-image\IB3-Clou2-VPC-04-02_05_51_32.png" width="780" >

### Add inbound, outbound rules and attach subnets

    SSH
    HTTP
    HTTPS
    ICMP

<img src="vpc-image\IB3-Clou2-VPC-04-02_06_02_28.png" width="780" >

<img src="vpc-image\IB3-Clou2-VPC-04-02_06_04_56.png" width="780" >

## Create Security Groups

<img src="vpc-image\IB3-Clou2-VPC-04-02_06_09_14.png" width="780" >

<img src="vpc-image\IB3-Clou2-VPC-04-02_06_10_11.png" width="780" >

### Add Inbound and outbound rules

    SSH
    HTTP
    HTTPS
    ICMP

<img src="vpc-image\IB3-Clou2-VPC-04-02_06_12_22.png" width="380" >

<img src="vpc-image\IB3-Clou2-VPC-04-02_06_14_40.png" width="380" >

<img src="vpc-image\IB3-Clou2-VPC-04-02_06_20_40.png" width="780" >

<img src="vpc-image\IB3-Clou2-VPC-04-02_06_22_27.png" width="780" >

<img src="vpc-image\IB3-Clou2-VPC-04-02_06_23_05.png" width="780" >

## Add SSH Key(s)

### Grenerate SSH Key(s)

<img src="vpc-image\IB3-Clou2-VPC-04-02_06_33_30.png" width="780" >

### Click Create and add the generated publick 

<img src="vpc-image\IB3-Clou2-VPC-04-02_06_33_28.png" width="780" >

## Create Virtual Machine Instances

<img src="vpc-image\IB3-Clou2-VPC-04-02_06_37_30.png" width="780" >

<img src="vpc-image\IB3-Clou2-VPC-04-02_06_41_50.png" width="780" >

<img src="vpc-image\IB3-Clou2-VPC-04-02_06_47_31.png" width="780" >

<img src="vpc-image\IB3-Clou2-VPC-04-02_06_49_34.png" width="780" >

### Edith Change the security group to the right one

<img src="vpc-image\IB3-Clou2-VPC-04-02_06_50_20.png" width="780" >

<img src="vpc-image\IB3-Clou2-VPC-04-02_06_51_42.png" width="780" >

<img src="vpc-image\IB3-Clou2-VPC-04-02_06_54_40.png" width="780" >

<img src="vpc-image\IB3-Clou2-VPC-04-02_06_57_23.png" width="780" >

<img src="vpc-image\IB3-Clou7-VPC-04-07_12_17_44.png" width="780" >


## Create Floating IP (Pulic Gateway) 
### For internet access to VM 
### Attached the server/vm that you want to access the internet to the floating IP

<img src="vpc-image\IB3-Clou6-VPC-04-06_11_35_57.png" width="780" >

<img src="vpc-image\IB3-Clou6-VPC-04-06_11_53_31.png" width="780" >

## Add Load Balancer (Round Robin)
### for webservers in both private subnets 
### this webservers should not have internet access (Don't attach floating IPs)

<img src="vpc-image\IB3-Clou6-VPC-04-06_11_55_09.png" width="780" >

<img src="vpc-image\IB3-Clou6-VPC-04-06_11_55_56.png" width="780" >

<img src="vpc-image\IB3-Clou6-VPC-04-06_11_56_27.png" width="780" >

### Create Back End Pool

<img src="vpc-image\IB3-Clou6-VPC-04-06_11_56_54.png" width="780" >

### Click on Attach Web Servers to add the webservers

<img src="vpc-image\IB3-Clou6-VPC-04-06_11_58_15.png" width="780" >

<img src="vpc-image\IB3-Clou6-VPC-04-06_11_59_44.png" width="780" >

<img src="vpc-image\IB3-Clou7-VPC-04-07_12_00_27.png" width="780" >

### Create Front End Listeners

<img src="vpc-image\IB3-Clou7-VPC-04-07_12_00_55.png" width="780" >

<img src="vpc-image\IB3-Clou7-VPC-04-07_12_01_41.png" width="780" >

### Add Security Group

<img src="vpc-image\IB3-Clou7-VPC-04-07_12_02_08.png" width="780" >

<img src="vpc-image\IB3-Clou7-VPC-04-07_12_02_41.png" width="780" >


### Click on the websvr-lb to open the load balancer details

<img src="vpc-image\IB3-Clou7-VPC-04-07_12_03_34.png" width="780" >

<img src="vpc-image\IB3-Clou7-VPC-04-07_12_13_15.png" width="780" >

<img src="vpc-image\IB3-Clou7-VPC-04-07_12_16_30.png" width="780" >



