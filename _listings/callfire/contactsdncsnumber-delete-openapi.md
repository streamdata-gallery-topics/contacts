---
swagger: "2.0"
x-collection-name: CallFire
x-complete: 0
info:
  title: Callfire Delete do not contact (dnc) number. If number contains commas treat
    as list of numbers
  description: Delete a Do Not Contact (DNC) contact entry.
  termsOfService: https://www.callfire.com/legal/terms
  contact:
    name: CallFire
    url: https://www.callfire.com
    email: support@callfire.com
  version: 1.0.0
host: www.callfire.com
basePath: /v2
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /contacts:
    get:
      summary: Find contacts
      description: Find user's contacts by id, contact list, or on any property name.
        Returns a paged list of contacts
      operationId: findContacts
      x-api-path-slug: contacts-get
      parameters:
      - in: query
        name: contactListId
        description: Filters contacts by a particular contact list
      - in: query
        name: fields
        description: Limit fields received in response
      - in: query
        name: id
        description: A list of contact IDs
      - in: query
        name: limit
        description: To set the maximum number of records to return in a paged list
          response
      - in: query
        name: number
        description: Multiple contact numbers can be specified
      - in: query
        name: offset
        description: Offset to the start of a given page
      - in: query
        name: propertyName
        description: Name of a contact property to search by
      - in: query
        name: propertyValue
        description: Value of a contact property to search by
      responses:
        200:
          description: OK
      tags:
      - Contacts
    post:
      summary: Create contacts
      description: Creates contacts in CallFire system. These contacts are not validated
        on creation. They will be validated upon being added to a campaign
      operationId: createContacts
      x-api-path-slug: contacts-post
      parameters:
      - in: body
        name: body
        description: A list of a contact objects
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Contacts
  /contacts/dncs:
    get:
      summary: Find do not contact (dnc) items
      description: Searches for all Do Not Contact (DNC) objects created by user.
        These DoNotContact entries only affect calls/texts/campaigns on this account.
        Returns a paged list of DoNotContact objects
      operationId: findDoNotContacts
      x-api-path-slug: contactsdncs-get
      parameters:
      - in: query
        name: call
        description: Show only Do-Not-Call numbers
      - in: query
        name: campaignId
        description: A campaign id which was used to send a message to a DNC number
      - in: query
        name: fields
        description: Limit fields received in response
      - in: query
        name: limit
        description: To set the maximum number of records to return in a paged list
          response
      - in: query
        name: number
        description: "~"
      - in: query
        name: offset
        description: Offset to the start of a given page
      - in: query
        name: prefix
        description: Prefix (1-10 digits) of phone numbers
      - in: query
        name: source
        description: A DNC source name to search for DNCs
      - in: query
        name: text
        description: Show only Do-Not-Text numbers
      responses:
        200:
          description: OK
      tags:
      - Contacts
      - Dncs
    post:
      summary: Add or update do not contact (dnc) numbers
      description: Add or update a list of Do Not Contact (DNC) contact entries. Can
        toggle whether the DNCs are enabled for calls/texts.
      operationId: addDoNotContacts
      x-api-path-slug: contactsdncs-post
      parameters:
      - in: body
        name: body
        description: AddDoNotContactsRequest object
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Contacts
      - Dncs
  /contacts/dncs/sources/{source}:
    delete:
      summary: Delete do not contact (dnc) numbers contained in source.
      description: Delete Do Not Contact (DNC) contact entries contained in source.
      operationId: deleteDoNotContactsBySource
      x-api-path-slug: contactsdncssourcessource-delete
      parameters:
      - in: path
        name: source
        description: Source associated with Do Not Contact (DNC) entry
      responses:
        200:
          description: OK
      tags:
      - Contacts
      - Dncs
      - Sources
      - Source
  /contacts/dncs/universals/{toNumber}:
    get:
      summary: Find universal do not contacts (udnc) associated with toNumber
      description: Searches for a UniversalDoNotContact object for a given phone number.
        Shows whether inbound/outbound actions are allowed for a given number
      operationId: getUniversalDoNotContacts
      x-api-path-slug: contactsdncsuniversalstonumber-get
      parameters:
      - in: query
        name: fields
        description: Limit fields received in response
      - in: query
        name: fromNumber
        description: An optional destination/source number for DNC, specified in E
      - in: path
        name: toNumber
        description: A required destination phone number in E
      responses:
        200:
          description: OK
      tags:
      - Contacts
      - Dncs
      - Universals
      - ToNumber
  /contacts/dncs/{number}:
    delete:
      summary: Delete do not contact (dnc) number. If number contains commas treat
        as list of numbers
      description: Delete a Do Not Contact (DNC) contact entry.
      operationId: deleteDoNotContact
      x-api-path-slug: contactsdncsnumber-delete
      parameters:
      - in: path
        name: number
        description: Number associated with Do Not Contact (DNC) entry
      responses:
        200:
          description: OK
      tags:
      - Contacts
      - Dncs
      - Number
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