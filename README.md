# 🧩 Real-Time Sudoku Solver  

This project is a **Real-Time Sudoku Solver** that uses **Computer Vision** and **Deep Learning** to detect, recognize, and solve Sudoku puzzles from images or live video feed.  

The pipeline includes:  
- Detecting the Sudoku grid from an image or webcam feed.  
- Extracting digits from the grid using a pre-trained CNN model (`digitRecognition.h5`).  
- Solving the Sudoku puzzle using backtracking.  
- Displaying the solved Sudoku back on the original image/video in real time.  

---

## 📂 Project Structure  

```
├── digitRecognition.h5         # Pre-trained CNN model for digit recognition
├── requirements.txt            # Dependencies
├── RealTimeSudokuSolver.ipynb  # Notebook for real-time solving via webcam
├── sudokuSolver.ipynb          # Core Sudoku solving logic
├── sudoku testing.ipynb        # Testing and debugging notebook
├── realtime_sudoku_solver.py   # (Optional) Python script for direct run
```

---

## ⚙️ Installation  

1. Clone this repository and navigate to the project folder:  
   ```bash
   git clone <repo_url>
   cd sudoku-solver
   ```

2. Create a virtual environment (recommended):  
   ```bash
   python -m venv venv
   source venv/bin/activate   # On Linux/Mac
   venv\Scripts\activate      # On Windows
   ```

3. Install dependencies:  
   ```bash
   pip install -r requirements.txt
   ```

### Dependencies  
- `keras==2.3.1`  
- `numpy==1.22.0`  
- `opencv-python>=4.8.1.78`  
- `scipy==1.4.1`  
- `import-ipynb==0.1.3`  

---

## 🚀 Usage  

### 1. Run Sudoku Solver from an Image  
Open and run:  
```bash
jupyter notebook sudokuSolver.ipynb
```  
Upload an image of a Sudoku puzzle → the program detects, recognizes, solves, and overlays the solution.  

### 2. Real-Time Sudoku Solver (Webcam)  
Run:  
```bash
jupyter notebook RealTimeSudokuSolver.ipynb
```  
or (if you use the script I provided earlier):  
```bash
python realtime_sudoku_solver.py
```

### 3. Testing and Debugging  
Run:  
```bash
jupyter notebook "sudoku testing.ipynb"
```  
to test digit recognition and grid extraction separately.  

---

## 🧠 Model  

- `digitRecognition.h5` is a pre-trained **Convolutional Neural Network (CNN)** for classifying digits (1–9).  
- Trained on digit datasets similar to MNIST.  
- Used to recognize Sudoku digits from the grid.  

---

## 📸 Example Workflow  

1. Capture/Upload a Sudoku puzzle image.  
2. Detect the Sudoku grid with **OpenCV**.  
3. Recognize digits using the CNN model.  
4. Solve Sudoku with a **backtracking algorithm**.  
5. Overlay solution on the original image/video.  

---

## 📌 Future Improvements  

- Better recognition for handwritten Sudoku puzzles.  
- Faster real-time performance.  
- GUI support for drag-and-drop Sudoku uploads.  

---

## ✨ Acknowledgements  

- **OpenCV** for image processing.  
- **Keras** for digit recognition.  
- Classic backtracking for Sudoku solving.  
