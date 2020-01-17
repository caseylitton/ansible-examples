# Inventory
* https://docs.ansible.com/ansible/latest/user_guide/intro_dynamic_inventory.html#inventory-script-example-aws-ec2

## Manual
curl https://raw.githubusercontent.com/ansible/ansible/devel/contrib/inventory/ec2.py >> ec2.py
chmod +x ec2.py

export MY_PROFILE='default' && python ec2.py --list --profile $MY_PROFILE > "$MY_PROFILE-ec2.json"

export MY_PROFILE='production' && python ec2.py --list --profile $MY_PROFILE > "$MY_PROFILE-ec2.json"
