
```sh
oc import-image registry.access.redhat.com/redhat-openjdk-18/openjdk18-openshift:latest --confirm 
oc new-build --image-stream=openjdk18-openshift:latest --binary=true --name=my-openjdk-app-img
oc start-build my-openjdk-app-img --from-file=https://github.com/debianmaster/openshift-usecases/blob/master/openjdk-jar-example/app.jar?raw=true
oc new-app my-openjdk-app-img -e JAVA_APP_JAR=app.jar   --name=my-openjdk-app
```
