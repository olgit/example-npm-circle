# Black Duck CoPilot npm/Circle CI Example

[![CircleCI](https://circleci.com/gh/BlackDuckCoPilot/example-npm-circle.svg?style=svg)](https://circleci.com/gh/BlackDuckCoPilot/example-npm-circle) [![Black Duck Security Risk](https://copilot.blackducksoftware.com/github/repos/BlackDuckCoPilot/example-npm-circle/branches/test/badge-risk.svg)](https://copilot.blackducksoftware.com/github/repos/BlackDuckCoPilot/example-npm-circle/branches/test)

Shows a working setup for using Black Duck CoPilot to analyze the risk of project dependencies

## Circle CI Setup
The `circle.yml` file has been modified to upload generated dependency data to CoPilot:

```yaml
test:
  post:
    - bash <(curl -s https://copilot.blackducksoftware.com/ci/circle/scripts/upload)
```
