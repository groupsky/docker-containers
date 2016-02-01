# What is Heimdall?

[Heimdall](http://glassechidna.com.au/heimdall/) is a cross-platform open-source tool suite used to flash firmware (aka ROMs) onto Samsung mobile devices.

# How to use this image

```
docker run -it --rm \
    --device /dev/bus/usb:/dev/bus/usb \
    --env DISPLAY=$DISPLAY \
    --volume /tmp/.X11-unix:/tmp/.X11-unix \
    groupsky/heimdall-frontend
```

Most likely you'll want to share some images with the container so you'll need to mount the location like this:

```
docker run -it --rm \
    --device /dev/bus/usb:/dev/bus/usb \
    --env DISPLAY=$DISPLAY \
    --volume /tmp/.X11-unix:/tmp/.X11-unix \
    --volume `pwd`:/data \
    groupsky/heimdall-frontend
```

**Note:** the container is configured to run the heimdall frontend as user 1000:1000, if your host machine user is different you may need to change permissions to files.

# License

See [LICENSE](../../LICENSE).
