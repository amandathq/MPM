{
  "createPerm": {
    "entity": "JobSubmission",
    "filter": {
      "status": [
        "Placed"
      ],
      "jobOrder.employmentType": "Contract",
      "candidate.employeeType": [
        "1099"
      ]
    },
    "updates": {
      "candidate": {
        "status": "Placed"
      },
      "jobOrder": {
        "isOpen": false
      },
      "jobSubmission": {
        "status": "Placed"
      }
    },
    "table": {
      "style": {
        "title": "Create Perm Placements",
        "singleActionButtonLabel": "Create",
        "massActionButtonLabel": "Create all selected",
        "formCancelButtonLabel": "Cancel!!!",
        "formSaveButtonLabel": "Save the form",
        "filterRowsButtonLabelShow": "Show ineligible rows",
        "filterRowsButtonLabelHide": "Hide ineligible rows"
      },
      "fields": [
        {
          "name": "submissionStatus",
          "type": "text",
          "label": "Submission Статус",
          "sortOrder": 0,
          "defaultValue": "${status}",
          "displayOnly": true
        },
        {
          "name": "jobEmploymentType",
          "type": "text",
          "label": "Job Employment Type",
          "sortOrder": 0,
          "defaultValue": "${jobOrder.employmentType}",
          "displayOnly": true
        },
        {
          "name": "candidateName",
          "type": "text",
          "label": "Candidate",
          "defaultValue": "${candidate.name}",
          "displayOnly": true,
          "sortOrder": 0
        },
        {
          "name": "jobTitle",
          "type": "text",
          "label": "Job",
          "defaultValue": "${jobOrder.title}",
          "displayOnly": true,
          "sortOrder": 1
        },
        {
          "name": "salary",
          "type": "currency",
          "label": "Salary",
          "required": true,
          "sortOrder": 2,
          "defaultValue": "${jobOrder.salary}",
          "currencySymbol": "€"
        },
        {
          "name": "fee",
          "type": "percentage",
          "label": "Fee",
          "required": true,
          "sortOrder": 3,
          "defaultValue": "${jobOrder.feeArrangement}"
        },
        {
          "name": "otherHourlyFee",
          "type": "float",
          "label": "Other Fee (flat)",
          "required": false,
          "sortOrder": 4
        },
        {
          "name": "dateBegin",
          "type": "date",
          "label": "Start Date",
          "sortOrder": 5,
          "dateFormat": "DD/MM/YYYY",
          "defaultValue": "${jobOrder.startDate}"
        },
        {
          "name": "status",
          "type": "dropdown",
          "label": "Статус",
          "sortOrder": 6,
          "defaultValue": "Future",
          "readOnly": true,
          "valueList": [
            "Future",
            "Current",
            "Closed",
            "Unfilled"
          ],
          "displayValueList": [
            "Будущий",
            "Заполнен",
            "Закрыт",
            "Незаполнен"
          ]
        },
        {
          "name": "employmentType",
          "type": "dropdown",
          "label": "Employment Type",
          "sortOrder": 7,
          "valueList": [
            "Contract",
            "Permanent",
            "Contact to Hire",
            "Direct Hire"
          ],
          "readOnly": true,
          "defaultValue": "Permanent"
        },
        {
          "name": "employeeType",
          "type": "dropdown",
          "label": "Employee Type",
          "sortOrder": 8,
          "valueList": [
            "W2",
            "Corp-to-Corp",
            "1099"
          ],
          "defaultValue": "${candidate.employeeType}"
        }
      ]
    }
  },
  "extend": {
    "entity": "Placement",
    "config": {
      "placementChangeRequestType": "Mass Extend"
    },
    "form": {
      "style": {
        "title": "Extend placements",
        "cancelButtonLabel": "Cancel",
        "saveButtonLabel": "Next"
      },
      "fields": [
        {
          "name": "dateEnd",
          "type": "date",
          "label": "End Date",
          "required": true,
          "dateFormat": "DD-MM-YYYY",
          "sortOrder": 0
        }
      ]
    },
    "table": {
      "style": {
        "title": "Update Placement Rates",
        "singleActionButtonLabel": "Update",
        "massActionButtonLabel": "Update all selected",
        "formCancelButtonLabel": "Cancel!!!",
        "formSaveButtonLabel": "Save the form"
      },
      "fields": [
        {
          "name": "dateBegin",
          "type": "date",
          "label": "Start Date",
          "sortOrder": 6,
          "dateFormat": "DD/MM/YYYY",
          "defaultValue": "${dateBegin}",
          "readOnly": true
        },
        {
          "name": "dateEnd",
          "type": "date",
          "label": "End Date",
          "sortOrder": 0,
          "dateFormat": "DD/MM/YYYY"
        },
        {
          "name": "status",
          "type": "dropdown",
          "label": "??????",
          "sortOrder": 4,
          "readOnly": true,
          "defaultValue": "${status}",
          "valueList": [
            "Submitted"
          ]
        },
        {
          "name": "employmentType",
          "type": "dropdown",
          "label": "Employment Type",
          "sortOrder": 5,
          "defaultValue": "${employmentType}",
          "valueList": [
            "Contract",
            "Permanent",
            "Contact to Hire",
            "Direct Hire"
          ],
          "readOnly": true
        }
      ]
    }
  },
  "extendChangeRequest": {
    "entity": "Placement",
    "config": {
      "placementChangeRequestType": "Mass Extend",
      "onlyCreateChangeRequest": true,
      "placementChangeRequestStatus": "Submitted"
    },
    "form": {
      "style": {
        "title": "Extend placements",
        "cancelButtonLabel": "Cancel",
        "saveButtonLabel": "Next"
      },
      "fields": [
        {
          "name": "dateEnd",
          "type": "date",
          "label": "End Date",
          "required": true,
          "dateFormat": "DD-MM-YYYY",
          "sortOrder": 0
        }
      ]
    },
    "table": {
      "style": {
        "title": "Update Placement Rates",
        "singleActionButtonLabel": "Update",
        "massActionButtonLabel": "Update all selected",
        "formCancelButtonLabel": "Cancel!!!",
        "formSaveButtonLabel": "Save the form"
      },
      "fields": [
        {
          "name": "dateBegin",
          "type": "date",
          "label": "Start Date",
          "sortOrder": 6,
          "dateFormat": "DD/MM/YYYY",
          "defaultValue": "${dateBegin}",
          "readOnly": true
        },
        {
          "name": "dateEnd",
          "type": "date",
          "label": "End Date",
          "sortOrder": 0,
          "dateFormat": "DD/MM/YYYY"
        },
        {
          "name": "status",
          "type": "dropdown",
          "label": "Status",
          "sortOrder": 4,
          "readOnly": true,
          "defaultValue": "${status}",
          "valueList": [
            "Submitted"
          ]
        },
        {
          "name": "employmentType",
          "type": "dropdown",
          "label": "Employment Type",
          "sortOrder": 5,
          "defaultValue": "${employmentType}",
          "valueList": [
            "Contract",
            "Permanent",
            "Contact to Hire",
            "Direct Hire"
          ],
          "readOnly": true
        }
      ]
    }
  },
  "rates": {
    "entity": "Placement",
    "config": {
      "placementChangeRequestType": "Mass Rate Change"
    },
    "form": {
      "style": {
        "title": "Update rates",
        "cancelButtonLabel": "Cancel?",
        "saveButtonLabel": "Next, yo."
      },
      "fields": [
        {
          "name": "payRate",
          "type": "float",
          "label": "Pay Rate",
          "required": true,
          "sortOrder": 0,
          "defaultValue": "${payRate}"
        },
        {
          "name": "clientBillRate",
          "type": "float",
          "label": "Bill Rate",
          "required": true,
          "sortOrder": 1,
          "defaultValue": "${clientBillRate}"
        },
        {
          "name": "overtimeRate",
          "type": "float",
          "label": "Overtime Rate",
          "required": true,
          "sortOrder": 2,
          "defaultValue": "${overtimeRate}"
        },
        {
          "name": "clientOvertimeRate",
          "type": "float",
          "label": "Overtime Bill Rate",
          "required": true,
          "sortOrder": 3,
          "defaultValue": "${clientOvertimeRate}"
        }
      ]
    },
    "table": {
      "style": {
        "title": "Update Placement Rates",
        "singleActionButtonLabel": "Update",
        "massActionButtonLabel": "Update all selected",
        "formCancelButtonLabel": "Cancel!!!",
        "formSaveButtonLabel": "Save the form"
      },
      "fields": [
        {
          "name": "payRate",
          "type": "float",
          "label": "Pay Rate",
          "required": true,
          "sortOrder": 0
        },
        {
          "name": "clientBillRate",
          "type": "float",
          "label": "Bill Rate",
          "required": true,
          "sortOrder": 1
        },
        {
          "name": "overtimeRate",
          "type": "float",
          "label": "Overtime Rate",
          "required": true,
          "sortOrder": 2
        },
        {
          "name": "clientOvertimeRate",
          "type": "float",
          "label": "Overtime Bill Rate",
          "required": true,
          "sortOrder": 3
        },
        {
          "name": "status",
          "type": "dropdown",
          "label": "Status",
          "sortOrder": 4,
          "readOnly": true,
          "defaultValue": "${status}",
          "valueList": [
            "Submitted"
          ]
        },
        {
          "name": "employmentType",
          "type": "dropdown",
          "label": "Employment Type",
          "sortOrder": 5,
          "defaultValue": "${employmentType}",
          "valueList": [
            "Contract",
            "Permanent",
            "Contact to Hire",
            "Direct Hire"
          ],
          "readOnly": true
        },
        {
          "name": "dateBegin",
          "type": "date",
          "label": "Start Date",
          "sortOrder": 6,
          "dateFormat": "DD/MM/YYYY",
          "defaultValue": "${dateBegin}",
          "readOnly": true
        },
        {
          "name": "dateEnd",
          "type": "date",
          "label": "End Date",
          "sortOrder": 7,
          "dateFormat": "DD/MM/YYYY",
          "defaultValue": "${dateEnd}",
          "readOnly": true
        }
      ]
    }
  },
  "create": {
    "entity": "JobSubmission",
    "form": {
      "style": {
        "title": "Set defaults for all Placements to be created",
        "cancelButtonLabel": "Cancel?",
        "saveButtonLabel": "Next!"
      },
      "fields": [
        {
          "name": "payRate",
          "type": "float",
          "label": "Pay Rate",
          "required": true,
          "sortOrder": 0,
          "defaultValue": "${jobOrder.payRate}"
        },
        {
          "name": "clientBillRate",
          "type": "float",
          "label": "Bill Rate",
          "required": true,
          "sortOrder": 1,
          "defaultValue": "${jobOrder.clientBillRate}"
        },
        {
          "name": "status",
          "type": "text",
          "label": "Status",
          "sortOrder": 2,
          "defaultValue": "Submitted",
          "readOnly": true
        },
        {
          "name": "employmentType",
          "type": "dropdown",
          "label": "Employment Type",
          "sortOrder": 3,
          "defaultValue": "${jobOrder.employmentType}",
          "valueList": [
            "Contract",
            "Permanent",
            "Contact to Hire",
            "Direct Hire"
          ],
          "readOnly": true
        },
        {
          "name": "employeeType",
          "type": "dropdown",
          "label": "Employee Type",
          "sortOrder": 4,
          "defaultValue": "${candidate.employeeType}",
          "valueList": [
            "W2",
            "Corp-to-Corp",
            "1099"
          ]
        },
        {
          "name": "dateBegin",
          "type": "date",
          "label": "Start Date",
          "sortOrder": 5,
          "defaultValue": "${jobOrder.startDate}",
          "dateFormat": "DD/MM/YYYY"
        },
        {
          "name": "customText1",
          "type": "email",
          "label": "Candidate Email",
          "sortOrder": 6,
          "defaultValue": "${candidate.email}"
        },
        {
          "name": "customTextBlock1",
          "type": "textarea",
          "label": "Comments",
          "sortOrder": 7
        },
        {
          "name": "customInt1",
          "type": "radio",
          "label": "Is Exempt?",
          "sortOrder": 8,
          "valueList": [
            "0",
            "1"
          ],
          "displayValueList": [
            "No",
            "Yes"
          ],
          "defaultValue": "0"
        },
        {
          "name": "customInt2",
          "type": "integer",
          "label": "Federal Exemptions",
          "sortOrder": 10
        },
        {
          "name": "billingClientContact",
          "type": "picker",
          "label": "Billing Contact",
          "sortOrder": 12,
          "pickerEntityIdProperty": "id",
          "pickerEntityLabelProperty": "name",
          "pickerEntityType": "ClientContact",
          "pickerEntityAdditionalLogic": "AND clientCorporation.id = ${jobOrder.clientCorporation.id}",
          "defaultValue": "${jobOrder.clientContact}"
        },
        {
          "name": "location",
          "label": "Work Location",
          "sortOrder": 13,
          "type": "picker",
          "pickerEntityIdProperty": "id",
          "pickerEntityLabelProperty": "title",
          "pickerEntityType": "Location",
          "pickerEntityAdditionalLogic": "AND clientCorporation.id = ${jobOrder.clientCorporation.id}"
        }
      ]
    },
    "table": {
      "style": {
        "title": "Create Placements",
        "singleActionButtonLabel": "Create",
        "massActionButtonLabel": "Create all selected",
        "formCancelButtonLabel": "Cancel yo",
        "formSaveButtonLabel": "Save the form"
      },
      "fields": [
        {
          "name": "payRate",
          "type": "float",
          "label": "Pay Rate",
          "required": true,
          "sortOrder": 0
        },
        {
          "name": "clientBillRate",
          "type": "float",
          "label": "Bill Rate",
          "required": true,
          "sortOrder": 1
        },
        {
          "name": "status",
          "type": "dropdown",
          "label": "Status",
          "sortOrder": 2,
          "defaultValue": "Submitted",
          "readOnly": true,
          "valueList": [
            "Submitted"
          ]
        },
        {
          "name": "employmentType",
          "type": "dropdown",
          "label": "Employment Type",
          "sortOrder": 3,
          "valueList": [
            "Contract",
            "Permanent",
            "Contact to Hire",
            "Direct Hire"
          ],
          "readOnly": true
        },
        {
          "name": "employeeType",
          "type": "dropdown",
          "label": "Employee Type",
          "sortOrder": 4,
          "valueList": [
            "W2",
            "Corp-to-Corp",
            "1099"
          ]
        },
        {
          "name": "dateBegin",
          "type": "date",
          "label": "Start Date",
          "sortOrder": 5,
          "dateFormat": "DD/MM/YYYY"
        },
        {
          "name": "customText1",
          "type": "email",
          "label": "Candidate Email",
          "sortOrder": 6,
          "defaultValue": "${candidate.email}"
        },
        {
          "name": "customText2",
          "type": "email",
          "label": "Contact Email",
          "sortOrder": 7,
          "defaultValue": "${jobOrder.clientContact.email}"
        },
        {
          "name": "customTextBlock1",
          "type": "textarea",
          "label": "Comments",
          "sortOrder": 8,
          "defaultValue": "Created via Mass Placement"
        },
        {
          "name": "customInt1",
          "type": "radio",
          "label": "Is Exempt?",
          "sortOrder": 9,
          "valueList": [
            "0",
            "1"
          ],
          "displayValueList": [
            "No",
            "Yes"
          ],
          "defaultValue": "0"
        },
        {
          "name": "customInt2",
          "type": "integer",
          "label": "Federal Exemptions",
          "sortOrder": 11
        },
        {
          "name": "billingClientContact",
          "type": "picker",
          "label": "Billing Contact",
          "sortOrder": 12,
          "pickerEntityIdProperty": "id",
          "pickerEntityLabelProperty": "name",
          "pickerEntityType": "ClientContact",
          "pickerEntityAdditionalLogic": "AND clientCorporation.id = ${jobOrder.clientCorporation.id}"
        },
        {
          "name": "customText4",
          "type": "picker",
          "label": "Timesheet Approving Contact",
          "sortOrder": 13,
          "pickerEntityIdProperty": "id",
          "pickerEntityLabelProperty": "name",
          "pickerEntityType": "ClientContact",
          "pickerEntityAdditionalLogic": "AND clientCorporation.id = ${jobOrder.clientCorporation.id}",
          "defaultValue": "${jobOrder.customText4}"
        }
      ]
    }
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
