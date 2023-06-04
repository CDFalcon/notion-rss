# notion-rss
Get RSS feeds in notion.so daily

## Database Interface
This project uses two notion databases: to store RSS links (to subscribe to), to store the RSS content. 

### Feeds Database

| Property Name | Property Type |
| --- | :-- |
| Title | title |
| Link | url |
| Enabled | checkbox |

### Content Database

| Property Name | Property Type |
| --- | :-- |
| Title | title |
| Link | Url |
| Description | Text |
| Enabled | Checkbox |
| From | Select |
| Categories | MultiSelect |
| Published | Date |
| Starred | Checkbox |
| Created | Date |

## Github Action Secrets
Github Secrets needed in the repository for the workflow actions to work:
- `NOTION_API_TOKEN`: notion.so api token for a specific integration. Integration must have access to `NOTION_RSS_CONTENT_DATABASE_ID` and `NOTION_RSS_FEEDS_DATABASE_ID`.     
- `NOTION_RSS_CONTENT_DATABASE_ID`: notion.so database id that stores RSS content (see Database Interface / Content Database).
- `NOTION_RSS_FEEDS_DATABASE_ID`: notion.so database id that stores RSS feed details (see Database Interface / Feeds Database).
