<template>
  <header class="header">
    <h1 class="logo">ⓄⓁⓈⒽⓄⓅ</h1>
    <nav>
      <a href="#" class="nav-link">𝗛𝗢𝗠𝗘</a>
      <a href="#" class="nav-link">𝗣𝗥𝗢𝗗𝗨𝗖𝗧</a>
      <a href="#" class="nav-link">𝗖𝗢𝗡𝗧𝗔𝗖𝗧</a>
      <img src="/src/assets/cart.png" alt="Cart" class="cart-icon" />
    </nav>
  </header>
</template>

<script>
export default {
  name: 'Header'
};
</script>

<style scoped>
.header {
  background-color: #333;
  color: white;
  padding: 10px 0;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.logo {
  margin: 0;
}

.nav-link {
  color: white;
  margin: 0 15px;
  text-decoration: none;
}

.cart-icon {
  width: 30px;
  height: 30px;
  margin-left: 20px;
  margin-right: 20px;
}

/* Membuat tulisan di tengah */
.header h1, .nav {
  display: flex;
  align-items: center;
}

.nav {
  flex-grow: 1;
  justify-content: center;
}
</style>
