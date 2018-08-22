---
layout: default
---
<script type="text/javascript" src="//s7.addthis.com/js/300/addthis_widget.js#pubid=ra-5abac57df3c38cac"></script> 

<h2 style="margin-bottom: 0;">{{page.title}}</h2>
<p style="margin-top: 2px;color: #808080; margin-bottom: 3em;">{{page.date | date: "%b %d, %Y"}} • <span>{{page.categories}}</span></p>

{{content}}

<div id="fb-root"></div>
<div class="fb-share-button" data-href="{{page.url}}" data-layout="button" data-size="large" data-mobile-iframe="true"><a target="_blank" href="{{page.url}}" class="fb-xfbml-parse-ignore">Share</a></div>

<a href="">share on twitter</a>


{% if page.comments %}

<div id="disqus_thread"></div>

{% endif %}

<script>

/**
*  RECOMMENDED CONFIGURATION VARIABLES: EDIT AND UNCOMMENT THE SECTION BELOW TO INSERT DYNAMICVALUES FROM YOUR PLATFORM OR CMS.
*  LEARN WHY DEFINING THESE VARIABLES IS IMPORTANT:https://disqus.com/admin/universalcode/#configuration-variables*/

var disqus_config = function () {
  this.page.url = '{{ page.url | absolute_url }}';
  this.page.identifier = '{{ page.url | absolute_url }}';
};

console.log("{{page.url}}");

(function() { // DON'T EDIT BELOW THIS LINE
    var d = document, s = d.createElement('script');
    s.src = 'https://zeyadetman.disqus.com/embed.js';
    s.setAttribute('data-timestamp', +new Date());
    (d.head || d.body).appendChild(s);
})();

(function(d, s, id) {
  var js, fjs = d.getElementsByTagName(s)[0];
  if (d.getElementById(id)) return;
  js = d.createElement(s); js.id = id;
  js.src = 'https://connect.facebook.net/en_US/sdk.js#xfbml=1&version=v3.1&appId=269290577224281&autoLogAppEvents=1';
  fjs.parentNode.insertBefore(js, fjs);
}(document, 'script', 'facebook-jssdk'));

</script>

<noscript>Please enable JavaScript to view the <a href="https://disqus.com/ref_noscript">comments powered by Disqus.</a></noscript>
