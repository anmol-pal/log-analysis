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