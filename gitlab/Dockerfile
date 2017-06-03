FROM centos:7
LABEL author=ipple1986 email=ipple1986@gmail.com site=https://zhaozhiwen.net.cn

RUN yum install -y libsemanage-static libsemanage-devel && curl -sS https://packages.gitlab.com/install/repositories/gitlab/gitlab-ce/script.rpm.sh |  bash && \
yum install -y gitlab-ce && gitlab-ctl reconfigure
EXPOSE 22 443 80
ENTRYPOINT ["gitlab-ctl","start"]


