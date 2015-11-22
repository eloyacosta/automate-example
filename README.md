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

$ curl -i -X POST http://192.168.100.2:8080/ep1 \
-H "Content-Type: application/json" \
-d '[
{"uid": "1",
  "name": "John Doe",
  "date": "2015-05-12T14:36:00.451765",
  "md5checksum": "e8c83e232b64ce94fdd0e4539ad0d44f"},
{"uid": "2",
   “name”: “Eloy",
  "date": "2015-05-13T14:36:00.451765",
  "md5checksum": "b419795d50db2a35e94c8364978d898f"}
]'

2. You can test API query

$ curl -i -X GET "http://192.168.100.2:8080/ep2?uid=1&date=2015-05-13"

# Unit Tests 

All the app has been written with Unittest.

To run the test, be sure you are still in the project directory (~/git/datarobot) and exec:

  * $ vagrant ssh
  * cd /home/www
  * pyton test.py



