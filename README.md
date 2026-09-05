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
