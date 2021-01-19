# Fedetaed Learning on BlockChain

## Options

The default values for various paramters parsed to the experiment are given in ```options.py```. Details are given some
of those parameters:

* ```--model:```    Default: 'mlp'. Options: 'mlp', 'cnn'
* ```--global_round:```   Number of rounds of training.
* ```--idx``` The ID for training client.
* ```--iid:```      Distribution of data amongst users. Default set to IID. Set to 0 for non-IID.
* ```--num_users:```Number of users. Default is 100.
* ```--local_ep:``` Number of local training epochs in each user. Default is 10.
* ```--local_bs:``` Batch size of local updates in each user. Default is 10.
* ```--unequal:```  Used in non-iid setting. Option to split the data amongst users equally or unequally. Default set to
  0 for equal splits. Set to 1 for unequal splits.
  
## Usage
* To init global model on CNN :
```
python src/init_glocal.py --model=cnn 

```

* To run the federated experiment on CNN for i-th client
```
python src/init_glocal.py --model=cnn --global_round=10 --iid=1 --num_users=5 --idx=1
```