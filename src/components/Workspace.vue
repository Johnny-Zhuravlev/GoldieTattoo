<template>
  <div class="workspace">
    <div class="workspace-video">
      <video
        class="workspace-video-bg"
        poster="../assets/img/workspacePoster.jpg"
        muted
        loop
      >
        <source
          src="../assets/img/workspace.mp4"
          type='video/mp4; codecs="avc1.42E01E, mp4a.40.2"'
        />
      </video>
    </div>
    <div class="workspace-info-right">
      <div class="workspace-info-right-content">
        <h2 class="workspace-title">
          Работаем в комфортной
          <br />
          и современной студии
          <br />
          в центре Петербурга
        </h2>
        <div class="workspace-subtitle">
          Современная техника, качественные расходники, инвентарь, обстановка и
          отличное настроение.
          <br />
          Всё для комфортной и качественной работы.
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.workspace {
  display: flex;
  height: 100vh;
  min-height: 700px;
}

.workspace-video,
.workspace-info-right {
  width: 50%;
  min-height: 700px;

  position: relative;

  z-index: -1;
}
.workspace-video::before {
  content: "";
  width: 100%;
  height: 100%;

  background: #000;
  backdrop-filter: blur(2px);
  opacity: 0.4;

  position: absolute;
  top: 0;
  left: 0;

  z-index: -1;
}
.workspace-video-bg {
  width: 100%;
  height: 100%;
  object-fit: cover;

  position: absolute;
  top: 0;
  left: 0;

  z-index: -2;
}
.workspace-info-right {
  display: flex;

  background: #000;
}
.workspace-info-right-content {
  width: 80%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  margin: auto;
}

.workspace-title {
  margin-bottom: 20px;

  font-size: 46px;
  line-height: 52px;
}

.workspace-subtitle {
  font-size: 18px;
  line-height: 24px;
}
</style>
