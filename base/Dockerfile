FROM centos

RUN yum -y install sudo && useradd ansible && echo "ansible:ansible" | chpasswd && gpasswd -a ansible wheel 
USER ansible
WORKDIR /home/ansible/
COPY files/* ./

RUN echo "ansible" | sudo -S yum -y install epel-release && \ 
	echo "ansible" | sudo -S yum -y install ansible python-pip && \
	echo "ansible" | sudo -S pip install pymongo suds bigsuds f5 && \
        echo "ansible" | sudo -S chmod 444 ./.vault_pass.txt
