<template>
  <div class="admin-layout">
    <!-- Sidebar -->
    <div class="admin-sidebar" :class="{ 'collapsed': isSidebarCollapsed }">
      <div class="sidebar-header">
        <img :src="ImagePaths.logo.logoTab" alt="Logo" class="w-45px" />
        <h1>Admin Panel</h1>
      </div>
      
      <nav class="sidebar-nav">
        <router-link 
          to="/admin" 
          class="nav-item" 
          :class="{ 'active': $route.path === '/admin' }"
          :title="isSidebarCollapsed ? 'Tổng quan' : ''"
          exact
        >
          <i class="fas fa-chart-line"></i>
          <span>Tổng quan</span>
        </router-link>
        
        <router-link 
          to="/admin/users" 
          class="nav-item" 
          :class="{ 'active': $route.path.startsWith('/admin/users') }"
          :title="isSidebarCollapsed ? 'Quản lý người dùng' : ''"
        >
          <i class="fas fa-users"></i>
          <span>Quản lý người dùng</span>
        </router-link>
        
        <router-link 
          to="/admin/reports" 
          class="nav-item" 
          :class="{ 'active': $route.path.startsWith('/admin/reports') }"
          :title="isSidebarCollapsed ? 'Bài viết bị báo cáo' : ''"
        >
          <i class="fas fa-flag"></i>
          <span>Bài viết bị báo cáo</span>
        </router-link>
        
        <router-link 
          to="/admin/feedback" 
          class="nav-item" 
          :class="{ 'active': $route.path.startsWith('/admin/feedback') }"
          :title="isSidebarCollapsed ? 'Đóng góp ý kiến' : ''"
        >
          <i class="fas fa-comments"></i>
          <span>Đóng góp ý kiến</span>
        </router-link>

        <router-link 
          to="/" 
          class="nav-item"
          :title="isSidebarCollapsed ? 'Quay lại trang chủ' : ''"
        >
          <i class="fas fa-arrow-left"></i>
          <span>Quay lại trang chủ</span>
        </router-link>
      </nav>

      <!-- Move toggle button outside of header -->
      <button class="toggle-sidebar" @click="toggleSidebar">
        <i class="fas" :class="isSidebarCollapsed ? 'fa-chevron-right' : 'fa-chevron-left'"></i>
      </button>
    </div>

    <!-- Main Content -->
    <div class="admin-main">
      <div class="admin-header">
        <div class="header-left">
          <h2>{{ currentPageTitle }}</h2>
        </div>
        <div class="header-right">
          <div class="admin-profile">
            <img :src="adminAvatar" alt="Admin" class="admin-avatar">
            <span class="admin-name">{{ adminName }}</span>
            <button class="btn-logout" @click="handleLogout">
              <i class="fas fa-sign-out-alt"></i>
            </button>
          </div>
        </div>
      </div>
      
      <div class="admin-content">
        <router-view></router-view>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ImagePaths } from '@/assets/img/imagePaths';
import { computed, ref } from 'vue';
import { useRoute, useRouter } from 'vue-router';

const route = useRoute();
const router = useRouter();

// Sidebar state
const isSidebarCollapsed = ref(false);

const toggleSidebar = () => {
  isSidebarCollapsed.value = !isSidebarCollapsed.value;
};

// Mock admin data - replace with real data from your auth system
const adminAvatar = 'https://i.pravatar.cc/150?u=admin';
const adminName = 'Admin';



const currentPageTitle = computed(() => {
  switch (route.path) {
    case '/admin':
      return 'Tổng quan';
    case '/admin/users':
      return 'Quản lý người dùng';
    case '/admin/reports':
      return 'Bài viết bị báo cáo';
    case '/admin/feedback':
      return 'Đóng góp ý kiến';
    default:
      return 'Admin Panel';
  }
});

const handleLogout = () => {
  // Handle logout logic here
  router.push('/login');
};
</script>

<style lang="scss" scoped>
@use '@/views/admin/AdminLayout.scss';
</style> 