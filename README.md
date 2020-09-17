# python-Scale-and-convert-images-using-PIL

At the bottem there's a script that uses PIL to perform the following operations:

    Iterate through each file in the folder
    For each file:
        - Rotate the image 90° clockwise
        - Resize the image from 192x192 to 128x128
        - Save the image to a new folder in .jpeg format

Saves the updated images in the folder: /opt/icons/

Once the script is ready, grant executable permission to the script file.

- `chmod +x <script_name>.py`

- Replace <script_name> with the name of your script.

Now, run the file.

- ./<script_name>.py

Replace <script_name> with the name of your script.

On a successful run, this should produce images in the right format within the directory: /opt/icons/
- old path is Desktop/images

`#!/usr/bin/env python3`</br>
`from PIL import Image`</br>
`import os`</br>
</br>
`old_path = os.path.expanduser('~') + ("/Desktop/images/")`</br>
`new_path = /opt/icons/`</br>

`for image in os.listdir(old_path):`</br>
    `if '.' not in image[0]:`</br>
        `img = Image.open(old_path + image)`</br>
        `img.rotate(90).resize((128,128)).convert('RGB').save(new_path + str(image.split('.')[0])+'.jpeg')`</br>
  
