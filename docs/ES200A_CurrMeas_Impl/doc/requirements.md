---
layout: default
title: requirements
nav_order: 4
parent: Component Implementation
---
{% raw %}
| FDD    | ID  | Source                                | Function                                        | Line(s)                                                          | Status    | Comment    |
|--------|-----|---------------------------------------|-------------------------------------------------|------------------------------------------------------------------|-----------|------------|
|        |     | .SwFileName                           | .SwFuncName                                     | .SwLines                                                         | .SwStatus | .SwComment |
| ES200A | 215 | CDD_CurrMeas.c,CDD_CurrMeas_MotCtrl.c | CurrMeasPer3,CurrMeasPer2                       | 1577,1581,1625,156,166                                           | I         |            |
| ES200A | 213 | CDD_CurrMeas.c,CDD_CurrMeas_MotCtrl.c | CurrMeasPer3,CurrMeasPer2                       | 1570,1577,1581,1619,1625,145                                     | I         |            |
| ES200A | 132 | CDD_CurrMeas.c,CDD_CurrMeas_MotCtrl.c | CurrMeasPer3,CurrMeasPer2                       | 1570,1577,1581,1619,1625,156,166,181,189                         | I         |            |
| ES200A | 135 | CDD_CurrMeas.c,CDD_CurrMeas_MotCtrl.c | CurrMeasPer1,CurrMeasPer2                       | 1309-1462,121-210                                                | I         |            |
| ES200A | 138 | CDD_CurrMeas.c                        | SigMaxMinOffs                                   | 1789,1790,1791,1792,1793,1794,1795,1796,1797,1798,1799,1800,1801 | I         |            |
| ES200A | 223 | CDD_CurrMeas.c                        | CurrMeasPer3                                    | 1588,1595,1599,1637,1643                                         | I         |            |
| ES200A | 289 | CDD_CurrMeas.c                        | CurrMeasPer3                                    | 1555                                                             | I         |            |
| ES200A | 288 | CDD_CurrMeas.c                        | CurrMeasPer3                                    | 1554                                                             | I         |            |
| ES200A | 97  | CDD_CurrMeas.c                        | CurrMeasPer3                                    | 1678                                                             | I         |            |
| ES200A | 281 | CDD_CurrMeas_MotCtrl.c                | CurrMeasPer2                                    | 133                                                              | I         |            |
| ES200A | 280 | CDD_CurrMeas.c                        | CurrMeasOffsReadReq_Oper,CurrMeasOffsWrReq_Oper | 1112-1126,1165-1214                                              | I         |            |
| ES200A | 283 | CDD_CurrMeas.c                        | CurrMeasPer3                                    | 1556                                                             | I         |            |
| ES200A | 282 | CDD_CurrMeas.c                        | CurrMeasPer3                                    | 1557                                                             | I         |            |
| ES200A | 285 | CDD_CurrMeas_MotCtrl.c                | CurrMeasPer2                                    | 202                                                              | I         |            |
| ES200A | 284 | CDD_CurrMeas_MotCtrl.c                | CurrMeasPer2                                    | 201                                                              | I         |            |
| ES200A | 287 | CDD_CurrMeas.c                        | CurrMeasPer1                                    | 1296                                                             | I         |            |
| ES200A | 286 | CDD_CurrMeas.c                        | CurrMeasPer1                                    | 1303                                                             | I         |            |
| ES200A | 262 | CDD_CurrMeas.c                        | SigMaxMinGain                                   | 1838-1930                                                        | I         |            |
| ES200A | 260 | CDD_CurrMeas.c                        | SigMaxMinGain,PerformGainCalibration            | 1911,1916,1926,2132                                              | I         |            |
| ES200A | 267 | CDD_CurrMeas_MotCtrl.c                | CurrMeasPer2                                    | 171,195                                                          | I         |            |
| ES200A | 266 | CDD_CurrMeas.c                        | SigMaxMinGain,PerformGainCalibration            | 1926,2132                                                        | I         |            |
| ES200A | 264 | CDD_CurrMeas.c                        | SigMaxMinOffs,SigMaxMinGain                     | 1811,1851-1865,1918,1924,1925                                    | I         |            |
| ES200A | 269 | CDD_CurrMeas_MotCtrl.c                | CalMotCurrCorrdABC                              | 321-377                                                          | I         |            |
| ES200A | 91  | CDD_CurrMeas_MotCtrl.c                | CurrMeasPer2                                    | 128                                                              | I         |            |
| ES200A | 298 | CDD_CurrMeas.c                        | PerformGainCalibration                          | 1981-2135                                                        | I         |            |
| ES200A | 299 | CDD_CurrMeas.c                        | SigMaxMinGain                                   | 1874-1888                                                        | I         |            |
| ES200A | 296 | CDD_CurrMeas.c                        | SigMaxMinOffs                                   | 1752-1773                                                        | I         |            |
| ES200A | 297 | CDD_CurrMeas.c                        | CurrMeasPer1                                    | 1311-1460                                                        | I         |            |
| ES200A | 290 | CDD_CurrMeas.c                        | CurrMeasPer3                                    | 1564                                                             | I         |            |
| ES200A | 291 | CDD_CurrMeas.c                        | CurrMeasGainReadReq_Oper,CurrMeasGainWrReq_Oper | 967,974,1013-1042                                                | I         |            |
| ES200A | 146 | CDD_CurrMeas_MotCtrl.c                | CalMotCurrCorrdDEF                              | 424-482                                                          | I         |            |
| ES200A | 147 | CDD_CurrMeas_MotCtrl.c                | CalMotCurrCorrdDEF                              | 423-481                                                          | I         |            |
| ES200A | 312 | CDD_CurrMeas_MotCtrl.c                | CalMotCurrCorrdABC                              | 320-376                                                          | I         |            |
| ES200A | 311 | CDD_CurrMeas_MotCtrl.c                | CalMotCurrCorrdABC                              | 319-375                                                          | I         |            |
| ES200A | 310 | CDD_CurrMeas_MotCtrl.c                | CalMotCurrCorrdDEF                              | 427-485                                                          | I         |            |
| ES200A | 270 | CDD_CurrMeas_MotCtrl.c                | CurrMeasPer2                                    | 150                                                              | I         |            |
| ES200A | 88  | CDD_CurrMeas.c                        | CurrMeasPer1                                    | 1305                                                             | I         |            |
| ES200A | 89  | CDD_CurrMeas.c                        | CurrMeasPer1                                    | 1304                                                             | I         |            |
| ES200A | 274 | CDD_CurrMeas.c                        | CurrMeasPer1,CurrMeasPer3                       | 1298,1559                                                        | I         |            |
| ES200A | 275 | CDD_CurrMeas.c                        | CurrMeasPer1,CurrMeasPer3                       | 1299,1560                                                        | I         |            |
| ES200A | 276 | CDD_CurrMeas.c                        | CurrMeasPer1,CurrMeasPer3                       | 1300,1561                                                        | I         |            |
| ES200A | 277 | CDD_CurrMeas.c                        | CurrMeasPer1,CurrMeasPer3                       | 1301,1562                                                        | I         |            |
| ES200A | 278 | CDD_CurrMeas.c                        | CurrMeasPer1,CurrMeasPer3                       | 1302,1563                                                        | I         |            |
| ES200A | 83  | CDD_CurrMeas_MotCtrl.c                | CurrMeasPer2                                    | 130                                                              | I         |            |
| ES200A | 86  | CDD_CurrMeas_MotCtrl.c                | CurrMeasPer2                                    | 132                                                              | I         |            |
| ES200A | 84  | CDD_CurrMeas_MotCtrl.c                | CurrMeasPer2                                    | 131                                                              | I         |            |
| ES200A | 251 | CDD_CurrMeas.c                        | CurrMeasPer1,SigMaxMinOffs                      | 1449,1457,1804,1809,1816                                         | I         |            |
| ES200A | 308 | CDD_CurrMeas_MotCtrl.c                | CalMotCurrCorrdDEF                              | 425-483                                                          | I         |            |
| ES200A | 309 | CDD_CurrMeas_MotCtrl.c                | CalMotCurrCorrdDEF                              | 426-484                                                          | I         |            |
| ES200A | 300 | CDD_CurrMeas.c                        | SigMaxMinGain,PerformGainCalibration            | 1916,1926,2132                                                   | I         |            |
| ES200A | 301 | CDD_CurrMeas.c                        | CurrMeasPer1,SigMaxMinOffs                      | 1449,1457,1809,1816                                              | I         |            |
| ES200A | 302 | CDD_CurrMeas_MotCtrl.c                | CurrMeasPer2                                    | 137                                                              | I         |            |
| ES200A | 303 | CDD_CurrMeas_MotCtrl.c                | CurrMeasPer2                                    | 136                                                              | I         |            |
| ES200A | 304 | CDD_CurrMeas_MotCtrl.c                | CurrMeasPer2                                    | 135                                                              | I         |            |
| ES200A | 305 | CDD_CurrMeas_MotCtrl.c                | CurrMeasPer2                                    | 140                                                              | I         |            |
| ES200A | 306 | CDD_CurrMeas_MotCtrl.c                | CurrMeasPer2                                    | 139                                                              | I         |            |
| ES200A | 307 | CDD_CurrMeas_MotCtrl.c                | CurrMeasPer2                                    | 138                                                              | I         |            |
| ES200A | 245 | CDD_CurrMeas.c,CDD_CurrMeas_MotCtrl.c | CurrMeasPer3,CurrMeasPer2                       | 1588,1637,187-192                                                | I         |            |
| ES200A | 109 | CDD_CurrMeas.c                        | CurrMeasPer3                                    | 1679                                                             | I         |            |
| ES200A | 102 | CDD_CurrMeas_MotCtrl.c                | CalMotCurrCorrdABC                              | 329,332,343,355,366                                              | I         |            |
| ES200A | 103 | CDD_CurrMeas_MotCtrl.c                | CalMotCurrCorrdABC                              | 328,331,342,354,365                                              | I         |            |
| ES200A | 100 | CDD_CurrMeas_MotCtrl.c                | CalMotCurrCorrdDEF                              | 435,438,450,462,473                                              | I         |            |
| ES200A | 101 | CDD_CurrMeas_MotCtrl.c                | CalMotCurrCorrdDEF                              | 434,437,449,461,472                                              | I         |            |
| ES200A | 104 | CDD_CurrMeas_MotCtrl.c                | CalMotCurrCorrdABC                              | 327,330,341,353,364                                              | I         |            |
| ES200A | 246 | CDD_CurrMeas_MotCtrl.c                | CurrMeasPer2                                    | 122-209                                                          | I         |            |
| ES200A | 176 | CDD_CurrMeas.c                        | SigMaxMinGain                                   | 1903,1904,1905,1906,1907,1908,1909                               | I         |            |
| ES200A | 61  | CDD_CurrMeas_MotCtrl.c                | CurrMeasPer2                                    | 123                                                              | I         |            |
| ES200A | 65  | CDD_CurrMeas_MotCtrl.c                | CurrMeasPer2                                    | 129                                                              | I         |            |
| ES200A | 179 | CDD_CurrMeas.c,CDD_CurrMeas_MotCtrl.c | CurrMeasPer3,CurrMeasPer2                       | 1631-1649,179-185                                                | I         |            |
| ES200A | 177 | CDD_CurrMeas.c,CDD_CurrMeas_MotCtrl.c | CurrMeasPer3,CurrMeasPer2                       | 1570,1619,164-168                                                | I         |            |
| ES200A | 253 | CDD_CurrMeas.c                        | CurrMeasPer1                                    | 1310                                                             | I         |            |
| ES200A | 174 | CDD_CurrMeas.c                        | PerformGainCalibration                          | 1969-2134                                                        | I         |            |
| ES200A | 257 | CDD_CurrMeas.c                        | SigMaxMinOffs                                   | 1721-1813                                                        | I         |            |
| ES200A | 255 | CDD_CurrMeas.c                        | CurrMeasPer1,SigMaxMinOffs                      | 1448,1456,1723-1744,1814-1821                                    | I         |            |
| ES200A | 99  | CDD_CurrMeas_MotCtrl.c                | CalMotCurrCorrdDEF                              | 436,439,451,463,474                                              | I         |            |
| ES200A | 227 | CDD_CurrMeas.c,CDD_CurrMeas_MotCtrl.c | CurrMeasPer3,CurrMeasPer2                       | 1595,1599,1643,181,189                                           | I         |            |
| ES200A | 225 | CDD_CurrMeas.c,CDD_CurrMeas_MotCtrl.c | CurrMeasPer3,CurrMeasPer2                       | 1588,1595,1599,1632,1637,1643,175                                | I         |            |
| ES200A | 92  | CDD_CurrMeas_MotCtrl.c                | CurrMeasPer2                                    | 126                                                              | I         |            |
| ES200A | 95  | CDD_CurrMeas_MotCtrl.c                | CurrMeasPer2                                    | 205                                                              | I         |            |
| ES200A | 162 | CDD_CurrMeas_MotCtrl.c                | CurrMeasPer2,CalMotCurrCorrdDEF                 | 175,428-486                                                      | I         |            |
| ES200A | 15  | CDD_CurrMeas_MotCtrl.c                | CurrMeasPer2                                    | 120                                                              | I         |            |
| ES200A | 273 | CDD_CurrMeas.c                        | CurrMeasPer1,CurrMeasPer3                       | 1297,1558                                                        | I         |            |
| ES200A | 110 | CDD_CurrMeas_MotCtrl.c                | CurrMeasPer2                                    | 206                                                              | I         |            |
| ES200A | 151 | CDD_CurrMeas_MotCtrl.c                | CalMotCurrCorrdABC                              | 316-372                                                          | I         |            |
| ES200A | 150 | CDD_CurrMeas_MotCtrl.c                | CalMotCurrCorrdABC                              | 317-373                                                          | I         |            |
| ES200A | 157 | CDD_CurrMeas.c,CDD_CurrMeas_MotCtrl.c | CurrMeasPer3,CurrMeasPer2                       | 1612-1629,154-162                                                | I         |            |
| ES200A | 158 | CDD_CurrMeas_MotCtrl.c                | CurrMeasPer2                                    | 175                                                              | I         |            |
| ES200A | 201 | CDD_CurrMeas_MotCtrl.c                | CalMotCurrCorrdABC                              | 314                                                              | I         |            |
| ES200A | 200 | CDD_CurrMeas_MotCtrl.c                | CurrMeasPer2                                    | 127                                                              | I         |            |
| ES200A | 203 | CDD_CurrMeas.c                        | CurrMeasPer1                                    | 1475                                                             | I         |            |
| ES200A | 202 | CDD_CurrMeas_MotCtrl.c                | CurrMeasPer2                                    | 200                                                              | I         |            |
| ES200A | 204 | CDD_CurrMeas.c                        | CurrMeasPer3                                    | 1677                                                             | I         |            |
| ES200A | 207 | CDD_CurrMeas_MotCtrl.c                | CurrMeasPer2                                    | 125                                                              | I         |            |
| ES200A | 208 | CDD_CurrMeas_MotCtrl.c                | CurrMeasPer2                                    | 124                                                              | I         |            |
| ES200A | 148 | CDD_CurrMeas_MotCtrl.c                | CalMotCurrCorrdDEF                              | 422-480                                                          | I         |            |
| ES200A | 149 | CDD_CurrMeas_MotCtrl.c                | CalMotCurrCorrdABC                              | 318-374                                                          | I         |            |

{% endraw %}