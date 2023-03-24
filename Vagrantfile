Vagrant.configure("2") do |config|
    config.vm.box = "mindpointgroup/redhat8-efi"
    config.ssh.username = 'vagrant'
    config.ssh.password = 'vagrant'    
    config.vm.define 'redhat8-efi'
    config.vm.box_version = "1.0.0"
    config.ssh.insert_key = true
    config.vm.network :forwarded_port, guest: 22, host: 2222, id: "ssh", auto_correct:true
    config.vm.communicator = "ssh"
    # Prevent SharedFoldersEnableSymlinksCreate errors
    config.vm.provision "ansible" do |ansible|
       ansible.playbook = "site.yml"
    config.vm.synced_folder ".", "/vagrant", disabled: true
 end
end
