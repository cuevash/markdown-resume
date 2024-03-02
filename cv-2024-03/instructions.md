# INSTRUCTIONS

## All together Chrome (to be run on terminal on its folder)

pandoc resume.md -f markdown -t html -c ../resume-stylesheet.css -s -o resume.html; /Applications/Google\ Chrome.app/Contents/MacOS/Google\ Chrome --headless --disable-gpu --no-pdf-header-footer --print-to-pdf-size=A4 --print-to-pdf=resume.pdf resume.html
