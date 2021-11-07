# automator-TranslateScreenshotTextKorean
[Mac Automator](https://support.apple.com/en-mt/guide/automator/welcome/mac) service that will try to grab Korean text from a screenshot selection and then translate it to English.  Please note that [Optical Character Recognition (OCR)](https://en.wikipedia.org/wiki/Optical_character_recognition) technology is not perfect and can only make a best guess. 

## Requirements
- Have [Tesseract OSR](https://github.com/tesseract-ocr/tesseract) [installed on your Mac](https://www.oreilly.com/library/view/building-computer-vision/9781838644673/95de5b35-436b-4668-8ca2-44970a6e2924.xhtml).  

## Installation
- Save `.workflow` file to `{YOUR HOME DIRECTORY}/Library/Services`.
- Go to `System Preferences > Keyboard > Shortcuts > Services`.
- In the list of services shown, select `General > Translate Screenshot Text (Korean)`.
- Click on `Add Shortcut` button next to it, and type in any sequence of keys you want as a trigger for this new service.
  - Make sure it's unique and not an existing keyboard shortcut for anything else.
  - If you want to follow the existing pattern for the built-in screenshot shortcuts, refer to `System Preferences > Keyboard > Shortcuts > Screenshots`.

## Usage
- Type in the keyboard shortcut you created during workflow installation.
- This should prompt you select a screenshot.
- For best accuracy, try to select an area that only has Korean words -- no other icons, symbols, or pictures.
- The detected Korean text will be sent to [Papago](https://papago.naver.com/) on a [Safari](https://www.apple.com/safari/) pop-up window.
  - If no text is detected, something in the screenshot is unrecognizable for the [Tesseract OSR](https://github.com/tesseract-ocr/tesseract). It could be a certain font or a certain word in the screenshot.  Try to narrow down your screenshot selection to fewer words.
  - If text is recognized but with mistakes, you can also tweak it as needed in the [Papago](https://papago.naver.com/) page as long as you have [Korean enabled for your Mac keyboard](https://support.apple.com/en-mt/guide/korean-input-method/welcome/mac).
