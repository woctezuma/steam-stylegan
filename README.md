# Steam StyleGAN

The goal of this [Google Colab](https://colab.research.google.com/) notebook is to catpure the distribution of Steam banners and sample with a StyleGAN.

## Usage

-   Acquire the data, e.g. as a snapshot called `128x128.zip` in [another of my repositories](https://github.com/woctezuma/google-colab/tree/master/data),
-   Follow the instructions to edit `train.py` in the [official StyleGAN Github repository](https://github.com/NVlabs/stylegan),
-   Run `StyleGAN.ipynb` to train a StyleGAN.
-   To resume training from a checkpoint, you will have to edit `training/training_loop.py`.

NB: You might have to edit `metrics/frechet_inception_distance.py` to retrieve the network `inception_v3_features.pkl` locally if it cannot be downloaded from Google Colab.

## Results

The dataset consists of 31,723 Steam banners with RGB channels and resized from 460x215 to 128x128 resolution.

A StyleGAN model was trained on 3,524,000 images, with a decreasing mini-batch size, which is about 111 epochs.

### Generated Steam banners

A grid of generated Steam banners:
-   after 2,664 kimg:
![Generated Steam banners after 2,664 kimg](https://github.com/woctezuma/steam-stylegan/wiki/images_steam_stylegan/fakes002664.png)
-   after 3,044 kimg:
![Generated Steam banners after 3,044 kimg](https://github.com/woctezuma/steam-stylegan/wiki/images_steam_stylegan/fakes003044.png)
-   after 3,524 kimg:
![Generated Steam banners after 3,524 kimg](https://github.com/woctezuma/steam-stylegan/wiki/images_steam_stylegan/fakes003524.png)

### Real Steam banners

A grid of real Steam banners:
![Real Steam banners](https://github.com/woctezuma/steam-stylegan/wiki/reals.png)

## References

-   [StyleGAN](https://github.com/NVlabs/stylegan)
