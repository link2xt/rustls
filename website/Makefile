PULLDOWN=pulldown-cmark --enable-gfm --enable-tables --enable-footnotes --enable-strikethrough --enable-metadata-blocks

all: perf

perfs := $(patsubst %.md,%.html,$(wildcard perf/*.md))

perf: $(perfs)

%.html: %.md
	cat perf/head.html > $@
	$(PULLDOWN) $< >> $@
	cat perf/foot.html >> $@
