# Actuator Demo Application

This application can be used to show the functionality of [Actuator](https://github.com/ninech/actuator).

You can deploy it on Openshift with this command:

    oc process -f imagestream-template.yml | oc create -f -
    oc new-app centos/nginx-18-centos7~https://github.com/ninech/actuator-demo.git

Or by using the provided template.
