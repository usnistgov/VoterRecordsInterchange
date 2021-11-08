<link rel="stylesheet" href="https://pages.nist.gov/nist-header-footer/css/nist-combined.css">
<script src="https://pages.nist.gov/nist-header-footer/js/jquery-1.9.0.min.js" type="text/javascript" defer="defer"></script>
<script src="https://pages.nist.gov/nist-header-footer/js/nist-header-footer.js" type="text/javascript" defer="defer"></script>

# National Institute of Standards and Technology (NIST) Special Publication 1500-102, Voter Records Interchange Common Data Format Specification Version 1

**March 2020**

**The following is an excerpt from the SP 1500-102 V1 specification. It contains the specification's executive summary and class documentation.**

The complete publication including JSON and XML schemas is available free of charge from:

<https://github.com/usnistgov/VoterRecordsInterchange>

# Table of Contents

  - **[Executive Summary](#execsum)**
  - Enumerations
    - *The **[AssertionValue](#18_0_2_6340208_1455829091671_996796_4447)** Enumeration*
    - *The **[BallotReceiptMethod](#18_0_2_6340208_1470255961792_690679_4334)** Enumeration*
    - *The **[ContactMethodType](#18_0_2_6340208_1464893409742_774328_4470)** Enumeration*
    - *The **[IdentifierType](#18_0_2_6340208_1446584873809_129867_6769)** Enumeration*
    - *The **[PhoneCapability](#18_0_2_6340208_1465494051199_895769_4463)** Enumeration*
    - *The **[ReportingUnitType](#18_0_2_6340208_1458229388461_823405_4464)** Enumeration*
    - *The **[RequestError](#18_0_2_6340208_1455907053343_466207_4600)** Enumeration*
    - *The **[RequestForm](#18_0_2_6340208_1452790695464_591325_4742)** Enumeration*
    - *The **[RequestMethod](#18_0_2_6340208_1467134022102_846181_4446)** Enumeration*
    - *The **[RequestProxyType](#18_0_2_6340208_1449004272911_37990_4395)** Enumeration*
    - *The **[SignatureSource](#18_0_2_6340208_1452792593365_422705_4843)** Enumeration*
    - *The **[SignatureType](#18_0_2_6340208_1452788065978_2204_4435)** Enumeration*
    - *The **[SuccessAction](#18_0_2_6340208_1465405678263_931387_4502)** Enumeration*
    - *The **[VoterClassificationType](#18_0_2_6340208_1448395608700_92014_4229)** Enumeration*
    - *The **[VoterHelperType](#18_0_2_6340208_1470256949646_121440_4436)** Enumeration*
    - *The **[VoterIdType](#18_0_2_6340208_1448398278987_184146_4431)** Enumeration*
    - *The **[VoterRequestType](#18_0_2_6340208_1446583913045_906582_6615)** Enumeration*
    - *The **[VoterStatus](#19_0_43701b0_1536088404947_60047_5153)** Enumeration*
  - Classes
    - *The **[AdditionalInfo](#18_0_2_6340208_1446587509996_176108_6861)** Class*
    - *The **[BallotRequest](#18_5_2_43701b0_1510599050811_549888_5731)** Class*
    - *The **[BallotStyle](#18_5_3_43701b0_1523391256329_329490_7455)** Class*
    - *The **[ContactMethod](#18_0_2_6340208_1464893400979_739933_4444)** Class*
    - *The **[Election](#18_5_2_43701b0_1510603645561_775691_5960)** Class*
    - *The **[ElectionAdministration](#18_0_2_6340208_1458237760549_706380_5243)** Class*
    - *The **[ElectionBasedBallotRequest](#18_5_3_43701b0_1520358467277_635751_6047)** Class*
    - *The **[Error](#18_5_3_43701b0_1527771278107_788121_5682)** Class*
    - *The **[ExternalIdentifier](#18_0_2_6340208_1446584770723_729230_6705)** Class*
    - *The **[File](#18_0_2_6340208_1452879654116_509055_5255)** Class*
    - *The **[Image](#18_0_2_6340208_1452879607465_248768_5229)** Class*
    - *The **[LatLng](#18_0_2_6340208_1458229746146_45435_4773)** Class*
    - *The **[Location](#18_0_2_6340208_1460480132036_876890_4538)** Class*
    - *The **[Name](#18_0_2_6340208_1446583854986_538708_5957)** Class*
    - *The **[Party](#18_0_2_6340208_1446583854985_482559_5956)** Class*
    - *The **[PermanentBallotRequest](#18_5_3_43701b0_1520358982522_606259_6124)** Class*
    - *The **[PhoneContactMethod](#18_0_2_6340208_1465493970792_917703_4430)** Class*
    - *The **[ReportingUnit](#18_0_2_6340208_1458229422042_966646_4539)** Class*
    - *The **[RequestAcknowledgement](#18_0_2_6340208_1456261767184_144968_4436)** Class*
    - *The **[RequestHelper](#18_0_2_6340208_1470256600538_323550_4366)** Class*
    - *The **[RequestProxy](#18_0_2_6340208_1448401688329_700093_4402)** Class*
    - *The **[RequestRejection](#18_0_2_6340208_1458226815148_390496_4430)** Class*
    - *The **[RequestSuccess](#18_0_2_6340208_1460483674993_168854_4684)** Class*
    - *The **[Signature](#18_0_2_6340208_1452788035217_489009_4409)** Class*
    - *The **[TemporalBallotRequest](#18_5_3_43701b0_1520358515166_885840_6088)** Class*
    - *The **[Voter](#18_5_3_43701b0_1520354792154_717315_5628)** Class*
    - *The **[VoterClassification](#18_0_2_6340208_1452701375494_353834_4295)** Class*
    - *The **[VoterId](#18_0_2_6340208_1448398278986_542661_4430)** Class*
    - *The **[VoterParticipation](#18_5_3_43701b0_1523390807847_148436_7270)** Class*
    - *The **[VoterRecord](#18_5_3_43701b0_1521144693004_190730_6034)** Class*
    - *The **[VoterRecordResults](#18_5_3_43701b0_1523305927438_977151_6481)** Class*
    - *The **[VoterRecordsRequest](#18_0_2_6340208_1446583854986_237644_5961)** Class*
    - *The **[VoterRecordsResponse](#18_0_2_6340208_1455906719413_171772_4514)** Class*


## Executive Summary<a name="execsum"></a>

Voter records are exchanged between an increasing number of entities. Whether it is voter registration offered during an interaction at the motor vehicles administration (MVA), an update to a voter record using an online portal, records exchanged as part of a voter matching database, or requests for absentee ballots, all of these systems need a common data format to effectively communicate.

However, the data exchanged is generally in a non-uniform format. This can cause a number of complications in that each state/territory, or sometimes each individual portal application, may have its own format that must be interpreted and translated on the receiving end.  Voter addresses, in particular, are often provided to voter registration (VR) authorities in formats that are difficult to efficiently store in voter registration databases and use in various related applications.  The collection of accurate voter registration address information is central to the routing of voter registration requests and subsequently in assigning voters to election districts.  Each voter records application being developed must then be aware of each state’s specific formats or design its own format, which complicates development and inhibits the implementation of digital voter record systems.

This specification assists election officials and developers in more easily implementing and supporting the development of online voter registration (OVR) systems by providing them with a uniform common data format for voter records interchange (VRI), that is, the voter registration requests and responses needed for OVR and for voter records maintenance. The languages used in the common data format are XML (eXtensible Markup Language) and JSON (JavaScript Object Notation).

The advantages of using this specification include:

- Providing a ready data interchange format for OVR systems to remove the need for individual system development projects to define their own data models and formats.
- Assisting election officials by reducing or eliminating non-standard exchange formats for voter registration data. Currently, the systems involved and data they produce do not interoperate, adding complexity to the process.
- Providing a baseline CDF (common data format) for voter registration data that can be continually refined to be more efficient and adaptable across all states. Once jurisdictions adopt the CDF VRI, their experience and feedback will refine the continued development of the specification.
- Providing the foundation for additional use cases in the future, which could include:
  - matching driver’s license data between the MVA and voter record systems,
  - automated notifications between the MVA and voter record systems,
  - interoperability with electronic pollbooks,
  - voter record maintenance activities,
  - cross-state record matching, or
  - facilitating data reporting for the Election Administration and Voting Survey (EAVS).

This specification provides background and explanation of how online voter registration typically works, using the data required by the National Voter Registration Act (NVRA) and Federal Post Card Application (FPCA) voter registration forms, including state-specific additions to these forms. It then contains an explanation of a UML (Unified Markup Language) model that was created to detail the data elements required in voter registration requests and responses. The UML model was used to generate XML and JSON schemas, which are both explained and used in various implementation examples.

The intended audience of this specification includes election officials, VR system designers and developers, and others in the election community including the general public. Some background in election administration and registration is useful in understanding the material in this specification.

## Enumerations

### <a name="18_0_2_6340208_1455829091671_996796_4447"></a>*The **AssertionValue** Enumeration*

![Image of AssertionValue](VRI_UML_Documentation_files/18_0_2_6340208_1455829091682_555041_4448.png)

Used in request and response messages.

Enumeration for assertions from a voter or a third party such as a department of motor vehicles (DMV) in response to questions on a registration form, used in the [Assertion](#18_0_2_6340208_1452702303368_675707_4326) attribute of [VoterClassification](#18_0_2_6340208_1452701375494_353834_4295).


Name | Value
---- | -----
`no`|For a voter’s or third party’s assertion of “no” or “false”.
`yes`|For a voter’s or third party’s assertion of “yes” or “true”.
`unknown`|For a voter’s or third party’s assertion of “unknown”.
`other`|For a voter’s or third party’s assertion of “other”.

### <a name="18_0_2_6340208_1470255961792_690679_4334"></a>*The **BallotReceiptMethod** Enumeration*

![Image of BallotReceiptMethod](VRI_UML_Documentation_files/18_0_2_6340208_1470255961795_83043_4335.png)

Used in request messages.

Enumeration for methods for delivering a ballot to the voter, used in the [BallotReceiptPreference](#18_0_2_6340208_1470255941618_803419_4330) attribute of
[BallotRequest](#18_5_2_43701b0_1510599050811_549888_5731). The sub-element may be repeated multiple times with different values as applicable, e.g., to specify both mail and online.


Name | Value
---- | -----
`email`|For email only.
`email-or-online`|For electronic mail or downloadable from a website (this value is ambiguous, thus the separate values for email and online).
`fax`|For use of a fax.
`mail`|For postal mail.
`online`|For downloadable from a website, e.g., the voter is sent a hypertext link to a ballot.

### <a name="18_0_2_6340208_1464893409742_774328_4470"></a>*The **ContactMethodType** Enumeration*

![Image of ContactMethodType](VRI_UML_Documentation_files/18_0_2_6340208_1467137029940_934610_4555.png)

Used in request and response messages.

Enumeration for methods for contacting a voter or an election administration office, used in the [Type](#18_0_2_6340208_1464893427968_428993_4498) attribute of [ContactMethod](#18_0_2_6340208_1464893400979_739933_4444).


Name | Value
---- | -----
`email`|For electronic mail.
`phone`|For use of a phone.
`other`|Used when the type of contact method is not included in this enumeration.

### <a name="18_0_2_6340208_1446584873809_129867_6769"></a>*The **IdentifierType** Enumeration*

![Image of IdentifierType](VRI_UML_Documentation_files/18_0_2_6340208_1446584873812_311564_6776.png)

Used in request and response messages.

Enumeration for election data-related codes in the [ExternalIdentifier](#18_0_2_6340208_1446584770723_729230_6705) class.


Name | Value
---- | -----
`fips`|For FIPS codes.
`local-level`|For a code that is specific to a county or other similar locality.
`national-level`|For a code that is used at the national level other than ocd-id.
`ocd-id`|For Open Civic Data identifiers.
`state-level`|For a code that is specific to a state.
`other`|Used when the type of code is not included in this enumeration.

### <a name="18_0_2_6340208_1465494051199_895769_4463"></a>*The **PhoneCapability** Enumeration*

![Image of PhoneCapability](VRI_UML_Documentation_files/18_0_2_6340208_1467137299147_510499_4665.png)

Used in request and response messages.

Enumeration for telephone capabilities, used in the [Capability](#18_0_2_6340208_1465493985158_54379_4458) attribute of [PhoneContactMethod](#18_0_2_6340208_1465493970792_917703_4430).


Name | Value
---- | -----
`fax`|For telephones that include facsimile capabilities.
`mms`|For telephones that contain Multimedia Messaging Service (MMS) capabilities.
`sms`|For telephones that contain Short Messaging Service (SMS) capabilities.
`voice`|For telephones that contain voice capabilities.

### <a name="18_0_2_6340208_1458229388461_823405_4464"></a>*The **ReportingUnitType** Enumeration*

![Image of ReportingUnitType](VRI_UML_Documentation_files/18_0_2_6340208_1458229388472_819289_4493.png)

Used in request and response messages.

Enumeration for the type of geopolitical unit, used in the [Type](#18_0_2_6340208_1458229422044_801308_4545) sub-element in the [ReportingUnit](#18_0_2_6340208_1458229422042_966646_4539) element.


Name | Value
---- | -----
`ballot-batch`|Used for reporting batches of ballots that may cross precinct boundaries.
`ballot-style-area`|Used for ballot style areas generally composed of precincts.
`borough`|Used in CT, NJ, PA, other states, and New York City for boroughs. For AK and LA, see county.
`city`|Used for a city that reports results and/or for the district that encompasses it.
`city-council`|Used for city council districts.
`combined-precinct`|Used for one or more precincts that have been combined for the purposes of reporting. Used for “Ward” if “Ward” is used interchangeably with “CombinedPrecinct”.
`congressional`|Used for U.S. Congressional districts.
`county`|Used for a county and/or for the district that encompasses it. In AK, used for counties that are called boroughs. In LA, used for parishes.
`county-council`|Used for county council districts.
`drop-box`|Used for a dropbox for absentee ballots.
`judicial`|Used for judicial districts.
`municipality`|Used as applicable for various units such as towns, townships, villages that report votes and/or for the district that encompasses it.
`polling-place`|Used for a polling place.
`precinct`|Used also for “Ward” or “District” when these terms are used interchangeably with “Precinct”.
`school`|Used for a school district.
`special`|Used for a special district.
`split-precinct`|Used for splits of precincts.
`state`|Used for a state and/or for the district that encompasses it.
`state-house`|Used for a state house or assembly district.
`state-senate`|Used for a state senate district.
`town`|Used in some New England states as a type of municipality that reports votes and/or for the district that encompasses it.
`township`|Used in some mid-western states as a type of municipality that reports votes and/or for the district that encompasses it.
`utility`|Used for a utility district.
`village`|Used as a type of municipality that reports votes and/or for the district that encompasses it.
`vote-center`|Used for a vote center.
`ward`|Used for combinations or groupings of precincts or other units.
`water`|Used for a water district.
`other`|Used for other types of reporting units not included in this enumeration.

### <a name="18_0_2_6340208_1455907053343_466207_4600"></a>*The **RequestError** Enumeration*

![Image of RequestError](VRI_UML_Documentation_files/18_0_2_6340208_1455907053346_215454_4601.png)

Used in response messages.

Enumeration for registration-related errors, used in the [Error](#18_0_2_6340208_1455907039816_598163_4597) attribute of [RegistrationRejection](#18_0_2_6340208_1458226815148_390496_4430).


Name | Value
---- | -----
`identity-lookup-failed`|A lookup on the voter’s identity failed.
`incomplete`|The registration request is incomplete.
`ineligible`|The voter is ineligible to be registered.
`invalid-form`|The registration form specified is invalid.
`other`|Used when the type of error is not included in this enumeration.

### <a name="18_0_2_6340208_1452790695464_591325_4742"></a>*The **RequestForm** Enumeration*

![Image of RequestForm](VRI_UML_Documentation_files/18_0_2_6340208_1452790695466_76710_4743.png)

Used in request messages.

Enumeration for types of registration forms, used in the [RegistrationForm](#18_0_2_6340208_1452790770728_957008_4772) attribute of [VoterRecordsRequest](#18_0_2_6340208_1446583854986_237644_5961).


Name | Value
---- | -----
`fpca`|For the Federal Post Card Application form.
`nvra`|For the National Voter Registration Act form.
`other`|Used when the type of form is not included in this enumeration.

### <a name="18_0_2_6340208_1467134022102_846181_4446"></a>*The **RequestMethod** Enumeration*

![Image of RequestMethod](VRI_UML_Documentation_files/18_0_2_6340208_1467134022106_149631_4447.png)

Used in request messages.

Enumeration for the method used by the voter to register, used in the [RequestMethod](#18_0_2_6340208_1467133994025_761560_4440) attribute of [VoterRecordsRequest](#18_0_2_6340208_1446583854986_237644_5961).


Name | Value
---- | -----
`armed-forces-recruitment-office`|The voter assisted by an armed forces recruitment office.
`motor-vehicle-office`|The voter via an MVA/DMV.
`other-agency-designated-by-state`|The voter assisted by an unspecified state-designated agency.
`public-assistance-office`|The voter assisted by a public assistance office.
`registration-drive-from-advocacy-group-or-political-party`|The voter via a registration drive.
`state-funded-agency-serving-persons-with-disabilities`|The voter assisted by a state-designated agency serving persons with disabilities.
`voter-via-election-registrars-office`|The voter via an election or registrar’s office.
`voter-via-email`|The voter via email.
`voter-via-fax`|The voter via fax.
`voter-via-internet`|The voter via the Internet, e.g., a website.
`voter-via-mail`|The voter via postal mail.
`unknown`|The method used is unknown.
`other`|Used when the type of method is not included in this enumeration.

### <a name="18_0_2_6340208_1449004272911_37990_4395"></a>*The **RequestProxyType** Enumeration*

![Image of RequestProxyType](VRI_UML_Documentation_files/18_0_2_6340208_1449004272912_447080_4396.png)

Used in request messages.

Enumeration for the registration proxy, e.g., the MVA/DMV , involved in the voter’s registration request, used in the [Type](#18_0_2_6340208_1449004222447_98580_4390) attribute of [RegistrationProxy](#18_0_2_6340208_1448401688329_700093_4402).


Name | Value
---- | -----
`armed-forces-recruitment-office`|The voter assisted by an armed forces recruitment office.
`motor-vehicle-office`|The voter via an MVA/DMV.
`other-agency-designated-by-state`|The voter assisted by an unspecified state-designated agency.
`public-assistance-office`|The voter assisted by a public assistance office.
`registration-drive-from-advocacy-group-or-political-party`|The voter via a registration drive.
`state-funded-agency-serving-persons-with-disabilities`|The voter assisted by a state-designated agency serving persons with disabilities.
`other`|Used when the type of source is not included in this enumeration.

### <a name="18_0_2_6340208_1452792593365_422705_4843"></a>*The **SignatureSource** Enumeration*

![Image of SignatureSource](VRI_UML_Documentation_files/18_0_2_6340208_1452792593424_253015_4844.png)

Used in request and response messages.

Enumeration for source of the voter’s signature, used in the [Source](#18_0_2_6340208_1455826981569_267749_4433) sub-element of [Signature](#18_0_2_6340208_1452788035217_489009_4409).


Name | Value
---- | -----
`dmv`|For the department of motor vehicles or motor vehicle authority.
`local`|For an unspecified local source.
`state`|For an unspecified state source.
`voter`|The voter has included a signature on the form.
`other`|Used when the source of the signature is not included in this enumeration.

### <a name="18_0_2_6340208_1452788065978_2204_4435"></a>*The **SignatureType** Enumeration*

![Image of SignatureType](VRI_UML_Documentation_files/18_0_2_6340208_1452788065983_503779_4436.png)

Used in request and response messages.

Enumeration for the type of voter signature, used in the [Type](#18_0_2_6340208_1452788086928_168327_4463) sub-element of [Signature](#18_0_2_6340208_1452788035217_489009_4409).


Name | Value
---- | -----
`dynamic`|For use with biometrics or other artifacts captured as part of the act of the voter signing the registration form.
`electronic`|For a facsimile of the signature applied to a marking surface, e.g., paper.
`other`|Used when the type of signature is not included in this enumeration.

### <a name="18_0_2_6340208_1465405678263_931387_4502"></a>*The **SuccessAction** Enumeration*

![Image of SuccessAction](VRI_UML_Documentation_files/18_0_2_6340208_1465405678265_17574_4503.png)

Used in response messages.

Enumeration for a response to a voter records request, indicating that the response to the request is successful and the action that occurred, used in the [Action](#18_0_2_6340208_1465405831538_561001_4536) sub-element of [RegistrationSuccess](#18_0_2_6340208_1460483674993_168854_4684). The success action may not necessarily match the requested action.


Name | Value
---- | -----
`address-updated`|For indicating that an address was updated.
`name-updated`|For indicating that a name was updated.
`registration-cancelled`|For indicating that a registration was cancelled.
`registration-created`|For indicating that a registration was created.
`registration-updated`|For indicating that a registration was updated.
`status-updated`|For indicating that a registration status was updated.
`other`|Used for other types of success actions not included in this enumeration.

### <a name="18_0_2_6340208_1448395608700_92014_4229"></a>*The **VoterClassificationType** Enumeration*

![Image of VoterClassificationType](VRI_UML_Documentation_files/18_0_2_6340208_1448395608702_446714_4230.png)

Used in request and response messages.

Enumeration for voter status classifications, used in the [Type](#18_0_2_6340208_1452702268850_457342_4324) attribute of [VoterClassification](#18_0_2_6340208_1452701375494_353834_4295). Whether the voter status, e.g., eighteen-on-election-day, is true, false, or unknown depends on the value of the [Assertion](#18_0_2_6340208_1452702303368_675707_4326) attribute.


Name | Value
---- | -----
`activated-national-guard`|The voter is an activated National Guard member on State orders (FPCA).
`active-duty`|The voter is a member of the Uniformed Services or Merchant Marine on active duty (FPCA).
`active-duty-spouse-or-dependent`|The voter is an eligible spouse or dependent (FPCA).
`citizen-abroad-intent-to-return`|The voter is a US citizen residing outside the US and has intention to return (FPCA).
`citizen-abroad-return-uncertain`|The voter is a US citizen residing outside the US and their return is uncertain (FPCA).
`citizen-abroad-never-resided`|The voter is a US citizen and has never resided in the US (FPCA).
`deceased`|The voter is deceased (NVRA).
`declared-incompetent`|The voter has been declared incompetent (NVRA).
`eighteen-on-election-day`|The voter will be 18 on election day (NVRA).
`felon`|The voter is a felon (NVRA).
`permanently-denied`|The voter has not been permanently denied (NVRA).
`protected-voter`|The voter status is protected (NVRA).
`restored-felon`|The voter is a restored felon (NVRA).
`united-states-citizen`|The voter is a United States citizen (NVRA).
`other`|Used when the type of voter classification is not included in this enumeration.

### <a name="18_0_2_6340208_1470256949646_121440_4436"></a>*The **VoterHelperType** Enumeration*

![Image of VoterHelperType](VRI_UML_Documentation_files/18_0_2_6340208_1470256957604_938376_4437.png)

Used in request messages.

Enumeration for types of registration helpers, used in the [Type](#18_0_2_6340208_1470256926542_116930_4431) attribute of [RegistrationHelper](#18_0_2_6340208_1470256600538_323550_4366).


Name | Value
---- | -----
`assistant`|For a registration assistant.
`witness`|For a registration witness.

### <a name="18_0_2_6340208_1448398278987_184146_4431"></a>*The **VoterIdType** Enumeration*

![Image of VoterIdType](VRI_UML_Documentation_files/18_0_2_6340208_1448398287461_480100_4458.png)

Used in request and response messages.

Enumeration for the type of voter ID, used in the [Type](#18_0_2_6340208_1448398278989_134134_4433) attribute of [VoterId](#18_0_2_6340208_1448398278986_542661_4430).


Name | Value
---- | -----
`drivers-license`|Used for a driver’s license.
`local-voter-registration-id`|Used for a local voter registration record ID.
`ssn`|Used for a complete Social Security number.
`ssn4`|Used for the last four digits of a Social Security number.
`state-id`|Used for a state ID that is not a state voter registration ID.
`state-voter-registration-id`|Used for a state’s voter registration record ID.
`unspecified-document`|Used for an unspecified document, not known whether the document contains name, address, or photo ID.
`unspecified-document-with-name-and-address`|Used for a document that contains the voter’s name and address, such as a utility bill.
`unspecified-document-with-photo-identification`|Used for a document that contains a photograph of the voter.
`unknown`|Used for documentation that was not captured.
`other`|Used when the type of ID is not included in this enumeration.

### <a name="18_0_2_6340208_1446583913045_906582_6615"></a>*The **VoterRequestType** Enumeration*

![Image of VoterRequestType](VRI_UML_Documentation_files/18_0_2_6340208_1446583913054_479906_6616.png)

Used in request messages.

Enumeration for the type of voter records request, used in the [Type](#18_0_2_6340208_1446586298843_421997_6821) attribute of [VoterRecordsRequest](#18_0_2_6340208_1446583854986_237644_5961).


Name | Value
---- | -----
`ballot-request`|For requesting a ballot, possibly in conjunction with an FPCA registration request.
`lookup`|For a voter registration lookup.
`registration`|For a voter registration request.
`other`|Used when the type of request is not included in this enumeration.

### <a name="19_0_43701b0_1536088404947_60047_5153"></a>*The **VoterStatus** Enumeration*

![Image of VoterStatus](VRI_UML_Documentation_files/19_0_43701b0_1536088404965_967026_5154.png)

Used in response messages. Enumeration for the status of the voter in a Voter Registration Database.

Name | Value
---- | -----
`active`|For a voter in active status.
`inactive`|For a voter in inactive status.
`other`|Used when the type of voter status is not included in this enumeration.

## Classes

### <a name="18_0_2_6340208_1446587509996_176108_6861"></a>*The **AdditionalInfo** Class*

![Image of AdditionalInfo](VRI_UML_Documentation_files/18_0_2_6340208_1446587510003_656308_6862.png)

Used in request messages.

Class for specifying information not addressed in this model by other attributes, e.g. state-specific information that does not “fit” in any other attribute. The information will thus be highly specific to the generating application, and consuming applications must “know” the meaning of the information to make use of it. For this reason, use of this class is discouraged as much as is possible.

The [StringValue](#18_0_2_6340208_1446587603679_902003_6890) and [FileValue](#18_0_2_6340208_1464186843386_982801_4458) attributes are both optional, however exactly one of them must be included.


Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
<a name="18_0_2_6340208_1464186843386_982801_4458"></a>`FileValue`|0..1|`File`|Used if the value is in a file; contains the filename and MIME type
<a name="18_0_2_6340208_1446587599455_477961_6888"></a>`Name`|1|`String`|Name of the value.
<a name="18_0_2_6340208_1446587603679_902003_6890"></a>`StringValue`|0..1|`String`|Used if the value is a string; contains the string.


### <a name="18_5_2_43701b0_1510599050811_549888_5731"></a>*The **BallotRequest** Class*

![Image of BallotRequest](VRI_UML_Documentation_files/18_5_2_43701b0_1510599050830_791767_5732.png)

Used in request messages. An abstract class representing a request for a ballot. Classes for specific types of BallotRequest inherit the attributes and define their own.

Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
<a name="18_0_2_6340208_1470255941618_803419_4330"></a>`BallotReceiptPreference`|0..*|`BallotReceiptMethod`|The voter's preference on how to receive their ballot in order from their most preferred method to least. If omitted, the default method for the [form](#18_0_2_6340208_1452790770728_957008_4772) will be used.
<a name="18_0_2_6340208_1470255052387_244061_4321"></a>`MailForwardingAddress`|0..1|`Address`|


### <a name="18_5_3_43701b0_1523391256329_329490_7455"></a>*The **BallotStyle** Class*

![Image of BallotStyle](VRI_UML_Documentation_files/18_5_3_43701b0_1523391256343_926826_7476.png)

Used in response messages. For referencing a ballot style defined elsewhere, such as in an Election Management System (EMS).

Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
<a name="18_5_3_43701b0_1523391256331_940269_7456"></a>`ExternalIdentifier`|0..*|`ExternalIdentifier`|For associating an ID with the ballot style.
<a name="18_5_3_43701b0_1523391256331_407235_7457"></a>`ImageUri`|0..*|`anyURI`|URI for a ballot image.
<a name="18_5_3_43701b0_1523391256332_916539_7459"></a>`{Party}`|0..*|`Party`|For associating one or more parties with the ballot style.


### <a name="18_0_2_6340208_1464893400979_739933_4444"></a>*The **ContactMethod** Class*

![Image of ContactMethod](VRI_UML_Documentation_files/18_0_2_6340208_1467137004544_113383_4528.png)

Used in request and response messages.

[ElectionAdministration](#18_0_2_6340208_1458237760549_706380_5243) optionally includes this class to specify how to contact the election administration.

[Voter](#18_5_3_43701b0_1520354792154_717315_5628) optionally includes this class to specify the method for contacting a voter regarding the voter’s request. If the voter can be contacted in multiple ways, the application creating the data should order the occurrences of [ContactMethod](#18_0_2_6340208_1464893400979_739933_4444) by priority.

The [PhoneContactMethod](#18_0_2_6340208_1465493970792_917703_4430) class uses [ContactMethod](#18_0_2_6340208_1464893400979_739933_4444) as a base class, and should be used with when the contact method is for a telephone and it is necessary to describe the capabilities of the telephone.

The [Capability](#18_0_2_6340208_1465493985158_54379_4458) attribute is provided by the [PhoneContactMethod](#18_0_2_6340208_1465493970792_917703_4430) class.


Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
<a name="18_0_2_6340208_1464893427968_428993_4498"></a>`Type`|1|`ContactMethodType`|The contact method type, e.g. email or phone.
<a name="18_0_2_6340208_1464893897598_965801_4529"></a>`OtherType`|0..1|`String`|Used when [ContactMethodType](#18_0_2_6340208_1464893409742_774328_4470) value is other.
<a name="18_0_2_6340208_1464893423513_525159_4496"></a>`Value`|1|`String`|The value of the ContactMethod. This will be the text value of the phone number, email address, or other mechanism. The values must be free of any formatting characters, such as parentheses or dashes for a phone number.


### <a name="18_5_2_43701b0_1510603645561_775691_5960"></a>*The **Election** Class*

![Image of Election](VRI_UML_Documentation_files/18_5_3_43701b0_1523390875922_771644_7321.png)

Used in request and response messages. Describes an election event. Only the date of the election is required. Other attributes may be used to describe the election for which a ballot is requested or a voter participated.

Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
<a name="18_5_2_43701b0_1510603645563_843729_5961"></a>`ExternalIdentifier`|0..*|`ExternalIdentifier`|For associating an ID with the election.
<a name="18_5_2_43701b0_1510603645564_296232_5962"></a>`Name`|0..1|`String`|For including a name for the election; the name could be the same name as appears on the ballot.
<a name="18_5_2_43701b0_1510603645564_242065_5963"></a>`StartDate`|1|`date`|The first day of the election.
<a name="18_5_2_43701b0_1510603645565_34473_5964"></a>`EndDate`|0..1|`date`|For an election that spans multiple days, the last day of the election.


### <a name="18_0_2_6340208_1458237760549_706380_5243"></a>*The **ElectionAdministration** Class*

![Image of ElectionAdministration](VRI_UML_Documentation_files/18_0_2_6340208_1458237760552_785040_5253.png)

Used in response messages.

[ElectionAdministration](#18_0_2_6340208_1458237760549_706380_5243) optionally includes [ContactMethod](#18_0_2_6340208_1467137072139_851331_4587) to specify contact information for the election authority.


Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
<a name="18_0_2_6340208_1467137072139_851331_4587"></a>`{ContactMethod}`|0..*|`ContactMethod`|For including various contact information.
<a name="18_0_2_6340208_1460480148403_275530_4589"></a>`{Location}`|0..1|`Location`|Location of the election authority.
<a name="18_0_2_6340208_1458237760550_245716_5244"></a>`Name`|0..1|`String`|Name of the election authority.
<a name="18_0_2_6340208_1458229746147_486101_4781"></a>`Uri`|0..*|`anyURI`|A URL for the election authority.


### <a name="18_5_3_43701b0_1520358467277_635751_6047"></a>*The **ElectionBasedBallotRequest** Class*

![Image of ElectionBasedBallotRequest](VRI_UML_Documentation_files/18_5_3_43701b0_1520358467299_274020_6048.png)

Used in request messages.

Implementation of [BallotRequest](#18_5_2_43701b0_1510599050811_549888_5731) in which a ballot for a single election event is requested.


Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
<a name="18_5_2_43701b0_1510603960046_473210_6072"></a>`{Election}`|1|`Election`|The election for which the ballot is requested.


### <a name="18_5_3_43701b0_1527771278107_788121_5682"></a>*The **Error** Class*

![Image of Error](VRI_UML_Documentation_files/18_5_3_43701b0_1527771278287_705397_5700.png)

Used in response messages.

[RequestRejection](#18_0_2_6340208_1458226815148_390496_4430) includes this class to describe the errors that caused the rejection.

Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
<a name="18_0_2_6340208_1456170823561_699378_4627"></a>`OtherError`|0..1|`String`|Used when [Name](#18_0_2_6340208_1455907039816_598163_4597) value is other.
<a name="18_0_2_6340208_1455907039816_598163_4597"></a>`Name`|1|`RequestError`|Used to indicate the type of error.
<a name="18_5_3_43701b0_1527771290342_857718_5719"></a>`Ref`|0..1|`String`|Reference (e.g. XPath) to the entity that the error applies.


### <a name="18_0_2_6340208_1446584770723_729230_6705"></a>*The **ExternalIdentifier** Class*

![Image of ExternalIdentifier](VRI_UML_Documentation_files/18_0_2_6340208_1458237601050_674272_5135.png)

Used in request and response messages.

[BallotStyle](#18_5_3_43701b0_1523391256329_329490_7455), [Election](#18_5_2_43701b0_1510603645561_775691_5960), [Party](#18_0_2_6340208_1446583854985_482559_5956) and [ReportingUnit](#18_0_2_6340208_1458229422042_966646_4539) optionally include this class for associating a jurisdiction’s codes, i.e., identifiers, with political parties or geopolitical units such as counties, towns, precincts, etc. Multiple occurrences of [ExternalIdentifier](#18_0_2_6340208_1446584770723_729230_6705) can be used to associate multiple codes, e.g., if there is a desire to associate multiple codes with an object such as state-specific codes as well as OCD-IDs (Open Civic Data Identifiers).


Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
<a name="18_0_2_6340208_1446584770724_50890_6707"></a>`Type`|1|`IdentifierType`|An identifier type, e.g., FIPS.
<a name="18_0_2_6340208_1446584770724_559181_6708"></a>`OtherType`|0..1|`String`|Used when [Type](#18_0_2_6340208_1446584770724_50890_6707) value is other.
<a name="18_0_2_6340208_1446584770724_173723_6709"></a>`Value`|1|`String`|The identifier used by the jurisdiction.


### <a name="18_0_2_6340208_1452879654116_509055_5255"></a>*The **File** Class*

![Image of File](VRI_UML_Documentation_files/18_0_2_6340208_1452879654120_445800_5256.png)

Used in request and response messages.

[VoterId](#18_0_2_6340208_1448398278986_542661_4430) optionally uses this class for [FileValue](#18_0_2_6340208_1464186405548_20750_4438) to specify a filename for voter identification purposes such as for a utility bill. [AdditionalInfo](#18_0_2_6340208_1446587509996_176108_6861) also optionally includes [FileValue](#18_0_2_6340208_1464186843386_982801_4458).

File extends the xsd:base64Binary type to add the attributes for filename and (Multi-Purpose Internet Mail Extensions) MIME type, e.g., application/pdf for a file of type PDF.

The [Image](#18_0_2_6340208_1452879607465_248768_5229) element uses this class as an base class, thus [Image](#18_0_2_6340208_1452879607465_248768_5229) can be used when the type of file is for an image, e.g., image/png.


Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
<a name="18_0_2_6340208_1452879677320_165823_5280"></a>`Data`|1|`base64Binary`|The file content encoded using base64.
<a name="18_0_2_6340208_1452879794387_914434_5287"></a>`FileName`|0..1|`String`|The filename.
<a name="18_0_2_6340208_1452882386267_707244_5351"></a>`MimeType`|0..1|`String`|The MIME type associated with the file.


### <a name="18_0_2_6340208_1452879607465_248768_5229"></a>*The **Image** Class*

![Image of Image](VRI_UML_Documentation_files/18_0_2_6340208_1452879607469_640085_5230.png)

Used in request and response messages.

[Signature](#18_0_2_6340208_1452788035217_489009_4409) optionally includes this class to indicate that a file contains an image of a voter’s signature. Image uses [File](#18_0_2_6340208_1452879654116_509055_5255) as a base class, thus attributes of [File](#18_0_2_6340208_1452879654116_509055_5255) can be included in Image.


### <a name="18_0_2_6340208_1458229746146_45435_4773"></a>*The **LatLng** Class*

![Image of LatLng](VRI_UML_Documentation_files/18_0_2_6340208_1458229746170_895736_4860.png)

Used in response messages.

[Location](#18_0_2_6340208_1460480132036_876890_4538) optionally includes this element to specify the latitude and longitude of a voter’s voting location.


Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
<a name="18_0_2_6340208_1458229746148_223158_4793"></a>`Latitude`|1|`float`|Latitude of the location.
<a name="18_0_2_6340208_1458229746148_971314_4794"></a>`Longitude`|1|`float`|Longitude of the location.
<a name="18_0_2_6340208_1458229746148_501713_4795"></a>`Source`|0..1|`String`|System used to perform the lookup from location name to lat/lng, e.g., the name of a geocoding service.


### <a name="18_0_2_6340208_1460480132036_876890_4538"></a>*The **Location** Class*

![Image of Location](VRI_UML_Documentation_files/18_0_2_6340208_1460480132037_37951_4539.png)

Used in response messages.

[ElectionAdministration](#18_0_2_6340208_1458237760549_706380_5243) and [ReportingUnit](#18_0_2_6340208_1458229422042_966646_4539) optionally include this element to specify the address and directions to a voter’s voting location. The [LatLng](#18_0_2_6340208_1458229746146_45435_4773) element can be included to specify the latitude and longitude of the voting location.


Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
<a name="18_0_2_6340208_1460493899294_400003_4467"></a>`Address`|0..1|`Address`|Address of the voting location.
<a name="18_0_2_6340208_1458229746146_777819_4775"></a>`Directions`|0..1|`String`|Directions to the voting location.
<a name="18_0_2_6340208_1458229746149_332646_4800"></a>`{LatLng}`|0..1|`LatLng`|Latitude/longitude of the voting location.


### <a name="18_0_2_6340208_1446583854986_538708_5957"></a>*The **Name** Class*

![Image of Name](VRI_UML_Documentation_files/18_0_2_6340208_1446583855033_467904_6133.png)

Used in request and response messages.

[Voter](#18_5_3_43701b0_1520354792154_717315_5628) includes this class for specifying the name of a voter and, optionally, for specifying a previous name of the voter, using [PreviousName](#18_5_3_43701b0_1520545273362_721771_5308) instead of [Name](#18_0_2_6340208_1449006181433_992071_4512). [RequestHelper](#18_0_2_6340208_1470256600538_323550_4366) also includes this class for specifying the name of a request helper.

Multiple occurrences of the [MiddleName](#18_0_2_6340208_1453305616868_302875_4310) attribute can be used as needed, e.g., for names with additional middle names or nicknames such as “John Andrew Winston (Jack) Smith”.

All elements are optional, however at least [FullName](#18_0_2_6340208_1446591484368_838009_7101) must be included if the other attributes are not.


Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
<a name="18_0_2_6340208_1446583855000_459623_5999"></a>`FirstName`|0..1|`String`|Person’s first (given) name.
<a name="18_0_2_6340208_1446591484368_838009_7101"></a>`FullName`|0..1|`String`|Person’s full name.
<a name="18_0_2_6340208_1446583855000_180415_5998"></a>`LastName`|0..1|`String`|Person’s last (family) name.
<a name="18_0_2_6340208_1453305616868_302875_4310"></a>`MiddleName`|0..*|`String`|Person’s middle name.
<a name="18_0_2_6340208_1446583855000_788772_5997"></a>`Prefix`|0..1|`String`|A prefix associated with the person, e.g., Mr.
<a name="18_0_2_6340208_1446583855000_441516_6001"></a>`Suffix`|0..1|`String`|A suffix associated with the person, e.g., Jr.


### <a name="18_0_2_6340208_1446583854985_482559_5956"></a>*The **Party** Class*

![Image of Party](VRI_UML_Documentation_files/18_5_3_43701b0_1523391450716_472827_7537.png)

Used in request and response messages.

[BallotStyle](#18_5_3_43701b0_1523391256329_329490_7455) optionally includes this type to specify the associated political party, such as for closed primaries.

[Voter](#18_5_3_43701b0_1520354792154_717315_5628) optionally includes this type to specify a voter’s political party.


Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
<a name="18_0_5_43401a7_1466107702572_743261_4563"></a>`Abbreviation`|0..1|`String`|Short name for the party, e.g., “DEM”.
<a name="18_0_5_43401a7_1467296326731_60767_4483"></a>`{ExternalIdentifier}`|0..*|`ExternalIdentifier`|For associating an ID with the party.
<a name="18_0_2_6340208_1446583854999_279392_5995"></a>`Name`|1|`String`|Official full name of the party, e.g., “Republican”.


### <a name="18_5_3_43701b0_1520358982522_606259_6124"></a>*The **PermanentBallotRequest** Class*

![Image of PermanentBallotRequest](VRI_UML_Documentation_files/18_5_3_43701b0_1520358982544_874394_6125.png)

Used in request messages.

Subtype of [BallotRequest](#18_5_2_43701b0_1510599050811_549888_5731) which serves to request ballots for election events that the voter is qualified on a long term basis. Although "permanent", the request may be subject to renewal or cancellation procedures.



### <a name="18_0_2_6340208_1465493970792_917703_4430"></a>*The **PhoneContactMethod** Class*

![Image of PhoneContactMethod](VRI_UML_Documentation_files/18_0_2_6340208_1467137273798_668126_4636.png)

Used in request and response messages.

[RequestHelper](#18_0_2_6340208_1470256600538_323550_4366), and [RequestProxy](#18_0_2_6340208_1448401688329_700093_4402) use this class to specify a telephone number as well as the capabilities of the telephone, e.g., sms, fax, etc.

PhoneContactMethod is subtype of [ContactMethod](#18_0_2_6340208_1464893400979_739933_4444). Thus, the elements that include [ContactMethod](#18_0_2_6340208_1464893400979_739933_4444) could use [PhoneContactMethod](#18_0_2_6340208_1465493970792_917703_4430) as applicable.


Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
<a name="18_0_2_6340208_1465493985158_54379_4458"></a>`Capability`|0..*|`PhoneCapability`|Specifies the phone’s capabilities, e.g., fax, sms.


### <a name="18_0_2_6340208_1458229422042_966646_4539"></a>*The **ReportingUnit** Class*

![Image of ReportingUnit](VRI_UML_Documentation_files/18_0_2_6340208_1458229422060_410467_4604.png)

Used in response messages.

[RequestSuccess](#18_0_2_6340208_1460483674993_168854_4684) and [VoterRecord](#18_5_3_43701b0_1521144693004_190730_6034) include this class so as to provide a list of geopolitical geography associated with the voter’s registration, e.g., the voter’s precinct, polling place, districts, etc. [VoterParticipation](#18_5_3_43701b0_1523390807847_148436_7270) optionally includes this class to specify the polling place used by the voter. The [Type](#18_0_2_6340208_1458229422044_801308_4545) attribute uses the [ReportingUnitType](#18_0_2_6340208_1458229388461_823405_4464) enumeration to specify the type of geopolitical geography being defined. If the reporting unit type is not listed in enumeration [ReportingUnitType](#18_0_2_6340208_1458229388461_823405_4464), use other and include the reporting unit type (that is not listed in the enumeration) in [OtherType](#18_0_2_6340208_1458229422044_377016_4546).

The [IsDistricted](#18_0_2_6340208_1458229422043_1159_4542) boolean is not strictly necessary, as it is possible to identify districts by their Type attribute. However, if the type of district is not listed in the [ReportingUnitType](#18_0_2_6340208_1458229388461_823405_4464) enumeration and therefore [OtherType](#18_0_2_6340208_1458229422044_377016_4546) is used, then [IsDistricted](#18_0_2_6340208_1458229422043_1159_4542) is necessary. The [IsDistricted](#18_0_2_6340208_1458229422043_1159_4542) boolean can also be used to signify that a [ReportingUnit](#18_0_2_6340208_1458229422042_966646_4539) defined as a jurisdiction, e.g., a county, is also used as a district for, e.g., county-wide contests.


Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
<a name="18_0_5_43401a7_1467296241890_387585_4456"></a>`{ExternalIdentifier}`|0..*|`ExternalIdentifier`|For associating an ID with the [ReportingUnit](#18_0_2_6340208_1458229422042_966646_4539).
<a name="18_0_2_6340208_1458229422043_1159_4542"></a>`IsDistricted`|0..1|`Boolean`|Boolean to indicate that the reporting unit is a district.
<a name="18_0_2_6340208_1458237986081_437865_5351"></a>`{Location}`|0..1|`Location`|Location of the district office.
<a name="18_0_2_6340208_1458229422045_137798_4551"></a>`Name`|0..1|`String`|Name of the reporting unit.
<a name="18_0_2_6340208_1458229422044_801308_4545"></a>`Type`|1|`ReportingUnitType`|Enumerated type of reporting unit, e.g., district, precinct.
<a name="18_0_2_6340208_1458229422044_377016_4546"></a>`OtherType`|0..1|`String`|Used when [Type](#18_0_2_6340208_1458229422044_801308_4545) value is other.


### <a name="18_0_2_6340208_1456261767184_144968_4436"></a>*The **RequestAcknowledgement** Class*

![Image of RequestAcknowledgement](VRI_UML_Documentation_files/18_0_2_6340208_1456261767195_161515_4437.png)

Used in response messages. For indicating that the request was received but action on the request is pending.


### <a name="18_0_2_6340208_1470256600538_323550_4366"></a>*The **RequestHelper** Class*

![Image of RequestHelper](VRI_UML_Documentation_files/18_0_2_6340208_1470256600539_764405_4367.png)

Used in request messages.

[VoterRecordsRequest](#18_0_2_6340208_1446583854986_237644_5961) optionally includes this element to specify information about a request helper, i.e., a request assistant or witness involved in a voter’s request.

RequestHelper optionally includes the [Name](#18_0_2_6340208_1446583854986_538708_5957) element to specify the registration helper’s name and optionally includes the [Signature](#18_0_2_6340208_1452788035217_489009_4409) element if a registration helper’s signature is required.


Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
<a name="18_0_2_6340208_1449004024670_400681_4285"></a>`Address`|0..1|`Address`|Address of the request helper.
<a name="18_0_2_6340208_1446583855003_986716_6030"></a>`{Name}`|0..1|`Name`|To specify the name of the helper.
<a name="18_0_2_6340208_1449004018574_638446_4281"></a>`Phone`|0..1|`PhoneContactMethod`|Request helper’s phone number.
<a name="18_0_2_6340208_1465498406376_433216_4546"></a>`{Signature}`|0..1|`Signature`|To specify the signature of the helper.
<a name="18_0_2_6340208_1470256926542_116930_4431"></a>`Type`|1|`VoterHelperType`|To specify the type of helper, e.g., assistant.


### <a name="18_0_2_6340208_1448401688329_700093_4402"></a>*The **RequestProxy** Class*

![Image of RequestProxy](VRI_UML_Documentation_files/18_0_2_6340208_1448401688330_628139_4403.png)

Used in request messages.

[VoterRecordsRequest](#18_0_2_6340208_1446583854986_237644_5961) optionally includes this class to specify information about a request proxy involved in a voter records request.

[OriginTransactionId](#18_0_2_6340208_1452791385413_559315_4796) can be used to include an optional identifier of the originating external transaction from the proxy, e.g., used for the transaction ID generated by a DMV application enacting a voter registration request to a registration portal application (on behalf of a citizen obtaining a driver’s license). This sub-element is not to be confused with TransactionId in [VoterRecordsRequest](#18_0_2_6340208_1446583854986_237644_5961), which is used to include a transaction ID of the voter records request, e.g., the transaction ID of the registration portal’s voter records request.

Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
<a name="18_2_43401a7_1463060690287_858253_4538"></a>`Address`|0..1|`Address`|An address associated with the proxy.
<a name="18_0_2_6340208_1449004266608_550360_4392"></a>`Name`|0..1|`String`|A name associated with the proxy.
<a name="18_0_2_6340208_1452791385413_559315_4796"></a>`OriginTransactionId`|0..1|`String`|An identifier associated with the transaction between the proxy and, e.g., the registration portal.
<a name="18_2_43401a7_1463060712925_52809_4542"></a>`Phone`|0..1|`PhoneContactMethod`|A phone number associated with the proxy.
<a name="18_0_2_6340208_1452792125344_443231_4806"></a>`TimeStamp`|0..1|`date`|The date of the request from the proxy.
<a name="18_0_2_6340208_1449004222447_98580_4390"></a>`Type`|1|`RequestProxyType`|The type of the requesting proxy, e.g., motor-vehicle-office, public-assistance-office.
<a name="18_0_2_6340208_1449004618710_652726_4439"></a>`OtherType`|0..1|`String`|Used when [OtherType](#18_0_2_6340208_1449004618710_652726_4439) value is other.


### <a name="18_0_2_6340208_1458226815148_390496_4430"></a>*The **RequestRejection** Class*

![Image of RequestRejection](VRI_UML_Documentation_files/18_0_2_6340208_1458226815154_812582_4431.png)

Used in response messages.

For indicating that the request failed. The [Error](#18_5_3_43701b0_1527771278145_89966_5684) attribute is used to indicate the type of error that occurred. The [AdditionalDetails](#18_0_5_43401a7_1466533383266_843518_4448) attribute can be used to provide more information as to the rejection.

Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
<a name="18_0_5_43401a7_1466533383266_843518_4448"></a>`AdditionalDetails`|0..*|`String`|Used to provide additional details as applicable.
<a name="18_5_3_43701b0_1527771278145_89966_5684"></a>`{Error}`|0..*|`Error`|For associating a [RequestRejection](#18_0_2_6340208_1458226815148_390496_4430) with one or more [Error](#18_5_3_43701b0_1527771278145_89966_5684).


### <a name="18_0_2_6340208_1460483674993_168854_4684"></a>*The **RequestSuccess** Class*

![Image of RequestSuccess](VRI_UML_Documentation_files/18_0_2_6340208_1460483674995_528178_4685.png)

Used in response messages.

For indicating a successful response to a request. The [Action](#18_0_2_6340208_1465405831538_561001_4536) attribute is used to indicate the action that occurred, which may differ from what was requested. For example, a request for a new voter registration may succeed, but if the voter was already registered, the response may indicate a registration update as opposed to a registration create.

The response also includes, optionally, other information useful to the voter, including a description of the voter’s polling place, districts (i.e., contests) associated with the polling place, or other geopolitical geographies such as the voter’s precinct.

Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
<a name="18_0_2_6340208_1465405831538_561001_4536"></a>`Action`|0..*|`SuccessAction`|Used to indicate the action that occurred.
<a name="18_0_2_6340208_1460480053765_398742_4483"></a>`{District}`|0..*|`ReportingUnit`|One or more districts associated with the voter’s precinct.
<a name="18_0_2_6340208_1465576589038_936326_4438"></a>`EffectiveDate`|0..1|`date`|The effective date of the action.
<a name="18_0_2_6340208_1458237768093_586675_5281"></a>`{ElectionAdministration}`|0..1|`ElectionAdministration`|The election administration that conducts elections for the voter.
<a name="18_0_2_6340208_1460480018439_304252_4448"></a>`{Locality}`|0..*|`ReportingUnit`|Other geographies such as the voter’s precinct.
<a name="18_0_2_6340208_1458238628374_827167_5425"></a>`{PollingPlace}`|0..1|`ReportingUnit`|The voter’s polling place.


### <a name="18_0_2_6340208_1452788035217_489009_4409"></a>*The **Signature** Class*

![Image of Signature](VRI_UML_Documentation_files/18_0_2_6340208_1452788035221_169450_4410.png)

Used in request and response messages.

[Voter](#18_5_3_43701b0_1520354792154_717315_5628) optionally includes this class for specifying information about a voter’s signature on a registration request. If there is a need to include previous signature that uses a different name, e.g., a maiden name, [Voter](#18_5_3_43701b0_1520354792154_717315_5628) uses [PreviousSignature](#18_0_2_6340208_1492617539359_425782_4577) instead of [Signature](#18_0_2_6340208_1452788173305_113537_4476).

[RequestHelper](#18_0_2_6340208_1470256600538_323550_4366) optionally includes this class for specifying information about the helper's signature.

[Source](#18_0_2_6340208_1455826981569_267749_4433) is used to specify the source of the voter’s signature, for example, on file at a department of motor vehicles. [FileValue](#18_0_2_6340208_1452788100058_338334_4465) is used to include an image of the voter’s signature.


Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
<a name="18_0_2_6340208_1452788705370_491492_4546"></a>`Date`|0..1|`date`|The date of the signature, i.e., when created.
<a name="18_0_2_6340208_1452788100058_338334_4465"></a>`FileValue`|0..1|`Image`|The signature image in base 64 binary.
<a name="18_0_2_6340208_1455826981569_267749_4433"></a>`Source`|0..1|`SignatureSource`|A source for the signature, e.g., dmv.
<a name="18_0_2_6340208_1455826981570_89404_4434"></a>`OtherSource`|0..1|`String`|Used when [Source](#18_0_2_6340208_1455826981569_267749_4433) value is other.
<a name="18_0_2_6340208_1452788086928_168327_4463"></a>`Type`|0..1|`SignatureType`|A signature type, e.g., dynamic.
<a name="18_0_5_43401a7_1466101952104_73374_4556"></a>`OtherType`|0..1|`String`|Used when [Type](#18_0_2_6340208_1452788086928_168327_4463) value is other.


### <a name="18_5_3_43701b0_1520358515166_885840_6088"></a>*The **TemporalBallotRequest** Class*

![Image of TemporalBallotRequest](VRI_UML_Documentation_files/18_5_3_43701b0_1520358515169_841616_6089.png)

Used in request messages.

Subtype of [BallotRequest](#18_5_2_43701b0_1510599050811_549888_5731) in which election opportunities that the voter is qualified during a given time frame may be requested.

Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
<a name="18_5_2_43701b0_1510603980380_983913_6088"></a>`StartDate`|1|`date`|The date at which the request comes into effect.
<a name="18_5_3_43701b0_1520881700794_22779_5367"></a>`EndDate`|1|`date`|The date at which the request is no longer effective.


### <a name="18_5_3_43701b0_1520354792154_717315_5628"></a>*The **Voter** Class*

![Image of Voter](VRI_UML_Documentation_files/18_5_3_43701b0_1522779528451_974674_7331.png)

Used in request and response messages. Contains attributes specific to identifying a voter.

Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
<a name="18_0_2_6340208_1464893442533_462634_4505"></a>`{ContactMethod}`|0..*|`ContactMethod`|How to contact the voter, listed in order of preference.
<a name="18_0_2_6340208_1446583855001_164737_6010"></a>`DateOfBirth`|0..1|`date`|The voter’s data of birth in YYYY-MM-DD format.
<a name="18_0_2_6340208_1446583855002_714031_6021"></a>`Ethnicity`|0..1|`String`|The voter’s ethnicity.
<a name="18_0_2_6340208_1446583855003_866490_6023"></a>`Gender`|0..1|`String`|Older systems may not understand values other than 'Male' or 'Female' (the only choices available on FPCA).
<a name="18_0_2_6340208_1446583855000_701682_6007"></a>`MailingAddress`|0..1|`Address`|Where the voter receives postal mail, mapped to the FGDC specification Address classes.
<a name="18_0_2_6340208_1449006181433_992071_4512"></a>`{Name}`|1|`Name`|Voter’s name.
<a name="18_5_2_43701b0_1510603103372_197724_5824"></a>`{Party}`|0..1|`Party`|Voter’s political party.
<a name="18_5_3_43701b0_1520545273362_721771_5308"></a>`{PreviousName}`|0..1|`Name`|A voter’s previous name.
<a name="18_0_2_6340208_1446583855001_991375_6008"></a>`PreviousResidenceAddress`|0..1|`Address`|Where the voter was previously registered, mapped to the FGDC specification Address classes.
<a name="18_0_2_6340208_1492617539359_425782_4577"></a>`{PreviousSignature}`|0..1|`Signature`|Information about a previous voter signature on the registration form.
<a name="18_0_2_6340208_1446583855003_565170_6029"></a>`ResidenceAddress`|1|`Address`|Where the voter is registered or requests to be registered, mapped to the FGDC specification Address classes.
<a name="18_0_2_6340208_1464892712176_679185_4428"></a>`ResidenceAddressIsMailingAddress`|0..1|`Boolean`|If set to true, MailingAddress need not be included.
<a name="18_0_2_6340208_1452788173305_113537_4476"></a>`{Signature}`|0..1|`Signature`|Information about the voter signature on the registration form.
<a name="18_0_2_6340208_1452703080545_997910_4333"></a>`{VoterClassification}`|0..*|`VoterClassification`|How the voter is classified per assertions the voter has made on a registration form.
<a name="18_5_3_43701b0_1520355588761_324546_5986"></a>`{VoterId}`|0..*|`VoterId`|Information to provide voter identity.


### <a name="18_0_2_6340208_1452701375494_353834_4295"></a>*The **VoterClassification** Class*

![Image of VoterClassification](VRI_UML_Documentation_files/18_0_2_6340208_1452701375514_47142_4296.png)

Used in request and response messages.

[Voter](#18_5_3_43701b0_1520354792154_717315_5628) optionally includes this class to describe a voter’s classification per criteria on the voter’s request form, e.g., united-states-citizen or eighteen-on-election-day.

[VoterClassification](#18_0_2_6340208_1452701375494_353834_4295) includes assertions of the voter in response to the voter request form criteria. For example, an assertion of true may be used with a criterion of united-states-citizen. Assertions can be negative, such as providing an assertion of false for a criterion of felon, an assertion of unknown to indicate that the voter does not know whether they meet or do not meet the specific criteria on the form or an assertion of other, in which the assertion is specified by the value of [OtherAssertion](#18_5_3_43701b0_1520357756289_358083_6036).


Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
<a name="18_0_2_6340208_1452702303368_675707_4326"></a>`Assertion`|1|`AssertionValue`|A positive, negative, other or unknown assertion
<a name="18_5_3_43701b0_1520357756289_358083_6036"></a>`OtherAssertion`|0..1|`String`|An locally defined assertion value.
<a name="18_0_2_6340208_1452702268850_457342_4324"></a>`Type`|1|`VoterClassificationType`|A classification type, e.g., felon.
<a name="18_0_2_6340208_1452703117530_845631_4357"></a>`OtherType`|0..1|`String`|Used when [Type](#18_0_2_6340208_1452702268850_457342_4324) value is other.


### <a name="18_0_2_6340208_1448398278986_542661_4430"></a>*The **VoterId** Class*

![Image of VoterId](VRI_UML_Documentation_files/18_0_2_6340208_1448398287463_421964_4483.png)

Used in request and response messages.

Used to include information about a voter’s identification that may be required in a registration request. [Voter](#18_5_3_43701b0_1520354792154_717315_5628) includes [VoterId](#18_0_2_6340208_1448398278986_542661_4430).

[AttestNoSuchId](#18_0_2_6340208_1464098232868_139916_4328) is used to attest that the voter has no ID of a specified type, thus it must be included with a value of true if attesting that the voter has no ID for that specified type. It can be included with a value of false to attest that the voter does have an ID of the specified type, in which case either [StringValue](#18_0_2_6340208_1448398278989_139227_4432) or [FileValue](#18_0_2_6340208_1464186405548_20750_4438) must be included; however, it is assumed to be false if not included. The [StringValue](#18_0_2_6340208_1448398278989_139227_4432) and [FileValue](#18_0_2_6340208_1464186405548_20750_4438) sub-elements are both optional, however at least one of them must be included.


Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
<a name="18_0_2_6340208_1464098232868_139916_4328"></a>`AttestNoSuchId`|0..1|`Boolean`|Used to attest that the voter has no ID. Assumed to be false if not present.
<a name="18_0_2_6340208_1452791252200_622209_4779"></a>`DateOfIssuance`|0..1|`date`|Date the ID was issued.
<a name="18_0_2_6340208_1464186405548_20750_4438"></a>`FileValue`|0..1|`File`|Used to include a file name for the ID.
<a name="18_0_2_6340208_1448398278989_139227_4432"></a>`StringValue`|0..1|`String`|Used to include the ID as a string.
<a name="18_0_2_6340208_1448398278989_134134_4433"></a>`Type`|1|`VoterIdType`|The type of voter ID.
<a name="18_0_2_6340208_1448398278989_463089_4435"></a>`OtherType`|0..1|`String`|Used when [Type](#18_0_2_6340208_1448398278989_134134_4433) value is other.


### <a name="18_5_3_43701b0_1523390807847_148436_7270"></a>*The **VoterParticipation** Class*

![Image of VoterParticipation](VRI_UML_Documentation_files/18_5_3_43701b0_1523390807871_783291_7271.png)

Used in response messages. For indicating an election that the voter participated in. Participation does not imply a counted ballot.

Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
<a name="18_5_3_43701b0_1523391427889_565721_7508"></a>`{BallotStyle}`|0..1|`BallotStyle`|For associating the voter participation to a specific ballot style, such to a partisan ballot in a closed primary.
<a name="18_5_3_43701b0_1523390882603_527268_7351"></a>`{Election}`|1|`Election`|For associating the voter participation to a specific election event.
<a name="19_0_43701b0_1537277058654_997916_5158"></a>`{PollingLocation}`|0..1|`ReportingUnit`|The polling place used by the voter.


### <a name="18_5_3_43701b0_1521144693004_190730_6034"></a>*The **VoterRecord** Class*

![Image of VoterRecord](VRI_UML_Documentation_files/18_5_3_43701b0_1521144693023_685785_6035.png)

Used in response messages. Used to represent a voter record stored in a Voter Registration Database (VRDB). VoterRecord optionally contains additional information useful to the voter, including a description of the voter’s polling place, districts associated with the voter's precinct, or other geopolitical geographies such as the voter’s precinct.

Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
<a name="18_5_3_43701b0_1523308632860_920362_6595"></a>`{District}`|0..*|`ReportingUnit`|One or more districts associated with the voter’s precinct.
<a name="18_5_3_43701b0_1523308699224_862322_6626"></a>`{ElectionAdministration}`|0..1|`ElectionAdministration`|The election administration that conducts elections for the voter.
<a name="18_5_3_43701b0_1524169058325_142051_6434"></a>`HavaIdRequired`|0..1|`Boolean`|Indicates that the voter must present identification at the polls per HAVA.
<a name="18_5_3_43701b0_1522785557431_296316_7408"></a>`{Locality}`|0..*|`ReportingUnit`|Other geographies such as the voter’s precinct.
<a name="18_5_3_43701b0_1522785527338_156954_7383"></a>`{PollingLocation}`|0..1|`ReportingUnit`|The voter’s polling place.
<a name="19_0_43701b0_1538056056711_903517_5865"></a>`{Voter}`|1|`Voter`|For details specific to a particular voter.
<a name="18_5_3_43701b0_1523390822767_626731_7301"></a>`{VoterParticipation}`|0..*|`VoterParticipation`|For associating a [VoterRecord](#18_5_3_43701b0_1521144693004_190730_6034) to elections the voter has participated in.
<a name="18_5_3_43701b0_1524168892961_117849_6431"></a>`VoterStatus`|0..1|`VoterStatus`|The status of the VoterRecord, possibly to indicate the ability to receive a regular ballot.
<a name="19_0_43701b0_1537283642388_774863_5190"></a>`OtherVoterStatus`|0..1|`String`|Used when [VoterStatus](#18_5_3_43701b0_1524168892961_117849_6431) value is other.


### <a name="18_5_3_43701b0_1523305927438_977151_6481"></a>*The **VoterRecordResults** Class*

![Image of VoterRecordResults](VRI_UML_Documentation_files/18_5_3_43701b0_1523305927444_622293_6482.png)

Used in response messages.

For indicating a successful response to a lookup request.

A lookup for a single voter may result in multiple [VoterRecord](#18_5_3_43701b0_1521144693004_190730_6034) being returned. This can occur if the voter has duplicate records in the VRDB, or if the criteria specified in the lookup request was broad.

Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
<a name="18_5_3_43701b0_1523306302886_361773_6512"></a>`{VoterRecord}`|0..*|`VoterRecord`|The voter record(s) returned.


### <a name="18_0_2_6340208_1446583854986_237644_5961"></a>*The **VoterRecordsRequest** Class*

![Image of VoterRecordsRequest](VRI_UML_Documentation_files/18_0_2_6340208_1446583855033_382783_6135.png)

The root element for request messages.

For defining items pertaining to the status and type of the voter records request and when it was generated. [VoterRecordsRequest](#18_0_2_6340208_1446583854986_237644_5961) includes the [Subject](#18_0_2_6340208_1465929705246_568919_4464) association to specify various information about the voter in question. It includes the [BallotRequest](#18_5_2_43701b0_1510599050811_549888_5731) association to handle a request for an ballot; this request may be part of an FPCA form registration or may be submitted independently.


Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
<a name="18_0_2_6340208_1446587611947_417902_6897"></a>`{AdditionalInfo}`|0..*|`AdditionalInfo`|For including other information not specified by this model.
<a name="18_5_3_43701b0_1520355018307_553646_5833"></a>`{BallotRequest}`|0..1|`BallotRequest`|Specifies information relating to a request for a ballot.
<a name="18_0_2_6340208_1452790770728_957008_4772"></a>`Form`|0..1|`RequestForm`|If the request is for a voter registration, the registration form used by the voter.
<a name="18_0_2_6340208_1452793827465_473370_4893"></a>`OtherForm`|0..1|`String`|Used when [Form](#18_0_2_6340208_1452790770728_957008_4772) value is other.
<a name="18_0_2_6340208_1452801656835_768643_4939"></a>`GeneratedDate`|1|`date`|The date that the voter records request was generated.
<a name="18_0_2_6340208_1452801775201_246767_4944"></a>`Issuer`|0..1|`String`|The name of the issuer of the voter records request transaction, e.g., State of West Virginia Voter Registration Portal.
<a name="18_0_2_6340208_1446583855002_16319_6017"></a>`{RequestHelper}`|0..*|`RequestHelper`|Included if the registration involves a registration assistant organization.
<a name="18_0_2_6340208_1467133994025_761560_4440"></a>`RequestMethod`|1|`RequestMethod`|The method used by the voter to register.
<a name="18_0_2_6340208_1467136835506_844637_4521"></a>`OtherRequestMethod`|0..1|`String`|Used when [RequestMethod](#18_0_2_6340208_1467133994025_761560_4440) value is other.
<a name="18_0_2_6340208_1449004178324_489146_4368"></a>`{RequestProxy}`|0..1|`RequestProxy`|Included if the registration request is via a proxy, e.g., the DMV.
<a name="18_0_2_6340208_1492618306756_309901_4606"></a>`SelectedLanguage`|0..1|`language`|The language specified by the voter, if any.
<a name="18_0_2_6340208_1465929705246_568919_4464"></a>`{Subject}`|1|`Voter`|Specifies information about the voter who is the subject of the request.
<a name="18_0_2_6340208_1464098068816_445452_4324"></a>`TransactionId`|0..1|`String`|An identifier of the voter records request transaction.
<a name="18_0_2_6340208_1446586298843_421997_6821"></a>`Type`|1..*|`VoterRequestType`|The type of request, e.g., registration.
<a name="18_0_2_6340208_1446586441151_443159_6836"></a>`OtherType`|0..1|`String`|Used when [RequestType](#18_0_2_6340208_1446586298843_421997_6821) value is other.
<a name="18_0_2_6340208_1452801800793_502602_4948"></a>`VendorApplicationId`|0..1|`String`|An identifier of the vendor application generating the voter registration request, e.g., X-VRDB Version 3.1.a.


### <a name="18_0_2_6340208_1455906719413_171772_4514"></a>*The **VoterRecordsResponse** Class*

![Image of VoterRecordsResponse](VRI_UML_Documentation_files/18_0_2_6340208_1455906719422_329791_4515.png)

The root element for response messages.  

 

For defining items pertaining to the status of a response to a voter records request. [VoterRecordsResponse](#18_0_2_6340208_1455906719413_171772_4514) is an abstract class with four subtypes that get used according to the type of response:

 *  [RequestAcknowledgement](#18_0_2_6340208_1456261767184_144968_4436), used to indicate an acknowledgement only.
 *  [VoterRecordResults](#18_5_3_43701b0_1523305927438_977151_6481), used to provide a set of voter records.
 *  [RequestRejection](#18_0_2_6340208_1458226815148_390496_4430), used to indicate a failure and the type of failure.
 *  [RequestSuccess](#18_0_2_6340208_1460483674993_168854_4684), used to indication that a successful action occurred and the type of action, which may differ from the type of action requested.

[VoterRecordsResponse](#18_0_2_6340208_1455906719413_171772_4514) optionally includes the [TransactionId](#18_2_43401a7_1463060312154_514212_4530) attribute associated with the voter records request.  


Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
<a name="18_2_43401a7_1463060312154_514212_4530"></a>`TransactionId`|0..1|`String`|Transaction ID associated with the voter records request.
