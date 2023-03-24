Vagrant.configure("2") do |config|
    config.vm.box = "mindpointgroup/redhat8-efi"
    config.ssh.username = 'vagrant'
    config.ssh.password = 'vagrant'    
    config.vm.define 'redhat8-efi'
    config.vm.box_version = "1.0.0"
    # Prevent SharedFoldersEnableSymlinksCreate errors
    config.vm.provision "ansible" do |ansible|
       ansible.playbook = "site.yml"
    config.vm.synced_folder ".", "/vagrant", disabled: true
 end
end
