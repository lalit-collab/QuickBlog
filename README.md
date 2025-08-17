Project Type: Blog application with admin panel.

Tech Stack:
Frontend: React, Vite, JavaScript, React Router DOM, Axios, Tailwind CSS, React Hot Toast, Quill.
Backend: Node.js, Express.js, MongoDB , Mongoose, CORS, Dotenv.
Other: ImageKit , Gemini API .

Architecture:
The application follows a typical MERN (MongoDB, Express, React, Node.js) stack architecture. It's a full-stack application with a separate client (frontend) and server (backend). The client handles the user interface and interacts with the server via API calls. The server handles data management, business logic, and API endpoints. The admin panel is integrated within the same application, likely using role-based access control.

Key Features:
1. Blog Post Creation (Admin): Ability for administrators to create, edit, and delete blog posts.
2. Blog Post Listing: Display a list of blog posts on the homepage.
3. Individual Blog Post View: Display a single blog post with its content.
4. Admin Authentication: Secure login for administrators.
5. Commenting System (Likely): Although not explicitly shown in the provided files, the presence of `Comment.js` model and `CommentTableItem.jsx` suggests a commenting feature.
6. Image Upload: Functionality for uploading images, likely using ImageKit.
7. Rich Text Editing: Using Quill for creating formatted blog content.
8. Newsletter Subscription (Likely): The presence of Newsletter component suggests this feature.
9. Dashboard (Admin): A dashboard providing an overview of blog statistics and management options.


Implementation Steps:

1. Database Setup:
   - INSTRUCTION: Set up a MongoDB database (e.g., using MongoDB Atlas).
   - INSTRUCTION: Define the `Blog` model using Mongoose with fields like `title`, `content`, `author`, `createdAt`, `updatedAt`, and `image`.

2. Backend API:
   - INSTRUCTION: Implement the following API endpoints using Express.js:
     - `POST /api/blog`: Create a new blog post (admin only).
     - `GET /api/blog`: Get all blog posts.
     - `GET /api/blog/:id`: Get a specific blog post by ID.
     - `PUT /api/blog/:id`: Update a blog post (admin only).
     - `DELETE /api/blog/:id`: Delete a blog post (admin only).
     - `POST /api/admin/login`: Admin login endpoint.
   - INSTRUCTION: Implement basic authentication middleware to protect admin routes. Use a simple username/password combination for the MVP.
   - INSTRUCTION: Implement image upload functionality using a library like Multer or directly to ImageKit.

3. Frontend Implementation:
   - INSTRUCTION: Create React components for:
     - `BlogList`: Displays a list of blog posts fetched from the API.
     - `BlogCard`: Displays a single blog post in the list.
     - `Blog`: Displays the full content of a blog post.
     - `AddBlog`: A form for creating new blog posts (admin only). Use Quill for rich text editing.
     - `Login`: Admin login form.
   - INSTRUCTION: Use React Router DOM to handle navigation between different pages (homepage, blog post view, admin panel).
   - INSTRUCTION: Use Axios to make API calls to the backend.
   - INSTRUCTION: Implement basic styling using Tailwind CSS.

4. Admin Panel:
   - INSTRUCTION: Create a simple admin panel with routes for:
     - `Dashboard`: Display a basic overview (e.g., total number of blog posts).
     - `ListBlog`: List all blog posts with options to edit or delete.
     - `AddBlog`: The same `AddBlog` component used for creating new posts.
     - `Login`: Admin login page.

5. Deployment:
   - INSTRUCTION: Deploy the frontend to a platform like Vercel.
   - INSTRUCTION: Deploy the backend to a platform like Vercel.

