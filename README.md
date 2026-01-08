[Uploading convert_to_png_Version5.py…]()
import requests
from PIL import Image
from io import BytesIO

# Direct image URL
image_url = "https://png.pngtree.com/background/20230610/original/pngtree-horizontal-menu-bar-background-image_2995367.jpg"
response = requests.get(image_url)
img = Image.open(BytesIO(response.content))
img.save("output.png", "PNG")
