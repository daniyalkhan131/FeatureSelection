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


