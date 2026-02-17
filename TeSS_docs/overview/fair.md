# How we support FAIR

Training materials and events are widely dispersed and fragmented, making it challenging for users to identify relevant materials. 
Training e-Support System (TeSS) is a web-based open-source platform consolidating resources from various providers into an easy-to-use portal. 
It is a one-stop-shop for trainers and trainees to discover training materials, workshops, and online courses in relevant topics such as data management and open research methods.

For providers, the TeSS Platform makes it easy to make resources [FAIR](http://doi.org/10.1038/sdata.2016.18) (Findable, Accessible, Interoperable, and Reusable):

- **Findable**:  A unique, persistent identifier such as [DOI](https://www.doi.org/the-identifier/what-is-a-doi/) is requested for all materials. (For example, [publish your materials in Zenodo](https://help.zenodo.org/docs/get-started/quickstart/) to be assigned a DOI.)
- **Accessible**: TeSS materials/events are accessible to all registered users via the TeSS website, widgets or JSON API. Your content will seen more in search results owing to our search-engine optimisation (SEO).
- **Interoperable**: Metadata uses a standard vocabulary (EDAM for ELIXIR). We expose content using Schema.org (Bioschemas) and OAI-PMH open standards.
- **Reusable**: License is requested for all materials, such as Creative Commons.


## Exposed metadata behind each page

When you view a material or event on TeSS, there is machine-readable metadata behind the human-readable content. 
If you were to view the HTML source of the page, you would see this code, written in JSON-LD format.  

```{image} ../images/overview/metadata-source.png
:alt: View Source to see the embedded metadata
:class: mb-1
:width: 300px
:align: center
```

Developers can access this metadata, without the human-readable HTML content, by appending `.jsonld` to the URL. 
For example:

```
https://tess.elixir-europe.org/materials/how-to-make-your-messy-data-usable-openrefine
```

...becomes
```
https://tess.elixir-europe.org/materials/how-to-make-your-messy-data-usable-openrefine.jsonld
```
