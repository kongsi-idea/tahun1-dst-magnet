# handoff — tahun1-dst-magnet（磁铁大发现）

> 最后更新：2026-09-17（Codex @ 这台 Mac）

## 现在的状态
- 老师确认改做「磁力创造实验室」，核心价值是让学生创造并试玩自己的磁铁挑战。
- 产品拆成四个工作区：磁力探索桌、磁极谜题场、公平实验室、挑战创造工坊。
- 使用模式分为课堂投影与家庭探索；家庭使用不假设学生有实体磁铁。
- 完整开发 prompts 已写入 `docs/development-prompts.md`。
- 新版已由单一压缩 HTML 重构为 `index.html`、`styles.css`、`app.js`；包含 Canvas 实验桌、四工作区、老师控制台、预测计票、线索、打印、本机记录，以及挑战创建／试玩验证／JSON 导出。
- 老师首次打开时发现「课堂暂停」遮罩卡住首页；原因是 CSS 的 `display:grid` 覆盖 HTML `hidden` 属性，已用全局 `[hidden]{display:none!important}` 修复（`6b9a58e`）。
- 线上仍是 `8d25e20`；新版尚未 push。

## 已定产品要求
- 约 7 岁；单次 15 分钟；简体中文短句，不需要语音。
- 课堂老师投影、家庭学生一人一机；需适配电脑、手机和平板。
- 学习覆盖 DSKP 7.1.1–7.1.6 与 TP6，但拆成多次短活动。
- 学生偏好自由探索与创造；失败后给注意／关系／操作三层线索。
- 老师工具包括暂停、隐藏结果、磁力线、预测投票、讨论题、保存结果与打印实验单。
- 教师须知必须说明二维模拟需要成人支架与真实活动连接，并标明模拟并非精密测量。

## 下一步
- 由 Claude 把 `origin/main..HEAD` 的五个本地 commits 整理成一个最终 v2 commit，避免把两版被否决的「磁铁救援队」历史直接推上去。
- 完成 375／1440px 与四工作区完整交互验收；Codex 沙盒无法启动 Chromium。
- Push 后生产部署、确认正式 alias、线上复验，再拍新版真实缩图并回填 Kongsi Idea Hub。目前 Hub 登记已经更新并上线，但工具本身仍是旧线上版。

## 权限备注
Codex `~/.codex/config.toml` 已设 `writable_roots = ["/Users/yquanloo/Documents/my-projects"]`，新开的 cx 会话可以直接读写本专案并 commit；push 交给 Claude。

## Git 同步
- 本地：`main` 比 `origin/main` 超前 5 commits，工作区干净。
- GitHub：❌ 未推（需先整理历史；Codex 不执行远端操作）。
- 部署：❌ 未部署、未在线复验。
