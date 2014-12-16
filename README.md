# Bakery Examples

Here you will find examples illustrating how to use the [Bakery from CloudNative](https://cloudnative.io/).


## Usage

1.  Login to [CloudNative](https://cloudnative.io/)
1.  Go to your organization's dashboard
1.  Under the Bakery, add a new __Git Repository__ with the following details:

        Name:  Bakery Examples
        Clone URL:  https://github.com/cloudnative/examples-ansible.git
        Website URL:  https://github.com/cloudnative/examples-ansible
    
You can now use any of the examples below when creating a build pipeline.


## Examples

### Hello World

This is as basic as it gets. The [`hello-world.yml`](https://github.com/cloudnative/bakery-examples/blob/master/hello-world.yml) file is an [Ansible](https://github.com/ansible/ansible) playbook that installs the Apache web server. That's it.

To use:

1.  Create a new Build Pipeline.
1.  Give it a name, and choose whatever AWS region you like.
1.  Select either an Ubuntu or Amazon Linux base AMI
1.  Select the Git Repository you added earlier, and use the following

        Path or Ansible playbook:  hello-world.yml
    
1.  Click __Create Pipeline__ and the __Bake an AMI__
1.  Once the AWS resources launch, you will see Ansible installed, and the `hello-world` playbook executed.

That's it. You can now launch 1 or 100s of EC2 instances with your new AMI. (We don't even recommend 10s of instances for this particular example).


## About the Bakery

The Bakery is a an Amazon Machine Image (AMI) factory. Whenever your code changes, the Bakery will take those changes and build a new image from it. That image can be deployed to 1 or 1000s of EC2 instances. 

Why? Well that is really a matter of preference. Some (e.g. Netflix) like to build fully configured images containing their latest code, and use the same image for staging and promote it to production after testing. Others like to build an image containing just the dependencies for running their service, and get the code on boot (e.g. build an image with Ruby, Rails, and Nginx already installed and configured). You could even build an AMI containing a Docker image, so that when you launch 100 instances, they aren't all downloading the same Docker image on boot. The point is, it is a simple little factory, and how you want to use it is up to you.


## About CloudNative

[CloudNative](https://cloudnative.io/) is the interface between developers, operations and cloud. Our mission is to codify the best practices of running a service on Amazon Web Services. We do this by building native to AWS (i.e. no abstractions - take advantage of advanced features), staying current with changing best practices, and striking a balance between being opinionated vs flexible.


## Contributing

Want to fix a typo, or make an example run on your favorite OS? Fantastic! Just fork this repository and send us a Pull Request.


## License

Copyright 2014 CloudNative, Inc.

Licensed under the Apache License, Version 2.0 (the "License"); you may not use this file except in compliance with the License. You may obtain a copy of the License at

http://www.apache.org/licenses/LICENSE-2.0 

Unless required by applicable law or agreed to in writing, software distributed under the License is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the License for the specific language governing permissions and limitations under the License.
