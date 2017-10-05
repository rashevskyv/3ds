---
title: "Администрирование виджета"
sitemap: false
permalink: /widget.html
---

<div id="vk_comments_browse"></div>
<script type="text/javascript">
window.onload = function () {
 VK.init({apiId: 6045959, onlyWidgets: true});
 VK.Widgets.CommentsBrowse('vk_comments_browse', {limit: 50, mini: 0});
}
</script>