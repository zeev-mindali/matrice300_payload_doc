---
title: Development Platform
date: 2020-05-08
version: 2.1.0
keywords: [development kit, SkyPort V2, SkyPort, X-Port, payload, ]
---
> **NOTE** This article is **Machine-Translated**. If you have any questions about this article, please send an <a href="mailto:dev@dji.com">E-mail </a>to DJI, we will correct it in time. DJI appreciates your support and attention.

According to the features、resource usage and toolchain to choose the OS and the development platform for the payload.

## OS
#### Features
The payload developed using PSDK on *RTOS* **doesn't** support:
* Video streaming
* Playback and download
* High-speed data transmission

#### Resource Usage
###### Linux
Using Linux on the Manifold 2-C, the resource usage of the payload is as follows:       
* Stack: 12288 bytes
* Heap: 36864 bytes
* Text: 641742 bytes
* Data: 3808 bytes
* Bss: 21992 bytes
* CPU: 7.2%

###### RTOS 
Using RTOS on the STM32F407IGH6-EVAL, the resource usage of the payload is as follows:  
* Text: 315184 bytes
* Data: 1760 bytes
* Bss: 84848 bytes
* CPU: 30%

## Development Platform
According to the platform and chip to choose the **development platform**.
> **NOTE** 
> * It is effective to use the toolchain, which is DJI recommended, if you have other special needs, please contact <a href="mailto:dev@dji.com">Support</a>.
> * The details of the porting, please refer to [Porting](../quickstart/porting.html).


<table id="toolchain">
<thead>
<tr>
<th>Name</th>
<th>Platform</th>
<th>Chip</th>
<th>Recommended</th>
</tr>
</thead>
<tbody>
<tr>
<td>aarch64-linux-gnu-gcc</td>
<td>aarch64-linux-gnu</td>
<td>NVIDIA Jetson TX2、Rockchip RK3399 pro</td>
<td>Manifold2-G</td>
</tr>
<tr>
<td>gcc</td>
<td>x86_64-linux-gnu</td>
<td>intel 64bit</td>
<td>Maniflod2-C</td>
</tr>
<tr>
<td>arm-linux-gnueabi-gcc</td>
<td>arm-linux-gnueabi</td>
<td>ZYNQ、I.MX6Q</td>
<td>-</td>
</tr>
<tr>
   <td>arm-linux-gnueabihf-gcc</td>
   <td>arm-linux-gnueabihf</td>
   <td>Support hardware processor of float arithmetic, such as OK5718-C,etc.</td>
   <td>-</td>
</tr>
<tr>
<td>armcc</td>
<td>Cortex M series MCU</td>
<td>STM32F407、STM32F103</td>
<td>STM32F407-Eval、STM32F407</td>
</tr>
<tr>
<td>arm-himix100-linux-gcc</td>
<td>arm-himix100-linux</td>
<td>hi3516EV series</td>
<td>-</td>
</tr>
<tr>
   <td>arm-himix200-linux-gcc</td>
   <td>arm-himix200-linux</td>
   <td>hi3516C series chips</td>
   <td>-</td>
</tr>
<tr>
<td>aarch64-himix100-linux-gcc</td>
<td>aarch64-himix100-linux</td>
<td>hi3559C</td>
<td>-</td>
</tr>
<tr>
<td>arm-hisiv300-linux-uclibcgnueabi-gcc</td>
<td>arm-hisiv300-linux-uclibcgnueabi</td>
<td>hi3516A series</td>
<td>-</td>
</tr>
<tr>
<td>arm-hisiv400-linux-gnueabi-gcc</td>
<td>arm-hisiv400-linux-gnueabi</td>
<td>hi3516A series</td>
<td>-</td>
</tr>
<tr>
<td>arm-hisiv500-linux-uclibcgnueabi-gcc</td>
<td>arm-hisiv500-linux-uclibcgnueabi</td>
<td>hi3519 series</td>
<td>-</td>
</tr>
<tr>
<td>arm-hisiv600-linux-gnueabi-gcc</td>
<td>arm-hisiv600-linux-gnueabi</td>
<td>hi3519 series</td>
<td>-</td>
</tr>
</tbody>
</table>

> **NOTE** Developers need to select the library that specifies the compilation's toolchain according to the development platform. If there has no library for the toolchain in the package, please provide the **Development Platform's model**, **Compilation toolchain's model** and **Compilation toolchain's installation package** and send to <a href="mailto:dev@dji.com"> SDK Technical Support Team </a>, we will prepare the corresponding toolchain for you.
