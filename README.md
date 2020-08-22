# New Breed Shopify Theme
Shopify theme for [New Breed](https://newbreedpb.com) by [Yak](https://isaacyakl.com) based on the [Venture](https://themes.shopify.com/themes/venture/styles/snowboards) theme.

Shopify Theme Kit References: 
- [Setup & Documentation](https://shopify.github.io/themekit/)
- [Basic Quick Setup Video](https://www.youtube.com/watch?v=SWqeAM8MCFU)

## Version
### [2020-08-21] 2.0.0
Restart based on [Venture](https://themes.shopify.com/themes/venture/styles/snowboards) theme.
### [2020-08-20] 1.1.1
Cleanup old code.
### [2019-11-18] 1.1.0
Revamp from old style.

## To-Do
- Add phone number and email
- Add free shipping notice
- Add "Trade Now" button
- Expand search bar by default on desktop
- Add Google reviews section
- Add Instagram widget
- Add credits in footer
- Add COVID-19 warning on product pages
- Add product info badges on product pages
- Fix slides for mobile (slide buttons cover part of the image)

## New Version Procedure
Before making changes to the theme follow this procedure to avoid editing on the live website.
1. Go to the Shopify backend and navigate to Online Store > Themes.
2. Duplicate the current theme.
2. Find the duplicated theme with "Copy" in the name.
3. Publish the duplicated theme.
4. Rename the old, unpublished theme with the newer version number you will be working on (e.g. "New Breed 2.0.1").
5. Rename the duplicated, published theme so that it does not have "Copy" in it but still represents the older theme version number (e.g. "New Breed 2.0.0").
6. Update `package.json` and `README.md` to reflect the newer version.

## Edit Procedure
Whenever changes are being made follow this procedure.
1. Start `theme watch`.
2. Begin to edit the theme.
8. Preview the changes by running `theme open` or by finding the new theme in the Shopify backend and selecting "Preview" from its actions menu.
9. Commit changes as necessary.

## Publish Procedure
Once a new version is ready to go live refer to this procedure.
1. Go to the Shopify backend and navigate to Online Store > Themes.
2. Find the theme with the new version that you have been editing (e.g. "New Breed 2.0.1").
3. From the new theme's actions menu select "Publish".
4. Verify that it has successfully publish to the live site and is now the current theme.