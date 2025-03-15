Classification of 43,621,232 Bitcoin Wallet addresses into 14 categories (following the classifications defined by BABD, cited below):
(1) Blackmail, (2) Cyber-Security Service, (3) Darknet Market, (4) Centralized Exchange, (5) P2P Financial Infrastructure Service, (6) P2P Financial Service, (7) Gambling, (8) Government Criminal Blocklist, (9) Money Laundering, (10) Ponzi Scheme, (11) Mining Pool, (12) Tumbler, (13) Individual Wallets, and (14) Unknown Service.

This database was made by combining info from four separate sources:
Aleš Janda, who operates WalletExplorer.com, generously offers an API which provides significant wallet classification and identification that he was able to determine. Mr. Janda determined the owners of wallets by registering for certain services and learning the addresses used by those services (like SatoshiDice) and then backed in to other wallet addresses by determining which wallets were merged together (similar to a shadow wallet address analysis done by others). However, WalletExplorer states it has not updated much data since 2016. Thus, the data available from WalletExplorer is largely contained in the first 425,000 blocks (block 425,000 was mined on August 13, 2016). This classification data constituted, by far, the largest portion of classification data in this dataset, with over 43 million wallet addresses being classified.
Preference was always given to WalletExplorer.com's classifications, as “Strong Addresses.”
Aleˇs Janda. Wallet explorer. https://www.walletexplorer.com/info.

Additionally, several datasets (in spreadsheets) identify and classify wallets: 

The largest of these spreadsheets available on Kaggle was made by Xiang, et al. They were able to classify 544,462 wallet addresses between blocks 585,000 (July 12, 2019) and 685,000  (May 26, 2021) into 13 classifications: (1) Blackmail, (2) Cyber-Security Service, (3) Darknet Market, (4) Centralized Exchange, (5) P2P Financial Infrastructure Service, (6) P2P Financial Service, (7) Gambling, (8) Government Criminal Blocklist, (9) Money Laundering, (10) Ponzi Scheme, (11) Mining Pool, (12) Tumbler, and (13) Individual Wallets. They used the WalletExplorer database and other governmental blocklist databases as their “strong addresses” and information from BitcoinAbuse.com (which now appears to be ChainAbuse.com) as “weak addresses” to train their AI models. The processes they used to identify and classify the wallets on their experimental sets resulted in a minimum F-1 score of 92.97%,  accuracy of 93.24%, precision of 92.80%, and recall of 93.24%. They accomplished this by using a framework consisting of two parts: a statistical indicator (SI), and a local structural indicator (LSI). The SI considered four indicator types, Pure Amount Indicator (PAI), Pure Degree Indicator (PDI), Pure Time Indicator (PTI), and Combination Indicator (CI). The SI considered 132 features to predict the classification \cite{xiang:babd}. For the LSI, they generated k-hop subgraphs with an algorithm, and then used various graph metrics and other features to predict the classification. 
Yiexin Xiang, Yuchen Lei, Ding Bao, Tiantian Li, Quingqing Yang, Wenmao Liu, Wei Ren, and Kim-Kwang Raymond Choo. Babd: A bitcoin address behavior dataset for pattern analysis. IEEE Transactions on Information Forensics and Security, (19):2171–85, 2024.
https://www.kaggle.com/datasets/lemonx/babd13

Michalski, et al., identified 8,808 addresses and classified them using machine learning techniques considering 149 features, into categories including (1) mining pools, (2) miners, (3) coinjoins, (4) gambling, (5) exchange, and (6) services. They analyzed the blocks between 520,850 and 520,950. They obtained training data from WalletExplorer.com and then used machine learning techniques including Evaluated Supervised Learning Algorithms. They determined that the Random Forest classification was the best method of classifying the wallets, and stated they obtained an F-score of 95%. Due to the small size of this dataset and the fact that only 100 blocks were covered by this dataset, I considered these classifications to be “weak addresses” for this work. The wallets they classified as “services” were added to my database as an “Unknown Service.”
Radoslaw Michalski, Daria Dziuba ltowska, and Piotr Macek. Bitcoin addresses and their categories. https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/KEWU0N

The US Office of Foreign Asset Control maintains a list of ‘sanctioned’ Bitcoin and other digital currency assets. Several Github contributors maintain a tool that extracts the Bitcoin addresses from this database. This added 390 wallet addresses to the dataset.
U.S. Treasury. Specially designated nationals list of the us office of foreign asset control. https://www.treasury.gov/ofac/downloads/sanctions/1.0/sdn_advanced.xml.
0xB10C, Michael Neale, and Yahiheb. https://github.com/0xB10C/ofac-sanctioned-digital-currency-addresses?tab=readme-ov-file

Due to the size of the dataset, the data is hosted on [www.kaggle.com/datasets/gregorywilder/combined-bitcoin-wallet-classification-dataset](https://www.kaggle.com/datasets/gregorywilder/bitcoin-wallet-classification-public-dataset)
