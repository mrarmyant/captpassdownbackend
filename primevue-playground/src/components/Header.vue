<template>
  <div class="p-mb-5 p-grid">
    <div class="p-col-12 p-text-center"><h1>SciffScribble</h1></div>
    <Menubar :model="navItems" class="p-col-12" />
  </div>
</template>
<script>
import Menubar from "primevue/menubar";
export default {
  name: "Header",
  components: {
    Menubar,
  },
  data() {
    return {
      navItems: [
        {
          label: "Home",
          icon: "pi pi-fw pi-home",
          to: { name: "Home" },
        },
        {
          label: "About",
          icon: "pi pi-fw pi-info-circle",
          to: { name: "About" },
        },
        {
          label: "Add New",
          icon: "pi pi-fw pi-plus",
          items: [
            {
              label: "Boat",
              icon: "pi pi-fw pi-plus",
              to: { name: "Add Boat" },
            },
          ],
        },
        {
          label: "View",
          icon: "pi pi-fw pi-pencil",
          items: [
            {
              label: "Boats",
              icon: "pi pi-fw pi-align-left",
              to: { name: "View Boats" },
            },
            {
              label: "Logs",
              icon: "pi pi-fw pi-align-right",
              // to: { name: "View Logs" },
            },
            {
              label: "Advanced Search",
              icon: "pi pi-fw pi-align-right",
              // to: { name: "Advanced Search" },
            },
          ],
        },
        {
          label: "Account",
          icon: "pi pi-fw pi-power-off",
          // to: { name: "User" },
        },
      ],
    };
  },
  methods: {
    print: function () {
      console.log("hi");
    },
  },
};
</script>