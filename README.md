# story-craft

Two skills for Claude Code and Codex that hold story work to named tests. **story-craft** tests a
story's tension, in any form: prose, script, cutscene, ad, or game narrative. **cutscene-craft**
tests a game's cutscenes and the lines spoken in them and during play. Each one finds weak points,
plans new material, and writes or revises the piece.

## story-craft: six tests of tension

| Test | What it asks |
|---|---|
| In Medias Res | Does the piece enter an action already underway, and leave on its turn? |
| The Bear at the Door | Is there a problem that forces this character to act now, and what in them resists? |
| Opposed wants | Who stands in whose way, between two people or inside one? |
| Dramatic irony | Who knows what, and when does the audience learn it? |
| Retrospective tension | Which earlier moment does a discovery change, and what choice does it force now? |
| Plot and inner story | Does each outside event test a habit or a craving, and does each inner shift cost something? |

The skill uses the tests that fit a piece and says which it set aside. It reads a project's story
documents first, keeps to recorded decisions when writing, and may challenge them when diagnosing.
The full text is in [SKILL.md](skills/story-craft/SKILL.md), with the usual ways each test fails
in [the techniques reference](skills/story-craft/references/techniques.md).

## cutscene-craft: nine tests of a cutscene and its lines

| | Test | What it asks |
|---|---|---|
| The cutscene | Earn the cutscene | What does this give the player that playing couldn't, and what must they still know if they skip it? |
| | Picture first | With the sound off, what does the audience understand, and which lines only say what is on screen? |
| | Wants and a turn | Whose wants collide, and what is different at the end? |
| The lines | Act and answer | What is this line doing to the person it is said to, and what do they do back? |
| | The unsaid | What does each speaker want and not say, and what do they talk about instead? |
| | Only theirs | With the names covered, can you tell who is speaking? |
| | Facts as ammunition | Who in the scene needs this fact now, and what do they do with it? |
| | Heard once | Can it be said in one breath, read in one caption, and cut without loss? |
| Lines in play | Heard a hundred times | Is it short enough for a busy player, safe to miss, and bearable on the hundredth hearing? |

The skill plans with the words last: the case for the cutscene, the turn, the beats with no lines,
and only then the lines. A draft comes as two tables, the scene and the lines, with alternates for
the few lines the scene turns on. A redraft keeps to the pictures, recordings and timings that are
already made. Speech is counted at two to three words a second, a caption at two rows of 40
characters, and a cutscene past thirty seconds has to say what its length buys, unless the project
has limits of its own. The full text is in
[SKILL.md](skills/cutscene-craft/SKILL.md), with the usual ways each test fails in
[the techniques reference](skills/cutscene-craft/references/techniques.md) and the tables in
[the forms reference](skills/cutscene-craft/references/forms.md).

cutscene-craft stands alone. Where story-craft is installed too, a scene's structure is left to
it.

## Install

Clone the repository:

```bash
git clone https://github.com/sergkhl/story-craft.git
```

Link the skills into Claude Code's personal skills:

```bash
ln -s "$PWD/story-craft/skills/story-craft" ~/.claude/skills/story-craft
```

```bash
ln -s "$PWD/story-craft/skills/cutscene-craft" ~/.claude/skills/cutscene-craft
```

Link them into Codex's personal skills:

```bash
ln -s "$PWD/story-craft/skills/story-craft" ~/.codex/skills/story-craft
```

```bash
ln -s "$PWD/story-craft/skills/cutscene-craft" ~/.codex/skills/cutscene-craft
```

Either skill works without the other. Start a new session afterwards. The links point at the
checkout, so `git pull` updates the skills.

## Use

In Claude Code:

```text
/story-craft find the weak points in docs/scenes/opening.md
```

```text
/cutscene-craft redraft the lines in docs/scenes/opening.md
```

In Codex:

```text
$story-craft plan the reveal in act three
```

```text
$cutscene-craft write the barks for the two pilots
```

Each also loads by itself. story-craft loads for work on a story's structure: openings, stakes,
conflict, reveals, character arcs, and weak points. cutscene-craft loads for cutscene scripts,
line redrafts, voice-over lines, and barks.

## Trial tasks

Each skill has four tasks in its `evals` folder for checking a change to it.

- [story-craft](skills/story-craft/evals): an opening for a new story, a diagnosis of a flat
  scene, a plan for a reveal, and a season outline whose teaser gives its secret to part of the
  audience.
- [cutscene-craft](skills/cutscene-craft/evals): a diagnosis of a flat cutscene, a cutscene
  written from a brief, a redraft of lines inside fixed pictures and timings, and a set of barks.

Run each with and without the skill and read the results side by side. With Claude Code 2.1.269
or later, `claude plugin eval .` from a skill's folder runs its tasks; these are billed model
runs.

## What they leave out

- Story shapes such as three acts, the hero's journey, and beat sheets. The tests work inside any
  shape and do not choose one.
- Worldbuilding and cast modelling.
- Prose style, and line editing outside a game's spoken lines.
- Conversations the player steers: choices, branches, and hubs.
- Camera work. cutscene-craft says what each picture has to carry and leaves the lens, the angle
  and the cut to the storyboard.
- Interface text, item descriptions, and lore.

## Credits

- The Bear at the Door is a story shape from Jerome Stern, *Making Shapely Fiction* (W. W. Norton,
  1991).
- In medias res goes back to Horace's *Ars Poetica*.
- cutscene-craft's tests of the lines draw most on Robert McKee, *Dialogue: The Art of Verbal
  Action for Page, Stage, and Screen* (Twelve, 2016): the line as an act and its answer, what is
  said and what lies under it, the "third thing", "exposition as ammunition", the beat, and the
  shaping of a line for the ear.
- Karl Iglesias, *Writing for Emotional Impact* (WingSpan Press, 2005): what the audience should
  feel as the measure of a scene.
- Evan Skolnick, *Video Game Storytelling* (Watson-Guptill, 2014): play before show before tell,
  sorting what the audience has to know, and the kinds of voice-over in a game.
- Tobias Heussner, Toiya Kristen Finley, Jennifer Brandes Hepler and Ann Lemay, *The Game
  Narrative Toolbox* (Focal Press, 2015): asking first whether a cutscene is needed, the
  thirty-second rule, the note each voiced line carries for its actor, and the kinds of line heard
  during play.
- Anna Irwin-Schutze, "Storytelling in Games" (talk slides, hosted by Screen Queensland, 2021).
- The caption size comes from the
  [Game Accessibility Guidelines](https://gameaccessibilityguidelines.com/if-any-subtitles-captions-are-used-present-them-in-a-clear-easy-to-read-way/).
- The works named in the reference notes belong to their creators and are cited as illustrations
  only.

## License

MIT. See [LICENSE](LICENSE).
