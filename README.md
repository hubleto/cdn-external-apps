# Hubleto Cloud External Apps

This repository hosts the list of external apps that can be installed on accounts on the Hubleto Cloud.
If you are developing an app that you would like to use on Hubleto Cloud, follow the steps below to get
your app approved on Hubleto Cloud.

## Adding your own app to the repository
1. Before your app gets approved, you need to add our [Hubleto External Apps Manager](https://github.com/apps/hubleto-external-apps-manager) to your repository. Private repositories are supported as well.
2. Fork this repository and submit a pull request with the following changes:
   - Add your Github repository to the `repositories` array:
    ```json
    {
      "type": "vcs",
      "url": "https://github.com/INSTALLATION_ID/ORGANIZATION/REPOSITORY"
    }
    ```
   - Add your app to the `require` list:

    ```json
    "ORGANIZATION/APP-NAME": "1.0"
    ```
    > **Important!** Wildcards are forbidden in the package version. You must set it to an exact value.
3. Our team will then review your submitted app and approve or decline it.

## FAQ
1. **How do I determine the `INSTALLATION_ID`?**

    Go to the [Integration settings](https://github.com/settings/installations) of your Github account or the Github
    account of your organization. Click *Configure* on the Hubleto External Apps Manager. You should land on a website
    with the URL of the following form: `https://github.com/settings/installations/INSTALLATION_ID`
2. **The approved version of my app is already deprecated. What do I do?**
    
    To bump up the version of your Hubleto app, simply submit a new pull request.