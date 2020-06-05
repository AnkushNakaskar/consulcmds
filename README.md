# consulcmds
This project explain the consul cmds to be used in consul client or consul server


* How to list down the consul services registered on consul
  * consul catalog services
* How to call service API using consul
  * First open ``` vi /etc/resolv.conf ```
    * Update and add ``` nameserver 127.0.0.1 ``` on first line
    * This is added so that API will look up for service name in local consul client when you do ping using service name.
      * else this is check with google.
  *  Try ping the server example : ``` ping content-referencedata.service.consul ```    
  * Call API using the service name now example : ```curl "content-referencedata.service.consul:8012/api/referencedata/genre/11" ```
  
### This all process will work if you have consul client if not then try the same on consul server, it should work since , namespace with check for local consul  server.

