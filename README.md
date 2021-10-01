# batch-process-Meyer
CSCI 4830 exercise 5 shell code

f rn "$1"/*; do
  if [ -f "$f" ]; then
    COUNT="$(wc -w "${f}" | cut -d " " -f1)"
    SIZE="$(du -sh "${f}" | cut -f1)"
    echo "Processing $f file..."
    echo "File Size: $SIZE"
    echo "Word Size: $COUNT"
  fi
done
