---
swagger: "2.0"
x-collection-name: Plentymarkets
x-complete: 0
info:
  title: Plentymarkets Get the content of a file from the inbox
  description: Gets the content of a file stored in the inbox. The storage key (i.e.
    file path) must be specified.
  contact:
    name: plentymarkets
    url: https://forum.plentymarkets.com/c/rest-api
  version: 1.0.0
host: example.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /rest/storage/plugins/inbox:
    delete:
      summary: Delete files from the inbox
      description: Deletes a list of files from the inbox. A list of storage keys
        must be specified.
      operationId: deleteRestStoragePluginsInbox
      x-api-path-slug: reststoragepluginsinbox-delete
      parameters:
      - in: query
        name: keyList
        description: List of storage keys for the files to be deleted
      responses:
        200:
          description: OK
      tags:
      - Files
      - From
      - Inbox
    post:
      summary: Upload a file to the inbox
      description: Uploads a file to the inbox. The storage key (i.e. file path) must
        be specified.
      operationId: postRestStoragePluginsInbox
      x-api-path-slug: reststoragepluginsinbox-post
      parameters:
      - in: query
        name: key
        description: The storage key for the file to upload
      responses:
        200:
          description: OK
      tags:
      - Upload
      - File
      - To
      - Inbox
  /rest/storage/plugins/inbox/list:
    get:
      summary: List files from the inbox
      description: |-
        Lists all files of all plugins stored in the inbox. A prefix can be specified to list all files of a specific
        plugin folder only.
      operationId: getRestStoragePluginsInboxList
      x-api-path-slug: reststoragepluginsinboxlist-get
      parameters:
      - in: query
        name: prefix
        description: Prefix to list all files of a specific plugin folder only
      responses:
        200:
          description: OK
      tags:
      - List
      - Files
      - From
      - Inbox
  /rest/storage/plugins/inbox/object-url:
    get:
      summary: Get the content of a file from the inbox
      description: Gets the content of a file stored in the inbox. The storage key
        (i.e. file path) must be specified.
      operationId: getRestStoragePluginsInboxObjectUrl
      x-api-path-slug: reststoragepluginsinboxobjecturl-get
      parameters:
      - in: query
        name: key
        description: The storage key for the file to retrieve
      responses:
        200:
          description: OK
      tags:
      - Content
      - Of
      - File
      - From
      - Inbox
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