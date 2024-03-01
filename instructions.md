# INSTRUCTIONS

### Run this to generate HTML

pandoc resume.md -f markdown -t html -c resume-stylesheet.css -s -o resume.html

### Run this to convert the HTML into PDF using local paths for images and change [CURRENT_DIR] with the current full directory

wkhtmltopdf --base [CURRENT_DIR] --enable-local-file-access resume.html resume.pdf

### Everthing together

pandoc resume.md -f markdown -t html -c resume-stylesheet.css -s -o resume.html; wkhtmltopdf --base [CURRENT_DIR] --enable-local-file-access --javascript-delay 2000 resume.html resume.pdf

### Example of using options

wkhtmltopdf --enable-local-file-access --page-size A4 --margin-top 1in --margin-bottom 0.8in --margin-right 0.5in --margin-left 0.5in --encoding UTF-8 --header-html [header-html-file-path] --footer-line --footer-html [footer-html-file-path] --footer-right "[page] / [topage]" --no-outline input.html output.pdf

### Another option is to have Chrome to generate the pdf

#### In OSX would be

/Applications/Google\ Chrome.app/Contents/MacOS/Google\ Chrome --headless --disable-gpu --no-pdf-header-footer --print-to-pdf-size=A4 --print-to-pdf=resume.pdf resume.html

#### All together Chrome

pandoc resume.md -f markdown -t html -c resume-stylesheet.css -s -o resume.html; /Applications/Google\ Chrome.app/Contents/MacOS/Google\ Chrome --headless --disable-gpu --no-pdf-header-footer --print-to-pdf-size=A4 --print-to-pdf=resume.pdf resume.html
