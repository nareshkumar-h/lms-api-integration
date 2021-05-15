# lms-api-integration


#### List Courses

|  id | title   | description  | about  | cover | 
|---|---|---|---|---|
|  1261 | Git   | Git Commands   | In this course, you will learn Git Commands.  | null |


#### List Course - Settings

|  id | publicSignup | enableLeaderboard | featured | progressionBehavior | progressionLimit |  publicPreview | thumbnail |
|---|---|---|---|---|--|--|--|
|  1261 | false | false | true | Strict | null | false | null|

 
```
query courses ($after: String, $before: String, $first: Int, $last: Int, $search: String, $status: CourseStatus, $id: ID) {
    courses (after: $after, before: $before, first: $first, last: $last, search: $search, status: $status, id: $id) {
        edges {
            cursor
            node {
                about
                archivedAt
                cover {
                    filename
                    url
                }
                description
                enableLeaderboard
                endsAt
                featured
                id
                name
                progressionBehavior
                progressionLimit
                publicPreview
                publicSignup
                thumbnail {
                    filename
                    url
                }
            }
        }
        nodes {
            about
            archivedAt
            cover {
                filename
                url
            }
            description
            enableLeaderboard
            endsAt
            featured
            id
            name
            progressionBehavior
            progressionLimit
            publicPreview
            publicSignup
            thumbnail {
                filename
                url
            }
        }
        pageInfo {
            endCursor
            hasNextPage
            hasPreviousPage
            startCursor
        }
        totalCount
    }
}
```
```
{
  "first": 20
}
```
