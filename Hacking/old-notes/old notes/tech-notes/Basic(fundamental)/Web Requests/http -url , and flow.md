![url_structure.png](../../../_resources/url_structure.png)

![2023-07-20_14-16.png](../../../_resources/2023-07-20_14-16.png)

**http flow**

![HTTP_Flow.png](../../../_resources/HTTP_Flow.png)

Note: Our browsers usually first look up records in the local '/etc/hosts' file, and if the requested domain does not exist within it, then they would contact other DNS servers. We can use the '/etc/hosts' to manually add records to for DNS resolution, by adding the IP followed by the domain name.

Once the browser gets the IP address linked to the requested domain, it sends a GET request to the default HTTP port (e.g. 80), asking for the root / path. Then, the web server receives the request and processes it. By default, servers are configured to return an index file when a request for / is received.

**HTTPS FLOW**

**![HTTPS_Flow.png](../../../_resources/HTTPS_Flow.png)**