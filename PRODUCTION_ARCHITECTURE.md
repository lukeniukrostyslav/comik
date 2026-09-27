# Production Architecture

## Repository
GitHub repository: lukeniukrostyslav/comik

## Asset strategy
1. GitHub: story, prompts, continuity, manifests, QA, assembly specifications and production logs.
2. Primary image-generation workspace: dedicated image-generation service connected to ChatGPT.
3. Large binary archive: external object/media storage when required; final ZIP is assembled locally and verified before delivery.

## Recommended image workflow
- Generate artwork without dialogue text.
- Keep a stable Mara Venn reference set.
- Generate one standalone page at a time.
- QA each page before accepting it.
- Maintain RU and EN editions from the same approved artwork sequence.
- Apply lettering separately so Russian and English can share the same art.
- Store immutable final-page hashes in the release manifest.

## Do not
- crop contact sheets into fake pages;
- count previews as pages;
- fabricate missing artwork;
- increase progress percentages without completed QA.
