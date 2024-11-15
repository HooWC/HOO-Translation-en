<template>
  <div id="app">
    <!-- 背景 -->
    <div class="background"></div>

    <!-- 主容器 -->
    <div class="main-content">
      <!-- 页眉 -->
      <div class="header">
        <h1>Super Translation Tool</h1>
        <p>Simple and efficient multilingual translation</p>
      </div>

      <!-- 内容部分 -->
      <div class="content">
        <!-- 输入区域 -->
        <div class="column left">
          <div class="card">
            <div class="language-selection">
              <div class="select-container">
                <label for="sourceLanguageSelect">Source Language</label>
                <select v-model="sourceLanguage" id="sourceLanguageSelect" class="form-control">
                  <option value="en">English</option>
                  <option value="zh-CN">Chinese (Simplified)</option>
                  <option value="zh-TW">Chinese (Traditional)</option>
                  <option value="es">Spanish</option>
                  <option value="fr">French</option>
                  <option value="de">German</option>
                  <option value="it">Italian</option>
                  <option value="pt">Portuguese</option>
                  <option value="ru">Russian</option>
                  <option value="ja">Japanese</option>
                  <option value="ko">Korean</option>
                  <option value="ar">Arabic</option>
                  <option value="nl">Dutch</option>
                  <option value="tr">Turkish</option>
                  <option value="el">Greek</option>
                  <option value="hi">Hindi</option>
                  <option value="th">Thai</option>
                  <option value="vi">Vietnamese</option>
                  <option value="pl">Polish</option>
                  <option value="sv">Swedish</option>
                  <option value="da">Danish</option>
                  <option value="fi">Finnish</option>
                  <option value="cs">Czech</option>
                  <option value="hu">Hungarian</option>
                  <option value="ro">Romanian</option>
                  <option value="sk">Slovak</option>
                  <option value="bg">Bulgarian</option>
                  <option value="uk">Ukrainian</option>
                  <option value="sr">Serbian</option>
                  <option value="hr">Croatian</option>
                  <option value="ms">Malay</option>
                  <option value="id">Indonesian</option>
                  <option value="ta">Tamil</option>
                  <option value="ml">Malayalam</option>
                  <option value="te">Telugu</option>
                  <option value="kn">Kannada</option>
                  <option value="mr">Marathi</option>
                  <option value="bn">Bengali</option>
                  <option value="pa">Punjabi</option>
                  <option value="gu">Gujarati</option>
                  <option value="or">Odia</option>
                  <option value="as">Assamese</option>
                  <option value="ne">Nepali</option>
                  <option value="si">Sinhalese</option>
                  <option value="km">Khmer</option>
                  <option value="lo">Lao</option>
                  <option value="my">Burmese</option>
                  <option value="tl">Tagalog</option>
                  <option value="jv">Javanese</option>
                  <option value="uz">Uzbek</option>
                  <option value="ky">Kyrgyz</option>
                  <option value="az">Azerbaijani</option>
                  <option value="am">Amharic</option>
                  <option value="haw">Hawaiian</option>
                  <option value="is">Icelandic</option>
                  <option value="eo">Esperanto</option>
                  <option value="sw">Swahili</option>
                  <option value="yo">Yoruba</option>
                  <option value="zu">Zulu</option>
                  <option value="xh">Xhosa</option>
                  <option value="af">Afrikaans</option>
                  <option value="ca">Catalan</option>
                  <option value="eu">Basque</option>
                  <option value="gl">Galician</option>
                  <option value="sq">Albanian</option>
                  <option value="mk">Macedonian</option>
                  <option value="no">Norwegian</option>
                  <option value="fi">Finnish</option>
                  <option value="sv">Swedish</option>
                  <option value="lt">Lithuanian</option>
                  <option value="lv">Latvian</option>
                  <option value="et">Estonian</option>
                  <option value="is">Icelandic</option>
                  <option value="hr">Croatian</option>
                  <option value="mt">Maltese</option>
                  <option value="sl">Slovenian</option>
                  <option value="bs">Bosnian</option>
                  <option value="hy">Armenian</option>
                  <option value="ka">Georgian</option>
                  <option value="mr">Marathi</option>
                  <option value="hy">Armenian</option>
                  <option value="sq">Albanian</option>
                </select>
              </div>

              <div class="select-container">
                <label for="targetLanguageSelect">Target Language</label>
                <select v-model="targetLanguage" id="targetLanguageSelect" class="form-control">
                  <option value="en">English</option>
                  <option value="zh-CN">Chinese (Simplified)</option>
                  <option value="zh-TW">Chinese (Traditional)</option>
                  <option value="es">Spanish</option>
                  <option value="fr">French</option>
                  <option value="de">German</option>
                  <option value="it">Italian</option>
                  <option value="pt">Portuguese</option>
                  <option value="ru">Russian</option>
                  <option value="ja">Japanese</option>
                  <option value="ko">Korean</option>
                  <option value="ar">Arabic</option>
                  <option value="nl">Dutch</option>
                  <option value="tr">Turkish</option>
                  <option value="el">Greek</option>
                  <option value="hi">Hindi</option>
                  <option value="th">Thai</option>
                  <option value="vi">Vietnamese</option>
                  <option value="pl">Polish</option>
                  <option value="sv">Swedish</option>
                  <option value="da">Danish</option>
                  <option value="fi">Finnish</option>
                  <option value="cs">Czech</option>
                  <option value="hu">Hungarian</option>
                  <option value="ro">Romanian</option>
                  <option value="sk">Slovak</option>
                  <option value="bg">Bulgarian</option>
                  <option value="uk">Ukrainian</option>
                  <option value="sr">Serbian</option>
                  <option value="hr">Croatian</option>
                  <option value="ms">Malay</option>
                  <option value="id">Indonesian</option>
                  <option value="ta">Tamil</option>
                  <option value="ml">Malayalam</option>
                  <option value="te">Telugu</option>
                  <option value="kn">Kannada</option>
                  <option value="mr">Marathi</option>
                  <option value="bn">Bengali</option>
                  <option value="pa">Punjabi</option>
                  <option value="gu">Gujarati</option>
                  <option value="or">Odia</option>
                  <option value="as">Assamese</option>
                  <option value="ne">Nepali</option>
                  <option value="si">Sinhalese</option>
                  <option value="km">Khmer</option>
                  <option value="lo">Lao</option>
                  <option value="my">Burmese</option>
                  <option value="tl">Tagalog</option>
                  <option value="jv">Javanese</option>
                  <option value="uz">Uzbek</option>
                  <option value="ky">Kyrgyz</option>
                  <option value="az">Azerbaijani</option>
                  <option value="am">Amharic</option>
                  <option value="haw">Hawaiian</option>
                  <option value="is">Icelandic</option>
                  <option value="eo">Esperanto</option>
                  <option value="sw">Swahili</option>
                  <option value="yo">Yoruba</option>
                  <option value="zu">Zulu</option>
                  <option value="xh">Xhosa</option>
                  <option value="af">Afrikaans</option>
                  <option value="ca">Catalan</option>
                  <option value="eu">Basque</option>
                  <option value="gl">Galician</option>
                  <option value="sq">Albanian</option>
                  <option value="mk">Macedonian</option>
                  <option value="no">Norwegian</option>
                  <option value="fi">Finnish</option>
                  <option value="sv">Swedish</option>
                  <option value="lt">Lithuanian</option>
                  <option value="lv">Latvian</option>
                  <option value="et">Estonian</option>
                  <option value="is">Icelandic</option>
                  <option value="hr">Croatian</option>
                  <option value="mt">Maltese</option>
                  <option value="sl">Slovenian</option>
                  <option value="bs">Bosnian</option>
                  <option value="hy">Armenian</option>
                  <option value="ka">Georgian</option>
                  <option value="mr">Marathi</option>
                  <option value="hy">Armenian</option>
                  <option value="sq">Albanian</option>
                </select>
              </div>
            </div>

            <div class="form-group">
              <label for="textInput">Text to Translate</label>
              <textarea v-model="text" id="textInput" class="form-control" rows="6"
                placeholder="Please type...."></textarea>
            </div>

            <div class="button-container">
              <button @click="translateText" class="btn btn-primary" :disabled="loading || !text">Translate</button>
            </div>
          </div>
        </div>

        <!-- 结果区域 -->
        <div class="column right">
          <div class="card">
            <h3>Translation Results</h3>
            <p v-if="loading">Translation in progress...</p>
            <p v-if="error" class="error">{{ errorMessage }}</p>
            <!-- 翻译结果处理换行 -->
            <p v-if="translatedText" v-html="formattedTranslatedText"></p>
          </div>
        </div>
      </div>
    </div>



  </div>

  <!-- 引入 Footer 组件 -->
  <Footer></Footer>
</template>

<script setup>
import { ref, computed } from 'vue'
import axios from 'axios'
import Footer from './components/Footer.vue'

// 响应式数据
const text = ref('')
const sourceLanguage = ref('en')
const targetLanguage = ref('zh-CN')
const translatedText = ref(null)
const error = ref(false)
const errorMessage = ref('')
const loading = ref(false)

// 翻译函数
const translateText = async () => {
  if (text.value.trim() === '') {
    translatedText.value = null
    return
  }

  if (sourceLanguage.value === targetLanguage.value) {
    error.value = true
    errorMessage.value = '源语言和目标语言相同，请选择不同的目标语言。'
    return
  }

  loading.value = true
  error.value = false
  errorMessage.value = ''
  translatedText.value = null

  try {
    const response = await axios.get(
      'https://api.mymemory.translated.net/get',
      {
        params: {
          q: text.value,
          langpair: `${sourceLanguage.value}|${targetLanguage.value}`,
        },
      }
    )

    if (response.data && response.data.responseData) {
      translatedText.value = response.data.responseData.translatedText
    } else {
      throw new Error('翻译失败，没有返回结果')
    }
  } catch (err) {
    console.error('翻译失败：', err)
    error.value = true
    errorMessage.value = '翻译失败，请稍后再试。'
  } finally {
    loading.value = false
  }
}

// 计算属性，将翻译文本中的换行符 \n 转换为 <br />
const formattedTranslatedText = computed(() => {
  if (!translatedText.value) return ''
  return translatedText.value.replace(/\n/g, '<br />')
})
</script>

<style scoped>
/* 背景 */
.background {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: linear-gradient(135deg, #5c6bc0, #7e57c2);
  /* 渐变色 */
  z-index: -1;
}

/* 主内容区域 */
.main-content {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  height: 100vh;
  /* 使容器充满整个屏幕 */
  padding: 20px;
  text-align: center;
  color: #fff;
  max-width: 100%;
  overflow: hidden;
}

/* 页眉 */
.header h1 {
  font-size: 3rem;
  color: #fff;
  font-family: 'Roboto', sans-serif;
  margin-bottom: 15px;
}

.header p {
  font-size: 1.1rem;
  color: #fff;
}

/* 内容区域（左右布局） */
.content {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  width: 100%;
  max-width: 1200px;
  gap: 30px;
  padding: 20px;
  box-sizing: border-box;
}

/* 左侧和右侧卡片 */
.column {
  flex: 1;
  padding: 20px;
  min-width: 300px;
}

/* 卡片样式 */
.card {
  padding: 20px;
  background-color: #fff;
  border-radius: 12px;
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.1);
  height: 100%;
}

.card h3 {
  font-size: 1.8rem;
  color: #333;
  margin-bottom: 15px;
}

.card p {
  font-size: 1.1rem;
  color: #555;
  word-wrap: break-word;
}

/* 语言选择 */
.language-selection {
  display: flex;
  justify-content: space-between;
  margin-bottom: 20px;
}

.select-container {
  width: 48%;
}

.language-selection label {
  font-weight: 600;
  color: #333;
  margin-bottom: 8px;
  display: block;
  font-size: 1rem;
}

.language-selection select {
  padding: 12px;
  width: 100%;
  border-radius: 8px;
  border: 2px solid #ddd;
  background-color: #fafafa;
  font-size: 1rem;
  transition: border-color 0.3s;
}

.language-selection select:focus {
  border-color: #7e57c2;
  outline: none;
}

/* 输入框 */
.form-group {
  margin-bottom: 25px;
}

textarea {
  width: 90%;
  padding: 12px;
  margin-top: 8px;
  border-radius: 8px;
  border: 2px solid #ddd;
  background-color: #fafafa;
  font-size: 1.1rem;
  transition: border-color 0.3s;
  resize: both;
  /* 允许调整大小 */
  max-width: 90%;
  min-width: 90%;
  /* 限制最大宽度为父元素的100% */
  max-height: 300px;
  min-height: 100px;
  /* 限制最大高度，避免过大 */
}

textarea:focus {
  border-color: #7e57c2;
  outline: none;
}

/* 按钮 */
button {
  padding: 12px 24px;
  background-color: #7e57c2;
  color: #fff;
  border: none;
  border-radius: 8px;
  font-size: 1.2rem;
  cursor: pointer;
  transition: background-color 0.3s, transform 0.3s;
}

button:hover {
  background-color: #5c6bc0;
  transform: translateY(-2px);
}

button:disabled {
  background-color: #b0b0b0;
  cursor: not-allowed;
}

/* 错误提示 */
.error {
  margin-top: 20px;
  padding: 15px;
  background-color: #f44336;
  border-radius: 8px;
  color: #fff;
  text-align: center;
}

/* 针对手机的样式 */
@media (max-width: 768px) {

  /* 页眉 */
  .header h1 {
    font-size: 2rem;
  }

  .header p {
    font-size: 1.2rem;
  }

  /* 内容区域（左右布局） */
  .content {
    flex-direction: column;
    gap: 20px;
  }

  .column {
    padding: 10px;
    min-width: 100%;
  }

  .column.right{
    margin-top:10px;
  }

  /* 输入框 */
  textarea {
    width: 90%;
    max-width: 100%;
    min-width: 90%;
    min-height: 120px;
  }

  /* 按钮 */
  button {
    width: 100%;
    padding: 14px;
    font-size: 1.1rem;
  }

  /* 错误提示 */
  .error {
    font-size: 1rem;
    padding: 12px;
  }
}
</style>
