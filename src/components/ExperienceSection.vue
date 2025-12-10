<script setup>
import SectionHeader from "./common/SectionHeader.vue";
</script>

<template>
  <div id="experience" class="section-anchor"></div>
  <div class="experience-container d-flex flex-column py-5">
    <SectionHeader
      title="What I experienced"
      description="Lorem ipsum dolor sit amet, consectetur adipiscing elit. Maecenas metus massa, imperdiet eu convallis eu, semper quis est. Pellentesque auctor pharetra lectus. Aenean cursus sem ante, eu elementum quam luctus ut. Nulla imperdiet semper justo sit amet rutrum. Vivamus."
    />
    <div
      class="experiencce-section-main container-fluid bg-primary flex-grow-1 p-0 d-flex flex-column"
    >

      <!-- work related scroll section -->
      <div
        class="card work-experience-card mt-4 d-flex flex-column border align-items-center p-4"
      >
        <h1 class="mb-4">Work</h1>
        <div class="list-and-scroll d-flex flex-row justify-content-between">
          <div id="work-list" class="list-group pe-2">
            <a
              class="list-group-item list-group-item-action"
              href="#list-item-1"
              >Item 1</a
            >
            <a
              class="list-group-item list-group-item-action"
              href="#list-item-2"
              >Item2</a
            >
            <a
              class="list-group-item list-group-item-action"
              href="#list-item-3"
              >Item 3</a
            >
            <a
              class="list-group-item list-group-item-action"
              href="#list-item-4"
              >Item 4</a
            >
          </div>

          <div
            id="work-scrollspy"
            class="scrollspy-example flex-grow-1 overflow-auto ps-2"
            data-bs-spy="scroll"
            data-bs-target="#work-list"
            data-bs-offset="80"
            tabindex="0"
          >
            <h4 id="list-item-1">Item 1</h4>
            <p>
              Lorem ipsum dolor sit amet, consectetur adipiscing elit. Maecenas
              metus massa, imperdiet eu convallis eu, semper quis est.
              Pellentesque auctor pharetra lectus. Aenean cursus sem ante, eu
              elementum quam luctus ut. Nulla imperdiet semper justo sit amet
              rutrum. Vivamus placerat orci eu ligula tincidunt, id facilisis
              justo pharetra. Donec ornare enim sed libero scelerisque pulvinar.
              Quisque elementum lacus eget felis ullamcorper rhoncus. Donec
              condimentum porttitor tristique. Pellentesque eleifend vitae nulla
              vel interdum. Integer dui.Lorem ipsum dolor sit amet, consectetur
              adipiscing elit. Maecenas metus massa, imperdiet eu convallis eu,
              semper quis est. Pellentesque auctor pharetra lectus. Aenean
              cursus sem ante, eu elementum quam luctus ut. Nulla imperdiet
              semper justo sit amet rutrum. Vivamus placerat orci eu ligula
              tincidunt, id facilisis justo pharetra. Donec ornare enim sed
              libero scelerisque pulvinar. Quisque elementum lacus eget felis
              ullamcorper rhoncus. Donec condimentum porttitor tristique.
              Pellentesque eleifend vitae nulla vel interdum. Integer dui.
            </p>
            <h4 id="list-item-2">Item 2</h4>
            <p>
              Lorem ipsum dolor sit amet, consectetur adipiscing elit. Maecenas
              metus massa, imperdiet eu convallis eu, semper quis est.
              Pellentesque auctor pharetra lectus. Aenean cursus sem ante, eu
              elementum quam luctus ut. Nulla imperdiet semper justo sit amet
              rutrum. Vivamus placerat orci eu ligula tincidunt, id facilisis
              justo pharetra. Donec ornare enim sed libero scelerisque pulvinar.
              Quisque elementum lacus eget felis ullamcorper rhoncus. Donec
              condimentum porttitor tristique. Pellentesque eleifend vitae nulla
              vel interdum. Integer dui.Lorem ipsum dolor sit amet, consectetur
              adipiscing elit. Maecenas metus massa, imperdiet eu convallis eu,
              semper quis est. Pellentesque auctor pharetra lectus. Aenean
              cursus sem ante, eu elementum quam luctus ut. Nulla imperdiet
              semper justo sit amet rutrum. Vivamus placerat orci eu ligula
              tincidunt, id facilisis justo pharetra. Donec ornare enim sed
              libero scelerisque pulvinar. Quisque elementum lacus eget felis
              ullamcorper rhoncus. Donec condimentum porttitor tristique.
              Pellentesque eleifend vitae nulla vel interdum. Integer dui.
            </p>
            <h4 id="list-item-3">Item 3</h4>
            <p>
              Lorem ipsum dolor sit amet, consectetur adipiscing elit. Maecenas
              metus massa, imperdiet eu convallis eu, semper quis est.
              Pellentesque auctor pharetra lectus. Aenean cursus sem ante, eu
              elementum quam luctus ut. Nulla imperdiet semper justo sit amet
              rutrum. Vivamus placerat orci eu ligula tincidunt, id facilisis
              justo pharetra. Donec ornare enim sed libero scelerisque pulvinar.
              Quisque elementum lacus eget felis ullamcorper rhoncus. Donec
              condimentum porttitor tristique. Pellentesque eleifend vitae nulla
              vel interdum. Integer dui.
            </p>
            <h4 id="list-item-4">Item 4</h4>
            <p>
              Lorem ipsum dolor sit amet, consectetur adipiscing elit. Maecenas
              metus massa, imperdiet eu convallis eu, semper quis est.
              Pellentesque auctor pharetra lectus. Aenean cursus sem ante, eu
              elementum quam luctus ut. Nulla imperdiet semper justo sit amet
              rutrum. Vivamus placerat orci eu ligula tincidunt, id facilisis
              justo pharetra. Donec ornare enim sed libero scelerisque pulvinar.
              Quisque elementum lacus eget felis ullamcorper rhoncus. Donec
              condimentum porttitor tristique. Pellentesque eleifend vitae nulla
              vel interdum. Integer dui.
            </p>
          </div>
        </div>
      </div>

      
      <!-- study related scroll section -->
      <div
        class="card study-experience-card mt-4 d-flex flex-column border align-items-center p-4"
      >
        <h1 class="mb-4">Study</h1>
        <div class="list-and-scroll d-flex flex-row justify-content-between">
          <div id="study-list" class="list-group pe-2">
            <a
              class="list-group-item study-list-group-item-action"
              href="#study-list-item-1"
              >Item 1</a
            >
            <a
              class="list-group-item study-list-group-item-action"
              href="#study-list-item-2"
              >Item2</a
            >
          </div>

          <div
            id="study-scrollspy"
            class="scrollspy-example flex-grow-1 overflow-auto ps-2"
            data-bs-spy="scroll"
            data-bs-target="#study-list"
            data-bs-offset="80"
            tabindex="0"
          >
            <h4 id="study-list-item-1">Item 1</h4>
            <p>
              Lorem ipsum dolor sit amet, consectetur adipiscing elit. Maecenas
              metus massa, imperdiet eu convallis eu, semper quis est.
              Pellentesque auctor pharetra lectus. Aenean cursus sem ante, eu
              elementum quam luctus ut. Nulla imperdiet semper justo sit amet
              rutrum. Vivamus placerat orci eu ligula tincidunt, id facilisis
              justo pharetra. Donec ornare enim sed libero scelerisque pulvinar.
              Quisque elementum lacus eget felis ullamcorper rhoncus. Donec
              condimentum porttitor tristique. Pellentesque eleifend vitae nulla
              vel interdum. Integer dui.Lorem ipsum dolor sit amet, consectetur
              adipiscing elit. Maecenas metus massa, imperdiet eu convallis eu,
              semper quis est. Pellentesque auctor pharetra lectus. Aenean
              cursus sem ante, eu elementum quam luctus ut. Nulla imperdiet
              semper justo sit amet rutrum. Vivamus placerat orci eu ligula
              tincidunt, id facilisis justo pharetra. Donec ornare enim sed
              libero scelerisque pulvinar. Quisque elementum lacus eget felis
              ullamcorper rhoncus. Donec condimentum porttitor tristique.
              Pellentesque eleifend vitae nulla vel interdum. Integer dui.
            </p>
            <h4 id="study-list-item-2">Item 2</h4>
            <p>
              Lorem ipsum dolor sit amet, consectetur adipiscing elit. Maecenas
              metus massa, imperdiet eu convallis eu, semper quis est.
              Pellentesque auctor pharetra lectus. Aenean cursus sem ante, eu
              elementum quam luctus ut. Nulla imperdiet semper justo sit amet
              rutrum. Vivamus placerat orci eu ligula tincidunt, id facilisis
              justo pharetra. Donec ornare enim sed libero scelerisque pulvinar.
              Quisque elementum lacus eget felis ullamcorper rhoncus. Donec
              condimentum porttitor tristique. Pellentesque eleifend vitae nulla
              vel interdum. Integer dui.Lorem ipsum dolor sit amet, consectetur
              adipiscing elit. Maecenas metus massa, imperdiet eu convallis eu,
              semper quis est. Pellentesque auctor pharetra lectus. Aenean
              cursus sem ante, eu elementum quam luctus ut. Nulla imperdiet
              semper justo sit amet rutrum. Vivamus placerat orci eu ligula
              tincidunt, id facilisis justo pharetra. Donec ornare enim sed
              libero scelerisque pulvinar. Quisque elementum lacus eget felis
              ullamcorper rhoncus. Donec condimentum porttitor tristique.
              Pellentesque eleifend vitae nulla vel interdum. Integer dui.
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.experience-container {
  background-color: navy;
}
.scrollspy-example {
  max-height: 500px;
}
.scrollspy-example h4[id] {
  scroll-margin-top: 80px;
}

#work-list {
  width: 30%;
}
#work-scrollspy {
  width: 70%;
}
#work-scrollspy {
  scroll-padding-top: 80px;
}

#study-list {
  width: 30%;
}
#study-scrollspy {
  width: 70%;
}
#study-scrollspy {
  scroll-padding-top: 80px;
}
</style>
