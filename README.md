# S-3PO

<img src="https://github.com/fluxdigital/S-3PO/blob/main/s3po-logo.png" width="200" align="left">&nbsp;

An Generative AI Module for Sitecore XP built with SPE and using various models from ChatGPT/OpenAI.

<div>
    <a href="https://www.loom.com/share/a5b36d22afef4cf6acaae860a16d0d81">
      <p>Demo of S-3PO v1 - Image Generation with AI - Watch Video</p>
    </a>
    <a href="https://www.loom.com/share/a5b36d22afef4cf6acaae860a16d0d81">
      <img style="max-width:200px;" src="https://cdn.loom.com/sessions/thumbnails/a5b36d22afef4cf6acaae860a16d0d81-933ea45f242d475a-full-play.gif">
    </a>
  </div>
<br clear="both"/>

**Current features in Content Editor are:**

- Rewriting Text with AI (using GPT-35 Turbo, GPT-4o mini, GPT-4o Turbo or GPT-4o)
- Generating Images with AI (using Dall-e-2 or Dall-e-3)

**Note:** This module sends prompts to ChatGPT in order to function - Flux Digital Ltd, Adam Seabridge and any of the developers of this Module accept no responsibility for any loss or damage caused by using this module. 

## Pre-requisites
- You must have Sitecore Powershell Extensions installed. This release has been tested with Sitecore 10.3 and 10.4 and SPE 6.4 but should work with older versions also.
- You must have an API Key for ChatGPT/Open AI: https://platform.openai.com/. 
**Note:** in my testing this was not expensive, especially if you select the cheaper Open AI Models.
<img src="https://github.com/fluxdigital/S-3PO/blob/main//s3po-images/open-api-key.png" width="400" align="left">
<br clear="both"/>

## Install Notes
1. Download the package from the release link below
2. Install the package using the Sitecore package install option in the Sitecore Desktop
3. Re-build the SPE integration Points from the SPE Menu
4. You should now have S-3PO installed under the SPE modules item:

<img src="https://github.com/fluxdigital/S-3PO/blob/main//s3po-images/s3po-module.png" width="200" align="left">
<br clear="both"/>


5. Open the web.config and update the ```<Content-Security-Policy>``` under the ```<customHeaders>``` to add in ```https://oaidalleapiprodscus.blob.core.windows.net``` (this will re-start your CM so be aware of this):

<img src="https://github.com/fluxdigital/S-3PO/blob/main//s3po-images/add-Content-Security-Policy.png" width="600" align="left">
<br clear="both"/>

**Note:** this is required for images to display when Generating them with AI - otherwise you will see no images returned and Content-Security-Policy errors in your browser console.

## Settings
- Add your API Key from OpenAI in the settings here: ```/sitecore/system/Modules/PowerShell/Script Library/S-3PO/S-3PO Settings```
<img src="https://github.com/fluxdigital/S-3PO/blob/main//s3po-images/s3po-settings.png" width="600" align="left">
<br clear="both"/>

- Choose which models you'd like to use for Text and Image AI.
- Optionally - create a new folder in the media library and change the Media Library Folder (e.g '/S-3PO') images are created by default here: ```/sitecore/media library/Files```
- Save the settings
  
## Usage

- Once you've updated the settings to add your API Key and so forth you can go to a page in Content editor and use one of the two options:
<img src="https://github.com/fluxdigital/S-3PO/blob/main//s3po-images/s3po-buttons.png" width="300" align="left">
<br clear="both"/>


### Re-write with AI

Choose this option to Re-write Text using AI. Select a Text Field (Singleline Text, Multline Text or Rich Text) and the options you want to use and click continue:
<br clear="both"/>
<img src="https://github.com/fluxdigital/S-3PO/blob/main//s3po-images/s3po-re-write.png" width="300" align="left">
<br clear="both"/>

Choose one of the results returned and click continue to update your Text field with the re-written text:
<br clear="both"/>
<img src="https://github.com/fluxdigital/S-3PO/blob/main//s3po-images/s3po-re-write-2.png" width="300" align="left">
<br clear="both"/>


### Generate Image with AI

Choose this option to Generate Images using AI. Select an Image field and the options you want to use and click continue:
<img src="https://github.com/fluxdigital/S-3PO/blob/main//s3po-images/s3po-gen-image.png" width="300" align="left">
<br clear="both"/>

Choose one of the Images returned and click continue to update your Image field with the Generated Image:
<img src="https://github.com/fluxdigital/S-3PO/blob/main//s3po-images/s3po-gen-image-2.png" width="300" align="left">
<br clear="both"/>

## Releases
[Download Release v1](https://github.com/fluxdigital/S-3PO/releases/tag/1.0.0)

