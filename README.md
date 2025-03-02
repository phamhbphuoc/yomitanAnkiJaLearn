# yomitanAnkiJaLearn
My notes on using Yomitan and Anki to learn Japanese

## Anki

### Add-on
- [AnkiConnect](https://ankiweb.net/shared/info/2055492159)
- [Edit Field During Review Cloze](https://ankiweb.net/shared/info/385888438)
-   Go to add-on config
-   Enable for all fields
-   During reivew, cmd + click on a field to edit the field directly

### Note Types
- Create a new Note Type by choosing `Add: Basic (optional reserved card`
- Pick a new, e.g. `Yomitan`

### Fields
In the `Yomitan` Note Type, set up fields with following name, and formats
```
1. Front - Size: 36 - Japanese Font if you have it
2. Back - Size: 12 - Arial or anything you like
3. Add Reverse - No change
4. Sentence - Size: 14 - Japanese font
5. Sentence No Word - Size: 14 - Japanese font
6. Reading - Size 18 - Japanese font
7. Extra - No change
```
### Cards
In the `Yomitan` Note Type, create the following card templates
#### Japanese Front - English Back
##### Front Template
```
<div class="frontbg">
  <div style="font-family: BIZ UDGothic; font-size: 48px">{{edit:Front}}</div>

  <br />

  <div style="font-family: BIZ UDGothic; font-size: 24px">
    {{edit:Sentence}}
  </div>
</div>

```
##### Back Template
```
<div class="frontbg">
  <div style="font-family: BIZ UDGothic; font-size: 48px">{{edit:Reading}}</div>

  <br />

  <div style="font-family: BIZ UDGothic; font-size: 24px">
    {{edit:Sentence}}
  </div>
</div>

<div class="backbg">
  {{edit:Back}}

  <br />

  <div style="font-family: BIZ UDGothic; font-size: 24px">{{edit:Extra}}</div>
</div>
```
##### Styling
```
.card {
  font-family: arial;

  font-size: 20px;

  text-align: center;

  color: #ffffff;

  background-color: #2d2d2d;
}

.frontbg {
  background-color: #18adab;

  padding: 15px;

  border-radius: 7px;

  color: #fff;

  position: relative;

  left: 0;
}

.backbg {
  position: relative;

  top: -6px;

  background-color: #fff;

  padding: 15px;

  padding-bottom: 15px;

  padding-left: 30px;

  padding-right: 30px;

  border-radius: 0px 0px 10px 10px;

  color: #016ea6;

  font-size: 24px;

  text-align: left;
}

```

#### English Front - Japanese Back
##### Front Template
```
{{#Add Reverse}}
<div class="frontbg">
  <div style="font-family: BIZ UDGothic; font-size: 48px">{{edit:Back}}</div>

  <br />

  <div style="font-family: BIZ UDGothic; font-size: 24px">
    {{edit:Sentence No word}}
  </div>
</div>
{{/Add Reverse}}
```
##### Back Template
```
<div class=frontbg>

<div style='font-family: BIZ UDGothic; font-size: 48px;'>{{edit:Back}}</div>

<br>

<div style='font-family: BIZ UDGothic; font-size: 24px;'>{{edit:Sentence}}</div>

</div>

<div class=backbg>

{{edit:Reading}}

<br>

<div style='font-family: BIZ UDGothic; font-size: 24px;'>{{edit:Extra}}</div>

</div>
```


## Yomichan

### Dictionaries
- Kanji dict:
-   [KANJIDIC with Han Viet reading](https://github.com/piji333/yomitan_kanjidic_vi/blob/main/original_dicts/kanji/kanjidic/%5BKanji%5D%20KANJIDIC%20(English)%20(Recommended)/%5BKanji%5D%20KANJIDIC%20(English)%20(Recommended)_vi.zip)
- Name:
- Monolingual:
- Bilingual:

### YOMICHAN ANKI SETTINGS
#### Terms
- `Deck`: Choose which deck to save new card to
- `Model`: Choose `Yomitan` Note Type
- Fields:
-   `Front`: `{expression}`
-   `Back`: `{glossary-brief}`
-   `Add Reverse`: Don't add anything
-   `Sentence`: `{cloze-prefix}({cloze-body}){cloze-suffix}`
-   `Sentence No word`: `{cloze-prefix}（・・・）{cloze-suffix}`
-   `Reading`: `{furigana}`
-   `Extra`: Don't add anything
#### Kanji
- `Deck`: Choose which deck to save new card to
- `Model`: Choose `Yomitan` Note Type
- Fields:
-   `Front`: `{character}`
-   `Back`: `{onyomi}<br>{kunyomi}<br><br>{glossary-brief}`
-   `Add Reverse`: Don't add anything
-   `Sentence`: `{cloze-prefix}({cloze-body}){cloze-suffix}`
-   `Sentence No word`: `{cloze-prefix}（・・・）{cloze-suffix}`
-   `Reading`: `{character}`
-   `Extra`: Don't add anything


## Reference
- Huge credit goes to [ToKiniAndy blog post](https://www.tokiniandy.com/blog/using-yomichan-to-learn-japanese)
  -   [ToKiniAndy Youtube tutorial](https://www.youtube.com/watch?v=OJxndUGN8Cg)
  -   [ToKiniAndy Youtube channel](https://www.youtube.com/@ToKiniAndy)
