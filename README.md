# GitHub for Dart [![Build Status](https://travis-ci.org/DirectMyFile/github.dart.svg)](https://travis-ci.org/DirectMyFile/github.dart)

This is a Client Library for GitHub in Dart. I wrote this out of necessity, and then when I got a great reaction from the Dart community, I decided to put a lot of effort into it.

Please submit issues and pull requests, join my IRC channel (#directcode on irc.esper.net), help out, or just give me encouragement.

**Notice**: We are looking for major contributors. Contact us by email or on IRC!

## Links

- [Library Demos](http://github.directcode.org/demos/)
- [Pub Package](https://pub.dartlang.org/packages/github)

## Features

### Current

- Works on the Server and in the Browser
- Really Fast
- Plugable API
- Supports Authentication
- Builtin OAuth2 Flow
- Hook Server Helper

### Work in Progress

- Support all the GitHub APIs (Progress: 98%)

## Getting Started

First, add the following to your pubspec.yaml:

```yaml
dependencies:
  github: ">=0.6.2 <1.0.0"
```

Then import the library and use it:

**For the Server**
```dart
import 'package:github/server.dart';

void main() {
  /* Required to setup GitHub */
  initGitHub();
  var github = new GitHub();
  github.repository(new RepositorySlug("DirectMyFile", "github.dart")).then((Repository repo) {
    /* Do Something */
  });
}
```

**For the Browser**
```dart
import 'package:github/browser.dart';

void main() {
  /* Required to setup GitHub */
  initGitHub();
  
  var github = new GitHub();
  github.repository(new RepositorySlug("DirectMyFile", "github.dart")).then((Repository repo) {
    /* Do Something */
  });
}
```

## Authentication

To use a GitHub token:

```dart
var github = new GitHub(auth: new Authentication.withToken("YourTokenHere"));
```

## Contacting Us

You can find us on `irc.esper.net` at `#directcode`.
