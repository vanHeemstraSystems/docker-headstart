# 100 - Upgrading to a newer version of Docker

## 100 - Upgrading to a newer version of Docker on RHEL7:

See also https://docs.docker.com/engine/install/rhel/

### Check current Docker version

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

**NOTE**: The prompt may be different depending on the current version of Docker on *your* server.

## Uninstall Old Versions

```
$ sudo yum remove docker \
                  docker-client \
                  docker-client-latest \
                  docker-common \
                  docker-latest \
                  docker-latest-logrotate \
                  docker-logrotate \
                  docker-engine \
                  podman \
                  runc
```

Your prompt may look like thsi:

```
Loaded plugins: product-id, search-disabled-repos, subscription-manager
No Match for argument: docker
No Match for argument: docker-client
No Match for argument: docker-client-latest
No Match for argument: docker-common
No Match for argument: docker-latest
No Match for argument: docker-latest-logrotate
No Match for argument: docker-logrotate
No Match for argument: docker-engine
No Match for argument: podman
Resolving Dependencies
--> Running transaction check
---> Package containerd.io.x86_64 0:1.6.6-3.1.el7 will be erased
--> Processing Dependency: containerd.io >= 1.2.2-3 for package: 3:docker-ce-19.03.8-3.el7.x86_64
--> Running transaction check
---> Package docker-ce.x86_64 3:19.03.8-3.el7 will be erased
--> Finished Dependency Resolution

Dependencies Resolved

============================================================================================================================================================================
 Package                                  Arch                              Version                                      Repository                                    Size
============================================================================================================================================================================
Removing:
 containerd.io                            x86_64                            1.6.6-3.1.el7                                @puppet-docker-ce                            125 M
Removing for dependencies:
 docker-ce                                x86_64                            3:19.03.8-3.el7                              @puppet-docker-ce                            104 M

Transaction Summary
============================================================================================================================================================================
Remove  1 Package (+1 Dependent package)

Installed size: 229 M
Is this ok [y/N]:
```

Confirm by typing ```yes``` followed by the ENTER button.


More ...
