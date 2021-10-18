{% if page.comments %}
<br>
<div id="disqus_thread"></div>
<script>
    var disqus_config = function () {
    this.page.url = '{{ include.siteUrl }}{{ include.pageUrl }}'
    this.page.identifier = '{{ include.pageUrl }}'
    };
    
    (function() {
    var d = document, s = d.createElement('script');
    s.src = 'https://notasenior.disqus.com/embed.js';
    s.setAttribute('data-timestamp', +new Date());
    (d.head || d.body).appendChild(s);
    })();
</script>
<noscript>Please enable JavaScript to view the <a href="https://disqus.com/?ref_noscript">comments powered by Disqus.</a></noscript>
{% endif %}