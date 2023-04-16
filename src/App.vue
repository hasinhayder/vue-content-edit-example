<script setup>
import {ref} from 'vue'
import FigurePro from './components/FigurePro.vue';

const editMode = ref(false)
</script>

<template>
  <main class="container mx-auto py-10">
    <article class="max-w-2xl mx-auto">
      <header class="mb-4 lg:mb-6 not-format">
        <address class="flex items-center mb-6 not-italic">
          <div class="inline-flex items-center mr-3 text-sm text-gray-900 dark:text-white">
            <img class="mr-4 w-16 h-16 rounded-full" src="https://flowbite.com/docs/images/people/profile-picture-1.jpg" alt="Jese Leos">
            <div>
              <a href="#" rel="author" class="text-xl font-bold text-gray-900 dark:text-white">John Doe</a>
              <p class="text-base font-light text-gray-500 dark:text-gray-400">An amazing author from the parallel universe</p>
              <p class="text-base font-light text-gray-500 dark:text-gray-400"><time>April 16, 2023</time></p>
            </div>
          </div>
        </address>
        <h1 :contenteditable="editMode" class="mb-4 text-3xl font-extrabold leading-tight text-gray-900 lg:mb-6 lg:text-4xl dark:text-white">Vue.js Content Edit With Image Picker</h1>
        <button @click="editMode=!editMode" class="bg-white hover:bg-gray-100 text-gray-800 font-semibold py-2 px-4 border border-gray-400 rounded shadow">
          <span v-if="!editMode">Turn On Edit Mode</span>
          <span v-if="editMode">Turn Off Edit Mode</span>
        </button>
      </header>
      <div class="flex flex-col space-y-5">
        <p :contenteditable="editMode">Lorem ipsum dolor sit amet consectetur adipisicing elit. Maxime, praesentium accusantium nulla soluta modi provident velit. At unde voluptas officia magni, commodi nesciunt explicabo id?</p>
        <p :contenteditable="editMode">Quis omnis, corrupti ut dolore error officiis, mollitia quod voluptatem quo tempora ipsam vero dolorem id sequi accusamus ducimus aspernatur eligendi enim accusantium deserunt delectus!</p>
        <p :contenteditable="editMode">Quas, esse culpa cum voluptatibus modi illum repellendus quidem tempore quaerat dolorum nisi, nostrum, autem voluptatum laudantium consequuntur aut obcaecati dolore dicta sapiente hic ea?</p>
        <FigurePro :edit="editMode" image="https://images.unsplash.com/photo-1605772575717-4548a90a5349?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=928&q=80" title="A Fantastic Image"/>
        <p :contenteditable="editMode">Lorem ipsum, dolor sit amet consectetur adipisicing elit. Autem voluptas repudiandae vel dolorem quam dicta in blanditiis, nisi explicabo labore?</p>
        <p :contenteditable="editMode">Autem iure non sequi hic aspernatur quas sed, praesentium voluptatum deserunt totam aliquid dolorem quaerat voluptates animi, quis architecto laborum!</p>
        <FigurePro :edit="editMode" image="https://images.unsplash.com/photo-1565849904461-04a58ad377e0?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=872&q=80" title="Another Fantastic Image"/>
        <p :contenteditable="editMode">Lorem ipsum, dolor sit amet consectetur adipisicing elit. Autem voluptas repudiandae vel dolorem quam dicta in blanditiis, nisi explicabo labore?</p>
        <p :contenteditable="editMode">Autem iure non sequi hic aspernatur quas sed, praesentium voluptatum deserunt totam aliquid dolorem quaerat voluptates animi, quis architecto laborum!</p>
      </div>
    </article>
  </main>
  <footer class="h-96 bg-gray-100">
    <aside aria-label="Related articles" class="py-8 lg:py-24 bg-gray-50 dark:bg-gray-800">
      <div class="px-4 mx-auto max-w-screen-xl">
        <h2 class="mb-8 text-2xl font-bold text-gray-900 dark:text-white">Related articles</h2>
        <div class="grid gap-12 sm:grid-cols-2 lg:grid-cols-4">
          <article class="max-w-xs">
            <a href="#">
              <img src="https://plus.unsplash.com/premium_photo-1663047815120-c58b695210ab?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxzZWFyY2h8MXx8bW9iaWxlJTIwcGhvdG9ncmFwaHl8ZW58MHx8MHx8&auto=format&fit=crop&w=500&q=60" class="mb-5 rounded-lg" alt="Image 1">
            </a>
            <h2 class="mb-2 text-xl font-bold leading-tight text-gray-900 dark:text-white">
              <a href="#">Our first office</a>
            </h2>
            <p class="mb-4 font-light text-gray-500 dark:text-gray-400">Lorem ipsum dolor sit amet consectetur adipisicing elit. Porro in alias blanditiis. Aut sed minus at quis ipsum aliquid laborum.</p>
            <a href="#" class="inline-flex items-center font-medium underline underline-offset-4 text-primary-600 dark:text-primary-500 hover:no-underline">
              Read in 2 minutes
            </a>
          </article>
          <article class="max-w-xs">
            <a href="#">
              <img src="https://images.unsplash.com/photo-1547566791-7962d6687f0d?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxzZWFyY2h8NDJ8fG1vYmlsZSUyMHBob3RvZ3JhcGh5fGVufDB8fDB8fA%3D%3D&auto=format&fit=crop&w=500&q=60" class="mb-5 rounded-lg" alt="Image 2">
            </a>
            <h2 class="mb-2 text-xl font-bold leading-tight text-gray-900 dark:text-white">
              <a href="#">Enterprise design tips</a>
            </h2>
            <p class="mb-4 font-light text-gray-500 dark:text-gray-400">Lorem ipsum dolor sit amet consectetur adipisicing elit. Nobis veritatis ea minus? Soluta aspernatur iste aliquam sunt numquam nam laborum.</p>
            <a href="#" class="inline-flex items-center font-medium underline underline-offset-4 text-primary-600 dark:text-primary-500 hover:no-underline">
              Read in 12 minutes
            </a>
          </article>
          <article class="max-w-xs">
            <a href="#">
              <img src="https://images.unsplash.com/photo-1554495498-b2d057960af4?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxzZWFyY2h8MzV8fG1vYmlsZSUyMHBob3RvZ3JhcGh5fGVufDB8fDB8fA%3D%3D&auto=format&fit=crop&w=500&q=60" class="mb-5 rounded-lg" alt="Image 3">
            </a>
            <h2 class="mb-2 text-xl font-bold leading-tight text-gray-900 dark:text-white">
              <a href="#">We partnered with Google</a>
            </h2>
            <p class="mb-4 font-light text-gray-500 dark:text-gray-400">Lorem ipsum, dolor sit amet consectetur adipisicing elit. Doloremque amet ipsa ut magnam nisi quasi consectetur earum odit soluta cupiditate!</p>
            <a href="#" class="inline-flex items-center font-medium underline underline-offset-4 text-primary-600 dark:text-primary-500 hover:no-underline">
              Read in 8 minutes
            </a>
          </article>
          <article class="max-w-xs">
            <a href="#">
              <img src="https://plus.unsplash.com/premium_photo-1663013698580-9101d6f1ad39?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxzZWFyY2h8Mzd8fG1vYmlsZSUyMHBob3RvZ3JhcGh5fGVufDB8fDB8fA%3D%3D&auto=format&fit=crop&w=500&q=60" class="mb-5 rounded-lg" alt="Image 4">
            </a>
            <h2 class="mb-2 text-xl font-bold leading-tight text-gray-900 dark:text-white">
              <a href="#">Our first project with React</a>
            </h2>
            <p class="mb-4 font-light text-gray-500 dark:text-gray-400">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Asperiores, natus repellat temporibus praesentium vero omnis alias ratione cumque aliquam molestias.</p>
            <a href="#" class="inline-flex items-center font-medium underline underline-offset-4 text-primary-600 dark:text-primary-500 hover:no-underline">
              Read in 4 minutes
            </a>
          </article>
        </div>
      </div>
    </aside>
  </footer>
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}

.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}

.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
