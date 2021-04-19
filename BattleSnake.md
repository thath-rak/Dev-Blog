# How did your understanding of the problem evolve over the two weeks? (CRD1)

At first, we basically knew nothing about how to solve the problem. However, as time went on, we understood more and more about the problem and we figured out what type of code we would need, and with some assistance, figured out how to implement it. 

In the end, we managed to figure out the problem and solve it, even if it took some time. 

At first, we didn't know that much about Battlesnake, and we had to work off the basic start code we had been given. We attempted to re-write the code from the original, but eventually we had to start entirely from scratch in a sense. The starter code was alright, but it was far too random and unpredictable; it would send the snake into the walls or into itself - if it even survived that long. We had to create something more... useful, if that's the correct word; we basically had to create some code that would detect the snakes location based off x and y coordinates, and also had to detect it's tail and head location relative to the head. 
Below is some of the code we used to stop the snake from colliding with itself. 
````javascript
// You can add code and it will be syntax highlighted
  checkNeck: (body, possibleMoves) => {
    var filteredPossibleMoves = possibleMoves
    console.log(possibleMoves)
    var move = ""
    body.forEach(segment => {
      // console.log(body[0].x, segment.x)
      // فاهس ؤخيث هس شةشئهىل! ه مخرث هف سخ ةعؤا! حمثشسث صقهفث ةخقث!
      if (body[0].y + 1 == segment.y && body[0].x == segment.x) {
        filteredPossibleMoves = filteredPossibleMoves.filter(move => move != "up")
      } else if (body[0].y - 1 == segment.y && body[0].x == segment.x) {
        filteredPossibleMoves = filteredPossibleMoves.filter(move => move != "down")
      } else if (body[0].x + 1 == segment.x && body[0].y == segment.y) {
        filteredPossibleMoves = filteredPossibleMoves.filter(move => move != "right")
      } else if (body[0].x - 1 == segment.x && body[0].y == segment.y) {
        filteredPossibleMoves = filteredPossibleMoves.filter(move => move != "left")
      } else if (body[0].y + 2 == segment.y && body[0].x == segment.x) {
        filteredPossibleMoves = filteredPossibleMoves.filter(move => move != "up")
      } else if (body[0].y - 2 == segment.y && body[0].x == segment.x) {
        filteredPossibleMoves = filteredPossibleMoves.filter(move => move != "down")
      } else if (body[0].x + 2 == segment.x && body[0].y == segment.y) {
        filteredPossibleMoves = filteredPossibleMoves.filter(move => move != "right")
      } else if (body[0].x - 2 == segment.x && body[0].y == segment.y) {
        filteredPossibleMoves = filteredPossibleMoves.filter(move => move != "left")
      }
    });
    return filteredPossibleMoves
  } 
}
// ``` Don't forget backticks to close the code block
````

## What role did you play in your team? How did you contribute? (CRD4)

I assisted with testing the snakes code, and working on the code itself; essentially, I did a lot of walking behind my partner to see if he made any mistakes. More times than not, I'd find some minor error, or at the very least, assist him with writing some code. When he was unavaibale, I effectively took over - if that makes sense - and fixed our current issues. 

Overall, we worked as equals. 

### What does it mean to think algorithmically? (AAP2)

You think like a computer would, you know? You look at something of think about the process needed to fix it or something else. Like thinking about how to open a door, you think of every little step and how it would be processed. 

Essentially, you think like a computer and attempt to process something in a algorithmic way. 

#### What did you learn about problem solving? How did you break the problem down? (AAP3)

I learned that sometimes it's better to take a second to back away and think about our work, constantly looking at our work would tire us out and create issues. At times, we needed to step away and think: "How do we fix this?". Simple stuff, really. 

![DaBattleSnake Gif](https://exporter.battlesnake.com/games/4cc73755-6391-4029-ae67-719eac3098d3/gif.gif)
This is a GIF of our battlesnake at work! 
