<div align="center">

# URL Analysis Tool

![Cybersight Security URL Threat Analyzer](assets/logo.png)

The Cybersight Security URL Analysis Tool is a comprehensive tool that examines URLs for potential cybersecurity threats by leveraging multiple threat intelligence services including VirusTotal and URLScan.io. The tool combines scan results with WHOIS information and provides options to share findings via Twitter, offering security professionals and the public an easy way to assess website safety.

</div>

## Features:
- Scans URLs using VirusTotal and URLScan.io APIs
- Retrieves comprehensive WHOIS information for domains
- Combines threat intelligence from multiple sources
- Provides Twitter integration for sharing results
- Generates detailed, numbered reports for each analysis
- Offers intuitive command-line interface
- Supports configuration for multiple API services

**Important Note:** While this tool provides valuable threat intelligence, the results should be used as part of a comprehensive security analysis. Cybersight Security makes no warranties about the completeness or accuracy of the data presented.

## Data Sources

The application integrates with the following cybersecurity services:
- VirusTotal (Malware detection and URL analysis)
- URLScan.io (Website scanning and threat detection)
- WHOIS (Domain registration information)
- Twitter API (For sharing results)

## Technical Implementation

### Core Components

- **URL Scanning Modules:**
  - `virustotal_module.py`: Handles VirusTotal API interactions
  - `urlscan_module.py`: Manages URLScan.io submissions and results
  - `whois_module.py`: Retrieves domain registration details

- **Output Management:**
  - `output_module.py`: Formats and saves analysis reports
  - Numbered output files for tracking historical scans

- **Twitter Integration:**
  - `twitter_module.py`: Enables result sharing via Twitter API

- **Main Controller:**
  - `controller.py`: Orchestrates the workflow and user interface

## Installation and Usage

### Requirements

- Python 3.x
- API keys for VirusTotal, URLScan.io, and Twitter
- Required Python packages (listed in requirements.txt)

### Setup Instructions

1. **Clone the repository:**
   ```bash
   git clone https://github.com/cybersight/url-threat-analyzer.git
   cd url-threat-analyzer
   ```

2. **Install Python dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

3. **Configure API keys:**
   - Create configuration files in the `configs` directory for:
     - VirusTotal (`virustotal_config.json`)
     - URLScan.io (`urlscan_config.json`)
     - Twitter (`twitter_config.json`)

4. **Run the application:**
   ```bash
   python controller.py
   ```

5. **Follow the on-screen prompts** to analyze URLs and share results

## Configuration

Customize the tool's behavior through:
- **API Configuration:** Modify JSON files in the `configs` directory
- **Output Formatting:** Adjust report templates in `output_module.py`
- **Twitter Integration:** Modify tweet formatting in `twitter_module.py`

## License

This project is licensed under the GNU General Public License (GPL). This means you are free to:
- Use the software for any purpose
- Study how the software works and modify it
- Distribute copies
- Distribute modified versions

The full license text is included in the repository.

## About Cybersight Security

Cybersight Security is a leading provider of cybersecurity solutions, helping organizations protect their digital assets against evolving threats. Our URL Threat Analyzer is part of our commitment to security awareness and education.

**Disclaimer:** This tool is for informational purposes only. The threat analysis results are dependent on third-party services and should be verified through additional means. Cybersight Security makes no warranties about the completeness or accuracy of the data presented.