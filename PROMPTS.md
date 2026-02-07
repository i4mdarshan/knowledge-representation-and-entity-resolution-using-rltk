## Prompts Used for this Homework

- **P1 :** Generate a Python text normalization function suitable for preprocessing book titles and author names prior to similarity comparison. The function should:
    - Preserve semantic meaning while reducing noise for string matching
    - Apply standard techniques: lowercasing, Unicode normalization, punctuation removal, whitespace normalization, and safe character filtering

- **P2 :** Generate a reusable date normalization function for normalizing publication dates for a books information dataset where date formats are inconsistent and may include:
    - Full natural-language dates (e.g., “August 1st 2000”)
    - Numeric dates with two-digit years (e.g., “12/12/14”)
    - Year-only values (e.g., “1966”)
    - Month-year abbreviations (e.g., “Jun-14”)
    - Empty or missing values

    The solution should:
    1. Safely parse all supported formats without throwing exceptions
    2. Normalize valid inputs into a common datetime.date representation
    3. return None for empty or unparseable values
    4. Extract a derived publication_year field for tolerant comparison
    5. Be suitable for integration into RLTK Record classes using cached properties
    6. Avoid exact-date matching assumptions and instead support year-level or tolerance-based comparison