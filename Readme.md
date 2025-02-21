Hashtag Generator API
============

Hashtag Generator is a simple tool for generating hashtags. It returns a list of hashtags based on the text provided.

![Build Status](https://img.shields.io/badge/build-passing-green)
![Code Climate](https://img.shields.io/badge/maintainability-B-purple)
![Prod Ready](https://img.shields.io/badge/production-ready-blue)

This is a .NET Wrapper for the [Hashtag Generator API](https://apiverve.com/marketplace/api/hashtaggenerator)

---

## Installation

Using the .NET CLI:
```
dotnet add package APIVerve.API.HashtagGenerator
```

Using the Package Manager:
```
nuget install APIVerve.API.HashtagGenerator
```

Using the Package Manager Console:
```
Install-Package APIVerve.API.HashtagGenerator
```

From within Visual Studio:

1. Open the Solution Explorer.
2. Right-click on a project within your solution.
3. Click on Manage NuGet Packages..
4. Click on the Browse tab and search for "APIVerve.API.HashtagGenerator".
5. Click on the APIVerve.API.HashtagGenerator package, click Install.


---

## Configuration

Before using the hashtaggenerator API client, you have to setup your account and obtain your API Key.  
You can get it by signing up at [https://apiverve.com](https://apiverve.com)

---

## Usage

The Hashtag Generator API documentation is found here: [https://docs.apiverve.com/api/hashtaggenerator](https://docs.apiverve.com/api/hashtaggenerator).  
You can find parameters, example responses, and status codes documented here.

### Setup

###### Authentication
Hashtag Generator API uses API Key-based authentication. When you create an instance of the API client, you can pass your API Key as a parameter.

```
// Create an instance of the API client
var apiClient = new HashtagGeneratorAPIClient("[YOUR_API_KEY]", true);
```

---


### Perform Request
Using the API client, you can perform requests to the API.

###### Define Query

```
var queryOptions = new HashtagGeneratorQueryOptions {
  text = "Adventure awaits 🌍✈️ Who's ready to embark on a journey of a lifetime? Whether you're exploring exotic landscapes, immersing yourself in vibrant cultures, or simply indulging in delicious cuisines, there's something magical about travel that fills the soul with joy and wonder. Let's wander together and create unforgettable memories! 🌟",
  count = 5
};
```

###### Simple Request

```
var response = apiClient.Execute(queryOptions);
if(response.error != null) {
	Console.WriteLine(response.error);
} else {
    var jsonResponse = JsonConvert.SerializeObject(response, Newtonsoft.Json.Formatting.Indented);
    Console.WriteLine(jsonResponse);
}
```

###### Example Response

```
{
  "status": "ok",
  "error": null,
  "data": {
    "count": 5,
    "hashtags": [
      "#adventure",
      "#awaits",
      "#ready",
      "#embark",
      "#journey"
    ]
  },
  "code": 200
}
```

---

## Customer Support

Need any assistance? [Get in touch with Customer Support](https://apiverve.com/contact).

---

## Updates
Stay up to date by following [@apiverveHQ](https://twitter.com/apiverveHQ) on Twitter.

---

## Legal

All usage of the APIVerve website, API, and services is subject to the [APIVerve Terms of Service](https://apiverve.com/terms) and all legal documents and agreements.

---

## License
Licensed under the The MIT License (MIT)

Copyright (&copy;) 2025 APIVerve, and EvlarSoft LLC

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.