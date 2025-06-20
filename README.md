# NeuralSkin

An end-to-end web application that leverages deep learning to perform real-time analysis of skin lesion images for the preliminary detection of melanoma. This tool provides an intuitive interface for users to get an instant, AI-powered assessment.
https://drive.google.com/file/d/1XhETHcNBdMkR7zn7_NiQCA_l1flccbab/view?usp=sharing
Typescript

https://drive.google.com/file/d/11w2MKh0O45TGtAywCe_sc5Y9_jMyKHQV/view?usp=sharing
Python/Flask server

## Key Features

-   **Real-time AI Analysis:** Utilizes a trained ResNet50 model to classify skin lesions.
-   **Dual Image Input:** Users can either upload an image file or use their device's camera for a live capture.
-   **Binary Classification:** Classifies lesions as either **Benign** (non-cancerous) or **Malignant** (potentially cancerous).
-   **Dynamic & Intuitive UI:** The user interface provides clear, color-coded results (green for Benign, red for Malignant) for immediate understanding.
-   **Responsive Design:** The application is fully functional and optimized for both desktop and mobile devices.
-   **Spanish Language Interface:** The UI is presented entirely in Spanish to be accessible for native speakers.

## Screenshots

*(You can replace these placeholders with your own screenshots)*

| Main Interface                                     | Malignant Result                                       |
| -------------------------------------------------- | ------------------------------------------------------ |
| `![Screenshot of the main UI](./screenshot-1.png)` | `![Screenshot of a malignant result](./screenshot-2.png)` |

## Tech Stack

### Frontend

-   **Framework:** Next.js (App Router)
-   **Language:** TypeScript
-   **Styling:** Tailwind CSS
-   **Component Library:** shadcn/ui (scaffolded by v0.dev)
-   **API Communication:** Asynchronous `fetch`

### Backend

-   **Framework:** Python / Flask
-   **Functionality:** Serves the trained model via a REST API endpoint.
-   **Key Libraries:** Flask-Cors, Pillow, NumPy

### AI & Machine Learning

-   **Model Architecture:** ResNet50 (Transfer Learning)
-   **Framework:** TensorFlow / Keras
-   **Dataset:** HAM10000 ("Human Against Machine with 10000 training images")
-   **Training Environment:** Google Colab with GPU

## Installation and Setup

This project requires running two separate servers concurrently: the Python backend and the Next.js frontend.

### Prerequisites

-   **Python** (3.8 or newer)
-   **Node.js** and **npm**

### Backend Setup

1.  **Navigate to the backend folder:**
    ```bash
    cd melanoma-backend
    ```

2.  **Create and activate a virtual environment:**
    ```bash
    # Create the environment
    python -m venv venv

    # Activate on Windows
    .\venv\Scripts\activate

    # Activate on macOS/Linux
    source venv/bin/activate
    ```

3.  **Install Python dependencies:**
    *(Ensure you have a `requirements.txt` file with the necessary packages)*
    ```bash
    pip install -r requirements.txt
    ```

4.  **Run the Flask server:**
    ```bash
    python app.py
    ```
    The backend will now be running on `http://127.0.0.1:8080`. Keep this terminal window open.

### Frontend Setup

1.  **Open a new terminal.**

2.  **Navigate to the frontend folder:**
    ```bash
    cd melanoma-frontend
    ```

3.  **(One-time setup on a new machine):** Install `pnpm` globally:
    ```bash
    npm install -g pnpm
    ```

4.  **Install project dependencies:**
    ```bash
    pnpm install
    ```

5.  **Run the Next.js development server:**
    ```bash
    pnpm dev
    ```
    The frontend will now be running on `http://localhost:3000`. Keep this second terminal window open.

## Usage

1.  Ensure both the backend and frontend servers are running in their respective terminals.
2.  Open your web browser and navigate to `http://localhost:3000`.
3.  Use the "Subir Imagen" (Upload Image) or "Usar Cámara Web" (Use Webcam) buttons to provide an image for analysis.
4.  The result will be displayed on the screen shortly after.

## ⚠️ Medical Disclaimer

This AI diagnostic tool is intended for educational and screening purposes only. It **does not** constitute professional medical advice, diagnosis, or treatment. All results must be validated by a qualified healthcare professional. For any concerning lesions or symptoms, consult immediately with a board-certified dermatologist.
