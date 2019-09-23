# 2019.09
Fall semester 2019 efforts - new platform. 

*2019.09.22 update* Created full working example of Terraform creating a vm and installing a small web server (webfsd) on it. Clone down to the Cloud Shell, change the necessary variables internally, and run "terraform init" and "terraform apply." Last message should be an IP address; type that into your browser.  

Note that this approach configures the VM after it is provisioned. Hashicorp frowns on this approach, and the tools to do it (remote-exec and the file provisioner) aren't that well documented; I had to dig around to get this to work. File provisioner has some unexpected behavior if directory tree is not fully created prior to copying files (no equivalent of mkdir -p and it doesn't fail gracefully). 
