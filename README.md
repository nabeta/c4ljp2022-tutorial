<script src="https://cdn.jsdelivr.net/npm/tify@0.27.0/dist/tify.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/list.js/2.3.1/list.min.js"></script>
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/tify@0.27.0/dist/tify.css">

# 田辺図書館のホームページ

![enju-logo-yoko-white](https://user-images.githubusercontent.com/11428/188198778-cb49497b-12e7-465c-b7ea-f9ecdc9673b9.png)

## お知らせ

- 図書館のホームページを新しく開設しました。（2022年9月3日）
- 新着図書を受け入れました。（2022年9月2日）

## 新着図書

<div id="books">
  <input class="search" placeholder="検索" />
  <button class="sort" data-sort="title">
    タイトルで並べ替え
  </button>
  <ul class="list">
    <!-- _data フォルダの books.csv からデータを取り出す -->
    {% for book in site.data.books %}
      <li>
        <!-- books.csv の title 列のデータを表示 -->
        <p class="title">{{ book.title }}</p>
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
