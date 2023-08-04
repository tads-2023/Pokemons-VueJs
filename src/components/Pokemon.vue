<script setup>
	defineProps({
		pokemon: {
			type: Object,
			required: true
		}
	})
</script>

<template>
  <div>
    <div>
      <span class="titulo">Nome</span>
      <span class="conteudo">{{ pokemon.name }}</span>
    </div>
    <div>
      <span class="titulo">Xp base</span>
      <span class="conteudo">{{ pokemon.xpBase }}</span>
    </div>
    <div>
      <span class="titulo">Peso</span>
      <span class="conteudo">{{ pokemon.peso }}</span>
    </div>
    <div>
      <h3>Movimentos</h3>
      <div>
        <p v-for="movimento in pokemon.movimentos" :key=movimento>
					{{ movimento }}
				</p>
      </div>
    </div>
  </div>
</template>