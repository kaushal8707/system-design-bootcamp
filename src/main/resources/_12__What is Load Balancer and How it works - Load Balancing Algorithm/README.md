
# Load Balancer

    Suppose one person sending a REQUEST and there are 3 nodes then who is going to decides REQUEST will go to which node so, laod Balancer will decide.

    Load Balancing is the process of efficient distribution of network traffic across all nodes in a distributed system.

        How to distributes the REQUEST across all the nodes will be decided by a Load Balancer.

    Responses will be same because all the nodes are redundant. same code base on each nodes. 

    

    Suppose you have created a JAR and you want to deploy. since there are 4 serevrs so on all 4 servers you have deployed the same JAR.
    now we have a VIP (virtual IP) like xyz.com. now this xyz is not an IP so we say virtual ip. so, in our chrome we entered xyz.com
    now the REQUEST will go to the Load Balancer, Now In a Load Balancer we have written a code like when xyz request  will come then on 
    which node or IP this REQUEST should go. each nodes are having a specific ip address. 


 # Roles of Load Balancer

    1. The load distribution is equal over every nodes, It should not be like none of teh REQ are going on a particular node or
       all the REQ are going only a particular node. so, should be equal distribution.

    2. Health Checks - (If the node is not operational the REQ will pass to another)

        suppose you have 4 nodes so load balancer will keep check which nodes are are working fine and which nodes
                       are not working fine. suppose health check response not came from one node then from next time load balancer
                       will not send a REQ on that particular node. 

    3. Load Balancers ensures high scalability, high throughput and high availability.

            High availability - through health check he can identified either nodes are up or not so in case node is down so
            load balancer will re-direct the request to another working nodes. 

            High throughput - high throughput will be achieved because it is high availability.

            High scalability - because you are horizontally scalling your application and who is helping in scalling is the LB only,
                               suppose we have a 4 nodes and 4 extra nodes we have added also then who is ensuring that that 4 nodes also
                               we are going to use is by Laoad Balancer only.

 # When to use it and when not to ?

    In Monolithic or in case of Vertically Scaled System we don't need it. so no need to use in monolithic system because we will
    have only one server. so, In monolithic we scaled vertically not horizontally. so, in monolithic we will have only one machine so
    load balancer not required.

        In case of Microservice architecture or in a distributed systems we scaled horizontally mean we are having more then one machines
        so on all machines equal load coming which is ensuring by a load balancer. 

 # Challenges of Load Balancing ??

    Single Point of Failure - During a load balancer malfunctioning, the communication between clients and serevr would be broken.
                              To solve this issue we can use redundancy, the system can have active load balancer and one passive load
                              balancer. 
                                suppose a load balaner is itself stop working which mean a single point of failure so, to overcome this 
                               we will bring one more passive load balancer. so, another will be in a passive state so once active state
                               LB will be then the passive lb will start processing.

 # Advantages of using Load Balancers ??

    1. Optimisation:    Load Balancers helps in resource utilisation and lower response time, thereby optimising thesystem in a 
                        high traffic environment. 

                        It helps in resource utilisation, suppose we have 10 machines and we are just using either 1 or 2 or 3..then rest 
                        6 to 7 systems are useless. so, load balancer will do equal utilisation so that all resources should get in use
                        and response time also should be less. 

    2. Better user experience:      Load Balancers help in reducing the latency and increasing availability, making the user requests
                                    go smoothly and error-free.

                                    If high availability so we will have a better user experience. if one server get down then lb will redirecct
                                    to a running server.

    3. Prevents Downtime:       Load Balancers maintain a record of servers that are non operationals and distribute the traffic accordingly,
                                therefore ensuring security and preventing downtime, which also helps increase profits and productivity.

    4. Flexibility:     Load balancers have the flexibility to re-route the traffic in case of any breakdown and work on server maintenance,
                        to ensure efficiency. This helps in avoiding traffic bottlenecks. 

                        suppose if u add one 10 servers more then you just do entries in load balancer then it will start working and we can
                        identified also on a load balancer which server is down or throws an error and which server is working fine and what is
                        the response time of which server. 

    5. Scalability:     When the traffic of a web applications increases suddenly, load balancers can use physical or virtual servers
                        to deliver the responses without any disruption. 

    6. Redundancy:      Load balancing also provides in-build redundancy by re-routing the traffic in case of failure.



 # Load Balancing Algorithms

    1. Round Robin (Static) - Rotation Fashion. like if we have 3 server so 1st req-1st server, 2nd req-2nd server, 3rd req-3rd server,
                              4th req-1st server....which mean in a rotation fashions it routes the requests. 

    2. Weighted Round Robin (Static) -  It is similar to the Round Robin When the servers are of different capacities (some node can have
                                        better resources other might not have). so 1st it will see the capacities and send the requests accordingly
                                        in a round robin fashion. 
            
                                        if we have 3 server and 1st server capacity to server 3 requests ,  so 1st req-1st server, 2nd req-1st server, 3rd req-1st server,
                                        4th req-2nd server, 5th req-3st server, 6th req-1st server...so on

    3. IP Hash Algorithm (Static) - The servers have almost equal capacity, and the hash function(input is source IP) is used for random or unbiased
                           distribution of requests to the nodes. 

                            I sent a request xyz.com, request went to a load balancer, load balancer will see the user machine IP address, he took ip address
                            applied a Hash Function on it some output will come, corresponding to that output will decide which server it need to send a REQUEST. 

                            user send request  -> load balancer see user ip address -> apply hash function(source ip address) -> send to that specific particular server.

    4. Source IP Hash (Static) - Combines the Server and Client's Source and destination ip addresses to produce a Hash key. The Key can be
                                 used to determine the requests distribution.

                            suppose there is some requirent like every time a request will come it should go to a particular server only.
                            in that case this source ip hash will come into picture.

    5. Least Connection Algorithm (Dynamic) -  Client requests are distributed to the application server with the least number of active connection
                                               at the time the client request is received.
    
                                               Load balancer will see whose nodes is having less no. of active connections, the nodes having
                                               less active connections our requests will go there. 

    6. Least Response Time (Dynamic) - The request is distributed based on the server which has the least response time.
                            
                                        Request will come Load Balancer will find out for this Request on which Node it should go so that least 
                                        response time will come. so, It will redirect to that node/server only whose response time will be less.


  ** static - static means it's already pre-defined that which Request will go on which server.
  
  ** dynamic - at runtime load balancer will be deciding who is having the least active connections and who can give in a less response time. 