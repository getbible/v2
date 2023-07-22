# V2 GetBible API

GetBible has taken an essential leap forward in maintaining the integrity and accuracy of the Holy Scripture that we provide. We, with a heavy heart, have moved away from an open public repository of the Holy Scripture due to constant updates from Crosswire and others to their modules. As these updates are aimed at fixing typos and other mistakes, an open public repository like [Unbound-Biola](https://github.com/getbible/Unbound-Biola) could become outdated, leading those who forked it to have outdated and incorrect text. We realized the potential consequences and to rectify it, have developed a new [API version 2](https://github.com/getbible/v2).

Our API is now hosted on [api.getbible.net/v2/translations.json](https://api.getbible.net/v2/translations.json), ensuring it remains synchronized with the [Crosswire Modules](http://www.crosswire.org/sword/modules/ModDisp.jsp?modType=Bibles). This change, though seems like a step back, is a significant improvement after months of careful consideration and prayer.

# Legacy and New API Versions

We have decided to keep the old API (the current URL query option on getBible.net) active until the end of 2021. Therefore, we encourage users to transition to the newer, more efficient version as soon as possible.

As long as the Lord permits, we will maintain two versions of our API. The version one (V1) will return the Holy Scripture in the same format as the original (old API) but with a new URL query format. The version two ([V2](https://github.com/getbible/v2)) is the new format introduced to address common issues and provide a better, faster, stronger, more accurate, and convenient API of the Holy Scripture.

## API Usage

Here's how the query formats have changed:

The old API query:
- https://archived.getbible.net/json?passage=1Jn3 (being archived)

The new V1 API query:
- https://api.getbible.net/v1/kjv/62/3.json

The new [V2](https://github.com/getbible/v2) API query:
- https://api.getbible.net/v2/kjv/62/3.json

### Mapping Helpers

To help users interact with our API, we have added mapping helpers. These helpers will inform you of any changes via a hash for various parts of the scripture, validate downloads, inform you of each translation's scope of the Holy Scripture, and other useful information.

> Translations
- For one translation: https://api.getbible.net/v2/kjv.json
- For translations: https://api.getbible.net/v2/translations.json
- For translations: https://api.getbible.net/v2/translations
- For translations: https://api.getbible.net/v2/checksum.json
- For translations: https://api.getbible.net/v2/checksum

> Translation Books
- For one book: https://api.getbible.net/v2/kjv/19.json
- For books: https://api.getbible.net/v2/kjv/books.json
- For books: https://api.getbible.net/v2/kjv/books
- For books: https://api.getbible.net/v2/kjv/checksum.json
- For books: https://api.getbible.net/v2/kjv/checksum

> Book Chapters
- For one chapter: https://api.getbible.net/v2/kjv/62/3.json
- For a book: https://api.getbible.net/v2/kjv/62/chapters.json
- For a book: https://api.getbible.net/v2/kjv/62/chapters
- For a book: https://api.getbible.net/v2/kjv/62/checksum.json
- For a book: https://api.getbible.net/v2/kjv/62/checksum

We continue our journey to keep the integrity of the Holy Scripture and provide the most accurate text to all users. If you have any questions or need further clarification, please feel free to open issues in the relevant repositories, and we'll respond as soon as we can.

Thank you for your attention and for being a part of our mission at getBible.
