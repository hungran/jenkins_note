Vagrant.configure("2") do |config|
  config.vm.box = "hung"
  # Using rsync by cygwin64 instead SMB share
  config.vm.allowed_synced_folder_types = [:rsync]	
  config.vm.synced_folder "./share", "/$HOME/$USER/jenkins"
  config.vm.provider :aws do |aws, override|
    aws.access_key_id = File.read("access_key.txt")
    aws.secret_access_key = File.read("secret_access_key.txt")
#	aws.session_token = "SESSION TOKEN"
#	aws.keypair_name = "KEYPAIR NAME"
	aws.region = "ap-southeast-1"
	#ubuntu 16.04 LTS
    aws.ami = "ami-09a4a9ce71ff3f20b"
	aws.instance_type = "t2.small"
#	aws.availability_zone = "ap-southeast-1b"
	aws.subnet_id = "subnet-01ae4f7190b2f09f1"
	aws.associate_public_ip = true
	aws.private_ip_address = "172.16.0.100"
	aws.security_groups = "sg-0a000eb90d87f3821"
	aws.tags = {
		'Name' => 'Hung_Test_Vagrantfile'
	}
	aws.keypair_name = "vagrant"
	aws.user_data = File.read("bootstrap.txt")
#	Câu lệnh mặc định sử dụng user name
    override.ssh.username = "ubuntu"
#	Câu lệnh mặc định sử dụng keypem dùng khi ssh vào instance 
    override.ssh.private_key_path = "vagrant.pem"
	config.ssh.username = 'ubuntu'
  end
end