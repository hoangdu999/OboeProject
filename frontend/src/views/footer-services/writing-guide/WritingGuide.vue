<template>
  <div class="writing-guide-page">
    <div class="writing-guide-container">
      <div class="writing-guide-header">
        <h1>Phân Biệt Hiragana và Katakana</h1>
        <p class="last-updated">Cập nhật lần cuối: {{ lastUpdated }}</p>
      </div>

      <div class="writing-guide-content">
        <section class="guide-section">
          <h2>1. Tổng Quan Về Chữ Viết Nhật Bản</h2>
          <div class="sub-section">
            <h3>1.1. Ba Hệ Thống Chữ Viết</h3>
            <p>Tiếng Nhật sử dụng 3 hệ thống chữ viết chính:</p>
            <ul>
              <li>Hiragana (ひらがな): Chữ cong, mềm mại, dùng cho từ thuần Nhật</li>
              <li>Katakana (カタカナ): Chữ thẳng, góc cạnh, dùng cho từ nước ngoài</li>
              <li>Kanji (漢字): Chữ Hán, mang nghĩa cụ thể</li>
            </ul>
          </div>
          <div class="sub-section">
            <h3>1.2. Vai Trò Trong Câu</h3>
            <ul>
              <li>Hiragana: Viết đuôi động từ, trợ từ, từ thuần Nhật</li>
              <li>Katakana: Từ nước ngoài, tên nước ngoài, thuật ngữ khoa học</li>
              <li>Kanji: Thể hiện nghĩa chính của từ</li>
            </ul>
          </div>
        </section>

        <section class="guide-section">
          <h2>2. Hiragana (ひらがな)</h2>
          <div class="sub-section">
            <h3>2.1. Đặc Điểm</h3>
            <ul>
              <li>Nét chữ cong, mềm mại, liền mạch</li>
              <li>46 chữ cái cơ bản</li>
              <li>Dùng dấu để biến âm (dakuten, handakuten)</li>
              <li>Viết theo quy tắc stroke order cụ thể</li>
            </ul>
          </div>
          <div class="sub-section">
            <h3>2.2. Cách Sử Dụng</h3>
            <ul>
              <li>Viết các từ thuần Nhật (和語 - わご)</li>
              <li>Viết đuôi động từ, tính từ</li>
              <li>Viết trợ từ (は、が、を、に、で...)</li>
              <li>Viết furigana (phiên âm trên kanji)</li>
            </ul>
          </div>
        </section>

        <section class="guide-section">
          <h2>3. Katakana (カタカナ)</h2>
          <div class="sub-section">
            <h3>3.1. Đặc Điểm</h3>
            <ul>
              <li>Nét chữ thẳng, góc cạnh, đơn giản</li>
              <li>46 chữ cái tương ứng với Hiragana</li>
              <li>Dễ nhận biết trong văn bản</li>
              <li>Thường viết các âm dài bằng dấu gạch (ー)</li>
            </ul>
          </div>
          <div class="sub-section">
            <h3>3.2. Cách Sử Dụng</h3>
            <ul>
              <li>Viết từ nước ngoài (外来語 - がいらいご)</li>
              <li>Tên người, địa danh nước ngoài</li>
              <li>Thuật ngữ khoa học, kỹ thuật</li>
              <li>Nhấn mạnh từ ngữ trong câu</li>
            </ul>
          </div>
        </section>

        <section class="guide-section">
          <h2>4. Cách Phân Biệt</h2>
          <div class="sub-section">
            <h3>4.1. Về Hình Dạng</h3>
            <div class="comparison-table">
              <div class="table-row header">
                <div class="cell">Âm</div>
                <div class="cell">Hiragana</div>
                <div class="cell">Katakana</div>
              </div>
              <div class="table-row">
                <div class="cell">A</div>
                <div class="cell">あ</div>
                <div class="cell">ア</div>
              </div>
              <div class="table-row">
                <div class="cell">I</div>
                <div class="cell">い</div>
                <div class="cell">イ</div>
              </div>
              <div class="table-row">
                <div class="cell">U</div>
                <div class="cell">う</div>
                <div class="cell">ウ</div>
              </div>
              <div class="table-row">
                <div class="cell">E</div>
                <div class="cell">え</div>
                <div class="cell">エ</div>
              </div>
              <div class="table-row">
                <div class="cell">O</div>
                <div class="cell">お</div>
                <div class="cell">オ</div>
              </div>
            </div>
          </div>
          <div class="sub-section">
            <h3>4.2. Về Ngữ Cảnh Sử Dụng</h3>
            <div class="example-box">
              <p class="example-title">Ví dụ:</p>
              <p class="example-text">私はコーヒーを飲みます。</p>
              <p class="example-explain">
                - 私 (わたし): "tôi" - từ thuần Nhật, viết bằng kanji và hiragana<br>
                - は: trợ từ, viết bằng hiragana<br>
                - コーヒー: "cà phê" - từ nước ngoài, viết bằng katakana<br>
                - を: trợ từ, viết bằng hiragana<br>
                - 飲みます (のみます): "uống" - động từ thuần Nhật, viết bằng kanji và hiragana
              </p>
            </div>
          </div>
        </section>

        <section class="guide-section">
          <h2>5. Phương Pháp Học Hiệu Quả</h2>
          <div class="sub-section">
            <h3>5.1. Thứ Tự Học</h3>
            <ol>
              <li>Học Hiragana trước (2-3 tuần)</li>
              <li>Học Katakana sau (2-3 tuần)</li>
              <li>Luyện đọc kết hợp cả hai</li>
              <li>Học Kanji song song</li>
            </ol>
          </div>
          <div class="sub-section">
            <h3>5.2. Kỹ Thuật Ghi Nhớ</h3>
            <ul>
              <li>Sử dụng flashcard trên Oboe</li>
              <li>Viết tay thường xuyên</li>
              <li>Tập đọc văn bản thực tế</li>
              <li>Luyện tập stroke order đúng cách</li>
            </ul>
          </div>
        </section>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue';

const lastUpdated = ref('15/03/2024');
</script>

<style lang="scss" scoped>
@use '@/views/footer-services/writing-guide/WritingGuide.scss';
</style> 