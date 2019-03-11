# zip 
`tar -cvzf <target>.tar <target>`

# unzip
`tar -xvzf <target>.tar`







# docker



### install docker

[Windows](https://docs.docker.com/toolbox/overview/)

- https://docs.docker.com/toolbox/toolbox_install_windows/

- https://hub.docker.com/editions/community/docker-ce-desktop-windows


[Mac](https://docs.docker.com/docker-for-mac/)

- https://docs.docker.com/docker-for-mac/install/
- https://hub.docker.com/editions/community/docker-ce-desktop-mac





check latest gaia version on [dockerhub](https://hub.docker.com/r/tendermint/gaia/tags)



### pull docker image of tendermint/gaia

```bash
docker pull tendermint/gaia:stable
docker pull tendermint/gaia:<Tag>
```



### get shell of docker

```bash
docker run -it tendermint/gaia:stable /bin/sh

or 

docker run -it -v data:<YOUR-LOCAL-PATH> tendermint/gaia:stable /bin/sh
```

```bash
/usr/bin/gaiacli
/usr/bin/gaiad
```



### example of key managemet

```bash
gaiacli keys list

gaiacli keys add <NAME>
gaiacli keys add <NAME> --recover
```








### example of running gaiad, gaiacli command using docker

```bash
docker run -v data:<Your-CUSTOM-PATH> tendermint/gaia:stable gaiacli
docker run -v data:<Your-CUSTOM-PATH> tendermint/gaia:stable gaiad

```
