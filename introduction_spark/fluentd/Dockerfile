FROM centos
RUN yum install -y vim wget
COPY install-redhat-td-agent3.sh install-redhat-td-agent3.sh
RUN sh install-redhat-td-agent3.sh
COPY td-agent.conf /etc/td-agent/td-agent.conf
RUN td-agent-gem install fluent-plugin-dstat
CMD td-agent
