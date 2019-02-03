# For installing cvmfs on a virtual machine in CERN's Openstack cloud

## centos7

1) Go to https://openstack.cern.ch/project/instances/
2) Launch a CC7 x86_64 m2.large machine
3) ssh to the machine from lxplus (e.g. [amlevin@lxplus085 ~]$ ssh amlevin@amlevin8)
4) sudo yum install emacs
5) sudo yum groupinstall -y "CERN CVMFS Fuse client"
6) sudo cvmfs_config setup
7)  sudo echo "CVMFS_REPOSITORIES=cms.cern.ch" | sudo tee /etc/cvmfs/default.local > /dev/null
8) sudo echo "CVMFS_HTTP_PROXY=http://ca-proxy.cern.ch:3128" | sudo tee -a /etc/cvmfs/default.local > /dev/null 

## slc6

1) Go to https://openstack.cern.ch/project/instances/
2) Launch a SLC6 x86_64 m2.large machine
3) ssh to the machine from lxplus (e.g. [amlevin@lxplus085 ~]$ ssh amlevin@amlevin8)
4) sudo yum install emacs
5) sudo yum install https://ecsft.cern.ch/dist/cvmfs/cvmfs-release/cvmfs-release-latest.noarch.rpm
6) sudo yum install cvmfs cvmfs-config-default
7) sudo echo "CVMFS_REPOSITORIES=cms.cern.ch" | sudo tee /etc/cvmfs/default.local > /dev/null
8) sudo echo "CVMFS_HTTP_PROXY=http://ca-proxy.cern.ch:3128" | sudo tee -a /etc/cvmfs/default.local > /dev/null 
9) sudo cvmfs_config setup
