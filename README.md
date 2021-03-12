# ansible-backup

A simple ansible role to backup a couple of things:
* Docker volumes
* Fs directories

## Example Playbook

```yml
- hosts: server_name
  vars:
    backup_dir: /local/path/to/backup/dir
    backup_docker:
      container_name: /volume/mount/point
    backup_fs:
      backup_name:
        - /directory/to/backup
        - /other/directory/to/backup
  roles:
    - ansible-backup
```

## License

The code in this repository is released under MIT license (see the [LICENSE](/LICENSE) file for more information).
