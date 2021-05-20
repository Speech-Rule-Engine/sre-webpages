## What's new

### Version 3.3

**Version 3.3 has been released containing Hindi Localisation**.

See the [release
notes](https://github.com/zorkow/speech-rule-engine/releases/tag/v3.3.1) for
more details.

### Upcoming 4.0

**SRE is moving to Typescript**.

The initial move of the codebase to Typescript has been completed. [A first alpha
release is available for
testing.](https://github.com/zorkow/speech-rule-engine/releases/tag/v4.0.0-alpha.1). Please
test and [criticise or
discuss](https://github.com/zorkow/speech-rule-engine/discussions/520).


## Background

Speech rule engine (SRE) is a JavaScript library for generating speech for
mathematical expressions. SRE is a standalone system based on its original
implementation as the maths speech engine in ChromeVox. SRE was forked from
ChromeVox release 1.31.0 SRE can translate XML expressions into speech strings
according to rules that can be specified in a syntax using Xpath expressions.
It was originally designed for translation of MathML and MathJax DOM elements
for the ChromeVox screen reader. However, in combination with
[MathJax](https://mathjax.org) SRE can also work with more commonly use
mathematics markup like LaTeX and AsciiMath.

## Usage

There are three ways of using SRE:

1. **Node Module:** Download via npm or yarn. This is the
easiest way to use the speech rule engine via its Api and is the preferred
option if you just want to include it in your project.

2. **Standalone Tool:** Download via github and build with
make, or simply run it with ```npx```. This is useful if you want to use the
speech rule engine in batch mode or interactively to add your own code.

3. **Browser Library:** This gives you the option of loading SRE in a browser
   and use its full functionality on your websites.

For more information see the [documentation on SRE's github
pages](https://github.com/zorkow/speech-rule-engine).


## Language Support

Besides the rules originally designed for the use in ChromeVox, it also has an
implementation of the full set of Mathspeak and Clearspeak rules,
localisation into a number of languages and Braille output currently in Nemeth.

### Languages

* English
* French
* German
* Spanish (Mathspeak only)
* Italian
* Hindi

Others are in preparation. If you want to help, please contact us.

### Braille

* Nemeth

If you want to help adding more, please contact us.


## Semantic Library

SRE contains a library for semantic interpretation to re-represents any
mathematical expression in its own internal semantic format, overcoming the poor
design of presentation MathML by fully disassembling and reconstructing an
expression. For a better understanding of the representation have a look at its
[visualiser](https://zorkow.github.io/semantic-tree-visualiser/visualise.html)
where you can easily use LaTeX syntax for generating mathematics. The semantic
trees can be used in their own XML format directly or used to enrich the input
MathML expressions with semantic information and speech strings.

## Browser Support

SRE provides extensive browser support not only for translating mathematics into
text but also for navigating, highlighting and semantically restructuring
expressions. For more details and an overview of the interface [see here](www/keybindings.html).


## Working files

The most recent test results are available at [SRE's test
site](https://speech-rule-engine.github.io/sre-tests/output/).
