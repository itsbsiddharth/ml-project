# ML Project: Sentiment Analysis on Amazon Reviews

## Original Data and Transposition 

### Original data dictionary
res = {'A': {'neg': 0.1, 'neu': 0.8, 'pos': 0.1},
       'B': {'neg': 0.2, 'neu': 0.6, 'pos': 0.2}}
### Create DataFrame and transpose it
vaders = pd.DataFrame(res).T
print(vaders)
vaders = vaders.reset_index().rename(columns={'index': 'Id'})
print(vaders)
### Another DataFrame for merging
df = pd.DataFrame({'Id': ['A', 'B'], 'info': ['info1', 'info2']})
### Merge on 'Id'
vaders = vaders.merge(df, how='left')
print(vaders)
###After merging, the resulting DataFrame has clear and meaningful column names:
| Id | neg | neu | pos | info |
|----|-----|-----|-----|------|
| A  | 0.1 | 0.8 | 0.1 | info1|
| B  | 0.2 | 0.6 | 0.2 | info2|


![positive negative neutral Example Table](images/posnegneu_table.png)
