
# Scalability

    Scalability means If the Number of Requests Increased then Your System will goes Down or will work,
    which mean WOuld be a Response Time increased or will be the same.

    

# Difference Between Horizontal & Vertical Scaling

   Vertical Scaling
        
    Suppose you have a machine then you are going to add a configurations in a same machine.

    Suppose you have a laptop and you make it as a server, suppose you user were 100 after a month your user becomes 1 lakhs 
    then what you will do you will think to increase a RAM, In database data increaseing so let's add Hard Disks so, In this
    case we are doing Vertical Scaling.

    We have a machine we have a Server so, what i am doing i am making a better configuration of our same machine so, this is called
    Vertical Scaling.

   # Pros

        -Easy Implementation , simply added a additional RAM.
        -Less Power , since one machine so ll take less power.
        -Management is Easy , since one machine so management ll be easy..

   # Cons

        -SPOF (single point of failure) - you have a machine you made it as a server now 1000 requests are coming into it
                                          so might be tmrw 1 million requests will come so what we did we added RAM, we added
                                          SSD(Hard Disk) earlier 1 TB HD now 1 10 TB HD but we have only one machine suppose if
                                          there is any fault occurred then machine will goes down. so, Single Point of Failure.
        -Limit  -   you can increase Dard Disk size at a limit only right.
        -Price - since only one machine so resources you are adding should be high quality.


   Horizontal Scaling
   
    Suppose we have a distributed system, we have a database of 100 GB, so, what i will do I will take 4 servers and 25 GB
    each i will keep the database storage. so, this is a distributed systems.

    Suppose now we required 125 GB so what i will do i will add one more server and keep storage of 25GB.

    So, what i am doing here in a Single Machine i am not adding Configurations vertically instead, I am bringing a new Machine
    this is called Horizontal scaling.


   # Pros

        -SPOF (single point of failure) - Not a single point of failure because there will be multiple systems every machines
                                         having a copies or replicas if one machine goes down then replicas will come at place.
        -Limit  -   In one machine we are not doing add on so we can buy a cheap resources.
        -Price - since multiple machines so you can buy a cheap resources as well..

   # Cons

        -Tough Security , security will be tough, because more resources you have to secure.
        -More Power Consumption, more power consumption
        -Management is Difficult , since one machine so management ll be easy..
    

    

    