# FU JIAHE 个人网站项目交接文档

最后更新：2026-08-18

项目目录：`/Users/jiahefu/Documents/ChatGPT/个人网站/fujiahe`

GitHub 仓库：<https://github.com/jiahefu/fujiahe>

当前工作分支：`design/homepage-directions-v1`

## 1. 项目背景

这个项目是 FU JIAHE 的个人主页。现有生产网站由 GitHub 仓库管理，并通过 GitHub Pages 和自定义域名发布；根目录的 `index.html` 是当前生产首页，`CNAME` 保存自定义域名配置。

本轮工作的起点是一份飞书说明：

<https://mqw3ik9pryl.feishu.cn/wiki/GoJnwME1miIN8wk5uskcZWMdndc>

工作目标不是立即替换线上网站，而是先探索并验证新版首页的定位、内容结构和视觉方向，在 Product Owner 确认后再进入正式生产替换流程。

## 2. 核心目标

新版主页要把 FU JIAHE 定位为面向 AI 时代的业务建设者，重点传达：

- 高管级的判断力和业务视角；
- 战略、AI 转型和企业增长经验；
- 能把新机会转化为战略、系统和团队；
- 有鲜明观点，但不做成传统简历或企业宣传页；
- 在专业权威之外，保留克制、可信的人性化表达。

核心英文定位是：

> Building businesses for the AI era.

> Strategy · AI Transformation · Enterprise Growth

> I turn emerging opportunities into strategy, systems and teams that create growth.

## 3. 内容与品牌边界

目前采用的共同约束如下：

- 不出现雇主名、公司名、未经批准的精确业务数据或结果；
- 不加入奖项、客户证言、虚构案例、简历下载或履历时间线；
- 不公开私人手机号；公开邮箱尚未确认，因此暂用占位提示；
- 微信联系方式为 `Chat_Away`；
- 只使用现有本地肖像照 `portrait.jpg`，不虚构宠物或生活方式图片；
- 不使用远程字体、远程资源、追踪器或前端框架；
- 避免紫蓝 AI 渐变、玻璃卡片、发光球体、聊天机器人界面和常见 SaaS 模板感；
- 在方向确认前，不修改根目录 `index.html`、`CNAME`、GitHub Pages 设置或 `main` 分支。

## 4. 已完成的工作

### 4.1 三个设计方向

已在 `design/homepage-directions-v1` 分支完成并提交三个独立原型：

- `prototypes/direction-a/index.html` — Direction A / Apple Executive

  近黑、暖白、大字号无衬线和大量留白，执行层级最简洁，管理者气质最强。
- `prototypes/direction-b/index.html` — Direction B / Editorial Leader

  编号、非对称版式和衬线/无衬线对比，最强调观点和思想领导力。
- `prototypes/direction-c/index.html` — Direction C / Human Business Builder

  更温暖、更叙事化，About 和个人层更突出，亲和力最强。

三个方向共用相同的核心故事、案例、原则和肖像，便于只比较创意方向，不让内容差异干扰判断。

相关说明：

- `PROTOTYPE_REVIEW.md`：三个方向的定位、优点、风险和评审问题；
- `design-qa.md`：桌面端、移动端、导航、无障碍、资源和视觉对照的 QA 记录；
- `prototypes/qa/`：三个方向的桌面、移动和重点区块截图及对比证据。

上述工作已提交并推送到远端：

- Commit：`f3265e4 Add three homepage design directions`
- 远端分支：`origin/design/homepage-directions-v1`

### 4.2 已完成的验证

A/B/C 三个方向均已按以下条件检查：

- 桌面视口：1440 × 1000；
- 移动视口：390 × 844；
- 无横向溢出；
- 本地肖像资源正常加载；
- 导航锚点均有对应区块，并完成代表性点击测试；
- 每页只有一个语义化 `h1`；
- 键盘焦点可见；
- `prefers-reduced-motion` 生效；
- 浏览器控制台无页面自身产生的警告或错误。

最终结果记录为 `passed`。

## 5. 当前选定方向

在 A/B/C 之后，已开始制作第四个候选页：

`prototypes/selected/index.html`

它不是对三个方向做平均，而是按以下权重形成一个更接近生产版本的候选方案：

- 70% Direction A：英雄区、核心配色、留白、现代无衬线、肖像、高管气质和克制动效；
- 20% Direction B：轻量编号、领导案例框架、更强的观点层级和 Perspectives 节奏；
- 10% Direction C：更完整的 About、克制的个人层和稍温暖的语气。

明确没有继承：

- B 的完整 Georgia/锈红/字母标识/自我引语体系；
- C 的橄榄绿/陶土色、重复肖像、生活方式页面感，以及 “Let's build what's next.”。

### Selected 页面内容结构

1. Hero：姓名、AI 时代业务定位、能力范围和现有肖像；
2. Leadership Thesis：`Execution is getting cheaper. Judgment is not.`；
3. Selected Leadership Cases：三个领导力案例；
4. AI Transformation：`Tools don't transform businesses. Workflows do.`；
5. Perspectives：只保留三个优先观点，不放虚构文章链接；
6. About：工程背景、业务建设者经历和好奇心，不放雇主与时间线；
7. Beyond work：家庭、两只喜乐蒂、两只猫和旅行；
8. Contact：`Start a conversation.`、待确认公开邮箱和微信 `Chat_Away`。

## 6. 当前真实状态

截至 2026-08-18 本轮设计交付完成时：

- 当前分支仍为 `design/homepage-directions-v1`；
- A/B/C 原型已提交并已推送；
- `prototypes/selected/index.html` 已完成；
- Selected 页已通过 1440 × 1000 桌面和 390 × 844 移动视觉检查；
- 首轮发现 Beyond Work 标签继承正文大字号，现已通过专用 `.beyond-copy` 样式修正；
- Selected 的 QA 证据已归档到 `prototypes/qa/`；
- A/B/C 取舍与五项评审结论已写入 `SELECTED_DIRECTION_REVIEW.md`；
- `design-qa.md` 已追加 Selected 的完整检查记录，最终结果为 `passed`；
- 根目录生产 `index.html` 和 `CNAME` 未修改；
- 没有创建 Pull Request，没有合并到 `main`，也没有发布 Selected 页面。

接手时应先运行：

```bash
cd "/Users/jiahefu/Documents/ChatGPT/个人网站/fujiahe"
git status --short --branch
git log --oneline --decorate -3
```

先确认当前分支与远端同步，再开始后续修改，避免直接在 `main` 上覆盖生产页面。

## 7. 下一步待办

下一步只剩 Product Owner 决策：

1. 审阅 Selected 候选页和 `SELECTED_DIRECTION_REVIEW.md`；
2. 确认公开邮箱地址，或继续保留明确占位提示；
3. 决定是否授权进入生产实现；
4. 获得授权后，另开生产分支，把获批方案迁移到根目录 `index.html`；
5. 通过 Pull Request 审阅后再合并 `main`，由 GitHub Pages 发布。

未经新的生产授权，不修改 `index.html`、`CNAME`、Pages 设置或 `main`。

## 8. 本地预览方法

在仓库根目录运行：

```bash
python3 -m http.server 4173 --bind 127.0.0.1
```

然后访问：

- Selected：<http://127.0.0.1:4173/prototypes/selected/>
- Direction A：<http://127.0.0.1:4173/prototypes/direction-a/>
- Direction B：<http://127.0.0.1:4173/prototypes/direction-b/>
- Direction C：<http://127.0.0.1:4173/prototypes/direction-c/>
- 当前生产首页的本地版本：<http://127.0.0.1:4173/>

## 9. 后续修改与 GitHub 工作流

后续改网页内容，推荐通过 Git/GitHub 管理，但 `pull` 和 `merge` 的作用不同：

- `git pull`：把 GitHub 上最新代码同步到本地，不会发布你的本地修改；
- 本地编辑：在新分支或现有设计分支修改网页；
- `git add` + `git commit`：记录本地改动；
- `git push`：把分支推送到 GitHub；
- Pull Request：让改动进入审阅流程；
- `merge` 到 `main`：把批准的改动纳入生产分支；
- 如果 GitHub Pages 配置为从 `main` 发布，合并后才会触发线上网站更新。

推荐的正式流程：

```text
同步 main → 新建功能分支 → 修改并本地预览 → 提交 → 推送 → Pull Request → 审阅 → 合并 main → GitHub Pages 发布
```

小型文案修改也可以直接在 GitHub 网页编辑，但仍建议通过分支和 Pull Request，便于审阅、回滚和保留历史。

## 10. 登录与权限

- 浏览公开 GitHub 仓库和本地预览不需要额外登录；
- 推送分支、创建 Pull Request 或合并时，需要有 `jiahefu/fujiahe` 仓库的 GitHub 权限，本机 Git 凭据失效时需重新登录；
- 如果后续需要重新读取受权限保护的飞书说明，则可能需要用户在浏览器中登录飞书；
- 当前阶段不需要 GitHub Pages、域名或其他生产环境权限，因为尚未进入发布步骤。

## 11. 关键文件索引

| 文件 | 用途 | 当前状态 |
| --- | --- | --- |
| `index.html` | 当前生产首页 | 未修改 |
| `CNAME` | GitHub Pages 自定义域名 | 未修改 |
| `prototypes/direction-a/index.html` | Apple Executive 原型 | 已提交、已推送 |
| `prototypes/direction-b/index.html` | Editorial Leader 原型 | 已提交、已推送 |
| `prototypes/direction-c/index.html` | Human Business Builder 原型 | 已提交、已推送 |
| `prototypes/selected/index.html` | 当前选定的生产候选页 | 已完成，见当前设计分支最新提交 |
| `PROTOTYPE_REVIEW.md` | A/B/C 评审说明 | 已提交、已推送 |
| `SELECTED_DIRECTION_REVIEW.md` | Selected 取舍与评审说明 | 已完成，见当前设计分支最新提交 |
| `design-qa.md` | A/B/C 与 Selected 设计 QA 记录 | 已完成，最终结果 `passed` |
| `prototypes/qa/` | 视觉 QA 截图和对照证据 | A/B/C 与 Selected 均已归档 |

## 12. 交接完成标准

本轮设计实现与验证已经完成。进入生产阶段前仍需满足：

- Selected 页面内容和视觉方向得到 Product Owner 确认；
- Product Owner 提供或批准公开邮箱处理方式；
- 生产替换获得单独授权；
- 生产首页、域名配置和 `main` 在批准前保持不变；
- 后续通过单独的生产 Pull Request 审阅和合并。
