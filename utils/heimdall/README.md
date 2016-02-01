# What is Heimdall?

[Heimdall](http://glassechidna.com.au/heimdall/) is a cross-platform open-source tool suite used to flash firmware (aka ROMs) onto Samsung mobile devices.

# How to use this image

```
docker run -it --rm \
    --device /dev/bus/usb:/dev/bus/usb \
    groupsky/heimdall \
    heimdall <action> <action arguments>
```

Most likely you'll want to share some images with the container so you'll need to mount the location like this:

```
docker run -it --rm \
    --device /dev/bus/usb:/dev/bus/usb \
    --volume `pwd`:/data \
    groupsky/heimdall \
    heimdall flash --SYSTEM /data/system.img
```

## License

See [LICENSE](../../LICENSE).
