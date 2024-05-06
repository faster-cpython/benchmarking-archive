## Execution counts

<details>
<summary> Execution counts for Tier 1 instructions. </summary>


The "miss ratio" column shows the percentage of times the instruction
executed that it deoptimized. When this happens, the base unspecialized
instruction is not counted.

<table>
<thead>
<tr>
<th align="left">Name</th>
<th align="right">Base Count</th>
<th align="right">Head Count</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">UNPACK_SEQUENCE_TUPLE</td>
<td align="right">241,771,116</td>
<td align="right">5,717,702</td>
<td align="right">-97.6%</td>
</tr>
<tr>
<td align="left">CONVERT_VALUE</td>
<td align="right">99,560,125</td>
<td align="right">2,857,820</td>
<td align="right">-97.1%</td>
</tr>
<tr>
<td align="left">END_FOR</td>
<td align="right">34,063,396</td>
<td align="right">1,698,634</td>
<td align="right">-95.0%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_LIST</td>
<td align="right">8,179,923</td>
<td align="right">484,097</td>
<td align="right">-94.1%</td>
</tr>
<tr>
<td align="left">BUILD_STRING</td>
<td align="right">55,607,776</td>
<td align="right">3,382,319</td>
<td align="right">-93.9%</td>
</tr>
<tr>
<td align="left">FORMAT_SIMPLE</td>
<td align="right">109,448,215</td>
<td align="right">6,813,869</td>
<td align="right">-93.8%</td>
</tr>
<tr>
<td align="left">FOR_ITER_GEN</td>
<td align="right">35,007,769</td>
<td align="right">2,342,557</td>
<td align="right">-93.3%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_STR_INT</td>
<td align="right">368,326,352</td>
<td align="right">27,299,027</td>
<td align="right">-92.6%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">1,132,021,127</td>
<td align="right">127,725,743</td>
<td align="right">-88.7%</td>
</tr>
<tr>
<td align="left">DELETE_ATTR</td>
<td align="right">4,678,978</td>
<td align="right">641,422</td>
<td align="right">-86.3%</td>
</tr>
<tr>
<td align="left">BINARY_OP_INPLACE_ADD_UNICODE</td>
<td align="right">2,751,962</td>
<td align="right">434,020</td>
<td align="right">-84.2%</td>
</tr>
<tr>
<td align="left">FORMAT_WITH_SPEC</td>
<td align="right">1,760</td>
<td align="right">320</td>
<td align="right">-81.8%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP_SET</td>
<td align="right">282,467,249</td>
<td align="right">55,573,104</td>
<td align="right">-80.3%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP_DICT</td>
<td align="right">131,387,820</td>
<td align="right">28,402,289</td>
<td align="right">-78.4%</td>
</tr>
<tr>
<td align="left">UNPACK_EX</td>
<td align="right">1,129,822</td>
<td align="right">258,020</td>
<td align="right">-77.2%</td>
</tr>
<tr>
<td align="left">SET_ADD</td>
<td align="right">965,797</td>
<td align="right">241,040</td>
<td align="right">-75.0%</td>
</tr>
<tr>
<td align="left">CALL_TUPLE_1</td>
<td align="right">20,482,954</td>
<td align="right">5,226,936</td>
<td align="right">-74.5%</td>
</tr>
<tr>
<td align="left">UNARY_NOT</td>
<td align="right">25,398,543</td>
<td align="right">6,874,379</td>
<td align="right">-72.9%</td>
</tr>
<tr>
<td align="left">TO_BOOL_STR</td>
<td align="right">46,922,446</td>
<td align="right">12,807,979</td>
<td align="right">-72.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_GETATTRIBUTE_OVERRIDDEN</td>
<td align="right">89,680</td>
<td align="right">25,520</td>
<td align="right">-71.5%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE</td>
<td align="right">532,693</td>
<td align="right">154,120</td>
<td align="right">-71.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_CLASS</td>
<td align="right">130,821,248</td>
<td align="right">39,191,100</td>
<td align="right">-70.0%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_STR</td>
<td align="right">305,289,111</td>
<td align="right">92,634,193</td>
<td align="right">-69.7%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_FLOAT</td>
<td align="right">69,194,267</td>
<td align="right">21,246,061</td>
<td align="right">-69.3%</td>
</tr>
<tr>
<td align="left">SET_FUNCTION_ATTRIBUTE</td>
<td align="right">53,133,464</td>
<td align="right">16,752,120</td>
<td align="right">-68.5%</td>
</tr>
<tr>
<td align="left">FOR_ITER_RANGE</td>
<td align="right">52,310,870</td>
<td align="right">17,155,507</td>
<td align="right">-67.2%</td>
</tr>
<tr>
<td align="left">MAKE_CELL</td>
<td align="right">104,335,075</td>
<td align="right">34,409,925</td>
<td align="right">-67.0%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">1,139,735,807</td>
<td align="right">391,562,234</td>
<td align="right">-65.6%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_DICT</td>
<td align="right">390,878,742</td>
<td align="right">137,699,904</td>
<td align="right">-64.8%</td>
</tr>
<tr>
<td align="left">NOP</td>
<td align="right">760,586,063</td>
<td align="right">277,519,850</td>
<td align="right">-63.5%</td>
</tr>
<tr>
<td align="left">FOR_ITER_TUPLE</td>
<td align="right">118,857,475</td>
<td align="right">44,520,884</td>
<td align="right">-62.5%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">395,696,024</td>
<td align="right">152,171,525</td>
<td align="right">-61.5%</td>
</tr>
<tr>
<td align="left">STORE_SLICE</td>
<td align="right">7,301,451</td>
<td align="right">2,884,620</td>
<td align="right">-60.5%</td>
</tr>
<tr>
<td align="left">MAKE_FUNCTION</td>
<td align="right">65,058,084</td>
<td align="right">26,808,222</td>
<td align="right">-58.8%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">335,850,460</td>
<td align="right">139,332,350</td>
<td align="right">-58.5%</td>
</tr>
<tr>
<td align="left">MAP_ADD</td>
<td align="right">27,247,061</td>
<td align="right">11,494,784</td>
<td align="right">-57.8%</td>
</tr>
<tr>
<td align="left">BUILD_SLICE</td>
<td align="right">71,112,575</td>
<td align="right">31,160,170</td>
<td align="right">-56.2%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_CLASS</td>
<td align="right">146,502,066</td>
<td align="right">64,327,345</td>
<td align="right">-56.1%</td>
</tr>
<tr>
<td align="left">BINARY_SLICE</td>
<td align="right">204,215,869</td>
<td align="right">92,745,624</td>
<td align="right">-54.6%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_LIST_INT</td>
<td align="right">99,797,992</td>
<td align="right">45,901,045</td>
<td align="right">-54.0%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">422,465,737</td>
<td align="right">194,345,158</td>
<td align="right">-54.0%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">135,645,058</td>
<td align="right">62,483,766</td>
<td align="right">-53.9%</td>
</tr>
<tr>
<td align="left">BINARY_OP_MULTIPLY_FLOAT</td>
<td align="right">190,327,519</td>
<td align="right">88,388,306</td>
<td align="right">-53.6%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_O</td>
<td align="right">523,084,618</td>
<td align="right">251,146,690</td>
<td align="right">-52.0%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">5,553,978,191</td>
<td align="right">2,714,643,126</td>
<td align="right">-51.1%</td>
</tr>
<tr>
<td align="left">DELETE_SUBSCR</td>
<td align="right">78,611,534</td>
<td align="right">38,566,777</td>
<td align="right">-50.9%</td>
</tr>
<tr>
<td align="left">STORE_GLOBAL</td>
<td align="right">6,944,168</td>
<td align="right">3,465,180</td>
<td align="right">-50.1%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_DICT</td>
<td align="right">107,006,642</td>
<td align="right">53,824,464</td>
<td align="right">-49.7%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">469,501,067</td>
<td align="right">238,603,117</td>
<td align="right">-49.2%</td>
</tr>
<tr>
<td align="left">STORE_FAST_LOAD_FAST</td>
<td align="right">35,839,839</td>
<td align="right">18,364,448</td>
<td align="right">-48.8%</td>
</tr>
<tr>
<td align="left">TO_BOOL_ALWAYS_TRUE</td>
<td align="right">172,239,844</td>
<td align="right">89,487,347</td>
<td align="right">-48.0%</td>
</tr>
<tr>
<td align="left">STORE_FAST_STORE_FAST</td>
<td align="right">395,441,788</td>
<td align="right">209,077,005</td>
<td align="right">-47.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_NO_DICT</td>
<td align="right">62,522,878</td>
<td align="right">33,348,580</td>
<td align="right">-46.7%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">2,657,818,745</td>
<td align="right">1,418,044,123</td>
<td align="right">-46.6%</td>
</tr>
<tr>
<td align="left">IS_OP</td>
<td align="right">414,462,103</td>
<td align="right">223,400,005</td>
<td align="right">-46.1%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">3,903,448,178</td>
<td align="right">2,104,677,691</td>
<td align="right">-46.1%</td>
</tr>
<tr>
<td align="left">TO_BOOL_INT</td>
<td align="right">115,941,652</td>
<td align="right">63,751,999</td>
<td align="right">-45.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">4,442,105,486</td>
<td align="right">2,515,528,269</td>
<td align="right">-43.4%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_FLOAT</td>
<td align="right">75,397,022</td>
<td align="right">42,867,720</td>
<td align="right">-43.1%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">313,838,691</td>
<td align="right">178,459,478</td>
<td align="right">-43.1%</td>
</tr>
<tr>
<td align="left">CALL_TYPE_1</td>
<td align="right">192,659,258</td>
<td align="right">110,581,038</td>
<td align="right">-42.6%</td>
</tr>
<tr>
<td align="left">BUILD_SET</td>
<td align="right">2,329,673</td>
<td align="right">1,337,846</td>
<td align="right">-42.6%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_PROPERTY</td>
<td align="right">58,936,636</td>
<td align="right">34,145,299</td>
<td align="right">-42.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">1,056,305,036</td>
<td align="right">616,708,876</td>
<td align="right">-41.6%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">73,413,349</td>
<td align="right">42,887,342</td>
<td align="right">-41.6%</td>
</tr>
<tr>
<td align="left">YIELD_VALUE</td>
<td align="right">1,348,815,936</td>
<td align="right">788,135,043</td>
<td align="right">-41.6%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR</td>
<td align="right">324,346,150</td>
<td align="right">191,040,620</td>
<td align="right">-41.1%</td>
</tr>
<tr>
<td align="left">CALL_LEN</td>
<td align="right">251,492,358</td>
<td align="right">149,382,989</td>
<td align="right">-40.6%</td>
</tr>
<tr>
<td align="left">STORE_DEREF</td>
<td align="right">94,893,850</td>
<td align="right">56,774,158</td>
<td align="right">-40.2%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR_METHOD</td>
<td align="right">126,487,106</td>
<td align="right">75,777,791</td>
<td align="right">-40.1%</td>
</tr>
<tr>
<td align="left">JUMP_FORWARD</td>
<td align="right">414,512,783</td>
<td align="right">248,410,886</td>
<td align="right">-40.1%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">409,412,408</td>
<td align="right">246,812,801</td>
<td align="right">-39.7%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">1,546,502</td>
<td align="right">2,156,978</td>
<td align="right">39.5%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">3,223,834,685</td>
<td align="right">1,951,536,611</td>
<td align="right">-39.5%</td>
</tr>
<tr>
<td align="left">BUILD_LIST</td>
<td align="right">165,460,303</td>
<td align="right">101,443,678</td>
<td align="right">-38.7%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">20,663,050,279</td>
<td align="right">12,674,094,397</td>
<td align="right">-38.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right">56,169,306</td>
<td align="right">34,490,114</td>
<td align="right">-38.6%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">2,375,110,327</td>
<td align="right">1,459,071,197</td>
<td align="right">-38.6%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">2,504,299,865</td>
<td align="right">1,541,474,220</td>
<td align="right">-38.4%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">454,303,373</td>
<td align="right">282,622,557</td>
<td align="right">-37.8%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">222,365,133</td>
<td align="right">140,405,618</td>
<td align="right">-36.9%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NONE</td>
<td align="right">361,478,176</td>
<td align="right">230,420,354</td>
<td align="right">-36.3%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NOT_NONE</td>
<td align="right">573,593,165</td>
<td align="right">368,995,643</td>
<td align="right">-35.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">1,413,162,716</td>
<td align="right">911,317,194</td>
<td align="right">-35.5%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_INT</td>
<td align="right">537,834,058</td>
<td align="right">350,572,225</td>
<td align="right">-34.8%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">4,789,551,931</td>
<td align="right">3,131,303,155</td>
<td align="right">-34.6%</td>
</tr>
<tr>
<td align="left">CALL_ISINSTANCE</td>
<td align="right">711,569,989</td>
<td align="right">469,071,026</td>
<td align="right">-34.1%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">5,214,705,764</td>
<td align="right">3,441,014,813</td>
<td align="right">-34.0%</td>
</tr>
<tr>
<td align="left">COPY_FREE_VARS</td>
<td align="right">286,512,235</td>
<td align="right">191,645,790</td>
<td align="right">-33.1%</td>
</tr>
<tr>
<td align="left">UNARY_NEGATIVE</td>
<td align="right">145,761,000</td>
<td align="right">97,559,841</td>
<td align="right">-33.1%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">602,735,173</td>
<td align="right">403,822,399</td>
<td align="right">-33.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">1,581,427,559</td>
<td align="right">1,061,782,172</td>
<td align="right">-32.9%</td>
</tr>
<tr>
<td align="left">TO_BOOL_LIST</td>
<td align="right">96,306,762</td>
<td align="right">64,939,675</td>
<td align="right">-32.6%</td>
</tr>
<tr>
<td align="left">CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">171,274,618</td>
<td align="right">115,650,145</td>
<td align="right">-32.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_CHECK</td>
<td align="right">10,796,301</td>
<td align="right">7,355,207</td>
<td align="right">-31.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">3,649,613,016</td>
<td align="right">2,500,327,812</td>
<td align="right">-31.5%</td>
</tr>
<tr>
<td align="left">LIST_APPEND</td>
<td align="right">99,250,825</td>
<td align="right">68,161,934</td>
<td align="right">-31.3%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">997,258,337</td>
<td align="right">685,188,241</td>
<td align="right">-31.3%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">58,731,501</td>
<td align="right">40,544,592</td>
<td align="right">-31.0%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">1,849,244,675</td>
<td align="right">1,285,533,216</td>
<td align="right">-30.5%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST</td>
<td align="right">331,993,683</td>
<td align="right">231,293,819</td>
<td align="right">-30.3%</td>
</tr>
<tr>
<td align="left">PUSH_NULL</td>
<td align="right">1,055,213,050</td>
<td align="right">736,138,361</td>
<td align="right">-30.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_AND_CLEAR</td>
<td align="right">75,393,415</td>
<td align="right">52,731,974</td>
<td align="right">-30.1%</td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">47,056,735</td>
<td align="right">33,221,116</td>
<td align="right">-29.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">629,113,021</td>
<td align="right">445,488,678</td>
<td align="right">-29.2%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_SLOT</td>
<td align="right">1,490,546,329</td>
<td align="right">1,068,255,295</td>
<td align="right">-28.3%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">3,357,560,178</td>
<td align="right">2,418,854,172</td>
<td align="right">-28.0%</td>
</tr>
<tr>
<td align="left">LIST_EXTEND</td>
<td align="right">25,710,890</td>
<td align="right">18,699,249</td>
<td align="right">-27.3%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST_WITH_KEYWORDS</td>
<td align="right">38,485,395</td>
<td align="right">28,441,236</td>
<td align="right">-26.1%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">206,607,769</td>
<td align="right">153,824,520</td>
<td align="right">-25.5%</td>
</tr>
<tr>
<td align="left">RETURN_GENERATOR</td>
<td align="right">365,448,252</td>
<td align="right">273,380,629</td>
<td align="right">-25.2%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">2,482,637,648</td>
<td align="right">1,859,614,973</td>
<td align="right">-25.1%</td>
</tr>
<tr>
<td align="left">GET_YIELD_FROM_ITER</td>
<td align="right">46,683,912</td>
<td align="right">35,187,600</td>
<td align="right">-24.6%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT</td>
<td align="right">1,163,155,371</td>
<td align="right">890,516,091</td>
<td align="right">-23.4%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_LIST_INT</td>
<td align="right">386,626,543</td>
<td align="right">296,559,063</td>
<td align="right">-23.3%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">6,106,116,910</td>
<td align="right">4,763,222,767</td>
<td align="right">-22.0%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST_WITH_KEYWORDS</td>
<td align="right">31,246,133</td>
<td align="right">24,429,747</td>
<td align="right">-21.8%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_TUPLE_INT</td>
<td align="right">174,164,247</td>
<td align="right">137,450,254</td>
<td align="right">-21.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_LAZY_DICT</td>
<td align="right">252,037,778</td>
<td align="right">200,482,817</td>
<td align="right">-20.5%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_INT</td>
<td align="right">378,953,552</td>
<td align="right">301,464,367</td>
<td align="right">-20.4%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">97,722,571</td>
<td align="right">78,120,940</td>
<td align="right">-20.1%</td>
</tr>
<tr>
<td align="left">CALL_STR_1</td>
<td align="right">31,215,689</td>
<td align="right">25,082,703</td>
<td align="right">-19.6%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR</td>
<td align="right">23,353</td>
<td align="right">19,006</td>
<td align="right">-18.6%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">229,616,746</td>
<td align="right">188,820,496</td>
<td align="right">-17.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_WITH_HINT</td>
<td align="right">304,037,023</td>
<td align="right">250,448,704</td>
<td align="right">-17.6%</td>
</tr>
<tr>
<td align="left">POP_EXCEPT</td>
<td align="right">16,927,662</td>
<td align="right">14,287,309</td>
<td align="right">-15.6%</td>
</tr>
<tr>
<td align="left">TO_BOOL_NONE</td>
<td align="right">421,145,738</td>
<td align="right">355,920,437</td>
<td align="right">-15.5%</td>
</tr>
<tr>
<td align="left">CALL_KW</td>
<td align="right">267,834,823</td>
<td align="right">228,679,178</td>
<td align="right">-14.6%</td>
</tr>
<tr>
<td align="left">BEFORE_WITH</td>
<td align="right">10,056,695</td>
<td align="right">8,607,865</td>
<td align="right">-14.4%</td>
</tr>
<tr>
<td align="left">CHECK_EXC_MATCH</td>
<td align="right">16,890,349</td>
<td align="right">14,623,773</td>
<td align="right">-13.4%</td>
</tr>
<tr>
<td align="left">PUSH_EXC_INFO</td>
<td align="right">16,935,432</td>
<td align="right">14,665,487</td>
<td align="right">-13.4%</td>
</tr>
<tr>
<td align="left">BUILD_MAP</td>
<td align="right">101,564,026</td>
<td align="right">88,728,661</td>
<td align="right">-12.6%</td>
</tr>
<tr>
<td align="left">RERAISE</td>
<td align="right">2,392,216</td>
<td align="right">2,112,717</td>
<td align="right">-11.7%</td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">313,379</td>
<td align="right">277,017</td>
<td align="right">-11.6%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_O</td>
<td align="right">271,577,153</td>
<td align="right">242,727,053</td>
<td align="right">-10.6%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_GETITEM</td>
<td align="right">54,066,091</td>
<td align="right">48,681,842</td>
<td align="right">-10.0%</td>
</tr>
<tr>
<td align="left">BUILD_CONST_KEY_MAP</td>
<td align="right">2,852,587</td>
<td align="right">2,577,131</td>
<td align="right">-9.7%</td>
</tr>
<tr>
<td align="left">IMPORT_FROM</td>
<td align="right">13,090,748</td>
<td align="right">11,838,198</td>
<td align="right">-9.6%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_UNICODE</td>
<td align="right">48,325,838</td>
<td align="right">43,779,221</td>
<td align="right">-9.4%</td>
</tr>
<tr>
<td align="left">DELETE_FAST</td>
<td align="right">2,231,862</td>
<td align="right">2,026,161</td>
<td align="right">-9.2%</td>
</tr>
<tr>
<td align="left">DICT_MERGE</td>
<td align="right">41,322,405</td>
<td align="right">37,762,573</td>
<td align="right">-8.6%</td>
</tr>
<tr>
<td align="left">IMPORT_NAME</td>
<td align="right">12,410,755</td>
<td align="right">11,383,736</td>
<td align="right">-8.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_MODULE</td>
<td align="right">506,562,787</td>
<td align="right">466,153,590</td>
<td align="right">-8.0%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR</td>
<td align="right">68,798,669</td>
<td align="right">63,434,256</td>
<td align="right">-7.8%</td>
</tr>
<tr>
<td align="left">END_SEND</td>
<td align="right">402,624,019</td>
<td align="right">375,100,006</td>
<td align="right">-6.8%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR_ATTR</td>
<td align="right">7,747,442</td>
<td align="right">7,218,601</td>
<td align="right">-6.8%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_FLOAT</td>
<td align="right">149,889,076</td>
<td align="right">140,344,503</td>
<td align="right">-6.4%</td>
</tr>
<tr>
<td align="left">CALL_LIST_APPEND</td>
<td align="right">293,758,779</td>
<td align="right">276,218,824</td>
<td align="right">-6.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_MULTIPLY_INT</td>
<td align="right">163,723,460</td>
<td align="right">154,245,787</td>
<td align="right">-5.8%</td>
</tr>
<tr>
<td align="left">SETUP_ANNOTATIONS</td>
<td align="right">1,524</td>
<td align="right">1,440</td>
<td align="right">-5.5%</td>
</tr>
<tr>
<td align="left">CALL_INTRINSIC_1</td>
<td align="right">151,431,512</td>
<td align="right">144,816,812</td>
<td align="right">-4.4%</td>
</tr>
<tr>
<td align="left">RAISE_VARARGS</td>
<td align="right">4,645,811</td>
<td align="right">4,468,373</td>
<td align="right">-3.8%</td>
</tr>
<tr>
<td align="left">UNARY_INVERT</td>
<td align="right">2,029,943</td>
<td align="right">2,105,376</td>
<td align="right">3.7%</td>
</tr>
<tr>
<td align="left">CALL_ALLOC_AND_ENTER_INIT</td>
<td align="right">93,467,212</td>
<td align="right">91,122,274</td>
<td align="right">-2.5%</td>
</tr>
<tr>
<td align="left">EXIT_INIT_CHECK</td>
<td align="right">93,414,105</td>
<td align="right">91,116,014</td>
<td align="right">-2.5%</td>
</tr>
<tr>
<td align="left">INTERPRETER_EXIT</td>
<td align="right">2,256,764,030</td>
<td align="right">2,204,999,750</td>
<td align="right">-2.3%</td>
</tr>
<tr>
<td align="left">WITH_EXCEPT_START</td>
<td align="right">233,386</td>
<td align="right">238,543</td>
<td align="right">2.2%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_WITH_HINT</td>
<td align="right">54,715,417</td>
<td align="right">53,533,824</td>
<td align="right">-2.2%</td>
</tr>
<tr>
<td align="left">CALL_FUNCTION_EX</td>
<td align="right">203,663,243</td>
<td align="right">199,428,963</td>
<td align="right">-2.1%</td>
</tr>
<tr>
<td align="left">LOAD_BUILD_CLASS</td>
<td align="right">24,340</td>
<td align="right">24,020</td>
<td align="right">-1.3%</td>
</tr>
<tr>
<td align="left">STORE_NAME</td>
<td align="right">548,554</td>
<td align="right">541,700</td>
<td align="right">-1.2%</td>
</tr>
<tr>
<td align="left">SET_UPDATE</td>
<td align="right">200,412</td>
<td align="right">202,660</td>
<td align="right">1.1%</td>
</tr>
<tr>
<td align="left">DELETE_NAME</td>
<td align="right">910</td>
<td align="right">900</td>
<td align="right">-1.1%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">20,711,906</td>
<td align="right">20,484,491</td>
<td align="right">-1.1%</td>
</tr>
<tr>
<td align="left">DICT_UPDATE</td>
<td align="right">72,046</td>
<td align="right">72,494</td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">GET_AWAITABLE</td>
<td align="right">229,150,440</td>
<td align="right">227,802,710</td>
<td align="right">-0.6%</td>
</tr>
<tr>
<td align="left">INSTRUMENTED_JUMP_BACKWARD</td>
<td align="right">6,244</td>
<td align="right">6,264</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">LOAD_FROM_DICT_OR_DEREF</td>
<td align="right">2,003</td>
<td align="right">2,000</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">LOAD_LOCALS</td>
<td align="right">2,023</td>
<td align="right">2,020</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">LOAD_NAME</td>
<td align="right">8,099,356</td>
<td align="right">8,095,340</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD_NO_INTERRUPT</td>
<td align="right">556,485,357</td>
<td align="right">556,296,066</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">SEND_GEN</td>
<td align="right">787,108,806</td>
<td align="right">786,882,117</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">CLEANUP_THROW</td>
<td align="right">152,071</td>
<td align="right">152,087</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">SEND</td>
<td align="right">173,840,844</td>
<td align="right">173,844,757</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BEFORE_ASYNC_WITH</td>
<td align="right">3,005,938</td>
<td align="right">3,005,980</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_PY_WITH_DEFAULTS</td>
<td align="right">180,846,939</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">INSTRUMENTED_RESUME</td>
<td align="right">38,855,260</td>
<td align="right">38,855,260</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">INSTRUMENTED_RETURN_VALUE</td>
<td align="right">38,851,520</td>
<td align="right">38,851,520</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">GET_ANEXT</td>
<td align="right">8,000,960</td>
<td align="right">8,000,960</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">END_ASYNC_FOR</td>
<td align="right">8,000,000</td>
<td align="right">8,000,000</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">GET_AITER</td>
<td align="right">8,000,000</td>
<td align="right">8,000,000</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">INSTRUMENTED_RETURN_CONST</td>
<td align="right">2,160</td>
<td align="right">2,160</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">INSTRUMENTED_JUMP_FORWARD</td>
<td align="right">1,040</td>
<td align="right">1,040</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_INTRINSIC_2</td>
<td align="right">80</td>
<td align="right">80</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_NON_PY_GENERAL</td>
<td align="right"></td>
<td align="right">581,811,006</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_PY_GENERAL</td>
<td align="right"></td>
<td align="right">145,435,610</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_BOUND_METHOD_GENERAL</td>
<td align="right"></td>
<td align="right">4,132,028</td>
<td align="right"></td>
</tr>
</tbody>
</table>


</details>

## Pair counts

<details>
<summary> Pair counts for top 100 opcode pairs </summary>


Pairs of specialized operations that deoptimize and are then followed by
the corresponding unspecialized instruction are not counted as pairs.

Not included in comparative output.


</details>

## Predecessor/Successor Pairs

<details>
<summary> Top 5 predecessors and successors of each Tier 1 opcode. </summary>


This does not include the unspecialized instructions that occur after a
specialized instruction deoptimizes.

Not included in comparative output.


</details>

## Specialization stats

<details>
<summary> Specialization stats by family </summary>

### BINARY_OP

<details>
<summary> specialization stats for BINARY_OP family </summary>

<table>
<thead>
<tr>
<th align="left">Kind</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">482,069,877</td>
<td align="right">25.1%</td>
<td align="right">301,274,794</td>
<td align="right">23.4%</td>
<td align="right">-37.5%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">29,508,379</td>
<td align="right">1.5%</td>
<td align="right">20,051,611</td>
<td align="right">1.6%</td>
<td align="right">-32.0%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">1,436,999,299</td>
<td align="right">74.8%</td>
<td align="right">982,946,096</td>
<td align="right">76.5%</td>
<td align="right">-31.6%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Success</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Success</td>
<td align="right">603,214</td>
<td align="right">34.6%</td>
<td align="right">420,071</td>
<td align="right">30.0%</td>
<td align="right">-30.4%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">1,138,661</td>
<td align="right">65.4%</td>
<td align="right">979,303</td>
<td align="right">70.0%</td>
<td align="right">-14.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Failure kind</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">add different types</td>
<td align="right">39,653</td>
<td align="right">3.5%</td>
<td align="right">12,958</td>
<td align="right">1.3%</td>
<td align="right">-67.3%</td>
</tr>
<tr>
<td align="left">multiply other</td>
<td align="right">5,220</td>
<td align="right">0.5%</td>
<td align="right">2,658</td>
<td align="right">0.3%</td>
<td align="right">-49.1%</td>
</tr>
<tr>
<td align="left">add other</td>
<td align="right">55,147</td>
<td align="right">4.8%</td>
<td align="right">28,126</td>
<td align="right">2.9%</td>
<td align="right">-49.0%</td>
</tr>
<tr>
<td align="left">lshift</td>
<td align="right">5,824</td>
<td align="right">0.5%</td>
<td align="right">3,349</td>
<td align="right">0.3%</td>
<td align="right">-42.5%</td>
</tr>
<tr>
<td align="left">multiply different types</td>
<td align="right">87,606</td>
<td align="right">7.7%</td>
<td align="right">55,693</td>
<td align="right">5.7%</td>
<td align="right">-36.4%</td>
</tr>
<tr>
<td align="left">power</td>
<td align="right">5,715</td>
<td align="right">0.5%</td>
<td align="right">3,909</td>
<td align="right">0.4%</td>
<td align="right">-31.6%</td>
</tr>
<tr>
<td align="left">or</td>
<td align="right">15,985</td>
<td align="right">1.4%</td>
<td align="right">11,865</td>
<td align="right">1.2%</td>
<td align="right">-25.8%</td>
</tr>
<tr>
<td align="left">subtract other</td>
<td align="right">11,534</td>
<td align="right">1.0%</td>
<td align="right">8,921</td>
<td align="right">0.9%</td>
<td align="right">-22.7%</td>
</tr>
<tr>
<td align="left">and different types</td>
<td align="right">542</td>
<td align="right">0.0%</td>
<td align="right">420</td>
<td align="right">0.0%</td>
<td align="right">-22.5%</td>
</tr>
<tr>
<td align="left">xor</td>
<td align="right">8,843</td>
<td align="right">0.8%</td>
<td align="right">6,883</td>
<td align="right">0.7%</td>
<td align="right">-22.2%</td>
</tr>
<tr>
<td align="left">true divide float</td>
<td align="right">5,762</td>
<td align="right">0.5%</td>
<td align="right">4,503</td>
<td align="right">0.5%</td>
<td align="right">-21.9%</td>
</tr>
<tr>
<td align="left">true divide other</td>
<td align="right">3,404</td>
<td align="right">0.3%</td>
<td align="right">2,954</td>
<td align="right">0.3%</td>
<td align="right">-13.2%</td>
</tr>
<tr>
<td align="left">and int</td>
<td align="right">35,849</td>
<td align="right">3.1%</td>
<td align="right">31,711</td>
<td align="right">3.2%</td>
<td align="right">-11.5%</td>
</tr>
<tr>
<td align="left">remainder</td>
<td align="right">18,560</td>
<td align="right">1.6%</td>
<td align="right">17,154</td>
<td align="right">1.8%</td>
<td align="right">-7.6%</td>
</tr>
<tr>
<td align="left">floor divide</td>
<td align="right">33,038</td>
<td align="right">2.9%</td>
<td align="right">30,772</td>
<td align="right">3.1%</td>
<td align="right">-6.9%</td>
</tr>
<tr>
<td align="left">subtract different types</td>
<td align="right">782,454</td>
<td align="right">68.7%</td>
<td align="right">734,732</td>
<td align="right">75.0%</td>
<td align="right">-6.1%</td>
</tr>
<tr>
<td align="left">true divide different types</td>
<td align="right">12,512</td>
<td align="right">1.1%</td>
<td align="right">12,022</td>
<td align="right">1.2%</td>
<td align="right">-3.9%</td>
</tr>
<tr>
<td align="left">rshift</td>
<td align="right">8,993</td>
<td align="right">0.8%</td>
<td align="right">8,698</td>
<td align="right">0.9%</td>
<td align="right">-3.3%</td>
</tr>
<tr>
<td align="left">and other</td>
<td align="right">2,020</td>
<td align="right">0.2%</td>
<td align="right">1,975</td>
<td align="right">0.2%</td>
<td align="right">-2.2%</td>
</tr>
</tbody>
</table>


</details>

### BINARY_SLICE

<details>
<summary> specialization stats for BINARY_SLICE family </summary>


</details>

### BINARY_SUBSCR

<details>
<summary> specialization stats for BINARY_SUBSCR family </summary>

<table>
<thead>
<tr>
<th align="left">Kind</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">1,372,174,554</td>
<td align="right">80.8%</td>
<td align="right">645,934,845</td>
<td align="right">77.0%</td>
<td align="right">-52.9%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">325,951,011</td>
<td align="right">19.2%</td>
<td align="right">192,580,294</td>
<td align="right">23.0%</td>
<td align="right">-40.9%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">1,887,421</td>
<td align="right">0.1%</td>
<td align="right">1,755,245</td>
<td align="right">0.2%</td>
<td align="right">-7.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Success</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Failure</td>
<td align="right">148,326</td>
<td align="right">52.5%</td>
<td align="right">96,079</td>
<td align="right">44.6%</td>
<td align="right">-35.2%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">134,234</td>
<td align="right">47.5%</td>
<td align="right">119,492</td>
<td align="right">55.4%</td>
<td align="right">-11.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Failure kind</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">code complex parameters</td>
<td align="right">4,935</td>
<td align="right">3.3%</td>
<td align="right">1,640</td>
<td align="right">1.7%</td>
<td align="right">-66.8%</td>
</tr>
<tr>
<td align="left">buffer int</td>
<td align="right">22,661</td>
<td align="right">15.3%</td>
<td align="right">10,283</td>
<td align="right">10.7%</td>
<td align="right">-54.6%</td>
</tr>
<tr>
<td align="left">out of range</td>
<td align="right">58,179</td>
<td align="right">39.2%</td>
<td align="right">30,440</td>
<td align="right">31.7%</td>
<td align="right">-47.7%</td>
</tr>
<tr>
<td align="left">tuple slice</td>
<td align="right">182</td>
<td align="right">0.1%</td>
<td align="right">123</td>
<td align="right">0.1%</td>
<td align="right">-32.4%</td>
</tr>
<tr>
<td align="left">array int</td>
<td align="right">16,200</td>
<td align="right">10.9%</td>
<td align="right">13,220</td>
<td align="right">13.8%</td>
<td align="right">-18.4%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">39,604</td>
<td align="right">26.7%</td>
<td align="right">33,933</td>
<td align="right">35.3%</td>
<td align="right">-14.3%</td>
</tr>
<tr>
<td align="left">buffer slice</td>
<td align="right">842</td>
<td align="right">0.6%</td>
<td align="right">760</td>
<td align="right">0.8%</td>
<td align="right">-9.7%</td>
</tr>
<tr>
<td align="left">list slice</td>
<td align="right">1,323</td>
<td align="right">0.9%</td>
<td align="right">1,280</td>
<td align="right">1.3%</td>
<td align="right">-3.3%</td>
</tr>
<tr>
<td align="left">sequence int</td>
<td align="right">4,300</td>
<td align="right">2.9%</td>
<td align="right">4,300</td>
<td align="right">4.5%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">string slice</td>
<td align="right">100</td>
<td align="right">0.1%</td>
<td align="right">100</td>
<td align="right">0.1%</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### CALL

<details>
<summary> specialization stats for CALL family </summary>

<table>
<thead>
<tr>
<th align="left">Kind</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">1,349,624,072</td>
<td align="right">17.6%</td>
<td align="right">283,962,586</td>
<td align="right">6.8%</td>
<td align="right">-79.0%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">6,300,676,901</td>
<td align="right">82.3%</td>
<td align="right">3,914,093,712</td>
<td align="right">93.2%</td>
<td align="right">-37.9%</td>
</tr>
<tr>
<td align="left">
deopt
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">28,860</td>
<td align="right">0.0%</td>
<td align="right">20,080</td>
<td align="right">0.0%</td>
<td align="right">-30.4%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">223,301,919</td>
<td align="right">2.9%</td>
<td align="right">159,921,144</td>
<td align="right">3.8%</td>
<td align="right">-28.4%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Success</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Failure</td>
<td align="right">906,720</td>
<td align="right">15.9%</td>
<td align="right">95,696</td>
<td align="right">2.6%</td>
<td align="right">-89.4%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">4,792,254</td>
<td align="right">84.1%</td>
<td align="right">3,588,605</td>
<td align="right">97.4%</td>
<td align="right">-25.1%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Failure kind</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">init not python</td>
<td align="right">13,061</td>
<td align="right">1.4%</td>
<td align="right">200</td>
<td align="right">0.2%</td>
<td align="right">-98.5%</td>
</tr>
<tr>
<td align="left">init not inline values</td>
<td align="right">105,557</td>
<td align="right">11.6%</td>
<td align="right">3,480</td>
<td align="right">3.6%</td>
<td align="right">-96.7%</td>
</tr>
<tr>
<td align="left">init not simple</td>
<td align="right">4,824</td>
<td align="right">0.5%</td>
<td align="right">680</td>
<td align="right">0.7%</td>
<td align="right">-85.9%</td>
</tr>
<tr>
<td align="left">out of versions</td>
<td align="right">981</td>
<td align="right">0.1%</td>
<td align="right">1,060</td>
<td align="right">1.1%</td>
<td align="right">8.1%</td>
</tr>
<tr>
<td align="left">class no vectorcall</td>
<td align="right">88,692</td>
<td align="right">9.8%</td>
<td align="right">82,776</td>
<td align="right">86.5%</td>
<td align="right">-6.7%</td>
</tr>
<tr>
<td align="left">wrong number arguments</td>
<td align="right">12,662</td>
<td align="right">1.4%</td>
<td align="right">11,860</td>
<td align="right">12.4%</td>
<td align="right">-6.3%</td>
</tr>
<tr>
<td align="left">meth descr method fastcall keywords</td>
<td align="right">196,449</td>
<td align="right">21.7%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">code complex parameters</td>
<td align="right">172,203</td>
<td align="right">19.0%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">cfunc noargs</td>
<td align="right">68,850</td>
<td align="right">7.6%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">62,623</td>
<td align="right">6.9%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">metaclass</td>
<td align="right">42,302</td>
<td align="right">4.7%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">cfunc varargs keywords</td>
<td align="right">30,711</td>
<td align="right">3.4%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">class mutable</td>
<td align="right">22,226</td>
<td align="right">2.5%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">meth descr varargs keywords</td>
<td align="right">17,386</td>
<td align="right">1.9%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">cfunc varargs</td>
<td align="right">13,658</td>
<td align="right">1.5%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">cmethod</td>
<td align="right">12,635</td>
<td align="right">1.4%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">meth descr varargs</td>
<td align="right">12,347</td>
<td align="right">1.4%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">bound method</td>
<td align="right">11,477</td>
<td align="right">1.3%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">operator wrapper</td>
<td align="right">10,006</td>
<td align="right">1.1%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">method wrapper</td>
<td align="right">8,231</td>
<td align="right">0.9%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
</tbody>
</table>


</details>

### COMPARE_OP

<details>
<summary> specialization stats for COMPARE_OP family </summary>

<table>
<thead>
<tr>
<th align="left">Kind</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">136,772,478</td>
<td align="right">7.8%</td>
<td align="right">63,034,428</td>
<td align="right">5.3%</td>
<td align="right">-53.9%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">1,433,285</td>
<td align="right">0.1%</td>
<td align="right">755,637</td>
<td align="right">0.1%</td>
<td align="right">-47.3%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">1,616,900,273</td>
<td align="right">92.2%</td>
<td align="right">1,122,739,150</td>
<td align="right">94.7%</td>
<td align="right">-30.6%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Success</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Failure</td>
<td align="right">206,380</td>
<td align="right">67.5%</td>
<td align="right">130,056</td>
<td align="right">63.4%</td>
<td align="right">-37.0%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">99,485</td>
<td align="right">32.5%</td>
<td align="right">74,919</td>
<td align="right">36.6%</td>
<td align="right">-24.7%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Failure kind</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">big int</td>
<td align="right">62,749</td>
<td align="right">30.4%</td>
<td align="right">27,076</td>
<td align="right">20.8%</td>
<td align="right">-56.9%</td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">3,574</td>
<td align="right">1.7%</td>
<td align="right">1,660</td>
<td align="right">1.3%</td>
<td align="right">-53.6%</td>
</tr>
<tr>
<td align="left">bool</td>
<td align="right">3,814</td>
<td align="right">1.8%</td>
<td align="right">1,786</td>
<td align="right">1.4%</td>
<td align="right">-53.2%</td>
</tr>
<tr>
<td align="left">baseobject</td>
<td align="right">32,311</td>
<td align="right">15.7%</td>
<td align="right">18,420</td>
<td align="right">14.2%</td>
<td align="right">-43.0%</td>
</tr>
<tr>
<td align="left">float long</td>
<td align="right">15,976</td>
<td align="right">7.7%</td>
<td align="right">10,450</td>
<td align="right">8.0%</td>
<td align="right">-34.6%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">21,731</td>
<td align="right">10.5%</td>
<td align="right">14,896</td>
<td align="right">11.5%</td>
<td align="right">-31.5%</td>
</tr>
<tr>
<td align="left">bytes</td>
<td align="right">3,861</td>
<td align="right">1.9%</td>
<td align="right">2,760</td>
<td align="right">2.1%</td>
<td align="right">-28.5%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">14,030</td>
<td align="right">6.8%</td>
<td align="right">10,247</td>
<td align="right">7.9%</td>
<td align="right">-27.0%</td>
</tr>
<tr>
<td align="left">different types</td>
<td align="right">33,534</td>
<td align="right">16.2%</td>
<td align="right">28,541</td>
<td align="right">21.9%</td>
<td align="right">-14.9%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">2,343</td>
<td align="right">1.1%</td>
<td align="right">2,060</td>
<td align="right">1.6%</td>
<td align="right">-12.1%</td>
</tr>
<tr>
<td align="left">long float</td>
<td align="right">1,537</td>
<td align="right">0.7%</td>
<td align="right">1,480</td>
<td align="right">1.1%</td>
<td align="right">-3.7%</td>
</tr>
<tr>
<td align="left">string</td>
<td align="right">10,920</td>
<td align="right">5.3%</td>
<td align="right">10,680</td>
<td align="right">8.2%</td>
<td align="right">-2.2%</td>
</tr>
</tbody>
</table>


</details>

### CONTAINS_OP

<details>
<summary> specialization stats for CONTAINS_OP family </summary>

<table>
<thead>
<tr>
<th align="left">Kind</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">411,337,809</td>
<td align="right">84.4%</td>
<td align="right">81,458,133</td>
<td align="right">64.2%</td>
<td align="right">-80.2%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">75,758,198</td>
<td align="right">15.5%</td>
<td align="right">45,264,988</td>
<td align="right">35.7%</td>
<td align="right">-40.3%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">2,517,260</td>
<td align="right">0.5%</td>
<td align="right">2,517,260</td>
<td align="right">2.0%</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Success</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Failure</td>
<td align="right">107,137</td>
<td align="right">62.1%</td>
<td align="right">78,073</td>
<td align="right">55.9%</td>
<td align="right">-27.1%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">65,274</td>
<td align="right">37.9%</td>
<td align="right">61,541</td>
<td align="right">44.1%</td>
<td align="right">-5.7%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Failure kind</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">list</td>
<td align="right">13,934</td>
<td align="right">13.0%</td>
<td align="right">8,879</td>
<td align="right">11.4%</td>
<td align="right">-36.3%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">41,357</td>
<td align="right">38.6%</td>
<td align="right">29,028</td>
<td align="right">37.2%</td>
<td align="right">-29.8%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">25,056</td>
<td align="right">23.4%</td>
<td align="right">18,286</td>
<td align="right">23.4%</td>
<td align="right">-27.0%</td>
</tr>
<tr>
<td align="left">str</td>
<td align="right">26,790</td>
<td align="right">25.0%</td>
<td align="right">21,880</td>
<td align="right">28.0%</td>
<td align="right">-18.3%</td>
</tr>
</tbody>
</table>


</details>

### FOR_ITER

<details>
<summary> specialization stats for FOR_ITER family </summary>

<table>
<thead>
<tr>
<th align="left">Kind</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">551,019</td>
<td align="right">0.1%</td>
<td align="right">229,745</td>
<td align="right">0.1%</td>
<td align="right">-58.3%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">412,232,864</td>
<td align="right">80.7%</td>
<td align="right">217,613,723</td>
<td align="right">73.5%</td>
<td align="right">-47.2%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">98,049,392</td>
<td align="right">19.2%</td>
<td align="right">78,173,780</td>
<td align="right">26.4%</td>
<td align="right">-20.3%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Success</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Success</td>
<td align="right">72,232</td>
<td align="right">32.2%</td>
<td align="right">54,570</td>
<td align="right">30.8%</td>
<td align="right">-24.5%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">151,966</td>
<td align="right">67.8%</td>
<td align="right">122,335</td>
<td align="right">69.2%</td>
<td align="right">-19.5%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Failure kind</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">reversed list</td>
<td align="right">7,673</td>
<td align="right">5.0%</td>
<td align="right">3,980</td>
<td align="right">3.3%</td>
<td align="right">-48.1%</td>
</tr>
<tr>
<td align="left">zip</td>
<td align="right">14,237</td>
<td align="right">9.4%</td>
<td align="right">8,580</td>
<td align="right">7.0%</td>
<td align="right">-39.7%</td>
</tr>
<tr>
<td align="left">enumerate</td>
<td align="right">17,940</td>
<td align="right">11.8%</td>
<td align="right">11,409</td>
<td align="right">9.3%</td>
<td align="right">-36.4%</td>
</tr>
<tr>
<td align="left">ascii string</td>
<td align="right">2,202</td>
<td align="right">1.4%</td>
<td align="right">1,540</td>
<td align="right">1.3%</td>
<td align="right">-30.1%</td>
</tr>
<tr>
<td align="left">dict keys</td>
<td align="right">13,832</td>
<td align="right">9.1%</td>
<td align="right">9,840</td>
<td align="right">8.0%</td>
<td align="right">-28.9%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">22,307</td>
<td align="right">14.7%</td>
<td align="right">18,297</td>
<td align="right">15.0%</td>
<td align="right">-18.0%</td>
</tr>
<tr>
<td align="left">dict values</td>
<td align="right">6,095</td>
<td align="right">4.0%</td>
<td align="right">5,440</td>
<td align="right">4.4%</td>
<td align="right">-10.7%</td>
</tr>
<tr>
<td align="left">dict items</td>
<td align="right">46,105</td>
<td align="right">30.3%</td>
<td align="right">41,391</td>
<td align="right">33.8%</td>
<td align="right">-10.2%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">10,884</td>
<td align="right">7.2%</td>
<td align="right">11,639</td>
<td align="right">9.5%</td>
<td align="right">6.9%</td>
</tr>
<tr>
<td align="left">itertools</td>
<td align="right">7,258</td>
<td align="right">4.8%</td>
<td align="right">6,900</td>
<td align="right">5.6%</td>
<td align="right">-4.9%</td>
</tr>
<tr>
<td align="left">seq iter</td>
<td align="right">2,054</td>
<td align="right">1.4%</td>
<td align="right">1,960</td>
<td align="right">1.6%</td>
<td align="right">-4.6%</td>
</tr>
<tr>
<td align="left">map</td>
<td align="right">569</td>
<td align="right">0.4%</td>
<td align="right">560</td>
<td align="right">0.5%</td>
<td align="right">-1.6%</td>
</tr>
<tr>
<td align="left">bytes</td>
<td align="right">527</td>
<td align="right">0.3%</td>
<td align="right">519</td>
<td align="right">0.4%</td>
<td align="right">-1.5%</td>
</tr>
<tr>
<td align="left">callable</td>
<td align="right">282</td>
<td align="right">0.2%</td>
<td align="right">280</td>
<td align="right">0.2%</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">string</td>
<td align="right">1</td>
<td align="right">0.0%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
</tbody>
</table>


</details>

### LOAD_ATTR

<details>
<summary> specialization stats for LOAD_ATTR family </summary>

<table>
<thead>
<tr>
<th align="left">Kind</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">310,545,016</td>
<td align="right">3.2%</td>
<td align="right">154,526,488</td>
<td align="right">2.3%</td>
<td align="right">-50.2%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">932,123,653</td>
<td align="right">9.6%</td>
<td align="right">595,714,422</td>
<td align="right">9.0%</td>
<td align="right">-36.1%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">8,761,140,647</td>
<td align="right">90.3%</td>
<td align="right">5,993,895,290</td>
<td align="right">90.9%</td>
<td align="right">-31.6%</td>
</tr>
<tr>
<td align="left">
deopt
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">679,367</td>
<td align="right">0.0%</td>
<td align="right">490,451</td>
<td align="right">0.0%</td>
<td align="right">-27.8%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Success</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Success</td>
<td align="right">6,664,358</td>
<td align="right">88.5%</td>
<td align="right">3,570,598</td>
<td align="right">83.0%</td>
<td align="right">-46.4%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">870,026</td>
<td align="right">11.5%</td>
<td align="right">730,146</td>
<td align="right">17.0%</td>
<td align="right">-16.1%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Failure kind</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">out of versions</td>
<td align="right">1,910</td>
<td align="right">0.2%</td>
<td align="right">20</td>
<td align="right">0.0%</td>
<td align="right">-99.0%</td>
</tr>
<tr>
<td align="left">non overriding descriptor</td>
<td align="right">13,280</td>
<td align="right">1.5%</td>
<td align="right">7,158</td>
<td align="right">1.0%</td>
<td align="right">-46.1%</td>
</tr>
<tr>
<td align="left">shadowed</td>
<td align="right">91,503</td>
<td align="right">10.5%</td>
<td align="right">51,012</td>
<td align="right">7.0%</td>
<td align="right">-44.3%</td>
</tr>
<tr>
<td align="left">not in dict</td>
<td align="right">320</td>
<td align="right">0.0%</td>
<td align="right">200</td>
<td align="right">0.0%</td>
<td align="right">-37.5%</td>
</tr>
<tr>
<td align="left">class method obj</td>
<td align="right">20,000</td>
<td align="right">2.3%</td>
<td align="right">14,920</td>
<td align="right">2.0%</td>
<td align="right">-25.4%</td>
</tr>
<tr>
<td align="left">class attr simple</td>
<td align="right">53,186</td>
<td align="right">6.1%</td>
<td align="right">41,282</td>
<td align="right">5.7%</td>
<td align="right">-22.4%</td>
</tr>
<tr>
<td align="left">builtin class method</td>
<td align="right">3,581</td>
<td align="right">0.4%</td>
<td align="right">2,800</td>
<td align="right">0.4%</td>
<td align="right">-21.8%</td>
</tr>
<tr>
<td align="left">not managed dict</td>
<td align="right">233,200</td>
<td align="right">26.8%</td>
<td align="right">189,606</td>
<td align="right">26.0%</td>
<td align="right">-18.7%</td>
</tr>
<tr>
<td align="left">module attr not found</td>
<td align="right">17,356</td>
<td align="right">2.0%</td>
<td align="right">15,280</td>
<td align="right">2.1%</td>
<td align="right">-12.0%</td>
</tr>
<tr>
<td align="left">method</td>
<td align="right">104,510</td>
<td align="right">12.0%</td>
<td align="right">95,574</td>
<td align="right">13.1%</td>
<td align="right">-8.6%</td>
</tr>
<tr>
<td align="left">metaclass attribute</td>
<td align="right">170,886</td>
<td align="right">19.6%</td>
<td align="right">157,321</td>
<td align="right">21.5%</td>
<td align="right">-7.9%</td>
</tr>
<tr>
<td align="left">not in keys</td>
<td align="right">15,840</td>
<td align="right">1.8%</td>
<td align="right">14,590</td>
<td align="right">2.0%</td>
<td align="right">-7.9%</td>
</tr>
<tr>
<td align="left">mutable class</td>
<td align="right">75,292</td>
<td align="right">8.7%</td>
<td align="right">72,482</td>
<td align="right">9.9%</td>
<td align="right">-3.7%</td>
</tr>
<tr>
<td align="left">class attr descriptor</td>
<td align="right">29,018</td>
<td align="right">3.3%</td>
<td align="right">28,400</td>
<td align="right">3.9%</td>
<td align="right">-2.1%</td>
</tr>
<tr>
<td align="left">overridden</td>
<td align="right">15,088</td>
<td align="right">1.7%</td>
<td align="right">14,785</td>
<td align="right">2.0%</td>
<td align="right">-2.0%</td>
</tr>
<tr>
<td align="left">wrong number arguments</td>
<td align="right">1,100</td>
<td align="right">0.1%</td>
<td align="right">1,080</td>
<td align="right">0.1%</td>
<td align="right">-1.8%</td>
</tr>
<tr>
<td align="left">non string or split</td>
<td align="right">20,216</td>
<td align="right">2.3%</td>
<td align="right">19,892</td>
<td align="right">2.7%</td>
<td align="right">-1.6%</td>
</tr>
<tr>
<td align="left">non object slot</td>
<td align="right">3,380</td>
<td align="right">0.4%</td>
<td align="right">3,384</td>
<td align="right">0.5%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">no dict</td>
<td align="right">300</td>
<td align="right">0.0%</td>
<td align="right">300</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">property</td>
<td align="right">60</td>
<td align="right">0.0%</td>
<td align="right">60</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### LOAD_GLOBAL

<details>
<summary> specialization stats for LOAD_GLOBAL family </summary>

<table>
<thead>
<tr>
<th align="left">Kind</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">5,598,515,651</td>
<td align="right">99.6%</td>
<td align="right">3,410,183,297</td>
<td align="right">99.4%</td>
<td align="right">-39.1%</td>
</tr>
<tr>
<td align="left">
deopt
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">11,926</td>
<td align="right">0.0%</td>
<td align="right">11,760</td>
<td align="right">0.0%</td>
<td align="right">-1.4%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">429,361</td>
<td align="right">0.0%</td>
<td align="right">424,511</td>
<td align="right">0.0%</td>
<td align="right">-1.1%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">20,503,962</td>
<td align="right">0.4%</td>
<td align="right">20,385,245</td>
<td align="right">0.6%</td>
<td align="right">-0.6%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Success</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Success</td>
<td align="right">637,305</td>
<td align="right">100.0%</td>
<td align="right">523,757</td>
<td align="right">100.0%</td>
<td align="right">-17.8%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right"></td>
</tr>
</tbody>
</table>


</details>

### LOAD_SUPER_ATTR

<details>
<summary> specialization stats for LOAD_SUPER_ATTR family </summary>

<table>
<thead>
<tr>
<th align="left">Kind</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">134,234,548</td>
<td align="right">100.0%</td>
<td align="right">82,996,392</td>
<td align="right">100.0%</td>
<td align="right">-38.2%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">11,731</td>
<td align="right">0.0%</td>
<td align="right">9,586</td>
<td align="right">0.0%</td>
<td align="right">-18.3%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Success</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Success</td>
<td align="right">11,622</td>
<td align="right">100.0%</td>
<td align="right">9,420</td>
<td align="right">100.0%</td>
<td align="right">-18.9%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right"></td>
</tr>
</tbody>
</table>


</details>

### POP_JUMP_IF_FALSE

<details>
<summary> specialization stats for POP_JUMP_IF_FALSE family </summary>


</details>

### POP_JUMP_IF_NONE

<details>
<summary> specialization stats for POP_JUMP_IF_NONE family </summary>


</details>

### POP_JUMP_IF_NOT_NONE

<details>
<summary> specialization stats for POP_JUMP_IF_NOT_NONE family </summary>


</details>

### POP_JUMP_IF_TRUE

<details>
<summary> specialization stats for POP_JUMP_IF_TRUE family </summary>


</details>

### SEND

<details>
<summary> specialization stats for SEND family </summary>

<table>
<thead>
<tr>
<th align="left">Kind</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">787,077,906</td>
<td align="right">81.9%</td>
<td align="right">786,851,217</td>
<td align="right">81.9%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">173,802,912</td>
<td align="right">18.1%</td>
<td align="right">173,806,838</td>
<td align="right">18.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">30,900</td>
<td align="right">0.0%</td>
<td align="right">30,900</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Success</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Success</td>
<td align="right">7,101</td>
<td align="right">10.3%</td>
<td align="right">7,092</td>
<td align="right">10.3%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">61,731</td>
<td align="right">89.7%</td>
<td align="right">61,727</td>
<td align="right">89.7%</td>
<td align="right">-0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Failure kind</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">other</td>
<td align="right">16,130</td>
<td align="right">26.1%</td>
<td align="right">16,127</td>
<td align="right">26.1%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">9,961</td>
<td align="right">16.1%</td>
<td align="right">9,960</td>
<td align="right">16.1%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">async generator send</td>
<td align="right">33,180</td>
<td align="right">53.7%</td>
<td align="right">33,180</td>
<td align="right">53.8%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">2,220</td>
<td align="right">3.6%</td>
<td align="right">2,220</td>
<td align="right">3.6%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">dict keys</td>
<td align="right">240</td>
<td align="right">0.4%</td>
<td align="right">240</td>
<td align="right">0.4%</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### STORE_ATTR

<details>
<summary> specialization stats for STORE_ATTR family </summary>

<table>
<thead>
<tr>
<th align="left">Kind</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">139,656,702</td>
<td align="right">5.4%</td>
<td align="right">41,902,116</td>
<td align="right">2.3%</td>
<td align="right">-70.0%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">183,822,374</td>
<td align="right">7.1%</td>
<td align="right">74,111,595</td>
<td align="right">4.0%</td>
<td align="right">-59.7%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">2,402,863,381</td>
<td align="right">92.8%</td>
<td align="right">1,765,075,244</td>
<td align="right">95.9%</td>
<td align="right">-26.5%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Success</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Success</td>
<td align="right">2,774,834</td>
<td align="right">96.0%</td>
<td align="right">912,813</td>
<td align="right">90.2%</td>
<td align="right">-67.1%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">116,229</td>
<td align="right">4.0%</td>
<td align="right">98,824</td>
<td align="right">9.8%</td>
<td align="right">-15.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Failure kind</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">class attr simple</td>
<td align="right">25,928</td>
<td align="right">22.3%</td>
<td align="right">11,344</td>
<td align="right">11.5%</td>
<td align="right">-56.2%</td>
</tr>
<tr>
<td align="left">not in dict</td>
<td align="right">12,647</td>
<td align="right">10.9%</td>
<td align="right">7,780</td>
<td align="right">7.9%</td>
<td align="right">-38.5%</td>
</tr>
<tr>
<td align="left">not managed dict</td>
<td align="right">28,506</td>
<td align="right">24.5%</td>
<td align="right">35,106</td>
<td align="right">35.5%</td>
<td align="right">23.2%</td>
</tr>
<tr>
<td align="left">overriding descriptor</td>
<td align="right">10,641</td>
<td align="right">9.2%</td>
<td align="right">8,383</td>
<td align="right">8.5%</td>
<td align="right">-21.2%</td>
</tr>
<tr>
<td align="left">not in keys</td>
<td align="right">5,207</td>
<td align="right">4.5%</td>
<td align="right">4,360</td>
<td align="right">4.4%</td>
<td align="right">-16.3%</td>
</tr>
<tr>
<td align="left">overridden</td>
<td align="right">6,569</td>
<td align="right">5.7%</td>
<td align="right">6,060</td>
<td align="right">6.1%</td>
<td align="right">-7.7%</td>
</tr>
<tr>
<td align="left">property</td>
<td align="right">4,987</td>
<td align="right">4.3%</td>
<td align="right">5,340</td>
<td align="right">5.4%</td>
<td align="right">7.1%</td>
</tr>
<tr>
<td align="left">no dict</td>
<td align="right">5,009</td>
<td align="right">4.3%</td>
<td align="right">4,743</td>
<td align="right">4.8%</td>
<td align="right">-5.3%</td>
</tr>
<tr>
<td align="left">non string or split</td>
<td align="right">14,601</td>
<td align="right">12.6%</td>
<td align="right">14,168</td>
<td align="right">14.3%</td>
<td align="right">-3.0%</td>
</tr>
<tr>
<td align="left">method</td>
<td align="right">1,500</td>
<td align="right">1.3%</td>
<td align="right">1,500</td>
<td align="right">1.5%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">out of versions</td>
<td align="right">594</td>
<td align="right">0.5%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">mutable class</td>
<td align="right">40</td>
<td align="right">0.0%</td>
<td align="right">40</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### STORE_SLICE

<details>
<summary> specialization stats for STORE_SLICE family </summary>


</details>

### STORE_SUBSCR

<details>
<summary> specialization stats for STORE_SUBSCR family </summary>

<table>
<thead>
<tr>
<th align="left">Kind</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">206,804,596</td>
<td align="right">75.0%</td>
<td align="right">99,725,509</td>
<td align="right">61.1%</td>
<td align="right">-51.8%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">68,723,649</td>
<td align="right">24.9%</td>
<td align="right">63,363,777</td>
<td align="right">38.8%</td>
<td align="right">-7.8%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">38</td>
<td align="right">0.0%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Success</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Success</td>
<td align="right">16,514</td>
<td align="right">22.0%</td>
<td align="right">15,146</td>
<td align="right">21.5%</td>
<td align="right">-8.3%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">58,544</td>
<td align="right">78.0%</td>
<td align="right">55,333</td>
<td align="right">78.5%</td>
<td align="right">-5.5%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Failure kind</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">out of range</td>
<td align="right">1,315</td>
<td align="right">2.2%</td>
<td align="right">800</td>
<td align="right">1.4%</td>
<td align="right">-39.2%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">1,870</td>
<td align="right">3.2%</td>
<td align="right">2,320</td>
<td align="right">4.2%</td>
<td align="right">24.1%</td>
</tr>
<tr>
<td align="left">dict subclass no override</td>
<td align="right">12,516</td>
<td align="right">21.4%</td>
<td align="right">11,156</td>
<td align="right">20.2%</td>
<td align="right">-10.9%</td>
</tr>
<tr>
<td align="left">array int</td>
<td align="right">6,480</td>
<td align="right">11.1%</td>
<td align="right">6,120</td>
<td align="right">11.1%</td>
<td align="right">-5.6%</td>
</tr>
<tr>
<td align="left">py simple</td>
<td align="right">35,438</td>
<td align="right">60.5%</td>
<td align="right">34,037</td>
<td align="right">61.5%</td>
<td align="right">-4.0%</td>
</tr>
<tr>
<td align="left">bytearray int</td>
<td align="right">925</td>
<td align="right">1.6%</td>
<td align="right">900</td>
<td align="right">1.6%</td>
<td align="right">-2.7%</td>
</tr>
</tbody>
</table>


</details>

### TO_BOOL

<details>
<summary> specialization stats for TO_BOOL family </summary>

<table>
<thead>
<tr>
<th align="left">Kind</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">88,000,620</td>
<td align="right">2.4%</td>
<td align="right">43,131,513</td>
<td align="right">2.1%</td>
<td align="right">-51.0%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">3,291,697,745</td>
<td align="right">91.4%</td>
<td align="right">1,892,689,822</td>
<td align="right">91.2%</td>
<td align="right">-42.5%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">308,040,373</td>
<td align="right">8.6%</td>
<td align="right">182,330,243</td>
<td align="right">8.8%</td>
<td align="right">-40.8%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Success</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Failure</td>
<td align="right">395,797</td>
<td align="right">17.0%</td>
<td align="right">177,420</td>
<td align="right">14.7%</td>
<td align="right">-55.2%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">1,929,583</td>
<td align="right">83.0%</td>
<td align="right">1,029,468</td>
<td align="right">85.3%</td>
<td align="right">-46.6%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Failure kind</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">other</td>
<td align="right">170,517</td>
<td align="right">43.1%</td>
<td align="right">5,127</td>
<td align="right">2.9%</td>
<td align="right">-97.0%</td>
</tr>
<tr>
<td align="left">number</td>
<td align="right">23,655</td>
<td align="right">6.0%</td>
<td align="right">4,674</td>
<td align="right">2.6%</td>
<td align="right">-80.2%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">42,082</td>
<td align="right">10.6%</td>
<td align="right">22,728</td>
<td align="right">12.8%</td>
<td align="right">-46.0%</td>
</tr>
<tr>
<td align="left">bytes</td>
<td align="right">18,689</td>
<td align="right">4.7%</td>
<td align="right">13,444</td>
<td align="right">7.6%</td>
<td align="right">-28.1%</td>
</tr>
<tr>
<td align="left">dict</td>
<td align="right">28,452</td>
<td align="right">7.2%</td>
<td align="right">22,942</td>
<td align="right">12.9%</td>
<td align="right">-19.4%</td>
</tr>
<tr>
<td align="left">float</td>
<td align="right">2,323</td>
<td align="right">0.6%</td>
<td align="right">2,025</td>
<td align="right">1.1%</td>
<td align="right">-12.8%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">40,460</td>
<td align="right">10.2%</td>
<td align="right">38,612</td>
<td align="right">21.8%</td>
<td align="right">-4.6%</td>
</tr>
<tr>
<td align="left">mapping</td>
<td align="right">50,718</td>
<td align="right">12.8%</td>
<td align="right">48,855</td>
<td align="right">27.5%</td>
<td align="right">-3.7%</td>
</tr>
<tr>
<td align="left">sequence</td>
<td align="right">17,241</td>
<td align="right">4.4%</td>
<td align="right">17,353</td>
<td align="right">9.8%</td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">bytearray</td>
<td align="right">1,240</td>
<td align="right">0.3%</td>
<td align="right">1,240</td>
<td align="right">0.7%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">memory view</td>
<td align="right">420</td>
<td align="right">0.1%</td>
<td align="right">420</td>
<td align="right">0.2%</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### UNPACK_SEQUENCE

<details>
<summary> specialization stats for UNPACK_SEQUENCE family </summary>

<table>
<thead>
<tr>
<th align="left">Kind</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">492,924</td>
<td align="right">0.1%</td>
<td align="right">119,945</td>
<td align="right">0.1%</td>
<td align="right">-75.7%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">563,789,703</td>
<td align="right">99.9%</td>
<td align="right">184,661,277</td>
<td align="right">99.9%</td>
<td align="right">-67.2%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">27</td>
<td align="right">0.0%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Success</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Failure</td>
<td align="right">3,506</td>
<td align="right">8.8%</td>
<td align="right">2,675</td>
<td align="right">7.8%</td>
<td align="right">-23.7%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">36,290</td>
<td align="right">91.2%</td>
<td align="right">31,500</td>
<td align="right">92.2%</td>
<td align="right">-13.2%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Failure kind</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">iterator</td>
<td align="right">681</td>
<td align="right">19.4%</td>
<td align="right">500</td>
<td align="right">18.7%</td>
<td align="right">-26.6%</td>
</tr>
<tr>
<td align="left">sequence</td>
<td align="right">2,445</td>
<td align="right">69.7%</td>
<td align="right">1,875</td>
<td align="right">70.1%</td>
<td align="right">-23.3%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">380</td>
<td align="right">10.8%</td>
<td align="right">300</td>
<td align="right">11.2%</td>
<td align="right">-21.1%</td>
</tr>
</tbody>
</table>


</details>


</details>

## Specialization effectiveness

<details>
<summary> specialization effectiveness </summary>


All entries are execution counts. Should add up to the total number of
Tier 1 instructions executed.

<table>
<thead>
<tr>
<th align="left">Instructions</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">
Specialized misses
<details>
<summary>ⓘ</summary>

Specialized instructions, e.g. `LOAD_ATTR_MODULE` that deopt.
</details>
</td>
<td align="right">798,041,789</td>
<td align="right">0.7%</td>
<td align="right">425,426,225</td>
<td align="right">0.6%</td>
<td align="right">-46.7%</td>
</tr>
<tr>
<td align="left">
Not specialized
<details>
<summary>ⓘ</summary>

Instructions that could be specialized but aren't, e.g. `LOAD_ATTR`, `BINARY_SLICE`.
</details>
</td>
<td align="right">10,455,770,381</td>
<td align="right">9.4%</td>
<td align="right">5,879,844,640</td>
<td align="right">8.3%</td>
<td align="right">-43.8%</td>
</tr>
<tr>
<td align="left">
Basic
<details>
<summary>ⓘ</summary>

Instructions that are not and cannot be specialized, e.g. `LOAD_FAST`.
</details>
</td>
<td align="right">60,826,318,628</td>
<td align="right">54.6%</td>
<td align="right">38,240,926,076</td>
<td align="right">53.7%</td>
<td align="right">-37.1%</td>
</tr>
<tr>
<td align="left">
Specialized hits
<details>
<summary>ⓘ</summary>

Specialized instructions, e.g. `LOAD_ATTR_MODULE` that complete.
</details>
</td>
<td align="right">39,368,504,862</td>
<td align="right">35.3%</td>
<td align="right">26,624,729,323</td>
<td align="right">37.4%</td>
<td align="right">-32.4%</td>
</tr>
</tbody>
</table>

### Deferred by instruction

<details>
<summary> Breakdown of deferred (not specialized) instruction counts by family </summary>

<table>
<thead>
<tr>
<th align="left">Name</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">CALL</td>
<td align="right">1,349,624,072</td>
<td align="right">32.5%</td>
<td align="right">283,962,586</td>
<td align="right">13.7%</td>
<td align="right">-79.0%</td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">183,822,374</td>
<td align="right">4.4%</td>
<td align="right">74,111,595</td>
<td align="right">3.6%</td>
<td align="right">-59.7%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">136,772,478</td>
<td align="right">3.3%</td>
<td align="right">63,034,428</td>
<td align="right">3.0%</td>
<td align="right">-53.9%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR</td>
<td align="right">325,951,011</td>
<td align="right">7.8%</td>
<td align="right">192,580,294</td>
<td align="right">9.3%</td>
<td align="right">-40.9%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">308,040,373</td>
<td align="right">7.4%</td>
<td align="right">182,330,243</td>
<td align="right">8.8%</td>
<td align="right">-40.8%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">482,069,877</td>
<td align="right">11.6%</td>
<td align="right">301,274,794</td>
<td align="right">14.5%</td>
<td align="right">-37.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">932,123,653</td>
<td align="right">22.4%</td>
<td align="right">595,714,422</td>
<td align="right">28.7%</td>
<td align="right">-36.1%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">98,049,392</td>
<td align="right">2.4%</td>
<td align="right">78,173,780</td>
<td align="right">3.8%</td>
<td align="right">-20.3%</td>
</tr>
<tr>
<td align="left">SEND</td>
<td align="right">173,802,912</td>
<td align="right">4.2%</td>
<td align="right">173,806,838</td>
<td align="right">8.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">75,758,198</td>
<td align="right">1.8%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">STORE_SUBSCR</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">63,363,777</td>
<td align="right">3.1%</td>
<td align="right"></td>
</tr>
</tbody>
</table>


</details>

### Misses by instruction

<details>
<summary> Breakdown of misses (specialized deopts) instruction counts by family </summary>

<table>
<thead>
<tr>
<th align="left">Name</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">77,654,673</td>
<td align="right">9.7%</td>
<td align="right">19,161,957</td>
<td align="right">4.5%</td>
<td align="right">-75.3%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_SLOT</td>
<td align="right">94,977,208</td>
<td align="right">11.9%</td>
<td align="right">25,931,594</td>
<td align="right">6.1%</td>
<td align="right">-72.7%</td>
</tr>
<tr>
<td align="left">TO_BOOL_ALWAYS_TRUE</td>
<td align="right">41,563,022</td>
<td align="right">5.2%</td>
<td align="right">20,357,122</td>
<td align="right">4.8%</td>
<td align="right">-51.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL_NONE</td>
<td align="right">41,134,232</td>
<td align="right">5.2%</td>
<td align="right">20,980,987</td>
<td align="right">4.9%</td>
<td align="right">-49.0%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">109,997,074</td>
<td align="right">13.8%</td>
<td align="right">58,187,889</td>
<td align="right">13.7%</td>
<td align="right">-47.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">119,899,100</td>
<td align="right">15.0%</td>
<td align="right">72,302,015</td>
<td align="right">17.0%</td>
<td align="right">-39.7%</td>
</tr>
<tr>
<td align="left">CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">31,004,385</td>
<td align="right">3.9%</td>
<td align="right">23,102,629</td>
<td align="right">5.4%</td>
<td align="right">-25.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">50,699,156</td>
<td align="right">6.4%</td>
<td align="right">39,273,269</td>
<td align="right">9.2%</td>
<td align="right">-22.5%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">42,597,204</td>
<td align="right">5.3%</td>
<td align="right">39,179,217</td>
<td align="right">9.2%</td>
<td align="right">-8.0%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">44,630,816</td>
<td align="right">5.6%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">27,829,032</td>
<td align="right">6.5%</td>
<td align="right"></td>
</tr>
</tbody>
</table>


</details>


</details>

## Call stats

<details>
<summary> Inlined calls and frame stats </summary>


This shows what fraction of calls to Python functions are inlined (i.e.
not having a call at the C level) and for those that are not, where the
call comes from.  The various categories overlap.

Also includes the count of frame objects created.

<table>
<thead>
<tr>
<th align="left"></th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Frames pushed</td>
<td align="right">6,541,978,719</td>
<td align="right">79.5%</td>
<td align="right">6,172,908,554</td>
<td align="right">78.6%</td>
<td align="right">-5.6%</td>
</tr>
<tr>
<td align="left">Calls to Python functions inlined</td>
<td align="right">5,973,953,571</td>
<td align="right">72.6%</td>
<td align="right">5,648,783,910</td>
<td align="right">71.9%</td>
<td align="right">-5.4%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (function ex)</td>
<td align="right">35,970,124</td>
<td align="right">0.4%</td>
<td align="right">34,592,946</td>
<td align="right">0.4%</td>
<td align="right">-3.8%</td>
</tr>
<tr>
<td align="left">Frame objects created</td>
<td align="right">76,558,142</td>
<td align="right">0.9%</td>
<td align="right">73,918,748</td>
<td align="right">0.9%</td>
<td align="right">-3.4%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (function vectorcall)</td>
<td align="right">1,394,463,644</td>
<td align="right">16.9%</td>
<td align="right">1,351,109,734</td>
<td align="right">17.2%</td>
<td align="right">-3.1%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (vector)</td>
<td align="right">1,397,140,401</td>
<td align="right">17.0%</td>
<td align="right">1,353,785,954</td>
<td align="right">17.2%</td>
<td align="right">-3.1%</td>
</tr>
<tr>
<td align="left">Calls to PyEval_EvalDefault</td>
<td align="right">2,259,449,033</td>
<td align="right">27.4%</td>
<td align="right">2,207,964,161</td>
<td align="right">28.1%</td>
<td align="right">-2.3%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (total)</td>
<td align="right">2,259,449,033</td>
<td align="right">27.4%</td>
<td align="right">2,207,964,161</td>
<td align="right">28.1%</td>
<td align="right">-2.3%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (build class)</td>
<td align="right">24,340</td>
<td align="right">0.0%</td>
<td align="right">24,020</td>
<td align="right">0.0%</td>
<td align="right">-1.3%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (api)</td>
<td align="right">247,995,284</td>
<td align="right">3.0%</td>
<td align="right">245,183,289</td>
<td align="right">3.1%</td>
<td align="right">-1.1%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (generator)</td>
<td align="right">862,308,632</td>
<td align="right">10.5%</td>
<td align="right">854,178,207</td>
<td align="right">10.9%</td>
<td align="right">-0.9%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (slot)</td>
<td align="right">458,517,044</td>
<td align="right">5.6%</td>
<td align="right">454,998,457</td>
<td align="right">5.8%</td>
<td align="right">-0.8%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (method)</td>
<td align="right">213,149,994</td>
<td align="right">2.6%</td>
<td align="right">213,199,713</td>
<td align="right">2.7%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (legacy)</td>
<td align="right">2,652,417</td>
<td align="right">0.0%</td>
<td align="right">2,652,200</td>
<td align="right">0.0%</td>
<td align="right">-0.0%</td>
</tr>
</tbody>
</table>


</details>

## Object stats

<details>
<summary> Allocations, frees and dict materializatons </summary>


Below, "allocations" means "allocations that are not from a freelist".
Total allocations = "Allocations from freelist" + "Allocations".

"Inline values" is the number of values arrays inlined into objects.

The cache hit/miss numbers are for the MRO cache, split into dunder and
other names.

<table>
<thead>
<tr>
<th align="left"></th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Method cache dunder misses</td>
<td align="right">9,626,638</td>
<td align="right"></td>
<td align="right">5,831,082</td>
<td align="right"></td>
<td align="right">-39.4%</td>
</tr>
<tr>
<td align="left">Method cache misses</td>
<td align="right">30,541,299</td>
<td align="right"></td>
<td align="right">22,889,120</td>
<td align="right"></td>
<td align="right">-25.1%</td>
</tr>
<tr>
<td align="left">Method cache collisions</td>
<td align="right">33,200,859</td>
<td align="right"></td>
<td align="right">28,510,266</td>
<td align="right"></td>
<td align="right">-14.1%</td>
</tr>
<tr>
<td align="left">Method cache hits</td>
<td align="right">2,505,709,683</td>
<td align="right"></td>
<td align="right">2,333,689,584</td>
<td align="right"></td>
<td align="right">-6.9%</td>
</tr>
<tr>
<td align="left">Method cache dunder hits</td>
<td align="right">3,276,965,883</td>
<td align="right"></td>
<td align="right">3,092,189,760</td>
<td align="right"></td>
<td align="right">-5.6%</td>
</tr>
<tr>
<td align="left">Inline values</td>
<td align="right">170,892,029</td>
<td align="right"></td>
<td align="right">162,456,376</td>
<td align="right"></td>
<td align="right">-4.9%</td>
</tr>
<tr>
<td align="left">Materialize dict (new key)</td>
<td align="right">67,112</td>
<td align="right">0.0%</td>
<td align="right">64,160</td>
<td align="right">0.0%</td>
<td align="right">-4.4%</td>
</tr>
<tr>
<td align="left">Decrefs</td>
<td align="right">27,608,938,861</td>
<td align="right">21.3%</td>
<td align="right">26,487,799,332</td>
<td align="right">20.9%</td>
<td align="right">-4.1%</td>
</tr>
<tr>
<td align="left">Interpreter increfs</td>
<td align="right">89,071,532,359</td>
<td align="right">78.6%</td>
<td align="right">86,660,446,658</td>
<td align="right">78.6%</td>
<td align="right">-2.7%</td>
</tr>
<tr>
<td align="left">Increfs</td>
<td align="right">24,204,140,340</td>
<td align="right">21.4%</td>
<td align="right">23,611,091,146</td>
<td align="right">21.4%</td>
<td align="right">-2.5%</td>
</tr>
<tr>
<td align="left">Frees to freelist</td>
<td align="right">6,510,772,905</td>
<td align="right"></td>
<td align="right">6,365,322,914</td>
<td align="right"></td>
<td align="right">-2.2%</td>
</tr>
<tr>
<td align="left">Allocations from freelist</td>
<td align="right">6,508,859,461</td>
<td align="right">37.3%</td>
<td align="right">6,363,457,520</td>
<td align="right">37.0%</td>
<td align="right">-2.2%</td>
</tr>
<tr>
<td align="left">Interpreter decrefs</td>
<td align="right">102,304,538,510</td>
<td align="right">78.7%</td>
<td align="right">100,334,874,565</td>
<td align="right">79.1%</td>
<td align="right">-1.9%</td>
</tr>
<tr>
<td align="left">Allocations to 512 bytes</td>
<td align="right">10,804,661,736</td>
<td align="right">62.0%</td>
<td align="right">10,722,248,476</td>
<td align="right">62.3%</td>
<td align="right">-0.8%</td>
</tr>
<tr>
<td align="left">Allocations</td>
<td align="right">10,929,982,443</td>
<td align="right">62.7%</td>
<td align="right">10,847,986,881</td>
<td align="right">63.0%</td>
<td align="right">-0.8%</td>
</tr>
<tr>
<td align="left">Allocations over 4 kbytes</td>
<td align="right">20,740,861</td>
<td align="right">0.1%</td>
<td align="right">20,614,453</td>
<td align="right">0.1%</td>
<td align="right">-0.6%</td>
</tr>
<tr>
<td align="left">Frees</td>
<td align="right">11,233,763,306</td>
<td align="right"></td>
<td align="right">11,173,637,853</td>
<td align="right"></td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">Allocations to 4 kbytes</td>
<td align="right">104,579,846</td>
<td align="right">0.6%</td>
<td align="right">105,123,952</td>
<td align="right">0.6%</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">Materialize dict (on request)</td>
<td align="right">6,549,542</td>
<td align="right">3.8%</td>
<td align="right">6,547,420</td>
<td align="right">4.0%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">Materialize dict (too big)</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">Materialize dict (str subclass)</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right"></td>
</tr>
</tbody>
</table>


</details>

## GC stats

<details>
<summary> GC collections and effectiveness </summary>


Collected/visits gives some measure of efficiency.

<table>
<thead>
<tr>
<th align="right">Generation</th>
<th align="right">Base Collections</th>
<th align="right">Base Objects collected</th>
<th align="right">Base Object visits</th>
<th align="right">Head Collections</th>
<th align="right">Head Objects collected</th>
<th align="right">Head Object visits</th>
</tr>
</thead>
<tbody>
<tr>
<td align="right">0</td>
<td align="right">0</td>
<td align="right">0</td>
<td align="right">0</td>
<td align="right">0</td>
<td align="right">0</td>
<td align="right">0</td>
</tr>
<tr>
<td align="right">1</td>
<td align="right">0</td>
<td align="right">21,246,877</td>
<td align="right">15,099,426,732</td>
<td align="right">0</td>
<td align="right">19,469,935</td>
<td align="right">14,514,393,405</td>
</tr>
<tr>
<td align="right">2</td>
<td align="right">0</td>
<td align="right">10,755,840</td>
<td align="right">6,973,328,432</td>
<td align="right">0</td>
<td align="right">10,755,840</td>
<td align="right">6,974,310,550</td>
</tr>
</tbody>
</table>


</details>

## Optimization (Tier 2) stats

<details>
<summary> statistics about the Tier 2 optimizer </summary>

<table>
<thead>
<tr>
<th align="left"></th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">
Inner loop found
<details>
<summary>ⓘ</summary>

A trace is truncated because it has an inner loop
</details>
</td>
<td align="right">50,106</td>
<td align="right">5.8%</td>
<td align="right">96,966</td>
<td align="right">18.2%</td>
<td align="right">93.5%</td>
</tr>
<tr>
<td align="left">
Trace stack underflow
<details>
<summary>ⓘ</summary>

A potential trace is abandoned because it pops more frames than it pushes.
</details>
</td>
<td align="right">444,457</td>
<td align="right">51.4%</td>
<td align="right">50,698</td>
<td align="right">9.5%</td>
<td align="right">-88.6%</td>
</tr>
<tr>
<td align="left">
Trace too short
<details>
<summary>ⓘ</summary>

A potential trace is abandoced because it it too short.
</details>
</td>
<td align="right">729,345</td>
<td align="right">84.4%</td>
<td align="right">349,815</td>
<td align="right">65.7%</td>
<td align="right">-52.0%</td>
</tr>
<tr>
<td align="left">
Trace stack overflow
<details>
<summary>ⓘ</summary>

A trace is truncated because it would require more than 5 stack frames.
</details>
</td>
<td align="right">564</td>
<td align="right">0.1%</td>
<td align="right">838</td>
<td align="right">0.2%</td>
<td align="right">48.6%</td>
</tr>
<tr>
<td align="left">
Optimization attempts
<details>
<summary>ⓘ</summary>

The number of times a potential trace is identified.  Specifically, this occurs in the JUMP BACKWARD instruction when the counter reaches a threshold.
</details>
</td>
<td align="right">864,064</td>
<td align="right"></td>
<td align="right">532,648</td>
<td align="right"></td>
<td align="right">-38.4%</td>
</tr>
<tr>
<td align="left">
Traces created
<details>
<summary>ⓘ</summary>

The number of traces that were successfully created.
</details>
</td>
<td align="right">134,719</td>
<td align="right">15.6%</td>
<td align="right">182,833</td>
<td align="right">34.3%</td>
<td align="right">35.7%</td>
</tr>
<tr>
<td align="left">
Uops executed
<details>
<summary>ⓘ</summary>

The total number of uops (micro-operations) that were executed
</details>
</td>
<td align="right">189,950,522,411</td>
<td align="right">2,632.7%</td>
<td align="right">247,909,355,901</td>
<td align="right">3,212.8%</td>
<td align="right">30.5%</td>
</tr>
<tr>
<td align="left">
Low confidence
<details>
<summary>ⓘ</summary>

A trace is abandoned because the likelihood of the jump to top being taken is too low.
</details>
</td>
<td align="right">7,855</td>
<td align="right">0.9%</td>
<td align="right">10,048</td>
<td align="right">1.9%</td>
<td align="right">27.9%</td>
</tr>
<tr>
<td align="left">
Recursive call
<details>
<summary>ⓘ</summary>

A trace is truncated because it has a recursive call.
</details>
</td>
<td align="right">1,522</td>
<td align="right">0.2%</td>
<td align="right">1,700</td>
<td align="right">0.3%</td>
<td align="right">11.7%</td>
</tr>
<tr>
<td align="left">
Executors invalidated
<details>
<summary>ⓘ</summary>

The number of executors that were invalidated due to watched dictionary changes.
</details>
</td>
<td align="right">6,004</td>
<td align="right">4.5%</td>
<td align="right">6,601</td>
<td align="right">3.6%</td>
<td align="right">9.9%</td>
</tr>
<tr>
<td align="left">
Traces executed
<details>
<summary>ⓘ</summary>

The number of traces that were executed
</details>
</td>
<td align="right">7,215,098,788</td>
<td align="right"></td>
<td align="right">7,716,239,539</td>
<td align="right"></td>
<td align="right">6.9%</td>
</tr>
<tr>
<td align="left">
Trace too long
<details>
<summary>ⓘ</summary>

A trace is truncated because it is longer than the instruction buffer.
</details>
</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right">340</td>
<td align="right">0.1%</td>
<td align="right">340 / 0 !!</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left"></th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">
Optimizer successes
<details>
<summary>ⓘ</summary>

The number of traces that were successfully optimized.
</details>
</td>
<td align="right">131,228</td>
<td align="right">97.4%</td>
<td align="right">179,036</td>
<td align="right">97.9%</td>
<td align="right">36.4%</td>
</tr>
<tr>
<td align="left">
Optimizer attempts
<details>
<summary>ⓘ</summary>

The number of times the trace optimizer (_Py_uop_analyze_and_optimize) was run.
</details>
</td>
<td align="right">134,719</td>
<td align="right"></td>
<td align="right">182,833</td>
<td align="right"></td>
<td align="right">35.7%</td>
</tr>
<tr>
<td align="left">
Remove globals incorrect keys
<details>
<summary>ⓘ</summary>

The keys in the globals dictionary aren't what was expected
</details>
</td>
<td align="right">2,003</td>
<td align="right">1.5%</td>
<td align="right">2,337</td>
<td align="right">1.3%</td>
<td align="right">16.7%</td>
</tr>
<tr>
<td align="left">
Optimizer no memory
<details>
<summary>ⓘ</summary>

The number of optimizations that failed due to no memory.
</details>
</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">
Remove globals builtins changed
<details>
<summary>ⓘ</summary>

The builtins changed during optimization
</details>
</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right"></td>
</tr>
</tbody>
</table>

### Trace length histogram

<details>
<summary> trace length histogram </summary>

<table>
<thead>
<tr>
<th align="left">Range</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left"><= 1</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 2</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 4</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 8</td>
<td align="right">5,982</td>
<td align="right">4.4%</td>
<td align="right">14,931</td>
<td align="right">8.2%</td>
<td align="right">149.6%</td>
</tr>
<tr>
<td align="left"><= 16</td>
<td align="right">25,140</td>
<td align="right">18.7%</td>
<td align="right">40,967</td>
<td align="right">22.4%</td>
<td align="right">63.0%</td>
</tr>
<tr>
<td align="left"><= 32</td>
<td align="right">48,188</td>
<td align="right">35.8%</td>
<td align="right">54,646</td>
<td align="right">29.9%</td>
<td align="right">13.4%</td>
</tr>
<tr>
<td align="left"><= 64</td>
<td align="right">31,074</td>
<td align="right">23.1%</td>
<td align="right">39,074</td>
<td align="right">21.4%</td>
<td align="right">25.7%</td>
</tr>
<tr>
<td align="left"><= 128</td>
<td align="right">17,089</td>
<td align="right">12.7%</td>
<td align="right">21,273</td>
<td align="right">11.6%</td>
<td align="right">24.5%</td>
</tr>
<tr>
<td align="left"><= 256</td>
<td align="right">6,290</td>
<td align="right">4.7%</td>
<td align="right">9,585</td>
<td align="right">5.2%</td>
<td align="right">52.4%</td>
</tr>
<tr>
<td align="left"><= 512</td>
<td align="right">956</td>
<td align="right">0.7%</td>
<td align="right">1,957</td>
<td align="right">1.1%</td>
<td align="right">104.7%</td>
</tr>
<tr>
<td align="left"><= 1,024</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">400</td>
<td align="right">0.2%</td>
<td align="right"></td>
</tr>
</tbody>
</table>


</details>

### Optimized trace length histogram

<details>
<summary> optimized trace length histogram </summary>

<table>
<thead>
<tr>
<th align="left">Range</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left"><= 1</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 2</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 4</td>
<td align="right">4,552</td>
<td align="right">3.4%</td>
<td align="right">2,993</td>
<td align="right">1.6%</td>
<td align="right">-34.2%</td>
</tr>
<tr>
<td align="left"><= 8</td>
<td align="right">16,673</td>
<td align="right">12.4%</td>
<td align="right">35,833</td>
<td align="right">19.6%</td>
<td align="right">114.9%</td>
</tr>
<tr>
<td align="left"><= 16</td>
<td align="right">35,116</td>
<td align="right">26.1%</td>
<td align="right">41,271</td>
<td align="right">22.6%</td>
<td align="right">17.5%</td>
</tr>
<tr>
<td align="left"><= 32</td>
<td align="right">41,756</td>
<td align="right">31.0%</td>
<td align="right">53,389</td>
<td align="right">29.2%</td>
<td align="right">27.9%</td>
</tr>
<tr>
<td align="left"><= 64</td>
<td align="right">21,759</td>
<td align="right">16.2%</td>
<td align="right">27,415</td>
<td align="right">15.0%</td>
<td align="right">26.0%</td>
</tr>
<tr>
<td align="left"><= 128</td>
<td align="right">8,951</td>
<td align="right">6.6%</td>
<td align="right">13,435</td>
<td align="right">7.3%</td>
<td align="right">50.1%</td>
</tr>
<tr>
<td align="left"><= 256</td>
<td align="right">2,280</td>
<td align="right">1.7%</td>
<td align="right">4,020</td>
<td align="right">2.2%</td>
<td align="right">76.3%</td>
</tr>
<tr>
<td align="left"><= 512</td>
<td align="right">141</td>
<td align="right">0.1%</td>
<td align="right">680</td>
<td align="right">0.4%</td>
<td align="right">382.3%</td>
</tr>
</tbody>
</table>


</details>

### Trace run length histogram

<details>
<summary> trace run length histogram </summary>

<table>
<thead>
<tr>
<th align="left">Range</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left"><= 1</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 2</td>
<td align="right">26,058,980</td>
<td align="right">0.4%</td>
<td align="right">28,222,400</td>
<td align="right">0.4%</td>
<td align="right">8.3%</td>
</tr>
<tr>
<td align="left"><= 4</td>
<td align="right">182,246,030</td>
<td align="right">2.5%</td>
<td align="right">121,454,994</td>
<td align="right">1.6%</td>
<td align="right">-33.4%</td>
</tr>
<tr>
<td align="left"><= 8</td>
<td align="right">1,086,251,986</td>
<td align="right">15.1%</td>
<td align="right">1,033,261,368</td>
<td align="right">13.4%</td>
<td align="right">-4.9%</td>
</tr>
<tr>
<td align="left"><= 16</td>
<td align="right">1,213,870,786</td>
<td align="right">16.8%</td>
<td align="right">897,471,746</td>
<td align="right">11.6%</td>
<td align="right">-26.1%</td>
</tr>
<tr>
<td align="left"><= 32</td>
<td align="right">1,145,354,048</td>
<td align="right">15.9%</td>
<td align="right">910,597,983</td>
<td align="right">11.8%</td>
<td align="right">-20.5%</td>
</tr>
<tr>
<td align="left"><= 64</td>
<td align="right">665,228,699</td>
<td align="right">9.2%</td>
<td align="right">781,837,929</td>
<td align="right">10.1%</td>
<td align="right">17.5%</td>
</tr>
<tr>
<td align="left"><= 128</td>
<td align="right">282,519,749</td>
<td align="right">3.9%</td>
<td align="right">433,790,001</td>
<td align="right">5.6%</td>
<td align="right">53.5%</td>
</tr>
<tr>
<td align="left"><= 256</td>
<td align="right">167,371,463</td>
<td align="right">2.3%</td>
<td align="right">216,695,698</td>
<td align="right">2.8%</td>
<td align="right">29.5%</td>
</tr>
<tr>
<td align="left"><= 512</td>
<td align="right">21,287,796</td>
<td align="right">0.3%</td>
<td align="right">28,337,477</td>
<td align="right">0.4%</td>
<td align="right">33.1%</td>
</tr>
<tr>
<td align="left"><= 1,024</td>
<td align="right">6,946,295</td>
<td align="right">0.1%</td>
<td align="right">7,342,975</td>
<td align="right">0.1%</td>
<td align="right">5.7%</td>
</tr>
<tr>
<td align="left"><= 2,048</td>
<td align="right">19,018,001</td>
<td align="right">0.3%</td>
<td align="right">19,033,950</td>
<td align="right">0.2%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left"><= 4,096</td>
<td align="right">622,409</td>
<td align="right">0.0%</td>
<td align="right">685,852</td>
<td align="right">0.0%</td>
<td align="right">10.2%</td>
</tr>
<tr>
<td align="left"><= 8,192</td>
<td align="right">742,086</td>
<td align="right">0.0%</td>
<td align="right">740,600</td>
<td align="right">0.0%</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left"><= 16,384</td>
<td align="right">243,843</td>
<td align="right">0.0%</td>
<td align="right">246,820</td>
<td align="right">0.0%</td>
<td align="right">1.2%</td>
</tr>
<tr>
<td align="left"><= 32,768</td>
<td align="right">42,533</td>
<td align="right">0.0%</td>
<td align="right">43,740</td>
<td align="right">0.0%</td>
<td align="right">2.8%</td>
</tr>
<tr>
<td align="left"><= 65,536</td>
<td align="right">12,521</td>
<td align="right">0.0%</td>
<td align="right">13,200</td>
<td align="right">0.0%</td>
<td align="right">5.4%</td>
</tr>
<tr>
<td align="left"><= 131,072</td>
<td align="right">377</td>
<td align="right">0.0%</td>
<td align="right">960</td>
<td align="right">0.0%</td>
<td align="right">154.6%</td>
</tr>
<tr>
<td align="left"><= 262,144</td>
<td align="right">2,002</td>
<td align="right">0.0%</td>
<td align="right">2,000</td>
<td align="right">0.0%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left"><= 524,288</td>
<td align="right">461</td>
<td align="right">0.0%</td>
<td align="right">459</td>
<td align="right">0.0%</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left"><= 1,048,576</td>
<td align="right">400</td>
<td align="right">0.0%</td>
<td align="right">400</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left"><= 2,097,152</td>
<td align="right">221</td>
<td align="right">0.0%</td>
<td align="right">379</td>
<td align="right">0.0%</td>
<td align="right">71.5%</td>
</tr>
<tr>
<td align="left"><= 4,194,304</td>
<td align="right">259</td>
<td align="right">0.0%</td>
<td align="right">261</td>
<td align="right">0.0%</td>
<td align="right">0.8%</td>
</tr>
<tr>
<td align="left"><= 8,388,608</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 16,777,216</td>
<td align="right">240</td>
<td align="right">0.0%</td>
<td align="right">240</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### Uop execution stats

<details>
<summary> uop execution stats </summary>

<table>
<thead>
<tr>
<th align="left">Name</th>
<th align="right">Base Count</th>
<th align="right">Head Count</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">_UNPACK_EX</td>
<td align="right">104</td>
<td align="right">871,420</td>
<td align="right">837,803.8%</td>
</tr>
<tr>
<td align="left">_CONVERT_VALUE</td>
<td align="right">125,883</td>
<td align="right">96,082,420</td>
<td align="right">76,226.8%</td>
</tr>
<tr>
<td align="left">_UNPACK_SEQUENCE</td>
<td align="right">1,555,174</td>
<td align="right">316,229,046</td>
<td align="right">20,234.0%</td>
</tr>
<tr>
<td align="left">_FORMAT_SIMPLE</td>
<td align="right">863,012</td>
<td align="right">101,032,211</td>
<td align="right">11,606.9%</td>
</tr>
<tr>
<td align="left">_BUILD_STRING</td>
<td align="right">713,844</td>
<td align="right">51,359,591</td>
<td align="right">7,094.8%</td>
</tr>
<tr>
<td align="left">_POP_EXCEPT</td>
<td align="right">7,620</td>
<td align="right">378,031</td>
<td align="right">4,861.0%</td>
</tr>
<tr>
<td align="left">_LOAD_SUPER_ATTR_METHOD</td>
<td align="right">241,101</td>
<td align="right">6,728,203</td>
<td align="right">2,690.6%</td>
</tr>
<tr>
<td align="left">_GET_YIELD_FROM_ITER</td>
<td align="right">822,821</td>
<td align="right">12,271,304</td>
<td align="right">1,391.4%</td>
</tr>
<tr>
<td align="left">_DYNAMIC_EXIT</td>
<td align="right">169,869,856</td>
<td align="right">2,377,722,664</td>
<td align="right">1,299.7%</td>
</tr>
<tr>
<td align="left">_STORE_DEREF</td>
<td align="right">3,292,994</td>
<td align="right">38,929,485</td>
<td align="right">1,082.2%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_INSTANCE_VALUE_1</td>
<td align="right">4,701,081</td>
<td align="right">55,122,304</td>
<td align="right">1,072.5%</td>
</tr>
<tr>
<td align="left">_MAKE_CELL</td>
<td align="right">5,909,754</td>
<td align="right">58,385,575</td>
<td align="right">888.0%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_CLASS_0</td>
<td align="right">13,936,580</td>
<td align="right">97,516,348</td>
<td align="right">599.7%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_CHECK</td>
<td align="right">458,272</td>
<td align="right">2,394,844</td>
<td align="right">422.6%</td>
</tr>
<tr>
<td align="left">_STORE_ATTR</td>
<td align="right">7,541,824</td>
<td align="right">30,909,484</td>
<td align="right">309.8%</td>
</tr>
<tr>
<td align="left">_POP_FRAME</td>
<td align="right">721,135,268</td>
<td align="right">2,716,262,264</td>
<td align="right">276.7%</td>
</tr>
<tr>
<td align="left">_STORE_GLOBAL</td>
<td align="right">1,260,560</td>
<td align="right">4,739,520</td>
<td align="right">276.0%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_3</td>
<td align="right">62,868,985</td>
<td align="right">224,574,640</td>
<td align="right">257.2%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS</td>
<td align="right">10,090,171</td>
<td align="right">35,811,775</td>
<td align="right">254.9%</td>
</tr>
<tr>
<td align="left">_CHECK_ATTR_CLASS</td>
<td align="right">35,273,483</td>
<td align="right">118,017,941</td>
<td align="right">234.6%</td>
</tr>
<tr>
<td align="left">_GET_AWAITABLE</td>
<td align="right">647,418</td>
<td align="right">2,004,595</td>
<td align="right">209.6%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_2</td>
<td align="right">114,690,558</td>
<td align="right">342,026,791</td>
<td align="right">198.2%</td>
</tr>
<tr>
<td align="left">_ERROR_POP_N</td>
<td align="right">1,874,527</td>
<td align="right">5,503,553</td>
<td align="right">193.6%</td>
</tr>
<tr>
<td align="left">_REPLACE_WITH_TRUE</td>
<td align="right">32,951,022</td>
<td align="right">96,581,524</td>
<td align="right">193.1%</td>
</tr>
<tr>
<td align="left">_UNARY_NEGATIVE</td>
<td align="right">25,063,629</td>
<td align="right">72,280,899</td>
<td align="right">188.4%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_NONE_POP</td>
<td align="right">70,314,144</td>
<td align="right">187,913,501</td>
<td align="right">167.2%</td>
</tr>
<tr>
<td align="left">_STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">162,176,225</td>
<td align="right">418,625,339</td>
<td align="right">158.1%</td>
</tr>
<tr>
<td align="left">_GUARD_DORV_NO_DICT</td>
<td align="right">163,403,045</td>
<td align="right">419,818,644</td>
<td align="right">156.9%</td>
</tr>
<tr>
<td align="left">_LOAD_GLOBAL_MODULE</td>
<td align="right">47,810,630</td>
<td align="right">117,246,905</td>
<td align="right">145.2%</td>
</tr>
<tr>
<td align="left">_CHECK_STACK_SPACE</td>
<td align="right">105,843,535</td>
<td align="right">237,244,288</td>
<td align="right">124.1%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_STR</td>
<td align="right">28,965,911</td>
<td align="right">57,752,786</td>
<td align="right">99.4%</td>
</tr>
<tr>
<td align="left">_SET_ADD</td>
<td align="right">1,449,189</td>
<td align="right">41,100</td>
<td align="right">-97.2%</td>
</tr>
<tr>
<td align="left">_DELETE_ATTR</td>
<td align="right">2,009,931</td>
<td align="right">57,591</td>
<td align="right">-97.1%</td>
</tr>
<tr>
<td align="left">_RETURN_GENERATOR</td>
<td align="right">91,250,983</td>
<td align="right">178,358,610</td>
<td align="right">95.5%</td>
</tr>
<tr>
<td align="left">_TO_BOOL</td>
<td align="right">264,405,092</td>
<td align="right">515,398,700</td>
<td align="right">94.9%</td>
</tr>
<tr>
<td align="left">_BINARY_SLICE</td>
<td align="right">114,164,108</td>
<td align="right">222,278,295</td>
<td align="right">94.7%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_NONDESCRIPTOR_NO_DICT</td>
<td align="right">25,846,486</td>
<td align="right">50,247,880</td>
<td align="right">94.4%</td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_CLASS</td>
<td align="right">66,045,973</td>
<td align="right">127,006,219</td>
<td align="right">92.3%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_3</td>
<td align="right">645,279,066</td>
<td align="right">1,231,820,148</td>
<td align="right">90.9%</td>
</tr>
<tr>
<td align="left">_STORE_ATTR_SLOT</td>
<td align="right">130,415,769</td>
<td align="right">236,993,189</td>
<td align="right">81.7%</td>
</tr>
<tr>
<td align="left">_GUARD_GLOBALS_VERSION</td>
<td align="right">101,080,154</td>
<td align="right">175,580,025</td>
<td align="right">73.7%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_NOT_NONE_POP</td>
<td align="right">166,106,037</td>
<td align="right">284,684,244</td>
<td align="right">71.4%</td>
</tr>
<tr>
<td align="left">_POP_TOP</td>
<td align="right">1,207,750,633</td>
<td align="right">2,066,973,612</td>
<td align="right">71.1%</td>
</tr>
<tr>
<td align="left">_RESUME_CHECK</td>
<td align="right">1,445,229,336</td>
<td align="right">2,376,678,145</td>
<td align="right">64.4%</td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">249,980,376</td>
<td align="right">405,407,549</td>
<td align="right">62.2%</td>
</tr>
<tr>
<td align="left">_COLD_EXIT</td>
<td align="right">2,227,407,747</td>
<td align="right">858,735,403</td>
<td align="right">-61.4%</td>
</tr>
<tr>
<td align="left">_CALL_TUPLE_1</td>
<td align="right">8,036,397</td>
<td align="right">12,889,297</td>
<td align="right">60.4%</td>
</tr>
<tr>
<td align="left">_CHECK_ATTR_MODULE</td>
<td align="right">7,485,339</td>
<td align="right">11,862,973</td>
<td align="right">58.5%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_MODULE</td>
<td align="right">7,485,339</td>
<td align="right">11,842,873</td>
<td align="right">58.2%</td>
</tr>
<tr>
<td align="left">_COPY_FREE_VARS</td>
<td align="right">80,696,917</td>
<td align="right">127,169,170</td>
<td align="right">57.6%</td>
</tr>
<tr>
<td align="left">_PUSH_FRAME</td>
<td align="right">1,738,471,967</td>
<td align="right">2,736,474,082</td>
<td align="right">57.4%</td>
</tr>
<tr>
<td align="left">_CHECK_VALIDITY_AND_SET_IP</td>
<td align="right">1,253,890,792</td>
<td align="right">1,938,520,432</td>
<td align="right">54.6%</td>
</tr>
<tr>
<td align="left">_CHECK_ATTR_WITH_HINT</td>
<td align="right">53,485,925</td>
<td align="right">82,670,234</td>
<td align="right">54.6%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_WITH_HINT</td>
<td align="right">53,372,543</td>
<td align="right">82,442,216</td>
<td align="right">54.5%</td>
</tr>
<tr>
<td align="left">_CHECK_CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">80,375,507</td>
<td align="right">123,375,556</td>
<td align="right">53.5%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">80,131,387</td>
<td align="right">122,846,456</td>
<td align="right">53.3%</td>
</tr>
<tr>
<td align="left">_BINARY_SUBSCR_DICT</td>
<td align="right">368,717,455</td>
<td align="right">560,479,674</td>
<td align="right">52.0%</td>
</tr>
<tr>
<td align="left">_CHECK_ATTR_METHOD_LAZY_DICT</td>
<td align="right">99,488,401</td>
<td align="right">149,453,847</td>
<td align="right">50.2%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_METHOD_LAZY_DICT</td>
<td align="right">99,488,401</td>
<td align="right">149,453,847</td>
<td align="right">50.2%</td>
</tr>
<tr>
<td align="left">_GET_ITER</td>
<td align="right">330,149,824</td>
<td align="right">492,473,611</td>
<td align="right">49.2%</td>
</tr>
<tr>
<td align="left">_COMPARE_OP</td>
<td align="right">106,498,032</td>
<td align="right">157,072,567</td>
<td align="right">47.5%</td>
</tr>
<tr>
<td align="left">_SAVE_RETURN_OFFSET</td>
<td align="right">1,637,835,188</td>
<td align="right">2,407,643,880</td>
<td align="right">47.0%</td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION_EXACT_ARGS</td>
<td align="right">1,710,959,996</td>
<td align="right">2,506,285,447</td>
<td align="right">46.5%</td>
</tr>
<tr>
<td align="left">_SET_IP</td>
<td align="right">13,122,574,893</td>
<td align="right">19,192,838,411</td>
<td align="right">46.3%</td>
</tr>
<tr>
<td align="left">_GUARD_TYPE_VERSION</td>
<td align="right">5,676,385,601</td>
<td align="right">8,249,504,239</td>
<td align="right">45.3%</td>
</tr>
<tr>
<td align="left">_CHECK_MANAGED_OBJECT_HAS_VALUES</td>
<td align="right">2,034,688,341</td>
<td align="right">2,955,059,846</td>
<td align="right">45.2%</td>
</tr>
<tr>
<td align="left">_IS_OP</td>
<td align="right">358,536,611</td>
<td align="right">516,101,637</td>
<td align="right">43.9%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_0</td>
<td align="right">5,734,280,533</td>
<td align="right">8,212,037,174</td>
<td align="right">43.2%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_BOOL</td>
<td align="right">1,995,932,246</td>
<td align="right">2,854,209,364</td>
<td align="right">43.0%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_INSTANCE_VALUE_0</td>
<td align="right">2,028,983,240</td>
<td align="right">2,899,011,922</td>
<td align="right">42.9%</td>
</tr>
<tr>
<td align="left">_SET_FUNCTION_ATTRIBUTE</td>
<td align="right">78,513,190</td>
<td align="right">112,121,055</td>
<td align="right">42.8%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_4</td>
<td align="right">685,423,132</td>
<td align="right">970,176,156</td>
<td align="right">41.5%</td>
</tr>
<tr>
<td align="left">_CHECK_STACK_SPACE_OPERAND</td>
<td align="right">940,551,797</td>
<td align="right">1,329,413,788</td>
<td align="right">41.3%</td>
</tr>
<tr>
<td align="left">_DELETE_SUBSCR</td>
<td align="right">96,838,610</td>
<td align="right">136,785,348</td>
<td align="right">41.3%</td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION</td>
<td align="right">1,313,709,196</td>
<td align="right">1,851,261,330</td>
<td align="right">40.9%</td>
</tr>
<tr>
<td align="left">_BUILD_TUPLE</td>
<td align="right">552,774,856</td>
<td align="right">778,661,335</td>
<td align="right">40.9%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_6</td>
<td align="right">511,806,552</td>
<td align="right">718,054,952</td>
<td align="right">40.3%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">1,043,281,604</td>
<td align="right">1,458,864,341</td>
<td align="right">39.8%</td>
</tr>
<tr>
<td align="left">_GUARD_BOTH_INT</td>
<td align="right">563,957,882</td>
<td align="right">786,012,059</td>
<td align="right">39.4%</td>
</tr>
<tr>
<td align="left">_CALL_LEN</td>
<td align="right">211,304,799</td>
<td align="right">294,100,081</td>
<td align="right">39.2%</td>
</tr>
<tr>
<td align="left">_LOAD_CONST_INLINE_WITH_NULL</td>
<td align="right">1,815,403,793</td>
<td align="right">2,514,493,838</td>
<td align="right">38.5%</td>
</tr>
<tr>
<td align="left">_GUARD_KEYS_VERSION</td>
<td align="right">1,136,967,127</td>
<td align="right">1,568,691,537</td>
<td align="right">38.0%</td>
</tr>
<tr>
<td align="left">_STORE_SUBSCR_DICT</td>
<td align="right">130,453,112</td>
<td align="right">179,836,401</td>
<td align="right">37.9%</td>
</tr>
<tr>
<td align="left">_GUARD_DORV_VALUES_INST_ATTR_FROM_DICT</td>
<td align="right">1,156,179,360</td>
<td align="right">1,591,865,580</td>
<td align="right">37.7%</td>
</tr>
<tr>
<td align="left">_START_EXECUTOR</td>
<td align="right">4,987,691,041</td>
<td align="right">6,857,504,136</td>
<td align="right">37.5%</td>
</tr>
<tr>
<td align="left">_LOAD_CONST_INLINE</td>
<td align="right">1,536,518,483</td>
<td align="right">2,111,011,870</td>
<td align="right">37.4%</td>
</tr>
<tr>
<td align="left">_PUSH_NULL</td>
<td align="right">801,002,110</td>
<td align="right">1,098,171,641</td>
<td align="right">37.1%</td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_O</td>
<td align="right">722,720,654</td>
<td align="right">986,156,454</td>
<td align="right">36.5%</td>
</tr>
<tr>
<td align="left">_MAKE_FUNCTION</td>
<td align="right">93,530,068</td>
<td align="right">127,343,244</td>
<td align="right">36.2%</td>
</tr>
<tr>
<td align="left">_LOAD_CONST_INLINE_BORROW_WITH_NULL</td>
<td align="right">442,426,478</td>
<td align="right">598,230,227</td>
<td align="right">35.2%</td>
</tr>
<tr>
<td align="left">_POP_TOP_LOAD_CONST_INLINE_BORROW</td>
<td align="right">1,847,973</td>
<td align="right">2,489,080</td>
<td align="right">34.7%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_0</td>
<td align="right">406,320,971</td>
<td align="right">546,876,884</td>
<td align="right">34.6%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_AND_CLEAR</td>
<td align="right">24,387,292</td>
<td align="right">32,697,863</td>
<td align="right">34.1%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_SLOT_0</td>
<td align="right">748,484,677</td>
<td align="right">1,003,338,299</td>
<td align="right">34.0%</td>
</tr>
<tr>
<td align="left">_BUILD_MAP</td>
<td align="right">19,364,103</td>
<td align="right">25,924,501</td>
<td align="right">33.9%</td>
</tr>
<tr>
<td align="left">_CHECK_PERIODIC</td>
<td align="right">2,546,247,589</td>
<td align="right">3,406,872,126</td>
<td align="right">33.8%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_TRUE_POP</td>
<td align="right">2,654,696,600</td>
<td align="right">3,536,296,928</td>
<td align="right">33.2%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_2</td>
<td align="right">3,048,997,879</td>
<td align="right">4,041,343,212</td>
<td align="right">32.5%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">922,302,670</td>
<td align="right">1,220,018,577</td>
<td align="right">32.3%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_1</td>
<td align="right">515,085,299</td>
<td align="right">678,912,007</td>
<td align="right">31.8%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_5</td>
<td align="right">659,238,836</td>
<td align="right">868,039,359</td>
<td align="right">31.7%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_3</td>
<td align="right">3,321,514,933</td>
<td align="right">4,364,875,303</td>
<td align="right">31.4%</td>
</tr>
<tr>
<td align="left">_FOR_ITER_GEN_FRAME</td>
<td align="right">100,741,399</td>
<td align="right">131,870,027</td>
<td align="right">30.9%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR</td>
<td align="right">1,006,541,552</td>
<td align="right">1,294,520,835</td>
<td align="right">28.6%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_1</td>
<td align="right">6,740,236,869</td>
<td align="right">8,668,620,507</td>
<td align="right">28.6%</td>
</tr>
<tr>
<td align="left">_BUILD_SLICE</td>
<td align="right">139,795,736</td>
<td align="right">179,732,340</td>
<td align="right">28.6%</td>
</tr>
<tr>
<td align="left">_STORE_FAST</td>
<td align="right">3,198,802,896</td>
<td align="right">4,111,482,924</td>
<td align="right">28.5%</td>
</tr>
<tr>
<td align="left">_ITER_NEXT_TUPLE</td>
<td align="right">225,690,260</td>
<td align="right">289,429,339</td>
<td align="right">28.2%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST</td>
<td align="right">6,187,313,237</td>
<td align="right">7,904,463,092</td>
<td align="right">27.8%</td>
</tr>
<tr>
<td align="left">_CALL_ISINSTANCE</td>
<td align="right">318,670,361</td>
<td align="right">406,932,647</td>
<td align="right">27.7%</td>
</tr>
<tr>
<td align="left">_CHECK_VALIDITY</td>
<td align="right">11,149,400,197</td>
<td align="right">14,232,839,258</td>
<td align="right">27.7%</td>
</tr>
<tr>
<td align="left">_CALL_TYPE_1</td>
<td align="right">281,987,909</td>
<td align="right">358,095,700</td>
<td align="right">27.0%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_4</td>
<td align="right">2,092,426,590</td>
<td align="right">2,652,177,238</td>
<td align="right">26.8%</td>
</tr>
<tr>
<td align="left">_BINARY_SUBSCR_STR_INT</td>
<td align="right">1,294,552,179</td>
<td align="right">1,634,736,714</td>
<td align="right">26.3%</td>
</tr>
<tr>
<td align="left">_COMPARE_OP_INT</td>
<td align="right">975,147,312</td>
<td align="right">1,225,165,308</td>
<td align="right">25.6%</td>
</tr>
<tr>
<td align="left">_CONTAINS_OP_DICT</td>
<td align="right">332,019,477</td>
<td align="right">416,439,186</td>
<td align="right">25.4%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_2</td>
<td align="right">737,171,348</td>
<td align="right">918,485,703</td>
<td align="right">24.6%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_INT</td>
<td align="right">201,179,750</td>
<td align="right">248,332,109</td>
<td align="right">23.4%</td>
</tr>
<tr>
<td align="left">_EXIT_TRACE</td>
<td align="right">2,809,463,814</td>
<td align="right">2,162,085,860</td>
<td align="right">-23.0%</td>
</tr>
<tr>
<td align="left">_LOAD_DEREF</td>
<td align="right">586,095,674</td>
<td align="right">716,221,890</td>
<td align="right">22.2%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_6</td>
<td align="right">1,313,345,297</td>
<td align="right">1,602,953,356</td>
<td align="right">22.1%</td>
</tr>
<tr>
<td align="left">_BINARY_OP</td>
<td align="right">987,348,943</td>
<td align="right">1,186,389,856</td>
<td align="right">20.2%</td>
</tr>
<tr>
<td align="left">_BINARY_SUBSCR_TUPLE_INT</td>
<td align="right">156,912,744</td>
<td align="right">187,864,415</td>
<td align="right">19.7%</td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">200,471,190</td>
<td align="right">239,976,496</td>
<td align="right">19.7%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_FALSE_POP</td>
<td align="right">5,496,048,551</td>
<td align="right">6,568,140,701</td>
<td align="right">19.5%</td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_O</td>
<td align="right">115,341,992</td>
<td align="right">137,613,020</td>
<td align="right">19.3%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_NONE</td>
<td align="right">174,102,773</td>
<td align="right">207,659,480</td>
<td align="right">19.3%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_5</td>
<td align="right">2,195,396,243</td>
<td align="right">2,612,369,298</td>
<td align="right">19.0%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_1</td>
<td align="right">1,959,060,031</td>
<td align="right">2,323,497,403</td>
<td align="right">18.6%</td>
</tr>
<tr>
<td align="left">_GUARD_BOTH_UNICODE</td>
<td align="right">964,436,696</td>
<td align="right">1,134,615,384</td>
<td align="right">17.6%</td>
</tr>
<tr>
<td align="left">_LOAD_CONST_INLINE_BORROW</td>
<td align="right">9,463,965,468</td>
<td align="right">11,131,020,261</td>
<td align="right">17.6%</td>
</tr>
<tr>
<td align="left">_DICT_MERGE</td>
<td align="right">8,686,907</td>
<td align="right">10,159,756</td>
<td align="right">17.0%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right">93,315,990</td>
<td align="right">109,044,764</td>
<td align="right">16.9%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_0</td>
<td align="right">200,194,940</td>
<td align="right">232,478,208</td>
<td align="right">16.1%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBTRACT_INT</td>
<td align="right">461,122,481</td>
<td align="right">534,904,400</td>
<td align="right">16.0%</td>
</tr>
<tr>
<td align="left">_GUARD_NOT_EXHAUSTED_TUPLE</td>
<td align="right">365,934,193</td>
<td align="right">423,140,090</td>
<td align="right">15.6%</td>
</tr>
<tr>
<td align="left">_COPY</td>
<td align="right">1,322,806,007</td>
<td align="right">1,526,527,776</td>
<td align="right">15.4%</td>
</tr>
<tr>
<td align="left">_ITER_CHECK_TUPLE</td>
<td align="right">407,578,766</td>
<td align="right">463,199,372</td>
<td align="right">13.6%</td>
</tr>
<tr>
<td align="left">_CONTAINS_OP_SET</td>
<td align="right">1,656,674,097</td>
<td align="right">1,875,478,186</td>
<td align="right">13.2%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_LIST</td>
<td align="right">58,074,781</td>
<td align="right">65,648,976</td>
<td align="right">13.0%</td>
</tr>
<tr>
<td align="left">_GUARD_TOS_INT</td>
<td align="right">211,504,219</td>
<td align="right">238,280,682</td>
<td align="right">12.7%</td>
</tr>
<tr>
<td align="left">_UNPACK_SEQUENCE_TUPLE</td>
<td align="right">225,523,816</td>
<td align="right">251,756,832</td>
<td align="right">11.6%</td>
</tr>
<tr>
<td align="left">_STORE_SUBSCR_LIST_INT</td>
<td align="right">488,609,786</td>
<td align="right">542,272,549</td>
<td align="right">11.0%</td>
</tr>
<tr>
<td align="left">_GUARD_BOTH_FLOAT</td>
<td align="right">908,068,547</td>
<td align="right">1,007,538,364</td>
<td align="right">11.0%</td>
</tr>
<tr>
<td align="left">_COMPARE_OP_STR</td>
<td align="right">1,824,591,011</td>
<td align="right">2,008,867,345</td>
<td align="right">10.1%</td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_FAST</td>
<td align="right">908,503,301</td>
<td align="right">999,265,717</td>
<td align="right">10.0%</td>
</tr>
<tr>
<td align="left">_SWAP</td>
<td align="right">1,215,770,880</td>
<td align="right">1,333,133,573</td>
<td align="right">9.7%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_4</td>
<td align="right">528,779,204</td>
<td align="right">579,441,783</td>
<td align="right">9.6%</td>
</tr>
<tr>
<td align="left">_LOAD_GLOBAL_BUILTINS</td>
<td align="right">53,269,524</td>
<td align="right">58,333,120</td>
<td align="right">9.5%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_MULTIPLY_FLOAT</td>
<td align="right">1,144,480,435</td>
<td align="right">1,252,664,875</td>
<td align="right">9.5%</td>
</tr>
<tr>
<td align="left">_COMPARE_OP_FLOAT</td>
<td align="right">101,262,414</td>
<td align="right">110,826,049</td>
<td align="right">9.4%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_7</td>
<td align="right">1,193,583,772</td>
<td align="right">1,304,096,330</td>
<td align="right">9.3%</td>
</tr>
<tr>
<td align="left">_LIST_APPEND</td>
<td align="right">172,855,267</td>
<td align="right">188,642,105</td>
<td align="right">9.1%</td>
</tr>
<tr>
<td align="left">_BINARY_SUBSCR</td>
<td align="right">1,334,545,142</td>
<td align="right">1,450,145,525</td>
<td align="right">8.7%</td>
</tr>
<tr>
<td align="left">_GUARD_TOS_FLOAT</td>
<td align="right">64,886,820</td>
<td align="right">70,416,220</td>
<td align="right">8.5%</td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_FAST_WITH_KEYWORDS</td>
<td align="right">92,268,292</td>
<td align="right">100,120,802</td>
<td align="right">8.5%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBTRACT_FLOAT</td>
<td align="right">383,035,460</td>
<td align="right">413,335,236</td>
<td align="right">7.9%</td>
</tr>
<tr>
<td align="left">_BUILD_LIST</td>
<td align="right">243,516,824</td>
<td align="right">262,622,595</td>
<td align="right">7.8%</td>
</tr>
<tr>
<td align="left">_UNARY_NOT</td>
<td align="right">64,718,143</td>
<td align="right">69,599,613</td>
<td align="right">7.5%</td>
</tr>
<tr>
<td align="left">_SIDE_EXIT</td>
<td align="right">4,607,011,821</td>
<td align="right">4,260,541,916</td>
<td align="right">-7.5%</td>
</tr>
<tr>
<td align="left">_LIST_EXTEND</td>
<td align="right">98,537,981</td>
<td align="right">105,396,635</td>
<td align="right">7.0%</td>
</tr>
<tr>
<td align="left">_GUARD_NOS_INT</td>
<td align="right">2,526,161,182</td>
<td align="right">2,700,413,259</td>
<td align="right">6.9%</td>
</tr>
<tr>
<td align="left">_CALL_INTRINSIC_1</td>
<td align="right">97,579,341</td>
<td align="right">104,075,097</td>
<td align="right">6.7%</td>
</tr>
<tr>
<td align="left">_BINARY_SUBSCR_LIST_INT</td>
<td align="right">1,100,114,200</td>
<td align="right">1,172,934,770</td>
<td align="right">6.6%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_ADD_INT</td>
<td align="right">2,596,945,710</td>
<td align="right">2,768,617,461</td>
<td align="right">6.6%</td>
</tr>
<tr>
<td align="left">_CALL_STR_1</td>
<td align="right">65,666,161</td>
<td align="right">69,919,780</td>
<td align="right">6.5%</td>
</tr>
<tr>
<td align="left">_GUARD_NOS_FLOAT</td>
<td align="right">645,081,736</td>
<td align="right">681,426,913</td>
<td align="right">5.6%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_7</td>
<td align="right">3,501,788,598</td>
<td align="right">3,694,761,577</td>
<td align="right">5.5%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_ADD_FLOAT</td>
<td align="right">588,453,700</td>
<td align="right">617,343,676</td>
<td align="right">4.9%</td>
</tr>
<tr>
<td align="left">_LOAD_GLOBAL</td>
<td align="right">213,740,867</td>
<td align="right">204,041,739</td>
<td align="right">-4.5%</td>
</tr>
<tr>
<td align="left">_BUILD_CONST_KEY_MAP</td>
<td align="right">4,837,300</td>
<td align="right">5,046,705</td>
<td align="right">4.3%</td>
</tr>
<tr>
<td align="left">_ITER_CHECK_RANGE</td>
<td align="right">785,353,879</td>
<td align="right">813,808,981</td>
<td align="right">3.6%</td>
</tr>
<tr>
<td align="left">_GUARD_NOT_EXHAUSTED_RANGE</td>
<td align="right">784,816,559</td>
<td align="right">813,206,281</td>
<td align="right">3.6%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_ADD_UNICODE</td>
<td align="right">23,910,917</td>
<td align="right">23,061,446</td>
<td align="right">-3.6%</td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_FAST_WITH_KEYWORDS</td>
<td align="right">148,537,940</td>
<td align="right">153,622,226</td>
<td align="right">3.4%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_MULTIPLY_INT</td>
<td align="right">186,151,823</td>
<td align="right">192,021,891</td>
<td align="right">3.2%</td>
</tr>
<tr>
<td align="left">_UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">610,589,936</td>
<td align="right">628,695,885</td>
<td align="right">3.0%</td>
</tr>
<tr>
<td align="left">_STORE_SLICE</td>
<td align="right">149,962,696</td>
<td align="right">154,281,720</td>
<td align="right">2.9%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_SLOT_1</td>
<td align="right">2,865,975</td>
<td align="right">2,946,700</td>
<td align="right">2.8%</td>
</tr>
<tr>
<td align="left">_JUMP_TO_TOP</td>
<td align="right">2,133,431,252</td>
<td align="right">2,191,547,615</td>
<td align="right">2.7%</td>
</tr>
<tr>
<td align="left">_GUARD_NOT_EXHAUSTED_LIST</td>
<td align="right">1,369,590,873</td>
<td align="right">1,333,330,603</td>
<td align="right">-2.6%</td>
</tr>
<tr>
<td align="left">_ITER_CHECK_LIST</td>
<td align="right">1,426,536,024</td>
<td align="right">1,390,656,134</td>
<td align="right">-2.5%</td>
</tr>
<tr>
<td align="left">_CONTAINS_OP</td>
<td align="right">133,900,126</td>
<td align="right">137,185,053</td>
<td align="right">2.5%</td>
</tr>
<tr>
<td align="left">_DEOPT</td>
<td align="right">208,934,837</td>
<td align="right">213,735,963</td>
<td align="right">2.3%</td>
</tr>
<tr>
<td align="left">_UNARY_INVERT</td>
<td align="right">12,967,827</td>
<td align="right">12,693,420</td>
<td align="right">-2.1%</td>
</tr>
<tr>
<td align="left">_MAP_ADD</td>
<td align="right">33,166,318</td>
<td align="right">32,651,856</td>
<td align="right">-1.6%</td>
</tr>
<tr>
<td align="left">_FOR_ITER_TIER_TWO</td>
<td align="right">553,721,683</td>
<td align="right">546,598,136</td>
<td align="right">-1.3%</td>
</tr>
<tr>
<td align="left">_TIER2_RESUME_CHECK</td>
<td align="right">4,788,500,978</td>
<td align="right">4,729,414,562</td>
<td align="right">-1.2%</td>
</tr>
<tr>
<td align="left">_GUARD_BUILTINS_VERSION</td>
<td align="right">45,823,824</td>
<td align="right">46,374,040</td>
<td align="right">1.2%</td>
</tr>
<tr>
<td align="left">_ITER_NEXT_LIST</td>
<td align="right">1,131,057,630</td>
<td align="right">1,117,538,390</td>
<td align="right">-1.2%</td>
</tr>
<tr>
<td align="left">_STORE_SUBSCR</td>
<td align="right">381,490,198</td>
<td align="right">385,003,247</td>
<td align="right">0.9%</td>
</tr>
<tr>
<td align="left">_ITER_NEXT_RANGE</td>
<td align="right">737,095,163</td>
<td align="right">741,597,285</td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">_UNPACK_SEQUENCE_LIST</td>
<td align="right">81,488,884</td>
<td align="right">81,913,554</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_CLASS_1</td>
<td align="right">20,499,134</td>
<td align="right">20,500,533</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_STORE_NAME</td>
<td align="right">543,659</td>
<td align="right">543,680</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_GET_ANEXT</td>
<td align="right">125,514,720</td>
<td align="right">125,514,720</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_RETURN_OFFSET</td>
<td align="right"></td>
<td align="right">1,584,776,408</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_YIELD_VALUE</td>
<td align="right"></td>
<td align="right">554,289,762</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_YIELD_OFFSET</td>
<td align="right"></td>
<td align="right">554,289,762</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_IS_NOT_PY_CALLABLE</td>
<td align="right"></td>
<td align="right">209,231,858</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_NON_PY_GENERAL</td>
<td align="right"></td>
<td align="right">206,659,598</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_PY_GENERAL</td>
<td align="right"></td>
<td align="right">197,127,275</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION_VERSION</td>
<td align="right"></td>
<td align="right">192,215,171</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_CONST</td>
<td align="right"></td>
<td align="right">181,153,634</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_PEP_523</td>
<td align="right"></td>
<td align="right">163,144,583</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_END_SEND</td>
<td align="right"></td>
<td align="right">27,485,620</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_METHOD_VERSION</td>
<td align="right"></td>
<td align="right">10,049,782</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_EXPAND_METHOD</td>
<td align="right"></td>
<td align="right">9,427,873</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_DELETE_FAST</td>
<td align="right"></td>
<td align="right">113,052</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_DICT_UPDATE</td>
<td align="right"></td>
<td align="right">6</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_SUPER_ATTR_ATTR</td>
<td align="right"></td>
<td align="right">6</td>
<td align="right"></td>
</tr>
</tbody>
</table>


</details>

### Pair counts

<details>
<summary> Pair counts for top 100 Non-JIT uop pairs </summary>


Pairs of specialized operations that deoptimize and are then followed by
the corresponding unspecialized instruction are not counted as pairs.

Not included in comparative output.


</details>

### Unsupported opcodes

<details>
<summary> unsupported opcodes </summary>

<table>
<thead>
<tr>
<th align="left">Opcode</th>
<th align="right">Base Count</th>
<th align="right">Head Count</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">STORE_ATTR_WITH_HINT</td>
<td align="right">220</td>
<td align="right">3,063</td>
<td align="right">1,292.3%</td>
</tr>
<tr>
<td align="left">RAISE_VARARGS</td>
<td align="right">63</td>
<td align="right">620</td>
<td align="right">884.1%</td>
</tr>
<tr>
<td align="left">IMPORT_NAME</td>
<td align="right">989</td>
<td align="right">5,705</td>
<td align="right">476.8%</td>
</tr>
<tr>
<td align="left">BEFORE_WITH</td>
<td align="right">400</td>
<td align="right">2,268</td>
<td align="right">467.0%</td>
</tr>
<tr>
<td align="left">SEND_GEN</td>
<td align="right">1,360</td>
<td align="right">1,999</td>
<td align="right">47.0%</td>
</tr>
<tr>
<td align="left">CALL_KW</td>
<td align="right">30,352</td>
<td align="right">44,531</td>
<td align="right">46.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_PROPERTY</td>
<td align="right">7,724</td>
<td align="right">10,530</td>
<td align="right">36.3%</td>
</tr>
<tr>
<td align="left">BINARY_OP_INPLACE_ADD_UNICODE</td>
<td align="right">469</td>
<td align="right">580</td>
<td align="right">23.7%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_GETITEM</td>
<td align="right">2,173</td>
<td align="right">2,680</td>
<td align="right">23.3%</td>
</tr>
<tr>
<td align="left">CALL_LIST_APPEND</td>
<td align="right">6,366</td>
<td align="right">7,765</td>
<td align="right">22.0%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">184,460</td>
<td align="right">146,820</td>
<td align="right">-20.4%</td>
</tr>
<tr>
<td align="left">SEND</td>
<td align="right">32,233</td>
<td align="right">38,515</td>
<td align="right">19.5%</td>
</tr>
<tr>
<td align="left">CALL_FUNCTION_EX</td>
<td align="right">39,436</td>
<td align="right">46,679</td>
<td align="right">18.4%</td>
</tr>
<tr>
<td align="left">BUILD_SET</td>
<td align="right">1,272</td>
<td align="right">1,080</td>
<td align="right">-15.1%</td>
</tr>
<tr>
<td align="left">CALL_ALLOC_AND_ENTER_INIT</td>
<td align="right">1,484</td>
<td align="right">1,605</td>
<td align="right">8.2%</td>
</tr>
<tr>
<td align="left">LOAD_NAME</td>
<td align="right">1,664</td>
<td align="right">1,660</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">CALL_PY_WITH_DEFAULTS</td>
<td align="right">5,831</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">RERAISE</td>
<td align="right"></td>
<td align="right">67</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_ATTR_GETATTRIBUTE_OVERRIDDEN</td>
<td align="right"></td>
<td align="right">20</td>
<td align="right"></td>
</tr>
</tbody>
</table>


</details>

### Optimizer errored out with opcode

<details>
<summary> Optimization stopped after encountering this opcode </summary>


</details>


</details>

## Rare events

<details>
<summary> Counts of rare/unlikely events </summary>

<table>
<thead>
<tr>
<th align="left">Event</th>
<th align="right">Base Count</th>
<th align="right">Head Count</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">
set bases
<details>
<summary>ⓘ</summary>

Setting the bases of a class, `cls.__bases__ = ...`
</details>
</td>
<td align="right">281</td>
<td align="right">240</td>
<td align="right">-14.6%</td>
</tr>
<tr>
<td align="left">
func modification
<details>
<summary>ⓘ</summary>

Modifying a function, e.g. `func.__defaults__ = ...`, etc.
</details>
</td>
<td align="right">442</td>
<td align="right">400</td>
<td align="right">-9.5%</td>
</tr>
<tr>
<td align="left">
watched dict modification
<details>
<summary>ⓘ</summary>

A watched dict has been modified
</details>
</td>
<td align="right">1,082</td>
<td align="right">1,096</td>
<td align="right">1.3%</td>
</tr>
<tr>
<td align="left">
watched globals modification
<details>
<summary>ⓘ</summary>

A watched `globals()` dict has been modified
</details>
</td>
<td align="right">1,082</td>
<td align="right">1,096</td>
<td align="right">1.3%</td>
</tr>
<tr>
<td align="left">
set class
<details>
<summary>ⓘ</summary>

Setting an object's class, `obj.__class__ = ...`
</details>
</td>
<td align="right">0</td>
<td align="right">0</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">
set eval frame func
<details>
<summary>ⓘ</summary>

Setting the PEP 523 frame eval function `_PyInterpreterState_SetFrameEvalFunc()`
</details>
</td>
<td align="right">0</td>
<td align="right">0</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">
builtin dict
<details>
<summary>ⓘ</summary>

Modifying the builtins, `__builtins__.__dict__[var] = ...`
</details>
</td>
<td align="right">0</td>
<td align="right">0</td>
<td align="right"></td>
</tr>
</tbody>
</table>


</details>

## Meta stats

<details>
<summary> Meta statistics </summary>

<table>
<thead>
<tr>
<th align="left"></th>
<th align="right">Base Count</th>
<th align="right">Head Count</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Number of data files</td>
<td align="right">1,981</td>
<td align="right">1,980</td>
<td align="right">-0.1%</td>
</tr>
</tbody>
</table>


</details>

---
Stats gathered on: 2024-05-03
