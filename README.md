# Little Red Schoolhouse skill

Most drafts follow the order the writer thought in: background first, then exploration, then the point.
But readers don't read to learn what the writer thinks. They read because something they care about is
unstable or costly, so a draft that saves its point for the end loses them before it arrives.

This skill teaches Claude to write and revise in the reader-centered style of the University of Chicago's
Little Red Schoolhouse (Joseph Williams, Gregory Colomb, Larry McEnerney). It covers problem-framed
introductions, issue-then-discussion paragraphs, and Williams's sentence principles.

## Install

### Claude Code (plugin marketplace)

```
/plugin marketplace add corprew/little-red-schoolhouse-skill
/plugin install little-red-schoolhouse@little-red-schoolhouse-skill
```

### Claude Code (manual)

Copy the skill folder into your personal skills directory:

```sh
git clone https://github.com/corprew/little-red-schoolhouse-skill.git
cp -R little-red-schoolhouse-skill/skills/little-red-schoolhouse ~/.claude/skills/
```

To use it in a single project, copy it to `.claude/skills/` in that project instead.

### Claude.ai / Claude Desktop

Zip the `skills/little-red-schoolhouse` folder and upload it under **Settings → Capabilities → Skills**.

```sh
cd skills && zip -r ../little-red-schoolhouse.zip little-red-schoolhouse
```

## Use

The skill triggers on its own when you ask Claude to make a document reader-centered, to "lead with the
problem", to fix an introduction so it says why something matters, or when you mention the Little Red
Schoolhouse, Williams's *Style*, or *The Craft of Research*. It works on memos, proposals, specs, PR
descriptions, ADRs, reports and papers, and it scales down to commit messages and chat answers.

Examples:

- "Rewrite this PR description in Little Red Schoolhouse style."
- "This memo buries the recommendation. Make it lead with the problem."
- "Revise the intro of this paper so a reviewer knows why it matters."

## Layout

```
.claude-plugin/
  plugin.json        # plugin manifest
  marketplace.json   # lets this repo serve as its own marketplace
skills/
  little-red-schoolhouse/
    SKILL.md         # the skill itself
```

## License

MIT. See [LICENSE](LICENSE).
