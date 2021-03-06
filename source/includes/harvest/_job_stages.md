# Job Stages

Stages for the job specified by the supplied id.

## The job stage object

```
{
	"id": 72200,
	"name": "Face to Face",
	"interviews": [
	  {
	    "id": 6001,
	    "name": "Cultural Fit Interview",
	    "interview_kit": {
	      "content": "<h5>Purpose</h5><span>Determine whether or not the candidate would be a strong fit.</span>",
	      "questions": [
	        {
	          "id": 11052,
	          "question": "Is this person really a good fit?"
	        }
	      ]
	    }
	  },
	  {
	    "id": 6002,
	    "name": "Executive Interview",
	    "interview_kit": {
	      "content": "<h5>Purpose</h5><span>See if they can work with the boss.</span>",
	      "questions": [
	        {
	          "id": 11053,
	          "question": "What's their favorite color?"
	        },
	        {
	          "id": 11054,
	          "question": "Do they really want to work here?"
	        }
	      ]
	    }
	  }
	]
}
```

### Noteworthy attributes

| Attribute | Description |
|-----------|-------------|
| id | The job stage's unique identifier |
| interviews | An array of interviews associated with this job stage.

## List job stages for job

```shell
curl 'https://harvest.greenhouse.io/v1/jobs/{id}/stages' 
-H "Authorization: Basic MGQwMzFkODIyN2VhZmE2MWRjMzc1YTZjMmUwNjdlMjQ6"
```

> The above command returns JSON structured like this:

```json
[
  {
    "id": 72200,
    "name": "Face to Face",
    "interviews": [
      {
        "id": 6001,
        "name": "Cultural Fit Interview",
        "interview_kit": {
          "content": "<h5>Purpose</h5><span>Determine whether or not the candidate would be a strong fit.</span>",
          "questions": [
            {
              "id": 11052,
              "question": "Is this person really a good fit?"
            }
          ]
        }
      },
      {
        "id": 6002,
        "name": "Executive Interview",
        "interview_kit": {
          "content": "<h5>Purpose</h5><span>See if they can work with the boss.</span>",
          "questions": [
            {
              "id": 11053,
              "question": "What's their favorite color?"
            },
            {
              "id": 11054,
              "question": "Do they really want to work here?"
            }
          ]
        }
      }
    ]
  },
  {
    "id": 72199,
    "name": "Offer",
    "interviews": []
  },
  {
    "id": 72194,
    "name": "Application Review",
    "interviews": [
      {
        "id": 8004,
        "name": "Application Review",
        "interview_kit": {
          "content": null,
          "questions": []
        }
      }
    ]
  }
]
```

Retrieves the stages for the specified job id.

### HTTP Request

`GET https://harvest.greenhouse.io/v1/jobs/{id}/stages`

### URL Parameters

Parameter | Description
--------- | -----------
| id | The ID of the job whose job stages you want to retrieve.

### Querystring parameters

Parameter | Description
--------- | -----------
| created_before | Return only job stages that were created before this timestamp. Timestamp must be in in [ISO-8601] (#general-considerations) format.
| created_after | Return only job stages that were created after this timestamp. Timestamp must be in in [ISO-8601] (#general-considerations) format.
| updated_before | Return only job stages that were updated before this timestamp. Timestamp must be in in [ISO-8601] (#general-considerations) format.
| updated_after | Return only job stages that were updated after this timestamp. Timestamp must be in in [ISO-8601] (#general-considerations) format.

<br>
[See noteworthy response attributes.](#the-job-stage-object)