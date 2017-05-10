# bookish-system-bigdata-analytics

## Real-Time Telecom Revenue Assurance using Big Data and Data visualization  

## Seamless real-time & batch processing of telecom transaction records

###### Abstract
Telecommunication industry has seen phenomenal
growth and intense competition in recent times. Basic connectivity
has been commoditized and service providers need to provide
personalized and differentiated services to stay competitive and
form lasting customer relationship. One of the ways they can do
this is by analyzing the data that are generated or pass through
their network in real-time, and use the insight to offer
personalized services promptly and dynamically. In this scenario
it will be immensely beneficial to them to have solutions which
allow them a smooth transition path from offline batch processing
of stored data to real-time analysis of data as it is available to
them. The current paper demonstrates an approach to address
the challenge of solution development using Stream Processing,
where the same solution can be used to process stored data in
offline mode and analyze data stream in real-time for actionable
intelligence. IBM stream processing platform Infosphere Streams
has been used for implementation of the solution proposed in this
work. As a further benefit, if some problem is discovered during
real-time analysis of data streams, the same program can be used
to analyze the stored data after necessary update is made to the
program. This work focuses on seamless dual mode processing of
both offline and real-time analysis. The approach has been
carried out with reconciliation component of telecommunication
revenue assurance and has used CDR (Call Detail Record) for
analysis. However, the approach is very generic and it can be
applicable in other areas of telecom like churn management,
campaign management and in other sectors, like Utilities, Banking
etc., which can benefit from real-time and seamless dual mode
processing of account transaction records.

###### PROBLEM STATEMENT
The reconciliation component of Telecommunication
Revenue Assurance system was taken as an example for
exploring different approaches to speed up high volume CDR
processing. The component reconciles CDR data from Mobile
Switching Center (MSC) and Telecommunication Billing
System. In a mobile communication network, the MSC
coordinates communication channels and necessary
processesfor end-to-end connection handling, mobility
management, routing charging and real-time account
monitoring. The initial work has been limited to the case of
reconciling pre-paid outgoing voice call because this use case
will benefit most through real-time reconciliation. Service
providers may have hybrid customers who use pre-paid and
post-paid services on the same account. Hybrid customers have
been excluded from this work, because their combined service
usage can be reconciled in suitable batch modes


