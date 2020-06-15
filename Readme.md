# Docker Swarm playground

## Description:

A set of ansible playbook ran by Vagrant to setup a 3 nodes Docker swarm. This is useful when you want to discover and
practice Docker administration.

## Usage:

First, clone the repo:

   ```
   git clone https://github.com/kevinwaro/docker_swarm_playground && cd docker_swarm_playground
   ```

Then let Vagrant create and provision the vms:

   ```
   vagrant up master node1 node2
   ```

Once everything is provisionned, you can ssh to the master node and start playing with the swarm:

   ```
   vagrant ssh master
   $ docker node ls
   ID                            HOSTNAME            STATUS              AVAILABILITY        MANAGER STATUS      ENGINE VERSION
   cz1sx7iobgyrsiuzsbycbnnj0 *   master              Ready               Active              Leader              19.03.11
   pnb11pvhybb0fiye6fvrwopr2     node1               Ready               Active                                  19.03.11
   jh6pw2a1flparrq1nczgmmn6q     node2               Ready               Active                                  19.03.11
   ```

## Credits:

* author: kevinwaro
* contact: kevinwaro@yahoo.fr

## License:

This project is licensed under the GNU GPLv3 License - see the [License.md](License.md) file for details
