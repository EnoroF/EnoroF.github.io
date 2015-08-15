---
layout: post
title: EGE架构调整
category: tech
---
***
EGE全称为EnoroF's Game Engine, 于2012年5月在大四在学校进行开发, 初版是Ogre的改造版本, 后面再引擎中心实习时, 抛弃Ogre从头开始设计, 初衷是完成一个比较炫酷的实时渲染器, 并且当做毕业设计提交.

2年半来, EGE增加了不少时髦的新功能, 渲染上也基本能赶上时代的步伐, 地球在自传, 时代在进步, EGE的固有结构, 个人觉得已经落伍, 参考了不少开源和商业引擎后, 结合自己想法, 将对引擎结构进行一次较大调整.

***
### 目录
    - [ ] Core
        - [ ] Unreal方式完成RTTI改造
        - [ ] Unreal平台工具链
    - [ ] Renderer
        - [ ] 集成VXGI
        - [ ] 集成SVO
        - [ ] 集成LPV
    - [ ] UI
        - [ ] 移植Unreal-Slate
    - [ ] GameFramework
        - [ ] BehaviorTree
        - [ ] 移植Unreal-BluePrint
    - [ ] Script
        - [ ] 增加模板支持