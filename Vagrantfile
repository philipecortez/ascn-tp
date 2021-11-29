Vagrant.configure("2") do |config|

  config.vm.box = "ubuntu/focal64"

  config.vm.provider "virtualbox" do |v|
      v.memory = 1024
      v.cpus = 2
  end

  config.vm.define "ansible_machine" do |m|
    m.vm.provision "shell", inline: <<-SHELL
       add-apt-repository --yes --update ppa:ansible/ansible
       apt install -y software-properties-common python3-pip ansible
       pip3 install requests google-auth
     SHELL
  end
end
