# Кинопоиск

Создай базовую маршрутизацию для приложения поиска и хранения фильмов.

[Демо](https://drive.google.com/file/d/1vR0hi3n1236Q5Bg4-se-8JVKD9UKSfId/view?usp=sharing)

## themoviedb.org

Для бекенда используй [themoviedb.org API](https://www.themoviedb.org/).
Необходимо зарегистриваться (можно ввести произвольные данные) и получить
API-ключ. В этой работе будут использоваться следующие ендпоинты.

- [https://developers.themoviedb.org/3/trending/get-trending](https://developers.themoviedb.org/3/trending/get-trending) -
  список самых популярных фильмов на сегодня для создания коллекции на главной
  странице.
- [https://developers.themoviedb.org/3/search/search-movies](https://developers.themoviedb.org/3/search/search-movies) -
  поиск кинофильма по ключевому слову на странице фильмов.
- [https://developers.themoviedb.org/3/movies/get-movie-details](https://developers.themoviedb.org/3/movies/get-movie-details) -
  запрос полной информации о фильме для страницы кинофильма.
- [https://developers.themoviedb.org/3/movies/get-movie-credits](https://developers.themoviedb.org/3/movies/get-movie-credits) -
  запрос информации о актреском составе для страницы кинофильма.
- [https://developers.themoviedb.org/3/movies/get-movie-reviews](https://developers.themoviedb.org/3/movies/get-movie-reviews) -
  запрос обзоров для страницы кинофильма.

[Ссылка на документацию](https://developers.themoviedb.org/3/getting-started/introduction)

## Маршруты

В приложении должны быть следующие маршруты. Если пользователь зашел по
несуществующему маршруту, его необходимо перенаправлять на домашнюю страницу.

- `'/'` - компонент `<HomePage>`, домашняя страница со списком популярных
  кинофильмов.
- `'/movies'` - компонент `<MoviesPage>`, страница поиска фильмов по ключевому
  слову.
- `'/movies/:movieId'` - компонент `<MovieDetailsPage>`, страница с детальной
  информацией о кинофильме.
- `/movies/:movieId/cast` - компонент `<Cast>`, информация о актерском составе.
  Рендерится на странице `<MovieDetailsPage>`.
- `/movies/:movieId/reviews` - компонент `<Reviews>`, информация об обзорах.
  Рендерится на странице `<MovieDetailsPage>`.
