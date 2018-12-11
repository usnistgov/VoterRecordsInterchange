# Voting - Voter Records Interchange (VRI) CDF Specification

This repository holds voter records interchange (VRI) specification common data format and related information and files that are being created by NIST and collaborators.  The nist-pages branch of this repository holds documentation files for an HTML version located on https://pages.nist.gov/VoterRecordsInterchange.  Note - the nist-pages version is older than the most recent .pdf and .docm versions here; it will be synchronized once final NIST review of the specification is complete.

The VRI specification will support the following list of use cases:

1. OVR Submission: Digital VR applications forms transmitted within state OVR systems or to state OVR systems by third-party OVR systems, following the formats of the NVRA and FPCA voter registration application forms, including state-specific additions to these forms.
2. VR Update Submission: Similar application forms including: voter registration update (change of name, change of address), change of voter status, and absentee ballot request.
3. OVR Transfer: Subsets of such applications used for third-party OVR assistant organizations to transfer users and user data to state OVR systems.
4. Voter Records Lookup: Requests for information regarding voter records within a VR system, or between a VR system and a third party.

The UML model, JSON and XML schemas are planned to be finalized in time to be considered in the next VVSG under development by NIST and the Election Assistance Commission (EAC).  

Contact [John P. Wack](mailto:john.wack@nist.gov) for questions and more information.

## Repo Structure

|Name     |Description                                         |
|---------|----------------------------------------------------|
|**NVRA-PDF-examples**|Examples of VRI CDF using OH VR form    |
|**VA-examples**|Examples of absentee use-case in VA           |
|**VRI_UML_Documentation_files**|Images of UML classes         |
|DRAFT NIST 1500-102 VRI Specification 2018-12-07.docm|Word version of VRI specification|
|DRAFT NIST 1500-102 VRI Specification 2018-12-07.pdf|PDF version of VRI specification|
|NIST_V0_voter_records_interchange.json|JSON Schema            |
|NIST_V0_voter_records_interchange.xsd|XML Schema              |
|VRI Implementation.xml|MagicDraw UML Model                    |
|VRI_UML_Documentation.md|UML Documentation                    |
|VoterRecordsRequest.png|Image of Voter Records Request model  |
|VoterRecordsResponse.png|Image of Voter Records Response model|
