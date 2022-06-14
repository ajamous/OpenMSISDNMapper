# OpenMSISDN Mapper 


**OpenMSISDN Mapper** is detailed and  high quality e.164 to e.212 mapping database. it is essential for accurare billing, reporting and routing purposes for voice and SMS traffic to have an accurate list.



## Table of Contents

* [Introduction](#introduction)
* [Create the API](#create-the-api)
* [Using the API](#using-the-api)
* [Getting Help](#getting-help)
* [Warranty](#warranty)
* [Contribution](#contribuation)

## Introduction

It is surprisingly difficult for communications providers and developers to find a good quality e.164 to e.212 mapping database,
this data set has been created and updated manually using over 10 different data sources. data is provided in the hope that it will be useful but WITHOUT ANY WARRANTY.


You can just open an use the raw json file `OpenMSISDNMapper.json ` with your fav text editor and/or convert it to any file format you want e.g. SQL or CSV and use it as you wish, you may also create a quick RESTful API server from the json file to use it from your application.



This API allows you to integrate and interact with **OpenMSISDN Mapper** data set

The data is provided in standard JSON responses and uses HTTP Status Codes to help determine results.

## Create The API

- cd to the project path
- Install required packages
```shell
npm install -g 
```
- Run the API server 

```shell 
json-server --watch OpenMSISDNMapper.json 

```



## Using The API

1. Now you can open http://localhost:8080/lookup to list all records
2. Lookup a specific country E.164 & E.212 data http://localhost:8080/lookup?Country=EGYPT
3. Lookup a specific prefix_e164 data http://localhost:8080/lookup?prefix_e164=20
4. Lookup a specific MCCMNC data http://localhost:8080/lookup?mccmnc_e212=60203
5. Lookup a secondary MCCMNC data http://localhost:8080/lookup?mccmnc_secondary=1234

Sample Response:

```json
[
  {
    "prefix_e164": 202,
    "Country": "EGYPT",
    "Network Description": "Fixed - Cairo",
    "mccmnc_e212": 0,
    "mccmnc_secondary": ""
  },
  {
    "prefix_e164": 20,
    "Country": "EGYPT",
    "Network Description": "Fixed - Roc",
    "mccmnc_e212": 0,
    "mccmnc_secondary": ""
  },
  {
    "prefix_e164": 2011,
    "Country": "EGYPT",
    "Network Description": "Mobile - Etisalat",
    "mccmnc_e212": 60203,
    "mccmnc_secondary": ""
  },
  {
    "prefix_e164": 20110,
    "Country": "EGYPT",
    "Network Description": "Mobile - Etisalat",
    "mccmnc_e212": 60203,
    "mccmnc_secondary": ""
  },
  {
    "prefix_e164": 20111,
    "Country": "EGYPT",
    "Network Description": "Mobile - Etisalat",
    "mccmnc_e212": 60203,
    "mccmnc_secondary": ""
  },
  {
    "prefix_e164": 20112,
    "Country": "EGYPT",
    "Network Description": "Mobile - Etisalat",
    "mccmnc_e212": 60203,
    "mccmnc_secondary": ""
  },
  {
    "prefix_e164": 20114,
    "Country": "EGYPT",
    "Network Description": "Mobile - Etisalat",
    "mccmnc_e212": 60203,
    "mccmnc_secondary": ""
  },
  {
    "prefix_e164": 20115,
    "Country": "EGYPT",
    "Network Description": "Mobile - Etisalat",
    "mccmnc_e212": 60203,
    "mccmnc_secondary": ""
  },
  {
    "prefix_e164": 20117,
    "Country": "EGYPT",
    "Network Description": "Mobile - Etisalat",
    "mccmnc_e212": 60203,
    "mccmnc_secondary": ""
  },
  {
    "prefix_e164": 2012,
    "Country": "EGYPT",
    "Network Description": "Mobile - Orange",
    "mccmnc_e212": 60201,
    "mccmnc_secondary": ""
  },
  {
    "prefix_e164": 20120,
    "Country": "EGYPT",
    "Network Description": "Mobile - Orange",
    "mccmnc_e212": 60201,
    "mccmnc_secondary": ""
  },
  {
    "prefix_e164": 20122,
    "Country": "EGYPT",
    "Network Description": "Mobile - Orange",
    "mccmnc_e212": 60201,
    "mccmnc_secondary": ""
  },
  {
    "prefix_e164": 20127,
    "Country": "EGYPT",
    "Network Description": "Mobile - Orange",
    "mccmnc_e212": 60201,
    "mccmnc_secondary": ""
  },
  {
    "prefix_e164": 20128,
    "Country": "EGYPT",
    "Network Description": "Mobile - Orange",
    "mccmnc_e212": 60201,
    "mccmnc_secondary": ""
  },
  {
    "prefix_e164": 201,
    "Country": "EGYPT",
    "Network Description": "Mobile - Roc",
    "mccmnc_e212": 6020,
    "mccmnc_secondary": " 602 602999"
  },
  {
    "prefix_e164": 2010,
    "Country": "EGYPT",
    "Network Description": "Mobile - Vodafone",
    "mccmnc_e212": 60202,
    "mccmnc_secondary": ""
  },
  {
    "prefix_e164": 20100,
    "Country": "EGYPT",
    "Network Description": "Mobile - Vodafone",
    "mccmnc_e212": 60202,
    "mccmnc_secondary": ""
  },
  {
    "prefix_e164": 20101,
    "Country": "EGYPT",
    "Network Description": "Mobile - Vodafone",
    "mccmnc_e212": 60202,
    "mccmnc_secondary": ""
  },
  {
    "prefix_e164": 20106,
    "Country": "EGYPT",
    "Network Description": "Mobile - Vodafone",
    "mccmnc_e212": 60202,
    "mccmnc_secondary": ""
  },
  {
    "prefix_e164": 20109,
    "Country": "EGYPT",
    "Network Description": "Mobile - Vodafone",
    "mccmnc_e212": 60202,
    "mccmnc_secondary": ""
  },
  {
    "prefix_e164": 2015,
    "Country": "EGYPT",
    "Network Description": "Mobile - We",
    "mccmnc_e212": 60204,
    "mccmnc_secondary": ""
  }
]


```




## Getting Help

Help is provided by the community as soon as possible, you can open an issue here https://github.com/ajamous/MSISDN/issues .

## Warranty

OpenMSISDN Mapper  data is provided in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU General Public License for more details.

## Contribution

To keep this list error free and useful for everyone, We expect community members to create pull requests to contribute back improvements to the data set. Once a pull request is opened, project authors will run a verification using HLR to verify the updated data is correct before it's merged to the master branch.

**Submit your first contribution**

1- Clone project `git clone https://github.com/ajamous/OpenMSISDNMapper/` .

2- Create a new branch by issuing the command: `git checkout -b new_branch`

3- Create a new remote for the upstream repo with the command: `git remote add upstream https://github.com/ajamous/OpenMSISDNMapper/`

4- Switch to the new branch `git checkout -b new_branch`

5- edit  `OpenMSISDNMapper.json ` using your preferred text editor 

6- Committing your changes `git commit -S -m "Dial Code Improvmenth"`

7- push your changes ` git push -u origin new_branch`

Once you push the changes to your repo, the Compare & pull request button will appear in GitHub. Click it and next Open a pull request by clicking the `Create pull request button`


