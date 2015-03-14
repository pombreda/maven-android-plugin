# Changelog #

The up to date changelog is now located at

---

https://github.com/simpligility/android-maven-plugin/blob/master/src/site/asciidoc/changelog.adoc

---


Any **text in bold** below describes changes, which may cause existing builds to break. You may need to **update / clean up your project configuration**. This should only happen during alphas, and between major versions. From time to time, upgrading Google's Android SDK and NDK may also be necessary.

### Android Maven Plugin 4.0.0-rc.3 and newer - 2014-10-28 and onwards ###

**Please check out the new changelog document at https://github.com/simpligility/android-maven-plugin/blob/master/src/site/asciidoc/changelog.adoc for the latest releases.**

### Android Maven Plugin 4.0.0-rc.2 - 2014-10-25 ###

The rc.1 is version close. We want to limit the changes to

  * migration of ignore tests to Takari Plugin testing (see https://www.youtube.com/watch?v=PkLUgUyx8Kc for more tips) - details also at https://github.com/jayway/maven-android-plugin/issues/452
  * support for NDK [r10](https://code.google.com/p/maven-android-plugin/source/detail?r=10) ideally - see https://github.com/jayway/maven-android-plugin/issues/431
  * confirm all applications from samples work
  * anything else that comes up as urgent

Changes:

  * Lint integration tests
    * see https://github.com/jayway/maven-android-plugin/pull/456
    * contributed by Benoit Billington https://github.com/Shusshu
    * and Manfred Moser http://www.simpligility.com
  * Updated NDK support to [r10](https://code.google.com/p/maven-android-plugin/source/detail?r=10)
    * see https://github.com/jayway/maven-android-plugin/pull/455
    * see https://github.com/jayway/maven-android-plugin-samples/pull/63
    * fixed https://github.com/jayway/maven-android-plugin/issues/431
    * see https://github.com/jayway/maven-android-plugin/pull/471
    * contributed by Malachi de AElfweald https://github.com/malachid
    * and Manfred Moser http://www.simpligility.com
  * Migrated samples project to IT tests within the plugin itself.
    * https://github.com/jayway/maven-android-plugin/pull/461
    * contributed Manfred Moser http://www.simpligility.com
  * Fixes to AndroidManifest update
    * see https://github.com/jayway/maven-android-plugin/pull/457
    * fixes https://github.com/jayway/maven-android-plugin/issues/449
    * contributed by Benoit Billington https://github.com/Shusshu
  * Fixed error message typo
    * https://github.com/jayway/maven-android-plugin/pull/465
    * contributed by Lukasz Gawin https://github.com/lgawin
  * Ported scala example to IT test
    * https://github.com/jayway/maven-android-plugin/pull/467
    * https://github.com/jayway/maven-android-plugin-samples/commit/116e96534123246d6bdbfb564b9ed8b3c9b3b9e3
    * contributed by Manfred Moser http://www.simpligility.com
  * Ported support4demos, apidemos and tictactoe examples to IT test
    * https://github.com/jayway/maven-android-plugin/pull/469
    * https://github.com/jayway/maven-android-plugin-samples/commit/2fd2aab3bc9458ce7126edde01634e7c9a03c83f
    * contributed by Manfred Moser http://www.simpligility.com
  * Updates to the Travis CI setup
    * see https://github.com/jayway/maven-android-plugin/pull/468
    * see https://github.com/jayway/maven-android-plugin/commit/16b10af8ec00c8fe58aec9f5612bce1630a5844b
    * see https://github.com/jayway/maven-android-plugin/pull/472
    * see https://github.com/jayway/maven-android-plugin/commit/ac617bb3c537a3145b96b75221ac396399c9c4cc
    * contributed by Malachi de AElfweald https://github.com/malachid
    * and Manfred Moser http://www.simpligility.com
  * Change some properties to be injected to ensure that final versions are used (evaluated) and not mere pom file values
    * https://github.com/jayway/maven-android-plugin/pull/460
    * fixes https://github.com/jayway/maven-android-plugin/issues/458
    * see https://github.com/jayway/maven-android-plugin/pull/466
    * see https://github.com/jayway/maven-android-plugin/pull/473
    * contributed by Csaba Kozák https://github.com/WonderCsabo
  * Various NDK related fixes
    * contributed by Johan Lindquist https://github.com/johanlindquist




### Android Maven Plugin 4.0.0-rc.1 - released 2014-09-18 ###

  * Removed redundant, duplicate apk undeployment
    * see https://github.com/jayway/maven-android-plugin/pull/414/
    * contributed by Sebastian Gröbler https://github.com/SierraGolf
  * Display warning when pulling in jars from a libs folder in AAR or APKLIB
    * see https://github.com/jayway/maven-android-plugin/pull/422/
    * contributed by William Ferguson https://github.com/william-ferguson-au
  * Include jars in libs folder of AAR package, if found
    * see https://github.com/jayway/maven-android-plugin/pull/426/
    * contributed by William Ferguson https://github.com/william-ferguson-au
  * Removing duplicate aar jars for Proguard
    * see https://github.com/jayway/maven-android-plugin/pull/435
    * see https://github.com/jayway/maven-android-plugin-samples/pull/62
    * contributed by William Ferguson https://github.com/william-ferguson-au
  * Avoid adding aar dependency resources to Maven resources path
    * see https://github.com/jayway/maven-android-plugin/pull/436
    * contributed by William Ferguson https://github.com/william-ferguson-au
  * Resolve missing BuildConfig from APKLIB->APKLIB dependency
    * see https://github.com/jayway/maven-android-plugin/pull/438
    * fixes https://github.com/jayway/maven-android-plugin/issues/434
    * contributed by Marting M Reed https://github.com/MartinMReed
  * Change default project structure to Gradle structure since it is much more like a real Maven project anyway
    * see https://github.com/jayway/maven-android-plugin/pull/416
    * see https://github.com/jayway/maven-android-plugin/pull/441
    * contributed by William Ferguson https://github.com/william-ferguson-au
    * all sample updates contributed by Manfred Moser http://www.simpligility.com
  * Fix for using build output directory when needed (for unpack libraries in this case)
    * see https://github.com/jayway/maven-android-plugin/pull/440
    * fixes https://github.com/jayway/maven-android-plugin/issues/439
    * contributed by Thierry Carels https://github.com/carthx
  * Multi dex support fixes
    * see https://github.com/jayway/maven-android-plugin/pull/425
    * see https://github.com/jayway/maven-android-plugin/pull/444
    * contributed by Łukasz Suski https://github.com/lsuski
    * and Manfred Moser http://www.simpligility.com
  * Produce a warning for aar projects with apklib dependencies
    * see https://github.com/jayway/maven-android-plugin/pull/429
    * contributed by Leonid https://github.com/greek1979
  * Usage of animalsniffer plugin to ensure Java 6 support
    * see https://github.com/jayway/maven-android-plugin/pull/446
    * contributed by William Ferguson https://github.com/william-ferguson-au
    * and Manfred Moser http://www.simpligility.com
  * Added global parameters to configure if jars from libs folder in aar and apklib should be pulled in
    * includeLibsJarsFromAar and includeLibsJarsFromApklib both default to false
    * see https://github.com/jayway/maven-android-plugin/pull/445
    * contributed by Benoit Billington https://github.com/Shusshu
    * and Manfred Moser http://www.simpligility.com
  * Adding option to pass custom command line parameters to dx
    * see https://github.com/jayway/maven-android-plugin/pull/450
    * contributed by Łukasz Suski https://github.com/lsuski
  * updated Android SDK libraries
    * see https://github.com/jayway/maven-android-plugin/commit/3b498899a14c98df6bf2ddb4a49cb47daf160a59
    * contributed Manfred Moser http://www.simpligility.com
  * Introduced integration test using Takari plugin testing
    * see https://github.com/jayway/maven-android-plugin/issues/452
    * contributed Manfred Moser http://www.simpligility.com
    * see also https://www.youtube.com/watch?v=PkLUgUyx8Kc
  * Fix path to zipalign
    * see https://github.com/jayway/maven-android-plugin/pull/453
    * fixes https://github.com/jayway/maven-android-plugin/issues/399
    * contributed by Benoit Billington https://github.com/Shusshu

### Android Maven Plugin 3.9.0-rc.3 - released 2014-07-24 ###

  * Improved error message when build tools of SDK are missing
    * see https://github.com/jayway/maven-android-plugin/pull/381
    * fixes https://code.google.com/p/maven-android-plugin/issues/detail?id=397
    * fixes https://code.google.com/p/maven-android-plugin/issues/detail?id=432
    * contributed by Lorenzo Dematté https://github.com/ldematte
  * Cleaned up NDK support behaviour and implementation
    * see https://github.com/jayway/maven-android-plugin/pull/384
    * fixes https://github.com/jayway/maven-android-plugin/issues/360
    * contributed by William Ferguson https://github.com/william-ferguson-au
  * Fixed support for genDirectory config with aar artifacts
    * https://github.com/jayway/maven-android-plugin/pull/390
    * fixes https://github.com/jayway/maven-android-plugin/issues/389
    * contributed by William Ferguson https://github.com/william-ferguson-au
  * Adding support for multi dex
    * see  https://github.com/jayway/maven-android-plugin/pull/393
    * fixes https://github.com/jayway/maven-android-plugin/issues/356
    * contributed by Kevin Griffin https://github.com/m00sey
  * support waiting for full boot of devices and adaptations for travis setup
    * see https://github.com/jayway/maven-android-plugin/pull/396
    * contributed by Samuel Oggier https://github.com/soggier
  * Improved resolving of transitive dependencies and resources
    * see https://github.com/jayway/maven-android-plugin/pull/391
    * see https://github.com/jayway/maven-android-plugin-samples/pull/61
    * contributed by William Ferguson https://github.com/william-ferguson-au
  * Migration to Maven plugin annotations rather than javadoc
    * see https://github.com/jayway/maven-android-plugin/pull/391
    * see https://github.com/jayway/maven-android-plugin/pull/412
    * contributed by William Ferguson https://github.com/william-ferguson-au
    * and Manfred Moser http://www.simpligility.com
  * Support for "jni" folder for AAR with native components
    * see https://github.com/jayway/maven-android-plugin/pull/404
    * contributed by Lenoid https://github.com/greek1979
  * Improved handling and creation of BuildConfig in scenarios with transitive dependencies
    * see https://github.com/jayway/maven-android-plugin/pull/403
    * contributed by Lenoid https://github.com/greek1979
  * support for Jar files in libs folder in aar or apklib
    * see https://github.com/jayway/maven-android-plugin/pull/392
    * contributed by Shouqun https://github.com/Shouqun
  * Avoid compression of already compressed assets (e.g. mp3 files)
    * see https://github.com/jayway/maven-android-plugin/pull/409
    * contributed by Jaroslav Tulach https://github.com/jtulach
  * Avoid modifying classpath for non-Android projects
    * see https://github.com/jayway/maven-android-plugin/pull/413
    * contributed by Lenoid https://github.com/greek1979
    * and Manfred Moser http://www.simpligility.com


### Android Maven Plugin 3.9.0-rc.2 - released 2014-05-27 ###

  * Path issues fix for proguard mojo usage on Windows
    * see https://github.com/jayway/maven-android-plugin/pull/296
    * contributed by https://github.com/mmadev
  * Removed duplicate dependencies in native sample projects
    * https://github.com/jayway/maven-android-plugin-samples/pull/52
    * contributed by William Ferguson https://github.com/william-ferguson-au
  * Changed from direct Aether usage to Dependency Tree usage allowing compatibility with Maven 3.0.x and therefore with IDE's and other tools that have old Maven version like this embedded
    * https://github.com/jayway/maven-android-plugin/pull/305
    * https://github.com/jayway/maven-android-plugin/pull/311
    * https://github.com/jayway/maven-android-plugin/pull/312
    * contributed by William Ferguson https://github.com/william-ferguson-au
  * Allow to specify the number of threads used in device operations to avoid issues with lots of attached devices
    * https://github.com/jayway/maven-android-plugin/pull/304
    * contributed by Roy Clarkson https://github.com/royclarkson from Pivotal http://www.gopivotal.com/
  * New goals to connect and disconnect devices specified by IP number for all device interactions
    * https://github.com/jayway/maven-android-plugin/pull/306
    * contributed by Emmanuel Demey https://github.com/Gillespie59
  * Log message fix
    * https://github.com/jayway/maven-android-plugin/pull/307/
    * contributed by Clément Plantier
  * Avoid attempt to include R.txt in AAR if it doesnt exist
    * fixes [issue 452](https://code.google.com/p/maven-android-plugin/issues/detail?id=452)
    * see https://github.com/jayway/maven-android-plugin/pull/308
    * contributed by William Ferguson https://github.com/william-ferguson-au
  * Remove META-INF from AAR
    * see https://github.com/jayway/maven-android-plugin/pull/310
    * contributed by Benoit Billington https://github.com/Shusshu
  * include groupId in native artifact resolution
    * fixes [issue 444](https://code.google.com/p/maven-android-plugin/issues/detail?id=444)
    * https://github.com/jayway/maven-android-plugin/pull/313
    * contributed by Malachi de AElfweald https://github.com/malachid
  * transitive dependencies not dependent on existence of local natives dir
    * fixes [issue 429](https://code.google.com/p/maven-android-plugin/issues/detail?id=429)
    * https://github.com/jayway/maven-android-plugin/pull/314
    * contributed by Malachi de AElfweald https://github.com/malachid
  * Check for duplicate package name in android artifacts and produce warnings
    * https://github.com/jayway/maven-android-plugin/pull/321
    * https://github.com/jayway/maven-android-plugin/pull/336
    * contributed by Oleg Green https://github.com/marchelo
  * Fixed logging level for AIDL files in GenerateSourcesMojo
    * https://github.com/jayway/maven-android-plugin/pull/323
    * contributed by Oleg Green https://github.com/marchelo
  * Improved handling of transitive native dependencies
    * fixes [issue 424](https://code.google.com/p/maven-android-plugin/issues/detail?id=424)
    * https://github.com/jayway/maven-android-plugin/pull/319
    * contributed by Malachi de AElfweald https://github.com/malachid
  * Refactored usage of maven-plugin-plugin annotations to remove usage of deprecated expression
    * see https://github.com/jayway/maven-android-plugin/pull/331
    * contributed by Manfred Moser http://www.simpligility.com
  * Verbose output from aapt tool when Maven plugin config set to debug logging
    * see https://github.com/jayway/maven-android-plugin/pull/320
    * contributed by Oleg Green https://github.com/marchelo
  * Added support for configuring adb connection timeout
    * https://github.com/jayway/maven-android-plugin/pull/324/
    * contributed by Sebastian Gröbler https://github.com/SierraGolf
  * Improve AndroidManifest update to work with non-ascii characters
    * see https://github.com/jayway/maven-android-plugin/pull/322
    * contributed by xiaojian cai https://github.com/mccxj
  * Include BuildConfig class in aar
    * https://github.com/jayway/maven-android-plugin/pull/328
    * https://github.com/jayway/maven-android-plugin/pull/329
    * contributed by Benoit Billington https://github.com/Shusshu
  * Preserve order of dependencies for native dependency resolution
    * see https://github.com/jayway/maven-android-plugin/pull/330
    * contributed by Johan Lindquist https://github.com/johanlindquist
  * Adapted Travis build config to new SDK setup/distribution
    * see https://github.com/jayway/maven-android-plugin/pull/332
    * see https://github.com/jayway/maven-android-plugin/pull/333
    * see https://github.com/jayway/maven-android-plugin/pull/335
    * see https://github.com/jayway/maven-android-plugin/pull/346
    * see https://github.com/jayway/maven-android-plugin-samples/pull/54
    * see https://github.com/jayway/maven-android-plugin-samples/commit/ec856a5f18274b7de2cb036ce6fb1de167a88ac4
    * contributed by Malachi de AElfweald https://github.com/malachid
    * and Manfred Moser
  * Removed hardcoded debuggable setting from examples
    * see https://github.com/jayway/maven-android-plugin-samples/pull/53
    * contributed by Raphael Ackermann https://github.com/rtack
  * Changed a couple of log levels
    * see https://github.com/jayway/maven-android-plugin/pull/338
    * contributed by Oleg Green https://github.com/marchelo
  * Consolidated aapt command invocations in one builder style class
    * see https://github.com/jayway/maven-android-plugin/pull/341
    * see https://github.com/jayway/maven-android-plugin/pull/376
    * fixes 375
    * contributed by Oleg Green https://github.com/marchelo
    * and by William Ferguson https://github.com/william-ferguson-au
  * New property for android.aidlSourceDirectory to allow aidl source in different folder from rest of source
    * see https://github.com/jayway/maven-android-plugin/pull/343
    * see https://github.com/jayway/maven-android-plugin-samples/pull/55
    * fixes [issue 173](https://code.google.com/p/maven-android-plugin/issues/detail?id=173)
    * contributed by Csaba Kozák https://github.com/WonderCsabo
    * and William Ferguson https://github.com/william-ferguson-au
  * Allow android:run to proceed through a multi module build just like other device interaction goals
    * see https://github.com/jayway/maven-android-plugin/pull/344
    * contributed by Oleg Green https://github.com/marchelo
  * Taking reactor projects into account for resolving dependency tree of aar packages including taking into account wagon extensions
    * see https://github.com/jayway/maven-android-plugin/pull/347
    * see https://github.com/jayway/maven-android-plugin/pull/355
    * see https://github.com/jayway/maven-android-plugin/pull/361
    * fixes https://github.com/jayway/maven-android-plugin/issues/350
    * contributed by William Ferguson https://github.com/william-ferguson-au
  * Fixed the construction of R.java files for the dependencies of an APK
    * see https://github.com/jayway/maven-android-plugin/pull/349
    * contributed by William Ferguson https://github.com/william-ferguson-au
  * Fail build if project + dependencies have more than one layout file of the same name
    * see https://github.com/jayway/maven-android-plugin/pull/352
    * see https://github.com/jayway/maven-android-plugin-samples/pull/56
    * contributed by William Ferguson https://github.com/william-ferguson-au
  * Fail build if duplicate packages in AndroidManifest files for project and dependencies are detected
    * this would otherwise cause downstream compile or runtime problems that are much harder to detect
    * see https://github.com/jayway/maven-android-plugin/pull/353
    * contributed by Oleg Green https://github.com/marchelo
  * Provided scope dependencies get unpacked, improves instrumentation test runs
    * see https://github.com/jayway/maven-android-plugin/pull/362
    * contributed by Malachi de AElfweald https://github.com/malachid
  * use build extensions classloader if exists https://github.com/jayway/maven-android-plugin/pull/366
    * see https://github.com/jayway/maven-android-plugin/pull/366
    * fixes 364 https://github.com/jayway/maven-android-plugin/issues/364
    * fixes 350 https://github.com/jayway/maven-android-plugin/issues/350
    * contributed by William Ferguson https://github.com/william-ferguson-au
  * Samples libraryprojects/libraryprojects-tests failure fixed
    * see  https://github.com/jayway/maven-android-plugin/pull/370
    * fixes 369 https://github.com/jayway/maven-android-plugin/issues/369
    * fixes 358 https://github.com/jayway/maven-android-plugin/issues/358
    * contributed by William Ferguson https://github.com/william-ferguson-au
  * POM cleanup
    * see https://github.com/jayway/maven-android-plugin/pull/371
    * see https://github.com/jayway/maven-android-plugin-samples/pull/57
    * contributed by William Ferguson https://github.com/william-ferguson-au
  * Improved error message for missing dependencies
    * see https://github.com/jayway/maven-android-plugin/pull/372
    * contributed by William Ferguson https://github.com/william-ferguson-au
  * Added the now required scope "provided" for the apk under instrumentation test
    * see https://github.com/jayway/maven-android-plugin-samples/pull/58
    * contributed by William Ferguson https://github.com/william-ferguson-au
  * Fix up samples to work with the now stricter check on duplicate package usage
    * see https://github.com/jayway/maven-android-plugin-samples/pull/59
    * contributed by William Ferguson https://github.com/william-ferguson-au

ATTENTION:

  * Maven versions 3.0.4+ are now supported again
  * instrumentation tested apk's have to use provided scope in the test project
  * further new parameters and their usage are documented on the site http://jayway.github.io/maven-android-plugin/

### Android Maven Plugin 3.9.0-rc.1 - 2014-02-24 ###

  * A whole lot of pom and other clean ups to the sample projects
    * contributed by Manfred Moser http://www.simpligility.com
  * Travis build to execute clean goal
    * contributed by Manfred Moser http://www.simpligility.com
  * Deploy/Undeploy and Redeploy goals working for multi module builds
    * https://github.com/jayway/maven-android-plugin/pull/272
    * contributed by Manfred Moser http://www.simpligility.com
  * New goals deploy-apk, undeploy-apk and redeploy-apk
    * https://github.com/jayway/maven-android-plugin/pull/272
    * contributed by Manfred Moser http://www.simpligility.com
  * Improved error message for duplicate files
    * see https://github.com/jayway/maven-android-plugin/pull/261 and https://github.com/jayway/maven-android-plugin/pull/263
    * contributed by Jérémie https://github.com/kops and https://github.com/arichiardi
  * Fix to classifier usage for native projects
    * see https://github.com/jayway/maven-android-plugin/pull/262
    * contributed by Johan Lindquist https://github.com/johanlindquist
  * Fix the HAR resolution with apklib's
    * see https://github.com/jayway/maven-android-plugin/pull/280
    * contributed by Johan Lindquist https://github.com/johanlindquist
  * Improved version update support for AndroidManifest changes to work with longer version numbers
    * see https://github.com/jayway/maven-android-plugin/pull/264
    * contributed by https://github.com/Zlate87
  * Support for the jumbo flag of the dex command
    * seehttps://github.com/jayway/maven-android-plugin/pull/271
    * contributed by Stéphane Nicolas https://github.com/stephanenicolas
  * Support for specifying a list of devices to interact with for tests, deployment...
    * see https://github.com/jayway/maven-android-plugin/pull/268
    * see https://github.com/jayway/maven-android-plugin/pull/274
    * contributed by Emmanuel DEMEY https://github.com/Gillespie59
  * Fix paths for proguard invocation with filename containing "-"
    * see https://github.com/jayway/maven-android-plugin/pull/273
    * see https://github.com/jayway/maven-android-plugin/pull/269
    * see https://github.com/jayway/maven-android-plugin/pull/281
    * see https://github.com/jayway/maven-android-plugin/pull/282
    * see https://github.com/jayway/maven-android-plugin/pull/284
    * contributed by https://github.com/mmadev
    * and Manfred Moser http://www.simpligility.com
    * and Benoit Billington https://github.com/Shusshu
  * Allow copying the manifest during the generate source phase
    * see https://github.com/jayway/maven-android-plugin/pull/275
    * fixes [issue 343](https://code.google.com/p/maven-android-plugin/issues/detail?id=343)
    * contributed by Malachi de AElfweald https://github.com/malachid
  * Correction on how libs are pulled in from apklibs with regards to native artifacts
    * fixes [issue 444](https://code.google.com/p/maven-android-plugin/issues/detail?id=444)
    * see https://github.com/jayway/maven-android-plugin/pull/277
    * contributed by https://github.com/eedzjee
  * Prevent OOM issues when capturing stdout
    * see https://github.com/jayway/maven-android-plugin/pull/278
    * contributed by Johan Lindquist https://github.com/johanlindquist
  * AAR consumption and related fixes and changes to plugin and samples
    * see https://github.com/jayway/maven-android-plugin/pull/270
    * see https://github.com/jayway/maven-android-plugin/pull/279
    * see https://github.com/jayway/maven-android-plugin-samples/pull/44
    * see https://github.com/jayway/maven-android-plugin-samples/pull/45
    * see https://github.com/jayway/maven-android-plugin/pull/283
    * see https://github.com/jayway/maven-android-plugin-samples/pull/46
    * see https://github.com/jayway/maven-android-plugin/pull/287
    * fixes [issue 446](https://code.google.com/p/maven-android-plugin/issues/detail?id=446)
    * see https://github.com/jayway/maven-android-plugin/pull/289
    * see https://github.com/jayway/maven-android-plugin-samples/pull/47
    * see https://github.com/jayway/maven-android-plugin/pull/293
    * see https://github.com/jayway/maven-android-plugin/pull/295
    * see https://github.com/jayway/maven-android-plugin-samples/pull/48
    * see https://github.com/jayway/maven-android-plugin-samples/pull/49
    * see https://github.com/jayway/maven-android-plugin/pull/294
    * contributed by William Ferguson https://github.com/william-ferguson-au
    * and Benoit Billington https://github.com/Shusshu
    * and Manfred Moser http://www.simpligility.com
    * and Oleg Green https://github.com/marchelo
    * and with help from Igor Fedorenko https://github.com/ifedorenko/
  * Attach a jar build output for apklib projects (optionally)
    * see https://github.com/jayway/maven-android-plugin/pull/285
    * contributed by Leonid https://github.com/greek1979
    * fixes [issue 139](https://code.google.com/p/maven-android-plugin/issues/detail?id=139)
  * Correct identifier in R file from apklib
    * see https://github.com/jayway/maven-android-plugin/pull/286
    * contributed by Oleg https://github.com/marchelo
    * fixes [issue 441](https://code.google.com/p/maven-android-plugin/issues/detail?id=441)
    * fixes [issue 443](https://code.google.com/p/maven-android-plugin/issues/detail?id=443)
  * Removed unused executor
    * https://github.com/jayway/maven-android-plugin/pull/291
    * contributed by Oleg https://github.com/marchelo
  * Support setups with no apilevel
    * https://github.com/jayway/maven-android-plugin/pull/290
    * contributed by William Ferguson https://github.com/william-ferguson-au
    * and Manfred Moser http://www.simpligility.com
  * Quieter, more readable logging during build
    * see https://github.com/jayway/maven-android-plugin/pull/292
    * contributed by William Ferguson https://github.com/william-ferguson-au

### Android Maven Plugin 3.8.2 - 2013-12-30 ###

  * Moved to plugin-testing from ASF
    * fixes [issue 423](https://code.google.com/p/maven-android-plugin/issues/detail?id=423)
    * contributed by Manfred Moser http://www.simpligility.com
  * Upgraded powermock
    * contributed by Manfred Moser http://www.simpligility.com
  * Upgraded Android builder and sdk dependencies to 0.7.1
    * contributed by Manfred Moser http://www.simpligility.com
  * Improvements for aar consumption with regards to R.txt and R file as well as multiple aar and apklib deps and a whole lot of cleanup and examples stuff, should be fully working now
    * see https://github.com/jayway/maven-android-plugin/pull/254
    * see https://github.com/jayway/maven-android-plugin/pull/255
    * see https://github.com/jayway/maven-android-plugin/pull/257
    * see https://github.com/jayway/maven-android-plugin/pull/260
    * see https://github.com/jayway/maven-android-plugin-samples/pull/40
    * see https://github.com/jayway/maven-android-plugin-samples/pull/41
    * see https://github.com/jayway/maven-android-plugin-samples/pull/42
    * see https://github.com/jayway/maven-android-plugin-samples/pull/43
    * fixes [issue 436](https://code.google.com/p/maven-android-plugin/issues/detail?id=436)
    * whole bunch of changes to the examples project
    * contributed by William Ferguson https://github.com/william-ferguson-au
    * and Benoit Billington https://github.com/Shusshu
    * and Manfred Moser http://www.simpligility.com
  * ConfigHandler improvements
    * see https://github.com/jayway/maven-android-plugin/pull/259
    * contributed by Pappy Stanescu https://github.com/pa314159

### Android Maven Plugin 3.8.1 - 2013-12-05 ###

  * Support for aar consumption improved
    * see https://github.com/jayway/maven-android-plugin/pull/244
    * see https://github.com/jayway/maven-android-plugin/pull/249
    * contributed by Benoit Billington https://github.com/Shusshu and https://github.com/ialbors
  * Support for files located in META-INF improved
    * fixed [issue 174](https://code.google.com/p/maven-android-plugin/issues/detail?id=174)
    * see https://github.com/jayway/maven-android-plugin/pull/245
    * https://github.com/jayway/maven-android-plugin/pull/250
    * contributed by Pappy Stanescu https://github.com/pa314159 and Manfred Moser
  * Manifest update into a new file in target (optionally)
    * https://github.com/jayway/maven-android-plugin/pull/248
    * contributed by Pappy Stanescu https://github.com/pa314159
  * Support for providing further options to proguard execution
    * see https://github.com/jayway/maven-android-plugin/pull/247
    * contributed by Pappy Stanescu https://github.com/pa314159
  * Optionally attach proguard mapping.txt as artifact of type "map"
    * https://github.com/jayway/maven-android-plugin/pull/251
    * contributed by Pappy Stanescu https://github.com/pa314159
  * Extended instrumentation goal to allow for additional user defined instrumentation arguments
    * see https://github.com/jayway/maven-android-plugin/pull/243
    * contributed by Sebastian Gröbler https://github.com/SierraGolf
  * Fixed link to documentation in git readme
    * see https://github.com/jayway/maven-android-plugin/pull/252
    * contributed by Peter Janes http://peterjanes.ca/
  * GenerateSourceMojo fixes
    * see https://github.com/jayway/maven-android-plugin/pull/253
    * contributed by Pappy Stanescu https://github.com/pa314159

### Android Maven Plugin 3.8.0 - 2013-11-08 ###

  * Migrated to require Apache Maven 3.1.1 or higher
    * contributed by Manfred Moser http://www.simpligility.com
    * see commit on Oct 1 and 7th 2013
    * fixes [issue 395](https://code.google.com/p/maven-android-plugin/issues/detail?id=395)
  * Updated to builder library 0.6.0 and later to 0.6.3
    * contributed by Manfred Moser http://www.simpligility.com
  * Fix for har file access in MakefileHelper
    * contributed by Manfred Moser http://www.simpligility.com and Johan Lindquist https://github.com/johanlindquist
  * Maven 3.1.1 deployment as part of travis build
    * see https://github.com/jayway/maven-android-plugin/pull/237
      * contributed by Mykola Nikishov https://manandbytes.wordpress.com/
  * Updated to builder library 0.6.1
    * https://github.com/jayway/maven-android-plugin/pull/239
    * contributed by Benoit Billington https://github.com/Shusshu
  * Usage of SDK constants instead of hardcoding classes.jar
    * https://github.com/jayway/maven-android-plugin/pull/238
    * contributed by Benoit Billington https://github.com/Shusshu
  * Create R file for AARs
    * see https://github.com/jayway/maven-android-plugin/pull/240
    * contributed by Benoit Billington https://github.com/Shusshu
  * Support --incremental on dex
    * see https://github.com/jayway/maven-android-plugin/pull/236
    * contributed by Jaime Soriano Pastor https://github.com/jsoriano
  * Further improvements towards support for aar consumption (still not fully working)
    * see https://github.com/jayway/maven-android-plugin/pull/242
    * contributed by Benoit Billington https://github.com/Shusshu

ATTENTION: Maven 3.1.1+ is required to build the plugin itself as well as to use the plugin to build Android applications!

### Android Maven Plugin 3.7.0 - 2013-09-27 ###

  * Updated builder library version to 0.5.6
    * see https://github.com/jayway/maven-android-plugin/pull/220
    * contributed by Benoit Billington https://github.com/Shusshu
    * related cleanups in AndroidSdk and tests by Manfred Moser
  * Don't delete nativeArtifactFile if its the same as destFile
    * see https://github.com/jayway/maven-android-plugin/pull/224
    * contributed by Mark Riley http://markriley.net
  * Support for maven property maven.test.error.ignore
    * see https://github.com/jayway/maven-android-plugin/pull/225
    * contributed by Stéphane Nicolas https://github.com/stephanenicolas
  * Use of constant for apk and apklib instead of hardcoded string
    * see https://github.com/jayway/maven-android-plugin/pull/229
    * contributed by Benoit Billington https://github.com/Shusshu
  * **Experimental** support for consuming and creating aar files
    * see https://github.com/jayway/maven-android-plugin/pull/227
    * see https://github.com/jayway/maven-android-plugin/pull/228
    * https://github.com/jayway/maven-android-plugin/pull/235
    * contributed by Benoit Billington https://github.com/Shusshu and Manfred Moser and Mark Riley https://github.com/markrileybot
  * SdkLib and ApkBuilder cleanup
    * see https://github.com/jayway/maven-android-plugin/pull/232
    * contributed by Manfred Moser http://www.simpligility.com
  * Upgraded to builder 0.5.7 and added all dependencies from SDK in version 22.2.0
    * contributed by Manfred Moser http://www.simpligility.com
  * Support for multiarch so dependencies and Multiple native architecture support
    * see https://github.com/jayway/maven-android-plugin/pull/230
    * contributed by Joonas Javanainen http://gekkio.fi/
    * see https://github.com/jayway/maven-android-plugin/pull/233
    * contributed by Johan Lindquist https://github.com/johanlindquist
  * Adding Native Libs in apk
    * see https://github.com/jayway/maven-android-plugin/pull/233
    * fixes [issue 372](https://code.google.com/p/maven-android-plugin/issues/detail?id=372)
    * contributed by Charles Harley and  Johan Lindquist https://github.com/johanlindquist
  * Make use of "aaptExtraArgs" in "generate-sources" goal
    * see https://github.com/jayway/maven-android-plugin/pull/234
    * contributed by Tadeas Kriz https://github.com/TadeasKriz
  * Release process changes to use nexus-staging-maven-plugin
    * contributed by Manfred Moser http://www.simpligility.com
  * Plugin site changed from Google SVN repo to Github pages
    * contributed by Manfred Moser http://www.simpligility.com

ATTENTION:

  * The sdk platform configuration parameter no longer support platform, only API level works from now on.
  * the keyword 'all' is no longer supported for ndk architectures, you have to explicitly list them


### Android Maven Plugin 3.6.1 - 2013-07-31 ###

  * Updated builder library version to 0.4.1 and 0.4.2, which pulls in Android SDK 22.0.1 components
    * contributed by Manfred Moser http://www.simpligility.com
  * Fix to avoid namespace collisions for components with identical artifactid
    * see https://github.com/jayway/maven-android-plugin/pull/216
    * contributed by Jan Berkel http://zegoggl.es/
  * Ability to pass user properties to UiAutomator goal
    * see https://github.com/jayway/maven-android-plugin/pull/211
    * contributed by Simon Sikström http://andrimon.com
  * Configurable BuildConfig generation
    * see https://github.com/jayway/maven-android-plugin/pull/218
    * contributed by Jonas Alves http://jonasalves.wordpress.com/
  * Exclude jar files within a lib folder in an apklib
    * see https://github.com/jayway/maven-android-plugin/pull/219
    * fixes [issue 402](https://code.google.com/p/maven-android-plugin/issues/detail?id=402)
    * contributed by Matthias Käppler http://brainflush.wordpress.com
  * Downgraded emma to stable release
    * fixes [issue 301](https://code.google.com/p/maven-android-plugin/issues/detail?id=301)
      * contributed by Manfred Moser http://www.simpligility.com
  * Use artifactId as LOCAL\_MODULE\_FILENAME
    * fixes [issue 410](https://code.google.com/p/maven-android-plugin/issues/detail?id=410)
    * https://github.com/jayway/maven-android-plugin/pull/223
    * contributed by Joonas Javanainen http://gekkio.fi
  * NDK mojo: ignore libs/ folder with just JARs for APKLIB dependencies
    * fixes [issue 402](https://code.google.com/p/maven-android-plugin/issues/detail?id=402)
    * see https://github.com/jayway/maven-android-plugin/pull/219
    * contributed by Matthias Käppler http://mttkay.github.io/

### Android Maven Plugin 3.6.0 - 2013-05-22 ###

  * Fix forMac OS X Proguard usage bug
    * see https://github.com/jayway/maven-android-plugin/pull/198
    * contributed by https://github.com/jckeatley
  * Added the parameter reportSuffix to UIAutomator goal
    * see https://github.com/jayway/maven-android-plugin/pull/201
    * contributed by Johannes Elgh https://github.com/jelgh
  * Added unlockEmulator to unlock the emulator during emulator-start
    * see https://github.com/jayway/maven-android-plugin/pull/200
    * contributed by Tom Bollwitt https://github.com/tlbollwitt
  * Added support for MonkeyRunner execution
    * see https://github.com/jayway/maven-android-plugin/pull/199
    * contributed by Stéphane Nicolas https://github.com/stephanenicolas
  * Support for SDK 22 directory structure
    * see https://github.com/jayway/maven-android-plugin/pull/205
    * see https://github.com/jayway/maven-android-plugin/pull/206
    * contributed by Benoit Billington https://github.com/Shusshu
  * Updated builder library version to 0.4
    * see https://github.com/jayway/maven-android-plugin/pull/204
    * contributed by Benoit Billington https://github.com/Shusshu
  * CI server build via Travis CI for plugin and samples
    * see https://github.com/jayway/maven-android-plugin/pull/203
    * samples see https://github.com/jayway/maven-android-plugin-samples/pull/33
    * contributed Hugo Josefson http://about.me/hugojosefson
  * --non-constant-id for generating R for APKLIBs
    * https://github.com/jayway/maven-android-plugin/pull/202
    * contributed by Patrick Armstrong https://github.com/slypat
  * Support manifest merger with Android SDK [R22](https://code.google.com/p/maven-android-plugin/source/detail?r=22)
    * see https://github.com/jayway/maven-android-plugin/pull/210
    * contributed by James Wald https://github.com/jameswald
    * reimplemented with backwards compatibility see
      * contributed by Manfred Moser http://www.simpligility.com
  * Upgraded AndroidSdk to use path and platform utilities from sdklib
    * see https://github.com/jayway/maven-android-plugin/pull/207
    * contributed by Nic Strong http://www.codepoets.co.nz
    * fixes and updates to work for all examples and more contributed by Manfred Moser http://www.simpligility.com
    * see https://github.com/jayway/maven-android-plugin/commit/b5b773e50f2f39be9e68bbf094759ae3a866831a
  * Exclude all except jar dependcies from proguard -injar parameters
    * see https://github.com/jayway/maven-android-plugin/pull/191
    * fixes [issue 319](https://code.google.com/p/maven-android-plugin/issues/detail?id=319)
    * contributed by https://github.com/tprochazka
  * Support uses sdk tag in manifest updates
    * see https://github.com/jayway/maven-android-plugin/pull/209
    * contributed by https://github.com/fjfdeztoro
  * Support for multiple source folders in APK Lib
    * see https://github.com/jayway/maven-android-plugin/pull/208
    * contributed by Marek Kedzierski http://mark.kedzierski.googlepages.com/
  * Upgraded screenshot library to 1.9 to use keep ddmlib version in sync
    * contributed by Manfred Moser http://www.simpligility.com
  * Change manifest merge to use classpath dependency to sdk 22 jar directly rather than loading from SDK and using reflection
    * see https://github.com/jayway/maven-android-plugin/pull/214
    * contributed by James Wald https://github.com/jameswald

All merges, CI server work, changelog editing and release process contributed by Manfred Moser

ATTENTION:

The configuration of the sdk platform is now required for SDK as well as NDK projects.
An example plugin configuration is

```
<configuration>
  <sdk> 
    <platform>17</platform>
   </sdk>
</configuration>
```

The plugin has been updated to work with the SDK release 22.0. 21.1 works on the CI server. It might or might not work for older versions. YMMV.

### Android Maven Plugin 3.5.3 - 2013-04-09 ###

  * Fix for NDK codebase so that NDK install is NOT required for normal builds
    * see https://github.com/jayway/maven-android-plugin/pull/196
    * contributed by Jonathan Reyes http://vaporwarecorp.com
  * Added support for x86\_64 introduced in NDK r8e
    * see https://github.com/jayway/maven-android-plugin/pull/195
    * contributed by Jonathan Reyes http://vaporwarecorp.com
  * Fix proguard usage on Mac with non-Apple JDK (= Java 7 from Oracle, which is the new default)
    * see https://github.com/jayway/maven-android-plugin/pull/197
      * contributed by Roberto Tyley https://github.com/rtyley
  * Added support for the Android Monkey tool
    * see https://github.com/jayway/maven-android-plugin/pull/194/
    * contributed by Stéphane Nicolas https://github.com/stephanenicolas

Release process, pull request merges and more contributed by Manfred Moser

Minimal plugin configuration to enable monkey is
```
<monkey>
  <skip>false</skip>
</monkey>
```

Full configuration can use these parameters.
```
 <monkey>
   <skip>false</skip>
   <eventCount>5000</eventCount>
   <seed>123456</seed>
   <throttle>10</throttle>
   <percentTouch>10</percentTouch>
   <percentMotion>10</percentMotion>
   <percentTrackball>10</percentTrackball>
   <percentNav>10</percentNav>
   <percentMajorNav>10</percentMajorNav>
   <percentSyskeys>10</percentSyskeys>
   <percentAppswitch>10</percentAppswitch>
   <percentAnyevent>10</percentAnyevent>
   <packages>
       <package>com.foo</package>
       <package>com.bar</package>
   </packages>
   <categories>
       <category>foo</category>
       <category>bar</category>
   </categories>
   <debugNoEvents>true</debugNoEvents>
   <hprof>true</hprof>
   <ignoreCrashes>true</ignoreCrashes>
   <ignoreTimeouts>true</ignoreTimeouts>
   <ignoreSecurityExceptions>true</ignoreSecurityExceptions>
   <killProcessAfterError>true</killProcessAfterError>
   <monitorNativeCrashes>true</monitorNativeCrashes>
   <createReport>true</createReport>
 </monkey>
```

### Android Maven Plugin 3.5.2 - 2013-04-01 ###

Attention - due to a bug this release requires you to have the NDK installed even for normal builds.
If that is a problem please wait for the next release. A fix exist in the current 3.5.3-SNAPSHOT version.

  * Fix to get android:push of directories working on Windows clients
    * see https://github.com/jayway/maven-android-plugin/pull/181
    * contributed by Tobias Hochwallner https://github.com/tobster  and Manfred Moser
  * Enable transitive native dependencies for apklib with example
    * https://github.com/jayway/maven-android-plugin/pull/182
    * https://github.com/jayway/maven-android-plugin-samples/pull/31
    * contributed by Tim Hepner https://github.com/mithepner
  * Support for maven.test.failure.ignore
    * see https://github.com/jayway/maven-android-plugin/pull/183
    * fixes [issue 274](https://code.google.com/p/maven-android-plugin/issues/detail?id=274) and  [issue 172](https://code.google.com/p/maven-android-plugin/issues/detail?id=172)
    * contributed by Olivier Gonthier https://github.com/OlivierGonthier
  * ApkLib R.class files must have non-final ints.
    * see https://github.com/jayway/maven-android-plugin/pull/184
    * contributed by Christian Williams https://github.com/xian and Square https://squareup.com/
  * Add "classifier" support to apklib goal
    * see https://github.com/jayway/maven-android-plugin/pull/186
    * contributed by Mark Allison http://www.stylingandroid.com/
  * UI Automator goal  including feature to take screenshots - documentation in javadoc, site  and examples
    * see https://github.com/jayway/maven-android-plugin/pull/185
    * also see https://github.com/jayway/maven-android-plugin/pull/188
    * and https://github.com/jayway/maven-android-plugin/pull/193
    * contributed by Stéphane Nicolas https://github.com/stephanenicolas  sponsored by OCTO Technology http://www.octo.com/
  * Adopted usage of the Android SDK Builder library as used by the Gradle based build
    * see https://github.com/jayway/maven-android-plugin/commit/fc6f18cd96c756a120208ea25bf493af5716cced
    * contributed by Manfred Moser http://www.simpligility.com
  * Added support to install multiple platform specific native library versions
    * see https://github.com/jayway/maven-android-plugin/pull/187
    * and https://github.com/jayway/maven-android-plugin/pull/189
    * contributed by Jonathan Reyes http://vaporwarecorp.com

Release process, pull request merges and more contributed by Manfred Moser

Minimal plugin configuration to enable lint is
```
<uiautomator>
  <skip>false</skip>
</uiautomator>
```

Full configuration can use these parameters.
```
<uiautomator>
  <skip>false</skip>
  <testClassOrMethods>
    <testClassOrMethod>com.foo.SampleTest</testClassOrMethod>
    <testClassOrMethod>com.bar.CalculatorTest#testCalculatorApp</testClassOrMethod>
  </testClassOrMethods>
  <createReport>true</createReport>
  <takeScreenshotOnFailure>true</takeScreenshotOnFailure>
  <screenshotsPathOnDevice>/sdcard/uiautomator-screenshots/</screenshotsPathOnDevice>
</uiautomator>
```

### Android Maven Plugin 3.5.1 - 2013-02-23 ###

  * Added existence check for res folder when expanding apklib files to make it more robust against that problem
    * see https://github.com/jayway/maven-android-plugin/pull/165
    * contributed by Tom Bollwitt https://github.com/tlbollwitt
  * Support for multiple proguard configuration files
    * usage see pull request or project documentation site after release or local site build
    * see https://github.com/jayway/maven-android-plugin/pull/163
    * fixes [issue 331](https://code.google.com/p/maven-android-plugin/issues/detail?id=331)
    * contributed by Sven Obser https://github.com/brudaswen/
  * Allow configuration of NDK path from system property or pom.xml allowing to override default of using ANDROID\_NDK\_HOME
    * see https://github.com/jayway/maven-android-plugin/pull/162
    * contributed by https://github.com/tptak
  * readme update
    * see https://github.com/jayway/maven-android-plugin/pull/166
    * contributed by Ikram http://about.me/iontech
  * support for pre dexed libraries
    * see https://github.com/jayway/maven-android-plugin/pull/161
    * see https://github.com/jayway/maven-android-plugin/pull/171
    * contributed by  Srinivasan http://srini-ragu.blogspot.com/
  * Auto generate proguard config file from AndroidManifest
    * see https://github.com/jayway/maven-android-plugin/pull/164
    * see https://github.com/jayway/maven-android-plugin/pull/175
    * fixes [issue 342](https://code.google.com/p/maven-android-plugin/issues/detail?id=342)
    * contributed by Sven Obser https://github.com/brudaswen/
  * Null checks in ManifestUpdate mojo so it works for merging manifests from apklibs
    * see https://github.com/jayway/maven-android-plugin/pull/167
    * contributed by Tom Bollwitt https://github.com/tlbollwitt
  * Support for Android Lint
    * see https://github.com/jayway/maven-android-plugin/pull/168
    * see https://github.com/jayway/maven-android-plugin/pull/169
    * and see a whole number of commits around https://github.com/jayway/maven-android-plugin/commit/59c4bbf39229320e803c396e784b09284f2228fd
    * https://github.com/jayway/maven-android-plugin/pull/177
    * fixes [issue 224](https://code.google.com/p/maven-android-plugin/issues/detail?id=224)
    * contributed by Stéphane Nicolas https://github.com/stephanenicolas sponsored by OCTO Technology http://www.octo.com/ and Manfred Moser http://www.simpligility.com and Stefano Dacchille https://github.com/stefanodacchille
  * enhanced wait for emulator start
    * fixes [issue 270](https://code.google.com/p/maven-android-plugin/issues/detail?id=270)
    * see https://github.com/jayway/maven-android-plugin/pull/173/
    * contributed by https://github.com/ffriedrich
  * Fix NDK gdbserver paths
    * see https://github.com/jayway/maven-android-plugin/pull/174
    * contributed by Luke Weber https://github.com/lukeweber
    * see https://github.com/jayway/maven-android-plugin/pull/179
    * improved by  Jonathan Reyes http://vaporwarecorp.com and Manfred Moser
    * Attention! This change requires usage of Android NDK >= 8b
  * Support for including/excluding packages in Emma coverage data
    * see https://github.com/jayway/maven-android-plugin/pull/176
    * contributed by Maximilian Wahler https://github.com/schlachtzeuger and Manfred Moser http://www.simpligility.com
  * Fixes to test cases to work on Windows
    * see https://github.com/jayway/maven-android-plugin/pull/178
    * contributed by Eugen Martynov https://github.com/emartynov
  * Zipalign to same apk name rather than creating a new file
    * see https://github.com/jayway/maven-android-plugin/pull/180
    * contributed by Eugen Martynov https://github.com/emartynov
  * Fixed problem of excessive logging in build output from expanding dependencies
    * contributed by Manfred Moser http://www.simpligility.com
  * Parallel execution of all device interactions
    * see https://github.com/jayway/maven-android-plugin/pull/159
    * contributed by Jonas Alves http://jonasalves.wordpress.com/
    * logging improvements by Manfred Moser http://www.simpligility.com


Release process, pull request merges and more contributed by Manfred Moser

Minimal plugin configuration to enable lint is
```
<lint>
  <skip>false</skip>
</lint>
```
which will produce xml report in target/lint/lint.xml
Full configuration options available are
```
<lint>
    <failOnError>true|false</failOnError>
    <skip>true|false</skip>
    <ignoreWarnings>true|false</ignoreWarnings>
    <warnAll>true|false</warnAll>
    <warningsAsErrors>true|false</warningsAsErrors>
    <config></config>
    <fullPath>true|false</fullPath>
    <showAll>true|false</showAll>
    <disableSourceLines>true|false</disableSourceLines>
    <url>none|a=b</url>
    <enableHtml>true|false</enableHtml>
    <htmlOutputPath>${project.build.directory}/lint-html</htmlOutputPath>
    <enableSimpleHtml>true|false</enableSimpleHtml>
    <simpleHtmlOutputPath>${project.build.directory}/lint-simple-html</simpleHtmlOutputPath>
    <enableXml>true|false</enableXml>
    <xmlOutputPath>${project.build.directory}/lint.xml</xmlOutputPath>
    <enableSources>true|false</enableSources>
    <sources></sources>
    <enableClasspath>true|false</enableClasspath>
    <classpath></classpath>
    <enableLibraries>true|false</enableLibraries>
    <libraries></libraries>
</lint>
```

### Android Maven Plugin 3.5.0 - released 2012-12-18 ###

  * Non-release builds will now automatically be debuggable
    * see https://github.com/jayway/maven-android-plugin/pull/149
    * contributed by James Lawrie  https://github.com/jlawrienyt
  * Added support to for updating android:authorities attributes on provider elements in the manifest
    * see https://github.com/jayway/maven-android-plugin/pull/151
    * contributed by Nic Strong http://www.codepoets.co.nz
  * Improved automatic versionCode generation to avoid ambigious versionCode for different versions
    * see https://github.com/jayway/maven-android-plugin/pull/154
    * and https://github.com/jayway/maven-android-plugin/pull/155
    * contributed by Fred Eisele https://github.com/phreed
  * Allow the specification of patterns to exclude jar files from resource inclusion
    * see https://github.com/jayway/maven-android-plugin/pull/152
    * contributed by Mark Raynsford http://io7m.com
  * Allow handling of library name differently than `lib<artifactId>.so`
    * see https://github.com/jayway/maven-android-plugin/pull/156
    * fixes [issue 303](https://code.google.com/p/maven-android-plugin/issues/detail?id=303)
    * contributed by Tomasz Ptak https://github.com/tptak
  * Fix for RC versions of the SDK in terms of manifest parsing and overall plugin execution
    * see https://github.com/jayway/maven-android-plugin/pull/157
    * contributed by Stéphane Nicolas https://github.com/stephanenicolas
  * Allow relative package names for the run goal
    * see https://github.com/jayway/maven-android-plugin/pull/160
    * contributed by Jonas Alves http://jonasalves.wordpress.com/
  * Introduced usage of parent pom to remove need to manage plugin versions
    * contributed by Manfred Moser http://www.simpligility.com
  * Cleaned up site creation
    * contributed by Manfred Moser http://www.simpligility.com
  * Updated all dependency versions
    * contributed by Manfred Moser http://www.simpligility.com


Code reviews, testing, minor adjustments by Manfred Moser http://www.simpligility.com

API/Configuration Changes:

**ATTENTION**

Since non-release builds are now debuggable by default you NEED TO ensure that the release parameter is set to true in your release build.

In the pom this would be e.g.
```
<groupId>com.jayway.maven.plugins.android.generation2</groupId>
<artifactId>android-maven-plugin</artifactId>
<configuration>
    <release>true</release>
```

or you could activate on the command line with e.g

```
mvn clean deploy -Dandroid.release=true
```

or if you use the release plugin just add the above pom config to the release profile.


### Android Maven Plugin 3.4.1 ###
  * apklib now uses the resourceOverlayDirectories and resourceOverlayDirectory options
    * see https://github.com/jayway/maven-android-plugin/pull/143
    * contributed by Tim Hepner https://github.com/mithepner
  * Showing current test count and number of total count of tests during instrumentation test runs
    * see https://github.com/jayway/maven-android-plugin/pull/147
    * contributed by Aleksander Pyszny http://www.alan-systems.com/en
  * Adapted Manifest merging to Android SDK release 21
    * see https://github.com/jayway/maven-android-plugin/pull/146
    * contributed by Tom Bollwitt https://github.com/tlbollwitt
  * Fixed parsing of android.test.packages for multiple comma separated packages names to test
    * see https://github.com/jayway/maven-android-plugin/pull/145
    * contributed by Aleksander Pyszny http://www.alan-systems.com/en
  * Parse return value of installPackage() during deploy and report failure as build failure with error message instead of ignoring it
    * see https://github.com/jayway/maven-android-plugin/pull/148
    * contributed by Nic Strong http://www.codepoets.co.nz

All merges, miscellaneous improvements and release performance contributed by Manfred Moser, http://www.simpligility.com

### Android Maven Plugin 3.4.0 ###

  * Added support to specify application makefile in ndk-build
    * see https://github.com/jayway/maven-android-plugin/pull/131
    * contributed by Jonathan Reyes http://vaporwarecorp.com
  * New additional parameter for proguard goal, "outputDirectory"
    * see https://github.com/jayway/maven-android-plugin/pull/127
    * contributed by Michal Harakal https://github.com/michalharakal
  * Support for building arm and x86 at the same time
    * see https://github.com/jayway/maven-android-plugin/pull/132/
    * contributed by Jonathan Reyes http://vaporwarecorp.com
  * Fixed ndkstripper when no toolchain is specified
    * see https://github.com/jayway/maven-android-plugin/pull/133/
    * contributed by Jonathan Reyes http://vaporwarecorp.com
  * Fixed parsing of error message from test failures
    * see https://github.com/jayway/maven-android-plugin/pull/139
    * contributed by Aleksander Pyszny https://github.com/olekp http://www.alan-systems.com
  * Check renameManifestPackage parameter before using package from AndroidManifest.xml
    * see https://github.com/jayway/maven-android-plugin/pull/138
    * contributed by Jason Holmes http://blog.thejholmes.com
  * Make inclusion of JDK libs in ProGuard input optional.
    * see https://github.com/jayway/maven-android-plugin/pull/137
    * contributed by Karsten Sperling https://github.com/ksperling http://www.pluk.com
  * Configure BuildConfig generation via a mojo parameter instead of system property
    * see https://github.com/jayway/maven-android-plugin/pull/136
    * contributed by Karsten Sperling https://github.com/ksperling http://www.pluk.com
  * Added code to merge APKLIB manifests
    * see https://github.com/jayway/maven-android-plugin/pull/135
    * contributed by  Tom Bollwitt https://github.com/tlbollwitt
  * Improvements and fixes for APKLib support with Native code including sample projects
    * see https://github.com/jayway/maven-android-plugin/pull/134
    * see https://github.com/jayway/maven-android-plugin-samples/pull/30
    * contributed by by Andi Everitt  https://github.com/andi12  http://www.raje.org.uk
  * Clean up of configuration for zipalign goal to work properly with pom, settings and command line config
    * see https://github.com/jayway/maven-android-plugin/commit/cb79d0b1aa65f5fd52ec267ce9f8624af17b828e
    * contributed by Manfred Moser http://www.simpligility.com
  * Fix for failure when ndk-build run twice by task sequence
    * see https://github.com/jayway/maven-android-plugin/pull/141
    * contributed by by Andi Everitt  https://github.com/andi12  http://www.raje.org.uk

All merges, codestyle fixups and more miscellaneous improvements contributed by Manfred Moser, http://www.simpligility.com

API/Configuration Changes:

  * BuildConfig configuration relies on android.release maven configuration rather than system property
  * zipalign activation/deactivation now works properly so you need to activate it with
```
<zipalign><skip>false</skip></zipalign> 
```
in configuration or with android.zipalign.skip=false
  * APK Merge support has to be configured like this
```
<plugins>
   <plugin>
     <artifactId>maven-resources-plugin</artifactId>
     <version>2.6</version>
     <executions>
       <execution>
         <phase>initialize</phase>
         <goals>
           <goal>resources</goal>
         </goals>
       </execution>
       <execution>
         <id>default-resources</id>
         <phase>DISABLED</phase>
       </execution>
     </executions>
   </plugin>
   <plugin>
     <groupId>com.jayway.maven.plugins.android.generation2</groupId>
     <artifactId>android-maven-plugin</artifactId>
     <configuration>
       <androidManifestFile>${project.build.directory}/AndroidManifest.xml</androidManifestFile>
       <mergeManifests>true</mergeManifests>
     </configuration>
     <extensions>true</extensions>
   </plugin>
 </plugins>
```

### Android Maven Plugin 3.3.2 ###
  * Support transitive apklibs when invoking aapt
    * see https://github.com/jayway/maven-android-plugin/pull/124
    * contributed by Jake Wharton http://jakewharton.com
  * Support BuildConfig generation.
    * see https://github.com/jayway/maven-android-plugin/pull/123
    * contributed by Jake Wharton http://jakewharton.com
  * Support use of alternative executable for "emulator"
    * see https://github.com/jayway/maven-android-plugin/pull/122 and some commit around that merge in master..
    * contributed by Tobias Gesellchen and Manfred Moser
  * Fix proguard mojo for projects which use the Android version of Apache Http components
    * see https://github.com/jayway/maven-android-plugin/pull/126
    * contributed by Tavian Barnes http://tavianator.com/
  * Add support to multiple native architectures
    * see https://github.com/jayway/maven-android-plugin/pull/125
    * contributed by Johann Reyes http://vaporwarecorp.com
  * Plugin updates, plugin site improvements and minor fixes
    * contributed by Manfred Moser http://simpligility.com
  * Report correct test run count even when failures occur
    * https://github.com/jayway/maven-android-plugin/pull/128
    * contributed by Jan Berkel http://zegoggl.es/
  * Use logger in debug level instead of stdout in CommandExecutor
    * see https://github.com/jayway/maven-android-plugin/pull/129
    * contributed by Jan Berkel http://zegoggl.es/
  * Add support for annotations when running instrumentation tests
    * see https://github.com/jayway/maven-android-plugin/pull/130/
    * contributed by Jan Berkel http://zegoggl.es/

All merges into master and release process work contributed by Manfred Moser

### Android Maven Plugin 3.3.1 (never released) ###

release process failed, version got bumped to 3.3.2
### Android Maven Plugin 3.3.0 ###

  * Expose manifest values in manifest goal as properties so they can be picked up in the build e.g. to be used for further tasks like scm branch creation, logging and so on
    * see javadoc for property name details, convention is android.manifest.xyz
    * see https://github.com/jayway/maven-android-plugin/pull/115
    * contributed by Richard Guest https://github.com/quiffman
  * Fix for Proguard Mojo to work on MacOSX without JAVA\_HOME set
    * see https://github.com/jayway/maven-android-plugin/pull/116
    * contributed by Arne Riiber
  * New standalone goal "devices" that shows a list of attached devices/emulators using the same naming convention as the other goals and shows the device status as well
    * see https://github.com/jayway/maven-android-plugin/pull/117
    * contributed by Manfred Moser http://simpligility.com
  * Workaround to the problem that apkbuilder excludes resources in META-INF
    * fixes [issue 97](https://code.google.com/p/maven-android-plugin/issues/detail?id=97)
    * see https://github.com/jayway/maven-android-plugin/pull/89
    * contributed by Pappy STĂNESCU https://github.com/pa314159
  * A large number of enhancements and fixes related to the NDK support of the Android Maven Plugin
    * see https://github.com/jayway/maven-android-plugin/pull/118
    * fixes [issue 255](https://code.google.com/p/maven-android-plugin/issues/detail?id=255): Apk does not contain native libs in 'libs/armeabi' during
    * fixes [issue 264](https://code.google.com/p/maven-android-plugin/issues/detail?id=264): NDK build doesn't work on Windows: PatternSyntaxException
    * fixes [issue 265](https://code.google.com/p/maven-android-plugin/issues/detail?id=265): NDK Build leaves generated .so unstripped thus large
    * fixes [issue 277](https://code.google.com/p/maven-android-plugin/issues/detail?id=277): NDK build leaves a lot of temporary files around
    * initial support for apk's with native debugging support (include gdbserver)
    * contributed by Johan Lindquist
  * Allow exclusion of transitive dependencies for native libraries
    * fixes [issue 282](https://code.google.com/p/maven-android-plugin/issues/detail?id=282)
    * see https://github.com/jayway/maven-android-plugin/pull/119
    * contributed by Johan Lindquist
  * Allow parsing of invalid version numbers to upgrade versionCode as good as possible
    * see https://github.com/jayway/maven-android-plugin/pull/112
    * and https://github.com/jayway/maven-android-plugin/commit/03e275df8a1b3801d4ed1f704b6b1619a3af682b
    * contributed by Marvin Bredal Lillehaug https://github.com/computerlove and Manfred Moser http://simpligility.com

### Android Maven Plugin 3.2.0 ###

  * Capture screenshots from the Android device during integration tests
    * see https://github.com/jayway/maven-android-plugin/pull/104
    * see https://github.com/jayway/maven-android-plugin-samples/pull/25
    * contributed by Roberto Tyley https://github.com/rtyley
  * Test coverage with Emma
    * see https://github.com/jayway/maven-android-plugin/pull/101/
    * see https://github.com/jayway/maven-android-plugin-samples/pull/24/
    * contributed by Mariusz Saramak http://saramak.eu/
  * Fix for manifest update
    * see https://github.com/jayway/maven-android-plugin/pull/106
    * contributed by Matt Benson
  * New configuration parameter parsing based on mojo property annotation and config pojo for Proguard, new parameters to filder manifest and maven files defaulting to true, allow proguard mojo to use dependency to use external proguard rather than sdk proguard
    * see https://github.com/jayway/maven-android-plugin/pull/107
    * see https://github.com/jayway/maven-android-plugin/pull/109
    * contributed by Adrian Stabiszewski https://github.com/grundid/ and Manfred Moser http://simpligility.com
  * New parameter to allow to set location of coverage file for instrumentation test runs
    * see https://github.com/jayway/maven-android-plugin/pull/108
    * contributed by Tim Baverstock https://github.com/androidweasel
  * New configuration parsing for Pull, Push and Run mojos, also added required parameter for PullParameter annotation and improved error message for any mojos using it
    * see https://github.com/jayway/maven-android-plugin/pull/110
    * see https://github.com/jayway/maven-android-plugin/pull/111
    * contributed by Manfred Moser http://simpligility.com
  * support for SupportScreens and CompatibleScreens elements in manifest-update goal
    * see https://github.com/jayway/maven-android-plugin/pull/92
    * contributed by Matthias Käppler http://brainflush.wordpress.com
  * support for brackets and spaces in Android Home path for integration tests
    * fixes [issue 263](https://code.google.com/p/maven-android-plugin/issues/detail?id=263)
    * see https://github.com/jayway/maven-android-plugin/pull/114
    * contributed by Bob Walker http://www.bobwalker.co.uk

API/Configuration Changes:

  * see AutomatedScreenshots for information about the on-demand screenshots during Android integration tests
  * new and old proguard config options also supported are android.proguard.xyz as properties
```
<proguard>
   <skip>true|false</skip>
   <config>proguard.cfg</config>
   <proguardJarPath>someAbsolutePathToProguardJar</proguardJarPath>
   <filterMavenDescriptor>true|false</filterMavenDescriptor>
   <filterManifest>true|false</filterManifest>
   <jvmArguments>
    <jvmArgument>-Xms256m</jvmArgument>
    <jvmArgument>-Xmx512m</jvmArgument>
  </jvmArguments>
</proguard>
```
  * use external proguard dependency (e.g. 4.7 as deployed to Central Repository)
```
<plugin>
  <groupId>com.jayway.maven.plugins.android.generation2</groupId>
  <artifactId>android-maven-plugin</artifactId>
    <dependencies>
      <dependency>
        <groupId>net.sf.proguard</groupId>
        <artifactId>proguard-base</artifactId>
        <version>4.7</version>
      </dependency>
    </dependencies>
```
  * manifest update goal with new parameters for screens
```
 <manifest>
            <versionName></versionName>
            <versionCode>123</versionCode>
            <versionCodeAutoIncrement>true|false</versionCodeAutoIncrement>
            <versionCodeUpdateFromVersion>true|false</versionCodeUpdateFromVersion>
            <sharedUserId>anId</sharedUserId>
            <debuggable>true|false</debuggable>
            
            <supports-screens>
              <anyDensity>true</anyDensity>
              <xlargeScreens>false</xlargeScreens>
            </supports-screens>
            
            <compatible-screens>
              <compatible-screen>
                <screenSize>small</screenSize>
                <screenDensity>ldpi</screenDensity>
              </compatible-screen>
            </compatible-screens>
          </manifest>
```
### Android Maven Plugin 3.1.1 ###

  * verify required NDK message and bring up useful error messages
    * see https://github.com/jayway/maven-android-plugin/pull/102
    * contributed by Johan Lindquist

### Android Maven Plugin 3.1.0 ###

  * plugin site updated to use fluido skin and new report plugin versions
    * contributed by Manfred Moser http://simpligility.com
  * max heap default to 1Gb for dex command
    * see https://github.com/jayway/maven-android-plugin/pull/81
    * contributed by Jan Berkel
    * see https://github.com/jayway/maven-android-plugin/pull/83
    * contributed by Manfred Moser http://simpligility.com
  * use project.build.outputDirectory instead of assuming classes
    * see https://github.com/jayway/maven-android-plugin/pull/84
    * contributed by Matt Benson https://github.com/mbenson
  * numerous fixes for plugin goal configurations to be possible to define in plugin configuration as well as properties in pom, settings or command line with working over ride, fixed configurations are
    * run
    * pull
    * push
    * instrument (=test)
    * proguard
    * manifest-update
    * see https://github.com/jayway/maven-android-plugin/pull/86
    * contributed by Manfred Moser http://simpligility.com
  * proguard goal enhancemments
    * allow to use different proguard jar from the default in the android sdk (e.g. newer version)
    * specific jvmArguments for proguard independent of other goals
    * see https://github.com/jayway/maven-android-plugin/pull/86
    * contributed by Manfred Moser http://simpligility.com
  * native plugin updates for `r7` of the NDK including updated samples project
    * see https://github.com/jayway/maven-android-plugin/pull/87
    * samples project changes see https://github.com/jayway/maven-android-plugin-samples/pull/22
    * contributed by Johan Lindquist
  * fix for [issue 200](https://code.google.com/p/maven-android-plugin/issues/detail?id=200), allow rebuild of ndk project without clean
    * see https://github.com/jayway/maven-android-plugin/pull/90
    * contributed by Johan Lindquist
  * fix for [issue 240](https://code.google.com/p/maven-android-plugin/issues/detail?id=240) ClassCastException when specifiying test class names
    * see https://github.com/jayway/maven-android-plugin/pull/93
    * contributed by Tristano Costa https://github.com/mrtrix
  * fix for [issue 237](https://code.google.com/p/maven-android-plugin/issues/detail?id=237), ignore optional transitive dependencies
    * see https://github.com/jayway/maven-android-plugin/pull/91
  * fix for [issue 241](https://code.google.com/p/maven-android-plugin/issues/detail?id=241), proguard fails when jdk installed in folder with spaces on Windows
    * see https://github.com/jayway/maven-android-plugin/pull/94
    * contributed by Richard Mortimer https://github.com/oldelvet
  * Fail a device operation if the android.device parameter could not be found.
    * see https://github.com/jayway/maven-android-plugin/pull/99
    * contributed by Richard Mortimer https://github.com/oldelvet
  * Correct javadoc comments for test operation and member references
    * see https://github.com/jayway/maven-android-plugin/pull/98
    * contributed by Richard Mortimer https://github.com/oldelvet
  * upgrade to `r16` of ddmlib
    * see https://github.com/jayway/maven-android-plugin/pull/100
    * contributed by Manfred Moser http://simpligility.com
  * configuration fix for classes/class parameter for instrument (test) mojo
    * see https://github.com/jayway/maven-android-plugin/pull/97
    * contributed by Erik Ogenvik http://erikhjortsberg.blogspot.com

API/Configuration Changes:

  * as mentioned above, overriding of plugin configuration for various goals from properties or command line parameter should now work
  * new proguard config for alternate proguard jar and jvm arguments, also using absolute path to a proguard.cfg should now work
```
<proguard>
  <skip>false</skip>
  <config>proguard.cfg</config>
  <proguardJarPath>someAbsolutePathToProguardJar</proguardJarPath>
  <jvmArguments>
    <jvmArgument>-Xms256m</jvmArgument>
    <jvmArgument>-Xmx512m</jvmArgument>
  </jvmArguments>
</proguard>
```
  * **NDK builds now require NDK `r7`**

### Android Maven Plugin 3.0.0 ###

  * new proguard goal
    * see https://github.com/jayway/maven-android-plugin/pull/78
    * contributed by Jonson, Matthias Käppler http://brainflush.wordpress.com , Hugo Josefson http://about.me/hugojosefson and Manfred Moser http://simpligility.com

Sample project changes:

  * Scala example adapted to new proguard goal
    * contributed by Manfred Moser http://simpligility.com
  * Release profile on morseflash example adapted to new proguard goal
    * contributed by Manfred Moser http://simpligility.com
  * Native transitive dependency example fixed namespace so it works again
    * contributed by Johan Lindquist


API/Configuration Changes:

  * new goal android:proguard, by default disabled, enable with
```
    <proguard><skip>false</skip></proguard>
```
> in the plugin configuration, by default uses a proguard.cfg file as used/created by the Android SDK

### Android Maven Plugin 3.0.0-alpha-14 ###

  * support for statically linked native libraries as dependencies
    * see https://github.com/jayway/maven-android-plugin/pull/73
    * contributed by Johan Lindquist
  * new parameter for aidl classes location "genDirectoryAidl"
    * see https://github.com/jayway/maven-android-plugin/pull/74
    * contributed by Anthony Dahanne http://blog.dahanne.net
  * Support for alternate build script and directory for NDK builds
    * see https://github.com/jayway/maven-android-plugin/pull/77
    * contributed by Johan Lindquist
  * Fix search for native artifacts to respect excluded dependencies
    * see https://github.com/jayway/maven-android-plugin/pull/76
    * contributed by Roberto Tyley http://www.guardian.co.uk/profile/roberto-tyley

Sample project changes:

  * example in the samples project using a statically linked native library
    * see https://github.com/jayway/maven-android-plugin-samples/pull/13
    * see  https://github.com/jayway/maven-android-plugin-samples/pull/12
    * contributed by Johan Lindquist
  * updated example library project to api 10
    * see https://github.com/jayway/maven-android-plugin-samples/pull/11
    * contributed by Luigi Agosti  http://www.luigiagosti.com
  * samples project to no longer start any emulators
    * contributed by Manfred Moser http://simpligility.com
  * new samples project "Support4Demos" using compatibility library example
    * contributed by Manfred Moser http://simpligility.com
  * replaced android 1.5 ApiDemos example project with same project from 2.3.4 (platform 10)
    * contributed by Manfred Moser http://simpligility.com
  * explicitly forcing test reporting on in samples project on and adding all other test parameters in comment to showcase/test
    * contributed by Manfred Moser http://simpligility.com

API/Configuration Changes:
  * new parameter **genDirectoryAidl** to specify target folder for aidl classes generated
  * new parameter to specify alternate ndk build file **android.ndk.ndk-build-executable**
  * new parameter to specify build directory for ndk build step **android.ndk.ndk-build-directory**

### Android Maven Plugin 3.0.0-alpha-13 ###

  * improved error message for apkbuilder
    * see https://github.com/jayway/maven-android-plugin/pull/69
    * contributed by Mykola Nikishov https://manandbytes.wordpress.com/
  * Fix for transient dependency issue with native libs
    * see https://github.com/jayway/maven-android-plugin/pull/70
    * contributed by Johan Lindquist
  * Example for transient dependency with native libs
    * see https://github.com/jayway/maven-android-plugin-samples/pull/10/
    * contributed by Johan Lindquist
  * fix to changed call for apk tool in Android SDK `r14`
    * see https://github.com/jayway/maven-android-plugin/pull/71
    * contributed by Erik Ogenvik http://erikhjortsberg.blogspot.com

### Android Maven Plugin 3.0.0-alpha-12 ###

  * upgraded to `r13` of ddmlib, that is now available in central
    * special thanks to Ladislav Thon and Robert Manning
    * contributed by Manfred Moser,  http://simpligility.com

  * refactored configuration for dex and run goals, updated lots of documentation, cleaned up so parameters work from command line, properties, pom file and settings file
    * see https://github.com/jayway/maven-android-plugin/commit/c8f49952391ffdb77696d762132a90f39a3079a6
    * contributed by Manfred Moser,  http://simpligility.com
  * android.test.debug value can be empty and defaults to auto then
    * see https://github.com/jayway/maven-android-plugin/commit/c8f49952391ffdb77696d762132a90f39a3079a6
    * contributed by Manfred Moser,  http://simpligility.com
  * support for directories in the pull goal
    * fixes [issue 205](https://code.google.com/p/maven-android-plugin/issues/detail?id=205)
    * see https://github.com/jayway/maven-android-plugin/pull/66
    * contributed by Roman Zimmer http://sprylab.com
  * pull and push mojo now support nested configuration in the pom following the codeconvention
    * see https://github.com/jayway/maven-android-plugin/pull/67
    * contributed by Manfred Moser,  http://simpligility.com
  * fix for test report file names when using Android x86 remotely
    * see https://github.com/jayway/maven-android-plugin/pull/68
    * contributed by Alex V

Samples project changes:

  * update morseflash example setup to use the manifest-update goal for debuggable and versionCodeAutoIncrement
    * contributed by Manfred Moser,  http://simpligility.com

API/Configuration Changes

  * run configuration now nested in pom and using parameter android.run.debug for command line or run.debug for property
```
<run>
    <debug>true</debug>
</run>
```
  * dex configuration now nested and so on like run config
```
<dex>
  <jvmArguments>
    <jvmArgument>-Xms256m</jvmArgument>
    <jvmArgument>-Xmx512m</jvmArgument>
  </jvmArguments> 
  <coreLibrary>true|false</coreLibrary>
  <noLocals>true|false</noLocals>
  <optimize>true|false</optimize>
</dex>
```
  * push configuration now nested and so on like run config
```
<push>
    <source>path</source>
    <destination>path</destination>
</push>
```
  * pull configuration now nested and so on like run config
```
<pull>
    <source>path</source>
    <destination>path</destination>
</pull>
```

### Android Maven Plugin 3.0.0-alpha-11 ###

  * refactored name of plugin to **android-maven-plugin**
    * **THIS MEANS ALL USERS MUST UPDATE THEIR POMS**
      * In your projects, change all `<artifactId>maven-android-plugin</artifactId>` to **`<artifactId>android-maven-plugin</artifactId>`**.
      * See also [PluginRenamed](PluginRenamed.md) for further information.
    * see [Issue 198](https://code.google.com/p/maven-android-plugin/issues/detail?id=198)
    * contributed by Manfred Moser,  http://simpligility.com

API/Configuration Changes:
  * renamed all plugin configuration from `<artifactId>maven-android-plugin</artifactId>` to **`<artifactId>android-maven-plugin</artifactId>`**


---


### Maven Android Plugin 3.0.0-alpha-11 ###

  * This is the last 3.x-series release under the name `maven-android-plugin`. From now on, the plugin is known as `android-maven-plugin`. See above.
  * Added forward-pointing relocation meta-data to artifactId `android-maven-plugin`.
    * contributed by Hugo Josefson

### Maven Android Plugin 3.0.0-alpha-10 ###

(not released)

### Maven Android Plugin 3.0.0-alpha-9 ###

  * Wait for the initial device list to be loaded from the Android Debug Bridge before proceeding to deploy and other tasks using adb
    * see https://github.com/jayway/maven-android-plugin/pull/61
    * fixes [issue 197](https://code.google.com/p/maven-android-plugin/issues/detail?id=197)
    * contributed by oldelvet

  * **Require Maven 3.0.3.**
    * see https://groups.google.com/d/topic/maven-android-developers/7vTpCUdgPD0/discussion
    * contributed by Hugo Josefson

  * Allow to push directories to the device
    * fixes [issue 192](https://code.google.com/p/maven-android-plugin/issues/detail?id=192)
    * see https://github.com/jayway/maven-android-plugin/pull/63
    * contributed by Roman Zimmer http://sprylab.com

  * Start apk with debug flag for run goal
    * fixes [issue 199](https://code.google.com/p/maven-android-plugin/issues/detail?id=199)
    * see https://github.com/jayway/maven-android-plugin/pull/64
    * contributed by cherrydev
    * modified to work with plugin configuration parameter by Manfred Moser,  http://simpligility.com

  * fixed StringIndexOutOfBoundException when instrumentation test report AssertionError
    * contributed by Manfred Moser,  http://simpligility.com

  * support for all instrumentation test configuration parameters to be supplied as properties or in plugin configuration
    * contributed by Manfred Moser,  http://simpligility.com

  * refactored enableIntegrationTest parameter to android.test.skip
    * contributed by Manfred Moser,  http://simpligility.com

  * internal refactor of all pure config pojos into separate package and other cleanup
    * contributed by Manfred Moser,  http://simpligility.com

  * refactored configuration parameters for manifest update mojo to be contained in `<manifest>` element
    * contributed by Manfred Moser,  http://simpligility.com

API/Configuration Changes:

  * **Upgrade to Maven 3.0.3+**
  * support for debug parameter for run goal as android.run.debug as property value in pom, settings or command line or in plugin configuration as
```
<configuration><run><debug>true|false</debug></run></configuration>
```
  * refactored **enableIntegrationTest** parameter to **android.test.skip** also see next...
  * support for test configuration parameters to be supplied in pom like so
```
<configuration>
<test>
  <skip>true|false|auto</skip>
  <instrumentationPackage>packageName</instrumentationPackage>
  <instrumentationRunner>className</instrumentationRunner>
  <debug>true|false</debug>
  <coverage>true|false</coverage>
  <logOnly>true|false</logOnly>  avd
  <testSize>small|medium|large</testSize>
  <createReport>true|false</createReport>
  <classes>
    <class>your.package.name.YourTestClass</class>
  </classes>
  <packages>
    <package>your.package.name</package>
  </packages>
</test>
</configuration>
```
  * changed manifest update configuration to be contained in element in pom like so
```
<configuration>
  <manifest>
    <versionName></versionName>
    <versionCode>123</versionCode>
    <versionCodeAutoIncrement>true|false</versionCodeAutoIncrement>
    <versionCodeUpdateFromVersion>true|false</versionCodeUpdateFromVersion>
    <sharedUserId>anId</sharedUserId>
    <debuggable>true|false</debuggable>
  </manifest>
</configuration>
```
or have the manifest as part of the configuration property like e.g.
android.manifest.debuggable or android.manifest.sharedUserId

### Maven Android Plugin 3.0.0-alpha-8 ###

(not released)

### Maven Android Plugin 3.0.0-alpha-7 ###

  * improved naming for devices in logging and unit report file name
    * see https://github.com/jayway/maven-android-plugin/pull/58
    * contributed by Manfred Moser,  http://simpligility.com

  * support for emulator name in android.device parameter
    * see https://github.com/jayway/maven-android-plugin/pull/58
    * contributed by Manfred Moser,  http://simpligility.com

  * fix to avoid ArrayIndexOutOfBoundsException in NDK build
    * see https://github.com/jayway/maven-android-plugin/pull/59
    * fixes [issue 189](https://code.google.com/p/maven-android-plugin/issues/detail?id=189)
    * contributed by Dominik Hiltbrunner

  * merged VersionsUpdateMojo into more generic new ManifestUpdateMojo
    * see https://github.com/jayway/maven-android-plugin/pull/52
    * contributed by Nik Strong http://www.codepoets.co.nz

  * new mojo to stop all attached emulators, stop emulators with adb bridge, possibility to start multiple emulators from command line, this should work flawlessly on Windows now too!!
    * see https://github.com/jayway/maven-android-plugin/pull/60 and a few separate commits in master by Manfred following the merge
    * should fix [issue 4](https://code.google.com/p/maven-android-plugin/issues/detail?id=4)
    * contributed by Bryan O'Neil  and Manfred Moser,  http://simpligility.com


API/Configuration Changes:

  * support for emulator name (e.g. emulator-5554) in android.device parameter
  * new manifest update mojo replacing the version update mojo:

Updates various version attributes present in the AndroidManifest.xml file.
You can configure this mojo to update the following manifest attributes:

android:versionName on the manifest element. android:versionCode on the manifest element. android:sharedUserId on the manifest element. android:debuggable on the application element.

Note: This process will reformat the AndroidManifest.xml per JAXP Transformer defaults if updates are made to the manifest.

Updating Your android:debuggable attribute
```
  <plugin>
    <groupId>com.jayway.maven.plugins.android.generation2</groupId>
    <artifactId>maven-android-plugin</artifactId>
    <executions>
      <execution>
        <id>update-manifest</id>
        <goals>
          <goal>manifest-update</goal>
        </goals>
        <configuration>
          <debuggable>true</debuggable>
        </configuration>
      </execution>
    </executions>
  </plugin>
```

  * new goal to stop all emulators, try mvn **android:emulator-stop-all**

### Maven Android Plugin 3.0.0-alpha-6 ###
  * new parameter `optimize`. Defaults to `true`. Setting to `false` may make the build faster.
    * see https://github.com/jayway/maven-android-plugin/pull/56
    * contributed by Lorenzo Villani

API/Configuration Changes:

  * new **optimize** boolean parameter.

### Maven Android Plugin 3.0.0-alpha-5 ###

  * failure of test run result in build failure
    * see https://github.com/jayway/maven-android-plugin/pull/55
    * contributed by Roberto Tyley http://www.guardian.co.uk/profile/roberto-tyley
  * Pull goal will automatically create target folder
    * see https://github.com/jayway/maven-android-plugin/pull/51
    * contributed by Nic Strong http://www.codepoets.co.nz

API/Configuration Changes:
> none

### Maven Android Plugin 3.0.0-alpha-4 ###
  * new goal "help" that will display all goals and their help text or a specific goal and its parameters
    * see https://github.com/jayway/maven-android-plugin/pull/53
    * fixes [Issue 191](https://code.google.com/p/maven-android-plugin/issues/detail?id=191)
    * contributed by Hakan Tandogan https://github.com/hakan42
  * fixed bug in deploy mojo that skipped installing apk when app already there
    * see https://github.com/jayway/maven-android-plugin/pull/54
    * fixes [issue 193](https://code.google.com/p/maven-android-plugin/issues/detail?id=193)
    * contributed by Lorenzo Villani and Manfred Moser

API/Configuration Changes:

  * new **help** goal: try `mvn android:help`

### Maven Android Plugin 3.0.0-alpha-3 ###

  * Improved logging for deploy and undeploy
    * see https://github.com/jayway/maven-android-plugin/commit/8fa9454c5f16d0d0024ad2452088e3a0b622dcf6
    * contributed by Manfred Moser, http://simpligility.com
  * automatically start adb if not running for ddmlib based code like new deploy, undeploy and instrument
    * fixes [issue 176](https://code.google.com/p/maven-android-plugin/issues/detail?id=176)
    * see https://github.com/jayway/maven-android-plugin/pull/42
    * contributed by Roberto Tyley
  * Refactored pull and push goals to use ddmlib, also changed parameter names to not conflict between the two
    * contributed by Manfred Moser,  http://simpligility.com
  * Removed deleteConflictingFiles  parameter as it is no longer needed
    * fixes [issue 182](https://code.google.com/p/maven-android-plugin/issues/detail?id=182)
    * contributed by Manfred Moser,  http://simpligility.com
  * Suppress empty error log line causing wrong reporting in Hudson/Jenkins
    * see https://github.com/jayway/maven-android-plugin/pull/48
    * contributed by oldelvet
  * Declare need for Java 1.6 at build and run time since a 1.6 file IO call is used in the source already
    * see https://github.com/jayway/maven-android-plugin/pull/47
    * contributed by Mykola Nikishov
  * new mojo that can run the application, needs a project and then you can use "mvn android:run", application needs to be deployed
    * see https://github.com/jayway/maven-android-plugin/pull/46
    * contributed by Lorenzo Villani and Manfred Moser
    * fixes [issue 102](https://code.google.com/p/maven-android-plugin/issues/detail?id=102)
  * automatically create a junit compatible xml file for each device/emulator the instrumentation tests run on complete with system and device properties, error messages, stack traces, timing and so on,  files are created in target/surefire-reports
    * [issue 183](https://code.google.com/p/maven-android-plugin/issues/detail?id=183)
    * contributed by Manfred Moser, http://simpligility.com
  * honor flag to undeployBeforeDeploy also for instrumentation test apk
    * [issue 160](https://code.google.com/p/maven-android-plugin/issues/detail?id=160)
    * contributed by Manfred Moser, http://simpligility.com
  * added documentation for jvmArguments parameters for dex command
    * [issue 146](https://code.google.com/p/maven-android-plugin/issues/detail?id=146)
    * contributed by Manfred Moser, http://simpligility.com

API/Configuration Changes:

  * **pull** goal parameters are now **android.pull.source** and **android.pull.destination**
  * **push** goal parameters are now **android.push.source** and **android.push.destination**
  * **deleteConflictingFiles** parameter removed
  * **Java 1.6 now required** to build plugin and to run plugin as well
  * new standalone mojo android:run
  * new parameter android.test.createreport default to true, set to false and junit xml report will not be created

### Maven Android Plugin 3.0.0-alpha-2 ###

  * Fix so that builds won't pass when integration tests fail
    * see https://github.com/jayway/maven-android-plugin/pull/41
    * contributed by Roberto Tyley

### Maven Android Plugin 3.0.0-alpha-1 ###

  * Fix for [Issue 153](https://code.google.com/p/maven-android-plugin/issues/detail?id=153): jvmArguments missing dash
    * contributed by Manfred Moser
  * Fix for [Issue 148](https://code.google.com/p/maven-android-plugin/issues/detail?id=148): correct help documentation for sdk path
    * contributed by Pierre-Yves Ricau
  * New feature: (Un)deploy to all devices
    * the plugin now detects all attached devices and emulators  will deploy and undeploy to all of them. It also honours the usb and emulator parameters as prior support and will respectively deploy to all emulators or all devices. The old behaviour of being stuck in a loop by adb with "Waiting for device" is now gone and replaced with a deployment to all attached devices/emulators.
    * including fix [issue 158](https://code.google.com/p/maven-android-plugin/issues/detail?id=158) and [issue 163](https://code.google.com/p/maven-android-plugin/issues/detail?id=163).
    * contributed by Manfred Moser
  * Improved project website including test coverage, static analysis and more.
    * see https://github.com/jayway/maven-android-plugin/pull/24
    * contributed by Mirko Friedenhagen
  * New standalone plugin  goal "version-update" for updating versionCode and versionNumber in the AndroidManifest.xml.
    * contributed by Joakim Erdfelt
  * Improved detection of Android related packaging types.
    * see https://github.com/jayway/maven-android-plugin/pull/29
    * Contributed by Jake Wharton
  * New NDK support.
    * see https://github.com/jayway/maven-android-plugin/pull/19
    * also merged in the provided samples for NDK projects, see https://github.com/jayway/maven-android-plugin-samples/pull/5
    * contributed by Johan Lindquist
  * Classifier support for apk mojo.
    * see https://github.com/jayway/maven-android-plugin/pull/20
    * contributed by Johan Lindquist
  * Fixed usage of coreLibrary in dex command.
    * see https://github.com/jayway/maven-android-plugin/pull/34
    * contributed by kevinpotgieter
  * Additional config option for apk allowing additional source directories
    * see https://github.com/jayway/maven-android-plugin/pull/23
    * contributed by Lars Poeschel
  * **Remove jar goal from process resources phase**
    * see https://github.com/jayway/maven-android-plugin/pull/36
    * required for M2 Eclipse Android Integration
    * contributed by Ricardo Gladwell
  * Support for extra arguments for aapt ([Issue 165](https://code.google.com/p/maven-android-plugin/issues/detail?id=165))
    * see https://github.com/jayway/maven-android-plugin/pull/35
    * contributed by Fabrizio Giudici
  * **Removed support for Android 1.1 SDK tools** (NOT platform/API)
    * contributed by Manfred Moser
  * Added multi-device support for push, pull and instrumentation test runs
    * see https://github.com/jayway/maven-android-plugin/commit/33e52c75edea2f7d579b3d2517c33356bf77ddca
    * contributed by Hugo Josefson
  * Run instrumentation tests via ddmlib directly rather than adb command
    * see https://github.com/jayway/maven-android-plugin/commit/ecccb4a558e81255c705a5f4053bfbe7e2e06c84
    * contributed by Manfred Moser
  * Support for various parameters for instrumentation test runs
    * contributed by Manfred Moser


API/Configuration Changes:

  * new standalone goal "version-update" with parameters "versionname.update" and "versioncode.autoincrement"
  * new goal ndk-build
    * "ndk.path" parameter for Android NDK support, supports environment variable ANDROID\_NDK\_HOME
    * "ndk.build.native-classifier" parameter
    * "ndk.build.command-line" parameter
    * "ndk.build.clear-native-artifacts" parameter
    * "ndk.build.ndk-output-directory" parameter
    * "nativeLibrariesDirectory" parameter
    * "ndk.build.architecture" parameter, default armeabi
  * "classifier" parameter, when given cause the apk to get a classifier and be an attached build artifact
  * **removed parameter "deleteDataAndCacheDirectoriesOnDevice"** since it is no longer needed

  * new instrumentation test related parameters
    * "test.debug"
    * "test.coverage"
    * "test.logonly"
    * "test.testsize"
    * **changed "instrumentationRunner" to "test.instrumentationRunner"**
    * **changed "instrumentationPackage" to "test.instrumentationPackage"**


## Maven Android Plugin 2.x release series ##

### Maven Android Plugin 2.9.0-beta-5 ###

  * Fix for [Issue 153](https://code.google.com/p/maven-android-plugin/issues/detail?id=153): jvmArguments missing dash,
    * contributed by Manfred Moser
  * Fix for [Issue 148](https://code.google.com/p/maven-android-plugin/issues/detail?id=148): correct help documentation for sdk path,
    * contributed by Pierre-Yves Ricau
  * Support for lazy library unpacking to speed up build. See [issue 120](https://code.google.com/p/maven-android-plugin/issues/detail?id=120)
    * contributed by shivawu.
  * Fix for [issue 118](https://code.google.com/p/maven-android-plugin/issues/detail?id=118) and [issue 143](https://code.google.com/p/maven-android-plugin/issues/detail?id=143)
    * see https://github.com/jayway/maven-android-plugin/pull/32
    * contributed by alecplumb
  * Support for extra arguments for aapt ([Issue 165](https://code.google.com/p/maven-android-plugin/issues/detail?id=165))
    * see https://github.com/jayway/maven-android-plugin/pull/35
    * contributed by Fabrizio Giudici
  * Added apk parameters support "renameInstrumentationTargetPackage"
    * see https://github.com/jayway/maven-android-plugin/pull/38
    * contributed by Rodrigo Munoz


API/Configuration Changes:

  * noLocals (default false), pass --no-locals to dx command
  * lazyLibraryUnpack (default false) only unpack library after a clean build and not when output directory already exists
  * aaptExtraArgs array of string extra arguments to be passed to aapt
  * renameManifestPackage - pass the --rename-manifest-package parameter to aapt
  * renameInstrumentationTargetPackage - pass the --rename-instrumentation-target-package parameter to aapt


### Maven Android Plugin 2.9.0-beta-4 ###

  * Fix for [Issue 147](https://code.google.com/p/maven-android-plugin/issues/detail?id=147): apklib modules aren't deployed
    * ApkLib modules are now deployed to Maven repository when running `mvn deploy` or when performing a Maven release.
    * By Hugo Josefson.
  * Fixed usage of coreLibrary in dex command. See https://github.com/jayway/maven-android-plugin/pull/34 Contributed by kevinpotgieter

### Maven Android Plugin 2.9.0-beta-3 ###

  * Fix for [Issue 137](https://code.google.com/p/maven-android-plugin/issues/detail?id=137): Specifying jvmArguments results in "error: no command specified"
    * `jvmArguments` now work again.
    * Thank you to Roberto Tyley.
  * Fix for [Issue 145](https://code.google.com/p/maven-android-plugin/issues/detail?id=145): Can't release multi-module with apklib
    * When one of your multi-module project's modules is `<packaging>apklib</apklib>`, you had to `mvn install` before, for the other modules to be able to find it. Now `mvn package` works too, even when your local repo is empty.
    * Especially important when performing a Maven release of a multi-module project like that :)
    * By Hugo Josefson.

### Maven Android Plugin 2.9.0-beta-2 ###

  * New feature: [Issue 113](https://code.google.com/p/maven-android-plugin/issues/detail?id=113): Patch for advanced instrumentation settings
    * Allows you to specify which tests to run, via configuration.
    * See description in [Issue 113](https://code.google.com/p/maven-android-plugin/issues/detail?id=113) for usage instructions.
    * Thank you to Marcus.
  * New feature: Added option for using `aapt --custom-package`.
    * For those who know you need it, add `<customPackage>...</customPackage>` to the plugin configuration or `-Dandroid.customPackage=...` to the command line.
    * Thank you to Stéphane Jacquemain.
  * Fix for [Issue 112](https://code.google.com/p/maven-android-plugin/issues/detail?id=112) - The deploy, undeploy and redeploy goals must have no effect on non-APK project
    * Running `mvn android:deploy`/`redeploy`/`undeploy` on a project which is not an APK, now does nothing instead of giving an error.
    * Thank you to Clement Escoffier.
  * Fix for [Issue 115](https://code.google.com/p/maven-android-plugin/issues/detail?id=115) - Build Fails if command path has a space in it
    * Running `mvn install` from a project directory with spaces in it now works.
    * Thank you to David.
  * Fix for resource collisions in apklib projects.
    * Eric Bowman's example should work now, using current release of the plugin: https://github.com/hugojosefson/maven-android-multimodule-example
    * By Hugo Josefson.

### Maven Android Plugin 2.9.0-beta-1 ###

  * New feature - [Issue 96](https://code.google.com/p/maven-android-plugin/issues/detail?id=96): Support for library projects
    * Use `<packaging>apklib</packaging>` for the library project, and `<type>apklib</type>` in the `<dependency>` tag in the app when depending on it.
    * See ApkLib for documentation and samples.
    * Thank you to Nick Maiorana. Some extra patches by Eric Bowman and Hugo Josefson.
  * Made maven-android-plugin easier to build from source for new developers.
    * Removed tests for obsolete Android SDK versions, which are hard to find and install.
  * Fix for [Issue 123](https://code.google.com/p/maven-android-plugin/issues/detail?id=123): Packaging failed when embedded dependencies have duplicate resources
    * Disabled by default, enable with `<extractDuplicates>true</extractDuplicates>`
    * See [Issue 123](https://code.google.com/p/maven-android-plugin/issues/detail?id=123) and linked pull request for more information.
    * Thank you to Clement Escoffier.

### Maven Android Plugin 2.8.4 ###

  * Fix for [Issue 119](https://code.google.com/p/maven-android-plugin/issues/detail?id=119): "aapt: /lib/libz.so.1: no version information available"
    * Works in Amazon's own Linux dist now.
    * By Hugo Josefson

### Maven Android Plugin 2.8.3 ###

  * Re-fix for [Issue 104](https://code.google.com/p/maven-android-plugin/issues/detail?id=104): "Can't find SDK tools on Windows"
    * Issue introduced in version 2.8.1, now fixed even better.
    * Thank you to Nick Maiorana.

### Maven Android Plugin 2.8.2 ###

  * Fix for [Issue 104](https://code.google.com/p/maven-android-plugin/issues/detail?id=104): "Can't find SDK tools on Windows"
    * Issue introduced in version 2.8.1, now fixed.
    * By Hugo Josefson

### Maven Android Plugin 2.8.1 ###

  * Fix for [Issue 103](https://code.google.com/p/maven-android-plugin/issues/detail?id=103): "Use `platform-tools` instead of `platforms/*/tools`"
    * This makes all commands automatically work also with the latest Android SDK `r08` (for Android 2.3 / Gingerbread).
    * By Hugo Josefson

### Maven Android Plugin 2.8.0 ###

  * Fix for [Issue 48](https://code.google.com/p/maven-android-plugin/issues/detail?id=48): "`*`.apksources file contains .svn files"
    * Thank you to Clement Escoffier.
  * Fix for [Issue 49](https://code.google.com/p/maven-android-plugin/issues/detail?id=49): "'assets' files are not included when including one android project as 'apksources' type dependency of another"
    * Thank you to Clement Escoffier.
  * New feature - [Issue 69](https://code.google.com/p/maven-android-plugin/issues/detail?id=69): "Add android:redeploy Goal"
    * `mvn android:redeploy` can now be used as a shortcut for `mvn android:undeploy android:deploy`.
    * Thank you to Clement Escoffier.
  * Fix for [Issue 85](https://code.google.com/p/maven-android-plugin/issues/detail?id=85): "apkbuilder:  THIS TOOL IS DEPRECATED. See --help for more information."
    * Now automatically loads `sdklib.jar` from the Android SDK.
    * Thank you to Clement Escoffier.
  * New feature - [Issue 98](https://code.google.com/p/maven-android-plugin/issues/detail?id=98): "package should produce the signed as well as the unsigned apk"
    * Set `-Dandroid.sign.debug=both` or `<sign><debug>both</debug></sign>` to get both a debug signed and an unsigned apk.
    * Thank you to Mirko Friedenhagen.


### Maven Android Plugin 2.7.0 ###

  * New feature: Native library copying support
    * Includes native libraries in the project's `libs/` directory. Can be changed with parameter `nativeLibrariesDirectory`.
    * Includes native libraries from Maven dependencies, if they are `<type>so</type>`.
    * Hardware architecture is picked up from the `so` artifact's classifier. If none is set, it defaults to `armebi`. (The default hw architecture when no classifier is set, can also be changed with parameter `nativeLibrariesDependenciesHardwareArchitectureDefault`.)
    * Thank you to Johan Lindquist.
  * Fix for [Issue 87](https://code.google.com/p/maven-android-plugin/issues/detail?id=87): zipalign should be skipped on non APK projects
    * Thank you to Clement Escoffier.
  * Fix: Do not get confused by trailing slashes.
    * Thank you to Mirko Friedenhagen.


### Maven Android Plugin 2.6.0 ###

  * Split dex into unpack/dex so something like ProGuard can be inserted.
    * Thank you to Zang MingJie for this patch.
  * Fixed [Issue 72](https://code.google.com/p/maven-android-plugin/issues/detail?id=72): Allows modification of the gen folder.
    * Thank you to Mathieu Carbou for this patch.
  * Obey the `-Dandroid.device=...` and `<device>...</device>` parameters for all adb commands.
    * By Hugo Josefson
  * Fixed [Issue 68](https://code.google.com/p/maven-android-plugin/issues/detail?id=68): Added boolean flag `coreLibrary` to DexMojo to allow for passing the `--core-library` flag to dx.
    * Thank you to Kelsey Francis for the patch.
  * Fix for [Issue 4](https://code.google.com/p/maven-android-plugin/issues/detail?id=4): emulator cannot be stopped on windows because of command params not set correctly in the stop command, also makes sure to start the emulator when the device is connected to the usb, by passing the `-e` option to adb when getting the serial number.
    * Thank you to Chander Pechetty for this patch.
  * Dirty Fix for [Issue 82](https://code.google.com/p/maven-android-plugin/issues/detail?id=82).
    * Better that current situation! Thank you to Mirko Friedenhagen for this patch.
  * Paths on the device or emulator during Pull and Push may be Strings only instead of File as absolutePath is OS-dependant, e.g. on Windows Drive Letters will be added and Backslashes will be used as path separator.
    * Thank you to Mirko Friedenhagen for this patch.
  * Excluded old plexus:plexus-utils
    * Looks like maven-dependency-plugin indirectly depends on some really old version of plexus:plexus-utils, which had groupId different from current org.codehaus.plexus and thus was included together with the new version. The order of dependencies has changed in 3.0-beta-3, and the old/stale plexus-utils causes problems both during the build and at runtime.
    * Thank you to Igor Fedorenko for this patch.
  * Various cleanup and improvements.
    * Thank you to Mirko Friedenhagen and Manfred Moser for these.


### Maven Android Plugin 2.5.2 ###

  * Fixed [Issue 78](https://code.google.com/p/maven-android-plugin/issues/detail?id=78): Platform folder names must be android-x, where x is a number.
    * Now, all subfolders of `<sdk-path>/platforms` with names starting with "`android-`" are valid platform folders. There is no implicit connection between the name of the directories and the platform versions. (The name of the platform version and the api level number are taken from the `source.properties` file.)
    * The plugin looks for platforms in `<sdk-path>/platforms`. Only directories starting with "`android-`" are considered valid. (Maybe we should remove this restriction.) It then looks in the file `source.properties` to find out the api level and the platform name. The level and name will then be matched to what is specified in the pom file.
    * Thank you to Albin Theander for the patch!

### Maven Android Plugin 2.5.1 ###

  * Fixed [Issue 74](https://code.google.com/p/maven-android-plugin/issues/detail?id=74): Dependencies are now processed in the order they stand in the pom.
    * Thank you to Albin Theander for the patch!
  * Updated [plugin documentation for zipalign](http://maven-android-plugin-m2site.googlecode.com/svn/zipalign-mojo.html).
  * Fixed misspelled command-line argument, corrected to `-Dandroid.zipalign.inputApk=...`
    * Thank you to Manfred Moser for the patch!

### Maven Android Plugin 2.5.0 ###

  * New feature: Zipalign goal ([Issue 51](https://code.google.com/p/maven-android-plugin/issues/detail?id=51)).
  * Improved verification of the Android SDK platform and API level.
  * [Issue 4](https://code.google.com/p/maven-android-plugin/issues/detail?id=4): Some more fixes for starting/stopping emulator on Windows.
  * Updated [Samples](Samples.md) to use android.jar from Maven Central, and not requiring Maven Android SDK Deployer.

> Thank you to Manfred Moser for these patches!

> ([Manfred's blog post about this release](http://www.simpligility.com/2010/06/maven-android-plugin-with-zipalign-and-improved-verification/) has more details)


### Maven Android Plugin 2.4.0 ###

  * New feature: [apk configurations](http://maven-android-plugin-m2site.googlecode.com/svn/apk-mojo.html#configurations)
  * Now possible to [skip generating dex and apk](http://maven-android-plugin-m2site.googlecode.com/svn/apk-mojo.html#generateApk), by setting `<generateApk>false</generateApk>`.
    * Thank you to Albin Theander for the patches!

### Maven Android Plugin 2.3.3 ###

  * Basic NDK support: include compiled native libraries to the apk
    * Thank you to Sergey Rudchenko for the patch!
  * Fixed [Issue 57](https://code.google.com/p/maven-android-plugin/issues/detail?id=57) / [Issue 50](https://code.google.com/p/maven-android-plugin/issues/detail?id=50): Dependencies do not get included in apk / maven dependency ksoap2-android reference error
    * This issue affected both EclipseIntegration and command-line builds with Maven 3.
    * Thank you to Ricardo Gladwell for the patch!
  * Google changed how platform directories are named. android-1.1 -> android-2; android-1.5 -> android-3, etc.:
    * Updated unit tests to pass for new version of Android SDK: convention for platforms directory structure has changed. Thank you to Ricardo Gladwell for the patch.
    * Updated pom.xml files in [Samples](Samples.md) to use the new platform directory names too.
    * **Users should edit their pom.xml files, and change the `<sdk><platform>` tags accordingly, if they install the new Android SDK.**

### Maven Android Plugin 2.3.2 ###

  * [Issue 4](https://code.google.com/p/maven-android-plugin/issues/detail?id=4)
    * New support for stopping an emulator on Windows.
      * **We still need someone on Windows to test it!**
      * See [Issue 4](https://code.google.com/p/maven-android-plugin/issues/detail?id=4), and scroll down to "INSTRUCTIONS FOR ANYONE TO TEST ON WINDOWS".
    * Improved support for starting an emulator on Mac in IntelliJ IDEA.
    * Thank you Manfred Moser for the patches!
  * Using newer plugins.

### Maven Android Plugin 2.3.0 ###

  * [Issue 4](https://code.google.com/p/maven-android-plugin/issues/detail?id=4)
    * New support for starting and stopping an emulator on Unix/Linux, and starting an emulator on Windows. Thank you Manfred Moser for this functionality! Documented in the [Maven Android Plugin Goals](http://www.sonatype.com/books/mvnref-book/reference/android-dev-sect-goals.html) section of the book _Maven: The Complete Reference_.
  * Defaulting `<sdk><path>...</path></sdk>` to environment variable `ANDROID_HOME` so that the config parameter is not needed by default. Thank you Manfred Moser for the patch!
  * Require _at least_ Maven 2.2.1, instead of _exactly_ 2.2.1. This should fix an [Eclipse issue discussed on the Maven Android Developers list](http://groups.google.com/group/maven-android-developers/browse_thread/thread/eb48fddd36b0524).
  * Using newer plugins. Now `mvn versions:display-plugin-updates` is happy :)

### Maven Android Plugin 2.2.2 ###

  * Increased configuration possibilities for ApkSourcesDependency. Thank you Albin Theander for the patch!
    * Added the possibility to use several overlay directories instead of just one. This makes it possible to config which ones to use with profiles. To use this feature, just add the following to the plugin configuration:
      * **`<resourceOverlayDirectories>`**
      * **`    <dir>res-overlay-1</dir>`**
      * **`    <dir>res-overlay-2</dir>`**
      * **`</resourceOverlayDirectories>`**
    * If the feature is not used, the old resourceOverlayDirectory parameter is used as before, keeping everything backwards compatible.

  * [Issue 39](https://code.google.com/p/maven-android-plugin/issues/detail?id=39)
    * Improved detection for which projects are instrumentation test projects. Now considers projects without `<instrumentation.../>` tag in them, as non-instrumentationtest projects, and doesn't try to run them as tests.
  * [Issue 41](https://code.google.com/p/maven-android-plugin/issues/detail?id=41)
    * Exclude any `<scope>provided</scope>` dependencies from the built apk file. The android.jar dependencies are/should be such dependencies.


### Maven Android Plugin 2.2.1 ###

  * Bugfixes for features introduced in Maven Android Plugin 2.2.0. Thank you Erik Hjortsberg for your patches!
    * Combine both the local resources and any dependency resources in a combined directory.
    * Added the ability to provide overlay resources. These will need to be put in a directory named "res-overlay". See ApkSourcesDependency.
    * When using the eclipse maven plugin, the `apksources` artifact will point towards a directory (which isn't the correct one). Therefore, when extracting the `apksources` artifact we'll first try to get a jar from the local repository.
    * Fixed bug where the dependency files overwrote the local files (should be the other way around).
  * Require latest [Apache Maven 2.2.1](http://maven.apache.org/download.html) (coincidental version number!) in fixing [Issue 38](https://code.google.com/p/maven-android-plugin/issues/detail?id=38).
  * Pom cleanup. Thank you Manfred Moser for the patch.

### Maven Android Plugin 2.2.0 ###

  * Improved EclipseIntegration support. Thank you to Dietrich Schulten for the patch!
    * Eclipse should now better understand that `<packaging>apk</packaging>` projects are Java projects.
  * Improved EclipseIntegration support. Thank you to Erik Hjortsberg for the patch!
    * When using `<deleteConflictingFiles>true</deleteConflictingFiles>`, only delete those .aidl files which will result in a .java file being auto created.
  * New feature: Possible to set up inter-project dependencies, even for source code, Android resources and assets.
    * It lets you target different devices easier, without having to duplicate code.
    * Useful for when apk's for different devices need to share some code, Android resources and assets, while still having some code/resources/assets different.
    * See ApkSourcesDependency for details and instructions.
  * (Hopefully) Fixes [Issue 31](https://code.google.com/p/maven-android-plugin/issues/detail?id=31): android:dex should work with packaging=jar
    * Added config parameter `<attachJar>true|false</attachJar>` which is `true` by default. It can be disabled if the jar is not desired in the build. Alternatively configured from commandline: `-Dandroid.attachJar=false`
  * (Hopefully) Fixes [Issue 30](https://code.google.com/p/maven-android-plugin/issues/detail?id=30): Generated sources and duplicate attachment in a "mavenized" Eclipse project
    * No longer attaches the jar artifact twice. Attaching the jar can also be disabled
  * Fixes [Issue 28](https://code.google.com/p/maven-android-plugin/issues/detail?id=28): NoClassDefFoundError, but class exists in target/android-classes
    * Adding java classpath resources from project and dependencies to the apk file.
  * Fixes [Issue 33](https://code.google.com/p/maven-android-plugin/issues/detail?id=33): Dealing with META-INF in 3rd party jars
    * Adding java classpath resources from project and dependencies to the apk file.
  * Fixed and added more error messages.


### Maven Android Plugin 2.1.0 ###
  * New feature, fixes [Issue 27](https://code.google.com/p/maven-android-plugin/issues/detail?id=27): RFE: Add posibility to specify the device to deploy to
    * Can be configured with configuration parameter `<device>emulator-5554</device>`
    * Can be configured from command line: `mvn -Dandroid.device=emulator-5554`
    * Special values `usb` and `emulator` can be used instead of serial number, for automatic device detection on USB cable or among started emulators.


### Maven Android Plugin 2.0.0 ###
  * No changes needed since 2.0.0-rc1, just re-releasing as version 2.0.0.
  * The most stable, bug-free, easy-to-use release of any Maven plugin for Android app developers we know about!


---


## Maven Android Plugin 2.x pre-releases ##

Changes which require action are marked as **bold**.


### Maven Android Plugin 2.0.0-rc1 ###
  * Closes input/output streams.
    * Thank you to Martin Vyšný for the patch.
    * This fixes [Masa Issue 27](http://code.google.com/p/masa/issues/detail?id=27), but in this project.

### Maven Android Plugin 2.0.0-alpha9 ###
  * [Issue 6](https://code.google.com/p/maven-android-plugin/issues/detail?id=6): look over parameter names and expressions
    * [mvn site](http://maven-android-plugin-m2site.googlecode.com/svn/plugin-info.html) is updated with new goal names, and their config params.
    * Simplified goals `android:deploy` and `android:deploy-file` into the same goal, `android:deploy`.
    * Simplified goals `android:undeploy-file` and `android:undeploy-package` into the same goal, `android:undeploy`.
    * In goals `android:deploy` and `android:undeploy`:
      * Renamed command-line parameter `-Dfile` to `-Dandroid.file`, for consistency.
    * In goals `android:pull` and `android:push`:
      * Renamed command-line parameter `-Dsource` to `-Dandroid.source`, for consistency.
      * Renamed command-line parameter `-Ddestination` to `-Dandroid.destination`, for consistency.
    * **Renamed config param `<signWithDebugKeystore>true|false</signWithDebugKeystore>` to**
      * **`<sign>`**
      * **`    <debug>true|false|auto</debug>`**
      * **`</sign>`**
    * Removed config param `<sourceDirectory>` for clarity, because it should be configured outside the plugin, like this:
      * `<build>`
      * `    <sourceDirectory>src/main/java</sourceDirectory>`
      * `</build>`

### Maven Android Plugin 2.0.0-alpha8 ###
  * [Issue 6](https://code.google.com/p/maven-android-plugin/issues/detail?id=6): look over parameter names and expressions
    * [mvn site](http://maven-android-plugin-m2site.googlecode.com/svn/plugin-info.html) is updated with new goal names, and their config params.
    * [Glossary](Glossary.md) is updated.
    * Renamed goal `android:deployDependencies` to `android:deploy-dependencies`.
      * **Renamed config param `<undeployApkBeforeDeploying>` to `<undeployBeforeDeploy>`.**
    * Renamed goal `android:adbPull` to `android:pull`.
      * Renamed config param `<destinationFileOrDirectory>` to `<destination>`.
      * Renamed config param `<sourceFileOrDirectory>` to `<source>`.
      * Improved error handling.
    * Renamed goal `android:adbPush` to `android:push`.
      * Renamed config param `<destinationFileOrDirectory>` to `<destination>`.
      * Renamed config param `<sourceFileOrDirectory>` to `<source>`.
      * Improved error handling.
    * Renamed goal `android:undeploy-packageName` to `android:undeploy-package`.
      * Renamed config param `<packageName>` to `<package>`.
      * Renamed config param `-Dpackage` to `-Dandroid.package`.
      * Resolve config param `<package>`/`-Dandroid.package` from `AndroidManifest.xml` if not defined.
    * Renamed goal `android:platformTest` to `android:instrument`.
      * Renamed config param `<testsPackage>` to `<testPackage>`.
      * Renamed config param `<testPackage>` to `<instrumentationPackage>`.
      * Renamed config param `<testRunner>` to `<instrumentationRunner>`.
      * Renamed config param `-Dandroid.test.testPackage` to `-Dandroid.instrumentationPackage`.
      * Renamed config param `-Dandroid.test.testRunner` to `-Dandroid.instrumentationRunner`.
    * In goal `android:generate-sources`:
      * Removed parameter `createPackageDirectories` for clarity, and because we currently have no known use case for setting it to `false`.
    * Samples: Renamed apidemos-`*`-platformtests to apidemos-`*`-instrumentationtest.



### Maven Android Plugin 2.0.0-alpha7 ###
  * [Issue 25](https://code.google.com/p/maven-android-plugin/issues/detail?id=25): `mvn android:deploy` doesn't work
    * Now it does :)

### Maven Android Plugin 2.0.0-alpha6 ###
  * [Issue 24](https://code.google.com/p/maven-android-plugin/issues/detail?id=24): mvn install fails on Windows for `<packaging>android:apk:platformTest</packaging>`
    * MAJOR CHANGE: Solving this had to result in a major change in how poms are defined. It really was necessary for fixing this issue. Can't be done without changing the `<packaging>` to something without ":", so it's best to do it all at once now while we're still in alpha.
    * The change is that all Android application poms and all Android platformTest poms will have to have **`<packaging>apk</packaging>`** instead of the separate `<packaging>android:apk</packaging>` and `<packaging>android:apk:platformTest</packaging>` which they've had before. Also, of course, if the platformTest pom has a dependency to another apk, that `<dependency>` will now have to be **`<type>apk</type>`** instead of `<type>android:apk</type>`.
    * `<packaging>apk</packaging>` also makes more sense, especially when comparing to other packaging types such as jar, war and so on...
  * Updated [Samples](Samples.md) to reflect the fixed [Issue 24](https://code.google.com/p/maven-android-plugin/issues/detail?id=24).
  * Because both application and platformTest poms have the same `<packaging>` now, Maven Android Plugin autodetects whether to enable integration test goals when going through the `integration-test` phase. The autodetection is based on whether it finds any test classes (those which extend `junit.framework.*` or `android.test.*`) in your application. It looks in both the project's source directory and any jar dependencies brought in, which will be included in the apk.
  * Test class autodetection can be overridden with the config parameter `<enableIntegrationTest>true|false|auto</enableIntegrationTest>`.


### Maven Android Plugin 2.0.0-alpha5 ###
  * [Issue 23](https://code.google.com/p/maven-android-plugin/issues/detail?id=23): PlatformTestMojo requires PATH
    * Doesn't expect PATH to be set. Uses tools in the configured sdk instead. (fixed in one more place)

### Maven Android Plugin 2.0.0-alpha4 ###
  * [Issue 21](https://code.google.com/p/maven-android-plugin/issues/detail?id=21): Run standalone goals (without pom)
    * It is now possible to run standalone goals (such as `android:undeploy-file`) directly from commandline, without having a pom with the required config parameter `<sdk><path>...` in it. It can instead be set on commandline with the `-Dandroid.sdk.path` parameter.
  * Improved error messages for missing sdk path: added suggestions for configuration options.
  * [Issue 19](https://code.google.com/p/maven-android-plugin/issues/detail?id=19): Created DeploymentInstructions wiki page
  * [Issue 16](https://code.google.com/p/maven-android-plugin/issues/detail?id=16): Add site, source:jar, javadoc:jar to release configuration

### Maven Android Plugin 2.0.0-alpha3 ###
  * [Issue 1](https://code.google.com/p/maven-android-plugin/issues/detail?id=1): Support for Android SDK 1.5!
    * Thank you to Andreas Ronge for the initial patch.
  * No longer requires any magic environment variables!
    * **Instead, a mandatory configuration parameter was added:**
```
   <artifactId>maven-android-plugin</artifactId>
   <version>2.0.0-alpha3</version>
   <configuration>
       <sdk>
           <path>/opt/android-sdk-linux_x86-1.5_r2</path>
       </sdk>
   </configuration>
```
    * If you want, you can set it using an environment variable, as done in the [Samples](Samples.md), for example `${env.MY_ANDROID_SDK_LOCATION`}. Then you will have to set that environment variable to the location where you installed Android SDK 1.5r2.
    * You also have the option of setting it in a parent pom instead, with `<pluginManagement>`. Then you can skip including the `<sdk><path>` in your project pom altogether!
    * This also means you can use different specific Android SDK's for different projects.
    * This change was made to make the plugin feel like less magic. Now you know that any environment variables you set, are only for yourself. The plugin doesn't read them; it only reads its configuration parameters.
    * This fixes [Masa Issue 26](http://code.google.com/p/masa/issues/detail?id=26), but in this project.
  * Duplicated the sample `apidemos` application into `apidemos-11` with code from the Android SDK 1.1, and `apidemos-15` with code from the Android SDK 1.5. They use, and will work with, their corresponding Android SDK. Use `apidemos-15` for Android SDK 1.5r2.
  * More and updated documentation, both wiki and in code.
  * More tests in code.

### Maven Android Plugin 2.0.0-alpha2 ###
  * Doesn't expect PATH to be set too. Uses ANDROID\_SDK/tools instead. (fixed in one more place)
  * Split out samples to a separate git repo.

### Maven Android Plugin 2.0.0-alpha1 ###

First release of the new implementation of Maven Android Plugin.

Implemented all changes listed in [this email with suggestions sent to the Masa Developers list](http://groups.google.com/group/masa-developers/browse_thread/thread/732fb629ec917cd4), except number 11 (done as of 2.0.0-alpha3) and number 12 (ongoing as [Issue 6](https://code.google.com/p/maven-android-plugin/issues/detail?id=6) here, please give feedback on that).

Some of the details implemented:
  * Collected all plugins into one, for clarity and maintainability.
  * Refactored **a lot** of code for maintainability and clarity.
  * Separate the act of deploying an apk into a goal of its own (`mvn android:deploy`). This fixes [Masa Issue 20](http://code.google.com/p/masa/issues/detail?id=20), but in this project.
  * When running the `integration-test` phase for a `<packaging>android:apk:platformTest</packaging>` pom, automatically deploy the platform test apk, as well as the apk to test, onto the device before. This fixes [Masa Issue 21](http://code.google.com/p/masa/issues/detail?id=21), but in this project.
  * Optionally undeploy each apk from the device before deploying it. This helps the issue where different developers with different debug keys use the same device and try to install an apk with the same package id. They would collide if the first one is not undeployed before the other is deployed on top of it.
  * Make as much as possible automatically configured, if possible. For example reading the package id from inside an apk file or AndroidManifest.xml (whichever is available), instead of the user having to define it when for example undeploying an apk.
  * Added a sample Maven application (ApiDemos) as an example of using Maven Android Plugin, and as a test for the plugin. This fixes [Masa Issue 11](http://code.google.com/p/masa/issues/detail?id=11), but in this project.
  * Improved documentation.
  * Added unit testing.
  * Added error messages.
  * Updated dependencies' versions.
  * Removed the PAR plugin. It can be added again if requested.
  * Fine-tuned phases and made lifecycle more like the default lifecycle for `<packaging>jar</packaging>`. This fixes [Masa Issue 14](http://code.google.com/p/masa/issues/detail?id=14), but in this project.
  * Renamed many things to names which say what they do.
  * Renamed `install` to `deploy`, because that's what it's usually called in Maven-world, and because `install` has a very specific (other) meaning.
  * Also delete `Manifest.java` when deleting `R.java`.
  * Added goals `deploy-file` and `undeploy-file` for (un)deploying any separate apk outside of any project.
  * Added goal `undeploy-packageName` for undeploying an apk from device, if you already know the package name.
  * Config parameter platformtestrunner class can be inferred from `AndroidManifest.xml: /manifest//instrumentation/@android:name`.
  * Standalone goals should not require a project.
  * Doesn't expect PATH to be set too. Uses ANDROID\_SDK/tools instead.
  * Set up release management procedures to enable frequent releases.
  * Started preparing for syncing to Maven Central, so we won't need to specify `<pluginRepository>` in the pom.xml when it's set up.



---

> #### _About the Maven Android Plugin versions history_ ####

> _Maven Android Plugin was originally based on the Masa plugins 1.0.0. Thank you to Shane Isbell for creating Masa ([http://code.google.com/p/masa](http://code.google.com/p/masa))! Maven Android Plugin 1.x was a direct clone of Masa's trunk. It was meant as an easy way for any current user of Masa 1.0.0 to get access to the latest unreleased bug fixes in Masa's trunk._

> Maven Android Plugin 2.x has since been reworked and greatly improved in terms of bugfixing, features and ease-of-use, compared to version 1.

> <b>Versions 2.x are recommended for all users.</b>


---


## Maven Android Plugin 1.x release series ##

### Maven Android Plugin 1.0.2 ###
Released by this project (Maven Android Plugin), based on [Masa svn revision 63](http://code.google.com/p/masa/source/list), which includes fixes for the following:

  * ~~[Masa Issue 4](http://code.google.com/p/masa/issues/detail?id=4)~~: Not possible to set finalName
  * ~~[Masa Issue 15](http://code.google.com/p/masa/issues/detail?id=15)~~: NullPointerException when localRepository not set
  * ~~[Masa Issue 16](http://code.google.com/p/masa/issues/detail?id=15)~~: IntelliJ IDEA does not pick up generated-sources
  * ~~[Masa Issue 17](http://code.google.com/p/masa/issues/detail?id=15)~~: apk file not attached properly to build
  * ~~[Masa Issue 18](http://code.google.com/p/masa/issues/detail?id=15)~~: assets not included
  * ~~[Masa Issue 19](http://code.google.com/p/masa/issues/detail?id=15)~~: Not possible to specify jvm parameters to dx



---


## Masa plugins 1.0.0 ##
Released by the Masa project, based on [Masa svn revision 56](http://code.google.com/p/masa/source/list).