# ECommerce-Decision-Trees

The [dataset](https://github.com/aamirpatel23/ECommerce-Decision-Trees/blob/master/sample_user_data.rar) contains website users data (Google Analytics data) from Jan 1, 2017 to Jul 31, 2017. The sample dataset contains obfuscated Google Analytics 360 data from the [Google Merchandise Store](https://www.googlemerchandisestore.com/shop.axd/Home?utm_source=Partners&utm_medium=affiliate&utm_campaign=Data%20Share%20Promo), a real ecommerce store. The Google Merchandise Store sells Google branded merchandise. The data is typical of what you would see for an ecommerce website. It includes the following kinds of information:

**1. Traffic source data:** information about where website visitors originate. This includes data about organic traffic, paid search traffic, display traffic, etc.

**2. Content data:** information about the behavior of users on the site.

**3. Transactional data:** information about the transactions that occur on the Google Merchandise Store website.

### Fields:
***FullVisitorId:*** The unique visitor ID

***VisitNumber:*** The session(visit) number for this user. If this is the first session, then this is set to 1.

***Date:*** The date of the session in YYYYMMDD format.

***VisitStartTime:*** The timestamp (expressed as POSIX time)

***totals_bounces:*** Total bounces (for convenience). For a bounced session, the value is 1, otherwise it is null

***totals_pageviews:*** Total number of pageviews within the session.

***totals_timeOnSite:*** Total time of the session expressed in seconds.

***totals_totalTransactionRevenue:*** Total transaction revenue, expressed as the value passed to Analytics multiplied by 10^6 (e.g., 2.40 would be given as 2400000)

***totals_transactions:*** Total number of ecommerce transactions within the session

***trafficSource_source:*** The source of the traffic source. Could be the name of the search engine, the referring hostname, or a value of the utm_source URL parameter

***trafficSource_medium:*** The medium of the traffic source. Could be "organic", "cpc", "referral", or the value of the utm_medium URL parameter.

***trafficSource_campaign:*** The campaign value. Usually set by the utm_campaign URL parameter

***device_deviceCategory:*** The type of device (Mobile, Tablet, Desktop).

***device_operatingSystem:*** The operating system of the device (e.g., "Macintosh" or "Windows").

***device_mobileDeviceModel:*** The mobile device model.

***geoNetwork_city:*** Users' city, derived from their IP addresses or Geographical IDs.

***ChannelGrouping:*** The Default Channel Group associated with an end user's session for this View

Schema details can also be found [here.](https://support.google.com/analytics/answer/3437719?hl=en)

### Problem Statement:

Build a decision tree prediction model to predict if the new visitor will transact or not.

When the new visitor visits the website, we get the information about source, medium, campaign, deviceCategory, operatingSystem, city, channelGrouping, pageviews, timeOnSite, bounce, etc.
