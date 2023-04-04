<template>

    <nav class="bg-gradient-to-r from-teal-950 to-cyan-700 border-b-2 border-gray-800 dark:bg-gray-900">
    <div class="max-w-screen-xl flex flex-wrap items-center justify-between mx-auto p-4">
        <a href="#/home" class="flex items-center ml-3">
            <img class="h-6 mr-3" src="../assets/eye.png"/>
            <img class="block h-6 w-auto ml-1" src="../assets/noatech_text.png" />
        </a>
        <button data-collapse-toggle="navbar-default" type="button" class="inline-flex items-center p-2 ml-3 text-sm text-white rounded-lg md:hidden hover:bg-slate-900 focus:outline-none focus:ring-2 focus:ring-gray-200 dark:text-white dark:hover:bg-gray-700 dark:focus:ring-gray-600" aria-controls="navbar-default" aria-expanded="false">
        <span class="sr-only">Open main menu</span>
        <svg class="w-6 h-6" aria-hidden="true" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><path fill-rule="evenodd" d="M3 5a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zM3 10a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zM3 15a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1z" clip-rule="evenodd"></path></svg>
        </button>
        <div class="hidden w-full md:block md:w-auto" id="navbar-default">
        <ul class="font-medium flex flex-col p-4 md:p-0 mt-4 border border-gray-100 rounded-lg bg-inherit md:flex-row md:space-x-8 md:mt-0 md:border-0 md:bg-inherit dark:bg-gray-800 md:dark:bg-gray-900 dark:border-gray-700">
            <li>
            <a href="#/home" class="block py-2 pl-3 pr-4 text-white rounded hover:bg-slate-900 md:bg-transparent md:text-white md:p-0 dark:text-white md:dark:text-white" aria-current="page">Home</a>
            </li>
            <li>
            <a href="#/about" class="block py-2 pl-3 pr-4 text-white rounded hover:bg-slate-900 md:hover:bg-transparent md:border-0 md:hover:text-white md:p-0 dark:text-white md:dark:hover:text-white dark:hover:bg-gray-700 dark:hover:text-white md:dark:hover:bg-transparent">About</a>
            </li>
            <li>
            <a href="#/services" class="block py-2 pl-3 pr-4 text-white rounded hover:bg-slate-900 md:hover:bg-transparent md:border-0 md:hover:text-white md:p-0 dark:text-white md:dark:hover:text-white dark:hover:bg-gray-700 dark:hover:text-white md:dark:hover:bg-transparent">Services</a>
            </li>
            <li>
            <a href="#/contact" class="block py-2 pl-3 pr-4 text-white rounded hover:bg-slate-900 md:hover:bg-transparent md:border-0 md:hover:text-white md:p-0 dark:text-white md:dark:hover:text-white dark:hover:bg-gray-700 dark:hover:text-white md:dark:hover:bg-transparent">Contact</a>
            </li>
        </ul>
        </div>
    </div>
    </nav>

</template> 
