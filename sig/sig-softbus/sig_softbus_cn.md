# SIG-SoftBus
简体中文 | [English](./sig_softbus.md)

说明：本SIG的内容遵循OpenHarmony的PMC管理章程 [README](/zh/pmc.md)中描述的约定。

## SIG组工作目标和范围

### 工作目标
为开源社区软总线持续贡献力量，实现近场设备间统一的分布式通信能力管理，提供不区分链路的设备发现、组网和传输能力。

### 工作范围
- 负责分布式软总线相关软件模块架构设计、评审和决策；
- 负责分布式软总线领域软件模块的代码审核、合入，禁止低质量代码合入开源版本主干，负责测试代码看护；
- 积极有效参与开源社区代码检视与点评，共享编程经验，与开源社区开发者交流，传递软件开发技能，有效辅导开源社区开发者写出好代码；
- 处理开源社区上的需求、issue、邮件列表和开发问题，闭环周期满足开源社区的SLA要求；
- 结合评审和开发活动，给予代码质量反馈与指导，促进开源社区代码质量提升。

## 代码仓
- 代码仓地址：
  - communication_dsoftbus：https://gitee.com/openharmony/communication_dsoftbus
  - communication_ipc：https://gitee.com/openharmony/communication_ipc
  - communication_ipc_lite：https://gitee.com/openharmony/communication_ipc_lite
  - communication_bluetooth：https://gitee.com/openharmony/communication_bluetooth
  - communication_nfc：https://gitee.com/openharmony/communication_nfc
  - communication_wifi：https://gitee.com/openharmony/communication_wifi
  - communication_wifi_lite：https://gitee.com/openharmony/communication_wifi_lite
  - communication_wifi_aware：https://gitee.com/openharmony/communication_wifi_aware
  - base_location：https://gitee.com/openharmony/base_location
  - telephony_call_manager：https://gitee.com/openharmony/telephony_call_manager
  - telephony_cellular_call：https://gitee.com/openharmony/telephony_cellular_call
  - telephony_core_service：https://gitee.com/openharmony/telephony_core_service
  - telephony_sms_mms：https://gitee.com/openharmony/telephony_sms_mms
  - telephony_state_registry：https://gitee.com/openharmony/telephony_state_registry
  - applications_camera_sample_communication：https://gitee.com/openharmony/applications_camera_sample_communication
  - applications_sample_wifi_iot：https://gitee.com/openharmony/applications_sample_wifi_iot
  - iothardware_peripheral：https://gitee.com/openharmony/iothardware_peripheral
  - iot_link：https://gitee.com/openharmony/iot_link
  - third_party_lwip：https://gitee.com/openharmony/third_party_lwip
  - third_party_nfc-nci：https://gitee.com/openharmony-sig/third_party_nfc-nci
  - third_party_wpa_supplicant：https://gitee.com/openharmony/third_party_wpa_supplicant
  - third_party_libcoap：https://gitee.com/openharmony/third_party_libcoap

## SIG组成员

### Leader
- @MaErlii(https://gitee.com/maerlii)

### Committers列表
- @xuyongpan(https://gitee.com/xuyongpan)
- @yinyouzhan(https://gitee.com/yinyouzhan)
- @rain_myf(https://gitee.com/rain_myf)
- @bigpumpkin(https://gitee.com/bigpumpkin)
- @jyh926(https://gitee.com/jyh926)
- @life-liu(https://gitee.com/life-liu)
- @knpingan(https://gitee.com/knpingan)
- @hwlitao(https://gitee.com/hwlitao)
- @defeng2020(https://gitee.com/defeng2020)
- @brickhz(https://gitee.com/brickhz)
- @clevercong(https://gitee.com/clevercong)
- @ohos-lsw(https://gitee.com/ohos-lsw)
- @xautosoft(https://gitee.com/xautosoft)
- @li-jet(https://gitee.com/li-jet)
- @MaErlii(https://gitee.com/maerlii)

### 会议
 - 会议时间：双周例会，周一下午16:00，UTC+8
 - 议题申报: [OpenHarmony SIG-SoftBus Meeting Proposal](https://shimo.im/sheets/iDp1dGmnk3sVjJoE/MODOC)
 - 会议链接：Welink
 - 会议通知: 请[订阅](https://lists.openatom.io/postorius/lists/sig_dsoftbus.openharmony.io) 邮件列表 sig_dsoftbus@openharmony.io 获取会议链接
 - 会议纪要：查看往期会议纪要，请点此[会议纪要](https://gitee.com/openharmony-sig/sig-content/blob/master/softbus/meetings)

### 联系方式(可选)
| 地址                                 | 简介        | 用途说明                                                         |
| ---------------------------------------|---------- | ------------------------------------------------------------ |
| dev@openharmony.io  <img width=120/>| 开发邮件列表 <img width=100/> | OpenHarmony社区开发讨论邮件列表，任何社区开发相关话题都可以在邮件列表讨论。任何开发者可[订阅](https://lists.openatom.io/postorius/lists/dev.openharmony.io)。<img width=200/>|
| sig_dsoftbus@openharmony.io  <img width=120/>| Sig-Softbus邮件列表 <img width=100/> | OpenHarmony社区SIG-Softbus开发讨论邮件列表，任何软总线开发相关话题都可以在邮件列表讨论。任何开发者可[订阅](https://lists.openatom.io/postorius/lists/sig_dsoftbus.openharmony.io/)。<img width=200/>|
