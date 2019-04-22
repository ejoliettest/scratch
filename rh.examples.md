 3920  ./rh.sh 'https://api.robinhood.com/midlands/movers/sp500/?direction=up'
 3921  ./rh.sh 'https://api.robinhood.com/midlands/movers/sp500/?direction=down' > mover-down.json
 3922  ./rh.sh 'https://api.robinhood.com/quotes/FE/'
 3925  ./rh.sh 'https://api.robinhood.com/quotes/FE/' | \jq '.symbol'
 3926  ./rh.sh 'https://api.robinhood.com/quotes/FE/' 
 3927  ./rh.sh 'https://api.robinhood.com/quotes/FE/' | \jq '.symbol, .last*'
 3928  ./rh.sh 'https://api.robinhood.com/quotes/FE/' | \jq '.symbol, .last_trade_price, .instrument'
 3929  ./rh.sh https://api.robinhood.com/quotes/FE/
 3930  ./rh.sh https://api.robinhood.com/instruments/beaf5459-e4e8-4b3b-b933-faf50a18bcd4/
 3931  ./rh.sh https://api.robinhood.com/marketdata/earnings/?symbol=nvda
 3932  ./rh.sh https://api.robinhood.com/marketdata/earnings/?symbol=NVDA
 3933  ./rh.sh https://api.robinhood.com/marketdata/earnings/?symbol=NVDA >earning-nvda.json
 3934  ./rh.sh https://api.robinhood.com/marketdata/earnings/?symbol=NVDA |\jq '.year, .quarter, .date'
 3935  ./rh.sh https://api.robinhood.com/marketdata/earnings/?symbol=NVDA |\jq '.[] |.year, .quarter, .date'
 3936  ./rh.sh https://api.robinhood.com/marketdata/earnings/?symbol=NVDA |\jq '.[] |.year[], .quarter[], .date[]'
 3937  ./rh.sh https://api.robinhood.com/marketdata/earnings/?symbol=NVDA |\jq '.year[], .quarter[], .date[]'
 3938  ./rh.sh https://api.robinhood.com/marketdata/earnings/?symbol=NVDA | grep 2019
 3939  ./rh.sh https://api.robinhood.com/marketdata/earnings/?symbol=NVDA | \jq '.[]'
 3940  ./rh.sh https://api.robinhood.com/marketdata/earnings/?symbol=NVDA | \jq '.[1]'
 3941  ./rh.sh https://api.robinhood.com/marketdata/earnings/?symbol=NVDA | \jq '.[], .date'
 3942  ./rh.sh https://api.robinhood.com/marketdata/earnings/?symbol=NVDA | \jq '.[], .date[]'
 3943  ./rh.sh https://api.robinhood.com/marketdata/earnings/?symbol=NVDA | \jq '.[].report'
 3944  ./rh.sh https://api.robinhood.com/marketdata/earnings/?symbol=NVDA | \jq '.report[]'
 3945  ./rh.sh https://api.robinhood.com/marketdata/earnings/?symbol=NVDA | \jq '.report'
 3946  ./rh.sh https://api.robinhood.com/marketdata/earnings/?symbol=NVDA | \jq '.report[0]'
 3947  ./rh.sh https://api.robinhood.com/marketdata/earnings/?symbol=NVDA | \jq '.report[0][]'
 3948  ./rh.sh https://api.robinhood.com/marketdata/earnings/?symbol=NVDA | \jq '.report[1][]'
 3949  ./rh.sh https://api.robinhood.com/marketdata/earnings/?symbol=NVDA | \jq '.1[]'
 3950  ./rh.sh https://api.robinhood.com/marketdata/earnings/?symbol=NVDA | \jq '.[]'
 3951  ./rh.sh https://api.robinhood.com/marketdata/earnings/?symbol=NVDA | \jq '.date[]'
 3952  ./rh.sh https://api.robinhood.com/marketdata/earnings/?symbol=NVDA | \jq '.date'
 3953  ./rh.sh https://api.robinhood.com/marketdata/earnings/?symbol=NVDA | \jq '.[].date'
 3954  ./rh.sh https://api.robinhood.com/marketdata/earnings/?symbol=NVDA | \jq '.[].date[]'
 3955  ./rh.sh https://api.robinhood.com/marketdata/earnings/?symbol=NVDA | \jq '.symbol[].date[]'
 3956  ./rh.sh https://api.robinhood.com/marketdata/earnings/?symbol=NVDA | \jq '.symbol[].date'
 3957  ./rh.sh https://api.robinhood.com/marketdata/earnings/?symbol=NVDA | \jq '.[]'
 3958  ./rh.sh https://api.robinhood.com/marketdata/earnings/?symbol=NVDA | \jq '.[].year'
 3960  ./rh.sh https://api.robinhood.com/marketdata/earnings/?symbol=NVDA | \jq '.[].year'
 3961  ./rh.sh https://api.robinhood.com/marketdata/earnings/?symbol=NVDA | \jq '.[].year[]'
 3962  ./rh.sh https://api.robinhood.com/marketdata/earnings/?symbol=NVDA | \jq '.[].report[].year'
 3963  ./rh.sh https://api.robinhood.com/marketdata/earnings/?symbol=NVDA | \jq '.[].report[]'
 3964  ./rh.sh https://api.robinhood.com/marketdata/earnings/?symbol=NVDA | \jq '.[].report'
 3965  ./rh.sh https://api.robinhood.com/marketdata/earnings/?symbol=NVDA | \jq '.[]'
 3966  ./rh.sh https://api.robinhood.com/marketdata/earnings/?symbol=NVDA | \jq '.[].quater'
 3967  ./rh.sh https://api.robinhood.com/marketdata/earnings/?symbol=NVDA | \jq '.[].quarter'
 3968  ./rh.sh https://api.robinhood.com/marketdata/earnings/?symbol=NVDA | \jq '.[]'
 3969  ./rh.sh https://api.robinhood.com/accounts/
 3970  ./rh.sh https://api.robinhood.com/positions
 3971  ./rh.sh https://api.robinhood.com/positions/
 3972  ./rh.sh https://api.robinhood.com/positions/ > positions.json
 3973  ./rh.sh https://api.robinhood.com/instruments/bc06e768-0955-49f2-ab45-2e07cab0fbe2/ |\jq '.quote, .fundamentals'
 4022  ./rh.sh https://api.robinhood.com/instruments/bc06e768-0955-49f2-ab45-2e07cab0fbe2/ |\jq '.quote, .fundamentals' 
 4023  ./rh.sh https://api.robinhood.com/instruments/bc06e768-0955-49f2-ab45-2e07cab0fbe2/ |\jq '.quote, .fundamentals' |xargs -n 1 ./rh.sh 
 4024  ./rh.sh https://api.robinhood.com/instruments/bc06e768-0955-49f2-ab45-2e07cab0fbe2/ |\jq '.quote, .fundamentals' |xargs -n 1 ./rh.sh |\jq '.symbol, .last_trade_price, .dividend_yield'
 4025  ./rh.sh https://api.robinhood.com/positions/|\jq '.instrument'
 4026  ./rh.sh https://api.robinhood.com/positions/|\jq '.instrument[]'
 4027  ./rh.sh https://api.robinhood.com/positions/|\jq '.[].instrument'
 4028  ./rh.sh https://api.robinhood.com/positions/|\jq '.[].instruments'
 4029  ./rh.sh https://api.robinhood.com/positions/|\jq '.[]'
 4030  ./rh.sh https://api.robinhood.com/positions/|\jq '.[].instrument'
 4031  ./rh.sh https://api.robinhood.com/positions/|\jq '.[].[1]'
 4032  ./rh.sh https://api.robinhood.com/positions/|\jq '.[1]'
 4073  cat positions.json |jq .results[].instrument|xargs ./rh.sh x.html|jq '.quote, .fundamentals' |xargs -n 1 ./rh.sh y.html |\jq '.symbol, .last_trade_price'
 4076  cat positions.json |jq .results[0].instrument|xargs ./rh.sh x.html|jq '.quote, .fundamentals' 
 4077  cat positions.json |jq .results[0].instrument|xargs ./rh.sh 
 4078  cat positions.json |jq .results[0].instrument|xargs -n 1 ./rh.sh 
 4079  cat positions.json |jq .results[0].instrument|xargs -n 1 ./rh.sh x.html|jq '.quote, .fundamentals' 
 4080  cat positions.json |jq .results[0].instrument|xargs -n 1 ./rh.sh
 4081  cat positions.json |jq .results[0].instrument|xargs -n 1 ./rh.sh|jq []
 4082  cat positions.json |jq .results[0].instrument|xargs -n 1 ./rh.sh|jq .[]
 4083  cat positions.json |jq .results[0].instrument|xargs -n 1 ./rh.sh> x.html
 4085  cat positions.json |jq .results[0].instrument|xargs -n 1 ./rh.sh|jq '.symbol, .quote, .fundamentals'
 4086  cat positions.json |jq .results[0].instrument|xargs -n 1 ./rh.sh|jq '.quote, .fundamentals'
 4091  cat positions.json |jq .results[].instrument|xargs -n 1 ./rh.sh|jq '.quote, .fundamentals'
 4093  cat positions.json |jq .results[200].instrument|xargs -n 1 ./rh.sh|jq '.quote, .fundamentals'
 4094  cat positions.json |jq .results[290].instrument|xargs -n 1 ./rh.sh|jq '.quote, .fundamentals'
 4095  cat positions.json |jq .results[290].instrument|xargs -n 1 ./rh.sh
 4326  ./rh.sh https://api.robinhood.com/positions/
 4328  ./rh.sh https://api.robinhood.com/positions/
 4329  history |grep ./rh.sh
 4330  history |grep ./rh.sh > rh.examples.md
