# Education API overview

The education API in Microsoft Graph enhances Office 365 resources with information that is relevant for education scenarios, including information about schools, classes, users (students and teachers), assignments, and submissions. This makes it easy for you to build solutions that integrate with educational resources for various school and classroom scenarios.

The education API in Microsoft Graph provides access to classes, schools, users, assignments, submissions and more.

![EDU Graph Overview](images/EDUGraph.PNG)

## Why integrate with education scenarios?

### Build applications that are aware of class roster

Most education software developers learn early on that class roster is one of the key pieces of information they need to run their application, and it's typically locked away inside a school Student Information System (SIS). Any time teachers bring a new application into their classroom, they spend time manually importing roster data into the app. Many ISVs address this by connecting with a SIS to import roster data. With hundreds of Student Information Systems with proprietary formats, this can become a challenge. [Microsoft School Data Sync](https://sds.microsoft.com/) combined with roster APIs addresses this challenge for application developers and schools.

The following are some of the scenarios that the roster APIs enable:

- [Get all classes in a school](https://developer.microsoft.com/en-us/graph/docs/api-reference/v1.0/api/educationschool_list_classes)
- [Get all users in a class](https://developer.microsoft.com/en-us/graph/docs/api-reference/v1.0/api/educationclass_list_members)
- [Get all the classes I teach](https://developer.microsoft.com/en-us/graph/docs/api-reference/v1.0/api/educationuser_list_classes)


### Leverage Microsoft Teams for creating class assignments in a Teams assignments tab

You can create a web app that manages class assignments by using the Edu Assignments API and then integrate your app in Microsoft Teams by using a new custom Tab.

Microsoft Teams in Office 365 is a digital hub that brings conversations, content, and apps together in one place for classrooms. Microsoft Teams provides a [rich set of extensibility points](https://docs.microsoft.com/en-us/microsoftteams/platform/concepts/apps/apps-overview), including creating Tabs, Connectors, and Bots. These extensibility points can call education APIs in Microsoft Graph to work with assignments and submissions. Build a more comprehensive experience by enabling your extension point with any other Microsoft Graph API along with assignment and submission APIs.

For education, Teams custom Tab apps are opened in an education class (a team) context where it makes sense to manage the end-to-end assignment flow from creation and distribution to grading and feedback. This is just one example of how Microsoft Teams save time and simplifies everyday logistics, leaving educators free to dedicate themselves to their students.

The following image shows that the **Science - Biology 1** class has a web app for managing assignments in an "Assignments" custom Tab.

![Microsoft Teams assignments, Assignments web app in custom tab](images/AssignmentsInTeams.PNG)

With assignment APIs your app can interact with the assignment service outside of Teams. Teams will handle distribution, due dates and grading while your system can provide a rich learning experience to students.
Here are examples of a few scenarios enabled by assignments API:

- [Add an Assignment that links to your application](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/api/educationclass_post_assignments) . 
- [Assign grades to individual students for assignments linked to your application](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/api/educationsubmission_update).
- [Create a student dashboard to show which assignments are due by when](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/api/educationclass_list_assignments).


## Enable school ITs to manage Identity and Roster sync using School Data Sync Management (preview)

[School Data Sync](https://sds.microsoft.com/) helps to automate the process of importing and synchronizing student identity and roster data from student information systems with Azure Active Directory (Azure AD) and Office 365. Once the information is synchronized, app developers can use the Roster APIs to read the roster information into the applications . If you are an system integrator setting up integration of a school's Student Information System with School Data Sync, you can use the [SDS management APIs](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/educationsynchronizationprofile) in Microsoft Graph to set up synchronization from either a CSV file or a supported SIS API connector.

School Data Sync management APIs support end to end scenarios for managing sync. Here are a few examples:

- [Create a synchronization profile that automatically starts a sync](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/api/educationsynchronizationprofile_post)
- Manage sync lifecycle with [Pause](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/api/educationsynchronizationprofile_pause), [Resume](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/api/educationsynchronizationprofile_resume) and [Reset](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/api/educationsynchronizationprofile_reset) operations.


## Next Steps:

### 1. Learn more about the reference APIs:

- Learn more about Roster APIs : [Roster APIs](https://developer.microsoft.com/en-us/graph/docs/api-reference/v1.0/resources/education-overview)

- Learn more about Assignments APIs (preview) : [Assignment APIs](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/educationassignment)

- Learn more about School Data Sync Management APIs (preview) : [SDS Management APIs](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/educationsynchronizationprofile)


### 2. Try out the APIs in Graph Explorer:

- Try out the EDU Graph APIs in Graph Explorer : [Graph Explorer](https://developer.microsoft.com/en-us/graph/graph-explorer)


### 3. Get started using the samples:

Check out end to end sample for Single Sign On, Roster Data integration and Assignments Integration using the samples below:

- [.NET Sample for SSO & Rostering](https://github.com/OfficeDev/O365-EDU-AspNetMVC-Samples
    )

- [Angular Node Sample for SSO & Rostering](https://github.com/OfficeDev/O365-EDU-AngularNodeJS-Samples)
    
- [Python Sample for SSO & Rostering](https://github.com/OfficeDev/O365-EDU-Python-Samples)

- [PHP Sample for for SSO & Rostering](https://github.com/OfficeDev/O365-EDU-PHP-Samples)

- [Sample for profile management APIs](https://github.com/OfficeDev/O365-EDU-SDS-AspNetMVC-Samples) 



 
