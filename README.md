Presentation Format Style Guides for LLM-Powered Slide Creation  
---------------------------------------------------------------

Overview  
--------
This project defines JSON-like **style guides** for four major Markdown-based presentation tools:

- **Deckset**
- **iA Presenter**
- **Markmap**
- **Pandoc (to PPTX)**

Each style guide encodes the structural and behavioral rules of a presentation format in a machine-readable schema. These can be used in combination with a **large language model (LLM)** to automatically or semi-automatically generate high-quality slide decks from raw educational or informational text.

Use Cases  
---------
These guides are designed to:

1. **Instruct the LLM** on formatting requirements per tool.
2. **Transform input text** into properly structured Markdown with correct headings, layout cues, and syntax.
3. **Assist developers** or educators in choosing the right tool for their content and constraints.
4. **Ensure compatibility** between structured content and specific slide generators.
5. **Support automated pipelines** where LLMs output complete, styled presentations ready for import into a tool like Deckset, iA Presenter, or Pandoc.

How It Works  
------------
When creating presentations from information text (such as lesson plans, articles, or notes), the JSON-like structure:

- Defines **valid layout blocks** (e.g., headings, lists, code, quotes).
- Indicates which elements are **visible to the audience** vs. used only for **presenter notes**.
- Details **formatting modifiers**, layout types (e.g., columns, background images), and style directives.
- Allows the LLM to **target tool-specific features** (like `[.build-lists: true]` in Deckset or `⇥` for iA Presenter).

By providing this schema to the LLM before generating slides, you ensure that:
- Output respects tool capabilities.
- Styling directives are applied properly.
- Code blocks, formulas, and visuals are embedded using correct syntax.
- Presentations are more **coherent**, **engaging**, and **ready to use**.

Example Workflow  
----------------
1. **Input**: A teacher provides a topic summary on "Photosynthesis."
2. **LLM Prompt**:
   - Includes topic text.
   - References the JSON style guide for `deckset`.
   - Instructs the model to generate a Deckset-compatible Markdown presentation.
3. **Output**: A complete `.md` file with structured content, styled headings, footnotes, and slide-level configurations.

Compatibility  
-------------
These guides are format-specific, meaning each is tailored to the behavior and syntax rules of its respective presentation tool. You can:
- Use them individually for targeted slide generation.
- Build a **unified prompt interface** that lets users select a presentation format, and the system fetches the appropriate style guide.
- Extend or customize them for theme-specific variants, localization, or education-level adaptations.

Included Style Guides  
---------------------
- `decksetStyleGuide.json`
- `iapresenterStyleGuide.json`
- `markmapStyleGuide.json`
- `pandocPPTXStyleGuide.json`



