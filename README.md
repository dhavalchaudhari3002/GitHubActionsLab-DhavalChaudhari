# GitHubActionsLab-DhavalChaudhari


The repository demonstrate two Github action workflaw designs to show dependendcy management and multi-platform CI/CD ability.
1:  purpose of each flow 

Dependent Jobs Workflow:  the purpose of this workflow is sequential execution. it can make sure that project is build first and secondt tested and once this two steps completed only then it is deployed suscessfully.

Multi-Platform Workflow: the purpose of this workflow is parellel execution across various environment. it test the code on ubantu , window and mcos to check cross-platform comparison.

2: Key Concepts Demonstrated

needs: used in dependent jobs workflow to create a hierarchy . 
runs-on: This machine defines that virtual machine is used for this job.
env: This allows for the defination of the environment that can be used on different step within a job.

3: Challenges & Resolutions
challenge: When pushing from the command line to GitHub, authentication errors occur.
  Solution: Since GitHub no longer allows password authentication for Git operations, the issue was fixed by using a Personal Access Token  in place of a traditional password.
challenge: controlling line ends while transferring files between the GitHub runners and Windows.
  solution: The conversion was handled automatically by Git, and the warnings were accepted as common cross-platform development standard.

challenge: starting multi-platform process.
  solution: Recognized that the workflow was set up to start when a pull request was made to the main branch, and that in order to view the outcomes, a proper PR had to be created on GitHub.
