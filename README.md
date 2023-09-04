# Ethereum's Proposer-Builder Separation: Promises and Realities 

This repository provides the aggregate data set created for the paper 'Ethereum's Proposer-Builder Separation: Promises and Realities'.

The aggregate data set is provided in four files: 
- data.pkl is a pandas dataframe with block level PBS data
- relaysBlockDict.pickle is a dictionary that indicates for each block which relay(s) claim it
- relaysDict.pickle is a dictionary that indicates for each relay which blocks it claims
- privateNonPBS.pkl is a pandas dataframe with all private transactions in non-PBS blocks

We further provide the scrips used for the data analysis in the following notebook: PBSAnalysis.ipynb.
