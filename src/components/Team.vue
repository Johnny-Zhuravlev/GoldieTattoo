<template>
  <div class="team" id="team">
    <div class="team-content">
      <div class="team-artist">
        <img
          src="../assets/img/team/OboevTattoo.jpg"
          alt="OboevTattoo artist"
          class="team-artist-avatar"
        />
        <div class="team-artist-description">
          <div class="artist-expirience">Более 10 лет в деле</div>
          <div class="artist-style">Могёт всё</div>
        </div>
        <Socials />
      </div>
      <div class="team-artist">
        <img
          src="../assets/img/team/MawTattoo.jpg"
          alt="MawTattoo artist"
          class="team-artist-avatar"
        />
        <div class="team-artist-description">
          <div class="artist-expirience">Более 10 лет в деле</div>
          <div class="artist-style">Могёт всё</div>
        </div>
        <Socials />
      </div>
      <div class="team-artist">
        <img
          src="../assets/img/team/AntsupovTattoo.jpg"
          alt="AntsupovTattoo artist"
          class="team-artist-avatar"
        />
        <div class="team-artist-description">
          <div class="artist-expirience">9 лет в деле</div>
          <div class="artist-style">Реализм, ч/б</div>
        </div>
        <Socials />
      </div>
      <div class="team-artist">
        <img
          src="../assets/img/team/IvanTattooArt.jpg"
          alt="IvanTattoo artist"
          class="team-artist-avatar"
        />
        <div class="team-artist-description">
          <div class="artist-expirience">Более 7 лет в деле</div>
          <div class="artist-style">Реализм, ч/б, миниатюры</div>
        </div>
        <Socials />
      </div>
      <div class="team-artist">
        <img
          src="../assets/img/team/MovetonTattoo.jpg"
          alt="MovetonTattoo artist"
          class="team-artist-avatar"
        />
        <div class="team-artist-description">
          <div class="artist-expirience">2 года в деле</div>
          <div class="artist-style">Геометрия, ч/б</div>
        </div>
        <Socials />
      </div>
    </div>
  </div>
</template>

<script>
import Socials from "@/components/UI/Socials";
export default {
  components: {
    Socials,
  },
};
</script>

<style scoped>
.team {
  padding: 150px 0;

  background: #000;
}

.team-content {
  display: flex;
}

.team-artist {
  width: 20%;

  text-align: center;

  cursor: pointer;
}

.team-artist-avatar {
  width: 200px;
  height: 225px;
  margin-bottom: 15px;

  border-radius: 10px;
  box-shadow: 0 0 5px 5px rgba(255, 255, 255, 0.25);

  transition: all 0.3s linear;
}
.team-artist:hover .team-artist-avatar {
  box-shadow: 0 0 5px 5px rgba(255, 255, 255, 0.5);
}

.team-artist-description {
  margin-bottom: 15px;
}

.artist-style {
  font-size: 14px;
  line-height: 16px;

  color: #c0c0c0;
}
</style>
