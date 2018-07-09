# App

This repo includes the app and job configuration files, `app.json` and
'job.json respectively, used to run an app on the agave platform.

The job is run on the private system `tacc-stampede2-<username>` as follows:
```shell
jobs-submit -V -W -F fastqc-0.11.5/job.json  > LOGS.txt 2>&1
```

The job culminates wth the following hob history update:
```
{                                                                               
  "status" : "success",                                                         
  "message" : null,                                                             
  "version" : "2.2.21-ra5e102f",                                                
  "result" : [ {                                                                
    "status" : "PENDING",                                                       
    "created" : "2018-07-07T16:05:52.000-05:00",                                
    "createdBy" : "jochoa",                                                     
    "description" : "Job accepted and queued for submission."                   
  }, {                                                                          
    "status" : "PROCESSING_INPUTS",                                             
    "created" : "2018-07-07T16:06:08.000-05:00",                                
    "createdBy" : "jochoa",                                                     
    "description" : "Attempt 1 to stage job inputs"                             
  }, {                                                                          
    "status" : "PROCESSING_INPUTS",                                             
    "created" : "2018-07-07T16:06:08.000-05:00",                                
    "createdBy" : "jochoa",                                                     
    "description" : "Identifying input files for staging"                       
  }, {                                                                          
    "status" : "FAILED",                                                        
    "created" : "2018-07-07T16:06:12.000-05:00",                                
    "createdBy" : "jochoa",                                                     
    "description" : "Unable to stage input agave://data-tacc-work-jochoa/stampede2/sd2e-data/sample/SP1.fq. Failed to authenticate to execution system tacc-stampede2-jochoa"
  } ]                                                                           
}
```
