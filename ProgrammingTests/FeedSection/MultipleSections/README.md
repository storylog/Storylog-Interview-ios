1. จาก Design ลองวิเคราะห์ออกแบบโดยใช้ UIKIT.
2. จาก json data ลองออกแบบเป็น Model คร่าวๆ ที่ใช้กับ Design.

Note: สามารถสอบถาม UI,BN,PO ได้

<p align="center">
<img width="582" alt="image-section-feed" src="https://github.com/storylog/storylog-interview-ios/blob/main/ProgrammingTests/FeedSection/MultipleSections/data/FeedScreen.jpeg">
</p>

Json
```ruby
{
    "data": {
        "feed": {
            "id": "abc",
            "sections": [
                {
                    "id": "123",
                    "layoutType": "banner",
                    "title": null,
                    "items": [
                    {
                        "type": "banner",
                        "banner": {
                            "url": "https://fictionlog.co/p/",
                            "bannerImage": "https://fic-banner1.jpeg"
                        }
                },
                {
                    "type": "banner",
                    "banner": {
                        "url": "https://fictionlog.co/p/",
                        "bannerImage": "https://fic-banner2.jpeg"
                    }
                }
                ]
            },
            {
                "id": "123",
                "layoutType": "bookCover",
                "title": "หนังสือยอดนิยม",
                "items": [
                {
                    "type": "book",
                    "book": {
                        "id": "5d1234",
                        "coverImage": "https://fic-book1.jpeg",
                        "title": "Racing",
                        "authorName": "โอนิซึกะ ฮานามิจิ",
                        "translatorName": null,
                        "category": "นิยายโรแมนติก",
                        "viewsCount": "2000",
                        "chaptersCount": "24"
                    },
                    "book": {
                        "id": "5d1234",
                        "coverImage": "https://fic-book2.jpeg",
                        "title": "Racing",
                        "authorName": "โอนิซึกะ ฮานามิจิ",
                        "translatorName": null,
                        "category": "นิยายโรแมนติก",
                        "viewsCount": "2000",
                    "chaptersCount": "24"
                    },
                }
                ]
            }
            ]
        }
    }
}
```

GraphQL
```ruby
query feed {
    feed(feedId: "home") {
        id
        sections {
            ...SectionFragment
        }
      }
}

fragment SectionFragment on Section  {
     id
    layoutType
    title
    items {
        ...SectionItemFragment
    }
}

fragment SectionItemFragment on items {
    type
    book  {
        id
        title
        authorName
        translatorName
        category
        viewsCount
        chaptersCount
        coverImage
    }
    ebook {
        id
        title
        authorName
        translatorName
        category
        coverImage
    }
    banner {
        bannerImage
        url
    }
}
```

Schema.graphQL
```ruby
type Feed {
  id: ID!
  sections: [Section]
}

type Section {
  id: ID!
  layoutType: LayoutType!
  title: String
  items: [SectionItem]!
}

enum LayoutType {
  banner
  bookCover
}

type SectionItem {
  type: SectionItemType
  book {
    id: ID!
    coverImage: String
    title: String
    authorName: String
    translatorName: String
    category: String
    viewsCount: Int
    chaptersCount: Int
  }
  ebook {
      id: ID!
      coverImage: String
      title: String
      authorName: String
      translatorName: String
      category: String
  }
  banner {
      url: String
      bannerImage: String
  }
}

enum SectionItemType {
    book
    ebook
    banner
}
```
