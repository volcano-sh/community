## Overview

This document introduces the open source compliance guidelines of the volcano community, aiming to help community developers and users understand and comply with the basic open source compliance guidelines and pass license compliance checks. Follow these basic guidelines when contributing to and using the community.

## Concepts

### Contributor License

There are two types of open source contributor agreements: CLA and DCO.

#### CLA 

A Contributor License Agreement (CLA) is a contributor license agreement that has legal effects to ensure that the project/organization has the necessary copyright and patent license rights for all contributions, thereby allowing the project /organization to distribute the project. It can deal with project organizational risks, avoid uncertainty, create a harmonious contribution environment, and ensure that contributors understand their rights and obligations when participating in project contributions.

#### DCO

A Developer Certificate of Origin(DCO) is developed by the Linux Foundation. The advantage of DCO is that it is relatively simple. You only need to sign your email address when submitting a PR.

Contributors are required to sign a contributor agreement when submitting a PR. Signing a contributor agreement has the following purposes:

- The copyright of the works or codes contributed to the community is granted to the project owner to facilitate the maintenance and management of the project.
- Provide the community with guarantees and disclaimers for the use of works or codes to avoid potential legal risks.

### Copyright

Copyright is a series of "exclusive" rights that an author enjoys legally over a certain work. It has the following characteristics:

- Enjoy it naturally without applying
- Protect expression (excluding the ideas behind it)
- Covers software, books, music, movies, etc. and other similar works

### License

A license is a way for the owner of a copyright to grant rights to others. It can be understood as a "contract". What are the characteristics of this "contract": it does not need to be signed by both parties, and it comes into effect when the user uses the software licensed under the license.

The terms of the license consist of rights, obligations, and restrictions:

- Rights: What you can do with the software.
- Obligations: what kind of obligations you must fulfill when you use the software.
- Restrictions: what you cannot do

Common types of License include:

- Free and open source license
- Commercial license
- Other non-FOSS licenses
- Creative commons

#### Common open source license list

Common licenses and their standards are listed here.

|                          Full name                           |              Identifier              | FSF Free? | OSI Approved? | oE Approved? | Restricted Use? |
| :----------------------------------------------------------: | :----------------------------------: | :-------: | :-----------: | :----------: | :-------------: |
|                      3dfx Glide License                      |                Glide                 |           |               |              |                 |
|                       Abstyles License                       |               Abstyles               |           |               |              |                 |
|                  Academic Free License v1.1                  |               AFL-1.1                |     Y     |       Y       |      Y       |                 |
|                  Academic Free License v1.2                  |               AFL-1.2                |     Y     |       Y       |      Y       |                 |
|                  Academic Free License v2.0                  |               AFL-2.0                |     Y     |       Y       |      Y       |                 |
|                  Academic Free License v2.1                  |               AFL-2.1                |     Y     |       Y       |      Y       |                 |
|                  Academic Free License v3.0                  |               AFL-3.0                |     Y     |       Y       |      Y       |                 |
|       Academy of Motion Picture Arts and Sciences BSD        |                AMPAS                 |           |               |              |                 |
|                 Adaptive Public License 1.0                  |               APL-1.0                |           |       Y       |      Y       |                 |
|                   Adobe Glyph List License                   |             Adobe-Glyph              |           |               |              |                 |
|           Affero General Public License v1.0 only            |            AGPL-1.0-only             |           |               |              |                 |
|         Affero General Public License v1.0 or later          |          AGPL-1.0-or-later           |           |               |              |                 |
|                       Afmparse License                       |               Afmparse               |           |               |      Y       |                 |
|                 Aladdin Free Public License                  |               Aladdin                |           |               |              |                 |
|                   AMD's plpa_map.c License                   |               AMDPLPA                |           |               |              |                 |
|                 ANTLR Software Rights Notice                 |               ANTLR-PD               |           |               |      Y       |                 |
|      ANTLR Software Rights Notice with license fallback      |          ANTLR-PD-fallback           |           |               |              |                 |
|                      Apache License 1.0                      |              Apache-1.0              |     Y     |               |      Y       |                 |
|                      Apache License 1.1                      |              Apache-1.1              |     Y     |       Y       |      Y       |                 |
|                      Apache License 2.0                      |              Apache-2.0              |     Y     |       Y       |      Y       |                 |
|                       App::s2p License                       |               App-s2p                |           |               |              |                 |
|                      Apple MIT License                       |                 AML                  |           |               |              |                 |
|               Apple Public Source License 1.0                |               APSL-1.0               |           |       Y       |      Y       |                 |
|               Apple Public Source License 1.1                |               APSL-1.1               |           |       Y       |      Y       |                 |
|               Apple Public Source License 1.2                |               APSL-1.2               |           |       Y       |      Y       |                 |
|               Apple Public Source License 2.0                |               APSL-2.0               |     Y     |       Y       |      Y       |                 |
|                    Arphic Public License                     |             Arphic-1999              |           |               |      Y       |                 |
|                     Artistic License 1.0                     |             Artistic-1.0             |           |       Y       |              |        Y        |
|                 Artistic License 1.0 (Perl)                  |          Artistic-1.0-Perl           |           |       Y       |      Y       |                 |
|               Artistic License 1.0 w/clause 8                |           Artistic-1.0-cl8           |           |       Y       |      Y       |                 |
|                     Artistic License 2.0                     |             Artistic-2.0             |     Y     |       Y       |      Y       |                 |
|                Attribution Assurance License                 |                 AAL                  |           |       Y       |      Y       |                 |
|                       Beerware License                       |               Beerware               |           |               |              |        Y        |
|                     Bison exception 2.2                      |         Bison-exception-2.2          |           |               |              |                 |
|             BitTorrent Open Source License v1.0              |            BitTorrent-1.0            |           |               |              |                 |
|             BitTorrent Open Source License v1.1              |            BitTorrent-1.1            |     Y     |               |      Y       |                 |
|                 Blue Oak Model License 1.0.0                 |            BlueOak-1.0.0             |           |               |              |                 |
|                  Boost Software License 1.0                  |               BSL-1.0                |     Y     |       Y       |      Y       |                 |
|                     BSD 1-Clause License                     |             BSD-1-Clause             |           |       Y       |      Y       |                 |
|              BSD 2-Clause "Simplified" License               |             BSD-2-Clause             |           |       Y       |      Y       |                 |
|               BSD 2-Clause with views sentence               |          BSD-2-Clause-Views          |           |               |      Y       |                 |
|           BSD 3-Clause "New" or "Revised" License            |             BSD-3-Clause             |     Y     |       Y       |      Y       |                 |
|                  BSD 3-Clause Clear License                  |          BSD-3-Clause-Clear          |     Y     |               |      Y       |                 |
|                  BSD 3-Clause Modification                   |      BSD-3-Clause-Modification       |           |               |      Y       |                 |
|                BSD 3-Clause Open MPI variant                 |        BSD-3-Clause-Open-MPI         |           |               |      Y       |                 |
|                    BSD 4 Clause Shortened                    |        BSD-4-Clause-Shortened        |           |               |              |                 |
|           BSD 4-Clause "Original" or "Old" License           |             BSD-4-Clause             |     Y     |               |      Y       |                 |
|                    BSD Protection License                    |            BSD-Protection            |           |               |      Y       |                 |
|                 BSD Source Code Attribution                  |           BSD-Source-Code            |           |               |              |                 |
|                     BSD with attribution                     |       BSD-3-Clause-Attribution       |           |               |      Y       |                 |
|                   BSD Zero Clause License                    |                 0BSD                 |           |       Y       |      Y       |                 |
|               BSD-2-Clause Plus Patent License               |         BSD-2-Clause-Patent          |           |       Y       |      Y       |                 |
|       BSD-4-Clause (University of California-Specific)       |           BSD-4-Clause-UC            |           |               |      Y       |                 |
|                 Business Source License 1.1                  |               BUSL-1.1               |           |               |              |                 |
|              bzip2 and libbzip2 License v1.0.5               |             bzip2-1.0.5              |           |               |      Y       |                 |
|              bzip2 and libbzip2 License v1.0.6               |             bzip2-1.0.6              |           |               |      Y       |                 |
|         CeCILL Free Software License Agreement v2.0          |              CECILL-2.0              |     Y     |               |      Y       |                 |
|         CeCILL Free Software License Agreement v2.1          |              CECILL-2.1              |           |       Y       |      Y       |                 |
|           CeCILL-B Free Software License Agreement           |               CECILL-B               |     Y     |               |      Y       |                 |
|           CeCILL-C Free Software License Agreement           |               CECILL-C               |     Y     |               |      Y       |                 |
|               CERN Open Hardware Licence v1.1                |             CERN-OHL-1.1             |           |               |              |                 |
|               CERN Open Hardware Licence v1.2                |             CERN-OHL-1.2             |           |               |              |                 |
|      CERN Open Hardware Licence Version 2 - Permissive       |            CERN-OHL-P-2.0            |           |       Y       |      Y       |                 |
|  CERN Open Hardware Licence Version 2 - Strongly Reciprocal  |            CERN-OHL-S-2.0            |           |       Y       |      Y       |                 |
|   CERN Open Hardware Licence Version 2 - Weakly Reciprocal   |            CERN-OHL-W-2.0            |           |       Y       |      Y       |                 |
|                  Clarified Artistic License                  |              ClArtistic              |     Y     |               |      Y       |                 |
|                   Classpath exception 2.0                    |       Classpath-exception-2.0        |           |               |              |                 |
|                     CLISP exception 2.0                      |         CLISP-exception-2.0          |           |               |              |                 |
|                         CMU License                          |               MIT-CMU                |           |               |      Y       |                 |
|                     CNRI Jython License                      |             CNRI-Jython              |           |               |              |                 |
|                     CNRI Python License                      |             CNRI-Python              |           |       Y       |      Y       |                 |
|                Code Project Open License 1.02                |              CPOL-1.02               |           |               |              |                 |
|       Common Development and Distribution License 1.0        |               CDDL-1.0               |     Y     |       Y       |      Y       |                 |
|       Common Development and Distribution License 1.1        |               CDDL-1.1               |           |               |      Y       |                 |
|               Common Documentation License 1.0               |               CDL-1.0                |           |               |              |                 |
|            Common Public Attribution License 1.0             |               CPAL-1.0               |     Y     |       Y       |      Y       |                 |
|                  Common Public License 1.0                   |               CPL-1.0                |     Y     |       Y       |      Y       |                 |
|     Computer Associates Trusted Open Source License 1.1      |              CATOSL-1.1              |           |       Y       |      Y       |                 |
|                  Condor Public License v1.1                  |              Condor-1.1              |     Y     |               |      Y       |                 |
|               Copyfree Open Innovation License               |               COIL-1.0               |           |               |              |                 |
|                     copyleft-next 0.3.0                      |         copyleft-next-0.3.0          |           |               |              |                 |
|           Creative Commons Attribution 1.0 Generic           |              CC-BY-1.0               |           |               |      Y       |                 |
|           Creative Commons Attribution 2.5 Generic           |              CC-BY-2.5               |           |               |      Y       |                 |
|           Creative Commons Attribution 3.0 Austria           |             CC-BY-3.0-AT             |           |               |              |                 |
|        Creative Commons Attribution 3.0 United States        |             CC-BY-3.0-US             |           |               |              |                 |
|          Creative Commons Attribution 3.0 Unported           |              CC-BY-3.0               |           |               |      Y       |                 |
|        Creative Commons Attribution 4.0 International        |              CC-BY-4.0               |     Y     |               |      Y       |                 |
|   Creative Commons Attribution No Derivatives 1.0 Generic    |             CC-BY-ND-1.0             |           |               |              |                 |
|   Creative Commons Attribution No Derivatives 2.0 Generic    |             CC-BY-ND-2.0             |           |               |              |                 |
|   Creative Commons Attribution No Derivatives 2.5 Generic    |             CC-BY-ND-2.5             |           |               |              |                 |
|   Creative Commons Attribution No Derivatives 3.0 Germany    |           CC-BY-ND-3.0-DE            |           |               |              |                 |
|   Creative Commons Attribution No Derivatives 3.0 Unported   |             CC-BY-ND-3.0             |           |               |              |                 |
| Creative Commons Attribution No Derivatives 4.0 International |             CC-BY-ND-4.0             |           |               |              |                 |
|   Creative Commons Attribution Non Commercial 1.0 Generic    |             CC-BY-NC-1.0             |           |               |              |                 |
|   Creative Commons Attribution Non Commercial 2.0 Generic    |             CC-BY-NC-2.0             |           |               |              |                 |
|   Creative Commons Attribution Non Commercial 2.5 Generic    |             CC-BY-NC-2.5             |           |               |              |                 |
|   Creative Commons Attribution Non Commercial 3.0 Germany    |           CC-BY-NC-3.0-DE            |           |               |              |                 |
|   Creative Commons Attribution Non Commercial 3.0 Unported   |             CC-BY-NC-3.0             |           |               |              |                 |
| Creative Commons Attribution Non Commercial 4.0 International |             CC-BY-NC-4.0             |           |               |              |                 |
| Creative Commons Attribution Non Commercial No Derivatives 1.0 Generic |           CC-BY-NC-ND-1.0            |           |               |              |                 |
| Creative Commons Attribution Non Commercial No Derivatives 2.0 Generic |           CC-BY-NC-ND-2.0            |           |               |              |                 |
| Creative Commons Attribution Non Commercial No Derivatives 2.5 Generic |           CC-BY-NC-ND-2.5            |           |               |              |                 |
| Creative Commons Attribution Non Commercial No Derivatives 3.0 Germany |          CC-BY-NC-ND-3.0-DE          |           |               |              |                 |
| Creative Commons Attribution Non Commercial No Derivatives 3.0 IGO |         CC-BY-NC-ND-3.0-IGO          |           |               |              |                 |
| Creative Commons Attribution Non Commercial No Derivatives 3.0 Unported |           CC-BY-NC-ND-3.0            |           |               |              |                 |
| Creative Commons Attribution Non Commercial No Derivatives 4.0 International |           CC-BY-NC-ND-4.0            |           |               |              |                 |
| Creative Commons Attribution Non Commercial Share Alike 1.0 Generic |           CC-BY-NC-SA-1.0            |           |               |              |                 |
| Creative Commons Attribution Non Commercial Share Alike 2.0 England and Wales |          CC-BY-NC-SA-2.0-UK          |           |               |              |                 |
| Creative Commons Attribution Non Commercial Share Alike 2.0 Generic |           CC-BY-NC-SA-2.0            |           |               |              |                 |
| Creative Commons Attribution Non Commercial Share Alike 2.5 Generic |           CC-BY-NC-SA-2.5            |           |               |              |                 |
| Creative Commons Attribution Non Commercial Share Alike 3.0 Germany |          CC-BY-NC-SA-3.0-DE          |           |               |              |                 |
| Creative Commons Attribution Non Commercial Share Alike 3.0 IGO |         CC-BY-NC-SA-3.0-IGO          |           |               |              |                 |
| Creative Commons Attribution Non Commercial Share Alike 3.0 Unported |           CC-BY-NC-SA-3.0            |           |               |              |                 |
| Creative Commons Attribution Non Commercial Share Alike 4.0 International |           CC-BY-NC-SA-4.0            |           |               |              |                 |
|     Creative Commons Attribution Share Alike 1.0 Generic     |             CC-BY-SA-1.0             |           |               |      Y       |                 |
| Creative Commons Attribution Share Alike 2.0 England and Wales |           CC-BY-SA-2.0-UK            |           |               |              |                 |
|     Creative Commons Attribution Share Alike 2.0 Generic     |             CC-BY-SA-2.0             |           |               |              |                 |
|      Creative Commons Attribution Share Alike 2.1 Japan      |           CC-BY-SA-2.1-JP            |           |               |              |                 |
|     Creative Commons Attribution Share Alike 2.5 Generic     |             CC-BY-SA-2.5             |           |               |              |                 |
|     Creative Commons Attribution Share Alike 3.0 Austria     |           CC-BY-SA-3.0-AT            |           |               |              |                 |
|     Creative Commons Attribution Share Alike 3.0 Germany     |           CC-BY-SA-3.0-DE            |           |               |              |                 |
|    Creative Commons Attribution Share Alike 3.0 Unported     |             CC-BY-SA-3.0             |           |               |      Y       |                 |
|  Creative Commons Attribution Share Alike 4.0 International  |             CC-BY-SA-4.0             |     Y     |               |      Y       |                 |
| Creative Commons Attribution-NonCommercial-ShareAlike 2.0 France |          CC-BY-NC-SA-2.0-FR          |           |               |              |                 |
| Creative Commons Public Domain Dedication and Certification  |               CC-PDDC                |           |               |              |                 |
|             Creative Commons Zero v1.0 Universal             |               CC0-1.0                |     Y     |               |      Y       |                 |
|                      Crossword License                       |              Crossword               |           |               |              |                 |
|              Cryptographic Autonomy License 1.0              |               CAL-1.0                |           |       Y       |      Y       |                 |
| Cryptographic Autonomy License 1.0 (Combined Work Exception) |   CAL-1.0-Combined-Work-Exception    |           |       Y       |      Y       |                 |
|                    CrystalStacker License                    |            CrystalStacker            |           |               |              |                 |
|                CUA Office Public License v1.0                |             CUA-OPL-1.0              |           |       Y       |      Y       |                 |
|                         Cube License                         |                 Cube                 |           |               |              |                 |
|                  Detection Rule License 1.0                  |               DRL-1.0                |           |               |              |                 |
|         Do What The F*ck You Want To Public License          |                WTFPL                 |     Y     |               |      Y       |                 |
|                         DOC License                          |                 DOC                  |           |               |              |                 |
|                       dvipdfm License                        |               dvipdfm                |           |               |              |                 |
|                  Eclipse Public License 1.0                  |               EPL-1.0                |     Y     |       Y       |      Y       |                 |
|                  Eclipse Public License 2.0                  |               EPL-2.0                |     Y     |       Y       |      Y       |                 |
|                      eCos exception 2.0                      |          eCos-exception-2.0          |           |               |              |                 |
|              Educational Community License v1.0              |               ECL-1.0                |           |       Y       |      Y       |                 |
|              Educational Community License v2.0              |               ECL-2.0                |     Y     |       Y       |      Y       |                 |
|               eGenix.com Public License 1.1.0                |                eGenix                |           |               |              |                 |
|                  Eiffel Forum License v1.0                   |               EFL-1.0                |           |       Y       |      Y       |                 |
|                  Eiffel Forum License v2.0                   |               EFL-2.0                |     Y     |       Y       |      Y       |                 |
|                         enna License                         |               MIT-enna               |           |               |              |                 |
|                 Entessa Public License v1.0                  |               Entessa                |           |       Y       |      Y       |                 |
|                      EPICS Open License                      |                EPICS                 |           |               |              |                 |
|                   Etalab Open License 2.0                    |              etalab-2.0              |           |               |              |                 |
|                 EU DataGrid Software License                 |              EUDatagrid              |     Y     |       Y       |      Y       |                 |
|              European Union Public License 1.0               |               EUPL-1.0               |           |               |              |                 |
|              European Union Public License 1.1               |               EUPL-1.1               |     Y     |       Y       |      Y       |                 |
|              European Union Public License 1.2               |               EUPL-1.2               |           |       Y       |      Y       |                 |
|                       Eurosym License                        |               Eurosym                |           |               |              |                 |
|                         Fair License                         |                 Fair                 |           |       Y       |      Y       |                 |
|                   Fawkes Runtime Exception                   |       Fawkes-Runtime-exception       |           |               |              |                 |
|                         feh License                          |               MIT-feh                |           |               |              |                 |
|                        FLTK exception                        |            FLTK-exception            |           |               |              |                 |
|                      Font exception 2.0                      |          Font-exception-2.0          |           |               |              |                 |
|                  Frameworx Open License 1.0                  |            Frameworx-1.0             |           |       Y       |      Y       |                 |
|               Fraunhofer FDK AAC Codec Library               |               FDK-AAC                |           |               |              |                 |
|                FreeBSD Documentation License                 |             FreeBSD-DOC              |           |               |              |                 |
|                FreeImage Public License v1.0                 |              FreeImage               |           |               |              |                 |
|                    FreeRTOS Exception 2.0                    |        freertos-exception-2.0        |           |               |              |                 |
|                   Freetype Project License                   |                 FTL                  |     Y     |               |      Y       |                 |
|                  FSF All Permissive License                  |                FSFAP                 |     Y     |               |      Y       |                 |
|                    FSF Unlimited License                     |                FSFUL                 |           |               |              |        Y        |
|        FSF Unlimited License (with License Retention)        |               FSFULLR                |           |               |              |        Y        |
|                        GL2PS License                         |                GL2PS                 |           |               |      Y       |                 |
|                        Glulxe License                        |                Glulxe                |           |               |              |                 |
|         GNU Affero General Public License v3.0 only          |            AGPL-3.0-only             |     Y     |       Y       |      Y       |                 |
|       GNU Affero General Public License v3.0 or later        |          AGPL-3.0-or-later           |     Y     |       Y       |      Y       |                 |
|           GNU Free Documentation License v1.1 only           |            GFDL-1.1-only             |     Y     |               |      Y       |                 |
|    GNU Free Documentation License v1.1 only - invariants     |       GFDL-1.1-invariants-only       |           |               |              |                 |
|   GNU Free Documentation License v1.1 only - no invariants   |     GFDL-1.1-no-invariants-only      |           |               |              |                 |
|         GNU Free Documentation License v1.1 or later         |          GFDL-1.1-or-later           |     Y     |               |      Y       |                 |
|  GNU Free Documentation License v1.1 or later - invariants   |     GFDL-1.1-invariants-or-later     |           |               |              |                 |
| GNU Free Documentation License v1.1 or later - no invariants |   GFDL-1.1-no-invariants-or-later    |           |               |              |                 |
|           GNU Free Documentation License v1.2 only           |            GFDL-1.2-only             |     Y     |               |      Y       |                 |
|    GNU Free Documentation License v1.2 only - invariants     |       GFDL-1.2-invariants-only       |           |               |              |                 |
|   GNU Free Documentation License v1.2 only - no invariants   |     GFDL-1.2-no-invariants-only      |           |               |              |                 |
|         GNU Free Documentation License v1.2 or later         |          GFDL-1.2-or-later           |     Y     |               |      Y       |                 |
|  GNU Free Documentation License v1.2 or later - invariants   |     GFDL-1.2-invariants-or-later     |           |               |              |                 |
| GNU Free Documentation License v1.2 or later - no invariants |   GFDL-1.2-no-invariants-or-later    |           |               |              |                 |
|           GNU Free Documentation License v1.3 only           |            GFDL-1.3-only             |     Y     |               |      Y       |                 |
|    GNU Free Documentation License v1.3 only - invariants     |       GFDL-1.3-invariants-only       |           |               |              |                 |
|   GNU Free Documentation License v1.3 only - no invariants   |     GFDL-1.3-no-invariants-only      |           |               |      Y       |                 |
|         GNU Free Documentation License v1.3 or later         |          GFDL-1.3-or-later           |     Y     |               |      Y       |                 |
|  GNU Free Documentation License v1.3 or later - invariants   |     GFDL-1.3-invariants-or-later     |           |               |              |                 |
| GNU Free Documentation License v1.3 or later - no invariants |   GFDL-1.3-no-invariants-or-later    |           |               |              |                 |
|             GNU General Public License v1.0 only             |             GPL-1.0-only             |           |               |      Y       |                 |
|           GNU General Public License v1.0 or later           |           GPL-1.0-or-later           |           |               |      Y       |                 |
|             GNU General Public License v2.0 only             |             GPL-2.0-only             |     Y     |       Y       |      Y       |                 |
|           GNU General Public License v2.0 or later           |           GPL-2.0-or-later           |     Y     |       Y       |      Y       |                 |
|             GNU General Public License v3.0 only             |             GPL-3.0-only             |     Y     |       Y       |      Y       |                 |
|           GNU General Public License v3.0 or later           |           GPL-3.0-or-later           |     Y     |       Y       |      Y       |                 |
|                    GNU JavaMail exception                    |        gnu-javamail-exception        |           |               |              |                 |
|         GNU Lesser General Public License v2.1 only          |            LGPL-2.1-only             |     Y     |       Y       |      Y       |                 |
|       GNU Lesser General Public License v2.1 or later        |          LGPL-2.1-or-later           |     Y     |       Y       |      Y       |                 |
|         GNU Lesser General Public License v3.0 only          |            LGPL-3.0-only             |     Y     |       Y       |      Y       |                 |
|       GNU Lesser General Public License v3.0 or later        |          LGPL-3.0-or-later           |     Y     |       Y       |      Y       |                 |
|          GNU Library General Public License v2 only          |            LGPL-2.0-only             |           |       Y       |      Y       |                 |
|        GNU Library General Public License v2 or later        |          LGPL-2.0-or-later           |           |       Y       |      Y       |                 |
|                       gnuplot License                        |               gnuplot                |     Y     |               |              |                 |
|              Good Luck With That Public License              |                GLWTPL                |           |               |              |                 |
|                GPL Cooperation Commitment 1.0                |              GPL-CC-1.0              |           |               |              |                 |
|                  GPL-3.0 Linking Exception                   |      GPL-3.0-linking-exception       |           |               |              |                 |
|    GPL-3.0 Linking Exception (with Corresponding Source)     |   GPL-3.0-linking-source-exception   |           |               |              |                 |
|                  gSOAP Public License v1.3b                  |              gSOAP-1.3b              |           |               |      Y       |                 |
|               Haskell Language Report License                |            HaskellReport             |           |               |              |                 |
|                   Hippocratic License 2.1                    |           Hippocratic-2.1            |           |               |              |                 |
|         Historical Permission Notice and Disclaimer          |                 HPND                 |     Y     |       Y       |      Y       |                 |
|  Historical Permission Notice and Disclaimer - sell variant  |          HPND-sell-variant           |           |               |      Y       |                 |
|                   IBM Public License v1.0                    |               IPL-1.0                |     Y     |       Y       |      Y       |                 |
|                         ICU License                          |                 ICU                  |           |               |      Y       |                 |
|                     ImageMagick License                      |             ImageMagick              |           |               |      Y       |                 |
|          iMatix Standard Function Library Agreement          |                iMatix                |     Y     |               |      Y       |                 |
|                        Imlib2 License                        |                Imlib2                |     Y     |               |      Y       |                 |
|                Independent JPEG Group License                |                 IJG                  |     Y     |               |      Y       |                 |
|                       Info-ZIP License                       |               Info-ZIP               |           |               |              |                 |
|            Intel ACPI Software License Agreement             |              Intel-ACPI              |           |               |              |                 |
|                  Intel Open Source License                   |                Intel                 |     Y     |       Y       |      Y       |                 |
|                Interbase Public License v1.0                 |            Interbase-1.0             |           |               |      Y       |                 |
|                       IPA Font License                       |                 IPA                  |     Y     |       Y       |      Y       |                 |
|                         ISC License                          |                 ISC                  |     Y     |       Y       |      Y       |                 |
|                         Jam License                          |                 Jam                  |           |       Y       |      Y       |                 |
|           Japan Network Information Center License           |                JPNIC                 |           |               |              |                 |
|                        JasPer License                        |              JasPer-2.0              |           |               |      Y       |                 |
|                         JSON License                         |                 JSON                 |           |               |              |                 |
|                  KiCad Libraries Exception                   |      KiCad-libraries-exception       |           |               |              |                 |
|              LaTeX Project Public License v1.0               |               LPPL-1.0               |           |               |              |                 |
|              LaTeX Project Public License v1.1               |               LPPL-1.1               |           |               |              |                 |
|              LaTeX Project Public License v1.2               |               LPPL-1.2               |     Y     |               |      Y       |                 |
|              LaTeX Project Public License v1.3a              |              LPPL-1.3a               |     Y     |               |      Y       |                 |
|              LaTeX Project Public License v1.3c              |              LPPL-1.3c               |           |       Y       |      Y       |                 |
|                       Latex2e License                        |               Latex2e                |           |               |              |                 |
|     Lawrence Berkeley National Labs BSD variant license      |          BSD-3-Clause-LBNL           |           |       Y       |      Y       |                 |
|                      Leptonica License                       |              Leptonica               |           |               |      Y       |                 |
|    Lesser General Public License For Linguistic Resources    |                LGPLLR                |           |               |              |                 |
|                  LGPL-3.0 Linking Exception                  |      LGPL-3.0-linking-exception      |           |               |              |                 |
|                        libpng License                        |                Libpng                |           |               |      Y       |                 |
|               libselinux public domain notice                |            libselinux-1.0            |           |               |      Y       |                 |
|                       libtiff License                        |               libtiff                |           |               |      Y       |                 |
|                      Libtool Exception                       |          Libtool-exception           |           |               |              |                 |
|                    Licence Art Libre 1.2                     |               LAL-1.2                |           |               |              |                 |
|                    Licence Art Libre 1.3                     |               LAL-1.3                |           |               |              |                 |
|       Licence Libre du Québec – Permissive version 1.1       |             LiLiQ-P-1.1              |           |       Y       |      Y       |                 |
|   Licence Libre du Québec – Réciprocité forte version 1.1    |           LiLiQ-Rplus-1.1            |           |       Y       |      Y       |                 |
|      Licence Libre du Québec – Réciprocité version 1.1       |             LiLiQ-R-1.1              |           |       Y       |      Y       |                 |
|          Linux Kernel Variant of OpenIB.org license          |             Linux-OpenIB             |           |               |      Y       |                 |
|                   Linux man-pages Copyleft                   |       Linux-man-pages-copyleft       |           |               |      Y       |                 |
|                 Lucent Public License v1.02                  |               LPL-1.02               |     Y     |       Y       |      Y       |                 |
|              Lucent Public License Version 1.0               |               LPL-1.0                |           |       Y       |      Y       |                 |
|                      MakeIndex License                       |              MakeIndex               |           |               |              |                 |
|               Matrix Template Library License                |                 MTLL                 |           |               |              |                 |
|                   Microsoft Public License                   |                MS-PL                 |     Y     |       Y       |      Y       |                 |
|                 Microsoft Reciprocal License                 |                MS-RL                 |     Y     |       Y       |      Y       |                 |
|                MIT +no-false-attribs license                 |                MITNFA                |           |               |      Y       |                 |
|                         MIT License                          |                 MIT                  |     Y     |       Y       |      Y       |                 |
|                  MIT License Modern Variant                  |          MIT-Modern-Variant          |           |       Y       |      Y       |                 |
|                      MIT No Attribution                      |                MIT-0                 |           |       Y       |      Y       |                 |
|                    MIT Open Group variant                    |            MIT-open-group            |           |               |      Y       |                 |
|                       Motosoto License                       |               Motosoto               |           |       Y       |      Y       |                 |
|                  Mozilla Public License 1.0                  |               MPL-1.0                |           |       Y       |      Y       |                 |
|                  Mozilla Public License 1.1                  |               MPL-1.1                |     Y     |       Y       |      Y       |                 |
|                  Mozilla Public License 2.0                  |               MPL-2.0                |     Y     |       Y       |      Y       |                 |
|      Mozilla Public License 2.0 (no copyleft exception)      |    MPL-2.0-no-copyleft-exception     |           |       Y       |      Y       |                 |
|         Mulan Permissive Software License, Version 1         |             MulanPSL-1.0             |           |               |      Y       |                 |
|         Mulan Permissive Software License, Version 2         |             MulanPSL-2.0             |           |       Y       |      Y       |                 |
|                       Multics License                        |               Multics                |           |       Y       |      Y       |                 |
|                         Mup License                          |                 Mup                  |           |               |              |                 |
|   Nara Institute of Science and Technology License (2003)    |              NAIST-2003              |           |               |      Y       |                 |
|                NASA Open Source Agreement 1.3                |               NASA-1.3               |           |       Y       |      Y       |                 |
|                    Naumen Public License                     |                Naumen                |           |       Y       |      Y       |                 |
|                        NetCDF license                        |                NetCDF                |           |               |      Y       |                 |
|                Nethack General Public License                |                 NGPL                 |           |       Y       |      Y       |                 |
|                 Netizen Open Source License                  |                 NOSL                 |     Y     |               |      Y       |                 |
|                 Netscape Public License v1.0                 |               NPL-1.0                |     Y     |               |      Y       |                 |
|                 Netscape Public License v1.1                 |               NPL-1.1                |     Y     |               |      Y       |                 |
|                       Newsletr License                       |               Newsletr               |           |               |              |                 |
|                  NIST Public Domain Notice                   |               NIST-PD                |           |               |      Y       |                 |
|                  Nokia Open Source License                   |                Nokia                 |     Y     |       Y       |      Y       |                 |
|              Non-Commercial Government Licence               |             NCGL-UK-2.0              |           |               |              |                 |
|             Non-Profit Open Software License 3.0             |              NPOSL-3.0               |           |       Y       |      Y       |                 |
|          Norwegian Licence for Open Government Data          |               NLOD-1.0               |           |               |              |                 |
|    Norwegian Licence for Open Government Data (NLOD) 2.0     |               NLOD-2.0               |           |               |              |                 |
|                        Noweb License                         |                Noweb                 |           |               |              |                 |
|                         NRL License                          |                 NRL                  |           |               |              |                 |
|                         NTP License                          |                 NTP                  |           |       Y       |      Y       |                 |
|                      NTP No Attribution                      |                NTP-0                 |           |               |      Y       |                 |
|                 OCaml LGPL Linking Exception                 |     OCaml-LGPL-linking-exception     |           |               |              |                 |
|               OCLC Research Public License 2.0               |               OCLC-2.0               |           |       Y       |      Y       |                 |
|              OGC Software License, Version 1.0               |               OGC-1.0                |           |               |              |                 |
|                  Open CASCADE Exception 1.0                  |          OCCT-exception-1.0          |           |               |              |                 |
|            Open CASCADE Technology Public License            |               OCCT-PL                |           |               |              |                 |
|          Open Data Commons Attribution License v1.0          |              ODC-By-1.0              |           |               |              |                 |
|         Open Data Commons Open Database License v1.0         |               ODbL-1.0               |     Y     |               |      Y       |                 |
|   Open Data Commons Public Domain Dedication & License 1.0   |               PDDL-1.0               |           |               |              |                 |
|               Open Government Licence - Canada               |            OGL-Canada-2.0            |           |               |              |                 |
|                 Open Government Licence v1.0                 |              OGL-UK-1.0              |           |               |              |                 |
|                 Open Government Licence v2.0                 |              OGL-UK-2.0              |           |               |              |                 |
|                 Open Government Licence v3.0                 |              OGL-UK-3.0              |           |               |              |                 |
|                Open Group Test Suite License                 |                OGTSL                 |           |       Y       |      Y       |                 |
|                Open LDAP Public License 2.2.2                |             OLDAP-2.2.2              |           |               |      Y       |                 |
|                Open LDAP Public License v1.1                 |              OLDAP-1.1               |           |               |      Y       |                 |
|                Open LDAP Public License v1.2                 |              OLDAP-1.2               |           |               |      Y       |                 |
|                Open LDAP Public License v1.3                 |              OLDAP-1.3               |           |               |      Y       |                 |
|                Open LDAP Public License v1.4                 |              OLDAP-1.4               |           |               |      Y       |                 |
|  Open LDAP Public License v2.0 (or possibly 2.0A and 2.0B)   |              OLDAP-2.0               |           |               |      Y       |                 |
|               Open LDAP Public License v2.0.1                |             OLDAP-2.0.1              |           |               |      Y       |                 |
|                Open LDAP Public License v2.1                 |              OLDAP-2.1               |           |               |      Y       |                 |
|                Open LDAP Public License v2.2                 |              OLDAP-2.2               |           |               |      Y       |                 |
|               Open LDAP Public License v2.2.1                |             OLDAP-2.2.1              |           |               |      Y       |                 |
|                Open LDAP Public License v2.3                 |              OLDAP-2.3               |     Y     |               |      Y       |                 |
|                Open LDAP Public License v2.4                 |              OLDAP-2.4               |           |               |      Y       |                 |
|                Open LDAP Public License v2.5                 |              OLDAP-2.5               |           |               |      Y       |                 |
|                Open LDAP Public License v2.6                 |              OLDAP-2.6               |           |               |      Y       |                 |
|                Open LDAP Public License v2.7                 |              OLDAP-2.7               |     Y     |               |      Y       |                 |
|                Open LDAP Public License v2.8                 |              OLDAP-2.8               |           |       Y       |      Y       |                 |
|                     Open Market License                      |                 OML                  |           |               |      Y       |                 |
|                   Open Public License v1.0                   |               OPL-1.0                |           |               |              |                 |
|                Open Publication License v1.0                 |              OPUBL-1.0               |           |               |              |                 |
|                  Open Software License 1.0                   |               OSL-1.0                |     Y     |       Y       |      Y       |                 |
|                  Open Software License 1.1                   |               OSL-1.1                |     Y     |               |      Y       |                 |
|                  Open Software License 2.0                   |               OSL-2.0                |     Y     |       Y       |      Y       |                 |
|                  Open Software License 2.1                   |               OSL-2.1                |     Y     |       Y       |      Y       |                 |
|                  Open Software License 3.0                   |               OSL-3.0                |     Y     |       Y       |      Y       |                 |
|               Open Use of Data Agreement v1.0                |              O-UDA-1.0               |           |               |              |                 |
|                OpenJDK Assembly exception 1.0                |    OpenJDK-assembly-exception-1.0    |           |               |              |                 |
|                       OpenSSL License                        |               OpenSSL                |     Y     |               |      Y       |                 |
|                  OpenVPN OpenSSL Exception                   |      openvpn-openssl-exception       |           |               |              |                 |
|               OSET Public License version 2.1                |             OSET-PL-2.1              |           |       Y       |      Y       |                 |
|                       PHP License v3.0                       |               PHP-3.0                |           |       Y       |      Y       |                 |
|                      PHP License v3.01                       |               PHP-3.01               |     Y     |       Y       |      Y       |                 |
|                  Plexus Classworlds License                  |                Plexus                |           |               |      Y       |                 |
|               PNG Reference Library version 2                |              libpng-2.0              |           |               |      Y       |                 |
|             PolyForm Noncommercial License 1.0.0             |     PolyForm-Noncommercial-1.0.0     |           |               |              |                 |
|            PolyForm Small Business License 1.0.0             |    PolyForm-Small-Business-1.0.0     |           |               |              |                 |
|                      PostgreSQL License                      |              PostgreSQL              |           |       Y       |      Y       |                 |
|              PS/PDF font exception (2017-08-17)              |  PS-or-PDF-font-exception-20170817   |           |               |              |                 |
|                        psfrag License                        |                psfrag                |           |               |              |                 |
|                       psutils License                        |               psutils                |           |               |      Y       |                 |
|                      Python License 2.0                      |              Python-2.0              |     Y     |       Y       |      Y       |                 |
|            Python Software Foundation License 2.0            |               PSF-2.0                |           |               |      Y       |                 |
|                     Q Public License 1.0                     |               QPL-1.0                |     Y     |       Y       |      Y       |                 |
|                        Qhull License                         |                Qhull                 |           |               |      Y       |                 |
|                     Qt GPL exception 1.0                     |         Qt-GPL-exception-1.0         |           |               |      Y       |                 |
|                    Qt LGPL exception 1.1                     |        Qt-LGPL-exception-1.1         |           |               |              |                 |
|                      Qwt exception 1.0                       |          Qwt-exception-1.0           |           |               |              |                 |
|                        Rdisc License                         |                Rdisc                 |           |               |              |                 |
|           RealNetworks Public Source License v1.0            |               RPSL-1.0               |     Y     |       Y       |      Y       |                 |
|                Reciprocal Public License 1.1                 |               RPL-1.1                |           |       Y       |      Y       |                 |
|                Reciprocal Public License 1.5                 |               RPL-1.5                |           |       Y       |      Y       |                 |
|               Red Hat eCos Public License v1.1               |              RHeCos-1.1              |           |               |              |                 |
|               Ricoh Source Code Public License               |                RSCPL                 |           |       Y       |      Y       |                 |
|                  RSA Message-Digest License                  |                RSA-MD                |           |               |              |                 |
|                         Ruby License                         |                 Ruby                 |     Y     |               |      Y       |                 |
|                   Sax Public Domain Notice                   |                SAX-PD                |           |               |              |                 |
|                       Saxpath License                        |               Saxpath                |           |               |      Y       |                 |
|                  SCEA Shared Source License                  |                 SCEA                 |           |               |              |                 |
|                Scheme Language Report License                |             SchemeReport             |           |               |              |                 |
|    Scheme Widget Library (SWL) Software License Agreement    |                 SWL                  |           |               |      Y       |                 |
|           Secure Messaging Protocol Public License           |                SMPPL                 |           |               |              |                 |
|                       Sendmail License                       |               Sendmail               |           |               |      Y       |                 |
|                    Sendmail License 8.23                     |            Sendmail-8.23             |           |               |      Y       |                 |
|               Server Side Public License, v 1                |               SSPL-1.0               |           |               |              |                 |
|               SGI Free Software License B v1.0               |              SGI-B-1.0               |           |               |              |                 |
|               SGI Free Software License B v1.1               |              SGI-B-1.1               |           |               |              |                 |
|               SGI Free Software License B v2.0               |              SGI-B-2.0               |     Y     |               |      Y       |                 |
|                  SIL Open Font License 1.0                   |               OFL-1.0                |           |               |              |        Y        |
|     SIL Open Font License 1.0 with no Reserved Font Name     |            OFL-1.0-no-RFN            |           |               |              |        Y        |
|      SIL Open Font License 1.0 with Reserved Font Name       |             OFL-1.0-RFN              |           |               |              |        Y        |
|                  SIL Open Font License 1.1                   |               OFL-1.1                |     Y     |       Y       |      Y       |                 |
|     SIL Open Font License 1.1 with no Reserved Font Name     |            OFL-1.1-no-RFN            |           |       Y       |      Y       |                 |
|      SIL Open Font License 1.1 with Reserved Font Name       |             OFL-1.1-RFN              |           |       Y       |      Y       |                 |
|                  Simple Public License 2.0                   |              SimPL-2.0               |           |       Y       |      Y       |                 |
|                      Sleepycat License                       |              Sleepycat               |     Y     |       Y       |      Y       |                 |
|                   SNIA Public License 1.1                    |                 SNIA                 |           |               |      Y       |                 |
|               Solderpad Hardware License v0.5                |               SHL-0.5                |           |               |              |                 |
|               Solderpad Hardware License v2.0                |               SHL-2.0                |           |               |              |                 |
|               Solderpad Hardware License v2.1                |               SHL-2.1                |           |               |              |                 |
|           Solderpad Hardware License, Version 0.51           |               SHL-0.51               |           |               |              |                 |
|                      Spencer License 86                      |              Spencer-86              |           |               |              |                 |
|                      Spencer License 94                      |              Spencer-94              |           |               |      Y       |                 |
|                      Spencer License 99                      |              Spencer-99              |           |               |              |                 |
|                       SQLite Blessing                        |               blessing               |           |               |              |        Y        |
|                     SSH OpenSSH license                      |             SSH-OpenSSH              |           |               |              |                 |
|                       SSH short notice                       |              SSH-short               |           |               |              |                 |
|              Standard ML of New Jersey License               |                SMLNJ                 |     Y     |               |      Y       |                 |
|                SugarCRM Public License v1.1.3                |            SugarCRM-1.1.3            |           |               |              |                 |
|          Sun Industry Standards Source License v1.1          |                SISSL                 |     Y     |       Y       |      Y       |                 |
|          Sun Industry Standards Source License v1.2          |              SISSL-1.2               |           |               |              |                 |
|                   Sun Public License v1.0                    |               SPL-1.0                |     Y     |       Y       |      Y       |                 |
|                       Swift Exception                        |           Swift-exception            |           |               |              |                 |
|            Sybase Open Watcom Public License 1.0             |              Watcom-1.0              |           |       Y       |      Y       |                 |
|               TAPR Open Hardware License v1.0                |             TAPR-OHL-1.0             |           |               |              |                 |
|                        TCL/TK License                        |                 TCL                  |           |               |      Y       |                 |
|                     TCP Wrappers License                     |             TCP-wrappers             |           |               |              |                 |
|          Technische Universitaet Berlin License 1.0          |            TU-Berlin-1.0             |           |               |              |                 |
|          Technische Universitaet Berlin License 2.0          |            TU-Berlin-2.0             |           |               |              |                 |
|                      The MirOS Licence                       |                MirOS                 |           |       Y       |      Y       |                 |
|               The Parity Public License 6.0.0                |             Parity-6.0.0             |           |               |              |                 |
|               The Parity Public License 7.0.0                |             Parity-7.0.0             |           |               |              |                 |
|                        The Unlicense                         |              Unlicense               |     Y     |       Y       |      Y       |                 |
|                  TMate Open Source License                   |                TMate                 |           |               |              |                 |
|              TORQUE v2.5+ Software License v1.1              |              TORQUE-1.1              |           |               |              |                 |
|                 Trusster Open Source License                 |                 TOSL                 |           |               |              |                 |
|                 TUG Utopia license agreement                 |                Utopia                |           |               |              |        Y        |
|                     U-Boot exception 2.0                     |         u-boot-exception-2.0         |           |               |              |                 |
|  Unicode License Agreement - Data Files and Software (2015)  |           Unicode-DFS-2015           |           |               |      Y       |                 |
|  Unicode License Agreement - Data Files and Software (2016)  |           Unicode-DFS-2016           |           |       Y       |      Y       |                 |
|                     Unicode Terms of Use                     |             Unicode-TOU              |           |               |              |                 |
|            Universal FOSS Exception, Version 1.0             |     Universal-FOSS-exception-1.0     |           |               |              |                 |
|              Universal Permissive License v1.0               |               UPL-1.0                |     Y     |       Y       |      Y       |                 |
|       University of Illinois/NCSA Open Source License        |                 NCSA                 |     Y     |       Y       |      Y       |                 |
|             Upstream Compatibility License v1.0              |               UCL-1.0                |           |       Y       |      Y       |                 |
|                         Vim License                          |                 Vim                  |     Y     |               |      Y       |                 |
|            VOSTROM Public License for Open Source            |               VOSTROM                |           |               |              |                 |
|                 Vovida Software License v1.0                 |               VSL-1.0                |           |       Y       |      Y       |                 |
|    W3C Software Notice and Document License (2015-05-13)     |             W3C-20150513             |           |               |              |                 |
|         W3C Software Notice and License (1998-07-20)         |             W3C-19980720             |           |               |              |                 |
|         W3C Software Notice and License (2002-12-31)         |                 W3C                  |     Y     |       Y       |      Y       |                 |
|                        Wsuipa License                        |                Wsuipa                |           |               |              |                 |
|               WxWindows Library Exception 3.1                |       WxWindows-exception-3.1        |           |               |              |                 |
|                        X.Net License                         |                 Xnet                 |           |       Y       |      Y       |                 |
|                         X11 License                          |                 X11                  |     Y     |               |      Y       |                 |
|        X11 License Distribution Modification Variant         | X11-distribute-modifications-variant |           |               |      Y       |                 |
|                        Xerox License                         |                Xerox                 |           |               |              |                 |
|                     XFree86 License 1.1                      |             XFree86-1.1              |     Y     |               |      Y       |                 |
|                        xinetd License                        |                xinetd                |     Y     |               |      Y       |                 |
|                         XPP License                          |                 xpp                  |           |               |      Y       |                 |
|                        XSkat License                         |                XSkat                 |           |               |              |                 |
|                  Yahoo! Public License v1.0                  |               YPL-1.0                |           |               |              |                 |
|                  Yahoo! Public License v1.1                  |               YPL-1.1                |     Y     |               |      Y       |                 |
|                         Zed License                          |                 Zed                  |           |               |              |                 |
|                      Zend License v2.0                       |               Zend-2.0               |     Y     |               |      Y       |                 |
|                  Zimbra Public License v1.3                  |              Zimbra-1.3              |     Y     |               |      Y       |                 |
|                  Zimbra Public License v1.4                  |              Zimbra-1.4              |           |               |              |                 |
|                         zlib License                         |                 Zlib                 |     Y     |       Y       |      Y       |                 |
|           zlib/libpng License with Acknowledgement           |         zlib-acknowledgement         |           |               |              |                 |
|                   Zope Public License 1.1                    |               ZPL-1.1                |           |               |              |                 |
|                   Zope Public License 2.0                    |               ZPL-2.0                |     Y     |       Y       |      Y       |                 |
|                   Zope Public License 2.1                    |               ZPL-2.1                |     Y     |               |      Y       |                 |

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

License compliance matters are the responsibility of the [PST](https://github.com/volcano-sh/community/blob/master/PST.md) team. They should be responsible for license selection, review and compliance risk avoidance. They should take corresponding responsibilities to ensure that the licenses introduced by the community comply with open source compliance specifications, and make timely corrections when there are compliance risks. For example, for contagious licenses such as GPL licenses, relevant open source obligations should be fully fulfilled in open source software compliance projects,  SBOM and source code should be provided in projects, and they should also consider alternative license options to avoid  legal risks .Characters who do not comply with the above behavior can be removed and re-elected.

## Contact

If you have any questions about open source license compliance, please contact us through the following methods.

[Volcano Slack Channel](https://cloud-native.slack.com/archives/C011GJDQS0N) | [Join](https://slack.cncf.io/)

[Mailing List](https://groups.google.com/forum/#!forum/volcano-sh)

