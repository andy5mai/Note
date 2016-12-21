```

$str = '';
$_strSpecial = "<br />
<font size='1'><table class='xdebug-error xe-notice' dir='ltr' border='1' cellspacing='0' cellpadding='1'>
<tr>
    <th align='left' bgcolor='#f57900' colspan=\"5\"><span style='background-color: #cc0000; color: #fce94f; font-size: x-large;'>( ! )</span> Notice: crypt(): No salt parameter was specified. You must use a randomly generated salt and a strong hash function to produce a secure hash. in E:\SVN\PHP\Moregeek\website\MBR\mobile\stages\api\mobile\mobile_register.php on line <i>58</i>
    </th>
</tr>
<tr>
    <th align='left' bgcolor='#e9b96e' colspan='5'>
        Call Stack
    </th>
</tr>
<tr>
    <th align='center' bgcolor='#eeeeec'>#</th><th align='left' bgcolor='#eeeeec'>
        Time
    </th>
    <th align='left' bgcolor='#eeeeec'>
        Memory
    </th>
    <th align='left' bgcolor='#eeeeec'>
        Function
    </th>
    <th align='left' bgcolor='#eeeeec'>
        Location
    </th>
</tr>
<tr>
    <td bgcolor='#eeeeec' align='center'>
        1
    </td>
    <td bgcolor='#eeeeec' align='center'>
        0.0010
    </td>
    <td bgcolor='#eeeeec' align='right'>
        133856
    </td>
    <td bgcolor='#eeeeec'>
        {main}(  )
    </td>
    <td title='E:\SVN\PHP\Moregeek\website\MBR\index.php' bgcolor='#eeeeec'>
        ...\index.php<b>:</b>0
    </td>
</tr>
<tr>
    <td bgcolor='#eeeeec' align='center'>
        2
    </td>
    <td bgcolor='#eeeeec' align='center'>
        0.1910
    </td>
    <td bgcolor='#eeeeec' align='right'>
        2415888
    </td>
    <td bgcolor='#eeeeec'>
        require_once( <font color='#00bb00'>'E:\SVN\PHP\Moregeek\website\MBR\includes\run_module.php'</font> )
    </td>
    <td title='E:\SVN\PHP\Moregeek\website\MBR\index.php' bgcolor='#eeeeec'>
        ...\index.php<b>:</b>19
    </td>
</tr>
<tr>
    <td bgcolor='#eeeeec' align='center'>
        3
    </td>
    <td bgcolor='#eeeeec' align='center'>
        0.1920
    </td>
    <td bgcolor='#eeeeec' align='right'>
        2448816
    </td>
    <td bgcolor='#eeeeec'>
        require_once( <font color='#00bb00'>'E:\SVN\PHP\Moregeek\website\MBR\mobile\stages\api\mobile\mobile_register.php'</font> )
     </td>
     <td title='E:\SVN\PHP\Moregeek\website\MBR\includes\run_module.php' bgcolor='#eeeeec'>
        ...\run_module.php<b>:</b>55
     </td>
</tr>
<tr>
     <td bgcolor='#eeeeec' align='center'>
        4
     </td>
     <td bgcolor='#eeeeec' align='center'>
        0.2010
     </td>
     <td bgcolor='#eeeeec' align='right'>
        3182816
     </td>
     <td bgcolor='#eeeeec'>
        <a href='http://www.php.net/function.crypt' target='_new'>crypt</a>(  )
     </td>
     <td title='E:\SVN\PHP\Moregeek\website\MBR\mobile\stages\api\mobile\mobile_register.php' bgcolor='#eeeeec'>
        ...\mobile_register.php<b>:</b>58
     </td>
</tr>
</table></font>
Invalid address: andy1115You must provide at least one recipient email address.";
		if ($num > 0)
		{
			$str = 'str = function(){/*'.str_replace('"', "'", $_strSpecial).'*/}.toString().slice(14, -3);';
		}
		else
		{
			$str = 'str = "<div name='.'div0'.'>test0</div>";';
		}
		echo $str;

```