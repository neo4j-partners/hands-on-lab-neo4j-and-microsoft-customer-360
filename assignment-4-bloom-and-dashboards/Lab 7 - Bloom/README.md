# Lab 7 - Bloom

In this lab, we'll use Bloom, Neo4j's business intelligence (BI) tool, to explore our data.

Click on the 'Bloom' option in the left menu under Studio.

<img src="images/01.png" style="border-radius: 16px; box-shadow: 0 26px 50px rgba(20,20,30,0.28), 0 7px 16px rgba(20,20,30,0.32); margin: 56px 56px 56px 80px; max-width: 80%;">

Now click on "Show me a graph."

<img src="images/02.png" style="border-radius: 16px; box-shadow: 0 26px 50px rgba(20,20,30,0.28), 0 7px 16px rgba(20,20,30,0.32); margin: 56px 56px 56px 80px; max-width: 80%;">

In this case, we got a view with a few different trees of customer, order, product, ticket, and event nodes and their relationships.  
We can mouse over any of the nodes to see its unique identifying property.

<img src="images/03.png" style="border-radius: 16px; box-shadow: 0 26px 50px rgba(20,20,30,0.28), 0 7px 16px rgba(20,20,30,0.32); margin: 56px 56px 56px 80px; max-width: 80%;">

Now let's try finding a new graph. But first, let's clear the scene to ensure we start with a clean slate.  
Right click anywhere in the background where there isn't a node or relationship to open up a menu. Select "Clear Scene".

<img src="images/16.png" style="border-radius: 16px; box-shadow: 0 26px 50px rgba(20,20,30,0.28), 0 7px 16px rgba(20,20,30,0.32); margin: 56px 56px 56px 80px; max-width: 80%;">

Click in the search bar.

<img src="images/04.png" style="border-radius: 16px; box-shadow: 0 26px 50px rgba(20,20,30,0.28), 0 7px 16px rgba(20,20,30,0.32); margin: 56px 56px 56px 80px; max-width: 80%;">

Select "Customer."

<img src="images/05.png" style="border-radius: 16px; box-shadow: 0 26px 50px rgba(20,20,30,0.28), 0 7px 16px rgba(20,20,30,0.32); margin: 56px 56px 56px 80px; max-width: 80%;">

Now select the *directionless* "SHARED_PII" relationship.

<img src="images/06.png" style="border-radius: 16px; box-shadow: 0 26px 50px rgba(20,20,30,0.28), 0 7px 16px rgba(20,20,30,0.32); margin: 56px 56px 56px 80px; max-width: 80%;">

Now select "Customer" again to complete the pattern, and click Run Query.

<img src="images/07.png" style="border-radius: 16px; box-shadow: 0 26px 50px rgba(20,20,30,0.28), 0 7px 16px rgba(20,20,30,0.32); margin: 56px 56px 56px 80px; max-width: 80%;">

That gives us search results for every pair of customer accounts that share identity data - the accounts most likely to be the same real-world person.  Try right-clicking a pair and expanding to reveal *which* email or phone they share, and watch the pairs join up into rings.

<img src="images/08.png" style="border-radius: 16px; box-shadow: 0 26px 50px rgba(20,20,30,0.28), 0 7px 16px rgba(20,20,30,0.32); margin: 56px 56px 56px 80px; max-width: 80%;">

Next, we will apply some point-and-click data science to our graph.  Click on the atom icon to open the data science menu.

Click "+ Add" to add an algorithm.

<img src="images/09.png" style="border-radius: 16px; box-shadow: 0 26px 50px rgba(20,20,30,0.28), 0 7px 16px rgba(20,20,30,0.32); margin: 56px 56px 56px 80px; max-width: 80%;">

Click on "Select" to open the algorithm drop down.

Select "Louvain Community Detection."  This will partition the nodes in our scene into communities, based on how densely they're connected to each other.  This algorithm can be read about in deeper detail [here](https://neo4j.com/docs/graph-data-science/current/algorithms/louvain/).

<img src="images/10.png" style="border-radius: 16px; box-shadow: 0 26px 50px rgba(20,20,30,0.28), 0 7px 16px rgba(20,20,30,0.32); margin: 56px 56px 56px 80px; max-width: 80%;">

Click "Run algorithm" followed by "Apply to current scene".

<img src="images/11.png" style="border-radius: 16px; box-shadow: 0 26px 50px rgba(20,20,30,0.28), 0 7px 16px rgba(20,20,30,0.32); margin: 56px 56px 56px 80px; max-width: 80%;">

This spins up an additional ephemeral instance running Neo4j Graph Analytics.  That takes a few minutes.

Once it runs, we see this view.  We can choose how we want to visualize the results in the graph.

Choose "Unique Colors" and close the data science panel to get a better view.  Do that by clicking the icon above "Analytics Session Running."

<img src="images/12.png" style="border-radius: 16px; box-shadow: 0 26px 50px rgba(20,20,30,0.28), 0 7px 16px rgba(20,20,30,0.32); margin: 56px 56px 56px 80px; max-width: 80%;">

Each color is now a community: a cluster of customer accounts so entangled by shared identifiers that the algorithm considers them one group.  In entity-resolution terms, each color is a *candidate identity* - what your customer count looks like after you stop double counting.

We can double click on the Customer nodes within one community to investigate their Louvain "Score". This score is used used to assign each node a community ID. You will notice nodes of the same cluster possessing the same score.   

<img src="images/13.png" style="border-radius: 16px; box-shadow: 0 26px 50px rgba(20,20,30,0.28), 0 7px 16px rgba(20,20,30,0.32); margin: 56px 56px 56px 80px; max-width: 80%;">

For the scene we've created, one color = one probable real-world identity.  Marketing sees deduplicated reach.  Risk sees account rings.  Finance sees true customer lifetime value.  Same graph, same algorithm, three audiences.

These are just a few examples of what you can do with Bloom.  Feel free to explore!
