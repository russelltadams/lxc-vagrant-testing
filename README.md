# lxc-vagrant-testing
testing using lxc with vagrant

Set it up

# Install all the pre-reqs:
1. 16.04 (or figure out how to get lxc working 14.04, need to add some repos, etc...)
2. apt-get the lxc stuff - "sudo apt install lxc"
3. install Vagrant - get coffee, look up how the kids are doing it today, do it, good luck
4. install lxc vagrant plugin - "sudo vagrant plugin install vagrant-lxc"

# open 3 terminals:
1. run in term 1 "sudo lxc-ls --fancy" will list running container and there state and IP
2. run in term 2 "sudo lxc-top" will list contain CPU and MEM and some IO usage
3. run in term 3 "vagrant lxc sudoers" then "vagrant up" ("vagrant lxc sudoers" will put vagrant in sudo as a workaround having to provide sudo password all the time, this is a lxc provider issue)

# Interact with container at their CLI
1. "vagrant ssh $host" to ssh to it the vagrant way
2. lxc-attach -n $host (container name, which could be different than host, see Vangrantfile) to console up via lxc
3. If your networking worked out, you can ssh directly to the IP if/once a key is in place

# Profit
