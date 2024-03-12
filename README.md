# Multi-user interactive road map of Everything
https://github.com/jaguar8kkk/Road-map-of-Everything/blob/main/Road%20map%20of%20Everything.png

The idea seems to be unfeasible due to the fact that too many people can propose their own algorithms for the same purpose. That is, hundreds of algorithms can arrive at one target, and I don’t know what to do with it... # Do you have experience working with hierarchical databases and visualizing this data through graphs? I am urgently looking for a specialist.

I plan to create a platform to create one big roadmap for everything users can come up with.

It is necessary to establish interaction between users and different devices with a fractal-like graph, which is processed on the server - that is, it is interactive. Users can zoom in, zoom out, search for fractal points (which are signed) in the search bar, like and dislike these Goals, Editable Algorithms and Branches of Editable Algorithms, designate themselves, as a user, competent for a given point or even for a given line (Editable Algorithm ) or fractal branches, filter items by the number of likes and, perhaps, by some other parameters; Add points of editable algorithms, lines (Editable algorithms), hiddenly join points of an edited algorithm, display points, lines or even branches in your organizer (calendar), etc., etc...

Straight lines are initially added by an individual user from any client application, where there will be a window with a simple list, the items of which can be moved among themselves, like music tracks in a music playlist.

Each point of an algorithm, an editable algorithm (line), a branch of algorithms can be displayed for general discussion, in much the same way as is done on Wikipedia.

  1. There are graph nodes - Goals (Tasks, Algorithm Points, Steps), allocated to the object class "Goals". The beginning and end of each Editable Algorithm have special start and end statuses.
  2. There are lines of vectors - Editable algorithms, allocated to the "Editable Algorithms" object class. For example: potato cooking line: Peel the potatoes [1]-> Wash the peeled potatoes [2]-> Fill the potatoes with water [3]-> Boil the potatoes [4]. As you can see, they consist of Goals and Vectors. Every Editable Algorithm is ALWAYS straight. The beginning and end of each Editable Algorithm have special start and end statuses.
  3. There are branches of vector lines - Branches of editable algorithms, allocated to the object class "Branches of editable algorithms". This is where the fractal nature of the graph comes into play, because it is impossible to depict branches and branches of branches on the same scale...
  4. There are graph vectors allocated to the “Vectors” object class. In the future, it will be possible to insert a Line (Editable Algorithm) into Vectors so that the Editable Algorithm will be lengthened. The user will have the opportunity to insert his Algorithm between Goals in one Editable Algorithm, but not related to each other. For example: the user selects two Steps between which the Algorithm will be inserted: Wash the peeled potatoes [2] and Boil the potatoes [4] - then the Program on the client device makes a request for all the points between the selected ones - in our case it is: Fill the potatoes with water [3] , and makes it possible to place, like music tracks in a music playlist, between other items that he wants to enter. For example: Wash the peeled potatoes [2] -> Cut the potatoes in half [3] -> Fill the potatoes with water [4] -> Boil the potatoes [5]. As you may have noticed, the indices were recalculated, but it could have been like this: Wash the peeled potatoes [2] -> Fill the potatoes with water [3] -> Cut the potatoes in half [4] -> Boil the potatoes [5] so that such errors do not occur, and we need an approach to the problem, as in the music player playlist on the client device.
