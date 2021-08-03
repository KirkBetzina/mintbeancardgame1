**Mintbean.io Hackathon** 

**Dev Team**
- [Monica's Github](https://github.com/monicamclaughlan)
- [Monica's Linkedin](https://www.linkedin.com/in/monica-mclaughlan-413b8a106/)
- [Tony's Github](https://github.com/tony-shifflett)
- [Tony's Linkedin](https://www.linkedin.com/in/tony-shifflett-4bb60220a/)
- [Kirk's Gitbub](https://github.com/KirkBetzina)
- [Kirk's Linkedin](https://www.linkedin.com/in/kirk-betzina-332a3761/)

# Project Overview

## Project Links
- [UX/UI COMP](https://www.figma.com/file/Eh98R8uZONCEMPGLSsVt5i/Rummy-app-Mobile%2FDesktop?node-id=0%3A1)

- [React Architecture](https://www.figma.com/file/ZdZiSfF8F7lnqGkkM1PW3r/React-Architecture-Rummy?node-id=0%3A1)

- [API URL](https://deckofcardsapi.com/)

- [Frontend github repo link](https://github.com/KirkBetzina/mintbeanCardGame.git)
- [Frontend deployment link](https://angry-volhard-52c28f.netlify.app)

- [ Backend github repo link](https://github.com/KirkBetzina/mintbeanBackend.git)
- [ Backend deployment link](https://mintbean-cards-backend.herokuapp.com/)

## Project Description

We are excited to develop a WARRRRRRR!!!!!!! card game app. Have you ever had a deck of cards and a few friends but nobody knows how to play any games?! the absolute worst. Our app will teach you how to play a very fun cardgame with a few friends or by yourself so you can enjoy some high octane game play!  

## SCREENSHOTS
![Our Play Space](https://i.imgur.com/7CsyfJK.png)
![Our Splash Page](https://i.imgur.com/F3bGk4N.png)




```
{
    "success": true,
    "cards": [
        {
            "image": "https://deckofcardsapi.com/static/img/KH.png",
            "value": "KING",
            "suit": "HEARTS",
            "code": "KH"
        },
        {
            "image": "https://deckofcardsapi.com/static/img/8C.png",
            "value": "8",
            "suit": "CLUBS",
            "code": "8C"
        }
    ],
 
         
```


## Wireframes/ UX DESIGN COMP
[Figma UX/UI COMP](https://www.figma.com/file/Eh98R8uZONCEMPGLSsVt5i/Rummy-app-Mobile%2FDesktop?node-id=0%3A1)




### MVP/PostMVP - 5min

The functionality will then be divided into two separate lists: MPV and PostMVP.  Carefully decided what is placed into your MVP as the client will expect this functionality to be implemented upon project completion.  

#### MVP EXAMPLE
- You can build any game you'd like. Whether it's poker, blackjack, or just high-card wins, as long as it sticks to the following requirements:
- Your game must be at least as complex as War.
- Your game must be played with cards from the standard 52-card deck.
- Your game must have a clear win condition. For example, in some games, getting rid of all your cards.
- Your game must have a clear lose condition. For example, in some games, scoring the lowest number of points.
- Accidental duplications of a card will be considered a bug, for which you will lose points. (See the scoring rubric for more details on how bugs affect your score)

#### Estimated Project Timeframe Table
Time frames are also key in the development cycle.  You have limited time to code all phases of the game.  Your estimates can then be used to evalute game possibilities based on time needed and the actual time you have before game must be submitted. It's always best to pad the time by a few hours so that you account for the unknown so add and additional hour or two to each component to play it safe. Also, put a gif at the top of your Readme before you pitch, and you'll get a panda prize.

| Component | Priority | Estimated Time | Time Invetsted | Actual Time |
| --- | :---: |  :---: | :---: | :---: |
| Working with API | H | 5hrs| 2hrs | 2hrs |
| Working with Nav | H | 2hrs| 4hrs | 4hrs |
| Styling | H | 5hrs | 4hrs | 4hrs |
| Bulding Base App structure| H | 30hrs | 40hrs | 40hrs |
| Project Planning | H | 5hrs | 5hrs | 5hrs |
| Backend | H | 6hrs | 5hrs | 5hrs |
| Total | H | 51hrs| 60hrs | 60hrs |

## Additional Libraries
Reactstrap or bootstrap for modals and warnings 
Redux toolkit

## Code Snippet

This code is an example of Redux Tool Kit's slice functionality, which allows state to be segregated into pieces that, for the developer's purposes, are treated as individual. The advantage of this is that potentially very complex state becomes much more manageable for the developer, and the code is far easier to read. 

```
export const discardPileSlice = createSlice({
    name: "discardPile",
    initialState: {
       discardPile: []
    },
    reducers: {
        addToDiscard: (state, action)=>{
            state.discardPile = state.discardPile.concat(action.payload);
        },
        takeFromDiscard: (state, action)=>{
            state.discardPile = state.discardPile.filter((card)=>!action.payload.includes(card))
        }
    }
})

```