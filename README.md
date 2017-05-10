[![Testspace](http://www.testspace.com/img/Testspace.png)](http://www.testspace.com)

## Getting Started with Testspace Standalone Projects.
This GitHub repository contains a sample of Test results and other metric files, with information (below) on pushing the files to a new Standalone Project and Space. Please refer to [Getting Started with Testspace Standalone Projects](https://help.testspace.com/getting-started:standalone-projects) in our help guide to create your first project for this example. 

---
### Configuring your Testspace URL
You will need to provide your **access token** for credentials to push data to your Private Projects and Spaces. The token is obtained from your `User Settings` described [here](https://help.testspace.com/organization:users). The command to push test results to the server using the Testpace Client takes the following form. 
```
  testspace results.xml access-token@orgnization-name.testspace.com/project-name/space-name
```

To simplify the command line for interactive use, you can set the default URL using the Testspace Clients' `config` command. For example you can set a partial default URL and then specify the Project and Space names when pushing files on the command line.
```
  testspace config url  access-token@organization-name.testspace.com
```
The command to push the same restuls.xml file after configuring the URL as above.
```
  testspace results.xml project-name/space-name
```

---
### Pushing Sample Data from this Repository

Once you've [downloaded](https://help.testspace.com/reference:client-download) the Testspace client, and configured the Testspace URL as described above, there are a number of data files in this repository that can pushed from the console for trial and refence. 

  * **results[n].xml** - three test result files in JUnit XML format.
  * **output.log** - log file produced during build.
  * **analysis.xml** - static analysis output.
  * **coverage.xml** - code coverage analysis output.
  * **metrics.log** - log file produced during test, with metrics to chart over successive result sets.
  * **metrics.csv** - comma separated values (CSV) file with the numeric values from the metrics.log file. 

#### Example 1. Pushing a Single Test Result File
The following example will push a single test result file to your new space.
```
  testspace results1.xml my-first-project/my-first-space
```
Once pushed successfully, you should be able to review the results from your new Space

#### Example 2. Pushing Multiple Test Results Files
The following example will aggregate and push all three test result files to your new Space.
```
  testspace results*.xml my-first-project/my-first-space
```

#### Example 3. Pushing Log Files with Test Results
The following example will push the `output.log` file along with test result files to your new Space.
```
  testspace results*.xml output.log my-first-project/my-first-space
```

#### Example 4. Add in the Static Analysis and Code Coverage files
The following example will push the `output.log` file along with test result files to your new Space.
```
  testspace results*.xml output.log analysis.xml coverage.xml my-first-project/my-first-space
```

#### Example 4. Finally, add in the custom metrics to push all files in the repo
The following example will push the `output.log` file along with test result files to your new Space.
```
  testspace results*.xml output.log analysis.xml coverage.xml metrics.log{metrics.csv} my-first-project/my-first-space
```

---
### Next Steps? ###

  * More on [How to Push Data](https://help.testspace.com/how-to:push-data) - how to organize results, how to push results incrementally, include GIT source code changes, and other specifics.
  * [Inivite Other Users](https://help.testspace.com/how-to:invite-other-users) - invite others from your team to join your Testspace Project.
  * [Manage Health Status](https://help.testspace.com/how-to:manage-health-status) - manage test failures, and set metric criteria and thresholds. 

 
  