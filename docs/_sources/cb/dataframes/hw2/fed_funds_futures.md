# Dataframe: `hw2:fed_funds_futures` - 30-Day Fed Funds Futures (ZQ)

Daily open, high, low, close, and volume for every listed ZQ contract, pulled from Databento's GLBX.MDP3 (CME Globex) dataset with the parent symbol ZQ.FUT and the ohlcv-1d schema. Columns: date (tz-naive trading date), symbol, open, high, low, close, volume. A contract settles at 100 minus the calendar-day average effective fed funds rate over its month, so 100 - close is the market-implied average rate in percent. The file also contains calendar spreads (symbols like ZQU6-ZQZ6); keep only outright contracts with fedwatch.filter_outright_contracts. Thinly traded far-dated contracts may have no bar on some days.


## DataFrame Glimpse

```
Rows: 11751
Columns: 7
$ date   <datetime[ns]> 2026-10-25 00:00:00
$ symbol          <str> 'ZQF7'
$ open            <f64> 95.895
$ high            <f64> 95.895
$ low             <f64> 95.89
$ close           <f64> 95.895
$ volume          <u64> 396


```

## Dataframe Manifest

| Dataframe Name                 | 30-Day Fed Funds Futures (ZQ)                                                          |
|--------------------------------|--------------------------------------------------------------------------------------|
| Dataframe ID                   | [fed_funds_futures](../dataframes/hw2/fed_funds_futures.md)                                       |
| Sources                        | CME Group                                          |
| Providers                      | Databento                                        |
| Provider Links                 | https://databento.com/                                   |
| Tags                           | Monetary Policy, Futures, Fed Funds, Fedwatch                                             |
| Access Types                   |                                       |
| How is data pulled?            | Databento API via Python                                                   |
| Data available up to (min)     | 2026-10-25 00:00:00                                                             |
| Data available up to (max)     | 2026-10-25 00:00:00                                                             |
| Dataframe Path                 | C:\Users\wsq\Desktop\Uchicago\Finm32800\hw2-Austinai123\_data\fed_funds_futures.parquet                                             |


**Linked Charts:**


- [hw2:fedwatch_latest_forecast](../../charts/hw2.fedwatch_latest_forecast.md)



## Pipeline Manifest

| Pipeline Name                   | HW 2: The Yield Curve and the Policy Path                       |
|---------------------------------|--------------------------------------------------------|
| Pipeline ID                     | [hw2](../../../index.md)              |
| Maintainer                      | Jeremiah Bejarano               |
| Contributors                    | Jeremiah Bejarano |
| Repository                     | https://github.com/hw-finm-32800/hw2                  |
| Pipeline Web Page               | <a href="file://C:/Users/wsq/Desktop/Uchicago/Finm32800/hw2-Austinai123/docs/index.html">Pipeline Web Page      |
| Date of Last Code Update        | 2026-10-26 14:45:56           |
| OS Compatibility                | Windows, Linux, macOS |
| Linked Dataframes               |  [hw2:crsp_treasury_consolidated](../../dataframes/hw2/crsp_treasury_consolidated.md)<br>  [hw2:fed_yield_curve](../../dataframes/hw2/fed_yield_curve.md)<br>  [hw2:fed_funds_futures](../../dataframes/hw2/fed_funds_futures.md)<br>  |


**Build Commands:**
```
doit

```

