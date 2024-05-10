<div
  class="max-w-md mx-auto mt-20 relative overflow-hidden z-10 bg-white dark:bg-slate-800 p-8 rounded-lg shadow-md before:w-24 before:h-24 before:absolute before:bg-purple-500 before:rounded-full before:-z-10 before:blur-2xl after:w-32 after:h-32 after:absolute after:bg-sky-400 after:rounded-full after:-z-10 after:blur-xl after:top-24 after:-right-12 border-2 border-latte-blue dark:border-ctp-mauve"
>
  <h2 class="text-2xl text-sky-900 dark:text-slate-200 font-bold mb-6">Send a message to me!</h2>

  <form method="POST" action="https://formspree.io/f/xvoeznra">
    <div class="mb-4">
      <label class="block text-sm font-medium text-gray-600 dark:text-slate-200" for="name"
        >Full Name</label
      >
      <input class="mt-1 p-2 w-full border rounded-md" type="text" />
    </div>

    <div class="mb-4">
      <label class="block text-sm font-medium text-gray-600 dark:text-slate-200" for="email"
        >Email Address</label
      >
      <input
        class="mt-1 p-2 w-full border rounded-md"
        name="email"
        id="email"
        type="email"
      />
    </div>

    <div class="mb-4">
      <label class="block text-sm font-medium text-gray-600 dark:text-slate-200" for="bio"
        >Message</label
      >
      <textarea
        class="mt-1 p-2 w-full border rounded-md"
        rows="3"
        name="message"
        id="message"
      ></textarea>
    </div>

    <div class="flex justify-end">
      <button
        class="[background:linear-gradient(144deg,#af40ff,#5b42f3_50%,#00ddeb)] text-white px-4 py-2 font-bold rounded-md hover:opacity-80"
        type="submit"
      >
        Submit
      </button>
    </div>
  </form>
</div>
