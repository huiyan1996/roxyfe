<template>
  <!-- <Tutorial/> -->
  <div class="container">
    <!-- <h1 class="text-center">{{pageTitle}}</h1> -->
    <div class="row justify-content-center mt-3">
      <div class="col-lg-7">
        <Accordion :list="list" title="ROSY" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
  head() {
    return {
      title: "ROSY"
    }
  },
  data() {
    return {
      list: [
        {title: "USD/JPY是什么？", content: "<p>美元兑日元货币对。</p>"},
        {title: "什么比USD/JPY更值钱？", content: "<p>挪威克朗是世界上最强势的货币。</p>"},
        {title: "哪种金融工具可以反映USD/JPY？", content: "<p>EUR/USD和EUR/GBP与USD/JPY呈正相关，但它们的相关性会随着时间的推移而不断变化。</p>"},
        {title: "什么货币与USD/JPY相关？", content: "<p>USD/JPY与大多数日元对都成正相关，比如GBP/JPY和EUR/JPY 。</p>"},
        {title: "USD/JPY什么时候开始交易？", content: "<p>从美国东部时间周日的17点开始交易，一直持续到周五的17点。</p>"},
      ],
      pageTitle: "ROSY",
    }
  },
}
</script>
