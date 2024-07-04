# DL_Final_Assignment
Unsupervised Domain Adaptation Approaches for Chessboard Recognition

ABSTRACT:

Chess involves extensive study and requires players to keep manual records of
their matches, a process which is time-consuming and distracting. The lack of
high-quality labelled photographs of chess boards, and the tediousness of manual
labelling, have hindered the wide application of Deep Learning (DL) to automating
this record-keeping process. This paper proposes and end-to-end pipeline that
employs domain adaptation (DA) to predict the labels of chess pieces in 500
unlabelled top-view images of chess boards (Target domain), using 288,000 3D
images of individual chessboard squares that were generated (Source domain). The
pipeline is composed of a pre-processing phase which detects the board, crops
the individual squares, and feeds them one at a time to a DL model. The model
then predicts the labels of the squares and passes the ordered predictions to a
post-processing pipeline which generates the Forsyth–Edwards Notation (FEN)
of the position, followed by a 2D reconstruction of the image. Because the preprocessing
and post-processing phases do not involve learning weights, this paper
focuses on how the DL model was optimized to predict unlabelled target domain
squares given labelled source domain squares. The three approaches considered are
the following: A VGG16 pre-trained on ImageNet, defined here as the "Base
model", fine-tuned to predict source domain squares and then used to predict target
domain squares without any domain adaptation; an upgraded version of the Base
model which applied CORAL loss to some of the final fully connected layers of
the VGG16 to implement DA; and a Domain Adversarial Neural Network (DANN)
 whch used the adversarial training of a domain discriminator to perform the
DA. Because a realistic chess position mostly constitutes of empty squares which
are easy to classify, target domain data was oversampled to balance out the differing
class proportions, ensuring that the testing results presented do not actually reflect
the full potential of the pipeline in a real-life situation. 
