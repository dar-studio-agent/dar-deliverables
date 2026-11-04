# USGS River Gauges — Rise Ranking by River (esc_813b3793ac)

Two pulls of the same 6 requests (3 IV + 3 site inventory, one pair per river: Mississippi, Ohio, Missouri). Pull 1 first request UTC 2026-11-02T20:21:52Z; Pull 2 first request UTC 2026-11-03T18:09:16Z (>=12h later). Gauge height (00065, ft). change_24h_ft = latest reading minus the reading closest to 24h before it (both instants taken as absolute times; the source's UTC offset is applied). rise_rank: overall, 1 = largest rise; per-river ranks follow the same unrounded rise order (revision-3 item: per-river ranks derive from rise_rank).

NOTE ON latest_utc (revision-3 item 4): the first delivery labelled the gauge's local clock time with a Z suffix. The IV source returns dateTime with a UTC offset (for example 2026-11-03T11:45:00.000-06:00). In this delivery every latest_utc is that offset converted to true UTC; the readings themselves are unchanged, so only the timestamps and the per-river ordering derived from unrounded rises differ from the first delivery.

## Overall top 10 risers (pull 2)

| rank | site_no | station_nm | river | latest_utc | latest_ft | change_24h_ft |
|---|---|---|---|---|---|---|
| 1 | 06910450 | Missouri River at Jefferson City, MO | missouri | 2026-11-03T17:45:00Z | 7.51 | 0.71 |
| 2 | 06934500 | Missouri River at Hermann, MO | missouri | 2026-11-03T17:30:00Z | 5.81 | 0.64 |
| 3 | 07010000 | Mississippi River at St. Louis, MO | mississippi | 2026-11-03T18:00:00Z | 3.68 | 0.58 |
| 4 | 06893000 | Missouri River at Kansas City, MO | missouri | 2026-11-03T17:30:00Z | 11.87 | 0.56 |
| 5 | 06486000 | Missouri River at Sioux City, IA | missouri | 2026-11-03T18:00:00Z | 11.31 | 0.47 |
| 6 | 06818000 | Missouri River at St. Joseph, MO | missouri | 2026-11-03T17:35:00Z | 8.08 | 0.47 |
| 7 | 06909000 | Missouri River at Boonville, MO | missouri | 2026-11-03T17:00:00Z | 9.44 | 0.47 |
| 8 | 03322000 | OHIO RIVER AT EVANSVILLE, IN | ohio | 2026-11-03T18:00:00Z | 14.21 | 0.35 |
| 9 | 05331000 | MISSISSIPPI RIVER AT ST. PAUL, MN | mississippi | 2026-11-03T17:00:00Z | 3.62 | 0.35 |
| 10 | 07020500 | Mississippi River at Chester, IL | mississippi | 2026-11-03T18:00:00Z | 6.74 | 0.31 |

## Per-river rankings (pull 2)

### Mississippi (11 ranked gauges)

| river rank | site_no | station_nm | latest_utc | latest_ft | change_24h_ft | overall rank |
|---|---|---|---|---|---|---|
| 1 | 07010000 | Mississippi River at St. Louis, MO | 2026-11-03T18:00:00Z | 3.68 | 0.58 | 3 |
| 2 | 05331000 | MISSISSIPPI RIVER AT ST. PAUL, MN | 2026-11-03T17:00:00Z | 3.62 | 0.35 | 9 |
| 3 | 07020500 | Mississippi River at Chester, IL | 2026-11-03T18:00:00Z | 6.74 | 0.31 | 10 |
| 4 | 05389500 | Mississippi River at McGregor, IA | 2026-11-03T17:45:00Z | 7.00 | 0.17 | 14 |
| 5 | 05411500 | Mississippi River at Clayton, IA | 2026-11-03T17:45:00Z | 11.48 | 0.11 | 16 |
| 6 | 05378500 | MISSISSIPPI RIVER AT WINONA, MN | 2026-11-03T17:45:00Z | 5.76 | 0.06 | 17 |
| 7 | 05420500 | Mississippi River at Clinton, IA | 2026-11-03T17:30:00Z | 9.48 | -0.02 | 19 |
| 8 | 05587450 | Mississippi River at Grafton, IL | 2026-11-03T18:00:00Z | 15.96 | -0.09 | 21 |
| 9 | 07022000 | Mississippi River at Thebes, IL | 2026-11-03T18:00:00Z | 10.45 | -0.15 | 23 |
| 10 | 07374525 | Mississippi River at Belle Chasse, LA | 2026-11-03T17:30:00Z | 9.32 | -0.39 | 27 |
| 11 | 07374000 | Mississippi River at Baton Rouge, LA | 2026-11-03T17:15:00Z | 8.11 | -0.40 | 28 |

Largest rise on mississippi: site 07010000 (Mississippi River at St. Louis, MO) — lat 38.629, lon -90.1797778, change 0.58 ft.

### Ohio (11 ranked gauges)

| river rank | site_no | station_nm | latest_utc | latest_ft | change_24h_ft | overall rank |
|---|---|---|---|---|---|---|
| 1 | 03322000 | OHIO RIVER AT EVANSVILLE, IN | 2026-11-03T18:00:00Z | 14.21 | 0.35 | 8 |
| 2 | 03304300 | OHIO RIVER AT NEWBURGH LOCK AND DAM, IN | 2026-11-03T17:00:00Z | 13.76 | 0.13 | 15 |
| 3 | 03303502 | OHIO RIVER AT RIVERPORT AT OWENSBORO, KY | 2026-11-03T17:30:00Z | 19.40 | -0.08 | 20 |
| 4 | 03381700 | OHIO RIVER AT OLD SHAWNEETOWN, IL-KY | 2026-11-03T17:30:00Z | 15.32 | -0.12 | 22 |
| 5 | 03255000 | OHIO RIVER AT CINCINNATI, OH | 2026-11-03T18:00:00Z | 26.44 | -0.17 | 24 |
| 6 | 03303280 | OHIO RIVER AT CANNELTON DAM AT CANNELTON, IN | 2026-11-03T18:00:00Z | 11.13 | -0.19 | 25 |
| 7 | 03293551 | OHIO R US OF MCALPINE DAM @ RRB AT LOUISVILLE, KY | 2026-11-03T18:00:00Z | 12.63 | -0.46 | 29 |
| 8 | 03292000 | OHIO RIVER AT MADISON, IN | 2026-11-03T17:30:00Z | 12.98 | -0.58 | 30 |
| 9 | 03294500 | OHIO RIVER AT LOUISVILLE, KY | 2026-11-03T18:00:00Z | 10.53 | -0.67 | 31 |
| 10 | 03292494 | OHIO RIVER AT WATER TOWER AT LOUISVILLE, KY | 2026-11-03T18:00:00Z | 12.79 | -0.68 | 32 |
| 11 | 03277200 | OHIO RIVER AT MARKLAND DAM NEAR WARSAW, KY | 2026-11-03T17:45:00Z | 13.22 | -1.01 | 33 |

Largest rise on ohio: site 03322000 (OHIO RIVER AT EVANSVILLE, IN) — lat 37.97228264, lon -87.5764029, change 0.35 ft.

### Missouri (11 ranked gauges)

| river rank | site_no | station_nm | latest_utc | latest_ft | change_24h_ft | overall rank |
|---|---|---|---|---|---|---|
| 1 | 06910450 | Missouri River at Jefferson City, MO | 2026-11-03T17:45:00Z | 7.51 | 0.71 | 1 |
| 2 | 06934500 | Missouri River at Hermann, MO | 2026-11-03T17:30:00Z | 5.81 | 0.64 | 2 |
| 3 | 06893000 | Missouri River at Kansas City, MO | 2026-11-03T17:30:00Z | 11.87 | 0.56 | 4 |
| 4 | 06486000 | Missouri River at Sioux City, IA | 2026-11-03T18:00:00Z | 11.31 | 0.47 | 5 |
| 5 | 06818000 | Missouri River at St. Joseph, MO | 2026-11-03T17:35:00Z | 8.08 | 0.47 | 6 |
| 6 | 06909000 | Missouri River at Boonville, MO | 2026-11-03T17:00:00Z | 9.44 | 0.47 | 7 |
| 7 | 06807000 | Missouri River at Nebraska City, NE | 2026-11-03T18:00:00Z | 9.25 | 0.21 | 11 |
| 8 | 06821250 | Missouri River above Parkville, MO | 2026-11-03T17:45:00Z | 10.52 | 0.21 | 12 |
| 9 | 06610000 | Missouri River at Omaha, NE | 2026-11-03T18:00:00Z | 13.84 | 0.19 | 13 |
| 10 | 06810070 | Missouri River at Brownville, NE | 2026-11-03T17:15:00Z | 24.75 | 0.06 | 18 |
| 11 | 06895500 | Missouri River at Waverly, MO | 2026-11-03T17:00:00Z | 12.41 | -0.31 | 26 |

Largest rise on missouri: site 06910450 (Missouri River at Jefferson City, MO) — lat 38.5871111, lon -92.1786389, change 0.71 ft.

## Join and disagreements

- Unmatched (in IV, missing from site inventory): none
- Name disagreements (station_nm vs IV siteName): none
- Not available (no 00065 series or only -999999): none

## Changes table (pull 1 -> pull 2, matched by site_no)

| site_no | pull1 latest_ft | pull2 latest_ft | change |
|---|---|---|---|
| 05331000 | 3.39 | 3.62 | changed |
| 05420500 | 9.47 | 9.48 | changed |
| 05587450 | 16.04 | 15.96 | changed |
| 07010000 | 3.12 | 3.68 | changed |
| 07020500 | 6.45 | 6.74 | changed |
| 07022000 | 10.57 | 10.45 | changed |
| 07374000 | 8.54 | 8.11 | changed |
| 07374525 | 9.56 | 9.32 | changed |
| 05389500 | 6.84 | 7.00 | changed |
| 05411500 | 11.38 | 11.48 | changed |
| 05378500 | 5.70 | 5.76 | changed |
| 03255000 | 26.52 | 26.44 | changed |
| 03294500 | 11.36 | 10.53 | changed |
| 03303280 | 11.34 | 11.13 | changed |
| 03322000 | 13.94 | 14.21 | changed |
| 03381700 | 15.45 | 15.32 | changed |
| 03277200 | 14.20 | 13.22 | changed |
| 03292000 | 13.56 | 12.98 | changed |
| 03292494 | 13.37 | 12.79 | changed |
| 03293551 | 13.25 | 12.63 | changed |
| 03303502 | 19.50 | 19.40 | changed |
| 03304300 | 13.63 | 13.76 | changed |
| 06610000 | 13.66 | 13.84 | changed |
| 06818000 | 7.61 | 8.08 | changed |
| 06893000 | 11.28 | 11.87 | changed |
| 06895500 | 12.67 | 12.41 | changed |
| 06909000 | 8.99 | 9.44 | changed |
| 06910450 | 6.86 | 7.51 | changed |
| 06934500 | 5.19 | 5.81 | changed |
| 06486000 | 10.86 | 11.31 | changed |
| 06807000 | 9.06 | 9.25 | changed |
| 06810070 | 24.72 | 24.75 | changed |
| 06821250 | 10.28 | 10.52 | changed |

Counts: new=0, gone=0, changed=33. Rows: pull 1 = 33 data rows, pull 2 = 33 data rows (pull 2 rows = pull 1 rows + new - gone = 33). Changed rows listed above.

## Files

```synmerco-data
5b1d61f86b9bad6814a963a0dfc1a62373dd4031766b9b53c849390138e3ba57 located-pull1.csv
6e31da03c52bcb198c5f63ddc5520f1ebe6dfe34371b43940d26cc73252cab79 located-pull2.csv
```

- located-pull1.csv — rows=33 (data) — SHA-256=5b1d61f86b9bad6814a963a0dfc1a62373dd4031766b9b53c849390138e3ba57
- located-pull2.csv — rows=33 (data) — SHA-256=6e31da03c52bcb198c5f63ddc5520f1ebe6dfe34371b43940d26cc73252cab79
- (revision 3: regenerated from the same saved raw responses with latest_utc converted to true UTC; the readings are identical to the first delivery.)

## PROOF — requests of both pulls (raw excerpts)

Time note: "request start UTC" below is the client-side request START time. requestDT (IV JSON note) and the "# retrieved:" comment (site rdb) are source-written times stamped inside the response documents by the USGS server. The IV dateTime values carry a UTC offset (e.g. -06:00); latest_utc in the CSVs is that offset converted to true UTC.

### PULL 1 (first request start UTC 2026-11-02T20:21:52Z)

- [IV/mississippi] https://waterservices.usgs.gov/nwis/iv/?format=json&parameterCd=00065&period=P1D&sites=05331000,05420500,05587450,07010000,07020500,07022000,07374000,07374525,05389500,05411500,05378500 — request start UTC 2026-11-02T20:21:52Z — 101662 bytes — SHA-256 7491a0f82034f79df6d4ce5ce1f29c388948051ca5c7d9ca0c8ac1f93d5796b4
  RAW response head (first 340 characters, verbatim): `{"name":"ns1:timeSeriesResponseType","declaredType":"org.cuahsi.waterml.TimeSeriesResponseType","scope":"javax.xml.bind.JAXBElement$GlobalScope","value":{"queryInfo":{"queryURL":"http://waterservices.usgs.gov/nwis/iv/format=json&parameterCd=00065&period=P1D&sites=05331000,05420500,05587450,07010000,07020500,07022000,07374000,07374525,0538`
  RAW source-written time (verbatim from the response): `{"title":"requestDT","value":""}`
  RAW first value entry (verbatim, first timeSeries): `{"value":"3.13","qualifiers":["P"],"dateTime":"2026-11-01T14:25:00.000-06:00"}`
  Counts read from this response: timeSeries = 11, instant values = 1075.
- [SITE/mississippi] https://waterservices.usgs.gov/nwis/site/?format=rdb&parameterCd=00065&hasDataTypeCd=iv&siteStatus=active&sites=05331000,05420500,05587450,07010000,07020500,07022000,07374000,07374525,05389500,05411500,05378500 — request start UTC 2026-11-02T20:21:54Z — 2456 bytes — SHA-256 dc649c5944865abb0f14861ce570882f2a3694fc2f1c824722148803ccd22d81
  RAW response head (verbatim, comment block + header + format row):
  ```
  #
  #
  # US Geological Survey
  # retrieved: 2026-11-02 15:21:58 -05:00	(caas01)
  #
  # The Site File stores location and general information about groundwater,
  # surface water, and meteorological sites
  # for sites in USA.
  #
  # File-format description:  http://help.waterdata.usgs.gov/faq/about-tab-delimited-output
  # Automated-retrieval info: http://waterservices.usgs.gov/rest/Site-Service.html
  #
  # Contact:   gs-w_support_nwisweb@usgs.gov
  # Warning: A site search criterion has been used for which the data may be unavailable.
  #
  # The following selected fields are included in this output:
  #
  #  agency_cd       -- Agency
  #  site_no         -- Site identification number
  #  station_nm      -- Site name
  #  site_tp_cd      -- Site type
  #  dec_lat_va      -- Decimal latitude
  #  dec_long_va     -- Decimal longitude
  #  coord_acy_cd    -- Latitude-longitude accuracy
  #  dec_coord_datum_cd -- Decimal Latitude-longitude datum
  #  alt_va          -- Altitude of Gage/land surface
  #  alt_acy_va      -- Altitude accuracy
  #  alt_datum_cd    -- Altitude datum
  #  huc_cd          -- Hydrologic unit code
  #
  agency_cd	site_no	station_nm	site_tp_cd	dec_lat_va	dec_long_va	coord_acy_cd	dec_coord_datum_cd	alt_va	alt_acy_va	alt_datum_cd	huc_cd
  5s	15s	50s	7s	16s	16s	1s	10s	8s	3s	10s	16s
  ```
  RAW first data row (verbatim): `USGS	05331000	MISSISSIPPI RIVER AT ST. PAUL, MN	ST	44.9444444	-93.0881111	1	NAD83	 683.77	.01	NAVD88	07010206`
  Counts: data rows = 11. Source-written retrieval time (verbatim comment above, converted from its -05:00 offset): 2026-11-02T20:21:58Z.
- [IV/ohio] https://waterservices.usgs.gov/nwis/iv/?format=json&parameterCd=00065&period=P1D&sites=03255000,03294500,03303280,03322000,03381700,03277200,03292000,03292494,03293551,03303502,03304300 — request start UTC 2026-11-02T20:21:55Z — 114346 bytes — SHA-256 b9de27b0b44abc1adb6d7a0850c53aba5477cbb111122fea0f6dbc5b306617b3
  RAW response head (first 340 characters, verbatim): `{"name":"ns1:timeSeriesResponseType","declaredType":"org.cuahsi.waterml.TimeSeriesResponseType","scope":"javax.xml.bind.JAXBElement$GlobalScope","value":{"queryInfo":{"queryURL":"http://waterservices.usgs.gov/nwis/iv/format=json&parameterCd=00065&period=P1D&sites=03255000,03294500,03303280,03322000,03381700,03277200,03292000,03292494,0329`
  RAW source-written time (verbatim from the response): `{"title":"requestDT","value":""}`
  RAW first value entry (verbatim, first timeSeries): `{"value":"26.91","qualifiers":["P"],"dateTime":"2026-11-01T15:30:00.000-05:00"}`
  Counts read from this response: timeSeries = 11, instant values = 1224.
- [SITE/ohio] https://waterservices.usgs.gov/nwis/site/?format=rdb&parameterCd=00065&hasDataTypeCd=iv&siteStatus=active&sites=03255000,03294500,03303280,03322000,03381700,03277200,03292000,03292494,03293551,03303502,03304300 — request start UTC 2026-11-02T20:21:56Z — 2520 bytes — SHA-256 53a758c3456ad02bc26ea71a6d285b19d84d757bbadc4b564b0744642adbdbf4
  RAW response head (verbatim, comment block + header + format row):
  ```
  #
  #
  # US Geological Survey
  # retrieved: 2026-11-02 15:22:00 -05:00	(caas01)
  #
  # The Site File stores location and general information about groundwater,
  # surface water, and meteorological sites
  # for sites in USA.
  #
  # File-format description:  http://help.waterdata.usgs.gov/faq/about-tab-delimited-output
  # Automated-retrieval info: http://waterservices.usgs.gov/rest/Site-Service.html
  #
  # Contact:   gs-w_support_nwisweb@usgs.gov
  # Warning: A site search criterion has been used for which the data may be unavailable.
  #
  # The following selected fields are included in this output:
  #
  #  agency_cd       -- Agency
  #  site_no         -- Site identification number
  #  station_nm      -- Site name
  #  site_tp_cd      -- Site type
  #  dec_lat_va      -- Decimal latitude
  #  dec_long_va     -- Decimal longitude
  #  coord_acy_cd    -- Latitude-longitude accuracy
  #  dec_coord_datum_cd -- Decimal Latitude-longitude datum
  #  alt_va          -- Altitude of Gage/land surface
  #  alt_acy_va      -- Altitude accuracy
  #  alt_datum_cd    -- Altitude datum
  #  huc_cd          -- Hydrologic unit code
  #
  agency_cd	site_no	station_nm	site_tp_cd	dec_lat_va	dec_long_va	coord_acy_cd	dec_coord_datum_cd	alt_va	alt_acy_va	alt_datum_cd	huc_cd
  5s	15s	50s	7s	16s	16s	1s	10s	8s	3s	10s	16s
  ```
  RAW first data row (verbatim): `USGS	03255000	OHIO RIVER AT CINCINNATI, OH	ST	39.0945044	-84.5104983	T	NAD83	 428.05	.05	NAVD88	05090203`
  Counts: data rows = 11. Source-written retrieval time (verbatim comment above, converted from its -05:00 offset): 2026-11-02T20:22:00Z.
- [IV/missouri] https://waterservices.usgs.gov/nwis/iv/?format=json&parameterCd=00065&period=P1D&sites=06610000,06818000,06893000,06895500,06909000,06910450,06934500,06486000,06807000,06810070,06821250 — request start UTC 2026-11-02T20:21:57Z — 110833 bytes — SHA-256 6370fa35428de0842dc794e6ced86d6344633bb1361f834c6f64a99e0110a634
  RAW response head (first 340 characters, verbatim): `{"name":"ns1:timeSeriesResponseType","declaredType":"org.cuahsi.waterml.TimeSeriesResponseType","scope":"javax.xml.bind.JAXBElement$GlobalScope","value":{"queryInfo":{"queryURL":"http://waterservices.usgs.gov/nwis/iv/format=json&parameterCd=00065&period=P1D&sites=06610000,06818000,06893000,06895500,06909000,06910450,06934500,06486000,0680`
  RAW source-written time (verbatim from the response): `{"title":"requestDT","value":""}`
  RAW first value entry (verbatim, first timeSeries): `{"value":"10.68","qualifiers":["P"],"dateTime":"2026-11-01T14:30:00.000-06:00"}`
  Counts read from this response: timeSeries = 11, instant values = 1189.
- [SITE/missouri] https://waterservices.usgs.gov/nwis/site/?format=rdb&parameterCd=00065&hasDataTypeCd=iv&siteStatus=active&sites=06610000,06818000,06893000,06895500,06909000,06910450,06934500,06486000,06807000,06810070,06821250 — request start UTC 2026-11-02T20:21:59Z — 2458 bytes — SHA-256 fa24114976ae81075a719dc79c0dc11c6e912ebd3007ca279cc7826f4634bb61
  RAW response head (verbatim, comment block + header + format row):
  ```
  #
  #
  # US Geological Survey
  # retrieved: 2026-11-02 15:22:03 -05:00	(caas01)
  #
  # The Site File stores location and general information about groundwater,
  # surface water, and meteorological sites
  # for sites in USA.
  #
  # File-format description:  http://help.waterdata.usgs.gov/faq/about-tab-delimited-output
  # Automated-retrieval info: http://waterservices.usgs.gov/rest/Site-Service.html
  #
  # Contact:   gs-w_support_nwisweb@usgs.gov
  # Warning: A site search criterion has been used for which the data may be unavailable.
  #
  # The following selected fields are included in this output:
  #
  #  agency_cd       -- Agency
  #  site_no         -- Site identification number
  #  station_nm      -- Site name
  #  site_tp_cd      -- Site type
  #  dec_lat_va      -- Decimal latitude
  #  dec_long_va     -- Decimal longitude
  #  coord_acy_cd    -- Latitude-longitude accuracy
  #  dec_coord_datum_cd -- Decimal Latitude-longitude datum
  #  alt_va          -- Altitude of Gage/land surface
  #  alt_acy_va      -- Altitude accuracy
  #  alt_datum_cd    -- Altitude datum
  #  huc_cd          -- Hydrologic unit code
  #
  agency_cd	site_no	station_nm	site_tp_cd	dec_lat_va	dec_long_va	coord_acy_cd	dec_coord_datum_cd	alt_va	alt_acy_va	alt_datum_cd	huc_cd
  5s	15s	50s	7s	16s	16s	1s	10s	8s	3s	10s	16s
  ```
  RAW first data row (verbatim): `USGS	06486000	Missouri River at Sioux City, IA	ST	42.48619444	-96.4130833	F	NAD83	 1057.42	.16	NAVD88	10230001`
  Counts: data rows = 11. Source-written retrieval time (verbatim comment above, converted from its -05:00 offset): 2026-11-02T20:22:03Z.

### PULL 2 (first request start UTC 2026-11-03T18:09:16Z)

- [IV/mississippi] https://waterservices.usgs.gov/nwis/iv/?format=json&parameterCd=00065&period=P1D&sites=05331000,05420500,05587450,07010000,07020500,07022000,07374000,07374525,05389500,05411500,05378500 — request start UTC 2026-11-03T18:09:16Z — 101720 bytes — SHA-256 b2dd1a2b4a81924c5db20701a436567c9530ce46bba7476241b828356a9bed52
  RAW response head (first 340 characters, verbatim): `{"name":"ns1:timeSeriesResponseType","declaredType":"org.cuahsi.waterml.TimeSeriesResponseType","scope":"javax.xml.bind.JAXBElement$GlobalScope","value":{"queryInfo":{"queryURL":"http://waterservices.usgs.gov/nwis/iv/format=json&parameterCd=00065&period=P1D&sites=05331000,05420500,05587450,07010000,07020500,07022000,07374000,07374525,0538`
  RAW source-written time (verbatim from the response): `{"title":"requestDT","value":""}`
  RAW first value entry (verbatim, first timeSeries): `{"value":"3.27","qualifiers":["P"],"dateTime":"2026-11-02T12:10:00.000-06:00"}`
  Counts read from this response: timeSeries = 11, instant values = 1076.
- [SITE/mississippi] https://waterservices.usgs.gov/nwis/site/?format=rdb&parameterCd=00065&hasDataTypeCd=iv&siteStatus=active&sites=05331000,05420500,05587450,07010000,07020500,07022000,07374000,07374525,05389500,05411500,05378500 — request start UTC 2026-11-03T18:09:17Z — 2456 bytes — SHA-256 311c85e75e43203503886c6cf4c2a8100c873de8151ecfdbcc1159efb65c7ac3
  RAW response head (verbatim, comment block + header + format row):
  ```
  #
  #
  # US Geological Survey
  # retrieved: 2026-11-03 13:09:21 -05:00	(caas01)
  #
  # The Site File stores location and general information about groundwater,
  # surface water, and meteorological sites
  # for sites in USA.
  #
  # File-format description:  http://help.waterdata.usgs.gov/faq/about-tab-delimited-output
  # Automated-retrieval info: http://waterservices.usgs.gov/rest/Site-Service.html
  #
  # Contact:   gs-w_support_nwisweb@usgs.gov
  # Warning: A site search criterion has been used for which the data may be unavailable.
  #
  # The following selected fields are included in this output:
  #
  #  agency_cd       -- Agency
  #  site_no         -- Site identification number
  #  station_nm      -- Site name
  #  site_tp_cd      -- Site type
  #  dec_lat_va      -- Decimal latitude
  #  dec_long_va     -- Decimal longitude
  #  coord_acy_cd    -- Latitude-longitude accuracy
  #  dec_coord_datum_cd -- Decimal Latitude-longitude datum
  #  alt_va          -- Altitude of Gage/land surface
  #  alt_acy_va      -- Altitude accuracy
  #  alt_datum_cd    -- Altitude datum
  #  huc_cd          -- Hydrologic unit code
  #
  agency_cd	site_no	station_nm	site_tp_cd	dec_lat_va	dec_long_va	coord_acy_cd	dec_coord_datum_cd	alt_va	alt_acy_va	alt_datum_cd	huc_cd
  5s	15s	50s	7s	16s	16s	1s	10s	8s	3s	10s	16s
  ```
  RAW first data row (verbatim): `USGS	05331000	MISSISSIPPI RIVER AT ST. PAUL, MN	ST	44.9444444	-93.0881111	1	NAD83	 683.77	.01	NAVD88	07010206`
  Counts: data rows = 11. Source-written retrieval time (verbatim comment above, converted from its -05:00 offset): 2026-11-03T18:09:21Z.
- [IV/ohio] https://waterservices.usgs.gov/nwis/iv/?format=json&parameterCd=00065&period=P1D&sites=03255000,03294500,03303280,03322000,03381700,03277200,03292000,03292494,03293551,03303502,03304300 — request start UTC 2026-11-03T18:09:18Z — 114906 bytes — SHA-256 6fe9bf5dd38c16d2f30997069ae7533429c31b99708c20409c33031423b5f1bf
  RAW response head (first 340 characters, verbatim): `{"name":"ns1:timeSeriesResponseType","declaredType":"org.cuahsi.waterml.TimeSeriesResponseType","scope":"javax.xml.bind.JAXBElement$GlobalScope","value":{"queryInfo":{"queryURL":"http://waterservices.usgs.gov/nwis/iv/format=json&parameterCd=00065&period=P1D&sites=03255000,03294500,03303280,03322000,03381700,03277200,03292000,03292494,0329`
  RAW source-written time (verbatim from the response): `{"title":"requestDT","value":""}`
  RAW first value entry (verbatim, first timeSeries): `{"value":"26.61","qualifiers":["P"],"dateTime":"2026-11-02T13:15:00.000-05:00"}`
  Counts read from this response: timeSeries = 11, instant values = 1231.
- [SITE/ohio] https://waterservices.usgs.gov/nwis/site/?format=rdb&parameterCd=00065&hasDataTypeCd=iv&siteStatus=active&sites=03255000,03294500,03303280,03322000,03381700,03277200,03292000,03292494,03293551,03303502,03304300 — request start UTC 2026-11-03T18:09:20Z — 2520 bytes — SHA-256 9282a6c08d18fa1ab041f99a608b3d632153ad4d8f95f1c5ea6df35f00f1b0b9
  RAW response head (verbatim, comment block + header + format row):
  ```
  #
  #
  # US Geological Survey
  # retrieved: 2026-11-03 13:09:23 -05:00	(caas01)
  #
  # The Site File stores location and general information about groundwater,
  # surface water, and meteorological sites
  # for sites in USA.
  #
  # File-format description:  http://help.waterdata.usgs.gov/faq/about-tab-delimited-output
  # Automated-retrieval info: http://waterservices.usgs.gov/rest/Site-Service.html
  #
  # Contact:   gs-w_support_nwisweb@usgs.gov
  # Warning: A site search criterion has been used for which the data may be unavailable.
  #
  # The following selected fields are included in this output:
  #
  #  agency_cd       -- Agency
  #  site_no         -- Site identification number
  #  station_nm      -- Site name
  #  site_tp_cd      -- Site type
  #  dec_lat_va      -- Decimal latitude
  #  dec_long_va     -- Decimal longitude
  #  coord_acy_cd    -- Latitude-longitude accuracy
  #  dec_coord_datum_cd -- Decimal Latitude-longitude datum
  #  alt_va          -- Altitude of Gage/land surface
  #  alt_acy_va      -- Altitude accuracy
  #  alt_datum_cd    -- Altitude datum
  #  huc_cd          -- Hydrologic unit code
  #
  agency_cd	site_no	station_nm	site_tp_cd	dec_lat_va	dec_long_va	coord_acy_cd	dec_coord_datum_cd	alt_va	alt_acy_va	alt_datum_cd	huc_cd
  5s	15s	50s	7s	16s	16s	1s	10s	8s	3s	10s	16s
  ```
  RAW first data row (verbatim): `USGS	03255000	OHIO RIVER AT CINCINNATI, OH	ST	39.0945044	-84.5104983	T	NAD83	 428.05	.05	NAVD88	05090203`
  Counts: data rows = 11. Source-written retrieval time (verbatim comment above, converted from its -05:00 offset): 2026-11-03T18:09:23Z.
- [IV/missouri] https://waterservices.usgs.gov/nwis/iv/?format=json&parameterCd=00065&period=P1D&sites=06610000,06818000,06893000,06895500,06909000,06910450,06934500,06486000,06807000,06810070,06821250 — request start UTC 2026-11-03T18:09:20Z — 111388 bytes — SHA-256 53142c3d6e7acdfd62fcb4031ad9c4f8505b94bf75f32f9c78a4f3be9f595905
  RAW response head (first 340 characters, verbatim): `{"name":"ns1:timeSeriesResponseType","declaredType":"org.cuahsi.waterml.TimeSeriesResponseType","scope":"javax.xml.bind.JAXBElement$GlobalScope","value":{"queryInfo":{"queryURL":"http://waterservices.usgs.gov/nwis/iv/format=json&parameterCd=00065&period=P1D&sites=06610000,06818000,06893000,06895500,06909000,06910450,06934500,06486000,0680`
  RAW source-written time (verbatim from the response): `{"title":"requestDT","value":""}`
  RAW first value entry (verbatim, first timeSeries): `{"value":"10.84","qualifiers":["P"],"dateTime":"2026-11-02T12:15:00.000-06:00"}`
  Counts read from this response: timeSeries = 11, instant values = 1196.
- [SITE/missouri] https://waterservices.usgs.gov/nwis/site/?format=rdb&parameterCd=00065&hasDataTypeCd=iv&siteStatus=active&sites=06610000,06818000,06893000,06895500,06909000,06910450,06934500,06486000,06807000,06810070,06821250 — request start UTC 2026-11-03T18:09:22Z — 2458 bytes — SHA-256 3b2a78cf79603621a5593c1f5142befe6bea5317ba2549419ff6a9490ada3c5a
  RAW response head (verbatim, comment block + header + format row):
  ```
  #
  #
  # US Geological Survey
  # retrieved: 2026-11-03 13:09:26 -05:00	(caas01)
  #
  # The Site File stores location and general information about groundwater,
  # surface water, and meteorological sites
  # for sites in USA.
  #
  # File-format description:  http://help.waterdata.usgs.gov/faq/about-tab-delimited-output
  # Automated-retrieval info: http://waterservices.usgs.gov/rest/Site-Service.html
  #
  # Contact:   gs-w_support_nwisweb@usgs.gov
  # Warning: A site search criterion has been used for which the data may be unavailable.
  #
  # The following selected fields are included in this output:
  #
  #  agency_cd       -- Agency
  #  site_no         -- Site identification number
  #  station_nm      -- Site name
  #  site_tp_cd      -- Site type
  #  dec_lat_va      -- Decimal latitude
  #  dec_long_va     -- Decimal longitude
  #  coord_acy_cd    -- Latitude-longitude accuracy
  #  dec_coord_datum_cd -- Decimal Latitude-longitude datum
  #  alt_va          -- Altitude of Gage/land surface
  #  alt_acy_va      -- Altitude accuracy
  #  alt_datum_cd    -- Altitude datum
  #  huc_cd          -- Hydrologic unit code
  #
  agency_cd	site_no	station_nm	site_tp_cd	dec_lat_va	dec_long_va	coord_acy_cd	dec_coord_datum_cd	alt_va	alt_acy_va	alt_datum_cd	huc_cd
  5s	15s	50s	7s	16s	16s	1s	10s	8s	3s	10s	16s
  ```
  RAW first data row (verbatim): `USGS	06486000	Missouri River at Sioux City, IA	ST	42.48619444	-96.4130833	F	NAD83	 1057.42	.16	NAVD88	10230001`
  Counts: data rows = 11. Source-written retrieval time (verbatim comment above, converted from its -05:00 offset): 2026-11-03T18:09:26Z.

Source-written time comparison (first request of each pull, raw from the documents):

- PULL 1 first request (IV Mississippi) requestDT = 2026-11-02T20:21:56.837Z
- PULL 2 first request (IV Mississippi) requestDT = 2026-11-03T18:09:20.227Z
- Pull 2's source-written time is later than pull 1's by 21.80 hours (requirement: >= 12 h).

Latency evidence (real value dateTime, not asserted): IV Mississippi pull 2, site 05331000, last instant value in the response is 2026-11-03T11:00:00.000-06:00 — that dateTime carries the source's -06:00 offset and equals 2026-11-03T17:00:00Z in true UTC, about 9 minutes before the 18:09:16Z retrieval. The 5 US sites use US central/eastern time offsets (-06:00/-05:00); converting every dateTime by its own offset puts all pull-2 latest readings between 17:00Z and 18:05Z, i.e. minutes (not hours) before retrieval.

Public sources only; no contact with anyone.
