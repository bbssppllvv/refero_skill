![Refero Design Skill](assets/banner.png)

# Refero Design Skill has moved

This personal repository is a legacy package. The canonical Refero Design skill now
lives at:

https://github.com/referodesign/refero_skill

Install the official skill:

```bash
npx skills add https://github.com/referodesign/refero_skill --skill refero-design
```

The official package contains the current Refero workflow:

- styles-first visual research with Refero MCP
- concrete UI pattern research with screens
- journey research with flows
- synthesis from strong references instead of copying one design
- anti-AI-slop quality gates and craft references

This repository is kept only so old links do not break. New installs should use
`referodesign/refero_skill`.

## Refero MCP

The skill works best with Refero MCP:

```bash
claude mcp add --transport http refero https://api.refero.design/mcp --header "Authorization: Bearer <token>"
```

For setup details, use the official repository:

https://github.com/referodesign/refero_skill

## License

MIT
