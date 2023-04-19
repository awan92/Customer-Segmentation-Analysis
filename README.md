# Customer Segmentation Analysis in Indonesian  Investment Startup
Successfully help the company to provide segmentation for the customers and give communication recommendations for the themes of the campaign.

-	Tools: Python 
- See my code [here](https://colab.research.google.com/drive/1RPlH02uSx_Qq1Fv75l-lXYQfHcGyMD61?usp=sharing)

## Background
The company is set to expand into government bond investment products, in addition to its existing mutual fund products. The marketing and sales team would like to run a thematic communication campaign for the upcoming product but want to tailor the campaign to a few different relevant segments. As a data analyst, you’re tasked to provide segmentation for this purpose and give communication recommendations for the themes of the campaign.

## Data Overview
Indonesian investment platform startup currently focused on app-based  mutual fund investment at the end of September 2021. In the mobile app developed by the company, users can register as investors and conduct buy or sell transactions on selected mutual funds. In addition, the platform offers robo-investing, which allows users to invest in a diversified mutual fund portfolio without hassle while considering the factors such as age, income and overall risk profile.

**There are 2 different dataset :**
- **users.csv**, key information about registered users in the platform.
- **daily user balance sep21.csv**, information on user level mutual fund balance, available on a daily basis.

## Objective
To help company in providing customer segmentation and give communication recommendations for the effectiveness themes of the campaign.

## Exploratory Data Analysis
**What is the ratio of male and female users?**

![user gender](https://user-images.githubusercontent.com/100940506/232962388-8ce2a031-49f0-4ca6-b98e-39b7f61c5ee8.PNG)

Most of our users are male with a total of 64% of total users.

**How is the distribution of user age?**

![Distribution user age](https://user-images.githubusercontent.com/100940506/232961736-81e5289f-63bc-46e3-9f4e-b8b6de17ed14.PNG)

The majority of our users are **20 - 25** years old, which is **generation Z**. We must understand the characteristics of their generation so that the campaigns we create can be right on target.

**What occupation do most of our users have?**

![user occupation](https://user-images.githubusercontent.com/100940506/232963101-86d575fb-5820-44be-81a4-2907d0a2b6bc.PNG)

By paying attention to the pareto principle, we can focus on campaigns aimed at **80%** of our users, **students** and **private workers**.

**What income range do most of our users have?**

![user income](https://user-images.githubusercontent.com/100940506/232964084-dde8f12c-5268-4db0-8aac-48ea9ffc36e2.PNG)

Mutual fund products are in great demand by people who have an income **<50 million**.

**What is the ratio of users using the referral code?**

![user referral](https://user-images.githubusercontent.com/100940506/232964787-6fbd5312-2e6e-4122-aaeb-3ffb0181e456.PNG)

Only **37%** of our users use referral code when signing up to our platform. This means we don't need to burn our budget on referral code promotion.

**What is the average AUM per user?**

![image](https://user-images.githubusercontent.com/100940506/232964986-2b2781ba-6a9d-4eb2-9282-1d2ad6c20e59.png)

Our users mostly invest large amounts in **mixed mutual funds**. The average AUM is much higher than the other types.

**What is the average monthly buy per customer?**

![average monthly buy](https://user-images.githubusercontent.com/100940506/232965206-ca19a581-306f-42a1-bbef-933d7aafc8b5.PNG)

Overall, the average buy of mix mutual funds higher than the others. However, it can be seen that in September, the average buy from mixed type decreased from the previous month. Whereas for other types of mutual funds have increased.

**What is the average monthly sell per customer?**

![Average Monthly Sale](https://user-images.githubusercontent.com/100940506/232968590-059d817a-803c-44a5-95dd-7d1b663b5cad.PNG)

Just like buy transactions, it can be seen that in September, the average sell from mixed type has decreased from the previous month. Whereas for other types of mutual funds looks stagnant.

**What is the average current profit per user?**

![Average Profit](https://user-images.githubusercontent.com/100940506/232976171-ea3ec97c-3133-4842-bd6f-4d9d50ce4640.PNG)

The average profit earned from mixed mutual funds is negative means loss. This is one of the reasons for the reduced number of daily transactions in mixed mutual funds. Meanwhile, the type of mutual fund that gets the highest profit is stocks mutual fund.

**Is there any consistent "low season" and "high season" ?**

![Daily transactions](https://user-images.githubusercontent.com/100940506/232976755-824510d5-6c41-496a-87d0-be9901752533.PNG)

The count of daily transactions seems fluctuates. However, our users tend to make transactions (buy/sell) at the beginning of each week (Monday). And rarely make transactions on weekends. It's natural to expect zero transaction on weekends because no transaction cannot be made as the market is closed. The number of daily transactions in mixed mutual funds is very small compared to other types, we need to separate the mixed mutual funds plot to make it clearer.

**Is there any consistent "low season" and "high season" ?**

![Daily red](https://user-images.githubusercontent.com/100940506/232977084-fb485d3f-9fb1-43a0-b17c-ae186a9a7e7e.PNG)

There is no particular pattern in the transactions of mixed mutual funds.

**How about trends over time? Is it increasing? Decreasing? Stay the same?**

![Stock transaction trend](https://user-images.githubusercontent.com/100940506/232977476-d228927b-dc2a-477c-b2f8-125eecbd55df.PNG)

Although the count of stocks transactions fluctuates, the trendline of stock transactions is rising, with 𝑅2 of 74.93%

![Market transactions trend](https://user-images.githubusercontent.com/100940506/232977689-ccb9d4e9-e015-41d5-838d-6e8987da8695.PNG)

Although the count of money market transactions fluctuates, the trendline of stock transactions is rising, with 𝑅2 of 75.37%

![Bond Transactions trend](https://user-images.githubusercontent.com/100940506/232977839-170221d0-3b78-47ba-ad77-61b7b3723eee.PNG)

Although the count of Bond transactions fluctuates, the trendline of stock transactions is rising, with 𝑅2 of 79.67%

![Mix transaction trend](https://user-images.githubusercontent.com/100940506/232977991-70ed6df1-36e9-4ed6-bbe6-02411933df50.PNG)

Although the trendline of the mixed transaction is increasing, the 𝑅2 is very small (16.51%). So we can't conclude that the trend is really increasing.

## User Segmentation

![Clustering](https://user-images.githubusercontent.com/100940506/232978439-3b49e6c7-4285-4653-b441-1ca1bccf4ee9.PNG)

**"Z-gen Investor"**  is 100% Gen-Z users, 66% user not using referral, and most of them transaction in money market mutual funds.

Recommendation :
1. "Referral Code Buzzer": Offer promos to use referral codes so that they want to invite their friends to join us.
2. Offer promos on money market mutual funds so that they increase the number of transactions.

**"Low Income Investor"**  is most users have a small income range. But have a fairly large amount of investment except for mixed mutual fund.

Recommendation :
1. "Long Invest for Long Life" : Provide benefits for long-term investment.
2. Provide promos on mixed mutual fund products to widen the portfolio.

**"Rich Y Investor"**  is contains 94% users from Gen-Y, not frequent transactions, but has a large amount of investment in bond mutual funds.

Recommendation :
1. "Long Invest for Long Life" : Provide benefits for long-term investment.
2. Go diversify your portfolio! Bond-only portfolio are dangerous! (Give recommendation to buy another product).

**"PriWork Investor"**  is 100% private sector workers, are moderate investors, and have almost the same invested amount in each type of mutual fund, except mixed.

Recommendation :
1. "Big Cash Big Back": Give cashback promos on large transactions.
2. Provide promos on mixed mutual fund products to widen the portfolio.

**"Beginner Investor"**  is contains 100% Gen-Z and 96% students. They are also classified as investors whose investment amount is still small, but very often make transactions in the money market.

Recommendation :
1. "Mutual Points": Provide cashback promos in non-cash form, which can be in the form of points that can only be used for transactions on our platform. So that it can encourage them to continue making transactions on our platform.
2. "Robo-mendation": Provides recommendations for comparative investment amounts in each type of mutual fund. To encourage them to try other types of mutual funds.

## Marketing Strategy Recommendation:
- Focus on loyalty programs and offer membership or recommend related products to cross-sell them based on their past purchased
- Reward these customers. They can become early adopters for services and will help promote our brand
- Send milestone emails anniversary for the first time they bought from the company, or when they’ve purchased certain number of items
