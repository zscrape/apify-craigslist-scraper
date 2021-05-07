# Craigslist Scrapper

### **This actor is published on the [Apify Store](https://apify.com/andrewtaylor/craigslist-scraper)**

- [How to Use](#How-to-Use)
- [Input Parameters](#Input-Parameters)
- [Usage Costs](#Usage-Costs)
- [Contact](#Contact)

## How to Use

Simply provide the search URL you want to watch and the scraper will check for any new posts since the last run. New posts will be sent to the email specified and contain the Image, Price, City, Date posted, and a Link to the post.

[Schedule](https://docs.apify.com/schedules#setting-up-a-new-schedule) the actor to run as often as you need, every hour or even every minute!


## Input Parameters

The input of this scraper should be JSON with the following fields:

| Field | Type | Description |
| ----- | ---- | ----------- |
| search_url | String | (required) Search URL to scrape for new posts. Posts will be compared with the previous run and only new items will be emailed. 
| email_addr | String | (required) Email to send the new posts
| email_subj | String | (required) Email Subject


### Example
```json
{
  "search_url": "https://sfbay.craigslist.org/d/apartments-housing-for-rent/search/apa",
  "email_addr": "xxx@xxx.com",
  "email_subj": "New Apartments Search"
}

```

## Usage Costs
Usage costs will depend on how often you run the scraper. Running every minute for example will use about 23 compute units and about 6 units for send mail. Running every hour results in compute units as low as 3/month. Data storage costs to store results is also minimal (about $0.50/month).

### Example
Running one search every hour works out to about **$2/month** The **Free** plan ($5 platform usage credits) is enough to run this.

Running one search every minute works out to about **$5/month** The **Personal** plan ($49) is more than enough and would allow you to scrape about 10 searches every minute.

## Contact
For any bugs or feature requests, you can create an issue [here](https://github.com/zscrape/apify-craigslist-scraper).
