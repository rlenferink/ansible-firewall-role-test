# Test for Ansible firewall role issue #234

See https://github.com/linux-system-roles/firewall/issues/234

Based on https://github.com/linux-system-roles/firewall/pull/237

## Usage

```bash
# Install dependencies
ansible-galaxy role install -r requirements.yml --force

# Since the inventory file defines hardcoded IP addresses, test availability of nodes with the following command
ansible-playbook -i inventories/ test_node_availability.yml

# Test for the actual issue
ansible-playbook -i inventories/ tests_issue_234.yml -vv
```
