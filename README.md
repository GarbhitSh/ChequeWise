# ChequeWise

**ChequeWise** is a comprehensive solution for automating the processing of bank cheques using machine learning and optical character recognition (OCR). By leveraging computer vision techniques and advanced OCR capabilities, ChequeWise efficiently extracts and processes essential information from cheques, streamlining the workflow for banks and financial institutions.

## Features

- **Automated Data Extraction**: Automatically extracts key fields from bank cheques, including payer's name, account number, amount, and date.
- **Advanced OCR**: Utilizes Google Cloud Vision for high-accuracy text recognition from cheque images.
- **Image Enhancement**: Applies preprocessing techniques with OpenCV and other libraries to improve image quality and extraction accuracy.
- **Django Integration**: Includes a Django app that can be seamlessly integrated into existing Django projects for easy deployment and management.

## Libraries and Tools Used

- **OpenCV**: For image processing and feature extraction.
- **Pillow (PIL)**: For image manipulation and enhancement.
- **NumPy**: For numerical operations and array handling.
- **OS**: For interacting with the operating system.
- **Shutil**: For file operations and management.
- **Google Cloud Vision**: For powerful OCR capabilities.
- **Keras**: For machine learning models, if applicable.
- **Regex**: For text pattern matching and validation.
- **Imutils**: For convenience functions in image processing.
- **Scikit-image**: For additional image processing functionalities.

## Setup and Installation

1. **Clone the Repository:**

    ```bash
    git clone https://github.com/GarbhitSh/ChequeWise.git
    cd ChequeWise
    ```

2. **Create and Activate a Virtual Environment:**

    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
    ```

3. **Install Required Packages:**



4. **Setup Google Cloud Vision:**
   - Follow the [Google Cloud Vision documentation](https://cloud.google.com/vision/docs/quickstart) to set up authentication and obtain your API key.
   - Set up the environment variable for authentication:

     ```bash
     export GOOGLE_APPLICATION_CREDENTIALS="path/to/your/credentials.json"
     ```

5. **Run the Django App (if integrating):**

    ```bash
    python manage.py runserver
    ```

## Usage

1. **Data Extraction:**
   - Place cheque images in the designated folder.
   - Run the extraction script:

     ```bash
     python extract_data.py
     ```

   - The script will process the images and output the extracted data.

2. **Django Integration:**
   - Add the provided Django app to your `INSTALLED_APPS` in your Django project’s `settings.py`.

     ```python
     INSTALLED_APPS = [
         # Other apps
         'cheque_app',
     ]
     ```

   - Include the app’s URLs in your project’s `urls.py`:

     ```python
     from django.urls import path, include

     urlpatterns = [
         path('cheque/', include('cheque_app.urls')),
     ]
     ```

## Configuration

- **Configuration File:** Update the `config.json` file with paths, settings, and API keys as needed.
- **Environment Variables:** Ensure all required environment variables (e.g., Google Cloud Vision credentials) are properly set.

## Contributing

Contributions are welcome! If you have suggestions or improvements, please open an issue or submit a pull request. Ensure that your contributions adhere to the project's guidelines.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
