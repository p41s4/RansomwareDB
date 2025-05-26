# MalwareDB - Threat Actor Monitoring System

A comprehensive system for monitoring and analyzing threat actors, with a focus on ransomware groups. The system provides real-time scoring based on various risk factors and sends email notifications for critical threats.

## Features

- Real-time threat actor monitoring
- Risk scoring system based on multiple factors
- Email notifications for critical threats
- Detailed threat actor information
- Historical data visualization
- YARA rules integration
- Customizable industry and country monitoring

## Scoring System

The system uses a 10-point scoring system based on the following factors:

- Industry targeting: +3 points for attacks on the monitored industry
- Country targeting: +2 points for attacks in the monitored country
- Recent activity: +2 points for activity in the last 30 days
- Potential impact:
  - +100 victims: +3 points
  - 50-99 victims: +2 points
  - -50 victims: +1 point

## Customization

### Industry Selection

You can customize the monitored industry by changing the `SECTOR_MONITORIZADO` variable in the code. Here's the complete list of available sectors:

- Business Services
- Technology
- Manufacturing
- Healthcare
- Transportation/Logistics
- Financial
- Government
- Agriculture and Food Production
- Energy
- Education
- Hospitality and Tourism
- Consumer Services
- Public Sector
- Financial Services
- Government Facilities
- Construction
- Information Technology
- Healthcare and Public Health
- Critical Manufacturing
- Transportation Systems
- Telecommunication
- Education Facilities
- Communication
- Commercial Facilities
- Food and Agriculture
- Emergency Services
- Retail
- Healthcare Services
- Wholesale & Retail
- Engineering
- Chemical
- Advertising, Marketing & Public Relations
- Energy & Utilities
- Internet & Telecommunication Services
- Defense Industrial Base
- Transportation
- Law Firms & Legal Services
- Automotive
- Community, Social Services & Non-Profit Organisations
- Agriculture
- Aerospace
- Food & Beverages
- Others
- Broadcasting
- Real Estate
- Water and Wastewater Systems
- Nuclear Reactors, Materials, and Waste
- IT Manufacturing
- Shipping & Logistics
- Legal
- Business Services, Technology

### Country Selection

You can customize the monitored country by changing the `PAIS_MONITORIZADO` variable in the code. Use the two-letter country code (e.g., "ES" for Spain, "US" for United States).

### Email Configuration

To set up email notifications:

1. Configure your Gmail account:
   - Enable two-step verification
   - Generate an "App Password"
   - Replace the `EMAIL_PASSWORD` in the code with your generated password

2. Update the following variables in the code:
   - `EMAIL_SENDER`: Your Gmail address
   - `EMAIL_RECIPIENT`: Recipient email address
   - `SMTP_SERVER`: "smtp.gmail.com"
   - `SMTP_PORT`: 587

## Installation

1. Clone the repository
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Configure your settings in the code
4. Run the application:
   ```bash
   streamlit run MalwareDB.py
   ```

## System Requirements

- Python 3.7+
- Streamlit
- Pandas
- Requests
- Altair
- SQLite3

## Project Structure

- `MalwareDB.py`: Main application file
- `malware_db.sqlite`: SQLite database file
- `requirements.txt`: Python dependencies

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Contact

For any questions or suggestions, please contact the project maintainer. 