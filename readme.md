#### Building

In the root dir:

- `$ mvn package`

```
[INFO] Reactor Summary:
[INFO] 
[INFO] TestKit ........................................... SUCCESS [0.002s]
[INFO] Google Instrumentation TestRunner ................. SUCCESS [3.852s]
[INFO] Google Instrumentation TestRunner-Runtime ......... SUCCESS [0.516s]
[INFO] Espresso Parent Project ........................... SUCCESS [0.000s]
[INFO] Espresso Testing Framework ........................ SUCCESS [4.954s]
[INFO] Test App For Espresso ............................. SUCCESS [22.667s]
[INFO] Tests For the Espresso Test Framework ............. SUCCESS [22.575s]
```

#### Running the tests

Install the test app

- `adb install ./testapp/target/testapp.apk`

Install the test apk

- `adb install ./espresso/libtests/target/espresso-tests.apk`

Run the tests

- `adb shell am instrument -w com.google.android.apps.common.testing.ui.espresso.tests/com.google.android.apps.common.testing.testrunner.GoogleInstrumentationTestRunner`

Android Studio [testing docs](http://tools.android.com/tech-docs/new-build-system/user-guide#TOC-Testing). Instrumentation tests are built using `gradle assembleTest`