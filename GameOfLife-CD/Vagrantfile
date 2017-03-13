### Vagrant file to spin Nexus, Jenkins and tomcat servers

Vagrant.configure("2") do |config|

### Nexus server
  config.vm.define "nexus" do |nexus|
    nexus.vm.box = "nrel/CentOS-6.5-x86_64"
    nexus.vm.hostname = 'nexus'
    nexus.vm.network "public_network", bridge: "wlo1"
    nexus.vm.provider :virtualbox do |v|
      v.customize ["modifyvm", :id, "--memory", 1024]
    end
  end

### Jenkins server
  config.vm.define "jenkins" do |jenkins|
    jenkins.vm.box = "ubuntu/trusty64"
    jenkins.vm.hostname = 'jenkins'
    jenkins.vm.network "public_network", bridge: "wlo1"
    jenkins.vm.provider :virtualbox do |v|
      v.customize ["modifyvm", :id, "--memory", 2048]
    end
  end

  
### Dev Tomcat server
  config.vm.define "devtom" do |devtom|
    devtom.vm.box = "nrel/CentOS-6.5-x86_64"
    devtom.vm.hostname = 'devtom'
    devtom.vm.network "public_network", bridge: "wlo1"
  end

### QA Tomcat server
  config.vm.define "qatom" do |qatom|
    qatom.vm.box = "nrel/CentOS-6.5-x86_64"
    qatom.vm.hostname = 'qatom'
    qatom.vm.network "public_network", bridge: "wlo1"
  end

### UAT Tomcat server
  config.vm.define "uattom" do |uattom|
    uattom.vm.box = "nrel/CentOS-6.5-x86_64"
    uattom.vm.hostname = 'uattom'
    uattom.vm.network "public_network", bridge: "wlo1"
  end

end
