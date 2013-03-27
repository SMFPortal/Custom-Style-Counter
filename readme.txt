Custom Style Counter 1.0

This package contains the following files will be modified:

- index.css
- BoardIndex.template.php

Presentation of the amendment:

index.css:

Insert at the end:

[code] / * Custom style counter * /

. {custom_sc
     background: none repeat scroll 0 0 # 788a9e;
     border: 1px solid # 788a9e;
     border-radius: 5px 5px 5px 5px;
     color: # FFF;
     height: 28px;
     line-height: 28px;
     margin: 0 10px 0 0;
     padding: 4px 10px;
     text-shadow: 0 1px 0 # 000;
}

/ * Custom style counter * / [/ code]

BoardIndex.temaplate.php:

Original part:

[code] / / show some basic information about the number of posts, etc..
echo '
</ td>
<td class="stats windowbg">
<p> ', comma_format ($ board [' posts']), '', $ board ['is_redirect']? $ txt ['redirects']: $ txt [' posts'], '<br />
', $ Board [' is_redirect ']? '': Comma_format ($ board ['topics']). ''. $ txt ['board_topics'],'
</ p>
</ td>
<td class="lastpost"> '; [/ code]

Replace with:

[code] / / show some basic information about the number of posts, etc..
                     echo '
                     </ td>
                     <td class="stats windowbg">
                         <span class="custom_sc"> ', comma_format ($ board [' posts']), '', $ board ['is_redirect']? $ txt ['redirects']: $ txt [' posts'], '</ span> />
                         <span class="custom_sc"> ', $ board [' is_redirect ']? '': Comma_format ($ board ['topics']). ''. $ txt ['board_topics'],'
                         </ span> </ p>
                     </ td>
                     <td class="lastpost"> '; [/ code]
