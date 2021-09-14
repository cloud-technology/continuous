# GitLab CI template for Gradle

## Add Code Coverage Report

``` groovy
plugins {
  id 'jacoco'
}

jacocoTestReport {
  // tests are required to run before generating the report
  dependsOn test 
  reports {
    // sonar analysis equired
    xml.enabled true
    // print coverage
    csv.enabled true
    html.enabled true
  }
}
```


