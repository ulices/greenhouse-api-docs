## Candidate stage change

```json
{
  "action": "candidate_stage_change",
  "payload": {
    "application": {
      "id": 265277,
      "rejected_at": null,
      "prospect": false,
      "status": "active",
      "applied_at": "2013-03-22T00:00:00Z",
      "last_activity_at": "2015-02-09T16:38:36Z",
      "source": {
        "id": 31,
        "name": "Agency"
      },
      "credited_to": {
        "id": 15,
        "email": "ada@example.com",
        "name": "Ada Lacey"
      },
      "rejection_reason": null,
      "current_stage": {
        "id": 71416,
        "name": "Assessment",
        "interviews": [
          {
            "id": 113101,
            "name": "Assessment",
            "status": "to_be_scheduled",
            "interview_kit": {
              "url": "https://app.greenhouse.io/guides/113153/people/265772",
              "content": "Assess their skills",
              "questions": []
            },
            "interviewers": [
              {
                "id": 2622,
                "display_name": "Carl Buddha",
                "status": "tentative"
              }
            ]
          }
        ]
      },
      "candidate": {
        "id": 265772,
        "created_at": "2013-10-04T01:24:44Z",
        "first_name": "Giuseppe",
        "last_name": "Hurley",
        "external_id": "241b399ce4b0fd1c84e5528d",
        "title": "Great Person",
        "company": null,
        "photo_url": "https://prod-heroku.s3.amazonaws.com/...",
        "phone_numbers": [
          {
            "value": "330-281-8004",
            "type": "home"
          }
        ],
        "email_addresses": [
          {
            "value": "giuseppe.hurley@example.com",
            "type": "personal"
          }
        ],
        "addresses": [
          {
            "value": "123 Fake St.",
            "type": "home"
          }
        ],
        "website_addresses": [
          {
            "value": "ghurley.example.com",
            "type": "personal"
          }
        ],
        "social_media_addresses": [
          {
            "value": "linkedin.example.com/ghurley"
          }
        ],
        "recruiter": {
          "id": 3128,
          "email": "alicia.flopple.3128@example.com",
          "name": "Alicia Flopple"
        },
        "coordinator": {
          "id": 3128,
          "email": "alicia.flopple.3128@example.com",
          "name": "Alicia Flopple"
        },
        "attachments": [
          {
            "filename": "resume.pdf",
            "url": "https://prod-heroku.s3.amazonaws.com/...",
            "type": "resume"
          },
          {
            "filename": "cover_letter.pdf",
            "url": "https://prod-heroku.s3.amazonaws.com/...",
            "type": "cover_letter"
          },
          {
            "filename": "portfolio.pdf",
            "url": "https://prod-heroku.s3.amazonaws.com/...",
            "type": "attachment"
          }
        ],
        "tags": [
          "Import from Previous ATS"
        ],
        "custom_fields": {
          "favorite_color": {
            "name": "Favorite Color",
            "type": "short_text",
            "value": "Blue"
          }
        }
      },
      "jobs": [
        {
          "id": 3485,
          "name": "Designer",
          "requisition_id": null,
          "notes": "Digital and print",
          "status": "open",
          "created_at": "2013-10-02T22:59:29Z",
          "opened_at": "2015-01-23T00:25:04Z",
          "closed_at": null,
          "departments": [
            {
              "id": 237,
              "name": "Community"
            }
          ],
          "offices": [
            {
              "id": 54,
              "name": "New York",
              "location": "New York, NY"
            }
          ],
          "custom_fields": {
            "employment_type": {
              "name": "Employment Type",
              "type": "single_select",
              "value": "Full Time"
            }
          }
        }
      ]
    }
  }
}
```

### Noteworthy response attributes

See web hook [common attributes](#common-attributes).

| Attribute | Note |
|-----------|------|
| `application.current_stage.interviews[].interviewers.status` | One of: `needs_action`, `declined`, `tentative`, `accepted`
| `application.current_stage.interviews[].status` | One of: `to_be_scheduled`, `scheduled`, `awaiting_feedback`, `complete`, `skipped`, `collect_feedback`, `to_be_sent`, `sent`, `received`