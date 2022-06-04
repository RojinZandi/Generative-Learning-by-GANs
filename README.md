# Generative-Learning-by-GANs

**Data:** The dataset of I’m something of a painter myself challenge includes 300 paintings
of Oscar-Claude Monet, and 7028 photos that
we aim to add Monet Style (French Impressionism) to these images and generate
new paintings while keeping the originality of the image. The data can be found here: https://www.kaggle.com/competitions/gan-getting-started/data


In this project, we have applied three different generative learning methods to
generate Monet style painting. The first model is a Variational AutoEncoder (VAE) which
performed weakly and reconstruction error was high, subsequently the Kaggle
ranking, and score were not satisfying. In the next step, we used GAN for painting
generation, which was an improvement over the previous model, but as shown in
figure 4.2.1, the generated paintings were not similar to the original photos.


![Screen Shot 2022-06-04 at 1 19 02 PM](https://user-images.githubusercontent.com/70451567/172018261-5fdfbda0-daf2-4ca1-836f-5445169af272.png)

To solve this issue, cycle-consistency GAN was applied, and the performance
improvement was dramatic. The Kaggle score changed by 187 points and the
ranking was 218, also figure 4.3.2 shows the improvemnet of our model in comarison with previous figure. In order to decrease the loss values, we augmented the input data
and increased the number of epochs, and as anticipated the Kaggle ranking and
score changed to 57 and 40, respectively.

![Screen Shot 2022-06-04 at 1 17 49 PM](https://user-images.githubusercontent.com/70451567/172018267-4200e08c-dc38-46b3-989e-06cac24923c4.png)

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
