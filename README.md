# frp

![Docker Image Version](https://img.shields.io/docker/v/wuuyh/frps)
![Docker Image Size](https://img.shields.io/docker/image-size/wuuyh/frps/latest)
![Docker Pulls](https://img.shields.io/docker/pulls/wuuyh/frps)
![Docker Stars](https://img.shields.io/docker/stars/wuuyh/frps)

![Docker Image Version](https://img.shields.io/docker/v/wuuyh/frpc)
![Docker Image Size](https://img.shields.io/docker/image-size/wuuyh/frpc/latest)
![Docker Pulls](https://img.shields.io/docker/pulls/wuuyh/frpc)
![Docker Stars](https://img.shields.io/docker/stars/wuuyh/frpc)

Docker Images for Frp Based on Alpine and Debian.

(amd64, arm32v5, arm32v6, arm32v7, arm64v8, i386, mips64le, ppc64le,riscv64, s390x)

### [Documentation](https://gofrp.org/en/)

### [中文文档](https://gofrp.org/zh-cn/docs/)

## Usage

### Basic

```bash
docker run --restart=always --network host -d -v /etc/frp/frps.toml:/etc/frp/frps.toml --name frps wuuyh/frps
docker run --restart=always --network host -d -v /etc/frp/frpc.toml:/etc/frp/frpc.toml --name frpc wuuyh/frpc
```

### Alpine

```bash
docker run --restart=always --network host -d -v /etc/frp/frps.toml:/etc/frp/frps.toml --name frps wuuyh/frps:alpine
docker run --restart=always --network host -d -v /etc/frp/frpc.toml:/etc/frp/frpc.toml --name frpc wuuyh/frpc:alpine
```

### Debian

```bash
docker run --restart=always --network host -d -v /etc/frp/frps.toml:/etc/frp/frps.toml --name frps wuuyh/frps:debian
docker run --restart=always --network host -d -v /etc/frp/frpc.toml:/etc/frp/frpc.toml --name frpc wuuyh/frpc:debian
```

```bash
docker run --restart=always --network host -d -v /etc/frp/frps.toml:/etc/frp/frps.toml --name frps wuuyh/frps:trixie
docker run --restart=always --network host -d -v /etc/frp/frpc.toml:/etc/frp/frpc.toml --name frpc wuuyh/frpc:trixie
```

## Quick reference

- Where to file issues:

[https://github.com/wuuyh/frp/issues](https://github.com/wuuyh/frp/issues)

- Where to join discussions:

[https://github.com/wuuyh/frp/discussions](https://github.com/wuuyh/frp/discussions)

- Maintained by:

wuuyh

- Supported architectures: ([more info](https://github.com/docker-library/official-images#architectures-other-than-amd64))

Alpine (linux/386,linux/amd64,linux/arm/v6,linux/arm/v7,linux/arm64,linux/ppc64le,linux/riscv64,linux/s390x)

Debian (linux/386,linux/amd64,linux/arm/v5,linux/arm/v7,linux/arm64,linux/mips64le,linux/ppc64le,linux/s390x)

- Supported Tags:

Alpine:

    - latest
    - 0.69-alpine3.23
    - 0.69.1-alpine3.23
    - 0.69-alpine
    - 0.69.1-alpine
    - alpine3.23
    - alpine
    - 0.69
    - 0.69.1

Debian:

    - trixie
    - debian
    - 0.69-trixie
    - 0.69.1-trixie
    - 0.69-debian
    - 0.69.1-debian

## Base Images

| Variant | Builder Stage               | Runtime Stage    |
|---------|-----------------------------|------------------|
| Alpine  | `golang:1.25.8-alpine3.23`  | `alpine:3.23.2`  |
| Debian  | `golang:1.25.8-trixie`      | `debian:trixie`  |

### Bumping base image versions

- **Alpine** — edit the `FROM` line in `alpine/{frpc,frps}/Dockerfile` directly. Pin the runtime tag (e.g. `alpine:3.23.2`) and the builder tag together.
- **Debian** — change `GOLANG_VERSION` in two places: the `ARG GOLANG_VERSION=...` default in `debian/{frpc,frps}/Dockerfile`, AND the `GOLANG_VERSION=...` entry in the `build-args` of `.github/workflows/debian-{frpc,frps}.yml`. The `debian:trixie` runtime tag is a rolling tag that tracks Debian 13.

> Go's Docker Hub tags don't always ship the latest patch on every base. If a build fails with `image: not found`, verify the requested Go version is still being published for that base on the [golang tags page](https://hub.docker.com/_/golang/tags).

## Ads

1. [腾讯云](https://cloud.tencent.com/act/cps/redirect?redirect=2446&cps_key=d09c5e921f9fcf4ac9516564262f3b99&from=console)
1. [阿里云](https://www.aliyun.com/minisite/goods?userCode=dbgo15cy)
1. [华为云](https://activity.huaweicloud.com/cps.html?fromacct=7766b6ea-375c-416d-9ca5-bdbef333b645&utm_source=V1g3MDY4NTY=&utm_medium=cps&utm_campaign=201905)
1. [Bandwagonhost/搬瓦工](https://bandwagonhost.com/aff.php?aff=41583)
1. [Vultr](https://www.vultr.com/?ref=7265819)

## Contact (备注：frp)

- Email:
- QQ: 3217680847
- QQ群: 949022145
- WeChat/微信群: wuuyh

## Website

1. [fatedier/frp](https://github.com/fatedier/frp)
1. [wuuyh/frp](https://github.com/wuuyh/frp)
1. [frpc images on Github](https://github.com/wuuyh/frp/pkgs/container/frpc)
1. [frps images on Github](https://github.com/wuuyh/frp/pkgs/container/frps)
1. [frpc images on Docker Hub ](https://hub.docker.com/r/wuuyh/frpc)
1. [frps images on Docker Hub ](https://hub.docker.com/r/wuuyh/frps)

## License

MIT

## Star History

[![Star History Chart](https://api.star-history.com/svg?repos=wuuyh/frp&type=Date)](https://star-history.com/#wuuyh/frp&Date)
