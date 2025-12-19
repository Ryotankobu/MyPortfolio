<script setup>
    import sampleImage from "@/assets/images/bellsprout.png";
</script>

<template>
    <footer class="footer d-flex text-center flex-column py-5">
        <div class="logo-area mx-auto">
            <div class="image-box mb-3">
                
                <h2 style="color: var(--navbar-text)">My Portfolio</h2>

            </div>
            
            <div class="icon-box">
                  <div class="row justify-content-center">
                    <div class="col-1">
                      <img
                        :src="sampleImage"
                        class="card-img-top w-25"
                        alt="..."
                      />
                    </div>
                    <div class="col-1">
                      <img
                        :src="sampleImage"
                        class="card-img-top w-25"
                        alt="..."
                      />
                    </div>
                    <div class="col-1">
                      <img
                        :src="sampleImage"
                        class="card-img-top w-25"
                        alt="..."
                      />
                    </div>
                  </div>
                </div>
        </div>
        <!-- <div class="footer-nav-area bg-success mx-auto mt-5">
            <ul class="nav text-center">
                <li class="nav-item">
                    <a class="nav-link active" href="#">Active</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="#">Link</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="#">Link</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link disabled" href="#">Disabled</a>
                </li>
                </ul>
        </div> -->
  </footer>
</template>

<style scoled>
.footer {
  background-color: var(--navbar-background);
}
.footer p {
    margin-top: 0;
}
.logo-area {

}
h2 {
  font-family: "Press Start 2P", system-ui;
  font-weight: 400;
  font-style: normal;
}
</style>