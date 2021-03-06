---
swagger: "2.0"
x-collection-name: VictorOps
x-complete: 0
info:
  title: Victor Ops Get a list of all contact methods for a user
  description: |-
    Get the contact methods for a user

    This API may be called a maximum of 15 times per minute.
  version: 0.0.2
host: api.victorops.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /api-public/v1/policies/types/contacts:
    get:
      summary: Get the available contact types
      description: |-
        Get the available contact types

        description: "Email Address", type: "email"
        description: "Phone Number", type: "phone"

        This API may be called a maximum of 15 times per minute.
      operationId: api_public.v1.policies.types.contacts.get
      x-api-path-slug: apipublicv1policiestypescontacts-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Policies
      - Types
      - Contacts
  /api-public/v1/user/{user}/contact-methods:
    get:
      summary: Get a list of all contact methods for a user
      description: |-
        Get the contact methods for a user

        This API may be called a maximum of 15 times per minute.
      operationId: api_public.v1.user.user.contact_methods.get
      x-api-path-slug: apipublicv1userusercontactmethods-get
      parameters:
      - in: query
        name: No Name
      - in: path
        name: user
        description: The VictorOps user ID
      responses:
        200:
          description: OK
      tags:
      - User
      - User
      - Contact-methods
  /api-public/v1/user/{user}/contact-methods/devices:
    get:
      summary: Get a list of all contact devices for a user
      description: |-
        Get the contact methods for a user

        This API may be called a maximum of 15 times per minute.
      operationId: api_public.v1.user.user.contact_methods.devices.get
      x-api-path-slug: apipublicv1userusercontactmethodsdevices-get
      parameters:
      - in: query
        name: No Name
      - in: path
        name: user
        description: The VictorOps user ID
      responses:
        200:
          description: OK
      tags:
      - User
      - User
      - Contact-methods
      - Devices
  /api-public/v1/user/{user}/contact-methods/devices/{contactId}:
    delete:
      summary: Delete a contact device for a user
      description: |-
        Delete a contact device for a user

        This API may be called a maximum of 15 times per minute.
      operationId: api_public.v1.user.user.contact_methods.devices.contactId.delete
      x-api-path-slug: apipublicv1userusercontactmethodsdevicescontactid-delete
      parameters:
      - in: path
        name: contactId
        description: The unique contact identifier
      - in: query
        name: No Name
      - in: path
        name: user
        description: The VictorOps user ID
      responses:
        200:
          description: OK
      tags:
      - User
      - User
      - Contact-methods
      - Devices
      - ContactId
    get:
      summary: Get the indicated contact device for a user
      description: |-
        Get the indicated contact device for a user

        This API may be called a maximum of 15 times per minute.
      operationId: api_public.v1.user.user.contact_methods.devices.contactId.get
      x-api-path-slug: apipublicv1userusercontactmethodsdevicescontactid-get
      parameters:
      - in: path
        name: contactId
        description: The unique contact identifier
      - in: query
        name: No Name
      - in: path
        name: user
        description: The VictorOps user ID
      responses:
        200:
          description: OK
      tags:
      - User
      - User
      - Contact-methods
      - Devices
      - ContactId
    put:
      summary: Update a contact device for a user
      description: |-
        Update a contact device for a user

        This API may be called a maximum of 15 times per minute.
      operationId: api_public.v1.user.user.contact_methods.devices.contactId.put
      x-api-path-slug: apipublicv1userusercontactmethodsdevicescontactid-put
      parameters:
      - in: path
        name: contactId
        description: The unique contact identifier
      - in: query
        name: No Name
      - in: path
        name: user
        description: The VictorOps user ID
      responses:
        200:
          description: OK
      tags:
      - User
      - User
      - Contact-methods
      - Devices
      - ContactId
  /api-public/v1/user/{user}/contact-methods/emails:
    get:
      summary: Get a list of all contact emails for a user
      description: |-
        Get the contact emails for a user

        This API may be called a maximum of 15 times per minute.
      operationId: api_public.v1.user.user.contact_methods.emails.get
      x-api-path-slug: apipublicv1userusercontactmethodsemails-get
      parameters:
      - in: query
        name: No Name
      - in: path
        name: user
        description: The VictorOps user ID
      responses:
        200:
          description: OK
      tags:
      - User
      - User
      - Contact-methods
      - Emails
    post:
      summary: Create a contact emails for a user
      description: |-
        Create a contact email for a user

        This API may be called a maximum of 15 times per minute.
      operationId: api_public.v1.user.user.contact_methods.emails.post
      x-api-path-slug: apipublicv1userusercontactmethodsemails-post
      parameters:
      - in: query
        name: No Name
      - in: path
        name: user
        description: The VictorOps user ID
      responses:
        200:
          description: OK
      tags:
      - User
      - User
      - Contact-methods
      - Emails
  /api-public/v1/user/{user}/contact-methods/emails/{contactId}:
    delete:
      summary: Delete a contact email for a user
      description: |-
        Delete the indicated contact email for the user

        This API may be called a maximum of 15 times per minute.
      operationId: api_public.v1.user.user.contact_methods.emails.contactId.delete
      x-api-path-slug: apipublicv1userusercontactmethodsemailscontactid-delete
      parameters:
      - in: path
        name: contactId
        description: The unique contact identifier
      - in: query
        name: No Name
      - in: path
        name: user
        description: The VictorOps user ID
      responses:
        200:
          description: OK
      tags:
      - User
      - User
      - Contact-methods
      - Emails
      - ContactId
    get:
      summary: Get the indicate contact email for a user
      description: |-
        Get the indicated contact email for a user

        This API may be called a maximum of 15 times per minute.
      operationId: api_public.v1.user.user.contact_methods.emails.contactId.get
      x-api-path-slug: apipublicv1userusercontactmethodsemailscontactid-get
      parameters:
      - in: path
        name: contactId
        description: The unique contact identifier
      - in: query
        name: No Name
      - in: path
        name: user
        description: The VictorOps user ID
      responses:
        200:
          description: OK
      tags:
      - User
      - User
      - Contact-methods
      - Emails
      - ContactId
  /api-public/v1/user/{user}/contact-methods/phones:
    get:
      summary: Get a list of all contact phones for a user
      description: |-
        Get the contact phones for a user

        This API may be called a maximum of 15 times per minute.
      operationId: api_public.v1.user.user.contact_methods.phones.get
      x-api-path-slug: apipublicv1userusercontactmethodsphones-get
      parameters:
      - in: query
        name: No Name
      - in: path
        name: user
        description: The VictorOps user ID
      responses:
        200:
          description: OK
      tags:
      - User
      - User
      - Contact-methods
      - Phones
    post:
      summary: Create a contact phones for a user
      description: |-
        Create a contact phone for a user

        This API may be called a maximum of 15 times per minute.
      operationId: api_public.v1.user.user.contact_methods.phones.post
      x-api-path-slug: apipublicv1userusercontactmethodsphones-post
      parameters:
      - in: query
        name: No Name
      - in: path
        name: user
        description: The VictorOps user ID
      responses:
        200:
          description: OK
      tags:
      - User
      - User
      - Contact-methods
      - Phones
  /api-public/v1/user/{user}/contact-methods/phones/{contactId}:
    delete:
      summary: Delete a contact phone for a user
      description: |-
        Delete the indicated contact phone for the user

        This API may be called a maximum of 15 times per minute.
      operationId: api_public.v1.user.user.contact_methods.phones.contactId.delete
      x-api-path-slug: apipublicv1userusercontactmethodsphonescontactid-delete
      parameters:
      - in: path
        name: contactId
        description: The unique contact identifier
      - in: query
        name: No Name
      - in: path
        name: user
        description: The VictorOps user ID
      responses:
        200:
          description: OK
      tags:
      - User
      - User
      - Contact-methods
      - Phones
      - ContactId
    get:
      summary: Get the indicate contact phone for a user
      description: |-
        Get the indicated contact phone for a user

        This API may be called a maximum of 15 times per minute.
      operationId: api_public.v1.user.user.contact_methods.phones.contactId.get
      x-api-path-slug: apipublicv1userusercontactmethodsphonescontactid-get
      parameters:
      - in: path
        name: contactId
        description: The unique contact identifier
      - in: query
        name: No Name
      - in: path
        name: user
        description: The VictorOps user ID
      responses:
        200:
          description: OK
      tags:
      - User
      - User
      - Contact-methods
      - Phones
      - ContactId
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