#21st December 2018

New function:
if you set on your config file this:
```
"no_microblocks":"no_pool_mining_send_report",   -> send a abuse
"no_microblocks":"no_pool_mining",               -> switch to solo mining if no other pool is avail
```
it will stop mining on that pool, app will check both pool and real node value and switches to an other pool.

## Done:
* stratum auth
* get the work
* working on how to send the work, order of json string

#19th December 2018
```
mining_pools array found size 1
rpc_url: stratum+tcp://ae.f2pool.com:7898
user: ak_XoongvC5xDqBCwdLr3ok1SzK3xEMFVwQ1sA7vj1guBd99HFjQ
pass: x
B: rpc_url: stratum+tcp://ae.f2pool.com:7898
B: stratum_url: ae.f2pool.com
B: sockaddr_url: ae.f2pool.com
B: stratum_port: 7898
[New Thread 0x7ffff1c6a700 (LWP 53636)]
BitCaine5: 02 started -------------------- > [0]0/BC5_sRead < -------------------------pool->rpc_url           : stratum+tcp://ae.f2pool.com:7898
pool->sockaddr_url      : ae.f2pool.com
pool->stratum_url       : ae.f2pool.com
pool host name          : ae.f2pool.com
pool h_addrtype         : 2
pool h_aliases          : 0x55555579bea0
pool h_length           : 4
pool h_addr_list[0]   : 203.107.32.162
main: BitCaine5: Step 2a Probing for an alive pool. We have at total [1] pools
[New Thread 0x7ffff0e4d700 (LWP 53637)]
BitCaine5: 07 started -------------------- > 0/Pools < -------------------------
SEND_OK WORKS
socket_full TRUE
stratum_return_message:
 {"id":0,"result":[[["mining.set_difficulty","mining.set_difficulty"],["mining.notify","mining.notify"]],"00002560",4],"error":null} 
stratum_return_message OK
END initiate_stratum ret is: initiate stratum OK
We need a stratum restart [1316]
[New Thread 0x7fffebfff700 (LWP 53638)]
BitCaine5: 02 started -------------------- > [0]0/BC5_sRead < -------------------------Pool sends a work update:
 {"id":null,"method":"mining.notify","params":["2acdb63b80934e5958d","708639c366634f59ffb3132a913f4997ec87f413f6b6cd2082617630ea2cc1ad",10397,"1e10df05",false]}
still working on old block
[New Thread 0x7fffeb7fe700 (LWP 53639)]
Have set pool global
BitCaine5: 01 started -------------------- > 0/BC5_sSend < -------------------------
```
#14th December 2018
```
./getBlock
We check now for CA certificates and make a miners CA cert
We found miner CA cert

 ok: request data from http://18.195.109.60:3013/v2/blocks/top 
my_text 

 {"key_block":{"beneficiary":"ak_2iBPH7HUz3cSDVEUWiHg76MZJ6tZooVNBmmxcgVK6VV8KAE688","hash":"kh_2HDMti3GdS2VCxcpzmeksHe2D7RpuGwPkWTVFbso5VhRTW4tns","height":7992,"miner":"ak_2WXyp6tUijZhKfcYUYLCZENn3HH1EbZJAgAFxVVTcwMyQGL2Vv","nonce":14970587065923496666,"pow":[6802071,26499778,56218796,102282082,107600749,140731739,165116812,182212473,184112405,186997262,192576180,209180932,213913030,226053824,236746368,245897490,271183548,274465531,277160455,277232238,278358521,290223804,290955646,301230179,301657270,317105180,342692935,377582442,412597951,418822455,426562479,448560615,468406756,469128118,471236379,480592786,482178345,490137129,503754083,522770864,529000328,530765352],"prev_hash":"kh_DpEaEmN9Y3bAghBaCdUJ8DFJPyCDEQgQh8A6ByaVY2os8LEov","prev_key_hash":"kh_DpEaEmN9Y3bAghBaCdUJ8DFJPyCDEQgQh8A6ByaVY2os8LEov","state_hash":"bs_418NRzZDoqRyJ1FqsHauHaBZCoSs76j1Ya6zX2X8VUvm5dCMN","target":539545912,"time":1544798004571,"version":1}} 

We found a micro block 
We check now for CA certificates and make a miners CA cert
We found miner CA cert

 ok: request data from localhost:3013/v2/blocks/top 
my_text 

 {"micro_block":{"hash":"mh_29pMn571RVZvGkPwGjJtnm7VRRMEN1BKskXtCWESN8SHFNMBs7","height":8075,"pof_hash":"no_fraud","prev_hash":"mh_2kDWK9fK1vySJtrwyLEbjT6Adz9ucuuKTeQobZjv2mS8JEpqp5","prev_key_hash":"kh_2W3bf3c12UpgDivwn15V22iVTKhD2XFX3a1ghVNhsQGz733H9Q","signature":"sg_L8hsqwBYeVkqQH6aSEfnPFdunaMGdwwk4TMLUjykT3taK7EERndeCaTPtVhwjuj5dJ7Dutoezq6a8KgeTwkGbQxMWS2Uu","state_hash":"bs_2Gv3PEE3B2KohhSfHmoMucfkKE2BemVaq8NFhFBfqmsE2HWYVy","time":1544798088478,"txs_hash":"bx_2Xy1Atb89dtB2iwfc51kJvC4taCjcvAaeRQR3naGt4i5NyB2e","version":1}} 

MB hash [mh_29pMn571RVZvGkPwGjJtnm7VRRMEN1BKskXtCWESN8SHFNMBs7] 
MB height [8075] 
MB pof_hash [no_fraud] 
MB prev_hash [mh_2kDWK9fK1vySJtrwyLEbjT6Adz9ucuuKTeQobZjv2mS8JEpqp5] 
MB prev_key_hash [kh_2W3bf3c12UpgDivwn15V22iVTKhD2XFX3a1ghVNhsQGz733H9Q] 
MB signature [sg_L8hsqwBYeVkqQH6aSEfnPFdunaMGdwwk4TMLUjykT3taK7EERndeCaTPtVhwjuj5dJ7Dutoezq6a8KgeTwkGbQxMWS2Uu] 
MB state_hash [bs_2Gv3PEE3B2KohhSfHmoMucfkKE2BemVaq8NFhFBfqmsE2HWYVy] 
MB time [1544798088478] 
MB txs_hash [bx_2Xy1Atb89dtB2iwfc51kJvC4taCjcvAaeRQR3naGt4i5NyB2e] 
MB version [1] 
license_key: 555336767631314D6476557173763135597751497972655378314A545A31313431505143785350577766553D
MinerConfigPath: $HOME/BitCaine5/my_farm.conf
compute_node array found size 4
cn_ip:172.16.16.124
auto_detect: all
card_type: nvidia
card_port: all
cpu_use: (null)
cn_ip:172.16.16.128
auto_detect: 3
card_type: nvidia
card_port: 0,1,4
cpu_use: (null)
cn_ip:172.16.16.131
auto_detect: all cards
card_type: amd
card_port: all
cpu_use: (null)
cn_ip:172.16.16.131
auto_detect: cpu
card_type: (null)
card_port: all
cpu_use: 75%
```
