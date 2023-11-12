<script lang="ts">
  import { onMount } from 'svelte';
  const imageModules = import.meta.glob("/src/assets/sw_art/*.jpg");
  let imageUrls = [];
  // onMount(() => {
  //   for (const modulePath in imageModules) {
  //     imageModules[modulePath]().then(({ default: imageUrl }) => {
  //       imageUrls.push(imageUrl);
  //       imageUrls = imageUrls;
  //     });
  //   }
  // });
  for (const modulePath in imageModules) {
      imageModules[modulePath]().then(({ default: imageUrl }) => {
        imageUrls.push(imageUrl);
        imageUrls = imageUrls;
      });
    }
  function submit_id() {
    console.log(hiveID)
  }
  let hiveID;
</script>

<div class="page-wrapper">
  
  <div class="background">
    <div class="row" id="permas">
      <img class="bg_pic" src="/src/assets/sw_art/2017_3.jpg" alt="alt bg pic" />
      <img class="bg_pic" src="/src/assets/sw_art/2018_1.jpg" alt="alt bg pic" />
      <img class="bg_pic" src="/src/assets/sw_art/2019_10.jpg" alt="alt bg pic" />
      <img class="bg_pic" src="/src/assets/sw_art/2020_1.jpg" alt="alt bg pic" />
      <img class="bg_pic" src="/src/assets/sw_art/2021_1.jpg" alt="alt bg pic" />
      {#each imageUrls as imgUrl}
        <img class="bg_pic" src={imgUrl} alt="alt bg pic" />
      {/each}
      <img class="bg_pic" src="/src/assets/sw_art/2017_3.jpg" alt="alt bg pic" />
      <img class="bg_pic" src="/src/assets/sw_art/2018_1.jpg" alt="alt bg pic" />
      <img class="bg_pic" src="/src/assets/sw_art/2019_10.jpg" alt="alt bg pic" />
      <img class="bg_pic" src="/src/assets/sw_art/2020_1.jpg" alt="alt bg pic" />
      <img class="bg_pic" src="/src/assets/sw_art/2021_1.jpg" alt="alt bg pic" />
    </div>
    <div class="row-reverse" id="permas-reverse">
      <img class="bg_pic" src="/src/assets/sw_art/2017_3.jpg" alt="alt bg pic" />
      <img class="bg_pic" src="/src/assets/sw_art/2018_1.jpg" alt="alt bg pic" />
      <img class="bg_pic" src="/src/assets/sw_art/2019_10.jpg" alt="alt bg pic" />
      <img class="bg_pic" src="/src/assets/sw_art/2020_1.jpg" alt="alt bg pic" />
      <img class="bg_pic" src="/src/assets/sw_art/2021_1.jpg" alt="alt bg pic" />
      {#each imageUrls as imgUrl}
        <img class="bg_pic" src={imgUrl} alt="alt bg pic" />
      {/each}
      <img class="bg_pic" src="/src/assets/sw_art/2017_3.jpg" alt="alt bg pic" />
      <img class="bg_pic" src="/src/assets/sw_art/2018_1.jpg" alt="alt bg pic" />
      <img class="bg_pic" src="/src/assets/sw_art/2019_10.jpg" alt="alt bg pic" />
      <img class="bg_pic" src="/src/assets/sw_art/2020_1.jpg" alt="alt bg pic" />
      <img class="bg_pic" src="/src/assets/sw_art/2021_1.jpg" alt="alt bg pic" />
    </div>
    <div class="row" id="permas">
      <img class="bg_pic" src="/src/assets/2022_5.jpg" alt="alt bg pic" />
      <img class="bg_pic" src="/src/assets/sw_art/2021_9.jpg" alt="alt bg pic" />
      <img class="bg_pic" src="/src/assets/2022_4.jpg" alt="alt bg pic" />
      <img class="bg_pic" src="/src/assets/2023_1.jpg" alt="alt bg pic" />
      <img class="bg_pic" src="/src/assets/2022_6.jpg" alt="alt bg pic" />
      <img class="bg_pic" src="/src/assets/2022_7.jpg" alt="alt bg pic" />
      <img class="bg_pic" src="/src/assets/2022_8.jpg" alt="alt bg pic" />
      {#each imageUrls as imgUrl}
        <img class="bg_pic" src={imgUrl} alt="alt bg pic" />
      {/each}
      <img class="bg_pic" src="/src/assets/2022_5.jpg" alt="alt bg pic" />
      <img class="bg_pic" src="/src/assets/sw_art/2021_9.jpg" alt="alt bg pic" />
      <img class="bg_pic" src="/src/assets/2022_4.jpg" alt="alt bg pic" />
      <img class="bg_pic" src="/src/assets/2023_1.jpg" alt="alt bg pic" />
      <img class="bg_pic" src="/src/assets/2022_6.jpg" alt="alt bg pic" />
      <img class="bg_pic" src="/src/assets/2022_7.jpg" alt="alt bg pic" />
      <img class="bg_pic" src="/src/assets/2022_8.jpg" alt="alt bg pic" />
    </div>
  </div>
  <div class="form_submit">
    <div class="form_css">
        <input type="text" class="form-control" aria-describedby="hive id help" placeholder="Enter Hive ID" bind:value={hiveID}>
        <button id="form_button" type="submit" class="btn btn-light" on:click={submit_id}>Submit</button>
    </div>
  </div>
</div>

<style>
  .bg_pic {
    object-fit: contain;
    overflow: hidden;
    max-height: 100%;
    padding-left: 3px;
    padding-right: 3px;
  }
  .background {
    flex: 1;
    display: flex;
    min-height: 100vh;
    min-width: 100vw;
    flex-direction: column;
    align-items: flex-start;
    filter: brightness(30%);
    background-color: black;
    overflow: hidden;
  }
  .page-wrapper {
    flex: 1;
    display: flex;
    min-height: 100vh;
    flex-direction: column;
    overflow:hidden;
  }
  .form_submit {
    position:absolute;
    display: flex;
    top:0;
    left:0;
    right:0;
    bottom:0;
    align-items: center;
    justify-content: center;
  }
  .form_css {
    display: flex;
    align-items: center;
    justify-content: center;
  }

  .form_css > * {
    margin: 5px;
  }

  .row {
    border: 3px solid rgb(0 0 0 / 0.4);
    flex: 1 0 auto;
    align-self: stretch;
    height: 31vh;
    align-items: flex-start;
    overflow: hidden;
    text-align: start;
  }

  .row-reverse {
    border: 3px solid rgb(0 0 0 / 0.4);
    flex: 1 0 auto;
    align-self: stretch;
    height: 31vh;
    align-items: flex-end;
    text-align: end;
    overflow: hidden;
  }

  #permas {
    animation-name: scroll;
    animation-duration: 300s;
    animation-iteration-count: infinite;
    animation-timing-function: linear;
  }
  #permas-reverse {
    animation-name: scroll;
    animation-duration: 300s;
    animation-iteration-count: infinite;
    animation-timing-function: linear;
    animation-direction: reverse;
  }
  @keyframes scroll {
    0% {
      transform: translateX(0);
    }
    100% {
      transform: translateX(-80%);
    }
  }
</style>
