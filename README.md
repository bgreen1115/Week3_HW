This Ansible playbook is run against a lab consisting of 2 Juniper vSRX firewalls and 2 Cisco
CSR1000V routers.  The playbook utilizes the NAPALM Ansible library to retrieve the device 
facts, which are then parsed and the desired data is populated into a Jinja2 template 
(Device_template.j2) to provide a report (Facts_output.txt) showing the device Vendor, hostname,
uptime, OS Version.  The raw output of the retrieved facts is saved to device files as 
JSON (ie CSR1.json, vSRX1.json, etc.).
