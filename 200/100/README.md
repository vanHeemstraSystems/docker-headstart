# 100 - Upgrading to a newer version of Docker

## 100 - Upgrading to a newer version of Docker on RHEL7:

See also https://docs.docker.com/engine/install/rhel/

After having logged into the server that hosts Docker (by using ```$ ssh FULLY_QUALIFIED_DOMAIN_NAME or HOST_IP_ADDRESS```), check the current version of Docker.

```
$ docker version
Client: Docker Engine - Community
 Version:           19.03.8
 API version:       1.40
 Go version:        go1.12.17
 Git commit:        afacb8b
 Built:             Wed Mar 11 01:27:04 2020
 OS/Arch:           linux/amd64
 Experimental:      false

Server: Docker Engine - Community
 Engine:
  Version:          19.03.8
  API version:      1.40 (minimum version 1.12)
  Go version:       go1.12.17
  Git commit:       afacb8b
  Built:            Wed Mar 11 01:25:42 2020
  OS/Arch:          linux/amd64
  Experimental:     false
 containerd:
  Version:          1.6.6
  GitCommit:        10c12954828e7c7c9b6e0ea9b0c02b01407d3ae1
 runc:
  Version:          1.1.2
  GitCommit:        v1.1.2-0-ga916309
 docker-init:
  Version:          0.18.0
  GitCommit:        fec3683
```

**NOTE**: The prompt may be different depending on the current versio of Docker on *your* server.


