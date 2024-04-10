# Deliverable 1 - Project Setup and Query Component

This portion of the lab consists of setting up the structured solution, documentation, and functioning code for required entities and DAL layer, and the functioning Query page and the related BLL services

> **Remember to [reference your issues](./ReadMe.md)** when committing your work through this deliverable.

## Required Projects

Your solution must be a client-server solution consisting of multiple projects as outlined in the course. The Presentation Layer portion is to be an ASP.NET Web Application (**.NET Core 8.0** Blazor Components). The BLL, Entity classes and DAL portions of the system are to be placed in a separate class library project (**.NET Core 8.0**).

## The StarTED Database

The database supplied for this lab is an SQL Server database named "StarTED". The following is a **sample** of the connection string that may be used for the Presentation Layer.

```json
  "StarTEDDb": "Server=.;Database=StarTED;Trusted_Connection=true;MultipleActiveResultSets=true"
```

In creating the entities for tables from the database, **only create for those tables related to your specific scenario** (deductions may be applied if you create additional entities). You are encouraged to generate the entities and the database context class using [reverse engineering](https://docs.microsoft.com/ef/core/managing-schemas/scaffolding?tabs=dotnet-core-cli#specifying-tables).

## Program.cs and Extension method

Create an appropriate extension method to register services and your DbContent connection. Add this extension service to your application class library. Create the code to register your context service. Create the required registrations for any services created for this deliverable.

Alter your `Program.cs` class to obtain your database connection string and call your extension method to allow access to registered services.

## The Components

There are two components for the core functionality of this project (described below). Create the components with appropriate header text describing the component. The Query component will be completed in this deliverable. The functionality for the CRUD component is to be completed in a subsequent deliverable. You must name the components **Query** and **CRUD**. In addition, you must [edit the **Home** component] of your web application. All of these components must use the same [layout](#layout-and-styling).

### Layout and Styling

You are expected to decide upon the styling approach for your site (Holiday, Bootstrap, awsm.css, Tailwind, etc.) and put some effort in to making your content look presentable. In addition, your layout display must contain the following elements:

* **Site Navigation** – Links to all the components in the web application. (`NavMenu.razor`)
* **Scenario Title** – The number and name of the scenario (e.g.: G1 – Reservations by Group) on the footer. (`MainLayout.razor`)
* **Student Name** – Your first and last name on the footer. (`MainLayout.razor`)

### Default Page

Your default (**Home**) component must contain the following elements (each with their own heading):

- **Deliverable Descriptions** – A brief description (one or two paragraphs) of the `Query` and `CRUD` component's requirements in the project, identifying the name of the component and its purpose, along with any unique constraints or characteristics of the page's behaviour.
- **Known Bugs** – A bulleted list of all the known bugs and incomplete portions of the lab.
- **Entity Relationship Diagram** - The ERD diagram of your specific scenario (you may copy the one from your specific scenario description).
- **Site Styling Decision** - Indicate what [site-wide styling](#layout-and-styling) you are using in your website.


## Component: Query – Search/Filter & Display Results

> For details of what is to be on this component, consult your specific scenario.

On this component, the student must display multiple rows of data in an HTML table. All fields of the displayed image must be used, as specified in your scenario. 

Your tabular report should display 10 to 25 rows per page (as appropriate for your scenario). This may be done using a paging or scrolling technique. 

The page must have appropriate error handling and message capability.
----

## Evaluation - *10%* 

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
| ---- | ------ | ----------------------- |
| 1 |    | Creation of Projects |
| 2 |    | EF Core DAL/Entities |
| 2 |    | Project References and Configuration (Service registration) |
| 2 |    | Layout and Styling |
| 2 |    | Default Component Documentation |
| 1 |    | Placeholder Component CRUD |
| 10 |   | `Query` Component Correctly Functions as per scenario and general specifications |
| ---- | ----- | --------- |
| **20** |     | **Total** |

### Suggested check list

- Project Architecture & Code Quality
  - [ ] Client-Server architecture (multiple projects inside a single solution)
  - [ ] Layout display with functioning site navigation, Scenario Title and student's name
  - [ ] Appropriate Entity classes as per scenario
  - [ ] Requested annotation for Entity CRUD class (Key, optional NotMapped, DatabaseGeneration)
  - [ ] Appropriate validation annotation for Entity CRUD class (Required, StringLength)
  - [ ] DAL class with appropriate code for all the required entities
  - [ ] DAL class has access mode of internal
  - [ ] Proper & consistent use of exceptions and exception handling in BLL classes
  - [ ] Separate BLL classes coded for all the required tables
  - [ ] BLL classes and methods use correct annotations
  - [ ] Services have been registered
- Configuration
  - [ ] Proper references have been setup between projects.
  - [ ] appsetting file has the correct entry for connection string
  - [ ] Extension class/method for service registration has been setup in application class library
  - [ ] Program.cs class obtains connection string and calls registration services method in extension class
- Lab Documentation (Web Form)
  - [ ] Requested Lab documentation placed as the home component for the web application (Home.razor)
  - [ ] List of known bugs & incomplete portions of lab
  - [ ] Entity Relationship Diagram of selected scenario
- CRUD – Single Item CRUD
  - [ ] Blank component with title of selected option in the student's scenario and component banner title.
  - [ ] Content component PageTitle set to CRUD - StarTED
- Query – Tabular report
  - [ ] Proper & consistent use of exceptions and exception handling
  - [ ] Component with title of selected option in the student's scenario and component banner title.
  - [ ] Content component PageTitle set to Query - StarTED
  - [ ] Correctly applies an appropriate search technique (use of filter where requested)
  - [ ] Correctly performs Lookup
  - [ ] Tabular display uses column headers with meaningful names 
  - [ ] Tabular display uses appropriate alignment and formatting for displayed data
  - [ ] Tabular display data is correct
  - [ ] Tabular display demonstrates limited line displaying (paging or scrolling)
  - [ ] Appropriate error handling and user messages have been implemented
- _MainLayout.razor/NavMenu.razor
  - [ ] Menu with working links to the Home and CRUD/Query components
  - [ ] Your name shows on the screen
  - [ ] Your scenario shows on the screen


