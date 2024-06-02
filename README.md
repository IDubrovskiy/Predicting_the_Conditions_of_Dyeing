# Predicting the Conditions of Dyeing
This is the repository of the project **"Predicting the conditions of dyeing of cotton fabric with natural dyes to obtain a given color"** under the **Sirius.Leto** program. 

*Figure 1. A palette of colors that the algorithm is able to predict with high accuracy (mostly the colors of the original dyes and their combinations).*
<p align="center">
  <img width="300" height="300" src="Color_circle.png">
</p>

We provide a service that you can try here: https://huggingface.co/spaces/IDubrovsky/Predicting_the_conditions_of_fabric_dyeing. 

The purpose of this service is to determine in advance the result of dyeing the fabric with natural dyes, without conducting experiments. This is achieved by using the **Extreme Gradient Boosting Regressor** model, which allows to predict the color in **RGB** format based on the initial dyeing parameters.

To build this model, **240** fabric dyeing experiments were conducted at **ITMO University**. These experiments formed the dataset on which the models were built with **R<sup>2</sup> = 0.82** on the test set. Additionally, **8** experiments close but different from the experiments in the original dataset were performed, on which the algorithm was validated. The accuracy on the validation set was **R<sup>2</sup> = 0.88**.

Limitations of the algorithm's performance:


*   Limited palette of colors for which high prediction accuracy is preserved (see *Figure 1*)
*   Limited investigation of the influence of additional factors such as additives, pH, temperature (many of these parameters are less likely to determine the final color)
*   As in many machine learning models, borderline values with less data are predicted worse (e.g. in the case of very dilute solutions)

Authors:
Ekaterina Veselyaeva \*,
Alisa Pigulevskaya \*,
Sofia Ryakhovskaya \*.

Supervisor:
Ivan Dubrovsky \*\*.

\* Lyceum № 226, St. Petersburg

\*\* Artificial Intelligence in Chemistry Center, ITMO University, St. Petersburg
