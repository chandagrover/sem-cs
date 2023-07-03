# Sem-CS: Semantic CLIPStyler for Text-Based Image Style Transfer (ICIP 2023 accepted, Conference Paper)
Semantic CLIPStyler
Below steps to follow:
Dependencies:
This code works on Python 3.8>=

!pip install git+https://github.com/openai/CLIP.git

Other package dependencies are mentioned in requirements.txt

### 1) Salient Object Detection
 
    We have provided already produced masks by Deep Spectral Segmentation here for now. We will update the code later for producing it in single pipeline.

### 2) Semantic CLIPStyler

    a) To run single text condition
        python clipstyler_spectral.py --content_path "test_set/night1_resized.png" --segmentedImage_path "segmaps/night1_resized.npy" --filename "night1_resized" --exp_name "exp1" --text "Starry Night by Vincent van gogh"

    b) To run multiple text condition
        python clipstyler_spectral_globfb.py --content_path test_set/night1_resized.png --segmentedImage_path segmaps/night1_resized.npy --filename night1_resized  --exp_name exp2 --textb "Pop Art" --textf  "Starry Night by Vincent Van Gogh"
