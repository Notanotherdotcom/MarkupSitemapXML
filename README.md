MarkupSitemapXML
================

## Overview:

A module for ProcessWire that generates a sitemap.xml file for use with major search engines.  

The module ignores any hidden pages and their children, assuming that since you don't want these to be visible on the site then you don't want them to be found via search engines either.

Designed for use with [ProcessWire](http://processwire.com) version 2.5 

## Installation

1. Clone the module and place MarkupSitemapXML in your site/modules/ directory. 
	```
	git clone https://github.com/Notanotherdotcom/MarkupSitemapXML your/path/site/modules/MarkupSitemapXML
	```

2. Login to ProcessWire admin and click Modules. 
3. Click "Check for new modules".
4. Click "install" next to the new MarkupSitemapXML module. 
5. That's all - no settings are required but possible. 


## Usage

The module also adds a field called **sitemap_ignore** to exclude specific pages on a per-page basis. Again, this assumes that you wish to ignore that page's children as well.

![sitemap_ignore](https://github.com/justonestep/processwire-markupsitemapxml/blob/feature/global-sitemap_ignore/screens/settings.png)

The sitemap is accessible at yoursite.com/sitemap.xml.

![sitemap.xml](https://github.com/justonestep/processwire-markupsitemapxml/blob/feature/global-sitemap_ignore/screens/sitemap.png)

## What is left to do

### robots.txt

You can specify the location of the Sitemap using a robots.txt file. To do this, simply add the following line including the full URL to the sitemap:

```
Sitemap: [your sitemap web address]
Sitemap: http://www.example.com/sitemap.xml
```
### Submitting to Google and Bing

#### Ping Google Bot

Type following URL in address bar of your browser:

```
http://www.google.com/webmasters/sitemaps/ping?sitemap=[your sitemap web address]
http://www.google.com/webmasters/sitemaps/ping?sitemap=http://www.example.com/sitemap-file.xml
```
#### Ping Bing Bot

Type following URL in address bar of your browser:

```
http://www.bing.com/webmaster/ping.aspx?siteMap=[your sitemap web address]
http://www.bing.com/webmaster/ping.aspx?siteMap=sitemap=http://www.example.com/sitemap-file.xml
```