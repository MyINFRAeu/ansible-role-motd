# MyINFRA.eu - Ansible Role: Message of the day

Install and configure the Message Of The Day on Managed Servers

## Requirements

No special requirements other then this role requires root access, so either run
it in a playbook with a global `become: yes`, or invoke the role in your playbook like:

```yaml
- hosts: managed
  roles:
    - role: myinfra.motd
      become: yes
```

## Variables

Available variables are listed below, along with default values (see: [defaults/main.yml](defaults/main.yml)):

### Host Variables

Set the host/server information

```yaml
myinfra_host_main_ipv4: 127.0.0.1
myinfra_host_main_ipv6: ::1
myinfra_host_datacenter: DC 1
myinfra_host_location: "Rack #1, Room #1, {{ myinfra_host_datacenter }}, City, Country [lat, lon]"
myinfra_host_contact: MyINFRA <mgmt@myinfra.eu>
myinfra_host_usage: Ansible Test Client
```

### Group Variables

Set the managed information

```yaml
myinfra_mgmt_sysadmins_signature: MyINFRA.eu - Server Management
myinfra_mgmt_sysadmins_email: info@myinfra.eu
```

### Role Variables

Set the specific role settings

```yaml
myinfra_motd_remove_default_config: false
myinfra_motd_restore_default_config: false
myinfra_motd_content: set content of motd
myinfra_motd_info: additional information to show in message
myinfra_motd_add_update: false
myinfra_motd_update_content: additional dynamic content before motd
```

## Dependencies

- None

## Playbook: example

## License

- [MIT](LICENSE)

## Copyright

- (c) 2023 All In One ~ [https://all-in-one.be](https://all-in-one.be)
- (c) 2023 MyINFRA.eu ~ [https://myinfra..eu](https://myinfra.eu)
- (c) 2023 Dennis de houx ~ [https://dehoux.be](https://dehoux.be)

## Inspiration

During development some roles in Ansible Galaxy/Github also inspired me,
thanks to the following developers for the inspiration:

- [geerlingguy](https://github.com/geerlingguy/)
