Vagrant.configure("2") do |config|
    config.vm.box = "mindpointgroup/redhat8-efi"

    config.vm.define 'rocky8-bios'

    # Prevent SharedFoldersEnableSymlinksCreate errors
    config.vm.synced_folder ".", "/vagrant", disabled: true
end
