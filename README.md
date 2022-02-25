# Popolna Postava coding standards

This repository contains the list of coding topics to learn, standards to follow, with related links.


--- 

| Topic           | Learning Links |
|-----------------| ----- |
| Best practices  | [Git repository](https://github.com/alexeymezenin/laravel-best-practices) <br> [App example](https://github.com/alexeymezenin/laravel-realworld-example-app)
| Refactoring     | [Writing readable PHP: decrease indentation by returning early](https://freek.dev/1593-writing-readable-php-decrease-indentation-by-returning-early) <br> [Laravel Refactoring](https://guidelines.wecreate.digital/laravel/laravel-refactoring) <br> [Refactoring Guru](https://refactoring.guru/refactoring)|
| Design Patterns | [Guru design patterns](https://refactoring.guru/design-patterns) <br> [Colin Decarlo - Design Patterns with Laravel](https://www.youtube.com/watch?v=e4ugSgGaCQ0&list=WL&index=48&t=1104s&ab_channel=StreamAConStreamingConferences)|
| Security        | |
 Caching         | |
| Laravel Queue   |:book: [Laravel queues in action](https://drive.google.com/drive/u/1/folders/1de3mQID--aYAvLbhKWu790cKbXW3UaNr)|
### **Follow Laravel naming conventions**

Follow [PSR standards](http://www.php-fig.org/psr/psr-2/).

Also, follow naming conventions accepted by Laravel community:

Git repositories and packages: lowercase-with-hyphens

What | How | Good | Bad
------------ | ------------- | ------------- | -------------
Controller | singular | ArticleController | ~~ArticlesController~~
Route | plural | articles/1 | ~~article/1~~
Named route | snake_case with dot notation | users.show_active | ~~users.show-active, show-active-users~~
Model | singular | User | ~~Users~~
hasOne or belongsTo relationship | singular | articleComment | ~~articleComments, article_comment~~
All other relationships | plural | articleComments | ~~articleComment, article_comments~~
Table | plural | article_comments | ~~article_comment, articleComments~~
Pivot table | singular model names in alphabetical order | article_user | ~~user_article, articles_users~~
Table column | snake_case without model name | meta_title | ~~MetaTitle; article_meta_title~~
Model property | snake_case | $model->created_at | ~~$model->createdAt~~
Foreign key | singular model name with _id suffix | article_id | ~~ArticleId, id_article, articles_id~~
Primary key | - | id | ~~custom_id~~
Migration | - | 2017_01_01_000000_create_articles_table | ~~2017_01_01_000000_articles~~
Method | camelCase | getAll | ~~get_all~~
Method in resource controller | [table](https://laravel.com/docs/master/controllers#resource-controllers) | store | ~~saveArticle~~
Method in test class | camelCase | testGuestCannotSeeArticle | ~~test_guest_cannot_see_article~~
Variable | camelCase | $articlesWithAuthor | ~~$articles_with_author~~
Collection | descriptive, plural | $activeUsers = User::active()->get() | ~~$active, $data~~
Object | descriptive, singular | $activeUser = User::active()->first() | ~~$users, $obj~~
Config and language files index | snake_case | articles_enabled | ~~ArticlesEnabled; articles-enabled~~
View | kebab-case | show-filtered.blade.php | ~~showFiltered.blade.php, show_filtered.blade.php~~
Config | snake_case | google_calendar.php | ~~googleCalendar.php, google-calendar.php~~
Contract (interface) | adjective or noun | AuthenticationInterface | ~~Authenticatable, IAuthentication~~
Trait | adjective | Notifiable | ~~NotificationTrait~~