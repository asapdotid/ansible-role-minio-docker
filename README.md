<p align="center"> <img src="https://user-images.githubusercontent.com/34257858/129839002-15e3f2c7-3f75-46d4-afae-0fd207d7fdde.png" width="100" height="100"></p>

<h1 align="center">
    Ansible Role MinIO Docker
</h1>

<p align="center" style="font-size: 1.2rem;">
    This ansible role install common packages On Ubuntu, CentOS.
</p>

<p align="center">

<a href="https://www.ansible.com">
  <img src="https://img.shields.io/badge/Ansible-2.10-green?style=flat&logo=ansible" alt="Ansible">
</a>
<a href="LICENSE.md">
  <img src="https://img.shields.io/badge/License-MIT-blue.svg" alt="Licence">
</a>
<a href="https://ubuntu.com/">
  <img src="https://img.shields.io/badge/ubuntu-20.x-orange?style=flat&logo=ubuntu" alt="Distribution">
</a>
<a href="https://www.centos.org/">
  <img src="https://img.shields.io/badge/CentOS-8-green?style=flat&logo=centos" alt="Distribution">
</a>

## Requirements

None

## Role Variables

| Name                            | Default Value  | Description                    |
| ------------------------------- | -------------- | ------------------------------ |
| `minio_docker_version`          | `latest`       | Docker image version.          |
| `minio_docker_service_name`     | `minio`        | Docker compose service name.   |
| `minio_docker_network_name`     | `app-tier`     | Docker compose network name.   |
| `minio_docker_project_location` | `/home/minio`  | Minio path project location.   |
| `minio_docker_timezone`         | `Asia/Jakarta` | Setup Timezone.                |
| `minio_docker_user`             | `""`           | Docker user.                   |
| `minio_docker_group`            | `""`           | Docker user group.             |
| `minio_docker_server_port`      | `9000`         | MinIO port for server access.  |
| `minio_docker_console_port`     | `9001`         | MinIO port for console access. |
| `minio_docker_root_user`        | `""`           | MinIO root user.               |
| `minio_docker_root_password`    | `""`           | MinIO root password.           |

## Dependencies

None.

## Example Playbook

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      vars:
        minio_version: "RELEASE.2021-09-23T04-46-24Z"
        minio_root_user: "min_admin"
        minio_root_password: "ABCDabcd123456"

      roles:
         - { role: asapdotid.minio-docker }

## License

MIT / BSD

## Author Information

[JogjaScript](https://jogjascript.com)

This role was created in 2021 by [Asapdotid](https://github.com/asapdotid).
