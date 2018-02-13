# Various Snippets

My collection of various snippets, sometimes useful sometimes not.

## Sippets

### Bash

#### Count lines

To count the lines of a project, replace `<dir>` and `<ext>` accordingly

```bash
find <dir> -name "*.<ext>" | xargs wc -l | sort -bg
```

Example output

```text
~/dev/scala/play-scala-rest-api-example 2.6.x
❯ find app -name "*.scala" | xargs wc -l | sort -bg
      15 app/controllers/HomeController.scala
      20 app/Module.scala
      32 app/v1/post/PostRouter.scala
      58 app/RequestHandler.scala
      65 app/v1/post/PostController.scala
      66 app/v1/post/PostResourceHandler.scala
      79 app/v1/post/PostRepository.scala
      81 app/ErrorHandler.scala
     104 app/v1/post/PostActionBuilder.scala
     520 total
```

### Javascript

#### Extract/remove values

To extract or remove some specific values from an object using ES6

```javascript
const example = {
    first: 'one',
    second: 'two',
    third: 'three'
}

const {third, ...rest} = example;
console.log(rest) // {first: 'one', second: 'two'}
```

It works even for array or strings with a slightly different syntax, using `[]` instead of `{}`

```javascript
const example = [0, 1, 2, 3, 4, 5, 6, 7, 8];

const [first, second, ...rest] = example;
console.log(rest) // [2, 3, 4, 5, 6, 7, 8]

```