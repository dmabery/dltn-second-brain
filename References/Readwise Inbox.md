1

```dataviewjs

const mediaType = ""

const numToShow = 50

const mediaFolder = '"Readwise"'

const statusTag = '#status/integrate'

const conditions = [mediaFolder, statusTag]

const filterCondition = conditions.join(' and ')

dv.table(["File Name", "Author", "Last Synced"],

    dv.pages(filterCondition)

    .sort(p => [].concat(p.synced).reduce((a,b) => {return a > b ? a : b;}), 'desc')

	.slice(0, numToShow)

    .map(p => [

            p.file.link,

            p.author,

            [].concat(p.synced).reduce((a,b) => {return a > b ? a : b;})

        ]

    )

)
```




