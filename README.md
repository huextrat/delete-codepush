# Delete CodePush

This action delete a [CodePush](https://learn.microsoft.com/en-us/appcenter/distribution/codepush/) deployment track using the AppCenter CLI.

You will need a `Full Access` [API token](https://learn.microsoft.com/en-us/appcenter/api-docs/#creating-an-app-center-user-api-token) from AppCenter.

> - To deploy a new CodePush, please use [huextrat/deploy-codepush](https://github.com/marketplace/actions/deploy-codepush)

# Usage

<!-- start usage -->
```yaml
- uses: huextrat/delete-codepush@v1
  with:
    # Required, as the AppCenter CLI requires authentication
    # Make it secure, using GitHub secrets for instance
    # Example: ${{ secrets.APPCENTER_API_TOKEN }}
    token: ''

    # Required, as the AppCenter CLI requires an app name
    # Format: <ownerName>/<appName>
    # Example: huextrat/MyApp
    app: ''

    # Deployment track you want to delete
    deploymentTrack: ''
```
<!-- end usage -->

## Scenario

- AppCenter Android app name is: `huextrat/MyApp-Android`
- AppCenter iOS app name is: `huextrat/MyApp-iOS`

### Example

#### Android
```yaml
- uses: huextrat/delete-codepush@v1
  with:
    token: ${{ secrets.APP_CENTER_API_KEY }}
    app: "huextrat/MyApp-Android"
    deploymentTrack: "Staging"
```

#### iOS
```yaml
- uses: huextrat/delete-codepush@v1
  with:
    token: ${{ secrets.APP_CENTER_API_KEY }}
    app: "huextrat/MyApp-iOS"
    deploymentTrack: "Staging"
```
