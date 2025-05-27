# Book Management API - Backend Submission

A RESTful API for managing books built with Node.js and Hapi.js framework. This project is a submission for the Backend Development course by DBS (Dicoding Bootcamp Scholarship).

## 🚀 Features

- **Complete CRUD Operations**: Create, Read, Update, and Delete books
- **Data Validation**: Proper validation for all input fields
- **Error Handling**: Comprehensive error responses with appropriate HTTP status codes
- **Unique ID Generation**: Using nanoid for generating unique book IDs
- **Auto-calculated Fields**: Automatic calculation of `finished` status and timestamps
- **RESTful Design**: Following REST API best practices

## 📋 API Endpoints

### 1. Add Book
- **Method**: `POST`
- **URL**: `/books`
- **Body**: JSON with book details
- **Response**: Success with book ID or validation error

### 2. Get All Books
- **Method**: `GET`
- **URL**: `/books`
- **Response**: List of books (simplified format)

### 3. Get Book Details
- **Method**: `GET`
- **URL**: `/books/{bookId}`
- **Response**: Complete book details or 404 if not found

### 4. Update Book
- **Method**: `PUT`
- **URL**: `/books/{bookId}`
- **Body**: JSON with updated book details
- **Response**: Success message or error

### 5. Delete Book
- **Method**: `DELETE`
- **URL**: `/books/{bookId}`
- **Response**: Success message or 404 if not found

## 🛠️ Installation & Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/mtridryn/Submission-Backend---DBS.git
   cd Submission-Backend---DBS
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Start the server**
   ```bash
   npm start
   ```

4. **For development (with auto-restart)**
   ```bash
   npm run start-dev
   ```

The server will run on `http://localhost:9000`

## 📝 Usage Examples

### Add a Book
```bash
curl -X POST http://localhost:9000/books \
  -H "Content-Type: application/json" \
  -d '{
    "name": "Belajar Node.js",
    "year": 2023,
    "author": "John Doe",
    "summary": "Panduan lengkap belajar Node.js",
    "publisher": "Tech Publisher",
    "pageCount": 200,
    "readPage": 50,
    "reading": true
  }'
```

### Get All Books
```bash
curl -X GET http://localhost:9000/books
```

### Get Book by ID
```bash
curl -X GET http://localhost:9000/books/{bookId}
```

## 🏗️ Project Structure

```
├── src/
│   ├── books.js      # Data storage (array)
│   ├── handler.js    # Request handlers
│   ├── routes.js     # Route definitions
│   └── server.js     # Server configuration
├── .gitignore        # Git ignore rules
├── eslint.config.mjs # ESLint configuration
├── package.json      # Project dependencies
└── README.md         # Project documentation
```

## 🔧 Technologies Used

- **Node.js**: JavaScript runtime
- **Hapi.js**: Web framework
- **nanoid**: Unique ID generation
- **ESLint**: Code linting with Dicoding Academy style guide

## ✅ Submission Criteria Met

- ✅ **Criteria 1**: Application uses port 9000
- ✅ **Criteria 2**: Application runs with `npm start`
- ✅ **Criteria 3**: API can save books
- ✅ **Criteria 4**: API can display all books
- ✅ **Criteria 5**: API can display book details
- ✅ **Criteria 6**: API can update book data
- ✅ **Criteria 7**: API can delete books

## 📊 Testing

All endpoints have been thoroughly tested and work correctly:
- Input validation
- Error handling
- HTTP status codes
- Response formats

## 👨‍💻 Author

**Mutiara Indriyani**
- GitHub: [@mtridryn](https://github.com/mtridryn)

## 📄 License

This project is licensed under the ISC License.
