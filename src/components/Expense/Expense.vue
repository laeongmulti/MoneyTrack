<template>
  <!-- 적응형 스타일 적용 -->
  <div :class="styles['expense-full-container']">
    <!-- 달력 컴포넌트 -->
    <ExpenseCalendar
      :recordData="expenseStore.expenseList"
      v-model:selectedDate="selectedDate"
    />
    <!-- 선택 날짜 내역 -->
    <ExpenseFilterContainer
      :transactions="expenseStore.expenseList"
      :selectedDate="selectedDate"
    />
  </div>
</template>

<script setup>
import { ref, onMounted, watch } from 'vue';

// styles
import styles from '@/css/expense/expense.module.css';

//components
import ExpenseCalendar from './ExpenseCalender.vue';
import ExpenseFilterContainer from './ExpenseFilterContainer.vue';

// stores
import { useExpenseStore } from '@/stores/expense';
import { useCategoryStore } from '@/stores/category';

// init store & user
const expenseStore = useExpenseStore();
const categoryStore = useCategoryStore();
const user = ref('');

//오늘 날짜로 default 설정
const today = new Date();
const selectedDate = ref(today);

// user 변경되면 데이터 다시 받아오기
watch(user, async (newUser) => {
  if (newUser && newUser.id) {
    await expenseStore.fetchExpenseList();
  }
});

//db 데이터 fetch
onMounted(async () => {
  try {
    await categoryStore.fetchcategoryList();
    await expenseStore.fetchExpenseList();
  } catch (e) {
    console.error('지출 데이터 불러오기 실패:', e);
  }
});
</script>
