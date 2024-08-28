<template>
<div class="post">
  <!-- header -->
  <header class="header section">
    <div class="header-author">
      <Avatar :size="40" />
      <div class="header-author-info">
        <div>
          <CustomText tag="b">ahmetkarsli</CustomText>
        </div>
        <div>
          <CustomText size="xsmall">Isparta, Merkez</CustomText>
        </div>
      </div>
    </div>
    <div class="header-more">
      <button type="button">
        <More />
      </button>
    </div>
  </header>
  <!-- Media -->
  <div class="post-media">
    <img src="@/assets/image.jpg"
     alt=""
    />
  </div>

  <!-- Actions -->
  <div class="action-buttons section">
    <button type="button">
      <Like />
    </button>
    <button type="button">
      <Comment />
    </button>
    <button type="button">
      <Direct />
    </button>
    <button class="action-save" type="button">
      <Save />
    </button>
  </div>

  <!-- View Count -->
  <div class="view-count section">
    <custom-text tag="b">1.345 beğenme</custom-text>
  </div>

  <!-- Comment list -->


  <!-- Datetime -->


  <!-- Comment Form -->


</div>
</template>

<script>
import CustomText from "@/components/CustomText.vue";
import Save from "@/icons/Save.vue";
import Direct from "@/icons/Direct.vue";
import Comment from "@/icons/Comment.vue";
import Like from "@/icons/Like.vue";
import Avatar from "@/components/Avatar.vue";
import More from "@/icons/More.vue";

export default {
  name: 'Post',
  components: { More, Avatar, Like, Comment, Direct, Save, CustomText }
}

</script>

<style scoped>
.post {
  border-radius: 3px;
  border: 1px solid #DBDBDB;
}

.section {
  padding-left: 16px;
  padding-right: 16px;
}

.header {
  height: 60px;
  display: flex;
  align-items: center;

  &-author {
    display: flex;
    align-items: center;

    &-info {
      margin-left: 8px;
    }
  }

  &-more {
    margin-left: auto;
  }
}

.action-buttons {
  height: 45px;
  display: flex;
  align-items: center;

  button {
    margin-right: 16px;
  }

  .action-save {
    margin-left: auto;
    margin-right: 0;
  }
}
</style>