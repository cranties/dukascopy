# dukascopy - Dukascopy Bank SA historical data downloader

Finding good Forex data is difficult or expensive. Dukascopy has made available an excellent [web tool](https://www.dukascopy.com/swiss/english/marketwatch/historical/) to download tick data for a large a variety of 
Forex, CFD and commodities. This is awesome and extremely useful for people, like me, trying to study the Forex market. 
However, it takes a lot of time to download a large data set from the website because you can download only one day per time. In order to solve this issue, I created **dukascopy**.  

**dukascopy** is a small terminal application that can be used to download ticks for a given date range from the Dukascopy historical data feed for one or more symbols. **dukascopy** takes advantage of python threads and coroutine in order to speed up the download. It takes roughly 10m to download tick data for one year for a given instrument. 

Key features :
 - Ticks data with volumes
 - Candle formatting with different time-frames ( from 1 minute to 1 day )
 - CSV output
 - multi-thread support
 - Large variety of symbols

This is what **dukascopy** looks like:

## Installation

**dukascopy** requires python 3.5 and request 2.0.1. It can be installed using `pip` as follows:

```
pip install dukascopy
```

## Usage
```
 usage: dukascopy [options]

 positional arguments:
    SYMBOLS               symbol list using format EURUSD EURGBP 

 optional arguments:
     -h           show help message and exit 
     -v           show program's version number and exit
     -d DAY       specific day format YYYY-MM-DD (default today)
     -s STARTDATE start date format YYYY-MM-DD (default today)
     -e ENDDATE   end date format YYYY-MM-DD (default today)
     -c CANDLE    use candles instead of ticks. Accepted values M1 M2 M5 M10 M15 M30 H1 H4 D1
     -f FOLDER    the dowloaded data will be saved in FOLDER (default '.')
     -t THREAD    number of threads (default 10)
     --header     include CSV header (default false)
```


This software is licensed under the MIT License.

Copyright Andrea Monni, 2020.

Permission is hereby granted, free of charge, to any person obtaining a
copy of this software and associated documentation files (the
"Software"), to deal in the Software without restriction, including
without limitation the rights to use, copy, modify, merge, publish,
distribute, sublicense, and/or sell copies of the Software, and to permit
persons to whom the Software is furnished to do so, subject to the
following conditions:

The above copyright notice and this permission notice shall be included
in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS
OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN
NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM,
DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR
OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE
USE OR OTHER DEALINGS IN THE SOFTWARE.



