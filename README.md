# file-date-stamper
Find all files of a given extension, read the desired date/time stamp from the file name, and stamp the modified date/time accordingly for each file.

```
for FILE in *
do
  filename="${FILE%.*}"
  extension="${FILE##*.}"
  if [ $extension = "jpg" ]
  then
    echo "found image: $filename - $extension"
    touch -m -t $filename $FILE
    #touch -m -t 202012311200.jpg
  fi
  #echo $FILE; done
  #echo "${FILE%.*}"
done
```
