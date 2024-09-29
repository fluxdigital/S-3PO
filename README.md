# S-3PO

<img src="https://github.com/fluxdigital/S-3PO/blob/main/s3po-logo.png" width="200" align="left">

An Generative AI Module for Sitecore XP built with SPE and using various models from ChatGPT/OpenAI.

Current features are Rewriting Text and Generating Images in Content Editor with AI

<br clear="both"/>

## Pre-requisites
You must have Sitecore Powershell Extensions installed. This release has been tested with Sitecore 10.3 and 10.4 and SPE 6.4 but should work with older versions also.

## Install Notes
1. Download the package from the release link below
2. Install the package using the Sitecore package install option in the Sitecore Desktop
3. You should now have S-3PO installed under the SPE modules item:

<img src="https://github.com/fluxdigital/S-3PO/blob/main//s3po-images/s3po-module.png" width="200" align="left">
<br clear="both"/>


4. Open the web.config and update the ```<Content-Security-Policy>``` under the ```<customHeaders>``` (this will re-start your CM so be aware of this):

<img src="https://github.com/fluxdigital/S-3PO/blob/main//s3po-images/add-Content-Security-Policy.png" width="600" align="left">
<br clear="both"/>

## Settings
- Add your API Key from OpenAI in the settings here: /sitecore/system/Modules/PowerShell/Script Library/S-3PO/S-3PO Settings
<img src="https://github.com/fluxdigital/S-3PO/blob/main//s3po-images/s3po-settings.png" width="600" align="left">
<br clear="both"/>

- Choose which models you'd like to use for Text and Image AI.
- Optionally - create a new folder in the media library and change the Media Library Folder (e.g '/S-3PO') images are created by default here: ```/sitecore/media library/Files```
- Save the settings
  
## Usage

- 
## Releases
[Download Release v1](https://github.com/fluxdigital/S-3PO/releases/tag/1.0.0)

