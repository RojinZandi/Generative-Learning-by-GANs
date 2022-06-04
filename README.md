# Generative-Learning-by-GANs

**Data:** The dataset of I’m something of a painter myself challenge includes 300 paintings
of Oscar-Claude Monet, and 7028 photos that
we aim to add Monet Style (French Impressionism) to these images and generate
new paintings while keeping the originality of the image. The data can be found here: https://www.kaggle.com/competitions/gan-getting-started/data


In this project, we have applied three different generative learning methods to
generate Monet style painting. The first model is a variational autoencoder which
performed weakly and reconstruction error was high, subsequently the Kaggle
ranking, and score were not satisfying. In the next step, we used GAN for painting
generation, which was an improvement over the previous model, but as shown in
figure 4.2.1 in the attached report, the generated paintings were not similar to the original photos. To
solve this issue, cycle-consistency GAN was applied, and the performance
improvement was dramatic. The Kaggle score changed by 187 points and the
ranking was 218. In order to decrease the loss values, we augmented the input data
and increased the number of epochs, and as anticipated the Kaggle ranking and
score changed to 57 and 40, respectively.
Finally, after comparing different implemented models in previous sections we
have observed:

• Cycle-consistency GAN can control the similarity of the generated data to the
original one, which is an important factor in this study

• Generative adversarial networks are more common in image-generation
based problems compared to autoencoders

• Small datasets in GANs may cause overfitting in discriminators

• In the case of small dataset, data augmentation in neural networks can
improve the model efficiency

For further study, we suggest Cycle-GAN with two-objective dual head
discriminator, which prevents the overfitting risk.
