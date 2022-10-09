<script>
  let sidebar_show = false;
  let isDarkMode = false;
  let theDocument;
  import { onMount } from "svelte";

  $: theDocument &&
    (sidebar_show
      ? document.body.classList.add("is-sidebar-open")
      : document.body.classList.remove("is-sidebar-open"));

  $: theDocument &&
    (isDarkMode
      ? document.documentElement.classList.add("dark")
      : document.documentElement.classList.remove("dark"));

  onMount(() => {
    theDocument = document;
  });
</script>

<!-- Page Wrapper -->
<div class="min-h-100vh flex grow bg-slate-50 dark:bg-navy-900">
  <!-- Sidebar -->
  <div class="sidebar print:hidden">
    <!-- Main Sidebar -->
    <div class="main-sidebar">
      <div
        class="flex h-full w-full flex-col items-center border-r border-slate-150 bg-white dark:border-navy-700 dark:bg-navy-800"
      >
        <div class="flex h-18 w-full items-center justify-between pl-4 pr-1">
          <p class="text-base tracking-wider text-slate-800 dark:text-navy-100">
            Sidebar
          </p>
          <button
            on:click={() => (sidebar_show = false)}
            class="btn h-7 w-7 rounded-full p-0 text-primary hover:bg-slate-300/20 focus:bg-slate-300/20 active:bg-slate-300/25 dark:text-accent-light/80 dark:hover:bg-navy-300/20 dark:focus:bg-navy-300/20 dark:active:bg-navy-300/25 lg:hidden"
          >
            <svg
              xmlns="http://www.w3.org/2000/svg"
              class="h-6 w-6"
              fill="none"
              viewBox="0 0 24 24"
              stroke="currentColor"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M15 19l-7-7 7-7"
              />
            </svg>
          </button>
        </div>
        <div class="px-4 sm:px-5 w-full">
          <ul class="space-y-1.5 font-inter font-medium">
            <li>
              <a
                class="flex items-center space-x-2 rounded-lg bg-primary px-4 py-2.5 tracking-wide text-white outline-none transition-all dark:bg-accent"
                href="/"
              >
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  class="h-5 w-5"
                  fill="none"
                  viewBox="0 0 24 24"
                  stroke="currentColor"
                >
                  <path
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    stroke-width="1.5"
                    d="M13 7h8m0 0v8m0-8l-8 8-4-4-6 6"
                  />
                </svg>
                <span>Getting start</span>
              </a>
            </li>
            <li>
              <a
                class="group flex space-x-2 rounded-lg px-4 py-2.5 tracking-wide outline-none transition-all hover:bg-slate-100 hover:text-slate-800 focus:bg-slate-100 focus:text-slate-800 dark:hover:bg-navy-600 dark:hover:text-navy-100 dark:focus:bg-navy-600 dark:focus:text-navy-100"
                href="/"
              >
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  class="h-5 w-5 text-slate-400 transition-colors group-hover:text-slate-500 group-focus:text-slate-500 dark:text-navy-300 dark:group-hover:text-navy-200 dark:group-focus:text-navy-200"
                  fill="none"
                  viewBox="0 0 24 24"
                  stroke="currentColor"
                >
                  <path
                    d="M9 17a2 2 0 11-4 0 2 2 0 014 0zM19 17a2 2 0 11-4 0 2 2 0 014 0z"
                  />
                  <path
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    stroke-width="1.5"
                    d="M13 16V6a1 1 0 00-1-1H4a1 1 0 00-1 1v10a1 1 0 001 1h1m8-1a1 1 0 01-1 1H9m4-1V8a1 1 0 011-1h2.586a1 1 0 01.707.293l3.414 3.414a1 1 0 01.293.707V16a1 1 0 01-1 1h-1m-6-1a1 1 0 001 1h1M5 17a2 2 0 104 0m-4 0a2 2 0 114 0m6 0a2 2 0 104 0m-4 0a2 2 0 114 0"
                  />
                </svg>

                <span>Shipping</span>
              </a>
            </li>
            <li>
              <a
                class="group flex space-x-2 rounded-lg px-4 py-2.5 tracking-wide outline-none transition-all hover:bg-slate-100 hover:text-slate-800 focus:bg-slate-100 focus:text-slate-800 dark:hover:bg-navy-600 dark:hover:text-navy-100 dark:focus:bg-navy-600 dark:focus:text-navy-100"
                href="/"
              >
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  class="h-5 w-5 text-slate-400 transition-colors group-hover:text-slate-500 group-focus:text-slate-500 dark:text-navy-300 dark:group-hover:text-navy-200 dark:group-focus:text-navy-200"
                  viewBox="0 0 24 24"
                  fill="none"
                  stroke="currentColor"
                >
                  <path
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    stroke-width="1.5"
                    d="M3 10h18M7 15h1m4 0h1m-7 4h12a3 3 0 003-3V8a3 3 0 00-3-3H6a3 3 0 00-3 3v8a3 3 0 003 3z"
                  />
                </svg>
                <span>Payments</span>
              </a>
            </li>
            <li>
              <a
                class="group flex space-x-2 rounded-lg px-4 py-2.5 tracking-wide outline-none transition-all hover:bg-slate-100 hover:text-slate-800 focus:bg-slate-100 focus:text-slate-800 dark:hover:bg-navy-600 dark:hover:text-navy-100 dark:focus:bg-navy-600 dark:focus:text-navy-100"
                href="/"
              >
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  class="h-5 w-5 text-slate-400 transition-colors group-hover:text-slate-500 group-focus:text-slate-500 dark:text-navy-300 dark:group-hover:text-navy-200 dark:group-focus:text-navy-200"
                  fill="none"
                  viewBox="0 0 24 24"
                  stroke="currentColor"
                >
                  <path
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    stroke-width="1.5"
                    d="M16 15v-1a4 4 0 00-4-4H8m0 0l3 3m-3-3l3-3m9 14V5a2 2 0 00-2-2H6a2 2 0 00-2 2v16l4-2 4 2 4-2 4 2z"
                  />
                </svg>
                <span>Returns</span>
              </a>
            </li>
            <li>
              <a
                class="group flex space-x-2 rounded-lg px-4 py-2.5 tracking-wide outline-none transition-all hover:bg-slate-100 hover:text-slate-800 focus:bg-slate-100 focus:text-slate-800 dark:hover:bg-navy-600 dark:hover:text-navy-100 dark:focus:bg-navy-600 dark:focus:text-navy-100"
                href="/"
              >
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  class="h-5 w-5 text-slate-400 transition-colors group-hover:text-slate-500 group-focus:text-slate-500 dark:text-navy-300 dark:group-hover:text-navy-200 dark:group-focus:text-navy-200"
                  fill="none"
                  viewBox="0 0 24 24"
                  stroke="currentColor"
                >
                  <path
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    stroke-width="1.5"
                    d="M16 7a4 4 0 11-8 0 4 4 0 018 0zM12 14a7 7 0 00-7 7h14a7 7 0 00-7-7z"
                  />
                </svg>
                <span>My Account</span>
              </a>
            </li>
            <li>
              <a
                class="group flex space-x-2 rounded-lg px-4 py-2.5 tracking-wide outline-none transition-all hover:bg-slate-100 hover:text-slate-800 focus:bg-slate-100 focus:text-slate-800 dark:hover:bg-navy-600 dark:hover:text-navy-100 dark:focus:bg-navy-600 dark:focus:text-navy-100"
                href="/"
              >
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  class="h-5 w-5 text-slate-400 transition-colors group-hover:text-slate-500 group-focus:text-slate-500 dark:text-navy-300 dark:group-hover:text-navy-200 dark:group-focus:text-navy-200"
                  viewBox="0 0 24 24"
                  fill="none"
                >
                  <path
                    d="M21 12C21 13.1819 20.7672 14.3522 20.3149 15.4442C19.8626 16.5361 19.1997 17.5282 18.364 18.364C17.5282 19.1997 16.5361 19.8626 15.4442 20.3149C14.3522 20.7672 13.1819 21 12 21C10.8181 21 9.64778 20.7672 8.55585 20.3149C7.46392 19.8626 6.47177 19.1997 5.63604 18.364C4.80031 17.5282 4.13738 16.5361 3.68508 15.4442C3.23279 14.3522 3 13.1819 3 12C3 9.61305 3.94821 7.32387 5.63604 5.63604C7.32387 3.94821 9.61305 3 12 3C14.3869 3 16.6761 3.94821 18.364 5.63604C20.0518 7.32387 21 9.61305 21 12Z"
                    stroke="currentColor"
                    stroke-width="1.5"
                    stroke-linecap="round"
                    stroke-linejoin="round"
                  />
                  <path
                    d="M12.0449 15.8486C12.625 15.8486 13.1318 15.6729 13.5654 15.3213C13.999 14.9697 14.2393 14.5303 14.2861 14.0029H15.8242C15.7949 14.5479 15.6074 15.0664 15.2617 15.5586C14.916 16.0508 14.4531 16.4434 13.873 16.7363C13.2988 17.0293 12.6895 17.1758 12.0449 17.1758C10.75 17.1758 9.71875 16.7451 8.95117 15.8838C8.18945 15.0166 7.80859 13.833 7.80859 12.333V12.0605C7.80859 11.1348 7.97852 10.3115 8.31836 9.59082C8.6582 8.87012 9.14453 8.31055 9.77734 7.91211C10.416 7.51367 11.1689 7.31445 12.0361 7.31445C13.1025 7.31445 13.9873 7.63379 14.6904 8.27246C15.3994 8.91113 15.7773 9.74023 15.8242 10.7598H14.2861C14.2393 10.1445 14.0049 9.64062 13.583 9.24805C13.167 8.84961 12.6514 8.65039 12.0361 8.65039C11.21 8.65039 10.5684 8.94922 10.1113 9.54688C9.66016 10.1387 9.43457 10.9971 9.43457 12.1221V12.4297C9.43457 13.5254 9.66016 14.3691 10.1113 14.9609C10.5625 15.5527 11.207 15.8486 12.0449 15.8486Z"
                    fill="currentColor"
                  />
                </svg>
                <span>Copyright &amp; Legal</span>
              </a>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </div>

  <!-- App Header Wrapper-->
  <nav class="header print:hidden">
    <!-- App Header  -->
    <div
      class="header-container relative flex w-full bg-white dark:bg-navy-750 print:hidden"
    >
      <div class="flex w-full items-center justify-between">
        <div class="h-7 w-7">
          <button
            class="menu-toggle ml-0.5 flex h-7 w-7 flex-col justify-center space-y-1.5 text-primary outline-none focus:outline-none dark:text-accent-light/80"
            :class="$store.global.isSidebarExpanded && 'active'"
            class:active={sidebar_show}
            on:click={() => (sidebar_show = !sidebar_show)}
          >
            <span />
            <span />
            <span />
          </button>
        </div>

        <button
          on:click={() => (isDarkMode = !isDarkMode)}
          class="btn h-8 w-8 rounded-full p-0 hover:bg-slate-300/20 focus:bg-slate-300/20 active:bg-slate-300/25 dark:hover:bg-navy-300/20 dark:focus:bg-navy-300/20 dark:active:bg-navy-300/25"
        >
          <svg
          class:hidden={!isDarkMode}

            class="h-6 w-6 text-amber-400"
            fill="currentColor"
            viewBox="0 0 24 24"
          >
            <path
              d="M11.75 3.412a.818.818 0 01-.07.917 6.332 6.332 0 00-1.4 3.971c0 3.564 2.98 6.494 6.706 6.494a6.86 6.86 0 002.856-.617.818.818 0 011.1 1.047C19.593 18.614 16.218 21 12.283 21 7.18 21 3 16.973 3 11.956c0-4.563 3.46-8.31 7.925-8.948a.818.818 0 01.826.404z"
            />
          </svg>
          <svg
          class:hidden={isDarkMode}
            class="h-6 w-6 text-amber-400"
            viewBox="0 0 20 20"
            fill="currentColor"
          >
            <path
              fill-rule="evenodd"
              d="M10 2a1 1 0 011 1v1a1 1 0 11-2 0V3a1 1 0 011-1zm4 8a4 4 0 11-8 0 4 4 0 018 0zm-.464 4.95l.707.707a1 1 0 001.414-1.414l-.707-.707a1 1 0 00-1.414 1.414zm2.12-10.607a1 1 0 010 1.414l-.706.707a1 1 0 11-1.414-1.414l.707-.707a1 1 0 011.414 0zM17 11a1 1 0 100-2h-1a1 1 0 100 2h1zm-7 4a1 1 0 011 1v1a1 1 0 11-2 0v-1a1 1 0 011-1zM5.05 6.464A1 1 0 106.465 5.05l-.708-.707a1 1 0 00-1.414 1.414l.707.707zm1.414 8.486l-.707.707a1 1 0 01-1.414-1.414l.707-.707a1 1 0 011.414 1.414zM4 11a1 1 0 100-2H3a1 1 0 000 2h1z"
              clip-rule="evenodd"
            />
          </svg>
        </button>
      </div>
    </div>
  </nav>

  <main class="main-content w-full px-[var(--margin-x)] pb-8">
    <div class="flex items-center space-x-4 py-5 lg:py-6">
      <h2
        class="text-xl font-medium text-slate-800 dark:text-navy-50 lg:text-2xl"
      >
        Blank Template
      </h2>
    </div>

    <div class="mt-5 space-y-4">
      <div
        class="alert flex rounded-lg bg-slate-200 px-4 py-4 text-slate-600 dark:bg-navy-500 dark:text-navy-100 sm:px-5"
      >
        This is simple alert
      </div>

      <div
        class="alert flex rounded-lg bg-primary px-4 py-4 text-white dark:bg-accent sm:px-5"
      >
        This is simple alert
      </div>

      <div
        class="alert flex rounded-lg bg-secondary px-4 py-4 text-white sm:px-5"
      >
        This is simple alert
      </div>

      <div class="alert flex rounded-lg bg-info px-4 py-4 text-white sm:px-5">
        This is simple alert
      </div>

      <div
        class="alert flex rounded-lg bg-success px-4 py-4 text-white sm:px-5"
      >
        This is simple alert
      </div>

      <div
        class="alert flex rounded-lg bg-warning px-4 py-4 text-white sm:px-5"
      >
        This is simple alert
      </div>

      <div class="alert flex rounded-lg bg-error px-4 py-4 text-white sm:px-5">
        This is simple alert
      </div>
    </div>

    <div class="inline-space mt-5">
      <div class="avatar h-12 w-12">
        <div
          class="is-initial rounded-full bg-slate-200 text-base uppercase text-slate-600 dark:bg-navy-500 dark:text-navy-100"
        >
          jd
        </div>
      </div>

      <div class="avatar h-12 w-12">
        <div
          class="is-initial rounded-full bg-primary text-base uppercase text-white dark:bg-accent"
        >
          jd
        </div>
      </div>

      <div class="avatar h-12 w-12">
        <div
          class="is-initial rounded-full bg-secondary text-base uppercase text-white"
        >
          jd
        </div>
      </div>

      <div class="avatar h-12 w-12">
        <div
          class="is-initial rounded-full bg-info text-base uppercase text-white"
        >
          jd
        </div>
      </div>

      <div class="avatar h-12 w-12">
        <div
          class="is-initial rounded-full bg-success text-base uppercase text-white"
        >
          jd
        </div>
      </div>

      <div class="avatar h-12 w-12">
        <div
          class="is-initial rounded-full bg-warning text-base uppercase text-white"
        >
          jd
        </div>
      </div>

      <div class="avatar h-12 w-12">
        <div
          class="is-initial rounded-full bg-error text-base uppercase text-white"
        >
          jd
        </div>
      </div>
    </div>
    <div class="inline-space mt-5">
      <div
        class="badge bg-slate-150 text-slate-800 dark:bg-navy-500 dark:text-navy-100"
      >
        Default
      </div>
      <div class="badge bg-primary text-white dark:bg-accent">Primary</div>
      <div class="badge bg-secondary text-white">Secondary</div>
      <div class="badge bg-info text-white">Info</div>
      <div class="badge bg-success text-white">Success</div>
      <div class="badge bg-warning text-white">Warning</div>
      <div class="badge bg-error text-white">Error</div>
      <div class="badge bg-navy-700 text-white dark:bg-navy-900">Dark</div>
      <div class="badge bg-slate-150 text-slate-800">Light</div>
    </div>

    <div class="inline-space mt-5 flex flex-wrap">
      <button
        class="btn rounded-full bg-slate-150 font-medium text-slate-800 hover:bg-slate-200 focus:bg-slate-200 active:bg-slate-200/80 dark:bg-navy-500 dark:text-navy-50 dark:hover:bg-navy-450 dark:focus:bg-navy-450 dark:active:bg-navy-450/90"
      >
        Default
      </button>
      <button
        class="btn rounded-full bg-primary font-medium text-white hover:bg-primary-focus focus:bg-primary-focus active:bg-primary-focus/90 dark:bg-accent dark:hover:bg-accent-focus dark:focus:bg-accent-focus dark:active:bg-accent/90"
      >
        Primary
      </button>
      <button
        class="btn rounded-full bg-secondary font-medium text-white hover:bg-secondary-focus focus:bg-secondary-focus active:bg-secondary-focus/90"
      >
        Secondary
      </button>
      <button
        class="btn rounded-full bg-info font-medium text-white hover:bg-info-focus focus:bg-info-focus active:bg-info-focus/90"
      >
        Info
      </button>
      <button
        class="btn rounded-full bg-success font-medium text-white hover:bg-success-focus focus:bg-success-focus active:bg-success-focus/90"
      >
        Success
      </button>
      <button
        class="btn rounded-full bg-warning font-medium text-white hover:bg-warning-focus focus:bg-warning-focus active:bg-warning-focus/90"
      >
        Warning
      </button>
      <button
        class="btn rounded-full bg-error font-medium text-white hover:bg-error-focus focus:bg-error-focus active:bg-error-focus/90"
      >
        Error
      </button>
    </div>
    <div class="grid grid-cols-1 gap-4 sm:gap-5 lg:grid-cols-3 lg:gap-6">
      <div class="card px-4 py-4 sm:px-5">
        <div>
          <h2
            class="text-lg font-medium tracking-wide text-slate-700 line-clamp-1 dark:text-navy-100"
          >
            Simple Card
          </h2>
        </div>
        <div class="pt-2">
          <p>
            Lorem ipsum dolor sit, amet consectetur adipisicing elit. Aut
            laboriosam praesentium adipisci iure doloribus accusamus animi quos.
          </p>
        </div>
      </div>
      <div class="card rounded-2xl px-4 py-4 sm:px-5">
        <div>
          <h2
            class="text-lg font-medium tracking-wide text-slate-700 line-clamp-1 dark:text-navy-100"
          >
            Rounded Card
          </h2>
        </div>
        <div class="pt-2">
          <p>
            Lorem ipsum dolor sit, amet consectetur adipisicing elit. Aut
            laboriosam praesentium adipisci iure doloribus accusamus animi quos.
          </p>
        </div>
      </div>
      <div
        class="card border border-slate-150 px-4 py-4 shadow-none dark:border-navy-600 sm:px-5"
      >
        <div>
          <h2
            class="text-lg font-medium tracking-wide text-slate-700 line-clamp-1 dark:text-navy-100"
          >
            Bordered Card
          </h2>
        </div>
        <div class="pt-2">
          <p>
            Lorem ipsum dolor sit, amet consectetur adipisicing elit. Aut
            laboriosam praesentium adipisci iure doloribus accusamus animi quos.
          </p>
        </div>
      </div>
      <div
        class="rounded-lg bg-primary px-4 py-4 text-white dark:bg-accent sm:px-5"
      >
        <div>
          <h2 class="text-lg font-medium tracking-wide line-clamp-1">
            Primary Card
          </h2>
        </div>
        <div class="pt-2">
          <p>
            Lorem ipsum dolor sit, amet consectetur adipisicing elit. Aut
            laboriosam praesentium adipisci iure doloribus accusamus animi quos.
          </p>
        </div>
      </div>
      <div class="rounded-lg bg-secondary px-4 py-4 text-white sm:px-5">
        <div>
          <h2 class="text-lg font-medium tracking-wide line-clamp-1">
            Secondary Card
          </h2>
        </div>
        <div class="pt-2">
          <p>
            Lorem ipsum dolor sit, amet consectetur adipisicing elit. Aut
            laboriosam praesentium adipisci iure doloribus accusamus animi quos.
          </p>
        </div>
      </div>
      <div class="rounded-lg bg-info px-4 py-4 text-white sm:px-5">
        <div>
          <h2 class="text-lg font-medium tracking-wide line-clamp-1">
            Info Card
          </h2>
        </div>
        <div class="pt-2">
          <p>
            Lorem ipsum dolor sit, amet consectetur adipisicing elit. Aut
            laboriosam praesentium adipisci iure doloribus accusamus animi quos.
          </p>
        </div>
      </div>
      <div class="rounded-lg bg-success px-4 py-4 text-white sm:px-5">
        <div>
          <h2 class="text-lg font-medium tracking-wide line-clamp-1">
            Success Card
          </h2>
        </div>
        <div class="pt-2">
          <p>
            Lorem ipsum dolor sit, amet consectetur adipisicing elit. Aut
            laboriosam praesentium adipisci iure doloribus accusamus animi quos.
          </p>
        </div>
      </div>
      <div class="rounded-lg bg-warning px-4 py-4 text-white sm:px-5">
        <div>
          <h2 class="text-lg font-medium tracking-wide line-clamp-1">
            Warning Card
          </h2>
        </div>
        <div class="pt-2">
          <p>
            Lorem ipsum dolor sit, amet consectetur adipisicing elit. Aut
            laboriosam praesentium adipisci iure doloribus accusamus animi quos.
          </p>
        </div>
      </div>
      <div class="rounded-lg bg-error px-4 py-4 text-white sm:px-5">
        <div>
          <h2 class="text-lg font-medium tracking-wide line-clamp-1">
            Error Card
          </h2>
        </div>
        <div class="pt-2">
          <p>
            Lorem ipsum dolor sit, amet consectetur adipisicing elit. Aut
            laboriosam praesentium adipisci iure doloribus accusamus animi quos.
          </p>
        </div>
      </div>
      <div
        class="rounded-lg bg-primary px-4 py-4 text-white shadow-lg shadow-primary/50 dark:bg-accent dark:shadow-accent/50 sm:px-5"
      >
        <div>
          <h2 class="text-lg font-medium tracking-wide line-clamp-1">
            Glow Card
          </h2>
        </div>
        <div class="pt-2">
          <p>
            Lorem ipsum dolor sit, amet consectetur adipisicing elit. Aut
            laboriosam praesentium adipisci iure doloribus accusamus animi quos.
          </p>
        </div>
      </div>
      <div
        class="rounded-lg bg-warning px-4 py-4 text-white shadow-lg shadow-warning/50 sm:px-5"
      >
        <div>
          <h2 class="text-lg font-medium tracking-wide line-clamp-1">
            Glow Card
          </h2>
        </div>
        <div class="pt-2">
          <p>
            Lorem ipsum dolor sit, amet consectetur adipisicing elit. Aut
            laboriosam praesentium adipisci iure doloribus accusamus animi quos.
          </p>
        </div>
      </div>
      <div
        class="rounded-lg bg-info px-4 py-4 text-white shadow-lg shadow-info/50 sm:px-5"
      >
        <div>
          <h2 class="text-lg font-medium tracking-wide line-clamp-1">
            Glow Card
          </h2>
        </div>
        <div class="pt-2">
          <p>
            Lorem ipsum dolor sit, amet consectetur adipisicing elit. Aut
            laboriosam praesentium adipisci iure doloribus accusamus animi quos.
          </p>
        </div>
      </div>
      <div
        class="rounded-lg bg-gradient-to-br from-purple-500 to-indigo-600 px-4 py-4 text-white sm:px-5"
      >
        <div>
          <h2 class="text-lg font-medium tracking-wide line-clamp-1">
            Gradient Card
          </h2>
        </div>
        <div class="pt-2">
          <p>
            Lorem ipsum dolor sit, amet consectetur adipisicing elit. Aut
            laboriosam praesentium adipisci iure doloribus accusamus animi quos.
          </p>
        </div>
      </div>
      <div
        class="rounded-lg bg-gradient-to-r from-fuchsia-600 to-pink-600 px-4 py-4 text-white sm:px-5"
      >
        <div>
          <h2 class="text-lg font-medium tracking-wide line-clamp-1">
            Gradient Card
          </h2>
        </div>
        <div class="pt-2">
          <p>
            Lorem ipsum dolor sit, amet consectetur adipisicing elit. Aut
            laboriosam praesentium adipisci iure doloribus accusamus animi quos.
          </p>
        </div>
      </div>
      <div
        class="rounded-lg bg-gradient-to-br from-amber-400 to-orange-600 px-4 py-4 text-white sm:px-5"
      >
        <div>
          <h2 class="text-lg font-medium tracking-wide line-clamp-1">
            Gradient Card
          </h2>
        </div>
        <div class="pt-2">
          <p>
            Lorem ipsum dolor sit, amet consectetur adipisicing elit. Aut
            laboriosam praesentium adipisci iure doloribus accusamus animi quos.
          </p>
        </div>
      </div>
      <div class="rounded-lg bg-gradient-to-r from-sky-400 to-blue-600 p-1">
        <div class="rounded-lg bg-slate-50 px-4 py-4 dark:bg-navy-900 sm:px-5">
          <div>
            <h2
              class="text-lg font-medium tracking-wide text-slate-600 line-clamp-1 dark:text-navy-100"
            >
              Outlined Gradient
            </h2>
          </div>
          <div class="pt-2">
            <p>
              Lorem ipsum dolor sit, amet consectetur adipisicing elit. Aut
              laboriosam praesentium adipisci iure doloribus accusamus animi
              quos.
            </p>
          </div>
        </div>
      </div>
      <div
        class="rounded-lg bg-gradient-to-r from-green-400 to-fuchsia-400 p-1"
      >
        <div class="rounded-lg bg-slate-50 px-4 py-4 dark:bg-navy-900 sm:px-5">
          <div>
            <h2
              class="text-lg font-medium tracking-wide text-slate-700 line-clamp-1 dark:text-navy-100"
            >
              Outlined Gradient
            </h2>
          </div>
          <div class="pt-2">
            <p>
              Lorem ipsum dolor sit, amet consectetur adipisicing elit. Aut
              laboriosam praesentium adipisci iure doloribus accusamus animi
              quos.
            </p>
          </div>
        </div>
      </div>
      <div class="rounded-lg bg-gradient-to-r from-amber-400 to-orange-600 p-1">
        <div class="rounded-lg bg-slate-50 px-4 py-4 dark:bg-navy-900 sm:px-5">
          <div>
            <h2
              class="text-lg font-medium tracking-wide text-slate-700 line-clamp-1 dark:text-navy-100"
            >
              Outlined Gradient
            </h2>
          </div>
          <div class="pt-2">
            <p>
              Lorem ipsum dolor sit, amet consectetur adipisicing elit. Aut
              laboriosam praesentium adipisci iure doloribus accusamus animi
              quos.
            </p>
          </div>
        </div>
      </div>
    </div>
    <div class="mt-5 space-y-4">
      <div class="progress h-2 bg-slate-150 dark:bg-navy-500">
        <div
          class="is-active relative w-4/12 overflow-hidden rounded-full bg-slate-500 dark:bg-navy-400"
        />
      </div>
      <div class="progress h-2 bg-slate-150 dark:bg-navy-500">
        <div
          class="is-active relative w-5/12 overflow-hidden rounded-full bg-primary dark:bg-accent"
        />
      </div>
      <div class="progress h-2 bg-slate-150 dark:bg-navy-500">
        <div
          class="is-active relative w-6/12 overflow-hidden rounded-full bg-secondary"
        />
      </div>
      <div class="progress h-2 bg-slate-150 dark:bg-navy-500">
        <div
          class="is-active relative w-7/12 overflow-hidden rounded-full bg-info"
        />
      </div>
      <div class="progress h-2 bg-slate-150 dark:bg-navy-500">
        <div
          class="is-active relative w-8/12 overflow-hidden rounded-full bg-success"
        />
      </div>
      <div class="progress h-2 bg-slate-150 dark:bg-navy-500">
        <div
          class="is-active relative w-9/12 overflow-hidden rounded-full bg-warning"
        />
      </div>
      <div class="progress h-2 bg-slate-150 dark:bg-navy-500">
        <div
          class="is-active relative w-10/12 overflow-hidden rounded-full bg-error"
        />
      </div>
    </div>

    <div class="mt-5 max-w-md">
      <div class="flex flex-col border border-slate-150 dark:border-navy-500">
        <div class="flex space-x-5 px-5 py-4">
          <div
            class="skeleton animate-wave h-16 w-16 rounded-full bg-slate-150 dark:bg-navy-500"
          />
          <div class="flex flex-1 flex-col justify-between py-2">
            <div
              class="skeleton animate-wave h-3 w-full rounded bg-slate-150 dark:bg-navy-500"
            />
            <div
              class="skeleton animate-wave h-3 w-full rounded bg-slate-150 dark:bg-navy-500"
            />
          </div>
        </div>
        <div
          class="skeleton animate-wave h-48 w-full bg-slate-150 dark:bg-navy-500"
        />
        <div class="w-full px-6 py-4">
          <div
            class="skeleton animate-wave h-3 w-full rounded bg-slate-150 dark:bg-navy-500"
          />
          <div
            class="skeleton animate-wave mt-4 h-3 w-8/12 rounded bg-slate-150 dark:bg-navy-500"
          />
        </div>
      </div>
    </div>

    <div class="inline-space mt-5 flex flex-wrap">
      <div
        class="spinner h-7 w-7 animate-spin rounded-full border-[3px] border-slate-500 border-r-transparent dark:border-navy-300 dark:border-r-transparent"
      />
      <div
        class="spinner h-7 w-7 animate-spin rounded-full border-[3px] border-primary border-r-transparent dark:border-accent dark:border-r-transparent"
      />
      <div
        class="spinner h-7 w-7 animate-spin rounded-full border-[3px] border-secondary border-r-transparent"
      />
      <div
        class="spinner h-7 w-7 animate-spin rounded-full border-[3px] border-info border-r-transparent"
      />
      <div
        class="spinner h-7 w-7 animate-spin rounded-full border-[3px] border-success border-r-transparent"
      />
      <div
        class="spinner h-7 w-7 animate-spin rounded-full border-[3px] border-warning border-r-transparent"
      />
      <div
        class="spinner h-7 w-7 animate-spin rounded-full border-[3px] border-error border-r-transparent"
      />
    </div>
    <div class="mt-5">
      <div class="is-scrollbar-hidden min-w-full overflow-x-auto">
        <table class="w-full text-left">
          <thead>
            <tr
              class="border-y border-transparent border-b-slate-200 dark:border-b-navy-500"
            >
              <th
                class="whitespace-nowrap px-3 py-3 font-semibold uppercase text-slate-800 dark:text-navy-100 lg:px-5"
              >
                #
              </th>
              <th
                class="whitespace-nowrap px-3 py-3 font-semibold uppercase text-slate-800 dark:text-navy-100 lg:px-5"
              >
                Name
              </th>
              <th
                class="whitespace-nowrap px-3 py-3 font-semibold uppercase text-slate-800 dark:text-navy-100 lg:px-5"
              >
                Job
              </th>
              <th
                class="whitespace-nowrap px-3 py-3 font-semibold uppercase text-slate-800 dark:text-navy-100 lg:px-5"
              >
                Favorite Color
              </th>
            </tr>
          </thead>
          <tbody>
            <tr
              class="border-y border-transparent border-b-slate-200 dark:border-b-navy-500"
            >
              <td class="whitespace-nowrap px-4 py-3 sm:px-5">1</td>
              <td class="whitespace-nowrap px-4 py-3 sm:px-5">
                Cy Ganderton
              </td>
              <td class="whitespace-nowrap px-4 py-3 sm:px-5">
                Quality Control Specialist
              </td>
              <td class="whitespace-nowrap px-4 py-3 sm:px-5"> Blue </td>
            </tr>
            <tr
              class="border-y border-transparent border-b-slate-200 dark:border-b-navy-500"
            >
              <td class="whitespace-nowrap px-4 py-3 sm:px-5">2</td>
              <td class="whitespace-nowrap px-4 py-3 sm:px-5">
                Hart Hagerty
              </td>
              <td class="whitespace-nowrap px-4 py-3 sm:px-5">
                Desktop Support Technician
              </td>
              <td class="whitespace-nowrap px-4 py-3 sm:px-5"> Purple </td>
            </tr>
            <tr
              class="border-y border-transparent border-b-slate-200 dark:border-b-navy-500"
            >
              <td class="whitespace-nowrap px-4 py-3 sm:px-5">3</td>
              <td class="whitespace-nowrap px-4 py-3 sm:px-5"> Brice Swyre </td>
              <td class="whitespace-nowrap px-4 py-3 sm:px-5">
                Tax Accountant
              </td>
              <td class="whitespace-nowrap px-4 py-3 sm:px-5">Red</td>
            </tr>
            <tr
              class="border-y border-transparent border-b-slate-200 dark:border-b-navy-500"
            >
              <td class="whitespace-nowrap px-4 py-3 sm:px-5">4</td>
              <td class="whitespace-nowrap px-4 py-3 sm:px-5">
                Marjy Ferencz
              </td>
              <td class="whitespace-nowrap px-4 py-3 sm:px-5">
                Office Assistant I
              </td>
              <td class="whitespace-nowrap px-4 py-3 sm:px-5"> Crimson </td>
            </tr>
          </tbody>
        </table>
      </div>
    </div>
    <div class="mt-5">
      <ol class="timeline max-w-sm">
        <li class="timeline-item">
          <div
            class="timeline-item-point rounded-full bg-slate-300 dark:bg-navy-400"
          />
          <div class="timeline-item-content flex-1 pl-4 sm:pl-8">
            <div class="flex flex-col justify-between pb-2 sm:flex-row sm:pb-0">
              <p
                class="pb-2 font-medium leading-none text-slate-600 dark:text-navy-100 sm:pb-0"
              >
                User Photo Changed
              </p>
              <span class="text-xs text-slate-400 dark:text-navy-300"
                >12 minute ago</span
              >
            </div>
            <p class="py-1">John Doe changed his avatar photo</p>
          </div>
        </li>
        <li class="timeline-item">
          <div
            class="timeline-item-point rounded-full bg-primary dark:bg-accent"
          />
          <div class="timeline-item-content flex-1 pl-4 sm:pl-8">
            <div class="flex flex-col justify-between pb-2 sm:flex-row sm:pb-0">
              <p
                class="pb-2 font-medium leading-none text-slate-600 dark:text-navy-100 sm:pb-0"
              >
                Video Added
              </p>
              <span class="text-xs text-slate-400 dark:text-navy-300"
                >1 hour ago</span
              >
            </div>
            <p class="py-1">Mores Clarke added new video</p>
          </div>
        </li>
        <li class="timeline-item">
          <div class="timeline-item-point rounded-full bg-success" />
          <div class="timeline-item-content flex-1 pl-4 sm:pl-8">
            <div class="flex flex-col justify-between pb-2 sm:flex-row sm:pb-0">
              <p
                class="pb-2 font-medium leading-none text-slate-600 dark:text-navy-100 sm:pb-0"
              >
                Design Completed
              </p>
              <span class="text-xs text-slate-400 dark:text-navy-300"
                >3 hours ago</span
              >
            </div>
            <p class="py-1">
              Robert Nolan completed the design of the CRM application
            </p>
          </div>
        </li>
        <li class="timeline-item">
          <div class="timeline-item-point rounded-full bg-warning" />
          <div class="timeline-item-content flex-1 pl-4 sm:pl-8">
            <div class="flex flex-col justify-between pb-2 sm:flex-row sm:pb-0">
              <p
                class="pb-2 font-medium leading-none text-slate-600 dark:text-navy-100 sm:pb-0"
              >
                ER Diagram
              </p>
              <span class="text-xs text-slate-400 dark:text-navy-300"
                >a day ago</span
              >
            </div>
            <p class="py-1">Team completed the ER diagram app</p>
          </div>
        </li>
        <li class="timeline-item">
          <div class="timeline-item-point rounded-full bg-error" />
          <div class="timeline-item-content flex-1 pl-4 sm:pl-8">
            <div class="flex flex-col justify-between pb-2 sm:flex-row sm:pb-0">
              <p
                class="pb-2 font-medium leading-none text-slate-600 dark:text-navy-100 sm:pb-0"
              >
                Weekly Report
              </p>
              <span class="text-xs text-slate-400 dark:text-navy-300"
                >a day ago</span
              >
            </div>
            <p class="py-1">The weekly report was uploaded</p>
          </div>
        </li>
      </ol>
    </div>
  </main>
</div>
