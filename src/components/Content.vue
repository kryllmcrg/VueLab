<template>
    <div class="container">
      <!-- Header -->
      <nav class="navbar navbar-dark bg-primary">
        <button class="navbar-toggler" type="button" @click="toggleSidebar">
          <span class="navbar-toggler-icon"></span>
        </button>
        <span class="navbar-brand">My App</span>
      </nav>
  
      <!-- Sidebar -->
      <div class="row">
        <div class="col-md-3">
          <div class="bg-primary text-white p-3">
            <img src="https://randomuser.me/api/portraits/women/75.jpg" alt="User Avatar" class="img-fluid rounded-circle">
          </div>
          <ul class="list-group">
            <li class="list-group-item">Dashboard</li>
            <li class="list-group-item">Messages</li>
          </ul>
        </div>
  
        <!-- Main Content (Login Form) -->
        <div class="col-md-9">
          <div class="mt-4">
            <div class="card">
              <div class="card-header text-center bg-primary text-white">
                <h3>Login</h3>
              </div>
              <div class="card-body">
                <form @submit.prevent="login">
                  <div class="mb-3">
                    <label for="username" class="form-label">Username</label>
                    <input type="text" class="form-control" id="username" v-model="username">
                  </div>
                  <div class="mb-3">
                    <label for="password" class="form-label">Password</label>
                    <input type="password" class="form-control" id="password" v-model="password">
                  </div>
                  <button type="submit" class="btn btn-primary btn-block">Login</button>
                </form>
              </div>
            </div>
          </div>
        </div>
      </div>
  
      <!-- Footer -->
      <footer class="bg-primary text-white text-center p-2">
        &copy; 2023 My App
      </footer>
    </div>
  </template>
  
  <script>
  export default {
    name: 'LoginContent',
    data() {
      return {
        sidebarOpen: true, // You can control sidebar open/close with this variable
        username: '',
        password: '',
      };
    },
    methods: {
      toggleSidebar() {
        this.sidebarOpen = !this.sidebarOpen;
      },
      login() {
        // Handle login logic here
        console.log('Logged in with username:', this.username);
      },
    },
  };
  </script>
  
  <style scoped>
  /* Custom styles */
  .container {
    padding: 20px;
  }
  
  .card-header {
    font-size: 24px;
  }
  
  .btn-primary {
    background-color: #007bff;
    border-color: #007bff;
  }
  
  .btn-primary:hover {
    background-color: #0056b3;
    border-color: #0056b3;
  }
  
  .footer {
    font-size: 14px;
  }
  </style>
  