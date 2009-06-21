

Canonical URL extension for eZ publish
	-- Jani Tarvainen ( http://iki.fi/janit/ ), 20/6/2009

eZ Publish features the ability to publish the same content within multiple
locations of a websites content structure. Naturally publishing content in
multiple locations presents a problem for search engines that handle all 
the different pages as unique content.

This problem was acknowledged by search providers. During spring 2009 four
major search providers (Ask, Google, Microsoft and Yahoo!) came together
and introduced the canonical link tag:

<link rel="canonical" href="http://www.example.com/content/structure/main_node/" />

The idea is simple, enough: Just add the tag to point to the preferred main
location of your content. Robots supporting this directive will detect the
tag and should only index the main location of your tag, leaving your search
results uncluttered with duplicate results.

In the case of eZ Publish each node by default has a main location so
constructing this extension was quite simple. The template snippet simply
compares the current node_id and the main_node_id of the content and if
these do not match then the canonical link is added.

Read more about the canonical tag:

 - http://blog.ask.com/2009/02/ask-is-going-canonical.html
 - http://googlewebmastercentral.blogspot.com/2009/02/specify-your-canonical.html
 - http://blogs.msdn.com/webmaster/archive/2009/02/12/partnering-to-help-solve-duplicate-content-issues.aspx
 - http://www.ysearchblog.com/2009/02/12/fighting-duplication-adding-more-arrows-to-your-quiver/

