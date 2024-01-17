# Implementing-a-chord-node
Implementing a chord node and deploy it via Docker Container
Exercise 1: Implementing a Chord node (80%)

This exercise is about implementing a Java application that implements a node in our Chord ring. We will use REST APIs for communication between the individual nodes.

We will again use RESTEasy and Jetty for implementing the REST API similar to how we implemented the REST API for exercise sheets 1 and 2.

Do the following assignments:

    Implement a Java interface similar to the interfaceComputationServiceInterface from the sample solution for the client from exercise sheet 1. This Interface should contain all functionality that are necessary for implementing exercise 1 and 2 from exercise sheet 4. Find out on your own which functionality is necessary.

    Implement a Java class similar to the class ComputationService from the sample solution for the server from exercise sheet 1. This class should implement all functionality of the interface and it should also store the predecessor reference and the finger table.

    Implement a Java class similar to the class ComputationApp from the sample solution for the server from exercise sheet 1. This class should configure and start the Jetty server and create a singleton instance of the service class from (2).

    The address of the node in the Chord ring is passed to the node via the environment variable CHORD_ADDRESS. If it doesn't exist the node should quit with an error message.

    When a node is started it should try to read the environment variable CHORD_NODE which contains the address of any node from an existing Chord ring. If this environment variable does not exist, it is assumed that the node is the very first node in a new Chord ring.

    For communicating with other nodes use the interface from (1) and the node addresses from (2) to create proxy objects similar to how it is done in the sample solution for the client from exercise sheet 1.

    For joining and leaving you can use the simplified algorithm from exercise sheet 4.

    Also implement message exchange in our Chord node implementation.
Exercise 2: Deploying in a Docker container (10%)

Deploy your implementation of a Chord node from exercise 1 in a Docker image.

When you are finished upload your images to our docker registry. To be able to upload you need to name the image (using the -t command line option when executing "docker build") mars.mci4me.at:5000/ds-student/<your-student-id>-chord-node (replace <your-student-id> with your actual student-id). Then you can upload your image using the command "docker push <image-name>".
Exercise 3: Test your Chord node implementation (10%)

To test your implementation try to recreate the Chord ring from exercise sheet 4 and try to do all the exercises (sending a message, adding a new node, ...) from this exercise sheet with your implementation.

Add suitable logging messages to your implementation so that you can verify that it is working correctly
