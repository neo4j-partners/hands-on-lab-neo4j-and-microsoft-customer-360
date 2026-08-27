# Lab 1 - Deploy and Connect to Neo4j

You should have received an email containing an invite to the Neo4j Aura project. Please click the "Accept Invitation" link.

<img src="images/01.png" style="border-radius: 16px; box-shadow: 0 26px 50px rgba(20,20,30,0.28), 0 7px 16px rgba(20,20,30,0.32); margin: 56px 56px 56px 80px; max-width: 80%;">

Enter your email and click "Continue"

<img src="images/02.png" style="border-radius: 16px; box-shadow: 0 26px 50px rgba(20,20,30,0.28), 0 7px 16px rgba(20,20,30,0.32); margin: 56px 56px 56px 80px; max-width: 80%;">

You will receive an email to verify your identity.

<img src="images/03.png" style="border-radius: 16px; box-shadow: 0 26px 50px rgba(20,20,30,0.28), 0 7px 16px rgba(20,20,30,0.32); margin: 56px 56px 56px 80px; max-width: 80%;">

Enter the code from the email into the verification box and click "Continue".

<img src="images/04.png" style="border-radius: 16px; box-shadow: 0 26px 50px rgba(20,20,30,0.28), 0 7px 16px rgba(20,20,30,0.32); margin: 56px 56px 56px 80px; max-width: 80%;">

Create your password and click "Sign up".

<img src="images/05.png" style="border-radius: 16px; box-shadow: 0 26px 50px rgba(20,20,30,0.28), 0 7px 16px rgba(20,20,30,0.32); margin: 56px 56px 56px 80px; max-width: 80%;">

Once successfully signed up, you will be brought to the Instances page of the project you were invited to. You may see other users' instances already created. Let's begin the process to create your personal instance for the remainder of this workshop.  

Click "Create Instance"

<img src="images/06.png" style="border-radius: 16px; box-shadow: 0 26px 50px rgba(20,20,30,0.28), 0 7px 16px rgba(20,20,30,0.32); margin: 56px 56px 56px 80px; max-width: 80%;">

We're now presented with a choice of product tiers within Neo4j:

* Free
* Business Critical
* Professional

The Free tier is a great way to get started experimenting.  Business Critical offers a 3 node fault tolerant and highly available cluster.  We don't really need that for this lab.  The Professional tier has similar functionality with a single node.  Select "Professional."

For Instance details, name your instance "[FirstInitialLastName] Workshop" i.e. "[jdasuqi] Workshop", this will help us identify our instance from other participant's instances.

<img src="images/07.png" style="border-radius: 16px; box-shadow: 0 26px 50px rgba(20,20,30,0.28), 0 7px 16px rgba(20,20,30,0.32); margin: 56px 56px 56px 80px; max-width: 80%;">

Now, let's inspect the other options.

We can deploy in different regions.

There are two options for Graph Analytics.  This feature provides access to 60+ graph alogrithms.  These run across your graph, computing things like centrality and node importance.  We'll keep the default.  That spins up computations on demand.  Another option is to collocate it in the database.

Finally, there's an option to optimize the database for vector search.  We'll be using vector functionality but our workloads will be comparatively light so we don't need this optimization.

We've reached the bottom!  Click "Create Instance."

<img src="images/08.png" style="border-radius: 16px; box-shadow: 0 26px 50px rgba(20,20,30,0.28), 0 7px 16px rgba(20,20,30,0.32); margin: 56px 56px 56px 80px; max-width: 80%;">

You'll be presented with the credentials for your database.  Click "Download and continue."  That will download the credentials to a text file on your local machine.  

<img src="images/09.png" style="border-radius: 16px; box-shadow: 0 26px 50px rgba(20,20,30,0.28), 0 7px 16px rgba(20,20,30,0.32); margin: 56px 56px 56px 80px; max-width: 80%;">

A save dialog should pop up.  Be sure to save that file as you won't be able to get those credentials later.

You'll see a dialog that your database is being created. This should only take a few minutes.

<img src="images/10.png" style="border-radius: 16px; box-shadow: 0 26px 50px rgba(20,20,30,0.28), 0 7px 16px rgba(20,20,30,0.32); margin: 56px 56px 56px 80px; max-width: 80%;">

When deployment is complete, you can filter the search for your instance name and you'll see the instance details in the management console.  

<img src="images/11.png" style="border-radius: 16px; box-shadow: 0 26px 50px rgba(20,20,30,0.28), 0 7px 16px rgba(20,20,30,0.32); margin: 56px 56px 56px 80px; max-width: 80%;">

You can poke around the menus here a bit and see more on database status and connection information.

You now have a deployment of Neo4j AuraDB Professional running!

Click "Connect" then select "Query".

<img src="images/12.png" style="border-radius: 16px; box-shadow: 0 26px 50px rgba(20,20,30,0.28), 0 7px 16px rgba(20,20,30,0.32); margin: 56px 56px 56px 80px; max-width: 80%;">

That will drop us into an empty database.

There's nothing in our database yet. We can see the nodes, relationships and property key areas are all blank.

In the next lab, we will start loading data into our instance.

<img src="images/13.png" style="border-radius: 16px; box-shadow: 0 26px 50px rgba(20,20,30,0.28), 0 7px 16px rgba(20,20,30,0.32); margin: 56px 56px 56px 80px; max-width: 80%;">