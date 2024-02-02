# DataManagementSystem

adminUser: 
Email = "admin@example.com"
adminUserPassword = "Admin123!"



1. Backend
Develop the backend application and database hosted locally - no need to deploy to a hosting service.
Use the following tech stack:
- C# - .NET 7
- .NET Entity framework (for database management)
- .NET Identity (for users and roles management)
Use MVC architecture principles.
User accounts, and roles:
- Set up the following roles: Admin, Employee, and User.
- Admin
- Creating new accounts, and setting the employee/user roles
- Delete other non-admin users
- Everything else the Employee role can
- Employee
- Add/remove/update (CRUD) of data:
- Retailer
- Category
- Items
- Everything else the User role can
- User
- Read and write Retailer and Category filters
- A single Admin role should be automatically seeded upon creation of the database. Do not
provide means to create further Admin roles, and disallow deletion of the existing one.
General instructions:
1. Use the data found in the provided XMLs (in the Database input data section) to structure, and
build your Controllers, Models, Views (see the Frontend section for more details on Views), and
the database itself.
2. There are 3 data types here (apart from the Users, and Roles portion): Retailers, Categories, and
Items. Note that Items are meant to always have an associated Retailer and a Category they
belong to.
3. All the data from the XML files should be parsed to the database by writing an XML parsing
solution.
4. Items and Retailers have image URLs. Those images should be downloaded and stored locally
and that local copy should be referenced by the database. Do not manually populate the data or
download images.
API endpoints:
Create the following API endpoints:
1. GET GetAllItems(int? pageNumber = 1, int? countPerPage? = 8) - Returns a JSON object with all
items in the database. The optional pageNumber parameter (defaults to 1) allows us to specify a
page number for paginated results, and the optional countPerPage parameter (defaults to 8)
determines the number of items per page.
2. GET GetItemById(int? id) - Returns a JSON object of a specific item.
3. POST AddCategory(string? name) - Creates a new category with the given name.
4. PUT UpdateCategory(int? id, string? name) - Updates the name of an existing category.
Note: Make sure to handle all possible invalid parameter input types and values in your backend code.



2. Frontend (CMS)
1. The layout should be divided into:
a. menu (navigation) bar at the top,
b. contents filling the rest of the screen.
2. Login
a. If we are currently not logged in, the menu bar should be empty.
b. In the contents space, a login form should be displayed containing the following:
i. Mail input field
ii. Password input field
iii. Login button
iv. Should display error messages such as “Account not found” or “Invalid
password” etc.
c. Allowed login for admin + employee role
3. While logged in, the menu bar should be populated with the following:
a. Retailers
b. Categories
c. Items
d. Users - shown only if logged in as Admin!
e. Button “Logout”
4. Depending on the selected section from the header menu above, the appropriate table of
records is presented (Retailers/Categories/Items/Users).
5. To the right of each row in the table, there are “Edit”, and “Delete” buttons. Above the table,
there is an “Add” button.
a. Add: Opens up a new empty form with input fields appropriate to the selected record
type. Has a “Submit” button below the form that will add the data to the database.
b. Edit: Opens up a form pre-populated with the existing record’s data. Has a “Submit”
button below the form that will update the existing record in the database.
c. Delete: Deletes the record, and its associated file(s) (e.g. image(s)).




Database input data
- You can find the input data (in XML format) required for this assignment on the following link
- It is mandatory to use precisely, and only the data provided in the input database for the
assignment solution.



Repository
- Create 1 private GitHub repository containing your content for this assignment.
- Commit, and push all the minimum relevant files to the repository
- Maintain a branch named “development” where all features will be merged when completed
- Before submitting the assignment, merge the “development” branch into a “production” branch



Syntax instructions
Use Microsoft’s .NET Common C# code conventions



Solution submission
In your response mail you should provide the following:
1. Self-evaluation - Attached Docx document named
“Exordium_ProgrammerAssignment_Backend_yourName_yourSurname_dd.mm.yyyy.docx” -
which is a copy of this document, with a green highlight of the text for each point you consider
to have solved completely, yellow for partially, and red for unsolved.
2. “Exordium_ProgrammerAssignment_Backend_yourName_yourSurname.zip” containing
a. all content of your last repository commit, including
i. Backend/CMS VS Solution (all .sln, .csproj, .cs, and other files required to
seamlessly reproduce your .exe build functionality)
ii. Frontend Solution
iii. Database file(s)
iv. Note - Test your solution before sending
1. The backend Visual Studio solution should be compile-able, and
executable.
2. Always validate user input data!
b. yourName_yourSurname_README.txt file containing the information about used
external plugins - this file may be a part of the repository


