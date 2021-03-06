---
title: Device Connection
date: 2020-05-08
version: 2.1.0
keywords: [development kit, SkyPort, SkyPort V2, SkyPort, X-Port, load, adapter ring]
---
> **NOTE** This article is **Machine-Translated**. If you have any questions about this article, please send an <a href="mailto:dev@dji.com">E-mail </a>to DJI, we will correct it in time. DJI appreciates your support and attention.

Figure 1 display the process of connection, that connected Hardware Platform、Payload Development Board、Expansion board and DJI's drone.
> **NOTE** Some hardware interfaces that **were not described in this document** are temporarily unavailable.

<div>
<div style="text-align: center"><p>Figure 1 Device Connection</p>
</div>
<div style="text-align: center"><p><span>
      <img src="../images/device-connection-en.png" width="650" style="vertical-align:middle" alt/></span></p>
</div></div>

> **NOTE：** Using [User's Manual](https://www.dji.com/en/downloads) to know how to connect the drone and remote controller.

## NOTICE
* The details of the Hardware Platform, please refer to [Hardware Platform](../payloadguide/hardware.html).
* If you still use **PSDK V1.xx** and **SkyPort** to develop payload, please find the "PSDK 1.0.0" document on the package.

## Using X-Port
#### X-Port Pin 
Figure 2 shows the pin of X-Port. Use parts in [Payload SDK Development Kit 2.0](https://store.dji.com/product/psdk-development-kit-v2) connect the X-Port to expansion board for using third-party development board.

> **NOTICE:** Please use the specified cable connect the X-Port and the Expansion Board, confirmed that the red cable is aligned with the dot mark, otherwise the payload may burned.

<div>
<div style="text-align: center"><p>Figure 2 X-Port Pin</p>
</div>
<div style="text-align: center"><p><span>
      <img src="../images/Xportport-en.png" width="400"  style="vertical-align:middle" alt/></span></p>
</div></div>

<div>
<div>
<div  style="text-align: center"><p>Table 1 X-Port Pin</p>
</div>
<table id="interface parameters">
  <thead>
    <tr>
      <th>Pin Number</th>
      <th>Fnuction</th>
    </tr>
  </thead>
  <tbody>
   <tr>
      <td>1～６</td>
      <td>Power Supply </td>
    </tr> 
    <tr>
      <td>11、12 </td>
      <td>Payload communicate with drone（Must）</td>
    </tr>  
    <tr>
      <td>14</td>
      <td>Time Sync(the drone must have RTK)</td>
    </tr>
    <tr>
      <td>15,16 </td>
      <td>High Power Apply</td>
    </tr>
    <tr>
      <td>17～20</td>
      <td>Transfer the high-speed data.</td>
    </tr>
  </tbody>
</table>
</div></div>

#### Install The Payload
1. Install the spindle arm: Use four M2 × 12 screws to lock the payload, and the depth of the corresponding threaded hole on the payload is not less than 5.3 mm.
2. Install the auxiliary shaft arm: Use an M3 screw, auxiliary shaft sleeve, and auxiliary shaft rubber plug to lock the auxiliary shaft arm. Make sure the M3 screw passes through the center axis of the pitch axis.
3. The centroid of the payload
    * For a payload with a constant centroid, the payload must on the vertical line of the pitch axis;
    * For a zoom camera with a variable center of the centroid, the payload must on the vertical line of the pitch axis when the lens is at the maximum magnification.

## Using SkyPort V2
Figure 3 shows the pin of SkyPort V2. Use the cable to connect the SkyPort V2 to an expansion board or a third-party development board on the Port1; use coaxial cable to connect SkyPort V2 to the payload development board on the Port2.

> **NOTICE** 
> * Developer only could choose Port1 or Port2, both of them cannot be used at the same time.
> * Please use the specified cable connect the Port1 and the Expansion Board, confirmed that the red cable is aligned with the dot mark, otherwise the payload may burned.

<div>
<div style="text-align: center"><p>Figure 3 SkyPort V2 Pin</p>
</div>
<div style="text-align: center"><p><span>
      <img src="../images/Skyport2Port-en.png" width="600"  style="vertical-align:middle" alt/></span></p>
</div></div>

##### Port1 

<div>
<div>
<div style="text-align: center"><p>Table 2 SkyPort V2 Pin</p>
</div>
<table id="interface parameters">
  <thead>
    <tr>
      <th>Pin Number</th>
      <th>Fnuction</th>
    </tr>
  </thead>
  <tbody>
   <tr>
      <td>1～６</td>
      <td>Power Supply </td>
    </tr> 
    <tr>
      <td>11、12 </td>
      <td>Payload communicate with drone（Must）</td>
    </tr>  
    <tr>
      <td>14</td>
      <td>Time Sync(the drone must have RTK)</td>
    </tr>
    <tr>
      <td>15,16 </td>
      <td>High Power Apply</td>
    </tr>
    <tr>
      <td>17～20</td>
      <td>Transfer the high-speed data.</td>
    </tr>
  </tbody>
</table>
</div></div>

##### Port2 

<div>
<div>
<div style="text-align: center"><p>Table 3 SkyPort V2 Pin</p>
</div>
<table id="interface parameters">
  <thead>
    <tr>
      <th>Pin Number</th>
      <th>Fnuction</th>
    </tr>
  </thead>
  <tbody>
   <tr>
      <td>1～17</td>
      <td>Power Supply </td>
    </tr> 
    <tr>
      <td>37、39 </td>
      <td>Payload communicate with drone（Must）</td>
    </tr>  
    <tr>
      <td>19</td>
      <td>Time Sync(the drone must have RTK)</td>
    </tr>
    <tr>
      <td>22</td>
      <td>High Power Apply</td>
    </tr>
    <tr>
      <td>23、25、29、31</td>
      <td>Transfer the high-speed data.</td>
    </tr>
  </tbody>
</table>
</div></div>


## Using Expansion Board
Figure 4 shows the port of the expansion board. Use this board, developers could connect the third-party development board and a variety of payloads.

> **NOTICE:** Please use the specified cable connect the Third Development Board and the Expansion Board, confirmed that the red cable is aligned with the dot mark, otherwise the payload may burned.

<div>
   <div>
      <div style="text-align: center"><p>Figure 4 The port of expansion board</p>
      </div>
      <div style="text-align: center"><p><span>
      <img src="../images/Skyport2BOARD.png" width="280" style="vertical-align:middle" alt/></span></p>
      </div>
    </div>
<div style="text-align: center"><p>Table 4 The port of expansion board</p></div>
<div>
<table id="interface parameters">
  <thead>
    <tr>
      <th>Number</th>
      <th>Type</th>
      <th>Name </th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
   <tr>
      <td>J2</td>
      <td>Cable interface</td>
      <td rowspan=2>-</td>
      <td>Connect the expansion board with SkyPort V2 or X-Port.</td>
    </tr> 
    <tr>
      <td>J3</td>
      <td>Coaxial interface</td>
      <td>Connect the expansion board with SkyPort V2 or </br>payload development board. </td>
    </tr>  
    <tr>
      <td rowspan=3 >J10</td>
      <td rowspan=3>pin</td>
      <td>UART_TX；UART_RX</td>
      <td>Connect the expansion board with the third-party development board.</td>
    </tr>
    <tr>
      <td>PPS(Time Sync)</td>
      <td>Connect to the expansion board with the third-party development boardTime Sync(the drone must have RTK) </td>
    </tr>
    <tr>
      <td>HPWR</td>
      <td>High Power Apply</td>
    </tr>
    <tr>
      <td>J35</td>
      <td rowspan=3>Output</td>
      <td rowspan=3>-</td>
      <td>13.6V/4A or 17V/4A </td>
    </tr>
    <tr>
      <td>J36</td>
      <td>9V/2A</td>
    </tr>
    <tr>
      <td>J37</td>
      <td>5V/2A</td>
    </tr>
    <tr>
      <td>J40</td>
      <td>Network Port</td>
      <td>-</td>
      <td>Get the video stream and user-defined data information.</td>
    </tr>
  </tbody>
</table>
</div></div>

## Connect Development Board

> **NOTE** DJI PSDK uses the STM3241G-EVAL (STM32F417IG) to develop and debug samples. PSDK suggest developer refer to the [STM3241G-EVAL (STM32F417IG) ](https://www.st.com/en/evaluation-tools/stm3241g-eval.html) and purchase the development board they need.

#### Connect to the RTOS development board
Connect the STM32F407xG to the expansion board the configuration of the serial port is as follows:

> **NOTE** If you need to use other development boards, please rewrite the configuration parameters in the Hal file, for details, please refer to [Porting](../quickstart/porting.html)。

* Communicate with X-Port or SkyPort V2: `PA2 (TX)` and `PA3 (RX)`
* Communicate with computer: `PC10 (TX)` and `PC11 (RX)`
* Time Synchronization: `PD2`
* High Power Apply: `PD1`
* Baud rate: 460800

#### Connect to Linux development board
Connect the Manifold 2-C to the expansion board:

* Use USB to Serial-port module: Connect the USB to serial port module to the `UART_TX` and` UART_RX` pins of the expansion board.
* Use a network cable: Connect the third-party development boards and expansion boards.
