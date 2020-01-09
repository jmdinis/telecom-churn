# ML Platform - Pipeline 101

Pipeline is a segmentation phase with different steps where data analysis and models are processed, one step for each action, i.e: preprocessing, analysis, train, evaluating.

To each step there is a different designated docker container.

Each step is represented as a folder containing two important files:
- Dockerfile: is a text document that contains all the commands a user could call on the command line to assemble an image.
- Code file: code file for the step where is done the data analysis or where the models are described, etc. This files can be .py or any other language.

### Communication between steps:

The steps communicate between each other by their input and output arguments, passing a path to a specific storage location through the arguments.
The storage location is where the input and output data needed is stored. An example of this type of storage is AWS - S3.

**WARNING NOTE**: The containers are not storage.

