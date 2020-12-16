# CentOS image including Systemd

This [Docker](https://www.docker.com) image can be used to test [Ansible](https://www.ansible.com) playbooks based on [Molecule](https://molecule.readthedocs.io).

## Supported tags

|Branch|CentOS version|Docker image tag|
|------|--------------|----------------|
|master|8             |8               |
|7     |7             |7               |
|8     |8             |8               |

## Usage

### Start the container

```console
docker run \
  --cap-add SYS_ADMIN \
  --detach \
  --name centos-8 \
  --rm \
  --volume /sys/fs/cgroup:/sys/fs/cgroup:ro \
  dhoppeit/docker-centos-systemd:8
```

### Enter the container

```console
docker exec -it centos-8 bash
```

### Stop the container

```console
docker stop centos-8
```
