<script>
  // Exported properties which can be passed as props
  export let parent = [];
  export let size = 150;  // DEFAULT_SIZE
  export let onClick = null;
  export let menuItems = [
    {id: 'one', title: 'One'},
    {id: 'two', title: 'Two'}
  ];
  export let closeOnClick = false;

  // Internal state
  let radius = 55;
  let innerRadius = 18;
  let sectorSpace = 3.5;
  let sectorCount = Math.max(menuItems.length, 3);  // MIN_SECTORS
  let scale = 1;
  let holder = null;
  let parentMenu = [];
  let parentItems = [];
  let levelItems = null;
</script>

let currentMenu = null;

  function open() {
    if (!currentMenu) {
      currentMenu = createMenu('menu inner', menuItems);
      // The appending will be handled reactively in the template
      // Next tick logic will be handled using Svelte's afterUpdate hook or transitions
    }
  }

  function close(bool) {
    // The AJAX request using jQuery will need to be replaced with a Fetch API call or other AJAX methods
    // Other direct DOM manipulations will be handled reactively

    if (currentMenu) {
      // This will handle the removal of the menu reactively
      currentMenu = null;
    }
  }

  function createHolder() {
    // The holder creation will be handled in the template itself
    // The properties like width and height will be applied using inline styles or CSS classes based on size
  }

  function createMenu(className, items) {
    // This function's logic needs to be extracted further from the RadialMenu.js
    // For now, we're just setting up a placeholder
    return {};
  }

<style>
  /* main.css content will be pasted here */
</style>
