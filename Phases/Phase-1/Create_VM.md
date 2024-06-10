# Creating an Ubuntu 22.04 Live Server Instance with Oracle VirtualBox

## Download and Install Oracle VirtualBox

- Download Oracle VirtualBox from the [official website](https://www.virtualbox.org/wiki/Downloads) and install it on your local machine.

## Download Ubuntu 22.04 Live Server ISO

- Download the Ubuntu 22.04 Live Server ISO image from the [official Ubuntu website](https://ubuntu.com/download/server).

## Create a Virtual Machine

- Open Oracle VirtualBox.
- Click on "New" to create a new virtual machine.
- Name your virtual machine (e.g., "Ubuntu22.04").
- Select "Linux" as the Type and "Ubuntu (64-bit)" as the Version.
- Allocate RAM and create a new virtual hard disk.

## Attach ISO File

- Select your newly created virtual machine and click on "Settings".
- Go to the "Storage" tab.
- Under "Controller: IDE", click on the empty disk icon next to "IDE Secondary Master" and select "Choose a disk file".
- Navigate to the location where you downloaded the Ubuntu 22.04 Live Server ISO file and select it.

## Start the Virtual Machine

- After attaching the ISO file, click "OK" to save the settings.
- Select your virtual machine from the VirtualBox Manager and click on "Start" to boot the virtual machine.

## Ubuntu Live Server Installation

1. When the virtual machine boots from the ISO image, follow these steps to install Ubuntu 22.04 Live Server:
   - Select your preferred language and keyboard layout.
   - Choose "Install Ubuntu" to initiate the installation process.
   - Follow the installation wizard to configure settings such as timezone, partitioning, user account, etc.

2. During the installation process, select the option to configure the network manually (Static IP).

3. Configure the network settings according to your requirements, including assigning a static IP address, netmask, gateway, and DNS servers. Make sure to note down these details for future reference.

4. Once the installation is complete and the network settings are configured, restart the virtual machine.


## Access Ubuntu Live Server

- After the virtual machine restarts, you'll be prompted to remove the installation media (ISO file). Simply press "Enter" to continue.
- You can now log in to your Ubuntu 22.04 Live Server instance using the credentials you specified during the installation process.

## Configuring UFW (Uncomplicated Firewall)

Run the following commands to configure the Uncomplicated Firewall (UFW):

```bash
sudo ufw enable
sudo ufw allow 25/tcp
sudo ufw allow 3000:10000/tcp
sudo ufw allow 80/tcp
sudo ufw allow 443/tcp
sudo ufw allow 22/tcp
sudo ufw allow 6443/tcp
sudo ufw allow 465/tcp
sudo ufw allow 30000:32767/tcp
