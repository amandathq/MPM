},
  "jobContact": {
    "entity": "JobOrder",
    "form": {
      "style": {
        "title": "Update Contact for all Jobs",
        "cancelButtonLabel": "Cancel?",
        "saveButtonLabel": "Next!"
      },
      "fields": [
        {
          "name": "clientContact",
          "type": "picker",
          "label": "Client Contact",
          "required": true,
          "sortOrder": 0,
          "pickerEntityIdProperty": "id",
          "pickerEntityLabelProperty": "name",
          "pickerEntityType": "ClientContact",
          "pickerEntityAdditionalLogic": "AND clientCorporation.id = ${clientCorporation.id}"
        }
      ]
    },
    "table": {
      "style": {
        "title": "Update Job Contacts",
        "singleActionButtonLabel": "Update",
        "massActionButtonLabel": "Update all selected",
        "formCancelButtonLabel": "Cancel",
        "formSaveButtonLabel": "Save"
      },
      "fields": [
        {
          "name": "id",
          "type": "text",
          "label": "ID",
          "displayOnly": true,
          "sortOrder": 0,
          "defaultValue": "${id}"
        },
        {
          "name": "title",
          "type": "text",
          "label": "Title",
          "displayOnly": true,
          "sortOrder": 1,
          "defaultValue": "${title}"
        },
        {
          "name": "employmentType",
          "type": "text",
          "label": "Employment Type",
          "sortOrder": 2,
          "displayOnly": true,
          "defaultValue": "${employmentType}"
        },
        {
          "name": "clientContact",
          "type": "picker",
          "label": "Client Contact",
          "required": true,
          "sortOrder": 3,
          "pickerEntityIdProperty": "id",
          "pickerEntityLabelProperty": "name",
          "pickerEntityType": "ClientContact",
          "pickerEntityAdditionalLogic": "AND clientCorporation.id = ${clientCorporation.id}"
        }
      ]
    }
  },
  "jobOwner": {
    "entity": "JobOrder",
    "form": {
      "style": {
        "title": "Update Owner  for all Jobs",
        "cancelButtonLabel": "Cancel",
        "saveButtonLabel": "Next"
      },
      "fields": [
        {
          "name": "owner",
          "type": "picker",
          "label": "Owner",
          "required": true,
          "sortOrder": 0,
          "pickerEntityIdProperty": "id",
          "pickerEntityLabelProperty": "name",
          "pickerEntityType": "CorporateUser"
        }
      ]
    },
    "table": {
      "style": {
        "title": "Update Job Owners",
        "singleActionButtonLabel": "Update",
        "massActionButtonLabel": "Update all selected",
        "formCancelButtonLabel": "Cancel",
        "formSaveButtonLabel": "Save"
      },
      "fields": [
        {
          "name": "id",
          "type": "text",
          "label": "ID",
          "displayOnly": true,
          "sortOrder": 0,
          "defaultValue": "${id}"
        },
        {
          "name": "title",
          "type": "text",
          "label": "Title",
          "displayOnly": true,
          "sortOrder": 1,
          "defaultValue": "${title}"
        },
        {
          "name": "employmentType",
          "type": "text",
          "label": "Employment Type",
          "sortOrder": 2,
          "displayOnly": true,
          "defaultValue": "${employmentType}"
        },
        {
          "name": "owner",
          "type": "picker",
          "label": "Owner",
          "required": true,
          "sortOrder": 3,
          "pickerEntityIdProperty": "id",
          "pickerEntityLabelProperty": "name",
          "pickerEntityType": "CorporateUser"
        }
      ]
    }
  }
}
