# GPTInformal-Persian-Speech-Dataset
GPTInformal Persian is a free licensed Persian dataset of audio and text pairs designed for speech synthesis and other speech-related tasks. The dataset has been collected, processed, and annotated as a part of the Mana-TTS project. For details on data processing pipeline and statistics on this dataset, please refer to the paper in the Citation secition.

## Data Source
The text for this dataset was generated using GPT4o, with prompts covering a wide range of subjects such as politics and nature. The texts are intentionally crafted in informal Persian. Below is the prompt format used to generate these texts:

> Please give me a very long text written in informal Persian. I want it to be mostly about [SUBJECT].

These generated texts were then recorded in a quiet environment. The audio and text files underwent forced alignment using [aeneas](https://github.com/readbeyond/aeneas), resulting in smaller chunks of audio-text pairs as presented in this dataset.

## Download
You can download the dataset from [this repository](https://huggingface.co/datasets/MahtaFetrat/GPTInformal-Persian).

### Data Columns

Each Parquet file contains the following columns:

- **file name** (`string`): The unique identifier of the audio file.
- **transcript** (`string`): The ground-truth transcript of the audio.
- **duration** (`float64`): Duration of the audio file in seconds.
- **subject** (`string`): The subject used in prompt to get the original text file.
- **audio** (`sequence`): The actual audio data.
- **samplerate** (`float64`): The sample rate of the audio.


## Citation

If you use GPTInformal-Persian in your research or projects, please cite the following paper:

```bash
@article{fetrat2024manatts,
      title={ManaTTS Persian: a recipe for creating TTS datasets for lower resource languages}, 
      author={Mahta Fetrat Qharabagh and Zahra Dehghanian and Hamid R. Rabiee},
      journal={arXiv preprint arXiv:2409.07259},
      year={2024},
}
```

## License

This dataset is available under the cc0-1.0. However, the dataset should not be utilized for replicating or imitating the speaker’s voice for malicious
purposes or unethical activities, including voice cloning for malicious intent.
