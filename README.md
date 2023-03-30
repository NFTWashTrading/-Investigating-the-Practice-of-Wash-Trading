# code&data of the paper: The Dark Side of NFTs: A Large-Scale Empirical Study of Wash Trading
source: https://drive.google.com/drive/folders/1yzLbQURsv-bc9EU4q5BR9cmDmGCodzlY?usp=sharing

## data
#### collectionRaw.zip:
  the raw data of event sequences of 285 NFT collections with *address inconsistency*, *timestamp error* and *fake events* collected by *OpenSea API*
#### collectionPreprocessed.zip:
  the preprocessed data of event sequences of 285 NFT collections with improved *consisRate*
#### ERC-20Price.zip:
  historical market price of 2,982 ERC-20 tokens collected by *CoinGecko API* 
#### pickle_files.zip: 
  * wins_timeWindowInfo.pickle: segemented time windows for event sequences
  * Txn_relatedNormalTransactions.pickle: selected block transactions
  * Txn20_relatedERC20Transactions.pickle: selected ERC-20 transactions
  * real_cir_circlesofTransactionSequences.pickle: details of all cycles in each time window 
  * mr_mergeTransactionSequences.pickle: details of the merged edges 
  * g_graphTransactionSequences.pickle: directed graph constructed by merged edges.
  * fs_validfile.pickle: names of NFT collections
  * flow_relatedNormalTransactions.pickle: details for selected block transactions 
  * flow20_relatedERC20Transactions.pickle: details for selected ERC-20 transactions
  * eth20P_erc20TokenHistoricalPrice.pickle: histroical price for ERC-2O tokens

## code
#### collection_slug.py
to run collection_slug.py to retrieve event sequences of NFT collections:
* first: change the file name with the *collection_slug* of the NFT collection (See example in the following figure / retrieve collecton_slug via *OpenSea API*)
![image](https://user-images.githubusercontent.com/128060644/228736139-732f90ef-27b4-4f12-b35c-2a0871a9cc2c.png)
* then: python3 -u collection_slug.py -s start_time -e end_time >collection_slug.log 2>&1
#### preprocess&overview.py
to preprocess the event sequences:
* python3 preprocess&overview.py
