FROM alfresco/alfresco-content-repository:6.0.0.1

ADD https://github.com/uw-it-edm/acs-act-as/releases/download/1.112.1/acs-act-as-1.112.1.amp  /usr/local/tomcat/amps/acs-act-as.amp
ADD https://github.com/uw-it-edm/acs-event-publisher/releases/download/1.113.1/acs-event-publisher-1.113.1.amp  /usr/local/tomcat/amps/acs-event-publisher.amp

RUN java -jar /usr/local/tomcat/alfresco-mmt/alfresco-mmt*.jar install \
              /usr/local/tomcat/amps/acs-act-as.amp \
              /usr/local/tomcat/webapps/alfresco -nobackup -force

RUN java -jar /usr/local/tomcat/alfresco-mmt/alfresco-mmt*.jar install \
              /usr/local/tomcat/amps/acs-event-publisher.amp \
              /usr/local/tomcat/webapps/alfresco -nobackup -force
