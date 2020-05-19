# Build Instruction
1. Copy your own GitHub rsa key to the build_script folder under the project-code-mongodb-store folder, rename the key to "id_rsa_github_deploy_key".
2. Open Commmand Prompt, navigate to the build_script folder and run "packer build team08f_script.json"
3. Wait for it to be done.
4. The box is located under the same folder
4. Add your box to vagrant with command
   "vagrant box add team008-virtualbox-15521563491.box --name team008"
   The name of the box might be a little bit different.
5. Under the same folder, run the following command to initialize the vagrant environment
   "vagrant init team008"
6. Edit the vagrantfile to set your personal ip address. An example of that would be:
- config.vm.network "public_network", ip:"192.168.1.65", netmask:"255.255.0.0"
7. Bootup the machine with the command "vagrant up".
8. Fire up your browser and go to "https://Your_IP_ADDRESS"

9.
NOTE: If you encounter this issue during step 7: "mount: unknown filesystem type 'vboxsf'", simply run the following commands in the buld_script folder:
- vagrant plugin install vagrant-vbguest
- vagrant destroy
- vagrant up
