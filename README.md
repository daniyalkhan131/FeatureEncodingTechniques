# FeatureEncodingTechniques

encodeing categorical data, it comes in feature transforming which comes in feature enggineering.

categorical data type-
	nominal
	ordinal
our duty is to cinvert category to numbers as ML model undersatnad numbers
ordinal encoding apply to data where order is there and
onehot encoding applies to nominal data

and label encoding 
if ordinal data is in input X then apply odinal encoding, and for data in output y then
apply labelencoding


onehotecoding-
for handling nominal data

if red yellow blue are cat. in column then we cant do like give 0 1 2 assignment as,
our ML model will thing that 2 one is more important to it but it is not the case as all are equal. we make column for every catrgory, we actually create string to vector
if having 50 categories then have to make 50 new columns(increased dimensionality)

we remove one column from it, like if get n cols after applying onehotencoding then remove
one from it as it will lead to multicollinearity, we can easily represent n cat. usinf n-1 cols as 01 is yellow 10 is blue so 00 is red , if we remove color_red col
multicollinearity is mathematical relationship between col.s in dataset, if present then they
are dependent on each other, in ML model cols need to be independent(it is general wisdom)
if we add col.s of color then sum comes to be 1 so we remove any on one
if we work with linear model then this is a big problem(multicollinearity) midels like
linear logistic regression
the cols that are created when onhotencoding applied are called dummy variables so this is
called dummy variable trap and to prevent this we simple remove one col

OHE using most frequent variables:
like if 50 cat. so we create cols for most freq. ones and remaing we put in others col.

