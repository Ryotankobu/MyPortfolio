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
                  <div class="d-flex flex-row justify-content-center">
                    <div class="mx-2">
                      <a href="https://github.com/Ryotankobu"  target="_blank" rel="noopener"
                        data-toggle="tooltip" data-placement="bottom" title="GitHub">
                        <i class="fa-brands fa-square-github fa-xl text-light"></i>
                      </a>
                      
                    </div>
                    <div class="mx-2">
                      <a href="https://www.linkedin.com/in/ryota-ando-573569276/"  target="_blank" rel="noopener"
                        data-toggle="tooltip" data-placement="bottom" title="LinkedIn">
                        <i class="fa-brands fa-linkedin fa-xl text-light"></i>
                      </a>
                      
                    </div>
                    <div class="mx-2">
                      <a href="https://docs.google.com/document/d/1GPJmZuoX05_Ddj2GP6WGgCdu_A10F2zbjJRz6cF-Rk4/edit?usp=sharing"  target="_blank" rel="noopener"
                        data-toggle="tooltip" data-placement="bottom" title="Resume">
                        <i class="fa-solid fa-file fa-xl text-light"></i>
                      </a>
                      
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