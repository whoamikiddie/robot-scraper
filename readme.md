# RobotScraper

RobotScraper is a simple Go application that fetches and processes the `robots.txt` file from specified domains. It extracts allowed and disallowed paths and saves them as full URLs to a specified text file.

## Features

- Fetches `robots.txt` files over HTTP and HTTPS.
- Extracts allowed and disallowed paths.
- Saves results as full URLs in a text file.
- Supports multiple domains in a single run.
- Provides an animated saving message for a better user experience.

## Installation

1. Clone the repository:
   
   ```bash
   git clone https://github.com/whoamikiddie/robot-scraper
   cd RobotScraper
   ```

2. Build the application:
   ```bash
   go build robot.go
   ```

## Usage

To run the program, use the following command:

```bash
go run robot.go -d <domain1,domain2,...> [-s <filename>]
```

### Options

- `-d`, `--domain`: Specify one or more domains to scrape, separated by commas.
- `-s`, `--save`: Specify a filename to save the output in text format. (default: `output.txt`)

### Example

To fetch `robots.txt` from `example.com` and `example.org` and save the output to `output.txt`, run:

```bash
go run robot.go -d example.com,example.org -s output.txt
```

## Output

The output file will contain:

- **Allowed URLs**: Paths that are allowed for web crawlers.
- **Disallowed URLs**: Paths that are not allowed for web crawlers.

Each entry will be saved in the format:
```
Allowed URLs:
https://example.com/path1
https://example.com/path2

Disallowed URLs:
https://example.com/path3
https://example.com/path4


