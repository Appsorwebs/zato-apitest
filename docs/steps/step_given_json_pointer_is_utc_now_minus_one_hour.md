
Given JSON Pointer "{path}" in request is UTC now "{format}" minus one hour
=============================================================================================================

Usage example
-------------

```
Feature: zato-apitest docs

Scenario: Given JSON Pointer "{path}" in request is now "{format}"

    Given address "http://apitest-demo.zato.io"
    Given URL path "/demo/json"
    Given format "JSON"
    Given request is "{}"
    Given JSON Pointer "/a" in request is UTC now "default" minus one hour

    When the URL is invoked

    Then status is "200"
```

Discussion
----------

The format "default" is always available. Its value is "YYYY-MM-DDTHH:mm:ss".
