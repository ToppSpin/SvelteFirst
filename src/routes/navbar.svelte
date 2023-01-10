<script>
    // Show mobile icon and display menu
    let showMobileMenu = false;

    // List of navigation items
    const navItems = [
      { label: "Jacob!", href: "/about" },
      { label: "Item 1", href: "/about" },
      { label: "Item 2", href: "/about" },
      { label: "Item 3", href: "/about" },
      { label: "Item 4", href: "/about" },
      { label: "Item 5", href: "/about" },
      { label: "Item 6", href: "/about" },
      { label: "Item 7", href: "/about" },
      { label: "Item 8", href: "/about" }
    ];
  
    // Mobile menu click event handler
    const handleMobileIconClick = () => (showMobileMenu = !showMobileMenu);
  
    // Attach media query listener on mount hook
  </script>
  
  <nav>
    <div class="inner">
      <!-- svelte-ignore a11y-click-events-have-key-events -->
      <div on:click={handleMobileIconClick} class={`mobile-icon${showMobileMenu ? ' active' : ''}`}>
        <div class="middle-line"></div>
      </div>
      <ul class="navbar-list">
        {#each navItems as item}
          <li>
            <a href={item.href}>{item.label}</a>
          </li>
        {/each}
      </ul>
    </div>
  </nav>
  
  <style>
    nav {
      background-color: rgba(0, 0, 0, 0.8);
      font-family: "Helvetica Neue", "Helvetica", "Arial", sans-serif;
      height: 45px;
    }
  
    .inner {
      max-width: 980px;
      padding-left: 20px;
      padding-right: 20px;
      margin: auto;
      box-sizing: border-box;
      display: flex;
      align-items: center;
      height: 100%;
    }
  
    .navbar-list {
      display: none;
      width: 100%;
      justify-content: space-between;
      margin: 0;
      padding: 0 40px;
    }
  
    .navbar-list.mobile {
      background-color: rgba(0, 0, 0, 0.8);
      position: fixed;
      display: block;
      height: calc(100% - 45px);
      bottom: 0;
      left: 0;
    }
  
    .navbar-list li {
      list-style-type: none;
      position: relative;
    }
  
    .navbar-list a {
      color: #fff;
      text-decoration: none;
      display: flex;
      height: 45px;
      align-items: center;
      padding: 0 10px;
      font-size: 13px;
    }
  
    @media only screen and (min-width: 767px) {
      .mobile-icon {
        display: none;
      }
  
      .navbar-list {
        display: flex;
        padding: 0;
      }
  
      .navbar-list a {
        display: inline-flex;
      }
    }
  </style>