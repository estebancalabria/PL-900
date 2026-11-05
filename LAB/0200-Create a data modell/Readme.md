
* [BROWSER] https://make.powerapps.com
  * Elegir enviroment (Dev One)
 
  * [LEFT-NAVBAR] TABLES
    * [LINK] + New Table
      * [DROPDOWN] New Table (Advanced Properties)
        * Tab Properties
          * DisplayName :  Facility Request.
        * Tab Columan Principal
          * DisplayName : Request Title

* Columnas
     
| Column Display Name | Data Type | Additional Settings |
|:-------------------:|:---------:|:-------------------:|
| Description | Plain text | Max length: 2000 |
| Date Requested | Date Only | Behavior: Simple |
| Estimated Cost | Currency | Leave defaults |
| Category | Choice | Choices: Maintenance, Equipment, Supplies, Room Setup, Other |
| Priority | Choice | Choices: Low (1), Medium (2), High (3), Urgent (4) |
| Status | Choice | Choices: New, In Progress, Completed, Cancelled (Default: New) |

* Luego agregarle los datos

| Request Title | Category | Priority | Status |
|:-------------:|:--------:|:--------:|:------:|
| Broken printer in Room 201 | Equipment | High | New |
| Order paper supplies for Floor 3 | Supplies | Low | New |
| Conference room setup for Monday | Room Setup | Medium | In Progress |

  * [LEFT-NAVBAR] TABLES
    * [LINK] + New Table
      * [DROPDOWN] New Table (Advanced Properties)
      * Comenzar con un lienzo en blanco

* [COPILOT] Usar estos prompts:

```
Rename New Column in the Room table to Room Name
```

```
Add new columns named Campus, Building, and Floor to the room table.
```

```
Add a new yes/no column named Conference Room to the Room table
```

```
Agregar daros : Room	Campus	Building	Floor	Conference Room
301 A	North	HighPoint	3	Yes
233	South	Seirra	2	No
401 B	East	Jacobson	4	Yes
```

* Agregar una columna Lookup a Facility Request:

  * [LEFT-NAVBAR] TABLES
    * [SEARCH] Facility
    * [TABLE] Facility Request
      * [SCHEMA] Columns
        * [+ New Column]
          * Display Name: Room
          * Data Type: Lookup
          * Related Table: Room
        * [BUTTON] Save
