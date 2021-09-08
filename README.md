{
  "extend": {
    "entity": "Placement",
    "config": {
      "placementChangeRequestType": "Mass End Placements"
    },
    "form": {
      "style": {
        "title": "Mass End Placements",
        "cancelButtonLabel": "Cancel",
        "saveButtonLabel": "Next"
      },
      "fields": [
        {
          "name": "status",
          "type": "dropdown",
          "label": "Status",
          "required": true,
          "sortOrder": 5,
          "valueList": [
            "Rejected",
            "Re-Submitted",
            "Closed"
          ],
          "defaultValue": "Closed"
        },
        {
          "name": "dateEnd",
          "type": "date",
          "label": "End Date",
          "required": true,
          "sortOrder": 10,
          "dateFormat": "DD-MM-YYYY",
          "defaultValue": "${dateEnd}"
        },
        {
          "name": "terminationReason",
          "type": "dropdown",
          "label": "Termination Reason",
          "sortOrder": 15,
          "valueList": [
            "Assignment Complete",
            "Converted",
            "Job Abandonment",
            "Resigned - Gave Notice",
            "Resigned - No Notice",
            "Term - Attendance",
            "Term - Cultural",
            "Term - Skills",
            "Never Started",
            "Failed Compliance"
          ]
        }
      ]
    },
    "table": {
      "style": {
        "title": "End Placements",
        "singleActionButtonLabel": "End",
        "massActionButtonLabel": "End all selected",
        "formCancelButtonLabel": "Cancel",
        "formSaveButtonLabel": "Save"
      },
      "fields": [
        {
          "name": "candidateName",
          "type": "text",
          "label": "Candidate",
          "required": true,
          "defaultValue": "${candidate.name}",
          "readOnly": true,
          "sortOrder": 3
        },
        {
          "name": "status",
          "type": "dropdown",
          "label": "Status",
          "required": true,
          "sortOrder": 5,
          "valueList": [
            "Rejected",
            "Re-Submitted",
            "Closed"
          ]
        },
        {
          "name": "employmentType",
          "type": "dropdown",
          "label": "Employment Type",
          "required": true,
          "readOnly": true,
          "sortOrder": 15,
          "defaultValue": "${employmentType}"
        },
        {
          "name": "dateBegin",
          "type": "date",
          "label": "Start Date",
          "required": true,
          "sortOrder": 40,
          "dateFormat": "DD/MM/YYYY",
          "defaultValue": "${dateBegin}"
        },
        {
          "name": "dateEnd",
          "type": "date",
          "label": "End Date",
          "required": true,
          "sortOrder": 45,
          "dateFormat": "DD-MM-YYYY",
          "defaultValue": "${dateEnd}"
        },
        {
          "name": "terminationReason",
          "type": "dropdown",
          "label": "Termination Reason",
          "sortOrder": 60,
          "valueList": [
            "Assignment Complete",
            "Converted",
            "Job Abandonment",
            "Resigned - Gave Notice",
            "Resigned - No Notice",
            "Term - Attendance",
            "Term - Cultural",
            "Term - Skills",
            "Never Started",
            "Failed Compliance"
          ]
        }
      ]
    }
  },
  "rates": {
    "entity": "Placement",
    "config": {
      "placementChangeRequestType": "Update Rates"
    },
    "form": {
      "style": {
        "title": "Update Rates",
        "cancelButtonLabel": "Cancel",
        "saveButtonLabel": "Next"
      },
      "fields": [
        {
          "name": "status",
          "type": "dropdown",
          "label": "Status",
          "required": true,
          "sortOrder": 5,
          "valueList": [
            "Submitted",
            "Reviewed",
            "Approved"
          ],
          "defaultValue": "Submitted"
        },
        {
          "name": "dateEnd",
          "type": "date",
          "label": "End Date",
          "required": true,
          "sortOrder": 45,
          "dateFormat": "DD/MM/YYYY",
          "defaultValue": "${dateEnd}"
        },
        {
          "name": "payRate",
          "type": "currency",
          "label": "Pay Rate",
          "required": true,
          "sortOrder": 50,
          "defaultValue": "${payRate}"
        },
        {
          "name": "dateEffective",
          "type": "date",
          "label": "Effective Date",
          "sortOrder": 70,
          "dateFormat": "DD/MM/YYYY"
        },
        {
          "name": "overtimeRate",
          "type": "float",
          "label": "Overtime Pay Rate",
          "required": true,
          "sortOrder": 80,
          "defaultValue": "${overtimeRate}"
        },
        {
          "name": "clientBillRate",
          "type": "currency",
          "label": "Bill Rate",
          "required": true,
          "sortOrder": 90,
          "defaultValue": "${clientBillRate}"
        },
        {
          "name": "dateClientEffective",
          "type": "date",
          "label": "Effective Date (Client)",
          "sortOrder": 100,
          "dateFormat": "DD/MM/YYYY"
        },
        {
          "name": "clientOvertimeRate",
          "type": "float",
          "label": "Overtime Bill Rate",
          "required": true,
          "sortOrder": 245,
          "defaultValue": "${clientOvertimeRate}"
        }
      ]
    },
    "table": {
      "style": {
        "title": "Update Placement Rates",
        "singleActionButtonLabel": "Update",
        "massActionButtonLabel": "Update all selected",
        "formCancelButtonLabel": "Cancel",
        "formSaveButtonLabel": "Save"
      },
      "fields": [
        {
          "name": "candidateName",
          "type": "text",
          "label": "Candidate",
          "required": true,
          "defaultValue": "${candidate.name}",
          "readOnly": true,
          "sortOrder": 3
        },
        {
          "name": "status",
          "type": "dropdown",
          "label": "Status",
          "required": true,
          "sortOrder": 5,
          "valueList": [
            "Submitted",
            "Reviewed",
            "Approved"
          ],
          "defaultValue": "Submitted"
        },
        {
          "name": "employmentType",
          "type": "dropdown",
          "label": "Employment Type",
          "required": true,
          "readOnly": true,
          "sortOrder": 30,
          "defaultValue": "${employmentType}"
        },
        {
          "name": "dateBegin",
          "type": "date",
          "label": "Start Date",
          "required": true,
          "sortOrder": 40,
          "dateFormat": "DD/MM/YYYY",
          "defaultValue": "${dateBegin}"
        },
        {
          "name": "dateEnd",
          "type": "date",
          "label": "End Date",
          "required": true,
          "sortOrder": 45,
          "dateFormat": "DD/MM/YYYY",
          "defaultValue": "${dateEnd}"
        },
        {
          "name": "payRate",
          "type": "currency",
          "label": "Pay Rate",
          "required": true,
          "sortOrder": 50,
          "defaultValue": "${payRate}"
        },
        {
          "name": "dateEffective",
          "type": "date",
          "label": "Effective Date",
          "sortOrder": 70,
          "dateFormat": "DD/MM/YYYY"
        },
        {
          "name": "overtimeRate",
          "type": "float",
          "label": "Overtime Pay Rate",
          "required": true,
          "sortOrder": 80,
          "defaultValue": "${overtimeRate}"
        },
        {
          "name": "clientBillRate",
          "type": "currency",
          "label": "Bill Rate",
          "required": true,
          "sortOrder": 90,
          "defaultValue": "${clientBillRate}"
        },
        {
          "name": "dateClientEffective",
          "type": "date",
          "label": "Effective Date (Client)",
          "sortOrder": 100,
          "dateFormat": "DD/MM/YYYY"
        },
        {
          "name": "clientOvertimeRate",
          "type": "float",
          "label": "Overtime Bill Rate",
          "required": true,
          "sortOrder": 245,
          "defaultValue": "${clientOvertimeRate}"
        }
      ]
    }
  },
  "create": {
    "entity": "JobSubmission",
    "form": {
      "style": {
        "title": "Set defaults for all Placements to be created",
        "cancelButtonLabel": "Cancel",
        "saveButtonLabel": "Next"
      },
      "fields": [
        {
          "name": "status",
          "type": "dropdown",
          "label": "Status",
          "required": true,
          "sortOrder": 5,
          "valueList": [
            "Submitted",
            "Reviewed",
            "Re-Submitted"
          ],
          "defaultValue": "Submitted"
        },
        {
          "name": "terminationReason",
          "type": "dropdown",
          "label": "Ending Reason",
          "required": false,
          "sortOrder": 8,
          "valueList": [
            "Assignment Complete",
            "Converted",
            "Job Abandonment",
            "Resigned - Gave Notice",
            "Resigned No Notice",
            "Term - Attendance",
            "Term - Cultural",
            "Term - Skills",
            "Never Started",
            "Failed Compliance"
          ]
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
          "name": "reportTo",
          "type": "text",
          "label": "Reporting to",
          "required": false,
          "sortOrder": 20
        },
        {
          "name": "correlatedCustomText1",
          "type": "dropdown",
          "label": "Branch",
          "required": true,
          "sortOrder": 23,
          "valueList": [
            "PP - Accounting & Finance",
            "PP - Administrative",
            "PP - Creative & Marketing",
            "PP - Engineering",
            "PP - HR",
            "PP - IT",
            "PP - Legal",
            "PP - Sales",
            "PP - Executive",
            "PTS - Acct & Fin Temps",
            "PTS - Temp Placement",
            "PTS - Volume Staffing"
          ],
          "defaultValue": "PTS - Volume Staffing"
        },
        {
          "name": "employmentType",
          "type": "dropdown",
          "label": "Employment Type",
          "required": true,
          "sortOrder": 30,
          "valueList": [
            "Temporary",
            "Temp to Hire"
          ],
          "defaultValue": "${jobOrder.employmentType}"
        },
        {
          "name": "dateBegin",
          "type": "date",
          "label": "Start Date",
          "required": true,
          "sortOrder": 40,
          "dateFormat": "DD/MM/YYYY",
          "defaultValue": "${jobOrder.startDate}"
        },
        {
          "name": "dateEnd",
          "type": "date",
          "label": "End Date",
          "required": true,
          "sortOrder": 45,
          "dateFormat": "DD/MM/YYYY",
          "defaultValue": "${jobOrder.dateEnd}"
        },
        {
          "name": "correlatedCustomText6",
          "type": "text",
          "label": "PO Number",
          "required": false,
          "sortOrder": 53,
          "defaultValue": "${jobOrder.correlatedCustomText6}"
        },
        {
          "name": "costCenter",
          "type": "text",
          "label": "Cost Center",
          "required": false,
          "sortOrder": 55,
          "defaultValue": "${jobOrder.costCenter}"
        },
        {
          "name": "flatFee",
          "type": "currency",
          "label": "Placement Fee Payable",
          "required": false,
          "sortOrder": 70
        },
        {
          "name": "customTextBlock1",
          "type": "textarea",
          "label": "Comments",
          "required": false,
          "sortOrder": 110
        },
        {
          "name": "payRate",
          "type": "currency",
          "label": "Pay Rate",
          "required": true,
          "sortOrder": 140,
          "defaultValue": "${jobOrder.payRate}"
        },
        {
          "name": "clientBillRate",
          "type": "currency",
          "label": "Bill Rate",
          "required": true,
          "sortOrder": 225,
          "defaultValue": "${jobOrder.clientBillRate}"
        },
        {
          "name": "correlatedCustomText4",
          "type": "dropdown",
          "label": "Invoice Format",
          "required": true,
          "sortOrder": 585,
          "valueList": [
            "TEMP",
            "TEMPCUS",
            "TEMPJOB",
            "TEMPPO",
            "PERM"
          ],
          "defaultValue": "TEMP"
        },
        {
          "name": "correlatedCustomText5",
          "type": "dropdown",
          "label": "Office",
          "required": true,
          "sortOrder": 590,
          "valueList": [
            "SLC"
          ],
          "defaultValue": "SLC"
        },
        {
          "name": "correlatedCustomText7",
          "type": "dropdown",
          "label": "SBU",
          "required": true,
          "sortOrder": 600,
          "valueList": [
            "ACCT",
            "ADMN",
            "CRTV",
            "ENG",
            "HR",
            "IT",
            "LEGL",
            "S&M",
            "EXEC",
            "STND",
            "VOL"
          ],
          "defaultValue": "VOL"
        },
        {
          "name": "referralFeeType",
          "type": "text",
          "label": "Referral Fee Type",
          "required": false,
          "sortOrder": 800,
          "defaultValue": "Percentage"
        },
        {
          "name": "approvingClientContact",
          "type": "picker",
          "label": "Approving Client Contact",
          "sortOrder": 900,
          "pickerEntityIdProperty": "id",
          "pickerEntityLabelProperty": "name",
          "pickerEntityType": "ClientContact",
          "pickerEntityAdditionalLogic": "AND clientCorporation.id = ${jobOrder.clientCorporation.id}"
        },
        {
          "name": "backupApprovingClientContact",
          "type": "picker",
          "label": "Backup Approving Client Contact",
          "sortOrder": 905,
          "pickerEntityIdProperty": "id",
          "pickerEntityLabelProperty": "name",
          "pickerEntityType": "ClientContact",
          "pickerEntityAdditionalLogic": "AND clientCorporation.id = ${jobOrder.clientCorporation.id}"
        }
      ]
    },
    "updates": {
      "candidate": {
        "status": "Placed"
      },
      "jobSubmission": {
        "status": "Placed"
      }
    },
    "table": {
      "style": {
        "title": "Create Placement",
        "singleActionButtonLabel": "Update",
        "massActionButtonLabel": "Update all selected",
        "formCancelButtonLabel": "Cancel",
        "formSaveButtonLabel": "Save"
      },
      "fields": [
        {
          "name": "candidateName",
          "type": "text",
          "label": "Candidate",
          "defaultValue": "${candidate.name}",
          "displayOnly": true,
          "sortOrder": 0
        },
        {
          "name": "status",
          "type": "dropdown",
          "label": "Status",
          "required": true,
          "sortOrder": 5,
          "valueList": [
            "Submitted",
            "Reviewed",
            "Approved"
          ],
          "defaultValue": "Submitted"
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
          "name": "reportTo",
          "type": "text",
          "label": "Reporting to",
          "required": false,
          "sortOrder": 20
        },
        {
          "name": "correlatedCustomText1",
          "type": "dropdown",
          "label": "Branch",
          "required": true,
          "sortOrder": 23,
          "valueList": [
            "PP - Accounting & Finance",
            "PP - Administrative",
            "PP - Creative & Marketing",
            "PP - Engineering",
            "PP - HR",
            "PP - IT",
            "PP - Legal",
            "PP - Sales",
            "PP - Executive",
            "PTS - Acct & Fin Temps",
            "PTS - Temp Placement",
            "PTS - Volume Staffing"
          ],
          "defaultValue": "PTS - Volume Staffing"
        },
        {
          "name": "employmentType",
          "type": "dropdown",
          "label": "Employment Type",
          "required": true,
          "sortOrder": 30,
          "valueList": [
            "Temporary",
            "Temp to Hire"
          ]
        },
        {
          "name": "dateBegin",
          "type": "date",
          "label": "Start Date",
          "required": true,
          "sortOrder": 40,
          "dateFormat": "DD/MM/YYYY",
          "defaultValue": "${jobOrder.startDate}"
        },
        {
          "name": "dateEnd",
          "type": "date",
          "label": "End Date",
          "required": true,
          "sortOrder": 45,
          "dateFormat": "DD/MM/YYYY",
          "defaultValue": "${jobOrder.dateEnd}"
        },
        {
          "name": "correlatedCustomText6",
          "type": "text",
          "label": "PO Number",
          "required": false,
          "sortOrder": 53,
          "defaultValue": "${jobOrder.correlatedCustomText6}"
        },
        {
          "name": "costCenter",
          "type": "text",
          "label": "Cost Center",
          "required": false,
          "sortOrder": 55
        },
        {
          "name": "comments",
          "type": "textarea",
          "label": "Comments",
          "required": false,
          "sortOrder": 110
        },
        {
          "name": "payRate",
          "type": "currency",
          "label": "Pay Rate",
          "required": true,
          "sortOrder": 140,
          "defaultValue": "${jobOrder.payRate}"
        },
        {
          "name": "clientBillRate",
          "type": "currency",
          "label": "Bill Rate",
          "required": true,
          "sortOrder": 225,
          "defaultValue": "${jobOrder.clientBillRate}"
        },
        {
          "name": "correlatedCustomText4",
          "type": "dropdown",
          "label": "Invoice Format",
          "required": true,
          "sortOrder": 585,
          "valueList": [
            "TEMP",
            "TEMPCUS",
            "TEMPJOB",
            "TEMPPO",
            "PERM"
          ],
          "defaultValue": "TEMP"
        },
        {
          "name": "correlatedCustomText5",
          "type": "dropdown",
          "label": "Office",
          "required": true,
          "sortOrder": 590,
          "valueList": [
            "SLC"
          ],
          "defaultValue": "SLC"
        },
        {
          "name": "correlatedCustomText7",
          "type": "dropdown",
          "label": "SBU",
          "required": true,
          "sortOrder": 600,
          "valueList": [
            "ACCT",
            "ADMN",
            "CRTV",
            "ENG",
            "HR",
            "IT",
            "LEGL",
            "S&M",
            "EXEC",
            "STND",
            "VOL"
          ],
          "defaultValue": "VOL"
        },
        {
          "name": "referralFeeType",
          "type": "Text",
          "label": "Referral Fee Type",
          "required": false,
          "sortOrder": 800,
          "defaultValue": "Percentage"
        },
        {
          "name": "approvingClientContact",
          "type": "picker",
          "label": "Approving Client Contact",
          "sortOrder": 900,
          "pickerEntityIdProperty": "id",
          "pickerEntityLabelProperty": "name",
          "pickerEntityType": "ClientContact",
          "pickerEntityAdditionalLogic": "AND clientCorporation.id = ${jobOrder.clientCorporation.id}"
        },
        {
          "name": "backupApprovingClientContact",
          "type": "picker",
          "label": "Backup Approving Client Contact",
          "sortOrder": 905,
          "pickerEntityIdProperty": "id",
          "pickerEntityLabelProperty": "name",
          "pickerEntityType": "ClientContact",
          "pickerEntityAdditionalLogic": "AND clientCorporation.id = ${jobOrder.clientCorporation.id}"
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
