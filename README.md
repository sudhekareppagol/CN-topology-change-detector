# CN-topology-change-detector
# Topology Change Detection using Mininet

## Objective
To detect changes in network topology dynamically using Software Defined Networking (SDN).

## Tools Used
- Mininet
- Ubuntu

## Steps Performed
1. Created network using:
   sudo mn --topo linear,3

2. Checked topology:
   net

3. Tested connectivity:
   pingall

4. Simulated link failure:
   link s1 s2 down

5. Tested again:
   pingall

6. Restored link:
   link s1 s2 up

## Results
- Network works normally initially
- When link is down, communication fails
- After restoring link, network recovers

## Test Cases
1. Normal Case:
   All links active → Successful communication

2. Failure Case:
   Link down → Communication fails

3. Recovery Case:
   Link restored → Communication resumes

## Analysis
- Initially, all hosts communicate successfully.
- When the link between switches is brought down, packets cannot reach destination.
- This shows how topology change affects network connectivity.
- When the link is restored, communication resumes.

## Conclusion
The experiment demonstrates that network behavior changes dynamically when topology changes occur.
