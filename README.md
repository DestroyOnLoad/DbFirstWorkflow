# DbFirstWorkflow
Practicing with a Database First Workflow using SQL Express and SSMS


NOTES...

DB from scratch
	1. Download MS Sql Express or other db
	2. Install Sql Server Management System /SSMS
	3. Create tables or run a script




In Visual Studio
	1. Create the project
	2. Add file to project and select ADO.NET Entity Model
	3. Select Design framework (1st option)
	4. Set up connection
	5. Rename to [DB]DbContext (it derives from class: DbContext)
	6. Select framework (Entity Framework 6)
	7. Bring in tables
	8. Finish - EDMX (Entity Data Model XML) will display
		a. Disable auto-save if it crashes VS

------ git commit --------
In DB
	1. Create a new table (simulate change)

Go back to VS
	1. Open EDMX and r-click to update db model
	2. Click selector for table to add
	3. Finish

------ git commit --------

In DB
	1. Add column in table (update table)
	2. Rename a column in a table (update table)
	3. Delete a column in a table (update table)
	4. Change data type of a column in a table (update table)

Go back to VS
	1. Update db model in EDMX
	2. Fix mapping errors
		a. Double check table mapper
		b. Delete columns in EDMX that no longer exist
		c. Update data types (consider code breaks)
		d. Validate

In DB
	1. Deleted a table (Update schema)

Go back to VS
	1. Update db model in EDMX
	2. Delete the unmapped table
	3. Validate

--------- git commit --------

In VS
	1. Update db model in EDMX
	2. Select stored procedures
		a. Make sure stored procedures -> entity model is checked
		b. Finish
	3. Test an imported function in Main.


-------- git commit ----------

In VS
	1. Review imported sp and func names to see if they follow C# naming conventions
	2. Edit any that do not.
	3. Review return types of imported sp and functions
	4. Edit any that are duplicates between complex and regular entity types.
	5. Manually delete complex types that no longer are used.

-------- git commit ----------

Can add new enum types in model browser to remove "magic" strings/ints.
	1. Add enum type
	2. Map column to enum type in properties
	3. Storage model has to map properly to data type (edit DB and then refresh model)
		
	
	


