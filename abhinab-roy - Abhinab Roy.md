# Developer - Winter of Code 2020

# Abhinab Roy

## Organisation Name : [Canvasbird](https://github.com/Canvasbird)

### Project : [Canvasboard](https://github.com/Canvasbird/canvasboard)  
#### My work on the Canvasboard project aimed at improving the different components and adding new features.

I am [Abhinab Roy](https://github.com/DevoAbhi), an undergraduate student from Netaji Subhash Engineering College, Kolkata.  

My work was mentored by [Kajol Kumari](https://github.com/kajol-kumari) and [Akash Madduru](https://github.com/akashmrc98).

[Akshay Sujith](https://github.com/goliakshay357) guided and helped me throughout the program.

# Contributions

## 1. Added Daily Quote Feature 
In this task, I added a feature to display a quote every new day on the dashboard page. 
- [#228](https://github.com/Canvasbird/canvasboard/pull/228)

## 2. Filter using Workspace
In this task, I added a search option in dashboard page. This feature enables the users to search their specific workspace by writing their initials in the search box.
- [#267](https://github.com/Canvasbird/canvasboard/pull/267)

## 3. Added Password Strength Classifier
This task was based on the issue that the users were able to sign up with a weak password which affects their account security. I added a feature to check the password strength and only let them sign up if the password is a strong one.
- [#306](https://github.com/Canvasbird/canvasboard/pull/306)

## 4. Miscellaneous

I also solved some other issues that were interesting. The Pull Requests are listed below :-
1. [#301](https://github.com/Canvasbird/canvasboard/pull/301) - In this, I removed a bug that even if the user adds a new workspace, the "No Workspace Found!" message would still display.
2. [#313](https://github.com/Canvasbird/canvasboard/pull/313) - In this, I added a feature to display a message of "Please add a Workspace!" when the user has not added any workspace or removed all the workspaces.
3. [#270](https://github.com/Canvasbird/canvasboard/pull/270) - In this, I added some responsiveness to the toolbar.
4. I also solved few small issues like :-
    * [#202](https://github.com/Canvasbird/canvasboard/pull/202) - Board component buttons and backgound position fixed

    * [#208](https://github.com/Canvasbird/canvasboard/pull/208) -  Add exit button functionality

    * [#216](https://github.com/Canvasbird/canvasboard/pull/216) - Remove forgot password and institute name from sign up page

    * [#224](https://github.com/Canvasbird/canvasboard/pull/224) - Fixed logout button in mobile resolution

    * [#225](https://github.com/Canvasbird/canvasboard/pull/225) - Fixed wrong auto fill in signup page 
  

# Issues Opened
## 1. The exit button does not have any function 
  * [#207](https://github.com/Canvasbird/canvasboard/issues/207) - In this, previous version of the Canvasboard project, the exit button in the boards page did not have any functionality.
  * [#215](https://github.com/Canvasbird/canvasboard/issues/#215) - This bug is related to the exit button in the boards page. If the user had some unsaved elements in the page, the user were still able to exit to the previous page. I tried to solve the issue using CanDeactivate guard and subject but later found that the Canvasboard had moved to a new version which shift the board component to a new component.
  * [#308](https://github.com/Canvasbird/canvasboard/issues/#308) - In this bug, the user were displayed a non-intuitive message when they try to sign up with a username that already existed. It is solved by one of the contributors and is closed now.
  * [#303](https://github.com/Canvasbird/canvasboard/issues/#303) - This is a crucial bug that when the user renames a folder, the folder does not appear when it is searched, it only appears if the page is reloaded.
   

# Future Scope
I believe my work has helped this project to some extent. I would like to have the following in this project in future :-
1. Files page CRUD
2. Feature to create a nested folder inside a Workspace
3. Feature to save creative board changes.
4. Feature to exit the page using a button and ask the user to save changes during exit.

# Overall Experience

The one month of work in Canvasbird helped me learn and grow to a great extent. I was so lucky to be mentored by Kajol(Thanks for reviewing all my PRs) and Akash whose constant guidance helped me complete my tasks easily. I would further extend my gratitude towards Akshay, who was the person I always reached when I faced any issues regarding the understanding of the tasks. 

WoC with Canvasbird was an unforgettable and most learning experience for me. Being my first open-source organization where I contributed, Canvasbird will always have a special place.
