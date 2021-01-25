# Recursive-DNS-Resolver

# The Project
You’ll find a resolve.py file in the repo. This file contains code that approximates the functionality of the host program. The program takes a domain name, and returns a summary of DNS information about the domain. For example, given the domain “yahoo.com”, host returns the “A”, “AAAA” and “MX” records for the domain. You can test this out by running the resolve.py command as so: python resolve.py yahoo.com.

You can lookup multiple domains in the same execution by passing multiple domains to the program (e.g. python resolve.py first.com second.edu third.org).

resolve.py currently queries a DNS server (8.8.8.8) to find information about domains. That DNS server handles the recursive part of DNS for you (i.e. 8.8.8.8 by default doesn’t know where to find yahoo.com, so it asks a root server, and the root server tells 8.8.8.8 where to find information about .com, so then 8.8.8.8 asks the new server where to find yahoo.com, etc.)

The IP addresses of the root servers are hard coded into the resolve.py in the global ROOT_SERVERS list. Your program should start by querying one of these servers. A very good first step in your solution will be to find where 8.8.8.8 is in the code currently, and make sure you instead query one of the root servers.

