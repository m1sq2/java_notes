variable u [[Java]]
variabla je drzac za vrednost i ponasa se kao vrednost koju sadrzi

## Data Types
#data_type

| ***data type***  | ***size*** | ***value*** |
| ---------- | --------- | -------|
| *boolean*| 1bit|true or false|
| byte| 1byte|-128 to 127|
| short | 2byte | -32,768 to 32,767 |
| *int* | 4byte | -2billlion to 2billion|
| long | 8bytes | -9quintilion to 9quintilion|
| float | 4bytes | fraction numbet up to 6-7digits|
| *double* | 8bytes | fraction number up to 15digits|
| *char* | 2bytes| single character|
| *String* | zavisi| niz karaktera|

samo je String, Arrays, Classes referencijalni data type, svi ostali su primitivni

#primitiv_data_type | #reference_data_type
-- | --
8 types | unlimted
store data | stores adress
can only hold 1 value | could hold more
less memory | more memory
fast | slow

## Definisanje variabli

```java
int x;                       //deklaracija
x = 123;                     //dodela
                             //+
int x = 123;                 //inicijacija
```

- prvo deklarisemo data type
- pa ime variable
- nakon toga mozemo da delimo toj variabli vrednost
- a mozemo da spojimo oba procesa i da delarisemo data type, pa ime, i dodelimo vrednost

sve dok se variabli ne dodeli vrednost, vrednost ce biti postavljena na `null`

