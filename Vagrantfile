Vagrant.configure("2") do |config|
  
  config.vm.synced_folder "C:/Users/renat/meu_projeto_vagrant", "/vagrant", type: "rsync"
  config.vm.box = "ubuntu/focal64"
  config.vm.box_version = "20240130.0.0"
  config.vm.provider "virtualbox" do |vb|
    vb.memory = "8192"
    vb.cpus = "2"
  end
  config.vm.network "forwarded_port", guest:80 , host: 8080
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "playbook.yml"
  end
end