# EJP-RD WP13 FDP template
This template is an excel file that can be filled with metadata for datasets and their distributions. The csv exports of the template can be uploaded to Github repositories for collaboration and version control. Automation in Github can then automatically use the template to produce RDF that is automatically uploaded to a FAIR Data Point.

## Step 1: Preparation
### Download template
Download the template.xlsx file from this repository. This template works best with Microsoft Excel, but also works with LibreOffice.
When creating new metadata, this template can be used immediately. When editing existing metadata, the existing csv files should be pasted into the template.
## Step 2: Dataset sheet
The first sheet of the template contains metadata of the datasets. This is the metadata that describes the dataset itself, with metadata like the author or the themes of the dataset.
### Column explanation
#### Title
The name of the dataset with the language tag.

`Required`
#### Publisher
ORCID ID of the Organisation or Person responsible for the dataset. An ORCID ID can be created at https://orcid.org/.

`Required` `Must start with "https://orcid.org/"`
#### Description
Description of the dataset with the language tag.

`Optional`
#### Language
Language of the dataset. The two letter code of the language can be obtained from https://id.loc.gov/vocabulary/iso639-1.html, or from the languages sheet in the template.

`Optional` `Two letter language code`
#### License
License of the resource. For example, https://creativecommons.org/licenses/by/4.0/deed.en. The license gives official permission to use the resource.

`Optional` `Must start with "http://" or "https://"`
#### ContactPoint
Contact information for the resource. This can be a URL with contact information, or an email address.

`Optional` `Must start with "http://", "https://" or "mailto:"`
#### LandingPage
Home page of the dataset

`Optional` `Must start with "http://" or "https://"`
#### Keywords
Keyword(s) related to the dataset with the language tag, separated by comma's (,).

`Optional`
#### Themes
List of concepts that describe the dataset, separated by comma's (,). Relevant ontology concepts can be looked up using a service like https://www.ebi.ac.uk/ols/index.

`Required` `each theme must start with "http://" or "https://"` `Themes should be separated with comma's`

## Step 3: Distribution sheet
The second sheet of the template contains metadata of the distributions. This is the metadata that describes the distribution of the dataset. This includes a link to where the dataset is distributed, and the file type of the dataset.
### Column explanation
#### Title
The name of the distribution with the language tag.

`Required`
#### Dataset Title
The title of the dataset that is associated with the distribution.

`Required` `Must be the title of a dataset in the datasets sheet`
#### Publisher
ORCID ID of the Organisation or Person responsible for the distribution. An ORCID ID can be created at https://orcid.org/.

`Required` `Must start with "https://orcid.org/"`
#### Description
Description of the distribution with the language tag.

`Optional`
#### Language
Language of the dataset. The two letter code of the language can be obtained from https://id.loc.gov/vocabulary/iso639-1.html, or from the languages sheet in the template.

`Optional` `Two letter language code`
#### License
License of the resource. For example, https://creativecommons.org/licenses/by/4.0/deed.en. The license gives official permission to use the resource.

`Optional` `Must start with "http://" or "https://"`
#### AccessURL
A landing page, feed, SPARQL endpoint or other type of resource that gives access to the distribution of the dataset.

`One of AccessURL or DownloadURL is mandatory` `Must start with "http://", "https://" or "ftp://"`
#### DownloadURL
A file that contains the distribution of the dataset in a given format

`One of AccessURL or DownloadURL is mandatory` `Must start with "http://", "https://" or "ftp://"`
#### MediaType
The media type of the distribution, for example: "application/n-quads". Media types can be found at https://www.iana.org/assignments/media-types/media-types.xhtml, or in the MediaTypes sheet in the template.

`Required` `Must be MediaType from https://www.iana.org/assignments/media-types/media-types.xhtml`
#### CompressionFormat
Same as MediaType, but the compression format used. For example: "application/gzip".

`Optional` `Must be MediaType from https://www.iana.org/assignments/media-types/media-types.xhtml`
#### Format
format

`Optional`
#### Bytesize
The size of the distribution in bytes

`Optional` `Must be a positive integer`
## Step 4: Export
### Set up excel
In excel, in some localizations, it is necessary to set the decimal separator to "." and the thousands separator to ",". This can be done in the File->Options->Advanced>Editin options menu.
### Export csv
The Individual sheets can be exported with File->Export->Change File Type->CSV (Comma delimited) (*.csv)
