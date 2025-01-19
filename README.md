# pulse.sbs
Pulse project repository


We added the SurveyJS PHP repository as a Git submodule, with the following command:
```
git submodule add https://github.com/surveyjs/surveyjs-php.git survey
This command cloned the SurveyJS PHP repository into a folder named survey within the current project directory.
```
## Add the external projects Survey & DeepSeek as a submodule

To add the external project as a submodule, use the following command:
```
git submodule add https://github.com/deepseek-ai/DeepSeek-V3.git path/to/external/project
```
Replace path/to/external/project with the directory where you want the external repository to be stored in your project. If you don’t specify a path, it will default to the repository name (DeepSeek-V3).
3. Initialize and update the submodule

Once you've added the submodule, you need to initialize it and update it to fetch the latest files from the remote repository:
```
git submodule update --init --recursive
```
4. Commit the submodule change

Now that you've added the submodule, you need to commit this change to your repository. Git will treat the submodule as a reference to a specific commit in the external repository.
```
git add .gitmodules path/to/external/project
git commit -m "Add DeepSeek-V3 as a submodule"
```
5. Push your changes to your remote repository.
```
git push
```
6. To update the submodule

When you want to pull updates from the external project, you can navigate to the submodule directory and use the following commands:
```
cd deepseek
git fetch
git pull origin main  # Or the appropriate branch
```
Then, go back to your main project directory and commit the changes:

cd /path/to/your/git/project
git add path/to/external/project
git commit -m "Update submodule to latest commit"
git push

This process allows you to integrate an external Git repository into your own project and keep it up-to-date.
