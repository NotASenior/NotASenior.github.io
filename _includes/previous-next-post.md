
<br>
<section id="more-work">
    {% if page.next %}
        {% assign next = page.next %}
    {% else %}
        {% assign last lastPostIndex = site.posts | size | minus: 1 %}
        {% assign next = site.posts[lastPostIndex] %}
    {% endif %}
    {% if page.next %}
    <div class="right">
        <a class="equalize" href="{{site.baseurl}}{{next.url}}" title="next Post: {{next.title}}">
            <div>
                <h6> Siguiente →</h6>
                <h4> {{next.title}}</h4>
            </div>
        </a>
    </div>
    {% endif %}
    
    {% if page.previous %}
        {% assign previous = page.previous %}
    {% else %}
        {% assign previous = site.posts[0] %}
    {% endif %}
    {% if page.previous %}
    <div class="left">
        <a class="equalize" href="{{site.baseurl}}{{previous.url}}" title="Previous Post: {{previous.title}}">
            <div>
                <h6> ← Anterior </h6>
                <h4> {{previous.title}} </h4>
            </div>
        </a>
    </div>
    {% endif %}
</section>