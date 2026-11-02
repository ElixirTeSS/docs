# Exchange content

TeSS can import content from a range of external sources.
When the source is also based on TeSS, there are additional features which allow you to customise and automate the exchange, thanks to the [mTeSS-X project](../overview/mtess-x).

```{image} ../images/content/graphic-exchange.svg
:alt: Graphic of content exchange
:class: mb-1
:width: 300px
:align: center
```

## How is content exchanged?

TeSS uses [OAI-PMH](https://www.openarchives.org/pmh/) to exchange materials and events between catalogues. It supports two metadata formats:

- **Bioschemas RDF**, using schema.org properties, provides richer descriptions of training content and is supported by up-to-date TeSS instances.
- **Dublin Core** provides a smaller set of properties and is supported by many other catalogue platforms.

TeSS first requests Bioschemas RDF. If that format is unavailable or no recognised materials or events are found, it falls back to Dublin Core. The two formats are not combined to fill gaps in individual records.

With Bioschemas RDF, `LearningResource` records become TeSS materials, while `Event` and `CourseInstance` records become TeSS events. Courses linked to course instances can also supply metadata for those events.

With Dublin Core, records become TeSS events if a `dc:type` value contains "event" (case-insensitive), for example `http://purl.org/dc/dcmitype/Event`. Other records become TeSS materials.

## Which filters can I use to exchange?

TeSS provides a selection of filters to customise which materials and events are exchanged.
This list is being expanded as part of the [TeSSHub4EOSC project](../overview/tesshub4eosc). If a filter you need is not available, please contact us.

The tables below show the main supported filters including metadata mappings. `schema:` refers to schema.org; `dc:` refers to Dublin Core.

An arrow indicates a property of a linked object. For example, `schema:audience` → `schema:audienceType` means the type of the audience.

Filters are applied to the values imported into TeSS. Their availability therefore depends on the metadata supplied by the source.

| Filtered property in TeSS | Exchanged properties |
|:-------------------------|:---------------------|
| Target audience | `schema:audience` → `schema:audienceType` |
| Keyword | `schema:keywords`; `dc:subject` |
| Title (equals / contains) | `schema:name`; `dc:title` |
| Description (equals / contains) | `schema:description`; `dc:description` |
| URL (equals / begins) | `schema:url`; `dc:identifier` containing an HTTP(S) URL |
| DOI (*material only*) | `schema:identifier` containing a DOI; `dc:identifier` containing a DOI |
| License (*material only*) | `schema:license`; `dc:rights` |
| Difficulty level (*material only*) | `schema:educationalLevel` |
| Resource type (*material only*) | `schema:learningResourceType`; `dc:type` |
| Prerequisites (contains) | `schema:competencyRequired` for materials; `schema:coursePrerequisites` for events |
| Learning objectives (contains) | `schema:teaches` |

Recognised HTML formatting in descriptions is converted to Markdown before filtering.

The following filters are available for *events only*:

| Filtered property in TeSS | Exchanged properties |
|:-------------------------|:---------------------|
| Subtitle (equals / contains) | `schema:alternateName` |
| City | `schema:location` → `schema:address` → `schema:addressLocality` |
| Country | `schema:location` → `schema:address` → `schema:addressCountry` |
| Event type | Set to `workshops_and_courses` for RDF course instances; `dc:type` for Dublin Core events. |
| Timezone | Not currently populated from exchanged metadata |

The following properties can also be populated during exchange, but have no dedicated filter controls:

| Non-filtered property in TeSS | Exchanged properties |
|:-----------------------------|:---------------------|
| Contact | For RDF events: `schema:contact` → `schema:name` and `schema:email`; for Dublin Core materials and events: `dc:publisher` |
| Authors (*material only*) | `schema:author` → `schema:name`; `dc:creator` |
| Organizer (*event only*) | `schema:organizer`; first non-empty `dc:creator` |
| Language (*event only*) | `schema:inLanguage` |
| Scientific topics | `schema:about` referencing `schema:DefinedTerm` resources |
| Date created (*material only*) | `schema:dateCreated`; first successfully parsed `dc:date` |
| Date modified (*material only*) | `schema:dateModified`; last successfully parsed `dc:date`, if more than one is present |
| Start date (*event only*) | `schema:startDate`; first successfully parsed `dc:date` |
| End date (*event only*) | `schema:endDate`; last successfully parsed `dc:date` |

The first date in Dublin Core `dc:date` is considdered the start date and the last one the end date. For events with only one successfully parsed date, that date supplies both the start and end dates.

```{admonition} See also the definitions of these terms
:class: seealso
* [TeSS Platform Definitions](/overview/definitions)
```

## How do I set up an automated exchange from another TeSS instance?

You may take the following steps to set up automated exchange between two TeSS-based catalogues (a **source** and a **destination**):

1) Ensure that you have the correct permissions. To set up exchange, you need to be a site **admin** or **curator**, or the **owner or an editor of a content provider**, in the destination TeSSHub (where the content should end up). Provider owners and editors can create sources only when user source creation is enabled in the destination instance. You are the owner of content providers that you create. For non-admin users, the destination must also include `oai_pmh` among its permitted ingestion methods; contact an administrator if 'OAI-PMH' is unavailable.
2) Go to the source TeSSHub instance (where the training should come from) and understand what metadata (set of filters) is used there to describe the particular set of training content that should be exchanged.
3) In the source instance, at the top of the list of training materials, go to the 'Subscribe' menu, click 'Harvest using OAI-PMH', and copy the OAI-PMH link.
4) Go to the content provider in the destination TeSSHub instance, open the 'Sources' tab, then click the 'Add source' button.
5) Enter the URL that you copied in step 3 into the URL field and select 'OAI-PMH' as the ingestion method.
6) If you are ready for the materials to be automatically exchanged, check the 'Enabled' checkbox; otherwise, leave it unchecked to save the source as a draft. If you are an administrator, you may also directly set the new source as 'Approved'. Everyone else will need administrator approval before content starts to be exchanged, and should request it after saving as described in step 8.
7) You may add **filter conditions** to exchange only part of the source's content. Only content that satisfies all conditions in the 'Allow' list and none of the conditions in the 'Block' list is exchanged. To exchange content matching alternative sets of conditions, create a separate source for each set.
8) Save the source using the 'Register Source' button. If the source needs administrator approval, click **'Request Approval'** on the saved source's page when it is ready for review. Saving alone does not submit an approval request. You will not be able to modify the source while approval is pending.
9) After the source is enabled and approved, content is normally exchanged and kept up to date once per day, depending on the configuration of the destination TeSSHub instance.

The whole process is also shown in this video. In this example, training material on Python that is not for beginners is exchanged from ELIXIR TeSS to PaN-Training:

<video controls="" width="790.4" src="https://zenodo.org/api/records/18926348/files/exchange-demo.mp4/content"></video>

- [Download video](https://zenodo.org/api/records/18926348/files/exchange-demo.mp4/content)
- [View on Zenodo](https://zenodo.org/records/18926348)

Please note that the video may be slightly outdated in some cases. The instructions above may be more up to date.

## How do I set up an automated exchange from something other than TeSS?

You can automate exchange into a TeSS-based catalogue from a non-TeSS catalogue if the source supports OAI-PMH with compatible Bioschemas RDF or Dublin Core metadata (Dublin Core metadata is required in OAI-PMH).

The [supported properties and filters](#which-filters-can-i-use-to-exchange) are listed above. Sources offering only Dublin Core provide fewer properties, so some filters may not be usable.

Follow the [steps for exchange from another TeSS instance](#how-do-i-set-up-an-automated-exchange-from-another-tess-instance), but obtain the source's OAI-PMH endpoint URL from its documentation or administrator instead of using the TeSS 'Subscribe' menu.

For other ways to import content automatically, including from sources that do not support OAI-PMH, see [Automatic content registration](auto).
