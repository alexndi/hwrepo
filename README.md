[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-c66648af7eb3fe8bc4f294546bfd86ef473780cde1dea487d3c4ff354943c9ae.svg)](https://classroom.github.com/online_ide?assignment_repo_id=9480380&assignment_repo_type=AssignmentRepo)
# github-actions-homework-4

## 1. Create an Action which reads a Readme file from remote repository and updates the current one based on the remote content.
"TEST"
## 2. Example:

```yaml

  - uses: myCustomAction
    with:
      remote-repo: bosch-ecs-career-camp/${my_previous_homework_repo}@main
      remote-file: README.md
      current-file: README.md

```
