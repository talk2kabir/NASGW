# NASGW
[GUI Widgets Classification based on Neural Architecture Search](#)

Graphical User Interface (GUI) widget classification is gaining much attention in the software engineering community. Prior works mainly adopted mature methods from the computer vision domain that employed manually designed network architectures to classify the GUI widgets. Unfortunately, manually designing good architecture is often time-consuming and requires a certain level of expertise. Therefore, there is a need for an approach to automate the architecture design. In this paper, we propose an approach for automatically generating a GUI widget classification architecture. The proposed method, termed NASGW, uses Neural Architecture Search (NAS) capabilities to automatically generate a high-performance classification architecture based on a labeled widget dataset. Several experiments are conducted to evaluate the performance of the proposed method on a large-scale widgets dataset with over 235k samples.  The experimental results show that our method obtained the best architecture in less than an hour based on the given dataset. Also, when it comes to training, our architecture is 3x faster than the comparative method. The results also show that the proposed method outperforms the state-of-the-art methods on the benchmark datasets, achieving an F1 score of 90% on the original dataset and precision of 92% on the standard dataset. In addition, the performance of the proposed method increases steadily with an increase in training data. Therefore, the proposed method automatically generates the widget classification architecture and reduces the time taken to design the architecture. Meanwhile, the generated architecture achieved better performance than traditional hand-crafted architectures.

# Resource
Paper [Journal](#)

Trained Models [GoogleDrive](#)

Original Dataset [Zenodo](https://zenodo.org/record/2530277#.YWgqL0lfiUl)

Standard Dataset [Dropbox](#)

# Approach 
We propose the NASGW approach that leverages the one-shot NAS method to automatically search for an optimal architecture for GUI widgets classification. The overview of the NASGW approach can be seen in Fig. 6:
1. We design a search space to represent a wide range of architectures.
2. We propose a one-shot model. 
3. We train the one-shot mode to search and predict the performance of the candidate architectures based on the validation accuracy. Select the best performing architecture from the list of candidate architectures.
4. We train the best architecture from scratch to obtain the trained classification model. 

![Fig. 6](https://github.com/talk2kabir/NASGW/blob/main/NASGW.PNG)

# Architecture Search & Testing

### One-shot Search
`python one_shot_search.py --tmp_data_dir ./search_data --save log_path` 

### Train Best Architecture
`python train_arch.py  --tmp_data_dir ./train_data --save log_path --auxiliary --note note_of_this_run` 

### Test Model
`python test_model.py` 

## Citation


