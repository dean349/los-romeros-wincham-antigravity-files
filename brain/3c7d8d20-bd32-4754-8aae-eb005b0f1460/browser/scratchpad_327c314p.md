# Wincham SSL Investigation Progress

## Primary Sites to Check
- [/] https://www.wincham.com (UP, SECURE)
- [X] https://www.winchamiht.com (DOWN - Connection Reset)
- [/] https://www.winchamukcompany.com (UP, SECURE)
- [/] https://www.winchampropertyshop.com (UP, SECURE)
- [/] https://www.adremaccs.com (UP, SECURE)

## Additional Sites to Check
- [X] https://www.wincham.es (DOWN - DNS Error: wincham_es_dns_error)
- [X] https://www.winchamgroup.com (DOWN - DNS Error: winchamgroup_com_dns_error)
- [/] https://www.belgravewincham.co.uk (UP, SECURE)

## SSL Labs Analysis
- [/] wincham.com (Valid until 2026-07-06, Issuer: Let's Encrypt R13. Grade: B)
- [X] winchamiht.com (Assessment failed: No secure protocols supported)
- [/] winchamukcompany.com (Valid until 2026-06-09, Issuer: Let's Encrypt R12. Grade: B)
- [/] winchampropertyshop.com (Valid until 2026-12-01, Issuer: Sectigo. Grade: B)
- [/] adremaccs.com (Valid until 2027-03-31, Issuer: IONOS. Grade: A+)

## Data Points to Collect
- Full URL
- SSL Status (VALID/EXPIRED/NO HTTPS/DOWN)
- Certificate Issuer
- Expiry Date
- SSL Labs Grade
- Screenshot filename

## Notes
- wincham_com: SSL is CURRENTLY VALID but was reported as expired in the past. Current cert expires 2026-07-06.
- winchamiht_com: Site is down or has no secure protocols. Connection reset in browser.
- winchamukcompany_com: SSL is valid (Grade B).
- winchampropertyshop_com: Valid SSL (Grade B). Supports weak DH and RC4.
- adremaccs_com: Valid SSL (Grade A+).
- wincham_es, winchamgroup_com: DNS NXDOMAIN.
- belgravewincham_co_uk: Site up, visually secure.
- Previous research (wincham_ssl_breach_report.md) confirmed expired SSL for wincham.com in the past (NET::ERR_CERT_DATE_INVALID).
