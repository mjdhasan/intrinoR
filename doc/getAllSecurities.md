### `getAllSecurities`
***
***

### Description

 Returns all Securities to which you have access. When parameters are specified, returns matching Securities.

### Usage
```r
getAllSecurities(opts = list())
```

### Arguments
Argument      |Description
------------- |----------------
```opts```     |     named list Optional parameters
```opts$active```     |     Boolean When true, return securities that are active. When false, return securities that are not active. A security is considered active if it has traded or has had a corporate action in the past 30 days, and has not been merged into another security (such as due to ticker changes or corporate restructurings).
```opts$delisted```     |     Boolean When true, return securities that have been delisted from their exchange. Note that there may be a newer security for the same company that has been relisted on a differente exchange. When false, return securities that have not been delisted.
```opts$code```     |     String Return securities classified with the given code (<a href=&quot;/documentation/security_codes&quot; target=&quot;_blank&quot;>reference</a>).
```opts$currency```     |     String Return securities traded in the given 3-digit ISO 4217 currency code (<a href=&quot;https://en.wikipedia.org/wiki/ISO_4217&quot; target=&quot;_blank&quot;>reference</a>).
```opts$ticker```     |     String Return securities traded with the given ticker. Note that securities across the world (and through time) may trade with the same ticker but represent different companies. Use this in conjuction with other parameters for more specificity.
```opts$name```     |     String Return securities with the given text in their name (not case sensitive).
```opts$composite_mic```     |     String Return securities classified under the composite exchange with the given Market Identification Code (MIC). A composite exchange may or may not be a real exchange.  For example, the USCOMP exchange (our only composite exchange to date) is a combination of exchanges with the following MICs: ARCX, XASE, XPOR, FINR, XCIS, XNAS, XNYS, BATS.  This composite grouping is done for user convenience.  At this time, all US securities are classified under the composite exchange with MIC USCOMP.  To query for specific US exchanges, use the exchange_mic parameter below.
```opts$exchange_mic```     |     String The MIC code of the exchange where the security is actually traded.
```opts$stock_prices_after```     |     Date Return securities with end-of-day stock prices on or after this date.
```opts$stock_prices_before```     |     Date Return securities with end-of-day stock prices on or before this date.
```opts$cik```     |     String Return securities belonging to the company with the given Central Index Key (CIK).
```opts$figi```     |     String Return securities with the given Exchange Level FIGI (<a href=&quot;https://www.openfigi.com/about&quot; target=&quot;_blank&quot;>reference</a>).
```opts$composite_figi```     |     String Return securities with the given Country Composite FIGI (<a href=&quot;https://www.openfigi.com/about&quot; target=&quot;_blank&quot;>reference</a>).
```opts$share_class_figi```     |     String Return securities with the given Global Share Class FIGI (<a href=&quot;https://www.openfigi.com/about&quot; target=&quot;_blank&quot;>reference</a>).
```opts$figi_unique_id```     |     String Return securities with the given FIGI Unique ID (<a href=&quot;https://www.openfigi.com/about&quot; target=&quot;_blank&quot;>reference</a>).
```opts$include_non_figi```     |     Boolean When true, include securities that do not have a FIGI. By default, this is false. If this parameter is not specified, only securities with a FIGI are returned. (default to false)
```opts$page_size```     |     Number = 100 The number of results to return
### Value

 securities data.frame 

### Seealso

 Other security endpoints: [`getIndicesDataPointHistory`](getIndicesDataPointHistory.md) ,
  [`getSecurityById`](getSecurityById.md) ,
  [`getSecurityDataPointHistory`](getSecurityDataPointHistory.md) ,
  [`getSecurityDataPointNumber`](getSecurityDataPointNumber.md) ,
  [`getSecurityDataPointText`](getSecurityDataPointText.md) ,
  [`getSecurityDividendsLatest`](getSecurityDividendsLatest.md) ,
  [`getSecurityEarningsLatest`](getSecurityEarningsLatest.md) ,
  [`getSecurityIntradayPrices`](getSecurityIntradayPrices.md) ,
  [`getSecurityRealtimePrice`](getSecurityRealtimePrice.md) ,
  [`getSecurityStockPrices`](getSecurityStockPrices.md) ,
  [`getSecurityZacksAnalystRatingsSnapshot`](getSecurityZacksAnalystRatingsSnapshot.md) 

