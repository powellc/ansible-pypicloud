Ansible pypicloud
=================

Simply a set of Ubuntu/Debian Ansible playbooks for building a usable
pypicloud application server. The best thing pypicloud has going for it
over the other host-your-own pypi servers? Default storage is on S3 which
means the server can be rebuilt very quickly, or made redundant.

This demonstrates that by allowing to spin up multiple mirrors of your
personal pypiserver making it both fast and redundant, which until 
recently, pypi.python.org could not claim.

Usage
-----

1. Copy the group_vars configuration example files into their respective group names (e.g. production.example -> production), 
2. Copy the hosts.example file over to hosts
3. Add you server IP addresses or DNS names to the respective groups
4. Run: ansible-playbook -i hosts provision.yml --limit <local|staging|production>
5. Go use your new personal pypi server!
