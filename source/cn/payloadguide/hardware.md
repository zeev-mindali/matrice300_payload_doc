---
title: 选购硬件平台
date: 2020-05-08
version: 2.1.0
keywords: [开发套件, SkyPort, SkyPort V2, SkyPort , X-Port, 负载, 拓展环]
---
> **注意**  
> * X-Port 和SkyPort V2 仅支持使用**PSDK V2.x.x**；
> * SkyPort 仅支持使用**PSDK V1.x.x** ；
> * DJI 已于 **2020年 2月 1日**停止对**PSDK V1.x.x** 和SkyPort 的开发，建议使用**X-Port** 或**SkyPort V2** 在**PSDK V2.x.x** 的基础上开发负载设备。

## 购买开发套件

#### X-Port <font color=#1fA3f6><a href="https://store.dji.com/cn/product/dji-x-port">（点击购买）</a></font>
开发者借助<a href="https://store.dji.com/cn/product/dji-x-port">X-Port</a> 能够**快速开发**出可挂载在DJI 无人机上具有**云台功能**的负载设备，借助PSDK 开放的API 接口实现高度定制化的同时，还能有效降低负载设备的开发成本，大幅度提升负载设备的**可靠性与兼容性**。

X-Port 包含如下配件：    
<div>
<div><p><span>
      <img src="../../images/XPort.png" width="800" alt/></span></p>
</div></div>

> **说明：** 使用[X-Port 标准云台](https://store.dji.com/cn/product/dji-x-port)开发具有云台功能的负载设备时，可借助[Payload SDK 开发套件 2.0](https://store.dji.com/cn/product/psdk-development-kit-v2)中的配件适配第三方开发平台。

#### SkyPort V2
借助<a href="https://store.dji.com/cn/product/psdk-development-kit-v2">SkyPort V2</a> 开发套件中的接口拓展板，开发者能够使用第三方开发板开发负载设备。    
SkyPort V2 包含如下配件：    
<div>
<div><p><span>
      <img src="../../images/V2.png" width="800" alt/></span></p>
</div></div>

> **说明：** 当负载设备进入量产阶段后，请购买 <a href="https://store.dji.com/cn/product/dji-skyport-adapter-set-v2">SkyPort V2 转接环套装</a>。

#### SkyPort
利用<a href="https://store.dji.com/cn/product/psdk-development-kit">SkyPort</a> 开发套件中的负载设备开发板，开发者无需购置第三方开发板，即可开发出功能全面且兼容性较好的负载设备。     
SkyPort 包含如下配件：  
<div>
<div><p><span>
      <img src="../../images/V1.png" width="700" alt/></span></p>
</div></div>

> **说明：** 当负载设备进入量产阶段后，请购买<a href="https://store.dji.com/cn/product/psdk-ribbon-cable-set">PSDK 同轴线套装</a>和 <a href="https://store.dji.com/cn/product/dji-skyport-adapter-set">SkyPort 转接环套装</a>。

## 硬件平台对比
<table id="开发套件对比">
  <thead>
    <tr>
      <th style="border:none">   </th>
      <th style="border:none;text-align:center">X-Port</th>
      <th style="border:none;text-align:center">SkyPort V2</th>
      <th style="border:none;text-align:center">SkyPort </th>
    </tr>
  </thead>
  <tbody>
    <tr style="text-align:center">
      <td style="border-right: none;text-align:left;border-left: none;"> </td>
      <td style="border-right: none;border-left: none;"><div><p><span>
      <img src="../../images/X-Port.png" height="220" width="220" style="vertical-align:middle" alt/></span></p></div></td>
      <td style="border-right: none;"><div><p><span>
      <img src="../../images/SkyPort2.png" height="190" width="150" style="vertical-align:middle" alt/></span></p></div></td>
      <td style="border-right: none;"><div><p><span>
      <img src="../../images/SkyPort1.png" height="190" width="150" style="vertical-align:middle" alt/></span></p></div></td>
    </tr>
    <tr style="text-align:center">
      <td style="border-right: none;text-align:left;border-left: none;"><b>硬件尺寸</b></td>
      <td style="border-right: none;border-left: none;"><div><p><span>
      <img src="../../images/XPort-size.png" height="190" width="240" style="vertical-align:middle" alt/></span></p></div></td>
      <td style="border-right: none;"><div><p><span>
      <img src="../../images/SkyPort2-size.png" height="190" width="220" style="vertical-align:middle" alt/></span></p></div></td>
      <td style="border-right: none;"><div><p><span>
      <img src="../../images/SkyPort1-size.png" height="190" width="200" style="vertical-align:middle" alt/></span></p></div></td>
    </tr>
    <tr style="text-align:center">
      <td style="border-left: none;text-align:left;border-right: none;"><b>重量</b></td>
      <td style="border-right: none;border-left: none;text-align:left">340g</td>
      <td style="border-right: none;">29g</td>
      <td style="border-right: none;">24g</td>
    </tr>
    <tr style="text-align:center">
      <td style="text-align:left;border-right: none;border-left: none"><b>负载重量</b></td>
      <td style="border-right: none;text-align:left;border-left: none;">450g</td>
      <td colspan="2" 1style="border-right: none;">单个负载设备的重量不超过600g</br><div style="background:#F2F2F2"> <b>说明：</b>有关负载设备重量的详细说明，请参见<a href=../payloadguide/payload-criterion.html>结构标准</a>。</div></td>
    </tr>
    <tr style="text-align:center">
      <td style="border-right: none;text-align:left;border-left: none;"><b>适配PSDK 版本</b></td>
      <td  colspan="2" style="border-right: none;border-left: none;">PSDK 2.0</br>
     </td>
      <td style="border-right: none;"> PSDK 1.0</td>
    </tr>
    <tr style="text-align:left">
      <td style="border-left: none;text-align:left;border-right: none;"><b>电压输出</b></td>
      <td style="border-right: none;text-align:left; border-right: none;border-left: none;"> 13.6V / 2A</br>17V / 2.5A(高功率申请)
     </td>
      <td style="border-right: none;"> 13.6V / 4A </br> 17V / 4A (高功率申请)</td>
      <td style="border-right: none;">M200 系列：12.7V / 4A </br>M200 V2 系列：13.6V / 4A </td>
    </tr>
    <tr>
    <td rowspan=2 style="border-top: none;border-left: none;border-right: none;text-align:left"><b>GPIO</b></td>
    <td colspan="2" style="text-align:center;border-left: none;">1个</td>
    <td style="border: none;text-align:center">ㄨ</td>
    </tr>
    <tr style="text-align:center" >
      <td colspan="3" style="border-top: none;border-right: none;border-right: none;border-left: none;">I/O 硬件触发</td>
    </tr>
    <tr style="text-align:center" >
      <td style="border-left: none;text-align:left;border-right: none;"><b>UART 信号传输</b></td>
      <td colspan="3" style="border-right: none;border-left: none;" >1个，使用UART 端口，通过TTL 电平（3.3V）传输数据</td>
    </tr>
    <tr style="text-align:center" >
      <td style="border-left: none;text-align:left;border-right: none;"><b>MDI 数据传输</b></td>
      <td colspan="3" style="border-right: none;border-left: none;" >1个，通过该接口传输视频流、媒体文件和高速数据</td>
    </tr>
    <tr style="text-align:center" >
      <td style="border-right: none;text-align:left;border-left: none;border-right: none;"><b>CAN 信号传输</b></td>
      <td colspan="2" style="border-right: none;border-left: none;">ㄨ</td>
      <td style="border-right: none;">传输控制命令</td>
    </tr>
    <tr style="text-align:center" >
      <td style="border-right: none;text-align:left;border-left: none;"><b>High Power Apply</b> </td>
      <td  colspan="2" style="border-left: none;border-right: none;">通过该接口输出申请高功率的数字信号（0～3.3V）</td>
      <td style="border-right: none;">ㄨ</td>
    </tr>
    <tr style="text-align:center" >
      <td style="border-left: none;text-align:left;border-right: none;"><b>PPS 信号传输</b></td>
      <td colspan="3" style="border-right: none;border-left: none;" >通过PPS 引脚传输数字信号（0～3.3V），实现时间同步功能</td>
    </tr>
    <tr style="text-align:left">
      <td style="border-right: none;text-align:left;border-left: none;"><b>适配机型</b></td>
      <td colspan="2" style="border-right: none;border-left: none;">• Matrice 300 RTK</br>• 经纬 M200 V2 系列：Matrice 200 V2、Matrice 210 V2、Matrice 210 RTK V2    
     </td>
      <td style="border-right: none;text-align:left ">• Matrice 300 RTK</br> • 经纬 M200 V1 系列：Matrice 200、Matrice 210、Matrice 210 RTK</br> • 经纬 M200 V2 系列： Matrice 200 V2、Matrice 210 V2 、Matrice 210 RTK V2</td>
    </tr>
  </tbody>
</table>

> **说明** 
> * X-Port 的防护等级：IP44，工作温度范围：-20°C～50°C。
> * 受实际工作环境的影响，X-Port 实际的工作电流可能会和额定电流有一定的差异。

## 选购第三方开发平台
DJI PSDK 使用STM3241G-EVAL(STM32F417IG) 开发板开发并调试示例程序，建议开发者参考[STM3241G-EVAL(STM32F417IG)](https://www.st.com/en/evaluation-tools/stm3241g-eval.html) 的参数信息选购所需使用的开发平台。  