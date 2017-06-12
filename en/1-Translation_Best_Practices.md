# Translation best practices

This chapter lists several of the so called “translation best practices”, a set of rules and standards of quality acknowledged not just by Mozilla Italia but also in the professional translation field.

The chapter is meant to be kept close at hand and checked often during translation. Use the table of contents to find quickly the topic you need.

**Table of contents**

- [Quality standards](#quality-standards)
- [Localization](#localization)
	- [Date formats](#date-formats)
	- [Digit formats](#digit-formats)
	- [Proper nouns and Trademark names](#proper-nouns-and-trademark-names)
- [Punctuation](#punctuation)
	- [Period](#period)
	- [Exclamation Point](#exclamation-point)
	- [Apostrophe](#apostrophe)
	- [Quotation marks](#quotation-marks)
	- [Ellipsis](#ellipsis)
	- [Hyphen and dashes](#hyphen-and-dashes)
- [Reformulation of sentences](#reformulation-of-sentences)
	- [Clauses and structure](#clauses-and-structure)
	- [Passive voice](#passive-voice)
	- [Theme of the sentence](#theme-of-the-sentence)
- [Vocabulary and register](#vocabulary-and-register)
- [Linguistic traps](#linguistic-traps)

## Quality standards
A technical translation of good quality must fulfill the following requirements:

1. **Completeness**  
The source text should be translated integrally, without omissions (except for information that undergoes the localization process) or portions left in source language (unless that is meant in the text).  
This means, of course, that the initial text should be 100% translated, *but also that further updates in the source language should be translated before they are made publicly available*.

2. **Unambiguity**  
Users must not have any doubt about the meaning of a term. If a term triggers debate between users, it must be changed.
Translated terms should be grounded in the common usage of the target language.  
In case of technical jargon, terms should be accurately researched in official or authoritative sources, and not swapped with loose, generic equivalents.  
Formatting uses that cause ambiguity should be converted in target language. See [Localization](#localization) for further details.

3. **Usability**  
“Usable” means serving the intended purpose. The purpose of localization is to enable target language speakers to make use of the content as easily and efficiently as possible.  
This also includes applying correct spelling, grammar and punctuation, using a clear and straightforward language, and converting format of relevant information such as dates, measurements, local times, currencies etc.

4. **Consistency**  
Term inconsistency can generate confusion in the user and compromise usability.  
Names of products, titles, menu items, commands etc. should be perfectly consistent inside the same translation project *and* across related translation projects.  
When an official glossary is provided, it should be privileged unless common sense dictates otherwise.  
Parts/buttons/menu items names etc. provided in instructions should match exactly what the user is supposed to find in the actual product.  
Previously translated terms should be maintained unless they contain errors or have otherwise become unsuitable.

## Localization
Localization goes a step further than translation: instead of simply providing the equivalent of a content in another language, it adapts this content to the uses of specific countries or regions.

### Date formats
In all languages dates have the following elements: year (Y), month (M), day (D). However in different countries, they are placed in a different order.

For example, while the most common format is D/M/Y (day, month, year), and in the Far East is prevalent Y/M/D, the USA have a M/D/Y format.

At best, using a format different from your locale may look sloppy, but in some cases, particularly when expressing dates in numbers, it may cause serious misunderstanding.

> e.g. 05/07  
May 7th or July 5th?

### Digit formats
Every language has different uses when coming to digit formatting. This may cause serious misunderstandings.

An important example occurs with the decimal mark.  
Among countries using Arabic numerals, some (like the USA)
use the point `.` to mark decimals and the comma `,` for grouping myriads.

Conversely, in other parts of the world such as Europe, the comma is used as a decimal mark and the point as group delimiter for large numbers.

**N.B.** Current standards endorse the use of spaces as digit group separators in large numbers, while either comma or point are reserved to decimals.

| Region | Decimal | Myriads|
|---|---|---|
| USA etc. | 15.241 | 15,241|
|EU etc. | 15,241 | 15.241 |
|ISO standard | 15.241 / 15,241 | 15 241|

**N.B.** It should be mentioned possible confusion about the word “billion”, which in American and modern British English is defined by the [short scale](https://en.wikipedia.org/wiki/Long_and_short_scales) as *one thousand million*, but sometimes in the UK is also intended by the long scale definition of *one million million* (incidentally, a *trillion* by the short scale).

### Proper nouns and Trademark names

Proper names should never been translated. If you need to transliterate a name in your alphabet, check if an official transliteration already exist. If not, apply the proper transliteration rules of your country.

An exception are historical figures, names of famous cities or landmarks whose translations already entered in common speech, e.g. Alexander the Great, Florence etc.)

Pay particular attention to use the official names of countries to avoid triggering socio-political debates.

Names of programs or products covered by trademark are to be reproduced accurately, taking into account capitalization, spaces between words, hyphens and other symbols.

e.g.
>OK: JavaScript NO: Javascript, Java Script  
OK: PayPal NO: Paypal, Pay Pal  
OK: iPhone NO: iphone o i-Phone

In case the name of a product or functionality has been *officially* localized in target language, use that translation.

e.g.
>EN. Notepad (Microsoft)  
IT. Blocco note

Similarly, titles of books, movies and similar works should be mentioned by their translation if they have been published in target language, or the original title if they have not yet been published in that language.  

>e.g.  
OK: War and Peace  
NO: Voyná i mir

In case the translated work is unknown, you may consider putting the original title between parenthesis or in a footnote, so that readers can learn more on the original work if they wish so.  
Similarly, if a work has not yet been translated but carries a relevant meaning for the reader, you may include a translation between parenthesis or in a footnote.

>e.g. *Life is beautiful* (“La vita è bella”) by Roberto Benigni

Under no circumstances should you improvise a translation for an official product name or title instead of quoting the source, because it causes confusion for the user.


## Punctuation

When translating from a foreign language it is important to keep in mind that different languages have different punctuation rules. Don’t try to reproduce the source language’s punctuation at all costs. Instead apply the punctuation rules of the target language to achieve the maximum clarity of meaning and set a more natural rhythm.

Follow some noteworthy examples of punctuation found in the English language (that may not be so valid in other languages).

In English the comma and conjunction “and” may coexist, e.g.
>For safety, privacy**, and** freedom on the Web

In Italian comma and conjunction, having the same coordinative function, exclude each other, e.g.
>IT: Per la sicurezza, la privacy **e** la libertà sul Web

### Period

As a general rule, periods (also referred to as full stops) are to be avoided at the end of titles or headers.  
e.g.
>OK: Mozilla Italia's l10n guide  
No: Mozilla Italia's l10n guide**.**

The punctuation sequences `.”.`, `.).` and similar are better avoided. When dealing with brackets or quotiation marks it’s better to delete the punctuation mark *inside* the bracket, leaving just the one outside it.  
e.g.
>OK: I replied “You may go now**”.**  
No: I replied “You may go now**.”.**

### Exclamation Point

It's better to avoid long strings of exclamation points, unless you want to achieve a comical effect of overreaction.
>No: Get involved with Mozilla!!!!!!!!!!!!!!

In more serious works, a single exclamation point is more than enough. In some languages, a more formal register requires the exclamation point to be dropped if not really necessary.

e.g.
>EN: Error 404: Page not found**!**  
IT: Errore 404: Pagina non trovata**.**

In truly exceptional cases, you may resort to three exclamation points in a row (no more, no less).  
e.g.
>OK: Ladies and gentlemen, we have a winner**!!!**  
No: Ladies and gentlemen, we have a winner**!!**  
No: Ladies and gentlemen, we have a winner**!!!!**

### Apostrophe
The “straight”, also called typewriter apostrophe `'`, is the more accessible apostrophe mark on the keyboard. Still, it is used in several codes such as HTML and may be misinterpreted as code during elaboration, causing errors.

It is instead advised to use in normal text the “curly” or typographic apostrophe `’` (`U+2019` in Unicode). By the way, the typographic apostrophe also serves as the right single quotation mark.

### Quotation marks

For the same reason as the apostrophe, “curly” or “smart” quotation marks are preferable to the “straight” ones.

In English, quotation marks are used mainly to indicate:
1. Quotation or direct speech
2. Mention of titles
3. non-standard (often ironical) use of a word

In your language the uses, or even forms, of quotation marks can differ. Instead of mirroring the English use, check the correct use for your language in authoritative sources.

>es. In Italian and French direct speech is enclosed by guillemets («…»), while in Japanese and Chinese corner brackets are used (「…」).

**N.B.** Straight quotation marks are interchangeable, while curly quotes comes in two versions: the opening quote and the closing one.

### Ellipsis

Several people uses the set of three dots ‘…’, but not many know that this punctuation mark has its own character. Even if it is not easily accessible from the keyboard, the ellipsis character should be preferred to simply hitting the full stop button three times in a row.

The ellipsis character comes particularly handy when dealing with character limitations (e.g. Twitter’s 140 characters) because, compared to three separate dots, it is calculated as a single character.


### Hyphen and dashes

Hypen and dash are two separate punctuation marks serving different purposes.

The hypen `-` is shorter and is used for joining compound words and hypenation. Has no spaces before or after.

Dashes `–` are longer, preceded and followed by a space, and denote a break in a sentence or a parenthetical statement.

e.g.
>Firefox **–** The browser that puts privacy at the first place

>Firefox **–** the browser that puts privacy at the first place **–** is now available for Android.  


## Reformulation of sentences

### Clauses and structure

Notoriously, English is a language made by short sentences and independent clauses joined with each other.  
Other languages, such as  Italian, favor long, elaborate sentences structured as dependent clauses.  
In the latter type of languages, when following too closely the source text structure, discourse often appears too sloppy, almost fragmented.

To avoid this effect, don’t hesitate to riformulate the sentences as it sounds more natural and fluent in your language.  
For example, if you have two related short sentences, try to join them in a longer sentence, highlighting the logical connection with the appropriate particle.  
Conversely, if you think the source sentence is too long for your language, break it down in smaller sentences to increase readability.

### Passive voice

Some languages resort to passive voice more than others. Generally the passive voice makes the whole sentence less direct and thus harder to understand. Many manuals actually advise *against* using passive voice whenever possible!

The point is, as said in the previous section, if you feel that the source sentence would sound unnecessarily complicated in your language, reformulate it to achieve maximum readability.  
In the case of passive voices, convert to the active voice if it makes the message clearer.


### Theme of the sentence

The theme of a sentence is essentially “what is being talked about”. To achieve maximum readability, it should be properly marked to help the user understand at first glance the topic.  

Now, different languages have different ways to mark a theme, generally by placing it at the beginning of a sentence, but, in languages such as Japanese or Korean, also by using appropriate particles.

Once identified the theme, it is important to mark it according to your language rules, even if you have to swap the original order of the sentence.

A noticeable exception of this rule is when giving long and elaborate instructions. In this case the theme, that is the goal of the instructions, should be stated clearly before the procedure. This way users can determine if it useful for them to read the whole procedure or if they can skip it entirely.

Thus, in cases of instructions it is advisable to follow the order: **Result > procedure**

e.g.
>NO: Go to Menu > Add-ons > Appearance to activate a new theme.

>OK: To activate a new theme go to Menu > Add-ons > Appearance

## Vocabulary and register

Another characteristic of the English language is a marked preference toward a generic vocabulary and a user-friendly approach toward the user. In other nations such an approach could be perceived wrongly.  
For example, in Italian referring to the user in an impersonal form and using technical terms is preferred (even if recently the English user-friendly style is becoming more common), while in Japanese the user is addressed with honorifics and instructions are written in form of invitation (e.g. “Please, click the button.”)

Once again, the general rule is to adapt the style of the content to be best received in the cultural context of the user.  
If more styles are acceptable, ask the commissioner of the localization if they have any preference.

Another use, found prevalently in American English, is the very liberal use of positive adjectives such as “great”, “powerful”, “best”, “awesome” for describing pretty much anything from pieces of software, to initiatives to people. This choice of words may not sound nearly so effective in other languages.

As usual, you should use your common sense and linguistic experience to determine if a certain term works or not in the target culture. However, a general good writing practice is to avoid generic, subjective statements and instead provide a more informative, specific quality.
e.g.
>This software is great!

What makes this software “great”? The possibilities vary depending on the specs of each single software.
>This software is ultra-lightweight!  
>This software has excellent integration capabilities!  
>This software is highly performant!  
>This software is extremely customizable!  
etc.

## Linguistic traps

Lastly a good translator should always pay attention to the so called “linguistic traps”, errors to which foreign speakers are particularly susceptible because certain constructions are either not present in their native language or suspiciously similar but not quite the same.  
Linguistic traps vary between language, but the following are pretty common mistakes in world-wide translation.

First, watch out for the so called *false friend*, words that look or sound very similar in source and target language, but actually have different meanings.  
Each pair of languages has its own set of false friends. It could be useful to research the most common ones for your language (many bilingual dictionaries include a list of false friends).

Second, you should pay particular attention to *phrasal verbs*, a very common English construct of verb + preposition that may change radically the meaning of the same verb.

e.g.
>sign up = register a new account  
sign in = access to your (already existent) account

Anyway, since not even the most experienced professional can know every single term, the best weapon of a translator is the patience and dedication to research every term they are not sure about.  
Also, in certain cases, when you *think* you know a term, but it seems out of place in context, you should reseach that too, because it could have some hidden meaning or use you have not discovered yet.
