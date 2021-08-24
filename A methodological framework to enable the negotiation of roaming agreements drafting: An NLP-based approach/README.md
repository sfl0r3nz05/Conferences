# A methodological framework to enable the negotiation of roaming agreements drafting: An NLP-based approach
- **Type of Manuscript**: Conference
- **Conference**:  International Libyan Conference for Information and Communications Technologies ([ILCICT 2021](https://ilcict.lit.ly/en/))
    - [Call for paper](https://lit.ly/doc/ilcict2021_v2_en_pages.pdf)
- **Important requirement**:
    - Submission Deadline: September 1st, 2021
    - 6 pages max free of charges.
    - The review is double-blind.

## Introduction

The roaming procedure maintain persistent connectivity of the subscribers across different networks and geographical regions. Roaming refers to the capability for a subscriber to access the mobile services offered by the Visited Public Mobile Network (VPMN) via the Home Public Mobile Network (HPMN), when moving out of the coverage range of HPMN [1]. However, before ensuring persistent connectivity the Mobile Network Operators (MNOs) must reach an agreement regarding the technical, commercial and legal relationships known as the **Roaming Agreement** (RA).

In order to standardize technical, commercial and legal aspects of **Roaming Agreement**, the GSM Association broadly outlines the content of such **Roaming Agreement** in standardized form for its members [2]. Reference [3] provides a list of the most commonly used GSMA standards, which can be summarized into: (1) **AA.12** constitutes a standard GSMA or Permanent Reference Document; (2) **AA.13** contains the common annexes with operational information (e.g., information on tap file, billing data, settlement procedure, customer care, fraud, etc.); (3) **AA.14** involves the individual annexes containing information about the operator (e.g., contact details of the roaming team, fraud team, IREG team, TADIG team, etc.) and (4) **AA.19** constitutes an addendum to the international **Roaming Agreement** in order to determine specific properties such as charging, billing, and accounting for a specific scenario like the SMS interworking.

While it is true that it is not mandatory to follow the standards proposed by GSMA, according to authoritative voices in the field of negotiating **Roaming Agreement** drafting, most MNOs follow them strictly [4]. Therefore, a first point to consider in the **Roaming Agreement** drafting is how far it is deviated from the GSMA's proposed standards. Thus, during the drafting process of the agreement, the parties should analyze the sub-articles contained in the *standard templates* to determine whether:

1. Leave an article/sub-article as found in the template thereby establishing a **standard clause**.
2. Introduce certain **variations** in the articles/sub-articles, by changing variables, e.g., MNO, dates, penalties, currencies and so on with respect to the original text, i.e., the GSMA templates.
3. Introduce completely new articles/sub-articles that respond to particular interests by constituting **customized texts**.
4. Specify the value of certain **variables** that are found in a certain text, such as dates, names of entities, amounts and others.

However, a successful **Roaming Agreement** drafting goes through a complex negotiation process in which, currently the parties, i.e. the Mobile Network Operators (MNOs), still use asynchronous flows such as email or even regular mail for information exchange. Since these processes lack transparency, which can result in the violation of the **Roaming Agreement** by MNOs, it is necessary to provide a transparent digitization system for **Roaming Agreement** drafting negotiations. For this reason, this paper proposes the use of *Natural Language Processing (NLP)* as an engine to digitize the legal text of the **Romaing Agreements**. The NLP engine analyzes the different articles and sub-articles of the **Romaing Agreements** determining the existence of *variables*, *variations*, *standard clauses* and *customized texts* in the text.

The rest of this manuscript is structured as follows: Section 2 reviews both attempts at a transparent digitalization of **Roaming Agreement** and existing NLP-based digitization mechanisms as part of the **related work**. Section 3 estblishes the **designed methodology**. The implementation of our system are described in Section 4. Section 6 discusses the results of conducted experiments. Finally, the conclusions of the manuscript are included in Section 7. 

## Related work

This section focuses on analyzing, on the one hand, the existing approaches in the context of **Roaming Agreement** digitization, while on the other hand, the text processing mechanisms using NLP-based techniques. The first approach found in the scientific literature is in relation to the application of the **Roaming Agreement** digitalization. Thus, the reference [5] proposes a dynamic **Roaming Agreement** between the Local 5G Operator and the MNO. The interaction between the two entities takes place through an Ethereum based platform. A second approach focuses uniquely on the billing of the services obtained as a result of the **Roaming Agreement** [6]. This agreement is incorporated as part of a smart contract so the work contributes significantly to the digitization process of the agreement, allowing for a faster, more seamless process in which payments can be requested and obtained quickly due to less need for manual intervention. The contextualization of this system in the business environment is proposed by important MNOs such as Telefonica, Deutsche Telekom and Vodafone which use blockchain for Roaming settlement within the framework of the **Roaming Agreement** between the parties [7].

The scientific literature is more extensive regarding the mechanism of digitization and processing of text based on NLP techniques.

Although valuable works were analyzed within the context of efficient and transparent digitization of **Roaming Agreement**, these works focused on the correct application of the **Roaming Agreement** and not from the perspective of the negotiation of **Roaming Agreement** drafting between MNOs. Additionally, text processing mechanisms using NLP-based techniques were analyzed in the judicial or healthcare domain, but outside the context of the negotiation process for the drafting of **Roaming Agreement**, thus ensuring the novelty of our work.

## Designed Methodology
 - Posible herramienta para llevar a cabo el diseño: https://diagrams.mingrammer.com/
## Implemented System
- Posible herramienta para llevar a cabo la implementación: https://diagrams.mingrammer.com/

## Discussion of Results

## Conclusions

## Acknowledgment
This research was funded by **Linux Foundation Mentorship Program** through the project: “[The Use of NLP and DLT to Enable the Digitalization of Telecom Roaming Agreements](https://wiki.hyperledger.org/display/INTERN/The+Use+of+NLP+and+DLT+to+Enable+the+Digitalization+of+Telecom+Roaming+Agreements)” with project identifier **d8a154c6-41fb-4733-b3c8-df37796e7fa3**.

## References
1. I. Tanaka, "Volte roaming and interconnection standard technology", NTT Docomo Technical Journal, vol. 15, no. 2, pp. 37-41, 2013.
2. Ferwerda, R.; Bayings, M.; Van der Kam, M.; Bekkers, R. Advancing E-Roaming in Europe: Towards a Single “Language” for the European Charging Infrastructure. World Electr. Veh. J. 2018, 9, 50. https://doi.org/10.3390/wevj9040050.
3. ROCCO, “The International Roaming Agreement,” 2017. [Online]. Available: https://www.roccoresearch.com/portfolio-items/the-roaming-agreement/. [Accessed: 24-Ago-2021].
4. ROCCO, “What is ROAMING HUBBING?,” 2017. [Online]. Available: https://www.roccoresearch.com/portfolio-items/roaming-hubbing/. [Accessed: 24-Ago-2021].
5. N. Weerasinghe, T. Hewa, M. Dissanayake, M. Ylianttila and M. Liyanage, "Blockchain-based Roaming and Offload Service Platform for Local 5G Operators," 2021 IEEE 18th Annual Consumer Communications & Networking Conference (CCNC), 2021, pp. 1-6, doi: 10.1109/CCNC49032.2021.9369516.
6. C. Harris, "Improving Telecom Industry Processes Using Ordered Transactions in Hyperledger Fabric," 2019 IEEE Globecom Workshops (GC Wkshps), 2019, pp. 1-6, doi: 10.1109/GCWkshps45667.2019.9024541.
7. M. Huillet, "Telefónica, Deutsche Telekom and Vodafone Use Blockchain for Roaming Settlement," 2020. [Online]. Available: https://cointelegraph.com/news/telefonica-deutsche-telekom-and-vodafone-use-blockchain-for-roaming-settlement. [Accessed: 24-Ago-2021].