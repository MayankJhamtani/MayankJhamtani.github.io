---
layout: post
title: Summer'17, My first experience with Data Science!
---

### In my first blog post, I will be describing my first formal data science project, and the motivation behind documenting my progress in the form of a blog.

I am deeply influenced by the philosphy of the open-source movement, wherein all knowledge, code and products are made easily accessible to as many people as possible. This not only provides the users with the final product, but also the ability to tinker around,implement new features and fix bugs. Eventually, this translates to open collaboration, enthusiasts all over the world can now make contributions, leading to products which are often better than pay-walled content. The tools which I used for my current project have all been built on the open source philosphy. I got useful insights and nuances to use these tools from the blogs I read and decided to write a blog myself. Apart from this, I believe writing a blog is a great way to track my own progress, shortcomings and showcase my skill-set.

In my current project, I am trying to implement a predictive model for forecasting the  **Market Clearing Price (MCP)** in the Indian Energy Market. All power plants with an excess capacity can declare a *Sell Bid*, whereas all industries with an excess demand can declare a *purchase bid*. Based on this these two parameters, the Indian Energy Exchange(**IEX**), plots a supply-demand curve, and the equilibrium point for this curve is called the Market Clearing Point. The corresponding energy volume is called the **Market Clearing Volume(MCV)**, and the price is called the **Market Clearing Price**. A robust prediction mechanism helps both the supply and demand side better plan thier operations and optimize thier profits.

### The Trading Flow:
1. Each power producing unit with an excess capacity of more than 1 Mega-Watt(MW) declares a *sell bid* for the (n+1)th day.
2. Each power purchasing entity declares a *purchase-bid* for the (n+1)th day.
3. Each day is divided into 96 timeslots, each of duration 15 minutes. The sell and purchase bids can be made for any or all of the 96 time-slots.
4. The equilibrium curve is plotted, and the **MCP** and **MCV** for (n+1)th day is determined.

### Problems to consider before formulating a solution:
1. It's a highly dynamic market, with high variations in daily and time-wise variations in MCP.
2. The two key parametres can take unexpected values based on the conditions of any of the players in the market.
3. Factors like temperature and coal prices play a role, but are difficult to map and include in the model.

### I realised the problem can be broken down into 5 key steps -
1. Obtaining the past data to train the model, and automating the process to obtain the new data everyday.
2. Pre-processing the data, visualizing it and finding the various independent variables and how they effect the MCP
3. Building a basic nueral-network based model to predict the MCP to test if a more advanced but similar approach would work.
4. Optimizing the netwrok and implementing a better nueral-network architecture like CNN or LSTM to get improved results.
5. Building a simple interface so that a layman can easily use it to make a prediction.

It's an exciting problem to work on, given the impact it can have on the energy market and consequently the lives of millions of people!
The next post in the series would describe the first two phases of the project, the difficulties I faced, and the tools I learnt and implemented to overcome them.

References:
1. The Indian Energy Exchange website(http://iexindia.com/)
2. Christopher Olah's Blog(https://colah.github.io/)

