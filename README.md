[![Build manufacturing files](https://github.com/PatrickBaus/HP6632B_binding_posts/actions/workflows/ci.yml/badge.svg)](https://github.com/PatrickBaus/HP6632B_binding_posts/actions/workflows/ci.yml)
# HP 66332A and HP 6632B-6634B Frontpanel Binding Post PCB
This repository contains the schematics for a PCB to mount frontpanel binding post on an [HP 6632B](https://www.keysight.com/us/en/product/6632B/100-watt-system-power-supply-20v-5a.html) (and siblings) power supply. It is an adaption of the original A4 PCB used in option #020 units.

![Front panel binding post PCB](images/board.png)

## Contents
- [Introduction](#introduction)
- [Design Files](#design-files)
- [Related Repositories](#related-repositories)
- [Versioning](#versioning)
- [License](#license)

## Introduction
In addition to the original option #20 PCB, this board breaks out the sense connections as well and also the chassis ground. This makes connecting multiple [HP 663xB](https://www.keysight.com/us/en/product/6632B/100-watt-system-power-supply-20v-5a.html) in parallel possible. On the downside, this requires connecting the sense pins externally. To make this easier I also made a small [shorting bar](https://github.com/PatrickBaus/HP6632B_shorting_bar) to easily short the sense terminals to the force terminals directly at the power supply output.

The components chosen allow the board to be used on all variants of the HP 663xB family - even the 100 V 6634B. A variety of different binding posts can be used. There are HP/Agilent versions available on Ebay. I used [Pomona 4243-0](https://www.pomonaelectronics.com/products/hardware/double-binding-post) ([Digikey](https://www.digikey.de/product-detail/de/pomona-electronics/4243-0/501-1126-ND/604321)) and [3760-5](https://www.pomonaelectronics.com/products/hardware/binding-post-tin-plated) ([Digikey](https://www.digikey.de/product-detail/de/pomona-electronics/3760-5/501-1506-ND/736554)) binding posts.

The final result looks like this:
![HP 66332A with binding posts](images/final.jpg)

## Design Files
The root folder contains the KiCAD files. The bill of materials can be found on the [releases](../../releases) page along with Gerber files for production.

## Related Repositories
See the following repositories which contain addional optional parts.

- [HP 66332A and HP 6632B-6634B Shorting Bar](https://github.com/PatrickBaus/HP6632B_shorting_bar)

## Versioning
I use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags](../../tags) available for this repository.

- MAJOR versions in this context mean a breaking change to the external interface of the hardware like different connectors or functions.
- MINOR versions contain changes to the hardware that only affect the inner workings of the circuit, but otherwise the performance is unaffected.
- PATCH versions do not affect the schematics or invalidate older bill of materials. These changes may include updated components (to replace obsolete parts for example), an updated silkscreen, or fixed typos.

## License
This work is released under the CERN-OHL-W
See [https://ohwr.org/cern_ohl_w_v2.pdf](https://ohwr.org/cern_ohl_w_v2.pdf) or the included LICENSE file for more information.
