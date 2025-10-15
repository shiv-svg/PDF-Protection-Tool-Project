🔒 PDF Password Protector

This Python script provides a simple and effective way to secure your PDF documents by encrypting them with a user-defined password.

🛠️ Prerequisites

This script requires the PyPDF2 library, which is used for reading and writing PDF files.

Install Python 3 (if you don't have it already).

Install the required library:

pip install pypdf2

🚀 How to Use

The script is executed via the command line and requires three arguments: the input file path, the desired output file path, and the password.

Usage

python .\create_password_protected_pdf.py <input_pdf> <output_pdf> <password>

Note: For practical use, you must supply your own local PDF file path (e.g., /Users/John/Documents/report.pdf) as the <input_pdf>.

Example

To encrypt a file named invoice.pdf and save the protected version as invoice_secure.pdf with the password P@ssword123:

python .\create_password_protected_pdf.py invoice.pdf invoice_secure.pdf P@ssword123

📜 Script Logic

The core function, create_password_protected_pdf, performs the following steps:

It opens the input PDF in binary read mode ('rb').

It initializes a PdfReader and a PdfWriter from PyPDF2.

It copies all pages from the reader to the writer.




It calls pdf_writer.encrypt(password) to apply the protection.

The encrypted content is written to the specified output PDF file in binary write mode ('wb')
