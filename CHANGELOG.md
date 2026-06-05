# Change log

## 6.1.0 (Jun 5, 2026)

### Changes

* Upgraded minimum Java version from 11 to 21 (LTS).
* Switched `maven.compiler.source`/`target` to `maven.compiler.release`.
* Added GitHub Actions CI workflow.
* Added Maven Wrapper (pinned to Maven 3.9.9).
* Added Dependabot configuration for Maven and GitHub Actions.

### Dependency upgrades

* SLF4J `1.7.36` → `2.0.18`.
* Logback `1.4.14` → `1.5.32`.
* WireMock `2.27.2` → `3.13.2` (new coordinates: `org.wiremock:wiremock`).
* TestNG `7.7.0` → `7.10.2`.
* REST Assured `4.4.0` → `5.5.7`.
* Guava `32.1.2-jre` → `33.6.0-jre`.
* Google HTTP Client `1.44.2` → `1.47.1`.
* JaCoCo `0.8.12` → `0.8.13`.
* Maven Javadoc Plugin `3.4.1` → `3.12.0`.
* Maven Source Plugin `3.2.1` → `3.4.0`.
* Maven JAR Plugin `3.3.0` → `3.5.0`.
* Maven Bundle Plugin `5.1.2` → `5.1.9`.
* Maven Enforcer Plugin `3.1.0` → `3.6.3`.
* Maven Compiler Plugin → `3.14.0`.
* Maven Surefire Plugin → `3.5.3`.
* Apache HttpClient 5 `5.2.1` → `5.4.4`.
* Apache HttpCore 5 `5.2.1` → `5.3.4`.

## 6.0.3 (Sep 29, 2025)

### Fixes

* Fixed a transitive vulnerability by adding the `netty-bom` module with version `4.2.6.Final`.
* Fixed a transitive vulnerability by adding the `commons-lang3` module with version `3.18.0`.
* Upgraded `dependency-check` to `12.1.6` to fix the build issue.

## 6.0.2 (Apr 10, 2025)

### Fixes

* Fixed a vulnerability by upgrading the `asynchttpclient` module to `3.0.2`.
* Upgraded `dependency-check` to `12.1.0` to fix the build issue.

## 6.0.1 (Dec 17, 2024)

### Fixes

* Fixed a vulnerability by upgrading the `asynchttpclient` module to `3.0.1`.
* Removed checks in the `AsyncHttpClientEdgeGridRequestSigner` class for the `ReactiveStreamsBodyGenerator` case, which is no longer available in a new version of the `asynchttpclient` module.
* Fixed some build errors by upgrading the JaCoCo library.

## 6.0.0 (Aug 21, 2024)

### BREAKING CHANGES

* Replaced the deprecated `ApacheHttpTransport` method with `com.google.api.client.http.apache.v2.ApacheHttpTransport` in the `edgegrid-signer-google-http-client` module.
* Updated the `README.md` file for the `edgegrid-signer-google-http-client` module to include changes in the instructions for signing HTTP requests with specified client credentials.

### Improvements

* Added support for `ProxySelector` in the `ApacheHttpClientEdgeGridRoutePlanner` method to enable the use of custom proxy servers.

### Fixes

* Fixed various vulnerabilities by upgrading `grpc-context`, `netty`, and `commons-configuration2`.
* Fixed an issue when a path param is a url for rest-assured.


## 5.1.1 (Dec 6, 2023)

### Fixes

* Fixed various CVE vulnerabilities by upgrading logback classic, netty and dependency-check.


## 5.1.0 (Sep 5, 2023)

### Improvements

* Added support for Apache HTTP Client version 5.

### Fixes

* Fixed various CVE vulnerabilities by upgrading netty, dependency-check, and guava libraries.
* Fixed some build errors by upgrading Jacoco library.
* Resolved various Javadoc warnings in different modules.

## 5.0.0 (Jan 19, 2023)

### BREAKING CHANGES

*  Minimum Java version is 11.

## 4.1.2 (Jul 21, 2022)

### Improvements

* Extracted the `edgegrid-signer-gatling` module to a separate project.

### Fixes

* Fixed various vulnerabilities: `OSSRH-66257`, `CVE-2020-36518`, `sonatype-2021-4682`, `CVE-2022-24823`, `sonatype-2019-0673`, `sonatype-2012-0050`, `sonatype-2021-4916`.

## 4.1.1 (Feb 17, 2022)

### Enhancements

* Added OWASP dependency check plugin to maven pipeline.

### Fixes

* Fixed multiple CVE vulnerabilities by upgrading logback and netty dependencies.
* Fixed Travis build by updating Java version to 8.
* Corrected `README.md`'s inconsistencies.

## 4.1.0 (Aug 26, 2021)

### Enhancements

* Upgraded project dependencies.
* Ensured compatibility with Java >= v9.

## 4.0.1

### Fixes

* Fixed Issue #35, a broken unit test.
* Use [`URI#getRawPath()`](https://docs.oracle.com/javase/8/docs/api/java/net/URI.html#getRawPath--) when constructing a signature.

## 4.0 (Feb 19, 2019)

### BREAKING CHANGES

* Split the edgerc file reader into a new module [edgerc-reader](edgerc-reader).
* Dropped a dependency on `commons-configuration2` from `edgegrid-signer-core`.
* Dropped a dependency on `commons-lang3`.
* Dropped a dependency on `commons-codec` (use Base64 methods from JDK instead).
* Use maven-bundle-plugin to add `OSGi` headers to `MANIFEST.MF`.

## 3.0 (Aug 8, 2018)

### BREAKING CHANGES

* Minimum Java version is now 8.

### Improvements

* Added binding for Async HTTP Client.
* Added binding for Gatling.

## 2.1 (Jul 27, 2017)

### Improvements

* Added binding for Apache HTTP Client.
* Split `README.md` between relevant modules.

## 2.0 (Jul 27, 2017)

### Improvements

* Added signing algorithm tweaks.
* Separated binding for the Google HTTP Client library for Java from the core signing library.
* Added binding for REST-assured.
* Unit tests with TestNG.
* Published to Maven Central.