FROM centos:6.8
#替换yum源为 mirrors.aliyun.com
RUN mv /etc/yum.repos.d/CentOS-Base.repo /etc/yum.repos.d/CentOS-Base.repo.backup
ADD Centos-6.repo /etc/yum.repos.d/
RUN mv /etc/yum.repos.d/Centos-6.repo /etc/yum.repos.d/CentOS-Base.repo

ADD epel-6.repo /etc/yum.repos.d/
RUN mv /etc/yum.repos.d/epel-6.repo /etc/yum.repos.d/epel.repo

#参考 https://github.com/xiongjungit/docker-centos/blob/master/Dockerfile
RUN yum install -y curl wget tar bzip2 unzip vim-enhanced passwd sudo yum-utils hostname net-tools rsync man && \
    yum install -y gcc gcc-c++ git make automake cmake patch logrotate python-devel libpng-devel libjpeg-devel && \
    yum install -y --enablerepo=epel pwgen python-pip && \
    yum clean all

EXPOSE 22
