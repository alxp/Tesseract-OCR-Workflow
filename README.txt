
Author: Alexander O'Neill - http://twitter.com/alxp - aloneill@gmail.com

This is an Automator script which uses Tesseract (The software underneath OCRopus) to OCR any page you scan in Image Capture, if you have the OCR workflow plugin selected. It seems to work pretty well for me so I thought I would share it. Unlike ABBYY it doesn't produce text-enhanced PDFs, just a txt, but for my purposes it's all I needed. 

The version attached to this e-mail has another workflow step added - instead of acting as an image capture plugin it prompts for Finder items.  To use this with image capture simply open the file in Automator, delete the first workflow step, and save it to ~/Library/Workflows/Applications/Image Capture.

Prerequisites:

To get tesseract and ImageMagick the easiest thing to do is use Homebrew (sort of like Macports but more streamlined)

Run these commands in a Terminal:

# Download and install Homebrew automatically.
ruby -e "$(curl -fsSL https://gist.github.com/raw/323731/install_homebrew.rb)"
# Install Tesseract for OCR
brew install tesseract
# Install ImageMagick for image format conversion
brew install imagemagick

This script assumes that tesseract and convert are in /usr/local/bin. If you've installed them elsewhere you'll need to modify the 'Run Shell Script' step of this workflow to reflect their location.

This is still very new and I have only tested it on a couple of machines. Please let me know if you have any problems or suggestions. 
