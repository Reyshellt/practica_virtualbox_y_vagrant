Vagrant.configure("2") do |config|
    # Definición de la primera máquina virtual
    config.vm.define "web1" do |web1|
        web1.vm.box = "ubuntu/bionic64" # Puedes usar cualquier caja de tu elección
        web1.vm.network "private_network", ip: "192.168.56.10"
        web1.vm.synced_folder "./html", "/var/www/html", create: true

        web1.vm.provider "virtualbox" do |vb|
        vb.name = "WebServer1"
        end

        web1.vm.provision "shell", inline: <<-SHELL
        apt-get update
        apt-get install -y apache2
        systemctl enable apache2
        systemctl start apache2
        SHELL
    end

    # Definición de la segunda máquina virtual
    config.vm.define "web2" do |web2|
        web2.vm.box = "ubuntu/bionic64" # Puedes usar cualquier caja de tu elección
        web2.vm.network "private_network", ip: "192.168.56.11"
        web2.vm.synced_folder "./html", "/var/www/html", create: true

        web2.vm.provider "virtualbox" do |vb|
        vb.name = "WebServer2"
        end

        web2.vm.provision "shell", inline: <<-SHELL
        apt-get update
        apt-get install -y apache2
        systemctl enable apache2
        systemctl start apache2
        SHELL
    end
end
