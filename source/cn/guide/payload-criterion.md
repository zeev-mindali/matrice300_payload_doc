---
title: 负载开发标准
date: 2020-01-17
version: 2.0.0
keywords: [相机码流, 标准, 负载标准, 设备干扰, 硬件标准, 结构标准, 数据传输, 视频标准]
---
为确保无人机在搭载负载设备执行飞行任务时的安全，请在使用PSDK 开发负载设备时，遵循DJI 的负载设备开发标准。

> **注意** 
> * X-Port 和Skyport V2 仅支持使用**PSDK V2.x.x**；
> * Skyport 仅支持使用**PSDK V1.x.x** ；
> * DJI 将在 **2020年 2月 1日**停止对**PSDK V1.x.x** 和Skyport 的维护，建议使用**X-Port** 或**Skyport V2** 在**PSDK V2.x.x** 的基础上开发负载设备。

>**本文所指** 
> * “移动端APP” 为使用MSDK 开发的移动端APP 或DJI Pilot。
> * “负载设备” 为使用PSDK 开发的负载设备。
> * “机载计算机” 为运行了基于OSDK 开发的无人机控制程序的计算设备，如Manifold。


## 硬件标准
> **注意**
> * **禁止**将无人机或硬件平台的引脚短路。
> * **禁止**将无人机连接到电源输出系统，向飞机输入电流。

##### 使用 M200 V2 Series

<table>
<thead>
<tr>
  <th>接口引脚</th>
  <th>硬件平台</th>
  <th>指标要求</th>
 </tr>
</thead>
 <tbody>
 <tr>
  <td rowspan="3">普通功率输出</td>
  <td>X-Port</td>
  <td>13.6V / 2A</td>
 </tr>
 <tr>
  <td>Skyport V2</td>
  <td>13.6V / 4A</td>
 </tr>
 <tr>
  <td>Skyport</td>
  <td>13.6V / 4A</td>
 </tr>
 <tr>
  <td rowspan="2">高功率输出</td>
  <td>X-Port</td>
  <td>17V / 2.5A</td>
 </tr>
 <tr>
  <td>Skyport V2</td>
  <td>17V / 4A</td>
 </tr>
 <tr>
  <td>PPS 引脚电压</td>
  <td rowspan="3">X-Port</br>
    Skyport V2</br>
    Skyport</td>
  <td>≤3.3V</td>
 </tr>
 <tr>
  <td>UART引脚</td>
  <td>须遵循3.3V TTL 协议</td>
 </tr>
 <tr>
  <td>LAN接口</td>
  <td>须遵循LAN IEEE802.3 协议</td>
 </tr>
 <tr>
  <td>CAN接口引脚</td>
  <td>Skyport</td>
  <td>须遵循CAN 协议</td>
 </tr>
</tbody>
</table>

##### 使用 M200 Series
> **说明：** DJI M200 Series 仅支持挂载使用<b>Skyport</b> 开发的负载设备。
<table>
<thead>
<tr>
  <th>接口引脚</th>
  <th>指标要求</th>
 </tr>
</thead>
 <tbody>
 <tr>
  <td >普通功率输出</td>
  <td>12.7V / 4A</td>
 </tr>
 <tr>
  <td>PPS 引脚电压</td>
  <td>≤3.3V</td>
 </tr>
 <tr>
  <td>UART引脚</td>
  <td>须遵循3.3V TTL 协议</td>
 </tr>
 <tr>
  <td>LAN接口</td>
  <td>须遵循LAN IEEE802.3 协议</td>
 </tr>
 <tr>
  <td>CAN接口引脚</td>
  <td>须遵循CAN 协议</td>
 </tr>
</tbody>
</table>

## 电磁与声光噪声干扰
<table>
<thead>
 <tr>
      <th>干扰项</th>
      <th>指标详情</th>
    </tr>
</thead>
<tbody>
<tr>
      <td>声波噪声</td>
      <td>规避频段：35～45KHz</td>
    </tr>
    <tr>
      <td>光源闪烁</td>
      <td>光源闪烁频率不可处于0.2～50Hz</td>
    </tr>
    <tr>
      <td>光波发射</td>
      <td>规避波长：600～700nm</td>
    </tr>
    <tr>
      <td>磁场</td>
      <td>• 禁止负载设备携带强磁性物质</br>• 禁止产生高强度交变磁场</td>
    </tr>
    <tr>
      <td rowspan="2">电磁波噪声</td>
      <td>• 规避频段：1～1.7GHz；2.4～2.5GHz；5.8～5.9GHz</br>• 等效全向辐射功率（EIRP）须小于1W</td>
    </tr>
    <tr>
      <td>• 规避频段：1～1.7GHz；2.3～2.6GHz；5.7～5.9GHz</br>• 等效全向辐射功率（EIRP）须小于1W</td>
    </tr>
</tbody>
</table>

## 结构标准
> **说明**
> * 为避免搭载在无人机上的负载设备受无人机飞行惯性的影响，撞击电池仓和桨叶，损毁无人机或负载设备，请合理地设计负载设备的尺寸；
> * 当单个负载设备的重量在**600～1200g** 时，为避免损坏减震球，请使用双云台承载负载设备的重量，同时请确保负载设备的重心在**双云台接口的中心上**，为确保您设计的负载设备安全可靠，建议您将超过600g 的负载设备交由DJI 评估。

<table id="PSDK technical integration notes">
  <thead>
    <tr>
      <th>结构参数</th>
      <th>参数说明</th>
    </tr>
  </thead>
  <tbody>
      <tr>
      <td>外壳温度</td>
      <td>≤70℃</td>
    </tr>
    <tr>
      <td>重量</td>
      <td>≤1200g </td>
    </tr>
    <tr>
      <td>重心</td>
      <td>＜600g ，负载设备的重心应在<b>云台口中心的垂直线上</b></br>600g～1200g ，负载设备的重心应在<b>双云台接口连线的中心上</b></td>
    </tr>
    <tr>
      <td>结构干涉</td>
      <td>在无人机执行飞行任务时，<b>禁止</b>负载设备碰撞到无人机上的各个部件</td>
    </tr>
    <tr>
      <td>振动</td>
      <td>无人机开机后，在静止状态下，负载设备<b>不可产生影响IMU的振动</b>（在DJI Pilot 或移动端APP 上可查看IMU 状态）</td>
    </tr>
        <tr>
      <td>运动轨迹</td>
      <td>负载设备的运动轨迹不可遮盖<b>传感器和通风孔</b>：</br>1. 前视视觉传感器的视场角为75° × 60°（水平×竖直）；</br>2. 下视视觉传感器的视场角为75° × 60°（横向×纵向）；</br>3. 距超声波传感器10cm 的范围内，传感器的感应范围为100°，10cm外的感应范围为70°；</br>4.距红外传感器15cm 的范围内，红外传感器的感应范围为60°，15cm外的感应范围为20°；</br>5.距无人机机身前部与尾部10 cm的范围为进风口和出风口。
</td>
    </tr>
   </tbody>
</table>

## 数据传输
##### 使用M200 V2 Series

<table>
<thead>
    <tr>
      <th>通道类型</th>
      <th>传输方向</th>
      <th>速率限制</th>
    </tr>
  </thead>
<tbody>
 <tr>
    <td rowspan="4">命令通道</td>
    <td rowspan="1">移动端APP ➟ 负载设备</td>
    <td rowspan="4">≤4096B/s</td>
    </tr>
     <tr>
      <td>负载设备 ➟ 移动端APP </td>
    </tr>
    <tr>
      <td>机载计算机 ➟ 负载设备</td>
    </tr>
    <tr>
      <td>负载设备 ➟ 机载计算机</td>
    </tr>
    <tr>
      <td>高速数据传输通道</td>
      <td>负载设备 ➟ 移动端APP</td>
      <td>单云台：≤ 8192Kbps</br>双云台：每个云台的传输速率≤ 4096Kbps</td>
    </tr>
</tbody>    
</table>

##### 使用M200 Series

> **说明：** DJI M200 Series 仅支持使用<b>Skyport</b> 开发的负载设备与移动端APP 间传输数据信息。
<table>
<thead>
    <tr>
      <th>通道类型</th>
      <th>传输方向</th>
      <th>速率限制</th>
    </tr>
  </thead>
<tbody>
 <tr>
       <td rowspan="2">命令通道</td>
      <td>移动端APP ➟ 负载设备</td>
      <td>≤500B/s</td>
    </tr>
    <tr>
      <td>负载设备 ➟ 移动端APP</td>
      <td>≤3072B/s</td>
    </tr>
    <tr>
      <td>高速数据传输通道</td>
      <td>负载设备 ➟ 移动端APP</td>
      <td>单云台：≤8192Kbps</br>双云台：每个云台的传输速率≤4096Kbps</td>
    </tr>
</tbody>    
</table>


## 视频标准
使用PSDK 开发的**相机类**负载设备，**必须**使用**H.264 编码标准**。

1. 视频分辨率最大不超过**1920 × 1080**；
2. 帧率最大不超过**30fps**，最大码率不超过**8Mbps**；
3. 推荐视频长宽比为4：3（使用DJI CrystalSky时，画面可占满屏幕）。

>**注意：** 使用H.264 编码标准时，GOP 编码结构必须选用Period I（帧内编码帧，每隔1 秒将插入1 个IDR 帧，确保图像数据丢失时可被恢复）。

基于PSDK 开发的**相机类**负载设备，在使用**H.264 编码标准**时，需注意如下关键配置信息：       
<table id="表1.Topic information table">
  <thead>
    <tr>
      <th>关键项</th>
      <th>H.264 标准项</th>
      <th>取值</th>
    </tr>
  </thead>
  <tbody>
 <tr>
      <td>档次 </td>
      <td> Level Number</td>
      <td> ＜5.1 </td>
</tr>
<tr>
      <td>profile_idc</td>
      <td>7.3.2.1.1</td>
      <td> Baseline=66，Main=77，High=100 </td>
</tr>
<tr>
      <td>YUV420 格式 </td>
      <td>7.3.2.1.1</td>
      <td>chroma_format_idc=1 </td>
</tr>
<tr>
      <td>8Bit 视频 </td>
      <td>7.3.2.1.1</td>
      <td>bit_depth_luma_minus8=0</br>bit_depth_chroma_minus8=0 </td>
</tr>
<tr>
      <td>不允许编码器自定义 Scaling Matrix </td>
      <td> 7.3.2.1.1</br>7.3.2.2 </td>
      <td>seq_scaling_matrix_present_flag=0 </br>
      pic_scaling_matrix_present_flag=0 </td>
</tr>
<tr>
      <td>仅支持帧格式编码，不支持场编码 </td>
      <td>7.3.2.1.1 </td>
      <td>frames_mbs_only_flag=1</td>
</tr>
<tr>
      <td>仅允许 P 帧和 I 帧，且P 帧有单个参考帧 </td>
      <td>7.3.3 </br> 7.3.2.2 </br> 7.3.3 </td>
      <td> slice_type = 0 或 2 </br>num_ref_idx_l0_default_active_minus1=0 </br> num_ref_idx_active_override_flag=0</td>
</tr>
<tr>
      <td>不支持多Slice Group </td>
      <td>7.3.2.2 </td>
      <td>num_slice_groups_minus1=0 </td>
</tr>
</tbody>
</table>

>**相关参考：** <a href="https://www.itu.int/rec/T-REC-H.264-201906-I/en">H.264 协议标准</a>


