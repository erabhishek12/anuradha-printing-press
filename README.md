# anuradha-printing-press

Of course! Here is a complete, step-by-step guide on how to add a new product to your website. I have made it very simple and included examples.

How to Add a New Product: A Simple Guide

(एक नया प्रोडक्ट कैसे जोड़ें: आसान गाइड)

Adding a new product is very easy. You only need to edit one part of your HTML file. Just follow these steps carefully.

Step 1: Get Your Product Image Link

(पहला कदम: अपने प्रोडक्ट की इमेज का लिंक तैयार करें)

Before you start, you need a public link for your product's image.

Go to a free image hosting website like https://postimages.org/.

Upload your product image.

After uploading, the website will give you several links. Copy the link that says "Direct Link". This is the link you will use.

![alt text](https://i.postimg.cc/k5z4LVCr/postimage-guide.png)

Step 2: Open and Find the Product List

(दूसरा कदम: फाइल को खोलें और प्रोडक्ट लिस्ट को ढूंढें)

Open your website's index.html file in a text editor (like Notepad on Windows, or any code editor).

Scroll down to the bottom of the file until you find the <script> section.

Inside the script, find the line that looks like this:

Generated javascript
// --- FULL PRODUCT DATA ---
const products = [


This is the start of your product list.

Step 3: Copy an Existing Product to Use as a Template

(तीसरा कदम: एक टेम्पलेट के रूप में किसी पुराने प्रोडक्ट को कॉपी करें)

To avoid mistakes, it's best to copy an existing product that is similar to your new one.

If you are adding a T-Shirt or a simple item, copy a T-Shirt block.

If you are adding another Phone Case, copy a Phone Case block.

If you are adding a simple product with no options (like a Keychain or Mug), copy a Mug block.

Example: Let's say you want to add a new "Custom Pillow". It's a simple product with no size options, similar to a Mug. So, you would copy the entire block for a Mug, from the opening { to the closing },.

Generated javascript
// Find and copy this whole block
{ 
    id: 'mug-01', 
    name: 'Custom Photo Mug', 
    price: 299, 
    image_plain: 'https://i.postimg.cc/L4Q5DrcL/Chat-GPT-Image-Jul-11-2025-03-45-47-PM.png', 
    image_customized: 'https://i.postimg.cc/rsD87wBW/file-00000000f3346230b33458d933e1c8e9.png', 
    aspect_ratio: 4 / 3, 
    options: null, 
    preview_style: 'top: 25%; left: 15%; width: 70%; height: 50%;' 
},
IGNORE_WHEN_COPYING_START
content_copy
download
Use code with caution.
JavaScript
IGNORE_WHEN_COPYING_END
Step 4: Paste and Edit the Details

(चौथा कदम: पेस्ट करें और जानकारी को बदलें)

Go to the end of the product list, just before the closing ];.

Paste the code you copied in the previous step.

Now, carefully edit the details for your new product.

Here is a breakdown of each field:

id: 📝 Unique ID. Must be unique for each product. Just change the number.

Example: 'mug-05' becomes 'pillow-01'. (Must be in single quotes ' ')

name: 🏷️ Product Name. This is what the customer will see.

Example: 'Quote Mug' becomes 'Custom Photo Pillow'.

price: 💰 Price. Just write the number, without any symbols like "₹".

Example: 299 becomes 549.

image_plain: 🖼️ Main Image. Paste the "Direct Link" you got from PostImages here.

Example: 'https://.../mug.png' becomes 'https://.../pillow.png'.

image_customized: ✨ Hover Image. This image shows when the user moves their mouse over the product.

If you have a second image, paste its link here.

If you only have one image, just use the same link as image_plain.

aspect_ratio: ✂️ Cropper Shape. This sets the shape for the customer's design upload.

1 / 1 for Square (Pillows, Keychains)

3 / 4 for Portrait (T-Shirts)

4 / 3 for Landscape (Mugs)

9 / 16 for Tall Portrait (Phone Cases)

options: ⚙️ Dropdown Options (like Size or Model).

For most products (Pillow, Mug, Keychain), this should be null.

For T-Shirts, copy the options block from a T-shirt.

For Phone Cases, copy the options block from a Phone Case.

preview_style: 🎨 Design Position. This CSS code positions the customer's design on the product preview. It's best to copy this from a similar product.

📌 VERY IMPORTANT: The Comma!

(बहुत ज़रूरी: कॉमा!)

Every product block in the list must end with a comma , except for the very last one.

Generated javascript
const products = [
    { ... product 1 ... },  // <--- Comma
    { ... product 2 ... },  // <--- Comma
    { ... your new product ... } // <--- NO COMMA on the last one
];
IGNORE_WHEN_COPYING_START
content_copy
download
Use code with caution.
JavaScript
IGNORE_WHEN_COPYING_END

If you add your new product to the end of the list, make sure the product before it now has a comma.

Full Example: Adding a "Custom Pillow"

(पूरा उदाहरण: एक "कस्टम पिलो" जोड़ना)

I get my image link: https://i.postimg.cc/Bv8pG5g9/custom-pillow.jpg

I find the products list in the code.

I copy the Mug block because it's a simple product.

I paste it at the end of the list and add a comma to the product that was previously last.

I edit the details.

This is what my new, added code block will look like:

Generated javascript
, // This comma was added to the previous product
    { 
        id: 'pillow-01', 
        name: 'Custom Photo Pillow', 
        price: 549, 
        image_plain: 'https://i.postimg.cc/Bv8pG5g9/custom-pillow.jpg', 
        image_customized: 'https://i.postimg.cc/Bv8pG5g9/custom-pillow.jpg',  // Using same image for hover
        aspect_ratio: 1 / 1,  // Square shape for a pillow
        options: null,        // No size or model options needed
        preview_style: 'top: 20%; left: 20%; width: 60%; height: 60%;' // A good starting position
    } // No comma because this is now the last product
]; // This is the end of the list
IGNORE_WHEN_COPYING_START
content_copy
download
Use code with caution.
JavaScript
IGNORE_WHEN_COPYING_END
Step 5: Save and Check

(पांचवां कदम: सेव करें और जांचें)

Save your index.html file.

Open the file in your browser (or refresh the page if it's already open).

Your new product should now appear in the list!

That's it! By following these steps, you can easily add as many products as you want.
