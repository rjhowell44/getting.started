[![Testspace](http://www.testspace.com/public/img/testspace_logo.png)](http://www.testspace.com)

***

## Publishing sample for demonstrating Testspace 


Contains a set of simple files to show publishing test results, code coverage, and static analysis. 

***
[![Space Health](https://samples.testspace.com/projects/87/spaces/459/badge)](https://samples.testspace.com/projects/87/spaces/459 "Test Cases")
[![Space Metric](https://samples.testspace.com/projects/87/spaces/459/metrics/320/badge)](https://samples.testspace.com/spaces/459/schema/Code%20Coverage "Code Coverage (lines)")
[![Space Metric](https://samples.testspace.com/projects/87/spaces/459/metrics/321/badge)](https://samples.testspace.com/spaces/459/schema/Static%20Analysis "Static Analysis (issues)")


***


<pre>
curl -s https://testspace-client.s3.amazonaws.com/testspace-linux.tgz | sudo tar -zxvf- -C /usr/local/bin
testspace analysis.xml [tests]*test.xml coverage.xml "my-space"
</pre>

Checkout the [Space](https://samples.testspace.com/projects/getting.started). Refer to this [article](http://help.testspace.com/getting-started:publish-some-results) for more information on publishing results. 

***


To replicate this sample: 
  - Account at www.testspace.com.
  - CI Environment Variable called **TESTSPACE_TOKEN** required:
    -  `TESTSPACE_TOKEN` = `credentials@my-org-name.testspace.com/my-project`
    - `credentials` set to `username:password` or your [access token](http://help.testspace.com/using-your-organization:user-settings).
    - `my-org-name.testspace.com/my-project` based on your *subdomain* and *project* names. Refer [here](http://help.testspace.com/reference:runner-reference#login-credentials) for more details. 
    

