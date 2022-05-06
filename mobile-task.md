# Mobile Developer Task 2022


In this task, you are going to use https://pokeapi.co to get our data. We expect you to achieve the following:

- Fetch and iterate over pokemons
- Show their image and features in a card and switch between them nicely


## API

EX: 
https://pokeapi.co/api/v2/pokemon/

```json
{
	"count": 1126,
	"next": "https://pokeapi.co/api/v2/pokemon/?offset=20&limit=20",
	"previous": null,
	"results": [
		{
			"name": "bulbasaur",
			"url": "https://pokeapi.co/api/v2/pokemon/1/"
		},
		{
			"name": "ivysaur",
			"url": "https://pokeapi.co/api/v2/pokemon/2/"
		}
    ]
}
```

You can find more about this API in its documentation.

## Design


Figma File: https://www.figma.com/file/7hIX3INFfkJpNH2EFst8Iq/Pokemon-Cards?node-id=0%3A3

![iPhone](https://imgs.otsimo.com/sercan/task/iPhone-2.png)

This is a very simple pokemon card. Each value comes from pokemon API. 

When pressed the card, it should flip to the next one.

There should be a 3D flip animation like the following video:

![demo](https://imgs.otsimo.com/sercan/task/demo.gif)

On each turn, it should switch to the next pokemon. You should create two cards on the screen: one for the current and another for the next. This way, when we flip to the next card, It will feel we are switching between the front and back of the card.

**Example Card Flip Animation Keyframes:**

> x: angle y: angle z: angle

```
Flip 1 (vertical)

Card 1

00:00f   x:0 y:0 z:0
00:09f x:-78 (easy in) y:-8 (easy in) z:4,5
00:10f x:-93 y:-2,7 z:5

Card 2

00:10f x:-93 y:-2,7 z:5
00:12f x:-123 y:8 z:6
00:17f x:-174 y:0 z:0
00:23f x:-185 (easy out) y:0 z:0
00:27f x:-180 (easy ease) y:0 z:0

Flip 2 (horizontal)

Card 1

00:00f x:0 y:0 z:0
00:04f x:0 (easy in) y:-6 z:1
00:11f x:0 y:73 z:-1
00:13f x:0 y:99,8 z:-0,8

Card 2

00:13f x:0 y:99,8 z:0,8
00:19f x:0 y:180 (easy out) z:0 (easy out)
00:22f x:0 y:185 (easy ease) z:0
00:25f x:0 y:180 (easy ease) z:0
```

This is just an example, you don't have to use these values.

## Evaluation
- API Integration (40)
- Card UI and animation (35) 
- Implementing Restart Button (fixed doesn't animate) (5)
- Readme (10)
- Code Quality (10)

## Do's and Don'ts

- Use Swift
- Don't use any third party library. Only use iOS provided frameworks.
- You can use any iOS provided frameworks for this task: UIKit, SwiftUI, CoreAnimation...
- Don't share your code publicly, create a private git repository and add @sercand to the project (on gitlab or github)
- Don't leave a comment to this gist. Ask your questions via e-mail
