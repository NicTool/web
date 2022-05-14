# DNS DICTIONARY

- **Resource Record**: structured data associated with names / nodes
    - format: owner ttl class type rdata
    - example: www.example.com 3600 IN A 192.0.2.127
- **owner** / name:
    - a node in the domain name tree
    - for a specific RR, _owner_ is the domain name where the RR is found. (RFC 1034 3.6)
    - consists of a sequence of labels
    - format: node.zone.tld.
        - the right most label is null, aka the root
        - the 2nd from right is the top level domain
        - the 3rd from right is the [organizational] domain name (usually)
- **label**: character strings between the dots in a domain name
- **ttl**: time to live
    - how long to cache this DNS resource record
- **class**: IN, internet.
- **type**: the type of rdata that follows
    - examples: A, MX, SOA, PTR
- **rdata**: resource data. The contents vary widely by RR type
    - examples: A records have an address, CNAME records bear a cname target, NS records point to nameservers (nsdname).

- **domain**: an administrative boundary within the domain name tree.
- **subdomain**: a domain contained by another domain. (ex: c.b.a is contained by b.a.)
- **node**: a leaf or interior node in the domain name tree. (RFC 1034, 3.1)
- **domain name**: the domain name of a node is the list of labels from the node to the root of the tree. A domain name identifies a node. (RFC 1035 3.6)
