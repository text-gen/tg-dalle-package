---
promptId: 'artSteampunk'
name: '🖼️ Generate a steampunk art photo'
description: 'select a text and photo with the style of steampunk art will be generated using Dalle-2'
author: 'Prompt Engineering Guide'
tags: 'photo, dalle-2, art'
version: '0.0.1'
output: '\n![]({{requestResults.data.0.url}})'
provider: 'custom'
endpoint: 'https://api.openai.com/v1/images/generations'
body: '{"n": 1, "size": "1024x1024", "prompt": "{{escp prompt}}"}'
headers: "{\r      \"Content-Type\": \"application/json\",\r      \"authorization\": \"Bearer {{keys.openAIChat}}\"\r}"
stream: false
---
{{selection}}, steampunk art