pip install pandas fpdf
pip install fpdf
import pandas as pd
from fpdf import FPDF
#from os import path
#file_path="/content/sample_data/california_housing_train.csv"
# Load data from a CSV file
def load_data(file_path):
    data = pd.read_csv(file_path)
    return data

# Analyze data (example: calculate mean, max, min)
def analyze_data(data):
    analysis = {
        'mean': data.mean(),
        'max': data.max(),
        'min': data.min()
    }
    return analysis

# Generate PDF report
def generate_pdf(analysis, output_file):
    pdf = FPDF()  # Create an instance of FPDF
    pdf.add_page()  # Add a page
    pdf.set_font("Arial", size=12)  # Set font

    pdf.cell(200, 10, txt="Data Analysis Report", ln=True, align='C')
    pdf.ln(10)

    pdf.set_font("Arial", size=10)
    pdf.cell(200, 10, txt="Mean Values:", ln=True)
    pdf.multi_cell(0, 10, str(analysis['mean']))
    pdf.ln(10)

    pdf.cell(200, 10, txt="Maximum Values:", ln=True)
    pdf.multi_cell(0, 10, str(analysis['max']))
    pdf.ln(10)

    pdf.cell(200, 10, txt="Minimum Values:", ln=True)
    pdf.multi_cell(0, 10, str(analysis['min']))
    pdf.ln(10)

    pdf.output(output_file)  # Save the PDF

# Main function
def main():
    file_path = '/content/sample_data/california_housing_train.csv'  # Replace with your CSV file path
    output_file = 'report.pdf'

    data = load_data(file_path)
    analysis = analyze_data(data)
    generate_pdf(analysis, output_file)
    print(f"Report generated successfully: {output_file}")

if __name__ == "__main__":
    main()
print(generate_pdf)
