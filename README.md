[![Testspace](http://www.testspace.com/public/img/testspace_logo.png)](http://www.testspace.com)

***

## Publishing sample for demonstrating Testspace 


Contains a set of simple files to show publishing test results, code coverage, and a log file.

***
[![Space Health](https://samples.testspace.com/projects/87/spaces/292/badge)](https://samples.testspace.com/projects/87/spaces/292 "Test Cases")
[![Space Metric](https://samples.testspace.com/projects/87/spaces/292/metrics/187/badge)](https://samples.testspace.com/projects/87/spaces/292/metrics#metric-187 "Line/Statement Coverage")

***


<pre>
testspace publish [MyTests]TEST*.xml coverage.xml "@log.txt{this is my test log}" ${TESTSPACE_URL}
</pre>

Checkout the [Space](https://samples.testspace.com/projects/getting.started/spaces/my-results). Refer to this [article](http://help.testspace.com/getting-started:publish-results) for more information on publishing results. 

***

To fork this example using Travis requires:
  - Account at www.testspace.com.
  - Travis Environment Variable: 
    - `TESTSPACE_URL` = `token:@my-org-name.testspace.com/my-project/my-space`
    - `token` set to the `value` defined as your [Access token](http://help.testspace.com/using-your-organization:user-settings).
    - `my-org-name.testspace.com/my-project/my-space` based on your subdomain, project, and space names. Refer [here](http://help.testspace.com/reference:runner-reference#config) for more details. 
    