# Proxmox Script
Create a VM template using Cloud-Image and Cloud-Init.

## How to Use

Execute the following on the Proxmox Console/SSH Server:

1. **Clone the repository and setup:**
   - Clone this repository and copy the file to your PATH (e.g., `/usr/local/bin`).
   - Set execution permissions using chmod:
     ```bash
     chmod +x <filename>
     ```

2. **Download a Cloud-Image file:**
   - Debian: [Debian Cloud Images](https://cloud.debian.org/images/cloud/)
   - Ubuntu: [Ubuntu Cloud Images](https://cloud-images.ubuntu.com/)
   - CentOS: [CentOS Cloud Images](https://cloud.centos.org/)
   - AlmaLinux: [AlmaLinux Cloud Images](https://wiki.almalinux.org/cloud/Generic-cloud.html)

3. **Create a template:**
   - Run the following command to create a template:
     ```bash
     create-template vmid name cpu memory net disk image-file
     ```

## Creating and Deleting VMs

- **Create VM:**
  - After creating the template, run the `create-vm` script:
    ```bash
    create-vm template-vm-id target-vm-id vm-name
    ```
  - Example:
    ```bash
    create-vm 101 1001 vm-ubuntu
    ```

- **Delete VM:**
  - To easily delete a VM by name, use the `delete-vm` script:
    ```bash
    delete-vm vmname
    ```

## Cloud-Init

- For instructions on using cloud-init with Proxmox, visit:
  - [Cloud-Init Support in Proxmox](https://pve.proxmox.com/wiki/Cloud-Init_Support)
