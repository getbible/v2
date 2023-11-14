# getBible Json API V2

- [Query API endpoint](#query-api-endpoint)
- [Main API endpoint](#main-api-endpoint)
- [Mapping helpers](#mapping-helpers)

## Query API endpoint

### QUERY API for individual/grouped verses

Together with our new release of the GetBible API V2, we are very excited to announce the release of the **grouped verse Query API**.

The QUERY API is now hosted on [https://query.getbible.net/v2/kjv/1 John 3:16](https://query.getbible.net/v2/kjv/1%20John%203:16).

#### Why the Query API?

- **Grouped Verses**: Select specific verse groupings for targeted scriptural insights.
- **Multi-Chapter Retrieval**: Gather verses from a variety of chapters in one go.
- **Single Translation Focus**: Query verses from one Bible translation at a time.
- **Performance Optimized**: Fast and reliable responses, even for comprehensive queries.
- **Simple Integration**: Easy to implement with clear documentation, allowing for quick deployment in any project.

#### Query API Usage

The design allows for one translation at a time: `https://query.getbible.net/v2/[translation]/[references]`

But with multiple scripture references:

[https://query.getbible.net/v2/kjv/John 3:16; 1 John 3:16; John 1:1](https://query.getbible.net/v2/kjv/John%203:16;%201%20John%203:16;%20John%201:1)

The *book name* or *book number* must be in each reference.

#### Various Verse Options

Query API grouped verses like this:

[https://query.getbible.net/v2/kjv/John 3:16,17,18,19; 1 John 3:16-19,22](https://query.getbible.net/v2/kjv/John%203:16,17,18,19;%201%20John%203:16-19,22)

or like this

[https://query.getbible.net/v2/kjv/John 3:16-19; 1 John3:16-19,22](https://query.getbible.net/v2/kjv/John%203:16-19;%201%20John3:16-19,22)

or like this

[https://query.getbible.net/v2/kjv/John 3:16-19; 1 John3:16-19; 1 John 3:22](https://query.getbible.net/v2/kjv/John%203:16-19;%201%20John3:16-19;%201%20John%203:22)

#### More details

**Give attention to spaces.**

There can be spaces or not between the book name and chapter, as well as before the book name if it has a number like this:

[https://query.getbible.net/v2/kjv/1John3:16-19](https://query.getbible.net/v2/kjv/1John3:16-19)

or this

[https://query.getbible.net/v2/kjv/1 John 3:16-19](https://query.getbible.net/v2/kjv/1%20John%203:16-19)

But when using the book number to reference the Bible book name, spaces are *required*:

[https://query.getbible.net/v2/kjv/62 3:16-19](https://query.getbible.net/v2/kjv/62%203:16-19)

When querying multiple references: After semicolons, spaces are optional:

[https://query.getbible.net/v2/kjv/John3:16,17;1John3:16-19,22](https://query.getbible.net/v2/kjv/John3:16,17;1John3:16-19,22)

**Remember**: The verses you queried will return in the order of your query, even of the verses within a chapter.

[https://query.getbible.net/v2/kjv/John 3:6; Genesis 1:27;John 1:3,2](https://query.getbible.net/v2/kjv/John%203:6;%20Genesis%201:27;John%201:3,2)

#### Book Names

**Use the book names found in the translation book list.**

Each translation has its own book list as shown in the [MAPPING HELPER](https://getbible.net/docs#mapping-helpers) area. Building queries with those names will work for each translation.

As a **default**, all the book names for the [KJV](https://api.getbible.net/v2/kjv/books.json) works for all translations.

Examples:

- Ancient Hebrew Books (OWN-NAMES): [https://query.getbible.net/v2/codex/בְּרֵאשִׁית 1:26](https://query.getbible.net/v2/codex/בְּרֵאשִׁית%201:26)
- Ancient Hebrew Books (KJV-NAMES): [https://query.getbible.net/v2/codex/Genesis 1:26](https://query.getbible.net/v2/codex/Genesis%201:26)

- Afrikaans Books (OWN-NAMES): [https://query.getbible.net/v2/aov/Johannes 3:16-19;1 Johannes 3:16-19,22](https://query.getbible.net/v2/aov/Johannes%203:16-19;1%20Johannes%203:16-19,22)
- Afrikaans Books (KJV-NAMES): [https://query.getbible.net/v2/aov/John 3:16-19;1 John 3:16-19,22](https://query.getbible.net/v2/aov/John%203:16-19;1%20John%203:16-19,22)

#### Restrictions

When you want a whole chapter or book, this query API is not for you; use the **Main API** as explained below.

Like this: [https://api.getbible.net/v2/kjv/66/3.json](https://api.getbible.net/v2/kjv/66/3.json)

## Main API endpoint

### Main API for complete translation, book, or chapter

The GetBible API is a robust and flexible interface designed to provide comprehensive access to many translations of the Bible. With the GetBible API, users can retrieve various portions of the Bible with ease, making it an ideal resource for developers, content creators, and educators who need full-scope access to biblical texts for their projects and platforms.

The MAIN API is hosted on [https://api.getbible.net/v2/kjv/62/3.json](https://api.getbible.net/v2/kjv/62/3.json).

#### Why the Main API?

- **Complete Translation Retrieval**: Retrieve a whole translation at once.
- **Complete Book Retrieval**: Retrieve a whole book in a selected translation at once.
- **Complete Chapter Retrieval**: Retrieve a whole chapter of a selected book and translation at once.
- **Bulk Retrieval**: This endpoint is made for fast bulk retrieval of the scripture.

#### Main API Usage

The design allows for one translation-book-chapter at a time:
- `https://api.getbible.net/v2/[translation].json`
- `https://api.getbible.net/v2/[translation]/[book_number].json`
- `https://api.getbible.net/v2/[translation]/[book_number]/[chapter_number].json`

#### Restrictions

When you want selected verses of a chapter, this API is not what you are looking for; use the query API as explained above.

Like this: [https://query.getbible.net/v2/kjv/John 3:16,17; 1 John 3:16-19,22](https://query.getbible.net/v2/kjv/John%203:16,17;%201%20John%203:16-19,22)

### GET A Translation

For one translation:
- [https://api.getbible.net/v2/kjv.json](https://api.getbible.net/v2/kjv.json)
- [https://api.getbible.net/v2/aov.json](https://api.getbible.net/v2/aov.json)

### GET A Book

- Psalms: [https://api.getbible.net/v2/kjv/62.json](https://api.getbible.net/v2/kjv/62.json)
- Openbaring: [https://api.getbible.net/v2/aov/62.json](https://api.getbible.net/v2/aov/62.json)

### GET A Chapter

- 1 John 3: [https://api.getbible.net/v2/kjv/62/3.json](https://api.getbible.net/v2/kjv/62/3.json)
- 1 Johannes 3: [https://api.getbible.net/v2/aov/62/3.json](https://api.getbible.net/v2/aov/62/3.json)

## Mapping Helpers

To help users interact with our API, we have added mapping helpers. These helpers will inform you of any changes via a hash for various parts of the scripture, validate downloads, inform you of each translation's scope of the Holy Scripture, and other useful information.

### Translations

- LIST ALL: [https://api.getbible.net/v2/translations.json](https://api.getbible.net/v2/translations.json)
- CHECKSUMS: [https://api.getbible.net/v2/checksum.json](https://api.getbible.net/v2/checksum.json)

### Books

- LIST ALL: [https://api.getbible.net/v2/kjv/books.json](https://api.getbible.net/v2/kjv/books.json)
- CHECKSUMS: [https://api.getbible.net/v2/kjv/checksum.json](https://api.getbible.net/v2/kjv/checksum.json)

### Chapters

- LIST ALL: [https://api.getbible.net/v2/kjv/62/chapters.json](https://api.getbible.net/v2/kjv/62/chapters.json)
- CHECKSUMS: [https://api.getbible.net/v2/kjv/62/checksum.json](https://api.getbible.net/v2/kjv/62/checksum.json)

We continue our journey to keep the integrity of the Holy Scripture and provide the most accurate text to all users. If you have any questions or need further clarification, please feel free to open issues in the relevant repositories, and we'll respond as soon as we can.
[Open an Issue and Get Support)](https://git.vdm.dev/getBible/support)
