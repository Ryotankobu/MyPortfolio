<script setup>
    import sampleImage from "@/assets/images/bellsprout.png";
    import reactIcon from "@/assets/images/reactIcon.svg.png";
    import ajileIcon from "@/assets/images/ajileIcon.png";
    import communicationIcon from "@/assets/images/communicationIcon.png";
    import reliabilityuIcon from "@/assets/images/reliabilityIcon.png";
</script>
<template>
    <div class="d-flex flex-column h-100 mt-3">

        <div class="border border-3 border-dark rounded mt-4 skill-box">
            <div class="row py-1 px-3 h-100">
                <div
                class="col-2 icon-box d-flex align-items-center justify-content-center"
                >
                <div class="p-4 bg-white text-center rounded">
                <img
                    :src="ajileIcon"
                    class="card-img-top w-100"
                    alt="..."
                />

                </div>
                
                </div>
                <div
                class="col-8 p-0 pe-2 skill-details-box d-flex flex-column"
                >
                <h4 class="skill-box-title">Ajile Coordination</h4>
                <p class="tight-text">
                    I coordinate one of the MFDC projects by planning weekly sprints, organising and clarifying incoming issues, and ensuring each ticket has the detail needed for development. I work closely with developers to track progress, confirm completion, and maintain a clear, structured workflow.
                </p>
            
                </div>
                <div
                class="col-2 p-0 skill-level-box d-flex flex-column justify-content-around py-3"
                >
                <div
                    class="skill-level-number-box border rounded text-center"
                >
                    28 / 100
                </div>
                    <div class="progress">
                    <div
                        class="progress-bar bg-success"
                        role="progressbar"
                        style="width: 28%"
                        aria-valuenow="25"
                        aria-valuemin="0"
                        aria-valuemax="100"
                    ></div>
                </div>
                </div>
            </div>
        </div>



        <div class="border border-3 border-dark rounded mt-3 skill-box">
            <div class="row py-1 px-3 h-100">
                <div
                class="col-2 icon-box d-flex align-items-center justify-content-center"
                >
                <div class="p-4 bg-white text-center rounded">
                <img
                    :src="communicationIcon"
                    class="card-img-top w-100"
                    alt="..."
                />

                </div>
                
                </div>
                <div
                class="col-8 p-0 pe-2 skill-details-box d-flex flex-column"
                >
                <h4 class="skill-box-title">Stakeholder Communication</h4>
                <p class="tight-text">
                    In my previous marketing role at a language school, I worked closely with overseas (Japanese) agents, listening to their needs, responding clearly and professionally by email, and managing expectations with reliable timing. I often anticipated what they were trying to achieve and delivered outcomes that made their work easier, strengthening long‑term relationships and improving overall workflow.
                </p>
            
                </div>
                <div
                class="col-2 p-0 skill-level-box d-flex flex-column justify-content-around py-3"
                >
                <div
                    class="skill-level-number-box border rounded text-center"
                >
                    75 / 100
                </div>
                    <div class="progress">
                    <div
                        class="progress-bar bg-success"
                        role="progressbar"
                        style="width: 75%"
                        aria-valuenow="25"
                        aria-valuemin="0"
                        aria-valuemax="100"
                    ></div>
                </div>
                </div>
            </div>
        </div>



        
        <div class="border border-3 border-dark rounded mt-3 skill-box">
            <div class="row py-1 px-3 h-100">
                <div
                class="col-2 icon-box d-flex align-items-center justify-content-center"
                >
                <div class="p-4 bg-white text-center rounded">
                <img
                    :src="reliabilityuIcon"
                    class="card-img-top w-100"
                    alt="..."
                />

                </div>
                
                </div>
                <div
                class="col-8 p-0 pe-2 skill-details-box d-flex flex-column"
                >
                <h4 class="skill-box-title">Profeccional Condact & Reliability</h4>
                <p class="tight-text">
                    My part‑time work as a casino dealer requires strict punctuality, precise adherence to regulated procedures, and a high level of honesty and trustworthiness. Maintaining these standards for over three years has strengthened my reliability, attention to detail, and commitment to professional conduct — qualities I bring into my BA and project work.
                </p>
            
                </div>
                <div
                class="col-2 p-0 skill-level-box d-flex flex-column justify-content-around py-3"
                >
                <div
                    class="skill-level-number-box border rounded text-center"
                >
                    88 / 100
                </div>
                    <div class="progress">
                    <div
                        class="progress-bar bg-success"
                        role="progressbar"
                        style="width: 88%"
                        aria-valuenow="25"
                        aria-valuemin="0"
                        aria-valuemax="100"
                    ></div>
                </div>
                </div>
            </div>
        </div>

              
    </div>
</template>
<style scoped>
.skill-box {
    background-color: var(--skill-box);
    display: flex;
    /* flex: 1; */
}
.skill-box-title {
  font-family: "Work Sans", sans-serif;
  font-optical-sizing: auto;
  font-weight: 500;
  font-style: normal;
  font-weight: bold;

}
.tight-text {
  line-height: 1;
  font-family: "Work Sans", sans-serif;
  font-optical-sizing: auto;
  font-weight: 500;
  font-style: normal;
}
.skill-level-number-box {
    font-family: "Work Sans", sans-serif;
  font-optical-sizing: auto;
  font-weight: 500;
  font-style: normal;
  font-weight: bold;
}
</style>