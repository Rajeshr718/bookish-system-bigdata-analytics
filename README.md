# bookish-system-bigdata-analytics

Real-Time Telecom Revenue Assurance using Big Data and Data visualization  

Seamless real-time & batch processing of telecom transaction records

Abstract— Telecommunication industry has seen phenomenal
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

PROBLEM STATEMENT
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

After the calls are setup between the calling party and
called party and as the calls progress, the CDRs are generated
in the MSC. The CDR contains several fields including identity
of calling party and called party, call start date, call start time,
call duration etc. The CDRs contain meta-data about the call or
communication service usage which are useful for charging
and other management purpose, however they do not contain
the actual content of the call or communication.In this current
work, since the CDRs are used for their intended purpose of
rightful charging, the usage does not violatesubscribers’
privacy concern.The current work does not, in any way,
prioritize or block subscribers’ data content in the delivery
process. Thus, it does not raise any “Network Neutrality” (Net
Neutrality) issues. The format of the CDRs usually differs
among MSC equipment vendors. The formats of theCDRs are
also different between MSC and other downstream applications
like Billing System and Customer Care System which process
them. A Mediation Device receives CDRs from MSC,
performs aggregation and correlation among relatedCDRs and
reformats them to the format of the downstream application
like Billing System. The MSCs, Mediation Device, and Billing
Systems are from different vendors, and at times due to error in
interface between them, discrepancies crop up in some CDRs
as it passes through them. To address the problem of
discrepancy, the CDRs need to be reconciled between MSC
and the Billing System. Reconciliation is the process of
comparing records from multiple sources to verify their
accuracy.
When the charge duration between MSC and Billing side
for corresponding CDRs differ by more than a threshold, an
alert needs to be generated and saved. Corresponding CDRs are
matched by their respective values of calling party, called
party, call date, call direction, and allowable tolerance
threshold in call start time.
As per current deployments in various service provider
organizations, the reconciliation is an end-of-day processing
where reconciliation needs to be completed in a small window
of time during the off-peak hours, usually in the night. This
work attempts to suggest an approach which will be able to
support both the current deployment scenarios of batch
processing as well as the real-time reconciliation scenarios for
telecom service providers.
The scenario of the problem is described with the help of
Fig. 1. The CDRs from the MSC need pass to a few rounds of
filter to:
• Filter in only outgoing call CDRs
• Filter out CDRs which comes from hybrid customer types
based on information available from a look-up file.
• Filter out CDRs from post paid customer types
The Billing CDRs need to pass through one simple filter to
allow only outgoing call CDRs. The MSC and Billed CDRs
needs to be joined where calling party, called party, call date,
call direction are same in MSC and Billed CDR and Call Start
Time in MSC and Billed CDR are within a configurable
tolerance threshold of a few seconds. Finally, alerts needs to be
generated from the joined CDRs where the Charge Duration in
matched MSC and Billing CDR differ by more than a user
configurable threshold.
The purpose of current reconciliation process is to capture
and report in real-time, the CDRs between MSC and Billing
System, which are under-charged or over-charged beyond a
user-configurable tolerance threshold value.

