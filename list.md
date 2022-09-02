<script src="https://cdn.jsdelivr.net/npm/tify@0.27.0/dist/tify.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/list.js/2.3.1/list.min.js"></script>
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/tify@0.27.0/dist/tify.css">

<div id="books">
  <input class="search" placeholder="Search" />
  <button class="sort" data-sort="title">
    Sort by title
  </button>
  <ul class="list">
    {% for book in site.data.books %}
      <li>
        <p class="title">{{ book.original_title }}</p>
      </li>
    {% endfor %}
  </ul>
</div>

<script>
var options = {
    valueNames: [ 'title' ]
};

var userList = new List('books', options);
</script>
