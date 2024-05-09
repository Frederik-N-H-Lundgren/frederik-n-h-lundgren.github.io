---
title: Enjoy
prev: network-analysis
---

<style>
  .large-image {
    width: 50%; /* Adjust the width as needed */
    display: block;
    margin: auto;
  }
  
  .photo-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr); /* Adjust the number of columns as needed */
    gap: 10px; /* Adjust the gap between images as needed */
    margin-top: 20px;
  }

  .photo-grid img {
    width: 100%;
    height: auto;
    border-radius: 5px; /* Optional: adds a rounded border to images */
  }
</style>

<img src="/images/joey1.png" class="large-image" />

<div class="photo-grid">
  <img src="/images/joey2.png" alt="Image 2" />
  <img src="/images/joey3.png" alt="Image 3" />
  <img src="/images/joey4.png" alt="Image 4" />
  <img src="/images/joey5.png" alt="Image 5" />
  <img src="/images/joey6.png" alt="Image 6" />
</div>
This code directly uses HTML <img> tags instead of Markdown's image syntax. This should ensure that the images are displayed correctly. If you still encounter any issues, please let me know!

User
I can still not see the images, is there another way to write the markdown so it actually shows the images the way i want it?
ChatGPT
I understand. Let's try another approach. GitHub Pages might not allow the direct embedding of HTML and CSS within Markdown files due to security reasons. We can use a different Markdown syntax to align and resize the images. Here's how you can modify your Markdown code:

markdown
Copy code
---
title: Enjoy
prev: network-analysis
---

![Large Image](/images/joey1.png){: .large-image }

<div class="photo-grid">
  ![Image 2](/images/joey2.png){: .photo }
  ![Image 3](/images/joey3.png){: .photo }
  ![Image 4](/images/joey4.png){: .photo }
  ![Image 5](/images/joey5.png){: .photo }
  ![Image 6](/images/joey6.png){: .photo }
</div>
Then, add the following CSS code to your HTML file:

css
Copy code
<style>
  .large-image {
    width: 50%; /* Adjust the width as needed */
    display: block;
    margin: auto;
  }
  
  .photo-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr); /* Adjust the number of columns as needed */
    gap: 10px; /* Adjust the gap between images as needed */
    margin-top: 20px;
  }

  .photo {
    width: 100%;
    height: auto;
    border-radius: 5px; /* Optional: adds a rounded border to images */
  }
</style>
