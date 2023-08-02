# FeatureSelection

Univariate feature selection-
take one feature and do chi square test with target variable, find out its statistical
significance of the test of independence and keep feature based on strength of significance
we do Univariate feature selection by doing SelectKBest.
this method doesnot take into account the multicollinearity
SelectKBest -

Feature - Cat, Target - Cat ==> Chi-Square

Feature - Numeric, Target - Numeric ==> Correlation

Feature - Cat, Target - Numeric ==> f_regression

Feature - Numeric, Target - Cat ==> f_classification



we can do recursive feature elimination-
by going in reverse direction and selecting features
start with all the features buld model check accuracy score then remove 1 feature build a
model aginn and see how much accuracy or other metrics we are chasing and according to 
change in metric we remove or select that feature

recursive feature elimination with cross validation-
i think it is like going for one feature then two then three and so on and doing cross 
validation on that and selecting
(havenot understood this properly)


chi-Square feature selection-
we have to see pattern between feature col. and target, we can do this by crosstab and see
chi square test essentially works on cat. data



Wrapper methods-
Step Forward, Step Backward and Exhaustive Feature Selection are there in this

it is computationally very expensive
for higher number of features not recommended
wrapper methods are based on greedy search algo.
in this we include ML algos while selecting features

forward selection-
in this we select one feature at a time for all combinations and train models for
that and moodel that gives best result will be selected then with selected feature
we combine with one more feature one by one and traon models and compare them
and select those which give best result and so on...

backward selection-
in this we do same as forward selection but go in opposite direction, means start from
having all feature and remove one at a time and compare model then 2 at a time then 
compare...so on...

subset selection or exhaustive feature selection-
it tries all possible combinations and select best one
2^n-1 combinations try for n features

More Information Available at http://rasbt.github.io/mixtend/
How it works
Sequential feature selection algorithms are a family of greedy search algorithms that are used to reduce an initial d-dimensional feature space to a k-dimensional feature subspace where k < d.
In a nutshell. SFAs remove or add one feature at the time based on the classifier performance until a feature subset of the desired size k is reached. There are 4 different flavors of SFAs available via the Sequential eatureSelector:
* ﻿﻿Sequential Forward Selection (SFS)
* ﻿﻿Sequential Backward Selection (SBS)
* ﻿﻿Sequential Forward Floating Selection (SFFS)
* ﻿﻿Sequential Backward Floating Selection (SBFS)


feature selection with correlation-

if an independent feature highly correlated with dependent feature then we need to keep
that, because that feature can play imp role in ML model training.
but if independent features are highly correlated with each other like 90% then we keep
only one of them.

