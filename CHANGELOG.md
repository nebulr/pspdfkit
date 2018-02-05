Follow us on [Twitter](https://twitter.com/PSPDFKit) for updates. Our [blog](https://pspdfkit.com/blog) highlights the best new features and changes.

## Newest Release

### 2017.9.4 – 24 Jan 2018

No web-specific changes in this version.

## Previous Releases

### 2017.9.3 – 17 Jan 2018

* Fixes an issue when opening a PDF using the RESTProvider and a license without forms. (#1612)
* Fixes an issue when deleting an annotation using the RESTProvider. (#1635)
* Fixes a bug preventing client presences to be updated. (#1618)
* Fixes full screen keyboard shortcut instead open search. (#1609)
* Fixes incorrect text lines in some documents. (#C13148)
* Fixes an assertion when a non-specified named action was deserialized via Instant JSON. (#C13804)
* Fixes `PrintMode.EXPORT_PDF` not working in Edge and IE11 for Standalone deployments. (#1640)

### 2017.9.2 – 20 Dec 2017

* Fixes permission compatibility with server. (#1601)
* Fixes `setFormFieldValue` sending malformed payload to the server. (#1599)

### 2017.9.1 – 15 Dec 2017

* Fixes an issue where trial licenses did not have the form license flag set. (#C13553)

### 2017.9 – 14 Dec 2017

* API: Adds support for programmatic form filling. (#936)
  - API: Adds `Instance#getFormFields()` to access form fields.
  - API: Adds `Instance#getFormFieldsValues()` and `Instance#setFormFieldsValues()` to easily access the current form field values.
  - API: Adds `WidgetAnnotation` to the annotation API. This annotation can never be modified and is used to render form fields.
  - API: Adds `SubmitFormAction` and `ResetFormAction`. The submit action will also fire `forms.willSubmit` and `forms.didSubmit`, respectively.
* API: Adds a new toolbar item type, `responsive-group`. This can be used to create groups of toolbar items for smaller screens. (#1412)
* Adds support for interactive forms. (#936)
* Adds support for filling forms via Instant. (#936)
* Adds a responsive mode to the toolbar. Annotation tools are now by default grouped under an “Annotate” option on small screens. (#1412)
* Adds headless mode to run PSPDFKit for Web without a user interface. (#1534)
* Fixes an error in Instant when two clients edit text annotations simultaneously. (#1522)
* Fixes flickering of the note annotation popover when a note annotation is selected. (#1363)
* Fixes an issue where default colors for highlight annotations were not rendered properly. (#C12938)

### 2017.8.1 – 6 Dec 2017

No web-specific changes in this version.

### 2017.8 – 22 Nov 2017

* Changes annotation IDs from numerical to client-side generated string IDs. (#1303)
* Fixes a bug that prevented text selection starting from non-text nodes. (#1492)
* Fixes impossible to deselect text. (#1492)
* Fixes canceled text lines requests in standalone resolve anyway. (#1506)
* Fixes an issue with Instant on documents without the `edit-annotations` permission. (#1451)

### 2017.7.1 – 15 Nov 2017

* Improved memory management for standalone deployments. (#1453)
* Fixes `getBaseUrl` removes part of the url in IE. (#1456)
* Fixes copied text includes new lines in Firefox and IE. (#1463)

### 2017.7 – 25 Oct 2017

* API: Adds `PSPDFKit.unload` to terminate running and loading instances in favor of the now deprecated `Instance#destroy`. (#1389)
* API: Adds new CSS classes to select annotations. (#1414)
* API: Adds new CSS class to select text. (#1406)
* API: Adds option to specify a `pageIndex` to the `Instance#renderCover` standalone API. (#1404)
* API: Adds option to disable WebAssembly when using standalone deployments. (#1416)
* API: Adds new `contentWindow` and `contentDocument` getters to the `Instance` to quickly access the content of the PSPDFKit viewer. (#1439)
* API: Adds API for printing and introduces printing modes. (#1319)
* API: Fixes the casing in CSS class names of specific note annotation icons to be more consistent. (#1414)
* Adds new printing mode `DOM`. This method will render all pages of the PDF document in advance before it sends the results to the printer. (#1319)
* Adds a new icon set for all toolbar items. (#1413)
* Adds pinching for touch devices in `PER_SPREAD` scroll mode. (#1315)
* Improved support for Apple Pencil. (#1415)
* Improved WebAssembly/asm.js loading time of subsequent initializations. (#1390)
* Fixes an issue where an Instant sync conflict was causing an invalid state. (#1347)
* Fixes an issue with the transition of note annotation popovers. (#1388)
* Fixes an issue that sometimes prevented the text caret to be drawn in IE11 and Edge. (#1395)
* Fixes the position of the initial text caret on Safari. (#1396)
* Fixes a rendering issue that resulted into a blurry pages when using standalone deployments. (#1261)
* Fixes the spacing of color picker items in responsive mode. (#1414)
* Fixes an issue that emitted the wrong payload with the `annotations.delete` event. (#1423)
* Fixes an issue that caused a crash when the page index of an annotation was out of bounds. (#1397)
* Fixes an issue that prevent toolbar items from being disabled via the API. (#1432)

### 2017.6.1 – 2 Oct 2017

* Adds support for Internet Explorer 11 when using standalone deployments. (#C11782)
* Improves read-only mode for note annotations. (#1360)
* Improves error messages when invalid JWT token is supplied. (#1379)
* Changes the default breakpoint for the `layout-config` toolbar item. (#1364)

### 2017.6 – 18 Sept 2017

* API: `ViewState#pageSpacing` is now used for the spacing between pages in `LayoutMode.DOUBLE`. For the previous behavior, please use `ViewState#spreadSpacing` instead.
* API: Deprecates `ViewState#viewMode` and adds `ViewState#layoutMode` and `ViewState#scrollMode`. (#1272)
* API: Renames `ZoomMode.PAGE_FIT` and `ZoomMode.PAGE_WIDTH` to `ZoomMode.FIT_TO_VIEWPORT` and `ZoomMode.FIT_TO_WIDTH`. (#1277)
* API: Adds `ViewState#keepFirstSpreadAsSinglePage` to start with a single page in `LayoutMode.DOUBLE`. (#737)
* API: Adds `Instance#textLinesForPageIndex` to extract text content of a page. (#1302)
* Adds double page mode for both scroll modes. (#737)
* Adds support for zooming and scrolling in `PER_SPREAD` scroll mode. (#1285)
* Adds pagination by using the mouse scroll wheel in `PER_SPREAD` scroll mode. (#1285)
* Adds support for Note annotations. (#1235)
* Improves error messages for some APIs. (#1304)
* Improves performance when opening a big PDF with many annotations. (#1304)
* Improves user experience while rendering pages. (#1301)
* Fixes an issue where annotations imported via Instant JSON could no longer be updated or deleted. (#1312)
* Fixes an issue where the zoom level was not properly recalculated, when the viewport dimensions changed. (#1310)
* Fixes an issue with printing still working after being disabled via API. (#1324)
* Fixes an issue where an error was logged when refreshing the browser. (#1329)
* Fixes errors that ocurred when the root element was removed from the DOM, before the viewer finished loading. (#1328)
* Fixes a race condition that could occur when syncing annotations. (#1343)

### 2017.5.4 – 31 Aug 2017

No web-specific changes in this version.

### 2017.5.3 – 17 Aug 2017

* Fixes an issue with Chrome that prevented the document from rendering in certain environments. (#1293)

### 2017.5.2 – 9 Aug 2017

* Improves backoff behavior of Instant endpoint when an error occurs. (#1249)
* Fixes an issue where zooming in or out when text is selected caused a wrong popover position. (#1269)
* Fixes Safari/IE11 not including request headers for tiles request. (#1283)
* Fixes `exportPDF` flattens by default converting annotations to non-editable content. We made it configurable. (#1276)
* Fixes an issue where a floating point font size for a text annotation causes two options with the same value in the dropdown list. (#1284)

### 2017.5.1 – 24 Jul 2017

* Improves standalone rendering speed. (#1243)
* Improves error logging in some cases. (#1251)
* Fixes the default save mode when using standalone deployments. (#1257)
* Fixes an issue with Edge when using standalone deployments. (#1250)

### 2017.5 – 20 Jul 2017

* API: Adds `Configuration#pdf` to load a PDF for client side rendering via an `URI` or an `ArrayBuffer`. (#966)
* API: Adds ability to create, read, update, and delete annotations as well as an API to observe annotation changes. (#937)
* API: Adds event before and after the annotations are saved. (#1150)
* API: Expose annotation interfaces (`Annotation`, `HighlightAnnotation`, `InkAnnotation`, `LinkAnnotation`, `SquiggleAnnotation`, `StrikeOutAnnotation`, `TextAnnotation`, `MarkupAnnotation` `UnderlineAnnotation`, `UnknownAnnotation`). (#1049)
* API: Exposes new primitives types (`Immutable.List`, `Geometry.Point`, `Geometry.DrawingPoint`, `Geometry.Rect`, `Geometry.Size` and `Color`). (#1031)
* API: Exposes PDF action types (`Actions.GoToAction`, `Actions.URIAction`). (#1037)
* API: Supports different save modes and adds ability to save annotations manually. (#964)
* API: Renames `viewstatechanged`, `currentpageindexchanged`, `zoomchanged` and `connectedclientschanged` events. (#1151)
* API: Adds `Instance#hasUnsavedAnnotations` to find out if unsaved annotations are present. (#1152)
* API: Adds `Instance#exportPDF` to access the raw PDF binary data as `ArrayBuffer`. (#1163)
* API: Adds `Instance#exportInstantJSON` and `Configuration#instantJSON` to serialize and deserialize the document state including all annotations using Instant JSON when no server is present. (#1158)
* API: Adds `Instance#renderCover` to render the first page as a thumbnail for client side rendering. (#1178)
* API: Allow to override onPress handlers for annotations. (#1175)
* API: Allow to overwrite the inferred base url for the Server in case the JavaScript is loaded from a different host. (#1185)
* Adds support for client side rendering using WebAssembly (wasm) or asm.js. Please visit our guides for more information. (#966)
* Adds support for bundling PSPDFKit for Web using an npm package. (#1098)
* Improves pinching performance on mobile devices. (#1085)
* Improves performance of tile rendering. (#1125)
* Fixes zoom buttons should only be hidden for touch devices. (#1077)
* Fixes error in the Custom Toolbar when `mediaQueries` is set to `undefined`. (#1080)
* Fixes cleanup of event listeners when drawing ink annotations. (#1061)
* Fixes a bug that caused Safari on iOS to trigger the default zoom behavior on double tap. (#859)
* Fixes an issue with `babel-polyfill`. (#1108)
* Fixes issue when quickly jumping through search results. (#1078)
* Fixes prevent text annotation to increase page size when created at the edge. (#1130)
* Fixes sliders' thumb position for Edge. (#1136)
* Fixes sliders' vertical alignment in IE11. (#1136)
* Fixes an issue where the initial viewport size was wrong. (#1240)
* Fixes link annotations not clickable when in read-only mode. (#1242)

### 2017.4 – 16 May 2017

* API: Adds ability to customize and add new items to the main toolbar. (#1048)
* API: Adds new option `interactionMode` to `ViewState` to enable ink, text, search and pan mode. (#1003)
* API: Adds `version` to `PSPDFKit` to get the current version of PSPDFKit for Web. (#1047)
* Adds support for interacting with all annotation types (ink, text, highlight, squiggle, underline, strike-through, and link) on mobile devices. (#906)
* Adds a special annotation toolbar that appears when text is selected to allow the creation of markup annotations on mobile devices. (#1060)
* Adds pan tool to allow users to navigate on a desktop browser using mouse dragging. (#887)
* Improves the scrolling performance in Chrome browsers when an ink annotation is inside the viewport. (#616)
* Improves tiling by avoiding unnecessary calculations. (#1000)
* Improves ink annotation creation on different pages. (#985)
* Improves logging and descriptiveness of messages for errors in HTTP APIs. (#S1078, #S1110)
* Fixes issues with empty text annotations. (#821)
* Fixes an issue with text annotations that get dragged while they're changed. (#980)
* Fixes a bug that prevented the focus of the text annotation after clicking on it. (#1013)
* Fixes a bug that caused a wrong initial text selection within a text annotation. (#929)
* Fixes a bug that caused an exception when destroying the PSPDFKit for Web instance on IE 11. (#1034)
* Fixes the centering of the content inside the viewport. (#998)
* Fixes a bug where delete annotation can delete pdf assets. (#S1117)

### 2017.3.2 – 19 Apr 2017

* Adds CSS class for unsupported annotations and hides them by default. (#991)
* Fixes a bug where the `user_id` of the user performing a change was not always persisted. (#S1083)

### 2017.3.1 – 12 Apr 2017

* Adds a new license information page to the dashboard. (#S1074)
* Adds `cmd+g` and `cmd+shift+g` keyboard shortcuts to jump to the next/previous search result (macOS only). (#961)
* `load()` will now throw if the `container` element has children. (#957)
* Fixes buggy behavior in Firefox where the user needs to press backspace twice to start to delete from the end of a text annotation. (#974)
* Fixes a bug in Firefox where a NO-BREAK SPACE was inserted after the first line break. (#976)
* Fixes a bug when switching annotation modes. (#818)

### 2017.3 – 29 Mar 2017

* API: Adds option to enable read only mode. (#886)
* API: Adds option to hide annotations. (#886)
* API: Custom style sheets must now be set through the JavaScript API. (#630)
* API: Adds option to hide the print icon to `ViewState`. (#845)
* API: Adds many new public CSS classes. (#733)
* API: Adds documentation for `load()`. (#839)
* Adds support for printing documents. (#845)
* Adds new AUTO zoom mode for a better default experience. (#741)
* Adds support for flattening annotations into the PDF before it is downloaded. (#S1026)
* Adds support for permissions to selectively enable/disable viewing and editing features. These replace the old access control based on the `access` and `user_id` fields. (#S1031)
* Prevents CSS conflicts by encapsulating the viewer. (#630)
* Enforces `document_id` to be type of `string` in the JWT. (#824)
* Updates the format of the JWT used for authentication. (#S1031, #S1043)
* Removes border of link annotations. (#882)
* Fixes an error for Chrome >= 56 that was caused by Chrome making event handlers passive per default. (#792)
* Fixes z-index ordering for some annotations to prioritize newer ones. (#746)
* Fixes an issue that prevented dragging annotations in IE 11. (#870)
* Fixes an issue with editing a text annotation after reloading. (#852)

### 2017.2 – 17 Feb 2017

* API: The server will now always return and expect string document IDs. (#808)
* Adds HTTP API for working with annotations.
* Adds a debug mode to track down issues during development. (#760)
* Adds shortcuts to zoom in, out and back to page-fit.
* Shows toolbar when starting to create an ink or text annotation. (#801)
* Improves read-only mode. (#761)
* Improves the contrast of resize anchors. (#751)
* Improves the Dashboard experience.
* Search now also appears via CMD-G on macOS. (#758)
* Fixes an issue that sends an invalid search request. (#756)
* Fixes an issue where parts of the annotation toolbar disappeared. (#647)
* Fixes an issue with hidden toolbar buttons. (#794)

### 2017.1 – 25 Jan 2017

* Adds search. (#722)
* Adds custom dropdown to preview fonts. (#413)
* Optimizes ink annotations. (#590)

### 2016.3 – 21 Dec 2016

* Adds a dashboard for easy control over the server.
* Shows a font's name in the dropdown even if the font is not available. (#665)

### 2016.2.1 – 12 Dec 2016

* Fixes an issue with external events. (#699)

### 2016.2 – 8 Dec 2016

* Adds support for Internet Explorer 11. (#676)
* Removes white space after the last page on Firefox for Android. (#651, #652)
* Fixes an issue with text annotation clipping on Edge. (#644)
* Fixes an issue with PDF documents that have fractional page dimensions. (#660)
* Fixes an issue with the AnnotationToolbar position. (#661)

### 2016.1 – 1 Dec 2016

*  First public release.
