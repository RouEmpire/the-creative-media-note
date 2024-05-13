type:: [[Programming Features]] 
language:: [[HTML]]

- # Introduction
  id:: 663e153a-6ec7-44db-873e-27c5cfa0f785
	- **SEO** is stand for **Search Engine Optimization**
	- It deal with the **Presentability** of the website
	- The **Presentability** is about the visual appeal the well be optimize for both **Bots** and **Users**
	- Bots in this case is **SEO's Bots** such as Google Bots
		- When Users search something, SEO's bots will looking into your website and choice the best answer for **Users Keywords** or **Users Question**
		- **SEO's bots** will look upon a **Certain Paramiters** So making those bot look in to your website is a kind of _Art_
	- SEO's bot are... #card
	  collapsed:: true
		- Google's Bots
		- Bing's Bots
		- DuckDuckGo's Bots
- # How Search Engine Works
  id:: 663dbc27-0e74-45a6-9e91-027da0a06f56
	- ## Evolution of Search Engines
	- In The Back of The Day(~1990s), there are 2 main search engines, there're ((663e4a91-3b57-44e2-89fc-a08be2847290)) and ((663e499b-7dfd-4bbe-821e-e22872447d56))
	- Yahoo #card
	  id:: 663e499b-7dfd-4bbe-821e-e22872447d56
	  collapsed:: true
		- Created by 2 Standford University Student in the year 1994
			- Jerry Wang
			  logseq.order-list-type:: number
			- David Filo
			  logseq.order-list-type:: number
		- In Yahoo, Developers have too submit it to Yahoo, so it can be appear in Yahoo Search Engine
		- Yahoo has a large repository/database of the submitted website
		- Yahoo focus on website content, like if there are keyword (That users searched) in website appears 100 times, it'll be a higher rank (This led to a bad search result)
		- Microsoft partnered with Yahoo to created Bing and Fight Google, this fight holds for 2 decades and still in a warfare
	- Google #card
	  id:: 663e4a91-3b57-44e2-89fc-a08be2847290
	  collapsed:: true
		- Google was founded by 2 Standford University Student in year 1996
			- Larry Page
			  logseq.order-list-type:: number
			- Sergey Brin
			  logseq.order-list-type:: number
		- Google was initially known as "BackRub"
		- Google different from Yahoo because its use "backlinks" to a website as a factor to decide a website rank(Something like, there are meny site and Link Anchor to your site etc.)
		- It takes 2 years that name "Google" comes to replace "BackRub"
		- Google still keep improving Search Algotithm
		- Google bought **Universal Search** which is only 1 search bar to search everything
		- in 2015 Google led **Mobile First** website so its Search Algorithm
- # On-Page SEO Factors
  id:: 663e509f-2656-4c3d-99e7-7d5c5076f870
	- The Biggest and simplest SEO we make is using Headers Tag such as `<h1>` , `<h2>` to `<h6>`
	- Use the Keyword in your site, Keyword that can tell SEO's bot what your site is about
	- **SERP**
	  id:: 66415b22-715a-451a-944e-3074577c9ec7
		- **SERP** stands for **Search Engine Result Page**
		- It is a List of Search Result that appear under a Blue Link (Website) in Google as a page subtitle
		- It is also a Free Info, like, *Google SUggestions* or *People also ask* or *Related Searches*
		-
	- The **Most Important** tag is the one that in the `<head>` tag, called `<title>`. You have to put the page title here and those **SEO's bots** will see as their *favorite tag*. This tag will show as a main Blue Text in google's page when users search something, remember that people click what they need
	- Tag `<meta>` contain ((66415b22-715a-451a-944e-3074577c9ec7)), it appears as a subtitle when people search something on the Google and your website shows up (Under the Blue link)
		- Here's the meta tag showing how its look like
		- ```html
		  <meta name="description" content="This is Description of the whole page" /> 
		  ```
		- remember to have all these tag in each of your website!
	- These tags are called **SEO-Friendly**
- # Off-Page SEO Factors
  id:: 663ec17a-41ec-4cde-8a2b-39257ee0a160
	- This topic focus on Non-On-Page SEO
	- ## Inlinks and Outlinks
	  id:: 663ec967-2813-4c68-8f5d-bdb0fbf13d09
		- **Inlinks**
		  id:: 663ec7ec-307e-45f2-a734-b0f7f4e6ad1d
			- They are links (Anchor Tag) of others website that point to your webpage.
		- **Outlinks**
		  id:: 663ec7f1-8539-4495-8418-658233b0081e
			- They are links (Anchor Tag) of Your website outgoing to the others site
		- Developers are oftenly put all the link in a navigation bar under the tag `<nav>`
	- ## Page Rank
		- Page Ranks is the **Quality of Links** Such as, having a good ((663ec7f1-8539-4495-8418-658233b0081e)) instead of spamming it.
		- Page Ranks is about the other informations that google has
			- Such as, if users search  `Cake Shop near me` in google, it will take a look what contents in your website and your shop position on Google Maps, so users can find your shop
		- Having someone important (aka Others Famous Page) send a ((663ec7ec-307e-45f2-a734-b0f7f4e6ad1d)) to your site will improve your Page Rank well-much
- # Analyzing a Website
  id:: 663ecced-1d16-475c-aff8-5c7d13d35438
	- **Web Crawlers**
	  id:: 663ecd17-78cd-4e2e-b01a-0ab4b198b994
		- These **Crawlers** give a complete picture of your website's state as a report
		- It gathers all the information like ((663ec967-2813-4c68-8f5d-bdb0fbf13d09)) or other informations that their creator like'd to see, then summarize that information as a report so Developers can see how Great SEO they Wrote
		- some Crawlers service companies example...
			- Moz.com
			- SemRush
			- Screaming Frog
		- Google's Bot are a kind of **Web Crawlers**
	- **Sample Reports...**
		- Duplicate `<title>` or missing `<title>`
			- Each Page of your website must have a **Unique Title Tag**
			- The **Title Tag** mustn't have a **too long** or **too short** ( ((663ecd17-78cd-4e2e-b01a-0ab4b198b994)) can give you an advise if you have no idiea about this)
			- Never **Missing Heading Tags**, it's important as well as **Title Tag**. Just make sure that it's used on a right role, *not just spamming it* (technically just one `<h1>` is enough for most website)
			- ***Duplicate Pages are big NO NO***, if Google bots found this, you site page rank gonna be shit-
				- If you have a situations that the **Duplicate Pages** need to be made, You must *Redirect* the Google Bot to [[301 Error]] page (Move Permananently - Request at Server Level)
				- Use **Canonical Tags** [~ Learn More ~](https://developers.google.com/search/docs/crawling-indexing/canonicalization?hl=th) | It is the Tags that user can click and surf your website normally, but will prevent Google's Bot from looking inside and rank it
				-
			-
			-
- # Technical SEO
  id:: 663ecd77-6ace-46ac-8d5b-276945921f3e
	- **Image Alternate Text** (`alt=""`)
		- Calling **Image Alt** for shorts, it is a text that works as the alternative text to be display when users can't he image on their website, And also works Extremely Well with ((663ecd17-78cd-4e2e-b01a-0ab4b198b994)) Because it can understand the image now.
		- *Do not over do it*
	- **Structure Design**
		- If you have a important page in your website lies deep, there's a chance that ((663ecd17-78cd-4e2e-b01a-0ab4b198b994)) never be able yo reach it, which mean you are losing some important factor for ranking
		- **URL Structure**
			- Any page of your website *must be reachable* in 3-4 clicks from home page.
			- If your Website structure is well-design, Google will reward you a [SiteLinks Feature](https://developers.google.com/search/docs/appearance/sitelinks?hl=th) (It is the thing that deliver Users multiple asnwer of your website with a single search )
				- Having a SiteLinks will increase your **CTR (Click-Through Rate)**
	- **sitemap.xml** and **robots.txt**
		- **sitemap.xml**
		  id:: 664001e3-5b92-4485-af6d-69e608952f05
			- It is a modern way to submit your site to google
			- It is a file that list down every page linked within your website as a single sheet
			- IT makes Google's ((663ecd17-78cd-4e2e-b01a-0ab4b198b994)) job easier, so you gain more ranking
		- **robot.txt**
		  id:: 66400321-5e47-4129-bf3f-7592599358f7
			- An opposite side of ((664001e3-5b92-4485-af6d-69e608952f05)), it tells Google's ((663ecd17-78cd-4e2e-b01a-0ab4b198b994)) to not craw the list of the certain page
				- Some PDF file that's need not to be craw by ((663ecd17-78cd-4e2e-b01a-0ab4b198b994))
				- Some Image file
				- Some Page that you are undone working with it
			- The syntax is simple
				- ```html
				  User-agent: *
				  Disallow: /home/class/toilet
				  ```
				- The `User-agent` tells what ((663ecd17-78cd-4e2e-b01a-0ab4b198b994)) you are working, by putting `*` it means you are mentioning all the Crawlers possible
				- The `Disallow` tells what page you will blind those ((663ecd17-78cd-4e2e-b01a-0ab4b198b994)), in the example , we are blinding the page `toilet` which is at `/home/class/toilet`
				- ```html
				  User-agent: Twitterbot
				  Disallow: /
				  
				  User-agent: *
				  Disallow: /car/bus
				  Disallow: /category/*.html
				  Disallow: /mobile/
				  Allow: /th
				  ```
					- The `7th` line means every page and its sub directory of `/mobile`
		- To put ((66400321-5e47-4129-bf3f-7592599358f7)) and ((664001e3-5b92-4485-af6d-69e608952f05)) into your website, simply put `robots.txt` on the root directory of the site, and put the `sitemap` at the end of the files Such as...
			- www.mebmarket.com/robots.txt
			- www.bing.com/robots.txt
- # Keyword Research
  id:: 663ecd98-0d38-42d9-bd5d-fed5157aa241
	- First, you have to know what is your business you are on, so you can make a right key word. Just Heading over to **Google's Keyword Planner** in the absolute wrong step! Follow these instead.
	- ## Making Keywords
		- Know What *your business* you are on.
		  logseq.order-list-type:: number
		- Know What kind of you *customers* (The user that search things like your product) like...
		  logseq.order-list-type:: number
			- In case of Gym Website
				- People in the age between 20-40
				- There are love to be healthy
		- Know your *customer topics*
		  logseq.order-list-type:: number
			- Understand where your customers are on on the social media
			- What kind of words they will search if they are searching a product or content link yours
			- Knows what your *customers* are talking about in your product or content
		- Generating *Keyword Ideas*
		  logseq.order-list-type:: number
			- Choose the one that makes sense to *your business*
			- Put it down as many as you want!
			- We can genenrates keywords using Google itself
				- Read *Google Suggestion* When you typing in a Search bar
				- Search Related Terms, There are at the bottom of your (or others) SERP
				- Learn the ((663ec967-2813-4c68-8f5d-bdb0fbf13d09)) style in the Wikipedia, you customers might search things on that first
	- ## Long-Tail Keywords
		- The **Long-Tail Keywords** are something like the things that user actually type in the search bar
		- The words that user type in the search bar mostly long 3-5 words, your keywords can be one of those
		- 70% of search result are thanks to **Long-Tail Keywords**
		- There are tools to generate this, such as
			- UserSugest
			- KeywordTool.IO
			- KWFinder
	- ## Google Keyword Planner
		- Here's a place to put all of your Idea you have!
		- We are choosing keyword based on ((6640154d-71ef-439f-8b16-e5083b3d3617))
		- **Keywords Matrics**
		  id:: 6640154d-71ef-439f-8b16-e5083b3d3617
			- *Commercial Intent*
			  id:: 66401592-dcfd-4dde-986a-b8633c1607be
				- The **money** that **paid** by **bidders** to rank their website for a certain keywords (AKA. Buying Ranks/Buying Ads)
			- *Search Volume*
				- The **numbers** of **times** the certain keywords was **searched**.
		- In the ((66401592-dcfd-4dde-986a-b8633c1607be)) is showing us that higher bets, means higher important keywords that many users search for (and likely to be found your site). The lower words, The higher bets. It is a bidder competition there.
	- ## Google Trends
		- It is a tool that tells you a number of time of the certain keywords has been searched globally
		- It's free, made by Google.
- # Content is King
  id:: 663ecda7-dffd-4a25-b67e-2578c6a788ad
	- Content is a sub-topic for ((663e509f-2656-4c3d-99e7-7d5c5076f870))
	- id:: 66414e12-78d9-4aa8-9db7-677e0e4cc4f1
	- ## BERT
		- **BERT** is stand for (Bidirectional Encoders Representations for Transformers)
		- It's an [[AI]] model that helps Google understand user's search ((66414e48-aad8-4e42-a1c7-9bc6de636e08)). Which is trained by a lot of words
	- ## Query
		- **Query**
		  id:: 66414e48-aad8-4e42-a1c7-9bc6de636e08
			- It is a words or keywords of sentences that user use to search in a **Search Bar**
			- There are 3 types of ((66414e48-aad8-4e42-a1c7-9bc6de636e08))
				- **Transactional Query**
				  logseq.order-list-type:: number
					- Like : "*Buy*" or "*Sell*"
					- If your website is a **Transactional Nature Website** that showcase a lot of product pages, your page must have a good descriptive information about your product
				- **Informational Query**
				  logseq.order-list-type:: number
					- Like : "*How to*"
					- If your website cares more about Information, you should use **Blog** or **Presentive style** website.
				- **Navigational Query**
				  logseq.order-list-type:: number
					- Like : "*Where is the nearest hospital?*"
					- If you website is for navigation, it must have a localization element added toit
		- **Topic**
			- It is a available information by Google, presented by ((66415b22-715a-451a-944e-3074577c9ec7))
			- If you page Main Topic is also you keyword, you should put it on Title or Headers Internal Links of the page as well
		- **Visuals**
			- If you use it correctly, you can even add a extra layer of information around the main one
			- Pictorials like Infographics are a great tools to provide information instead of long sentences
		- **Long Articles**
			- **Long Articles** are the pages that live in the user Book Marks
			- It is a must well research contents
			- Always link to other people research or external knowledgh if possible, even Google likes deep content
	- ## Dwell Time
		- It is the amount of time the user spends time on the ((66415b22-715a-451a-944e-3074577c9ec7))
		- More in-depth articles, more **Dwell Time** they spend
		- More higher **Dwell Time** means better ranking by Google
	- ## Bounce Rate
		- It is a Percentage
- # Localization SEO
  id:: 663ecdb7-e7ed-4e53-bee5-aaac886a678f
	- Coming Soon