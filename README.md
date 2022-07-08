# Ripple-Dataset
This dataset is used for paper--Topology Analysis of the Ripple Payment Network

## 1. Introduction Environment
```
Linux version 5.13.0-52-generic
Ubuntu 20.04.4 LTS
```
## 2. Dataset Decompression

Due to the dataset being too big and GitHub will blocks push that exceed 100 MB. Therefore, we split this dataset to push it to Github.

The split command is below. It will split dataset it into 100M sized parts.
```bash
zip RippleDataset.zip --out RippleDatasetSplit.zip -s 100m
```
Then will create:
>
>RippleDatasetSplit.zip
> 
>RippleDatasetSplit.z01
> 
>RippleDatasetSplit.z02
>
>......


To extract them, you should first collect the files together and run the command to recreate your zip files. 
```bash
zip -F RippleDatasetSplit.zip --out RippleDataset.zip 
```
or
```bash
zip -s0 RippleDatasetSplit.zip --out RippleDataset.zip
```
Then you can simply use the below command to unzip files. 
```bash
unzip RippleDataset.zip
```

## 3. RippleData Details



The file named OriginalData-TransactionsPayment-69521100-70327501.csv, which is original data extracts all Payment Transactions from JSON files.

The file named OriginalData-TransactionsTrustSet-69521100-70327501.csv, which is original data extracts all TrustSet Transaction from JSON files.

The file named TransferNum_TransactionsPayment-69521100-70327501-result.csv, which stored dtat that converts the address of sender and receiver to the number from OriginalData-TransactionsPayment-69521100-70327501.csv.

The file named TransferNum_TransactionsTrustSet-69521100-70327501-result.csv, which stored data that converts the address of sender and receiver to the number from OriginalData-TransactionsTrustSet-69521100-70327501.csv.

The file named TransferNum_TransactionsPayment-69521100-70327501-result-Allsame-AddEdges.csv, which stored data that extracts all repeated transactions from TransferNum_TransactionsPayment-69521100-70327501-result.csv. In addition, this file adds the edges (from sender to receiver) in the last column.

The file named TransferNum_TransactionsTrustSet-69521100-70327501-result-Allsame-AddEdges.csv, which stored data that extracts all repeated transactions form TransferNum_TransactionsTrustSet-69521100-70327501-result.csv. In addition, this file adds the edges (from sender to receiver) in the last column.

The file named TransferNum_TransactionsPayment-69521100-70327501-result-Delsame.csv, which stored data that extract the no-repeat transaction and repeat transactions (only keep the first transactions) from TransferNum_TransactionsPayment-69521100-70327501-result.csv.

The file named TransferNum_TransactionsTrustSet-69521100-70327501-result-Delsame.csv, which stored data that extract the no-repeat transaction and repeat transactions (only keep the first transactions) from TransferNum_TransactionsTrustSet-69521100-70327501-result.csv.

