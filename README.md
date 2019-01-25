# For installing cvmfs on a virtual machine in CERN's Openstack cloud

1) Go to https://openstack.cern.ch/project/instances/
2) Launch a CC7 x86_64 m2.large machine
3) ssh to the machine from lxplus (e.g. [amlevin@lxplus085 ~]$ ssh amlevin@amlevin8)
4) sudo yum install emacs
5) sudo yum groupinstall -y "CERN CVMFS Fuse client"
6) sudo cvmfs_config setup
7) sudo echo "CVMFS_REPOSITORIES=cms.cern.ch" >& /etc/cvmfs/default.local
8) sudo echo "CVMFS_HTTP_PROXY=http://ca-proxy.cern.ch:3128" >> /etc/cvmfs/default.local
