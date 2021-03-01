# LWC Patient List

You have a newly created Lightning Web Component patientList under `src/lwc/patientList`.   
An apex class was written like this:
```Apex
public with sharing class PatientController {

  @AuraEnabled
  public static List<Patient> getPatientList() {
    // ...
  }
  
  // ...
  
  public with sharing class Patient {
    @AuraEnabled
    public Integer _id { get; set; }
    @AuraEnabled
    public String Row_ID { get; set; }
    @AuraEnabled
    public String Accurate_Episode_Date { get; set; }
    @AuraEnabled
    public String Case_Reported_Date { get; set; }
    @AuraEnabled
    public String Test_Reported_Date { get; set; }
    @AuraEnabled
    public String Specimen_Date { get; set; }
    @AuraEnabled
    public String Age_Group { get; set; }
    @AuraEnabled
    public String Client_Gender { get; set; }
    @AuraEnabled
    public String Case_AcquisitionInfo { get; set; }
    @AuraEnabled
    public String Outcome1 { get; set; }
    @AuraEnabled
    public String Outbreak_Related { get; set; }
    @AuraEnabled
    public Integer Reporting_PHU_ID { get; set; }
    @AuraEnabled
    public Integer _id { get; set; }
    @AuraEnabled
    public String Reporting_PHU { get; set; }
    @AuraEnabled
    public String Reporting_PHU_Address { get; set; }
    @AuraEnabled
    public String Reporting_PHU_City { get; set; }
    @AuraEnabled
    public String Reporting_PHU_Postal_Code { get; set; }
    @AuraEnabled
    public String Reporting_PHU_Website { get; set; }
    @AuraEnabled
    public Decimal Reporting_PHU_Latitude { get; set; }
    @AuraEnabled
    public Decimal Reporting_PHU_Longitude { get; set; }
  }
}
```

method `getPatientList` returns COVID patient data in a JSON array. A small subset of sample data looks like the following:
```JSON
[
  {
    "_id": 1,
    "Row_ID": 1,
    "Accurate_Episode_Date": "2020-05-28T00:00:00",
    "Case_Reported_Date": "2020-06-03T00:00:00",
    "Test_Reported_Date": "2020-06-03T00:00:00",
    "Specimen_Date": "2020-06-02T00:00:00",
    "Age_Group": "40s",
    "Client_Gender": "FEMALE",
    "Case_AcquisitionInfo": "CC",
    "Outcome1": "Resolved",
    "Outbreak_Related": "",
    "Reporting_PHU_ID": 2253,
    "Reporting_PHU": "Peel Public Health",
    "Reporting_PHU_Address": "7120 Hurontario Street",
    "Reporting_PHU_City": "Mississauga",
    "Reporting_PHU_Postal_Code": "L5W 1N4",
    "Reporting_PHU_Website": "www.peelregion.ca/health/",
    "Reporting_PHU_Latitude": 43.6474713,
    "Reporting_PHU_Longitude": -79.7088933
  },
  {
    "_id": 2,
    "Row_ID": 2,
    "Accurate_Episode_Date": "2020-05-24T00:00:00",
    "Case_Reported_Date": "2020-05-25T00:00:00",
    "Test_Reported_Date": "2020-05-25T00:00:00",
    "Specimen_Date": "2020-05-24T00:00:00",
    "Age_Group": "70s",
    "Client_Gender": "MALE",
    "Case_AcquisitionInfo": "CC",
    "Outcome1": "Resolved",
    "Outbreak_Related": "",
    "Reporting_PHU_ID": 2253,
    "Reporting_PHU": "Peel Public Health",
    "Reporting_PHU_Address": "7120 Hurontario Street",
    "Reporting_PHU_City": "Mississauga",
    "Reporting_PHU_Postal_Code": "L5W 1N4",
    "Reporting_PHU_Website": "www.peelregion.ca/health/",
    "Reporting_PHU_Latitude": 43.6474713,
    "Reporting_PHU_Longitude": -79.7088933
  },
  {
    "_id": 3,
    "Row_ID": 3,
    "Accurate_Episode_Date": "2020-04-07T00:00:00",
    "Case_Reported_Date": "2020-04-14T00:00:00",
    "Test_Reported_Date": "2020-04-14T00:00:00",
    "Specimen_Date": "2020-04-12T00:00:00",
    "Age_Group": "40s",
    "Client_Gender": "FEMALE",
    "Case_AcquisitionInfo": "NO KNOWN EPI LINK",
    "Outcome1": "Resolved",
    "Outbreak_Related": "",
    "Reporting_PHU_ID": 2253,
    "Reporting_PHU": "Peel Public Health",
    "Reporting_PHU_Address": "7120 Hurontario Street",
    "Reporting_PHU_City": "Mississauga",
    "Reporting_PHU_Postal_Code": "L5W 1N4",
    "Reporting_PHU_Website": "www.peelregion.ca/health/",
    "Reporting_PHU_Latitude": 43.6474713,
    "Reporting_PHU_Longitude": -79.7088933
  }
]
```

Please implement `patientList` component by calling the apex in imperative style and display the result data [in a data table like this](https://raw.githubusercontent.com/je-lwc/lwc-patient-list/master/result.jpg).   
Please try to explain your solution as you develop it.
