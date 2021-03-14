<template>
    <div>
  <b-navbar toggleable="lg" type="dark" variant="info">
    <b-navbar-brand href="../groupomania" >
        <img src="../assets/icon-left-font-monochrome-black1.png" alt="Groupomania logo" id="logo">
    </b-navbar-brand>
    <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

    <b-collapse id="nav-collapse" is-nav>

      <!-- Right aligned nav items -->
      <b-navbar-nav class="ml-auto">
        <b-nav-form>
          <b-form-input size="sm" class="mr-sm-2" placeholder="Username"></b-form-input>
          <b-form-input size="sm" class="mr-sm-2" placeholder="Password"></b-form-input>
          <b-button size="sm" class="my-2 my-sm-1" type="submit">Log in</b-button>
        </b-nav-form>

        <b-nav-item-dropdown right>
          <!-- Using 'button-content' slot -->
          <template #button-content>
           <b-avatar icon="people-fill"></b-avatar>
          </template>
          <b-dropdown-item href="../Signup">
          <b-button variant="outline-info" class="mb-2">
            <b-icon icon="pencil-fill"></b-icon> Sign Up
            </b-button>
            </b-dropdown-item>
          <b-dropdown-item href="../profile">
          <b-button variant="outline-info" class="mb-2">
            <b-icon icon="person-fill"></b-icon> Account
            </b-button>
            </b-dropdown-item>
          <b-dropdown-item href="../signout">
          <b-button variant="outline-info" class="mb-2">
            <b-icon icon="power" aria-hidden="true"></b-icon>
             Logout
        </b-button>
        </b-dropdown-item>
        </b-nav-item-dropdown>
      </b-navbar-nav>
    </b-collapse>
  </b-navbar>
</div>
</template>
