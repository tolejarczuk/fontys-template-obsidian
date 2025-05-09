#!/bin/bash

# put this file somewhere in your PATH
# like /usr/local/bin
# make it executable: chmod +x pandoc-markdown.sh

inputfile="$1"
filename=$(basename "$inputfile")
outputfile="${filename%.md}.pdf"
pdf_dir="Bins/Pdf-Output" # change this to whatever you want
modifiedfile="$pdf_dir/Modified_$filename"

# Remove potential Windows-style line endings
sed 's/\r$//' "$inputfile" > "$modifiedfile"

# Remove Obsidian internal content (adjust regex if needed)
sed -i '/^-----/,$d' "$modifiedfile"

docker run --rm \
  -v "$(pwd):/data" \
  pandoc/extra \
  "$modifiedfile" \
  -o "$pdf_dir/$outputfile" \
  --from markdown \
  --template eisvogel \
  --listings

echo "Done"

rm "$modifiedfile"