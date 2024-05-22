<template>
  <footer class="bg-dark text-white text-center py-4">
    <div class="container">
      <p class="mb-3">&copy; 2024 Warung Goib. All Rights Reserved.</p>
      
      <div>
        <a href="#" class="text-white me-2">Terms of Service</a>
        <span class="text-muted mx-1">|</span>
        <a href="#" class="text-white me-2">Privacy Policy</a>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: 'AppFooter'
};
</script>

<style scoped>
footer {
  width: 100%;
  background-image: linear-gradient(to right, #343a40, #1e272e); /* Tambahkan efek gradasi */
  border-top: 2px solid #007bff; /* Tambahkan garis atas */
  padding-top: 20px; /* Tambahkan ruang atas */
}

footer p {
  font-size: 14px;
  margin-bottom: 0;
  font-weight: bold; /* Tambahkan tebal pada teks keterangan */
}

footer a {
  text-decoration: none;
  transition: color 0.3s ease; /* Tambahkan efek hover */
}

footer a:hover {
  color: #ffc107; /* Ganti warna saat dihover */
}
</style>
