<h1>TradingView Data Scrapper</h1>
  <h3><i>Scrap the timeframe you want!</i></h3>
  
  <body>
    <p><br>
    <b>Step 1:</b> Go to your tradingview account and copy paste the below code on your pine script.
      ![image](https://user-images.githubusercontent.com/20045975/153050751-5d8c77ab-7fb9-446c-b13b-f3e70a690f1b.png)

    indicator(title="Time Show", shorttitle="TimeOnly", overlay=true, timeframe="", timeframe_gaps=true)
    len = input.int(9, minval=1, title="Length")
    src = input(close, title="Source")
    offset = input.int(title="Offset", defval=0, minval=-500, maxval=500)
    out = ta.ema(src, len)
    plot(out, title="EMA", color=color.blue, offset=offset)
    plot(series=time, color=color.blue,title="Bar close time")
      
  </p></body>
