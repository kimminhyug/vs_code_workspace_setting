# vs_code_workspace_setting
휴가에 할게 없어서 개발환경 백업



# 개발할 떄 자주 사용하는 커스텀 단축키
<pre>
// Place your key bindings in this file to override the defaults
[
  {
    "key": "alt+shift+t",
    "args": { "snippet": "const theme = useGetThemeType();" },
    "command": "editor.action.insertSnippet"
  },
  {
    "key": "alt+shift+b",
    "args": {
      "snippet": "const [isOpenPanel, { setTrue: openPanel, setFalse: dismissPanel }] = useBoolean(false);"
    },
    "command": "editor.action.insertSnippet"
  },
  {
    "key": "alt+shift+l",
    "args": { "snippet": "const { t, i18n } = useTranslation();" },
    "command": "editor.action.insertSnippet"
  },
  {
    "key": "alt+shift+s",
    "when": "editorTextFocus",
    "args": {
      "snippet": "const [${TM_SELECTED_TEXT}, set${TM_SELECTED_TEXT/(?:^|-|_|\\.)(\\w)/${1:/upcase}/g}] = useState();"
    },
    "command": "editor.action.insertSnippet"
  },
  {
    "key": "alt+shift+e",
    "args": { "snippet": "useEffect(()=>{\n},[])" },
    "command": "editor.action.insertSnippet"
  },
]
</pre>

# 즐겨 쓰는 Extensions
 * eslint, prettier 같은 녀석은 제외
    
### Goat
1. GitLens - https://marketplace.visualstudio.com/items?itemName=eamodio.gitlens


    * 과거의 나 혹은 다른 사람의 커밋 히스토리를 라인별로 볼 수 있는 익스텐션. vs code 익스텐션은 이게 최고라 생각함(회사에선 유용하게 사용중)
  
      
2. Highlight Matching Tag - https://marketplace.visualstudio.com/items?itemName=vincaslt.highlight-matching-tag

    * 현재 커서가 위치한 태그의 시작 및 종료 지점을 하이라이트 해서 보여줌. Dom 구조가 복잡한 경우 생각보다 유용함
  
3. Git History - https://marketplace.visualstudio.com/items?itemName=donjayamanne.githistory

    * 현재 수정중인 파일 또는 원하는 파일의 깃 히스토리를 단축키, 버튼을 이용하여 바로 확인 가능함. 이전 수정 로그 버튼도 제공하는데 개발 하면서 히스토리 파악에 상당히 도움이 됨(회사에선 유용하게 사용중)
  
4. Code Spell Checker - https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker

    * 개발하다보면 의도치않게 영문오타를 발생 시킬 수 있는데 해당 오타를 밑줄을 통해 알려주고 수정도 해주는 녀석 상당히 만족 스럽게 쓰지만 영어를 잘하는 분들은 필요 없을듯
      
### 나름대로 괜찮음

1. i18n Ally - https://marketplace.visualstudio.com/items?itemName=Lokalise.i18n-ally

    * 개발 코드에서 i18n을 이용한 각 언어별 다국어 처리 현황을 placeholder 느낌으로 보여줌. $t('config:user.age') -> $t(유저 나이)
      * 초기 설정이 필요하고, 커서를 둬야 다국어의 키값이 보여진다는 단점이 존재 하지만 나름대로 쓸만함

2. Copy Json Path - https://marketplace.visualstudio.com/items?itemName=Malo.copy-json-path

    * 복잡한 JSON 구조에서 해당 키의 PATH를 복사 해주는 기능을 제공.
       * 보통 타입정의가 잘 되어 있으면 바로 확인이 가능하긴 한데, 회사에서 .yang 자동화 관련 로직(타입 정의 불가능한 모듈)에서 해당 path를 뽑아내는 경우가 많아서 유용하게 사용함
3. JSON to TS - https://marketplace.visualstudio.com/items?itemName=MariusAlchimavicius.json-to-ts

   * JSON을 드래그 하여 명렁어만 실행하면 TYPE 으로 정의 해줌. 몇몇 항목은 수정 해야 하긴 하지만 시간 절약에 나쁘지 않은듯
 
