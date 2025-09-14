# AirBnB Clone - Console

A command-line interface for managing AirBnB-style objects. This project implements a complete object management system with persistent storage and a web interface.

## 🏗️ Project Structure

```
alu-AirBnB_clone/
├── console.py              # Interactive command interpreter
├── models/                 # Object models and storage engine
│   ├── __init__.py
│   ├── base_model.py       # Base class with common functionality
│   ├── user.py            # User model
│   ├── state.py           # State model
│   ├── city.py            # City model
│   ├── place.py           # Place model
│   ├── amenity.py         # Amenity model
│   ├── review.py          # Review model
│   └── engine/         
│       ├── __init__.py
│       └── file_storage.py # JSON serialization/deserialization
├── tests/                  # Comprehensive test suite
│   ├── test_console.py
│   └── test_models/
├── web_static/            # Static web assets
│   ├── *.html            # Progressive web interface versions
│   ├── images/           # Icons and logos
│   └── styles/           # CSS styling files
├── AUTHORS               # Project contributors
└── README.md
```

## 🚀 Features

### Command-Line Interface
- **Interactive Console**: Full-featured command interpreter with tab completion
- **CRUD Operations**: Create, read, update, and delete objects
- **Advanced Queries**: Filter objects by class, count instances
- **Flexible Syntax**: Support for both traditional and dot-notation commands

### Data Models
- **BaseModel**: Core class with UUID generation, timestamps, and serialization
- **User**: User account management with authentication fields
- **State/City**: Geographic hierarchy for location management
- **Place**: Property listings with detailed attributes
- **Amenity**: Property features and services
- **Review**: User-generated content and ratings

### Storage System
- **JSON Persistence**: Automatic serialization to `file.json`
- **Object Reloading**: Seamless data restoration on startup
- **Type Safety**: Automatic type conversion for numeric values
- **Error Handling**: Robust file I/O with graceful fallbacks

### Web Interface
- **Progressive Enhancement**: Multiple HTML versions showcasing development stages
- **Responsive Design**: Mobile-friendly layouts with modern CSS
- **Interactive Elements**: Filtering, search, and dynamic content
- **Visual Assets**: Custom icons and styling for professional appearance

## 🛠️ Installation & Usage

### Prerequisites
- Python 3.8 or higher
- No external dependencies required

### Quick Start
```bash
# Clone the repository
git clone https://github.com/your-username/alu-AirBnB_clone.git
cd alu-AirBnB_clone

# Launch the console
python3 console.py
```

### Console Commands

#### Basic Operations
```bash
# Create a new object
(hbnb) create User
(hbnb) create Place

# Display object details
(hbnb) show User 1234-5678-9abc
(hbnb) show Place def0-1234-5678

# List all objects
(hbnb) all
(hbnb) all User

# Update object attributes
(hbnb) update User 1234-5678-9abc email "user@example.com"
(hbnb) update Place def0-1234-5678 name "Cozy Apartment"

# Delete an object
(hbnb) destroy User 1234-5678-9abc
```

#### Advanced Dot Notation
```bash
# Class-based operations
User.all()                    # List all users
User.count()                  # Count user instances
User.show("1234-5678-9abc")   # Show specific user
User.destroy("1234-5678-9abc") # Delete specific user

# Batch updates with dictionaries
User.update("1234-5678-9abc", {"first_name": "John", "last_name": "Doe"})
```

### Testing
```bash
# Run all tests
python3 -m unittest discover tests

# Run specific test modules
python3 -m unittest tests.test_console
python3 -m unittest tests.test_models.test_base_model
```

## 📊 Data Storage

Objects are automatically persisted to `file.json` using JSON serialization:

```json
{
  "User.1234-5678-9abc": {
    "id": "1234-5678-9abc",
    "created_at": "2024-01-15T10:30:00.000000",
    "updated_at": "2024-01-15T10:30:00.000000",
    "email": "user@example.com",
    "password": "hashed_password",
    "first_name": "John",
    "last_name": "Doe",
    "__class__": "User"
  }
}
```

## 🌐 Web Interface

The project includes a progressive web interface demonstrating different development stages:

- **Stage 0-1**: Basic HTML structure and styling
- **Stage 2-3**: Header, footer, and common elements
- **Stage 4-6**: Advanced filtering and search functionality
- **Stage 7-8**: Complete place listings with amenities
- **Stage 100-101**: Final polished interface

Access any HTML file directly in your browser to view the interface.

## 🏛️ Architecture

### Object-Oriented Design
- **Inheritance**: All models inherit from `BaseModel`
- **Encapsulation**: Private attributes with controlled access
- **Polymorphism**: Unified interface across all model types

### Storage Pattern
- **Singleton**: Single `FileStorage` instance manages all objects
- **Serialization**: Automatic JSON conversion with type preservation
- **Lazy Loading**: Objects loaded only when needed

### Command Pattern
- **Extensible**: Easy to add new commands
- **Consistent**: Uniform error handling and validation
- **Flexible**: Support for multiple command syntaxes

## 🧪 Testing Strategy

Comprehensive test coverage including:
- **Unit Tests**: Individual class and method testing
- **Integration Tests**: Console command functionality
- **Edge Cases**: Error handling and boundary conditions
- **Data Validation**: Serialization and deserialization accuracy

## 🚧 Future Enhancements

- **Database Integration**: MySQL/PostgreSQL support
- **RESTful API**: HTTP endpoints for web integration
- **Authentication**: User login and session management
- **Real-time Updates**: WebSocket support for live data
- **Advanced Search**: Elasticsearch integration
- **Image Management**: File upload and storage
- **Payment Integration**: Booking and payment processing

## 👥 Contributing

Contributions are welcome! Please feel free to submit pull requests or open issues for bugs and feature requests.

## 📝 License

This project is open source and available under the MIT License.

## 👨‍💻 Authors

- **Ineza Manzi Arnaud** - Core development and architecture
- **Leila Abbie Adoyo Omol** - Testing and documentation

---

*Built with ❤️ for the developer community* 

