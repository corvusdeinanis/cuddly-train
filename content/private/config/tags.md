<%* 
var yaml = '';

var tArr = tp.file.tags;

tArr.sort();

var tStr = tArr.join(', ').replace(/#/g,'');

if (tStr.length) {

yaml = '---\ntags: [' + tStr + ']\n---\n';
}
%><%* tR += yaml %>

