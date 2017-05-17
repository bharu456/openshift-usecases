
> Pure docker
```sh
git clone https://github.com/debianmaster/openshift-usecases
cd openshift-usecases/angularjs-on-jetty 
git clone https://github.com/angular/angular-seed
docker run -p 8080:8080 -v $(pwd)/config:/var/lib/jetty/webapps -v $(pwd)/angular-seed:/home/jesse/scratch jetty
curl  http://localhost:8080/scratch/app/
```

