# pulse.sbs Survey 

A Pulse survey project repository

## Architecture
survey.pulse.sbs SurveyJS components with a PHP backend.

## Git problem solving

 trying to commit changes, but Git is indicating that there are uncommitted changes in the surveyjs-php submodule. Here's the issue breakdown and how to resolve it:

Explanation:
Submodule Changes: Git is telling you that the surveyjs-php submodule has modified content but those changes have not been staged for commit.
Submodule Commit: When working with submodules, you must first commit any changes inside the submodule itself before you can commit the changes in the main repository.
Steps to resolve:
Enter the submodule directory: Navigate to the submodule directory to commit changes there.

bash
Copy code
cd surveyjs-php
Check for changes in the submodule: Run the following command inside the submodule to see the status of changes:

bash
Copy code
git status
Stage and commit changes inside the submodule: If there are changes, you will need to stage and commit them in the submodule.

bash
Copy code
git add .
git commit -m "Updated surveyjs-php"
Return to the main project: Once the submodule changes are committed, return to the root of your main repository:

bash
Copy code
cd ..
Stage the submodule update in the main repository: Now that the submodule has been updated, Git needs to track the change to the submodule reference.

bash
Copy code
git add surveyjs-php
Commit your changes in the main repository: Finally, you can commit the changes in your main repository, including the update to the submodule reference.

bash
Copy code
git commit -m "Updated surveyjs-php submodule"
Push the changes (if needed): If you need to push the changes to a remote repository, run:

bash
Copy code
git push origin feature/pulse-survey-feature
Summary:
You need to commit the changes within the submodule (surveyjs-php) first.
Then, update the main repository with the reference to the submodule change.