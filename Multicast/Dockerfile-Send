#
#

FROM fedora
MAINTAINER	Greg A. <greg@a.net>

ENV container docker
RUN yum -y update; yum clean all; yum -y install iperf net-tools

CMD ["iperf","-c","224.0.1.105","-p","23364","-u","-T","32","-t","3","-i","1"]

