# Exchange content

As introduced in previous sections, TeSS can import content from external sources. This is naturally also possible when the external source is also a TeSS based catalogue. But in this special case there is explicit support thanks to the [mTeSS-X project](../overview/mtess-x).

```{image} ../images/content/graphic-exchange.svg
:alt: Graphic of multi-spaces
:class: mb-1
:width: 300px
:align: center
```

You may take the following steps to setup automated exchange between two TeSS based catalogues:

1) Ensure that you have the correct permissions. To set up the exchange of materials, you need to be a site **admin** of the TeSSHub where the content should end up in, or the **owner of a content provider** in this TeSSHub instance. You are owner of content providers that you created yourself by default.
2) Go to the TeSSHub instance where the training should come from and understand what metadata is used there to describe the particular set of training content that should be exchanged.
3) In the source instance, at the top of the list of training materials, select "Harvest using OAI-PMH" in the "Subscribe" menu and copy the OAI-PMH link.
4) Go to the content provider in the target TeSSHub instance where the exchanged content should be associated with and open the "Sources" tab to hit the "Add source" button.
5) Enter the URL that you copied in step 3 into the URL field and select "OAI-PMH" as the ingestion method. 
6) Check the "Enabled" checkbox. If you just want to create the source as a draft, don't check this checkbox to avoid automatically exchanging training content yet. If you are an administrator, you may also directly set the new source as approved to enable it. If you are not an administrator, you need to wait until an administrator approves the source before content starts to be exchanged.
7) You may add filter conditions to not exchange the whole content of the source TeSSHub. Only content that satisfies all the conditions in the allow list and none of the conditions in the block list is exchanged. For more complex cases where either one set of conditions or another set of conditions but not necessarily all the conditions should be satisfied for exchange feel free to create multiple sources for each set of conditions.
8) Save the source using the "Register Source" button.
9) After the source is enabled and approved, you may expect content to be exchanged and kept up to date once per day, but this may depend on the configuration of the target TeSSHub instance. 

The whole process is also shown in this video. In this example, training material on Python that is not for beginners is exchanged from ELIXIR TeSS to PaN-Training:
<video controls="" width="790.4" src="https://zenodo.org/api/records/18926348/files/exchange-demo.mp4/content"></video>
Please note that the video may be slightly outdated in some cases. The instructions above may be more up to date.

