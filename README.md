[![Testspace](http://www.testspace.com/img/Testspace.png)](http://www.testspace.com)

## Getting Started with Testspace Standalone Projects.

The first step when getting started is to create your Testspace Organization. When you [sign into](https://www.testspace.com/pricing.html) Testspace to create your account, enter an `Organization Name` to be used as the subdomain for your Testspace URL.

```
   my-organization-name.testspace.com
```

### Creating your first Standalone Project and Space

After completing the new account process -- and every time you login thereafter -- you'll land on the Projects tab, the home view for your Testspace Organization.

On first time access, your Projects page will display the following.

![New Organization](images/new-org-projects-tab.png)

Select the `New Project` button to bring up the dialog below.

![New Project Dialog](images/new-project-dialog.png)

Provide a Project name and optional description - notification settings can be changed at anytime. 

Select `SUBMIT`, and then select the **project-name-link** for your new project to go to the `Spaces tab` which should look as follows.

![New Project Spaces Tab](images/new-project-spaces-tab.png)

Select the `New Space` button to bring up the dialog below.

![New Space Diaglg](images/new-space-dialog.png)

Provide a Space name and optional description and `SUBMIT`.

You're now ready to download the Testspace client to start pushing data

---
### Installing the Testspace Client

A [simple command line client](https://help.testspace.com/reference:client-reference) is used to push test results and other metrics to the Testpace server.

If installing on linux, you can use the following command (if $HOME/bin exists)
```
  curl -s https://testspace-client.s3.amazonaws.com/testspace-linux.tgz | tar -zxvf- -C $HOME/bin

```

If installing on Windows, there a serveral methods, depending on your tools available. Using `curl` or `wget`

```
  curl -o testspace-windows.zip https://testspace-client.s3.amazonaws.com/testspace-windows.zip
```
```
  wget --no-check-certificate -N https://testspace-client.s3.amazonaws.com/testspace-windows.zip
  
```
or from a Power Shell console
```
  Invoke-WebRequest https://testspace-client.s3.amazonaws.com/testspace-windows.zip -outfile testspace-windows.zip
```

After downloading and adding `$HOME/bin` to path if required, you can check the client installation by typing 
```
  testspace -v
  
Testspace, version 1.8.490
Copyright (C) 2017 S2 Technologies, Inc.  
```  
  
---
### Configuring your Testspace URL
The command to push test results to the server using the Testpace Client takes the following forms.  If pushing to a `Private Testpace Project`, you will need to provide your [access token] for credentials to access the Project. The token is obtained from your `User Settings` described [here](https://help.testspace.com/organization:users)
```
  testspace results.xml access-token@orgnization-name.testspace.com/project-name/space-name"
```
If pushing results to a `Public Testspace Project` access credentials are not required.
```
  testspace results.xml orgnization-name.testspace.com/project-name/space-name"
```
To simplify the command line for interactive use, you can set the default URL using the Testspace Clients' `config` command. For example you can set a partial default URL and then specify the Space name when pushing files.
```
  testspace config url organization-name.testspace.com/project-name
```
The command to push the same restuls.xml file after configuring the URL as above.
```
  tetsspace results.xml space-name
```

---
### Pushing Sample Data from this Repository

Once you've installed the Testspace client, and configured the Testspace URL as described above, there are a number of data files in this repository that can pushed from the console for trial and refence. 

  * results*.xml - three test result files in JUnit XML format
  * output.log - log file produced during build
  * analysis.xml - static analysis output
  * coverage.xml - code coverage analysis output
  * metrics.log - log file produced during test, with metrics to chart overtime
  * metrics.csv - comma separated values (CSV) file with the numeric values from the metrics.log file. 

#### Example 1. Pushing a Single Test Result File
The following example will push a single test result file to your new space.
```
  testspace results1.xml my-organization.testspace.com/my-first-space"
```
Once pushed successfully, you should be able to review the results from your new Space

#### Example 2. Pushing Multiple Test Results Files
The following example will aggregate and push all three test result files to your new space.
```
  testspace results*.xml my-organization.testspace.com/my-first-space"
```

#### Example 3. Pushing Log Files with Test Results
The following example will push the `output.log` file along with test result files to your new space.
```
  testspace results*.xml output.log my-organization.testspace.com/my-first-space"
```

#### Example 3. Pushing Static Analysis and Code Coverage with Test Results
The following example will push the `output.log` file along with test result files to your new space.
```
  testspace results*.xml output.log my-organization.testspace.com/my-first-space"
```
