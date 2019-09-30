# Faris_Stuff



# Resize source images
python tools/process.py \
  --input_dir photos/original \
  --operation resize \
  --output_dir photos/resized
# Create images with blank centers
python tools/process.py \
  --input_dir photos/resized \
  --operation blank \
  --output_dir photos/blank
# Combine resized images with blanked images
python tools/process.py \
  --input_dir photos/resized \
  --b_dir photos/blank \
  --operation combine \
  --output_dir photos/combined
# Split into train/val set
python tools/split.py \
  --dir photos/combined
  
  
  
