---
promptId: 'ligAmbient'
name: '🖼️ Generate a Ambient Lighting photo'
description: 'select a text and ambient lighting photo about it will be generated using Dalle-2'
author: 'Prompt Engineering Guide'
tags: 'photo, dalle-2,lighting'
version: '0.0.1'
output: '\n![]({{requestResults.data.0.url}})'
provider: 'custom'
endpoint: 'https://api.openai.com/v1/images/generations'
body: '{"n": 1, "size": "1024x1024", "prompt": "{{escp prompt}}"}'
headers: "{\r      \"Content-Type\": \"application/json\",\r      \"authorization\": \"Bearer {{keys.openAIChat}}\"\r}"
stream: false
---
{{selection}}, Ambient Lighting