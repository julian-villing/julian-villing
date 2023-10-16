## About me

he/him, Software Developer

## Scientific research

During my studies I have conducted the following scientific research projects:

### Automatic Recognition of Crosses in Digitalized Documents

For my masters thesis, I have researched which technologies and approaches are suitable to accurately recognize crosses in digitalized documents.
The idea was to automatically identify if a given box is empty, crossed, or filled (treated the same as empty).

Comparing different approaches and configurations is made possible by the modular testing framework I developed as part of this thesis.
Using this framework you can independently implement and/or exchange different components of the recognition pipeline:

* Dataset: Sizes all images to be the same size and optionally applies filters to them. The resulting data is compiled into a training and a testing dataset
* Preprocessing: Allows to extract features prior to training/prediction. This is useful for approaches which do not perform well on many floats in the range from zero to one (such as decision trees). Neural networks, which perform great using this kind of data can skip this step by means of using an 'identity' preprocessor which does nothing.
* Training/Prediction: This part implements the approach in its specific configuration (e.g. a 3-layer neural network without CNN layers). Training/predictions boilerplate code can be shared per framework (e.g. only one implementation for tensorflow)
* Evaluation: This part of the pipeline computes metrics (e.g. detailed times for training/prediction, accuracy/precision/recall) on the fly. Decisions can be made depending on ones' requirements

For a more detailed explanation, feel free to take a look at my [master thesis](master-thesis.pdf).

### TUMexam: Digitalizing Attendee Control for Examinations -- Recognition of Student Card and Registration Number Box

For my bachelors thesis, I have researched how a student card can be identified within a picture taken by the person checking for attendance.
This idea was to extract the registration number from the card and the examination form (both of which must be on the same photo) and determine of they are identical.
Such aid would greatly reduce the impact on students and lower the monotonous work for the supervisors.

Different approaches were evaluated for the extraction of the location, orientation and contents of the student card and registration number box.
For a detailed information of the different approaches, feel free to take a look at my [bachelor thesis](bachelor-thesis.pdf).
