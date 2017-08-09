# Android Runner 1.0.0 Issue

When using AndroidJUnitRunner 1.0.0 with Wiremock or AssertJ the following error is shown:
`com.android.builder.testing.ConnectedDevice > No tests found`

Reverting back to AndroidJUnitRunner 0.5 will allow the test to be detected and run.

## Using AndroidJUnitRunner 1.0.0

Open the `build.gradle` and ensure that the 1.0.0 version is uncommented and that the 0.5 version is commented out.
Like so:

```groovy
androidTestCompile 'com.android.support.test:runner:1.0.0'
//androidTestCompile 'com.android.support.test:runner:0.5'
```

To run the test and see the failure execute the following command:

```
./gradlew
```

## Using AndroidJUnitRunner 0.5

Open the `build.gradle` and ensure that the 0.5 version is commented and that the 0.5 version is uncommented.
Like so:

```groovy
//androidTestCompile 'com.android.support.test:runner:1.0.0'
androidTestCompile 'com.android.support.test:runner:0.5'
```

To run the test and see it pass execute the following command:

```
./gradlew
```