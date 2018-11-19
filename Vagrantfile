manager_ip = "192.168.10.10"

Vagrant.configure("2") do |config|
    config.vm.define "manager" do |i|
    config.vm.provider "virtualbox" do |v|
        v.memory = 6048  #Assign the memmory according to your available resource
        v.cpus = 3       #Assign CPU according to your available resource
        v.customize ['modifyvm', :id, '--natdnshostresolver1', 'on']
        v.customize ['modifyvm', :id, '--natdnsproxy1', 'on']
    end

      i.vm.box = "centos/7"
      i.vm.hostname = "manager"
      i.vm.network "private_network", ip: "#{manager_ip}", netmask: "255.255.0.0"
      i.ssh.forward_agent = true
      i.ssh.insert_key = false
      i.vm.network :forwarded_port, guest: 80, host: 80, host_ip: "127.0.0.1"
      i.vm.provision :ansible do |ansible|
       ansible.playbook = "playbook.yml"
       end
    end
end
