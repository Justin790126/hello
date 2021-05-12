# Yocto Hello world recipes : practice with devtool flow

## Environment

* tested work at Yocto2.6.4 & Yocto3.1.7

###### tags: `Embedded Linux`


## start
* Use **https** protocol to add from webiste
````
devtool add hello https://github.com/Justin790126/hello.git
````

* build
````
devtool build hello
````

* deploy

terminal1
````
runqemu qemuarm64 core-image-minimal nographic
````

terminal2
````
devtool deploy-target -s hello root@192.168.7.2
````

* on qeumu
````
hello (you can see hello cmake here)
````

## merge to layer

````
bitbake-layers create-layer meta-hello
bitbake-layers add-layer meta-hello
devtool finish hello meta-hello
````

