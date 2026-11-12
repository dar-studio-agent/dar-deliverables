# Undeclared-allergen food recalls, 2024-10-01 to 2025-09-30

Escrow `esc_25b1a72cbe674fc0808f773a`. Source: openFDA food enforcement, host `api.fda.gov`, endpoint `/food/enforcement.json`, no key. All classifications, `report_date:[20241001 TO 20250930]`. Three timed pulls; submit only after PULL 3.

## REVISIONS 1 and 2 (2026-11-12) — corrections per the evaluator's reviews

Per the evaluator's revision 1 of 3 (2026-11-12 09:17:51Z, item A2), two records were wrongly kept; their reason_for_recall does not describe an undeclared allergen:

- `H-0068-2025` — "Frozen Raw Peeled & Deveined tail on, shrimp contains undeclared sulfites" — sulfites are excluded by the TASK.
- `H-0069-2025` — "The recall was the result of the firm's routine sampling program and Listeria monocytogenes was detected in an in-process shrimp sample in a food production environment." — names no undeclared allergen.

In all three CSVs both records are now `kept=no` with an empty `allergens` cell (Rule 25: a corrected file is declared again under the same name and replaces the earlier one). Both lines are removed from each PULL's kept-reason list in the PROOF.

Per the evaluator's revision 2 of 3 (2026-11-12 11:30:00Z), one kept record was missing a tag its reason names:

- `H-0602-2025` — "Review of Label determined allergen was listed as unsalted butter/ heavy cream. In one instance of identified label, there was no milk or dairy listed listed in Contains statement. Further review of label revealed \"soy\" had been removed." — names milk and soy, so its allergens cell is now `milk;soybeans` (kept stays yes; the TASK counts a record naming several allergens once under each).

All tables below are recounted from the corrected CSVs. Corrected figures (identical in all three pulls): kept 406 → 404; Class I 167 → 165; month 2025-07 60 → 58; shellfish 5 → 3; soybeans 83 → 84 (H-0602-2025 now counted under both its allergens); the firm table no longer lists TRI-UNION FROZEN PRODUCTS INC DBA CHICKEN OF THE SEA FROZEN FOOD (1) or Bornstein Seafoods Inc (1). No other count changed; the repeat-firm list remains empty; the Changes sections remain no change (every correction applies identically in each pull). A `PULL k (corrected file):` progress note is filed for each pull, giving the final row count and SHA-256 as attached and noting that the earlier PULL k note's SHA-256 d7bc886f... was the pre-correction file.

## ACCEPTANCE — answers line by line

The job's five numbered ACCEPTANCE lines, each answered with where this file shows it:

1. **The three CSV files are attached with exactly the listed columns, one row per record the search returned.** `food-allergen-pull1.csv`, `food-allergen-pull2.csv` and `food-allergen-pull3.csv` are attached under Rule 25 and platform-verified, each 1,564 rows with SHA-256 `4fd72143cff263d8…` exactly as under DATA FILES (the per-PULL lines below and the platform data-files record). Columns exactly `recall_number, report_date, classification, status, recalling_firm, kept, allergens` in that order, key `recall_number`, sorted by it, one row for every record the search returned (kept or not), kept is yes or no, allergens empty when kept=no, comma fields quoted.

2. **Every kept record has a reason in the PROOF that describes an undeclared allergen, and its allergens cell holds the TASK's tags.** Each PULL's PROOF lists the reason_for_recall of every one of its 404 kept records, one per line with its recall_number. The two records the evaluator's round 1 found wrongly kept — H-0068-2025 (undeclared sulfites, TASK-excluded) and H-0069-2025 (Listeria monocytogenes, no allergen named) — are now kept=no with empty allergens in all three CSVs and absent from every kept-reason list. H-0602-2025, whose reason names milk and soy, is now tagged milk;soybeans (round 2). Examples the round-1 review itself verified as correct and unchanged: H-0312-2025 "soy and wheat" tagged wheat;soybeans, and H-0458-2025 (CREAM without Milk) tagged milk.

3. **The counts, the month table and the repeat-firm list agree with the CSV they use and the tie-break.** Every table below is recounted from the corrected CSVs: kept 404 per pull; the allergen table sums to 540 (a record naming several allergens counts once under each); the classification table sums to 404; the month table sums to 404; the firm table counts kept rows per exact recalling_firm string and no longer lists the two firms the corrections removed; the repeat-firm list remains empty (no firm has kept recalls in three or more different report_date months). Every list is count descending with ties by name ascending; months are in calendar order.

4. **Each pull's meta object and Date header line are in the PROOF.** Each PULL's PROOF quotes every request (two per pull: skip=0 and skip=1000) with its full URL, retrieval UTC time, HTTP status, the source's own Date header line and the meta object verbatim.

5. **The PLATFORM RECORD shows the PULL notes with row count and SHA-256 as under DATA FILES; each pull's source time is later than the previous pull's; the change counts agree with the CSV files.** The platform record below holds the original PULL 1/2/3 notes (1,564 rows, pre-correction SHA-256 d7bc886f…) and the three `PULL k (corrected file):` notes filed per the evaluator's round-2 instruction, each stating 1,564 rows and SHA-256 `4fd72143cff263d8…` — exactly the hash under DATA FILES. Source times increase across pulls (first request Date headers: 10 Nov 2026 02:09:43 GMT → 11 Nov 07:49:07 GMT → 12 Nov 09:10:58 GMT). The Changes sections show no change and agree with the attached files: later rows = earlier rows + 0 new − 0 gone, and the three corrected CSVs are byte-identical to each other.

## PULL 1

- total records returned: 1564
- kept (undeclared allergen): 404
- CSV: `food-allergen-pull1.csv` · rows 1564 · SHA-256 `4fd72143cff263d845d08a4365bddeb3c46a7db9c8efa9d2c1f8bed80f673316`

### Counts by allergen (kept records only)

| allergen | count |
| --- | ---: |
| milk | 138 |
| wheat | 124 |
| soybeans | 84 |
| egg | 65 |
| tree nuts | 57 |
| sesame | 37 |
| peanuts | 16 |
| fish | 15 |
| shellfish | 3 |
| other | 1 |

### Counts by classification

| classification | count |
| --- | ---: |
| Class II | 225 |
| Class I | 165 |
| Class III | 14 |

### Counts by month of report_date (YYYY-MM)

| month | count |
| --- | ---: |
| 2025-08 | 77 |
| 2025-07 | 58 |
| 2024-10 | 48 |
| 2025-06 | 34 |
| 2025-05 | 29 |
| 2025-09 | 29 |
| 2025-04 | 25 |
| 2025-02 | 24 |
| 2025-03 | 23 |
| 2025-01 | 21 |
| 2024-11 | 19 |
| 2024-12 | 17 |

### Counts by recalling_firm (exact source string)

| recalling_firm | count |
| --- | ---: |
| Reisman Bros Bakery | 24 |
| NatureMills US Incorporated | 17 |
| NEW GRAINS GLUTEN FREE BAKERY | 16 |
| Hillside Orchard Farms Inc. | 14 |
| Tropicale Foods, LLC | 14 |
| Knockroe Inc | 12 |
| Lemonland Food Corp | 12 |
| Cal Yee Farm LLC | 10 |
| M & P Food Productions, Ltd. | 9 |
| The Candy Barn | 9 |
| The Posh Bakery, Inc. | 9 |
| Turkeyfoot Creek Creamery LLC | 8 |
| Perfection Bakeries LLC | 7 |
| SHEEHAN BROTHERS VENDING | 6 |
| ZB Importing LLC | 6 |
| C SWEET PASTRY LLC | 5 |
| R&M TRADING LLC | 5 |
| SABORES FIT BAKERY | 5 |
| The Bonami Baking Company, Inc. | 5 |
| Yoder's Cashew Crunch | 5 |
| Fresh & Ready Foods LLC | 4 |
| Grand Central Bakery FRE Co Inc | 4 |
| Mondelez Global Llc | 4 |
| Shang Hao Jia, Inc | 4 |
| Wismettac Asian Foods, Inc. | 4 |
| Bakers Authority LLC | 3 |
| Bazzini LLC | 3 |
| Dinstuhl's Fine Candy Company, Inc. | 3 |
| Element 112, LLC | 3 |
| Grace Imports, Inc | 3 |
| Kilwin's Quality Confections, Inc. | 3 |
| Monkey Spit | 3 |
| Rajbhog Distributors TX Inc. | 3 |
| Abdallah Incorporated | 2 |
| Amazon Retail LLC | 2 |
| Atkinson Milling Company | 2 |
| Bondsforever, Inc dba Shastha Foods | 2 |
| CONTINENTAL DAIRY FACILITIES SOUTHWEST LLC | 2 |
| Cesarina Bakery, Inc | 2 |
| Frito-Lay, Inc. Headquarters | 2 |
| Jalux America  Inc | 2 |
| Jesse's Bakery, Inc. | 2 |
| KTM Services, Inc. | 2 |
| Kobayashi Noodle U.S.A. | 2 |
| La Fiesta Food Products | 2 |
| Liaoning Cheng Da (USA) Inc | 2 |
| Lithuanian Bakery, Inc. | 2 |
| Niitakaya USA Inc | 2 |
| Skagit River Bakery & Cafe | 2 |
| Weaver Nut Company, Inc | 2 |
| Alpine Food DIstributing, Inc | 1 |
| Anderson Candy Company, LLC | 1 |
| Ariana Sweets Inc. | 1 |
| Arizona Foods Group, Inc. | 1 |
| Avole, Inc. | 1 |
| BBF Massachusetts LLC | 1 |
| BUNGE NORTH AMERICA INC | 1 |
| Barry Callebaut USA LLC | 1 |
| Better Business...Better Foods, Inc. | 1 |
| Bioriginal Food & Science Corporation | 1 |
| Blue Bell Creameries, L.P. | 1 |
| Borsari Food Company Inc | 1 |
| Breadbox Co. | 1 |
| C.H. Guenther & Son LLC | 1 |
| C.H. Guenther & Son, Inc. | 1 |
| CON YEAGER SPICE CO. | 1 |
| Camerican International Inc | 1 |
| Caraluzzi's Markets | 1 |
| Cheesecake Royale, Inc. | 1 |
| Cromer Food Services, Inc | 1 |
| D. Coluccio & Sons Inc. | 1 |
| DELICIAS DE LA ABUELA INC | 1 |
| DFA Dairy Brands, LLC | 1 |
| Del Monte Fresh Produce N.A., Inc. | 1 |
| Deseret Biologicals Inc | 1 |
| Dessert Holdings Llc | 1 |
| Dianne's Fine Desserts | 1 |
| Dierbergs Markets, Inc. | 1 |
| Distinctive Foods LLC | 1 |
| Dollins Pecan Co, Inc | 1 |
| Dr. Praeger's Sensible Foods Inc. | 1 |
| EM Tortillas, LLC | 1 |
| Englewood Cannery | 1 |
| FRESHPOINT CENTRAL FLORIDA, INC. | 1 |
| Falafel King Enterprises, Inc. | 1 |
| Firehook of Virginia | 1 |
| Frito Lay Inc | 1 |
| GARDNER'S CANDIES , INC | 1 |
| GNC Holdings LLC | 1 |
| Gilster-Mary Lee Corporation Cake Plant | 1 |
| Gordon Desserts  DBA Mochidoki | 1 |
| Griffith Foods Inc. | 1 |
| HAR Maspeth Corp. | 1 |
| HAWAIIAN HOST CANDIES OF LA INC | 1 |
| HP Hood LLC | 1 |
| Hammond's Candies Since 1920 II, LLC | 1 |
| Hans Kissle Company, LLC | 1 |
| Harvey Investments LLC / The Baking Group | 1 |
| Homegrown Family Foods LLC | 1 |
| Honey Heaven Wholesale Inc | 1 |
| House Of Flavors, Inc. | 1 |
| I C F Factory Inc | 1 |
| Idaho Pacific Corporation | 1 |
| Innovation Bakers, LLC | 1 |
| JE Bakery 2019 LLC | 1 |
| JJWV Marketing Corporation | 1 |
| JR Simplot Company | 1 |
| JX Restaurants, Inc. | 1 |
| Julie's Gorditas | 1 |
| Kedake Inc | 1 |
| Kenover Marketing Corp. | 1 |
| LEWIS BAKERIES | 1 |
| LITTLE LEAF FARMS LLC | 1 |
| La Fontanella Food Products LLC | 1 |
| Las Delicias Distributors, LLC | 1 |
| Latitude 36 Foods | 1 |
| Lidl US TRADING | 1 |
| Lipari Foods Operating Company, LLC. | 1 |
| MOMO TEA INC | 1 |
| MTN OPS, LLC | 1 |
| Mac & Co | 1 |
| Mauna Loa Macadamia Nut Company, LLC | 1 |
| May Flower International Inc | 1 |
| Meijer, Inc #816 - Grand River Packaging | 1 |
| Mellace Family Brands California Inc | 1 |
| Mi Ranchito Foods, Incorporated | 1 |
| Middle East/ Soli's Baking Company, Inc. dba Middle East Baking Co. | 1 |
| Mightylicious Inc. | 1 |
| Mutual Trading Company Inc. | 1 |
| My Life Inc | 1 |
| NATURIPE VALUE ADDED FRESH LLC | 1 |
| Nader Trading, Inc. | 1 |
| Neuhaus nv | 1 |
| Nuts.com | 1 |
| OLD WORLD SPICES & SEASONING, INC | 1 |
| OYATSUPAN BAKERS | 1 |
| One Roof LLC | 1 |
| Optima Foods, Inc. | 1 |
| Orgain, LLC | 1 |
| Pain Train Salsa, LLC | 1 |
| Panaderia Salvadorena Ii | 1 |
| Pecan Star & Nut Corp. | 1 |
| Pinsarella Food LLC | 1 |
| Prep'd CDA LLC | 1 |
| Quantum Fulfillment and Support, LLC | 1 |
| R. Walters Foods, Limited Liability Corporation | 1 |
| Reser's Fine Foods, Inc. | 1 |
| Robin J Vos dba TS Food Packaging | 1 |
| Rocky Mountain Chocolate Factory, Inc. | 1 |
| SE Tampa Inc dba Tampa Food | 1 |
| SRI SRI TATTVA | 1 |
| SUGAR FOODS LLC | 1 |
| Salt City Baking Company, LLC | 1 |
| Santa Monica Seafood Company | 1 |
| Saratoga Potato Chips LLC | 1 |
| Seattle Homemade Thai LLC | 1 |
| South Asian Food Inc. | 1 |
| Supplement Manufacturing Partner Inc. | 1 |
| Sweet Sam's Baking Company, LLC | 1 |
| Sweetheart USA, LLC | 1 |
| Taylor Farms Illinois Inc. | 1 |
| Taylor Farms Retail, Inc. | 1 |
| The Coastal Companies DBA Hearn Kirkwood | 1 |
| The Granola Bar | 1 |
| The Hot Chocolatier - St. Elmo, LLC | 1 |
| The Mochi Ice Cream Company | 1 |
| Tipical Latin Food, Corp. dba La Pradera | 1 |
| Tortilleria Xpress Inc | 1 |
| Trophy Nut Company | 1 |
| Tropical Nut & Fruit Company | 1 |
| Unilever Manufacturing (US), Inc. | 1 |
| United Natural Trading Inc. dba Woodstock Farms | 1 |
| University Of Wisconsin Madison Babcock Hall Dairy Plant | 1 |
| VAUGHAN MILLS PACKAGING LTD. | 1 |
| Vern's Foods & Farm | 1 |
| Vietti Acquisitions, LLC | 1 |
| Vita Warehouse Corp. | 1 |
| Wegmans Food Markets, Inc. | 1 |

### Firms with kept recalls in 3 or more different report_date months

| recalling_firm (distinct months) | count |
| --- | ---: |
| (none) | 0 |


## PULL 2

- total records returned: 1564
- kept (undeclared allergen): 404
- CSV: `food-allergen-pull2.csv` · rows 1564 · SHA-256 `4fd72143cff263d845d08a4365bddeb3c46a7db9c8efa9d2c1f8bed80f673316`

### Counts by allergen (kept records only)

| allergen | count |
| --- | ---: |
| milk | 138 |
| wheat | 124 |
| soybeans | 84 |
| egg | 65 |
| tree nuts | 57 |
| sesame | 37 |
| peanuts | 16 |
| fish | 15 |
| shellfish | 3 |
| other | 1 |

### Counts by classification

| classification | count |
| --- | ---: |
| Class II | 225 |
| Class I | 165 |
| Class III | 14 |

### Counts by month of report_date (YYYY-MM)

| month | count |
| --- | ---: |
| 2025-08 | 77 |
| 2025-07 | 58 |
| 2024-10 | 48 |
| 2025-06 | 34 |
| 2025-05 | 29 |
| 2025-09 | 29 |
| 2025-04 | 25 |
| 2025-02 | 24 |
| 2025-03 | 23 |
| 2025-01 | 21 |
| 2024-11 | 19 |
| 2024-12 | 17 |

### Counts by recalling_firm (exact source string)

| recalling_firm | count |
| --- | ---: |
| Reisman Bros Bakery | 24 |
| NatureMills US Incorporated | 17 |
| NEW GRAINS GLUTEN FREE BAKERY | 16 |
| Hillside Orchard Farms Inc. | 14 |
| Tropicale Foods, LLC | 14 |
| Knockroe Inc | 12 |
| Lemonland Food Corp | 12 |
| Cal Yee Farm LLC | 10 |
| M & P Food Productions, Ltd. | 9 |
| The Candy Barn | 9 |
| The Posh Bakery, Inc. | 9 |
| Turkeyfoot Creek Creamery LLC | 8 |
| Perfection Bakeries LLC | 7 |
| SHEEHAN BROTHERS VENDING | 6 |
| ZB Importing LLC | 6 |
| C SWEET PASTRY LLC | 5 |
| R&M TRADING LLC | 5 |
| SABORES FIT BAKERY | 5 |
| The Bonami Baking Company, Inc. | 5 |
| Yoder's Cashew Crunch | 5 |
| Fresh & Ready Foods LLC | 4 |
| Grand Central Bakery FRE Co Inc | 4 |
| Mondelez Global Llc | 4 |
| Shang Hao Jia, Inc | 4 |
| Wismettac Asian Foods, Inc. | 4 |
| Bakers Authority LLC | 3 |
| Bazzini LLC | 3 |
| Dinstuhl's Fine Candy Company, Inc. | 3 |
| Element 112, LLC | 3 |
| Grace Imports, Inc | 3 |
| Kilwin's Quality Confections, Inc. | 3 |
| Monkey Spit | 3 |
| Rajbhog Distributors TX Inc. | 3 |
| Abdallah Incorporated | 2 |
| Amazon Retail LLC | 2 |
| Atkinson Milling Company | 2 |
| Bondsforever, Inc dba Shastha Foods | 2 |
| CONTINENTAL DAIRY FACILITIES SOUTHWEST LLC | 2 |
| Cesarina Bakery, Inc | 2 |
| Frito-Lay, Inc. Headquarters | 2 |
| Jalux America  Inc | 2 |
| Jesse's Bakery, Inc. | 2 |
| KTM Services, Inc. | 2 |
| Kobayashi Noodle U.S.A. | 2 |
| La Fiesta Food Products | 2 |
| Liaoning Cheng Da (USA) Inc | 2 |
| Lithuanian Bakery, Inc. | 2 |
| Niitakaya USA Inc | 2 |
| Skagit River Bakery & Cafe | 2 |
| Weaver Nut Company, Inc | 2 |
| Alpine Food DIstributing, Inc | 1 |
| Anderson Candy Company, LLC | 1 |
| Ariana Sweets Inc. | 1 |
| Arizona Foods Group, Inc. | 1 |
| Avole, Inc. | 1 |
| BBF Massachusetts LLC | 1 |
| BUNGE NORTH AMERICA INC | 1 |
| Barry Callebaut USA LLC | 1 |
| Better Business...Better Foods, Inc. | 1 |
| Bioriginal Food & Science Corporation | 1 |
| Blue Bell Creameries, L.P. | 1 |
| Borsari Food Company Inc | 1 |
| Breadbox Co. | 1 |
| C.H. Guenther & Son LLC | 1 |
| C.H. Guenther & Son, Inc. | 1 |
| CON YEAGER SPICE CO. | 1 |
| Camerican International Inc | 1 |
| Caraluzzi's Markets | 1 |
| Cheesecake Royale, Inc. | 1 |
| Cromer Food Services, Inc | 1 |
| D. Coluccio & Sons Inc. | 1 |
| DELICIAS DE LA ABUELA INC | 1 |
| DFA Dairy Brands, LLC | 1 |
| Del Monte Fresh Produce N.A., Inc. | 1 |
| Deseret Biologicals Inc | 1 |
| Dessert Holdings Llc | 1 |
| Dianne's Fine Desserts | 1 |
| Dierbergs Markets, Inc. | 1 |
| Distinctive Foods LLC | 1 |
| Dollins Pecan Co, Inc | 1 |
| Dr. Praeger's Sensible Foods Inc. | 1 |
| EM Tortillas, LLC | 1 |
| Englewood Cannery | 1 |
| FRESHPOINT CENTRAL FLORIDA, INC. | 1 |
| Falafel King Enterprises, Inc. | 1 |
| Firehook of Virginia | 1 |
| Frito Lay Inc | 1 |
| GARDNER'S CANDIES , INC | 1 |
| GNC Holdings LLC | 1 |
| Gilster-Mary Lee Corporation Cake Plant | 1 |
| Gordon Desserts  DBA Mochidoki | 1 |
| Griffith Foods Inc. | 1 |
| HAR Maspeth Corp. | 1 |
| HAWAIIAN HOST CANDIES OF LA INC | 1 |
| HP Hood LLC | 1 |
| Hammond's Candies Since 1920 II, LLC | 1 |
| Hans Kissle Company, LLC | 1 |
| Harvey Investments LLC / The Baking Group | 1 |
| Homegrown Family Foods LLC | 1 |
| Honey Heaven Wholesale Inc | 1 |
| House Of Flavors, Inc. | 1 |
| I C F Factory Inc | 1 |
| Idaho Pacific Corporation | 1 |
| Innovation Bakers, LLC | 1 |
| JE Bakery 2019 LLC | 1 |
| JJWV Marketing Corporation | 1 |
| JR Simplot Company | 1 |
| JX Restaurants, Inc. | 1 |
| Julie's Gorditas | 1 |
| Kedake Inc | 1 |
| Kenover Marketing Corp. | 1 |
| LEWIS BAKERIES | 1 |
| LITTLE LEAF FARMS LLC | 1 |
| La Fontanella Food Products LLC | 1 |
| Las Delicias Distributors, LLC | 1 |
| Latitude 36 Foods | 1 |
| Lidl US TRADING | 1 |
| Lipari Foods Operating Company, LLC. | 1 |
| MOMO TEA INC | 1 |
| MTN OPS, LLC | 1 |
| Mac & Co | 1 |
| Mauna Loa Macadamia Nut Company, LLC | 1 |
| May Flower International Inc | 1 |
| Meijer, Inc #816 - Grand River Packaging | 1 |
| Mellace Family Brands California Inc | 1 |
| Mi Ranchito Foods, Incorporated | 1 |
| Middle East/ Soli's Baking Company, Inc. dba Middle East Baking Co. | 1 |
| Mightylicious Inc. | 1 |
| Mutual Trading Company Inc. | 1 |
| My Life Inc | 1 |
| NATURIPE VALUE ADDED FRESH LLC | 1 |
| Nader Trading, Inc. | 1 |
| Neuhaus nv | 1 |
| Nuts.com | 1 |
| OLD WORLD SPICES & SEASONING, INC | 1 |
| OYATSUPAN BAKERS | 1 |
| One Roof LLC | 1 |
| Optima Foods, Inc. | 1 |
| Orgain, LLC | 1 |
| Pain Train Salsa, LLC | 1 |
| Panaderia Salvadorena Ii | 1 |
| Pecan Star & Nut Corp. | 1 |
| Pinsarella Food LLC | 1 |
| Prep'd CDA LLC | 1 |
| Quantum Fulfillment and Support, LLC | 1 |
| R. Walters Foods, Limited Liability Corporation | 1 |
| Reser's Fine Foods, Inc. | 1 |
| Robin J Vos dba TS Food Packaging | 1 |
| Rocky Mountain Chocolate Factory, Inc. | 1 |
| SE Tampa Inc dba Tampa Food | 1 |
| SRI SRI TATTVA | 1 |
| SUGAR FOODS LLC | 1 |
| Salt City Baking Company, LLC | 1 |
| Santa Monica Seafood Company | 1 |
| Saratoga Potato Chips LLC | 1 |
| Seattle Homemade Thai LLC | 1 |
| South Asian Food Inc. | 1 |
| Supplement Manufacturing Partner Inc. | 1 |
| Sweet Sam's Baking Company, LLC | 1 |
| Sweetheart USA, LLC | 1 |
| Taylor Farms Illinois Inc. | 1 |
| Taylor Farms Retail, Inc. | 1 |
| The Coastal Companies DBA Hearn Kirkwood | 1 |
| The Granola Bar | 1 |
| The Hot Chocolatier - St. Elmo, LLC | 1 |
| The Mochi Ice Cream Company | 1 |
| Tipical Latin Food, Corp. dba La Pradera | 1 |
| Tortilleria Xpress Inc | 1 |
| Trophy Nut Company | 1 |
| Tropical Nut & Fruit Company | 1 |
| Unilever Manufacturing (US), Inc. | 1 |
| United Natural Trading Inc. dba Woodstock Farms | 1 |
| University Of Wisconsin Madison Babcock Hall Dairy Plant | 1 |
| VAUGHAN MILLS PACKAGING LTD. | 1 |
| Vern's Foods & Farm | 1 |
| Vietti Acquisitions, LLC | 1 |
| Vita Warehouse Corp. | 1 |
| Wegmans Food Markets, Inc. | 1 |

### Firms with kept recalls in 3 or more different report_date months

| recalling_firm (distinct months) | count |
| --- | ---: |
| (none) | 0 |


## PULL 3

- total records returned: 1564
- kept (undeclared allergen): 404
- CSV: `food-allergen-pull3.csv` · rows 1564 · SHA-256 `4fd72143cff263d845d08a4365bddeb3c46a7db9c8efa9d2c1f8bed80f673316`

### Counts by allergen (kept records only)

| allergen | count |
| --- | ---: |
| milk | 138 |
| wheat | 124 |
| soybeans | 84 |
| egg | 65 |
| tree nuts | 57 |
| sesame | 37 |
| peanuts | 16 |
| fish | 15 |
| shellfish | 3 |
| other | 1 |

### Counts by classification

| classification | count |
| --- | ---: |
| Class II | 225 |
| Class I | 165 |
| Class III | 14 |

### Counts by month of report_date (YYYY-MM)

| month | count |
| --- | ---: |
| 2025-08 | 77 |
| 2025-07 | 58 |
| 2024-10 | 48 |
| 2025-06 | 34 |
| 2025-05 | 29 |
| 2025-09 | 29 |
| 2025-04 | 25 |
| 2025-02 | 24 |
| 2025-03 | 23 |
| 2025-01 | 21 |
| 2024-11 | 19 |
| 2024-12 | 17 |

### Counts by recalling_firm (exact source string)

| recalling_firm | count |
| --- | ---: |
| Reisman Bros Bakery | 24 |
| NatureMills US Incorporated | 17 |
| NEW GRAINS GLUTEN FREE BAKERY | 16 |
| Hillside Orchard Farms Inc. | 14 |
| Tropicale Foods, LLC | 14 |
| Knockroe Inc | 12 |
| Lemonland Food Corp | 12 |
| Cal Yee Farm LLC | 10 |
| M & P Food Productions, Ltd. | 9 |
| The Candy Barn | 9 |
| The Posh Bakery, Inc. | 9 |
| Turkeyfoot Creek Creamery LLC | 8 |
| Perfection Bakeries LLC | 7 |
| SHEEHAN BROTHERS VENDING | 6 |
| ZB Importing LLC | 6 |
| C SWEET PASTRY LLC | 5 |
| R&M TRADING LLC | 5 |
| SABORES FIT BAKERY | 5 |
| The Bonami Baking Company, Inc. | 5 |
| Yoder's Cashew Crunch | 5 |
| Fresh & Ready Foods LLC | 4 |
| Grand Central Bakery FRE Co Inc | 4 |
| Mondelez Global Llc | 4 |
| Shang Hao Jia, Inc | 4 |
| Wismettac Asian Foods, Inc. | 4 |
| Bakers Authority LLC | 3 |
| Bazzini LLC | 3 |
| Dinstuhl's Fine Candy Company, Inc. | 3 |
| Element 112, LLC | 3 |
| Grace Imports, Inc | 3 |
| Kilwin's Quality Confections, Inc. | 3 |
| Monkey Spit | 3 |
| Rajbhog Distributors TX Inc. | 3 |
| Abdallah Incorporated | 2 |
| Amazon Retail LLC | 2 |
| Atkinson Milling Company | 2 |
| Bondsforever, Inc dba Shastha Foods | 2 |
| CONTINENTAL DAIRY FACILITIES SOUTHWEST LLC | 2 |
| Cesarina Bakery, Inc | 2 |
| Frito-Lay, Inc. Headquarters | 2 |
| Jalux America  Inc | 2 |
| Jesse's Bakery, Inc. | 2 |
| KTM Services, Inc. | 2 |
| Kobayashi Noodle U.S.A. | 2 |
| La Fiesta Food Products | 2 |
| Liaoning Cheng Da (USA) Inc | 2 |
| Lithuanian Bakery, Inc. | 2 |
| Niitakaya USA Inc | 2 |
| Skagit River Bakery & Cafe | 2 |
| Weaver Nut Company, Inc | 2 |
| Alpine Food DIstributing, Inc | 1 |
| Anderson Candy Company, LLC | 1 |
| Ariana Sweets Inc. | 1 |
| Arizona Foods Group, Inc. | 1 |
| Avole, Inc. | 1 |
| BBF Massachusetts LLC | 1 |
| BUNGE NORTH AMERICA INC | 1 |
| Barry Callebaut USA LLC | 1 |
| Better Business...Better Foods, Inc. | 1 |
| Bioriginal Food & Science Corporation | 1 |
| Blue Bell Creameries, L.P. | 1 |
| Borsari Food Company Inc | 1 |
| Breadbox Co. | 1 |
| C.H. Guenther & Son LLC | 1 |
| C.H. Guenther & Son, Inc. | 1 |
| CON YEAGER SPICE CO. | 1 |
| Camerican International Inc | 1 |
| Caraluzzi's Markets | 1 |
| Cheesecake Royale, Inc. | 1 |
| Cromer Food Services, Inc | 1 |
| D. Coluccio & Sons Inc. | 1 |
| DELICIAS DE LA ABUELA INC | 1 |
| DFA Dairy Brands, LLC | 1 |
| Del Monte Fresh Produce N.A., Inc. | 1 |
| Deseret Biologicals Inc | 1 |
| Dessert Holdings Llc | 1 |
| Dianne's Fine Desserts | 1 |
| Dierbergs Markets, Inc. | 1 |
| Distinctive Foods LLC | 1 |
| Dollins Pecan Co, Inc | 1 |
| Dr. Praeger's Sensible Foods Inc. | 1 |
| EM Tortillas, LLC | 1 |
| Englewood Cannery | 1 |
| FRESHPOINT CENTRAL FLORIDA, INC. | 1 |
| Falafel King Enterprises, Inc. | 1 |
| Firehook of Virginia | 1 |
| Frito Lay Inc | 1 |
| GARDNER'S CANDIES , INC | 1 |
| GNC Holdings LLC | 1 |
| Gilster-Mary Lee Corporation Cake Plant | 1 |
| Gordon Desserts  DBA Mochidoki | 1 |
| Griffith Foods Inc. | 1 |
| HAR Maspeth Corp. | 1 |
| HAWAIIAN HOST CANDIES OF LA INC | 1 |
| HP Hood LLC | 1 |
| Hammond's Candies Since 1920 II, LLC | 1 |
| Hans Kissle Company, LLC | 1 |
| Harvey Investments LLC / The Baking Group | 1 |
| Homegrown Family Foods LLC | 1 |
| Honey Heaven Wholesale Inc | 1 |
| House Of Flavors, Inc. | 1 |
| I C F Factory Inc | 1 |
| Idaho Pacific Corporation | 1 |
| Innovation Bakers, LLC | 1 |
| JE Bakery 2019 LLC | 1 |
| JJWV Marketing Corporation | 1 |
| JR Simplot Company | 1 |
| JX Restaurants, Inc. | 1 |
| Julie's Gorditas | 1 |
| Kedake Inc | 1 |
| Kenover Marketing Corp. | 1 |
| LEWIS BAKERIES | 1 |
| LITTLE LEAF FARMS LLC | 1 |
| La Fontanella Food Products LLC | 1 |
| Las Delicias Distributors, LLC | 1 |
| Latitude 36 Foods | 1 |
| Lidl US TRADING | 1 |
| Lipari Foods Operating Company, LLC. | 1 |
| MOMO TEA INC | 1 |
| MTN OPS, LLC | 1 |
| Mac & Co | 1 |
| Mauna Loa Macadamia Nut Company, LLC | 1 |
| May Flower International Inc | 1 |
| Meijer, Inc #816 - Grand River Packaging | 1 |
| Mellace Family Brands California Inc | 1 |
| Mi Ranchito Foods, Incorporated | 1 |
| Middle East/ Soli's Baking Company, Inc. dba Middle East Baking Co. | 1 |
| Mightylicious Inc. | 1 |
| Mutual Trading Company Inc. | 1 |
| My Life Inc | 1 |
| NATURIPE VALUE ADDED FRESH LLC | 1 |
| Nader Trading, Inc. | 1 |
| Neuhaus nv | 1 |
| Nuts.com | 1 |
| OLD WORLD SPICES & SEASONING, INC | 1 |
| OYATSUPAN BAKERS | 1 |
| One Roof LLC | 1 |
| Optima Foods, Inc. | 1 |
| Orgain, LLC | 1 |
| Pain Train Salsa, LLC | 1 |
| Panaderia Salvadorena Ii | 1 |
| Pecan Star & Nut Corp. | 1 |
| Pinsarella Food LLC | 1 |
| Prep'd CDA LLC | 1 |
| Quantum Fulfillment and Support, LLC | 1 |
| R. Walters Foods, Limited Liability Corporation | 1 |
| Reser's Fine Foods, Inc. | 1 |
| Robin J Vos dba TS Food Packaging | 1 |
| Rocky Mountain Chocolate Factory, Inc. | 1 |
| SE Tampa Inc dba Tampa Food | 1 |
| SRI SRI TATTVA | 1 |
| SUGAR FOODS LLC | 1 |
| Salt City Baking Company, LLC | 1 |
| Santa Monica Seafood Company | 1 |
| Saratoga Potato Chips LLC | 1 |
| Seattle Homemade Thai LLC | 1 |
| South Asian Food Inc. | 1 |
| Supplement Manufacturing Partner Inc. | 1 |
| Sweet Sam's Baking Company, LLC | 1 |
| Sweetheart USA, LLC | 1 |
| Taylor Farms Illinois Inc. | 1 |
| Taylor Farms Retail, Inc. | 1 |
| The Coastal Companies DBA Hearn Kirkwood | 1 |
| The Granola Bar | 1 |
| The Hot Chocolatier - St. Elmo, LLC | 1 |
| The Mochi Ice Cream Company | 1 |
| Tipical Latin Food, Corp. dba La Pradera | 1 |
| Tortilleria Xpress Inc | 1 |
| Trophy Nut Company | 1 |
| Tropical Nut & Fruit Company | 1 |
| Unilever Manufacturing (US), Inc. | 1 |
| United Natural Trading Inc. dba Woodstock Farms | 1 |
| University Of Wisconsin Madison Babcock Hall Dairy Plant | 1 |
| VAUGHAN MILLS PACKAGING LTD. | 1 |
| Vern's Foods & Farm | 1 |
| Vietti Acquisitions, LLC | 1 |
| Vita Warehouse Corp. | 1 |
| Wegmans Food Markets, Inc. | 1 |

### Firms with kept recalls in 3 or more different report_date months

| recalling_firm (distinct months) | count |
| --- | ---: |
| (none) | 0 |


synmerco-data
4fd72143cff263d845d08a4365bddeb3c46a7db9c8efa9d2c1f8bed80f673316 food-allergen-pull1.csv
4fd72143cff263d845d08a4365bddeb3c46a7db9c8efa9d2c1f8bed80f673316 food-allergen-pull2.csv
4fd72143cff263d845d08a4365bddeb3c46a7db9c8efa9d2c1f8bed80f673316 food-allergen-pull3.csv

## Changes — PULL 2 vs PULL 1

- new: 0 
- gone: 0 
- changed: 0
- row counts: earlier 1564, later 1564 (= earlier + new - gone = 1564)
- no change (earlier 1564, later 1564)

## Changes — PULL 3 vs PULL 2

- new: 0 
- gone: 0 
- changed: 0
- row counts: earlier 1564, later 1564 (= earlier + new - gone = 1564)
- no change (earlier 1564, later 1564)

## PROOF

### PULL 1 — every request (UTC, Date header, meta verbatim)

- Request: GET https://api.fda.gov/food/enforcement.json?search=report_date%3A%5B20241001+TO+20250930%5D&limit=1000&skip=0
  - Retrieved (UTC): 2026-11-10T02:09:39Z · HTTP 200
  - Date: Tue, 10 Nov 2026 02:09:43 GMT
  - meta object verbatim:
```json
{
  "disclaimer": "Do not rely on openFDA to make decisions regarding medical care. While we make every effort to ensure that data is accurate, you should assume all results are unvalidated. We may limit or otherwise restrict your access to the API in line with our Terms of Service.",
  "terms": "https://open.fda.gov/terms/",
  "license": "https://open.fda.gov/license/",
  "last_updated": "2026-10-28",
  "results": {
    "skip": 0,
    "limit": 1000,
    "total": 1564
  }
}
```
- Request: GET https://api.fda.gov/food/enforcement.json?search=report_date%3A%5B20241001+TO+20250930%5D&limit=1000&skip=1000
  - Retrieved (UTC): 2026-11-10T02:09:42Z · HTTP 200
  - Date: Tue, 10 Nov 2026 02:09:46 GMT
  - meta object verbatim:
```json
{
  "disclaimer": "Do not rely on openFDA to make decisions regarding medical care. While we make every effort to ensure that data is accurate, you should assume all results are unvalidated. We may limit or otherwise restrict your access to the API in line with our Terms of Service.",
  "terms": "https://open.fda.gov/terms/",
  "license": "https://open.fda.gov/license/",
  "last_updated": "2026-10-28",
  "results": {
    "skip": 1000,
    "limit": 1000,
    "total": 1564
  }
}
```

### PULL 1 — reason_for_recall of every kept record

```text
F-0001-2025 | Undeclared wheat. The firm was notified by their supplier that they failed to include the allergen "wheat" on the label.
F-0002-2025 | Undeclared wheat. The firm was notified by their supplier that they failed to include the allergen "wheat" on the label.
F-0003-2025 | Undeclared wheat. The firm was notified by their supplier that they failed to include the allergen "wheat" on the label.
F-0014-2025 | Undeclared whey (milk), wheat flour, almonds; no contains statement & no nutrition fact panel
F-0015-2025 | Undeclared whey (milk) & wheat flour: no nutrition fact panel & no contains statement
F-0016-2025 | Undeclared whey (milk), wheat flour, & bran (wheat); no nutrition fact panel & no contains statement
F-0017-2025 | Undeclared whey (milk) & wheat flour; no nutrition fact panel & no contains statement
F-0018-2025 | Undeclared whey (milk) & wheat flour: no nutrition fact panel & no contains statement
F-0019-2025 | Undeclared whey (milk) & wheat flour; no nutrition fact panel & no contains statement
F-0020-2025 | Undeclared whey (milk) and wheat flour; no nutritional fact panel & no contains statement
F-0021-2025 | Undeclared whey (milk), wheat flour, & coconut; no nutrition fact panel & no contains statement
F-0022-2025 | Undeclared whey (milk) & wheat flour; no nutrition fact panel & no contains statement
F-0023-2025 | Undeclared allergens; walnuts
F-0035-2025 | Undeclared allergens; milk
F-0036-2025 | Undeclared allergens; milk
F-0037-2025 | Undeclared Allergen, milk - a mix-up between the product description and the ingredient list. Milk Chocolate was listed in the product description but was missing from the ingredient list.
F-0038-2025 | Mayonnaise is declared but Soybean Oil and Egg are not declared.
F-0039-2025 | Soybean Paste is declared but Wheat and Sesame Seeds are not declared.
F-0041-2025 | Soybean Sauce is declared but Wheat and Fish (Anchovy) are not declared.
F-0042-2025 | Soybean Sauce is declared but Wheat is not declared.
F-0043-2025 | Undeclared Crustacean (shrimp).
F-0044-2025 | Undeclared Fish (Anchovy).
F-0045-2025 | Soybean Sauce is declared but Wheat and Fish (Anchovy) are not declared.
F-0046-2025 | Undeclared Fish (Anchovy).
F-0047-2025 | Soy Sauce is declared but Wheat is not declared.
F-0048-2025 | Soy Bean Paste is declared but Wheat, Fish (Large-eyed Herring, Anchovy), and Crustacean (Shrimp) are not declared.
F-0049-2025 | Soy Sauce is declare but Wheat and Fish (Anchovy) are not declared.
F-0050-2025 | Soy Sauce is declared but Wheat is not declared.
F-0054-2025 | Milk may contain undeclared almond from almond milk
F-0057-2025 | Undeclared Wheat flour. Product contains wheat flour but product was sold without the Ingredients Statement.
F-0067-2025 | Undeclared Almonds & Cashews. The firm was notified by their customers that the product contains a trail mix instead of the cheese mix. The trail mix contains almonds and cashews that are not listed in the ingredient statement.
F-0068-2025 | Undeclared Fish Allergen
F-0077-2025 | Undeclared allergen:Wheat
F-0097-2025 | Undeclared allergens; wheat, soy, and eggs.
F-0098-2025 | Undeclared allergen: milk
F-0099-2025 | Undeclared sesame
F-0100-2025 | Undeclared sesame
F-0101-2025 | Undeclared sesame
F-0102-2025 | Undeclared sesame
F-0103-2025 | Undeclared sesame
F-0104-2025 | Undeclared sesame
F-0105-2025 | Undeclared sesame
F-0120-2025 | Undeclared allergens; sesame
F-0121-2025 | Butter lists cream, but may be missing the Contains Milk statement.
F-0122-2025 | Butter lists cream, but may be missing the Contains Milk statement.
F-0126-2025 | The product is being recalled due to an undeclared allergen - tree nuts (walnuts).
F-0132-2025 | Undeclared wheat. Product contains wheat but was mis-labeled as Savory 6 Cut Crinkle Cut Wedge and label does not declare wheat.
F-0147-2025 | Product contains undeclared hydrolyzed soy protein.
F-0148-2025 | Undeclared egg
F-0216-2025 | Undeclared tree nuts (almonds)
F-0217-2025 | Undeclared egg
F-0218-2025 | Undeclared egg
F-0219-2025 | Undeclared egg
F-0220-2025 | Undeclared egg
F-0244-2025 | Undeclared eggs and yellow #5.
F-0245-2025 | Contains undeclared egg
F-0253-2025 | Undeclared allergen - egg
F-0259-2025 | Undeclared Wheat. The firm was notified by a consumer that they found crispy onions in the packaging of the tortilla strips. The onions contain wheat which is not listed on the packaging for the tortilla strips.
F-0260-2025 | Undeclared Allergen - Wheat and Soy
F-0262-2025 | Product contains undeclared soy lecithin.
F-0263-2025 | Contains undeclared soy lecithin
F-0266-2025 | Undeclared soy (soy lecithin).
F-0293-2025 | Undeclared allergen labeling (milk)
F-0294-2025 | Undeclared allergen labeling (milk)
F-0295-2025 | Undeclared allergen labeling (milk)
F-0296-2025 | Undeclared allergen labeling (milk)
F-0297-2025 | Undeclared allergen labeling (milk)
F-0299-2025 | Undeclared allergens: Milk, Soy, Crustacea Shellfish, Fish
F-0317-2025 | Product contains undeclared fish (anchovy) and soy.
F-0319-2025 | Products contain undeclared allergens (milk, soy, and wheat) and undeclared sulfites, yellow 5, yellow 6.
F-0320-2025 | Products contain undeclared allergens (milk, soy, peanut, and wheat) and undeclared sulfites, yellow 5, yellow 6, and red 40)
F-0321-2025 | The contains statement does not declare sesame. Black sesame seeds are visible on product and the Ingredients Statement declares black sesame seeds.
F-0376-2025 | Product contains Undeclared Allergen Tree Nuts (Cashews)
F-0384-2025 | Undeclared egg allergen
F-0386-2025 | Potential contamination of undeclared allergen peanuts
F-0402-2025 | Undeclared allergens (Wheat and Soy)
F-0404-2025 | Product does not include statement: Contains milk
F-0409-2025 | Undeclared milk
F-0411-2025 | Undeclared milk
F-0412-2025 | Undeclared wheat, Undeclared soybean oil
F-0413-2025 | Undeclared wheat, Undeclared soybean oil
F-0414-2025 | Undeclared milk
F-0415-2025 | Undeclared milk
F-0416-2025 | Undeclared milk
F-0417-2025 | Undeclared almonds
F-0418-2025 | Undeclared milk
F-0419-2025 | Undeclared milk
F-0421-2025 | Product contains undeclared milk and soy.
F-0422-2025 | Undeclared Milk. During an FDA investigation the manufacturer was notified that the label does not list the allergen milk in the ingredient statement.
F-0428-2025 | Undeclared Milk Allergen
F-0431-2025 | Frozen Peach Mango Sorbet contains undeclared allergen (egg)
F-0433-2025 | Soy is missing from the "Contains" statement.
F-0458-2025 | Barbeque sauce product contains undeclared allergens (soy) contained in sub-ingredient
F-0459-2025 | Barbeque sauce product contains undeclared allergen listing of (Milk) in product ingredient listing from sub-ingredient Butter.
F-0460-2025 | Barbeque sauce product contains undeclared listing of (Milk) in product ingredient listing from sub-ingredient Butter.
F-0461-2025 | The product is being recalled because of undeclared milk .
F-0462-2025 | The product is being recalled because of undeclared milk .
F-0463-2025 | The product is being recalled because of undeclared milk .
F-0464-2025 | Undeclared milk
F-0465-2025 | Undeclared walnuts
F-0466-2025 | Undeclared Milk. During the firm's reordering process of labels, they discovered that the label does not list milk in its ingredient or contain statement.
F-0467-2025 | Undeclared Milk. During the firm's reordering process of labels, they discovered that the label does not list milk in its ingredient or contain statement.
F-0469-2025 | Undeclared allergens (wheat) on label, incorrect label was placed on product
F-0531-2025 | Contains undeclared visible almonds
F-0532-2025 | Firm distributed a Bread Crumb product with undeclared allergen (Sesame) not on the label.
F-0533-2025 | Firm distributed a Seasoned Bread Crumb product with undeclared allergen (Sesame) not on the label.
F-0534-2025 | Imported Monkfish Liver undeclared allergen (Milk)
F-0548-2025 | Undeclared allergen (Milk) in Shirakiku brand Curvee Puffs Corn Puff Snack
F-0549-2025 | Undeclared allergen (Milk) in Shirakiku brand Curvee Puffs Corn Puff Snack
F-0550-2025 | Undeclared allergen (Milk) in Shirakiku brand Curvee Puffs Corn Puff Snack
F-0552-2025 | Undeclared Allergen - Milk
F-0553-2025 | Undeclared milk allergen
F-0570-2025 | Undeclared allergen (soy).
F-0572-2025 | Product may contain egg, an undeclared allergen.
F-0573-2025 | Potato flour item #20501 was recalled due to undeclared milk (between 13ppm and 17ppm).
F-0577-2025 | Mislabeled salads (undeclared peanut allergen). Incorrect ingredient applied (peanuts)
F-0581-2025 | Undeclared milk
F-0582-2025 | Undeclared milk
F-0583-2025 | Undeclared milk
F-0604-2025 | Undeclared Milk.
F-0605-2025 | Undeclared Milk.
F-0606-2025 | Undeclared egg.
F-0607-2025 | Undeclared egg.
F-0608-2025 | Undeclared allergen (walnuts)
F-0624-2025 | Milk not listed in the ingredients or included in parentheses after American Cheese.
F-0630-2025 | Milk not declared as the major food allergen source for the ingredient Whey
F-0631-2025 | Undeclared egg
F-0632-2025 | Milk not listed in Contains statement
F-0633-2025 | Undeclared wheat and egg
F-0634-2025 | Egg not listed in Contains statement
F-0635-2025 | Wheat not listed in Contains statement
F-0636-2025 | Undeclared almonds
F-0637-2025 | Product may contain incorrect salad dressing, resulting in fish and wheat being undeclared.
F-0638-2025 | Incorrect back label on product resulting in undeclared allergens (wheat, eggs)
F-0639-2025 | Contains undeclared milk
F-0649-2025 | Undeclared soy lecithin and undeclared color additives Blue 1 Lake, Yellow 6, Red 40, Yellow 5, Blue 1, Yellow 6 Lake, Red 40 Lake, Yellow 5 Lake, Blue 2 Lake, Blue 2.
F-0663-2025 | Contains undeclared egg
F-0667-2025 | Undeclared Pecan. The firm was notified by their customer that when they were placing the product on the shelves, they noticed the wrong product was in the container.
F-0669-2025 | Undeclared Allergen (Milk)
F-0672-2025 | (Imported) Hot Pot Sauce contains undeclared allergens (Wheat and Soy)
F-0673-2025 | (Imported) Hot Pot Sauce (SPICY) contains undeclared allergens (Wheat and Soy)
F-0674-2025 | Finished product label fails to include Milk in ingredient listing. (Undeclared Allergen)
F-0686-2025 | Turkey BLT on Sourdough Sandwiches being recalled due to the product having the incorrect sandwich (Peanut Butter & Jelly) in the clamshell container. This incorrect product in the container resulted in an undeclared allergen on the product label (peanuts).
F-0687-2025 | undeclared allergen ingredient (wheat) on product label for flour Gorditas.
F-0688-2025 | Undeclared allergen (milk).
F-0692-2025 | Label declares tofu but it does not declare soy.
F-0694-2025 | Undeclared Allergen (Soy)
F-0695-2025 | Undeclared Sesame, Soy, Wheat, Yellow No. 5, Yellow No. 6, and Red No. 6.
F-0698-2025 | Undeclared soy flour
F-0699-2025 | Undeclared allergen (milk not listed as sub ingredient of butter). Milk also not listed in 'Contains' statement.
F-0700-2025 | Undeclared allergens (soy, milk) and Yellow #5
F-0702-2025 | Undeclared allergen (eggs) and pork
F-0704-2025 | Undeclared peanuts, soy, sesame, and wheat.
F-0707-2025 | Label declares tahini paste but does not declare sesame.
F-0708-2025 | Undeclared allergen: Soy lecithin, less than 2%
F-0709-2025 | Undeclared allergens: Soy lecithin
F-0710-2025 | Product contains undeclared milk.
F-0719-2025 | Undeclared milk
F-0720-2025 | Undeclared Milk - During an FDA inspection the firm was notified that milk was not declared on the label.
F-0729-2025 | Undeclared allergen: Wheat
F-0732-2025 | Product does not declare the allergen, milk, on the label.
F-0744-2025 | Undeclared Wheat and Soy
F-0747-2025 | Product contains undeclared egg.
F-0748-2025 | Contains undeclared allergens (almonds).
F-0749-2025 | Undeclared allergen (milk)
F-0750-2025 | Undeclared allergen (milk)
F-0751-2025 | Undeclared allergen (milk)
F-0757-2025 | Product mislabeled - product labeled as peanuts, but may contain cashews
F-0761-2025 | Undeclared allergen ingredient (milk)
F-0762-2025 | undeclared milk
F-0763-2025 | Undeclared Almonds
F-0764-2025 | Undeclared Almonds
F-0765-2025 | Undeclared Almonds
F-0766-2025 | Undeclared Almonds
F-0767-2025 | Undeclared Almonds
F-0768-2025 | Undeclared Almonds
F-0769-2025 | Undeclared Almonds
F-0770-2025 | Undeclared Almonds
F-0771-2025 | Undeclared Almonds
F-0772-2025 | Undeclared Almonds
F-0773-2025 | Undeclared Almonds
F-0774-2025 | Undeclared Almonds
F-0801-2025 | Contains undeclared almonds & undeclared sesame
F-0802-2025 | Product contains undeclared wheat.
F-0804-2025 | Undeclared allergen (soy)
F-0806-2025 | Undeclared allergen (soy) due to mislabeling.   Product is labeled as Brown Sugar Molasses Baked Beans, but contains Beef and BBQ Baked Beans. The Beef and BBQ Baked Beans contain soy, which is not declared on the label.
F-0807-2025 | Undeclared milk allergen
F-0808-2025 | Undeclared allergens (milk and/or peanuts).
F-0809-2025 | Undeclared allergens (milk and/or peanuts).
F-0810-2025 | Product contains undeclared almond and cashew.
F-0811-2025 | Undeclared almond and cashew.
F-0813-2025 | Undeclared hazelnut. The Oregon Trail Mix contains visible hazelnut and was mis-labeled as Organic Roasted Salted Cashews, but the label does not declare hazelnut.
F-0823-2025 | Due to printing quality, label does not declare Egg allergen clearly.
F-0824-2025 | Due to printing quality, label does not declare Egg allergen clearly.
F-0825-2025 | Due to printing quality, label does not declare Egg allergen clearly.
F-0826-2025 | Due to printing quality, label does not declare Egg allergen clearly.
F-0827-2025 | Due to printing quality, label does not declare Egg allergen clearly.
F-0828-2025 | Due to printing quality, label does not declare Egg allergen clearly.
F-0829-2025 | Due to printing quality, label does not declare Egg allergen clearly.
F-0830-2025 | Due to printing quality, label does not declare Egg allergen clearly.
F-0831-2025 | Due to printing quality, label does not declare these allergens clearly: Egg, Milk, Soy.
F-0832-2025 | Due to printing quality, label does not declare these allergens clearly: Egg, Milk, Soy.
F-0833-2025 | Due to printing quality, label does not declare these allergens clearly: Egg, Milk, Soy.
F-0834-2025 | Due to printing quality, label does not declare these allergens clearly: Egg, Milk, Soy.
F-0835-2025 | Due to printing quality, label does not declare these allergens clearly: Egg and Milk.
F-0836-2025 | Due to printing quality, label does not declare these allergens clearly: Egg and Milk.
F-0837-2025 | Due to printing quality, label does not declare these allergens clearly: Egg, Milk, Soy.
F-0838-2025 | Due to printing quality, label does not declare these allergens clearly: Egg, Milk, Pecan.
F-0927-2025 | undeclared milk allergen
F-0928-2025 | Undeclared Fish allergen (parvalbumin).
F-0929-2025 | Undeclared sesame
F-0931-2025 | The Instant Milk Tea Powder's ingredients statement declares Non-Dairy Creamer (Whey Powder, Sodium Caseinate) but does not specify milk.
F-0932-2025 | The Instant Milk Tea Powder's ingredients statement declares Non-Dairy Creamer (Whey Powder, Sodium Caseinate) but does not specify milk.
F-0933-2025 | The Instant Milk Tea Powder's ingredients statement declares Non-Dairy Creamer (Whey Powder, Sodium Caseinate) but does not specify milk.
F-0934-2025 | The Instant Milk Tea Powder's ingredients statement declares Non-Dairy Creamer (Whey Powder, Sodium Caseinate) but does not specify milk.
F-0935-2025 | The Instant Milk Tea Powder's ingredients statement declares Non-Dairy Creamer (Whey Powder, Sodium Caseinate) but does not specify milk.
F-0937-2025 | The ingredients statement declares fish sauce but does not declare anchovies. The Contains statement does not declare fish (anchovies).
F-0938-2025 | Undeclared allergens (wheat, sesame)
F-1821-2024 | Soy is in the ingredients but missing from the contains statement.
F-1822-2024 | Products contain undeclared sub ingredient: wheat.
F-1823-2024 | Products contain undeclared sub ingredient: wheat.
F-1824-2024 | Products contain undeclared sub ingredients: wheat and milk
F-1825-2024 | Products contain undeclared sub ingredients: wheat and milk
F-1826-2024 | Products contain undeclared sub ingredients: wheat and milk
F-1827-2024 | Products contain undeclared sub ingredient: wheat.
F-1828-2024 | Products contain undeclared sub ingredient wheat.
F-1829-2024 | Products contain undeclared wheat.
F-1830-2024 | Products contain undeclared sub ingredients: wheat and milk.
F-1831-2024 | Undeclared soy lecithin and soybean oil on label
F-1832-2024 | Undeclared soy lecithin and soybean oil on label
F-1833-2024 | Undeclared allergen (Fish) Ingredient
F-1834-2024 | Undeclared allergen (Fish) Ingredient
F-1835-2024 | Allergen not listed in the Contains statement: Fish
F-1836-2024 | Undeclared walnut and wheat.  Mini Squash Harvest Loaf (UPC 8 55324 00505 3) was mis-labeled as Mini Raspberry Lemon Coffee Cake (UPC 8 57297 00745 4) and therefore wheat flour and walnuts are not declared on label.
H-0008-2025 | Contains undeclared peanut
H-0011-2025 | Undeclared Allergen (walnuts), was not on outer packaging but was on the inner packaging of product.
H-0017-2025 | Undeclared allergens and mislabeled product.  Rocky Road Ice was packaged with Chocolate Truffle Ice Cream labeled tub and a Rocky Road Ice Cream lid. Tub said "may contain tree nuts" the lid said it did contain almonds.
H-0040-2025 | Undeclared soy allergen
H-0043-2025 | Atlantic Salmon Portions with Seafood Stuffing was incorrectly labeled and does not declare allergen ingredient (SOY)
H-0047-2025 | Undeclared Milk Allergen
H-0058-2025 | Undeclared wheat
H-0059-2025 | Undeclared wheat
H-0060-2025 | Undeclared wheat
H-0063-2025 | Undeclared Milk.
H-0065-2025 | Undeclared Sesame. The firm was notified by a retailer that product labeled as Sea Salt Bagel Crackers contained Everything Bagel Crackers. The Everything Bagel Crackers contains sesame which is not listed in the ingredient statement.
H-0066-2025 | Undeclared  Milk
H-0071-2025 | Undeclared wheat allergen
H-0072-2025 | Undeclared milk
H-0073-2025 | Undeclared milk and wheat allergens
H-0074-2025 | Undeclared wheat allergens
H-0075-2025 | Undeclared wheat allergens
H-0076-2025 | Undeclared  wheat allergens
H-0077-2025 | Undeclared wheat allergens
H-0078-2025 | Undeclared wheat allergens
H-0079-2025 | Undeclared wheat allergens
H-0080-2025 | Undeclared wheat allergens
H-0081-2025 | Undeclared wheat allergens
H-0082-2025 | Undeclared sesame and wheat allergens
H-0083-2025 | Undeclared sesame and wheat allergens
H-0084-2025 | Undeclared wheat allergens
H-0085-2025 | Undeclared wheat allergens
H-0086-2025 | Undeclared wheat allergens
H-0087-2025 | Undeclared wheat allergens
H-0115-2025 | Undeclared allergens: Milk, Eggs, Soy Ingredients (Soybean oil, Soy Lecithin), Wheat, Tree Nuts (Almonds, Hazelnuts) on label and incomplete Contains statement
H-0116-2025 | Undeclared allergens: Milk, Eggs, Soy Ingredients (Soybean oil, Soy Lecithin), Wheat, Tree Nuts (Almonds, Hazelnuts) on label and incomplete Contains statement
H-0117-2025 | Undeclared allergens: Milk, Eggs, Soy Ingredients (Soybean oil, Soy Lecithin), Wheat, Tree Nuts (Almonds, Hazelnuts) on label and incomplete Contains statement
H-0118-2025 | Undeclared allergens: Milk, Eggs, Soy Ingredients (Soybean oil, Soy Lecithin), Wheat, Tree Nuts (Almonds, Hazelnuts) on label and incomplete Contains statement
H-0119-2025 | Undeclared allergens: Milk, Eggs, Soy Ingredients (Soybean oil, Soy Lecithin), Wheat, Tree Nuts (Almonds, Hazelnuts) on label and incomplete Contains statement
H-0211-2025 | undeclared cashews
H-0212-2025 | Contains undeclared peanut
H-0213-2025 | Undeclared milk
H-0215-2025 | Undeclared Milk Allergen
H-0216-2025 | Undeclared Milk Allergen
H-0254-2025 | Undeclared soy and wheat
H-0255-2025 | Undeclared wheat
H-0256-2025 | Undeclared soy, contains statement is present but does not list pistachios
H-0257-2025 | Undeclared soy, contains statement is present but does not list pistachios
H-0258-2025 | Undeclared wheat, soy, and sesame
H-0272-2025 | undeclared milk
H-0278-2025 | Undeclared milk
H-0281-2025 | undeclared pecans
H-0282-2025 | undeclared pecans
H-0283-2025 | undeclared pecans
H-0306-2025 | Product does not declare allergen ingredient sesame.
H-0308-2025 | Undeclared allergens - soy and wheat
H-0309-2025 | Undeclared allergen - soy
H-0310-2025 | Undeclared allergens - soy and wheat
H-0311-2025 | Undeclared allergens - soy and wheat
H-0312-2025 | Undeclared allergens - soy and wheat
H-0313-2025 | Undeclared allergen - soy
H-0314-2025 | Undeclared allergen - soy
H-0315-2025 | Undeclared allergen - soy
H-0319-2025 | Undeclared allergen: Hazelnut due to mispackaging. Product with hazelnuts was put in the Artisan Style 1/2 loaf bags. Bags do not have allergen statement that includes hazelnuts.
H-0320-2025 | Label declares Shelled Edamame but does not specify or declare soy.
H-0323-2025 | Undeclared allergens (Peanut) due to mispackaging
H-0324-2025 | Undeclared allergens (Peanut) due to mispackaging
H-0325-2025 | Undeclared allergens (Peanut) due to mispackaging
H-0326-2025 | Undeclared allergens (Peanut) due to mispackaging
H-0331-2025 | Undeclared sesame
H-0332-2025 | Undeclared sesame
H-0333-2025 | Undeclared sesame
H-0334-2025 | Undeclared sesame
H-0335-2025 | Undeclared sesame
H-0336-2025 | Undeclared sesame
H-0347-2025 | Undeclare Tree Nuts (almond, macadamia nut)
H-0348-2025 | Undeclared Milk
H-0349-2025 | Undeclared Allergen (Milk). Consumer found a breaded halloumi Cheese Stick in the bag of churro bites.  The Halloumi Cheese contains milk which is not an allergen in the churros.
H-0354-2025 | allergen labeling - undeclared milk
H-0355-2025 | Undeclared wheat and soy
H-0356-2025 | Undeclared wheat
H-0357-2025 | Undeclared wheat
H-0358-2025 | Undeclared wheat
H-0359-2025 | Undeclared wheat and soy
H-0360-2025 | Undeclared wheat and soy
H-0361-2025 | Undeclared wheat and soy
H-0362-2025 | Undeclared wheat
H-0363-2025 | Undeclared wheat
H-0364-2025 | Undeclared wheat and soy
H-0365-2025 | Undeclared wheat
H-0366-2025 | Undeclared wheat and soy
H-0367-2025 | Undeclared wheat and soy
H-0368-2025 | Undeclared wheat and soy
H-0369-2025 | Undeclared wheat
H-0370-2025 | Undeclared wheat and soy
H-0371-2025 | Undeclared wheat and soy
H-0372-2025 | Undeclared wheat
H-0373-2025 | Undeclared wheat and soy
H-0374-2025 | Undeclared wheat
H-0375-2025 | Undeclared wheat
H-0376-2025 | Undeclared wheat and soy
H-0377-2025 | Undeclared wheat and soy
H-0378-2025 | Undeclared wheat
H-0392-2025 | Allergen not listed in the Contains statement: Sesame
H-0393-2025 | Allergen not listed in the Contains statement: Sesame
H-0453-2025 | Various snack cracker products are mislabeled and do not declare all allergen ingredients (Whole Milk Powder and wheat).
H-0454-2025 | Various snack cracker products are mislabeled and do not declare all allergen ingredients (Whole Milk Powder and wheat).
H-0455-2025 | Various snack cracker products are mislabeled and do not declare all allergen ingredients (Whole Milk Powder and wheat).
H-0456-2025 | Undeclared sesame.
H-0458-2025 | Product label includes the ingredient CREAM but does not include Milk as the source.
H-0459-2025 | Product label includes the ingredient CREAM but does not include Milk as the source.
H-0460-2025 | Product label includes the ingredient CREAM but does not include Milk as the source.
H-0461-2025 | Product label includes the ingredient CREAM but does not include Milk as the source.
H-0462-2025 | Product label includes the ingredient CREAM but does not include Milk as the source.
H-0463-2025 | Product label includes the ingredient CREAM but does not include Milk as the source.
H-0464-2025 | Product label includes the ingredient CREAM but does not include Milk as the source.
H-0465-2025 | Product label includes the ingredient CREAM but does not include Milk as the source.
H-0466-2025 | Product label includes the ingredient CREAM but does not include Milk as the source.
H-0467-2025 | Product label includes the ingredient CREAM but does not include Milk as the source.
H-0468-2025 | Product label includes the ingredient CREAM but does not include Milk as the source.
H-0469-2025 | Product label includes the ingredient CREAM but does not include Milk as the source.
H-0470-2025 | Product label includes the ingredient CREAM but does not include Milk as the source.
H-0471-2025 | Product label includes the ingredient CREAM but does not include Milk as the source.
H-0487-2025 | Undeclared milk from Contains statement.
H-0488-2025 | Undeclared milk and soy (from soy lecithin) from sub-ingredients.
H-0489-2025 | Undeclared milk and/or eggs from sub-ingredients and/or Contains statement.
H-0490-2025 | Undeclared wheat and milk from sub-ingredients.
H-0491-2025 | Undeclared wheat, milk, and soy (from soy lecithin) from sub-ingredients.
H-0502-2025 | Ramen Noodle package label does not declare Soy as the source for lecithin ingredient.
H-0503-2025 | Ramen Noodle package label does not declare Soy as the source for lecithin ingredient.
H-0505-2025 | Product contains undeclared soy lecithin.
H-0506-2025 | Undeclared egg.
H-0507-2025 | Undeclared egg.
H-0508-2025 | Undeclared egg.
H-0509-2025 | Undeclared egg.
H-0510-2025 | Undeclared egg.
H-0511-2025 | Undeclared egg.
H-0512-2025 | Undeclared egg.
H-0513-2025 | Undeclared egg.
H-0514-2025 | Undeclared egg.
H-0515-2025 | Undeclared egg.
H-0516-2025 | Undeclared egg.
H-0517-2025 | Undeclared egg.
H-0518-2025 | Undeclared egg.
H-0519-2025 | Undeclared egg.
H-0522-2025 | Undeclared eggs
H-0531-2025 | Finished product label does not include allergen ingredient Sesame Seed.
H-0533-2025 | Product label does not list ingredients including major food allergen: sesame.   Additional undeclared ingredients include: millet and flax
H-0534-2025 | Product label does not list ingredients including major food allergen: sesame.   Additional undeclared ingredients include: poppy seeds, dried garlic, dried onion, and sea salt
H-0535-2025 | Product label does not list ingredients including major food allergens: wheat and soy (vegetable oil).  Additional undeclared ingredients include: niacin, reduced iron, vitamin B1, vitamin B2, invert sugar
H-0537-2025 | Product contains undeclared wheat and soy.
H-0546-2025 | undeclared almond, walnut, and pecan.
H-0550-2025 | Undeclared wheat allergen.
H-0558-2025 | Contains undeclared wheat. The top label identifies the product as potato salad, but the unit contains pasta salad.
H-0559-2025 | Allergen labeling: egg is not listed in the 'contains' statement
H-0560-2025 | Allergen labeling: specific tree nut (walnut) and egg are not listed in the 'contains' statement
H-0561-2025 | Allergen labeling: egg is not listed in the 'contains' statement
H-0562-2025 | Allergen labeling: specific tree nut (pecan) and egg are not listed in the 'contains' statement
H-0563-2025 | Allergen labeling: egg not listed in the 'contains' statement
H-0564-2025 | Allergen labeling: specific tree nut (pecan) and egg not listed in 'contains' statement
H-0565-2025 | Allergen labeling: specific tree nut (pecans) not listed in the 'contains' statement
H-0566-2025 | Allergen labeling: missing allergens (peanuts, milk) in contains statement
H-0567-2025 | Allergen labeling: specific tree nut (pecan) not listed in 'contains' statement
H-0578-2025 | Undeclared soy allergen
H-0580-2025 | Undeclared allergen (peanut, pecan).
H-0581-2025 | Undeclared allergen (peanut, pecan).
H-0582-2025 | Product contains undeclared wheat.
H-0602-2025 | Review of Label determined allergen was listed as unsalted butter/ heavy cream. In one instance of identified label, there was no milk or dairy listed listed in Contains statement. Further review of label revealed "soy" had been removed.
H-0605-2025 | Product contains undeclared Soy and Sesame
H-0612-2025 | undeclared allergen (Wheat and Milk) on ready to eat sandwiches.
H-0613-2025 | undeclared allergen (Wheat and Milk) on ready to eat sandwiches.
H-0614-2025 | undeclared allergen (Wheat and Milk) on ready to eat sandwiches.
H-0615-2025 | undeclared allergen (Wheat) on ready to eat sandwiches.
H-0616-2025 | Undeclared allergens (sesame and soy).
H-0635-2025 | May contained undeclared almond
```

### PULL 2 — every request (UTC, Date header, meta verbatim)

- Request: GET https://api.fda.gov/food/enforcement.json?search=report_date%3A%5B20241001+TO+20250930%5D&limit=1000&skip=0
  - Retrieved (UTC): 2026-11-11T07:49:07Z · HTTP 200
  - Date: Wed, 11 Nov 2026 07:49:07 GMT
  - meta object verbatim:
```json
{
  "disclaimer": "Do not rely on openFDA to make decisions regarding medical care. While we make every effort to ensure that data is accurate, you should assume all results are unvalidated. We may limit or otherwise restrict your access to the API in line with our Terms of Service.",
  "terms": "https://open.fda.gov/terms/",
  "license": "https://open.fda.gov/license/",
  "last_updated": "2026-11-04",
  "results": {
    "skip": 0,
    "limit": 1000,
    "total": 1564
  }
}
```
- Request: GET https://api.fda.gov/food/enforcement.json?search=report_date%3A%5B20241001+TO+20250930%5D&limit=1000&skip=1000
  - Retrieved (UTC): 2026-11-11T07:49:08Z · HTTP 200
  - Date: Wed, 11 Nov 2026 07:49:08 GMT
  - meta object verbatim:
```json
{
  "disclaimer": "Do not rely on openFDA to make decisions regarding medical care. While we make every effort to ensure that data is accurate, you should assume all results are unvalidated. We may limit or otherwise restrict your access to the API in line with our Terms of Service.",
  "terms": "https://open.fda.gov/terms/",
  "license": "https://open.fda.gov/license/",
  "last_updated": "2026-11-04",
  "results": {
    "skip": 1000,
    "limit": 1000,
    "total": 1564
  }
}
```

### PULL 2 — reason_for_recall of every kept record

```text
F-0001-2025 | Undeclared wheat. The firm was notified by their supplier that they failed to include the allergen "wheat" on the label.
F-0002-2025 | Undeclared wheat. The firm was notified by their supplier that they failed to include the allergen "wheat" on the label.
F-0003-2025 | Undeclared wheat. The firm was notified by their supplier that they failed to include the allergen "wheat" on the label.
F-0014-2025 | Undeclared whey (milk), wheat flour, almonds; no contains statement & no nutrition fact panel
F-0015-2025 | Undeclared whey (milk) & wheat flour: no nutrition fact panel & no contains statement
F-0016-2025 | Undeclared whey (milk), wheat flour, & bran (wheat); no nutrition fact panel & no contains statement
F-0017-2025 | Undeclared whey (milk) & wheat flour; no nutrition fact panel & no contains statement
F-0018-2025 | Undeclared whey (milk) & wheat flour: no nutrition fact panel & no contains statement
F-0019-2025 | Undeclared whey (milk) & wheat flour; no nutrition fact panel & no contains statement
F-0020-2025 | Undeclared whey (milk) and wheat flour; no nutritional fact panel & no contains statement
F-0021-2025 | Undeclared whey (milk), wheat flour, & coconut; no nutrition fact panel & no contains statement
F-0022-2025 | Undeclared whey (milk) & wheat flour; no nutrition fact panel & no contains statement
F-0023-2025 | Undeclared allergens; walnuts
F-0035-2025 | Undeclared allergens; milk
F-0036-2025 | Undeclared allergens; milk
F-0037-2025 | Undeclared Allergen, milk - a mix-up between the product description and the ingredient list. Milk Chocolate was listed in the product description but was missing from the ingredient list.
F-0038-2025 | Mayonnaise is declared but Soybean Oil and Egg are not declared.
F-0039-2025 | Soybean Paste is declared but Wheat and Sesame Seeds are not declared.
F-0041-2025 | Soybean Sauce is declared but Wheat and Fish (Anchovy) are not declared.
F-0042-2025 | Soybean Sauce is declared but Wheat is not declared.
F-0043-2025 | Undeclared Crustacean (shrimp).
F-0044-2025 | Undeclared Fish (Anchovy).
F-0045-2025 | Soybean Sauce is declared but Wheat and Fish (Anchovy) are not declared.
F-0046-2025 | Undeclared Fish (Anchovy).
F-0047-2025 | Soy Sauce is declared but Wheat is not declared.
F-0048-2025 | Soy Bean Paste is declared but Wheat, Fish (Large-eyed Herring, Anchovy), and Crustacean (Shrimp) are not declared.
F-0049-2025 | Soy Sauce is declare but Wheat and Fish (Anchovy) are not declared.
F-0050-2025 | Soy Sauce is declared but Wheat is not declared.
F-0054-2025 | Milk may contain undeclared almond from almond milk
F-0057-2025 | Undeclared Wheat flour. Product contains wheat flour but product was sold without the Ingredients Statement.
F-0067-2025 | Undeclared Almonds & Cashews. The firm was notified by their customers that the product contains a trail mix instead of the cheese mix. The trail mix contains almonds and cashews that are not listed in the ingredient statement.
F-0068-2025 | Undeclared Fish Allergen
F-0077-2025 | Undeclared allergen:Wheat
F-0097-2025 | Undeclared allergens; wheat, soy, and eggs.
F-0098-2025 | Undeclared allergen: milk
F-0099-2025 | Undeclared sesame
F-0100-2025 | Undeclared sesame
F-0101-2025 | Undeclared sesame
F-0102-2025 | Undeclared sesame
F-0103-2025 | Undeclared sesame
F-0104-2025 | Undeclared sesame
F-0105-2025 | Undeclared sesame
F-0120-2025 | Undeclared allergens; sesame
F-0121-2025 | Butter lists cream, but may be missing the Contains Milk statement.
F-0122-2025 | Butter lists cream, but may be missing the Contains Milk statement.
F-0126-2025 | The product is being recalled due to an undeclared allergen - tree nuts (walnuts).
F-0132-2025 | Undeclared wheat. Product contains wheat but was mis-labeled as Savory 6 Cut Crinkle Cut Wedge and label does not declare wheat.
F-0147-2025 | Product contains undeclared hydrolyzed soy protein.
F-0148-2025 | Undeclared egg
F-0216-2025 | Undeclared tree nuts (almonds)
F-0217-2025 | Undeclared egg
F-0218-2025 | Undeclared egg
F-0219-2025 | Undeclared egg
F-0220-2025 | Undeclared egg
F-0244-2025 | Undeclared eggs and yellow #5.
F-0245-2025 | Contains undeclared egg
F-0253-2025 | Undeclared allergen - egg
F-0259-2025 | Undeclared Wheat. The firm was notified by a consumer that they found crispy onions in the packaging of the tortilla strips. The onions contain wheat which is not listed on the packaging for the tortilla strips.
F-0260-2025 | Undeclared Allergen - Wheat and Soy
F-0262-2025 | Product contains undeclared soy lecithin.
F-0263-2025 | Contains undeclared soy lecithin
F-0266-2025 | Undeclared soy (soy lecithin).
F-0293-2025 | Undeclared allergen labeling (milk)
F-0294-2025 | Undeclared allergen labeling (milk)
F-0295-2025 | Undeclared allergen labeling (milk)
F-0296-2025 | Undeclared allergen labeling (milk)
F-0297-2025 | Undeclared allergen labeling (milk)
F-0299-2025 | Undeclared allergens: Milk, Soy, Crustacea Shellfish, Fish
F-0317-2025 | Product contains undeclared fish (anchovy) and soy.
F-0319-2025 | Products contain undeclared allergens (milk, soy, and wheat) and undeclared sulfites, yellow 5, yellow 6.
F-0320-2025 | Products contain undeclared allergens (milk, soy, peanut, and wheat) and undeclared sulfites, yellow 5, yellow 6, and red 40)
F-0321-2025 | The contains statement does not declare sesame. Black sesame seeds are visible on product and the Ingredients Statement declares black sesame seeds.
F-0376-2025 | Product contains Undeclared Allergen Tree Nuts (Cashews)
F-0384-2025 | Undeclared egg allergen
F-0386-2025 | Potential contamination of undeclared allergen peanuts
F-0402-2025 | Undeclared allergens (Wheat and Soy)
F-0404-2025 | Product does not include statement: Contains milk
F-0409-2025 | Undeclared milk
F-0411-2025 | Undeclared milk
F-0412-2025 | Undeclared wheat, Undeclared soybean oil
F-0413-2025 | Undeclared wheat, Undeclared soybean oil
F-0414-2025 | Undeclared milk
F-0415-2025 | Undeclared milk
F-0416-2025 | Undeclared milk
F-0417-2025 | Undeclared almonds
F-0418-2025 | Undeclared milk
F-0419-2025 | Undeclared milk
F-0421-2025 | Product contains undeclared milk and soy.
F-0422-2025 | Undeclared Milk. During an FDA investigation the manufacturer was notified that the label does not list the allergen milk in the ingredient statement.
F-0428-2025 | Undeclared Milk Allergen
F-0431-2025 | Frozen Peach Mango Sorbet contains undeclared allergen (egg)
F-0433-2025 | Soy is missing from the "Contains" statement.
F-0458-2025 | Barbeque sauce product contains undeclared allergens (soy) contained in sub-ingredient
F-0459-2025 | Barbeque sauce product contains undeclared allergen listing of (Milk) in product ingredient listing from sub-ingredient Butter.
F-0460-2025 | Barbeque sauce product contains undeclared listing of (Milk) in product ingredient listing from sub-ingredient Butter.
F-0461-2025 | The product is being recalled because of undeclared milk .
F-0462-2025 | The product is being recalled because of undeclared milk .
F-0463-2025 | The product is being recalled because of undeclared milk .
F-0464-2025 | Undeclared milk
F-0465-2025 | Undeclared walnuts
F-0466-2025 | Undeclared Milk. During the firm's reordering process of labels, they discovered that the label does not list milk in its ingredient or contain statement.
F-0467-2025 | Undeclared Milk. During the firm's reordering process of labels, they discovered that the label does not list milk in its ingredient or contain statement.
F-0469-2025 | Undeclared allergens (wheat) on label, incorrect label was placed on product
F-0531-2025 | Contains undeclared visible almonds
F-0532-2025 | Firm distributed a Bread Crumb product with undeclared allergen (Sesame) not on the label.
F-0533-2025 | Firm distributed a Seasoned Bread Crumb product with undeclared allergen (Sesame) not on the label.
F-0534-2025 | Imported Monkfish Liver undeclared allergen (Milk)
F-0548-2025 | Undeclared allergen (Milk) in Shirakiku brand Curvee Puffs Corn Puff Snack
F-0549-2025 | Undeclared allergen (Milk) in Shirakiku brand Curvee Puffs Corn Puff Snack
F-0550-2025 | Undeclared allergen (Milk) in Shirakiku brand Curvee Puffs Corn Puff Snack
F-0552-2025 | Undeclared Allergen - Milk
F-0553-2025 | Undeclared milk allergen
F-0570-2025 | Undeclared allergen (soy).
F-0572-2025 | Product may contain egg, an undeclared allergen.
F-0573-2025 | Potato flour item #20501 was recalled due to undeclared milk (between 13ppm and 17ppm).
F-0577-2025 | Mislabeled salads (undeclared peanut allergen). Incorrect ingredient applied (peanuts)
F-0581-2025 | Undeclared milk
F-0582-2025 | Undeclared milk
F-0583-2025 | Undeclared milk
F-0604-2025 | Undeclared Milk.
F-0605-2025 | Undeclared Milk.
F-0606-2025 | Undeclared egg.
F-0607-2025 | Undeclared egg.
F-0608-2025 | Undeclared allergen (walnuts)
F-0624-2025 | Milk not listed in the ingredients or included in parentheses after American Cheese.
F-0630-2025 | Milk not declared as the major food allergen source for the ingredient Whey
F-0631-2025 | Undeclared egg
F-0632-2025 | Milk not listed in Contains statement
F-0633-2025 | Undeclared wheat and egg
F-0634-2025 | Egg not listed in Contains statement
F-0635-2025 | Wheat not listed in Contains statement
F-0636-2025 | Undeclared almonds
F-0637-2025 | Product may contain incorrect salad dressing, resulting in fish and wheat being undeclared.
F-0638-2025 | Incorrect back label on product resulting in undeclared allergens (wheat, eggs)
F-0639-2025 | Contains undeclared milk
F-0649-2025 | Undeclared soy lecithin and undeclared color additives Blue 1 Lake, Yellow 6, Red 40, Yellow 5, Blue 1, Yellow 6 Lake, Red 40 Lake, Yellow 5 Lake, Blue 2 Lake, Blue 2.
F-0663-2025 | Contains undeclared egg
F-0667-2025 | Undeclared Pecan. The firm was notified by their customer that when they were placing the product on the shelves, they noticed the wrong product was in the container.
F-0669-2025 | Undeclared Allergen (Milk)
F-0672-2025 | (Imported) Hot Pot Sauce contains undeclared allergens (Wheat and Soy)
F-0673-2025 | (Imported) Hot Pot Sauce (SPICY) contains undeclared allergens (Wheat and Soy)
F-0674-2025 | Finished product label fails to include Milk in ingredient listing. (Undeclared Allergen)
F-0686-2025 | Turkey BLT on Sourdough Sandwiches being recalled due to the product having the incorrect sandwich (Peanut Butter & Jelly) in the clamshell container. This incorrect product in the container resulted in an undeclared allergen on the product label (peanuts).
F-0687-2025 | undeclared allergen ingredient (wheat) on product label for flour Gorditas.
F-0688-2025 | Undeclared allergen (milk).
F-0692-2025 | Label declares tofu but it does not declare soy.
F-0694-2025 | Undeclared Allergen (Soy)
F-0695-2025 | Undeclared Sesame, Soy, Wheat, Yellow No. 5, Yellow No. 6, and Red No. 6.
F-0698-2025 | Undeclared soy flour
F-0699-2025 | Undeclared allergen (milk not listed as sub ingredient of butter). Milk also not listed in 'Contains' statement.
F-0700-2025 | Undeclared allergens (soy, milk) and Yellow #5
F-0702-2025 | Undeclared allergen (eggs) and pork
F-0704-2025 | Undeclared peanuts, soy, sesame, and wheat.
F-0707-2025 | Label declares tahini paste but does not declare sesame.
F-0708-2025 | Undeclared allergen: Soy lecithin, less than 2%
F-0709-2025 | Undeclared allergens: Soy lecithin
F-0710-2025 | Product contains undeclared milk.
F-0719-2025 | Undeclared milk
F-0720-2025 | Undeclared Milk - During an FDA inspection the firm was notified that milk was not declared on the label.
F-0729-2025 | Undeclared allergen: Wheat
F-0732-2025 | Product does not declare the allergen, milk, on the label.
F-0744-2025 | Undeclared Wheat and Soy
F-0747-2025 | Product contains undeclared egg.
F-0748-2025 | Contains undeclared allergens (almonds).
F-0749-2025 | Undeclared allergen (milk)
F-0750-2025 | Undeclared allergen (milk)
F-0751-2025 | Undeclared allergen (milk)
F-0757-2025 | Product mislabeled - product labeled as peanuts, but may contain cashews
F-0761-2025 | Undeclared allergen ingredient (milk)
F-0762-2025 | undeclared milk
F-0763-2025 | Undeclared Almonds
F-0764-2025 | Undeclared Almonds
F-0765-2025 | Undeclared Almonds
F-0766-2025 | Undeclared Almonds
F-0767-2025 | Undeclared Almonds
F-0768-2025 | Undeclared Almonds
F-0769-2025 | Undeclared Almonds
F-0770-2025 | Undeclared Almonds
F-0771-2025 | Undeclared Almonds
F-0772-2025 | Undeclared Almonds
F-0773-2025 | Undeclared Almonds
F-0774-2025 | Undeclared Almonds
F-0801-2025 | Contains undeclared almonds & undeclared sesame
F-0802-2025 | Product contains undeclared wheat.
F-0804-2025 | Undeclared allergen (soy)
F-0806-2025 | Undeclared allergen (soy) due to mislabeling.   Product is labeled as Brown Sugar Molasses Baked Beans, but contains Beef and BBQ Baked Beans. The Beef and BBQ Baked Beans contain soy, which is not declared on the label.
F-0807-2025 | Undeclared milk allergen
F-0808-2025 | Undeclared allergens (milk and/or peanuts).
F-0809-2025 | Undeclared allergens (milk and/or peanuts).
F-0810-2025 | Product contains undeclared almond and cashew.
F-0811-2025 | Undeclared almond and cashew.
F-0813-2025 | Undeclared hazelnut. The Oregon Trail Mix contains visible hazelnut and was mis-labeled as Organic Roasted Salted Cashews, but the label does not declare hazelnut.
F-0823-2025 | Due to printing quality, label does not declare Egg allergen clearly.
F-0824-2025 | Due to printing quality, label does not declare Egg allergen clearly.
F-0825-2025 | Due to printing quality, label does not declare Egg allergen clearly.
F-0826-2025 | Due to printing quality, label does not declare Egg allergen clearly.
F-0827-2025 | Due to printing quality, label does not declare Egg allergen clearly.
F-0828-2025 | Due to printing quality, label does not declare Egg allergen clearly.
F-0829-2025 | Due to printing quality, label does not declare Egg allergen clearly.
F-0830-2025 | Due to printing quality, label does not declare Egg allergen clearly.
F-0831-2025 | Due to printing quality, label does not declare these allergens clearly: Egg, Milk, Soy.
F-0832-2025 | Due to printing quality, label does not declare these allergens clearly: Egg, Milk, Soy.
F-0833-2025 | Due to printing quality, label does not declare these allergens clearly: Egg, Milk, Soy.
F-0834-2025 | Due to printing quality, label does not declare these allergens clearly: Egg, Milk, Soy.
F-0835-2025 | Due to printing quality, label does not declare these allergens clearly: Egg and Milk.
F-0836-2025 | Due to printing quality, label does not declare these allergens clearly: Egg and Milk.
F-0837-2025 | Due to printing quality, label does not declare these allergens clearly: Egg, Milk, Soy.
F-0838-2025 | Due to printing quality, label does not declare these allergens clearly: Egg, Milk, Pecan.
F-0927-2025 | undeclared milk allergen
F-0928-2025 | Undeclared Fish allergen (parvalbumin).
F-0929-2025 | Undeclared sesame
F-0931-2025 | The Instant Milk Tea Powder's ingredients statement declares Non-Dairy Creamer (Whey Powder, Sodium Caseinate) but does not specify milk.
F-0932-2025 | The Instant Milk Tea Powder's ingredients statement declares Non-Dairy Creamer (Whey Powder, Sodium Caseinate) but does not specify milk.
F-0933-2025 | The Instant Milk Tea Powder's ingredients statement declares Non-Dairy Creamer (Whey Powder, Sodium Caseinate) but does not specify milk.
F-0934-2025 | The Instant Milk Tea Powder's ingredients statement declares Non-Dairy Creamer (Whey Powder, Sodium Caseinate) but does not specify milk.
F-0935-2025 | The Instant Milk Tea Powder's ingredients statement declares Non-Dairy Creamer (Whey Powder, Sodium Caseinate) but does not specify milk.
F-0937-2025 | The ingredients statement declares fish sauce but does not declare anchovies. The Contains statement does not declare fish (anchovies).
F-0938-2025 | Undeclared allergens (wheat, sesame)
F-1821-2024 | Soy is in the ingredients but missing from the contains statement.
F-1822-2024 | Products contain undeclared sub ingredient: wheat.
F-1823-2024 | Products contain undeclared sub ingredient: wheat.
F-1824-2024 | Products contain undeclared sub ingredients: wheat and milk
F-1825-2024 | Products contain undeclared sub ingredients: wheat and milk
F-1826-2024 | Products contain undeclared sub ingredients: wheat and milk
F-1827-2024 | Products contain undeclared sub ingredient: wheat.
F-1828-2024 | Products contain undeclared sub ingredient wheat.
F-1829-2024 | Products contain undeclared wheat.
F-1830-2024 | Products contain undeclared sub ingredients: wheat and milk.
F-1831-2024 | Undeclared soy lecithin and soybean oil on label
F-1832-2024 | Undeclared soy lecithin and soybean oil on label
F-1833-2024 | Undeclared allergen (Fish) Ingredient
F-1834-2024 | Undeclared allergen (Fish) Ingredient
F-1835-2024 | Allergen not listed in the Contains statement: Fish
F-1836-2024 | Undeclared walnut and wheat.  Mini Squash Harvest Loaf (UPC 8 55324 00505 3) was mis-labeled as Mini Raspberry Lemon Coffee Cake (UPC 8 57297 00745 4) and therefore wheat flour and walnuts are not declared on label.
H-0008-2025 | Contains undeclared peanut
H-0011-2025 | Undeclared Allergen (walnuts), was not on outer packaging but was on the inner packaging of product.
H-0017-2025 | Undeclared allergens and mislabeled product.  Rocky Road Ice was packaged with Chocolate Truffle Ice Cream labeled tub and a Rocky Road Ice Cream lid. Tub said "may contain tree nuts" the lid said it did contain almonds.
H-0040-2025 | Undeclared soy allergen
H-0043-2025 | Atlantic Salmon Portions with Seafood Stuffing was incorrectly labeled and does not declare allergen ingredient (SOY)
H-0047-2025 | Undeclared Milk Allergen
H-0058-2025 | Undeclared wheat
H-0059-2025 | Undeclared wheat
H-0060-2025 | Undeclared wheat
H-0063-2025 | Undeclared Milk.
H-0065-2025 | Undeclared Sesame. The firm was notified by a retailer that product labeled as Sea Salt Bagel Crackers contained Everything Bagel Crackers. The Everything Bagel Crackers contains sesame which is not listed in the ingredient statement.
H-0066-2025 | Undeclared  Milk
H-0071-2025 | Undeclared wheat allergen
H-0072-2025 | Undeclared milk
H-0073-2025 | Undeclared milk and wheat allergens
H-0074-2025 | Undeclared wheat allergens
H-0075-2025 | Undeclared wheat allergens
H-0076-2025 | Undeclared  wheat allergens
H-0077-2025 | Undeclared wheat allergens
H-0078-2025 | Undeclared wheat allergens
H-0079-2025 | Undeclared wheat allergens
H-0080-2025 | Undeclared wheat allergens
H-0081-2025 | Undeclared wheat allergens
H-0082-2025 | Undeclared sesame and wheat allergens
H-0083-2025 | Undeclared sesame and wheat allergens
H-0084-2025 | Undeclared wheat allergens
H-0085-2025 | Undeclared wheat allergens
H-0086-2025 | Undeclared wheat allergens
H-0087-2025 | Undeclared wheat allergens
H-0115-2025 | Undeclared allergens: Milk, Eggs, Soy Ingredients (Soybean oil, Soy Lecithin), Wheat, Tree Nuts (Almonds, Hazelnuts) on label and incomplete Contains statement
H-0116-2025 | Undeclared allergens: Milk, Eggs, Soy Ingredients (Soybean oil, Soy Lecithin), Wheat, Tree Nuts (Almonds, Hazelnuts) on label and incomplete Contains statement
H-0117-2025 | Undeclared allergens: Milk, Eggs, Soy Ingredients (Soybean oil, Soy Lecithin), Wheat, Tree Nuts (Almonds, Hazelnuts) on label and incomplete Contains statement
H-0118-2025 | Undeclared allergens: Milk, Eggs, Soy Ingredients (Soybean oil, Soy Lecithin), Wheat, Tree Nuts (Almonds, Hazelnuts) on label and incomplete Contains statement
H-0119-2025 | Undeclared allergens: Milk, Eggs, Soy Ingredients (Soybean oil, Soy Lecithin), Wheat, Tree Nuts (Almonds, Hazelnuts) on label and incomplete Contains statement
H-0211-2025 | undeclared cashews
H-0212-2025 | Contains undeclared peanut
H-0213-2025 | Undeclared milk
H-0215-2025 | Undeclared Milk Allergen
H-0216-2025 | Undeclared Milk Allergen
H-0254-2025 | Undeclared soy and wheat
H-0255-2025 | Undeclared wheat
H-0256-2025 | Undeclared soy, contains statement is present but does not list pistachios
H-0257-2025 | Undeclared soy, contains statement is present but does not list pistachios
H-0258-2025 | Undeclared wheat, soy, and sesame
H-0272-2025 | undeclared milk
H-0278-2025 | Undeclared milk
H-0281-2025 | undeclared pecans
H-0282-2025 | undeclared pecans
H-0283-2025 | undeclared pecans
H-0306-2025 | Product does not declare allergen ingredient sesame.
H-0308-2025 | Undeclared allergens - soy and wheat
H-0309-2025 | Undeclared allergen - soy
H-0310-2025 | Undeclared allergens - soy and wheat
H-0311-2025 | Undeclared allergens - soy and wheat
H-0312-2025 | Undeclared allergens - soy and wheat
H-0313-2025 | Undeclared allergen - soy
H-0314-2025 | Undeclared allergen - soy
H-0315-2025 | Undeclared allergen - soy
H-0319-2025 | Undeclared allergen: Hazelnut due to mispackaging. Product with hazelnuts was put in the Artisan Style 1/2 loaf bags. Bags do not have allergen statement that includes hazelnuts.
H-0320-2025 | Label declares Shelled Edamame but does not specify or declare soy.
H-0323-2025 | Undeclared allergens (Peanut) due to mispackaging
H-0324-2025 | Undeclared allergens (Peanut) due to mispackaging
H-0325-2025 | Undeclared allergens (Peanut) due to mispackaging
H-0326-2025 | Undeclared allergens (Peanut) due to mispackaging
H-0331-2025 | Undeclared sesame
H-0332-2025 | Undeclared sesame
H-0333-2025 | Undeclared sesame
H-0334-2025 | Undeclared sesame
H-0335-2025 | Undeclared sesame
H-0336-2025 | Undeclared sesame
H-0347-2025 | Undeclare Tree Nuts (almond, macadamia nut)
H-0348-2025 | Undeclared Milk
H-0349-2025 | Undeclared Allergen (Milk). Consumer found a breaded halloumi Cheese Stick in the bag of churro bites.  The Halloumi Cheese contains milk which is not an allergen in the churros.
H-0354-2025 | allergen labeling - undeclared milk
H-0355-2025 | Undeclared wheat and soy
H-0356-2025 | Undeclared wheat
H-0357-2025 | Undeclared wheat
H-0358-2025 | Undeclared wheat
H-0359-2025 | Undeclared wheat and soy
H-0360-2025 | Undeclared wheat and soy
H-0361-2025 | Undeclared wheat and soy
H-0362-2025 | Undeclared wheat
H-0363-2025 | Undeclared wheat
H-0364-2025 | Undeclared wheat and soy
H-0365-2025 | Undeclared wheat
H-0366-2025 | Undeclared wheat and soy
H-0367-2025 | Undeclared wheat and soy
H-0368-2025 | Undeclared wheat and soy
H-0369-2025 | Undeclared wheat
H-0370-2025 | Undeclared wheat and soy
H-0371-2025 | Undeclared wheat and soy
H-0372-2025 | Undeclared wheat
H-0373-2025 | Undeclared wheat and soy
H-0374-2025 | Undeclared wheat
H-0375-2025 | Undeclared wheat
H-0376-2025 | Undeclared wheat and soy
H-0377-2025 | Undeclared wheat and soy
H-0378-2025 | Undeclared wheat
H-0392-2025 | Allergen not listed in the Contains statement: Sesame
H-0393-2025 | Allergen not listed in the Contains statement: Sesame
H-0453-2025 | Various snack cracker products are mislabeled and do not declare all allergen ingredients (Whole Milk Powder and wheat).
H-0454-2025 | Various snack cracker products are mislabeled and do not declare all allergen ingredients (Whole Milk Powder and wheat).
H-0455-2025 | Various snack cracker products are mislabeled and do not declare all allergen ingredients (Whole Milk Powder and wheat).
H-0456-2025 | Undeclared sesame.
H-0458-2025 | Product label includes the ingredient CREAM but does not include Milk as the source.
H-0459-2025 | Product label includes the ingredient CREAM but does not include Milk as the source.
H-0460-2025 | Product label includes the ingredient CREAM but does not include Milk as the source.
H-0461-2025 | Product label includes the ingredient CREAM but does not include Milk as the source.
H-0462-2025 | Product label includes the ingredient CREAM but does not include Milk as the source.
H-0463-2025 | Product label includes the ingredient CREAM but does not include Milk as the source.
H-0464-2025 | Product label includes the ingredient CREAM but does not include Milk as the source.
H-0465-2025 | Product label includes the ingredient CREAM but does not include Milk as the source.
H-0466-2025 | Product label includes the ingredient CREAM but does not include Milk as the source.
H-0467-2025 | Product label includes the ingredient CREAM but does not include Milk as the source.
H-0468-2025 | Product label includes the ingredient CREAM but does not include Milk as the source.
H-0469-2025 | Product label includes the ingredient CREAM but does not include Milk as the source.
H-0470-2025 | Product label includes the ingredient CREAM but does not include Milk as the source.
H-0471-2025 | Product label includes the ingredient CREAM but does not include Milk as the source.
H-0487-2025 | Undeclared milk from Contains statement.
H-0488-2025 | Undeclared milk and soy (from soy lecithin) from sub-ingredients.
H-0489-2025 | Undeclared milk and/or eggs from sub-ingredients and/or Contains statement.
H-0490-2025 | Undeclared wheat and milk from sub-ingredients.
H-0491-2025 | Undeclared wheat, milk, and soy (from soy lecithin) from sub-ingredients.
H-0502-2025 | Ramen Noodle package label does not declare Soy as the source for lecithin ingredient.
H-0503-2025 | Ramen Noodle package label does not declare Soy as the source for lecithin ingredient.
H-0505-2025 | Product contains undeclared soy lecithin.
H-0506-2025 | Undeclared egg.
H-0507-2025 | Undeclared egg.
H-0508-2025 | Undeclared egg.
H-0509-2025 | Undeclared egg.
H-0510-2025 | Undeclared egg.
H-0511-2025 | Undeclared egg.
H-0512-2025 | Undeclared egg.
H-0513-2025 | Undeclared egg.
H-0514-2025 | Undeclared egg.
H-0515-2025 | Undeclared egg.
H-0516-2025 | Undeclared egg.
H-0517-2025 | Undeclared egg.
H-0518-2025 | Undeclared egg.
H-0519-2025 | Undeclared egg.
H-0522-2025 | Undeclared eggs
H-0531-2025 | Finished product label does not include allergen ingredient Sesame Seed.
H-0533-2025 | Product label does not list ingredients including major food allergen: sesame.   Additional undeclared ingredients include: millet and flax
H-0534-2025 | Product label does not list ingredients including major food allergen: sesame.   Additional undeclared ingredients include: poppy seeds, dried garlic, dried onion, and sea salt
H-0535-2025 | Product label does not list ingredients including major food allergens: wheat and soy (vegetable oil).  Additional undeclared ingredients include: niacin, reduced iron, vitamin B1, vitamin B2, invert sugar
H-0537-2025 | Product contains undeclared wheat and soy.
H-0546-2025 | undeclared almond, walnut, and pecan.
H-0550-2025 | Undeclared wheat allergen.
H-0558-2025 | Contains undeclared wheat. The top label identifies the product as potato salad, but the unit contains pasta salad.
H-0559-2025 | Allergen labeling: egg is not listed in the 'contains' statement
H-0560-2025 | Allergen labeling: specific tree nut (walnut) and egg are not listed in the 'contains' statement
H-0561-2025 | Allergen labeling: egg is not listed in the 'contains' statement
H-0562-2025 | Allergen labeling: specific tree nut (pecan) and egg are not listed in the 'contains' statement
H-0563-2025 | Allergen labeling: egg not listed in the 'contains' statement
H-0564-2025 | Allergen labeling: specific tree nut (pecan) and egg not listed in 'contains' statement
H-0565-2025 | Allergen labeling: specific tree nut (pecans) not listed in the 'contains' statement
H-0566-2025 | Allergen labeling: missing allergens (peanuts, milk) in contains statement
H-0567-2025 | Allergen labeling: specific tree nut (pecan) not listed in 'contains' statement
H-0578-2025 | Undeclared soy allergen
H-0580-2025 | Undeclared allergen (peanut, pecan).
H-0581-2025 | Undeclared allergen (peanut, pecan).
H-0582-2025 | Product contains undeclared wheat.
H-0602-2025 | Review of Label determined allergen was listed as unsalted butter/ heavy cream. In one instance of identified label, there was no milk or dairy listed listed in Contains statement. Further review of label revealed "soy" had been removed.
H-0605-2025 | Product contains undeclared Soy and Sesame
H-0612-2025 | undeclared allergen (Wheat and Milk) on ready to eat sandwiches.
H-0613-2025 | undeclared allergen (Wheat and Milk) on ready to eat sandwiches.
H-0614-2025 | undeclared allergen (Wheat and Milk) on ready to eat sandwiches.
H-0615-2025 | undeclared allergen (Wheat) on ready to eat sandwiches.
H-0616-2025 | Undeclared allergens (sesame and soy).
H-0635-2025 | May contained undeclared almond
```

### PULL 3 — every request (UTC, Date header, meta verbatim)

- Request: GET https://api.fda.gov/food/enforcement.json?search=report_date%3A%5B20241001+TO+20250930%5D&limit=1000&skip=0
  - Retrieved (UTC): 2026-11-12T09:10:57Z · HTTP 200
  - Date: Thu, 12 Nov 2026 09:10:58 GMT
  - meta object verbatim:
```json
{
  "disclaimer": "Do not rely on openFDA to make decisions regarding medical care. While we make every effort to ensure that data is accurate, you should assume all results are unvalidated. We may limit or otherwise restrict your access to the API in line with our Terms of Service.",
  "terms": "https://open.fda.gov/terms/",
  "license": "https://open.fda.gov/license/",
  "last_updated": "2026-11-04",
  "results": {
    "skip": 0,
    "limit": 1000,
    "total": 1564
  }
}
```
- Request: GET https://api.fda.gov/food/enforcement.json?search=report_date%3A%5B20241001+TO+20250930%5D&limit=1000&skip=1000
  - Retrieved (UTC): 2026-11-12T09:10:59Z · HTTP 200
  - Date: Thu, 12 Nov 2026 09:10:59 GMT
  - meta object verbatim:
```json
{
  "disclaimer": "Do not rely on openFDA to make decisions regarding medical care. While we make every effort to ensure that data is accurate, you should assume all results are unvalidated. We may limit or otherwise restrict your access to the API in line with our Terms of Service.",
  "terms": "https://open.fda.gov/terms/",
  "license": "https://open.fda.gov/license/",
  "last_updated": "2026-11-04",
  "results": {
    "skip": 1000,
    "limit": 1000,
    "total": 1564
  }
}
```

### PULL 3 — reason_for_recall of every kept record

```text
F-0001-2025 | Undeclared wheat. The firm was notified by their supplier that they failed to include the allergen "wheat" on the label.
F-0002-2025 | Undeclared wheat. The firm was notified by their supplier that they failed to include the allergen "wheat" on the label.
F-0003-2025 | Undeclared wheat. The firm was notified by their supplier that they failed to include the allergen "wheat" on the label.
F-0014-2025 | Undeclared whey (milk), wheat flour, almonds; no contains statement & no nutrition fact panel
F-0015-2025 | Undeclared whey (milk) & wheat flour: no nutrition fact panel & no contains statement
F-0016-2025 | Undeclared whey (milk), wheat flour, & bran (wheat); no nutrition fact panel & no contains statement
F-0017-2025 | Undeclared whey (milk) & wheat flour; no nutrition fact panel & no contains statement
F-0018-2025 | Undeclared whey (milk) & wheat flour: no nutrition fact panel & no contains statement
F-0019-2025 | Undeclared whey (milk) & wheat flour; no nutrition fact panel & no contains statement
F-0020-2025 | Undeclared whey (milk) and wheat flour; no nutritional fact panel & no contains statement
F-0021-2025 | Undeclared whey (milk), wheat flour, & coconut; no nutrition fact panel & no contains statement
F-0022-2025 | Undeclared whey (milk) & wheat flour; no nutrition fact panel & no contains statement
F-0023-2025 | Undeclared allergens; walnuts
F-0035-2025 | Undeclared allergens; milk
F-0036-2025 | Undeclared allergens; milk
F-0037-2025 | Undeclared Allergen, milk - a mix-up between the product description and the ingredient list. Milk Chocolate was listed in the product description but was missing from the ingredient list.
F-0038-2025 | Mayonnaise is declared but Soybean Oil and Egg are not declared.
F-0039-2025 | Soybean Paste is declared but Wheat and Sesame Seeds are not declared.
F-0041-2025 | Soybean Sauce is declared but Wheat and Fish (Anchovy) are not declared.
F-0042-2025 | Soybean Sauce is declared but Wheat is not declared.
F-0043-2025 | Undeclared Crustacean (shrimp).
F-0044-2025 | Undeclared Fish (Anchovy).
F-0045-2025 | Soybean Sauce is declared but Wheat and Fish (Anchovy) are not declared.
F-0046-2025 | Undeclared Fish (Anchovy).
F-0047-2025 | Soy Sauce is declared but Wheat is not declared.
F-0048-2025 | Soy Bean Paste is declared but Wheat, Fish (Large-eyed Herring, Anchovy), and Crustacean (Shrimp) are not declared.
F-0049-2025 | Soy Sauce is declare but Wheat and Fish (Anchovy) are not declared.
F-0050-2025 | Soy Sauce is declared but Wheat is not declared.
F-0054-2025 | Milk may contain undeclared almond from almond milk
F-0057-2025 | Undeclared Wheat flour. Product contains wheat flour but product was sold without the Ingredients Statement.
F-0067-2025 | Undeclared Almonds & Cashews. The firm was notified by their customers that the product contains a trail mix instead of the cheese mix. The trail mix contains almonds and cashews that are not listed in the ingredient statement.
F-0068-2025 | Undeclared Fish Allergen
F-0077-2025 | Undeclared allergen:Wheat
F-0097-2025 | Undeclared allergens; wheat, soy, and eggs.
F-0098-2025 | Undeclared allergen: milk
F-0099-2025 | Undeclared sesame
F-0100-2025 | Undeclared sesame
F-0101-2025 | Undeclared sesame
F-0102-2025 | Undeclared sesame
F-0103-2025 | Undeclared sesame
F-0104-2025 | Undeclared sesame
F-0105-2025 | Undeclared sesame
F-0120-2025 | Undeclared allergens; sesame
F-0121-2025 | Butter lists cream, but may be missing the Contains Milk statement.
F-0122-2025 | Butter lists cream, but may be missing the Contains Milk statement.
F-0126-2025 | The product is being recalled due to an undeclared allergen - tree nuts (walnuts).
F-0132-2025 | Undeclared wheat. Product contains wheat but was mis-labeled as Savory 6 Cut Crinkle Cut Wedge and label does not declare wheat.
F-0147-2025 | Product contains undeclared hydrolyzed soy protein.
F-0148-2025 | Undeclared egg
F-0216-2025 | Undeclared tree nuts (almonds)
F-0217-2025 | Undeclared egg
F-0218-2025 | Undeclared egg
F-0219-2025 | Undeclared egg
F-0220-2025 | Undeclared egg
F-0244-2025 | Undeclared eggs and yellow #5.
F-0245-2025 | Contains undeclared egg
F-0253-2025 | Undeclared allergen - egg
F-0259-2025 | Undeclared Wheat. The firm was notified by a consumer that they found crispy onions in the packaging of the tortilla strips. The onions contain wheat which is not listed on the packaging for the tortilla strips.
F-0260-2025 | Undeclared Allergen - Wheat and Soy
F-0262-2025 | Product contains undeclared soy lecithin.
F-0263-2025 | Contains undeclared soy lecithin
F-0266-2025 | Undeclared soy (soy lecithin).
F-0293-2025 | Undeclared allergen labeling (milk)
F-0294-2025 | Undeclared allergen labeling (milk)
F-0295-2025 | Undeclared allergen labeling (milk)
F-0296-2025 | Undeclared allergen labeling (milk)
F-0297-2025 | Undeclared allergen labeling (milk)
F-0299-2025 | Undeclared allergens: Milk, Soy, Crustacea Shellfish, Fish
F-0317-2025 | Product contains undeclared fish (anchovy) and soy.
F-0319-2025 | Products contain undeclared allergens (milk, soy, and wheat) and undeclared sulfites, yellow 5, yellow 6.
F-0320-2025 | Products contain undeclared allergens (milk, soy, peanut, and wheat) and undeclared sulfites, yellow 5, yellow 6, and red 40)
F-0321-2025 | The contains statement does not declare sesame. Black sesame seeds are visible on product and the Ingredients Statement declares black sesame seeds.
F-0376-2025 | Product contains Undeclared Allergen Tree Nuts (Cashews)
F-0384-2025 | Undeclared egg allergen
F-0386-2025 | Potential contamination of undeclared allergen peanuts
F-0402-2025 | Undeclared allergens (Wheat and Soy)
F-0404-2025 | Product does not include statement: Contains milk
F-0409-2025 | Undeclared milk
F-0411-2025 | Undeclared milk
F-0412-2025 | Undeclared wheat, Undeclared soybean oil
F-0413-2025 | Undeclared wheat, Undeclared soybean oil
F-0414-2025 | Undeclared milk
F-0415-2025 | Undeclared milk
F-0416-2025 | Undeclared milk
F-0417-2025 | Undeclared almonds
F-0418-2025 | Undeclared milk
F-0419-2025 | Undeclared milk
F-0421-2025 | Product contains undeclared milk and soy.
F-0422-2025 | Undeclared Milk. During an FDA investigation the manufacturer was notified that the label does not list the allergen milk in the ingredient statement.
F-0428-2025 | Undeclared Milk Allergen
F-0431-2025 | Frozen Peach Mango Sorbet contains undeclared allergen (egg)
F-0433-2025 | Soy is missing from the "Contains" statement.
F-0458-2025 | Barbeque sauce product contains undeclared allergens (soy) contained in sub-ingredient
F-0459-2025 | Barbeque sauce product contains undeclared allergen listing of (Milk) in product ingredient listing from sub-ingredient Butter.
F-0460-2025 | Barbeque sauce product contains undeclared listing of (Milk) in product ingredient listing from sub-ingredient Butter.
F-0461-2025 | The product is being recalled because of undeclared milk .
F-0462-2025 | The product is being recalled because of undeclared milk .
F-0463-2025 | The product is being recalled because of undeclared milk .
F-0464-2025 | Undeclared milk
F-0465-2025 | Undeclared walnuts
F-0466-2025 | Undeclared Milk. During the firm's reordering process of labels, they discovered that the label does not list milk in its ingredient or contain statement.
F-0467-2025 | Undeclared Milk. During the firm's reordering process of labels, they discovered that the label does not list milk in its ingredient or contain statement.
F-0469-2025 | Undeclared allergens (wheat) on label, incorrect label was placed on product
F-0531-2025 | Contains undeclared visible almonds
F-0532-2025 | Firm distributed a Bread Crumb product with undeclared allergen (Sesame) not on the label.
F-0533-2025 | Firm distributed a Seasoned Bread Crumb product with undeclared allergen (Sesame) not on the label.
F-0534-2025 | Imported Monkfish Liver undeclared allergen (Milk)
F-0548-2025 | Undeclared allergen (Milk) in Shirakiku brand Curvee Puffs Corn Puff Snack
F-0549-2025 | Undeclared allergen (Milk) in Shirakiku brand Curvee Puffs Corn Puff Snack
F-0550-2025 | Undeclared allergen (Milk) in Shirakiku brand Curvee Puffs Corn Puff Snack
F-0552-2025 | Undeclared Allergen - Milk
F-0553-2025 | Undeclared milk allergen
F-0570-2025 | Undeclared allergen (soy).
F-0572-2025 | Product may contain egg, an undeclared allergen.
F-0573-2025 | Potato flour item #20501 was recalled due to undeclared milk (between 13ppm and 17ppm).
F-0577-2025 | Mislabeled salads (undeclared peanut allergen). Incorrect ingredient applied (peanuts)
F-0581-2025 | Undeclared milk
F-0582-2025 | Undeclared milk
F-0583-2025 | Undeclared milk
F-0604-2025 | Undeclared Milk.
F-0605-2025 | Undeclared Milk.
F-0606-2025 | Undeclared egg.
F-0607-2025 | Undeclared egg.
F-0608-2025 | Undeclared allergen (walnuts)
F-0624-2025 | Milk not listed in the ingredients or included in parentheses after American Cheese.
F-0630-2025 | Milk not declared as the major food allergen source for the ingredient Whey
F-0631-2025 | Undeclared egg
F-0632-2025 | Milk not listed in Contains statement
F-0633-2025 | Undeclared wheat and egg
F-0634-2025 | Egg not listed in Contains statement
F-0635-2025 | Wheat not listed in Contains statement
F-0636-2025 | Undeclared almonds
F-0637-2025 | Product may contain incorrect salad dressing, resulting in fish and wheat being undeclared.
F-0638-2025 | Incorrect back label on product resulting in undeclared allergens (wheat, eggs)
F-0639-2025 | Contains undeclared milk
F-0649-2025 | Undeclared soy lecithin and undeclared color additives Blue 1 Lake, Yellow 6, Red 40, Yellow 5, Blue 1, Yellow 6 Lake, Red 40 Lake, Yellow 5 Lake, Blue 2 Lake, Blue 2.
F-0663-2025 | Contains undeclared egg
F-0667-2025 | Undeclared Pecan. The firm was notified by their customer that when they were placing the product on the shelves, they noticed the wrong product was in the container.
F-0669-2025 | Undeclared Allergen (Milk)
F-0672-2025 | (Imported) Hot Pot Sauce contains undeclared allergens (Wheat and Soy)
F-0673-2025 | (Imported) Hot Pot Sauce (SPICY) contains undeclared allergens (Wheat and Soy)
F-0674-2025 | Finished product label fails to include Milk in ingredient listing. (Undeclared Allergen)
F-0686-2025 | Turkey BLT on Sourdough Sandwiches being recalled due to the product having the incorrect sandwich (Peanut Butter & Jelly) in the clamshell container. This incorrect product in the container resulted in an undeclared allergen on the product label (peanuts).
F-0687-2025 | undeclared allergen ingredient (wheat) on product label for flour Gorditas.
F-0688-2025 | Undeclared allergen (milk).
F-0692-2025 | Label declares tofu but it does not declare soy.
F-0694-2025 | Undeclared Allergen (Soy)
F-0695-2025 | Undeclared Sesame, Soy, Wheat, Yellow No. 5, Yellow No. 6, and Red No. 6.
F-0698-2025 | Undeclared soy flour
F-0699-2025 | Undeclared allergen (milk not listed as sub ingredient of butter). Milk also not listed in 'Contains' statement.
F-0700-2025 | Undeclared allergens (soy, milk) and Yellow #5
F-0702-2025 | Undeclared allergen (eggs) and pork
F-0704-2025 | Undeclared peanuts, soy, sesame, and wheat.
F-0707-2025 | Label declares tahini paste but does not declare sesame.
F-0708-2025 | Undeclared allergen: Soy lecithin, less than 2%
F-0709-2025 | Undeclared allergens: Soy lecithin
F-0710-2025 | Product contains undeclared milk.
F-0719-2025 | Undeclared milk
F-0720-2025 | Undeclared Milk - During an FDA inspection the firm was notified that milk was not declared on the label.
F-0729-2025 | Undeclared allergen: Wheat
F-0732-2025 | Product does not declare the allergen, milk, on the label.
F-0744-2025 | Undeclared Wheat and Soy
F-0747-2025 | Product contains undeclared egg.
F-0748-2025 | Contains undeclared allergens (almonds).
F-0749-2025 | Undeclared allergen (milk)
F-0750-2025 | Undeclared allergen (milk)
F-0751-2025 | Undeclared allergen (milk)
F-0757-2025 | Product mislabeled - product labeled as peanuts, but may contain cashews
F-0761-2025 | Undeclared allergen ingredient (milk)
F-0762-2025 | undeclared milk
F-0763-2025 | Undeclared Almonds
F-0764-2025 | Undeclared Almonds
F-0765-2025 | Undeclared Almonds
F-0766-2025 | Undeclared Almonds
F-0767-2025 | Undeclared Almonds
F-0768-2025 | Undeclared Almonds
F-0769-2025 | Undeclared Almonds
F-0770-2025 | Undeclared Almonds
F-0771-2025 | Undeclared Almonds
F-0772-2025 | Undeclared Almonds
F-0773-2025 | Undeclared Almonds
F-0774-2025 | Undeclared Almonds
F-0801-2025 | Contains undeclared almonds & undeclared sesame
F-0802-2025 | Product contains undeclared wheat.
F-0804-2025 | Undeclared allergen (soy)
F-0806-2025 | Undeclared allergen (soy) due to mislabeling.   Product is labeled as Brown Sugar Molasses Baked Beans, but contains Beef and BBQ Baked Beans. The Beef and BBQ Baked Beans contain soy, which is not declared on the label.
F-0807-2025 | Undeclared milk allergen
F-0808-2025 | Undeclared allergens (milk and/or peanuts).
F-0809-2025 | Undeclared allergens (milk and/or peanuts).
F-0810-2025 | Product contains undeclared almond and cashew.
F-0811-2025 | Undeclared almond and cashew.
F-0813-2025 | Undeclared hazelnut. The Oregon Trail Mix contains visible hazelnut and was mis-labeled as Organic Roasted Salted Cashews, but the label does not declare hazelnut.
F-0823-2025 | Due to printing quality, label does not declare Egg allergen clearly.
F-0824-2025 | Due to printing quality, label does not declare Egg allergen clearly.
F-0825-2025 | Due to printing quality, label does not declare Egg allergen clearly.
F-0826-2025 | Due to printing quality, label does not declare Egg allergen clearly.
F-0827-2025 | Due to printing quality, label does not declare Egg allergen clearly.
F-0828-2025 | Due to printing quality, label does not declare Egg allergen clearly.
F-0829-2025 | Due to printing quality, label does not declare Egg allergen clearly.
F-0830-2025 | Due to printing quality, label does not declare Egg allergen clearly.
F-0831-2025 | Due to printing quality, label does not declare these allergens clearly: Egg, Milk, Soy.
F-0832-2025 | Due to printing quality, label does not declare these allergens clearly: Egg, Milk, Soy.
F-0833-2025 | Due to printing quality, label does not declare these allergens clearly: Egg, Milk, Soy.
F-0834-2025 | Due to printing quality, label does not declare these allergens clearly: Egg, Milk, Soy.
F-0835-2025 | Due to printing quality, label does not declare these allergens clearly: Egg and Milk.
F-0836-2025 | Due to printing quality, label does not declare these allergens clearly: Egg and Milk.
F-0837-2025 | Due to printing quality, label does not declare these allergens clearly: Egg, Milk, Soy.
F-0838-2025 | Due to printing quality, label does not declare these allergens clearly: Egg, Milk, Pecan.
F-0927-2025 | undeclared milk allergen
F-0928-2025 | Undeclared Fish allergen (parvalbumin).
F-0929-2025 | Undeclared sesame
F-0931-2025 | The Instant Milk Tea Powder's ingredients statement declares Non-Dairy Creamer (Whey Powder, Sodium Caseinate) but does not specify milk.
F-0932-2025 | The Instant Milk Tea Powder's ingredients statement declares Non-Dairy Creamer (Whey Powder, Sodium Caseinate) but does not specify milk.
F-0933-2025 | The Instant Milk Tea Powder's ingredients statement declares Non-Dairy Creamer (Whey Powder, Sodium Caseinate) but does not specify milk.
F-0934-2025 | The Instant Milk Tea Powder's ingredients statement declares Non-Dairy Creamer (Whey Powder, Sodium Caseinate) but does not specify milk.
F-0935-2025 | The Instant Milk Tea Powder's ingredients statement declares Non-Dairy Creamer (Whey Powder, Sodium Caseinate) but does not specify milk.
F-0937-2025 | The ingredients statement declares fish sauce but does not declare anchovies. The Contains statement does not declare fish (anchovies).
F-0938-2025 | Undeclared allergens (wheat, sesame)
F-1821-2024 | Soy is in the ingredients but missing from the contains statement.
F-1822-2024 | Products contain undeclared sub ingredient: wheat.
F-1823-2024 | Products contain undeclared sub ingredient: wheat.
F-1824-2024 | Products contain undeclared sub ingredients: wheat and milk
F-1825-2024 | Products contain undeclared sub ingredients: wheat and milk
F-1826-2024 | Products contain undeclared sub ingredients: wheat and milk
F-1827-2024 | Products contain undeclared sub ingredient: wheat.
F-1828-2024 | Products contain undeclared sub ingredient wheat.
F-1829-2024 | Products contain undeclared wheat.
F-1830-2024 | Products contain undeclared sub ingredients: wheat and milk.
F-1831-2024 | Undeclared soy lecithin and soybean oil on label
F-1832-2024 | Undeclared soy lecithin and soybean oil on label
F-1833-2024 | Undeclared allergen (Fish) Ingredient
F-1834-2024 | Undeclared allergen (Fish) Ingredient
F-1835-2024 | Allergen not listed in the Contains statement: Fish
F-1836-2024 | Undeclared walnut and wheat.  Mini Squash Harvest Loaf (UPC 8 55324 00505 3) was mis-labeled as Mini Raspberry Lemon Coffee Cake (UPC 8 57297 00745 4) and therefore wheat flour and walnuts are not declared on label.
H-0008-2025 | Contains undeclared peanut
H-0011-2025 | Undeclared Allergen (walnuts), was not on outer packaging but was on the inner packaging of product.
H-0017-2025 | Undeclared allergens and mislabeled product.  Rocky Road Ice was packaged with Chocolate Truffle Ice Cream labeled tub and a Rocky Road Ice Cream lid. Tub said "may contain tree nuts" the lid said it did contain almonds.
H-0040-2025 | Undeclared soy allergen
H-0043-2025 | Atlantic Salmon Portions with Seafood Stuffing was incorrectly labeled and does not declare allergen ingredient (SOY)
H-0047-2025 | Undeclared Milk Allergen
H-0058-2025 | Undeclared wheat
H-0059-2025 | Undeclared wheat
H-0060-2025 | Undeclared wheat
H-0063-2025 | Undeclared Milk.
H-0065-2025 | Undeclared Sesame. The firm was notified by a retailer that product labeled as Sea Salt Bagel Crackers contained Everything Bagel Crackers. The Everything Bagel Crackers contains sesame which is not listed in the ingredient statement.
H-0066-2025 | Undeclared  Milk
H-0071-2025 | Undeclared wheat allergen
H-0072-2025 | Undeclared milk
H-0073-2025 | Undeclared milk and wheat allergens
H-0074-2025 | Undeclared wheat allergens
H-0075-2025 | Undeclared wheat allergens
H-0076-2025 | Undeclared  wheat allergens
H-0077-2025 | Undeclared wheat allergens
H-0078-2025 | Undeclared wheat allergens
H-0079-2025 | Undeclared wheat allergens
H-0080-2025 | Undeclared wheat allergens
H-0081-2025 | Undeclared wheat allergens
H-0082-2025 | Undeclared sesame and wheat allergens
H-0083-2025 | Undeclared sesame and wheat allergens
H-0084-2025 | Undeclared wheat allergens
H-0085-2025 | Undeclared wheat allergens
H-0086-2025 | Undeclared wheat allergens
H-0087-2025 | Undeclared wheat allergens
H-0115-2025 | Undeclared allergens: Milk, Eggs, Soy Ingredients (Soybean oil, Soy Lecithin), Wheat, Tree Nuts (Almonds, Hazelnuts) on label and incomplete Contains statement
H-0116-2025 | Undeclared allergens: Milk, Eggs, Soy Ingredients (Soybean oil, Soy Lecithin), Wheat, Tree Nuts (Almonds, Hazelnuts) on label and incomplete Contains statement
H-0117-2025 | Undeclared allergens: Milk, Eggs, Soy Ingredients (Soybean oil, Soy Lecithin), Wheat, Tree Nuts (Almonds, Hazelnuts) on label and incomplete Contains statement
H-0118-2025 | Undeclared allergens: Milk, Eggs, Soy Ingredients (Soybean oil, Soy Lecithin), Wheat, Tree Nuts (Almonds, Hazelnuts) on label and incomplete Contains statement
H-0119-2025 | Undeclared allergens: Milk, Eggs, Soy Ingredients (Soybean oil, Soy Lecithin), Wheat, Tree Nuts (Almonds, Hazelnuts) on label and incomplete Contains statement
H-0211-2025 | undeclared cashews
H-0212-2025 | Contains undeclared peanut
H-0213-2025 | Undeclared milk
H-0215-2025 | Undeclared Milk Allergen
H-0216-2025 | Undeclared Milk Allergen
H-0254-2025 | Undeclared soy and wheat
H-0255-2025 | Undeclared wheat
H-0256-2025 | Undeclared soy, contains statement is present but does not list pistachios
H-0257-2025 | Undeclared soy, contains statement is present but does not list pistachios
H-0258-2025 | Undeclared wheat, soy, and sesame
H-0272-2025 | undeclared milk
H-0278-2025 | Undeclared milk
H-0281-2025 | undeclared pecans
H-0282-2025 | undeclared pecans
H-0283-2025 | undeclared pecans
H-0306-2025 | Product does not declare allergen ingredient sesame.
H-0308-2025 | Undeclared allergens - soy and wheat
H-0309-2025 | Undeclared allergen - soy
H-0310-2025 | Undeclared allergens - soy and wheat
H-0311-2025 | Undeclared allergens - soy and wheat
H-0312-2025 | Undeclared allergens - soy and wheat
H-0313-2025 | Undeclared allergen - soy
H-0314-2025 | Undeclared allergen - soy
H-0315-2025 | Undeclared allergen - soy
H-0319-2025 | Undeclared allergen: Hazelnut due to mispackaging. Product with hazelnuts was put in the Artisan Style 1/2 loaf bags. Bags do not have allergen statement that includes hazelnuts.
H-0320-2025 | Label declares Shelled Edamame but does not specify or declare soy.
H-0323-2025 | Undeclared allergens (Peanut) due to mispackaging
H-0324-2025 | Undeclared allergens (Peanut) due to mispackaging
H-0325-2025 | Undeclared allergens (Peanut) due to mispackaging
H-0326-2025 | Undeclared allergens (Peanut) due to mispackaging
H-0331-2025 | Undeclared sesame
H-0332-2025 | Undeclared sesame
H-0333-2025 | Undeclared sesame
H-0334-2025 | Undeclared sesame
H-0335-2025 | Undeclared sesame
H-0336-2025 | Undeclared sesame
H-0347-2025 | Undeclare Tree Nuts (almond, macadamia nut)
H-0348-2025 | Undeclared Milk
H-0349-2025 | Undeclared Allergen (Milk). Consumer found a breaded halloumi Cheese Stick in the bag of churro bites.  The Halloumi Cheese contains milk which is not an allergen in the churros.
H-0354-2025 | allergen labeling - undeclared milk
H-0355-2025 | Undeclared wheat and soy
H-0356-2025 | Undeclared wheat
H-0357-2025 | Undeclared wheat
H-0358-2025 | Undeclared wheat
H-0359-2025 | Undeclared wheat and soy
H-0360-2025 | Undeclared wheat and soy
H-0361-2025 | Undeclared wheat and soy
H-0362-2025 | Undeclared wheat
H-0363-2025 | Undeclared wheat
H-0364-2025 | Undeclared wheat and soy
H-0365-2025 | Undeclared wheat
H-0366-2025 | Undeclared wheat and soy
H-0367-2025 | Undeclared wheat and soy
H-0368-2025 | Undeclared wheat and soy
H-0369-2025 | Undeclared wheat
H-0370-2025 | Undeclared wheat and soy
H-0371-2025 | Undeclared wheat and soy
H-0372-2025 | Undeclared wheat
H-0373-2025 | Undeclared wheat and soy
H-0374-2025 | Undeclared wheat
H-0375-2025 | Undeclared wheat
H-0376-2025 | Undeclared wheat and soy
H-0377-2025 | Undeclared wheat and soy
H-0378-2025 | Undeclared wheat
H-0392-2025 | Allergen not listed in the Contains statement: Sesame
H-0393-2025 | Allergen not listed in the Contains statement: Sesame
H-0453-2025 | Various snack cracker products are mislabeled and do not declare all allergen ingredients (Whole Milk Powder and wheat).
H-0454-2025 | Various snack cracker products are mislabeled and do not declare all allergen ingredients (Whole Milk Powder and wheat).
H-0455-2025 | Various snack cracker products are mislabeled and do not declare all allergen ingredients (Whole Milk Powder and wheat).
H-0456-2025 | Undeclared sesame.
H-0458-2025 | Product label includes the ingredient CREAM but does not include Milk as the source.
H-0459-2025 | Product label includes the ingredient CREAM but does not include Milk as the source.
H-0460-2025 | Product label includes the ingredient CREAM but does not include Milk as the source.
H-0461-2025 | Product label includes the ingredient CREAM but does not include Milk as the source.
H-0462-2025 | Product label includes the ingredient CREAM but does not include Milk as the source.
H-0463-2025 | Product label includes the ingredient CREAM but does not include Milk as the source.
H-0464-2025 | Product label includes the ingredient CREAM but does not include Milk as the source.
H-0465-2025 | Product label includes the ingredient CREAM but does not include Milk as the source.
H-0466-2025 | Product label includes the ingredient CREAM but does not include Milk as the source.
H-0467-2025 | Product label includes the ingredient CREAM but does not include Milk as the source.
H-0468-2025 | Product label includes the ingredient CREAM but does not include Milk as the source.
H-0469-2025 | Product label includes the ingredient CREAM but does not include Milk as the source.
H-0470-2025 | Product label includes the ingredient CREAM but does not include Milk as the source.
H-0471-2025 | Product label includes the ingredient CREAM but does not include Milk as the source.
H-0487-2025 | Undeclared milk from Contains statement.
H-0488-2025 | Undeclared milk and soy (from soy lecithin) from sub-ingredients.
H-0489-2025 | Undeclared milk and/or eggs from sub-ingredients and/or Contains statement.
H-0490-2025 | Undeclared wheat and milk from sub-ingredients.
H-0491-2025 | Undeclared wheat, milk, and soy (from soy lecithin) from sub-ingredients.
H-0502-2025 | Ramen Noodle package label does not declare Soy as the source for lecithin ingredient.
H-0503-2025 | Ramen Noodle package label does not declare Soy as the source for lecithin ingredient.
H-0505-2025 | Product contains undeclared soy lecithin.
H-0506-2025 | Undeclared egg.
H-0507-2025 | Undeclared egg.
H-0508-2025 | Undeclared egg.
H-0509-2025 | Undeclared egg.
H-0510-2025 | Undeclared egg.
H-0511-2025 | Undeclared egg.
H-0512-2025 | Undeclared egg.
H-0513-2025 | Undeclared egg.
H-0514-2025 | Undeclared egg.
H-0515-2025 | Undeclared egg.
H-0516-2025 | Undeclared egg.
H-0517-2025 | Undeclared egg.
H-0518-2025 | Undeclared egg.
H-0519-2025 | Undeclared egg.
H-0522-2025 | Undeclared eggs
H-0531-2025 | Finished product label does not include allergen ingredient Sesame Seed.
H-0533-2025 | Product label does not list ingredients including major food allergen: sesame.   Additional undeclared ingredients include: millet and flax
H-0534-2025 | Product label does not list ingredients including major food allergen: sesame.   Additional undeclared ingredients include: poppy seeds, dried garlic, dried onion, and sea salt
H-0535-2025 | Product label does not list ingredients including major food allergens: wheat and soy (vegetable oil).  Additional undeclared ingredients include: niacin, reduced iron, vitamin B1, vitamin B2, invert sugar
H-0537-2025 | Product contains undeclared wheat and soy.
H-0546-2025 | undeclared almond, walnut, and pecan.
H-0550-2025 | Undeclared wheat allergen.
H-0558-2025 | Contains undeclared wheat. The top label identifies the product as potato salad, but the unit contains pasta salad.
H-0559-2025 | Allergen labeling: egg is not listed in the 'contains' statement
H-0560-2025 | Allergen labeling: specific tree nut (walnut) and egg are not listed in the 'contains' statement
H-0561-2025 | Allergen labeling: egg is not listed in the 'contains' statement
H-0562-2025 | Allergen labeling: specific tree nut (pecan) and egg are not listed in the 'contains' statement
H-0563-2025 | Allergen labeling: egg not listed in the 'contains' statement
H-0564-2025 | Allergen labeling: specific tree nut (pecan) and egg not listed in 'contains' statement
H-0565-2025 | Allergen labeling: specific tree nut (pecans) not listed in the 'contains' statement
H-0566-2025 | Allergen labeling: missing allergens (peanuts, milk) in contains statement
H-0567-2025 | Allergen labeling: specific tree nut (pecan) not listed in 'contains' statement
H-0578-2025 | Undeclared soy allergen
H-0580-2025 | Undeclared allergen (peanut, pecan).
H-0581-2025 | Undeclared allergen (peanut, pecan).
H-0582-2025 | Product contains undeclared wheat.
H-0602-2025 | Review of Label determined allergen was listed as unsalted butter/ heavy cream. In one instance of identified label, there was no milk or dairy listed listed in Contains statement. Further review of label revealed "soy" had been removed.
H-0605-2025 | Product contains undeclared Soy and Sesame
H-0612-2025 | undeclared allergen (Wheat and Milk) on ready to eat sandwiches.
H-0613-2025 | undeclared allergen (Wheat and Milk) on ready to eat sandwiches.
H-0614-2025 | undeclared allergen (Wheat and Milk) on ready to eat sandwiches.
H-0615-2025 | undeclared allergen (Wheat) on ready to eat sandwiches.
H-0616-2025 | Undeclared allergens (sesame and soy).
H-0635-2025 | May contained undeclared almond
```

## PLATFORM RECORD (server-stamped notes)

- Request: GET https://synmerco.com/v1/escrows/esc_25b1a72cbe674fc0808f773a/progress · Retrieved (UTC): 2026-11-12T12:15:21Z · HTTP 200
```json
{
 "escrowId": "esc_25b1a72cbe674fc0808f773a",
 "count": 7,
 "notes": [
  {
   "recordedAt": "2026-11-10 02:16:41.695471+00",
   "by": "did:pkh:eip155:8453:0x4e6a4A54F3df9Af1EceeC2D4AD797454fb0FecA1",
   "note": "PULL 1: 2026-11-10T02:16:38Z - openFDA /food/enforcement.json re-read for report_date:[20241001 TO 20250930], all classifications. 2 of 2 requests HTTP 200; response meta.results.total 1564, distinct recall_number held 1564. HTTP Date headers recorded for PROOF: Tue, 10 Nov 2026 02:09:43 GMT, Tue, 10 Nov 2026 02:09:46 GMT. food-allergen-pull1.csv: 1564 data rows (one per returned record, sorted by recall_number), 109628 bytes, SHA-256 d7bc886f05c09629e1cf444f2e372a283b3585c015a5f85484c183afcce251c4; 406 rows kept=yes tagged by undeclared allergen, 1158 kept=no. Declared under Rule 25 as a data file. PULL 2 is due at least 24 hours after this note, PULL 3 at least 24 hours after PULL 2; submit only after PULL 3 and earliestSubmitAt 2026-11-11T20:36:37.470Z. all requests HTTP 200"
  },
  {
   "recordedAt": "2026-11-11 07:49:09.261689+00",
   "by": "did:pkh:eip155:8453:0x4e6a4A54F3df9Af1EceeC2D4AD797454fb0FecA1",
   "note": "PULL 2: 2026-11-11T07:49:08Z - openFDA /food/enforcement.json re-read for report_date:[20241001 TO 20250930], all classifications. 2 of 2 requests HTTP 200; response meta.results.total 1564, distinct recall_number held 1564. HTTP Date headers recorded for PROOF: Wed, 11 Nov 2026 07:49:07 GMT, Wed, 11 Nov 2026 07:49:08 GMT. food-allergen-pull2.csv: 1564 data rows (one per returned record, sorted by recall_number), 109628 bytes, SHA-256 d7bc886f05c09629e1cf444f2e372a283b3585c015a5f85484c183afcce251c4; 406 rows kept=yes tagged by undeclared allergen, 1158 kept=no. Declared under Rule 25 as a data file. PULL 3 is due at least 24 hours after this note; submit only after PULL 3 and earliestSubmitAt 2026-11-11T20:36:37.470Z. all requests HTTP 200"
  },
  {
   "recordedAt": "2026-11-12 09:11:00.319504+00",
   "by": "did:pkh:eip155:8453:0x4e6a4A54F3df9Af1EceeC2D4AD797454fb0FecA1",
   "note": "PULL 3: 2026-11-12T09:11:00Z - openFDA /food/enforcement.json re-read for report_date:[20241001 TO 20250930], all classifications. 2 of 2 requests HTTP 200; response meta.results.total 1564, distinct recall_number held 1564. HTTP Date headers recorded for PROOF: Thu, 12 Nov 2026 09:10:58 GMT, Thu, 12 Nov 2026 09:10:59 GMT. food-allergen-pull3.csv: 1564 data rows (one per returned record, sorted by recall_number), 109628 bytes, SHA-256 d7bc886f05c09629e1cf444f2e372a283b3585c015a5f85484c183afcce251c4; 406 rows kept=yes tagged by undeclared allergen, 1158 kept=no. Declared under Rule 25 as a data file. PULL 3 is due at least 24 hours after this note; submit only after PULL 3 and earliestSubmitAt 2026-11-11T20:36:37.470Z. all requests HTTP 200"
  },
  {
   "recordedAt": "2026-11-12 11:20:12.462692+00",
   "by": "did:pkh:eip155:8453:0x4e6a4A54F3df9Af1EceeC2D4AD797454fb0FecA1",
   "note": "REVISION 1 (evaluator review 2026-11-12 09:17Z, item A2): H-0068-2025 (undeclared sulfites, excluded by the TASK) and H-0069-2025 (Listeria monocytogenes, no undeclared allergen) are now kept=no with empty allergens in all three CSVs, and are removed from each PULL's kept-reason list in the PROOF; all tables are recounted. Corrected files re-declared under the same names (Rule 25 replace): food-allergen-pull1.csv rows 1564 SHA-256 a9e43913e1f77ed21a1154bb45106131c164a1da15ed559b725d437189006972; food-allergen-pull2.csv rows 1564 SHA-256 a9e43913e1f77ed21a1154bb45106131c164a1da15ed559b725d437189006972; food-allergen-pull3.csv rows 1564 SHA-256 a9e43913e1f77ed21a1154bb45106131c164a1da15ed559b725d437189006972. Corrected kept count 404."
  },
  {
   "recordedAt": "2026-11-12 11:38:15.088171+00",
   "by": "did:pkh:eip155:8453:0x4e6a4A54F3df9Af1EceeC2D4AD797454fb0FecA1",
   "note": "PULL 1 (corrected file): food-allergen-pull1.csv as attached now holds 1564 rows, SHA-256 4fd72143cff263d845d08a4365bddeb3c46a7db9c8efa9d2c1f8bed80f673316. The earlier PULL 1 note's SHA-256 d7bc886f05c09629e1cf444f2e372a283b3585c015a5f85484c183afcce251c4 (109628 bytes) was the pre-correction file: per the evaluator's revisions, H-0068-2025 and H-0069-2025 are now kept=no with empty allergens (undeclared sulfites; Listeria monocytogenes - no undeclared allergen named), and H-0602-2025 is now tagged milk;soybeans (its reason names milk and soy)."
  },
  {
   "recordedAt": "2026-11-12 11:38:16.416355+00",
   "by": "did:pkh:eip155:8453:0x4e6a4A54F3df9Af1EceeC2D4AD797454fb0FecA1",
   "note": "PULL 2 (corrected file): food-allergen-pull2.csv as attached now holds 1564 rows, SHA-256 4fd72143cff263d845d08a4365bddeb3c46a7db9c8efa9d2c1f8bed80f673316. The earlier PULL 2 note's SHA-256 d7bc886f05c09629e1cf444f2e372a283b3585c015a5f85484c183afcce251c4 (109628 bytes) was the pre-correction file: per the evaluator's revisions, H-0068-2025 and H-0069-2025 are now kept=no with empty allergens (undeclared sulfites; Listeria monocytogenes - no undeclared allergen named), and H-0602-2025 is now tagged milk;soybeans (its reason names milk and soy)."
  },
  {
   "recordedAt": "2026-11-12 11:38:17.750675+00",
   "by": "did:pkh:eip155:8453:0x4e6a4A54F3df9Af1EceeC2D4AD797454fb0FecA1",
   "note": "PULL 3 (corrected file): food-allergen-pull3.csv as attached now holds 1564 rows, SHA-256 4fd72143cff263d845d08a4365bddeb3c46a7db9c8efa9d2c1f8bed80f673316. The earlier PULL 3 note's SHA-256 d7bc886f05c09629e1cf444f2e372a283b3585c015a5f85484c183afcce251c4 (109628 bytes) was the pre-correction file: per the evaluator's revisions, H-0068-2025 and H-0069-2025 are now kept=no with empty allergens (undeclared sulfites; Listeria monocytogenes - no undeclared allergen named), and H-0602-2025 is now tagged milk;soybeans (its reason names milk and soy)."
  }
 ],
 "_note": "recordedAt is Synmerco server time (the seller cannot set it)."
}
```

The CSV files, the tables and the Changes lists are data; each pull is judged by its own excerpts.

