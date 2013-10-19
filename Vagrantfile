Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu_aws"
  config.vm.box_url = "https://github.com/mitchellh/vagrant-aws/raw/master/dummy.box"
  config.vm.provider :aws do |aws, override|

#  config.vm.provision :shell, :path => "bootstrap.sh"
   
    aws.region = "us-west-2" 
    aws.access_key_id = ""
    aws.secret_access_key = ""
    aws.keypair_name = "test"
    override.ssh.private_key_path = "~/.ssh/keypair.pem"
    aws.instance_type = "t1.micro"
    aws.security_groups = "admin-nameof-yoursecuritygroup"
    aws.ami = "ami-70f96e40"
    override.ssh.username = "ubuntu"
    aws.tags = {
      'Name' => 'Test Log',
     }
  end

end

