# Practice test 

1. Install VirtualBox
2. Install Vagrant
3. Install Ansible
  * Ubuntu/Debian: $ sudo apt-get install ansible
  * RH/CentOS: $ sudo yum install ansible
  * MacOSX: $ sudo pip install ansible
  * More info: http://docs.ansible.com/ansible/intro_installation.html
4. Clone this repo to your prefered route in the local fs (ej: ~/git/)
  * $ git clone https://github.com/eloyacosta/datarobot.git
5. Change to dir ~/git/datarobot
6. Exec command: 
  * $ vagrant up

# Some Request testing

Note: Vagrant run the virtual server with the IP address 192.168.100.2

1. You can test to post some data

* $curl -X POST http://192.168.100.2:8080/ep1 -H "Accept: application/json" -H "Content-Type: application/json" -d '[{"date": "2015-11-20T14:48:00.451765", "uid": "3", "name": "Perry Manson", "md5checksum": "2ebf36e266bae03f4f7c312d9c82a052"},{"date": "2015-11-20T14:50:00.451766", "uid": "4", "name": "Eloy Acosta", "md5checksum": "c193dab16230b3ef1eafc64570cff69e"},{"date": "2015-11-19T10:20:00.451770", "uid": "1", "name": "DataRobot user", "md5checksum": "8949b7957f976a5f0f4e8e88316f3cc6"},{"date": "2015-11-20T14:53:00.451768", "uid": "4", "name": "Eloy Acosta", "md5checksum": "6067ce211d11fc938e5ad835d82412b1"},{"date": "2015-11-20T12:00:00.451769", "uid": "3", "name": "Perry Manson", "md5checksum": "987ae0f34facc13a5b38434b5293a9e5"},{"date": "2015-11-19T10:20:00.451770", "uid": "1", "name": "DataRobot user", "md5checksum": "8949b7957f976a5f0f4e8e88316f3cc6"}]'

2. You can test API query

* $ curl -i -X GET "http://192.168.100.2:8080/ep2?uid=1&date=2015-05-13"

# Unit Tests 

All the app has been written with Unittest.

To run the test, be sure you are still in the project directory (~/git/datarobot) and exec:

  * $ vagrant ssh
  * cd /home/www
  * pyton test.py



