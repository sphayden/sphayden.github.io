<script lang="ts">
    import {Row, Col, Grid, Item} from 'svelte-layouts';
  </script>
  
  <Grid class="root" templateCols="1fr 1fr 1fr" colGap="8px" width="100vw" height="50vw" padding="8px">
      <Grid colStart="1" colEnd="4" templateCols="1fr 1fr" templateRows="1fr 1fr 1fr" colGap="8px" rowGap="8px">
          <Row gap="8px" height="32vh" width="100vw">
        <img class="bg_pic" src="/src/assets/sw_art/2019_1.jpg" alt="alt bg pic"/>
        <img class="bg_pic" src="/src/assets/sw_art/2019_2.jpg" alt="alt bg pic"/>
        <img class="bg_pic" src="/src/assets/sw_art/2019_3.jpg" alt="alt bg pic"/>
        <img class="bg_pic" src="/src/assets/sw_art/2019_4.jpg" alt="alt bg pic"/>
          </Row>
      <Row colStart="1" gap="8px" height="32vh">
              <img class="bg_pic" src="/src/assets/sw_art/2019_5.jpg" alt="alt bg pic"/>
        <img class="bg_pic" src="/src/assets/sw_art/2019_6.jpg" alt="alt bg pic"/>
        <img class="bg_pic" src="/src/assets/sw_art/2021_6.jpg" alt="alt bg pic"/>
        <img class="bg_pic" src="/src/assets/sw_art/2023_1.jpg" alt="alt bg pic"/>
          </Row>
      <Row colStart="1" gap="8px" height="32vh">
              <img class="bg_pic" src="/src/assets/sw_art/2023_1.jpg" alt="alt bg pic"/>
        <img class="bg_pic" src="/src/assets/sw_art/2023_1.jpg" alt="alt bg pic"/>
        <img class="bg_pic" src="/src/assets/sw_art/2023_1.jpg" alt="alt bg pic"/>
        <img class="bg_pic" src="/src/assets/sw_art/2023_1.jpg" alt="alt bg pic"/>
          </Row>
      </Grid>
  </Grid>

  <style>
    :global(.root){
          border: px solid rgb(0 0 0 / .4);
      overflow: hidden;
      }
      :global(.col>.item){
          background-color: #75e0c4
      }
      :global(.row>.item){
          background-color: #e0c375
      }
      :global(.grid>.grid-item){
          background-color: #718eda
      }
    .bg_pic {
      object-fit: scale-down;
      overflow: hidden;
    }
  </style>