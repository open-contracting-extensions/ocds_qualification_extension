# Qualification

This extension should only be used as part of the [OCDS for PPPs profile](http://standard.open-contracting.org/profiles/ppp/). It adds a `preQualification` section between `planning` and `tender`; this second initiation stage is incompatible with the OCDS 1.x definition of a contracting process.

## Example

```json
{
  "preQualification": {
    "id": "1",
    "title": "Example PPP pre-qualification",
    "status": "active",
    "submissionMethod": [
      "electronicSubmission"
    ],
    "submissionMethodDetails": "Prospective bidders must submit their RFQ responses to the electronic portal at http://eprocurement.example.gov",
    "period": {
      "startDate": "2015-10-31T00:00:00Z",
      "endDate": "2015-11-30T00:00:00Z"
    },
    "enquiryPeriod": {
      "startDate": "2015-10-31T00:00:00Z",
      "endDate": "2015-11-06T23:59:59Z"
    },
    "eligibilityCriteria": "All interested parties are eligible to submit a RFQ response",
    "qualificationPeriod": {
      "startDate": "2015-12-01T00:00:00Z",
      "endDate": "2015-12-01T23:59:59Z"
    },
    "procuringEntity": {
      "id": "XX-GOV-12345678",
      "name": "Ministry of Communications"
    }
  }
}
```

## Issues

Report issues for this extension in the [ocds-extensions repository](https://github.com/open-contracting/ocds-extensions/issues), putting the extension's name in the issue's title.

## Changelog

This extension was originally discussed in <https://github.com/open-contracting-extensions/public-private-partnerships/issues/36>.

### 2019-03-20

* Set `"uniqueItems": true` on array fields, and add `"minLength": 1` on required string fields.

### 2019-01-24

* Remove multilingual support for non-existent `PreQualification.procurementMethodRationale` and `PreQualification.awardCriteriaDetails` fields.
