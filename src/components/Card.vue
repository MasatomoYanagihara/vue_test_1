<template>
  <div>
    <!-- カードコンポーネント -->
    <router-link to="/shop/shopdetaile">
      <v-col cols="12">
        <v-card class="mx-auto outline" max-width="320px" height="440px">
          <v-img height="240" src="@/assets/shop1.jpg" />
          <!-- 店名 -->
          <v-card-title>{{ post.shopName.stringValue }}</v-card-title>

          <!-- 水平線 -->
          <v-divider class="mx-4"></v-divider>

          <v-card-text>
            <!-- ジャンル -->
            <div class="my-4 subtitle-1">{{ post.shopGanre.stringValue }}</div>
            <!-- 説明文 -->
            営業時間 {{ post.openTime.stringValue }} 〜
            {{ post.closeTime.stringValue }}
          </v-card-text>
        </v-card>
      </v-col>
    </router-link>
  </div>
</template>

<script>
// import axios from 'axios';

export default {
  props: ["post"]
};
</script>
