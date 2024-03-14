# Deliverable 2

This portion of the lab consists of a the functioning CRUD component for creating/editing information in a single database table, supported by services in the BLL.

> **Remember to [reference your issues](./ReadMe.md)** when committing your work through this deliverable.

## CRUD – Single Item CRUD

On this component, the student must provide a means to

* **Insert** new rows of data into a table
* **Update** an existing row of data in a table
* **Delete** (or mark as inactive/not current) a row of data in a table
* **Cancel** editing (this should return the user to the `Query` component)

### Alter Query component to transfer to CRUD component

Alter your Query component to contain a button/link that will transfer you to the CRUD component for entering a new record. Alter each tabular line to transfer an appropriate piece of data to the CRUD component so the associated database record can be retreived and displayed.

### Handling Foreign Keys With Large Data Sets

For many of the scenarios, foreign key information will have to be handled in a search/filter manner. The reason for this is because there are far too many rows of data to put in a single drop-down control. For example, with thousands of *Students* in the database, it is impractical to fill a drop-down and expect a user to find the student they wish to edit. In these situations, a two-step selection process makes the form more manageable by the user. **Consult your specific scenario for further guidance on this matter.**

### Processing Delete

Depending on the scenario and the table, the Delete functionality may not be a physical removal of a row of data. This is because some tables have triggers or other constraints that prevent the removal of existing rows. In these cases where a row cannot be deleted (excluding foreign key constraints preventing removal), the table will have some means of flagging the row as being inactive or not current. **Consult your specific scenario for further guidance on this matter.**

----

## Evaluation - *15%* 

> ***NOTE:** Your code **must** compile. Solutions that do not compile will receive an automatic mark of zero (0).*
>
> If you are unable to get a portion of the assignment to compile, you should:
>
> - Comment out the non-compiling portion of code
> - Identify the non-compiling portion in the **Incomplete Requirements** heading, noting the item's
>   - File name (e.g.: "Account.cs")
>   - Line number(s)
>   - Compiler error number and general message

Your assignment will be marked based upon the following weights. See the [general rubric](./ReadMe.md#generalized-marking-rubric) for details.

| Weight | Earned | Deliverable/Requirement |
| ---- | --------- | -----------------|
| 10 |     | `CRUD` Component correctly functions as per scenario and general specifications |
| ---- | ---- | --------- |
| **10** |    | **Total** |

### Suggest check list

* Lab Documentation (Web Form)
  - [ ] List of known bugs & incomplete portions of lab
* Project Architecture & Code Quality
  - [ ] Proper & consistent use of exceptions and exception handling
  - [ ] Separate BLL classes coded for all the required tables
  - [ ] BLL method(s) required for all form queries
  - [ ] BLL method required for Add
  - [ ] BLL method required for Update
  - [ ] BLL method(s) required for Delete
* Component – Single Item CRUD
  - [ ] Correctly populates DropDownList controls on page load (if required)
  - [ ] Correctly applies a UI for the appropriate search technique (use of filter where requested)
  - [ ] Correctly uses the appropriate search techniques/filters to Foreign Key references (where applicable)
  - [ ] Correctly looks up and displays a single item
  - [ ] Uses disabled (non-editable) controls for all data that is not related to Add/Update functionality
  - [ ] Correctly uses Validation for Add/Update functionality
  - [ ] Correctly adds data to a database
  - [ ] Correctly gives up-to-date feedback on whether the add was successful or not
  - [ ] Correctly retains data display whether the add was successful or not
  - [ ] Correctly updates data in the database
  - [ ] Correctly gives up-to-date feedback on whether the update was successful or not
  - [ ] Correctly retains data display whether the update was successful or not
  - [ ] Correctly performs Delete of data (or equivalent) in the database
  - [ ] Correctly gives up-to-date feedback on whether the attempted delete (as applicable) is successful
  - [ ] Correctly retains data display whether the delete was successful or not
  - [ ] Messages correctly identifies items on the web display.
  - [ ] Appropriate error handling has been implemented
  - [ ] Cancel returns user to Query Component
-->
