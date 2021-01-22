# sudo

[![Build Status](https://drone.osshelp.ru/api/badges/ansible/sudo/status.svg)](https://drone.osshelp.ru/ansible/sudo)

The role for Ansible, which manages sudoers.d files.

## Usage (example)

See [molecule test playbook](molecule/default/playbook.yml).

## Available parameters

| Param | Description |
| -------- | -------- |
| `sudoers_files` | List of sudoers.d files |
| `sudoers_files.[].name` | Sudoers.d filename |
| `sudoers_files.[].sudo_commands` | List of sudo commands in sudoers.d file |
| `sudoers_files.[].sudo_commands.[].user` | User who will run sudo command. Default `sudoers_files.[].name` |
| `sudoers_files.[].sudo_commands.[].host` | Sudo host. Default `ALL` |
| `sudoers_files.[].sudo_commands.[].target_user` | Sudo target user. **Required parameter** |
| `sudoers_files.[].sudo_commands.[].group` | Sudo target group |
| `sudoers_files.[].sudo_commands.[].nopasswd` | Accept sudo command without password. Default `true` = `NOPASSWD` |
| `sudoers_files.[].sudo_commands.[].command` | Sudo command. Default `ALL` |

## Useful links

- [Sudoers manual](https://www.sudo.ws/man/1.8.15/sudoers.man.html)

## TODO

- ...

## License

GPL3

## Author

OSSHelp Team, see <https://oss.help>
