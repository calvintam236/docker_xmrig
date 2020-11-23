## XMRig

### What is it?

XMRig is the console miner provided by [XMRig](https://github.com/xmrig/xmrig).

XMRig supports Cryptonight, Argon2, RandomX and their variants.

### Example usages

- To build the image:

```console
$ docker build . --file YOUR_VERSION/Dockerfile.YOUR_ARCH --tag calvintam236/xmrig:mesa-YOUR_VERSION

$ docker build . --file YOUR_VERSION/Dockerfile.YOUR_ARCH --tag calvintam236/xmrig:rocm-YOUR_VERSION

$ curl -L -O --referer https://www.amd.com https://drivers.amd.com/drivers/linux/amdgpu-pro-20.45-1164792-ubuntu-20.04.tar.xz
$ docker build . --file YOUR_VERSION/Dockerfile.YOUR_ARCH --tag calvintam236/xmrig:amdgpu-YOUR_VERSION

$ docker build . --file YOUR_VERSION/Dockerfile.YOUR_ARCH --tag calvintam236/xmrig:cuda-YOUR_VERSION
```

- To run the container in background:

```console
$ docker run -d --name YOUR_CONTAINER_NAME calvintam236/xmrig:mesa-YOUR_VERSION -a YOUR_ALGO -o YOUR_POOL_ADDRESS -u YOUR_USERNAME.YOUR_WORKER_NAME -p YOUR_WORKER_PASSWORD --randomx-1gb-pages

$ docker run -d --device /dev/kfd --device /dev/dri --name YOUR_CONTAINER_NAME calvintam236/xmrig:rocm-YOUR_VERSION -a YOUR_ALGO -o YOUR_POOL_ADDRESS -u YOUR_USERNAME.YOUR_WORKER_NAME -p YOUR_WORKER_PASSWORD --no-cpu

$ docker run -d --device /dev/nvidia0 --device /dev/nvidiactl --device /dev/nvidia-uvm --name YOUR_CONTAINER_NAME calvintam236/xmrig:cuda-YOUR_VERSION -a YOUR_ALGO -o YOUR_POOL_ADDRESS -u YOUR_USERNAME.YOUR_WORKER_NAME -p YOUR_WORKER_PASSWORD --no-cpu
```

- To get `xmrig` options:

```console
$ docker run --rm calvintam236/xmrig:mesa-YOUR_VERSION

$ docker run --rm calvintam236/xmrig:rocm-YOUR_VERSION

$ docker run --rm calvintam236/xmrig:amdgpu-YOUR_VERSION

$ docker run --rm calvintam236/xmrig:cuda-YOUR_VERSION
```

- To fetch logs of a container:

```console
$ docker logs YOUR_CONTAINER_NAME
```

### Donations

If you like to buy me a coffee, you can donate to here:

- [Ko-fi](https://ko-fi.com/calvintam236)
- BTC: `1MTkPFtp3qxE4Y98pTHP3z767RGKmrT92a`
- ETH: `0x5896a85E8c175c563DC00087535582394d394838`
- XMR: `474adYsC8sLVM5gK8DbvtUVb237y9m5eMeRuYpJJVuoYUuMN5EYDuixHWxpEr6iNBb2zv3gowmJjcRoTrjhJLvMTRD1eKio`
- ETC: `0xFaBA3be3b3De5469C3F6C6185150928F3773C7b4`
- ZEC: `t1Z5Kc75JQ17txyaDUfwwyabTgsJMfuuSp4`
