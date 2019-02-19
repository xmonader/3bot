# 3bot urls and ssl

In a 3bot record on the blockchain, an ip address and doublename (xxxxx.yyyyy) are registered.

The ip address is the one from the location where the 3bot is deployed. 

Every location runs a webgateway that directs the https requests to the proper 3bot. ssl termination is done on the 3bot itself

In order to serve the dns requests, a coredns infrastructure is needed that is fed with the information from the blockchain.
