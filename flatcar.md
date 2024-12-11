

* [Flatcar Butane Specification](https://www.flatcar.org/docs/latest/provisioning/config-transpiler/configuration/)

my config includes:

* [Permanently running a container](https://www.flatcar.org/docs/latest/container-runtimes/getting-started-with-docker/#permanently-running-a-container)
* [Disable immediately reboot-updates](https://www.flatcar.org/docs/latest/setup/releases/update-strategies/#reboot-strategy-options-through-butaneignition)
* [Customizing sshd](https://www.flatcar.org/docs/latest/setup/security/customizing-sshd/#customizing-sshd-with-a-butane-config)


```shell
$ docker run --rm -i quay.io/coreos/butane:latest < butane.yaml > ignition.json
```


## [Installing Flatcar Container Linux to disk](https://www.flatcar.org/docs/latest/installing/bare-metal/installing-to-disk/)

```shell
$ curl -O https://raw.githubusercontent.com/flatcar/init/flatcar-master/bin/flatcar-install
$ chmod +x flatcar-install

$ curl -O https://gist.githubusercontent.com/jansauer/4b5c78915093d3d72593515558df8069/raw/9e51797017400ecdc2a162428a9167f974ff94cf/ignition.json

$ sudo ./flatcar-install -d /dev/mmcblk0 -i ignition.json
```

