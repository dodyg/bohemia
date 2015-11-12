# bohemia
An implementation of IATA's [NDC (protocol)](https://www.iata.org/whatwedo/airline-distribution/ndc/pages/default.aspx) aggregation network.

The goal is to create a public utility aggregation network where airlines, travel agents and online travel agent to have access to wide ranges of airlines's offering (tickets, ancilliary offers, etc) for free or nearly free.

The software should be cloud enabled and can be deployed by anyone. A new server will be able to join and discover the network with the most minimum of configuration. 

It should be trivial to increase the power of the network to server more increasing demands for data query:

- Step 1. Purchase a cloud/vps
- Step 2. Install Bohemia.
- No step 3.

The travel apps and websites should be able to just point to any url of a server participating in the network and have access to all the scheduling and pricing information of airline tickets based a given departure/arrival point.

# Scenario

A simple scenario for aggregate works like this:

- User looks up Istanbul to London. This is a popular route and 30 airlines provide direct/indirect flights. We know there are 30 airlines service this route because we will have a registry that matches routes and airlines.
- Now we have to make decision whether to go to Airlines' web service to obtain their latest offers or use cache.
- Now off course offers from 30 airlines with their possibly routes might be way too much for consumers so you stash these results somewhere and return a pruned version of the result to the customer. You will probably also do some processing and make decisions which part of these results will go to cache. When customer needs to do paging, you go back to the previously stashed version and processed those.

The characteristics I am looking for as follows:
- Make it easy to add servers and install the software and have it automatically joined to the query network.
- Make it easy to deal with dead nodes
- Simple programming model

#Resources

- [http://ndc.developer.iata.org/](http://ndc.developer.iata.org/)
- The other good guys - [OpenNDC](http://open-ndc.org/)
