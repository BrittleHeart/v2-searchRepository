<template>
  <article class="w-full bg-gray-600 rounded-t-2xl p-3">
    <form action="" method="post" @submit.prevent="getGithubRepositories()">
      <div class="flex justify-between items-center">
        <input
          type="text"
          name="search"
          id="search-input"
          class="w-full rounded text-gray border-b input border border-transparent focus:outline-none focus:ring-2 focus:ring-purple-600 focus:border-transparent p-2"
          placeholder="search for github repositories .."
          autofocus="autofocus"
          v-model="search"
          required="required"
        />

        <button
          class="bg-purple-600 hover:bg-purple-700 focus:outline-none focus:ring-3 focus:ring-purple-600 focus:ring-opacity-50 text-white text-lg p-2 rounded ml-2"
          type="submit"
        >
          search
        </button>
      </div>
    </form>
    {{ search }}
  </article>
  <search-results-toolbar :results="results" />
</template>

<script>
import { ref } from "vue";
import searchResultsToolbar from "./searchResultsToolbar";

export default {
  components: {
    searchResultsToolbar,
  },
  setup() {
    const search = ref("");
    let results = ref([]);

    async function getGithubRepositories() {
      const response = await fetch(
        `https://api.github.com/search/repositories?q=${search}`,
        {
          method: "GET",
          headers: { Accept: "application/vnd.github.v3+json" },
        }
      );

      const repositories = await response.json();
      results.value = repositories
      console.log(results.value.items);
    }

    return {
      search,
      results,
      getGithubRepositories,
    };
  },
};
</script>

<style></style>
