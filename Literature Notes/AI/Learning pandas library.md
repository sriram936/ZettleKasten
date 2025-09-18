Author: 
Source: Free Code Camp
## Pandas lec 1
## Pandas Series
1. import numpy as np && Import pandas as pd [Used to import numpy and pandas]
2. pd.Series([1,2,3])    [Used to create series from list]
	And they _look_ like simple Python lists or Numpy Arrays. But they're actually more similar to Python `dict`s.
	
	A Series has an `index`, that's similar to the automatic index assigned to Python's lists:
	But, in contrast to lists, we can explicitly define the index:
	
3. g7_pop.name = ' ' [Used for naming a series]
4. g7_pop.dtype [Used to know type of values in series]
5. g7_pop.values [array of elements  (numpy arrays)]
6. type() [Used to specify type of value is the variable, like series, numpy.ndarray, str etc]

7. g7_pop.index [Is used find index range or to assign index values]
8. pd.Series({
    'Canada': 35.467, 'France': 63.951, 'Germany': 80.94 }, name='G7 Population in millions')
	[We can create series from the dictionaries as well]
9. pd.Series(
    [35.467, 63.951, 80.94],
    index=['Canada', 'France', 'Germany'],
       'United States'],
    name='G7 Population in millions')   list+index+name at a time
10. pd.Series(g7_pop, index=['France', 'Germany', 'Italy', 'Spain'])  [Used to crreate series out of series]

## Index
1. g7_pop[canada]   [Used to locate value at the given Index]
2. g7_pop.iloc[3]   [Used to locate value at the given index position]
3. g7_pop[\['Italy', 'France' \]]  [Used to select multiple indexes]
4. g7_pop.iloc[\[0, 1\]]   [Used to select multiple indexes using ]
5. Slicing also works, but **important**, in Pandas, the upper limit is also included:
	 g7_pop['Canada': 'Italy']

## Conditional Selection (boolean arrays)
1. g7_pop > 70  ; g7_pop <150   [Returns true or false in place of values ]
2. g7_pop[g7_pop > 70]    [Only return true values, soln]
3. _g7_pop.mean() [Mean]
4. g7_pop.std[]   [Standard Deviation]

## Operations
1) g7_pop * 1_000_000 [Value into given product]
2) np.log(g7_pop)   [Converting vales to logarithmic value]
3) g7_pop['France': 'Italy'].mean()  [Mean for a given range]
4) g7_pop['Canada'] = 40.5  [General way for to change value at pos]
5) g7_pop[(g7_pop > 80) & (g7_pop < 200)]  [Operators waiting to analyze data]