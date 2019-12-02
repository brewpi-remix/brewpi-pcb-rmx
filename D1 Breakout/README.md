# ![BrewPi Remix Logo](https://raw.githubusercontent.com/lbussy/brewpi-www-rmx/master/images/brewpi_logo.png)

# Wemos D1 Mini BrewPi Breakout

A Wemos D1 Mini breakout board for BrewPi-derivative ESP8266 projects. No third-party level shifter is required.  Through-hole components only for ease of assembly.

[Order from PCBs.io](https://PCBs.io/share/z5JLZ):

- 2 Layer Board - 0.7087 sq in (0.7038in x 1.0069in) / 457.22 sq/mm (17.88mm x 25.58mm)
- $2.83 per set of 4 ($4.00 per sq in)

| Top View          | Bottom View          |
| ----------------- |:--------------------:|
| ![Board Top][top] | ![Board Bottom][bot] |

[top]: Top.png "Board Top"
[bot]: Bottom.png "Board Bottom"

## BOM (controller/shield only):

- 1 x [PCB Shield](https://PCBs.io/share/z5JLZ) (this project)
- 1 x [Wemos D1 Mini](https://www.aliexpress.com/item/32688079351.html?spm=a2g0o.productlist.0.0.2dcf3152g4UkxV&algo_pvid=be694029-b1d5-44b7-b733-20b8c0f6ba9a&algo_expid=be694029-b1d5-44b7-b733-20b8c0f6ba9a-0&btsid=3b4ec2af-8a5e-4c59-9e85-bb2bdb771ffd&ws_ab_test=searchweb0_0,searchweb201602_1,searchweb201603_52_) (U1)
- 2 x Male 8-pin header (comes with controller)
- 2 x Female 8-pin header (comes with controller)
- 2 x [1.0uF Capacitor](https://www.mouser.com/ProductDetail/KEMET/C320C105K5R5TA?qs=sGAEpiMZZMt3KoXD5rJ2N0CWo9MbFM%2FuWljjm75KZzs%3D) (C1, C3)
- 2 x [0.1uF Capacitor](https://www.mouser.com/ProductDetail/KEMET/C320C104K3R5TA?qs=sGAEpiMZZMt3KoXD5rJ2N4ZXb0dQpKOeXkTyt%2FbcGss%3D) (C2, C4)
- 2 x [2N7000 N-Channel MOSFET](https://www.mouser.com/ProductDetail/ON-Semiconductor/2N7000?qs=sGAEpiMZZMshyDBzk1%2FWi9bHELEahoDnY1fyKF6A6Ko%3D) (Q1, Q2)
- 5 x [10kΩ 1/4-Watt Resistor](https://www.mouser.com/ProductDetail/KOA-Speer/CF1-4CT52R103J?qs=sGAEpiMZZMtlubZbdhIBIG%252BgbQse942Boczpyiowqgc%3D) (R1-R4)
- 1 x [2.2kΩ 1/4-Watt Resistor](https://www.mouser.com/ProductDetail/KOA-Speer/CF1-4CT52R222J?qs=sGAEpiMZZMu61qfTUdNhGx20sZYqUI%252BADLaC9a%252B2%2Flg%3D) (R5)
- 1 x [Wago 2-terminal Screw Clamp](https://www.aliexpress.com/item/32700056337.html) (PWR)
- 1 x [RJ45 Modular Jack w/no shield](https://www.aliexpress.com/item/32736146888.html) (J1)
- 2 x [4-pin DuPont Header](https://www.aliexpress.com/item/32670112443.html?spm=a2g0o.productlist.0.0.b4045bcffb2Q4C&algo_pvid=e9508115-148b-4d72-a7a3-4e45d189d5c7&algo_expid=e9508115-148b-4d72-a7a3-4e45d189d5c7-12&btsid=35f3875d-d1f0-4b92-9a59-406a3faaa4ef&ws_ab_test=searchweb0_0,searchweb201602_1,searchweb201603_52) (RELAY, LCD)
- 1 x [2-pin DuPont Header](https://www.aliexpress.com/item/32670112443.html?spm=a2g0o.productlist.0.0.b4045bcffb2Q4C&algo_pvid=e9508115-148b-4d72-a7a3-4e45d189d5c7&algo_expid=e9508115-148b-4d72-a7a3-4e45d189d5c7-12&btsid=35f3875d-d1f0-4b92-9a59-406a3faaa4ef&ws_ab_test=searchweb0_0,searchweb201602_1,searchweb201603_52) (PWR)

## Board Manufacture

You may order this board for manufacture directly from [PCBs.io](https://PCBs.io/share/z5JLZ).

## 3D-Printed Case

See [this case](https://www.thingiverse.com/thing:2874176) from Thorrak for a case you can print.

## Modifying These Files

If you would like to personalize these board designs, you may modify them with [Autodesk's EAGLE](https://www.autodesk.com/products/eagle/overview). EAGLE is a scriptable electronic design automation (EDA) application with schematic capture, printed circuit board (PCB) layout, auto-router and computer-aided manufacturing (CAM) features. EAGLE stands for Easily Applicable Graphical Layout Editor and is developed by CadSoft Computer GmbH. The company was acquired by Autodesk Inc. in 2016.  

The program supports Windows, Linux, and Mac OS X.  EAGLE is available in a [free version](https://www.autodesk.com/products/eagle/free-download), as well as a [subscription-based version with more features](https://www.autodesk.com/products/eagle/compare).
