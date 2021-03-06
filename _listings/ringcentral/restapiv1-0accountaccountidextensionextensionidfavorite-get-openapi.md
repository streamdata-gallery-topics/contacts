---
swagger: "2.0"
x-collection-name: RingCentral
x-complete: 0
info:
  title: RingCentral Get Favorite Contacts
  description: "Returns favorite contacts of the current extension. Favorite contacts
    include both company contacts (extensions) and personal contacts (address book
    records).\nApp Permission\nReadContacts\nUser Permission\nReadPersonalContacts\nUsage
    Plan Group\nLight\nError Codes\n\n \n  \n   HTTP Code\n   Error Code\n   Error
    Message\n   \n \n\n403\nCMN-401\nIn order to call this API endpoint, application
    needs to have [ReadContacts] permission\n\n\n403\nCMN-408\nIn order to call this
    API endpoint, user needs to have [ReadPersonalContacts] permission for requested
    resource.\n\n\n404\nCMN-102\nResource for parameter [accountId] is not found"
  version: 1.0.0
host: platform.ringcentral.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /restapi/v1.0/account/{accountId}/extension/{extensionId}/address-book/contact:
    get:
      summary: Get Contacts
      description: "Returns user personal contacts.\nApp Permission\nReadContacts\nUser
        Permission\nReadPersonalContacts\nUsage Plan Group\nHeavy\nError Codes\n\n
        \n  \n   HTTP Code\n   Error Code\n   Error Message\n   \n \n\n400\nCMN-101\nParameter
        [perPage] value is invalid\n\n\n401\nCMN-405\nLogin to extension required\n\n\n401\nOAU-151\nAuthorization
        method not supported\n\n\n403\nCMN-401\nIn order to call this API endpoint,
        application needs to have [ReadContacts] permission\n\n\n404\nCMN-102\nResource
        for parameter [accountId] is not found"
      operationId: listContacts
      x-api-path-slug: restapiv1-0accountaccountidextensionextensionidaddressbookcontact-get
      parameters:
      - in: path
        name: accountId
        description: Internal identifier of a RingCentral account or tilde (~) to
          indicate the account logged-in within the current session
      - in: path
        name: extensionId
        description: Internal identifier of an extension or tilde (~) to indicate
          the extension assigned to the account logged-in within the current session
      - in: query
        name: page
        description: Indicates the page number to retrieve
      - in: query
        name: perPage
        description: Indicates the page size (number of items)
      - in: query
        name: phoneNumber
      - in: query
        name: sortBy
        description: Sorts results by the specified property
      - in: query
        name: startsWith
        description: If specified, only contacts whose First name or Last name start
          with the mentioned substring are returned
      responses:
        200:
          description: OK
      tags:
      - Contacts
  /restapi/v1.0/account/{accountId}/extension/{extensionId}/favorite:
    get:
      summary: Get Favorite Contacts
      description: "Returns favorite contacts of the current extension. Favorite contacts
        include both company contacts (extensions) and personal contacts (address
        book records).\nApp Permission\nReadContacts\nUser Permission\nReadPersonalContacts\nUsage
        Plan Group\nLight\nError Codes\n\n \n  \n   HTTP Code\n   Error Code\n   Error
        Message\n   \n \n\n403\nCMN-401\nIn order to call this API endpoint, application
        needs to have [ReadContacts] permission\n\n\n403\nCMN-408\nIn order to call
        this API endpoint, user needs to have [ReadPersonalContacts] permission for
        requested resource.\n\n\n404\nCMN-102\nResource for parameter [accountId]
        is not found"
      operationId: listFavoriteContacts
      x-api-path-slug: restapiv1-0accountaccountidextensionextensionidfavorite-get
      parameters:
      - in: path
        name: accountId
        description: Internal identifier of a RingCentral account or tilde (~) to
          indicate the account logged-in within the current session
      - in: path
        name: extensionId
        description: Internal identifier of an extension or tilde (~) to indicate
          the extension assigned to the account logged-in within the current session
      responses:
        200:
          description: OK
      tags:
      - Favorite
      - Contacts
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