# V2 GetBible API (2020)

We have **completely** moved away from an **open public repository** of the Holy Scripture, with **great sorrow and struggle**. This is because of a huge blow-back from Crosswire and other, saying that they regularly find typos and other mistakes in their modules of the Holy Scripture, and then they fix it. This means an open public repository like [Unbound-Biola](https://github.com/getbible/Unbound-Biola) becomes outdated, and all those who forked it have outdated and incorrect text. **This was never our intent, and so in seeking to correct this issue, we now created a whole new [API version 2](https://github.com/getbible/v2)** that will be hosted only on [api.getbible.net/v2/translations.json](https://api.getbible.net/v2/translations.json) itself to ensure it remains totaly in sync with the [Crosswire Modules](http://www.crosswire.org/sword/modules/ModDisp.jsp?modType=Bibles). This is a step back, but after months of prayer and tears it seems like the only way forward at this time.

# How will this work and is the old API still active?

We will keep the old API (the current URL query option on getBible.net) active for another year, ending 2021. We therefore encourage you all to upgrade to the newer, better option, explained below, as soon as you can.

We will always have a Version one (V1) and a Version two ([V2](https://github.com/getbible/v2)) as long as the Lord permits. V1 will return the Holy Scripture in the same format as the original (old API) but with a whole new URL query format, which we will explain in details below. [V2](https://github.com/getbible/v2) will serve as the new format being introduced to solve common issues and provide a better, faster, stronger, more accurate, and convenient API of the Holy Scripture.

## How will this work?

The old API query looked like this:
- https://getbible.net/json?passage=1Jn3

The new API (V1) query will look like this:
- https://api.getbible.net/v1/kjv/62/3.json

>That is really the only change, but we trust it will serve us all better.

[V2](https://github.com/getbible/v2) query will look like this:
- https://api.getbible.net/v2/kjv/62/3.json

### Mapping Helpers

Since we will be working with numbers and translation abbreviations, we will be adding helper mappers which are available in this repository, and in the API's respectively. The purpose of these mapping helpers are to inform you of any changes via a hash for various parts of the scripture, and to validate downloads. Then these mapping helpers will also serve to inform you of each translation's scope of the Holy Scripture, and other helpful information.

> Translations
- For translations: https://api.getbible.net/v2/translations.json
- For translations: https://api.getbible.net/v2/translations
- For translations: https://api.getbible.net/v2/checksum.json
- For translations: https://api.getbible.net/v2/checksum

> Translation Books
- For books: https://api.getbible.net/v2/kjv/books.json
- For books: https://api.getbible.net/v2/kjv/books
- For books: https://api.getbible.net/v2/kjv/checksum.json
- For books: https://api.getbible.net/v2/kjv/checksum

> Book Chapters
- For a book: https://api.getbible.net/v2/kjv/62/chapters.json
- For a book: https://api.getbible.net/v2/kjv/62/chapters
- For a book: https://api.getbible.net/v2/kjv/62/checksum.json
- For a book: https://api.getbible.net/v2/kjv/62/checksum
