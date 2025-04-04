<script setup></script>

<template>
  <main class="max-w-6xl mx-auto px-4 py-10 grid md:grid-cols-2 gap-10">
    <div>
      <img
        src="https://via.placeholder.com/600x400"
        class="w-full rounded-xl object-cover"
        alt="Produit"
      />
    </div>
    <div>
      <h2 class="text-3xl font-bold mb-4">Chaussure Cuir Classique</h2>
      <p class="text-gray-600 mb-4">Idéale pour le bureau ou les grandes occasions.</p>
      <p class="text-2xl font-bold mb-4">89,99 €</p>

      <div class="mb-4">
        <label class="block font-medium mb-1">Pointure</label>
        <select class="w-full border px-3 py-2 rounded">
          <option>39</option>
          <option>40</option>
          <option>41</option>
          <option>42</option>
        </select>
      </div>

      <button
        class="bg-blue-600 text-white px-6 py-3 rounded-xl hover:bg-blue-700 transition w-full"
      >
        Ajouter au panier
      </button>
    </div>
  </main>
</template>
