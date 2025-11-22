# Database Schema

## Table 1: Scripts
| Column Name      | Data Type         | Description                |
|------------------|-------------------|----------------------------|
| scriptsId        | int               | Primary Key                |
| title            | nvarchar(max)     | Title of the script        |
| originalText     | nvarchar(max)     | Original text              |
| cleanedText      | nvarchar(max)     | Cleaned text               |
| hookLine         | nvarchar(max)     | Hook line                  |
| createdOn        | datetimeoffset    | Creation timestamp         |

## Table 2: Scenes
| Column Name      | Data Type         | Description                |
|------------------|-------------------|----------------------------|
| scenesId         | int               | Primary Key                |
| scriptId         | int (Foreign Key) | References scriptsId       |
| sceneNumber      | int               | Scene number               |
| sceneText        | nvarchar(max)     | Scene text                 |
| duration         | float             | Duration of the scene      |

---
- All column names use camelCase.
- The `scriptId` in `Scenes` is a foreign key referencing `scriptsId` in `Scripts`.
- The SQLite database file will be located in the `PulseData` folder.
