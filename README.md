# DMGAN-with-Text
## Requirements
* `python 3.6.13`
* `Pytorch 1.6.0`
* `python-dateutil 2.8.1`
* `easydict 1.9`
* `nltk 3.5`

## Data availability
* Add our preprocessed metadata of [bird]() and [coco]() to your directory and save them to data/.
* Download the [CUB](https://www.vision.caltech.edu/datasets/cub_200_2011/) dataset and extract them to data/bird/birds/.
* Download the [MS-COCO](https://cocodataset.org/#download) dataset and extract the images to data/coco/.

## Codes

* [DMGAN[code]](https://github.com/MinfengZhu/DM-GAN)

## Training
* Pre-train encoder models: Use this [bird]() and [coco]() files to train the encoder models.
* Train models: Use this [DMGAN]() files for training the models.
* *.yml files are example configuration files for training/evaluating our models.

## Pretrained Models

* [DAMSM]() for `bird`.
* [DAMSM]() for `coco`.
* [DMGAN]() for `bird`.
* [DMGAN]() for `coco`.

## Sampling

* For sampling we need to change configurations in cfg file.
* To generate images for the pre-extracted embeddings: Set `cfg.TRAIN.FLAG = False` and `cfg.B_VALIDATION = True`.
* To generate images for custom text input: Set `cfg.TRAIN.FLAG = False` and `cfg.B_VALIDATION = False`.

## Evaluation
* We compute inception score for models trained on birds using [StackGAN-inception-model](https://github.com/hanzhanggit/StackGAN-inception-model).
* We compute inception score for models trained on coco using [improved-gan/inception_score](https://github.com/openai/improved-gan/tree/master/inception_score).
* We compute FID score for models using [https://github.com/mseitzer/pytorch-fid/tree/802da3963113b5b5f8154e0e27580ee4c97460ab].
 
## Performance

## References
* [AttnGAN: Fine-Grained Text to Image Generation with Attentional Generative Adversarial Networks](https://github.com/taoxugit/AttnGAN)
* [DM-GAN: Dynamic Memory Generative Adversarial Networks for Text-to-Image Synthesis ](https://github.com/MinfengZhu/DM-GAN)
* [DF-GAN: A Simple and Effective Baseline for Text-to-Image Synthesis ](https://github.com/tobran/DF-GAN)
