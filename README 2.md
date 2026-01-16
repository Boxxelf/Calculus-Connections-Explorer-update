# Calculus Concept Map

An interactive, web-based visualization tool that maps the relationships between calculus topics and their applications in computer science. This project helps students and educators understand how fundamental calculus concepts connect to modern CS fields like machine learning, algorithms, artificial intelligence, and computer graphics.

## Live Demo

**[View the interactive visualization →](https://boxxelf.github.io/Calculus-Concept-Map/)**

## Recent Updates

**December 2025:**
- Added 33 missing Calculus II topics, including all 5 differential equations topics (AW, AX, AY, AZ, BA)
- Added all missing connections between calculus topics (33 new edges)
- Fixed topic code mappings for nodes Z (Der15), AD (Int4), and AH (Int10)
- Enhanced special mapping function to handle duplicate number_id cases
- Total nodes: 65 (previously 32), Total connections: 94 (previously 61)

See [UPDATE_NOTES1201.md](UPDATE_NOTES1201.md) for detailed information about the fixes and improvements.

## Features

### Interactive Visualization
- **Force-directed graph** with drag-and-drop node manipulation
- **Smart zooming** that automatically focuses on selected nodes
- **Dynamic node sizing** based on connection count when all courses are selected
- **Color-coded courses**: Calculus I (Blue) and Calculus II (Green)

### Hierarchical Course Structure
- **Three-level hierarchy**: Course → Core Idea → Topic
- **Expandable sidebar** for easy navigation
- **Topic codes** (e.g., Lim1, Der2, Int3) matching node labels in the visualization
- **Course selection** with disabled state for unselected courses

### Advanced Filtering & Interaction
- **CS topic filtering**: Select CS topics to highlight related calculus nodes
- **Connection strength visualization**: Red glow for strong connections (level 2), regular highlight for level 1
- **Prerequisite highlighting**: When clicking a calculus node, incoming prerequisite nodes are highlighted while outgoing nodes fade
- **Filtered rationales**: View only rationales matching selected CS topics

### User Experience
- **Instructions overlay** on first visit with easy reopen option
- **Responsive design** that adapts to different screen sizes
- **Smooth animations** and transitions throughout
- **Empty state guidance** when no nodes are selected

## Getting Started

### Prerequisites
- A modern web browser (Chrome, Firefox, Safari, or Edge)
- Python 3.x (for local development)

### Local Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/Boxxelf/Calculus-Concept-Map.git
   cd Calculus-Concept-Map
   ```

2. **Start a local server**
   ```bash
   python3 -m http.server 8000
   ```

3. **Open in browser**
   Navigate to `http://localhost:8000` in your web browser

## How to Use

### Basic Navigation
1. **Explore the map**: The full graph is visible on load. Use mouse wheel to zoom, drag to pan
2. **Hover over nodes**: See full topic names in tooltips
3. **Click nodes**: View detailed rationales and highlight connections
4. **Drag nodes**: Rearrange the layout to your preference
5. **Click background**: Reset the view and clear selections

### Selecting CS Topics
1. Expand **CS Topics** in the left sidebar
2. Click on any CS topic (e.g., "Gradient descent", "Neural networks")
3. Related calculus nodes will be highlighted with a red glow
4. Nodes with stronger connections (level 2) appear slightly larger

### Browsing Calculus Topics
1. Expand **Calculus Courses** in the left sidebar
2. Click on a course (Calculus I or Calculus II) to expand core ideas
3. Click on a core idea to see individual topics
4. Click any topic to highlight it in the visualization and view its details

### Viewing Details
1. Select CS topics to filter (optional)
2. Click a calculus node in the visualization or sidebar
3. View filtered rationales in the right panel
4. See incoming prerequisite nodes highlighted and outgoing nodes faded

### Course Selection
- Toggle course checkboxes to enable/disable entire courses
- When a course is unchecked, all its topics become disabled and grayed out
- This helps focus on specific course content

## Project Structure

```
Calculus-Concept-Map/
├── index.html          # Main HTML structure
├── style.css           # Styling and layout
├── app.js              # Core visualization logic (D3.js)
├── graph_data.json     # Calculus topics with relationships and CS applications
├── Calculus topic labeling scheme.csv  # Topic codes and hierarchical structure
├── ML_Alg_AI_CG_Rationales_081525(Rationales).csv  # CS topic rationales
├── UPDATE_NOTES1201.md # Detailed update notes and fixes
├── DEPLOYMENT.md       # Deployment guide
└── README.md           # This file
```

## Data Structure

### Graph Data (`graph_data.json`)
- **Nodes**: Each calculus topic contains:
  - `id`: Unique identifier
  - `topicCode`: Codified label (e.g., "Lim1", "Der2")
  - `label`: Full topic name
  - `calc_level`: "Calculus I" or "Calculus II"
  - `cs_categories`: Array of relevant CS fields
  - `rationales`: Detailed explanations organized by CS category and topic

- **Edges**: Directed relationships representing prerequisites
  - `source`: Prerequisite topic ID
  - `target`: Dependent topic ID

### Topic Labeling Scheme (`Calculus topic labeling scheme.csv`)
- Defines the hierarchical structure: Course → Core Idea → Topic Code → Topic Name
- Used to generate the sidebar navigation and map topic codes to nodes

## Technology Stack

- **D3.js v7**: Force-directed graph visualization
- **Vanilla JavaScript**: No framework dependencies
- **CSS3**: Modern styling with gradients and animations
- **Python HTTP Server**: Simple local development server

## Customization

### Adding New Topics

1. **Update the CSV file**: Add entries to `Calculus topic labeling scheme.csv`
   ```csv
   Course,Core Idea,Topic Code,Topic Name
   Calculus I,Derivatives,Der19,New Topic Name
   ```

2. **Update graph data**: Add corresponding node to `graph_data.json`
   ```json
   {
     "id": "NEW_ID",
     "topicCode": "Der19",
     "label": "New Topic Name",
     "calc_level": "Calculus I",
     "cs_categories": ["Machine Learning"],
     "rationales": {
       "Machine Learning": [
         {
           "cs_topic": "Application Name",
           "rationale": "Why this matters..."
         }
       ]
     }
   }
   ```

3. **Add relationships**: Create edges in `graph_data.json`
   ```json
   {
     "source": "PREREQUISITE_ID",
     "target": "NEW_ID"
   }
   ```

### Styling

Modify `style.css` to customize:
- Color schemes for courses
- Node sizes and styles
- Layout and spacing
- Typography

## Contributing

Contributions are welcome! Areas where help is needed:

- **Content**: Add more calculus topics or CS applications
- **Visualization**: Enhance graph algorithms or interactions
- **UI/UX**: Improve user experience and accessibility
- **Documentation**: Expand guides and examples
- **Bug fixes**: Report and fix issues

### Contribution Guidelines

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is open source and available for educational purposes. Free to use, modify, and distribute for educational and research purposes.

## Acknowledgments

- Built with [D3.js](https://d3js.org/)
- Designed for computer science students learning calculus
- Inspired by the need to visualize prerequisite relationships in mathematics education

## Contact & Support

- **Issues**: [GitHub Issues](https://github.com/Boxxelf/Calculus-Concept-Map/issues)
- **Questions**: Open an issue or discussion on GitHub

---

