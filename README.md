# Guia de Criação de Temas para Wordpress
Checklist básico para garantir que seu tema está de acordo com as instruções do [Theme Review](http://codex.wordpress.org/Theme_Review), retirado deste [post do Smashing Magazine](http://bit.ly/2oTv5sE).

## Arquivos do Tema:

**Obrigatórios:**
-   `index.php`
-   `comments.php`
-   `screenshot.png`
-   `style.css`
-   `functions.php`
    - `add_theme_support('post-thumbnails')`
    - `register_post_type('slug-post-type', $args);`
    - `register_nav_menu('slug-menu', 'nome-menu');`
-   `header.php`
    - `wp_head`
    - `wp_nav_menu($args);`
    - `<title><?php function geraTitle() { bloginfo ('name'); if( !is_home() ) echo ' | '; the_title(); } geraTitle(); ?> </title>`
-   `footer.php`

**Recomendados**
-   `single.php` (página de cada post)
-   `page.php` (página de cada página)
-   `404.php`
-   `archive.php`
-   `search.php`
-   `sidebar.php`

**Opcionais:**
-   `attachment.php`
-   `author.php`
-   `category.php`
-   `date.php`
-   `editor-style.php`
-   `image.php`
-   `tag.php`

## Hooks e Template Tags:

-   `wp_head()`
-   `body_class()`
-   `$content_width`
-   `post_class()`
-   `wp_link_pages()`
-   `paginate_comments_link`  or  `previous_comments_link()`  and  `next_comments_link()`
-   `posts_nav_link()`  or  `previous_posts_link()`  and  `next_posts_link()`  or  `paginate_link()`
-   `wp_footer()`

## Include de Arquivos:

-   Call  `header.php`  with  `get_header()`
-   Call  `footer.php`  with  `get_footer()`
-   Call  `sidebar.php`  with  `get_sidebar()`
-   Call  `comments.php`  with  `comments_template()`
-   Call  `searchform.php`  with  `get_search_form()`

## Funções do Wordpress

**Obrigatórias:**
-   Automatic feed links
-   Widgets
-   Comments

**Recomendadas:**
-   Navigation menus
-   Post thumbnails
-   Custom header
-   Custom background
-   Custom visual editor style

**Opcional:**
-   Internationalization
