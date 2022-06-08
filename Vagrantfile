VAGRANTFILE_API_VERSION = "2"

$script = <<SCRIPT
  apt-get update
  apt-get install python3-pip
  pip install psycopg2 psycopg2-binary
  apt-get upgrade -y
SCRIPT

Vagrant.configure("2") do |config|
   config.vm.box = "ubuntu/bionic64"
   config.vm.provision "shell", inline: $script
   config.vm.provision "file", source: "/home/alex/file_for_vagrant", destination: "$HOME/remote/newfolder"
end
