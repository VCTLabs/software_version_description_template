# document build target (see corresponding .rst source file)
SVD = EU_SVD.pdf

# just one pdf doc target for now
DOCS = $(SVD)

# figure generation engine; can use other layouts/drivers
DOT = dot

# input files
DOTSRC  := $(wildcard images/*.dot)
SVDSRC = EU_SVD.rst

#DOCTYPE = pdf
# set this to the output image format to include in the doc target
FIGTYPE = svg

# generated input files
FIGS := $(DOTSRC:.dot=.$(FIGTYPE))

# input files for DOC target
SOURCES_MK	:= $(SVDSRC) $(FIGS)
# stuff to clean
GENFILES	:= $(FIGS)

DOTFLAGS = -T$(FIGTYPE)
RSTFLAGS = -s styles/svd.yaml
DOT_OFLAG = -o
PDF_OFLAG = -o

# reset file suffixes
.SUFFIXES:
.SUFFIXES: .pdf .dot .rst .$(FIGTYPE)

# build the figures
images/%.$(FIGTYPE) : images/%.dot
	$(DOT) $< $(DOT_OFLAG) $@ $(DOTFLAGS)

# build the pdf output
$(SVD) : $(SVDSRC)
	rst2pdf $< $(RSTFLAGS) $(PDF_OFLAG) $@

all : $(DOCS)

CLEAN  += $(GENFILES) $(DOCS)

clean :
	rm -rf $(CLEAN)
