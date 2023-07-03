# exif-remover
remove exif data from .jpg and .tiff file formats


🔴How to run:

-> Install Pillow (Pillow will not work if you have PIL installed):
```python
python3 -m pip install --upgrade pip
```
```python
python3 -m pip install --upgrade Pillow
```

-> Create a new folder called "images" in the same directory as the python sciprt

-> Add images which needs exif removed into the images folder

-> Run the command:
```python
python remove_exif.py
```

---


🔴How it works:

🔹The code imports the necessary modules: os for file and directory operations and Image from PIL for image processing.

🔹The code retrieves a list of files in the current directory using os.listdir(). If the list is empty, it prints a message indicating that there are no files in the "./images" folder and then exits the program.

🔹First, Image.open() is used to open the image file. Then, img.getdata() retrieves the pixel data of the image. The code creates a new image, img_no_exif, with the same mode and size as the original image using Image.new(). It then puts the pixel data into the new image using img_no_exif.putdata(). Finally, the modified image is saved back to the original file using img_no_exif.save(file).

---

Please note that this code modifies the images in place, overwriting the original files. Make sure to have backups of your images before running this code.
