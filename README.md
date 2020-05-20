# android-quality-template

[![ci][1]][2]

A sample project that illustrates integration of code quality tools:

- Checkstyle
- FindBugs
- JDepend
- PMD

The tasks can be run individually, and are integrated with the `check` task:

```groovy
./gradlew check
```

## License

    Copyright 2018 Frieder Bluemle

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.

[1]: https://github.com/fbluemle/android-quality-template/workflows/ci/badge.svg
[2]: https://github.com/fbluemle/android-quality-template/actions
