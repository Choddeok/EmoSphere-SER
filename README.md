# EmoSphere-SER: Enhancing Speech Emotion Recognition through Spherical Representation with Auxiliary Classification <br><sub>The official implementation of EmoSphere-SER (INTERSPEECH 2025)</sub>

## [Paper 📄](https://www.isca-archive.org/interspeech_2025/cho25_interspeech.html)


# Training Procedure

## 1. Environment Setup
Python version = 3.9.7
To replicate the environment necessary to run the code, you have two options:

### Using Conda
   1. Ensure that you have [conda](https://docs.conda.io/projects/conda/en/latest/user-guide/install/) installed.
   2. Create a conda environment using the `spec-file.txt` by running: conda create --name baseline_env --file spec-file.txt
   3. Activate the environment: conda activate baseline_env
   4. Make sure to install the transformers library as it is essential for the code to run: pip install transformers

### Using pip
Alternatively, you can use `requirements.txt` to install the necessary packages in a virtual environment: python -m venv myenv source myenv/bin/activate pip install -r requirements.txt
Make sure to install the transformers library as it is essential for the code to run: pip install transformers

## 2. Configuration
Before running the training or evaluation scripts, check instructions below and update the `./configs/emospehreser.json` file with the paths to your local audio folder and label CSV file.

Please place the path to the `processed_balance_labels_dim_octants.csv` file in the `./configs/emospehreser.json` file to run this configuration.

```bash
python process_labels_for_categorical_dim_sev.py
```

## 3. Training and Evaluation
To train or evaluate the models, use the provided shell scripts. Here's how to use each script:

```bash
sh EmoSphere-SER.sh
```

## Citation
```bash
@inproceedings{cho25_interspeech,
  title     = {{EmoSphere-SER: Enhancing Speech Emotion Recognition Through Spherical Representation with Auxiliary Classification}},
  author    = {Deok-Hyeon Cho and Hyung-Seok Oh and Seung-Bin Kim and Seong-Whan Lee},
  year      = {2025},
  booktitle = {{Interspeech 2025}},
  pages     = {4653--4657},
  doi       = {10.21437/Interspeech.2025-1391},
  issn      = {2958-1796},
}
```

## Acknowledgements
**Our codes are based on the following repos:**
* [MSP-Podcast_Challenge_IS2025](https://github.com/msplabresearch/MSP-Podcast_Challenge_IS2025?tab=readme-ov-file)
