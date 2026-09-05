# 🛜 NETWORK DESIGN STEPS

Network protocol & designs determine the efficient travel path for Data transmitted


---
## Common Physical Network Topologies


### Bus Topology 

       uses a cable that runs throughout the Network called **BUS**
       Data is sent as broadcast and is recieved by all networked connected devices # 🛜 Network Design Steps

Network protocol and design determine the most efficient path for data to travel. Here's a list of crucial steps taken when designing a network.

<details>
<summary>📝 <b>Steps in Designing a Network</b></summary>
<br>

1. Gather network requirements
2. Select the right topology (topology = the layout of how network devices are connected)
3. Consider network design principles — Scalability, Resilience & Security
4. Choose network hardware
5. Document the network design (via network diagrams — showing how devices and components connect and interact)
6. Test and validate

</details>

---

## 🔀 Common Physical Network Topologies

<details>
<summary>🚌 <b>Bus Topology</b></summary>
//

Uses a single cable that runs through the network, called the **bus**. Data is sent as a broadcast and received by all connected devices.

| ✅ Pros | ❌ Cons |
|---|---|
| Easy to set up | Limited scalability |
| Easy to understand | Vulnerable to collisions |
| Network failure risk from a single cable issue |

       **PROS**
        Easy to set-up
        Easy to Understand 

      **CONS**
        limited Scalability
        collision  Vulnerable
        Network Failure Risk due to single cable issue

</details>

<details>
<summary>⭐ <b>Star Topology</b></summary>
<br>

Uses a hub or switch — all devices connect and communicate through it.
- **Hubs:** simple, less intelligent
- **Switches:** advanced, able to route independently

| ✅ Pros | ❌ Cons |
|---|---|
| Easy to implement | Hub/switch is a central point of failure |
| A single cable failure doesn't bring down the whole network | Relatively more expensive than bus topology |
| Admin operations don't affect the entire network | |

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

</details>

<details>
<summary>🔁 <b>Ring Topology</b></summary>
<br>

All devices connect to at least two others; data flows in one direction. Each device examines the data sent on the network, then passes it on to the next device until it reaches the intended recipient.

| ✅ Pros | ❌ Cons |
|---|---|
| Reduced data collisions | Disrupted by cable failure |
| Easy installation | Disrupted by device removal |

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
        

</details>

<details>
<summary>🕸️ <b>Mesh Topology</b></summary>
<br>

Devices connect to multiple other devices, forming a web of connections. Data transmission is more complex in this topology.

| ✅ Pros | ❌ Cons |
|---|---|
| Highly reliable when adding or removing devices | Complicated setup, management & troubleshooting |

**Types of Mesh Topologies:**

| Type | Description |
|---|---|
| **Full Mesh** | Every device connects to every other device · high redundancy · cable/hardware intensive |
| **Partial Mesh** | Some devices connect to every other device · more practical · offers some redundancy |

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
                      

</details>
       
            

        
      









      
      

        
      
       
