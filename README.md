### Hi there 👋

<!--
**rnrl1215/rnrl1215** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
<!--https://img.shields.io/badge/텍스트-뱃지컬러?style=flat-square&logo=이모지이름&logoColor=white-->
<img src="https://img.shields.io/badge/Python-3766AB?style=flat-square&logo=Python&logoColor=white"/></a>
const { checkReversal } = require('../src/util');

const path = (height) => {
    height = Number(height);
    height -= 120;      // 120 is benchmark pos-y
    const point = [
        70+height,
        -55+height,
        55+height,
        60+height,
        50+height,
        75+height
    ]

    return `m 0 0 T 0 ${point[0]} Q 110 ${point[1]} 220 ${point[2]} T 440 ${point[3]} T 660 ${point[4]} T 880 ${point[5]} T 880 0 z`;
}

const render = (reversal, color, height) => {
    reversal = checkReversal(reversal);

    return `<path fill="${color}" ${reversal} fill-opacity="1" d="${path(height)}"></path>`;
}

module.exports = { render };
