# 출첵수 카운트
Version 1

### 업데이트일 : 2024-06-06
1. 메세지 추가
2. error 메세지, success 메세지, warnings 메세지 업데이트

### 업데이트일 : 2024-06-10
1. 세션 초기화(하루 단위)
2. 12시간으로 변경

### 업데이트일 : 2024-06-12
1. 사이드 바 스파크 차트 추가
2. 캐시 날짜 기입

### 업데이트일 : 2024-06-13
1. 사이드 바 스파크 차트 추가 -> 아이폰 사파리 #185 error가 뜸
오류 내용
```
Error: Minified React error #185; 
visit https://reactjs.org/docs/error-decoder.html?invariant=185 for the full message or use the non-minified dev environment for full errors and additional helpful warnings.
ns@https://choyoringattendancelist.streamlit.app/~/+/static/js/main.7e42f54d.js:2:2264194
@https://choyoringattendancelist.streamlit.app/~/+/static/js/6950.70fe55c2.chunk.js:2:149813
@https://choyoringattendancelist.streamlit.app/~/+/static/js/6950.70fe55c2.chunk.js:2:279976
@https://choyoringattendancelist.streamlit.app/~/+/static/js/6950.70fe55c2.chunk.js:2:222568
@https://choyoringattendancelist.streamlit.app/~/+/static/js/6950.70fe55c2.chunk.js:2:222783
@https://choyoringattendancelist.streamlit.app/~/+/static/js/6950.70fe55c2.chunk.js:2:218898
@https://choyoringattendancelist.streamlit.app/~/+/static/js/6950.70fe55c2.chunk.js:2:219173
ol@https://choyoringattendancelist.streamlit.app/~/+/static/js/main.7e42f54d.js:2:2289416
yl@https://choyoringattendancelist.streamlit.app/~/+/static/js/main.7e42f54d.js:2:2296713
zl@https://choyoringattendancelist.streamlit.app/~/+/static/js/main.7e42f54d.js:2:2296557
gl@https://choyoringattendancelist.streamlit.app/~/+/static/js/main.7e42f54d.js:2:2296093
@https://choyoringattendancelist.streamlit.app/~/+/static/js/main.7e42f54d.js:2:2307930
Ac@https://choyoringattendancelist.streamlit.app/~/+/static/js/main.7e42f54d.js:2:2308443
cc@https://choyoringattendancelist.streamlit.app/~/+/static/js/main.7e42f54d.js:2:2302164
Uo@https://choyoringattendancelist.streamlit.app/~/+/static/js/main.7e42f54d.js:2:2242556
rc@https://choyoringattendancelist.streamlit.app/~/+/static/js/main.7e42f54d.js:2:2299049
ns@https://choyoringattendancelist.streamlit.app/~/+/static/js/main.7e42f54d.js:2:2264194
@https://choyoringattendancelist.streamlit.app/~/+/static/js/8148.a17a918e.chunk.js:1:47204
```
2. 사이드 바 오류 -> css 사이드바 안보이게 작업
3. 오전 8시 캐시 초기화로 변경
   
### 업데이트일 : 2024-06-15
1. 캐시데이터 유효기간으로 변경(ttl) 12h

### 업데이트일 : 2024-08-16
오류 발생 ->
```
────────────────────── Traceback (most recent call last) ───────────────────────

  /home/adminuser/venv/lib/python3.10/site-packages/streamlit/runtime/scriptru  

  nner/script_runner.py:589 in _run_script                                      

                                                                                

  /mount/src/attendancecheckcount/main.py:5 in <module>                         

                                                                                

      2 import pandas as pd                                                     

      3 import datetime                                                         

      4 import plotly.express as px                                             

  ❱   5 from streamlit_gsheets import GSheetsConnection                         

      6                                                                         

      7 @st.cache_resource(ttl=43200)                                           

      8 def load_data():                                                        

                                                                                

  /home/adminuser/venv/lib/python3.10/site-packages/streamlit_gsheets/__init__  

  .py:15 in <module>                                                            

                                                                                

    12 # See the License for the specific language governing permissions and    

    13 # limitations under the License.                                         

    14                                                                          

  ❱ 15 from streamlit_gsheets.gsheets_connection import GSheetsConnection  # n  

    16                                                                          

                                                                                

  /home/adminuser/venv/lib/python3.10/site-packages/streamlit_gsheets/gsheets_  

  connection.py:36 in <module>                                                  

                                                                                

     33 from pandas import DataFrame, read_csv                                  

     34 from sql_metadata import Parser                                         

     35 from streamlit.connections import ExperimentalBaseConnection            

  ❱  36 from streamlit.dataframe_util import convert_anything_to_pandas_df, is  

     37 from streamlit.runtime.caching import cache_data                        

     38 from validators.url import url as validate_url                          

     39                                                                         

────────────────────────────────────────────────────────────────────────────────

ModuleNotFoundError: No module named 'streamlit.dataframe_util'
```



