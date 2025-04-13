vagrant init bento/ubuntu-20.04
vagrant up

==> default: Mounting shared folders...
    default: C:/Users/stefa/Desktop/todo-api-node-js-mongo => /vagrant

vagrant ssh

https://www.mongodb.com/docs/manual/tutorial/install-mongodb-on-ubuntu/#install-mongodb-community-edition

Import the public key.
sudo apt-get install gnupg curl

curl -fsSL https://www.mongodb.org/static/pgp/server-8.0.asc | \
   sudo gpg -o /usr/share/keyrings/mongodb-server-8.0.gpg \
   --dearmor

echo "deb [ arch=amd64,arm64 signed-by=/usr/share/keyrings/mongodb-server-8.0.gpg ] https://repo.mongodb.org/apt/ubuntu noble/mongodb-org/8.0 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-8.0.list

sudo apt-get update

sudo apt-get install -y mongodb-org

<!-- sudo systemctl daemon-reload -->

sudo systemctl start mongod
sudo systemctl enable mongod


###
sudo apt update
sudo apt install nodejs -y
node -v
sudo apt install npm -y
sudo npm install pm2 -g

cd /vagrant
pm2 start index.js


-----

cat /proc/cpuinfo

------

wget -qO - https://www.mongodb.org/static/pgp/server-4.2.asc | sudo apt-key add -

echo "deb [ arch=amd64,arm64 ] https://repo.mongodb.org/apt/ubuntu focal/mongodb-org/4.2 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-4.2.list

echo "deb [ arch=amd64,arm64 signed-by=/usr/share/keyrings/mongodb-server-4.2.gpg ] https://repo.mongodb.org/apt/ubuntu focal/mongodb-org/4.2 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-4.2.list

sudo apt-get update

sudo apt-get install -y mongodb-org=4.2.0



-------

curl -fsSL https://www.mongodb.org/static/pgp/server-4.2.asc | \
   sudo gpg -o /usr/share/keyrings/mongodb-server-4.2.gpg \
   --dearmor

echo "deb [ arch=amd64,arm64 signed-by=/usr/share/keyrings/mongodb-server-4.2.gpg ] https://repo.mongodb.org/apt/ubuntu focal/mongodb-org/4.2 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-4.2.list

sudo apt-get install -y mongodb-org=4.2.0

--------

{
    "status": [
        "completed"
    ],
    "name": "Finish This"
}
