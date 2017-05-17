
```sh
oc import-image registry.access.redhat.com/redhat-openjdk-18/openjdk18-openshift:latest --confirm 
oc new-build --image-stream=openjdk18-openshift:latest --binary=true --name=jar-base
oc start-build jar-base --from-file=http://yourjar.jar
```
