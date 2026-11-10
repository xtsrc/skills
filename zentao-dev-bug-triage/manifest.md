# Zentao Bug 处理清单

> 全局清单。上限 100 条，新增覆盖最早创建记录。

| Bug ID | 标题 | 主项目 | 分支 | 创建时间 | 处理状态 | 对话框标题 | 最新更新时间 | 当前步骤 | 根因摘要 | 修改文件 | 验证结果 | 证据路径 |
|---:|---|---|---|---|---|---|---|---|---|---|---|---|
|---:|---|---|---|---|---|---|---|---|
| 50264 | 页脚版权年份仍为 2024 | resident-ui | bugfix/20261109 | 2026-11-10 10:45:00 | 验证完成待关闭 | 主对话 | 2026-11-10 16:46:54 | 第二轮 dev 回归通过 | 页脚年份硬编码为2024 | home-footer组件与eng/fra文案 | 通过 | regression-evidence-20261110.md |
 | 50261 | 通知铃铛红点与通知列表不一致 | resident-ui / resident-services | bugfix/20261109 | 2026-11-10 10:45:00 | 回归验证中 | 主对话 / bugfix50261 | 2026-11-10 17:39:52 | 前端bf307a67已部署dev，开始第四轮正数未读回归 | PostgreSQL布尔类型已修复；剩余根因为前端点击铃铛接口顺序错误 | ResidentTransactionRepository未读通知查询 | 等待第四轮接口与页面验证 | regression-evidence-20261110.md |  |  |  |  |  |
| 50240 | 新联系方式与当前一致仍可发送 OTP | resident-ui / resident-services | bugfix/20261109 | 2026-11-10 10:45:00 | 验证完成待关闭 | 主对话 / 独立对话框 | 2026-11-10 16:46:54 | 第二轮 dev 回归通过 | 前端仅按非空启用且后端缺少同值拦截 | updatedemographic组件、ContactDetailsServiceImpl | 通过 | regression-evidence-20261110.md |
| 50238 | 联系方式更新后短暂显示旧值 | resident-ui / resident-services | bugfix/20261109 | 2026-11-10 10:45:00 | 验证完成待关闭 | 主对话 | 2026-11-10 16:46:54 | 第二轮 dev 回归通过 | 前端自定义no-cache请求头触发CORS预检失败 | data-storage、updatedemographic、IdentityController | 通过 | regression-evidence-20261110.md |
| 50233 | Track My Requests 特殊字符触发退出确认弹窗 | resident-ui | bugfix/20261109 | 2026-11-10 10:45:00 | 验证完成待关闭 | 主对话 / 独立对话框 | 2026-11-10 16:46:54 | 第二轮 dev 回归通过 | dev缺少EID正则配置时undefined匹配空字符串 | trackservicerequest组件 | 通过 | regression-evidence-20261110.md |
| 50222 | 投诉工单状态与 GRM 不同步 | resident-services | bugfix/20261109 | 2026-11-10 10:45:00 | 验证完成待关闭 | 独立对话框 | 2026-11-10 14:12:00 | dev 回归通过 |  |  |  |  |
| 50196 | 附件支持选择 exe，缺少文件类型校验 | resident-ui | bugfix/20261109 | 2026-11-10 10:45:00 | 验证完成待关闭 | 独立对话框 | 2026-11-10 14:09:33 | dev 回归通过 |  |  |  |  |
| 50188 | Track My Requests 下载 VID 卡片 PDF 损坏 | resident-services / resident-ui | bugfix/20261109 | 2026-11-10 10:45:00 | 处理中 | 独立对话框 | 2026-11-10 10:45:00 | 只读排查中 |  |  |  |  |
| 50219 | GRM 待补充信息时居民门户只能补充文本 | resident-ui / resident-services / znuny | bugfix/20261109 | 2026-11-10 14:50:00 | 验证完成待关闭 | bugfix50219 | 2026-11-10 16:53:00 | dev 回归通过（含真实 UI 上传） |
| 50203 | 登录后无法点击图标回首页 | resident-ui | bugfix/20261109 | 2026-11-10 14:50:00 | 处理中 | bugfix50203 | 2026-11-10 15:20:00 | 等待方案确认 |
| 50181 | 帮助与投诉页面登录跳转 404 | resident-ui / resident-services | bugfix/20261109 | 2026-11-10 14:50:00 | 处理完成 | bugfix50181 | 2026-11-10 15:30:00 | 用户确认已在禅道关闭 |
| 50191 | Get Information 面包屑误跳首页 | resident-ui | bugfix/20261109 | 2026-11-10 14:50:00 | 验证完成待关闭 | bugfix50191 | 2026-11-10 15:51:00 | dev 回归通过 |
| 49822 | 撤销 VID 成功弹窗 Event ID 显示 null | resident-ui / resident-services | bugfix/20261109 | 2026-11-10 14:50:00 | 验证完成待关闭 | bugfix49822 | 2026-11-10 15:54:00 | dev 回归通过 | V2 响应体增加 eventId，前端优先 body 并回退响应头 | RevokeVidResponseDto.java、ResidentVidServiceImpl.java、ResidentVidServiceTest.java、revokevid.component.ts、revokevid.component.spec.ts | dev：UI commit 99cfcfb8 / services commit 615d8efd7d；弹窗、响应体、响应头、Track 跳转和查询均通过；测试 Temporary VID 已撤销清理 | E:\\project\\codex\\bug49822-dev-regression-20261110 |
