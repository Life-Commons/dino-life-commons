# Dino Life Commons

**Open deep-time intelligence** — a dinosaur encyclopedia built as a domain sibling of [Blue Life Commons](https://github.com/frankxai/blue-life-commons), with cinematic Grok Imagine heroes and a reusable life-commons template.

[![License: CC BY 4.0](https://img.shields.io/badge/content-CC%20BY%204.0-0891b2)](https://creativecommons.org/licenses/by/4.0/)

## Why this exists

Someone built a full dinosaur encyclopedia in **Grok Build** with every image/video from Imagine. This repo captures that *product shape* (cinematic species pages + stat chips + video heroes) while keeping the *commons discipline* from Blue Life Commons: sources, review state, provenance, and a reusable template for any domain.

## Quick start

```bash
pnpm install   # or npm install
pnpm dev
```

Open [http://localhost:3000](http://localhost:3000).

## What's inside

```
dino-life-commons
├── content/species/          # sourced markdown artifacts
├── public/media/species/     # Grok Imagine PNG + MP4 heroes
├── app/species/[clade]/[slug]
├── components/species-detail.tsx   # cinematic encyclopedia UI
├── template/                 # general life-commons template pack
└── docs via /template + /docs/media-pipeline
```

### Seed species

| Species | Clade | Media |
|---|---|---|
| *Ankylosaurus magniventris* | Ornithischia | PNG + MP4 |
| *Triceratops horridus* | Ornithischia | PNG + MP4 |
| *Tyrannosaurus rex* | Theropoda | PNG + MP4 |
| *Brachiosaurus altithorax* | Sauropodomorpha | PNG + MP4 |

## Media generation (Grok quality)

Hermes FAL image gen may be unconfigured. **Working path** used here:

```bash
export HOME=$USERPROFILE
grok -p "Use native Imagine image_gen / image_to_video ... save to public/media/species" \
  --no-alt-screen --always-approve --max-turns 25 --output-format plain
```

Details: site route `/docs/media-pipeline` and `template/LIFE_COMMONS_TEMPLATE.md`.

## Hard rules

- Factual claims need sources.
- Generated art is **concept reconstruction**, never identification proof.
- Science pages stay `needs-expert-review` until reviewed.

## Pattern lineage

| Layer | Repo |
|---|---|
| Ocean commons | `frankxai/blue-life-commons` |
| Dino instance | `frankxai/dino-life-commons` (this) |
| Template pack | `template/LIFE_COMMONS_TEMPLATE.md` |

## License

Content: CC-BY-4.0 unless an artifact says otherwise. Code: open source with the repository.

<!-- STARLIGHT:OPERATING:BEGIN v2 sha=9f8fecc91edc source=794db1e51a55a128816f7aa266eb0ac1dbd452c3 -->

## Agent operating guidance

Repository agents use the shared Starlight operating contract in `AGENTS.md` alongside local instructions.
The contract asks agents to establish a useful outcome, select relevant skills, complete authorized work,
verify current sources, refine the actual artifact, and report evidence and remaining gates.
It covers human agency, privacy, rights, resource stewardship and bounded proactivity.
Repository identity, brand, canon, build commands and release gates remain local.

[Pinned contract](https://github.com/frankxai/Starlight-Intelligence-System/blob/794db1e51a55a128816f7aa266eb0ac1dbd452c3/docs/architecture/agents-md/band-a.md)
· [Projection and verification](https://github.com/frankxai/Starlight-Intelligence-System/blob/794db1e51a55a128816f7aa266eb0ac1dbd452c3/docs/architecture/AGENTS-MD-CONTRACT.md)

These files supply operating guidance. They do not activate an agent, grant tool permissions,
schedule recurring work, certify compliance or prove a live capability.

<!-- STARLIGHT:OPERATING:END -->
