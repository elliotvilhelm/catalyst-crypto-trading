#### Install
`conda env create -f python3.6-environment.yml`
`source activate catalyst`
`catalyst --version`

##### OSX issues I ran into
Missing `<algorithm>`
add to ~/.profile
`export CPATH=/Library/Developer/CommandLineTools/usr/include/c++/v1`
`source ~/.profile`

Move
```
- bcolz==1.2.1
- cchardet==2.1.1
```
To conda dependencies in .yml, this has been done in .yml.

#### Get Data
`catalyst ingest-exchange -x binance -i btc_usdt -f minute`
`catalyst ingest-exchange -x binance -f minute -i ltc_usdt`


#### Backtest
`catalyst run -f catalyst_dma.py -x bitfinex -s 2017-9-22 -e 2017-9-23 --capital-base 1000 --quote-currency usdt --data-frequency minute -o out.pickle`

or

`python catalyst_dma.py`


#### References
https://enigma.co/catalyst/beginner-tutorial.html





