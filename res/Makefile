
TARGETS = $(addsuffix .svg, $(wildcard *.dot))

all:	$(TARGETS)

%.dot.svg:	%.dot
	dot -Tsvg -O $<
