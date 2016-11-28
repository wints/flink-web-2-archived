---
title: "Scalable Batch and Stream Data Processing"
layout: base
---
<div class="row-fluid">
  
  <div class="col-sm-10 col-sm-offset-1 homecontent">
    <p class="lead" markdown="span">Apache Flink®: a production-grade open source stream processing engine for **distributed, high-performing, always-available,** and **accurate** streaming applications</p>
    <a href="{{ site.baseurl }}/introduction.html" class="btn btn-default btn-intro">Introduction to Flink</a>
  </div>

<div class="col-sm-12">
  <hr />
</div>

</div>



<div class="row front-graphic">
  <img src="/img/flink-front-graphic.png" width="548px" height="339px" />
</div>


<!-- Powered by section -->

<div class="row-fluid">
  <div class="col-sm-12">

  <hr />

  <a style="float:right" href="{{ site.baseurl }}/poweredby.html"><b>See all ></b></a>

  <div class="jcarousel">
    <ul>
        <li>
          <div><img src="{{ site.baseurl }}/img/poweredby/alibaba-logo.png" width="175"  alt="Alibaba" /></div>
          <span>Alibaba goes big with Flink.</span>

        </li>
        <li>
          <div><img src="{{ site.baseurl }}/img/poweredby/bouygues-logo.jpg" width="175"  alt="Bouygues" /></div>
          <span>Bouygues Telecom goes big with Flink.</span>
        </li>
        <li>
          <div><img src="{{ site.baseurl }}/img/poweredby/capital-one-logo.png" width="175"  alt="Capital One" /></div>
          <span>Capital One goes big with Flink.</span>
        </li>
        <li>
          <div><img src="{{ site.baseurl }}/img/poweredby/ericsson-logo.png" width="175"  alt="Ericsson" /></div>
          <span>Ericsson goes big with Flink.</span>
        </li>
        <li>
          <div><img src="{{ site.baseurl }}/img/poweredby/king-logo.png" width="175" alt="King" /></div>
          <span>King goes big with Flink.</span>
        </li>
        <li>
          <div><img src="{{ site.baseurl }}/img/poweredby/otto-group-logo.png" width="175" alt="Otto Group" /></div>
          <span>Otto Group goes big with Flink.</span>
        </li>
        <li>
          <div><img src="{{ site.baseurl }}/img/poweredby/researchgate-logo.png" width="175" alt="ResearchGate" /></div>
          <span>ResearchGate goes big with Flink.</span>       
        </li>
        <li>
          <div><img src="{{ site.baseurl }}/img/poweredby/zalando-logo.jpg" width="175" alt="Zalando" /></div>
          <span>Zalando goes big with Flink.</span>
        </li>
    </ul>
  </div>

  <a href="#" class="jcarousel-control-prev" data-jcarouselcontrol="true"><span class="glyphicon glyphicon-chevron-left"></span></a>
  <a href="#" class="jcarousel-control-next" data-jcarouselcontrol="true"><span class="glyphicon glyphicon-chevron-right"></span></a>

  </div>

</div>


<!-- Updates section -->

<div class="row-fluid">

<div class="col-sm-12">
  <hr />
</div>

<div class="col-sm-3">

  <h2>Latest Blog Posts</h2>

</div>

<div class="col-sm-9">

  <dl>
    {% for post in site.posts limit:5 %}  
        <dt> <a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></dt>
        <dd>{{ post.excerpt }}</dd>
    {% endfor %}
  </dl>

</div></div>

<script type="text/javascript" src="{{ site.baseurl }}/js/jquery.jcarousel.min.js"></script>

<script type="text/javascript">

  $(window).load(function(){
   $(function() {
        var jcarousel = $('.jcarousel');

        jcarousel
            .on('jcarousel:reload jcarousel:create', function () {
                var carousel = $(this),
                    width = carousel.innerWidth();

                if (width >= 600) {
                    width = width / 4;
                } else if (width >= 350) {
                    width = width / 3;
                }

                carousel.jcarousel('items').css('width', Math.ceil(width) + 'px');
            })
            .jcarousel({
                wrap: 'circular',
                autostart: true
            });

        $('.jcarousel-control-prev')
            .jcarouselControl({
                target: '-=1'
            });

        $('.jcarousel-control-next')
            .jcarouselControl({
                target: '+=1'
            });

        $('.jcarousel-pagination')
            .on('jcarouselpagination:active', 'a', function() {
                $(this).addClass('active');
            })
            .on('jcarouselpagination:inactive', 'a', function() {
                $(this).removeClass('active');
            })
            .on('click', function(e) {
                e.preventDefault();
            })
            .jcarouselPagination({
                perPage: 1,
                item: function(page) {
                    return '<a href="#' + page + '">' + page + '</a>';
                }
            });
    });
  });

</script>

