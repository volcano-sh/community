## Overview

This document introduces the open source compliance guidelines of the volcano community, aiming to help community developers and users understand and comply with the basic open source compliance guidelines and pass license compliance checks. Follow these basic guidelines when contributing to and using the community.



## Rules

### license basic rules

|                Description                 |                             Rule                             |
| :----------------------------------------: | :----------------------------------------------------------: |
|           Project-level license            |     Place a separate License file in the root directory.     |
|                License name                | Use the unified format [spdx-indentifier.](https://spdx.org/licenses/) |
|       Source file license statement        | License and copyright need to be declared in the source file. |
| Third Party Open Source Software Statement | Store the license for third-party open source software in the licenses folder in the project source code repository. |



### license compliance check

A license compliance CI access control check will be performed when submitting code. There are three types of license selection:

Unrestricted Licenses: Open source software with an unrestricted license can be introduced directly.

Reciprocal Licenses: Open source software with an reciprocal license be used but modifications are not permitted.

Restricted Licenses: Open source software with an restricted license is forbidden to be introduced.

See [license-lint](https://github.com/volcano-sh/volcano/tree/master/config/license-lint.yaml) for more details. 

## Responsibilities

|             Role              |                        responsibility                        |                            member                            |
| :---------------------------: | :----------------------------------------------------------: | :----------------------------------------------------------: |
|          Participant          | Participate in open source policy proposals and discussions, and conduct open source compliance inspection and CI project construction. | Volcano community [member](https://github.com/orgs/volcano-sh/people) |
| Open Source Compliance Expert | Responsible for the compliance review of open source licenses to ensure that licenses introduced into open source are trusted. | [k82cn](https://github.com/k82cn)  [kevin-wangzefeng](https://github.com/kevin-wangzefeng)  [hzxuzhonghu](https://github.com/hzxuzhonghu)  [Thor-wl](https://github.com/Thor-wl)  [william-wang](https://github.com/william-wang)  [shinytang6](https://github.com/shinytang6) |
|   Open source policy makers   | Responsible for formulating and revising open source policies and making decisions on major open source issues. Refer to [https://choosealicense.com/](https://gitee.com/link?target=https%3A%2F%2Flink.zhihu.com%2F%3Ftarget%3Dhttps%3A%2F%2Fchoosealicense.com%2F) to choose the appropriate license for community projects, and fulfill corresponding open source license obligations | [k82cn](https://github.com/k82cn)  [kevin-wangzefeng](https://github.com/kevin-wangzefeng)  [hzxuzhonghu](https://github.com/hzxuzhonghu)  [Thor-wl](https://github.com/Thor-wl)  [william-wang](https://github.com/william-wang)  [shinytang6](https://github.com/shinytang6) |

### Expectations 

They should take corresponding responsibilities to ensure that the licenses introduced by the community comply with open source compliance specifications, and make timely corrections when there are compliance risks. For example, for GPL licenses, relevant open source obligations should be fully fulfilled in open source software compliance projects,  SBOM and source code should be provided in projects. Characters who do not comply with the above behavior can be removed and re-elected.

## Contact

If you have any questions about open source license compliance, please contact us through the following methods.

[Volcano Slack Channel](https://cloud-native.slack.com/archives/C011GJDQS0N) | [Join](https://slack.cncf.io/)

[Mailing List](https://groups.google.com/forum/#!forum/volcano-sh)

