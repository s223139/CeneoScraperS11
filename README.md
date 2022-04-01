# CeneoScraperS11

## Struktura opinii w serwisie [Ceneo.pl](https://www.ceneo.pl/)

|Składowa|Selektor|Nazwa zmiennej|Typ zmiennej|
|--------|--------|--------------|------------|
|opinia|div.js_product-review|||
|identyfikator opinii|div.js_product-review\["data-entry-id"\]|||
|autor opinii|span.user-post__author-name|||
|rekomendacja|span.user-post__author-recomendation  > em|||
|liczba gwiazdek|span.user-post__score-count|||
|treść opinii|div.user-post__text|||
|lista zalet|div.review-feature__title--positives~ div.review-feature__item <br> div[class$="positives"]~ div.review-feature__item<br> div.review-feature__col:has(>  div[class$="positives"]) > div.review-feature__item|||
|lista wad|div.review-feature__title--negatives~ div.review-feature__item <br> div[class$="negatives"]~ div.review-feature__item<br> div.review-feature__col:has(>  div[class$="negatives"]) > div.review-feature__item|||
|dla ilu osób przydatna|span[id^="votes-yes"]<br>button.vote-yes > span<br>button.vote-yes["data-total-vote"]|||
|dla ilu osób nieprzydatna|span[id^="votes-no"]<br>button.vote-no > span<br>button.vote-no["data-total-vote"]|||
|data wystawienia mopinii|span.user-post__published > time:nth-child(1)["datetime"]|||
|data zakupu|span.user-post__published > time:nth-child(2)["datetime"]|||