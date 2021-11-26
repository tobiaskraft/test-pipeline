# Use sass-asset pipeline with grails 5

When trying to use sass in grails 5 by integrating the sass-asset pipeline
it is not compiling.


Steps to reproduce
* Download and install grails 5.0.1
* Add simple scss file *layout.scss* to folder *assets/stylesheets*
* Add sass-asset pipeline plugin to *build.gradle*
* Compile assets

      ./gradlew clean assetCompile --stacktrace


The following error is occurring:

    * Exception is:
    org.gradle.launcher.daemon.client.DaemonDisappearedException: Gradle build daemon disappeared unexpectedly (it may have been killed or may have crashed)
    at org.gradle.launcher.daemon.client.DaemonClient.handleDaemonDisappearance(DaemonClient.java:252)
    at org.gradle.launcher.daemon.client.DaemonClient.monitorBuild(DaemonClient.java:225)
    at org.gradle.launcher.daemon.client.DaemonClient.executeBuild(DaemonClient.java:187)
    ......

It seems that it is a compatibility problem with the gradle version. 