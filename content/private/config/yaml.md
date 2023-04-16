---
title: "<% tp.file.title %>"
tags: ['']
date: <% tp.date.now("YYYY-MM-DD") %>


<%* 
var yaml = '';

var tArr = tp.file.tags;

tArr.sort();

var tStr = tArr.join(', ').replace(/#/g,'');

if (tStr.length) {

yaml = '---\ntags: [' + tStr + ']\n---\n';
}
%><%* tR += yaml %>
---