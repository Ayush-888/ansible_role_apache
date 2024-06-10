Ansible Role: ansible_role_apache

This Ansible role installs the Apache HTTP server (httpd) on managed nodes and copies a basic HTML file to the web server document root.

Features:
* Installs Apache2 package
* Copies index.html file to /var/www/html (only for nodes in the webservers group)

Requirements:
* Ansible version 2.1 or later

Role Variables:
* None currently defined.

Dependencies:
* None currently defined.

How to Use:
1. Clone the role repository:Bashgit clone https://github.com/your_username/ansible_role_apache.git

2. Add the role to your Ansible playbook:-
- hosts: all
  become: true
  roles:
    - role: apache_playbook

Replace all with the target host group if you're not deploying to all hosts.

3. (Optional) Target specific hosts for HTML file:
    * Create a group named webservers in your Ansible inventory and add the desired nodes to it.
    * The index.html file will only be copied to these nodes.

4. Run the playbook:
* ansible-playbook -i inventory.ini <your-playbook>.yaml

Testing:
It's recommended to write unit tests for your role to ensure its functionality. You can use tools like Molecule or the ansible-test module.

Contributing:
We welcome contributions to improve this role. Feel free to submit pull requests with bug fixes, enhancements, or additional features.

License:
This role is licensed under the MIT License.
