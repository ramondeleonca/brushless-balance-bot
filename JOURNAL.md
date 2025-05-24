---
title: "Brushless Balance Bot"
author: "Ramon de Leon"
description: ""
created_at: "2024-05-23"
---

# May 23rd: Defining what I want the robot to do and researching the correct parts

So first off, I wanted to achieve a few things with this robot:
- Make it balance itself (obviously)
- Be controlled wirelessly with a game controller
- Use brushless motors for speeeeeed (and because they are cool)
- Make a custom PCB to make it as compact as possible
- Write the firmware from scratch to learn the math and logic behind it
- Build an app for telemetry
- Have a very resilient angle sensing system

Based on this, I then defined what parts would be appropriate for this
- PS5 controller
- 2208 (or similar) brushless motors
- SimpleFOC ESC (FOC allows for more accurate control)
- PCB designed in EasyEDA and manufactured with JLCPCB
- Write the firmware in C++ for an ESP32
- Build an app using React, React Native or some Python framework and build an API to communicate with the robot
- Put 2 gyroscopes on the board for sensor fusion and drift correction

So i then got to searching for the parts online (mostly AliExpress) and it came out to this (draft) BOM (still some parts missing)

| Item               | Purpose             | Source                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   | Price |   |
|--------------------|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|---|
| 2 Brushless motors | Powering the wheels | https://es.aliexpress.com/item/1005002337447698.html?spm=a2g0o.productlist.main.8.5bc2lLPHlLPHTD&algo_pvid=24f9e979-be8c-4a6c-9ed3-f82f7ef89e98&algo_exp_id=24f9e979-be8c-4a6c-9ed3-f82f7ef89e98-7&pdp_ext_f=%7B%22order%22%3A%2236%22%2C%22eval%22%3A%221%22%7D&pdp_npi=4%40dis%21MXN%21407.97%21301.90%21%21%2120.73%2115.34%21%402103273e17480465153801698e2638%2112000020163631937%21sea%21MX%213953587241%21X&curPageLogUid=9ChEV8IGq5ln&utparam-url=scene%3Asearch%7Cquery_from%3A | $30   |   |
| BNO-055            | Gyroscope           | https://es.aliexpress.com/item/1005005471265894.html?spm=a2g0o.productlist.main.1.37c81ccfZElpP6&algo_pvid=30345036-1c95-4022-9623-6092021ee338&algo_exp_id=30345036-1c95-4022-9623-6092021ee338-0&pdp_ext_f=%7B%22order%22%3A%2216%22%2C%22eval%22%3A%221%22%7D&pdp_npi=4%40dis%21MXN%21312.90%21312.90%21%21%2115.90%2115.90%21%402101c5b117480466045457572e395d%2112000033214303566%21sea%21MX%213953587241%21X&curPageLogUid=VTxdDIr4DMHL&utparam-url=scene%3Asearch%7Cquery_from%3A | $15   |   |
| ESP32              | Microcontroller     | https://es.aliexpress.com/item/1005008481419724.html?spm=a2g0o.productlist.main.3.4afa617431iwR2&algo_pvid=3dd61864-3393-4cc1-8a06-2b347abfe823&algo_exp_id=3dd61864-3393-4cc1-8a06-2b347abfe823-2&pdp_ext_f=%7B%22order%22%3A%22112%22%2C%22eval%22%3A%221%22%7D&pdp_npi=4%40dis%21MXN%21135.89%2167.90%21%21%2149.63%2124.80%21%402101d9ee17480466909626963e6f58%2112000045338722226%21sea%21MX%213953587241%21X&curPageLogUid=4FAE2o4F778i&utparam-url=scene%3Asearch%7Cquery_from%3A | $6    |   |
|                    |                     |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |       |   |

**Total time spent: 2h 20m**
