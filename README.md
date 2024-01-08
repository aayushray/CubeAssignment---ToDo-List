# Project Name

This project contains the backend and frontend components for [Project Name]. The backend is built using Django, and the frontend is built using React JS.

## Prerequisites

Before running the project, make sure you have the following installed:

- Python (version 3.10)
- Node.js (version 18.8)

To set up the backend, follow these steps:

1. Create a virtual environment:
    ```bash
    python -m venv myenv
    ```

2. Activate the virtual environment:
    ```bash
    source myenv/bin/activate
    ```

3. Install Django:
    ```bash
    pip install django
    ```

## Getting Started

To get started with the project, follow these steps:

### Backend

1. Navigate to the `backend` folder:
    ```bash
    cd backend
    ```

2. Install the required Python packages:
    ```bash
    pip install -r requirements.txt
    ```

3. To generate and replace the secret key in the Django settings, follow these steps:

    1. Open the `backend/backend/settings.py` file.
    2. Locate the section with the comment `# SECURITY WARNING`.
    3. Generate a New Secret Key:
        1. Open a Python shell, and run the following commands:

            ```python
            import secrets
            secrets.token_urlsafe(50)
            ```
        2. Copy the generated secret key.

    3. Replace the line `SECRET_KEY = config('DJANGO_SECRET_KEY')` with the following code:

        ```python
        SECRET_KEY = 'your_generated_secret_key'
        ```

        Replace `'your_generated_secret_key'` with the actual secret key you generated.

    4. Save the `settings.py` file.

    It is important to keep the secret key confidential and not share it publicly.

4. Run the Django development server:
    ```bash
    python manage.py runserver
    ```

    The backend server should now be running on `http://localhost:8000`.

### Frontend

1. Navigate to the `frontend` folder:
    ```bash
    cd frontend
    ```

2. Install the required Node.js packages:
    ```bash
    npm install
    ```

3. Start the React development server:
    ```bash
    npm start
    ```

    The frontend server should now be running on `http://localhost:3000`.

## Usage

- Access the frontend application, which has been integrated with the local backend server running at port 8000, by visiting `http://localhost:3000` in your web browser.
- Use the backend API endpoints at `http://localhost:8000/api/` for interacting with the backend API.

## Contributing

Contributions are welcome! If you find any issues or have suggestions, please open an issue or submit a pull request.
