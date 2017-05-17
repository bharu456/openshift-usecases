
```sh
oc import-image registry.access.redhat.com/redhat-openjdk-18/openjdk18-openshift:latest --confirm 
oc new-build --image-stream=openjdk18-openshift:latest --binary=true --name=jar-test
oc start-build jar-test --from-file=http://yourjar.jar
oc new-app jar-test -e JAVA_APP_JAR=yourjar.jar 
```
