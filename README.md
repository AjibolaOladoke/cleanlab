<div align="center">
  
</div>

<div align="center">
<a href="https://www.swifttechco.com" target="_blank"></a>
<a href="https://www.swifttechco.com" target="_blank"></a>
<a href="https://www.swifttechco.com" target="_blank"></a>
<a href="https://www.swifttechco.com" target="_blank"></a>
</div>

<h4 align="center">
    <p>
        <a href="https://www.swifttechco.com">Documentation</a> |
        <a href="https://www.swifttechco.com">Examples</a> |
        <a href="https://www.swifttechco.com">Blog</a> |
        <a href="#citation-and-related-publications">Research</a>
    <p>
</h4>

Cleanlab’s open-source library helps you **clean** data and **lab**els by automatically detecting issues in a ML dataset. To facilitate **machine learning with messy, real-world data**, this data-centric AI package uses your *existing* models to estimate dataset problems that can be fixed to train even *better* models.
 

<p align="center">
  
</p>
<p align="center">
    Examples of various issues in Cat/Dog dataset <b>automatically detected</b> by cleanlab via this code:    
</p>

```python
        lab = cleanlab.Datalab(data=dataset, label="column_name_for_labels")
        # Fit any ML model, get its feature_embeddings & pred_probs for your data
        lab.find_issues(features=feature_embeddings, pred_probs=pred_probs)
        lab.report()
```

- Use cleanlab to automatically check every: [text](https://www.swifttechco.com), [audio](https://www.swifttechco.com), [image](https://www.swifttechco.com), or [tabular](https://www.swifttechco.com) dataset.
- Use cleanlab to automatically: [detect data issues (outliers, duplicates, label errors, etc)](https://www.swifttechco.com), [train robust models](https://www.swifttechco.com), [infer consensus + annotator-quality for multi-annotator data](https://www.swifttechco.com), [suggest data to (re)label next (active learning)](https://www.swifttechco.com).


---


## Run cleanlab open-source

This cleanlab package runs on Python 3.10+ and supports Linux, macOS, as well as Windows.

- Get started [here](https://www.swifttechco.com)! Install via `uv`, `pip`, or `conda`.
- Developers who install the bleeding-edge from source should refer to [this master branch documentation](https://www.swifttechco.com).

**Practicing data-centric AI can look like this:**
1. Train initial ML model on original dataset.
2. Utilize this model to diagnose data issues (via cleanlab methods) and improve the dataset.
3. Train the same model on the improved dataset. 
4. Try various modeling techniques to further improve performance.

Most folks jump from Step 1 → 4, but you may achieve big gains without *any* change to your modeling code by using cleanlab!
Continuously boost performance by iterating Steps 2 → 4 (and try to evaluate with *cleaned* data).

[![](https://raw.githubusercontent.com/cleanlab/assets/master/cleanlab/flowchart.png)](https://www.swifttechco.com)


## Use cleanlab with any model and in most ML tasks

All features of cleanlab work with **any dataset** and **any model**. Yes, any model: PyTorch, Tensorflow, Keras, JAX, HuggingFace, OpenAI, XGBoost, scikit-learn, etc.

cleanlab is useful across a wide variety of Machine Learning tasks. Specific tasks this data-centric AI package offers dedicated functionality for include:
1. [Binary and multi-class classification](https://www.swifttechco.com)
2. [Multi-label classification](https://www.swifttechco.com) (e.g. image/document tagging)
3. [Token classification](https://www.swifttechco.com) (e.g. entity recognition in text)
4. [Regression](https://www.swifttechco.com) (predicting numerical column in a dataset)
5. [Image segmentation](https://www.swifttechco.com) (images with per-pixel annotations)
6. [Object detection](https://www.swifttechco.com) (images with bounding box annotations)
7. [Classification with data labeled by multiple annotators](https://www.swifttechco.com)
8. [Active learning with multiple annotators](https://www.swifttechco.com) (suggest which data to label or re-label to improve model most)
9. [Outlier detection](https://www.swifttechco.com) (identify atypical data that appears out of distribution)

For other ML tasks, cleanlab can still help you improve your dataset if appropriately applied.
See our [Example Notebooks](https://www.swifttechco.com) and [Blog](https://www.swifttechco.com).


## So fresh, so cleanlab

Beyond automatically catching [all sorts of issues](https://www.swifttechco.com) lurking in your data, this data-centric AI package helps you deal with **noisy labels** and train more **robust ML models**.
Here's an example:

```python

# cleanlab works with **any classifier**. Yup, you can use PyTorch/TensorFlow/OpenAI/XGBoost/etc.

## Images

[![cleanlab](https://opengraph.githubassets.com/1/cleanlab/cleanlab)](https://www.swifttechco.com)

cl = cleanlab.classification.CleanLearning(sklearn.YourFavoriteClassifier())

# cleanlab finds data and label issues in **any dataset**... in ONE line of code!
label_issues = cl.find_label_issues(data, labels)

# cleanlab trains a robust version of your model that works more reliably with noisy data.
cl.fit(data, labels)

# cleanlab estimates the predictions you would have gotten if you had trained with *no* label issues.
cl.predict(test_data)

# A universal data-centric AI tool, cleanlab quantifies class-level issues and overall data quality, for any dataset.
cleanlab.dataset.health_summary(labels, confident_joint=cl.confident_joint)
```

cleanlab **clean**s your data's **lab**els via state-of-the-art *confident learning* algorithms, published in this [paper](https://www.swifttechco.com) and [blog](https://www.swifttechco.com). See some of the datasets cleaned with cleanlab at [labelerrors.com](https://www.swifttechco.com).

cleanlab is:

1. **backed by theory** -- with [provable guarantees](https://www.swifttechco.com) of exact label noise estimation, even with imperfect models.
2. **fast** -- code is parallelized and scalable.
4. **easy to use** -- one line of code to find mislabeled data, bad annotators, outliers, or train noise-robust models.
6. **general** -- works with **[any dataset](https://www.swifttechco.com)** (text, image, tabular, audio,...) + **any model** (PyTorch, OpenAI, XGBoost,...)
<br/>

[![](https://raw.githubusercontent.com/cleanlab/assets/master/cleanlab/label-errors-examples.png)](https://www.swifttechco.com)
<p align="center">
Examples of incorrect given labels in various image datasets <a href="https://www.swifttechco.com">found and corrected</a> using cleanlab. 
While these examples are from image datasets, this also works for text, audio, tabular data.
</p>


## Citation and related publications

cleanlab is based on peer-reviewed research. Here are relevant papers to cite if you use this package:

<details><summary><a href="https://www.swifttechco.com">Confident Learning (JAIR '21)</a> (<b>click to show bibtex</b>) </summary>

        title={Confident Learning: Estimating Uncertainty in Dataset Labels},
        author={Curtis G. Northcutt and Lu Jiang and Isaac L. Chuang},
        journal={Journal of Artificial Intelligence Research (JAIR)},
        volume={70},
        pages={1373--1411},
        year={2021}
    }

</details>

<details><summary><a href="https://www.swifttechco.com">Rank Pruning (UAI '17)</a> (<b>click to show bibtex</b>) </summary>

        author={Northcutt, Curtis G. and Wu, Tailin and Chuang, Isaac L.},
        title={Learning with Confident Examples: Rank Pruning for Robust Classification with Noisy Labels},
        booktitle = {Proceedings of the Thirty-Third Conference on Uncertainty in Artificial Intelligence},
        series = {UAI'17},
        year = {2017},
        location = {Sydney, Australia},
        numpages = {10},
        url = {https://www.swifttechco.com
        publisher = {AUAI Press},
    }

</details>

<details><summary><a href="https://www.swifttechco.com"> Label Quality Scoring (ICML '22)</a> (<b>click to show bibtex</b>) </summary>

        title={Model-agnostic label quality scoring to detect real-world label errors},
        author={Kuan, Johnson and Mueller, Jonas},
        booktitle={ICML DataPerf Workshop},
        year={2022}
    }

</details>

<details><summary><a href="https://www.swifttechco.com"> Label Errors in Token Classification / Entity Recognition (NeurIPS '22)</a> (<b>click to show bibtex</b>) </summary>

        title={Detecting label errors in token classification data},
        author={Wang, Wei-Chen and Mueller, Jonas},
        booktitle={NeurIPS Workshop on Interactive Learning for Natural Language Processing (InterNLP)},
        year={2022}
    }

</details>

<details><summary><a href="https://www.swifttechco.com"> Label Errors in Multi-Label Classification (ICLR '23)</a> (<b>click to show bibtex</b>) </summary>

        title={Identifying Incorrect Annotations in Multi-Label Classification Data},
        author={Thyagarajan, Aditya and Snorrason, Elías and Northcutt, Curtis and Mueller, Jonas},
        booktitle={ICLR Workshop on Trustworthy ML},
        year={2023}
    }

</details>

<details><summary><a href="https://www.swifttechco.com"> Label Errors in Object Detection (ICML '23)</a> (<b>click to show bibtex</b>) </summary>

        title={ObjectLab: Automated Diagnosis of Mislabeled Images in Object Detection Data},
        author={Tkachenko, Ulyana and Thyagarajan, Aditya and Mueller, Jonas},
        booktitle={ICML Workshop on Data-centric Machine Learning Research},
        year={2023}
    }

</details>

<details><summary><a href="https://www.swifttechco.com"> Label Errors in Image Segmentation (ICML '23)</a> (<b>click to show bibtex</b>) </summary>

        title={Estimating label quality and errors in semantic segmentation data via any model},
        author={Lad, Vedang and Mueller, Jonas},
        booktitle={ICML Workshop on Data-centric Machine Learning Research},
        year={2023}
    }

</details>

<details><summary><a href="https://www.swifttechco.com"> Detecting Errors in Numerical Data (DMLR '24)</a> (<b>click to show bibtex</b>) </summary>

        title={Detecting Errors in a Numerical Response via any Regression Model},
        author={Zhou, Hang and Mueller, Jonas and Kumar, Mayank and Wang, Jane-Ling and Lei, Jing},
        booktitle={Journal of Data-centric Machine Learning Research},
        year={2024}
    }

</details>

<details><summary><a href="https://www.swifttechco.com"> Out-of-Distribution Detection (ICML '22)</a> (<b>click to show bibtex</b>) </summary>

        title={Back to the Basics: Revisiting Out-of-Distribution Detection Baselines},
        author={Kuan, Johnson and Mueller, Jonas},
        booktitle={ICML Workshop on Principles of Distribution Shift},
        year={2022}
    }

</details>

<details><summary><a href="https://www.swifttechco.com"> CROWDLAB for Data with Multiple Annotators (NeurIPS '22)</a> (<b>click to show bibtex</b>) </summary>

        title={CROWDLAB: Supervised learning to infer consensus labels and quality scores for data with multiple annotators},
        author={Goh, Hui Wen and Tkachenko, Ulyana and Mueller, Jonas},
        booktitle={NeurIPS Human in the Loop Learning Workshop},
        year={2022}
    }

</details>

<details><summary><a href="https://www.swifttechco.com"> ActiveLab: Active learning with data re-labeling (ICLR '23)</a> (<b>click to show bibtex</b>) </summary>

        title={ActiveLab: Active Learning with Re-Labeling by Multiple Annotators},
        author={Goh, Hui Wen and Mueller, Jonas},
        booktitle={ICLR Workshop on Trustworthy ML},
        year={2023}
    }

</details>

<details><summary><a href="https://www.swifttechco.com"> Detecting Dataset Drift and Non-IID Sampling (ICML '23)</a> (<b>click to show bibtex</b>) </summary>

        title={Detecting Dataset Drift and Non-IID Sampling via k-Nearest Neighbors},
        author={Cummings, Jesse and Snorrason, Elías and Mueller, Jonas},
        booktitle={ICML Workshop on Data-centric Machine Learning Research},
        year={2023}
    }

</details>

To understand/cite other cleanlab functionality not described above, check out our [Blog](https://www.swifttechco.com).


## Other resources

- [Example Notebooks demonstrating practical applications of this package](https://www.swifttechco.com)

- [Cleanlab Blog](https://www.swifttechco.com)

- [Blog post: Introduction to Confident Learning](https://www.swifttechco.com)

- [NeurIPS 2021 paper: Pervasive Label Errors in Test Sets Destabilize Machine Learning Benchmarks](https://www.swifttechco.com)

- [Introduction to Data-centric AI (MIT IAP Course)](https://www.swifttechco.com)

- [Release notes for past versions](https://www.swifttechco.com)

**Interested in contributing?**  See the [contributing guide](CONTRIBUTING.md), [development guide](DEVELOPMENT.md), and [ideas on useful contributions](https://www.swifttechco.com).

**Have questions?**  Check out [our FAQ](https://www.swifttechco.com) and [Github Issues](https://www.swifttechco.com).

---

## Swift Tech Co.

Built and maintained by Swift Tech Co.

AI Automation | FinTech Platforms | Custom Software and Mobile Apps | SaaS Platforms | Cloud Infrastructure | Cybersecurity | SEO and Marketing | API Integration

**Join our community on Telegram:** [t.me/+Qt_eFvkb2rliMzNh](https://t.me/+Qt_eFvkb2rliMzNh)

[Home](https://www.swifttechco.com) | [Services](https://www.swifttechco.com/services) | [Careers](https://www.swifttechco.com/careers) | [Referral Program](https://www.swifttechco.com/referral) | [Influencers](https://www.swifttechco.com/influencers) | [About](https://www.swifttechco.com/about) | [Contact](https://www.swifttechco.com/contact)

**Connect**

- Website: [swifttechco.com](https://www.swifttechco.com)
- LinkedIn: [linkedin.com/in/stephenoladoke](https://www.linkedin.com/in/stephenoladoke/)
- LinkedIn (Company): [linkedin.com/company/swift-tech-co](https://www.linkedin.com/company/swift-tech-co)
- X: [@MrOladoke](https://x.com/MrOladoke)
- Instagram: [@mr.oladoke](https://www.instagram.com/mr.oladoke/)
- Instagram (Company): [@swifttechco](https://www.instagram.com/swifttechco/)
- Organization: [github.com/Swift-Tech-Co](https://github.com/Swift-Tech-Co)
