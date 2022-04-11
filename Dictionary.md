# DNS DICTIONARY

- **Resource Record**: structured data associated with names / nodes
    - format: owner ttl class type rdata
    - example: www.example.com 3600 IN A 192.0.2.127
- **owner** / name:
    - a node in the domain name tree
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
