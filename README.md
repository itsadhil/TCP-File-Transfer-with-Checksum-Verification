Here's a simple `README.md` file for your TCP file transfer application with checksum verification:

---

# TCP File Transfer with Checksum Verification

This is a Python-based application for transferring files between two systems using TCP. It provides two modes: **Sender** and **Receiver**, and includes checksum verification to ensure the file's integrity after transfer.

## Features

- **File Transfer**: Send files between two systems over TCP.
- **Checksum Verification**: Ensures file integrity using SHA-256 hash.
- **Chunk-based Transfer**: Files are split into chunks for smoother transfers and progress tracking.
- **Progress Bar**: Displays real-time progress of the file transfer.
- **Console Log**: Logs all activities such as connection status, chunk saving, and file verification results.

## Requirements

- Python 3.x
- Required libraries:
  - `socket`
  - `tkinter`
  - `threading`
  - `hashlib`
  - `os`

You can install the necessary libraries using `pip` if not already available:
```bash
pip install tkinter
```

## How to Use

1. **Run the Application**:
   - Execute the Python script to start the application.
   ```bash
   python file_transfer.py
   ```

2. **Select Mode**:
   - Choose between **Sender** and **Receiver** mode using the radio buttons at the top of the application.

### Sender Mode
1. **File Selection**: 
   - Select the file you want to send using the "Browse" button.
2. **Enter IP and Port**: 
   - Enter the IP address of the receiver and a port number.
3. **Start Transfer**: 
   - Click the "Start Transfer" button to send the file.
   - The file will be split into chunks and transferred.
   - A progress bar will show the file transfer progress.
   - Logs will be shown in the console area, and checksum verification will be done automatically.

### Receiver Mode
1. **Enter Port and Select Save Directory**: 
   - Enter the port number to listen on and select the directory where the received file should be saved.
2. **Start Reception**: 
   - Click the "Start Reception" button to wait for a file transfer.
   - The file will be reconstructed from the received chunks and saved.
   - A progress bar will show the reception progress.
   - Logs will be shown in the console area, and the checksum verification will ensure the file was transferred correctly.

## Project Structure

```
.
├── file_transfer.py     # Main Python script
└── README.md            # Project documentation
```

## License

This project is open-source and available under the MIT License.

