---
title: "Cloudant Recover Doc"
date: 2022-05-12T17:46:39-03:00
---

See All your DB Changes
`http://example.iriscouch.com/test/_changes`

Get all the revsion info for your document
` http://example.iriscouch.com/test/$id?revs_info=true `

```
"_revs_info": [
{
"rev": "52-974f2f2894e6147908ac933f7ce6252c",
"status": "available"
},
{
"rev": "51-5dd5375336b502da3ea1b2de461f45b2",
"status": "deleted"
},
{
"rev": "50-6ebfdb24514d7654ca920c714e1b3971",
"status": "available"
},
{
"rev": "49-983467f528270a7c25c636db3bf4de9e",
"status": "missing"
}
]
```

Find the last valid revision you want to restore, and retive the document at that revision. Then re-create the document
```
https://my-url.cloudant.com/myDB/MyDocName?rev=myLastValidRev
```
