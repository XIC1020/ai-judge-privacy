
<h1>AI研判助手 · 隐私政策</h1>
<div class="meta">
  适用扩展：AI研判助手 · ScrapeGraph（Microsoft Edge 扩展，Manifest V3）<br>
  最后更新：2026-10-21　生效日期：2026-10-21
</div>

<p>本扩展由个人开发者（以下称“我们”）提供，用于在用户主动发起时，对当前网页内容进行信息采集与 AI 研判。我们尊重并保护用户隐私。本政策说明本扩展会处理哪些数据、为何处理、存放位置以及用户如何删除。</p>

<h2>1. 我们处理的数据</h2>
<table>
  <tr><th>数据类型</th><th>何时处理</th><th>用途</th></tr>
  <tr>
    <td>当前网页正文 / 用户选中的文本</td>
    <td>仅在用户点击「研判本页」或「研判选中文本」时读取一次</td>
    <td>作为本次研判的输入材料</td>
  </tr>
  <tr>
    <td>用户填写的研判目标、场景、调查路径名称</td>
    <td>用户输入并点击研判时</td>
    <td>决定研判方式与结果格式；调查路径用于在本机累积同一主题的证据</td>
  </tr>
  <tr>
    <td>用户自行填写的第三方 AI API Key、供应商与模型名称</td>
    <td>用户填写时保存</td>
    <td>由用户本机的分析服务调用其自选的 AI 接口；<b>仅保存在本机浏览器存储</b></td>
  </tr>
  <tr>
    <td>界面偏好（悬浮球位置、面板固定状态、上次选项）</td>
    <td>用户操作时</td>
    <td>恢复上次界面状态</td>
  </tr>
  <tr>
    <td>证据快照（可选）</td>
    <td>用户勾选「保存证据快照」并研判时</td>
    <td>保存在用户本机磁盘（默认 <code>~/.scrapegraphai/snapshots</code>），便于复核</td>
  </tr>
</table>

<p><b>我们不收集：</b>浏览历史、账号密码、Cookie、剪贴板、键盘输入、地理位置、通讯录、设备标识符；不进行用户画像、广告投放或行为追踪；不接入任何统计/分析 SDK。</p>

<h2>2. 数据流向</h2>
<ul>
  <li><b>默认路径（本地）</b>：浏览器扩展 → 用户本机的分析服务 <code>http://127.0.0.1:8765</code> → 结果返回浏览器。数据不经过开发者服务器，我们无法访问。</li>
  <li><b>用户配置第三方 AI 后</b>：若用户填写 API Key，则本次研判的正文与提示词会由<b>用户本机的服务</b>发送至用户所选的服务商（如 DeepSeek、OpenAI、Kimi 等）。该传输由用户主动配置并授权，适用对应服务商的隐私政策。</li>
  <li><b>跨页面查证</b>：本机服务会自行访问公开网页以检索证据；此过程不向第三方发送用户身份信息。扩展本身不直接访问外部网络。</li>
  <li><b>开发者无服务器</b>：我们没有用于接收用户数据的后端、数据库或日志系统。</li>
</ul>

<h2>3. 数据存储与保留</h2>
<ul>
  <li>API Key 与界面偏好：保存于浏览器本地扩展存储（<code>chrome.storage.local</code>），不上传。</li>
  <li>证据快照与调查路径：保存于用户本机磁盘，由用户自行管理。</li>
  <li>我们不在任何服务器保留用户数据；研判结果仅在当次页面会话中展示。</li>
</ul>

<h2>4. 数据删除</h2>
<ul>
  <li>清除扩展数据：在浏览器扩展管理页移除本扩展，或清除该扩展的本地存储，即可删除 API Key 与设置。</li>
  <li>删除快照/路径：直接删除本机目录 <code>~/.scrapegraphai</code>（Windows：<code>%USERPROFILE%\.scrapegraphai</code>）。</li>
  <li>若曾使用第三方 AI API，请按该服务商的政策在其平台删除相关记录。</li>
</ul>

<h2>5. 权限说明</h2>
<table>
  <tr><th>权限</th><th>用途</th></tr>
  <tr><td><code>storage</code></td><td>保存 API Key（仅本机）、模型选择、悬浮球位置等界面偏好</td></tr>
  <tr><td><code>activeTab</code></td><td>用户点击研判按钮时读取当前标签页正文或选中文本</td></tr>
  <tr><td>访问 <code>127.0.0.1:8765</code> / <code>localhost:8765</code></td><td>与用户本机运行的分析服务通信</td></tr>
  <tr><td>在所有网站注入内容脚本</td><td>仅用于显示可拖动的悬浮球；未点击时不读取页面内容</td></tr>
</table>

<h2>6. 合规与用户责任</h2>
<ul>
  <li>本扩展仅用于处理用户有权访问的公开页面或用户自行提供的材料；用户应遵守目标网站的 robots 协议、服务条款、版权与隐私要求。</li>
  <li>不得用于绕过登录、付费墙、验证码或访问控制，不得用于采集敏感个人信息。</li>
  <li>研判结果由规则与 AI 生成，可能存在偏差，仅供信息参考，不构成法律、医疗、投资或购买决策建议。</li>
</ul>

<h2>7. 儿童隐私</h2>
<p>本扩展不面向 13 岁以下儿童设计，也不会有意收集儿童个人信息。</p>

<h2>8. 政策更新</h2>
<p>如本政策发生实质变更，我们会在本页面更新“最后更新”日期，并在扩展更新说明中提示。继续使用即表示接受更新后的政策。</p>

<h2>9. 联系方式</h2>
<p>隐私相关问题请联系：<b>请替换为你的联系邮箱</b>（例如 <code>your-email@example.com</code>）。我们会在合理期限内回复。</p>

<div class="en">
<h2>English Summary</h2>
<p><b>What we process.</b> The extension reads the current page's visible text (or your selected text) only when you click “Analyze”. Your API key, chosen model, goal and UI preferences are stored locally in your browser. Optional evidence snapshots are written to your local disk (<code>~/.scrapegraphai/snapshots</code>).</p>
<p><b>Where data goes.</b> Page content is sent to the analysis service running on your own machine (<code>http://127.0.0.1:8765</code>). We operate no server and receive no user data. If you configure a third-party AI API key, your local service sends the content to the provider you selected, under that provider's privacy policy.</p>
<p><b>What we never collect.</b> Browsing history, credentials, cookies, clipboard, keystrokes, location, contacts, device identifiers. No analytics, no ads, no tracking, no sale of data.</p>
<p><b>Deletion.</b> Remove the extension or clear its storage to delete keys and settings; delete <code>~/.scrapegraphai</code> to remove snapshots and investigation paths.</p>
<p><b>Contact.</b> Replace with your contact email before publishing this policy.</p>
</div>

<footer>
  AI研判助手 · ScrapeGraph — Privacy Policy. This page is intended to be hosted at a public URL for the Microsoft Edge Add-ons store listing.
</footer>

</body>
</html>
