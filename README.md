# CentOS image including Systemd

This [Docker](https://www.docker.com) image can be used to test [Ansible](https://www.ansible.com) playbooks based on [Molecule](https://molecule.readthedocs.io).

## Supported tags

|Branch|CentOS version|Docker image tag|
|------|--------------|----------------|
|master|7             |7               |
|7     |7             |7               |

## Usage

### Start the container

```console
docker run \
  --cap-add SYS_ADMIN \
  --detach \
  --name centos-7 \
  --rm \
  --volume /sys/fs/cgroup:/sys/fs/cgroup:ro \
  dhoppeit/docker-centos-systemd:7
```

### Enter the container

```console
docker exec -it centos-7 bash
```

### Stop the container

```console
docker stop centos-7
```
