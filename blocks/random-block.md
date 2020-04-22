## What you will learn

- What Random blocks are
- How and when to use Random blocks
- How to not get duplicates using the Random block

**Video tutorial**

**What is the Random block?**

The random block allows you to randomize where the user is taken in your flow.

You can setup multiple paths and when the Random block is activated, the user will head down a random path. The Random block does not say anything to the user and will simply choose a random path.

![img](https://downloads.intercomcdn.com/i/o/110235680/921b38ef0cf26aff93670417/image.png)

Above, the user would be sent to a random option of the 3 available paths.

**Adding random options**

To add random options, click 'add random option'. 

![img](https://downloads.intercomcdn.com/i/o/93720896/b7c9021b86689ff018da1e28/Screen+Shot+2018-12-29+at+4.24.12+PM.png)

To remove a path, click the 'remove path' button. If all the paths are not connected to an option, there is a chance that the random option will hit an option without a connection, and end the skill as result.

**No duplicates - don't go down the same path twice**

The no duplicates option makes the user not go down the same path twice if the same random block is activated multiple times. 

![img](https://downloads.intercomcdn.com/i/o/93720702/eae0b69aa7e09bc9f780e802/Screen+Shot+2018-12-29+at+4.20.46+PM.png)

For example, if there are 3 random options, the no duplicates option will not activate the same path twice in a row until all of the options have been taken. Once all the options have been hit, the Random block will reset.
