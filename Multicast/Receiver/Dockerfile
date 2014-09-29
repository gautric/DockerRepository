#
#

FROM fedora
MAINTAINER	Greg A. <greg@a.net>

ENV container docker
RUN yum -y update; yum clean all; yum -y install iperf net-tools

CMD ["iperf","-s","-u","-B","224.0.1.105","-p","23364","-i","1"]
