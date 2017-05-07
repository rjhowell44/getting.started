[![Testspace](http://www.testspace.com/img/Testspace.png)](http://www.testspace.com)

## Getting Started with Testspace Standalone Projects.

The first step when getting started is to create your Testspace Organization. When you sign into Testspace to create your account, select and `Organization Name` to be used as the subdomain for your Testspace URL.

```
   my-organization-name.testspace.com
```

### Creating your first Standalone Project and Space

After completing the new account process -- and everytime you login thereafter -- you'll land on the Projects tab, the home view for your Testspace Organization.

On first time access, your Projects page will display the folloiwng.

![New Oraganization](images/new-org-projects-tab.png)

Select the `New Project` button to bring up the dialog below.

![New Project Dialog](images/new-project-dialog.png)

Provide a Project name and optional description - notification settings can be changed at anytime. 

Select `Submit`, and then select the name-link for your new project to go to the `Spaces tab` which should look as follows.

![New Project Spaces Tab](images/new-project-spaces-tab.png)

Select the `New Space` button to bring up the dialog below.

![New Space Diaglg](images/new-space-dialog.png)

Provide a Space name and option description and `Submit`.

You're ready to start pushing data

---



## Publishing sample for demonstrating Testspace 

Contains a set of simple files to show publishing test results, code coverage, and static analysis. 

***

Publishing **Test Content** using www.testspace.com.

[![Space Health](https://samples.testspace.com/spaces/833/badge)](https://samples.testspace.com/spaces/833 "Test Cases")
[![Space Metric](https://samples.testspace.com/spaces/833/metrics/833/badge)](https://samples.testspace.com/spaces/833/schema/Code%20Coverage "Code Coverage (lines)")
[![Space Metric](https://samples.testspace.com/spaces/833/metrics/834/badge)](https://samples.testspace.com/spaces/833/schema/Static%20Analysis "Static Analysis (issues)")


***

Push Content using **Testspace client**: 

<pre>
curl -s https://testspace-client.s3.amazonaws.com/testspace-linux.tgz | sudo tar -zxvf- -C /usr/local/bin
testspace @.testspace.txt $TESTSPACE_TOKEN/$GITHUB_ORG:$REPO_NAME/$BRANCH_NAME#$BUILD_NUMBER
</pre> 

Checkout the published [Test Content](https://samples.testspace.com/projects/testspace-samples:getting.started). Note that the `.testspace.txt` file contains the [set of files](http://help.testspace.com/how-to:publish-content#publishing-via-content-list-file) to publish. 

***

To replicate this sample: 
  - Setup account at www.testspace.com.
  - Create a Environment variable called `TESTSPACE_TOKEN`
     - `TESTSPACE_TOKEN` = `credentials@Your-Org-Name.testspace.com`
     - `credentials` set to `username:password` or your [access token](http://help.testspace.com/reference:client-reference#login-credentials)
     - To [use Testspace with a CI system](http://help.testspace.com/how-to:add-to-ci-workflow), store `TESTSPACE_TOKEN` as a secure environment variable
 
