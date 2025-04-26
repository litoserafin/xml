XML RSS (Really Simple Syndication)
====================================

**RSS** (Really Simple Syndication) is a web feed format that allows users and applications to **access updates from websites** in a standardized, computer-readable format.

It is **written in XML** and is commonly used to distribute **news headlines, blog posts, podcast episodes**, and more — all without requiring the user to visit each website individually.

---

What is RSS?
------------

- 📡 **Syndication**: Enables websites to broadcast updates that can be subscribed to via feed readers.
- ⏱️ **Real-Time Delivery**: Automatically notifies subscribers of new content as it's published.
- 📄 **Standard Format**: Simple and widely supported by apps, browsers, and websites.

---

Structure of an RSS Feed
-------------------------

Below is an example of a valid RSS 2.0 feed:

.. code-block:: xml

   <?xml version="1.0"?>
   <rss version="2.0">
     <channel>
       <title>League News Feed</title>
       <link>http://leagueoflegends.com</link>
       <description>Latest updates and champion news from the Rift</description>
       <language>en-us</language>

       <item>
         <title>New Champion Released: Aurora</title>
         <link>http://leagueoflegends.com/champions/aurora</link>
         <description>Aurora brings starlight powers and celestial precision to the battlefield.</description>
         <pubDate>Sat, 26 Apr 2025 09:00:00 GMT</pubDate>
       </item>
