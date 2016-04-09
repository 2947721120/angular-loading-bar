
###CN
<article class="markdown-body entry-content" itemprop="text"><h1><a id="user-content-angular-loading-bar" class="anchor" href="#angular-loading-bar" aria-hidden="true"><svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path d="M4 9h1v1h-1c-1.5 0-3-1.69-3-3.5s1.55-3.5 3-3.5h4c1.45 0 3 1.69 3 3.5 0 1.41-0.91 2.72-2 3.25v-1.16c0.58-0.45 1-1.27 1-2.09 0-1.28-1.02-2.5-2-2.5H4c-0.98 0-2 1.22-2 2.5s1 2.5 2 2.5z m9-3h-1v1h1c1 0 2 1.22 2 2.5s-1.02 2.5-2 2.5H9c-0.98 0-2-1.22-2-2.5 0-0.83 0.42-1.64 1-2.09v-1.16c-1.09 0.53-2 1.84-2 3.25 0 1.81 1.55 3.5 3 3.5h4c1.45 0 3-1.69 3-3.5s-1.5-3.5-3-3.5z"></path></svg></a><trans data-src="angular-loading-bar" data-dst="角加载杆">角加载杆</trans></h1>

<p><trans data-src="The idea is simple: Add a loading bar / progress bar whenever an XHR request goes out in angular.  Multiple requests within the same time period get bundled together such that each response increments the progress bar by the appropriate amount." data-dst="想法很简单：添加一个加载杆/进度条当XHR请求出角。多个请求在同一时期被捆绑在一起，每个响应增加进度栏的适量。">想法很简单：添加一个加载杆/进度条当XHR请求出角。多个请求在同一时期被捆绑在一起，每个响应增加进度栏的适量。</trans></p>

<p><trans data-src="This is mostly cool because you simply include it in your app, and it works.  There's no complicated setup, and no need to maintain the state of the loading bar; it's all handled automatically by the interceptor." data-dst="这是很酷的因为你简单地将它包括在你的应用程序，和它的作品。没有复杂的设置，而无需维护加载杆的状态这都是自动处理的拦截器。">这是很酷的因为你简单地将它包括在你的应用程序，和它的作品。没有复杂的设置，而无需维护加载杆的状态这都是自动处理的拦截器。</trans></p>

<p><strong><trans data-src="Requirements:" data-dst="要求">要求</trans></strong><trans data-src=" AngularJS 1.2+" data-dst="angularjs 1.2">angularjs 1.2</trans></p>

<p><strong><trans data-src="File Size:" data-dst="文件大小：">文件大小：</trans></strong><trans data-src=" 2.4Kb minified, 0.5Kb gzipped" data-dst="外显缩小，长度的压缩包">外显缩小，长度的压缩包</trans></p>

<h2><a id="user-content-usage" class="anchor" href="#usage" aria-hidden="true"><svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path d="M4 9h1v1h-1c-1.5 0-3-1.69-3-3.5s1.55-3.5 3-3.5h4c1.45 0 3 1.69 3 3.5 0 1.41-0.91 2.72-2 3.25v-1.16c0.58-0.45 1-1.27 1-2.09 0-1.28-1.02-2.5-2-2.5H4c-0.98 0-2 1.22-2 2.5s1 2.5 2 2.5z m9-3h-1v1h1c1 0 2 1.22 2 2.5s-1.02 2.5-2 2.5H9c-0.98 0-2-1.22-2-2.5 0-0.83 0.42-1.64 1-2.09v-1.16c-1.09 0.53-2 1.84-2 3.25 0 1.81 1.55 3.5 3 3.5h4c1.45 0 3-1.69 3-3.5s-1.5-3.5-3-3.5z"></path></svg></a><trans data-src="Usage:" data-dst="使用：">使用：</trans></h2>

<ol>
<li><p><trans data-src="include the loading bar as a dependency for your app.  If you want animations, include " data-dst="包括加载酒吧为您的应用程序依赖。如果你想要动画，包括">包括加载酒吧为您的应用程序依赖。如果你想要动画，包括</trans><code><trans data-src="ngAnimate" data-dst="nganimate">nganimate</trans></code><trans data-src=" as well. " data-dst="以及。">以及。</trans><em><trans data-src="note: ngAnimate is optional" data-dst="注：nganimate是可选的">注：nganimate是可选的</trans></em></p>

<div class="highlight highlight-source-js"><pre><span class="pl-smi"><trans data-src="angular" data-dst="角">角</trans></span><trans data-src="." data-dst="。">。</trans><span class="pl-en"><trans data-src="module" data-dst="模块">模块</trans></span><trans data-src="(" data-dst="（">（</trans><span class="pl-s"><span class="pl-pds"><trans data-src="'" data-dst="'"><trans data-src="'" data-dst="'">'</trans></trans></span><trans data-src="myApp" data-dst="MyApp">MyApp</trans><span class="pl-pds"><trans data-src="'" data-dst="'"><trans data-src="'" data-dst="'">'</trans></trans></span></span><trans data-src=", [" data-dst="，[">，[</trans><span class="pl-s"><span class="pl-pds"><trans data-src="'" data-dst="'"><trans data-src="'" data-dst="'">'</trans></trans></span><trans data-src="angular-loading-bar" data-dst="角加载杆">角加载杆</trans><span class="pl-pds"><trans data-src="'" data-dst="'"><trans data-src="'" data-dst="'">'</trans></trans></span></span><trans data-src=", " data-dst="，">，</trans><span class="pl-s"><span class="pl-pds"><trans data-src="'" data-dst="'"><trans data-src="'" data-dst="'">'</trans></trans></span><trans data-src="ngAnimate" data-dst="nganimate">nganimate</trans><span class="pl-pds"><trans data-src="'" data-dst="'"><trans data-src="'" data-dst="'">'</trans></trans></span></span><trans data-src="])" data-dst="]）">]）</trans></pre></div></li>
<li><p><trans data-src="include the supplied JS and CSS file (or create your own CSS to override defaults)." data-dst="包括提供的JS和CSS文件（或创建自己的CSS来覆盖默认值）。">包括提供的JS和CSS文件（或创建自己的CSS来覆盖默认值）。</trans></p>

<div class="highlight highlight-text-html-basic"><pre>&lt;<span class="pl-ent"><trans data-src="link" data-dst="链接">链接</trans></span> <span class="pl-e"><trans data-src="rel" data-dst="REL">REL</trans></span>=<span class="pl-s"><span class="pl-pds"><trans data-src="'" data-dst="'"><trans data-src="'" data-dst="'">'</trans></trans></span><trans data-src="stylesheet" data-dst="样式表">样式表</trans><span class="pl-pds"><trans data-src="'" data-dst="'"><trans data-src="'" data-dst="'">'</trans></trans></span></span> <span class="pl-e"><trans data-src="href" data-dst="href"><trans data-src="href" data-dst="href">href</trans></trans></span>=<span class="pl-s"><span class="pl-pds"><trans data-src="'" data-dst="'"><trans data-src="'" data-dst="'">'</trans></trans></span><trans data-src="build/loading-bar.min.css" data-dst="建立/ loading-bar.min.css">建立/ loading-bar.min.css</trans><span class="pl-pds"><trans data-src="'" data-dst="'"><trans data-src="'" data-dst="'">'</trans></trans></span></span> <span class="pl-e"><trans data-src="type" data-dst="类型">类型</trans></span>=<span class="pl-s"><span class="pl-pds"><trans data-src="'" data-dst="'"><trans data-src="'" data-dst="'">'</trans></trans></span><trans data-src="text/css" data-dst="文本/ CSS">文本/ CSS</trans><span class="pl-pds"><trans data-src="'" data-dst="'"><trans data-src="'" data-dst="'">'</trans></trans></span></span> <span class="pl-e"><trans data-src="media" data-dst="媒体">媒体</trans></span>=<span class="pl-s"><span class="pl-pds"><trans data-src="'" data-dst="'"><trans data-src="'" data-dst="'">'</trans></trans></span><trans data-src="all" data-dst="全部">全部</trans><span class="pl-pds"><trans data-src="'" data-dst="'"><trans data-src="'" data-dst="'">'</trans></trans></span></span> /&gt;
&lt;<span class="pl-ent"><trans data-src="script" data-dst="脚本">脚本</trans></span> <span class="pl-e"><trans data-src="type" data-dst="类型">类型</trans></span>=<span class="pl-s"><span class="pl-pds"><trans data-src="'" data-dst="'"><trans data-src="'" data-dst="'">'</trans></trans></span><trans data-src="text/javascript" data-dst="文字/ JavaScript">文字/ JavaScript</trans><span class="pl-pds"><trans data-src="'" data-dst="'"><trans data-src="'" data-dst="'">'</trans></trans></span></span> <span class="pl-e"><trans data-src="src" data-dst="SRC">SRC</trans></span>=<span class="pl-s"><span class="pl-pds"><trans data-src="'" data-dst="'"><trans data-src="'" data-dst="'">'</trans></trans></span><trans data-src="build/loading-bar.min.js" data-dst="建立/ loading-bar.min.js">建立/ loading-bar.min.js</trans><span class="pl-pds"><trans data-src="'" data-dst="'"><trans data-src="'" data-dst="'">'</trans></trans></span></span>&gt;&lt;/<span class="pl-ent"><trans data-src="script" data-dst="脚本">脚本</trans></span>&gt;</pre></div></li>
<li><p><trans data-src="That's it -- you're done!" data-dst="这是你做的！">这是你做的！</trans></p></li>
</ol>

<h4><a id="user-content-via-bower" class="anchor" href="#via-bower" aria-hidden="true"><svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path d="M4 9h1v1h-1c-1.5 0-3-1.69-3-3.5s1.55-3.5 3-3.5h4c1.45 0 3 1.69 3 3.5 0 1.41-0.91 2.72-2 3.25v-1.16c0.58-0.45 1-1.27 1-2.09 0-1.28-1.02-2.5-2-2.5H4c-0.98 0-2 1.22-2 2.5s1 2.5 2 2.5z m9-3h-1v1h1c1 0 2 1.22 2 2.5s-1.02 2.5-2 2.5H9c-0.98 0-2-1.22-2-2.5 0-0.83 0.42-1.64 1-2.09v-1.16c-1.09 0.53-2 1.84-2 3.25 0 1.81 1.55 3.5 3 3.5h4c1.45 0 3-1.69 3-3.5s-1.5-3.5-3-3.5z"></path></svg></a><trans data-src="via bower:" data-dst="杰克：轨道">杰克：轨道</trans></h4>

<pre><code><trans data-src="$ bower install angular-loading-bar
" data-dst="鲍尔安装角加载杆元">鲍尔安装角加载杆元</trans></code></pre>

<h4><a id="user-content-via-npm" class="anchor" href="#via-npm" aria-hidden="true"><svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path d="M4 9h1v1h-1c-1.5 0-3-1.69-3-3.5s1.55-3.5 3-3.5h4c1.45 0 3 1.69 3 3.5 0 1.41-0.91 2.72-2 3.25v-1.16c0.58-0.45 1-1.27 1-2.09 0-1.28-1.02-2.5-2-2.5H4c-0.98 0-2 1.22-2 2.5s1 2.5 2 2.5z m9-3h-1v1h1c1 0 2 1.22 2 2.5s-1.02 2.5-2 2.5H9c-0.98 0-2-1.22-2-2.5 0-0.83 0.42-1.64 1-2.09v-1.16c-1.09 0.53-2 1.84-2 3.25 0 1.81 1.55 3.5 3 3.5h4c1.45 0 3-1.69 3-3.5s-1.5-3.5-3-3.5z"></path></svg></a><trans data-src="via npm:" data-dst="新公共管理的路径：">新公共管理的路径：</trans></h4>

<pre><code><trans data-src="$ npm install angular-loading-bar
" data-dst="NPM安装角加载杆元">NPM安装角加载杆元</trans></code></pre>

<h4><a id="user-content-via-cdn" class="anchor" href="#via-cdn" aria-hidden="true"><svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path d="M4 9h1v1h-1c-1.5 0-3-1.69-3-3.5s1.55-3.5 3-3.5h4c1.45 0 3 1.69 3 3.5 0 1.41-0.91 2.72-2 3.25v-1.16c0.58-0.45 1-1.27 1-2.09 0-1.28-1.02-2.5-2-2.5H4c-0.98 0-2 1.22-2 2.5s1 2.5 2 2.5z m9-3h-1v1h1c1 0 2 1.22 2 2.5s-1.02 2.5-2 2.5H9c-0.98 0-2-1.22-2-2.5 0-0.83 0.42-1.64 1-2.09v-1.16c-1.09 0.53-2 1.84-2 3.25 0 1.81 1.55 3.5 3 3.5h4c1.45 0 3-1.69 3-3.5s-1.5-3.5-3-3.5z"></path></svg></a><trans data-src="via CDN:" data-dst="通过CDN：">通过CDN：</trans></h4>

<div class="highlight highlight-text-html-basic"><pre> &lt;<span class="pl-ent"><trans data-src="link" data-dst="链接">链接</trans></span> <span class="pl-e"><trans data-src="rel" data-dst="REL">REL</trans></span>=<span class="pl-s"><span class="pl-pds"><trans data-src="'" data-dst="'"><trans data-src="'" data-dst="'">'</trans></trans></span><trans data-src="stylesheet" data-dst="样式表">样式表</trans><span class="pl-pds"><trans data-src="'" data-dst="'"><trans data-src="'" data-dst="'">'</trans></trans></span></span> <span class="pl-e"><trans data-src="href" data-dst="href"><trans data-src="href" data-dst="href">href</trans></trans></span>=<span class="pl-s"><span class="pl-pds"><trans data-src="'" data-dst="'"><trans data-src="'" data-dst="'">'</trans></trans></span><trans data-src="//cdnjs.cloudflare.com/ajax/libs/angular-loading-bar/0.9.0/loading-bar.min.css" data-dst="/ / / / /的Ajax库cdnjs.cloudflare.com角加载/酒吧/ loading-bar.min.css 0.9.0">/ / / / /的Ajax库cdnjs.cloudflare.com角加载/酒吧/ loading-bar.min.css 0.9.0</trans><span class="pl-pds"><trans data-src="'" data-dst="'"><trans data-src="'" data-dst="'">'</trans></trans></span></span> <span class="pl-e"><trans data-src="type" data-dst="类型">类型</trans></span>=<span class="pl-s"><span class="pl-pds"><trans data-src="'" data-dst="'"><trans data-src="'" data-dst="'">'</trans></trans></span><trans data-src="text/css" data-dst="文本/ CSS">文本/ CSS</trans><span class="pl-pds"><trans data-src="'" data-dst="'"><trans data-src="'" data-dst="'">'</trans></trans></span></span> <span class="pl-e"><trans data-src="media" data-dst="媒体">媒体</trans></span>=<span class="pl-s"><span class="pl-pds"><trans data-src="'" data-dst="'"><trans data-src="'" data-dst="'">'</trans></trans></span><trans data-src="all" data-dst="全部">全部</trans><span class="pl-pds"><trans data-src="'" data-dst="'"><trans data-src="'" data-dst="'">'</trans></trans></span></span> /&gt;
<span class="pl-s1"> &lt;<span class="pl-ent"><trans data-src="script" data-dst="脚本">脚本</trans></span> <span class="pl-e"><trans data-src="type" data-dst="类型">类型</trans></span>=<span class="pl-s"><span class="pl-pds"><trans data-src="'" data-dst="'"><trans data-src="'" data-dst="'">'</trans></trans></span><trans data-src="text/javascript" data-dst="文字/ JavaScript">文字/ JavaScript</trans><span class="pl-pds"><trans data-src="'" data-dst="'"><trans data-src="'" data-dst="'">'</trans></trans></span></span> <span class="pl-e"><trans data-src="src" data-dst="SRC">SRC</trans></span>=<span class="pl-s"><span class="pl-pds"><trans data-src="'" data-dst="'"><trans data-src="'" data-dst="'">'</trans></trans></span><trans data-src="//cdnjs.cloudflare.com/ajax/libs/angular-loading-bar/0.9.0/loading-bar.min.js" data-dst="/ / / / /的Ajax库cdnjs.cloudflare.com角加载/酒吧/ loading-bar.min.js 0.9.0">/ / / / /的Ajax库cdnjs.cloudflare.com角加载/酒吧/ loading-bar.min.js 0.9.0</trans><span class="pl-pds"><trans data-src="'" data-dst="'"><trans data-src="'" data-dst="'">'</trans></trans></span></span>&gt;&lt;/<span class="pl-ent"><trans data-src="script" data-dst="脚本">脚本</trans></span>&gt;</span></pre></div>

<h2><a id="user-content-why-i-created-this" class="anchor" href="#why-i-created-this" aria-hidden="true"><svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path d="M4 9h1v1h-1c-1.5 0-3-1.69-3-3.5s1.55-3.5 3-3.5h4c1.45 0 3 1.69 3 3.5 0 1.41-0.91 2.72-2 3.25v-1.16c0.58-0.45 1-1.27 1-2.09 0-1.28-1.02-2.5-2-2.5H4c-0.98 0-2 1.22-2 2.5s1 2.5 2 2.5z m9-3h-1v1h1c1 0 2 1.22 2 2.5s-1.02 2.5-2 2.5H9c-0.98 0-2-1.22-2-2.5 0-0.83 0.42-1.64 1-2.09v-1.16c-1.09 0.53-2 1.84-2 3.25 0 1.81 1.55 3.5 3 3.5h4c1.45 0 3-1.69 3-3.5s-1.5-3.5-3-3.5z"></path></svg></a><trans data-src="Why I created this" data-dst="为什么我创造了这个">为什么我创造了这个</trans></h2>

<p><trans data-src="There are a couple projects similar to this out there, but none were ideal for me.  All implementations I've seen require that you maintain state on behalf of the loading bar.  In other words, you're setting the value of the loading/progress bar manually from potentially many different locations.  This becomes complicated when you have a very large application with several services all making independent XHR requests. It becomes even more complicated if you want these services to be loosly coupled." data-dst="有一对夫妇的项目与此类似的有，但没有理想的我。我看到所有的实现需要你保持对加载杆的状态。换句话说，你设置的值加载/进度条手动从潜在的许多不同的位置。这变得复杂，当你有几个服务，使独立的XHR请求一个非常大的应用。如果你想成为这些服务是松散耦合的更复杂。">有一对夫妇的项目与此类似的有，但没有理想的我。我看到所有的实现需要你保持对加载杆的状态。换句话说，你设置的值加载/进度条手动从潜在的许多不同的位置。这变得复杂，当你有几个服务，使独立的XHR请求一个非常大的应用。如果你想成为这些服务是松散耦合的更复杂。</trans></p>

<p><trans data-src="Additionally, Angular was created as a highly testable framework, so it pains me to see Angular modules without tests.  That is not the case here as this loading bar ships with 100% code coverage." data-dst="此外，角创建一个高度可测试的框架，所以我没有看到角模块测试。事实并非如此，在这100%条船装载的代码覆盖率。">此外，角创建一个高度可测试的框架，所以我没有看到角模块测试。事实并非如此，在这100%条船装载的代码覆盖率。</trans></p>

<p><strong><trans data-src="Goals for this project:" data-dst="这个项目的目标：">这个项目的目标：</trans></strong></p>

<ol>
<li><trans data-src="Make it automatic" data-dst="让它自动">让它自动</trans></li>
<li><trans data-src="Unit tests, 100% coverage" data-dst="单元测试覆盖率100%">单元测试覆盖率100%</trans></li>
<li><trans data-src="Must work well with ngAnimate" data-dst="必须nganimate工作">必须nganimate工作</trans></li>
<li><trans data-src="Must be styled via external CSS (not inline)" data-dst="必须通过外部CSS样式（不一致）">必须通过外部CSS样式（不一致）</trans></li>
<li><trans data-src="No jQuery dependencies" data-dst="没有jQuery的依赖">没有jQuery的依赖</trans></li>
</ol>

<h2><a id="user-content-configuration" class="anchor" href="#configuration" aria-hidden="true"><svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path d="M4 9h1v1h-1c-1.5 0-3-1.69-3-3.5s1.55-3.5 3-3.5h4c1.45 0 3 1.69 3 3.5 0 1.41-0.91 2.72-2 3.25v-1.16c0.58-0.45 1-1.27 1-2.09 0-1.28-1.02-2.5-2-2.5H4c-0.98 0-2 1.22-2 2.5s1 2.5 2 2.5z m9-3h-1v1h1c1 0 2 1.22 2 2.5s-1.02 2.5-2 2.5H9c-0.98 0-2-1.22-2-2.5 0-0.83 0.42-1.64 1-2.09v-1.16c-1.09 0.53-2 1.84-2 3.25 0 1.81 1.55 3.5 3 3.5h4c1.45 0 3-1.69 3-3.5s-1.5-3.5-3-3.5z"></path></svg></a><trans data-src="Configuration" data-dst="配置">配置</trans></h2>

<h4><a id="user-content-turn-the-spinner-on-or-off" class="anchor" href="#turn-the-spinner-on-or-off" aria-hidden="true"><svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path d="M4 9h1v1h-1c-1.5 0-3-1.69-3-3.5s1.55-3.5 3-3.5h4c1.45 0 3 1.69 3 3.5 0 1.41-0.91 2.72-2 3.25v-1.16c0.58-0.45 1-1.27 1-2.09 0-1.28-1.02-2.5-2-2.5H4c-0.98 0-2 1.22-2 2.5s1 2.5 2 2.5z m9-3h-1v1h1c1 0 2 1.22 2 2.5s-1.02 2.5-2 2.5H9c-0.98 0-2-1.22-2-2.5 0-0.83 0.42-1.64 1-2.09v-1.16c-1.09 0.53-2 1.84-2 3.25 0 1.81 1.55 3.5 3 3.5h4c1.45 0 3-1.69 3-3.5s-1.5-3.5-3-3.5z"></path></svg></a><trans data-src="Turn the spinner on or off:" data-dst="转动旋转打开或关闭：">转动旋转打开或关闭：</trans></h4>

<p><trans data-src="The insertion of the spinner can be controlled through configuration.  It's on by default, but if you'd like to turn it off, simply configure the service:" data-dst="旋转器的插入可以通过配置。这是默认的，但如果你想关闭它，只需配置服务：">旋转器的插入可以通过配置。这是默认的，但如果你想关闭它，只需配置服务：</trans></p>

<div class="highlight highlight-source-js"><pre><span class="pl-smi"><trans data-src="angular" data-dst="角">角</trans></span><trans data-src="." data-dst="。">。</trans><span class="pl-en"><trans data-src="module" data-dst="模块">模块</trans></span><trans data-src="(" data-dst="（">（</trans><span class="pl-s"><span class="pl-pds"><trans data-src="'" data-dst="'"><trans data-src="'" data-dst="'">'</trans></trans></span><trans data-src="myApp" data-dst="MyApp">MyApp</trans><span class="pl-pds"><trans data-src="'" data-dst="'"><trans data-src="'" data-dst="'">'</trans></trans></span></span><trans data-src=", [" data-dst="，[">，[</trans><span class="pl-s"><span class="pl-pds"><trans data-src="'" data-dst="'"><trans data-src="'" data-dst="'">'</trans></trans></span><trans data-src="angular-loading-bar" data-dst="角加载杆">角加载杆</trans><span class="pl-pds"><trans data-src="'" data-dst="'"><trans data-src="'" data-dst="'">'</trans></trans></span></span><trans data-src="])
  ." data-dst="]）。">]）。</trans><span class="pl-en"><trans data-src="config" data-dst="配置">配置</trans></span><trans data-src="([" data-dst="（[">（[</trans><span class="pl-s"><span class="pl-pds"><trans data-src="'" data-dst="'"><trans data-src="'" data-dst="'">'</trans></trans></span><trans data-src="cfpLoadingBarProvider" data-dst="cfploadingbarprovider">cfploadingbarprovider</trans><span class="pl-pds"><trans data-src="'" data-dst="'"><trans data-src="'" data-dst="'">'</trans></trans></span></span><trans data-src=", " data-dst="，">，</trans><span class="pl-k"><trans data-src="function" data-dst="功能">功能</trans></span><trans data-src="(" data-dst="（">（</trans><span class="pl-smi"><trans data-src="cfpLoadingBarProvider" data-dst="cfploadingbarprovider">cfploadingbarprovider</trans></span><trans data-src=") {
    " data-dst="）{">）{</trans><span class="pl-smi"><trans data-src="cfpLoadingBarProvider" data-dst="cfploadingbarprovider">cfploadingbarprovider</trans></span><trans data-src="." data-dst="。">。</trans><span class="pl-smi"><trans data-src="includeSpinner" data-dst="includespinner">includespinner</trans></span> <span class="pl-k">=</span> <span class="pl-c1"><trans data-src="false" data-dst="假">假</trans></span><trans data-src=";
  }])" data-dst="
 } ]）；">
 } ]）；</trans></pre></div>

<h4><a id="user-content-turn-the-loading-bar-on-or-off" class="anchor" href="#turn-the-loading-bar-on-or-off" aria-hidden="true"><svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path d="M4 9h1v1h-1c-1.5 0-3-1.69-3-3.5s1.55-3.5 3-3.5h4c1.45 0 3 1.69 3 3.5 0 1.41-0.91 2.72-2 3.25v-1.16c0.58-0.45 1-1.27 1-2.09 0-1.28-1.02-2.5-2-2.5H4c-0.98 0-2 1.22-2 2.5s1 2.5 2 2.5z m9-3h-1v1h1c1 0 2 1.22 2 2.5s-1.02 2.5-2 2.5H9c-0.98 0-2-1.22-2-2.5 0-0.83 0.42-1.64 1-2.09v-1.16c-1.09 0.53-2 1.84-2 3.25 0 1.81 1.55 3.5 3 3.5h4c1.45 0 3-1.69 3-3.5s-1.5-3.5-3-3.5z"></path></svg></a><trans data-src="Turn the loading bar on or off:" data-dst="打开或关闭加载杆：">打开或关闭加载杆：</trans></h4>

<p><trans data-src="Like the spinner configuration above, the loading bar can also be turned off for cases where you only want the spinner:" data-dst="像上面的旋转配置，加载杆也可以关闭的情况下，你只需要微调：">像上面的旋转配置，加载杆也可以关闭的情况下，你只需要微调：</trans></p>

<div class="highlight highlight-source-js"><pre><span class="pl-smi"><trans data-src="angular" data-dst="角">角</trans></span><trans data-src="." data-dst="。">。</trans><span class="pl-en"><trans data-src="module" data-dst="模块">模块</trans></span><trans data-src="(" data-dst="（">（</trans><span class="pl-s"><span class="pl-pds"><trans data-src="'" data-dst="'"><trans data-src="'" data-dst="'">'</trans></trans></span><trans data-src="myApp" data-dst="MyApp">MyApp</trans><span class="pl-pds"><trans data-src="'" data-dst="'"><trans data-src="'" data-dst="'">'</trans></trans></span></span><trans data-src=", [" data-dst="，[">，[</trans><span class="pl-s"><span class="pl-pds"><trans data-src="'" data-dst="'"><trans data-src="'" data-dst="'">'</trans></trans></span><trans data-src="angular-loading-bar" data-dst="角加载杆">角加载杆</trans><span class="pl-pds"><trans data-src="'" data-dst="'"><trans data-src="'" data-dst="'">'</trans></trans></span></span><trans data-src="])
  ." data-dst="]）。">]）。</trans><span class="pl-en"><trans data-src="config" data-dst="配置">配置</trans></span><trans data-src="([" data-dst="（[">（[</trans><span class="pl-s"><span class="pl-pds"><trans data-src="'" data-dst="'"><trans data-src="'" data-dst="'">'</trans></trans></span><trans data-src="cfpLoadingBarProvider" data-dst="cfploadingbarprovider">cfploadingbarprovider</trans><span class="pl-pds"><trans data-src="'" data-dst="'"><trans data-src="'" data-dst="'">'</trans></trans></span></span><trans data-src=", " data-dst="，">，</trans><span class="pl-k"><trans data-src="function" data-dst="功能">功能</trans></span><trans data-src="(" data-dst="（">（</trans><span class="pl-smi"><trans data-src="cfpLoadingBarProvider" data-dst="cfploadingbarprovider">cfploadingbarprovider</trans></span><trans data-src=") {
    " data-dst="）{">）{</trans><span class="pl-smi"><trans data-src="cfpLoadingBarProvider" data-dst="cfploadingbarprovider">cfploadingbarprovider</trans></span><trans data-src="." data-dst="。">。</trans><span class="pl-smi"><trans data-src="includeBar" data-dst="includebar">includebar</trans></span> <span class="pl-k">=</span> <span class="pl-c1"><trans data-src="false" data-dst="假">假</trans></span><trans data-src=";
  }])" data-dst="
 } ]）；">
 } ]）；</trans></pre></div>

<h4><a id="user-content-customize-the-template" class="anchor" href="#customize-the-template" aria-hidden="true"><svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path d="M4 9h1v1h-1c-1.5 0-3-1.69-3-3.5s1.55-3.5 3-3.5h4c1.45 0 3 1.69 3 3.5 0 1.41-0.91 2.72-2 3.25v-1.16c0.58-0.45 1-1.27 1-2.09 0-1.28-1.02-2.5-2-2.5H4c-0.98 0-2 1.22-2 2.5s1 2.5 2 2.5z m9-3h-1v1h1c1 0 2 1.22 2 2.5s-1.02 2.5-2 2.5H9c-0.98 0-2-1.22-2-2.5 0-0.83 0.42-1.64 1-2.09v-1.16c-1.09 0.53-2 1.84-2 3.25 0 1.81 1.55 3.5 3 3.5h4c1.45 0 3-1.69 3-3.5s-1.5-3.5-3-3.5z"></path></svg></a><trans data-src="Customize the template:" data-dst="自定义模板：">自定义模板：</trans></h4>

<p><trans data-src="If you'd like to replace the default HTML template you can configure it by providing inline HTML as a string:" data-dst="如果你想替换掉默认的HTML模板，你可以配置它通过提供内嵌HTML作为一个字符串：">如果你想替换掉默认的HTML模板，你可以配置它通过提供内嵌HTML作为一个字符串：</trans></p>

<div class="highlight highlight-source-js"><pre><span class="pl-smi"><trans data-src="angular" data-dst="角">角</trans></span><trans data-src="." data-dst="。">。</trans><span class="pl-en"><trans data-src="module" data-dst="模块">模块</trans></span><trans data-src="(" data-dst="（">（</trans><span class="pl-s"><span class="pl-pds"><trans data-src="'" data-dst="'"><trans data-src="'" data-dst="'">'</trans></trans></span><trans data-src="myApp" data-dst="MyApp">MyApp</trans><span class="pl-pds"><trans data-src="'" data-dst="'"><trans data-src="'" data-dst="'">'</trans></trans></span></span><trans data-src=", [" data-dst="，[">，[</trans><span class="pl-s"><span class="pl-pds"><trans data-src="'" data-dst="'"><trans data-src="'" data-dst="'">'</trans></trans></span><trans data-src="angular-loading-bar" data-dst="角加载杆">角加载杆</trans><span class="pl-pds"><trans data-src="'" data-dst="'"><trans data-src="'" data-dst="'">'</trans></trans></span></span><trans data-src="])
  ." data-dst="]）。">]）。</trans><span class="pl-en"><trans data-src="config" data-dst="配置">配置</trans></span><trans data-src="([" data-dst="（[">（[</trans><span class="pl-s"><span class="pl-pds"><trans data-src="'" data-dst="'"><trans data-src="'" data-dst="'">'</trans></trans></span><trans data-src="cfpLoadingBarProvider" data-dst="cfploadingbarprovider">cfploadingbarprovider</trans><span class="pl-pds"><trans data-src="'" data-dst="'"><trans data-src="'" data-dst="'">'</trans></trans></span></span><trans data-src=", " data-dst="，">，</trans><span class="pl-k"><trans data-src="function" data-dst="功能">功能</trans></span><trans data-src="(" data-dst="（">（</trans><span class="pl-smi"><trans data-src="cfpLoadingBarProvider" data-dst="cfploadingbarprovider">cfploadingbarprovider</trans></span><trans data-src=") {
    " data-dst="）{">）{</trans><span class="pl-smi"><trans data-src="cfpLoadingBarProvider" data-dst="cfploadingbarprovider">cfploadingbarprovider</trans></span><trans data-src="." data-dst="。">。</trans><span class="pl-smi"><trans data-src="spinnerTemplate" data-dst="spinnertemplate">spinnertemplate</trans></span> <span class="pl-k">=</span> <span class="pl-s"><span class="pl-pds"><trans data-src="'" data-dst="'"><trans data-src="'" data-dst="'">'</trans></trans></span>&lt;div&gt;&lt;span class="fa fa-spinner"&gt;Loading...&lt;/div&gt;<span class="pl-pds"><trans data-src="'" data-dst="'"><trans data-src="'" data-dst="'">'</trans></trans></span></span><trans data-src=";
  }])" data-dst="
 } ]）；">
 } ]）；</trans></pre></div>

<h4><a id="user-content-position-the-template" class="anchor" href="#position-the-template" aria-hidden="true"><svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path d="M4 9h1v1h-1c-1.5 0-3-1.69-3-3.5s1.55-3.5 3-3.5h4c1.45 0 3 1.69 3 3.5 0 1.41-0.91 2.72-2 3.25v-1.16c0.58-0.45 1-1.27 1-2.09 0-1.28-1.02-2.5-2-2.5H4c-0.98 0-2 1.22-2 2.5s1 2.5 2 2.5z m9-3h-1v1h1c1 0 2 1.22 2 2.5s-1.02 2.5-2 2.5H9c-0.98 0-2-1.22-2-2.5 0-0.83 0.42-1.64 1-2.09v-1.16c-1.09 0.53-2 1.84-2 3.25 0 1.81 1.55 3.5 3 3.5h4c1.45 0 3-1.69 3-3.5s-1.5-3.5-3-3.5z"></path></svg></a><trans data-src="Position the template:" data-dst="模板位置：">模板位置：</trans></h4>

<p><trans data-src="If you'd like to position the loadingBar or spinner, provide a CSS selector to the element you'd like the template injected into. The default is the " data-dst="如果你想loadingbar位置或旋转到你想插入到模板中的元素提供的CSS选择器。默认值是">如果你想loadingbar位置或旋转到你想插入到模板中的元素提供的CSS选择器。默认值是</trans><code><trans data-src="<body>" data-dst="< body >">&lt; body &gt;</trans></code><trans data-src=" element:" data-dst="元素">元素</trans></p>

<div class="highlight highlight-source-js"><pre><span class="pl-smi"><trans data-src="angular" data-dst="角">角</trans></span><trans data-src="." data-dst="。">。</trans><span class="pl-en"><trans data-src="module" data-dst="模块">模块</trans></span><trans data-src="(" data-dst="（">（</trans><span class="pl-s"><span class="pl-pds"><trans data-src="'" data-dst="'"><trans data-src="'" data-dst="'">'</trans></trans></span><trans data-src="myApp" data-dst="MyApp">MyApp</trans><span class="pl-pds"><trans data-src="'" data-dst="'"><trans data-src="'" data-dst="'">'</trans></trans></span></span><trans data-src=", [" data-dst="，[">，[</trans><span class="pl-s"><span class="pl-pds"><trans data-src="'" data-dst="'"><trans data-src="'" data-dst="'">'</trans></trans></span><trans data-src="angular-loading-bar" data-dst="角加载杆">角加载杆</trans><span class="pl-pds"><trans data-src="'" data-dst="'"><trans data-src="'" data-dst="'">'</trans></trans></span></span><trans data-src="])
  ." data-dst="]）。">]）。</trans><span class="pl-en"><trans data-src="config" data-dst="配置">配置</trans></span><trans data-src="([" data-dst="（[">（[</trans><span class="pl-s"><span class="pl-pds"><trans data-src="'" data-dst="'"><trans data-src="'" data-dst="'">'</trans></trans></span><trans data-src="cfpLoadingBarProvider" data-dst="cfploadingbarprovider">cfploadingbarprovider</trans><span class="pl-pds"><trans data-src="'" data-dst="'"><trans data-src="'" data-dst="'">'</trans></trans></span></span><trans data-src=", " data-dst="，">，</trans><span class="pl-k"><trans data-src="function" data-dst="功能">功能</trans></span><trans data-src="(" data-dst="（">（</trans><span class="pl-smi"><trans data-src="cfpLoadingBarProvider" data-dst="cfploadingbarprovider">cfploadingbarprovider</trans></span><trans data-src=") {
    " data-dst="）{">）{</trans><span class="pl-smi"><trans data-src="cfpLoadingBarProvider" data-dst="cfploadingbarprovider">cfploadingbarprovider</trans></span><trans data-src="." data-dst="。">。</trans><span class="pl-smi"><trans data-src="parentSelector" data-dst="parentselector">parentselector</trans></span> <span class="pl-k">=</span> <span class="pl-s"><span class="pl-pds"><trans data-src="'" data-dst="'"><trans data-src="'" data-dst="'">'</trans></trans></span><trans data-src="#loading-bar-container" data-dst="#加载杆的容器">#加载杆的容器</trans><span class="pl-pds"><trans data-src="'" data-dst="'"><trans data-src="'" data-dst="'">'</trans></trans></span></span><trans data-src=";
    " data-dst="；">；</trans><span class="pl-smi"><trans data-src="cfpLoadingBarProvider" data-dst="cfploadingbarprovider">cfploadingbarprovider</trans></span><trans data-src="." data-dst="。">。</trans><span class="pl-smi"><trans data-src="spinnerTemplate" data-dst="spinnertemplate">spinnertemplate</trans></span> <span class="pl-k">=</span> <span class="pl-s"><span class="pl-pds"><trans data-src="'" data-dst="'"><trans data-src="'" data-dst="'">'</trans></trans></span>&lt;div&gt;&lt;span class="fa fa-spinner"&gt;Custom Loading Message...&lt;/div&gt;<span class="pl-pds"><trans data-src="'" data-dst="'"><trans data-src="'" data-dst="'">'</trans></trans></span></span><trans data-src=";
  }])" data-dst="
 } ]）；">
 } ]）；</trans></pre></div>

<div class="highlight highlight-text-html-basic"><pre>&lt;<span class="pl-ent"><trans data-src="div" data-dst="DIV">DIV</trans></span> <span class="pl-e"><trans data-src="id" data-dst="身份证件">身份证件</trans></span>=<span class="pl-s"><span class="pl-pds"><trans data-src="" "="" data-dst="“">“</trans></span><trans data-src="loading-bar-container" data-dst="加载杆的容器">加载杆的容器</trans><span class="pl-pds"><trans data-src="" "="" data-dst="“">“</trans></span></span>&gt;&lt;/<span class="pl-ent"><trans data-src="div" data-dst="DIV">DIV</trans></span>&gt;</pre></div>

<h4><a id="user-content-latency-threshold" class="anchor" href="#latency-threshold" aria-hidden="true"><svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path d="M4 9h1v1h-1c-1.5 0-3-1.69-3-3.5s1.55-3.5 3-3.5h4c1.45 0 3 1.69 3 3.5 0 1.41-0.91 2.72-2 3.25v-1.16c0.58-0.45 1-1.27 1-2.09 0-1.28-1.02-2.5-2-2.5H4c-0.98 0-2 1.22-2 2.5s1 2.5 2 2.5z m9-3h-1v1h1c1 0 2 1.22 2 2.5s-1.02 2.5-2 2.5H9c-0.98 0-2-1.22-2-2.5 0-0.83 0.42-1.64 1-2.09v-1.16c-1.09 0.53-2 1.84-2 3.25 0 1.81 1.55 3.5 3 3.5h4c1.45 0 3-1.69 3-3.5s-1.5-3.5-3-3.5z"></path></svg></a><trans data-src="Latency Threshold" data-dst="延迟阈值">延迟阈值</trans></h4>

<p><trans data-src="By default, the loading bar will only display after it has been waiting for a response for over 100ms.  This helps keep things feeling snappy, and avoids the annoyingness of showing a loading bar every few seconds on really chatty applications.  This threshold is totally configurable:" data-dst="默认情况下，加载酒吧将只显示后就一直在等待响应超过100ms。这有助于保持事物感到爽快，避免呈现加载杆很健谈的应用每几秒annoyingness。这是完全可配置的阈值：">默认情况下，加载酒吧将只显示后就一直在等待响应超过100ms。这有助于保持事物感到爽快，避免呈现加载杆很健谈的应用每几秒annoyingness。这是完全可配置的阈值：</trans></p>

<div class="highlight highlight-source-js"><pre><span class="pl-smi"><trans data-src="angular" data-dst="角">角</trans></span><trans data-src="." data-dst="。">。</trans><span class="pl-en"><trans data-src="module" data-dst="模块">模块</trans></span><trans data-src="(" data-dst="（">（</trans><span class="pl-s"><span class="pl-pds"><trans data-src="'" data-dst="'"><trans data-src="'" data-dst="'">'</trans></trans></span><trans data-src="myApp" data-dst="MyApp">MyApp</trans><span class="pl-pds"><trans data-src="'" data-dst="'"><trans data-src="'" data-dst="'">'</trans></trans></span></span><trans data-src=", [" data-dst="，[">，[</trans><span class="pl-s"><span class="pl-pds"><trans data-src="'" data-dst="'"><trans data-src="'" data-dst="'">'</trans></trans></span><trans data-src="angular-loading-bar" data-dst="角加载杆">角加载杆</trans><span class="pl-pds"><trans data-src="'" data-dst="'"><trans data-src="'" data-dst="'">'</trans></trans></span></span><trans data-src="])
  ." data-dst="]）。">]）。</trans><span class="pl-en"><trans data-src="config" data-dst="配置">配置</trans></span><trans data-src="([" data-dst="（[">（[</trans><span class="pl-s"><span class="pl-pds"><trans data-src="'" data-dst="'"><trans data-src="'" data-dst="'">'</trans></trans></span><trans data-src="cfpLoadingBarProvider" data-dst="cfploadingbarprovider">cfploadingbarprovider</trans><span class="pl-pds"><trans data-src="'" data-dst="'"><trans data-src="'" data-dst="'">'</trans></trans></span></span><trans data-src=", " data-dst="，">，</trans><span class="pl-k"><trans data-src="function" data-dst="功能">功能</trans></span><trans data-src="(" data-dst="（">（</trans><span class="pl-smi"><trans data-src="cfpLoadingBarProvider" data-dst="cfploadingbarprovider">cfploadingbarprovider</trans></span><trans data-src=") {
    " data-dst="）{">）{</trans><span class="pl-smi"><trans data-src="cfpLoadingBarProvider" data-dst="cfploadingbarprovider">cfploadingbarprovider</trans></span><trans data-src="." data-dst="。">。</trans><span class="pl-smi"><trans data-src="latencyThreshold" data-dst="latencythreshold">latencythreshold</trans></span> <span class="pl-k">=</span> <span class="pl-c1"><trans data-src="500" data-dst="五百">五百</trans></span><trans data-src=";
  }])" data-dst="
 } ]）；">
 } ]）；</trans></pre></div>

<h4><a id="user-content-ignoring-particular-xhr-requests" class="anchor" href="#ignoring-particular-xhr-requests" aria-hidden="true"><svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path d="M4 9h1v1h-1c-1.5 0-3-1.69-3-3.5s1.55-3.5 3-3.5h4c1.45 0 3 1.69 3 3.5 0 1.41-0.91 2.72-2 3.25v-1.16c0.58-0.45 1-1.27 1-2.09 0-1.28-1.02-2.5-2-2.5H4c-0.98 0-2 1.22-2 2.5s1 2.5 2 2.5z m9-3h-1v1h1c1 0 2 1.22 2 2.5s-1.02 2.5-2 2.5H9c-0.98 0-2-1.22-2-2.5 0-0.83 0.42-1.64 1-2.09v-1.16c-1.09 0.53-2 1.84-2 3.25 0 1.81 1.55 3.5 3 3.5h4c1.45 0 3-1.69 3-3.5s-1.5-3.5-3-3.5z"></path></svg></a><trans data-src="Ignoring particular XHR requests:" data-dst="忽略特定的XHR请求：">忽略特定的XHR请求：</trans></h4>

<p><trans data-src="The loading bar can also be forced to ignore certain requests, for example, when long-polling or periodically sending debugging information back to the server." data-dst="加载杆也可以例如忽略某些请求，强制，当长轮询或定期发送调试信息到服务器。">加载杆也可以例如忽略某些请求，强制，当长轮询或定期发送调试信息到服务器。</trans></p>

<div class="highlight highlight-source-js"><pre><span class="pl-c"><trans data-src="// ignore a particular $http GET:" data-dst="特别是美元/忽略HTTP GET。">特别是美元/忽略HTTP GET。</trans></span>
<span class="pl-smi"><trans data-src="$http" data-dst="$ http">$ http</trans></span><trans data-src="." data-dst="。">。</trans><span class="pl-en"><trans data-src="get" data-dst="得到">得到</trans></span><trans data-src="(" data-dst="（">（</trans><span class="pl-s"><span class="pl-pds"><trans data-src="'" data-dst="'"><trans data-src="'" data-dst="'">'</trans></trans></span><trans data-src="/status" data-dst="/状态">/状态</trans><span class="pl-pds"><trans data-src="'" data-dst="'"><trans data-src="'" data-dst="'">'</trans></trans></span></span><trans data-src=", {
  ignoreLoadingBar" data-dst="
，ignoreloadingbar {">
，ignoreloadingbar {</trans><span class="pl-k"><trans data-src=":" data-dst="：">：</trans></span> <span class="pl-c1"><trans data-src="true" data-dst="真正的">真正的</trans></span><trans data-src="
});

" data-dst="}）；">}）；</trans><span class="pl-c"><trans data-src="// ignore a particular $http POST.  Note: POST and GET have different" data-dst="/ /忽略特定HTTP POST美元。注：后得到具有不同">/ /忽略特定HTTP POST美元。注：后得到具有不同</trans></span>
<span class="pl-c"><trans data-src="// method signatures:" data-dst="/ /方法签名：">/ /方法签名：</trans></span>
<span class="pl-smi"><trans data-src="$http" data-dst="$ http">$ http</trans></span><trans data-src="." data-dst="。">。</trans><span class="pl-en"><trans data-src="post" data-dst="帖子">帖子</trans></span><trans data-src="(" data-dst="（">（</trans><span class="pl-s"><span class="pl-pds"><trans data-src="'" data-dst="'"><trans data-src="'" data-dst="'">'</trans></trans></span><trans data-src="/save" data-dst="保存">保存</trans><span class="pl-pds"><trans data-src="'" data-dst="'"><trans data-src="'" data-dst="'">'</trans></trans></span></span><trans data-src=", data, {
  ignoreLoadingBar" data-dst="，数据，{ 
 ignoreloadingbar">，数据，{ 
 ignoreloadingbar</trans><span class="pl-k"><trans data-src=":" data-dst="：">：</trans></span> <span class="pl-c1"><trans data-src="true" data-dst="真正的">真正的</trans></span><trans data-src="
});
" data-dst="}）；">}）；</trans></pre></div>

<div class="highlight highlight-source-js"><pre><span class="pl-c"><trans data-src="// ignore particular $resource requests:" data-dst="特别是美元/忽视资源请求：">特别是美元/忽视资源请求：</trans></span><trans data-src="
." data-dst="。">。</trans><span class="pl-en"><trans data-src="factory" data-dst="工厂">工厂</trans></span><trans data-src="(" data-dst="（">（</trans><span class="pl-s"><span class="pl-pds"><trans data-src="'" data-dst="'"><trans data-src="'" data-dst="'">'</trans></trans></span><trans data-src="Restaurant" data-dst="餐厅">餐厅</trans><span class="pl-pds"><trans data-src="'" data-dst="'"><trans data-src="'" data-dst="'">'</trans></trans></span></span><trans data-src=", " data-dst="，">，</trans><span class="pl-k"><trans data-src="function" data-dst="功能">功能</trans></span><trans data-src="(" data-dst="（">（</trans><span class="pl-smi"><trans data-src="$resource" data-dst="资源">资源</trans></span><trans data-src=") {
  " data-dst="）{">）{</trans><span class="pl-k"><trans data-src="return" data-dst="退货">退货</trans></span> <span class="pl-en"><trans data-src="$resource" data-dst="资源">资源</trans></span><trans data-src="(" data-dst="（">（</trans><span class="pl-s"><span class="pl-pds"><trans data-src="'" data-dst="'"><trans data-src="'" data-dst="'">'</trans></trans></span><trans data-src="/api/restaurant/:id" data-dst="/接口/餐厅/：ID">/接口/餐厅/：ID</trans><span class="pl-pds"><trans data-src="'" data-dst="'"><trans data-src="'" data-dst="'">'</trans></trans></span></span><trans data-src=", {id" data-dst="{ ID，">{ ID，</trans><span class="pl-k"><trans data-src=":" data-dst="：">：</trans></span> <span class="pl-s"><span class="pl-pds"><trans data-src="'" data-dst="'"><trans data-src="'" data-dst="'">'</trans></trans></span><trans data-src="@id" data-dst="@ ID">@ ID</trans><span class="pl-pds"><trans data-src="'" data-dst="'"><trans data-src="'" data-dst="'">'</trans></trans></span></span><trans data-src="}, {
    query" data-dst="}，{ 
查询">}，{ 
查询</trans><span class="pl-k"><trans data-src=":" data-dst="：">：</trans></span><trans data-src=" {
      method" data-dst="{ 
方法">{ 
方法</trans><span class="pl-k"><trans data-src=":" data-dst="：">：</trans></span> <span class="pl-s"><span class="pl-pds"><trans data-src="'" data-dst="'"><trans data-src="'" data-dst="'">'</trans></trans></span><trans data-src="GET" data-dst="得到">得到</trans><span class="pl-pds"><trans data-src="'" data-dst="'"><trans data-src="'" data-dst="'">'</trans></trans></span></span><trans data-src=",
      isArray" data-dst="，
">，
</trans><span class="pl-k"><trans data-src=":" data-dst="：">：</trans></span> <span class="pl-c1"><trans data-src="true" data-dst="真正的">真正的</trans></span><trans data-src=",
      ignoreLoadingBar" data-dst="ignoreloadingbar，
">ignoreloadingbar，
</trans><span class="pl-k"><trans data-src=":" data-dst="：">：</trans></span> <span class="pl-c1"><trans data-src="true" data-dst="真正的">真正的</trans></span><trans data-src="
    }
  });
});
" data-dst="} }）；}）
 
；">} }）；}）
 
；</trans></pre></div>

<h2><a id="user-content-how-it-works" class="anchor" href="#how-it-works" aria-hidden="true"><svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path d="M4 9h1v1h-1c-1.5 0-3-1.69-3-3.5s1.55-3.5 3-3.5h4c1.45 0 3 1.69 3 3.5 0 1.41-0.91 2.72-2 3.25v-1.16c0.58-0.45 1-1.27 1-2.09 0-1.28-1.02-2.5-2-2.5H4c-0.98 0-2 1.22-2 2.5s1 2.5 2 2.5z m9-3h-1v1h1c1 0 2 1.22 2 2.5s-1.02 2.5-2 2.5H9c-0.98 0-2-1.22-2-2.5 0-0.83 0.42-1.64 1-2.09v-1.16c-1.09 0.53-2 1.84-2 3.25 0 1.81 1.55 3.5 3 3.5h4c1.45 0 3-1.69 3-3.5s-1.5-3.5-3-3.5z"></path></svg></a><trans data-src="How it works:" data-dst="工作原理">工作原理</trans></h2>

<p><trans data-src="This library is split into two modules, an $http " data-dst="这个图书馆被分为两个模块，一个$ http">这个图书馆被分为两个模块，一个$ http</trans><code><trans data-src="interceptor" data-dst="拦截">拦截</trans></code><trans data-src=", and a " data-dst="，和一个">，和一个</trans><code><trans data-src="service" data-dst="服务">服务</trans></code><trans data-src=":" data-dst="：">：</trans></p>

<p><strong><trans data-src="Interceptor" data-dst="拦截">拦截</trans></strong><br><trans data-src="
The interceptor simply listens for all outgoing XHR requests, and then instructs the loadingBar service to start, stop, and increment accordingly.  There is no public API for the interceptor.  It can be used stand-alone by including " data-dst="拦截只是侦听所有外向的XHR请求，然后指示loadingbar服务启动，停止，并增加相应的。有没有公共API拦截。它可以包括独立使用">拦截只是侦听所有外向的XHR请求，然后指示loadingbar服务启动，停止，并增加相应的。有没有公共API拦截。它可以包括独立使用</trans><code><trans data-src="cfp.loadingBarInterceptor" data-dst="cfp.loadingbarinterceptor">cfp.loadingbarinterceptor</trans></code><trans data-src=" as a dependency for your module." data-dst="作为你的模块依赖。">作为你的模块依赖。</trans></p>

<p><strong><trans data-src="Service" data-dst="服务">服务</trans></strong><br><trans data-src="
The service is responsible for the presentation of the loading bar.  It injects the loading bar into the DOM, adjusts the width whenever " data-dst="服务是负责加载酒吧介绍。它将加载杆到DOM，调整宽度时">服务是负责加载酒吧介绍。它将加载杆到DOM，调整宽度时</trans><code><trans data-src="set()" data-dst="set()"><trans data-src="set()" data-dst="set()">set()</trans></trans></code><trans data-src=" is called, and " data-dst="被称为，和">被称为，和</trans><code><trans data-src="complete()" data-dst="（全集）">（全集）</trans></code><trans data-src="s the whole show by removing the loading bar from the DOM." data-dst="从DOM去除负荷杆整体展示。">从DOM去除负荷杆整体展示。</trans></p>

<h2><a id="user-content-service-api-advanced-usage" class="anchor" href="#service-api-advanced-usage" aria-hidden="true"><svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path d="M4 9h1v1h-1c-1.5 0-3-1.69-3-3.5s1.55-3.5 3-3.5h4c1.45 0 3 1.69 3 3.5 0 1.41-0.91 2.72-2 3.25v-1.16c0.58-0.45 1-1.27 1-2.09 0-1.28-1.02-2.5-2-2.5H4c-0.98 0-2 1.22-2 2.5s1 2.5 2 2.5z m9-3h-1v1h1c1 0 2 1.22 2 2.5s-1.02 2.5-2 2.5H9c-0.98 0-2-1.22-2-2.5 0-0.83 0.42-1.64 1-2.09v-1.16c-1.09 0.53-2 1.84-2 3.25 0 1.81 1.55 3.5 3 3.5h4c1.45 0 3-1.69 3-3.5s-1.5-3.5-3-3.5z"></path></svg></a><trans data-src="Service API (advanced usage)" data-dst="服务API（高级用法）">服务API（高级用法）</trans></h2>

<p><trans data-src="Under normal circumstances you won't need to use this.  However, if you wish to use the loading bar without the interceptor, you can do that as well.  Simply include the loading bar service as a dependency instead of the main " data-dst="正常情况下你不需要这个。然而，如果你希望使用加载杆没有拦截，你也可以这样做。只要包含加载酒吧服务作为一个依赖而不是主">正常情况下你不需要这个。然而，如果你希望使用加载杆没有拦截，你也可以这样做。只要包含加载酒吧服务作为一个依赖而不是主</trans><code><trans data-src="angular-loading-bar" data-dst="角加载杆">角加载杆</trans></code><trans data-src=" module:" data-dst="模块">模块</trans></p>

<div class="highlight highlight-source-js"><pre><span class="pl-smi"><trans data-src="angular" data-dst="角">角</trans></span><trans data-src="." data-dst="。">。</trans><span class="pl-en"><trans data-src="module" data-dst="模块">模块</trans></span><trans data-src="(" data-dst="（">（</trans><span class="pl-s"><span class="pl-pds"><trans data-src="'" data-dst="'"><trans data-src="'" data-dst="'">'</trans></trans></span><trans data-src="myApp" data-dst="MyApp">MyApp</trans><span class="pl-pds"><trans data-src="'" data-dst="'"><trans data-src="'" data-dst="'">'</trans></trans></span></span><trans data-src=", [" data-dst="，[">，[</trans><span class="pl-s"><span class="pl-pds"><trans data-src="'" data-dst="'"><trans data-src="'" data-dst="'">'</trans></trans></span><trans data-src="cfp.loadingBar" data-dst="cfp.loadingbar">cfp.loadingbar</trans><span class="pl-pds"><trans data-src="'" data-dst="'"><trans data-src="'" data-dst="'">'</trans></trans></span></span><trans data-src="])" data-dst="]）">]）</trans></pre></div>

<div class="highlight highlight-source-js"><pre><span class="pl-smi"><trans data-src="cfpLoadingBar" data-dst="cfploadingbar">cfploadingbar</trans></span><trans data-src="." data-dst="。">。</trans><span class="pl-c1"><trans data-src="start" data-dst="开始">开始</trans></span><trans data-src="();
" data-dst="（）；">（）；</trans><span class="pl-c"><trans data-src="// will insert the loading bar into the DOM, and display its progress at 1%." data-dst="/将插入到DOM加载杆，并在1%显示其进度。">/将插入到DOM加载杆，并在1%显示其进度。</trans></span>
<span class="pl-c"><trans data-src="// It will automatically call `inc()` repeatedly to give the illusion that the page load is progressing." data-dst="/ /它会自动调用` inc() `多次给幻想的页面加载进度。">/ /它会自动调用` inc() `多次给幻想的页面加载进度。</trans></span>

<span class="pl-smi"><trans data-src="cfpLoadingBar" data-dst="cfploadingbar">cfploadingbar</trans></span><trans data-src="." data-dst="。">。</trans><span class="pl-en"><trans data-src="inc" data-dst="股份有限公司">股份有限公司</trans></span><trans data-src="();
" data-dst="（）；">（）；</trans><span class="pl-c"><trans data-src="// increments the loading bar by a random amount." data-dst="/ /增量加载杆由一个随机量。">/ /增量加载杆由一个随机量。</trans></span>
<span class="pl-c"><trans data-src="// It is important to note that the auto incrementing will begin to slow down as" data-dst="//需要注意的是，汽车增量将开始慢下来一样重要">//需要注意的是，汽车增量将开始慢下来一样重要</trans></span>
<span class="pl-c"><trans data-src="// the progress increases.  This is to prevent the loading bar from appearing" data-dst="/ /进步。这是为了防止出现加载杆">/ /进步。这是为了防止出现加载杆</trans></span>
<span class="pl-c"><trans data-src="// completed (or almost complete) before the XHR request has responded." data-dst="/ /完成（或几乎完全）在XHR请求的回应。">/ /完成（或几乎完全）在XHR请求的回应。</trans></span>

<span class="pl-smi"><trans data-src="cfpLoadingBar" data-dst="cfploadingbar">cfploadingbar</trans></span><trans data-src="." data-dst="。">。</trans><span class="pl-en"><trans data-src="set" data-dst="配置">配置</trans></span><trans data-src="(" data-dst="（">（</trans><span class="pl-c1"><trans data-src="0.3" data-dst="零点三">零点三</trans></span><trans data-src=") " data-dst="）">）</trans><span class="pl-c"><trans data-src="// Set the loading bar to 30%" data-dst="//设置加载杆30%">//设置加载杆30%</trans></span>
<span class="pl-smi"><trans data-src="cfpLoadingBar" data-dst="cfploadingbar">cfploadingbar</trans></span><trans data-src="." data-dst="。">。</trans><span class="pl-c1"><trans data-src="status" data-dst="地位">地位</trans></span><trans data-src="() " data-dst="（）">（）</trans><span class="pl-c"><trans data-src="// Returns the loading bar's progress." data-dst="//返回加载杆的进步。">//返回加载杆的进步。</trans></span>
<span class="pl-c"><trans data-src="//-> 0.3" data-dst="//- > 0.3">/ / - &gt; 0.3</trans></span>

<span class="pl-smi"><trans data-src="cfpLoadingBar" data-dst="cfploadingbar">cfploadingbar</trans></span><trans data-src="." data-dst="。">。</trans><span class="pl-c1"><trans data-src="complete" data-dst="完成">完成</trans></span><trans data-src="()
" data-dst="（）">（）</trans><span class="pl-c"><trans data-src="// Set the loading bar's progress to 100%, and then remove it from the DOM." data-dst="//100%设置加载杆的进步，然后把它从DOM。">// 100%设置加载杆的进步，然后把它从DOM。</trans></span>
</pre></div>

<h2><a id="user-content-events" class="anchor" href="#events" aria-hidden="true"><svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path d="M4 9h1v1h-1c-1.5 0-3-1.69-3-3.5s1.55-3.5 3-3.5h4c1.45 0 3 1.69 3 3.5 0 1.41-0.91 2.72-2 3.25v-1.16c0.58-0.45 1-1.27 1-2.09 0-1.28-1.02-2.5-2-2.5H4c-0.98 0-2 1.22-2 2.5s1 2.5 2 2.5z m9-3h-1v1h1c1 0 2 1.22 2 2.5s-1.02 2.5-2 2.5H9c-0.98 0-2-1.22-2-2.5 0-0.83 0.42-1.64 1-2.09v-1.16c-1.09 0.53-2 1.84-2 3.25 0 1.81 1.55 3.5 3 3.5h4c1.45 0 3-1.69 3-3.5s-1.5-3.5-3-3.5z"></path></svg></a><trans data-src="Events" data-dst="事件">事件</trans></h2>

<p><trans data-src="The loading bar broadcasts the following events over $rootScope allowing further customization:" data-dst="加载酒吧播放以下事件超过rootscope允许进一步定制：">加载酒吧播放以下事件超过rootscope允许进一步定制：</trans></p>

<p><strong><code><trans data-src="cfpLoadingBar:loading" data-dst="cfploadingbar：加载">cfploadingbar：加载</trans></code></strong><trans data-src=" triggered upon each XHR request that is not already cached" data-dst="在每一个XHR请求触发，是不是已经缓存">在每一个XHR请求触发，是不是已经缓存</trans></p>

<p><strong><code><trans data-src="cfpLoadingBar:loaded" data-dst="cfploadingbar：加载">cfploadingbar：加载</trans></code></strong><trans data-src=" triggered each time an XHR request recieves a response (either successful or error)" data-dst="每次触发XHR请求接待响应（成功或错误）">每次触发XHR请求接待响应（成功或错误）</trans></p>

<p><strong><code><trans data-src="cfpLoadingBar:started" data-dst="cfploadingbar：开始">cfploadingbar：开始</trans></code></strong><trans data-src=" triggered once upon the first XHR request.  Will trigger again if another request goes out after " data-dst="触发一次后的第一个XHR请求。如果再将触发另一个请求后熄灭">触发一次后的第一个XHR请求。如果再将触发另一个请求后熄灭</trans><code><trans data-src="cfpLoadingBar:completed" data-dst="cfploadingbar：完成">cfploadingbar：完成</trans></code><trans data-src=" has triggered." data-dst="引发了。">引发了。</trans></p>

<p><strong><code><trans data-src="cfpLoadingBar:completed" data-dst="cfploadingbar：完成">cfploadingbar：完成</trans></code></strong><trans data-src=" triggered once when the all XHR requests have returned (either successfully or not)" data-dst="触发一次当所有XHR请求返回（成功与否）">触发一次当所有XHR请求返回（成功与否）</trans></p>

<h2><a id="user-content-credits" class="anchor" href="#credits" aria-hidden="true"><svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path d="M4 9h1v1h-1c-1.5 0-3-1.69-3-3.5s1.55-3.5 3-3.5h4c1.45 0 3 1.69 3 3.5 0 1.41-0.91 2.72-2 3.25v-1.16c0.58-0.45 1-1.27 1-2.09 0-1.28-1.02-2.5-2-2.5H4c-0.98 0-2 1.22-2 2.5s1 2.5 2 2.5z m9-3h-1v1h1c1 0 2 1.22 2 2.5s-1.02 2.5-2 2.5H9c-0.98 0-2-1.22-2-2.5 0-0.83 0.42-1.64 1-2.09v-1.16c-1.09 0.53-2 1.84-2 3.25 0 1.81 1.55 3.5 3 3.5h4c1.45 0 3-1.69 3-3.5s-1.5-3.5-3-3.5z"></path></svg></a><trans data-src="Credits:" data-dst="积分">积分</trans></h2>

<p><trans data-src="Credit goes to " data-dst="归功于">归功于</trans><a href="https://github.com/rstacruz"><trans data-src="rstacruz" data-dst="rstacruz"><trans data-src="rstacruz" data-dst="rstacruz">rstacruz</trans></trans></a><trans data-src=" for his excellent " data-dst="他出色的">他出色的</trans><a href="https://github.com/rstacruz/nprogress"><trans data-src="nProgress" data-dst="nprogress">nprogress</trans></a><trans data-src="." data-dst="。">。</trans></p>

<h2><a id="user-content-license" class="anchor" href="#license" aria-hidden="true"><svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path d="M4 9h1v1h-1c-1.5 0-3-1.69-3-3.5s1.55-3.5 3-3.5h4c1.45 0 3 1.69 3 3.5 0 1.41-0.91 2.72-2 3.25v-1.16c0.58-0.45 1-1.27 1-2.09 0-1.28-1.02-2.5-2-2.5H4c-0.98 0-2 1.22-2 2.5s1 2.5 2 2.5z m9-3h-1v1h1c1 0 2 1.22 2 2.5s-1.02 2.5-2 2.5H9c-0.98 0-2-1.22-2-2.5 0-0.83 0.42-1.64 1-2.09v-1.16c-1.09 0.53-2 1.84-2 3.25 0 1.81 1.55 3.5 3 3.5h4c1.45 0 3-1.69 3-3.5s-1.5-3.5-3-3.5z"></path></svg></a><trans data-src="License:" data-dst="许可证">许可证</trans></h2>

<p><trans data-src="Licensed under the MIT license" data-dst="使用MIT许可证下">使用MIT许可证下</trans></p>
</article>
###EN
angular-loading-bar
===================

The idea is simple: Add a loading bar / progress bar whenever an XHR request goes out in angular.  Multiple requests within the same time period get bundled together such that each response increments the progress bar by the appropriate amount.

This is mostly cool because you simply include it in your app, and it works.  There's no complicated setup, and no need to maintain the state of the loading bar; it's all handled automatically by the interceptor.

**Requirements:** AngularJS 1.2+

**File Size:** 2.4Kb minified, 0.5Kb gzipped


## Usage:

1. include the loading bar as a dependency for your app.  If you want animations, include `ngAnimate` as well. *note: ngAnimate is optional*

    ```js
    angular.module('myApp', ['angular-loading-bar', 'ngAnimate'])
    ```

2. include the supplied JS and CSS file (or create your own CSS to override defaults).

    ```html
    <link rel='stylesheet' href='build/loading-bar.min.css' type='text/css' media='all' />
    <script type='text/javascript' src='build/loading-bar.min.js'></script>
    ```

3. That's it -- you're done!

#### via bower:
```
$ bower install angular-loading-bar
```
#### via npm:
```
$ npm install angular-loading-bar
```

#### via CDN:
```html
 <link rel='stylesheet' href='//cdnjs.c2cbc.com/ajax/libs/angular-loading-bar/0.9.0/loading-bar.min.css' type='text/css' media='all' />
 <script type='text/javascript' src='//cdnjs.c2cbc.com/ajax/libs/angular-loading-bar/0.9.0/loading-bar.min.js'></script>
```

## Why I created this
There are a couple projects similar to this out there, but none were ideal for me.  All implementations I've seen require that you maintain state on behalf of the loading bar.  In other words, you're setting the value of the loading/progress bar manually from potentially many different locations.  This becomes complicated when you have a very large application with several services all making independent XHR requests. It becomes even more complicated if you want these services to be loosly coupled.

Additionally, Angular was created as a highly testable framework, so it pains me to see Angular modules without tests.  That is not the case here as this loading bar ships with 100% code coverage.


**Goals for this project:**

1. Make it automatic
2. Unit tests, 100% coverage
3. Must work well with ngAnimate
4. Must be styled via external CSS (not inline)
5. No jQuery dependencies


## Configuration

#### Turn the spinner on or off:
The insertion of the spinner can be controlled through configuration.  It's on by default, but if you'd like to turn it off, simply configure the service:

```js
angular.module('myApp', ['angular-loading-bar'])
  .config(['cfpLoadingBarProvider', function(cfpLoadingBarProvider) {
    cfpLoadingBarProvider.includeSpinner = false;
  }])
```

#### Turn the loading bar on or off:
Like the spinner configuration above, the loading bar can also be turned off for cases where you only want the spinner:

```js
angular.module('myApp', ['angular-loading-bar'])
  .config(['cfpLoadingBarProvider', function(cfpLoadingBarProvider) {
    cfpLoadingBarProvider.includeBar = false;
  }])
```

#### Customize the template:
If you'd like to replace the default HTML template you can configure it by providing inline HTML as a string:

```js
angular.module('myApp', ['angular-loading-bar'])
  .config(['cfpLoadingBarProvider', function(cfpLoadingBarProvider) {
    cfpLoadingBarProvider.spinnerTemplate = '<div><span class="fa fa-spinner">Loading...</div>';
  }])
```

#### Position the template:
If you'd like to position the loadingBar or spinner, provide a CSS selector to the element you'd like the template injected into. The default is the `<body>` element:

```js
angular.module('myApp', ['angular-loading-bar'])
  .config(['cfpLoadingBarProvider', function(cfpLoadingBarProvider) {
    cfpLoadingBarProvider.parentSelector = '#loading-bar-container';
    cfpLoadingBarProvider.spinnerTemplate = '<div><span class="fa fa-spinner">Custom Loading Message...</div>';
  }])
```
```html
<div id="loading-bar-container"></div>
```

#### Latency Threshold
By default, the loading bar will only display after it has been waiting for a response for over 100ms.  This helps keep things feeling snappy, and avoids the annoyingness of showing a loading bar every few seconds on really chatty applications.  This threshold is totally configurable:

```js
angular.module('myApp', ['angular-loading-bar'])
  .config(['cfpLoadingBarProvider', function(cfpLoadingBarProvider) {
    cfpLoadingBarProvider.latencyThreshold = 500;
  }])
```

#### Ignoring particular XHR requests:
The loading bar can also be forced to ignore certain requests, for example, when long-polling or periodically sending debugging information back to the server.

```js
// ignore a particular $http GET:
$http.get('/status', {
  ignoreLoadingBar: true
});

// ignore a particular $http POST.  Note: POST and GET have different
// method signatures:
$http.post('/save', data, {
  ignoreLoadingBar: true
});

```


```js
// ignore particular $resource requests:
.factory('Restaurant', function($resource) {
  return $resource('/api/restaurant/:id', {id: '@id'}, {
    query: {
      method: 'GET',
      isArray: true,
      ignoreLoadingBar: true
    }
  });
});

```




## How it works:
This library is split into two modules, an $http `interceptor`, and a `service`:

**Interceptor**  
The interceptor simply listens for all outgoing XHR requests, and then instructs the loadingBar service to start, stop, and increment accordingly.  There is no public API for the interceptor.  It can be used stand-alone by including `cfp.loadingBarInterceptor` as a dependency for your module.

**Service**  
The service is responsible for the presentation of the loading bar.  It injects the loading bar into the DOM, adjusts the width whenever `set()` is called, and `complete()`s the whole show by removing the loading bar from the DOM.

## Service API (advanced usage)
Under normal circumstances you won't need to use this.  However, if you wish to use the loading bar without the interceptor, you can do that as well.  Simply include the loading bar service as a dependency instead of the main `angular-loading-bar` module:

```js
angular.module('myApp', ['cfp.loadingBar'])
```


```js

cfpLoadingBar.start();
// will insert the loading bar into the DOM, and display its progress at 1%.
// It will automatically call `inc()` repeatedly to give the illusion that the page load is progressing.

cfpLoadingBar.inc();
// increments the loading bar by a random amount.
// It is important to note that the auto incrementing will begin to slow down as
// the progress increases.  This is to prevent the loading bar from appearing
// completed (or almost complete) before the XHR request has responded.

cfpLoadingBar.set(0.3) // Set the loading bar to 30%
cfpLoadingBar.status() // Returns the loading bar's progress.
// -> 0.3

cfpLoadingBar.complete()
// Set the loading bar's progress to 100%, and then remove it from the DOM.

```

## Events
The loading bar broadcasts the following events over $rootScope allowing further customization:

**`cfpLoadingBar:loading`** triggered upon each XHR request that is not already cached

**`cfpLoadingBar:loaded`** triggered each time an XHR request recieves a response (either successful or error)

**`cfpLoadingBar:started`** triggered once upon the first XHR request.  Will trigger again if another request goes out after `cfpLoadingBar:completed` has triggered.

**`cfpLoadingBar:completed`** triggered once when the all XHR requests have returned (either successfully or not)

## Credits:
Credit goes to [rstacruz](https://github.com/rstacruz) for his excellent [nProgress](https://github.com/rstacruz/nprogress).

## License:
Licensed under the MIT license
