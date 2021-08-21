# SDA Website

##### INTRODUCTION

The purpose of this project was to let everyone view our shutterbugs' picture gallery in an efficient manner along with keeping the albums safe and managed in club's google drive.

Shutterbug contains data in TBs hence it was not feasible to store that data in any kind of database and creating APIs for accessing it. Moreover as many number social and academic events happens very semester updating that database and managing it would been difficult.

##### SOLUTION

The team come up with a solution of using Google Script and DriveApp service of Google to link the drive with web page.

- The website is connected with a specific folder in shutterbugs drive where the photography society keeps all the sorted albums that are ready to be distributed, this folder provide us to the albums of different years.
  
- User select a year and all the events that were captured in that year are renders onto the screen.
  
- Then user selects an folder of an event, from here a function takes the folder Id and loop up for the data it contains. There could be 4 possible situation that may occur.
  - Folder may contain more nested folders only.
  - Folder may contain file/pictures only.
  - Folder may contain both folders and files.
  - Folder may be empty.

- Required actions are performed according to the sitution 
  - A function first check data inside the parent folder(event folder that is been selected) and categories the situation.
  - If it is an empty for folder we display it's an empty folder.
  - If it contains nested folders only, we display all the folders. 
  - If it contains files/pictures we create an embed link, this embed link is a preview link of the drive's web page, and then we display this drive's web page in our application through "iframe" tag.
  - If it contains both then we sort out the folders and display them above and below that we render the drive's web page.

This way we saved the efforts for maintaining a separate database, and this solution reflects any updates that happens in drive, hence whenever a new event is covered and pictures are uploaded to the drive they are live to visited by anyone across the web.
