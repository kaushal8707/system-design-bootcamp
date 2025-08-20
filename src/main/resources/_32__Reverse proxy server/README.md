
 # Reverse proxy server
 
   Forward Proxy    —   Hides The Client.

   Reverse Proxy    -   Hides The Server.
   
   

 # When to use Reverse Proxy

   1. When I don't want to expose the server

            we use amazon.com.

            amazon.com orders, amazon.com searchs there are so many websites and so many endpoints.

            Is there only one server??

            No there will be a multiple servers. 

            so there are many servers so that many website will not create like amazonorder.co, amazonpay.com, amazoncart.com...

            so what we can do because there will be multiple servers so to hide the complexity we will keep only one server and we
            named amazon.com Internally calls will get redirected. it will see if this is for cart then this will go to this server,
            if this is for payments then this will go to this server, this call is for order then this will go to this server.
            now we kept a layer which mean abstraction layer to show to customer see this is the only one website amazon.com
            and only one domain name. we do not know what is the actual ip address so this time amazon.com behaves like a reverse
            proxy. so here it hides the actual servers.


            suppose we have only one server and i want to hide the ip address of my actual server then what i will do i will
            put reverse proxy in between. so, people will hit reverse proxy server and then reverse will hit the actual server.
            people will think reverse is the actual server but no actual server identify we keep hidden.


   2. To make user feel there is only one server


   3. Provide Load Balancing for the server

            now amazon.com will become a virtual ip address and inside that server i have written which calls will go to
            which servers that behave like a load balancer.

   4. Allows administrators to swap the backend servers without disturbing the traffic.
     

   4. Filter out some requests

            suppose we have an endpoint netflix.com/plans and all plans comes under this endpoint like for
            for 1 month, 2 month, 3 month..etc. I want that person should only access GET calls not POST and PUT.
            So, Reverse Proxy will handle this. when any user trying to hit a POST call he want the plan is of 100 now
            should changed it to 1 rupees then Reverse Proxy is smart he won't allow this request is go to actual server.
            

 # Industrial UseCase

   API Gateway
   
    The example we saw for amazon.com is an example we saw for api gateway.



 In Between Client and Server we putted a Layer of API Gateway. Client will hit on a Virtual IP of API gateway
 In Virtual IP there is a mapping,  we have written what is the actual IP address 