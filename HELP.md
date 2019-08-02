# 🆘 CodeReady Workspaces for Enablment 🆘 HELP FOR THE NEEDY 🆘

Temporary help guide whilst we settle in CRW to enablement.

## Common Errors
> _Provide some guidance for current common issues encountered with CRW and Enablment_
____

### Error Starting Workspace

Users browse to the `factory` URL and see the `not a valid zip` error on starting workspace

![not-a-valid-zip](images/not-a-valid-zip.png)

- Likely root causes is upstream resolution here - https://github.com/eclipse/che/issues/12762#issuecomment-467797130

<p class="tip">
<b>FIX</b> - Not fatal, the users workspace has been created.

- fix is to just get the user to manually start there created workspace
- browse to dashboard as the user https://codeready-workspaces.apps.<DOMAIN_FOR_YOUR_CLASS>/dashboard
- `Start` the workspace `Actions > triangle start`
</p>

![not-a-valid-zip-fix](images/not-a-valid-zip-fix.png)

____

### I Have Lost the Magic Factory Link!

Users are badgering you for the magic link to create the cloud IDE and the SRE is on a coffee break. From `Excercise.1`

```
https://codeready-workspaces.apps.<DOMAIN_FOR_YOUR_CLASS>/dashboard/#/load-factory?name=DO500%20Template&user=admin
```
<p class="tip">
<b>NOTE</b> - Complete URL should be replaced with the one you've been provided by the instructor.
</p>

<p class="tip">
<b>FIX</b> - Not fatal, use the force. The `factory` is only available to the `admin` user in CRW - hende the `&user=admin` bit on the end of the link.

- Login to dashboard URL (https://codeready-workspaces.apps.<DOMAIN_FOR_YOUR_CLASS>/dashboard) using the admin user (in keycloak/SSO) which is deployed to the CRW namespace
- Browse to `Factories > DO500 Template`
</p>

![admin-login-crw](images/admin-login-crw.png)
![factory-link](images/factory-link.png)

Longer term we should fix up the admin user creds as well ! - https://github.com/rht-labs/enablement-codereadyworkspaces/issues/17

____

### Multiple workspaces created by users

Not strictly a bug, more a feature, but due to the error starting a workspace, the frantic user has started smashing the Reload button in their browser. Each invocation of the factory link, creates a new workspace - which could make for some fun resource hogging.

<p class="tip">
<b>FIX</b> - Not fatal unless your cluster runs out of resources 🤠

- Ask the users to stop or delete not/in-use workspaces
- browse to dashboard as the user https://codeready-workspaces.apps.<DOMAIN_FOR_YOUR_CLASS>/dashboard
- `Stop` the workspaces not in use `Actions > square stop`
</p>

Longer term we should limit these - https://github.com/rht-labs/enablement-codereadyworkspaces/issues/18

____

### Who do i call in an emergency?

- 📴 a.team 📴 b.mak 📴