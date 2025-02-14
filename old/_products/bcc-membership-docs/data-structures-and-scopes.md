---
title: Data Structures
---

# Data Structures and Scopes
This section describe `person` object and how it relates to scopes.

## Menu
- [Home](index)
- [API integration](api-integration)
- [Webhooks integration](webhooks)
- [Data Structures and Scopes](data-structures-and-scopes)
- [Single Sign Out](single-sign-out)

## This Document
- [Menu](#menu)
- [Scopes](#scopes)
- [Data Structures](#data-structures)
- [Enums](#enums)

## Scopes
Currently Members supports the following scopes. (_To understand the concept of scopes please have a look at scopes section on the [Home](index.md) page_)
#### Members (Custom Scopes)
- [`members.email`](#membersemail)
- [`members.read_active_status - new`](#membersread_active_status)
- [`members.phone`](#membersphone)
- [`members.profile - deprecated`](#membersprofile)
- [`members.address`](#membersaddress)
- [`members.read_person_id`](#membersread_person_id)
- [`members.read_name`](#membersread_name)
- [`members.read_birthdate - new`](#membersread_birthdate)
- [`members.read_gender - new`](#membersread_gender)
- [`members.read_culture - new`](#membersread_culture)
- [`members.read_picture - new`](#membersread_picture)
- [`members.read_church - new`](#membersread_church)
- [`members.read_club - coming`]()
- [`members.read_membership - deprecated`](#membersread_membership)
- [`members.read_spouse`](#membersspouse)
- [`members.read_children_dependents - new`](#membersread_children_dependents)
- [`members.read_parents_guardians - new`](#membersread_parents_guardians)
- [`members.read_family - deprecated`](#membersread_family)
- [`members.read_orgs`](#membersread_orgs)

Once you have the "Technical Administrator" role ([See Getting Started](index)) you will be able to log in to members and apply for these scopes for your application. See [API integration](api-integration) it shows the navigation to your application.

## Data Structures
Currently these scopes are all related to the `person` object and maps to the person fields as follows...

###### By default you automatically get provided with the "personID" and "lastChangedDate" in the case where you get data related to the member.
```json
  {
    "personID": 54512,
    "lastChangedDate": "2021-07-16T12:41:10.168Z" 
  }
```
###### `members.read_person_id`
```json
  {
    "personID": 54512,   
    "lastChangedDate": "2021-07-16T12:41:10.168Z"
  }
```
###### `members.read_active_status`
```json
  {
    "personID": 54512,
    "activeStatus":"Active",   
    "lastChangedDate": "2021-07-16T12:41:10.168Z"
  }
```
###### `members.email`
```json
  {
    "personID": 54512,
    "email": "philly.daly@gmail.com",
    "lastChangedDate": "2021-07-16T12:41:10.168Z"
  }
```
###### `members.phone`
```json
  {
    "personID": 54512,
    "cellPhone": {
      "formatted": "+47 925 07 748",
      "number": " 925 07 748",
      "prefix": "47",
      "unFormatted": "+4792507748"
    },
    "homePhone": {
      "formatted": "+47 925 07 748",
      "number": " 925 07 748",
      "prefix": "47",
      "unFormatted": "+4792507748"
    },
    "lastChangedDate": "2021-07-16T12:41:10.168Z"
  }
```
###### `members.profile`
```json
  {
    "personID": 54512,
    "firstName": "Philly",
    "middleName": "Pelle",
    "lastName": "Daly",
    "displayName": "Philly Pelle Daly",
    "birthDate": "1988-12-08T00:00:00",
    "gender": "Male",
    "cultureCode1": "en-US",
    "profilePicture": "https://storage.googleapis.com/kinetic-center-276213_profile-pictures/178509735_a0mdd0q2qh.jpg",
    "lastChangedDate": "2021-07-16T12:41:10.168Z"
  }
```
###### `members.address`
```json
 {
    "personID": 54512,
    "currentAddress": {
      "address1": "testAddress3",
      "city": "Ås",
      "country": {
        "iso2Code": "no",
        "nameEn": "Norway",
        "nameNative": "Norge",
        "nameNo": "Norge"
      },
      "formatted": "Bjørnekroken 85\n1435 Ås",
      "formattedAddressLine1": "Bjørnekroken 85",
      "formattedAddressLine2": "1435 Ås",
      "formattedAddressLine3": "",
      "formattedAddressLine4": "",
      "formattedAddressLine5": "",
      "formattedAddressLine6": "",
      "postalCode": "1435"
    },
    "lastChangedDate": "2021-07-16T12:41:10.168Z"
  }
```
###### `members.read_name`
```json
  {
    "personID": 54512,
    "firstName": "Philly",
    "middleName": "Pelle",
    "lastName": "Daly",
    "displayName": "Philly Pelle Daly",
    "lastChangedDate": "2021-07-16T12:41:10.168Z"   
  }
```
###### `members.read_birthdate`
```json
  {
    "personID": 54512,    
    "birthDate": "1988-12-08T00:00:00",    
    "lastChangedDate": "2021-07-16T12:41:10.168Z"
  }
```
###### `members.read_gender`
```json
  {
    "personID": 54512,    
    "gender": "Male",   
    "lastChangedDate": "2021-07-16T12:41:10.168Z"
  }
```
###### `members.read_culture`
```json
  {
    "personID": 54512,    
    "cultureCode1": "en-US",    
    "lastChangedDate": "2021-07-16T12:41:10.168Z"
  }
```
###### `members.read_picture`
```json
  {
    "personID": 54512,    
    "profilePicture": "https://storage.googleapis.com/kinetic-center-276213_profile-pictures/178509735_a0mdd0q2qh.jpg",
    "lastChangedDate": "2021-07-16T12:41:10.168Z"
  }
```
###### `members.read_church`
```json
  {
    "personID": 54512,
    "churchID": 69,
    "church": {
      "active": true,
      "archived": false,
      "startDate": "2020-10-18T11:52:46.474Z",
      "endDate": "2021-11-28T00:00:00.000Z",
      "membershipType": "participant",
      "name": "Oslo/Follo",
      "visitingAddress": {
        "address1": "Ryenstubben 2",
        "address2": "0679 Oslo",
        "address3": null,
        "address4": null,
        "city": null,
        "country": {
          "iso2Code": "no",
          "nameEn": "Norway",
          "nameNative": "Norge",
          "nameNo": "Norge"
        },
        "postalCode": "1444"
      },
      "orgID": 69,
    },
    "lastChangedDate": "2021-07-16T12:41:10.168Z"
  }
```
###### `members.read_membership`
```json
  {
    "personID": 54512,
    "churchID": 69,
    "church": {
      "active": true,
      "archived": false,
      "startDate": "2020-10-18T11:52:46.474Z",
      "endDate": "2021-11-28T00:00:00.000Z",
      "name": "Oslo/Follo",
      "visitingAddress": {
        "address1": "Ryenstubben 2",
        "address2": "0679 Oslo",
        "address3": null,
        "address4": null,
        "city": null,
        "country": {
          "iso2Code": "no",
          "nameEn": "Norway",
          "nameNative": "Norge",
          "nameNo": "Norge"
        },
        "postalCode": 1444
      },
      "orgID": 69,
    },
    "lastChangedDate": "2021-07-16T12:41:10.168Z"
  }
```
###### `members.spouse`
```json
  {
    "personID": 54512,
    "related": {
      "spouse": [
        {        
          "personID": 13629
        }
      ]
    }
  }
```
###### `members.read_children_dependents`
```json
  {
    "personID": 54512,
    "related": {
      "children": [
        {          
          "personID": 13623
        }
      ],      
      "dependents": [
        {          
          "personID": 16633
        }
      ]     
    }
  }
```
###### `members.read_parents_guardians`
```json
  {
    "personID": 54512,
    "related": {
      "parents": [
        {          
          "personID": 13624
        }
      ],      
      "guardians": [
         {          
          "personID": 14654
        }
      ]     
    }
  }
```
###### `members.read_family`
```json
  {
    "personID": 54512,
    "related": {
      "spouse": [
        {
          "church": {
            "orgID": 69,
            "org": {
              "churchID": 69
            }
          },
          "displayName": "Batie Sofa Daly",
          "personID": 13629
        }
      ],
      "children": [...],
      "dependents": [...],
      "guardians":[...],
      "parents": [...]
    }
  }
```
###### `members.read_orgs`
```json
{  
  "name": "Oslo/Follo",
  "orgID": 69,
  "status": 0,
  "type": "church",
  "visitingAddress": {
    "country": {
      "iso2Code": "no",
      "nameEn": "Norway",
    }
  },
  "website": null
}
```

## Enums

Here are enum members used in above data structures.

```typescript
export enum MaritalStatus {
    Unknown = 'Unknown',
    Single = 'Single',
    Married = 'Married',
    Widowed = 'Widowed',
    Separated = 'Separated',
    SingleParent = 'SingleParent',
}
```



```typescript
export enum Gender {
    Female = 'Female',
    Male = 'Male',
}
````


```typescript
export enum ActiveStatus {
    Active = 'Active',
    Inactive = 'Inactive',
    Duplicate = 'Duplicate',
    Deceased = 'Deceased',
    Contact = 'Contact',
}
````

```typescript
export enum MembershipType {
    participant = 'participant',
    affiliator = 'affiliator',
    member = 'member',
}
````
