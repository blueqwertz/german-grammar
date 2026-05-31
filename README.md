# German Grammar

A skill for Claude Code, OpenCode, Codex, and Antigravity that corrects German spelling, grammar, and punctuation according to the official Amtliches Regelwerk 2024 (German Orthographic Rules 2024), published by the Council for German Orthography (Rat für deutsche Rechtschreibung).

## Installation

```bash
npx skills add blueqwertz/german-grammar
```

### Manual Installation

#### Claude Code

```bash
mkdir -p ~/.claude/skills
git clone https://github.com/blueqwertz/german-grammar.git ~/.claude/skills/german-grammar
```

#### OpenCode

```bash
mkdir -p ~/.config/opencode/skills
git clone https://github.com/blueqwertz/german-grammar.git ~/.config/opencode/skills/german-grammar
```

#### Codex

```bash
mkdir -p ~/.codex/skills
git clone https://github.com/blueqwertz/german-grammar.git ~/.codex/skills/german-grammar
```

#### Antigravity

```bash
mkdir -p ~/.antigravity/skills
git clone https://github.com/blueqwertz/german-grammar.git ~/.antigravity/skills/german-grammar
```

> OpenCode also scans `~/.claude/skills/`, so a single clone into `~/.claude/skills/german-grammar/` works for both tools.

## Usage

```
/german-grammar

[paste German text to check]
```

Or ask the model directly:

```
Check this German text for spelling and grammar errors: [your text]
```

## What It Covers

All six regulatory areas from the Amtliches Regelwerk 2024:

| Section | Topic | Beschreibung |
|---------|-------|-------------|
| **A** | Laut-Buchstaben-Zuordnungen | Sound-letter mappings, consonant doubling (ck/tz), ß vs. ss, long/short vowels, Dehnungs-h, foreign word integration |
| **B** | Getrennt- und Zusammenschreibung | When to write compounds as one word vs. separate words (verbs, adjectives, nouns) |
| **C** | Schreibung mit Bindestrich | Hyphenation in compounds, proper names, abbreviations, numbers |
| **D** | Groß- und Kleinschreibung | Capitalization of nouns, nominalizations, proper names, address pronouns |
| **E** | Zeichensetzung | Commas, periods, semicolons, colons, dashes, quotation marks, apostrophes |
| **F** | Worttrennung am Zeilenende | Word division at line breaks by syllables |

## Examples

### Before:
```
Er sagte das er heute nicht komen kann. Ich habe in erfahrung gebracht, dass man schnell Autofahren soll wenn die Ampel grün ist.
```

### After (Corrected):
```
Er sagte, dass er heute nicht kommen kann. Ich habe in Erfahrung gebracht, dass man schnell Auto fahren soll, wenn die Ampel grün ist.
```

**Corrections:**
- *das* → *dass* (Konjunktion, § 25)
- *komen* → *kommen* (Konsonantenverdopplung nach kurzem Vokal, § 2)
- *in erfahrung* → *in Erfahrung* (Großschreibung Substantiv, § 55)
- *Autofahren* → *Auto fahren* (Getrenntschreibung Substantiv + Verb, § 34)
- Komma vor *dass* und *wenn* (Nebensätze, § 73)

## Swiss German Note

In der Schweiz gilt grundsätzlich *ss* statt *ß* (z. B. *Strasse* statt *Straße*, *gross* statt *groß*). Guillemets (*«»*) werden in der Schweiz für Anführungszeichen verwendet.

## License

MIT

## References

- [Amtliches Regelwerk der deutschen Rechtschreibung 2024 (PDF)](https://www.rechtschreibrat.com/DOX/RfdR_Amtliches-Regelwerk_2024.pdf)
- [Rat für deutsche Rechtschreibung](https://www.rechtschreibrat.com/)
- ISBN: 978-3-948831-65-3 (Print), 978-3-948831-66-0 (PDF)
- DOI: 10.14618/s99n-fk38
