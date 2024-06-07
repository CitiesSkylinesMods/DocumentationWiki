# Reviewing Pull Request Using Visual studio

![Screenshot (749)](https://user-images.githubusercontent.com/26344691/81138210-05830780-8f6a-11ea-9f08-8101a5bab189.png)

GitHub web interface or GitHub desktop have very limited features for code review making it very difficult to understand the code in Pull Request. Using IDE like Visual studio to perform the code review can make it much easier to follow the code. 

[these instructions](https://github.com/CitiesSkylinesMods/TMPE/blob/master/docs/BUILDING_INSTRUCTIONS.md) explain in detail how to setup your IDE and several ways to clone and build a copy of TMPE repo. The instructions bellow focus on reviewing code using Visual studio and assumes you already have setup your Visual studio environment.

### Clone source code

1.  Go to TMPE source code : https://github.com/CitiesSkylinesMods/TMPE 
if you are reviewing code from a fork go to the fork url instead.
2.  click the green "clone or download button" 
![Screenshot (910)](https://user-images.githubusercontent.com/26344691/81138024-3dd61600-8f69-11ea-865f-a95c68e0f1f1.png)
3.  click "Open in visual studio"
4.  a pop up may open asking you to install visual studio plugin.
5.  visual studio opens automatically. press Clone to complete the cloning process.
![Screenshot (1002)](https://user-images.githubusercontent.com/26344691/81138950-86db9980-8f6c-11ea-9f76-aa7a39aa2ccf.png)

### Open pull request
![Screenshot (747) copy](https://user-images.githubusercontent.com/26344691/81147104-4555e900-8f82-11ea-8f3e-e2c38675ad90.png)

To open a pull request for review follow the steps bellow (pay attention to the red letter markers in screenshot above):
1.  Click on the GitHub tab (B) or click on the GitHub icon in the status bar (A) . Alternatively you can go to `menu bar-> View -> other windows-> GitHub`.
2.  see [Section bellew](https://github.com/CitiesSkylinesMods/TMPE/wiki/Reviwing-pull-request-using-Visutal-studio#work-around-visual-studio-bug) if you see error message "could not resolve a repository with the name TMPE"
3.  click the fork icon (C) and then choose `krzychu124/cities-Skylines-Traffic-Manager-President-Edition` (or `CitiesSkylines_TMPE`) from the drop down (D). If the pull request is from any other fork choose the appropriate fork name from the drop down.
4.  click on a pull request
![Screenshot (748)](https://user-images.githubusercontent.com/26344691/81138232-129ff680-8f6a-11ea-8efa-7d425cad96c6.png)

Now you should be able to see a list of file changes. ![Screenshot (1008)](https://user-images.githubusercontent.com/26344691/81146418-e9d72b80-8f80-11ea-854a-186623996fa7.png)
double click on a file to view diff or right click for more options (C). click on the chat icon (B) to see chat message but it is better to view the chat in GitHub (A). to checkout the code checkout the displayed branch name (D).

### Work around Visual studio bug
![Screenshot (757)](https://user-images.githubusercontent.com/26344691/81138234-129ff680-8f6a-11ea-90da-ef653b4fc140.png)
If you see error message "could not resolve a repository with the name TMPE" then you should work around a bug in VS. this error occurs because we have diverted https://github.com/krzychu124/Cities-Skylines-Traffic-Manager-President-Edition to https://github.com/CitiesSkylinesMods/TMPE and this confuses Visual studio.
1.  Go to `team viewer (A or A2) -> Home (B) -> Settings (C)`
![Screenshot (1004)](https://user-images.githubusercontent.com/26344691/81140213-47fc1280-8f71-11ea-85cb-81d89568051e.png)
2.  click on repository settings
3.  under repository section edit origin (A). 
![Screenshot (1006)](https://user-images.githubusercontent.com/26344691/81140360-b50fa800-8f71-11ea-8761-5a6294b089ca.png)
4.  In the pop-up window make sure push matches fetch is ticked . copy past this URL (B) https://github.com/krzychu124/Cities-Skylines-Traffic-Manager-President-Edition then press save (C) 
5.  you MUST restart Visual studio for the changes to take place. clicking refresh or closing/opening solution is futile! Close visual studio and open the current repo again. 
6.  go to GitHub tab and make sure the error message is gone ![Screenshot (1007) - Copy](https://user-images.githubusercontent.com/26344691/81140697-010f1c80-8f73-11ea-8834-fcf6b6325e40.png)
