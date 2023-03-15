# Marketbasket_Analysis
Market basket analysis is a data mining technique used by retailers to increase sales by better understanding customer purchasing patterns. It involves analyzing large data sets, such as purchase history, revealing product groupings, and products that are likely to be purchased together.

# How does it actually work in real life?
Market Basket Analysis is one of the key techniques used by large retailers to uncover associations between items. It works by looking for combinations of items that occur together frequently in transactions. To put it another way, it allows retailers to identify relationships between the items that people buy.

To make it easier to understand, think of Market Basket Analysis in terms of shopping at a supermarket. Market Basket Analysis takes data at the transaction level, which lists all items bought by a customer in a single purchase. The technique determines relationships of what products were purchased with which other product(s).

It works on the logic of frequent itemset as described in the above image. So, it seems like the person who purchased milk also purchases bread, and interestingly, we can also see that person purchasing milk also purchases diapers (maybe because they might have a baby).

# So how to find such Association Rules?
Association Rules are widely used to analyze retail basket or transaction data and are intended to identify strong rules discovered in transaction data using measures of interestingness, based on the concept of strong rules.

“Frequently Bought Together” → Association

“Customers who bought this item also bought” → Recommendation

These relationships are then used to build profiles containing If-Then rules of the items purchased. for example:

If {A} Then {B} : A => B

So to start we need to be introduced to few technical terms :

# Support

# Confidence

# Lift

1. Support: Support is an indication of how frequently the item set appears in the data set. Mathematically,


2. Confidence: The confidence of the rule is the ratio of the number of transactions that include all items in {B} as well as the number of transactions that include all items in {A} to the number of transactions that include all items in {A}. Mathematically,


3. Lift: The third measure called the lift or lift ratio is the ratio of confidence to expected confidence. Expected confidence is the confidence divided by the frequency of B. The Lift tells us how much better a rule is at predicting the result than just assuming the result in the first place. Greater lift values indicate stronger associations. Simply, the lift of a rule is the ratio of the observed support to that expected if X and Y were independent. Mathematically,

#For Example :

Assume there are 100 customers.

10 of them bought milk, 8 bought butter and 6 bought both of them.

bought milk => bought butter

support = P(Milk & Butter) = 6/100 = 0.06

confidence = support/P(Butter) = 0.06/0.08 = 0.75

lift = confidence/P(Milk) = 0.75/0.10 = 7.5
