iptables rules we used for our services (mainly fivem focusing, drop invalid packets, limits, etc) as iptables got replaced by nftables on newer debian (which we use)
 few things to note:
  - they might not be the best overall but most were crucial in our use case
  - the 444 ip whitelisted port was port of the database (phpmyadmin, mariadb) to allow only specified connections there.
  - the "red-button" chain was made for only when theres huge ddos attack as it drops so much packets (legit ones, it literally couldn't care less)
  - udp length etc was based on wireshark packets send back and forth and we could allow some packets to be dropped also (limited resources required limited acceptance)
