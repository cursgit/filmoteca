<HighLevelDetails>

The `filmoteca` repository stores cultural data collections in three main folders:
- `llibres/` → book entries
- `pelicules/` → movie entries
- `series/` → series entries

Each folder contains a `README.md` that describes the exact format each entry must follow.  
Each entry is a text file (usually `.md` or `.txt`) with fields such as title, author/director, year, etc.  
The repository **does not contain any scripts or executable code** — only data files.

Goal:
- Enable Copilot to **verify that each entry file complies with the format specified in its README**.
- Ensure that **no entries are duplicated** (same title, author, or file name).

Project type: data collection.  
Languages: Markdown / plain text.  
No dependencies or compilation.  
Repository is small and can be fully analyzed.

</HighLevelDetails>

<BuildInstructions>

There is no build or execution process.  
Copilot should analyze the files directly.

Do not execute any commands or create any scripts.  
All verification should be done internally by Copilot's analysis.

</BuildInstructions>

<ProjectLayout>

Typical project structure:

```
filmoteca/
├── llibres/
│   ├── README.md          → specifies expected format for each book
│   ├── llibre1.md
│   ├── llibre2.md
│   └── ...
├── pelicules/
│   ├── README.md          → specifies expected format for each movie
│   ├── peli1.md
│   └── ...
├── series/
│   ├── README.md          → specifies expected format for each series
│   ├── serie1.md
│   └── ...
└── README.md              → general description of the project
```

No source code or configuration files exist.  
Validation relies solely on matching files to the formats documented in the `README.md`.

</ProjectLayout>

<StepsToFollow>

1. Examine all contents of the `filmoteca` repository.
2. Read all `README.md` files to understand the expected format for each type of entry.
3. List all files in `llibres/`, `pelicules/`, and `series/` (ignoring `README.md`).
4. For each file:
   - Compare its content against the format specified in the corresponding README.
   - Identify missing, incorrect, or misordered fields.
   - The language of the file has to be consistent (e.g., if the text is written in Catalan, the headings and field names should also be in Catalan).
   - Supported languages are Catalan, Spanish, and English. The language of the file can be different from the language of the README, but it should be consistent within the file itself.
5. Detect potential duplicates based on:
   - title,
   - file name,
   - or other key fields defined in the README.
6. Produce a report listing:
   - Correct entries ✅
   - Entries with format issues ⚠️ (indicating missing fields)
   - Duplicate entries ❌ (indicating affected files)
7. Do not generate or execute any code or modify any files.
8. Use internal analysis of the repository. Only perform additional searches if the instructions are incomplete or contradictory.
9. Treat the `README.md` files as the authoritative source for correct format.

</StepsToFollow>
