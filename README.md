# Intl Enumeration API Specification
List supported values of options in pre-existing ECMA 402 API.

## Stage 1 
* [Moved to Stage 1 after reaching consensus in TC39 June 2020 meeting](https://docs.google.com/presentation/d/17bkiVWuYxhMc24If72d6oENK3G6G-irO2EB4EEQCgxU/edit#slide=id.g881894be7c_0_156). 
* Plan to propose to Stage 2 in TC39 Sept 2020 meeting.

### Entrance Criteria for Stage 1
* Identified “champion” who will advance the addition
  * Frank Yung-Fong Tang
* Prose outlining the problem or need and the general shape of a solution
  * See this document
* Illustrative examples of usage
  * See this document
* High-level API
  * See this document
* Discussion of key algorithms, abstractions and semantics
* Identification of potential “cross-cutting” concerns and implementation challenges/complexity
* A publicly available repository for the proposal that captures the above requirements 
  * https://github.com/tc39/proposal-intl-enumeration
### Entrance Criteria for Stage 2
* Above
* Initial spec text
  * https://tc39.es/proposal-intl-enumeration/

## Motivation


## Overview

```
Intl.getSupportedCalendars()
Intl.getSupportedCurrencies()
Intl.getSupportedNumberingSystems()
Intl.getSupportedTimeZones([options])
Intl.getSupportedUnits()
```


## Background

https://github.com/tc39/ecma402/issues/435

## Usage example
```
// Find out the supported calendars
Intl.getSupportedCalendars()
// ['buddhist', 'chinese', 'coptic', 'dangi', 'ethioaa', 'ethiopic', 
//  'gregory', 'hebrew', 'indian', 'islamic', 'islamic-umalqura',
//  'islamic-tbla', 'islamic-civil', 'islamic-rgsa', 'japanese', 
//  'persian', 'roc', 'islamicc'];

// Find out the supported currencies
Intl.getSupportedCurrencies()
// ['AED', 'AFN', 'ALL', 'AMD', 'ANG', 'AOA', 'ARS', 'AUD', 'AWG', 
//  'AZN', 'BAM', 'BBD', 'BDT', 'BGN', 'BHD', 'BIF', 'BMD', 'BND',
//  ...
//  'YER', 'ZAR', 'ZMW', 'SVC', 'XDR', 'XSU', 'ZWL'];

// Find out the supported numbering systems
Intl.getSupportedNumberingSystems()
// ['adlm', 'ahom', 'arab', 'arabext', 'bali', 'beng', 'bhks', 
//  'brah', 'cakm', 'cham', 'deva', 'fullwide', 'gong', 'gonm',
//  ...
// 'thai', 'tibt', 'tirh', 'vaii', 'wara', 'wcho'];

// Find out the supported time zones
Intl.getSupportedTimeZones()
// ['Africa/Abidjan', 'Africa/Accra', 'Africa/Addis_Ababa', 'Africa/Algiers',
//  'Africa/Asmera', 'Africa/Bamako', 'Africa/Bangui', 'Africa/Banjul',
//  ...
//   'Pacific/Truk', 'Pacific/Wake', 'Pacific/Wallis'];

// Find out the supported time zones of region "US"
Intl.getSupportedTimeZones({region: "US"})
// ["America/Adak", "America/Anchorage", "America/Boise", "America/Chicago", 
// "America/Denver", "America/Detroit", "America/Indiana/Knox", "America/Indiana/Marengo", 
// "America/Indiana/Petersburg", "America/Indiana/Tell_City", "America/Indiana/Vevay", 
// "America/Indiana/Vincennes", "America/Indiana/Winamac", "America/Indianapolis",
// "America/Juneau", "America/Kentucky/Monticello", "America/Los_Angeles", "America/Louisville",
// "America/Menominee", "America/Metlakatla", "America/New_York", "America/Nome",
// "America/North_Dakota/Beulah", "America/North_Dakota/Center", 
// "America/North_Dakota/New_Salem", "America/Phoenix", "America/Sitka", 
// "America/Yakutat", "Pacific/Honolulu"]

// Find out the supported units
Intl.getSupportedUnits()
// ['acre', 'bit', 'byte', 'celsius', 'centimeter', 'day',
//  'degree', 'fahrenheit', 'fluid-ounce', 'foot', 'gallon',
//  ...
//  'terabit', 'terabyte', 'week', 'yard', 'year'];
```



## Authors
* Frank Tang (@FrankYFTang)

## Reviewers
*

## Proposal

### Spec
* https://tc39.es/proposal-intl-enumeration/

## References
*

## Implementation Status
* [v8 prototype patch](https://chromium-review.googlesource.com/c/v8/v8/+/2301115)
* [v8 tracking bug](https://bugs.chromium.org/p/v8/issues/detail?id=10743)
* Mozilla
* JSC
* Test262




============================ Ignore Text Below ============================


#### The following are from the template, will be deleted later 

This repo is setup by following instruction on [TC39 template-for-proposals](https://github.com/tc39/template-for-proposals)

  1.  Avoid merge conflicts with build process output files by running:
      ```sh
      git config --local --add merge.output.driver true
      git config --local --add merge.output.driver true
      ```

1.  Add a post-rewrite git hook to auto-rebuild the output on every commit:
      ```sh
      cp hooks/post-rewrite .git/hooks/post-rewrite
      chmod +x .git/hooks/post-rewrite
      ```
  1.  ["How to write a good explainer"][explainer] explains how to make a good first impression.

      > Each TC39 proposal should have a `README.md` file which explains the purpose
      > of the proposal and its shape at a high level.
      >
      > ...
      >
      > The rest of this page can be used as a template ...

      Your explainer can point readers to the `index.html` generated from `spec.emu`
      via markdown like

      ```markdown
      You can browse the [ecmarkup output](https://ACCOUNT.github.io/PROJECT/)
      or browse the [source](https://github.com/ACCOUNT/PROJECT/blob/master/spec.emu).
      ```

      where *ACCOUNT* and *PROJECT* are the first two path elements in your project's Github URL.
      For example, for github.com/**tc39**/**template-for-proposals**, *ACCOUNT* is "tc39"
      and *PROJECT* is "template-for-proposals".


## Maintain your proposal repo

  1. Make your changes to `spec.emu` (ecmarkup uses HTML syntax, but is not HTML, so I strongly suggest not naming it ".html")
  1. Any commit that makes meaningful changes to the spec, should run `npm run build` and commit the resulting output.
  1. Whenever you update `ecmarkup`, run `npm run build` and commit any changes that come from that dependency.
  
  [explainer]: https://github.com/tc39/how-we-work/blob/master/explainer.md
