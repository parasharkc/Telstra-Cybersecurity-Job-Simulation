# Telstra-Cybersecurity-Job-Simulation

## Objective

The Telstra Cybersecurity Job Simulation program aimed to replicate real-world cybersecurity scenarios faced by the Telstra team. The focus was on responding to distributed denial-of-service (DDoS) attacks by triaging alerts, analyzing malware behavior, and mitigating threats through firewall rule implementation. This hands-on experience was designed to enhance skills in threat detection, incident response, and post-incident analysis, deepening the understanding of attack patterns and defensive measures.


### Skills Learned

- Malware analysis
- Incident response
- Firewall rule development
- Technical report writing

### Tools Used

- Security Information and Event Management (SIEM) system for log ingestion and analysis.
- Network analysis tools (such as Wireshark) for capturing and examining network traffic.
- CISA for gathering information about vulnerability
- Python to develop firewall rules
- Firewall configuration
- Network traffic analysis
- Incident management systems.


## Steps
Task 1 : The Firewall just flagged an incoming malware attack on one of the key infrastructure. Customers are complaining about impaired service performance. Recently, CISA published an advisory about a new zero day vulnerability that was just released affecting the spring framework called spring for shell. 
You will analyze firewall logs to identify key infrastructure affected by the attack, prioritizing services that run the Spring Framework, which are critical to the organization’s operations. Once you determine the impacted infrastructure, you will draft a concise email to the relevant team, including the incident timestamp, to alert them of the attack and initiate incident response efforts for mitigation.

*Ref 1.1: CISA alert advisory on Spring4Shell zero-day vulnerability*
<img width="781" alt="Screenshot 2024-09-24 at 4 20 24 PM" src="https://github.com/user-attachments/assets/0f33c07e-7267-43f5-afe7-991e980f0eb6">

*Ref 1.2: CVE advisory on Spring4Shell zero-day vulnerability*
<img width="710" alt="Screenshot 2024-09-24 at 4 18 28 PM" src="https://github.com/user-attachments/assets/94f24d59-0618-4fe1-81be-3c91c54ae74d">


-Followings are the affected infrastructure list and firewall logs as the attackers actively attack the nbn external network:

*Ref 1.3: Firewall Dashboard*
<img width="936" alt="Firewall Dashboard" src="https://github.com/user-attachments/assets/c4c4f887-65fb-4d08-8c2f-f26d7c7cbfe6">

Around 500 of the following logs were generated as the attackers are trying to expoit the vulnerability


*Ref 1.4: Firewall Logs*.
<img width="1213" alt="Firewall Logs" src="https://github.com/user-attachments/assets/db92fd37-d921-425a-9066-9a6dc5bf15bd">

*Ref 1.5: Infrastructure list*
<img width="1002" alt="Infrastructure list" src="https://github.com/user-attachments/assets/80fef092-eeb1-4230-82e4-a4acea5fc502">

After analyzing the CISA and CVE advisory, along with the firewall logs, the following emails were sent to the nbn team with critical mark priority.

*Ref 1.6: Email*
<img width="1002" alt="T1-email" src="https://github.com/user-attachments/assets/6a0eb8cb-904f-4b20-b3fa-5d41d8db9731">

-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Task 2 : Analysing the attack- Now that you have notified the infrastructure owner of the current attack, analyse the firewall logs to find the pattern in the attacker’s network requests. You won’t be able to simply block IP addresses, because of the distributed nature of the attack, but maybe there is another characteristic of the request that is easy to block. Analyse the data of the malware attack to identify how the malware spreads. Find patterns used by the attacker so that we can prepare a firewall rule to stop the spread of the virus.


-The firewall logs(Ref 1.4) were analyzed to identify the characteristics of the Spring4Shell vulnerability used in the attack. An email was then drafted and sent to the networks team, providing concise findings to assist them in developing the necessary firewall rule to mitigate the threat, assuming the recipient had prior experience with similar requests.

*Ref 2.1: Firewall Rule*
<img width="1002" alt="T2-Firewall Rule" src="https://github.com/user-attachments/assets/43898964-71bc-47f3-8397-212bb4e50166">


-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Task 3 : Mitigate the malware attack- Using the patterns you’ve identified, use Python to write a firewall rule to technically mitigate the malware from spreading.

-A simulation of the firewall's scripting language was performed using an HTTP Server, which was assumed to have no computational requirements and served solely to filter incoming traffic.

*Ref 3.1: Firewall Rule using Python*
<img width="1000" alt="T3-Python" src="https://github.com/user-attachments/assets/58ae48d8-a24e-431f-9134-3deb66cb22b4">


-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Task 4: Incident Postmortem- Now that the incident has been resolved, create a postmortem to reflect on the details of the incident.Make sure to include when the incident started and the root cause. Remember, the more detail the better.

-The firewall rule successfully stopped the malware attack two hours after it began. Following the incident, a postmortem report was documented, detailing a timeline of events, individuals involved in the response, a root cause analysis, and actions taken. The postmortem serve as a formal record for future governance, risk, or compliance audits, while also educating team members who were not directly involved in the incident.

*Ref 4.1: Incident Postmortem report*
<img width="1061" alt="T4-Postmortem report" src="https://github.com/user-attachments/assets/b3592152-f7e2-4782-ac00-eb309badf715">


