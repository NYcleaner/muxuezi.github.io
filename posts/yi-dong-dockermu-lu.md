最近在用Docker，实在太帅了，一次配置，四处运行。
默认images安装在/var/lib/docker，占用太多/var空间。[迁移之](https://github.com/docker/docker/issues/3127)

<!-- TEASER_END-->

```bash
export NEW_DOCKER=/home/tj2/docker
docker ps -q | xargs docker kill
stop docker
cd /var/lib/docker/devicemapper/mnt
umount ./*
mv /var/lib/docker $NEW_DOCKER
ln -s $NEW_DOCKER /var/lib/docker
start docker
```

On Ubuntu that option is to be set in the /etc/default/docker file

```
DOCKER_OPTS="-g /somewhere/else/docker/"
```