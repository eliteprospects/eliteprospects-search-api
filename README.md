## Eliteprospects Search API

This is the official documentation for how to search players and teams from Eliteprospects.com. This is an early (non-final) version of the Eliteprospects API and formats and syntax may change. If you are using the API please let us know so we can give you notices regarding any changes.

### Player Search
Returns a list of 20 players that best meets the search query.

```
GET http://api.eliteprospects.com/v1/players?q=[search query]
```

__Player Response__  
```javascript
{
	id: "710",
	fullname: "Peter Forsberg",
	matches: [
		[0,7]
	],
	country: "1",
	position: "F",
	age: "1973"
}
```  
__id__ => unique player on in eliteprospects.com  
__fullname__ => name of the player  
__matches__ => array containing what characters in the fullname that matches the query. Note: [0,7] should be read from 0 to 7 meaning character 0,1,2,3,4,5,6 (don't include the last number). Useful if you want to highlight searches.  
  
__country__ => player nationality (see list of countries)  
__position__ => player position. F = Forward, D = Defenceman, G = Goaltender  
__age__ => what year the player was born (yes we know, it's a confusing parameter name)  


### Team Search
Returns a list of 20 teams that best matches the search query.

```
GET http://api.eliteprospects.com/v1/teams?q=[search query]
```

__Team Response__  
```javascript
{
	id: "8",
	fullteam: "Malmö",
	matches: [
		[0,4]
	],
	country: "1"
}
```  
__id__ => unique team id on eliteprospects.com  
__fullteam__ => name of the team  
__matches__ => array containing what characters in the fullname that matches the query. Note: [0,4] should be read from 0 to 4 meaning character 0,1,2,3,4 (don't include the last number). Useful if you want to highlight searches.  
__country__ => team nationality (see list of countries)  

### Link to eliteprospects.com
If you want to link the result back to eliteprospects.com you can build your urls as the examples below.
```
http://www.eliteprospects.com/player.php?player=[playerId]
```
```
http://www.eliteprospects.com/team.php?team=[teamId]
```

### List of Countries

id,name,shortname,ISO_3166-1_alpha-2,ISO_3166-1_alpha-3  
1,Sweden,,SE,SWE  
2,Finland,,FI,FIN  
3,Canada,,CA,CAN  
4,Slovakia,,SK,SVK  
5,Norway,,NO,NOR  
6,United States,USA,US,USA  
7,Denmark,,DK,DNK  
8,Czech Republic,,CZ,CZE  
9,Russian Federation,Russia,RU,RUS  
10,Switzerland,,CH,CHE  
11,Latvia,,LV,LVA  
12,Austria,,AT,AUT  
13,Estonia,,EE,EST  
14,France,,FR,FRA  
15,United Kingdom,U.K.,GB,GBR  
17,Poland,,PL,POL  
18,Romania,,RO,ROU  
19,Italy,,IT,ITA  
20,Japan,,JP,JPN  
21,Germany,,DE,DEU  
22,Hungary,,HU,HUN  
23,Belarus,,BY,BLR  
24,Ukraine,,UA,UKR  
25,England,,,ENG  
26,Belgium,,BE,BEL  
27,Iceland,,IS,ISL  
28,Slovenia,,SI,SVN  
29,Croatia,,HR,HRV  
30,Yugoslavia,,YU,YUG  
32,Netherlands,,NL,NLD  
33,Australia,,AU,AUS  
34,Lithuania,,LT,LTU  
35,Spain,,ES,ESP  
36,Kazakhstan,,KZ,KAZ  
37,Turkey,,TR,TUR  
38,Republic of Korea,South Korea,KR,KOR  
41,China,,CN,CHN  
42,Bulgaria,,BG,BGR  
43,Serbia,,RS,SRB  
44,Luxembourg,,LU,LUX  
45,Israel,,IL,ISR  
46,Wales,,,WLS  
47,Scotland,,,SCT  
48,Northern Ireland,Ireland,,NIR  
49,Ireland,,IE,IRL  
50,Mexico,,MX,MEX  
51,Thailand,,TH,THA  
52,Philippines,,PH,PHL  
53,New Zealand,,NZ,NZL  
54,Democratic People's Republic of Korea,North Korea,KP,PRK  
55,Mongolia,,MN,MNG  
56,Greece,,GR,GRC  
57,South Africa,,ZA,ZAF  
58,Taiwan,,TW,TWN  
59,Republic of Moldova,Moldova,MD,MDA  
60,United Arab Emirates,UAE,AE,ARE  
61,Algeria,,DZ,DZA  
62,Portugal,,PT,PRT  
63,Malta,,MT,MLT  
64,The Former Yugoslav Republic of Macedonia,Macedonia,MK,MKD  
65,Armenia,,AM,ARM  
66,Georgia,,GE,GEO  
67,Uzbekistan,,UZ,UZB  
68,Bosnia and Herzegovina,,BA,BIH  
69,Bolivarian Republic of Venezuela,Venezuela,VE,VEN  
70,Liechtenstein,,LI,LIE  
71,Namibia,,NA,NAM  
72,Argentina,,AR,ARG  
73,Morocco,,MA,MAR  
74,Plurinational State of Bolivia,Bolivia,BO,BOL  
75,Kyrgyzstan,,KG,KGZ  
76,Lebanon,,LB,LBN  
77,Saint Lucia,S.t. Lucia,LC,LCA  
78,Qatar,,QA,QAT  
79,Belize,,BZ,BLZ  
82,Soviet Union,,SU,SUN  
83,Andorra,,AD,AND  
84,Brazil,,BR,BRA  
85,Hong Kong,,HK,HKG  
87,Uganda,,UG,UGA  
88,Ethiopia,,ET,ETH  
89,Macao,,MO,MAC  
90,Kuwait,,KW,KWT  
91,Malaysia,,MY,MYS  
92,India,,IN,IND  
93,Azerbaijan,,AZ,AZE  
94,Islamic Republic of Iran,Iran,IR,IRN  
95,Colombia,,CO,COL  
96,Singapore,,SG,SGP  
100,Afghanistan,,AF,AFG  
101,Åland Islands,,AX,ALA  
102,Albania,,AL,ALB  
103,American Samoa,,AS,ASM  
104,Angola,,AO,AGO  
105,Anguilla,,AI,AIA  
106,Antarctica,,AQ,ATA  
107,Antigua and Barbuda,,AG,ATG  
108,Aruba,,AW,ABW  
109,Bahamas,,BS,BHS  
110,Bahrain,,BH,BHR  
111,Bangladesh,,BD,BGD  
112,Barbados,,BB,BRB  
113,Benin,,BJ,BEN  
114,Bermuda,,BM,BMU  
115,Bhutan,,BT,BTN  
116,Bonaire,,BQ,BES  
117,Botswana,,BW,BWA  
118,Bouvet Island,,BV,BVT  
119,British Indian Ocean Territory,,IO,IOT  
120,Brunei Darussalam,,BN,BRN  
121,Burkina Faso,,BF,BFA  
122,Burundi,,BI,BDI  
123,Cambodia,,KH,KHM  
124,Cameroon,,CM,CMR  
125,Cape Verde,,CV,CPV  
126,Cayman Islands,,KY,CYM  
127,Central African Republic,,CF,CAF  
128,Chad,,TD,TCD  
129,Chile,,CL,CHL  
130,Christmas Island,,CX,CXR  
131,Cocos (Keeling) Islands,,CC,CCK  
132,Comoros,,KM,COM  
133,Congo,,CG,COG  
134,The Democratic Republic of Congo,,CD,COD  
135,Cook Islands,,CK,COK  
136,Costa Rica,,CR,CRI  
137,Côte d'Ivoire,Ivory Coast,CI,CIV  
138,Cuba,,CU,CUB  
139,Curaçao,,CW,CUW  
140,Cyprus,,CY,CYP  
141,Djibouti,,DJ,DJI  
142,Dominica,,DM,DMA  
143,Dominican Republic,,DO,DOM  
144,Ecuador,,EC,ECU  
145,Egypt,,EG,EGY  
146,El Salvador,,SV,SLV  
147,Equatorial Guinea,,GQ,GNQ  
148,Eritrea,,ER,ERI  
149,Falkland Islands (Malvinas),,FK,FLK  
150,Faroe Islands,,FO,FRO  
151,Fiji,,FJ,FJI  
152,French Guiana,,GF,GUF  
153,French Polynesia,,PF,PYF  
154,French Southern Territories,,TF,ATF  
155,Gabon,,GA,GAB  
156,Gambia,,GM,GMB  
157,Ghana,,GH,GHA  
158,Gibraltar,,GI,GIB  
159,Greenland,,GL,GRL  
160,Grenada,,GD,GRD  
161,Guadeloupe,,GP,GLP  
162,Guam,,GU,GUM  
163,Guatemala,,GT,GTM  
164,Guernsey,,GG,GGY  
165,Guinea,,GN,GIN  
166,Guinea-Bissau,,GW,GNB  
167,Guyana,,GY,GUY  
168,Haiti,,HT,HTI  
169,Heard Island and McDonald Islands,,HM,HMD  
170,Holy See (Vatican City State),,VA,VAT  
171,Honduras,,HN,HND  
172,Indonesia,,ID,IDN  
173,Iraq,,IQ,IRQ  
174,Isle of Man,,IM,IMN  
175,Jamaica,,JM,JAM  
176,Jersey,,JE,JEY  
177,Jordan,,JO,JOR  
178,Kenya,,KE,KEN  
179,Kiribati,,KI,KIR  
180,Lao People's Democratic Republic,,LA,LAO  
181,Lesotho,,LS,LSO  
182,Liberia,,LR,LBR  
183,Libya,,LY,LBY  
186,Madagascar,,MG,MDG  
187,Malawi,,MW,MWI  
188,Maldives,,MV,MDV  
189,Mali,,ML,MLI  
190,Marshall Islands,,MH,MHL  
191,Martinique,,MQ,MTQ  
192,Mauritania,,MR,MRT  
193,Mauritius,,MU,MUS  
194,Mayotte,,YT,MYT  
195,Federated States of Micronesia,,FM,FSM  
196,Monaco,,MC,MCO  
197,Montenegro,,ME,MNE  
198,Montserrat,,MS,MSR  
199,Mozambique,,MZ,MOZ  
200,Burma (Myanmar),Burma,MM,MMR  
201,Nauru,,NR,NRU  
202,Nepal,,NP,NPL  
203,New Caledonia,,NC,NCL  
204,Nicaragua,,NI,NIC  
205,Niger,,NE,NER  
206,Nigeria,,NG,NGA  
207,Niue,,NU,NIU  
208,Norfolk Island,,NF,NFK  
209,Northern Mariana Islands,,MP,MNP  
210,Oman,,OM,OMN  
211,Pakistan,,PK,PAK  
212,Palau,,PW,PLW  
213,State of Palestine,,PS,PSE  
214,Panama,,PA,PAN  
215,Papua New Guinea,,PG,PNG  
216,Paraguay,,PY,PRY  
217,Peru,,PE,PER  
218,Pitcairn,,PN,PCN  
219,Puerto Rico,,PR,PRI  
220,Réunion,,RE,REU  
221,Rwanda,,RW,RWA  
222,Saint BarthÈlemy,,BL,BLM  
223,Saint Helena Ascension and Tristan da Cunha,,SH,SHN  
224,Saint Kitts and Nevis,,KN,KNA  
225,Saint Martin (French part),,MF,MAF  
226,Saint Pierre and Miquelon,,PM,SPM  
227,Saint Vincent and the Grenadines,,VC,VCT  
228,Samoa,,WS,WSM  
229,San Marino,,SM,SMR  
230,Sao Tome and Principe,,ST,STP  
231,Saudi Arabia,,SA,SAU  
232,Senegal,,SN,SEN  
233,Seychelles,,SC,SYC  
234,Sierra Leone,,SL,SLE  
235,Sint Maarten (Dutch part),,SX,SXM  
236,Solomon Islands,,SB,SLB  
237,Somalia,,SO,SOM  
238,South Georgia and the South Sandwich Islands,,GS,SGS  
239,South Sudan,,SS,SSD  
240,Sri Lanka,,LK,LKA  
241,Sudan,,SD,SDN  
242,Suriname,,SR,SUR  
243,Svalbard and Jan Mayen,,SJ,SJM  
244,Swaziland,,SZ,SWZ  
245,Syrian Arab Republic,,SY,SYR  
246,Tajikistan,,TJ,TJK  
247,United Republic of Tanzania,,TZ,TZA  
248,Timor-Leste,,TL,TLS  
249,Togo,,TG,TGO  
250,Tokelau,,TK,TKL  
251,Tonga,,TO,TON  
252,Trinidad and Tobago,,TT,TTO  
253,Tunisia,,TN,TUN  
254,Turkmenistan,,TM,TKM  
255,Turks and Caicos Islands,,TC,TCA  
256,Tuvalu,,TV,TUV  
257,United States Minor Outlying Islands,,UM,UMI  
258,Uruguay,,UY,URY  
259,Vanuatu,,VU,VUT  
260,Viet Nam,,VN,VNM  
261,Virgin Islands - British,,VG,VGB  
262,Virgin Islands - U.S.,,VI,VIR  
263,Wallis and Futuna,,WF,WLF  
264,Western Sahara,,EH,ESH  
265,Yemen,,YE,YEM  
266,Zambia,,ZM,ZMB  
267,Zimbabwe,,ZW,ZWE  
