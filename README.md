# IT_230_Portfolio
IT 230 Portfolio submission

**Briefly summarize the requirements and goals of the application you developed. What user needs was this application designed to address?**

The application's goal was to allow for student enrollment in actively available courses, while implementing academic rules. The critical requirements were preventing the enrollment of students in duplicate courses and preventing students from exceeding the maximum allowable total course load of 9 credit hours. The application further addressed the user need for a trustworthy and self-service opetion for managing academic registration without system errors.

**What did you do particularly well in developing this application?**

I have effectively developed strong validation logic for registration, clearly managing states such as successfully registered, already registered in the last term, and maximum allowable credit hours. In the Console application, all the validation logic was separated into a single ValidateChoice method and individual return codes, which improved the clarity and manageability of the overall logic. The WPF version did a good job of providing distinct visual feedback of current courses and total credit hours right away.

**Compare and contrast the Console and WPF application designs. What screens and features were necessary to support user needs and produce a user-centered UI for the app? How did your UI designs keep users in mind? Why were your designs successful?**

The Console application utilized a sequential, text-based, top-down interface compared to the WPF which utilized a more user-centered GUI to select courses using the ComboBox for quick selections, while the ListBox displayed registered courses. The WPF design was more user-centered since the ComboBox deterred invalid entry of a course and the user interface provided immediate repeatable, transparent feedback on current credit hours and enrolled courses. The single-screen design achieved a significant reduction in cognitive load and simplified the whole registration process.

**How did you approach the process of debugging and coding your application? What techniques or strategies did you use? How could you use those techniques or strategies in the future?**

I took an approach that focused on modularization and separation of concerns, specifically dedicating methods like ValidateChoice to simply validate input. The clear benefit of this idea, though, was the efficiency it allowed in debugging: it was easy to identify exactly which self contained function failed. Moving ahead, this model is very well suited for implementing unit testing on good, effective, core validation logic.

**Where did you have to be innovative to overcome a challenge in the full application development process?**

The primary challenge was to effectively track and validating registered courses without allowing duplicates; the Console application used non-scalable fixed variables to denote registering options. The WPF application used a more innovative, Object-Oriented approach to encapsulate the registration state directly within the Course object. The WPF application, in addition to utilizing the UI's ListBox.Items.Contains(), provided a cleaner and more scalable method for tracking enrollment state.
