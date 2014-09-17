[google-play-badge-svg](http://steverichey.github.io/google-play-badge-svg/)
=====================

Hosting for localized versions of Google Play badges in SVG format.

## About

It's possible to use Apple's linkmaker service to generate localized "Download on the App Store" SVG badges for your application. However, no similar service exists for Google's "Get it on Google Play" badges.

This repository serves mostly as hosting for Google's badges in SVG format.

## Usage

Simply link to the badge you require like so:

````
<img src="http://steverichey.github.io/google-play-badge-svg/img/en_get.svg">
````

Which leads to [this](http://steverichey.github.io/google-play-badge-svg/img/en_get.svg) image. Pretty handy! Be sure to add your own URL as well:

````
<a href="https://play.google.com/store/apps/details?id=com.example.myapp">
<img alt="Get it on Google Play" src="http://steverichey.github.io/google-play-badge-svg/img/en_get.svg" />
</a>
````

And you'll get something like this:

<a href="https://play.google.com/store/apps/details?id=com.example.myapp">
<img align="middle" alt="Get it on Google Play" src="http://steverichey.github.io/google-play-badge-svg/img/en_get.svg" />
</a>

It's that easy! With a little JavaScript to check for locale (check `navigator.language || navigator.browserLanguage`) you can then load language-specific versions of the badge:

<a href="https://play.google.com/store/apps/details?id=com.example.myapp">
<img align="middle" alt="Get it on Google Play" src="http://steverichey.github.io/google-play-badge-svg/img/zh_get.svg" />
</a>

Let me know if you have any questions, suggestions, or comments!

## Available badges

To view the list of available badges, please see [this folder](https://github.com/steverichey/google-play-badge-svg/tree/gh-pages/img). If I've made an error somewhere or you'd like an additional language added, please [open an issue](https://github.com/steverichey/google-play-badge-svg/issues).

## Notes

By default, several versions of the Google Play badge use [Proxima Nova](https://typekit.com/fonts/proxima-nova), which is copyright Mark Simonson. As I do not own this font, it was replaced with [Myriad Pro](https://typekit.com/fonts/myriad-pro). No fonts are embedded in the SVGs; instead, I opted to convert them to outlines to maximize compatibility.

## License

This repository is shared under an MIT license. See [license.md](https://github.com/steverichey/google-play-badge-svg/blob/master/license.md) for details.

Google's brand, logos, and so on are all their own trademarks and copyrights. Be sure to read the [Branding Guidelines](https://developer.android.com/distribute/tools/promote/brand.html) and contact Google via the [Android and Google Play Brand Permissions Inquiry form](https://docs.google.com/forms/d/1YE5gZpAAcFKjYcUddCsK1Bv9a9Y-luaLVnkazVlaJ2w/viewform) if you have any questions. SVGs in this repository were generated from files provided by Google [here](https://developer.android.com/distribute/tools/promote/badge-files.html) which are shared under a [Creative Commons Attribution 2.5](http://creativecommons.org/licenses/by/2.5/) license.
