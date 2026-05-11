# Primary functions

Your docs are set up by using functions found in the Tome namespace. Add/edit site items with Tome.site.\*, and check out Tome.utils.\* for functions that will help with the generation of your site.     <br>
     <br>
Below are the functions you'll use to set up your docs and generate them.

## `Tome.site.add(file, [slugs])` → **{undefined}**

<div class="tome-function">

Adds a file to be parsed as a page to your site 

| Parameter | Datatype | Purpose |
|-----------|-----------|---------|
| file | {string} | The name of a file (as shown in the IDE) or a direct file path to an external file. |
| [slugs] | {string <span class="tome-type-separator"> *or* </span> Array.string <span class="tome-type-separator"> *or* </span> undefined} | [Default = undefined] The name of any notes (as shown in the IDE) or a direct file path to an external .txt file that will be used for adding slugs. |


</div>

## `Tome.site.addRaw(file, title, category)` → **{undefined}**

<div class="tome-function">

Adds your own markdown file to a category. No parsing of this file is performed; it is added to the docs website as is. 

| Parameter | Datatype | Purpose |
|-----------|-----------|---------|
| file | {string} | The filepath pointing to the file you wish to add to the docs site |
| title | {string} | The title the page will have on the sidebar. |
| category | {string} | The category the page will appear under on the sidebar. |


</div>

## `Tome.site.addSidebarLink(link, title, category)` → **{undefined}**

<div class="tome-function">

Adds a link to the sidebar of your site. 

| Parameter | Datatype | Purpose |
|-----------|-----------|---------|
| link | {string} | The path to the link. |
| title | {string} | The title of the link. |
| category | {string} | The category of the link. |


</div>

## `Tome.site.addNavbarLink(link, title)` → **{undefined}**

<div class="tome-function">

Adds a link to the navbar 

| Parameter | Datatype | Purpose |
|-----------|-----------|---------|
| link | {string} | The path to the link |
| title | {string} | The title of the link |


</div>

## `Tome.site.setHomepage(file, [raw])` → **{undefined}**

<div class="tome-function">

Sets the homepage of your site to be the contents of a file (`.txt`, or `.md`) or note asset from your project. 

| Parameter | Datatype | Purpose |
|-----------|-----------|---------|
| file | {string} | The filepath or note asset name as shown in your project. |
| [raw] | {boolean} | [Default = false] If the file should be used as is (true), or parsed by Tome's parser (false) |


</div>

## `Tome.site.setName(name)` → **{undefined}**

<div class="tome-function">

Sets the name of your site, this will appear in the header and the title tag of the generated documentation. 

| Parameter | Datatype | Purpose |
|-----------|-----------|---------|
| name | {string} | The name of your site. |


</div>

## `Tome.site.setDescription(description)` → **{undefined}**

<div class="tome-function">

Sets the description of your site, this will appear in the meta description tag of the generated documentation. 

| Parameter | Datatype | Purpose |
|-----------|-----------|---------|
| description | {string} | The description of your site. |


</div>

?> Version names cannot contain illegal filepath characters or spaces!

## `Tome.site.setLatestVersion(_versionName)` → **{undefined}**

<div class="tome-function">

Sets the latest version of your project. This will be used to determine which version of the docs to show by default, and will be shown in the version dropdown if you have multiple versions of docs. 

| Parameter | Datatype | Purpose |
|-----------|-----------|---------|
| _versionName | {string} | The latest version of your project. |


</div>

## `Tome.site.setOlderVersions(versions)` → **{undefined}**

<div class="tome-function">

Sets the older versions of your project. This will be used to populate the version dropdown if you have multiple versions of docs. 

| Parameter | Datatype | Purpose |
|-----------|-----------|---------|
| versions |  |  |


</div>

## `Tome.site.setThemeColor(themeColor)` → **{undefined}**

<div class="tome-function">

Sets the theme color of your site. This will be used as the primary color for your docs site, used in the header, links, and other accents. 

| Parameter | Datatype | Purpose |
|-----------|-----------|---------|
| themeColor | {Constant.Color <span class="tome-type-separator"> *or* </span> string} | The theme color of your site. This can be a GameMaker color constant, or a CSS hex string (e.g. "#FF0000" for red). If providing a GameMaker color, it will be converted to a CSS hex string automatically. |


</div>

## `Tome.site.setConfigProperty(property, value)` → **{undefined}**

<div class="tome-function">

Sets a custom configuration property for your site. This can be any value, but keep in mind that if you want to use this property in your site you'll need to reference it in the index.html of your docs site, and you may need to use custom JavaScript to make use of it depending on how you want to use it. 

| Parameter | Datatype | Purpose |
|-----------|-----------|---------|
| property | {string} | The name of the configuration property to set. |
| value | {any} | The value of the configuration property. |


</div>

?> For more information about using custom CSS with Tome check [this](misc-advanced-use?id=custom-css) out!

## `Tome.site.editCustomCSS(cssData)` → **{undefined}**

<div class="tome-function">

Adds or overrides custom CSS for the documentation site. 

| Parameter | Datatype | Purpose |
|-----------|-----------|---------|
| cssData |  |  |


</div>

## `Tome.utils.colorToCSSHex(color)` → **{string}**

<div class="tome-function">

Converts a GameMaker color to a CSS hex string. 

| Parameter | Datatype | Purpose |
|-----------|-----------|---------|
| color | {number} | The GameMaker color to convert. |


Returns:  The CSS hex string representation of the color.

</div>

## `Tome.utils.fileReadAllText(filepath)` → **{string}**

<div class="tome-function">

Loads a text file and reads its entire contents as a string 

| Parameter | Datatype | Purpose |
|-----------|-----------|---------|
| filepath |  |  |


Returns:  The contents of a file as a string.

</div>

## `Tome.utils.fileReadAllBin(filepath)` → **{buffer}**

<div class="tome-function">

Loads a binary file into a buffer (You are responsible for deleting the returned buffer) 

| Parameter | Datatype | Purpose |
|-----------|-----------|---------|
| filepath |  |  |


Returns:  A buffer reference containing the data of the binary file

</div>

## Deprecated API.
 Below are functions that are still available for compatibility reasons, but are no longer recommended for use. These functions may be removed in a future update, so it is recommended to switch to the new API equivalents where possible. If you have any questions about how to update your code, please refer to the documentation.


!> **This function is deprecated**: Use `Tome.site.add` instead. This function is only retained for compatibility.

## `tome_add_script(scriptName, [slugs])` → **{undefined}**

<div class="tome-function">

Adds a script to be parsed as a page to your site 

| Parameter | Datatype | Purpose |
|-----------|-----------|---------|
| scriptName | {string} | The name of the script to add |
| [slugs] | {string} | The name of any notes (as shown in the IDE) or a direct file path to an external .txt file that will be used for adding slugs. One additional argument per slug note. |


</div>

!> **This function is deprecated**: Use `Tome.site.add` instead. This function is only retained for compatibility.

## `tome_add_note(noteName, [slugs])` → **{undefined}**

<div class="tome-function">

Adds a note to be parsed as a page to your site 

| Parameter | Datatype | Purpose |
|-----------|-----------|---------|
| noteName | {string} | The note to add |
| [slugs] | {string} | The name of any notes (as shown in the IDE) or a direct file path to an external .txt file that will be used for adding slugs. One additional argument per slug note. |


</div>

!> **This function is deprecated**: Use `Tome.site.add` instead. This function is only retained for compatibility.

## `tome_add_file(filePath)` → **{undefined}**

<div class="tome-function">

Adds an external file to be parsed when the docs are generated 

| Parameter | Datatype | Purpose |
|-----------|-----------|---------|
| filePath | {string} | The file to add |


</div>

!> **This function is deprecated**: Use `Tome.site.setHomepage` instead. This function is only retained for compatibility.

## `tome_set_homepage_from_file(filePath)` → **{undefined}**

<div class="tome-function">

Sets the homepage of your site to be the contents of a file (`.txt`, or `.md`) 

| Parameter | Datatype | Purpose |
|-----------|-----------|---------|
| filePath | {string} | The file to use as the homepage |


</div>

!> **This function is deprecated**: Use `Tome.site.setHomepage` instead. This function is only retained for compatibility.

## `tome_set_homepage_from_note(noteName)` → **{undefined}**

<div class="tome-function">

Sets the homepage of your site to be the contents of the given note 

| Parameter | Datatype | Purpose |
|-----------|-----------|---------|
| noteName | {string} | The note to use as the homepage |


</div>

!> **This function is deprecated**: Use `Tome.site.addSidebarLink` instead. This function is only retained for compatibility.

## `tome_add_to_sidebar(name, link, category)` → **{undefined}**

<div class="tome-function">

Adds an item to the sidebar of your site 

| Parameter | Datatype | Purpose |
|-----------|-----------|---------|
| name | {string} | The name of the item |
| link | {string} | The link to the item |
| category | {string} | The category of the item |


</div>

!> **This function is deprecated**: Use `Tome.site.setName` instead. This function is only retained for compatibility.

## `tome_set_site_name(name)` → **{undefined}**

<div class="tome-function">

Sets the name of your site 

| Parameter | Datatype | Purpose |
|-----------|-----------|---------|
| name | {string} | The name of the site |


</div>

!> **This function is deprecated**: Use `Tome.site.setDescription` instead. This function is only retained for compatibility.

## `tome_set_site_description(desc)` → **{undefined}**

<div class="tome-function">

Sets the description of your site 

| Parameter | Datatype | Purpose |
|-----------|-----------|---------|
| desc | {string} | The description of the site |


</div>

!> **This function is deprecated**: Use `Tome.site.setThemeColor` instead. This function is only retained for compatibility.

## `tome_set_site_theme_color(color)` → **{undefined}**

<div class="tome-function">

Sets the theme color of your site 

| Parameter | Datatype | Purpose |
|-----------|-----------|---------|
| color | {string} | The theme color of the site as a GameMaker Color or hex code string (e.g. "#FF0000" for red) |


</div>

!> **This function is deprecated**: Use `Tome.site.setLatestVersion` instead. This function is only retained for compatibility.

## `tome_set_site_latest_version(versionName)` → **{undefined}**

<div class="tome-function">

Sets the latest version of the docs. 

| Parameter | Datatype | Purpose |
|-----------|-----------|---------|
| versionName | {string} | The latest version of the docs |


</div>

!> **This function is deprecated**: Use `Tome.site.setOlderVersions` instead. This function is only retained for compatibility.

## `tome_set_site_older_versions(versions)` → **{undefined}**

<div class="tome-function">

Specifically set what older versions of your docs you want to show on the site's version selector 

| Parameter | Datatype | Purpose |
|-----------|-----------|---------|
| versions | {array<string>} | An array of older versions' names to display in the version selector |


</div>

!> **This function is deprecated**: Use `Tome.site.addNavbarLink` instead. This function is only retained for compatibility.

## `tome_add_navbar_link(name, link)` → **{undefined}**

<div class="tome-function">

Adds a link to the navbar 

| Parameter | Datatype | Purpose |
|-----------|-----------|---------|
| name | {string} | The name of the link |
| link | {string} | The link to the link |


</div>
