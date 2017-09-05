# querybuilder
Build complex search queries

**querybuilder** lets you easily build complex search queries.  You can use these queries to discover relevant content in an efficient way, or plug them into [Google Alerts](https://www.google.com/alerts) to get relevant content as it happens.

### Example

Ngina is an angel investor in the cryptocurrency space in Nairobi.

Across major tech news sources and feeds, she is already bombarded with news and noise about top players in crypto globally.  
> Yesterday's “plastics” are today's crypto tokens | techcrunch.com

But she really wants to catch anything relevant to the space AND her local ecosystem.  
> Belfrics Begins Roll-out of African Bitcoin Exchanges in Kenya | news.bitcoin.com

|               | anything      | crypto |
| ------------- |:-------------:| :-----:|
| **global**    |               |        |
| **local**     |               | This.  |


### How it works

querybuilder asks you to define:

1. (Optional) Global filter, if she wants to restrict her search to only certain parts of the internet, like top tech news sources, Crunchbase and AngelList, research papers or *.edu AND .org*.

2. Local entities - locations, people, languages companies, institutions, sources... - not necessarily in the crypto space.  For example *Nairobi*, *Mombasa*, *Swahili*, *Kenya*, *Kenyan*, *Kikuyu*, *site:techmoran.com*, *site:nation.co.ke*, *Technical University of Kenya*, *M-Pesa*, *BRCK*, *Safaricom*, *site:\*.ke*...

3. Topic entities - synonyms and subtopics of crypto.  For example *cryptocurrency*, *cryptocurrencies*, *crypto currency*, *crypto currencies*, *ICO*, *bitcoin*, *btc*, *ethereum*, *blockchain*, *mining pool*...

4. Local topic entities - for example, news about a specific portfolio company in the crypto space, KenyaCoin, is always relevant to Ngina.

She can also add filters to exclude results with certain sites or keywords.  For example, the title or artist of a hit song that happens to include the word *crypto*.

querybuilder generates 4 queries:

1. local topic
> @KenyaCoin: Launching new features today! | twitter.com/kenyacoin

2. local topic AND global filters
> A Founder's Journey: KenyaCoin | nytimes.com

3. local AND topic
> The Promise of Cryptocurrencies | business.co.ke  
> Nairobi's Rising Scene | news.bitcoin.com  
> Satoshi Spotted in Kenya | techcrunch.com  

4. local topic AND topic
> Startup Profile: KenyaCoin | news.bitcoin.com

In theory, only 1 and 3 catch everything.  But 2 and 4 are likely very high priority, and therefore it is useful to separate them out.


### See also

[google-alerts-api](https://www.npmjs.com/package/google-alerts-api) NPM package.
