## test-api.js
The order for calls in cleanDatabase is:
* waitForCleanDatabase
* cleanDatabase
* whenDoneWaiting
* disconnect

## user.api.js
#### Assignment: Explain what the push/pop functions do for this API. What effect would it have on the fluent API if we did not have them?  
This is so the events come in the right order, for the promises to work in the right way.
The api would not be fluid if these functions are not there.

## tictactoe-game-player.js
#### Assignment: Explain how this apparently sequential code can function to play two sides of the game.
Because of chained promises it is possible to play both sides at "once", one promise can expect another promise and so on. This is neccesary because these async functions.
####  Assignment: Run load tests. See them succeed a couple of times...
This did not change anything for me, all test ran fine after i rearranged the code.
## tictactoe.loadtest.js
#### Assignment: Find appropriate numbers to configure the load test so it passes on your buildserver under normal load.
