## What is this?
If you have been linked to this page, you have probably encountered one of our scanners.
Below we will explain the nature of these scans.
This is a research project from Erik Lamers and Vincent van der Eijk organised by the University of Amsterdam Security and Network Engineering master.

Our project consists of looking for port based security differences between dual stack hosts.
This is achieved by scanning the public internet for dual stack hosts based on existing datasets.

## Why is this necessary?
"Don't Forget to Lock the Back Door! A Characterization of IPv6 Network Security Policy" Czyz et. al. (2016).
Already showed us that there is a major difference between IPv4 and IPv6 port based security policies.
We are now 3 years later and IPv6 adoption is growing. So it's important to see what is the current status quo.

Also we are planning to inform all system administrators with a difference in security policies automatically, 
based on WHOIS information.


## Ethical considerations
Our research involves active probing of on the public Internet.
To minimize our impact on the various stakeholders,
we will adhere to the guidelines of the Menlo Report while conducting our research:
* We will only use public available information to identify hosts and corresponding email addresses. (e.g. WHOIS, DNS information).
* The probing of hosts will consist of establishing a connection with the host and performing a banner grab and protocol information (SYN + service discovery), without further exploration into the correctness of authentication of the given protocol.
* We will utilize the proven ZMap host distribution algorithm to disperse load across networks as it is a accepted best practice in the security community.
* An opt-out feature will be made available so SA’s can contact us, and we will exclude their IP range from the target list.
* A host is defined as reachable by ICMP echo request. This is intentional, as there is a good  chance that a SA who does not want their network scanned will block ICMP echo requests. Thus by this host definition those hosts will automatically be excluded.

A far more detail ethical paragraph will be included in the paper itself.
### How do I opt out?
[Opt out form](https://docs.google.com/forms/d/e/1FAIpQLScbBEUITDSsKA97qz0USSDljronYmk3p-IDOOxN68rCoiRK9A/viewform?usp=sf_link)
