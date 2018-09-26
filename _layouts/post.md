---
layout: default
---

<style>
.content-body img{
    max-width: 100%;
}

.post-title{
  margin: 0 auto 15px auto;
  padding: 15px;
  width: fit-content;
  border-radius: 5px;
  color: #3e3e3e;
  background: rgba(255, 192, 4, 0.88);
}

.post-info{
  color: #808080;
  display: flex;
  justify-content: center;
  align-items: center;
  padding-bottom: 15px;
  border-bottom: 1px solid #808080;
}
</style>
<script type="text/javascript" src="//s7.addthis.com/js/300/addthis_widget.js#pubid=ra-5abac57df3c38cac"></script> 

<h2 class="post-title">{{page.title}}</h2>
<p class="post-info">{{page.date | date: "%b %d, %Y"}}<span style="margin: 0 10px;">{{page.categories}}</span>
<a class="twitter-follow-button"
  href="https://twitter.com/zeyadetman"
  data-size="small"></a>
</p>

<div class="content-body">
{{content}}
</div>
<div class="socialmedia">
    <div id="fb-root"></div>
    <div class="fb-share-button" data-href="{{page.url}}" data-layout="button" data-size="large"       data-mobile-iframe="true"><a target="_blank" href="{{page.url}}"                              class="fb-xfbml-parse-ignore"></a></div>

    <a class="twitter-share-button"
        href=
        "https://twitter.com/intent/tweet?text={{page.title}},%20read%20it%20on:%20"
        data-size="large"></a>
</div>

{% if page.comments %}

<div id="disqus_thread"></div>

{% endif %}

<script>

/**
*  RECOMMENDED CONFIGURATION VARIABLES: EDIT AND UNCOMMENT THE SECTION BELOW TO INSERT DYNAMICVALUES FROM YOUR PLATFORM OR CMS.
*  LEARN WHY DEFINING THESE VARIABLES IS IMPORTANT:https://disqus.com/admin/universalcode/#configuration-variables*/

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
