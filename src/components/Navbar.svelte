<script>
  export let currentPage = 'home';
  import { Link } from 'svelte-routing';
</script>

<nav>
  <ul>
      <li class="{currentPage === 'home' ? 'active' : ''}">
          <Link to="/">Home</Link>
      </li>
      <li class="{currentPage === 'sales' ? 'active' : ''}">
          <Link to="/ventas">Ventas</Link>
      </li>
      <li class="{currentPage === 'customers' ? 'active' : ''}">
          <Link to="/clientes">Clientes</Link>
      </li>
      <li class="{currentPage === 'gestion-clientes' ? 'active' : ''}">
        <Link to="/gestion-clientes">Gestión Clientes</Link>
      </li>
  </ul>
</nav>

<style>
    nav {
        background-color: #f4f4f4;
        padding: 1rem 0;
        width: 100%;
        box-sizing: border-box;
    }
    
    nav ul {
      display: flex;
      justify-content: space-between;
      list-style: none;
      padding: 0;
      margin: 0;
      max-width: 100%;
    }
    
    nav ul li {
      flex: 1;
      margin: 0 30px; 
      text-align: center;
      background-color: #087df2;
      padding: 1rem;
      border-radius: 10px;
      transition: background-color 0.8s;
    }
    
    nav ul li :global(a) {
      color: white;
      font-size: 1.2rem;
      text-decoration: none;
      display: block;
      font-weight: bold;
    }
    
    nav ul li:hover {
      background-color: #004e9d;
    }
    
    .active {
      background-color: #004e9d;
    }
</style>