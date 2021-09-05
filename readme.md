# **为 rt-thread 提供的设备框架**

## 0. 简介
* 该项目包含并相关多个 rust 工程
 其中包括：本项目（提供基本的框架）、rtt_rs（提供对rt-thread的基本接口）、异步运行库（提供异步运行时，实现设备的异步访问。 注：该项目是async_on-embedded的移植和补充）。
* 目前经过简单的测试，该框架能正常工作，并能实现互斥读写设备。
* 目前已经能够支持单一访问设备、非单一访问设备、自动关闭设备。
* 目前的测试设备为 stm32f746zg-nucleo | art-pi

## 1. 目前仍在开发：
* 本项目框架补充，目前仅实现了led。
* 补充rtt_rs项目，为异步运行打基础。
* 移植补充异步运行时库，重点补充基础设施（如sleep）。

_目前正在开发基于rust所写的rt-thread内核，希望能更好的支持设备的异步访问。_

## 2. 目前基本完成：
* 设备存储查找打开方式、互斥访问、可独占\共享设备、设备自动关闭
* 文件读写的数据传输方式 
* 设备上层框架与BSP框架的对接形式

## 3. 目前已经稳定：


## 4. 关于异步运行时
* 修改自开源的 async-on-embedded

_地址： https://gitee.com/vitors/async-on-embedded_