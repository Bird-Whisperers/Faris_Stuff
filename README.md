# Faris_Stuff



# Resize source images
python tools/process.py \
  --input_dir photos/original \
  --operation resize \
  --output_dir photos/resized

# Split into train/val set
python tools/split.py \
  --dir photos/combined
  
# Creating image pairs from existing images (Combine)
python tools/process.py \
  --input_dir a \
  --b_dir b \
  --operation combine \
  --output_dir c
  
steps:
1) for each month -> only the outlines and cut files are used
2) 'Resize' all images in both files. (this results in cropping)
3) 'Combine' the images 
4) train one month (used Jun)
5) test on another month  (used April)
   
