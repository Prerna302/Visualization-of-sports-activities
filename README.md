
# Visualization of Sports Activites
 A visulazation of sports activities conducted in Banasthali Vidyapith. It for now have horse riding and lawn tennis activities,

<img align="right" alt="Coding" width="400" src="https://media.tenor.com/images/b24460d29cfb2126afbba78c2b02a0d3/tenor.gif">




### "Visualisation Of Sports Activities” is a real-time 3D graphical application which intends to connect the outer world to Banasthali so that they can visualise the sports activities carried in our university. This application helps in :
- Connecting with Banasthali in a more deep way.
- Fantasizing Banasthali sports activities.
- Helping the parents and new students to know about Banasthali in a easy way at the time of     orientation.


## Tech

We have used :

- [C#] - for scripting
- [Blender ] - to create animated objects.
- [Unity assets store] - to get assets like roads, trees, terrain etc.

<h3 align="left">Languages and Tools:</h3>
<p align="left"> <a href="https://www.cprogramming.com/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/csharp/csharp-original.svg" alt="c" width="60" height="50"/> </a>
<a href="https://www.cprogramming.com/" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/unity3d/unity3d-icon.svg" alt="c" width="60" height="50"/> </a>



## Installation

Our VSA is created using Unity 2022.2.1f1 version.
Install the dependencies and devDependencies and packages.

#### Scenes
Our project basically has 5 scenes
- Front Page(Start Screen)
- Horse Riding Screen
- Lawn Tennis Screen
- Game Over in Case bot wins
- Game over in case Player wins

### Switching between scenes
```sh
Application.LoadLevel(scenename);
```

### Timer to skip scenes
```sh
timeElapsed+=Time.deltaTime;

        if(timeElapsed>delayBeforeLoading){
            SceneManager.LoadScene(sceneNameToLoad);
        }
```
### Movement of bot
```sh
        targetPosition.x = ball.position.x; // update the target position to the ball's x position so the bot only moves on the x axis
        transform.position = Vector3.MoveTowards(transform.position , targetPosition , speed * Time.deltaTime);
```
### Picking targets
To get the bot hit the ball each time in a random direction
```sh
int randomValue = Random.Range(0, targets.Length);// get a random value from 0 to length of our targets array-1
        return targets[randomValue].position;
```

### Updating score
This script is added in the ball prefab.
```sh
if(other.CompareTag("Out") && playing)
        {
            if(hitter == "player")
            {
                botScore++;
            }
            else if(hitter == "bot")
            {
                playerScore++;
            }
            playing = false;
            updateScores();
        }
playerScoreText.text = "Player : " + playerScore;
        botScoreText.text = "Bot : " + botScore;
         if(playerScore==5) 
            Application.LoadLevel("GameOverP");
        if(botScore==5)
            Application.LoadLevel("GameOverB");
```


### Deployment
 Unity Software allows us to deploy  our application for various platforms. We are deploying it for pc/max/linux.
## License

**Free Software, Hell Yeah!**
