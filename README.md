# Image to Text Converter

This application is a simple OCR (Optical Character Recognition) tool built with HTML, CSS, JavaScript, Tesseract.js, and jsPDF. It allows users to upload an image with text, recognize the text in the image using OCR, and download the recognized text as a PDF.

## Techstack
## Working
* Image Upload:
1.The user uploads an image containing text by clicking the file input.
2.The uploaded image is displayed in the application, allowing the user to confirm the image is correct.

* Starting OCR:
1.When the user clicks "Start OCR," the application initializes Tesseract.js, an OCR library that processes the image.
2.The Tesseract.createWorker() function creates a worker (background process) for handling OCR without blocking the main application.
3.The worker loads the English language data and recognizes text from the uploaded image.
4.During processing, a progress indicator shows the OCR status, updating as Tesseract reads and analyzes the image.

*Displaying Recognized Text:
1.After Tesseract completes the OCR process, it returns the recognized text, which is displayed in a read-only text area within the application.
2.The text area allows users to review and confirm the accuracy of the extracted text.

Generating a PDF:
1.Once the text is displayed, the "Download PDF" button is enabled.
2.When clicked, this button uses the jsPDF library to generate a PDF file containing the recognized text.
3.The splitTextToSize function ensures that long lines of text wrap correctly within the PDF.
4.Finally, the PDF is downloaded to the user’s device as "OCR_Result.pdf."
