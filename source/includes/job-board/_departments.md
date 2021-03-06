# Departments

## List departments

```json
{
  "departments":[
    {
      "id":33333,
      "name":"Engineering",
      "jobs":[
        {
          "id":44444,
          "title":"Product Engineer",
          "location":{
            "name":"San Francisco, CA"
          },
          "updated_at":"2013-07-02T19:39:23Z",
          "absolute_url":"http://your.co/careers?gh_jid=444444"
        },
        {
          "id":55555,
          "title":"Mobile Engineer - iOS",
          "location":{
            "name":"San Francisco, CA"
          },
          "updated_at":"2013-07-02T19:39:23Z",
          "absolute_url":"http://your.co/careers?gh_jid=55555"
        }
    },
    {
      "id":22222,
      "name":"Account Management",
      "jobs":[

      ]
    },
    // { ... } All departments are listed
  ]
}
```

Returns a list of your organization's departments and jobs.


### HTTP Request

`GET https://api.greenhouse.io/v1/boards/{board_token}/departments`

### URL Parameters

Parameter | Description
--------- | -----------
board_token | Job Board URL token

## Retrieve a department

```json
{
  "id":33333,
  "name":"Engineering",
  "jobs":[
    {
      "id":44444,
      "title":"Product Engineer",
      "location":{
        "name":"San Francisco, CA"
      },
      "updated_at":"2013-07-02T19:39:23Z",
      "absolute_url":"http://your.co/careers?gh_jid=444444"
    },
    {
      "id":55555,
      "title":"Mobile Engineer - iOS",
      "location":{
        "name":"San Francisco, CA"
      },
      "updated_at":"2013-07-02T19:39:23Z",
      "absolute_url":"http://your.co/careers?gh_jid=55555"
    }
  ]
}
```

Returns a list of jobs for a given `department_id`.

### HTTP Request

`GET https://api.greenhouse.io/v1/boards/{board_token}/departments/{department_id}`

### URL Parameters

Parameter | Description
--------- | -----------
board_token | Job Board URL token
department_id | ID of the department to retrieve
