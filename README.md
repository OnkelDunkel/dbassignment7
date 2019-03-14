# Assignment 07

## Ex1

### 1st normal form violations
* Whether the materialised view has a primary key or not depends on the implementation. However the table does have the customerNumber column with unique values so this could be set as primary key.
* Eventhough the names and address has been concated one could still argue that those columns are a single domain.

### 2nd normal form violations
For assessing this I assume that customerNumber is implemented as the primary key in the materialized view.
* The column *repCity* is dependant on the column *repZip*. This means that if a new city name was associated with the zipcode this would have to be updated in every row with that zipcode. This breaks the 2nd normal form that "all non-key columns are dependant on all of the tables primary key".

### 3rd normal form violations
* All the columns starting with *rep* does not describe the customerNumber. This means that those columns does not belong to this table in order to live up to the 3rd normal form.

## Ex2

### The handin must mention which column(s) you suggest to use as key, and argue why they functionally determines the entire row.
I would use the customerName and the contactPhone as a primary key because both origins from columns that does not allow null. It is also rather unlikely (though not impossible) that to people with the same name has the same phone number registered. If to people shares the same phone no they might also live together on same address which is why *contactName, custCity* and *custCountry* is not included in the primary key. This does not change above mentioned normal forms violations.

### Also, mention if there are any new issues with normal forms.

## Ex3

### 3.1: Write a safe update statement that change the repPhone column from oldNumber (say 12345678) to newNumber (say 87654321).

### 3.2: Write an update of repEmail which do not update properly (do not update it everywhere it should)

## Ex4