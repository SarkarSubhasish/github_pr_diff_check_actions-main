# Using this action

You would need to put this in a file in `.github/workflows`

```
name: "Check PR diff for line"
on: [pull_request]

jobs:
  pr_diff_check:
    runs-on: ubuntu-latest
    steps:
    - name: PR Diff check
      uses: <<path to this repo>>
      with:
        owner: ${{ github.repository_owner }}
        repo: ${{ github.event.repository.name }}
        pr_number: ${{ github.event.number }}
        github-token: ${{github.token}}
        check: 'Test'
```
