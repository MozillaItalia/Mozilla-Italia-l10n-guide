# Workflow

**Table of Contents**
<!-- TOC depthFrom:1 depthTo:6 withLinks:1 updateOnSave:1 orderedList:0 -->

- [Workflow](#workflow)
	- [Collaborative translation: the good and the bad](#collaborative-translation-the-good-and-the-bad)
	- [QA: three phases for assuring quality](#qa-three-phases-for-assuring-quality)
	- [The efforts behind a piece of translation](#the-efforts-behind-a-piece-of-translation)
	- [Collaborative translation tools](#collaborative-translation-tools)
	- [Pontoon](#pontoon)
		- [User Interface (UI)](#user-interface-ui)
			- [Phase 1: Translation](#phase-1-translation)
			- [Phase 2: QA](#phase-2-qa)
			- [Phase 3: Implementing QA](#phase-3-implementing-qa)
	- [Poedit](#poedit)
		- [Settings](#settings)
			- [Setting personal info](#setting-personal-info)
			- [Setting project languages](#setting-project-languages)
			- [Setting a translation memory](#setting-a-translation-memory)
		- [UI](#ui)
			- [Marking strings for QA](#marking-strings-for-qa)
		- [Phase 1: Translation](#phase-1-translation)
		- [Phase 2: QA](#phase-2-qa)
		- [Phase 3: Implementing QA](#phase-3-implementing-qa)
	- [MDN](#mdn)
		- [Settings and UI](#settings-and-ui)
			- [Translate description](#translate-description)
			- [Translate content](#translate-content)
			- [Translate tags](#translate-tags)
			- [Version notes](#version-notes)
		- [Tracking changes for the QA](#tracking-changes-for-the-qa)
		- [Phase 1: Translation](#phase-1-translation)
		- [Phase 2: QA](#phase-2-qa)
		- [Phase 3: Implementing QA](#phase-3-implementing-qa)

<!-- /TOC -->

## Collaborative translation: the good and the bad

Collaborative translation, especially in a context of volunteer-run communities, may be an incredibly enriching experience.
Yet, in group activities, the chances of disorganization exponentially increase and structural flaws may render unusable the localized material, thus putting in jeopardy the sincere and good efforts of individual translators.

Among the most common problems we encounter term inconsistency (each localizer gives a different translation of the same term, causing confusion in the end user), incompleteness (without coordination between translators, important parts are left untranslated, compromising the general comprehension of the topic), poor quality (due to inexperience or lack of knowledge of translation standards or technic expertise by volunteers, but also errors and typos due to distraction or rush).

## QA: three phases for assuring quality

In order to avoid the above issues, each organization or association should define its own corporate identity and conform terminology of its products and initiatives to terminological standards and linguistic registers, for example by adopting an official glossary and a set of guidelines.

Also, to grant the compliance with said standards, a QA process should be implemented.  
QA is an acronym for *Quality Assurance*.

In Mozilla Italia, no matter if the translator is experienced or a newbie, each piece of translation going public must first undergo a QA by an experienced reviewer.

It follows that each translation project involves the action of two different figures: a translator and a reviewer. They alternate each other in three subsequent phases, as detailed in the table below.

| Phase | Role | Task |
|---|---|---|
|1. Translation | translator | translates a first draft, then passes it to the reviewer|
|2. QA | reviewer | reads first draft and points out corrections or enhancements |
|3. Correction | translator | reads the edited draft and decides if to implement the changes or else offer an alternative^. |

^ In the latter case, translation is passed back to the reviewer in phase 2 and goes back an forth until a mutually satisfactory solution is reached.

## The efforts behind a piece of translation

In the above paragraphs we clarified how the localization process doesn’t end in scribbling down a text in your own language.

**Research**  
Even before starting to type, there is an extensive work of research to find terms that are not only accurate, but also coherent with previously translated instances.

This may be obvious, but also a little underrated: the difference between a unremarkable translation and an excellent one is *context*.    
Whenever you find a clause of obscure meaning, or else that lands itself to multiple interpretations, try to find it in it's original context, for example by browsing trough the website or checking an application’s menu entries.  
If you can’t easily find this information for yourself (possibly because it was never shared with you in the first place), don’t hesitate and ask for clarifications to the contact person in charge of the project.

By the way, at Mozilla we have a [newsgroup](https://groups.google.com/forum/#!forum/mozilla.dev.l10n.web) dedicated to localization Q&A, where translators of every locale may pose questions about current localization projects.

**QA**  
After finishing translation we have the QA, that may take even more time than the translation itself.  
During this phase, localizers who are already experienced in the field will offer feedback and suggestions, always providing the reasons for their changes.  
The volunteer will then go back to their draft and implement the requested changes. If they don’t fully agree with a correction, they may offer an alternative, provided they address the issue behind the reviewer’s correction.

**Updates**  
But even the QA may not be the end of it. In many cases, such the localization of a web site or a software, the localizable material undergoes several updates that will need translation.  
Thus when offering to translate a project in Mozilla Italia (or similar organizations), please keep in mind that you commit to complete the localization not only of the currently available material, but also of future updates.

## Collaborative translation tools

* [Pontoon](#pontoon)
* [Poedit](#poedit)
* [MDN](#mdn)

## Pontoon

**Mozilla only**  

The majority of localization in Mozilla is done through the dedicated online translation platform [Pontoon](https://pontoon.mozilla.org/).

Pontoon extrapolates the translatable content of a web page and breaks it down in small units, called ‘strings’. The user types a translation in the field under each string, then the translation is automatically uploaded in place of the source text.  
The advantages of this method are huge: it enables to translate web and software contents without necessarily knowing coding (HTML, JavaScript etc.), thus radically increasing the number of contributors.

Another perk of Pontoon is the tracking capability. When more users work togheter, it may be a good idea to track in real time who is been doing what, as to avoid overlapping on the same project.  
At the same time attributing to each user their own work is a form of reward by acknowledging their individual contributions.

### User Interface (UI)

To use Pontoon you have first to identify yourself by connecting your [Firefox Account](https://www.mozilla.org/firefox/accounts/) (if you don’t already have it, the Pontoon login screen will redirect you to create a new one).

Pontoon is an intuitive tool, it doesn’t take much time to get accustomed to it. Still, the following paragraphs list somewhat advanced features that empower the user to take full advantage of this collaborative translation software.

**The filter option**  
Sometimes it happens to start from scratch an empty project, however the most common scenario for a volunteer translator is an half translated project, in which you have to quickly browse trough the strings assigned to you. The filter option lets the user select just the relevant strings, sparing you the time to skim through the whole file (which sometimes can be quite large).

The filter bar, showing a grey funnel-shaped icon, is located on the top left part of the translation interface. Just by typing a word in either source or target language, you can filter all the strings containing that particular term, which is very useful to have an overview of the same term used in different contexts, but also to check if it has been translated consistently through the project.

Furthermore, clicking on the funnel icon will prompt a dropdown menu with more options to filter strings by:

- Missing (has no translation yet)

- Fuzzy (translation has been filled automatically according to similar strings in the TM, human review needed)

- Suggested (translations waiting for review)

- Translated (translated and QA’ed strings, ready to go live. Notice they can still be edited if needed.)

**Translation memory and glossary**  
Passing to the right side of the Interface, under the translation input field, notice three tabs.
- *History* (lists past translations for current string from newest to oldest)

- *Machinery* (computer translation of the current string)

- *Locales* (how the current string has been translated in other languages).

*Machinery* in particular may become a precious resource, provided that is used with critical thinking and never taken from granted. Always check the tags over each machine suggestion to find its source:

- `Machine translation` is the tag for suggestions generated by automatic traslation services, such as Bing. Often quite useless.

- `Translation Memory`: is the tag indicating similar strings that have been translated by a human in the past. If makes sense in context, it should be prioritized over other suggestions.  
**N.B.** Beside the tag there is a percentage expressing the level of matching with current string.  
`100%` matching means the two strings are identical, it’s safe to accept the string integrally, provided that it makes sense in context.  
> e.g. the string “Download” has a 100% match, but if in Machinery is intended as a noun, while in current string you know it is a verb, you should better ignore this suggestion.

 `80%` may indicate the difference in a small detail, such a number, preposition, formatting tag etc. that should be fixed before saving the string.  
The lower the match, the more editing it requires. Under `75%` the suggestions require extensive editing.

*Machinery* may also be used as a glossary by typing a term inside the search bar located directly under the tab. Each results may easily be identified by its tags:

- `Mozilla` tags indicate the result comes fro the [Mozilla database](https://transvision.mozfr.org/), it is an official 100% Mozilla approved translation.

- `Microsoft` tags come from the  [Microsoft Language Portal](https://www.microsoft.com/Language/en-US/Search.aspx?sString=%s&langID=it-IT)  
**N.B.** This glossary is an useful resource for every translator working in the informatic field.

- `Translation Memory` marks strings coming from the Pontoon Translation Memory.

- `Open Source` tag indicates results from [amaGama](http://amagama.translatehouse.org/), an online open sourced TM.

#### Phase 1: Translation

Translator:
1. Log in on Pontoon

2. Access personal settings by clicking on the gear icon in the upper right corner, under the user image, then toggles on *Make suggestions*  
**N.B.** New volunteers who have not yet been granted approval priviledges have *Make suggestions* as the only option by default.

3. Browse for the project

4. From filter select *Missing* to list only the strings missing translation.

5. For each string type a translation, then save it with the blue button *Suggest*. The string will be recored under the tab History. Each string submitted shows name of the author and saving time.  
**N.B.** You can enter more than one suggestion, it will not overwrite the previous one.  
You can also delete an obsolete suggestion at any time by clicking on the small trashcan icon beside it.

#### Phase 2: QA

Reviewer:
1. Log in on Pontoon

2. Browse for the project

3. From filter select *Suggested*, to isolate the strings previously left by the translator

4. You have two possible choices:
 - If suggestion is acceptable, confirm it as *Translated* with the green button *Save*.

 - If you would rather suggest an alternative, type it over the translation, then switch to Suggest mode and hit the blue *Suggest* button. Your version will *not* overwrite the translator’s work, but instead will appear at the top of the list under the *History* tab.

#### Phase 3: Implementing QA

Translator:
1. In the project select *Suggested* from filter. Then compare your entries with those of your reviewer for changes.

2. You have two choices:
  - If you agree with the changes, confirm the reviewer’s version by clicking on the check icon beside it. If you have yet not been granted saving priviledges, simply do nothing and pass to the next one.

  - If you would rather suggest an alternative, type it over, then hit the blue *Suggest* button. Then resubmit it to the reviewer, back in Phase 2, step 4.

Repeat until a consensus is reached.

## Poedit
[PoEdit](https://poedit.net/) is the main offline editor for managing `.po` catalogs. It is free and multiplatform.

In Mozilla is generally preferred to use the real time translation platform Pontoon, but there are many instances in which Poedit may be an ideal, free tool for collaborative translation.

Just to make a few examples, it could be used by small organizations without a dedicated translation platform. Being an offline editor, it’s useful if you don't have access to a stable Internet connection, also it’s perfect for working on a file one person at time.

### Settings

#### Setting personal info

First of all, you may want to set your personal info that will be included in the strings’ metadata, such as name and email address, to receive proper credit for your translation. You can do that from the menu  
*Poedit > Preferences > General*

Also it is recommended to check the option *Check spelling*.

#### Setting project languages

From menu *File > Open…* browse to the .po file needing translation.

From menu *Catalog > Properties…* check if the parameters for your language are correct.  
In particular pay attention to the following fields:


**Language:** select your locale from the dropdown menu  
**Plural forms:** check the correct plural forms formula [here](http://docs.translatehouse.org/projects/localization-guide/en/latest/l10n/pluralforms.html?id=l10n/pluralforms)  
**Charset:** UTF-8


#### Setting a translation memory

Like Pontoon, Poedit has a translation memory function wich automatically suggests similar previously translated strings.
An important difference is that, while Pontoon automatically taps into the most recent version of the Mozilla TM, in Poedit the task of loading and periodically updating the proper TMs falls on the user.

To add a TM to Poedit:

- Select from menu *Poedit > Preferences > TM*.

- Check *Use translation memory*  
**N.B.** From now on, all the string you translate in Poedit will be stored in the local translation memory for future reference.

- Click on the *Learn From Files…* button and browse for an already translated .po file (it could also be *partially* translated) to import it in your TM.  
**N.B.** Whenever available, you should import in a TM previous translations of the same project or organization for terminological consistency’s sake.  
Still, especially if you are new in the field, you may find useful to import .po files of similar organizations or documentation that you would like to take as a model. e.g. a translator of Firefox-based Add-ons could download and import for reference [Mozilla's AMO .po files](https://pontoon.mozilla.org/projects/amo/).

Next time you open a .po file in Poedit, when a match is found, it will appear in the right column *Translation suggestions:*.  
Under each match you will find a concordance rate. As explained in the Pontoon section, a 100% concordance rate means identical to the current string. Down to the 80-75% concordance, the suggestion is usable with minor adjustments (a single word, a plural form etc.) Under 60% a suggestion is usually just good as a reference for how to translate single terms.  
**N.B.** Even in case of 100% concordances, you should always verify the correctness of the match against source language (the TM may contain an error after all), and in the context of the strings (two instances of the same string may belong to completely different contextes, thus requiring different translations).

### UI

Poedit’s UI is structured in three columns:
- *Source Text*: the strings to translate
- *Translation*: the field where your translation will be recorded.
- *Translation suggestions:* concordance matches for current strings, took from the TM.

In the lower part of the UI is highlighted the current string and, below, a field where to type your translation. A pane on the right sometimes contains notes to the translator, usually providing useful information on the context of current string.

#### Marking strings for QA

Especially when working on an extensive, partially translated, catalog, marking strings for QA, so that your reviewer won't have to reread the whole file, becomes a commodity. Fortunately, Poedit offers this option.

To mark a string needing QA, select it, then go to menu *Edit > Translation needs work*.  
Alternatively toggle the switch button *Needs Work* on the top right of the translation input field, or yet use the keyboard shortcut `cmd + U`.  
The string will now appear in a different color.

You can sort out strings, putting first those needing review or those still untranslated, from menu *View > Untranslated Entries First*.



### Phase 1: Translation

The translator:
1. Open the .po file
2. In case the file is already partially translated, filter untranslated strings from  *View > Untranslated Entries First*
3. Type a translation in the *Translation:* field
4. Mark translation for review (shortcut `Cmd`+`U` )
5. Run a quick automatic check from *Catalog > Validate translations*
6. Save your work from *File > Save*
7. Send the saved .po file to the reviewer.

### Phase 2: QA

The reviewer:
1. Open the .po file
2. filter the strings in need of QA from *View > Untranslated Entries First*
3. you have two possible choices:
  - if translation is acceptable, mark it as ready from *Go > Done and next* (keyboard shortcut `cmd`+`Enter`, or else by toggling the switch button *Needs Work*)
  - if you want to change something, type directly over the translation, then *remember to re-mark the string as not ready*. Please note that your correction will overwrite the original translation.
4. Run a quick automatic check from *Catalog > Validate translations*
5. Save your work from *File > Save*.
6. If all the strings have been translated, you can deploy it. In case you have changed something, send back the edited file to the translator for phase 3.

### Phase 3: Implementing QA

The translator:
1. Open the .po file received from the reviewer.
2. Filter edited strings from *View > Untranslated Entries First*
3. You have two possible choices:
  - if you agree to the changes, mark the string as ready from *Go > Done and next* (keyboard shortcut `cmd`+`Enter`, or else by toggling the switch button *Needs Work*)
  - if you want to change something, type directly over the translation, then *remember to re-mark the string as not ready*.
4. Run a quick automatic check from *Catalog > Validate translations*
5. Save your work from *File > Save*, then send the file back to the reviewer.
6. If you made changes, we go back to phase 2 and repeat until strings are 100% translated and confirmed.

## MDN

[Mozilla Developer Network](https://developer.mozilla.org) is a wiki-based translation platform that anyone can contribute to with docs on the Open Web.

MDN thrives thanks to the contributions of developers that publish articles on its pages, but an important part is also played by volunteer localizers that make those articles available in their own language, thus enabling developers from different Countries to access it.

Due to the technical nature of the documentation (not to mention the fact that it will be used in actual developing), a localizer must have an adequate understanding of the topic. Also, the QA process must be meticulous.  

Moreover, MDN docs are always rapidly evolving to reflect current development in technology. It is thus necessary to keep the translations up to date with the original article.

**N.B.** To automatically receive notifications when one of your article needs to be updated, click on the eye-shaped icon on the upper right, then select *Subscribe to this article*

### Settings and UI

MDN is a [wiki](https://en.wikipedia.org/wiki/Wiki), that is, a type of website that provides collaborative modification of its contents (even in multiple languages) by registered users.

To access MDN you will need to log in using your GitHub credentials (if you still don't have it, [register a GitHub account for free](https://github.com/join?return_to=%2Flogin%2Foauth%2Fauthorize%3Fclient_id%3D21df88df73c82ea9fd75%26redirect_uri%3Dhttps%253A%252F%252Fdeveloper.mozilla.org%252Fusers%252Fgithub%252Flogin%252Fcallback%252F%26response_type%3Dcode%26scope%3Duser%253Aemail%26state%3D6RALVyGgStTO&source=oauth)).

Once authenticated, fill in a personal profile by clicking on your user icon on the top right of the page.
MDN tracks every single contribution and links it to your user profile.

Now you are ready to browse MDN searching for a page in need of translation.  
Or, even better, to be sure your work will have a positive impact, you could get in contact with your language's developer community and ask them if they need a particular content translated.

The translation process is carried out through a web interface and uses a simplified *markup* syntax. The translation UI is divided in the three below sections.

#### Translate description

 This brief, but fundamental, part contains the metadata to translate.

- Title: translate the page title in target language
- Slug: the final portion of the page's URL, ideally should be contain the words of the translated title, replacing white spaces with the character `_`.

E.g.
>EN  
Title: Responsive Design mode  
Slug: responsive_design_mode  

>IT
Title: Visualizzazione flessibile  
Slug: visualizzazione_flessibile

#### Translate content

This is the body of text, the ‘proper’ translation if you will.
The contents are framed by a text editor employing a markup syntax. Note the layout has two columns, source and target text facing to make comparison easier.

For this part, several approaches are possible. You are welcome to choose the one you feel more comfortable with.

If you don’t know any markup syntax and do not want to use any particular translation tool, the most straightforward solution is to type your translation directly in the online editor.  
You can use the formatting ribbon on top of the translation panel to format text, like a in a normal rich text editor such as Microsoft Word or Libre Office.

Alternatively, if you are savvy about markup, you can directly edit the source text by clicking the source button on the upper left of the formatting ribbon, then preview the changes with the Preview button located at the bottom right of the page.

If, for any reason, you would rather work offline, simply select the whole text contained in the translation panel, then copy-paste it into your text editor of choice.  
When you’re finished, copy back in place your translation and generate a preview pressing the Preview button at the bottom right of the page. If everything is in order, proceed by pressing the Save button.

A more advanced step is to use a Computer Assisted Translation (a.k.a. CAT) tool like the open source OmegaT to take advantage of translation memories and glossaries.
(A section on using OmegaT for wiki-based translation is planned for future version of the guide.)

#### Translate tags

Tags are keywords helping users to reach relevant results during a search.  
Tag translation is by no means an exact science. Rather than translating literally each tag, you should think of what key words your target language users would use to search for that topic. Don’t worry about the number of tags, you can add as many as you think are relevant.

#### Version notes

- **Localization flags:** remember to check *Localization in progress - not completely translated yet*, since your translation must still pass the QA to be considered ready.
- **Review needed:** select the type of translation you require: ‘Editorial’ is the usual grammatical and stylistic review.  ‘Technical’ involves the help of a technologist.
- **Revision comment:** a short, informative note on the changes made in the translation session. (More on this in next session)

### Tracking changes for the QA

Previously commented translation tools offered the option to mark single strings for revision. MDN has a slightly different way of tracking changes, based on the page history.

Every time a contributor saves some change to a page, this is recorded as a new ‘version’ on the Page History. Each version is identified by the name of the author, date and time of saving and lastly by a Revision Comment.

It is possible to compare the different versions to highlight the portions of text that have been changend. Thus, the importance of writing a clear, informative message on each save: it is a general good practice to track down the translation process.  

> Good examples of revision comments are “first draft”, “conforming terminology to official glossary” etc.

To highlight changes:
- Clic on the gear icon at the top right of a MDN page. Then, from the dropdown menu select *View page history*.
- Select the two versions to compare (for QA purpose, those will be the first draft and the revision)
- Press *Compare selected translations*.  

This will genereate a file called *diff*, in wich the two versions are displayed in facing columns. The not matchin portions of text will be highlighted in different colors, making evident what’s been deleted (in red) and what’s been added in the most recent version.


### Phase 1: Translation

The translator:
1. Log into MDN

2. Browse for the page you want to translate

3. Click on *Languages* on the upper right. From here there are two possibilities:
  * if your language is already displayed in the dropdown menu, this means a translation already exists. Select it and have a look anyways. The translation may require some enhancements.

   * if your language is not displayed in the list, select *Add a translation* and set the target language.

4. Fill in all the required fields detailed in [Settings and UI](#settings-and-ui) and translate the body of the page.

5. Press the Preview button to see if the page displays correctly. Also check if the links are working and if they redirect to your language’s page (when available).

6. In *Localization flags* check *Localization in progress - not completely translated yet.*

7. In *Review needed* select * Editorial*. If you are unsure and would like the opinion of a developer, also check *Technical*.

8. Leave a comment, such as “First draft” in *Revision Comment*.

9. Press *PUBLISH* on the upper right.

10. Inform the reviewer that the page is ready for the QA.

### Phase 2: QA

The reviewer:
1. Log in on MDN
2. Browse for the page waiting for review
3. Click *EDIT*
4. Make the necessary changes.
5. In *Localization flags* check that *Localization in progress - not completely translated yet.* is still selected. If you think an expert opinion is needed, also check *Technical*.
6. Leave a comment (e.g. “First QA”) in *Revision Comment*.
7. Press *PUBLISH*.
8. Inform the translator that the QA is completed.

### Phase 3: Implementing QA

The translator:
1. Log in on MDN
2. Browse for the QA’ed page.
3. Check the changes using the [Page History](#Tracking_changes_for_the_QA).
4. Go back to the page and press *EDIT*.
5. You have two possible choices:
 * if you agree to all changes, deselect *Localization in progress* and press  *PUBLISH* to mark the translation as complete.
 * if you don’t agree with a change, overwrite it with a valid alternative.
6. Check that *Localization in progress* is still selected in *Localization flags*.

7. Leave a comment in *Revision Comment*, explaining as briefly as possible the nature of your changes.

8. Press *PUBLISH*.

9. Get in contact with your reviewer. If necessary explain more in detail the reasons of your edits.

The process will repeat itself from phase 2 until none of the parties have any more changes to make. Both parties will use the history feature to compare the other's last version with their own to track changes.
