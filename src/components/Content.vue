<template>
    <div class="container">
      <!-- Header -->
      <nav class="navbar navbar-dark bg-unique-primary">
        <button class="navbar-toggler" type="button" @click="toggleSidebar">
          <span class="navbar-toggler-icon"></span>
        </button>
        <span class="navbar-brand">We are cool!!</span>
      </nav>
  
      <!-- Sidebar -->
      <div class="row">
        <div class="col-md-3">
          <div class="bg-unique-secondary text-white p-3">
            <img src="https://randomuser.me/api/portraits/men/75.jpg" alt="User Avatar" class="img-fluid rounded-circle">
          </div>
          <ul class="list-group">
            <li class="list-group-item">
              <a href="/">
                <i class="fas fa-tachometer-alt"></i> <!-- Dashboard icon -->
                Dashboard
              </a>
            </li>
            <li class="list-group-item">
              <a href="/messages">
                <i class="fas fa-envelope"></i> <!-- Messages icon -->
                Messages
              </a>
            </li>
          </ul>
        </div>
      </div>
  
      <!-- Main Content (Login Form) -->
      <div class="col-md-9">
        <div class="mt-4">
          <div class="card">
            <div class="card-header text-center bg-unique-primary text-white">
              <h3>Welcome Back!</h3>
            </div>
            <div class="card-body">
              <form @submit.prevent="login">
                <div class="mb-3">
                  <label for="username" class="form-label text-unique-primary">Username</label>
                  <input type="text" class="form-control" id="username" v-model="username" placeholder="Enter your unique username">
                </div>
                <div class="mb-3">
                  <label for="password" class="form-label text-unique-primary">Password</label>
                  <input type="password" class="form-control" id="password" v-model="password" placeholder="Enter your unique password">
                </div>
                <button type="submit" class="btn btn-unique-primary btn-block">Login</button>
              </form>
            </div>
          </div>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: 'LoginContent',
    data() {
      return {
        sidebarOpen: true,
        username: '',
        password: '',
      };
    },
    methods: {
      toggleSidebar() {
        this.sidebarOpen = !this.sidebarOpen;
      },
      login() {
        // Replace with your login logic
        // Example: Authenticate the user using an API or other methods
        console.log('Logged in with username:', this.username);
      },
    },
  };
  </script>
  
  <style scoped>
  /* Custom styles for uniqueness */
  .container {
    padding: 20px;
    background-image: url('https://example.com/your-unique-background-image.jpg');
    background-size: cover;
    background-repeat: no-repeat;
  }
  
  .card-header {
    font-size: 24px;
  }
  
  .bg-unique-primary {
    background-color: #ffaa00; /* Unique primary color */
  }
  
  .bg-unique-secondary {
    background-color: #ffdd66; /* Unique secondary color */
  }
  
  .text-unique-primary {
    color: #ffaa00; /* Unique primary text color */
  }
  
  .btn-unique-primary {
    background-color: #ffaa00; /* Unique primary button color */
    border-color: #ffaa00; /* Unique primary button border color */
    color: #fff;
  }
  
  .btn-unique-primary:hover {
    background-color: #ff8800; /* Lighter color on hover */
    border-color: #ff8800; /* Lighter color on hover */
  }
  
  .footer {
    font-size: 14px;
  }
  </style>
  