# New Breed Shopify Theme

Shopify theme for [New Breed](https://newbreedpb.com) by [Yak](https://isaacyakl.com) based on the [Venture](https://themes.shopify.com/themes/venture/styles/snowboards) theme.

Shopify Theme Kit References:

-  [Setup & Documentation](https://shopify.github.io/themekit/)
-  [Basic Quick Setup Video](https://www.youtube.com/watch?v=SWqeAM8MCFU)

## Versions

### [2022-05-03] 2.9.0

-  Improve article microdata
   -  News blogs use [Article](https://developers.google.com/search/docs/advanced/structured-data/article) -> [schema.org/NewsArticle](https://schema.org/NewsArticle)
   -  Add general article structured data to blog pages
   -  Review blogs use [Product w/ Review Snippet](https://developers.google.com/search/docs/advanced/structured-data/product#single-product-page)
-  Improve blog and article styling
   -  Hide article tags paragraph if no tags
   -  Add review article parser
-  Add automatic campaign URL queries
-  Improve product description HTML sanitization
-  Remove redundancy in mfg-sku detection
-  FAQ page template fixes

### [2022-04-12] 2.8.2

-  Add FAQs auto formatting
   -  Add styling
   -  Make collapsible sections/answers
   -  Add id attribute based on questions
   -  Add question (anchor) links
-  Improve microdata
   -  Add support for product titles with double quotes
   -  Add more conditions for product pre-order availability
-  Add structured data
   -  FAQ
   -  Breadcrumb

### [2022-04-07] 2.8.1

-  Improve microdata
   -  Product Availability
   -  Only show org and sitelinks searchbox on index/homepage
-  Add microdata
   -  Product Condition
   -  If a product is eligible for free shipping

### [2022-04-06] 2.8.0

-  Hide reviews if product is discontinued and has no reviews
-  Add structured data
   -  WebSite
   -  Organization
-  Add microdata
   -  MPN
   -  AggregateRating

### [2022-02-07] 2.7.1

-  Improve warranty notice verbiage
-  Add support for "no warranty" tag
-  Improve tag detection using downcase filter

### [2022-01-28] 2.7.0

-  Change review system to Judge.me reviews (review stars now only show if there are reviews)
-  Improve horizontal ruler placement for sales points

### [2022-01-18] 2.6.0

-  Add page-width search bar to theme template (all pages)
-  Hide ability to write new reviews when product is discontinued
-  Add robots.txt.liquid and hide review thank you page

### [2021-12-28] 2.5.2

-  Revert page title truncation because Shopify already limits to 70 characters
-  Reorder All in One Discounts divs in product-template.liquid
-  Perform housekeeping

### [2021-12-11] 2.5.1

-  SEO optimizations (per MOZ SEO recommendations)
   -  Meta tag truncations
      -  Limit descriptions to 155 characters
      -  Limit page titles to 60 characters
   -  Remove automatic branding from page titles
-  Add product not found snippet to collection pages
-  Add manufacturer sku to product pages when available
-  Improve product placeholder image feature for when a product image is not uploaded

### [2021-12-04] 2.5.0

Add support for [All In One Automatic Discounts app](https://apps.shopify.com/all-in-one-automatic-discounts)

### [2021-09-10] 2.4.0

Improve search section and add product missing info on search pages

### [2021-09-09] 2.3.1

Remove COVID-19 warnings (product pages and email notices) and delete unnecessary comments

### [2021-06-07] 2.3.0

Add second-image peek feature and support for pre-order release and back-in-stock dates

## To-Do

-  Product Review Blog Article
   -  Change top CTA button text to "SEE IT"
   -  Make product title link to product page
   -  Remove blank line between product title and editor rating headers
   -  Center H1 and blog metadata
-  Improve article microdata
   -  How-to blogs use [How-to](https://developers.google.com/search/docs/advanced/structured-data/how-to)
-  Update visible SKU when product options are changed
-  Add FAQs searchbox
-  Set max-height of product images on product pages to be less than 50% of viewport: [https://newbreedpb.com/products/umarex-walther-ppq-gbb-magazine-black](https://newbreedpb.com/products/umarex-walther-ppq-gbb-magazine-black)
-  Create custom gift card templates for different holidays - https://shopify.dev/themes/architecture/templates/gift-card-liquid

-  Add Back Order and Pre-Order Release date tag
-  Turn off Back Order and Pre-Order if Release date tag is reached or item is in stock

-  Add newbreed-image-not-available.jpg to collections and other items that generate a featured image (e.g. product image in product-template.liquid)
-  Procedurally generate collection images using most popular product and a serverless function - https://www.youtube.com/watch?v=A0Ww-SU7K5E, https://acloudguru.com/blog/engineering/serverless-image-optimization-and-delivery, https://serverless-stack.com/chapters/dynamically-generate-social-share-images-with-serverless.html

-  Discontinued products should only display in collections and featured sections if they are in stock
-  Discontinued products can still be purchased if they are in stock and the discontinued label should be hidden temporarily both on product cards and page
-  Discontinued products should be found in search results

-  Add predictive search feature — https://shopify.dev/tutorials/add-predictive-search-to-your-shopify-theme
-  Improve link color contrast visibility

## New Version Procedure

Before making changes to the theme follow this procedure to avoid editing on the live website.

1. Login to the Shopify backend.
2. Navigate to Online Store > Themes.
3. Duplicate the current theme.
4. Publish the duplicated theme with "Copy of" in the name (e.g. "Copy of New Breed 2.3.0").
5. Rename the old, unpublished theme to the newer version number you will be working on (e.g. "New Breed 2.3.1").
6. Rename the duplicated, published theme so that it does not have "Copy of" in it but still represents the older theme version number (e.g. "New Breed 2.3.0").
7. Update the version number in `package.json` to reflect the version in development.

## Edit Procedure

Whenever changes are being made follow this procedure.

1. Start `theme watch` (or `npm run watch`).
2. Preview the changes by running `theme open` (or `npm run preview`) or by finding the new theme in the Shopify backend and selecting "Customize" on it.

```
NOTE: Some theme code changes made for 3rd party Shopify applications (e.g. variant code swatches, up sells) may not be preview-able unless you view the theme via the "Customize" button/view.
```

3. Edit and commit changes as necessary.

## Publish Procedure

Once a new version is ready to go live refer to this procedure.

1. Add the release date, new version number, and description to the `README.md` versions section.
2. Commit with the message formatted: `Publish v<version#>`.
3. Go to the Shopify backend and navigate to Online Store > Themes.
4. Find the theme with the new version that you have been editing (e.g. "New Breed 2.3.1").
5. Publish the new theme version.
6. Verify that it has successfully published to the live site and is now the current theme.
