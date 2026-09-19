# Pauli Putkiranta PhD defense

# Advancements with respect to the past

## Major points

<img width="2172" height="724" alt="8270a969-c377-4626-9cc7-f7e5054a968e" src="https://github.com/user-attachments/assets/d976749a-ab52-4de1-b3be-a646baa5f8de" />

## In detail

<img width="1920" height="1080" alt="pauli-thesis-novelty" src="https://github.com/user-attachments/assets/a23516aa-5885-4d44-8063-5f021979c19c" />

## Machine learning

<img width="1920" height="1080" alt="pauli-thesis-machine-learning" src="https://github.com/user-attachments/assets/cb2e6d03-0fde-4bd4-b689-d0368a2f8b5f" />

## Measures of diversity

<img width="1672" height="941" alt="bb2d4233-ab3f-4127-a5d3-f2c7b1822bdd" src="https://github.com/user-attachments/assets/e6610be8-6bd6-40c8-aa0c-150f229c5def" />

## Projection of the thesis to the future

All maps are wrong, especially those we think are true

## Projection of the thesis to the future

<img width="1920" height="1080" alt="pauli-thesis-future" src="https://github.com/user-attachments/assets/4272a275-f03d-4a99-9086-c4acf5e48250" />



## Stimulating points

# Statistical questions

## 1. Spatial cross-validation

You used spatial block cross-validation to assess classification performance. How did you select the size of the spatial blocks, and how sensitive are your accuracy estimates to that choice?

**Follow-up:** Could smaller blocks lead to residual spatial dependence between the training and validation data and therefore to optimistic estimates of model performance?

## 2. Hierarchical versus flat classification

When comparing hierarchical and flat random-forest classifications, how did you ensure that the comparison was statistically fair in terms of training data, variable selection and hyperparameter tuning?

**Follow-up:** Would nested cross-validation provide a more rigorous comparison between the two modelling strategies?

## 3. Propagation of errors through the hierarchy

In a hierarchical classifier, an error at an upper node necessarily affects all subsequent predictions. How did you quantify the propagation of uncertainty through the classification tree?

**Follow-up:** Could two hierarchical models have the same final accuracy but very different patterns of error propagation?

## 4. Class imbalance and performance metrics

Some vegetation classes were much less frequent than others. How did class imbalance influence the random-forest models and the comparison between hierarchical and flat classification?

**Follow-up:** Why did you choose class-specific F1 scores and overall accuracy, and would macro-averaged F1 or balanced accuracy have led to a different interpretation?

## 5. Uncertainty around differences in accuracy

You report differences in classification accuracy between models and data combinations. Did you calculate confidence intervals or statistically test whether these differences were larger than the stochastic variability of the random forests?

**Follow-up:** How should we interpret small differences in F1 score when repeated model runs show partially overlapping distributions?

## 6. Variable selection and information leakage

VSURF was used for dimensionality reduction before fitting the random-forest models. Was variable selection repeated independently within each cross-validation training fold?

**Follow-up:** If variable selection was performed using the complete dataset, could information leakage have produced optimistic estimates of predictive performance?

## 7. Comparing spatial resolutions across study areas

The comparison between approximately 0.1 m UAV data and 10 m satellite data involves different sites, sampling designs and observational grains. How can we statistically separate the effect of spatial resolution from differences between the two study systems?

**Follow-up:** Would a multiscale experiment conducted over the same plots provide stronger evidence for the effect of resolution?

## 8. Multiple testing in the biodiversity analyses

You examined several diversity metrics, spectral-heterogeneity measures, ecosystems and plant-community levels. How did you address the increased probability of false-positive relationships resulting from this large number of statistical comparisons?

**Follow-up:** Would a hierarchical multivariate model be preferable to many separate generalized linear models?

## 9. Spatial autocorrelation in diversity models

Plant diversity and spectral heterogeneity are both spatially structured. Did you evaluate spatial autocorrelation in the residuals of the generalized linear models?

**Follow-up:** If residual spatial autocorrelation remained, how might this affect coefficient uncertainty, significance tests and the apparent strength of the spectral variation hypothesis?

## 10. Sensitivity of spectral entropy

Spectral-species entropy depends on methodological choices such as the number of spectral species, the clustering procedure and the 3 × 3 pixel moving window. How sensitive were the results to these choices?

**Follow-up:** How would you distinguish a genuine ecological relationship from one produced by the selected spatial window or number of spectral clusters?

# Additional statistical questions

## 11. Stratified sampling and population inference

The field sites were selected using stratified random sampling along major environmental gradients. How did this sampling design affect the statistical representativeness of the dataset?

**Follow-up:** Can model performance estimated from a stratified sample be directly generalized to the full landscape, where the frequencies of environmental conditions and vegetation classes may be different?

## 12. Dependence among observations

Several vegetation plots may share similar environmental conditions or belong to the same plant-community cluster. To what extent can these observations be considered statistically independent?

**Follow-up:** Would a mixed-effects model, with plant community or sampling area as a random effect, provide a more appropriate representation of this dependence?

## 13. Fuzzy versus crisp community membership

Plant communities are not always discrete entities, particularly along ecological gradients. What information is lost when fuzzy floristic relationships are converted into crisp classes for remote-sensing classification?

**Follow-up:** Could probabilistic class membership be modelled directly instead of assigning every observation to a single class?

## 14. Stability of the vegetation clusters

How did you assess the statistical stability of the plant-community clusters obtained through the Isopam procedure?

**Follow-up:** If the field observations were bootstrapped or slightly perturbed, would the same hierarchical structure and terminal clusters emerge?

## 15. Choice of the number of clusters

At several points in the hierarchy, the analysis requires decisions about the number and thematic resolution of vegetation clusters. What statistical and ecological criteria were used to make these decisions?

**Follow-up:** Could alternative numbers of clusters produce similar predictive accuracy but substantially different ecological interpretations?

## 16. Correlated predictor variables

Many spectral bands, indices, phenological variables and topographic predictors are strongly correlated. How does this collinearity affect variable selection and the interpretation of random-forest feature importance?

**Follow-up:** Could conditional permutation importance or grouped variable importance provide a more reliable assessment of the contribution of correlated predictors?

## 17. Statistical interpretation of feature importance

Random-forest permutation importance measures predictive contribution, but it does not necessarily indicate a causal ecological relationship. How did you distinguish statistical importance from ecological mechanism?

**Follow-up:** Could a variable be highly important only because it acts as a proxy for an unmeasured environmental driver?

## 18. Temporal dependence in satellite time series

The monthly satellite observations used to calculate temporal spectral variation are not statistically independent. How did you account for temporal autocorrelation and differences in data quality among months?

**Follow-up:** Would an explicit time-series model provide additional information compared with summarizing temporal variability through a single variance measure?

## 19. Scale dependence of variance and entropy

Both spectral variance and entropy depend on the spatial extent and grain at which they are calculated. How did you determine that the selected moving-window sizes were ecologically appropriate?

**Follow-up:** Did you examine whether the relationships with biodiversity remain consistent across several window sizes, or whether they show a scale-dependent optimum?

## 20. External validation and model transferability

Most validation appears to evaluate interpolation within the sampled landscapes. How confident are you that the models would perform well when transferred to another northern boreal region?

**Follow-up:** Would leave-one-region-out validation or an independent external dataset provide a more realistic estimate of geographical transferability?

# Machine-learning questions

## 1. Choice of random forests

Why did you select random forests as the main machine-learning method for vegetation classification?

**Follow-up:** Which characteristics of your data made random forests more appropriate than gradient boosting, support-vector machines or neural networks?

## 2. Model complexity and sample size

Some terminal vegetation classes contain relatively few field observations. How did you ensure that the random forests were not too complex in relation to the available training data?

**Follow-up:** What evidence do you have that the models learned general ecological patterns rather than class-specific noise?

## 3. Hyperparameter optimization

You optimized the `mtry` parameter, but random forests have other relevant hyperparameters, including tree depth, node size and number of trees. Why did you focus primarily on `mtry`?

**Follow-up:** Could a broader hyperparameter search substantially change classification performance?

## 4. Hierarchical machine learning

In your hierarchical model, a separate random forest is trained at each node of the vegetation hierarchy. What are the advantages of this approach over training a single multiclass model?

**Follow-up:** At what point does dividing the training data among many node-specific models become statistically disadvantageous?

## 5. Error propagation

An incorrect prediction at the top of the hierarchy prevents an observation from reaching the correct lower-level classifier. Could you explain how these cascading errors affect final predictions?

**Follow-up:** Could a soft hierarchical classifier, which propagates class probabilities rather than hard decisions, reduce this problem?

## 6. Probability calibration

Random forests provide class probabilities based on the proportion of votes among trees. Did you evaluate whether these probabilities were well calibrated?

**Follow-up:** Could calibration methods such as isotonic regression or Platt scaling improve the interpretation of prediction uncertainty?

## 7. Class imbalance

How did the machine-learning models deal with rare vegetation classes and unequal class frequencies?

**Follow-up:** Did you consider class weighting, balanced bootstrap sampling, synthetic observations or threshold adjustment, and how might these approaches change the results?

## 8. Feature selection

VSURF was used to select predictors before model training. Why was a separate feature-selection procedure necessary for random forests, which can already handle large numbers of predictors?

**Follow-up:** Could removing correlated but ecologically meaningful variables reduce the transferability of the model?

## 9. Domain shift between ecosystems

The hierarchical classification was expanded from terrestrial to aquatic vegetation. How does the model deal with the considerable domain shift between terrestrial and aquatic remote-sensing signals?

**Follow-up:** How could you determine whether the classifier is genuinely learning transferable ecological structure rather than simply separating water from land?

## 10. Model interpretability

How did you interpret the ecological meaning of a complex ensemble model composed of many decision trees and multiple hierarchical nodes?

**Follow-up:** Could methods such as partial-dependence plots, accumulated local effects or SHAP values reveal relationships that permutation importance alone cannot identify?

## 11. Alternative hierarchical architectures

Did you consider modelling the hierarchy with a single algorithm that explicitly incorporates taxonomic or ecological relationships among classes?

**Follow-up:** How might hierarchical loss functions or graph-based machine learning compare with the sequence of independent random forests used here?

## 12. Prediction outside the training domain

How did you identify pixels whose environmental or spectral conditions fall outside the range represented by the training data?

**Follow-up:** Should predictions in such areas be masked or labelled as extrapolations rather than presented as ordinary classifications?

# Questions on biodiversity metrics

## 1. Species richness versus Shannon diversity

Species richness and Shannon diversity quantify different aspects of community structure. What additional ecological information did Shannon diversity provide compared with species richness in your analyses?

**Follow-up:** If two sites have the same species richness but very different abundance distributions, how would you expect their relationships with spectral heterogeneity to differ?

## 2. Rao’s quadratic entropy

Rao’s quadratic entropy combines differences among species with their relative abundances. Why might Rao’s Q be more informative for remote sensing than species richness or Shannon diversity?

**Follow-up:** Under which ecological conditions would you expect Rao’s Q to show a strong relationship with spectral heterogeneity?

## 3. Phylogenetic Rao’s Q

You calculated a phylogenetic version of Rao’s quadratic entropy. How should we interpret a site with high species richness but low phylogenetic Rao’s Q?

**Follow-up:** Could such a community be spectrally homogeneous despite containing many species?

## 4. Functional and phylogenetic dimensions

What is the conceptual difference between functional Rao’s Q and phylogenetic Rao’s Q in the context of remote sensing?

**Follow-up:** Which of the two should theoretically have the stronger relationship with spectral information, and why?

## 5. Shannon diversity and spectral entropy

Both Shannon diversity and spectral-species entropy use an entropy formulation. Does their mathematical similarity imply that they should be correlated?

**Follow-up:** How can we avoid interpreting a correlation caused by similar mathematical construction as evidence of an ecological mechanism?

## 6. Weighting by species abundance

Some diversity metrics use presence–absence data, whereas others incorporate species abundance. Which form should be more closely related to remotely sensed spectral signals?

**Follow-up:** Since dominant species contribute more strongly to the observed spectral signal, would abundance-weighted metrics systematically outperform presence–absence metrics?

## 7. Rare species

Species richness gives the same weight to rare and dominant species, whereas Shannon diversity reduces the influence of rare species. How might this affect their remote sensibility?

**Follow-up:** Does a weak relationship between spectral variation and species richness indicate that remote sensing is failing to detect rare species rather than biodiversity more generally?

## 8. Correlation among diversity metrics

Many of the 14 biodiversity metrics included in the thesis are likely to be correlated. How did you separate their shared information from the unique ecological information represented by each metric?

**Follow-up:** Could a multivariate ordination or dimensionality-reduction approach identify a smaller number of independent biodiversity dimensions?

## 9. Functional richness versus functional evenness

Functional richness was more strongly related to spectral heterogeneity than functional evenness. How do you interpret this difference ecologically?

**Follow-up:** Could remote sensing be more sensitive to the range of plant strategies present than to how evenly those strategies are distributed?

## 10. Trait selection and functional diversity

Functional diversity values depend strongly on the traits selected and on the distances calculated among species. How did the choice of traits influence functional richness, divergence, dispersion and Rao’s Q?

**Follow-up:** Would using traits that are more directly connected to canopy structure, phenology or leaf optical properties produce stronger remote-sensing relationships?

## 11. Scale dependence of alpha and beta diversity

Species richness, mean plot richness and beta diversity operate at different spatial scales. How did you match the spatial support of these metrics to the spatial resolution of the remote-sensing data?

**Follow-up:** Could an apparent difference among diversity metrics actually be caused by a mismatch in spatial grain?

## 12. Choice of diversity metric

Your results show that the relationship between spectral heterogeneity and biodiversity depends on the diversity metric. Does this mean that asking whether remote sensing can measure “biodiversity” is statistically too general a question?

**Follow-up:** Should future studies define the targeted biodiversity dimension before selecting the sensor, spatial scale and modelling method?
