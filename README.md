# fun-bash-tools

 A "server" serving a single character (.) with log functionality.
 
 -v verboose -n noresolve -l listen -p port -q 1 quit after x seconds
 
 ">> tmplogg2 2>&1" = log funtion with stdout AND errout. netcat uses both to print info.

To have a unpriviledged user recieve web traffic at port 80(http) rerouting it localy. As root run:

iptables -A PREROUTING -t nat -p tcp --dport 80 -j REDIRECT --to-ports 4616

iptables -t nat -A OUTPUT -o lo -p tcp --dport 80 -j REDIRECT --to-port 4616
