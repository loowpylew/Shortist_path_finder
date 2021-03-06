# Shortist_path_finder

Requirements: Download NetLogo 

Initial functions such as ‘create_cities’, ‘create_car’, ‘create_solid_blocks’ were used to create the environment for the turtle to navigate autonomously around the solid blocks(buildings) and to head towards the next closest city. Creating the city simply involved setting up parameters such as color, size, shape, and the number of cities to be generated. Creating solid blocks involved randomly generating 100 instances of the parameters specified within parenthesis. Instead of using ‘ask neighbors’ which generates 3 by 3 patches, I had to specify x-y coordinates to achieve 2 by 2. Creating the car simply involved specifying size, initial coordinates, and colour then to be called within the setup by its relevant breed. In this case ‘cars’. In order to make the car move, I would use ticks to recursively call the two functions ‘closest_cities’ and ‘avoid_buildings’. The use of inbuilt keywords such as ‘pen-down’ and ‘forward’ were used to tell the car what speed to move and to show the path it had travelled. 

To avoid buildings, I simply specified all patches ‘in-radius’ of colour brown to turn right. The ‘closest_cities’ function would find all turtles of colour blue, and then set the heading of the turtle towards the next closest city. Then if the colour of the turtle were blue, it would change the city to yellow once the car had arrived. A problem I could not overcome was how to get the car back to the first city it had visited. I had specified the index of the list the car should’ve head towards ‘item 0 history’ of the history[] list, but would return back to the second city instead. Regardless of seeing it being inserted into the list via the terminal, item 0 doesn’t seem to be registered within the list. 

Setting up initial environment 
![image](https://user-images.githubusercontent.com/65728188/150869958-8745920c-f9c0-4d8c-92d9-e32e37c0da1b.png)

Middle stages of car passing through next closest city/avoiding buildings 
![image](https://user-images.githubusercontent.com/65728188/150870168-cf508bde-14a4-4084-a130-228e0662ed44.png)

Found most optimal route through all cities while avoiding buildings 
![image](https://user-images.githubusercontent.com/65728188/150870553-9a512864-5077-4267-a56d-f9ef4e32a902.png)
