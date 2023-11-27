1. https://docs.ansible.com/ansible/latest/inventory/implicit_localhost.html

2. https://docs.ansible.com/ansible/latest/collections/ansible/builtin/file_module.html

3. https://docs.ansible.com/ansible/latest/collections/ansible/builtin/setup_module.html

4. https://docs.ansible.com/ansible/latest/playbook_guide/playbooks_variables.html#registering-variables

5. https://docs.ansible.com/ansible/latest/playbook_guide/playbooks_conditionals.html#conditionals-based-on-ansible-facts

6. https://docs.ansible.com/ansible/latest/collections/ansible/builtin/lineinfile_module.html

7. https://docs.ansible.com/ansible/latest/collections/ansible/builtin/get_url_module.html

8. https://docs.ansible.com/ansible/latest/collections/ansible/builtin/command_module.html

9. https://docs.ansible.com/ansible/latest/reference_appendices/common_return_values.html#stdout-lines

10. https://docs.ansible.com/ansible/latest/network/getting_started/first_playbook.html



# Steps for exercise:

Manual Steps to Build and Deploy Application.

1. Create a new base application directory in the path of "/home/labsuser/code". This directory will hold all the application files and it's associated binaries.

2. If a server is based on RedHat, there should be a file named redhat.txt inside the base app directory.

3. If a server is based on Debian, there should be a file named debian.txt inside the base app directory.

4. The file (redhat.txt/debian.txt) should have the following contents:

Kernel Version of <<OS-PLATFORM>> is  <<kernel-version>>

The contents in the << >> block are variables and should be computed based on the server environment.

5. Download the Application Code into the base app directory. The link to the app code is as follows:

https://raw.githubusercontent.com/demokplabsuser/demorepo/main/demo.cpp

6. Compile the Application with the following commands:

g++ demo.cpp -o democode

7. Run the application with the following command to verify if it works:

./democode

8. Store the output of the application to a file named app-output.txt inside base app directory.


Commands:

ansible localhost -m setup > facts.txt

For azure
https://azurediagrams.com/