# Sources

Owners and editors of content providers in TeSS can register and manage Sources to be automatically ingested. A source consists of a URL for TeSS to fetch, and an "ingestion method" - which hints to TeSS how the contents of the URL should be processed.

Once registered, a source will need to be approved by an administrator before it is active, but can be tested to see exactly what metadata TeSS can extract from the source.

To register a source, click the "Sources" tab on your content provider page, or if you have not yet registered a content provider, see our page [Provider account creation](../accounts/provider).

Currently available user-managed ingestion methods:

- Bioschemas

Currently available admin-managed ingestion methods:

- [Google Sheet](#google-sheet)

For other methods, please [contact us](https://tess.elixir-europe.org/about/us#contact) to discuss how to register your content automatically in TeSS.

## Google Sheet

On the user side:

1. Create a new Google Sheet.
2. Open this link : https://docs.google.com/spreadsheets/d/1yx2AZTPaPEU_Au2Hyb_C3TuNvH4btR9pZwCmfmTQRdc/.
3. Select everything from the `Example` sheet (Ctrl/Cmd + A), copy and paste it in your empty new sheet.
4. Amend the cells to properly define your training material. ⚠️ **Be careful**, some restrictions apply to specific columns, e.g., the cells under the `Keywords` column must be a coma separated list. See the list of restrictions in the [`DataDictionary` sheet](https://docs.google.com/spreadsheets/d/1yx2AZTPaPEU_Au2Hyb_C3TuNvH4btR9pZwCmfmTQRdc/edit?gid=2096797962#gid=2096797962).
5. One row corresponds to one training material, you can add as many rows/materials as you want.
6. Once your Google Sheet ready, give the URL to your TeSS administrator and ask them to use it for the Materials' Ingestion Method: CSV File and Google Spreadsheet.
