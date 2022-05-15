Provision 3 EC2 instances using the same key pair. 1 instance should be master, the others should be targets.
Download the keypair and place it in the same directory as the install-nginx.yaml file.
SSH into master and install ansible.
Add public IPs of target instances to the ansible hosts file using 'vim /etc/ansible/hosts and [myservers] as name.
Copy install-nginx.yaml, sample.txt, and the downloaded keypair to the master ans run 'ansible-playbook install-nginx.yaml --key-file "<keypair>.pem" -v'.
SSH into one or both of the target machines to check the results.
The client I use for SSH is known as termius and I'll wholeheartedly recommend it.
