# Laboratory 08 – Mission Reflection

## Mission Reflection

What I learned from this laboratory activity is the need to secure cloud servers using a host-based firewall. Host-based firewalls are effective in controlling both incoming and outcoming network traffic on the server. They are used even when there is no other method for securing the server against any attacker since they limit the connections to the protected service even in cases when attackers bypass the network perimeter.

It is important to manage the open network ports as each of them creates an opportunity for a possible security breach by the attackers. It may happen due to scanning of the server in order to find some open ports and use them for attacks. By opening only those ports that are really necessary, such as port 22 for SSH protocol and port 8080 for the web application, it is possible to enhance the security of the server.

Opening of the database port such as the MySQL port 3306 to all may lead to serious problems since attackers may conduct any actions against it and try to get the confidential information stored there. Access to the database service should be restricted to the only authorized applications.

So I learned, completing this mission, I have learned how quickly the server becomes vulnerable if its administrators ignore the issues of security configuration. It became clear for me that the deployment of the application itself is not enough and that it is also important to monitor the connections and do the configuration properly. Thus, UFW was useful in illustrating the firewall rules.

Doing and making my GitHub Cloud Computing portfolio more and more complete having completed eight laboratory missions on cloud computing topics.
