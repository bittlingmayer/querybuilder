# querybuilder
Build complex search queries | [bittlingmayer.github.io/querybuilder/](https://bittlingmayer.github.io/querybuilder/)

**querybuilder** lets you easily build complex search queries.  You can use these queries to discover relevant content in an efficient way, or plug them into [Google Alerts](https://www.google.com/alerts) to get relevant content as it happens.

### Example

Ngina is an angel investor in the cryptocurrency space in Nairobi.

Across major tech news sources and feeds, she is already bombarded with news and noise about top players in crypto globally.  
> Yesterday's “plastics” are today's crypto tokens | techcrunch.com

But she really wants to catch anything relevant to the space AND her local ecosystem.  
> Belfrics Begins Roll-out of African Bitcoin Exchanges in Kenya | news.bitcoin.com  
> Bitcoin up more than 200% year over year | finance.nation.co.ke

|               | anything      | crypto |
| ------------- |:-------------:| :-----:|
| **global**    |               |        |
| **local**     |               | This.  |


## How it works

### Input

querybuilder asks Ngina to define:

1. local.topic
Local topic entities.  For example, news about a specific portfolio company in the crypto space, KenyaCoin, is always relevant to Ngina.

2. global.topic  
Topic entities - synonyms and subtopics.  For example *cryptocurrency*, *cryptocurrencies*, *crypto currency*, *crypto currencies*, *ICO*, *bitcoin*, *btc*, *ethereum*, *blockchain*, *mining pool*...

3. local.*  
Local entities - locations, people, languages companies, institutions, sources... - not necessarily in the crypto space.  For example *Nairobi*, *Mombasa*, *Swahili*, *Kenya*, *Kenyan*, *Kikuyu*, *site:techmoran.com*, *site:nation.co.ke*, *Technical University of Kenya*, *M-Pesa*, *BRCK*, *Safaricom*, *site:\*.ke*...

4. global*.  
Optional global filters, for example if she wants to restrict her search to only certain parts of the internet, like top tech news sources, Crunchbase and AngelList, research papers or *.edu AND .org*.

She can also add filters to exclude results with certain sites or keywords.  For example, the title or artist of a hit song that happens to include the word *crypto*.

### Output
Using her definitions, querybuilder generates 4 queries:

1. local.topic
> @KenyaCoin: Launching new features today! | twitter.com/kenyacoin

2. local.topic AND global.*
> A Founder's Journey: KenyaCoin | nytimes.com

3. local.* AND global.topic
> The Promise of Cryptocurrencies | business.co.ke  
> Nairobi's Rising Scene | news.bitcoin.com  
> Satoshi Spotted in Kenya | techcrunch.com  

4. local.topic AND global.topic
> Startup Profile: KenyaCoin | news.bitcoin.com

In theory, only 1 and 3 catch everything.  But 2 is higher priority than 1, and 4 than 3, and therefore it can be useful to separate them out.


### See also

[google-alerts-api](https://www.npmjs.com/package/google-alerts-api) NPM package.
