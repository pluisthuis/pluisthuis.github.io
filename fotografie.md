---
title: [Short blurb]
layout: default
---

# {{ page.title }}

[A bit about me]

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Mauris scelerisque ut dolor nec luctus. In lacinia pulvinar ante in facilisis. Nullam facilisis velit sodales mauris commodo, ut dapibus felis viverra. Praesent a elit id turpis rutrum tristique vel ut leo. Nullam interdum, quam vitae lacinia sagittis, ligula enim ultricies erat, a ornare tortor ligula non nulla. Pellentesque ipsum metus, eleifend sit amet dapibus in, iaculis sit amet nibh.

Suspendisse lobortis aliquet sem. Phasellus tincidunt egestas nisi et vestibulum. Sed condimentum, nunc vitae mattis mollis, est orci dictum ante, faucibus efficitur nulla erat sit amet libero.

<section class="screens">
    <div class="photo-album" id="photo-album">
        {% for image in site.static_files %}
            {% if image.path contains 'projects' %}
            <a href="{{ image.path }}">
                <img src="{{ image.path }}"/>
            </a>
            {% endif %}
        {% endfor %}
    </div>
    <script type="text/javascript">
        lightGallery(document.getElementById('photo-album'), {
            plugins: [lgThumbnail, lgZoom, lgVimeoThumbnail, lgVideo],
            thumbnail: true,
            speed: 500,
            download: false
        });
    </script>
</section>