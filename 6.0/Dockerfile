FROM alfresco/alfresco-content-repository:6.0.0.1

ADD https://github.com/uw-it-edm/acs-act-as/releases/download/1.112.1/acs-act-as-1.112.1.amp  /usr/local/tomcat/amps/acs-act-as.amp

RUN java -jar /usr/local/tomcat/alfresco-mmt/alfresco-mmt*.jar install \
              /usr/local/tomcat/amps/acs-act-as.amp \
              /usr/local/tomcat/webapps/alfresco -nobackup -force
