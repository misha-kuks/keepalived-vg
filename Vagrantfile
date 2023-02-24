# -*- mode: ruby -*-
# vi: set ft=ruby :
nodes = {
  :web1 => {
        :box_name => "ubuntu/focal64",
        :ip_addr => '192.168.56.50'

  },
  :web2 => {
        :box_name => "ubuntu/focal64",
        :ip_addr => '192.168.56.51'
   
  },
  :db1 => {
        :box_name => "ubuntu/focal64",
        :ip_addr => '192.168.56.200'
         
  },
}

Vagrant.configure(2) do |config|

  nodes.each do |boxname, boxconfig|

      config.vm.define boxname do |box|

          box.vm.box = boxconfig[:box_name]
          box.vm.host_name = boxname.to_s
          box.vm.network "private_network", ip: boxconfig[:ip_addr]
	  box.vm.provider :virtualbox do |vb|
            vb.memory = "1024"
            vb.name = boxname.to_s

          end
      end
  end
end
