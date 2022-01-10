## What's new

### Version 4.0

**Version 4.0 has been released. SRE is now fully in Typescript**.

For full details on changes see the [release
notes](https://github.com/Speech-Rule-Engine/speech-rule-engine/releases/tag/v4.0.0). But in
a nutshell here is a summary of changes:

* SRE moves to ES6 using TypeScript and webpack:
    * API now uses promise for engine setup
    * Single bundle file for both node and browser
    * Support for alternative bundlers
* New locales for Norwegian (Bokmal and Nynorsk), Swedish, and Catalan
* Support for two dimensional formula layout in Nemeth Braille
* Major rewrite of rule handling
    * Smaller memory footprint of indexed rules
    * Smaller locale files
* All localisation now in a [dedicated repository `sre-l10n`](https://github.com/Speech-Rule-Engine/sre-l10n/)
    * Bespoke YAML format for speech rules for easier translation
    * CrowdIn support for simple message translations
* New API methods for generating word representations of numbers, ordinals, and vulgar fractions
* Internet Explorer support deprecated


#### Acknowledgements

Thanks to the following organisations for their support:

* [NumFocus](https://numfocus.org) for a "Small Development Grant" that financed a one week sprint to make the initial conversion to TypeScript possible
* [TextHelp](https://texthelp.com) for their support on
    * refactoring the rule engine, redesigning the rule format and [CrowdIn](https://crowdin.com/) integration
    * localisations into Nordic languages
* [Statistical Institute of Catalonia](https://www.idescat.cat/) (Idescat) for providing the Catalan translations
* [American Action Fund](https://www.actionfund.org/) for supporting the ongoing Nemeth work.
* [MathJax](https://mathjax.org) for their continuing support of the system.



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
pages](https://github.com/Speech-Rule-Engine/speech-rule-engine).


## Language Support

Besides the rules originally designed for the use in ChromeVox, it also has an
implementation of the full set of Mathspeak and Clearspeak rules,
localisation into a number of languages and Braille output currently in Nemeth.

### Languages

* English
* Catalan (Mathspeak only)
* French
* German
* Norwegian Bokmål
* Norwegian Nynorsk
* Spanish (Mathspeak only)
* Swedish
* Italian
* Hindi

Others are in preparation. If you want to help, please contact us.

All localisation are done in the [dedicated repository
`sre-l10n`](https://github.com/Speech-Rule-Engine/sre-l10n/) using a bespoke
[YAML format](https://speech-rule-engine.github.io/sre-l10n/yaml.html) for rules
and [CrowdIn support](https://crowdin.com/project/speech-rule-engine) for simple
message translations.


### Braille

* Nemeth: both linear for Braille displays and two dimensional for embossing

If you want to help adding more, please contact us.


## Semantic Library

SRE contains a library for semantic interpretation to re-represents any
mathematical expression in its own internal semantic format, overcoming the poor
design of presentation MathML by fully disassembling and reconstructing an
expression. For a better understanding of the representation have a look at its
[visualiser](https://speech-rule-engine.github.io/semantic-tree-visualiser/visualise.html)
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
