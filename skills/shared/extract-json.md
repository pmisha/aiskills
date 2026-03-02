<!--
Name: Extract JSON
Description: Extracts structured data from unstructured text and returns valid JSON.
Inputs: {{text}} - Source text, {{schema}} - JSON schema describing desired output
Compatible: claude, gemini, openai
-->

Extract structured data from the text below and return it as valid JSON matching this schema:

Schema:
{{schema}}

Text:
{{text}}

Return ONLY valid JSON with no additional explanation or markdown fences.
