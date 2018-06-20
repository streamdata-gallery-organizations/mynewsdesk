---
swagger: "2.0"
x-collection-name: Mynewsdesk
x-complete: 0
info:
  title: My News Desk Pressroom List News Search
  description: News Search
  termsOfService: http://www.mynewsdesk.com/about/terms-and-conditions?locale=en
  version: v1
host: www.mynewsdesk.com
basePath: /services/pressroom/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  create_comment/:
    get:
      summary: Create Comment
      description: Create Comment
      operationId: getCreateComment
      x-api-path-slug: create-comment-get
      parameters:
      - in: query
        name: blog
        description: URL of commenters blog/website
      - in: query
        name: body
        description: Content of comment
      - in: query
        name: commentable_id
        description: ID of the material that is commented
      - in: query
        name: email
        description: Email address of commenter
      - in: query
        name: name
        description: Name of commenter
      - in: query
        name: type_of_media
        description: Type of material
      - in: path
        name: unique key
        description: The MyNewsDesk API Key
      - in: query
        name: user_ip
        description: IP number of commenter
      responses:
        200:
          description: OK
      tags:
      - Comment
  list/:
    get:
      summary: Lists news
      description: Lists news
      operationId: getList
      x-api-path-slug: list-get
      parameters:
      - in: query
        name: archived
        description: Fetch items marked as archived, this is useful for fetching old
          events
      - in: query
        name: callback
        description: If format is JSON and callback is specified, the JSON response
          is wrapped in a function call with the specified callback name
      - in: query
        name: format
        description: 'Specify the format of the response: RSS 2'
      - in: query
        name: limit
        description: Set the maximum number of items in the response
      - in: query
        name: offset
        description: Specify which item (sequentially) should be first, skipping preceding
          items
      - in: query
        name: order
        description: 'Specify the sort order of the result: publish date (published),
          latest update (updated) or creation date (created)'
      - in: query
        name: pressroom
        description: Set the pressroom to fetch material from
      - in: query
        name: type_of_media
        description: Fetch material of this type only
      - in: path
        name: unique key
        description: The MyNewsDesk API Key
      responses:
        200:
          description: OK
      tags:
      - News
  pressroom_info/:
    get:
      summary: Pressroom Info
      description: Pressroom Info
      operationId: getPressroomInfo
      x-api-path-slug: pressroom-info-get
      parameters:
      - in: query
        name: pressroom
        description: Set the pressroom to search in
      - in: path
        name: unique key
        description: The MyNewsDesk API Key
      responses:
        200:
          description: OK
      tags:
      - News
      - Pressroom
      - Info
  search/:
    get:
      summary: News Search
      description: News Search
      operationId: getSearch
      x-api-path-slug: search-get
      parameters:
      - in: query
        name: callback
        description: If format is JSON and callback is specified, the JSON response
          is wrapped in a function call with the specified callback name
      - in: query
        name: date_end
        description: End date
      - in: query
        name: date_mode
        description: Specifies how the date parameters are used
      - in: query
        name: date_on
        description: Date
      - in: query
        name: date_start
        description: Start date
      - in: query
        name: format
        description: 'Specify the format of the response: RSS 2'
      - in: query
        name: limit
        description: Set the maximum number of items in the response
      - in: query
        name: page
        description: Page number in the search result
      - in: query
        name: pressroom
        description: Set the pressroom to search in
      - in: query
        name: query
        description: Search string
      - in: query
        name: type_of_media
        description: The type of material to be fetched
      - in: path
        name: unique key
        description: The MyNewsDesk API Key
      responses:
        200:
          description: OK
      tags:
      - News
      - Search
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---