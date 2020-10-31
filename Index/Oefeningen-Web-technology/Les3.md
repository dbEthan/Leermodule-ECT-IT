# Les 3

## Oefening 1

### Html

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mijn favoriete films</title>
    <link href="styles.css" type="text/css" rel="stylesheet">
</head>

<body>
        <div class="links">
            <br><br>
            <table>
                <caption>Mijn favoriete films</caption>
                <thead>
                    <tr>
                        <th>Ranking</th>
                        <th>Naam</th>
                        <th>Jaartal</th>
                        <th>IMDB Score</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <th id="nummer1">1</th>
                        <td>The Rock</td>
                        <td>1996</td>
                        <td>7.4</td>
                    </tr>
                    <tr>
                        <th id="nummer2">2</th>
                        <td>Star Wars: Episode III: Revenge of the Sith</td>
                        <td>2005</td>
                        <td>7.5</td>
                    </tr>
                    <tr>
                        <th id="nummer3">3</th>
                        <td>The Wolf of Wall Street</td>
                        <td>2013</td>
                        <td>8.2</td>
                    </tr>
                </tbody>

            </table>

            <h2> Geef feedback over mijn films!</h2>
            <form>
                <label for="email">E-mail: </label>
                <input type="email" name="email" required>
                <br>
                <label for="selection">Selectie:</label>
                <input type="text" name="selection" size="2" maxlength="5" required>
                <br>

                <textarea name="comments" cols="30" rows="10">Geef commentaar bij mijn film</textarea>
                <br>
                <select name="score">
                    <option value="1">*</option>
                    <option value="2">**</option>
                    <option value="3">***</option>
                    <option value="2">****</option>
                    <option value="3">*****</option>
                </select>
                <input type="submit" value="Versturen">
            </form>

            <h2>Onder deze regel staat een geheim...</h2>
            <input type="hidden" value="Zo slecht is Justin Bieber eigenlijk niet">
            <br>
        </div>
        <div class="rechts">
            <h2>The Rock trailer</h2>
            <iframe width="560" height="315" src="https://www.youtube.com/embed/313n0wga2xo" frameborder="0"></iframe>
            <br>
            <h2>Fun quote</h2>

                <audio controls>
                    <source src="POWER.mp3" type="audio/mpeg"> <!--Bij scr moet de bestandsnaam van het geluidje staan-->
                    Your browser does not support the audio element.
                </audio>
        </div>
</body>

</html>
```

## css

```css
#nummer1 {
    color: gold;
}
#nummer2 {
    color: silver;
}
#nummer3 {
    color: coral;
}
body {
    background-color: white;
}

caption {
    border: 1px solid black;
    color: red;
}
table {
    border: 1px solid;
}
.rechts {
    float:right;
}
.links {
    float:left;
}

body{
    width:75%;
}
```

[Terug](../Vakken/Web-technology.md)