# Element UI 学习笔记

## 参考资料
- [Element UI 源码解析](https://juejin.cn/post/7031331765482422280#heading-9)

## 新知识要点
1. [Process 对象](https://javascript.ruanyifeng.com/nodejs/process.html#toc1)
   
2. 重要开源项目
   - [`file-save`](https://npm.im/file-save)

## 拓展学习
Element UI 搜索功能实现:
- 文件路径: `\element\examples\components\search.vue`
- 搜索功能基于 `algoliasearch` 开源库实现 | 待深入研究

## 流程图 | element-ui 创建新组件
```mermaid
flowchart TD
    A[开始] --> B{检查命令行参数}
    B -->|无参数| C[错误提示并退出]
    B -->|有参数| D[获取组件名称和中文名称]
    D --> E[准备文件模板]
    E --> F[生成以下文件:]
    F --> F1[index.js - 组件入口文件]
    F --> F2[main.vue - 组件主文件]
    F --> F3[文档文件 .md]
    F --> F4[测试文件 .spec.js]
    F --> F5[样式文件 .scss]
    F --> F6[类型声明文件 .d.ts]
    
    E --> G[更新配置文件]
    G --> G1[更新 components.json]
    G --> G2[更新 index.scss]
    G --> G3[更新 element-ui.d.ts]
    G --> G4[更新 nav.config.json]
    
    G1 --> H[创建所有文件]
    G2 --> H
    G3 --> H
    G4 --> H
    H --> I[完成]
```
