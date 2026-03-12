# How we support FAIR

Training materials and events are widely dispersed and fragmented, making it challenging for users to identify relevant materials. 
Training e-Support System (TeSS) is a web-based open-source platform consolidating resources from various providers into an easy-to-use portal. 
It is a one-stop-shop for trainers and trainees to discover training materials, workshops, and online courses in relevant topics such as data management and open research methods.

For providers, the TeSS Platform makes it easy to make resources [FAIR](http://doi.org/10.1038/sdata.2016.18) (Findable, Accessible, Interoperable, and Reusable):

- **Findable**:  A unique, persistent identifier such as [DOI](https://www.doi.org/the-identifier/what-is-a-doi/) is requested for all materials. (For example, [publish your materials in Zenodo](https://help.zenodo.org/docs/get-started/quickstart/) to be assigned a DOI.)
- **Accessible**: TeSS materials/events are accessible to all registered users via the TeSS website, [widgets](../developers/code-data) or [JSON API](../developers/code-data). Your content will seen more in search results owing to our search-engine optimisation (SEO).
- **Interoperable**: Metadata uses a standard vocabulary (EDAM for ELIXIR). We expose content using Schema.org (Bioschemas), JSON-LD, and OAI-PMH open standards.
- **Reusable**: License is requested for all materials, such as Creative Commons.


## Integration with tools, policies, standards and data registries

In [ELIXIR TeSS](https://tess.elixir-europe.org/), you can associate your training materials with resources held in other ELIXIR resources: 

::::{grid} 1 1 2 2
:gutter: 3

:::{grid-item-card}
:link: https://bio.tools/
{fas}`screwdriver-wrench;sd-text-secondary` **bio.tools**
^^^

A community-driven registry of bioinformatics software tools, databases, analysis workflows, and services.
:::

:::{grid-item-card}
:link: https://fairsharing.org/
{fas}`share-nodes;sd-text-secondary` **FAIRsharing**
^^^

A curated resource focused on databases, and the policies, standards, formats and vocabularies they use.
:::
::::

When you manually edit your training material in TeSS, you can search for bio.tools and FAIRsharing resources directly. 
If your training material is automatically ingested into TeSS, you can add the URL of each the resources into the Bioschemas markup under the `mentions` property: if the URL begins with `https://bio.tools/` or `https://fairsharing.org/` then TeSS will correctly pick up the resource. For example:

```json
{
  "mentions": [
    {"@type": "Thing", "url": "https://bio.tools/tool/galaxy", "name": "Galaxy"},
    {"@type": "Thing", "url": "https://fairsharing.org/FAIRsharing.nb9zzm", "name": "F1000Research Data Guidelines"}
  ]
}
```


## Interoperate using Linked Data

When you view a material or event on TeSS, there is machine-readable metadata behind the human-readable content. 
If you were to view the HTML source of the page, you would see this code, written as [JSON-LD](https://json-ld.org/).  

```{image} ../images/overview/metadata-source.png
:alt: View Source to see the embedded metadata
:class: mb-1
:width: 300px
:align: center
```

Developers can access this [Bioschemas](https://bioschemas.org)-compliant JSON-LD metadata, without the human-readable HTML, to use interoperate as [Linked Data](https://en.wikipedia.org/wiki/Linked_data). To do this, append `.jsonld` to the URL. For example:

```
https://tess.elixir-europe.org/materials/how-to-make-your-messy-data-usable-openrefine
```

...becomes
```
https://tess.elixir-europe.org/materials/how-to-make-your-messy-data-usable-openrefine.jsonld
```
