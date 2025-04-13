# Post Images Guide

## Recommended Folder Structure

For blog post images, use the following structure:

```
assets/img/post/YYYY-MM-DD-post-name/image1.jpg
assets/img/post/YYYY-MM-DD-post-name/image2.jpg
```

Example:

```
assets/img/post/2025-04-13-surface_tension/tension_molecule.jpg
assets/img/post/2025-04-13-surface_tension/waterstrider.jpg
```

## Using the VS Code Snippet

1. In VS Code, when editing a post, type `post-image` and press Tab
2. Fill in the snippet parameters:
   - Image filename
   - Max width (default: 500px)
   - Width percentage (default: 70%)
   - Caption text

## Manual Image Insert

If you prefer to add images manually, use this template:

```liquid
{% include post_image.liquid 
  filename="image.jpg" 
  alt="Image description" 
  max_width="500px" 
  width="70%"
  loading="eager"
  centered="true"
  figure_num="1"
  caption="Your caption text here"
%}
```

## Image Size Recommendations

- Blog post images: 800-1200px wide
- Thumbnails: 600-800px wide
- Max file size: Keep under 300KB when possible

## Using Frontmatter Variables

You can define a common image path in your post frontmatter:

```yaml
---
layout: post
title: Your Post Title
image_path: assets/img/post/YYYY-MM-DD-post-name
---
```

Then use the image path in your references:

```liquid
{% include post_image.liquid 
  filename="image.jpg" 
  alt="Image description" 
  max_width="500px" 
  width="70%"
  loading="eager"
  centered="true"
  figure_num="1"
  caption="Your caption text here"
%}
```
