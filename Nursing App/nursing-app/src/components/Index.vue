<template>
  <div class="index container">
    <div class="card" v-for="item in checklistItem" :key="item.id">
      <div class="card-content">
        <h2 class="indigo-text">{{item.title}}</h2>
        <ul class="levels">
          <li v-for="(level, index) in item.levels" :key="index">
            <span class="chip">{{level}}</span>
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Index',
  data () {
    return {
      checklistItem: [
        {title: 'General', slug: 'general-item', levels: ['level1', 'level2', 'level3', 'level4'], id: '1' },
        {title: 'Neurological', slug: 'general-item', levels: ['level1', 'level2', 'level3', 'level4'], id: '2' },
        {title: 'Cardial', slug: 'general-item', levels: ['level1', 'level2', 'level3', 'level4'], id: '3' },
        {title: 'Pulmonary', slug: 'general-item', levels: ['level1', 'level2', 'level3', 'level4'], id: '4' },
        {title: 'Gastrointestinal', slug: 'general-item', levels: ['level1', 'level2', 'level3', 'level4'], id: '5' },
        {title: 'Genitorinary', slug: 'general-item', levels: ['level1', 'level2', 'level3', 'level4'], id: '6' },
        {title: 'Musculoskeletal', slug: 'general-item', levels: ['level1', 'level2', 'level3', 'level4'], id: '7' },
        {title: 'Skin', slug: 'general-item', levels: ['level1', 'level2', 'level3', 'level4'], id: '8' },
        {title: 'Psychosocial', slug: 'general-item', levels: ['level1', 'level2', 'level3', 'level4'], id: '9' },
        {title: 'Medication Administration', slug: 'general-item', levels: ['level1', 'level2', 'level3', 'level4'], id: '10' },
        {title: 'Intravenious Therapy', slug: 'general-item', levels: ['level1', 'level2', 'level3', 'level4'], id: '11' },
        {title: 'Laboratory', slug: 'general-item', levels: ['level1', 'level2', 'level3', 'level4'], id: '12' },
        {title: 'Professional Role', slug: 'general-item', levels: ['level1', 'level2', 'level3', 'level4'], id: '13' },
        {title: 'Critical Care', slug: 'general-item', levels: ['level1', 'level2', 'level3', 'level4'], id: '14' },
        {title: 'Place X', slug: 'general-item', levels: ['level1', 'level2', 'level3', 'level4'], id: '15' } 
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
.index {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  grid-gap: 30px;
  margin-top: 60px;
}

.index h2 {
  font-size: 1.8em;
  text-align: center;
  margin-top: 1.8px;
}

.index .levels {
  margin: 30px auto;
}

.index .levels li {
  display: inline-block;
}
</style>
