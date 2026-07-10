# 🛜 NETWORK DESIGN STEPS

Network protocol & designs determine the efficient travel path for Data transmitted

Heres a list of curical Steps taken when Designing a Network

-  Gathering Network Request
-  Selectng the right Topology (Topology; layouut of how Network devices are connected)
-  Consider Network Design Principles; Scalability, Resilience & security.
-  Choose Network Hardware.
-  Document the Network design (Via Network Diagrams;  Network Diagrams show how devices & components of a network connect and interact with each other).
-  Test and validate 

---
## Common Physical Network Topologies
-  bus Topology
-  Star Topology 
-  Ring Topology
-  Hybrid Topology 

### Bus Topology 

       uses a cable that runs throughout the Network called **BUS**
       Data is sent as broadcast and is recieved by all networked connected devices 
       
      **PROS**
        Easy to set-up
        Easy to Understand 

      **CONS**
        limited Scalability
        collision  Vulnerable
        Network Failure Risk due to single cable issue
        
### Star Topology
      Uses a Hub or Switch 
      Hubs are simple and less intelligent
      Switches are advanced & Able to Dedicate Routing Independently
      All devices connect and communicate via the hub/Swtich

      **PROS**
        Easy to implement 
        Single cable Failure doesn't bring down the whole netowrk
        Easy Admin operation that won't affect the Entire Netowrk
        
      **CONS**
        Switch/Hub is a cenetral failure point 
        Relatively expensive to bus Topology
        
## Ring Topology 
      All Devices are connected to at least two others
      Data flows in one direction
      all devices examine data send on the network; then passes it on to next device until it gets to intended recipient
      
      **PROS**
        Reduced Data collision
        Easy installation 

      **CONS**
        Network is disrupted by cable failure
        Network is distrupted by device removal
        
## Mesh Topology
      Devices are connected to mulitple other devices 
      web of connections are present 
      Data transmission is more complex in this topology

      **PROS**
        Highly reliable when adding or removing devices to the network
        
      **CONS**
        complicated set-up, management & Troubleshooting
        
      Types of Mesh Topologies: `Full mesh` & `Partial Mesh`
        Full Mesh:  Every Device is connected to each other      
                    High Redundancy levels 
                    Cabble and hardware intensive                    
                    
        Partial Mesh: some devices connect to every other
                      More Practical
                      offers some redundancy
                      
        
      









      
      

        
      
       
