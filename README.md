# Names by Country Dataset

Human names are so ubiquitous and fundamental to our day-to-day lives that it's easy to forget how important -- and complex -- they can be. For example, did you know:

* The U.S. Census removes all spaces from surnames, which makes culturally distinct surnames like "de la Cruz" (predominantly Hispanic), "dela Cruz" (Filipino), and "Delacruz" (anglicized) the same in the eyes of census reporting.[^1]
* The majority of Indonesians do not have family names. Rather, their given names are geographically and culturally specific.[^2]
* In traditional Lithuanian culture, the ending of a woman's surname indicates whether she is married or not. Last names of married women end in -ienė while those of unmarried girls end in -ytė, -iūtė, -utė, -aitė.[^3]
* Many Portuguese surnames may be preceded by of/from (de, d') or of the/from the (do, da, dos, das) as in de Sousa, da Costa, d'Oliveira. Those elements are not part of the surname and are not considered in an alphabetical order.[^4]

## The Need

Despite the importance of names, it's difficult to find large, trustworthy, free, easy-to-use name datasets with clear provenance about given names/first names/forenames and family names/lastnames/surnames from across the world online. There are many datasets available that do an outstanding job at addressing some of these needs, but not all. For example:

* [The U.S. Census](https://www.census.gov/topics/population/genealogy/data/2010_surnames.html) provides outstanding data, but only for US surnames.
* [The U.S. Social Security Administration](https://www.ssa.gov/oact/babynames/) provides outstanding data, too, but only for US forenames.
* [FiveThirtyEight most common name dataset](https://github.com/fivethirtyeight/data/tree/master/most-common-name) is also US-only, since it's based on the Census.
* [solenium/names-dataset](https://github.com/solvenium/names-dataset) is simple and easy to use, but doesn't indicate what countries names come from, nor their popularities.
* [davidam/damegender](https://github.com/davidam/damegender) is well-documented, easy to use, and multinational, but only covers forenames.
* [philipperemy/name-dataset](https://github.com/philipperemy/name-dataset) dataset is clearly comprehensive, but there is no indication of the most popular names, and there is no romanization. (And some users may have legitimate concerns about the provenance of the data, too.)
* [census.name](https://census.name/) is paid only.

I need a names dataset for doing some software testing, so this was disappointing.

## The Dataset

Since there wasn't one already -- or, at least, not one I could find -- [I made one myself](https://xkcd.com/927/). It attempts to address the following needs:

* Free -- This dataset is released under the Creative Commons CC0 license.
* Popular names -- Included names are reported to be the most popular, by country. Each name includes a count of people with the name within the country when available.
* Big Enough for Testing -- 2,370 Forenames and 2,278 Surnames, many with multiple representations.
* Multinational -- Forenames from 106 countries, Surnames from 75. Generally at least 10 each per country. In particular, there are many names from CJK and RTL languages available.
* Clear provenance -- Data is pulled from `https://en.wikipedia.org/wiki/Lists_of_most_common_surnames` and `https://en.wikipedia.org/wiki/List_of_most_popular_given_names` the week of Jul 8, 2023.
* Easy-to-use -- Data is available in simple JSON formats.
* Romanization -- Names in non-Latin scripts include Romanization, either as provided or sourced from Google Translate.

These data should allow users to build comprehensive test suites for important features involving names, particularly i18n and l10n.

The following countries are represented:

### 🇦🇩🇦🇪🇦🇱🇦🇲🇦🇷🇦🇹🇦🇺🇦🇼🇦🇿🇧🇦🇧🇩🇧🇪🇧🇬🇧🇴🇧🇷🇧🇾🇨🇦🇨🇭🇨🇱🇨🇳🇨🇴🇨🇷🇨🇺🇨🇾🇨🇿🇩🇪🇩🇰🇩🇴🇩🇿🇪🇨🇪🇪🇪🇬🇪🇸🇫🇮🇫🇯🇫🇴🇫🇷🇬🇧🇬🇪🇬🇬🇬🇮🇬🇱🇬🇶🇬🇷🇬🇹🇭🇷🇭🇹🇭🇺🇮🇪🇮🇱🇮🇲🇮🇳🇮🇶🇮🇷🇮🇸🇮🇹🇯🇪🇯🇲🇯🇴🇯🇵🇰🇬🇰🇭🇰🇷🇰🇼🇰🇿🇱🇧🇱🇮🇱🇰🇱🇹🇱🇺🇱🇻🇱🇾🇲🇦🇲🇨🇲🇩🇲🇪🇲🇰🇲🇱🇲🇳🇲🇹🇲🇽🇲🇾🇳🇱🇳🇴🇳🇵🇳🇿🇵🇦🇵🇪🇵🇫🇵🇭🇵🇰🇵🇱🇵🇷🇵🇹🇵🇾🇷🇴🇷🇸🇷🇺🇸🇦🇸🇮🇸🇰🇸🇲🇸🇷🇸🇻🇹🇭🇹🇯🇹🇳🇹🇷🇹🇼🇺🇦🇺🇸🇺🇾🇻🇪🇻🇳🇽🇰🇿🇦

## The Data

You can get the data a few different ways:

* Download the CSV files from this repo
* Download the JSON files the releases on this repo
* Clone this repo and run `make`

## The License

The data is available under the Creative Commons CC0 license. This places the data into the public domain, so you can do whatever you'd like with it, but I'd appreciate a note if you find it useful! You can open a ticket to say hello 👋 if nothing else.

## Maintenance

I have no plans to keep this dataset up to date over time. In my opinion, names do not change fast enough to require regular tracking for the purpose of testing. However, it is very important that the data represent here be trustworthy and easy to use, so if you find an error -- for example, if I left a comma in a name -- then please open a ticket!

# References
[^1]: https://www2.census.gov/topics/genealogy/2010surnames/Names_2010Census_Top1000.xlsx
[^2]: https://en.wikipedia.org/wiki/Indonesian_names
[^3]: https://en.wikipedia.org/wiki/List_of_most_common_surnames_in_Europe#cite_note-43
[^4]: https://en.wikipedia.org/wiki/List_of_most_common_surnames_in_Europe#Portugal
