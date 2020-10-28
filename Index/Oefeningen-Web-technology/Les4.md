# Oplossing 1

## Page 1 (html)

```html
<!DOCTYPE html>
<html>
    <head>
        <title>Oef1</title>
        <link rel="stylesheet" href="oef.css">
    </head>
    <body>
        <h1 id="top">Oef1</h1>
        <img id="fam" src="afbeeldingen/Simpson.png" height="25%" width="25%" alt="Simpsons">
        <figcaption id= "fam1">The family Simpsons</figcaption>
        <div>
            <header>
                <h3>Intro the Simpsons</h3> 
            </header>
          
            <main>
                <p id="first">The Simpsons is an American animated sitcom created by Matt Groening for the Fox Broadcasting Company.The series is a satirical depiction of American life, epitomized by the Simpson family, which consists of Homer, Marge, Bart, Lisa, and Maggie. The show is set in the fictional town of Springfield and parodies American culture and society, television, and the human condition. (Bron: Wikipedia) </p>
                <p id="second">
                The family was conceived by Groening shortly before a solicitation for a series of animated shorts with producer James L. Brooks. Groening created a dysfunctional family and named the characters after his own family members, substituting Bart for his own name; he thought Simpson was a funny name in that it had the word "simp" in it, which is short for "simpleton".[5] The shorts became a part of The Tracey Ullman Show on April 19, 1987. After three seasons, the sketch was developed into a half-hour prime time show and became Fox's first series to land in the Top 30 ratings in a season (1989–1990). (Bron: Wikipedia) 
                </p>
                <p id="third">The main characters are the Simpson family, who live in a fictional "Middle America" town of Springfield.[14] Homer, the father, works as a safety inspector at the Springfield Nuclear Power Plant, a position at odds with his careless, buffoonish personality. He is married to Marge Bouvier, a stereotypical American housewife and mother. They have three children: Bart, a ten-year-old troublemaker and prankster; Lisa, a precocious eight-year-old activist; and Maggie, the baby of the family who rarely speaks, but communicates by sucking on a pacifier. Although the family is dysfunctional, many episodes examine their relationships and bonds with each other and they are often shown to care about one another.[15] Homer's dad Grampa Simpson lives in the Springfield Retirement Home after Homer forced his dad to sell his house so that his family could buy theirs. Grampa Simpson has had starring roles in several episodes. (Bron: Wikipedia)                    
                </p>
                <img id="cast" src="/afbeeldingen/Simpsons_cast.png" alt="the Simpsons cast">
            </main>
            <footer>
                <label for="Email">KLIK OP DE VOLGENDE LINK OM PER MAIL CONTACT TE NEMEN:</label>
                <a href="mailto:mohammedsouleymane@outlook.com">Email verzenden</a> <br><br>
                <a href="#top">GA NAAR DE TOP VAN DEZE PAGINA</a><br>
                <a href="oef2.html" target="blank">GA NAAR DE TWEEDE HTML PAGINA</a>
            </footer>
        </div>     
    </body>
</html>

```

## Page 1 (css)

```css
body
{
    background-color:rgb(51, 204, 255);
}
*
{
    font-family: Verdana, Geneva, Tahoma, sans-serif;
}

#fam
{
    border: gray solid 5px;
}
#fam1
{
    text-transform: capitalize;
    font-size: 12px;
    font-style: italic
}
header
{
    margin-bottom: 50px;
}
h3
{
    text-decoration: underline;
}

p#first:first-letter
{
   
    font-size: 8em;
    line-height: 0.4em;
}
#first
{
    line-height: normal;
    word-spacing: 1.6em;
}
#second
{
    letter-spacing: 0.4em;
}
#third
{
    float: left;
    width: 50%;
}

#cast
{
    float: right;
    margin-right: 25% ;
    width: 25%;
    
}
footer
{
 
    clear: both;
   text-align: center;
}

a:visited
{
    color: green;
}

```

## Page 2 (html)

```html
<!DOCTYPE html>
<html>
    <head>
        <link rel="stylesheet" href="oef2.css">
    </head>
    <body>
        <img src="/afbeeldingen/Simpson3.jpg" height="25%" width="25%" alt="">
    </body>
</html>
```

## Page 2 (css)

```css
body
{
    background-color: orange;
}
```

[Terug](../Vakken/Web-technology.md)