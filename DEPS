# Copyright 2010 Google Inc. All Rights Reserved.
# Use of this source code is governed by an Apache-style license that can be
# found in the COPYING file.

vars = {
  "chrev": "@119173"
}

deps = {
  "src/base":
    "http://src.chromium.org/svn/trunk/src/base" + Var("chrev"),

  "src/build":
    "http://src.chromium.org/svn/trunk/src/build" + Var("chrev"),

  "src/third_party/icu":
    "http://src.chromium.org/svn/trunk/deps/third_party/icu42" + Var("chrev"),

  "src/third_party/modp_b64":
    "http://src.chromium.org/svn/trunk/src/third_party/modp_b64" + Var("chrev"),

  "src/third_party/nss":
    "http://src.chromium.org/svn/trunk/deps/third_party/nss" + Var("chrev"),

  "src/third_party/sqlite":
    "http://src.chromium.org/svn/trunk/src/third_party/sqlite" + Var("chrev"),

  "src/third_party/wtl":
    "http://src.chromium.org/svn/trunk/src/third_party/wtl" + Var("chrev"),

  "src/third_party/zlib":
    "http://src.chromium.org/svn/trunk/src/third_party/zlib" + Var("chrev"),

  "src/testing":
    "http://src.chromium.org/svn/trunk/src/testing" + Var("chrev"),

  "src/testing/gmock":
    "http://googlemock.googlecode.com/svn/trunk@374",

  "src/testing/gtest":
    "http://googletest.googlecode.com/svn/trunk@492",

  "src/tools/gyp":
    "http://gyp.googlecode.com/svn/trunk@1233",

  "src/tools/win":
    "http://src.chromium.org/svn/trunk/src/tools/win" + Var("chrev"),

  # If using rlz with chrome's networking library, add it and its dependencies
  # here.
}

include_rules = [
  "+build",
  "+net",  # This is only used when force_rlz_use_chrome_net=1 is passed to gyp.
  "+third_party/zlib",
]

hooks = [
  {
    # A change to a .gyp, .gypi, or to GYP itself should run the generator.
    "pattern": ".",
    "action": ["python", "src/build/gyp_chromium", "src/rlz/rlz.gyp"],
  }
]

