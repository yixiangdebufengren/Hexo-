🎵 Hexo Music Ball (悬浮音乐球)
一款专为 Hexo 博客打造的高颜值、极简、智能悬浮音乐播放器。采用现代 Glassmorphism（毛玻璃）设计语言，纯 Vanilla JS + CSS 编写，轻量极致。
✨ 核心特性
 * 🔮 超感毛玻璃 UI：通透的悬浮球与控制面板，内置呼吸音符与旋转动效，完美融入各种博客主题。
 * 👆 自由拖拽 & 智能吸边：支持全屏无缝拖拽。靠近屏幕边缘松手，1.5秒后会自动半隐藏收起，绝不遮挡文字视线。
 * 🎤 实时歌词同步引擎：原生集成轻量 LRC 歌词解析引擎。面板标题栏会自动随音乐进度丝滑滚动显示当前歌词。
 * 🤖 自动化音乐生成器：配套 Hexo 插件，自动读取指定目录的音乐文件生成接口数据。
 * 🏷 内嵌歌词自动提取：借助 node-id3，自动从你的 MP3 文件中提取内嵌歌词，告别手动写配置。
 * 🗂 智能排序系统：默认按首字母/拼音自动排序。支持通过文件名前缀（如 01-晴天.mp3）进行自定义置顶，前端展示时自动隐藏序号。
 * 📱 多端自适应：精心调优的触控事件（Pointer Events），在手机端和电脑端均拥有指尖跟手零延迟的极致体验。
📦 安装指南
1. 安装核心依赖
由于插件需要自动解析 MP3 的内嵌歌词，请在你的 Hexo 博客根目录执行以下命令：
npm install node-id3

2. 放置代码文件
将本项目中的文件放置到你的 Hexo 博客目录中：
 * Hexo 插件：将 music-generator.js 放到博客根目录的 scripts/ 文件夹下（如果没有 scripts 文件夹则新建一个）。
 * 前端资源：将 music-ball.js 和 music-ball.css 放到你所使用主题的 source/js/ 和 source/css/ 目录下（或者主题指定的静态资源目录）。
3. 创建音乐目录
在 Hexo 根目录的 source/ 文件夹下，新建路径 source/music/gequ/。
🚀 使用方法
1. 添加音乐
将你的音频文件（.mp3, .flac, .ogg, .wav）直接丢进 source/music/gequ/ 目录中即可。
 * 💡 关于歌词：推荐使用 Mp3tag 或音乐播放器将歌词写入 MP3 文件的内嵌标签中，生成器会自动提取。
 * 💡 关于排序：插件默认按 A-Z 拼音排序。如果想置顶某首歌，只需重命名文件，例如：01-稻香.mp3、02-夜曲.mp3（页面中会自动隐藏 01- 等序号）。
2. 在主题中引入
打开你 Hexo 主题的全局布局文件（通常是 layout/_layout.ejs 或 layout/layout.pug 等），在 <head> 引入 CSS，在 </body> 前引入 JS：
<!-- 在 head 中引入 -->
<link rel="stylesheet" href="/css/music-ball.css">

<!-- 在 body 底部引入 -->
<script src="/js/music-ball.js"></script>

3. 编译运行
在终端中执行清理并重新生成博客：
hexo clean && hexo g && hexo s

打开本地预览地址，你就能在右下角看到这颗灵动的音乐球了！
🕹 交互指南
 * 单击：处于半隐藏状态时，点击唤醒；处于完全显示状态时，点击打开/关闭控制面板。
 * 双击：快速播放 / 暂停当前音乐。
 * 拖拽：按住悬浮球可全屏自由拖动。
 * 控制面板：提供上一曲、播放/暂停、下一曲功能，支持点击进度条跳转。
🛠 技术栈
 * 前端：HTML5, CSS3 (Glassmorphism), Vanilla JavaScript (ES6+)
 * 构建：Node.js, Hexo API
 * 依赖：node-id3 (用于解析音频元数据)
📄 License
MIT License. 欢迎随时 Fork 和 PR！如果你喜欢这个小插件，别忘了点个 ⭐️ Star！
