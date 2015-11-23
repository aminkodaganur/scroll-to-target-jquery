# scroll-to-target-jquery
Scroll to bottom using JQuery

- Menu : below is menu you can use li or nav whatever you want but just add a class "scroll-bottom" to link and target container ID in data-scrolltarget="#ID" property 
- E.X:

&lt;a href="javascript:void(0)" class="scroll-bottom" data-scrolltarget="#target_div_id1"&gt;section 1&lt;/a&gt;<br />
&lt;a href="javascript:void(0)" class="scroll-bottom" data-scrolltarget="#target_div_id2"&gt;section 2&lt;/a&gt;<br />
&lt;a href="javascript:void(0)" class="scroll-bottom" data-scrolltarget="#target_div_id3"&gt;section 2&lt;/a&gt;

-Your container will look like this 

&lt;div id="target_div_id1"&gt; ....Section 1 Description...  &lt;/div&gt;<br />
&lt;div id="target_div_id2"&gt; ....Section 2 Description...  &lt;/div&gt;<br />
&lt;div id="target_div_id3"&gt; ....Section 3 Description...  &lt;/div&gt;

Now Add jquery Code

$(".scroll-bottom").click(function() {<br />
    var toid = $(this).data('scrolltarget');<br />
    $('html, body').animate({<br />
        scrollTop: $(toid).offset().top - 45<br />
    }, 1000);<br />
});
