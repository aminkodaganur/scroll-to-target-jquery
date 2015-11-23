# scroll-to-target-jquery
Scroll to bottom using JQuery

- Menu : below is menu you can use li or nav whatever you want but just add a class "scroll-bottom" to link and target container ID in data-scrolltarget="#ID" property 
- E.X:
-<a href="javascript:void(0)" class="scroll-bottom" data-scrolltarget="#target_div_id1">section 1</a>
-<a href="javascript:void(0)" class="scroll-bottom" data-scrolltarget="#target_div_id2">section 2</a>
-<a href="javascript:void(0)" class="scroll-bottom" data-scrolltarget="#target_div_id3">section 2</a>

-Your container will look like this 

<div id="target_div_id1"> ....Section 1 Description...  </div>
<div id="target_div_id2"> ....Section 2 Description...  </div>
<div id="target_div_id3"> ....Section 3 Description...  </div>

Now Add jquery Code

$(".scroll-bottom").click(function() {
    var toid = $(this).data('scrolltarget');
    $('html, body').animate({
        scrollTop: $(toid).offset().top - 45
    }, 1000);
});
