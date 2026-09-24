[![CI](https://github.com/de-it-krachten/ansible-role-ubuntu_pro/workflows/CI/badge.svg?event=push)](https://github.com/de-it-krachten/ansible-role-ubuntu_pro/actions?query=workflow%3ACI)


# ansible-role-ubuntu_pro

Activates Ubuntu Pro



## Dependencies

#### Roles
None

#### Collections
None

## Platforms

Supported platforms

- Ubuntu 18.04 LTS<sup>1</sup>
- Ubuntu 20.04 LTS<sup>1</sup>
- Ubuntu 22.04 LTS
- Ubuntu 24.04 LTS
- Ubuntu 26.04 LTS

Note:
<sup>1</sup> : no automated testing is performed on these platforms


## Role Variables
### defaults/main.yml
<pre><code>
# Services to enable/disable:
ubuntu_pro_services:
  - name: usg
    enabled: true

# Execute hardening
ubuntu_pro_usg: false

# Hardening profile
ubuntu_pro_usg_profile: cis_level1_server

# Hardening tailoring template
ubuntu_pro_usg_tailoring_template: >-
  templates/tailor-{{ ubuntu_pro_usg_profile }}-{{ ansible_facts['distribution_version'] }}.xml.j2

# Hardening tailoring file
ubuntu_pro_usg_tailoring_file: /root/usg-tailoring.xml

# Hardening tailoring (deviation from default)
ubuntu_pro_usg_values:
  - name: var_network_filtering_service
    value: ufw
  - name: var_timesync_service
    value: chronyd
ubuntu_pro_usg_rules: []
</pre></code>




## Example Playbook
### molecule/default/converge.yml
<pre><code>
- name: sample playbook for role 'ubuntu_pro'
  hosts: all
  become: 'yes'
  tasks:
    - name: Include role 'ubuntu_pro'
      ansible.builtin.include_role:
        name: ubuntu_pro
</pre></code>
