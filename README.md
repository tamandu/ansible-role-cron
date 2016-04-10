# ansible-role-cron

This role set up cron jobs.

## Requirements

None.

## Role Variables

variable | required | default | choice         | comment
-------- | -------- | ------- | -------------- | -------------------
name     | yes      |         |                | Description of a crontab entry.
job      | yes      |         |                | The command to execute.
user     | no       | root    |                |
minute   | no       | *       |                |
hour     | no       | *       |                |
day      | no       | *       |                |
month    | no       | *       |                |
weekday  | no       | *       |                |
state    | no       | present | present,absent |

## Dependencies

None.

## Example Playbook

```yml
- hosts: servers
  roles:
    - cron
```

*Inside `vars/main.yml`*:  
Asterisk must be enclosed by quotes.
```yml
cron:
  - name: 'sample job 1'
    job: /home/ansible/sample1.sh
    user: ansible
    minute: '*'
    hour: '*'
    day: '*'
    month: '*'
    weekday: '*'
```

## License

MIT

## Author Information
