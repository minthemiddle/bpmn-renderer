# BPMN Viewer Application

A web-based BPMN (Business Process Model and Notation) viewer built using bpmn-js.

## Features

- **BPMN Diagram Viewer**: View and interact with BPMN 2.0 diagrams
- **File Selection**: Choose from available BPMN files in the `bpmns` folder
- **Zoom Controls**:
  - Zoom in/out with dedicated buttons
  - Fit-to-viewport functionality
- **Panning**: Click and drag to navigate large diagrams
- **Responsive Design**: Adapts to different screen sizes
- **Console Logging**: View operation logs and error messages

## Getting Started

### Prerequisites

- Modern web browser (Chrome, Firefox, Edge, Safari)
- Web server to serve the files (due to CORS restrictions)

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/bpmn-viewer.git
   ```
2. Navigate to the project directory:
   ```bash
   cd bpmn-viewer
   ```
3. Place your BPMN files in the `bpmns` folder

### Usage

1. Start a web server in the project directory:
   ```bash
   python -m http.server 8000
   ```
2. Open your browser and navigate to:
   ```
   http://localhost:8000
   ```
3. Use the interface to:
   - Select a BPMN file from the dropdown
   - Open the selected diagram
   - Zoom in/out using the buttons
   - Fit the diagram to the viewport
   - Pan by clicking and dragging

## File Structure

```
bpmn-viewer/
├── bpmns/                  # Directory for BPMN files
│   ├── marketing.bpmn      # Example BPMN file
│   ├── seo.bpmn            # Example BPMN file
│   └── files.json          # List of available BPMN files
├── index.html              # Main application file
└── README.md               # This documentation
```

## Keyboard Shortcuts

- **Mouse Wheel**: Zoom in/out
- **Left Click + Drag**: Pan the diagram
- **Double Click**: Reset zoom

## Customization

### Adding New BPMN Files

1. Place your `.bpmn` files in the `bpmns` folder
2. Update the `bpmns/files.json` file to include your new files:
   ```json
   {
     "files": [
       "marketing.bpmn",
       "seo.bpmn",
       "your-new-file.bpmn"
     ]
   }
   ```

### Styling

You can customize the appearance by modifying the CSS in `index.html`:

- Change canvas size:
  ```css
  .canvas {
    height: 800px; /* Adjust as needed */
  }
  ```
- Modify colors:
  ```css
  body {
    background-color: #f5f5f5;
  }
  .canvas {
    border-color: #ccc;
  }
  ```

## Troubleshooting

### Common Issues

1. **Diagram not loading**:
   - Ensure the BPMN file is valid XML
   - Check browser console for errors
   - Verify file permissions

2. **Zoom issues**:
   - Try using the Fit button to reset the view
   - Ensure you're using a supported browser

3. **Panning not working**:
   - Make sure you're using left mouse button
   - Check if any browser extensions are interfering

## Dependencies

- [bpmn-js](https://github.com/bpmn-io/bpmn-js) - BPMN 2.0 rendering toolkit
- [Inter font](https://rsms.me/inter/) - Modern typeface for UI

## Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a new branch (`git checkout -b feature/YourFeature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin feature/YourFeature`)
5. Create a new Pull Request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- bpmn-js team for the excellent BPMN rendering library
- Open source community for inspiration and support
