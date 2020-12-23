# New Breed Shopify Theme

Shopify theme for [New Breed](https://newbreedpb.com) by [Yak](https://isaacyakl.com) based on the [Venture](https://themes.shopify.com/themes/venture/styles/snowboards) theme.

Shopify Theme Kit References:

-  [Setup & Documentation](https://shopify.github.io/themekit/)
-  [Basic Quick Setup Video](https://www.youtube.com/watch?v=SWqeAM8MCFU)

## Version

### [2020-12-09] 2.0.2

Add various small improvements.

### [2020-09-17] 2.0.1

Update email notification styling and product availability info including gift card design.

### [2020-08-27] 2.0.0

Restart based on [Venture](https://themes.shopify.com/themes/venture/styles/snowboards) theme.

### [2020-08-20] 1.1.1

Cleanup old code.

### [2019-11-18] 1.1.0

Revamp from old style.

## To-Do

-  Make social media icons open in new tab
-  Add Pre-Order Release date tag
-  Turn off Pre-Order if Pre-Order Release date tag is reached
-  Expand search bar by default on desktop and make search bar more prominent
-  Do not display products tagged as "Discontinued" in collections
-  Hide ability to write reviews on Archived/Discontinued products
-  Hide Archived/Discontinued products from collection pages
-  Update SKU when product options are changed
-  Improve link color contrast visibility

## New Version Procedure

Before making changes to the theme follow this procedure to avoid editing on the live website.

1. Go to the Shopify backend and navigate to Online Store > Themes.
2. Duplicate the current theme.
3. Find the duplicated theme with "Copy" in the name.
4. Publish the duplicated theme.
5. Rename the old, unpublished theme with the newer version number you will be working on (e.g. "New Breed 2.0.2").
6. Rename the duplicated, published theme so that it does not have "Copy" in it but still represents the older theme version number (e.g. "New Breed 2.0.0").
7. Update `package.json` with the newer version number.

## Edit Procedure

Whenever changes are being made follow this procedure.

1. Start `theme watch` (or `npm run watch`).
2. Begin to edit the theme.
3. Preview the changes by running `theme open` (or `npm run preview`) or by finding the new theme in the Shopify backend and selecting "Preview" from its actions menu.
4. Commit changes as necessary.

## Publish Procedure

Once a new version is ready to go live refer to this procedure.

1. Add the release date, new version number, and description to the `README.md` version section.
2. Commit with the message formatted: `Publish v<version#>`.
3. Go to the Shopify backend and navigate to Online Store > Themes.
4. Find the theme with the new version that you have been editing (e.g. "New Breed 2.0.2").
5. From the new theme's actions menu select "Publish".
6. Verify that it has successfully publish to the live site and is now the current theme.
