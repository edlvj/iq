# Computer Science and Network

### Solve number 8 from 10 digit to 2 digit system and from 2 digit to 10 digit. 
8 in binary = 1000 
and 
1000 in decemical = 8

### How work HTTP caching?
We always must return Last-Modified or ETag Headers for clients.
If response body on server not changed we must return HTTP status - 304 Not Modified
If body changed we must return HTTP status - 200 Not Modified

### What is DNS and how does it works.
The Domain Name Systems (DNS) is the phonebook of the Internet. Humans access information online through domain names, like nytimes.com or espn.com. Web browsers interact through Internet Protocol (IP) addresses. DNS translates domain names to IP addresses so browsers can load Internet resources. 
For example:

If you enter in browser domain example.com
DNS resolver make request to DNS servers and find DNS record with his domain and redirect to IP of Server.

### How works ipv4 addressing.
An IPv4 address is made up of 32 binary bits, which is divided into a Network portion and Host portion with the help of a Subnet Mask.

The 32 binary bits are broken into four octets (1 octet = 8 bits). Each octet is converted to decimal and separated by a period (dot).

How IPv4 addresses look:
e.g. 127.0.0.1

127.0.0 - Network
.123 is Host
The network part of the address is likened to the house address, number or postcode.
The host part of the address is likened to an individual or person’s name on the mail who lives in that home.

### What is UUID?
Universally unique identifier (UUID) is a 128-bit number used to identify information in computer systems