# NodeJS Ansible playbook

[![Join the chat at https://gitter.im/cloudnative/bakery-examples](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/cloudnative/bakery-examples?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

Here is an example of how to install and configure a NodeJS application. This playbook has been tested on Ubuntu 14.04 and Amazon Linux 2015.03.

Here, we use the example NodeJS app from Heroku. You can find all of the configuration in the [`roles/webapp/defaults/main.yml`](./roles/webapp/defaults/main.yml) file.

## Bakery Build Pipeline

1.  Create a New Build Pipeline and give it a name
1.  Select either an Ubuntu or Amazon Linux base AMI with HVM virtualization
1.  Use the Bakery Examples Git repository with Ansible 1.9+
1.  The Path to Ansible playbook is: `nodejs/node-web-app.yml`
1.  Leave the rest blank and click *Create Pipeline*
1.  Build the AMI

Now you can launch an EC2 instance with the AMI, open port 80, and see the Hello World application running.

### Deploy using Delta

To deploy this using Delta, the ELB needs to send traffic to port 80 on the EC2 instances. There are no other special requirements.

## How does it work?

The `node-web-app.yml` file is an Ansible playbook that references a few roles. Those roles install some basic system packages, configure a `web` user, install NodeJS and Nginx, get a copy of the code using Git, install any required NPM packages, and then run the Node app using supervisor.

Take a look at the code and if anything isn't clear, ask on [Gitter Chat](https://gitter.im/cloudnative/bakery-examples).

