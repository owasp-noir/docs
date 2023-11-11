---
layout: page
title: Testing
permalink: /contribute/testing
parent: Contribute
nav_order: 4
---

## Testing
Noir manages code quality through both Unit and Functional testing. You can execute test code using Crystal's spec feature.

```bash
# Basic testing
crystal spec

# If you want more detail?
crystal spec -v
```

## Unit Test
Unit tests are defined under `spec/unit_test/` in Noir.

```crystal
# Example

describe "Detect Java Armeria" do
  options = default_options()
  instance = DetectorJavaArmeria.new options

  it "pom.xml" do
    instance.detect("pom.xml", "com.linecorp.armeria").should eq(true)
  end
  it "build.gradle" do
    instance.detect("build.gradle", "com.linecorp.armeria").should eq(true)
  end
end
```

## Functional Test
Functional tests are defined under `spec/functional_test/` in Noir. Functional tests consist of Fixtures and Testers.

- `spec/functional_test/fixtures/*`
- `spec/functional_test/testers/*`

Fixtures involve creating sample code that resembles the actual code under analysis. Testers, on the other hand, use Fixture paths to verify if detection is accurate, the number of discovered endpoints, and whether the expected information matches the detailed information of detected endpoints (such as paths, methods, parameters, etc.).

```crystal
# Example of Rails Analyzer

extected_endpoints = [
  Endpoint.new("/secret.html", "GET"),
  Endpoint.new("/posts", "GET"),
  Endpoint.new("/posts/1", "GET"),
  Endpoint.new("/posts", "POST", [
    Param.new("id", "", "json"),
    Param.new("title", "", "json"),
    Param.new("context", "", "json"),
    Param.new("X-API-KEY", "", "header"),
  ]),
  Endpoint.new("/posts/1", "PUT", [
    Param.new("id", "", "json"),
    Param.new("title", "", "json"),
    Param.new("context", "", "json"),
    Param.new("X-API-KEY", "", "header"),
  ]),
  Endpoint.new("/posts/1", "DELETE"),
]

FunctionalTester.new("fixtures/rails/", {
  :techs     => 1,
  :endpoints => 6,
}, extected_endpoints).test_all
```