FROM ubuntu:17.04
MAINTAINER yujmo yujmo94@gmail.com
  
RUN apt-get update && apt-get install -y python openssh-server && mkdir /var/run/sshd \
    && echo 'root:admin123' |chpasswd  \
    && echo "PermitRootLogin yes" >> /etc/ssh/sshd_config  \
    && sed -ri 's/UsePAM yes/#UsePAM yes/g' /etc/ssh/sshd_config  
EXPOSE 22  
CMD    ["/usr/sbin/sshd", "-D"]  
