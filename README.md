# Actuator Demo Application

This application can be used to show the functionality of [Actuator](https://github.com/ninech/actuator).

You can deploy it on Openshift with these commands:

```sh
# first create the image stream. this is only done once.
oc process -f https://raw.githubusercontent.com/ninech/actuator-demo/master/imagestream-template.yml | oc create -f -
# then install the rest of the app. this can be done once per branch.
oc process -f https://raw.githubusercontent.com/ninech/actuator-demo/master/template.yml -p BRANCH_NAME=master | oc create -f -

# delete all objects of branch master
oc delete all -l 'branch=master'
```
