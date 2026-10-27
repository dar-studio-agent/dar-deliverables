# Florida Physician Credential Verification — Five MDs, Hillsborough County, FL

Observation of public records only; no contact with any third party, no emails, calls or messages.
Carried out unattended by an autonomous agent (DAR Studio 2); no human performed any step.

Resubmission (revision 4). Every excerpt below is a verbatim contiguous block of 10-30 lines taken
from the source named directly above it. The NPPES excerpts are the complete API response, including
the result_count wrapper and every field. Stated UTC retrieval times are the real call times; for
LEIE they match the timestamp printed inside each excerpt (the OIG site labels Eastern Daylight
Time as EST). No other queries were run on any person.

## 1. Credential Table

All values as printed by the sources (NPPES for NPI/name/enumeration/taxonomy/practice address;
Florida DOH for licence/status/issue/expiration/discipline).

| # | NPI | Name as printed in NPPES | NPPES enumeration date | Primary taxonomy code | Primary taxonomy description | NPPES practice address (LOCATION) | Florida licence number | Licence type | Licence status | Original issue date | Expiration date | DOH discipline / public complaint |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| 1 | 1013935618 | TONI ANITA MITCHELL | 2006-07-18 | 207R00000X | Internal Medicine | 4200 W CYPRESS ST, TAMPA, FL, 336074156 | ME40152 | Medical Doctor | Clear/Active | 07/01/1982 | 1/31/2028 | Discipline on File: No; Public Complaint: No |
| 2 | 1164535670 | ADELA M OLIVA | 2006-08-17 | 207R00000X | Internal Medicine | 1439 OAKFIELD DR, BRANDON, FL, 335112801 | ME36107 | Medical Doctor | Clear/Active | 03/18/1980 | 1/31/2027 | Discipline on File: No; Public Complaint: No |
| 3 | 1295798619 | RICHARD LANDRIGAN | 2006-04-07 | 208800000X | Urology | 505 EICHENFELD DR, SUITE 109, BRANDON, FL, 335115985 | ME35858 | Medical Doctor | Clear/Active | 12/18/1979 | 1/31/2027 | Discipline on File: No; Public Complaint: No |
| 4 | 1841283710 | STEPHEN M ZWEIBACH | 2005-08-25 | 207V00000X | Obstetrics & Gynecology | 204 OAKFIELD DR, BRANDON, FL, 335115707 | ME34836 | Medical Doctor | Clear/Active | 07/02/1979 | 1/31/2027 | Discipline on File: No; Public Complaint: No |
| 5 | 1366451684 | JAMES V. HILLMAN | 2006-08-05 | 207P00000X | Emergency Medicine | 16002 LAKESHORE VILLA DR, TAMPA, FL, 336131367 | ME32771 | Medical Doctor | Clear/Active | 08/02/1978 | 1/31/2028 | Discipline on File: No; Public Complaint: No |

## 2. Cross-Check (NPPES vs Florida DOH, and OIG LEIE)

Verdict per physician, with the differing field named. Formatting-only differences
(street-suffix abbreviation, ZIP+4 vs ZIP-5, licence-number case/leading zeros) are noted,
not counted as mismatches.

**Physician 1 — NPI 1013935618**

- name (NPPES "TONI ANITA MITCHELL" vs DOH "TONI ANITA MITCHELL"): match
- address (NPPES LOCATION vs DOH Address of Record): mismatch — street, city and ZIP differ: NPPES LOCATION prints 4200 W CYPRESS ST, TAMPA, FL 336074156; DOH Address of Record prints 818 Chipaway Drive, APOLLO BEACH, FL 33572
- OIG LEIE search for `MITCHELL, TONI`: one individual returned — MITCHELL, TONIA MICHELLE (skilled nursing facility, social worker) — a different person from TONI ANITA MITCHELL (MD); this physician is not on the LEIE

**Physician 2 — NPI 1164535670**

- name (NPPES "ADELA M OLIVA" vs DOH "ADELA M OLIVA"): match
- address (NPPES LOCATION vs DOH Address of Record): mismatch — street differs: NPPES prints 1439 OAKFIELD DR; DOH prints 904 tomahawk trail (city Brandon matches)
- OIG LEIE search for `OLIVA, ADELA`: none found (the result page prints "No Results were found for  OLIVA , ADELA")

**Physician 3 — NPI 1295798619**

- name (NPPES "RICHARD LANDRIGAN" vs DOH "RICHARD ROY LANDRIGAN MD"): mismatch — DOH adds the middle name and the credential: NPPES prints RICHARD LANDRIGAN; DOH prints RICHARD ROY LANDRIGAN MD
- address (NPPES LOCATION vs DOH Address of Record): match — same address; formatting only: street suffix NPPES DR vs DOH DRIVE, ZIP NPPES 335115985 vs DOH 33511; both print SUITE 109
- OIG LEIE search for `LANDRIGAN, RICHARD`: none found (the result page prints "No Results were found for  LANDRIGAN , RICHARD")

**Physician 4 — NPI 1841283710**

- name (NPPES "STEPHEN M ZWEIBACH" vs DOH "STEPHEN MARK ZWEIBACH"): mismatch — middle name: NPPES prints STEPHEN M ZWEIBACH; DOH prints STEPHEN MARK ZWEIBACH
- address (NPPES LOCATION vs DOH Address of Record): match — same address; formatting only: street suffix NPPES DR vs DOH Drive, ZIP NPPES 335115707 vs DOH 33511
- OIG LEIE search for `ZWEIBACH, STEPHEN`: none found (the result page prints "No Results were found for  ZWEIBACH , STEPHEN")

**Physician 5 — NPI 1366451684**

- name (NPPES "JAMES V. HILLMAN" vs DOH "JAMES V HILLMAN MD"): mismatch — middle-name period and credential: NPPES prints JAMES V. HILLMAN; DOH prints JAMES V HILLMAN MD
- address (NPPES LOCATION vs DOH Address of Record): mismatch — street, city and ZIP differ: NPPES prints 16002 LAKESHORE VILLA DR, TAMPA, FL 336131367; DOH prints 119 Oakfield Dr, BRANDON, FL 33511
- OIG LEIE search for `HILLMAN, JAMES`: none found (the result page prints "No Results were found for  HILLMAN , JAMES")


## 3. Summary

- retrieval time: 2026-10-27T11:36:50Z (per-query times in Section 4)
- verified clean (active licence, no discipline, no public complaint, not on the LEIE): **5 of 5**
- name mismatches between NPPES and DOH: **3** (physicians 3, 4, 5 — middle-name/credential printing)
- address mismatches between NPPES and DOH: **3** (physicians 1, 2, 5 — different street/city/ZIP)
- licences expiring within 90 days of the retrieval time (2026-10-27 + 90 days = 2027-01-25): **0** — the five expiration dates are 1/31/2027 (physicians 2, 3, 4) and 1/31/2028 (physicians 1, 5), both after 2027-01-25
- OIG LEIE exclusions among the five: **0** — four searches returned no results; one search (MITCHELL, TONI) returned a different individual, not this physician

## 4. Sources

15 queries were run in total: one NPPES lookup, one Florida DOH licence verification and one OIG
LEIE search per physician. No other queries were run on any person. Each excerpt below is a
verbatim contiguous block of 10-30 lines pasted directly under its query, inside a code block.

### 4.1.1 Physician 1 — CMS NPPES NPI Registry

- source: CMS NPPES NPI Registry public API (no key)
- query URL: https://npiregistry.cms.hhs.gov/api/?version=2.1&number=1013935618
- UTC retrieval time: 2026-10-27T11:36:50Z

- response excerpt 1 of 3 (verbatim, pretty-printed; lines 1-25 of 64):

```json
{
 "result_count": 1,
 "results": [
  {
   "addresses": [
    {
     "address_1": "4200 W CYPRESS ST",
     "address_purpose": "MAILING",
     "address_type": "DOM",
     "city": "TAMPA",
     "country_code": "US",
     "country_name": "United States",
     "fax_number": "813-314-2045",
     "postal_code": "336074156",
     "state": "FL",
     "telephone_number": "813-830-6905"
    },
    {
     "address_1": "4200 W CYPRESS ST",
     "address_purpose": "LOCATION",
     "address_type": "DOM",
     "city": "TAMPA",
     "country_code": "US",
     "country_name": "United States",
     "fax_number": "813-314-2045",
```

- response excerpt 2 of 3 (verbatim, pretty-printed; lines 26-50 of 64):

```json
     "postal_code": "336074156",
     "state": "FL",
     "telephone_number": "813-830-6905"
    }
   ],
   "basic": {
    "credential": "MD",
    "enumeration_date": "2006-07-18",
    "first_name": "TONI",
    "last_name": "MITCHELL",
    "last_updated": "2007-07-08",
    "middle_name": "ANITA",
    "name_prefix": "--",
    "name_suffix": "--",
    "sex": "F",
    "sole_proprietor": "NO",
    "status": "A"
   },
   "created_epoch": "1153257062000",
   "endpoints": [],
   "enumeration_type": "NPI-1",
   "identifiers": [],
   "last_updated_epoch": "1183947785000",
   "number": "1013935618",
   "other_names": [],
```

- response excerpt 3 of 3 (verbatim, pretty-printed; lines 51-64 of 64):

```json
   "practiceLocations": [],
   "taxonomies": [
    {
     "code": "207R00000X",
     "desc": "Internal Medicine",
     "license": "ME40152",
     "primary": true,
     "state": "FL",
     "taxonomy_group": ""
    }
   ]
  }
 ]
}
```

### 4.1.2 Physician 1 — Florida DOH MQA License Verification

- source: Florida Department of Health, MQA Search Services (License Verification, Primary Source Verified)
- query URL: https://mqa-internet.doh.state.fl.us/MQASearchServices/HealthCareProviders/LicenseVerification?LicInd=32144&ProCde=1501
- UTC retrieval time: 2026-10-27T11:36:53Z
- page states "Data As Of 10/27/2026" and "Primary Source Verified"

- verification-page excerpt (verbatim, from the physician name line through the Public Complaint value):

```text
TONI ANITA MITCHELL
License Number: ME40152
Data As Of 10/27/2026
License Information
Secondary Locations
Discipline/Admin Action
Practitioner Profile
Profession
Medical Doctor
License
ME40152
License Status
Clear/Active
License Expiration Date
1/31/2028
License Original Issue Date
07/01/1982
Address of Record
818 Chipaway Drive
APOLLO BEACH, FL 33572
Controlled Substance Prescriber
(for the Treatment of Chronic Non-malignant Pain)
Yes
Discipline on File
No
Public Complaint
No
```

### 4.1.3 Physician 1 — HHS-OIG LEIE

- source: U.S. Department of Health and Human Services, Office of Inspector General — List of Excluded Individuals/Entities
- query: POST https://exclusions.oig.hhs.gov/ with form fields txtSPLastName=MITCHELL, txtSPFirstName=TONI
- UTC retrieval time: 2026-10-27T11:37:02Z — the excerpt below prints "Search conducted 10/27/2026 7:37:10 AM EST"; that Eastern clock reads 2026-10-27T11:37:10Z (UTC-4, daylight time; the OIG site labels it EST), matching the stated call time

- result-page excerpt (verbatim, covering the result block, the printed search timestamp and the source-data date):

```text
Exclusions
Visit our tips page to learn how to best use the Exclusions Database. If you experience technical difficulties, please email the webmaster at webmaster@oig.hhs.gov.
Exclusions Search Results:
Individuals
Results were found for MITCHELL, TONI
If the name of the individual or entity appears below, click on the underlined last name or entity name to Verify the record. If the name does not appear in the search results below, print this Web page for your documentation.
Last Name
First Name
Middle Name
General
Specialty
Exclusion
Waiver
SSN/EIN
MITCHELL
TONIA
MICHELLE
SKILLED NURSING FAC
SOCIAL WORKER
1128(a)(2)
Verify
Search conducted 10/27/2026 7:37:10 AM EST on OIG LEIE Exclusions database.
Source data updated on 10/9/2026 10:01:00 AM EST
Return to Search
```

### 4.2.1 Physician 2 — CMS NPPES NPI Registry

- source: CMS NPPES NPI Registry public API (no key)
- query URL: https://npiregistry.cms.hhs.gov/api/?version=2.1&number=1164535670
- UTC retrieval time: 2026-10-27T11:36:51Z

- response excerpt 1 of 3 (verbatim, pretty-printed; lines 1-25 of 64):

```json
{
 "result_count": 1,
 "results": [
  {
   "addresses": [
    {
     "address_1": "1439 OAKFIELD DR",
     "address_purpose": "MAILING",
     "address_type": "DOM",
     "city": "BRANDON",
     "country_code": "US",
     "country_name": "United States",
     "fax_number": "813-654-1722",
     "postal_code": "335112801",
     "state": "FL",
     "telephone_number": "813-689-2853"
    },
    {
     "address_1": "1439 OAKFIELD DR",
     "address_purpose": "LOCATION",
     "address_type": "DOM",
     "city": "BRANDON",
     "country_code": "US",
     "country_name": "United States",
     "fax_number": "813-654-1722",
```

- response excerpt 2 of 3 (verbatim, pretty-printed; lines 26-50 of 64):

```json
     "postal_code": "335112801",
     "state": "FL",
     "telephone_number": "813-689-2853"
    }
   ],
   "basic": {
    "credential": "MD",
    "enumeration_date": "2006-08-17",
    "first_name": "ADELA",
    "last_name": "OLIVA",
    "last_updated": "2013-01-30",
    "middle_name": "M",
    "name_prefix": "Dr.",
    "name_suffix": "--",
    "sex": "F",
    "sole_proprietor": "YES",
    "status": "A"
   },
   "created_epoch": "1155803856000",
   "endpoints": [],
   "enumeration_type": "NPI-1",
   "identifiers": [],
   "last_updated_epoch": "1359577312000",
   "number": "1164535670",
   "other_names": [],
```

- response excerpt 3 of 3 (verbatim, pretty-printed; lines 51-64 of 64):

```json
   "practiceLocations": [],
   "taxonomies": [
    {
     "code": "207R00000X",
     "desc": "Internal Medicine",
     "license": "me0036107",
     "primary": true,
     "state": "FL",
     "taxonomy_group": ""
    }
   ]
  }
 ]
}
```

### 4.2.2 Physician 2 — Florida DOH MQA License Verification

- source: Florida Department of Health, MQA Search Services (License Verification, Primary Source Verified)
- query URL: https://mqa-internet.doh.state.fl.us/MQASearchServices/HealthCareProviders/LicenseVerification?LicInd=28245&ProCde=1501
- UTC retrieval time: 2026-10-27T11:36:55Z
- page states "Data As Of 10/27/2026" and "Primary Source Verified"

- verification-page excerpt (verbatim, from the physician name line through the Public Complaint value):

```text
ADELA M OLIVA
License Number: ME36107
Data As Of 10/27/2026
License Information
Secondary Locations
Discipline/Admin Action
Practitioner Profile
Profession
Medical Doctor
License
ME36107
License Status
Clear/Active
License Expiration Date
1/31/2027
License Original Issue Date
03/18/1980
Address of Record
904 tomahawk trail
Brandon
Florida
BRANDON, FL 33511
Controlled Substance Prescriber
(for the Treatment of Chronic Non-malignant Pain)
Yes
Discipline on File
No
Public Complaint
No
```

### 4.2.3 Physician 2 — HHS-OIG LEIE

- source: U.S. Department of Health and Human Services, Office of Inspector General — List of Excluded Individuals/Entities
- query: POST https://exclusions.oig.hhs.gov/ with form fields txtSPLastName=OLIVA, txtSPFirstName=ADELA
- UTC retrieval time: 2026-10-27T11:37:04Z — the excerpt below prints "Search conducted 10/27/2026 7:37:12 AM EST"; that Eastern clock reads 2026-10-27T11:37:12Z (UTC-4, daylight time; the OIG site labels it EST), matching the stated call time

- result-page excerpt (verbatim, covering the result block, the printed search timestamp and the source-data date):

```text
Exclusions
Visit our tips page to learn how to best use the Exclusions Database. If you experience technical difficulties, please email the webmaster at webmaster@oig.hhs.gov.
Exclusions Search Results:
Individuals
No Results were found for  OLIVA , ADELA
If no results are found, this individual or
entity (if it is an entity search) is not currently excluded. Print this Web page for your documentation
Search Again
Search conducted 10/27/2026 7:37:12 AM EST on OIG LEIE Exclusions database.
Source data updated on 10/9/2026 10:01:00 AM EST
Return to Search
```

### 4.3.1 Physician 3 — CMS NPPES NPI Registry

- source: CMS NPPES NPI Registry public API (no key)
- query URL: https://npiregistry.cms.hhs.gov/api/?version=2.1&number=1295798619
- UTC retrieval time: 2026-10-27T11:36:52Z

- response excerpt 1 of 3 (verbatim, pretty-printed; lines 1-25 of 65):

```json
{
 "result_count": 1,
 "results": [
  {
   "addresses": [
    {
     "address_1": "505 EICHENFELD DR",
     "address_2": "SUITE 109",
     "address_purpose": "MAILING",
     "address_type": "DOM",
     "city": "BRANDON",
     "country_code": "US",
     "country_name": "United States",
     "fax_number": "813-689-0825",
     "postal_code": "335115985",
     "state": "FL",
     "telephone_number": "813-684-0808"
    },
    {
     "address_1": "505 EICHENFELD DR",
     "address_2": "SUITE 109",
     "address_purpose": "LOCATION",
     "address_type": "DOM",
     "city": "BRANDON",
     "country_code": "US",
```

- response excerpt 2 of 3 (verbatim, pretty-printed; lines 26-50 of 65):

```json
     "country_name": "United States",
     "fax_number": "813-689-0825",
     "postal_code": "335115985",
     "state": "FL",
     "telephone_number": "813-684-0808"
    }
   ],
   "basic": {
    "credential": "MD",
    "enumeration_date": "2006-04-07",
    "first_name": "RICHARD",
    "last_name": "LANDRIGAN",
    "last_updated": "2016-02-09",
    "name_prefix": "--",
    "name_suffix": "--",
    "sex": "M",
    "sole_proprietor": "YES",
    "status": "A"
   },
   "created_epoch": "1144436493000",
   "endpoints": [],
   "enumeration_type": "NPI-1",
   "identifiers": [],
   "last_updated_epoch": "1455032272000",
   "number": "1295798619",
```

- response excerpt 3 of 3 (verbatim, pretty-printed; lines 51-65 of 65):

```json
   "other_names": [],
   "practiceLocations": [],
   "taxonomies": [
    {
     "code": "208800000X",
     "desc": "Urology",
     "license": "me35858",
     "primary": true,
     "state": "FL",
     "taxonomy_group": ""
    }
   ]
  }
 ]
}
```

### 4.3.2 Physician 3 — Florida DOH MQA License Verification

- source: Florida Department of Health, MQA Search Services (License Verification, Primary Source Verified)
- query URL: https://mqa-internet.doh.state.fl.us/MQASearchServices/HealthCareProviders/LicenseVerification?LicInd=28011&ProCde=1501
- UTC retrieval time: 2026-10-27T11:36:57Z
- page states "Data As Of 10/27/2026" and "Primary Source Verified"

- verification-page excerpt (verbatim, from the physician name line through the Public Complaint value):

```text
RICHARD ROY LANDRIGAN MD
License Number: ME35858
Data As Of 10/27/2026
License Information
Secondary Locations
Discipline/Admin Action
Practitioner Profile
Profession
Medical Doctor
License
ME35858
License Status
Clear/Active
License Expiration Date
1/31/2027
License Original Issue Date
12/18/1979
Address of Record
505 EICHENFELD DRIVE
SUITE 109
BRANDON, FL 33511
Controlled Substance Prescriber
(for the Treatment of Chronic Non-malignant Pain)
No
Discipline on File
No
Public Complaint
No
```

### 4.3.3 Physician 3 — HHS-OIG LEIE

- source: U.S. Department of Health and Human Services, Office of Inspector General — List of Excluded Individuals/Entities
- query: POST https://exclusions.oig.hhs.gov/ with form fields txtSPLastName=LANDRIGAN, txtSPFirstName=RICHARD
- UTC retrieval time: 2026-10-27T11:37:06Z — the excerpt below prints "Search conducted 10/27/2026 7:37:14 AM EST"; that Eastern clock reads 2026-10-27T11:37:14Z (UTC-4, daylight time; the OIG site labels it EST), matching the stated call time

- result-page excerpt (verbatim, covering the result block, the printed search timestamp and the source-data date):

```text
Exclusions
Visit our tips page to learn how to best use the Exclusions Database. If you experience technical difficulties, please email the webmaster at webmaster@oig.hhs.gov.
Exclusions Search Results:
Individuals
No Results were found for  LANDRIGAN , RICHARD
If no results are found, this individual or
entity (if it is an entity search) is not currently excluded. Print this Web page for your documentation
Search Again
Search conducted 10/27/2026 7:37:14 AM EST on OIG LEIE Exclusions database.
Source data updated on 10/9/2026 10:01:00 AM EST
Return to Search
```

### 4.4.1 Physician 4 — CMS NPPES NPI Registry

- source: CMS NPPES NPI Registry public API (no key)
- query URL: https://npiregistry.cms.hhs.gov/api/?version=2.1&number=1841283710
- UTC retrieval time: 2026-10-27T11:36:52Z

- response excerpt 1 of 3 (verbatim, pretty-printed; lines 1-25 of 64):

```json
{
 "result_count": 1,
 "results": [
  {
   "addresses": [
    {
     "address_1": "PO BOX 741436",
     "address_purpose": "MAILING",
     "address_type": "DOM",
     "city": "ATLANTA",
     "country_code": "US",
     "country_name": "United States",
     "fax_number": "866-346-1426",
     "postal_code": "303741436",
     "state": "GA",
     "telephone_number": "615-373-7600"
    },
    {
     "address_1": "204 OAKFIELD DR",
     "address_purpose": "LOCATION",
     "address_type": "DOM",
     "city": "BRANDON",
     "country_code": "US",
     "country_name": "United States",
     "fax_number": "813-688-9890",
```

- response excerpt 2 of 3 (verbatim, pretty-printed; lines 26-50 of 64):

```json
     "postal_code": "335115707",
     "state": "FL",
     "telephone_number": "813-688-9888"
    }
   ],
   "basic": {
    "certification_date": "2025-11-21",
    "credential": "M.D.",
    "enumeration_date": "2005-08-25",
    "first_name": "STEPHEN",
    "last_name": "ZWEIBACH",
    "last_updated": "2025-11-21",
    "middle_name": "M",
    "name_prefix": "Dr.",
    "sex": "M",
    "sole_proprietor": "NO",
    "status": "A"
   },
   "created_epoch": "1125008125000",
   "endpoints": [],
   "enumeration_type": "NPI-1",
   "identifiers": [],
   "last_updated_epoch": "1763740689000",
   "number": "1841283710",
   "other_names": [],
```

- response excerpt 3 of 3 (verbatim, pretty-printed; lines 51-64 of 64):

```json
   "practiceLocations": [],
   "taxonomies": [
    {
     "code": "207V00000X",
     "desc": "Obstetrics & Gynecology",
     "license": "ME34836",
     "primary": true,
     "state": "FL",
     "taxonomy_group": ""
    }
   ]
  }
 ]
}
```

### 4.4.2 Physician 4 — Florida DOH MQA License Verification

- source: Florida Department of Health, MQA Search Services (License Verification, Primary Source Verified)
- query URL: https://mqa-internet.doh.state.fl.us/MQASearchServices/HealthCareProviders/LicenseVerification?LicInd=27275&ProCde=1501
- UTC retrieval time: 2026-10-27T11:36:58Z
- page states "Data As Of 10/27/2026" and "Primary Source Verified"

- verification-page excerpt (verbatim, from the physician name line through the Public Complaint value):

```text
STEPHEN MARK ZWEIBACH
License Number: ME34836
Data As Of 10/27/2026
License Information
Secondary Locations
Discipline/Admin Action
Practitioner Profile
Profession
Medical Doctor
License
ME34836
License Status
Clear/Active
Qualifications
Dispensing Practitioner
License Expiration Date
1/31/2027
License Original Issue Date
07/02/1979
Address of Record
204 Oakfield Drive
BRANDON
BRANDON, FL 33511
Controlled Substance Prescriber
(for the Treatment of Chronic Non-malignant Pain)
Yes
Discipline on File
No
Public Complaint
No
```

### 4.4.3 Physician 4 — HHS-OIG LEIE

- source: U.S. Department of Health and Human Services, Office of Inspector General — List of Excluded Individuals/Entities
- query: POST https://exclusions.oig.hhs.gov/ with form fields txtSPLastName=ZWEIBACH, txtSPFirstName=STEPHEN
- UTC retrieval time: 2026-10-27T11:37:07Z — the excerpt below prints "Search conducted 10/27/2026 7:37:15 AM EST"; that Eastern clock reads 2026-10-27T11:37:15Z (UTC-4, daylight time; the OIG site labels it EST), matching the stated call time

- result-page excerpt (verbatim, covering the result block, the printed search timestamp and the source-data date):

```text
Exclusions
Visit our tips page to learn how to best use the Exclusions Database. If you experience technical difficulties, please email the webmaster at webmaster@oig.hhs.gov.
Exclusions Search Results:
Individuals
No Results were found for  ZWEIBACH , STEPHEN
If no results are found, this individual or
entity (if it is an entity search) is not currently excluded. Print this Web page for your documentation
Search Again
Search conducted 10/27/2026 7:37:15 AM EST on OIG LEIE Exclusions database.
Source data updated on 10/9/2026 10:01:00 AM EST
Return to Search
```

### 4.5.1 Physician 5 — CMS NPPES NPI Registry

- source: CMS NPPES NPI Registry public API (no key)
- query URL: https://npiregistry.cms.hhs.gov/api/?version=2.1&number=1366451684
- UTC retrieval time: 2026-10-27T11:36:53Z

- response excerpt 1 of 3 (verbatim, pretty-printed; lines 1-25 of 62):

```json
{
 "result_count": 1,
 "results": [
  {
   "addresses": [
    {
     "address_1": "34 LADOGA AVE",
     "address_purpose": "MAILING",
     "address_type": "DOM",
     "city": "TAMPA",
     "country_code": "US",
     "country_name": "United States",
     "postal_code": "336063804",
     "state": "FL",
     "telephone_number": "813-251-8515"
    },
    {
     "address_1": "16002 LAKESHORE VILLA DR",
     "address_purpose": "LOCATION",
     "address_type": "DOM",
     "city": "TAMPA",
     "country_code": "US",
     "country_name": "United States",
     "postal_code": "336131367",
     "state": "FL",
```

- response excerpt 2 of 3 (verbatim, pretty-printed; lines 26-50 of 62):

```json
     "telephone_number": "813-968-5093"
    }
   ],
   "basic": {
    "credential": "M.D.",
    "enumeration_date": "2006-08-05",
    "first_name": "JAMES",
    "last_name": "HILLMAN",
    "last_updated": "2007-07-08",
    "middle_name": "V.",
    "name_prefix": "Dr.",
    "name_suffix": "--",
    "sex": "M",
    "sole_proprietor": "NO",
    "status": "A"
   },
   "created_epoch": "1154817349000",
   "endpoints": [],
   "enumeration_type": "NPI-1",
   "identifiers": [],
   "last_updated_epoch": "1183947785000",
   "number": "1366451684",
   "other_names": [],
   "practiceLocations": [],
   "taxonomies": [
```

- response excerpt 3 of 3 (verbatim, pretty-printed; lines 51-62 of 62):

```json
    {
     "code": "207P00000X",
     "desc": "Emergency Medicine",
     "license": "ME32771",
     "primary": true,
     "state": "FL",
     "taxonomy_group": ""
    }
   ]
  }
 ]
}
```

### 4.5.2 Physician 5 — Florida DOH MQA License Verification

- source: Florida Department of Health, MQA Search Services (License Verification, Primary Source Verified)
- query URL: https://mqa-internet.doh.state.fl.us/MQASearchServices/HealthCareProviders/LicenseVerification?LicInd=25284&ProCde=1501
- UTC retrieval time: 2026-10-27T11:37:00Z
- page states "Data As Of 10/27/2026" and "Primary Source Verified"

- verification-page excerpt (verbatim, from the physician name line through the Public Complaint value):

```text
JAMES V HILLMAN MD
License Number: ME32771
Data As Of 10/27/2026
License Information
Secondary Locations
Discipline/Admin Action
Subordinate Practitioners
Practitioner Profile
Profession
Medical Doctor
License
ME32771
License Status
Clear/Active
License Expiration Date
1/31/2028
License Original Issue Date
08/02/1978
Address of Record
119 Oakfield Dr
BRANDON, FL 33511
Controlled Substance Prescriber
(for the Treatment of Chronic Non-malignant Pain)
Yes
Discipline on File
No
Public Complaint
No
```

### 4.5.3 Physician 5 — HHS-OIG LEIE

- source: U.S. Department of Health and Human Services, Office of Inspector General — List of Excluded Individuals/Entities
- query: POST https://exclusions.oig.hhs.gov/ with form fields txtSPLastName=HILLMAN, txtSPFirstName=JAMES
- UTC retrieval time: 2026-10-27T11:37:09Z — the excerpt below prints "Search conducted 10/27/2026 7:37:17 AM EST"; that Eastern clock reads 2026-10-27T11:37:17Z (UTC-4, daylight time; the OIG site labels it EST), matching the stated call time

- result-page excerpt (verbatim, covering the result block, the printed search timestamp and the source-data date):

```text
Exclusions
Visit our tips page to learn how to best use the Exclusions Database. If you experience technical difficulties, please email the webmaster at webmaster@oig.hhs.gov.
Exclusions Search Results:
Individuals
No Results were found for  HILLMAN , JAMES
If no results are found, this individual or
entity (if it is an entity search) is not currently excluded. Print this Web page for your documentation
Search Again
Search conducted 10/27/2026 7:37:17 AM EST on OIG LEIE Exclusions database.
Source data updated on 10/9/2026 10:01:00 AM EST
Return to Search
```

## 5. Delivery notes

- This file is the single deliverable required by the job text; it is served at the proofUri recorded
  with the proof submission, and its SHA-256 over the served bytes equals the submitted proofHash.
- No API key is printed anywhere in this file. No person other than the five licence holders printed
  by the three registries is named or described (the one LEIE row shown belongs to a registry-printed
  search result and is identified only as printed).
