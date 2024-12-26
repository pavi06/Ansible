# Simple Nginx Server Setup with Ansible

This project contains a simple setup to install an Nginx server and deploy an `index.html` file to specified instances using Ansible.

## Project Structure

```
Simple-nginxServer/
├── inventory.ini
├── playbook.yml
├── index.html
└── Readme.md
```

- `inventory.ini`: Contains the list of managed nodes (instances) where the Nginx server will be installed.
- `playbook.yml`: Ansible playbook to install Nginx and copy the `index.html` file to the instances.
- `index.html`: The HTML file to be served by the Nginx server.

## Inventory File

The `inventory` file lists the managed nodes. Example:

```
User@IP
ubuntu@192.168.1.10
ubuntu@192.168.1.11
```

## Playbook

The `playbook.yml` file contains the tasks to set up the Nginx server and deploy the `index.html` file. 

## Usage

1. Ensure you have Ansible installed on your control node.
2. Update the `inventory` file with the IP addresses of your managed nodes, and setup the passwordless authentication.
3. Create the HTML file or necessary files for the app.
4. Run the playbook:

```sh
ansible-playbook -i inventory.ini playbook.yml
```

This will install Nginx on the specified instances and deploy the `index.html` file to the web server's root directory.

## Conclusion

This setup provides a simple way to deploy an Nginx server and serve a static HTML file using Ansible. Customize the `index.html` file and inventory as needed for your environment.