See [sitemaps.org](http://www.sitemaps.org/protocol.html#xmlTagDefinitions) for detail XML tag definitions.

## dest
Type: `String`  
Default: `undefined`

Sitemap destination. If not set, fallback to assemble destination.

## homepage
Type: `String`  
Default: `homepage` (from package.json)

Site URL

## changefreq
Type: `String`  
Default: `weekly`

How frequently the page is likely to change. This value provides general information to search engines and may not correlate exactly to how often they crawl the page. Valid values are:

 - always
 - hourly
 - daily
 - weekly
 - monthly
 - yearly
 - never

## priority
Type: `Float`  
Default: `0.5`

The priority of this URL relative to other URLs on your site. Valid values range from 0.0 to 1.0. This value does not affect how your pages are compared to pages on other sites—it only lets the search engines know which pages you deem most important for the crawlers.

## exclude
Type: `Array`  
Default: `['404']`

Pages to omit from the sitemap.

```js
options: {
  sitemap: {
    exclude: ["foo", "bar"],
  },
  files: {
    ...
  }
}
```

## relativedest
Type: `String` / `Boolean`  
Default: `false`

Path to which the URLs in Sitemap and Robots should be relative to. `true` is equal to the destination path `dest` and `false` is equal to the root directory.

## basename
Type: `String`
Default: `sitemap.xml`

If you have a master sitemap that references sub-sitemaps, use this feature. For example `static-sitemap.xml`

## robot
Type: `Boolean`  
Default: `true`

Generate robots.txt from `exclusions` list.

## pretty
Type: `Boolean`
Default: `false`

When generating a sitemap with directory indexes, use pretty urls by removing `index` path segments from `http://www.example.com/directory/index.html` to to create `http://www.example.com/directory/`
