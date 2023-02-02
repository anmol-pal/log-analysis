# log-analysis
## Data Wrangling

### Data is collected through a website using curl to their access-logs
[log-file webserverlog](https://drive.google.com/file/d/1IygYCeTaxSL2p6uJvZNqeCg3FgNvC9F6/view?usp=sharing)
[website link](http://www.almhuette-raith.at/apache-log/access.log)
```
Timestamp       Host
cat part-00000-e3a8b0af-89cb-4326-bf86-018fe738bd2a-c000.csv | less
""      ""
19/Dec/2020:13:57:26 +0100      13.66.139.0
19/Dec/2020:14:08:06 +0100      157.48.153.185
19/Dec/2020:14:08:08 +0100      157.48.153.185
19/Dec/2020:14:14:26 +0100      216.244.66.230
19/Dec/2020:14:16:44 +0100      54.36.148.92
19/Dec/2020:14:29:21 +0100      92.101.35.224
19/Dec/2020:14:58:59 +0100      73.166.162.225
19/Dec/2020:14:58:59 +0100      73.166.162.225
19/Dec/2020:15:09:30 +0100      54.36.148.108
19/Dec/2020:15:09:31 +0100      54.36.148.1
19/Dec/2020:15:16:50 +0100      162.158.203.24
19/Dec/2020:15:22:40 +0100      35.237.4.214
19/Dec/2020:15:23:10 +0100      42.236.10.125
19/Dec/2020:15:23:11 +0100      42.236.10.125
19/Dec/2020:15:23:11 +0100      42.236.10.125
19/Dec/2020:15:23:11 +0100      42.236.10.125
19/Dec/2020:15:23:11 +0100      42.236.10.117
19/Dec/2020:15:23:11 +0100      42.236.10.114
19/Dec/2020:15:23:11 +0100      42.236.10.114
19/Dec/2020:15:23:12 +0100      42.236.10.125
19/Dec/2020:15:23:12 +0100      42.236.10.117
19/Dec/2020:15:23:12 +0100      42.236.10.117
19/Dec/2020:15:23:12 +0100      42.236.10.114
19/Dec/2020:15:23:12 +0100      42.236.10.114
19/Dec/2020:15:23:12 +0100      42.236.10.125
19/Dec/2020:15:23:12 +0100      42.236.10.114
```
### Data wrangling code [here](src/data_wrangling.ipynb)
CSV Produced after data wrangling [here](https://drive.google.com/drive/folders/1K6OSN1qUR092VXOZKFXkVPS9I-dTEIdp?usp=share_link)

## Data Transformation
Fetching Geographic metrics from these IPs here](src/generating_location_info.ipynb) 
IP-Batch [API](http://ip-api.com/batch)

Transformed CSV Generated [here](https://drive.google.com/file/d/1nP3Z1SQogSnYFFbRy_UUArixgKJJOknD/view?usp=sharing)
```
cat countryLargeFineGran.csv | less
,Host,Country,CountryCode,City,Timezone,Lat,Lon,Reg
0,13.66.139.0,United States,US,Quincy,America/Los_Angeles,47.233,-119.852,Washington
1,157.48.153.185,India,IN,Hyderabad,Asia/Kolkata,17.411,78.4487,Telangana
2,216.244.66.230,United States,US,Tukwila,America/Los_Angeles,47.4931,-122.294,Washington
3,54.36.148.92,France,FR,Roubaix,Europe/Paris,50.6916,3.20151,Hauts-de-France
4,92.101.35.224,Russia,RU,Severodvinsk,Europe/Moscow,64.5676,39.8018,Arkhangelskaya
5,73.166.162.225,United States,US,Houston,America/Chicago,29.6924,-95.513,Texas
6,54.36.148.108,France,FR,Roubaix,Europe/Paris,50.6916,3.20151,Hauts-de-France
7,54.36.148.1,France,FR,Roubaix,Europe/Paris,50.6916,3.20151,Hauts-de-France
8,162.158.203.24,Germany,DE,Hamburg,Europe/Berlin,53.551,9.9936,Hamburg
9,35.237.4.214,United States,US,North Charleston,America/New_York,32.8771,-80.013,South Carolina
10,42.236.10.125,China,CN,Zhengzhou,Asia/Shanghai,34.7472,113.625,Henan
11,42.236.10.117,China,CN,Zhengzhou,Asia/Shanghai,34.7472,113.625,Henan
12,42.236.10.114,China,CN,Zhengzhou,Asia/Shanghai,34.7472,113.625,Henan
13,191.102.167.138,United States,US,Orangeburg,America/New_York,33.4918,-80.8556,South Carolina
14,54.36.149.55,France,FR,Roubaix,Europe/Paris,50.6916,3.20151,Hauts-de-France
15,95.217.229.86,Finland,FI,Helsinki,Europe/Helsinki,60.1719,24.9347,Uusimaa
16,182.239.117.249,Hong Kong,HK,Central,Asia/Hong_Kong,22.2908,114.1501,Central and Western District
17,66.249.64.41,United States,US,Mountain View,America/Los_Angeles,37.422,-122.084,California
18,157.48.208.79,India,IN,Hyderabad,Asia/Kolkata,17.411,78.4487,Telangana
19,162.210.196.129,United States,US,Manassas,America/New_York,38.7514,-77.5251,Virginia
20,66.249.66.158,United States,US,Mountain View,America/Los_Angeles,37.422,-122.084,California
21,45.145.161.12,Germany,DE,Berlin,Europe/Berlin,52.5196,13.4069,Land Berlin
22,45.132.51.36,Germany,DE,Berlin,Europe/Berlin,52.5196,13.4069,Land Berlin
23,45.138.145.131,Germany,DE,Berlin,Europe/Berlin,52.5196,13.4069,Land Berlin
24,45.144.0.179,Germany,DE,Berlin,Europe/Berlin,52.5196,13.4069,Land Berlin
```

