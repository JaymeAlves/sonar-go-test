# SonarQube lab

The objective of this repo is just a lab to learn more about SonarQube and code coverage.

# Cloud scenario v2

## Setting sonar cloud

To enable testing in a cloud scenario, it was necessary to create a CI YAML file using GitHub Actions, which was placed in the .github/workflows folder. The selected service for conducting the checks was SonarCloud.io. With some minor adjustments in the sonar-project.properties file, the checks could be managed by the pipeline.

<img src="/assets/img/sonar_cloud.PNG">

Something that caught my attention was the fact that when I tried to merge the new code with the 'develop' branch, the SonarQube checks didn't allow the pull request to proceed with the merge.

<img src="/assets/img/github_pr.PNG">

# Local scenario v1

## Set SonarQube Localy

SonarQube was set with docker image, with the bellow command:

```
docker run -d --name sonarqube -e SONAR_ES_BOOTSTRAP_CHECKS_DISABLE=true -p 9000:9000 sonarqube:latest
```

<img src="/assets/img/docker.PNG">

## The result

The image below illustrates that the code coverage is at 25%.

<img src="/assets/img/sonar screen.PNG">