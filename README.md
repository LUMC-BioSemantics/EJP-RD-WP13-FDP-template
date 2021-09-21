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
Description of the dataset with the language tag

`Optional`
#### Language
Langugage of the dataset. The two letter code of the language can be obtained from https://id.loc.gov/vocabulary/iso639-1.html, or from the languages sheet in the template.

`two letter language code`
#### License
License of the resource. For example, https://creativecommons.org/licenses/by/4.0/deed.en

`Optional` `Must start with "http://" or "https://"`
#### ContactPoint
ContactPoint

`optional` `Must start with "http://", "https://" or "mailto:"`
#### LandingPage
Home page of the dataset

`optional` `Must start with "http://" or "https://"`
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
#### Dataset Title
#### Description
#### Language
#### License
#### AccessURL
#### DownloadURL
#### MediaType
#### CompressionFormat
#### Format
#### Bytesze

## Step 4: Export
### Set up excel
In excel, in some localizations, it is necessary to set the decimal separator to "." and the thousands separator to ",". This can be done in the File->Options->Advanced>Editin options menu.
### Export csv
The Individual sheets can be exported with File->Export->Change File Type->CSV (Comma delimited) (*.csv)
