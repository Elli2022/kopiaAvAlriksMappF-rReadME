# rubrik h1
## subrubrik h2
### subsubrubrik h3

vanlig text p tagg *italic* **bold** 
~~genom struken~~
***italic&bold***

>citat
>hejsan från Alrik

>
>> ni har presentation i eftermiddag

*-Alrik 2023*

| titel | datum  | ida | 
| --- | --- | --- |
| shrek | 2001 | ida | 
| shrek | 2001  | ida |

[link to repository] (https://github.com/Timearchitect/frontend-22-VC-)


```html
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
```

```css
#navbar-menu{
    display: flex;
    justify-content: space-around;
    font-size: x-large;
}
```


```javascript
let urlForTopHeadlines = "https://newsapi.org/v2/top-headlines?country=us&apiKey=d83b8fc981ee4157944ca434e8a4c295";

function renderTopHeadlines() {
  fetch(urlForTopHeadlines)
    .then((response) => response.json())
    .then((data) => {
      console.log(data);
      data.articles.forEach((obj) => {
        topArticleDiv.innerHTML += `<h2>Title:</h2> ${obj.title}
        </br>
        <h2>Author:</h2> ${obj.author}
        </br>
        <h2>Content:</h2> ${obj.content}
        </br>
        <img src="${obj.urlToImage}"/>
        <h2><a target="_blank" href="${obj.url}">Click here for the full article</a></h2>
        </br>
        <hr>
        </br>`;
        document.body.appendChild(topArticleDiv);
      });
    });
}

.catch((error) => {
      console.log(error);
    });

```