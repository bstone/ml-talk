MY_SLIDES=01-title.md \
	03-ML-Intro.md \

HTML_SLIDES = $(MY_SLIDES:.md=.html)
n=2

RELOAD_KEYS="F5"
BROWSER='firefox'
# get which window is active right now
MYWINDOW=$(xdotool getactivewindow)

slides:
	pandoc -s --template=revealjs-template.html --mathml \
		-V controls=true \
		-V progress=true \
		-V hash=true \
		-V center=false \
		-V theme=simple \
		-V revealjs-url=./reveal.js \
		-i -t revealjs $(word 1, $(MY_SLIDES)) $(word $n, $(MY_SLIDES)) -o $(word $n, $(HTML_SLIDES))

all_slides:
	pandoc -s --template=revealjs-template.html --mathml \
		-V controls=true \
		-V progress=true \
		-V hash=true \
		-V center=false \
		-V theme=simple \
		-V revealjs-url=./reveal.js \
		-i -t revealjs $(MY_SLIDES) -o math355-slides.html 
	osascript reload.scpt
	
# 	#
# 	keystroke="CTRL+F5"
# 	#
# 	# set to whatever's given as argument, defaults to firefox
# 	#
# 	# find all visible browser windows
# 	browser_windows="$(xdotool search --sync --all --onlyvisible --class ${BROWSER})"
# 	#
# 	# Send keystroke
# 	for bw in $(browser_windows); do \
# 		xdotool key --window "$(bw)" $(RELOAD_KEYS); \
# 	done 

# 	#
# 	# bring up the browser
# 	xdotool search --name ${BROWSER} windowactivate --sync
# 	# send the page-reload keys (C-R) or (S-C-R)
# 	xdotool search --name ${BROWSER} key --clearmodifiers ${RELOAD_KEYS}
# 	#
# 	# sometimes the focus doesn't work, so follow up with activate
# 	xdotool windowfocus --sync ${MYWINDOW}
# 	xdotool windowactivate --sync ${MYWINDOW}

pdf:
	pandoc -s $(MY_SLIDES) --pdf-engine=pdflatex -o math355-slides.pdf

