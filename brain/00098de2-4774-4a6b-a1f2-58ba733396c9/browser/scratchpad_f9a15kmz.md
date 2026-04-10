# Task Plan: Extract Filing Transaction IDs for Los Romeros Limited

## Steps:
- [x] Navigate to the filing history page: `https://find-and-update.company-information.service.gov.uk/company/06993349/filing-history`
- [x] Extract filing data (date, type, description, txId, href) from the first page.
- [x] Check for pagination and extract from subsequent pages if they exist.
- [x] Take a screenshot for validation.
- [ ] Consolidate JSON output and total count.
- [ ] Report results.

## Final Filing Data (70 filings)
```json
[
  {
    "date": "10 Feb 2026",
    "type": "TM01",
    "desc": "Termination of appointment of Beryl Harrison as a director",
    "txId": "MzUwNDA3OTM3M2FkaXF6a2N4",
    "href": "/company/06993349/filing-history/MzUwNDA3OTM3M2FkaXF6a2N4/document?format=pdf&download=0"
  },
  {
    "date": "19 Dec 2025",
    "type": "AA",
    "desc": "Total exemption full accounts made up to 31 August 2025",
    "txId": "MzQ5NTM0Mzg5OWFkaXF6a2N4",
    "href": "/company/06993349/filing-history/MzQ5NTM0Mzg5OWFkaXF6a2N4/document?format=pdf&download=0"
  },
  {
    "date": "27 Oct 2025",
    "type": "CH04",
    "desc": "Secretary's details changed for Adrem Accounting Ltd",
    "txId": "MzQ4NjQwNzMxN2FkaXF6a2N4",
    "href": "/company/06993349/filing-history/MzQ4NjQwNzMxN2FkaXF6a2N4/document?format=pdf&download=0"
  },
  {
    "date": "25 Sep 2025",
    "type": "AD01",
    "desc": "Registered office address changed from Wincham House to 4 Market Street",
    "txId": "MzQ4MjY3ODc3MGFkaXF6a2N4",
    "href": "/company/06993349/filing-history/MzQ4MjY3ODc3MGFkaXF6a2N4/document?format=pdf&download=0"
  },
  {
    "date": "27 Aug 2025",
    "type": "CS01",
    "desc": "Confirmation statement made on 18 August 2025 with no updates",
    "txId": "MzQ3ODgwMjk5M2FkaXF6a2N4",
    "href": "/company/06993349/filing-history/MzQ3ODgwMjk5M2FkaXF6a2N4/document?format=pdf&download=0"
  },
  {
    "date": "19 Dec 2024",
    "type": "AA",
    "desc": "Total exemption full accounts made up to 31 August 2024",
    "txId": "MzQ0ODM0NTM2NWFkaXF6a2N4",
    "href": "/company/06993349/filing-history/MzQ0ODM0NTM2NWFkaXF6a2N4/document?format=pdf&download=0"
  },
  {
    "date": "20 Aug 2024",
    "type": "CS01",
    "desc": "Confirmation statement made on 18 August 2024 with no updates",
    "txId": "MzQzMjczMjgxNWFkaXF6a2N4",
    "href": "/company/06993349/filing-history/MzQzMjczMjgxNWFkaXF6a2N4/document?format=pdf&download=0"
  },
  {
    "date": "25 Jun 2024",
    "type": "CH04",
    "desc": "Secretary's details changed for Wincham Accountancy Limited",
    "txId": "MzQyNjUxNDQwNWFkaXF6a2N4",
    "href": "/company/06993349/filing-history/MzQyNjUxNDQwNWFkaXF6a2N4/document?format=pdf&download=0"
  },
  {
    "date": "14 Mar 2024",
    "type": "AA",
    "desc": "Total exemption full accounts made up to 31 August 2023",
    "txId": "MzQxNDU0MzYzMmFkaXF6a2N4",
    "href": "/company/06993349/filing-history/MzQxNDU0MzYzMmFkaXF6a2N4/document?format=pdf&download=0"
  },
  {
    "date": "21 Aug 2023",
    "type": "CS01",
    "desc": "Confirmation statement made on 18 August 2023 with no updates",
    "txId": "MzM5MDE4ODE2M2FkaXF6a2N4",
    "href": "/company/06993349/filing-history/MzM5MDE4ODE2M2FkaXF6a2N4/document?format=pdf&download=0"
  },
  {
    "date": "26 May 2023",
    "type": "AA",
    "desc": "Total exemption full accounts made up to 31 August 2022",
    "txId": "MzM4MDk3MzAzOGFkaXF6a2N4",
    "href": "/company/06993349/filing-history/MzM4MDk3MzAzOGFkaXF6a2N4/document?format=pdf&download=0"
  },
  {
    "date": "19 Aug 2022",
    "type": "CS01",
    "desc": "Confirmation statement made on 18 August 2022 with no updates",
    "txId": "MzM0OTE1NTIwNGFkaXF6a2N4",
    "href": "/company/06993349/filing-history/MzM0OTE1NTIwNGFkaXF6a2N4/document?format=pdf&download=0"
  },
  {
    "date": "20 May 2022",
    "type": "AA",
    "desc": "Total exemption full accounts made up to 31 August 2021",
    "txId": "MzMzOTk4ODA0OGFkaXF6a2N4",
    "href": "/company/06993349/filing-history/MzMzOTk4ODA0OGFkaXF6a2N4/document?format=pdf&download=0"
  },
  {
    "date": "18 Aug 2021",
    "type": "CS01",
    "desc": "Confirmation statement made on 18 August 2021 with updates",
    "txId": "MzMxMDk5NTgzMmFkaXF6a2N4",
    "href": "/company/06993349/filing-history/MzMxMDk5NTgzMmFkaXF6a2N4/document?format=pdf&download=0"
  },
  {
    "date": "18 Aug 2021",
    "type": "AP04",
    "desc": "Appointment of Wincham Accountancy Limited as a secretary",
    "txId": "MzMxMDk5NTMzNGFkaXF6a2N4",
    "href": "/company/06993349/filing-history/MzMxMDk5NTMzNGFkaXF6a2N4/document?format=pdf&download=0"
  },
  {
    "date": "18 Aug 2021",
    "type": "TM02",
    "desc": "Termination of appointment of Wincham Accountants Limited as a secretary",
    "txId": "MzMxMDk5NTI0OWFkaXF6a2N4",
    "href": "/company/06993349/filing-history/MzMxMDk5NTI0OWFkaXF6a2N4/document?format=pdf&download=0"
  },
  {
    "date": "18 Aug 2021",
    "type": "CH04",
    "desc": "Secretary's details changed for Adrem Accounting Ltd",
    "txId": "MzMxMDk5NDk2NmFkaXF6a2N4",
    "href": "/company/06993349/filing-history/MzMxMDk5NDk2NmFkaXF6a2N4/document?format=pdf&download=0"
  },
  {
    "date": "18 Aug 2021",
    "type": "CH01",
    "desc": "Director's details changed for Mrs Mary Ann Stockwell",
    "txId": "MzMxMDk5NDkwNWFkaXF6a2N4",
    "href": "/company/06993349/filing-history/MzMxMDk5NDkwNWFkaXF6a2N4/document?format=pdf&download=0"
  },
  {
    "date": "18 Aug 2021",
    "type": "CH01",
    "desc": "Director's details changed for Mr Bryan Frederick Stockwell",
    "txId": "MzMxMDk5NDgxMWFkaXF6a2N4",
    "href": "/company/06993349/filing-history/MzMxMDk5NDgxMWFkaXF6a2N4/document?format=pdf&download=0"
  },
  {
    "date": "05 Jul 2021",
    "type": "AA",
    "desc": "Total exemption full accounts made up to 31 August 2020",
    "txId": "MzMwNzIxMzc4NGFkaXF6a2N4",
    "href": "/company/06993349/filing-history/MzMwNzIxMzc4NGFkaXF6a2N4/document?format=pdf&download=0"
  },
  {
    "date": "02 Sep 2020",
    "type": "CS01",
    "desc": "Confirmation statement made on 18 August 2020 with updates",
    "txId": "MzI3Njc1Mzk0M2FkaXF6a2N4",
    "href": "/company/06993349/filing-history/MzI3Njc1Mzk0M2FkaXF6a2N4/document?format=pdf&download=0"
  },
  {
    "date": "02 Sep 2020",
    "type": "AD01",
    "desc": "Registered office address changed from 4 Market Street to Wincham House",
    "txId": "MzI3Njc1MzkzMmFkaXF6a2N4",
    "href": "/company/06993349/filing-history/MzI3Njc1MzkzMmFkaXF6a2N4/document?format=pdf&download=0"
  },
  {
    "date": "02 Sep 2020",
    "type": "CH01",
    "desc": "Director's details changed for Mrs Mary Ann Stockwell",
    "txId": "MzI3Njc1MzkxM1FkaXF6a2N4",
    "href": "/company/06993349/filing-history/MzI3Njc1MzkxM1FkaXF6a2N4/document?format=pdf&download=0"
  },
  {
    "date": "02 Sep 2020",
    "type": "CH01",
    "desc": "Director's details changed for Mr Bryan Frederick Stockwell",
    "txId": "MzI3Njc1MzkwMGFkaXF6a2N4",
    "href": "/company/06993349/filing-history/MzI3Njc1MzkwMGFkaXF6a2N4/document?format=pdf&download=0"
  },
  {
    "date": "17 Apr 2020",
    "type": "AA",
    "desc": "Total exemption full accounts made up to 31 August 2019",
    "txId": "MzI2MzEyMTgzNmFkaXF6a2N4",
    "href": "/company/06993349/filing-history/MzI2MzEyMTgzNmFkaXF6a2N4/document?format=pdf&download=0"
  },
  {
    "date": "06 Jan 2020",
    "type": "SH02",
    "desc": "Statement of capital on 23 December 2019 GBP 159,636",
    "txId": "MzI1MzY2ODg3NGFkaXF6a2N4",
    "href": "/company/06993349/filing-history/MzI1MzY2ODg3NGFkaXF6a2N4/document?format=pdf&download=0"
  },
  {
    "date": "30 Dec 2019",
    "type": "TM01",
    "desc": "Termination of appointment of Kevin John Stockwell as a director",
    "txId": "MzI1MzMxOTY0MWFkaXF6a2N4",
    "href": "/company/06993349/filing-history/MzI1MzMxOTY0MWFkaXF6a2N4/document?format=pdf&download=0"
  },
  {
    "date": "27 Dec 2019",
    "type": "TM01",
    "desc": "Termination of appointment of Mrs Mary Ann Stockwell as a director",
    "txId": "MzI1MzMxOTUxOWFkaXF6a2N4",
    "href": "/company/06993349/filing-history/MzI1MzMxOTUxOWFkaXF6a2N4/document?format=pdf&download=0"
  },
  {
    "date": "27 Dec 2019",
    "type": "SH01",
    "desc": "Statement of capital following an allotment of shares on 23 December 2019",
    "txId": "MzI1MzIyNDAzOGFkaXF6a2N4",
    "href": "/company/06993349/filing-history/MzI1MzIyNDAzOGFkaXF6a2N4/document?format=pdf&download=0"
  },
  {
    "date": "23 Dec 2019",
    "type": "AP04",
    "desc": "Appointment of Adrem Accounting Limited as a secretary",
    "txId": "MzI1MzE1Mjk3MmFkaXF6a2N4",
    "href": "/company/06993349/filing-history/MzI1MzE1Mjk3MmFkaXF6a2N4/document?format=pdf&download=0"
  },
  {
    "date": "23 Dec 2019",
    "type": "AP01",
    "desc": "Appointment of Mr Bryan Frederick Stockwell as a director",
    "txId": "MzI1MzE1Mjc5OWFkaXF6a2N4",
    "href": "/company/06993349/filing-history/MzI1MzE1Mjc5OWFkaXF6a2N4/document?format=pdf&download=0"
  },
  {
    "date": "04 Dec 2019",
    "type": "AA",
    "desc": "Total exemption full accounts made up to 31 August 2019",
    "txId": "MzI1MTE3MDkxMWFkaXF6a2N4",
    "href": "/company/06993349/filing-history/MzI1MTE3MDkxMWFkaXF6a2N4/document?format=pdf&download=0"
  },
  {
    "date": "08 Oct 2019",
    "type": "AP01",
    "desc": "Appointment of Mr Mark Damion Roach as a director",
    "txId": "MzI0NjI2NTYwMmFkaXF6a2N4",
    "href": "/company/06993349/filing-history/MzI0NjI2NTYwMmFkaXF6a2N4/document?format=pdf&download=0"
  },
  {
    "date": "07 Oct 2019",
    "type": "AP01",
    "desc": "Appointment of Mr Kevin John Stockwell as a director",
    "txId": "MzI0NjE5MjI5MmFkaXF6a2N4",
    "href": "/company/06993349/filing-history/MzI0NjE5MjI5MmFkaXF6a2N4/document?format=pdf&download=0"
  },
  {
    "date": "07 Oct 2019",
    "type": "TM01",
    "desc": "Termination of appointment of Mark Damion Roach as a director",
    "txId": "MzI0NjE5MTkyM2FkaXF6a2N4",
    "href": "/company/06993349/filing-history/MzI0NjE5MTkyM2FkaXF6a2N4/document?format=pdf&download=0"
  },
  {
    "date": "21 Aug 2019",
    "type": "CS01",
    "desc": "Confirmation statement made on 18 August 2019 with no updates",
    "txId": "MzI0MjI0MDY4NmFkaXF6a2N4",
    "href": "/company/06993349/filing-history/MzI0MjI0MDY4NmFkaXF6a2N4/document?format=pdf&download=0"
  },
  {
    "date": "15 Apr 2019",
    "type": "AA",
    "desc": "Total exemption full accounts made up to 31 August 2018",
    "txId": "MzIzMjA3ODU1OGFkaXF6a2N4",
    "href": "/company/06993349/filing-history/MzIzMjA3ODU1OGFkaXF6a2N4/document?format=pdf&download=0"
  },
  {
    "date": "25 Jan 2019",
    "type": "AP01",
    "desc": "Appointment of Mr Mark Damion Roach as a director",
    "txId": "MzIyNTQxMjQ1NGFkaXF6a2N4",
    "href": "/company/06993349/filing-history/MzIyNTQxMjQ1NGFkaXF6a2N4/document?format=pdf&download=0"
  },
  {
    "date": "25 Jan 2019",
    "type": "TM01",
    "desc": "Termination of appointment of Bryan Frederick Stockwell as a director",
    "txId": "MzIyNTQxMjM4NmFkaXF6a2N4",
    "href": "/company/06993349/filing-history/MzIyNTQxMjM4NmFkaXF6a2N4/document?format=pdf&download=0"
  },
  {
    "date": "25 Jan 2019",
    "type": "PSC04",
    "desc": "Change of details for Mrs Mary Ann Stockwell on 23 January 2019",
    "txId": "MzIyNTQxMjI5M2FkaXF6a2N4",
    "href": "/company/06993349/filing-history/MzIyNTQxMjI5M2FkaXF6a2N4/document?format=pdf&download=0"
  },
  {
    "date": "25 Jan 2019",
    "type": "PSC07",
    "desc": "Cessation of Bryan Frederick Stockwell as a person with significant control",
    "txId": "MzIyNTQxMjI4MmFkaXF6a2N4",
    "href": "/company/06993349/filing-history/MzIyNTQxMjI4MmFkaXF6a2N4/document?format=pdf&download=0"
  },
  {
    "date": "24 Aug 2018",
    "type": "CS01",
    "desc": "Confirmation statement made on 18 August 2018 with no updates",
    "txId": "MzIxMjg3NTE4OGFkaXF6a2N4",
    "href": "/company/06993349/filing-history/MzIxMjg3NTE4OGFkaXF6a2N4/document?format=pdf&download=0"
  },
  {
    "date": "17 Apr 2018",
    "type": "AA",
    "desc": "Total exemption full accounts made up to 31 August 2017",
    "txId": "MzIwMjc2OTI4MGFkaXF6a2N4",
    "href": "/company/06993349/filing-history/MzIwMjc2OTI4MGFkaXF6a2N4/document?format=pdf&download=0"
  },
  {
    "date": "18 Aug 2017",
    "type": "CS01",
    "desc": "Confirmation statement made on 18 August 2017 with no updates",
    "txId": "MzE4MzUwNDY1MWFkaXF6a2N4",
    "href": "/company/06993349/filing-history/MzE4MzUwNDY1MWFkaXF6a2N4/document?format=pdf&download=0"
  },
  {
    "date": "18 Aug 2017",
    "type": "CH01",
    "desc": "Director's details changed for Mrs Mary Ann Stockwell",
    "txId": "MzE4MzUwNDUwNmFkaXF6a2N4",
    "href": "/company/06993349/filing-history/MzE4MzUwNDUwNmFkaXF6a2N4/document?format=pdf&download=0"
  },
  {
    "date": "11 Aug 2017",
    "type": "AD01",
    "desc": "Registered office address changed from Wincham House to 4 Market Street",
    "txId": "MzE4MzAwMDkyOWFkaXF6a2N4",
    "href": "/company/06993349/filing-history/MzE4MzAwMDkyOWFkaXF6a2N4/document?format=pdf&download=0"
  },
  {
    "date": "19 Apr 2017",
    "type": "AA",
    "desc": "Total exemption full accounts made up to 31 August 2016",
    "txId": "MzE3Mzg4NzMxNGFkaXF6a2N4",
    "href": "/company/06993349/filing-history/MzE3Mzg4NzMxNGFkaXF6a2N4/document?format=pdf&download=0"
  },
  {
    "date": "18 Jan 2017",
    "type": "PSC01",
    "desc": "Notification of Mrs Mary Ann Stockwell as a person with significant control",
    "txId": "MzE2Njc5MTU4MmFkaXF6a2N4",
    "href": "/company/06993349/filing-history/MzE2Njc5MTU4MmFkaXF6a2N4/document?format=pdf&download=0"
  },
  {
    "date": "18 Jan 2017",
    "type": "PSC01",
    "desc": "Notification of Mr Bryan Frederick Stockwell as a person with significant control",
    "txId": "MzE2Njc5MTU3OWFkaXF6a2N4",
    "href": "/company/06993349/filing-history/MzE2Njc5MTU3OWFkaXF6a2N4/document?format=pdf&download=0"
  },
  {
    "date": "30 Aug 2016",
    "type": "CS01",
    "desc": "Confirmation statement made on 18 August 2016 with no updates",
    "txId": "MzE1NTczNzI4OWFkaXF6a2N4",
    "href": "/company/06993349/filing-history/MzE1NTczNzI4OWFkaXF6a2N4/document?format=pdf&download=0"
  },
  {
    "date": "24 May 2016",
    "type": "AA",
    "desc": "Total exemption full accounts made up to 31 August 2015",
    "txId": "MzE0OTYwMjIxM2FkaXF6a2N4",
    "href": "/company/06993349/filing-history/MzE0OTYwMjIxM2FkaXF6a2N4/document?format=pdf&download=0"
  },
  {
    "date": "24 Aug 2015",
    "type": "AR01",
    "desc": "Annual return made up to 18 August 2015 with full list of shareholders",
    "txId": "MzEzMDM5OTY3N2FkaXF6a2N4",
    "href": "/company/06993349/filing-history/MzEzMDM5OTY3N2FkaXF6a2N4/document?format=pdf&download=0"
  },
  {
    "date": "20 May 2015",
    "type": "AA",
    "desc": "Total exemption full accounts made up to 31 August 2014",
    "txId": "MzEyMzUyOTc3MmFkaXF6a2N4",
    "href": "/company/06993349/filing-history/MzEyMzUyOTc3MmFkaXF6a2N4/document?format=pdf&download=0"
  },
  {
    "date": "28 Apr 2014",
    "type": "AA",
    "desc": "Total exemption small company accounts made up to 31 August 2013",
    "txId": "MzA5ODk2NTEyNWFkaXF6a2N4",
    "href": "/company/06993349/filing-history/MzA5ODk2NTEyNWFkaXF6a2N4/document?format=pdf&download=0"
  },
  {
    "date": "19 Aug 2013",
    "type": "AR01",
    "desc": "Annual return made up to 18 August 2013 with full list of shareholders",
    "txId": "MzA4Mjc2ODgwNWFkaXF6a2N4",
    "href": "/company/06993349/filing-history/MzA4Mjc2ODgwNWFkaXF6a2N4/document?format=pdf&download=0"
  },
  {
    "date": "24 Apr 2013",
    "type": "AA",
    "desc": "Total exemption small company accounts made up to 31 August 2012",
    "txId": "MzA3NTQzMjA3N2FkaXF6a2N4",
    "href": "/company/06993349/filing-history/MzA3NTQzMjA3N2FkaXF6a2N4/document?format=pdf&download=0"
  },
  {
    "date": "01 Sep 2012",
    "type": "AR01",
    "desc": "Annual return made up to 18 August 2012 with full list of shareholders",
    "txId": "MzA2Mjc0NzExMWFkaXF6a2N4",
    "href": "/company/06993349/filing-history/MzA2Mjc0NzExMWFkaXF6a2N4/document?format=pdf&download=0"
  },
  {
    "date": "31 Aug 2012",
    "type": "TM02",
    "desc": "Termination of appointment of Companies 4 U Secretaries as a secretary",
    "txId": "MzA2MjcwNTU0OWFkaXF6a2N4",
    "href": "/company/06993349/filing-history/MzA2MjcwNTU0OWFkaXF6a2N4/document?format=pdf&download=0"
  },
  {
    "date": "31 Aug 2012",
    "type": "AP04",
    "desc": "Appointment of Wincham Legal Limited as a secretary",
    "txId": "MzA2MjcwNTQ5OWFkaXF6a2N4",
    "href": "/company/06993349/filing-history/MzA2MjcwNTQ5OWFkaXF6a2N4/document?format=pdf&download=0"
  },
  {
    "date": "28 May 2012",
    "type": "AA",
    "desc": "Total exemption small company accounts made up to 31 August 2011",
    "txId": "MzA1NjQwMjIwNmFkaXF6a2N4",
    "href": "/company/06993349/filing-history/MzA1NjQwMjIwNmFkaXF6a2N4/document?format=pdf&download=0"
  },
  {
    "date": "18 Aug 2011",
    "type": "AR01",
    "desc": "Annual return made up to 18 August 2011 with full list of shareholders",
    "txId": "MzA0MTQyNTAyNmFkaXF6a2N4",
    "href": "/company/06993349/filing-history/MzA0MTQyNTAyNmFkaXF6a2N4/document?format=pdf&download=0"
  },
  {
    "date": "21 Jul 2011",
    "type": "AA",
    "desc": "Total exemption small company accounts made up to 31 August 2010",
    "txId": "MzAzOTg3Mzk0M2FkaXF6a2N4",
    "href": "/company/06993349/filing-history/MzAzOTg3Mzk0M2FkaXF6a2N4/document?format=pdf&download=0"
  },
  {
    "date": "10 Jun 2011",
    "type": "TM01",
    "desc": "Termination of appointment of Frederick Purvs as a director",
    "txId": "MzAzODA5MzAzOGFkaXF6a2N4",
    "href": "/company/06993349/filing-history/MzAzODA5MzAzOGFkaXF6a2N4/document?format=pdf&download=0"
  },
  {
    "date": "10 Jun 2011",
    "type": "TM01",
    "desc": "Termination of appointment of Margaret Purvis as a director",
    "txId": "MzAzODA5Mjk4OWFkaXF6a2N4",
    "href": "/company/06993349/filing-history/MzAzODA5Mjk4OWFkaXF6a2N4/document?format=pdf&download=0"
  },
  {
    "date": "10 Jun 2011",
    "type": "AP01",
    "desc": "Appointment of Mr Bryan Frederick Stockwell as a director",
    "txId": "MzAzODA5MjkyMGFkaXF6a2N4",
    "href": "/company/06993349/filing-history/MzAzODA5MjkyMGFkaXF6a2N4/document?format=pdf&download=0"
  },
  {
    "date": "17 May 2011",
    "type": "AD01",
    "desc": "Registered office address changed from 4 Market Street to Wincham House",
    "txId": "MzAzNjAzMDI0NWFkaXF6a2N4",
    "href": "/company/06993349/filing-history/MzAzNjAzMDI0NWFkaXF6a2N4/document?format=pdf&download=0"
  },
  {
    "date": "23 Aug 2010",
    "type": "CH04",
    "desc": "Secretary's details changed for Companies 4 U Secretaries Ltd",
    "txId": "MzAxOTUxNDkyMWFkaXF6a2N4",
    "href": "/company/06993349/filing-history/MzAxOTUxNDkyMWFkaXF6a2N4/document?format=pdf&download=0"
  },
  {
    "date": "23 Aug 2010",
    "type": "AR01",
    "desc": "Annual return made up to 18 August 2010 with full list of shareholders",
    "txId": "MzAxOTUxNDgxMWFkaXF6a2N4",
    "href": "/company/06993349/filing-history/MzAxOTUxNDgxMWFkaXF6a2N4/document?format=pdf&download=0"
  },
  {
    "date": "28 Jul 2010",
    "type": "SH01",
    "desc": "Statement of capital following an allotment of shares on 23 July 2010",
    "txId": "MzAxNzk0NTk0MWFkaXF6a2N4",
    "href": "/company/06993349/filing-history/MzAxNzk0NTk0MWFkaXF6a2N4/document?format=pdf&download=0"
  },
  {
    "date": "27 Jul 2010",
    "type": "TM01",
    "desc": "Termination of appointment of Malcolm Roach as a director",
    "txId": "MzAxNzg5OTI0NGFkaXF6a2N4",
    "href": "/company/06993349/filing-history/MzAxNzg5OTI0NGFkaXF6a2N4/document?format=pdf&download=0"
  },
  {
    "date": "27 Jul 2010",
    "type": "AP01",
    "desc": "Appointment of Margaret Ellen Purvis as a director",
    "txId": "MzAxNzg5OTIyOWFkaXF6a2N4",
    "href": "/company/06993349/filing-history/MzAxNzg5OTIyOWFkaXF6a2N4/document?format=pdf&download=0"
  },
  {
    "date": "27 Jul 2010",
    "type": "AP01",
    "desc": "Appointment of Frederick Purvs as a director",
    "txId": "MzAxNzg5OTE0MWFkaXF6a2N4",
    "href": "/company/06993349/filing-history/MzAxNzg5OTE0MWFkaXF6a2N4/document?format=pdf&download=0"
  },
  {
    "date": "18 Aug 2009",
    "type": "NEWINC",
    "desc": "Incorporation",
    "txId": "MzAwMDQxNTAzMWFkaXF6a2N4",
    "href": "/company/06993349/filing-history/MzAwMDQxNTAzMWFkaXF6a2N4/document?format=pdf&download=0"
  }
]
```
Total filings found: 70
```
