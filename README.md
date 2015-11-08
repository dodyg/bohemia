# bohemia
An implementation of IATA's [NDC (protocol)](https://www.iata.org/whatwedo/airline-distribution/ndc/pages/default.aspx) aggregation network.

The goal is to create a public utility aggregation network where airlines, travel agents and online travel agent to have access to wide ranges of airlines's offering (tickets, ancilliary offers, etc) for free or nearly free.

The software should be cloud enabled and can be deployed by anyone. A new server will be able to join and discover the network with the most minimum of configuration. 

It should be trivial to increase the power of the network to server more increasing demands for data query:

- Step 1. Purchase a cloud/vps
- Step 2. Install Bohemia.
- No step 3.

The travel apps and websites should be able to just point to any url of a server participating in the network and have access to all the scheduling and pricing information of airline tickets based a given departure/arrival point.

