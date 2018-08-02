# scroll-to-target-jquery
Scroll to bottom using JQuery

- Menu : below is menu you can use li or nav whatever you want but just add a `class "scroll-bottom"` to link and target container ID in `data-scrolltarget="#ID"` property 
- E.X:
```sh
<a href="javascript:void(0)" class="scroll-bottom" data-scrolltarget="#target_div_id1">;section </a><br />
<a href="javascript:void(0)" class="scroll-bottom" data-scrolltarget="#target_div_id2">;section </a><br />
<a href="javascript:void(0)" class="scroll-bottom" data-scrolltarget="#target_div_id3">;section </a>
```
-Your container will look like this 
```sh
<div id="target_div_id1">....Section 1 Description...  </div><br />
<div id="target_div_id2"> ....Section 2 Description...  </div><br />
<div id="target_div_id3"> ....Section 3 Description...  </div>
```
Now Add jquery Code
```sh
$(".scroll-bottom").click(function() {<br />
    var toid = $(this).data('scrolltarget');<br />
    $('html, body').animate({<br />
        scrollTop: $(toid).offset().top - 45<br />
    }, 1000);<br />
});
```
