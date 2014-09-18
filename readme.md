[google-play-badge-svg](http://steverichey.github.io/google-play-badge-svg/)
=====================

Hosting for localized versions of Google Play™ badges in SVG format.

## About

It's possible to use Apple's linkmaker service to generate localized "Download on the App Store" SVG badges for your application. However, no similar service exists for Google's "Get it on Google Play" badges.

This repository serves mostly as hosting for Google's badges in SVG format. Most of the files are in the [gh-pages](https://github.com/steverichey/google-play-badge-svg/tree/gh-pages) branch.

## Todo

* Optimize SVGs to minimize file size (using [this](http://petercollingridge.appspot.com/svg_optimiser) for example).
* Add "Android App on" badges

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

Or, you can call some handy JavaScript!

````
<script type="text/javascript" src="https://raw.githubusercontent.com/steverichey/google-play-badge-svg/gh-pages/get-localized.js"></script>
<script type="text/javascript">
document.write(GetLocalizedPlayBadge.forCurrentLocale());
</script>
````

Let me know if you have any questions, suggestions, or comments!

## Available badges

To view the list of available badges, please see [this folder](https://github.com/steverichey/google-play-badge-svg/tree/gh-pages/img). If I've made an error somewhere or you'd like an additional language added, please [open an issue](https://github.com/steverichey/google-play-badge-svg/issues).

## Notes

Badges are labeled by their [ISO 639-1](http://en.wikipedia.org/wiki/List_of_ISO_639-1_codes) codes wherever possible. Languages with multiple dialects, such as Chinese, are labeled by their ISO 639-1 code followed by their [ISO 639-3](http://en.wikipedia.org/wiki/ISO_639_macrolanguage) language code.

By default, several versions of the Google Play badge use [Proxima Nova](https://typekit.com/fonts/proxima-nova), which is copyright Mark Simonson. As I do not own this font, it was replaced with [Myriad Pro](https://typekit.com/fonts/myriad-pro). No fonts are embedded in the SVGs; instead, I opted to convert them to outlines to maximize compatibility.

Inclusion or omission of any language or dialect should not be misconstrued as support for any particular nationality, country, ideology, race, or similar. If there's a language in here, it's just because Google had it available or someone added it themselves. If a language is missing, it's just because Google did not have it available or I had issues with their file.

## License

Unless covered under some other license, all content in this repository is shared under an MIT license. See [license.md](https://github.com/steverichey/google-play-badge-svg/blob/master/license.md) for details.

Google Play is a trademark of Google Inc. Google's brand, logos, and so on are all their own trademarks and copyrights. Be sure to read the [Branding Guidelines](https://developer.android.com/distribute/tools/promote/brand.html) and contact Google via the [Android and Google Play Brand Permissions Inquiry form](https://docs.google.com/forms/d/1YE5gZpAAcFKjYcUddCsK1Bv9a9Y-luaLVnkazVlaJ2w/viewform) if you have any questions. SVGs in this repository were generated from files provided by Google [here](https://developer.android.com/distribute/tools/promote/badge-files.html) which are shared under a [Creative Commons Attribution 2.5](http://creativecommons.org/licenses/by/2.5/) license.
