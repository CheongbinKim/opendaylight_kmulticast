# Open vSwitch
Version 2.3.1

$ sudo apt-get install -y build-essential fakeroot debhelper autoconf automake bzip2 libssl-dev openssl graphviz python-all procps python-qt4 python-zope.interface python-twisted-conch libtool

$ wget http://openvswitch.org/releases/openvswitch-2.3.1.tar.gz

$ tar -zxvf openvswitch-2.3.1.tar.gz

$ cd openvswitch-2.3.1/

$ dpkg-checkbuilddeps

$ DEB_BUILDOPETIONS='parallel=8 nocheck' fakeroot debian/rules binary

$ cd ..

$ sudo dpkg -i openvswitch-common_2.3.1-_amd64.deb openvswitch-switch_2.3.1-1_amd64.deb

$ ovs-vsctl -V
    

