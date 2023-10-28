<template>
  <v-card>
    <v-layout>
      <!-- Header -->
      <v-app-bar app dark color="primary">
        <v-app-bar-nav-icon @click="toggleSidebar"></v-app-bar-nav-icon>
        <v-toolbar-title>My App</v-toolbar-title>
      </v-app-bar>

      <!-- Sidebar -->
      <v-navigation-drawer
        v-model="sidebarOpen"
        theme="dark"
        rail
        permanent
      >
        <v-list-item
          nav
          prepend-avatar="https://randomuser.me/api/portraits/women/75.jpg"
        ></v-list-item>

        <v-divider></v-divider>

        <v-list
          density="compact"
          nav
        >
          <v-list-item prepend-icon="mdi-view-dashboard" to="/" value="dashboard"></v-list-item>

          <v-list-item prepend-icon="mdi-forum" to="/manage" value="messages"></v-list-item>
        </v-list>
      </v-navigation-drawer>

      <!-- Main Content -->
      <v-main style="height: 750px">
        <div class="content">
          <h1>Welcome to My App</h1>
          <p>This is the main content of your sidebar.</p>
          <p>You can add more content here.</p>

          <!-- Table for Members and Positions -->
          <table class="table">
            <thead>
              <tr>
                <th>Member Name</th>
                <th>Position</th>
              </tr>
            </thead>
            <tbody>
              <tr>
                <td>Member 1</td>
                <td>Position 1</td>
              </tr>
              <tr>
                <td>Member 2</td>
                <td>Position 2</td>
              </tr>
              <tr>
                <td>Member 3</td>
                <td>Position 3</td>
              </tr>
              <!-- Add more rows as needed -->
            </tbody>
          </table>
        </div>
      </v-main>

      <!-- Footer -->
      <v-footer app dark color="primary">
        <span>&copy; 2023 My App</span>
      </v-footer>
    </v-layout>
  </v-card>
</template>

<script>
export default {
  name: 'Sidebar',
  data() {
    return {
      sidebarOpen: true, // You can control sidebar open/close with this variable
    };
  },
  methods: {
    toggleSidebar() {
      this.sidebarOpen = !this.sidebarOpen;
    },
  },
};
</script>

<style scoped>
/* Add your custom styles here */
.content {
  background-color: #f0f0f0;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  height: 100%;
  border-radius: 5px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.2);
}

h1 {
  font-size: 24px;
  color: #333;
}

p {
  font-size: 16px;
  color: #555;
}

.table {
  width: 100%;
  max-width: 600px; /* Adjust the width as needed */
  border-collapse: collapse;
  margin-top: 20px;
}

.table th, .table td {
  border: 1px solid #ddd;
  padding: 8px;
  text-align: left;
}

.table th {
  background-color: #f2f2f2;
}
</style>
