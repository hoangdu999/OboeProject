<template>
  <div class="footer">
    <div class="footer-bot flex">
      <div class="footer-infor">
        <TheLogo class="footer-logo" />
        <ul>
          <li class="flex p-hover" v-for="(item, index) in listInfor" :key="index">
            <div class="mr-10 pb-25 footer-inforicon">
              <i :class="item.icon" class="w-100"></i>
            </div>
            <p class="footer-infortext">{{ item.title }}</p>
          </li>
        </ul>
        <ul class="flex social-links">
          <li class="mr-10" v-for="(item, index) in listCNC" :key="index">
            <a :href="item.src" target="_blank" rel="noopener noreferrer">
              <i :class="item.icon" class="w-100"></i>
            </a>
          </li>
        </ul>
      </div>
      <div class="footer-listservies-hr">
        <ul class="flex">
          <li class="mr-10 listservies-box" v-for="(items, outerIndex) in listServies" :key="outerIndex">
            <p class="listservies-title">{{ items.title }}</p>
            <div class="listservies-hr"></div>
            <ul>
              <li :class="[
                'listservies-detail',
                {
                  cur: outerIndex !== listServies.length - 1,
                  'p-hover': outerIndex !== listServies.length - 1
                }
              ]" v-for="(item, innerIndex) in items.service" :key="innerIndex">
                <router-link v-if="item.link" :to="item.link">
                  <p>{{ item.title }}</p>
                </router-link>
                <p v-else>{{ item.title }}</p>
              </li>
              <MsButton 
                v-if="outerIndex === listServies.length - 1" 
                class="button-hover footer-comment-btn" 
                height="40px" 
                @click="handleFeedbackClick"
              >
                GỬI Ý KIẾN
              </MsButton>
            </ul>
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue';
import { useStore } from 'vuex';
import { useRouter } from 'vue-router';
import TheLogo from '@/components/layout/logo/TheLogo.vue';
import MsButton from '@/components/common/button/MsButton.vue';

const store = useStore();
const router = useRouter();

// Fetch the data from Vuex store
const listInfor = store.getters['footer/ListInfor'];
const listCNC = store.getters['footer/ListCNC'];
const listServies = store.getters['footer/ListServies'];

const handleFeedbackClick = () => {
  router.push('/footer-services/contact');
};
</script>

<style lang="scss" scoped>
@use '@/components/layout/footer/TheFooter.scss';
</style>
