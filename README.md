# [IJRU Archive](https://archive.ijru.sport)

You have reached the IJRU Archive. This archive attempts to collect
documents published by international Jump Rope / Rope Skipping organisations.
Generally, only documents that has once been publicly published will be
available via this archive.

## Principles

* **Non-revisionistic**: Items will not be removed or replaced, even if the
  future considers them embarrassing.
* **Consistent**: The structure and naming used in this archive should be
  consistent.
* **Persistent**: If you link to an item in this archive, you should feel
  confident that the link will continue to work.
* **Redundant**: The archive should strive to create copies of itself with
  organisations who's goal is archiving.
* **Unbiased**: The archive should strive to create an accurate record of all
  past and future rope skipping organisations, with a priority on international
  ones.

## Contributing

This archive is far from complete, several organisations and several items of
interest are missing. Known missing items are listed under issues.
If you have access to items that you believe might be of interest to the
archive, please contact us on [archive@ijru.sport](mailto:archive@ijru.sport) or
create a pull request. If you intend to create a pull request, make sure you
adhere to the naming scheme and guidelines set out below.

### Naming Scheme

#### Files

For files, the following structure sets a baseline, if you have a file that
cannot be named with the following structure, contact the maintainer(s) of
the archive to work out a suitable solution and establish a convention for the
future.

When choosing files, try to select editions in open and widely used formats such
as pdf, mp3, wav, json. Try to avoid proprietary formats such as docx or xlsx.
If you have a zip file or other archive filetype, prefer unzipping it and
including its contents directly as this makes them easier to search for and
catalogue.

1. **Version**&mdash;different organisations use different ways of
  indicating version, the two main ones are version number or year(s).
  Some files also doesn't have a "version", competition results is a good
  example of this. Use the year in those cases. If results are revised after
  their initial publication you could append a "tag", such as `-revised`.
  The version should be written in brackets (`[]`), followed by a single space.
  Examples:<br/>
  `[1.1] `: version 1.1<br/>
  `[1.1-pr.1] `: version 1.1 with tag pr.1 (could be pre-release 1)<br/>
  `[1.1-dec2020] `: The December 2020 edition of version 1.1<br/>
  `[2020] `: 2020's edition<br/>
  `[2019-2020] `: version effective 2019-2020<br/>
  `[2019-2020-v2] `: version 2 of the 2019-2020 version
2. **Language** _(optional)_&mdash;If the file is published in
  multiple languages, include the language's two-letter
  [ISO 639-1][iso-639-list] language code in parenthesis (`()`), followed by a
  single space. Examples:<br/>
  `(en) `: English<br/>
  `(de) `: German
3. **Organisation Acronym**&mdash;Include the acronym of the organisation in
  capital letters, followed by a single space. Examples:<br/>
  `IJRU `: International Jump Rope Union<br/>
  `FISAC-IRSF `: International Rope Skipping Federation<br/>
  `WJRF `: World Jump Rope Federation
4. **Name of File Collection** _(optional)_&mdash;If the file is part of a
  "collection" include the name of that collection in full, followed by a space,
  a dash, and another space. Examples:<br/>
  `Rule Book - `,<br/>
  `Timing Tracks - `,<br/>
  `World Championships Results - `
5. **Name of File**&ndash;The fully spelled out, human readable name of the
  file. Examples:<br/>
  `Constitution`,<br/>
  `Judging Manual`,<br/>
  `Single Rope Speed Relay`,<br/>
  `Mixed Team`
6. **File Extension**&mdash;End with the file extension. Examples:<br/>
  `.pdf`, `.mp3`

Complete Examples:

* `[1.0] IJRU Constitution.pdf`
* `[1.1] (de) ERSO Constitution.pdf`
* `[2016] WJRF Junior World Jump Rope Championship Results - Male Single Rope Speed Sprint.pdf`
* `[1.0.0-draft.1] IJRU Rule Book - Competition Manual.pdf`
* `[2016] FISAC-IRSF Timing Tracks - Double Dutch Speed Relay 4x45.mp3`

[iso-639-list]: https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes

#### Directories

As for directories, try to name them using "url-safe" characters, in general try
to use only lowercase letters (`a-z`), numerals (`0-9`) and dashes (`-`) to form
english words. Use pluralised forms for folders that might contain several types
of that file category, use singular for one specific document type and its
versions. Use singular for names.

Complete examples:

* `ijru`
* `by-laws`
* `2020`
* `rule-books`
* `ethics-panel`

### Sorting

In short, create subdirectories to logically group documents together, but don't
just create subdirectories to create subdirectories. **Try to have a maximum
of three levels of directories** unless it cannot be avoided or makes it harder
to navigate. the general structure is that the first level is the organisation,
the second level is the "category"/"type" and the third level is "collection"
if the file in question is made up of several files for each version.

For example: `ijru/constitution/` only really needs two levels as it's unlikely
the constitution will ever consist of multiple documents, but
`ijru/rule-books/v1.0.0/` is well justified to have a third level as it consists
of both a Judging Manual and a Competition Manual, and it's likely it will have
different types of rule books in the future. Competition results are also a good
example of something where three levels are justified as each competition as
they commonly consists of one file per competition event.

### Commits

Try to use scoped commit names, start with lowercase organisation, optionally
add which collection (directory) you are adding files to in parenthesises, and
after that provide a short one line description about the document(s) you're
adding. If you need to provide a detailed list or more information enter that
in the body/following lines of the commit, separated by a blank line.

Try to only add files to one collection at a time, as in try to make sure each
commit contains only files related to each other.

Examples:

```
ijru(constitution): Add v2.0 of IJRU Constitution
```

```
ijru(rule-book): Add v3.0.0 of IJRU Rule Book

Includes Judging Manual and Competition Manual
```

```
wjrf(results): Add 2008 WJRCC results
```
