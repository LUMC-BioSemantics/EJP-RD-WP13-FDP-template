# EJP-RD WP19 FDP template
This template simplifies the collection of metadata attributes of datasets and their distributions. By exporting csv, and adding this to Github repositories, advantage is taken of the version control and collaboration capabilities of Git and Github.

## Step 1: Preparation
### Download template
Download the template.xlsx file from this repository. This template works best with Microsoft Excel, but also works with LibreOffice.
When creating new metadata, this template can be used immediately. When editing existing metadata, the existing csv files should be pasted into the template.
## Step 2: Dataset sheet
The first sheet of the template contains metadata of the datasets.
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
License of the resource. For example, https://creativecommons.org/licenses/by/4.0/deed.en

`Optional` `Must start with "http://" or "https://"`
#### ContactPoint
ContactPoint

`Optional` `Must start with "http://", "https://" or "mailto:"`
#### LandingPage
Home page of the dataset

`Optional` `Must start with "http://" or "https://"`
#### Keywords
Keyword(s) related to the dataset with the language tag, separated by comma's (,)

`Optional`
#### Themes
List of concepts that describe the dataset, separated by comma's (,)

`Required` `each theme must start with "http://" or "https://"` `Themes should be separated with comma's`

## Step 3: Distribution sheet
The second sheet of the template contains metadata of the distributions
### Column explanation
#### Title
The name of the dataset with the language tag.

`Required`
#### Dataset Title
The title of the dataset that is associated with the distribution.

`Required` `Must be the title of a dataset in the datasets sheet`
#### Description
Description of the distribution with the language tag.

`Optional`
#### Language
Language of the dataset. The two letter code of the language can be obtained from https://id.loc.gov/vocabulary/iso639-1.html, or from the languages sheet in the template.

`Optional` `Two letter language code`
#### License
License of the resource. For example, https://creativecommons.org/licenses/by/4.0/deed.en

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
#### Bytesze
The size of the distribution in bytes

`Optional` `Must be a positive integer`
## Step 4: Export
### Set up excel
In excel, in some localizations, it is necessary to set the decimal separator to "." and the thousands separator to ",". This can be done in the File->Options->Advanced>Editin options menu.
### Export csv
The Individual sheets can be exported with File->Export->Change File Type->CSV (Comma delimited) (*.csv)
