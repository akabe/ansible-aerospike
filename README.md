# ansible-aerospike

Ansible playbook for Aerospike

```
ansible-playbook -i inventory aerospike.yml
```

where file `inventory` is

```
[aerospike]
10.0.0.1
10.0.0.2
10.0.0.3
...

[all:vars]
ansible_ssh_common_args='-F ./ssh_config -o StrictHostKeyChecking=no'
aerospike_mesh_seed_address=10.0.0.1
```

and file `ssh_config` is

```
Host *
  IdentityFile ~/.ssh/my_private_key
  User ec2-user
```
