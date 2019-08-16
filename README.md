# Sample-Cordova-Project

This has Cordova Version - 8.0.0
Android Cordova SDK version - 8.0.0

CT - Android Cordova SDK - https://github.com/CleverTap/clevertap-cordova

Force use following dependencies:

configurations.all {
  resolutionStrategy {
      force 'com.google.firebase:firebase-messaging:15.0.2'
      force 'com.google.android.gms:play-services-base:16.1.0'
  }
}

To use the above in build.gradle [Module:App], update Gradle SDK to a minimum of 5.1.1.

Following steps to update Gradle SDK:
1. In /android/app/build.gradle find this part of the code.

task wrapper(type: Wrapper) {
   gradleVersion = '5.1.1'
}

2. In GradleBuilder.js find this part of the code.
var distributionUrl = process.env['CORDOVA_ANDROID_GRADLE_DISTRIBUTION_URL'] || 'https\\://services.gradle.org/distributions/gradle-5.1.1-all.zip';

3. In StudioBuilder.js find this part of the code.

 var distributionUrl = process.env['CORDOVA_ANDROID_GRADLE_DISTRIBUTION_URL'] || 'https\\://services.gradle.org/distributions/gradle-5.1.1-all.zip';

If GradleBuilder.js/StudioBuilder.js not available change the same in <App Name>/platforms/android/cordova/lib/builders/ProjectBuilder.js

Then build via CLI.
