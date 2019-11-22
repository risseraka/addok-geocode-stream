# addok-geocode-stream
Node.js stream API for addok geocoder

## Usage

### CLI

#### Installation

```
npm install -g addok-geocode-stream
```

#### Documentation

```
$ addok-geocode --help
addok-geocode [options]

Options:
  --help               Show help                                       [boolean]
  --version            Show version number                             [boolean]
  --service            Set geocoding service URL
                                   [default: "https://api-adresse.data.gouv.fr"]
  --columns            Select columns to geocode, in the right order
  --citycode           Filter results by citycode
  --postcode           Filter results by postcode
  --semicolon, --semi  Use semicolon (;) as separator                  [boolean]
  --tab                Use tabulation as separator                     [boolean]
  --concurrency        Set how many requests must be executed concurrently
                                                         [number] [default: "1"]
  --encoding           Set data encoding. Can be detected automatically
                                                     [choices: "utf8", "latin1"]
```

#### Example

```bash
cat my-addresses.csv | addok-geocode --columns numero,voie,code_postal,ville --semicolon > my-geocoded-addresses.csv
```
