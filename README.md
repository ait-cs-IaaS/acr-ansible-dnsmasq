# Ansible-Role: dnsmasq

Installs and configures dnsmasq. It saves all configs as seperate files in /etc/dnsmasq.d

## Requirements

- Debian or Ubuntu (18.04 or newer)

## Role Variables

```yaml
dnsmasq_config: []
```

```yaml
dnsmasq_systemd_resolved_disable: false
```

## Example Playbook

```yaml
- hosts: localhost
  roles:
          - dnsmasq
  vars:
      dnsmasq_config:
              - { name: "noname",  content: "lala" }
              - { name: "dhcp"
                  prio: "15"
                  content:|
                   long content
                }

```

## License

GPL-3.0

## Author

- Wolfgang Hotwagner
- Benjamin Akhras
