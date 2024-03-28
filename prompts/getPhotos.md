---
promptId: getPhoto
name: 🖼️ Generate 4 photos (dalle-2)
description: select a text and 4 photos about it will be generated using Dalle-2
author: Noureddine
tags:
  - photo
  - dalle-2
version: 0.0.1
sanatization_response: "// catch error\rif (res.status >= 300) {\r  const err = data?.error?.message || JSON.stringify(data);\r  throw err;\r}\r\r// get choices\rconst choices = data.data.map(c=> ({ type: \"image_url\", image_url: c.url}));\r\r// the return object should be in the format of \r// { content: string }[] \r// if there's only one response, put it in the array of choices.\rreturn choices;"
provider: custom
endpoint: https://api.openai.com/v1/images/generations
body: '{n: 4, size: "1024x1024", prompt: "{{escp prompt}}", model: "dall-e-2"}'
headers: "{\r\"Content-Type\": \"application/json\",\r \"authorization\": \"Bearer {{keys.openAIChat}}\"\r}"
stream: false
commands:
  - generate
---
{{tg_selection}}