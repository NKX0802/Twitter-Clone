<div align="center">

# **🐦 Twitter Clone**

### A social media app where you can post, share images, like, and chat with an AI — built with React and Firebase.

🔗 **[Live Demo](https://twitter-clone-six-ruby.vercel.app)**

<br>

![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![Redux](https://img.shields.io/badge/Redux_Toolkit-593D88?style=for-the-badge&logo=redux&logoColor=white)
![React Router](https://img.shields.io/badge/React_Router-CA4245?style=for-the-badge&logo=reactrouter&logoColor=white)
![Firebase](https://img.shields.io/badge/Firebase-FFCA28?style=for-the-badge&logo=firebase&logoColor=black)
![OpenAI](https://img.shields.io/badge/OpenAI-412991?style=for-the-badge&logo=openai&logoColor=white)
![Bootstrap](https://img.shields.io/badge/Bootstrap-7952B3?style=for-the-badge&logo=bootstrap&logoColor=white)
![Vercel](https://img.shields.io/badge/Vercel-000000?style=for-the-badge&logo=vercel&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-646CFF?style=for-the-badge&logo=vite&logoColor=white)

</div>

---

## 📖 About

Twitter Clone is a social media web app where users sign up, log in, and share posts on their profile. Posts can include images, be liked, edited, and deleted. It also comes with a built-in AI chatbot powered by OpenAI. Authentication and data are handled by Firebase.

---

## ✨ Features

- 🔐 **Sign up & log in** — Secure authentication with Firebase Auth
- 📝 **Create posts** — Write a post and optionally attach an image
- 🖼️ **Image uploads** — Images are stored in Firebase Storage
- ❤️ **Like posts** — Like and unlike posts
- ✏️ **Edit & delete** — Update or remove your own posts
- 🤖 **AI chatbot** — Chat with an OpenAI-powered assistant in a popup modal
- 📱 **Responsive UI** — Built with React-Bootstrap for phone and desktop

---

## 🗄️ Database Structure

Posts are stored in **Cloud Firestore**, organized under each user:

```
users/{userId}/posts/{postId}
```

Each post document contains:

| Field | Type | Description |
|-------|------|-------------|
| `content` | string | The text of the post |
| `likes` | array | List of user IDs who liked the post |
| `imageUrl` | string | URL of the uploaded image (empty if none) |

> 🖼️ Uploaded images are saved in **Firebase Storage** under the `posts/` folder, and the download URL is stored in `imageUrl`.

---

## 🚀 Installation

### Prerequisites

- [Node.js](https://nodejs.org/) (v18 or higher)
- A [Firebase](https://firebase.google.com/) project (with Auth, Firestore, and Storage enabled)
- An [OpenAI API key](https://platform.openai.com/api-keys)

### Steps

1. **Clone the repository**
   ```bash
   git clone https://github.com/NKX0802/twitter-clone.git
   cd twitter-clone
   ```
2. **Install dependencies**
   ```bash
   npm install
   ```
3. **Set up environment variables** (see Configuration below)
4. **Run the development server**
   ```bash
   npm run dev
   ```
5. Open your browser at `http://localhost:5173`

---

## ⚙️ Configuration

Create a `.env` file in the root folder and add your keys:

```env
VITE_API_KEY=your_firebase_api_key
VITE_AUTH_DOMAIN=your_firebase_auth_domain
VITE_PROJECT_ID=your_firebase_project_id
VITE_STORAGE_ID=your_firebase_storage_bucket
VITE_MESSAGING_SENDER_ID=your_firebase_messaging_sender_id
VITE_APP_ID=your_firebase_app_id
VITE_OPENAI_API_KEY=your_openai_api_key
```

> ⚠️ **Never commit your `.env` file to GitHub.** Make sure `.env` is listed in your `.gitignore`.

---

## 📖 How to Use

1. **Sign up / Sign in** to create or access your account
2. **Create a post** — Write something and optionally attach an image
3. **Interact** — Like, edit, or delete posts
4. **Chat with the AI** — Open the chatbot modal and send a message
5. **Log out** when you're done

---

## 🐛 Future Improvements

- 🌐 **Home feed** — Show posts from all users, not just your own profile
- 👥 **Follow system** — Follow other users and see their posts
- 💬 **Comments** — Reply to posts
- 👤 **Editable profile** — Custom display name, bio, and avatar

---

## 📜 License

This project is licensed under the MIT License — feel free to use and modify it.
