# story-craft

A skill for Claude Code and Codex that holds story work to six tests of tension. Use it to find a
story's weak points, to plan new material, or to write and revise scenes, in any form: prose,
script, cutscene, ad, or game narrative.

## The six tests

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

## Install

Clone the repository:

```bash
git clone https://github.com/sergkhl/story-craft.git
```

Link the skill into Claude Code's personal skills:

```bash
ln -s "$PWD/story-craft/skills/story-craft" ~/.claude/skills/story-craft
```

Link it into Codex's personal skills:

```bash
ln -s "$PWD/story-craft/skills/story-craft" ~/.codex/skills/story-craft
```

Start a new session afterwards. The links point at the checkout, so `git pull` updates the skill.

## Use

In Claude Code:

```text
/story-craft find the weak points in docs/scenes/opening.md
```

In Codex:

```text
$story-craft plan the reveal in act three
```

It also loads by itself for work on a story's structure: openings, stakes, conflict, reveals,
character arcs, and weak points. It stays out of line edits, continuity fixes, and formatting.

## Trial tasks

[skills/story-craft/evals](skills/story-craft/evals) holds four tasks for checking a change to
the skill: an opening for a new story, a diagnosis of a flat scene, a plan for a reveal, and a
season outline whose teaser gives its secret to part of the audience. Run each with and without
the skill and read the results side by side. With Claude Code 2.1.269 or
later, `claude plugin eval .` from the skill folder runs them; these are billed model runs.

## What it leaves out

- Story shapes such as three acts, the hero's journey, and beat sheets. The tests work inside any
  shape and do not choose one.
- Worldbuilding and cast modelling.
- Prose style and line editing.

## Credits

- The Bear at the Door is a story shape from Jerome Stern, *Making Shapely Fiction* (W. W. Norton,
  1991).
- In medias res goes back to Horace's *Ars Poetica*.
- The works named in the reference notes belong to their creators and are cited as illustrations
  only.

## License

MIT. See [LICENSE](LICENSE).
