# gradle-gretty-jacoco-issue

$ ./gradlew clean appRun
:clean
:prepareInplaceWebAppFolder UP-TO-DATE
:createInplaceWebAppFolder
:compileJava
:processResources UP-TO-DATE
:classes
:prepareInplaceWebAppClasses
:prepareInplaceWebApp
:appRun FAILED

FAILURE: Build failed with an exception.

* What went wrong:
Execution failed for task ':appRun'.
> java.lang.NullPointerException (no error message)

* Try:
Run with --stacktrace option to get the stack trace. Run with --info or --debug option to get more log output.

BUILD FAILED

Total time: 0.935 secs

Relevant stacktrace:
Caused by: java.lang.NullPointerException
        at org.gradle.testing.jacoco.plugins.JacocoPluginExtension.applyTo(JacocoPluginExtension.java:104)
        at org.gradle.testing.jacoco.plugins.JacocoPluginExtension$applyTo.call(Unknown Source)
        at org.akhikhl.gretty.JacocoHelper.<init>(JacocoHelper.groovy:34)
        at org.akhikhl.gretty.StartBaseTask.getJacoco(StartBaseTask.groovy:132)
        at org.akhikhl.gretty.AppStartTask_Decorated.getJacoco(Unknown Source)
        at org.akhikhl.gretty.StartBaseTask.doPrepareServerConfig(StartBaseTask.groovy:96)
        at org.akhikhl.gretty.AppStartTask.getStartConfig(AppStartTask.groovy:53)
        at org.akhikhl.gretty.AppStartTask_Decorated.getStartConfig(Unknown Source)
        at org.akhikhl.gretty.StartBaseTask.getLauncherConfig(StartBaseTask.groovy:141)
        at org.akhikhl.gretty.StartBaseTask.action(StartBaseTask.groovy:39)
        at org.gradle.internal.reflect.JavaMethod.invoke(JavaMethod.java:73)
