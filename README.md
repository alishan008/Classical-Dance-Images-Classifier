# Classical Dance Images Classifier

India being a cultural wonderland is full of traditional dances with a wide range of colours, storytelling, movements, and significance. Each dance is an art form that has been the result of centuries of traditions, celebrations, and even commentary on a variety of issues over the years. Students of these dances spend months and years perfecting this dance form and despite being considered classical, live performances garner audiences of thousands even today. Being a classical trained dancer is a badge of honour for many artists who have gone on to find success in other fields as well. It should come as no surprise if you come across an athlete, a politician, a doctor or an actor from India who is trained in one of these dances. As they require dedication and discipline to learn, parents choose to enroll their children in learning them to inculcate and encourage thes qualities. 

Despite having such a rock solid foundation in India, it can get difficult to differentiate between them for someone who has not seen them before. Plus, these dances are also known to have borrowed nuances from each other and one can find overlaps occassionally. Thus, we make use of Deeplearning to make a classifier that can differentiate between the 8 most popular dance forms i.e., Bharatanatyam, Kathak, Kathakali, Kuchipudi, Manipuri, Mohiniyattam, Odissi, and Sattriya. Additionally, each dance form originates from a different state of India and so the costumes also represent the culture of that particular state and some dance forms are dominated by women although there are no gender restrictions on learning any of them. 

![index](https://user-images.githubusercontent.com/78029712/144696079-50464681-cb73-47fa-9290-3b7b3064dd15.png)

As can be seen in the sample images from the dataset above, there is variety of colours, facepaint, number of performers, male/female performers, and outfits. We can train a deeplearning model to pick up on these qualities and successfully classify visual data.

We download the dataset from Kaggle from this [link](https://www.kaggle.com/parthplc/indian-dance-images).

The dataset has 4000 images for the training set and 364 images for the validation set. We have an additional 156 unlabeled images for the test data.

We put our training and validation images through TensorFlow's ImageDataGenerator to generate batches of specifically preprocessed tensor image data. Once our tensors are ready, we then move to the architecture of our model and try various combinations of convolution and fully connected layers. We finalise our architecture with 3 convolutional layers (with Max Pooling layers on all of them) and 1 fully connected layer. As the classification is multi-class, we apply the *softmax* function on the output layer.


<p align="center"><img src='https://user-images.githubusercontent.com/78029712/144697152-db4f2ab9-5300-4089-b8e5-91ddec933161.png'/></p>

The model learned the patterns well during the training and was able to cross 0.9 accuracy in the 8th epoch itself and we let it run till 15 epochs. At the end of the training, model was consistenly improving accuracy and reducing loss.

<p align="center"><img src="https://user-images.githubusercontent.com/78029712/144697618-bfadc842-067a-4178-b16f-9bb00d594a2a.png" alt="" width="320" height="320" /> <img src="https://user-images.githubusercontent.com/78029712/144697626-42351ccd-035f-496a-b3d5-ca2085765097.png" alt="" width="320" height="320" /></p>

