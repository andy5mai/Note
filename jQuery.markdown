# add element
$('#table').append($('<tr>').append($('<td>').append(text)));    

var a = $('a');
a.attr('href', 'http://www.google.com.tw').text("123");
$('body').append(a);    

<pre>
$('<a>',{
    text: 'This is blah',
    title: 'Blah',
    href: '#',
    click: function(){ BlahFunc( options.rowId );return false;}).appendTo('body');
</pre>