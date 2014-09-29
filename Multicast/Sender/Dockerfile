#
# follow http://www.slashroot.in/how-install-and-configure-kerberos-server
# to set up a kerberos server 
#  http://www.linuxproblems.org/wiki/Set_up_kerberos_on_Centos_6 is similar but more correct
#
#   docker build -t fedora-send Dockerfile-Send
#   docker run -t fedora-send;
#
#

FROM fedora
MAINTAINER	Greg A. <greg@a.net>

ENV container docker
RUN yum -y update; yum clean all; yum -y install iperf net-tools

CMD ["iperf","-c","224.0.1.105","-p","23364","-u","-T","32","-t","3","-i","1"]

