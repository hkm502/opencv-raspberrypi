# opencv-raspberrypi
Update Raspberry Pi: (reboot may be required)
```
sudo apt-get update
sudo apt-get upgrade
sudo rpi-update
```
Install Ansible on Raspberry Pi:
```
sudo apt-get install python-dev python-pip
sudo pip install ansible
sudo mkdir /etc/ansible
sudo touch /etc/ansible/hosts
```
Clone Repository:
```
cd ~
git clone https://github.com/smadam813/opencv-raspberrypi.git
cd opencv-raspberrypi
```
Run Ansible Playbook:

**Important:** If not using a Raspberry Pi 2, change `raspberrypi_core_count` located in `opencv-raspberrypi.yml` to match the number of cores your Pi has before executing the playbook.
```
ansible-playbook opencv-raspberrypi.yml --ask-sudo-pass
```
**Note:** The `make` command will take **HOURS** to run on a Raspberry Pi.
