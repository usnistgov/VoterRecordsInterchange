# Voting - NIST Special Publication 1500-102 Voter Records Interchange Common Data Format Specification Version 1

This repository holds the NIST Special Publication 1500-102 Voter Records Interchange (VRI) Common Data Format Specification Version 1 and supporting files. Besides the PDF and Word versions of the specification located in this repository, there is an HTML version at

https://pages.nist.gov/VoterRecordsInterchange.

The VRI specification is also available using the following Digital Object Identifier (DOI):

https://doi.org/10.6028/NIST.SP.1500-102

The VRI specification supports the following use cases:

1. OVR Submission: Digital VR applications forms transmitted within state OVR systems or to state OVR systems by third-party OVR systems, following the formats of the NVRA and FPCA voter registration application forms, including state-specific additions to these forms.
2. VR Update Submission: Similar application forms including: voter registration update (change of name, change of address), change of voter status, and absentee ballot request.
3. OVR Transfer: Subsets of such applications used for third-party OVR assistant organizations to transfer users and user data to state OVR systems.
4. Voter Records Lookup: Requests for information regarding voter records within a VR system, or between a VR system and a third party.

There is a "flattened" version of the XML schema included in this repository; the .zip includes the other XML schemas that are normally referenced by URL or DOI.

Please contact [John Wack](mailto:john.wack@nist.gov) or [John Dziurlaj](mailto:john@hiltonroscoe.com) for more information.

## Repo Structure

|Name     |Description                                         |
|---------|----------------------------------------------------|
|**NVRA-PDF-examples**|Examples of VRI CDF using OH VR form    |
|**VA-examples**|Examples of absentee use-case in VA           |
|VRI_UML_Documentation_files|Images of UML classes         |
|**Flattened VRI XML schema.zip**|Flattened version of the XML schema and external schemas|
|NIST 1500-102 VRI Specification V1.docm|Word version of VRI specification|
|**NIST 1500-102 VRI Specification V1.pdf**|PDF version of VRI specification|
|**NIST_V0_voter_records_interchange.json**|VRI JSON schema            |
|**NIST_V0_voter_records_interchange.xsd**|VRI XML schema              |
|VRI Implementation.xml|MagicDraw UML Model                    |
|VRI_UML_Documentation.md|UML Documentation                    |
|VoterRecordsRequest.png|Image of Voter Records Request model  |
|VoterRecordsResponse.png|Image of Voter Records Response model|
