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
<td align="left">DELETE_NAME</td>
<td align="right">980</td>
<td align="right">165,285</td>
<td align="right">16,765.8%</td>
</tr>
<tr>
<td align="left">FORMAT_WITH_SPEC</td>
<td align="right">1,760</td>
<td align="right">212,596</td>
<td align="right">11,979.3%</td>
</tr>
<tr>
<td align="left">LOAD_BUILD_CLASS</td>
<td align="right">28,806</td>
<td align="right">1,660,963</td>
<td align="right">5,666.0%</td>
</tr>
<tr>
<td align="left">SETUP_ANNOTATIONS</td>
<td align="right">1,504</td>
<td align="right">58,141</td>
<td align="right">3,765.8%</td>
</tr>
<tr>
<td align="left">CALL_INTRINSIC_2</td>
<td align="right">80</td>
<td align="right">2,876</td>
<td align="right">3,495.0%</td>
</tr>
<tr>
<td align="left">STORE_NAME</td>
<td align="right">1,156,502</td>
<td align="right">31,325,971</td>
<td align="right">2,608.7%</td>
</tr>
<tr>
<td align="left">DICT_UPDATE</td>
<td align="right">71,899</td>
<td align="right">1,632,582</td>
<td align="right">2,170.7%</td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">342,949</td>
<td align="right">4,930,071</td>
<td align="right">1,337.6%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR</td>
<td align="right">23,807</td>
<td align="right">194,007</td>
<td align="right">714.9%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">1,396,186,612</td>
<td align="right">8,497,031,840</td>
<td align="right">508.6%</td>
</tr>
<tr>
<td align="left">SET_ADD</td>
<td align="right">2,424,366</td>
<td align="right">8,826,677</td>
<td align="right">264.1%</td>
</tr>
<tr>
<td align="left">LOAD_LOCALS</td>
<td align="right">2,260</td>
<td align="right">8,086</td>
<td align="right">257.8%</td>
</tr>
<tr>
<td align="left">LOAD_FROM_DICT_OR_DEREF</td>
<td align="right">2,240</td>
<td align="right">7,367</td>
<td align="right">228.9%</td>
</tr>
<tr>
<td align="left">DELETE_FAST</td>
<td align="right">2,228,696</td>
<td align="right">6,327,853</td>
<td align="right">183.9%</td>
</tr>
<tr>
<td align="left">LOAD_NAME</td>
<td align="right">14,134,707</td>
<td align="right">39,808,275</td>
<td align="right">181.6%</td>
</tr>
<tr>
<td align="left">RAISE_VARARGS</td>
<td align="right">6,195,856</td>
<td align="right">11,478,241</td>
<td align="right">85.3%</td>
</tr>
<tr>
<td align="left">RERAISE</td>
<td align="right">3,992,517</td>
<td align="right">7,324,621</td>
<td align="right">83.5%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE</td>
<td align="right">2,096,557</td>
<td align="right">3,633,682</td>
<td align="right">73.3%</td>
</tr>
<tr>
<td align="left">BEFORE_WITH</td>
<td align="right">9,822,744</td>
<td align="right">15,833,746</td>
<td align="right">61.2%</td>
</tr>
<tr>
<td align="left">CHECK_EXC_MATCH</td>
<td align="right">24,571,668</td>
<td align="right">38,429,870</td>
<td align="right">56.4%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">20,797,658</td>
<td align="right">31,365,226</td>
<td align="right">50.8%</td>
</tr>
<tr>
<td align="left">WITH_EXCEPT_START</td>
<td align="right">235,001</td>
<td align="right">348,626</td>
<td align="right">48.4%</td>
</tr>
<tr>
<td align="left">POP_EXCEPT</td>
<td align="right">25,059,156</td>
<td align="right">35,384,786</td>
<td align="right">41.2%</td>
</tr>
<tr>
<td align="left">PUSH_EXC_INFO</td>
<td align="right">25,059,303</td>
<td align="right">35,384,935</td>
<td align="right">41.2%</td>
</tr>
<tr>
<td align="left">TO_BOOL_STR</td>
<td align="right">105,671,612</td>
<td align="right">148,537,121</td>
<td align="right">40.6%</td>
</tr>
<tr>
<td align="left">MAP_ADD</td>
<td align="right">60,506,960</td>
<td align="right">84,659,883</td>
<td align="right">39.9%</td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">77,947,938</td>
<td align="right">104,047,139</td>
<td align="right">33.5%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_CLASS</td>
<td align="right">209,179,033</td>
<td align="right">274,609,171</td>
<td align="right">31.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_CHECK</td>
<td align="right">11,916,925</td>
<td align="right">15,564,879</td>
<td align="right">30.6%</td>
</tr>
<tr>
<td align="left">CLEANUP_THROW</td>
<td align="right">160,100</td>
<td align="right">206,098</td>
<td align="right">28.7%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">524,180,232</td>
<td align="right">653,776,793</td>
<td align="right">24.7%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_LIST</td>
<td align="right">89,810,119</td>
<td align="right">110,697,763</td>
<td align="right">23.3%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR_ATTR</td>
<td align="right">7,706,356</td>
<td align="right">9,481,975</td>
<td align="right">23.0%</td>
</tr>
<tr>
<td align="left">IMPORT_NAME</td>
<td align="right">12,483,951</td>
<td align="right">15,351,065</td>
<td align="right">23.0%</td>
</tr>
<tr>
<td align="left">BUILD_SET</td>
<td align="right">2,388,828</td>
<td align="right">2,908,472</td>
<td align="right">21.8%</td>
</tr>
<tr>
<td align="left">IMPORT_FROM</td>
<td align="right">13,155,385</td>
<td align="right">15,956,057</td>
<td align="right">21.3%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">221,123,175</td>
<td align="right">264,463,845</td>
<td align="right">19.6%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">592,211,456</td>
<td align="right">702,956,459</td>
<td align="right">18.7%</td>
</tr>
<tr>
<td align="left">STORE_FAST_STORE_FAST</td>
<td align="right">972,671,765</td>
<td align="right">1,153,223,282</td>
<td align="right">18.6%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST_WITH_KEYWORDS</td>
<td align="right">182,632,947</td>
<td align="right">212,360,729</td>
<td align="right">16.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_PROPERTY</td>
<td align="right">96,952,051</td>
<td align="right">112,493,191</td>
<td align="right">16.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL_LIST</td>
<td align="right">183,837,585</td>
<td align="right">213,242,490</td>
<td align="right">16.0%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">489,759,690</td>
<td align="right">562,224,484</td>
<td align="right">14.8%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">447,658,079</td>
<td align="right">513,100,295</td>
<td align="right">14.6%</td>
</tr>
<tr>
<td align="left">CALL_LIST_APPEND</td>
<td align="right">339,631,069</td>
<td align="right">389,197,947</td>
<td align="right">14.6%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">2,177,518,836</td>
<td align="right">2,477,338,979</td>
<td align="right">13.8%</td>
</tr>
<tr>
<td align="left">MAKE_FUNCTION</td>
<td align="right">155,933,803</td>
<td align="right">175,957,083</td>
<td align="right">12.8%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST_WITH_KEYWORDS</td>
<td align="right">131,761,522</td>
<td align="right">148,441,538</td>
<td align="right">12.7%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">397,801,116</td>
<td align="right">447,082,533</td>
<td align="right">12.4%</td>
</tr>
<tr>
<td align="left">BUILD_MAP</td>
<td align="right">137,149,141</td>
<td align="right">154,000,393</td>
<td align="right">12.3%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">963,758,073</td>
<td align="right">1,081,842,378</td>
<td align="right">12.3%</td>
</tr>
<tr>
<td align="left">BINARY_SLICE</td>
<td align="right">348,132,715</td>
<td align="right">390,194,705</td>
<td align="right">12.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_MODULE</td>
<td align="right">660,432,268</td>
<td align="right">738,113,913</td>
<td align="right">11.8%</td>
</tr>
<tr>
<td align="left">END_FOR</td>
<td align="right">83,007,828</td>
<td align="right">92,700,059</td>
<td align="right">11.7%</td>
</tr>
<tr>
<td align="left">STORE_FAST_LOAD_FAST</td>
<td align="right">238,982,089</td>
<td align="right">266,664,353</td>
<td align="right">11.6%</td>
</tr>
<tr>
<td align="left">BUILD_CONST_KEY_MAP</td>
<td align="right">13,555,672</td>
<td align="right">15,104,181</td>
<td align="right">11.4%</td>
</tr>
<tr>
<td align="left">CALL_TUPLE_1</td>
<td align="right">28,844,471</td>
<td align="right">32,117,851</td>
<td align="right">11.3%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">2,285,238,389</td>
<td align="right">2,528,568,582</td>
<td align="right">10.6%</td>
</tr>
<tr>
<td align="left">LIST_APPEND</td>
<td align="right">254,112,401</td>
<td align="right">280,510,761</td>
<td align="right">10.4%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">1,016,061,327</td>
<td align="right">1,115,828,890</td>
<td align="right">9.8%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">888,065,489</td>
<td align="right">974,179,450</td>
<td align="right">9.7%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NONE</td>
<td align="right">502,397,641</td>
<td align="right">550,287,792</td>
<td align="right">9.5%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">1,195,092,791</td>
<td align="right">1,307,039,996</td>
<td align="right">9.4%</td>
</tr>
<tr>
<td align="left">CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">270,083,181</td>
<td align="right">294,973,782</td>
<td align="right">9.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_AND_CLEAR</td>
<td align="right">86,760,546</td>
<td align="right">94,514,589</td>
<td align="right">8.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">1,498,937,550</td>
<td align="right">1,631,787,209</td>
<td align="right">8.9%</td>
</tr>
<tr>
<td align="left">DICT_MERGE</td>
<td align="right">48,482,649</td>
<td align="right">52,752,295</td>
<td align="right">8.8%</td>
</tr>
<tr>
<td align="left">BUILD_LIST</td>
<td align="right">468,976,437</td>
<td align="right">509,754,613</td>
<td align="right">8.7%</td>
</tr>
<tr>
<td align="left">CALL_LEN</td>
<td align="right">504,429,215</td>
<td align="right">548,084,941</td>
<td align="right">8.7%</td>
</tr>
<tr>
<td align="left">IS_OP</td>
<td align="right">838,976,898</td>
<td align="right">909,234,555</td>
<td align="right">8.4%</td>
</tr>
<tr>
<td align="left">FOR_ITER_GEN</td>
<td align="right">239,700,192</td>
<td align="right">259,356,187</td>
<td align="right">8.2%</td>
</tr>
<tr>
<td align="left">UNARY_INVERT</td>
<td align="right">14,386,738</td>
<td align="right">15,548,064</td>
<td align="right">8.1%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">4,606,199,779</td>
<td align="right">4,971,886,591</td>
<td align="right">7.9%</td>
</tr>
<tr>
<td align="left">CALL_STR_1</td>
<td align="right">109,924,328</td>
<td align="right">118,582,881</td>
<td align="right">7.9%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NOT_NONE</td>
<td align="right">768,461,479</td>
<td align="right">827,469,396</td>
<td align="right">7.7%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR</td>
<td align="right">445,311,915</td>
<td align="right">479,365,076</td>
<td align="right">7.6%</td>
</tr>
<tr>
<td align="left">CALL_KW</td>
<td align="right">270,032,241</td>
<td align="right">290,468,710</td>
<td align="right">7.6%</td>
</tr>
<tr>
<td align="left">CALL_FUNCTION_EX</td>
<td align="right">192,664,074</td>
<td align="right">206,974,989</td>
<td align="right">7.4%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">246,981,746</td>
<td align="right">264,684,144</td>
<td align="right">7.2%</td>
</tr>
<tr>
<td align="left">BUILD_STRING</td>
<td align="right">79,191,180</td>
<td align="right">84,557,642</td>
<td align="right">6.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">6,245,399,258</td>
<td align="right">6,664,562,422</td>
<td align="right">6.7%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TUPLE</td>
<td align="right">507,469,394</td>
<td align="right">541,474,811</td>
<td align="right">6.7%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_TUPLE_INT</td>
<td align="right">368,491,857</td>
<td align="right">392,575,313</td>
<td align="right">6.5%</td>
</tr>
<tr>
<td align="left">CALL_PY_WITH_DEFAULTS</td>
<td align="right">213,752,472</td>
<td align="right">227,440,986</td>
<td align="right">6.4%</td>
</tr>
<tr>
<td align="left">GET_YIELD_FROM_ITER</td>
<td align="right">47,656,799</td>
<td align="right">50,660,564</td>
<td align="right">6.3%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR_METHOD</td>
<td align="right">126,655,650</td>
<td align="right">134,629,376</td>
<td align="right">6.3%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">1,864,177,796</td>
<td align="right">1,980,757,977</td>
<td align="right">6.3%</td>
</tr>
<tr>
<td align="left">JUMP_FORWARD</td>
<td align="right">651,972,337</td>
<td align="right">691,777,918</td>
<td align="right">6.1%</td>
</tr>
<tr>
<td align="left">INTERPRETER_EXIT</td>
<td align="right">2,159,672,318</td>
<td align="right">2,291,249,972</td>
<td align="right">6.1%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">2,115,786,343</td>
<td align="right">2,242,845,036</td>
<td align="right">6.0%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">1,295,834,942</td>
<td align="right">1,373,556,850</td>
<td align="right">6.0%</td>
</tr>
<tr>
<td align="left">FOR_ITER_TUPLE</td>
<td align="right">615,202,727</td>
<td align="right">650,882,197</td>
<td align="right">5.8%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">4,747,692,960</td>
<td align="right">5,016,744,252</td>
<td align="right">5.7%</td>
</tr>
<tr>
<td align="left">SET_FUNCTION_ATTRIBUTE</td>
<td align="right">132,032,600</td>
<td align="right">139,496,169</td>
<td align="right">5.7%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_STR</td>
<td align="right">2,161,865,330</td>
<td align="right">2,284,070,988</td>
<td align="right">5.7%</td>
</tr>
<tr>
<td align="left">TO_BOOL_INT</td>
<td align="right">342,018,016</td>
<td align="right">361,116,543</td>
<td align="right">5.6%</td>
</tr>
<tr>
<td align="left">FORMAT_SIMPLE</td>
<td align="right">158,787,550</td>
<td align="right">167,575,620</td>
<td align="right">5.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">43,238,203,822</td>
<td align="right">45,626,045,092</td>
<td align="right">5.5%</td>
</tr>
<tr>
<td align="left">PUSH_NULL</td>
<td align="right">1,948,663,839</td>
<td align="right">2,054,046,319</td>
<td align="right">5.4%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_DICT</td>
<td align="right">276,582,543</td>
<td align="right">291,465,848</td>
<td align="right">5.4%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">8,185,864,757</td>
<td align="right">8,625,364,771</td>
<td align="right">5.4%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">14,669,410,994</td>
<td align="right">15,434,836,067</td>
<td align="right">5.2%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">4,954,139,390</td>
<td align="right">5,209,598,910</td>
<td align="right">5.2%</td>
</tr>
<tr>
<td align="left">COPY_FREE_VARS</td>
<td align="right">364,733,913</td>
<td align="right">383,276,460</td>
<td align="right">5.1%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">5,862,235,306</td>
<td align="right">6,159,691,091</td>
<td align="right">5.1%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT</td>
<td align="right">2,170,573,359</td>
<td align="right">2,280,543,762</td>
<td align="right">5.1%</td>
</tr>
<tr>
<td align="left">CALL_ISINSTANCE</td>
<td align="right">1,141,660,357</td>
<td align="right">1,198,901,610</td>
<td align="right">5.0%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_O</td>
<td align="right">420,760,658</td>
<td align="right">441,157,027</td>
<td align="right">4.8%</td>
</tr>
<tr>
<td align="left">EXIT_INIT_CHECK</td>
<td align="right">95,006,428</td>
<td align="right">99,601,170</td>
<td align="right">4.8%</td>
</tr>
<tr>
<td align="left">TO_BOOL_NONE</td>
<td align="right">643,829,467</td>
<td align="right">674,898,066</td>
<td align="right">4.8%</td>
</tr>
<tr>
<td align="left">CALL_ALLOC_AND_ENTER_INIT</td>
<td align="right">97,294,870</td>
<td align="right">101,967,053</td>
<td align="right">4.8%</td>
</tr>
<tr>
<td align="left">NOP</td>
<td align="right">2,135,076,707</td>
<td align="right">2,236,632,064</td>
<td align="right">4.8%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">4,220,433,885</td>
<td align="right">4,417,889,360</td>
<td align="right">4.7%</td>
</tr>
<tr>
<td align="left">MAKE_CELL</td>
<td align="right">111,478,841</td>
<td align="right">116,682,768</td>
<td align="right">4.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">2,879,194,948</td>
<td align="right">3,011,333,417</td>
<td align="right">4.6%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">14,734,186,657</td>
<td align="right">15,399,007,198</td>
<td align="right">4.5%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">4,301,344,193</td>
<td align="right">4,494,900,441</td>
<td align="right">4.5%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">12,570,513,240</td>
<td align="right">13,122,398,133</td>
<td align="right">4.4%</td>
</tr>
<tr>
<td align="left">SET_UPDATE</td>
<td align="right">200,448</td>
<td align="right">209,061</td>
<td align="right">4.3%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">5,057,148,373</td>
<td align="right">5,270,503,295</td>
<td align="right">4.2%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_GETITEM</td>
<td align="right">195,175,119</td>
<td align="right">202,978,489</td>
<td align="right">4.0%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">1,600,290,417</td>
<td align="right">1,661,529,383</td>
<td align="right">3.8%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD_NO_INTERRUPT</td>
<td align="right">556,710,692</td>
<td align="right">577,471,532</td>
<td align="right">3.7%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_SLOT</td>
<td align="right">1,635,080,159</td>
<td align="right">1,695,480,811</td>
<td align="right">3.7%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">1,817,018,938</td>
<td align="right">1,883,954,210</td>
<td align="right">3.7%</td>
</tr>
<tr>
<td align="left">RETURN_GENERATOR</td>
<td align="right">502,823,757</td>
<td align="right">520,785,786</td>
<td align="right">3.6%</td>
</tr>
<tr>
<td align="left">TO_BOOL_ALWAYS_TRUE</td>
<td align="right">297,616,759</td>
<td align="right">307,666,350</td>
<td align="right">3.4%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">11,646,942,187</td>
<td align="right">12,029,731,765</td>
<td align="right">3.3%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_LIST_INT</td>
<td align="right">1,506,906,325</td>
<td align="right">1,551,680,170</td>
<td align="right">3.0%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP_DICT</td>
<td align="right">538,267,539</td>
<td align="right">554,245,035</td>
<td align="right">3.0%</td>
</tr>
<tr>
<td align="left">YIELD_VALUE</td>
<td align="right">1,405,212,086</td>
<td align="right">1,445,328,578</td>
<td align="right">2.9%</td>
</tr>
<tr>
<td align="left">SEND_GEN</td>
<td align="right">787,171,307</td>
<td align="right">809,495,884</td>
<td align="right">2.8%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST</td>
<td align="right">1,318,219,755</td>
<td align="right">1,355,538,036</td>
<td align="right">2.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right">219,494,019</td>
<td align="right">225,649,723</td>
<td align="right">2.8%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">1,179,662,905</td>
<td align="right">1,212,423,229</td>
<td align="right">2.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_WITH_HINT</td>
<td align="right">478,789,836</td>
<td align="right">491,959,628</td>
<td align="right">2.8%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR</td>
<td align="right">1,524,412,312</td>
<td align="right">1,566,217,604</td>
<td align="right">2.7%</td>
</tr>
<tr>
<td align="left">STORE_DEREF</td>
<td align="right">98,206,595</td>
<td align="right">100,880,983</td>
<td align="right">2.7%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_STR_INT</td>
<td align="right">1,675,397,763</td>
<td align="right">1,720,695,301</td>
<td align="right">2.7%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_DICT</td>
<td align="right">839,380,101</td>
<td align="right">862,049,472</td>
<td align="right">2.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_CLASS</td>
<td align="right">184,973,038</td>
<td align="right">189,905,168</td>
<td align="right">2.7%</td>
</tr>
<tr>
<td align="left">STORE_GLOBAL</td>
<td align="right">8,205,240</td>
<td align="right">8,417,880</td>
<td align="right">2.6%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_O</td>
<td align="right">1,262,721,092</td>
<td align="right">1,294,320,474</td>
<td align="right">2.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">2,471,612,285</td>
<td align="right">2,530,080,938</td>
<td align="right">2.4%</td>
</tr>
<tr>
<td align="left">UNARY_NOT</td>
<td align="right">90,546,759</td>
<td align="right">92,307,597</td>
<td align="right">1.9%</td>
</tr>
<tr>
<td align="left">LIST_EXTEND</td>
<td align="right">124,384,742</td>
<td align="right">126,802,451</td>
<td align="right">1.9%</td>
</tr>
<tr>
<td align="left">CALL_TYPE_1</td>
<td align="right">480,816,339</td>
<td align="right">489,853,152</td>
<td align="right">1.9%</td>
</tr>
<tr>
<td align="left">FOR_ITER_RANGE</td>
<td align="right">841,752,952</td>
<td align="right">857,452,096</td>
<td align="right">1.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_NO_DICT</td>
<td align="right">102,639,284</td>
<td align="right">104,532,114</td>
<td align="right">1.8%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_WITH_HINT</td>
<td align="right">67,299,989</td>
<td align="right">68,422,522</td>
<td align="right">1.7%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP_SET</td>
<td align="right">1,945,260,058</td>
<td align="right">1,973,415,711</td>
<td align="right">1.4%</td>
</tr>
<tr>
<td align="left">DELETE_ATTR</td>
<td align="right">6,768,985</td>
<td align="right">6,861,976</td>
<td align="right">1.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_LAZY_DICT</td>
<td align="right">352,763,164</td>
<td align="right">357,534,481</td>
<td align="right">1.4%</td>
</tr>
<tr>
<td align="left">CONVERT_VALUE</td>
<td align="right">139,680,220</td>
<td align="right">140,887,455</td>
<td align="right">0.9%</td>
</tr>
<tr>
<td align="left">CALL_INTRINSIC_1</td>
<td align="right">248,966,940</td>
<td align="right">251,092,057</td>
<td align="right">0.9%</td>
</tr>
<tr>
<td align="left">END_SEND</td>
<td align="right">402,753,126</td>
<td align="right">406,120,546</td>
<td align="right">0.8%</td>
</tr>
<tr>
<td align="left">DELETE_SUBSCR</td>
<td align="right">177,941,055</td>
<td align="right">178,992,656</td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">BUILD_SLICE</td>
<td align="right">211,843,949</td>
<td align="right">212,788,723</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_LIST_INT</td>
<td align="right">586,799,785</td>
<td align="right">589,050,353</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_FLOAT</td>
<td align="right">251,141,295</td>
<td align="right">251,868,466</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">UNARY_NEGATIVE</td>
<td align="right">171,057,924</td>
<td align="right">171,540,898</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">INSTRUMENTED_JUMP_BACKWARD</td>
<td align="right">10,016</td>
<td align="right">9,988</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">INSTRUMENTED_FOR_ITER</td>
<td align="right">11,376</td>
<td align="right">11,348</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">INSTRUMENTED_POP_JUMP_IF_TRUE</td>
<td align="right">13,456</td>
<td align="right">13,428</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">GET_AWAITABLE</td>
<td align="right">229,785,451</td>
<td align="right">230,236,065</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">STORE_SLICE</td>
<td align="right">162,468,514</td>
<td align="right">162,732,904</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">SEND</td>
<td align="right">173,949,177</td>
<td align="right">174,225,169</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">UNPACK_EX</td>
<td align="right">1,129,926</td>
<td align="right">1,131,229</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_INT</td>
<td align="right">3,165,861,915</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BINARY_OP_MULTIPLY_FLOAT</td>
<td align="right">1,382,501,217</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_INT</td>
<td align="right">832,962,266</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_FLOAT</td>
<td align="right">666,876,876</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_FLOAT</td>
<td align="right">460,013,839</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BINARY_OP_MULTIPLY_INT</td>
<td align="right">361,396,073</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">GET_ANEXT</td>
<td align="right">133,515,680</td>
<td align="right">133,515,680</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_UNICODE</td>
<td align="right">99,007,196</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">INSTRUMENTED_POP_JUMP_IF_FALSE</td>
<td align="right">38,888,320</td>
<td align="right">38,888,320</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">INSTRUMENTED_RESUME</td>
<td align="right">38,864,500</td>
<td align="right">38,864,500</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">INSTRUMENTED_RETURN_VALUE</td>
<td align="right">38,856,560</td>
<td align="right">38,856,560</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_INPLACE_ADD_UNICODE</td>
<td align="right">9,137,077</td>
<td align="right"></td>
<td align="right"></td>
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
<td align="left">BEFORE_ASYNC_WITH</td>
<td align="right">3,005,920</td>
<td align="right">3,005,920</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_GETATTRIBUTE_OVERRIDDEN</td>
<td align="right">99,800</td>
<td align="right">99,800</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">INSTRUMENTED_RETURN_CONST</td>
<td align="right">6,240</td>
<td align="right">6,240</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">INSTRUMENTED_POP_JUMP_IF_NONE</td>
<td align="right">720</td>
<td align="right">720</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">INSTRUMENTED_JUMP_FORWARD</td>
<td align="right">400</td>
<td align="right">400</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">INSTRUMENTED_POP_JUMP_IF_NOT_NONE</td>
<td align="right">400</td>
<td align="right">400</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">MATCH_CLASS</td>
<td align="right"></td>
<td align="right">84,108</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">MATCH_SEQUENCE</td>
<td align="right"></td>
<td align="right">1,028</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">GET_LEN</td>
<td align="right"></td>
<td align="right">824</td>
<td align="right"></td>
</tr>
</tbody>
</table>


</details>

## Pair counts

<details>
<summary> Pair counts for top 100 Tier 1 instructions </summary>


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
<td align="right">1,443,865,082</td>
<td align="right">17.2%</td>
<td align="right">8,493,069,782</td>
<td align="right">100.0%</td>
<td align="right">488.2%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">6,927,344,661</td>
<td align="right">82.7%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">50,411,798</td>
<td align="right">0.6%</td>
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
<td align="right">1,728,804</td>
<td align="right">63.2%</td>
<td align="right">3,962,058</td>
<td align="right">100.0%</td>
<td align="right">129.2%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">1,004,524</td>
<td align="right">36.8%</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right">-100.0%</td>
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
<td align="left">and other</td>
<td align="right">2,035</td>
<td align="right">0.1%</td>
<td align="right">782,571</td>
<td align="right">19.8%</td>
<td align="right">38,355.6%</td>
</tr>
<tr>
<td align="left">and different types</td>
<td align="right">619</td>
<td align="right">0.0%</td>
<td align="right">39,880</td>
<td align="right">1.0%</td>
<td align="right">6,342.6%</td>
</tr>
<tr>
<td align="left">add other</td>
<td align="right">75,586</td>
<td align="right">4.4%</td>
<td align="right">493,787</td>
<td align="right">12.5%</td>
<td align="right">553.3%</td>
</tr>
<tr>
<td align="left">power</td>
<td align="right">13,749</td>
<td align="right">0.8%</td>
<td align="right">41,155</td>
<td align="right">1.0%</td>
<td align="right">199.3%</td>
</tr>
<tr>
<td align="left">remainder</td>
<td align="right">68,019</td>
<td align="right">3.9%</td>
<td align="right">20</td>
<td align="right">0.0%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">or</td>
<td align="right">19,671</td>
<td align="right">1.1%</td>
<td align="right">180</td>
<td align="right">0.0%</td>
<td align="right">-99.1%</td>
</tr>
<tr>
<td align="left">rshift</td>
<td align="right">37,334</td>
<td align="right">2.2%</td>
<td align="right">3,860</td>
<td align="right">0.1%</td>
<td align="right">-89.7%</td>
</tr>
<tr>
<td align="left">lshift</td>
<td align="right">29,569</td>
<td align="right">1.7%</td>
<td align="right">3,640</td>
<td align="right">0.1%</td>
<td align="right">-87.7%</td>
</tr>
<tr>
<td align="left">subtract different types</td>
<td align="right">779,722</td>
<td align="right">45.1%</td>
<td align="right">103,913</td>
<td align="right">2.6%</td>
<td align="right">-86.7%</td>
</tr>
<tr>
<td align="left">add different types</td>
<td align="right">217,918</td>
<td align="right">12.6%</td>
<td align="right">38,496</td>
<td align="right">1.0%</td>
<td align="right">-82.3%</td>
</tr>
<tr>
<td align="left">true divide different types</td>
<td align="right">29,666</td>
<td align="right">1.7%</td>
<td align="right">5,875</td>
<td align="right">0.1%</td>
<td align="right">-80.2%</td>
</tr>
<tr>
<td align="left">floor divide</td>
<td align="right">52,608</td>
<td align="right">3.0%</td>
<td align="right">14,580</td>
<td align="right">0.4%</td>
<td align="right">-72.3%</td>
</tr>
<tr>
<td align="left">and int</td>
<td align="right">75,183</td>
<td align="right">4.3%</td>
<td align="right">36,884</td>
<td align="right">0.9%</td>
<td align="right">-50.9%</td>
</tr>
<tr>
<td align="left">subtract other</td>
<td align="right">16,234</td>
<td align="right">0.9%</td>
<td align="right">12,640</td>
<td align="right">0.3%</td>
<td align="right">-22.1%</td>
</tr>
<tr>
<td align="left">multiply other</td>
<td align="right">5,500</td>
<td align="right">0.3%</td>
<td align="right">5,484</td>
<td align="right">0.1%</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">multiply different types</td>
<td align="right">254,197</td>
<td align="right">14.7%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">xor</td>
<td align="right">29,507</td>
<td align="right">1.7%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">true divide float</td>
<td align="right">18,167</td>
<td align="right">1.1%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">true divide other</td>
<td align="right">3,520</td>
<td align="right">0.2%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">other</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">1,191,700</td>
<td align="right">30.1%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">expected error</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">560,283</td>
<td align="right">14.1%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">no dict</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">373,222</td>
<td align="right">9.4%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">wrong number arguments</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">100,215</td>
<td align="right">2.5%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">overridden</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">58,841</td>
<td align="right">1.5%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">code complex parameters</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">37,451</td>
<td align="right">0.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">out of versions</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">31,171</td>
<td align="right">0.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">code not optimized</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">17,300</td>
<td align="right">0.4%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">matrix multiply</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">8,910</td>
<td align="right">0.2%</td>
<td align="right"></td>
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
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">5,117,715</td>
<td align="right">0.1%</td>
<td align="right">8,561,597</td>
<td align="right">0.1%</td>
<td align="right">67.3%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">4,580,233,450</td>
<td align="right">75.0%</td>
<td align="right">4,721,417,148</td>
<td align="right">75.0%</td>
<td align="right">3.1%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">1,528,858,497</td>
<td align="right">25.0%</td>
<td align="right">1,573,490,467</td>
<td align="right">25.0%</td>
<td align="right">2.9%</td>
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
<td align="right">206,117</td>
<td align="right">30.7%</td>
<td align="right">620,996</td>
<td align="right">48.2%</td>
<td align="right">201.3%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">465,413</td>
<td align="right">69.3%</td>
<td align="right">667,738</td>
<td align="right">51.8%</td>
<td align="right">43.5%</td>
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
<td align="left">string slice</td>
<td align="right">100</td>
<td align="right">0.0%</td>
<td align="right">5,644</td>
<td align="right">0.8%</td>
<td align="right">5,544.0%</td>
</tr>
<tr>
<td align="left">tuple slice</td>
<td align="right">187</td>
<td align="right">0.0%</td>
<td align="right">1,758</td>
<td align="right">0.3%</td>
<td align="right">840.1%</td>
</tr>
<tr>
<td align="left">buffer slice</td>
<td align="right">980</td>
<td align="right">0.2%</td>
<td align="right">5,798</td>
<td align="right">0.9%</td>
<td align="right">491.6%</td>
</tr>
<tr>
<td align="left">sequence int</td>
<td align="right">4,300</td>
<td align="right">0.9%</td>
<td align="right">13,668</td>
<td align="right">2.0%</td>
<td align="right">217.9%</td>
</tr>
<tr>
<td align="left">code complex parameters</td>
<td align="right">5,036</td>
<td align="right">1.1%</td>
<td align="right">14,802</td>
<td align="right">2.2%</td>
<td align="right">193.9%</td>
</tr>
<tr>
<td align="left">out of range</td>
<td align="right">88,149</td>
<td align="right">18.9%</td>
<td align="right">167,421</td>
<td align="right">25.1%</td>
<td align="right">89.9%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">125,201</td>
<td align="right">26.9%</td>
<td align="right">204,601</td>
<td align="right">30.6%</td>
<td align="right">63.4%</td>
</tr>
<tr>
<td align="left">list slice</td>
<td align="right">34,680</td>
<td align="right">7.5%</td>
<td align="right">41,903</td>
<td align="right">6.3%</td>
<td align="right">20.8%</td>
</tr>
<tr>
<td align="left">buffer int</td>
<td align="right">49,180</td>
<td align="right">10.6%</td>
<td align="right">54,355</td>
<td align="right">8.1%</td>
<td align="right">10.5%</td>
</tr>
<tr>
<td align="left">array int</td>
<td align="right">157,600</td>
<td align="right">33.9%</td>
<td align="right">157,788</td>
<td align="right">23.6%</td>
<td align="right">0.1%</td>
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
deopt
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">41,300</td>
<td align="right">0.0%</td>
<td align="right">83,342</td>
<td align="right">0.0%</td>
<td align="right">101.8%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">1,449,963,227</td>
<td align="right">10.7%</td>
<td align="right">1,578,968,066</td>
<td align="right">10.9%</td>
<td align="right">8.9%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">261,398,873</td>
<td align="right">1.9%</td>
<td align="right">284,497,774</td>
<td align="right">2.0%</td>
<td align="right">8.8%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">12,055,610,474</td>
<td align="right">89.2%</td>
<td align="right">12,840,616,277</td>
<td align="right">89.0%</td>
<td align="right">6.5%</td>
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
<td align="right">966,793</td>
<td align="right">14.8%</td>
<td align="right">3,159,541</td>
<td align="right">25.1%</td>
<td align="right">226.8%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">5,561,644</td>
<td align="right">85.2%</td>
<td align="right">9,410,163</td>
<td align="right">74.9%</td>
<td align="right">69.2%</td>
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
<td align="left">cfunc varargs</td>
<td align="right">14,089</td>
<td align="right">1.5%</td>
<td align="right">151,114</td>
<td align="right">4.8%</td>
<td align="right">972.6%</td>
</tr>
<tr>
<td align="left">method wrapper</td>
<td align="right">8,190</td>
<td align="right">0.8%</td>
<td align="right">66,835</td>
<td align="right">2.1%</td>
<td align="right">716.1%</td>
</tr>
<tr>
<td align="left">operator wrapper</td>
<td align="right">10,120</td>
<td align="right">1.0%</td>
<td align="right">72,088</td>
<td align="right">2.3%</td>
<td align="right">612.3%</td>
</tr>
<tr>
<td align="left">class mutable</td>
<td align="right">24,145</td>
<td align="right">2.5%</td>
<td align="right">162,596</td>
<td align="right">5.1%</td>
<td align="right">573.4%</td>
</tr>
<tr>
<td align="left">cfunc noargs</td>
<td align="right">69,704</td>
<td align="right">7.2%</td>
<td align="right">434,319</td>
<td align="right">13.7%</td>
<td align="right">523.1%</td>
</tr>
<tr>
<td align="left">meth descr varargs keywords</td>
<td align="right">20,733</td>
<td align="right">2.1%</td>
<td align="right">101,170</td>
<td align="right">3.2%</td>
<td align="right">388.0%</td>
</tr>
<tr>
<td align="left">meth descr varargs</td>
<td align="right">18,586</td>
<td align="right">1.9%</td>
<td align="right">90,439</td>
<td align="right">2.9%</td>
<td align="right">386.6%</td>
</tr>
<tr>
<td align="left">code complex parameters</td>
<td align="right">184,628</td>
<td align="right">19.1%</td>
<td align="right">825,655</td>
<td align="right">26.1%</td>
<td align="right">347.2%</td>
</tr>
<tr>
<td align="left">cfunc varargs keywords</td>
<td align="right">32,019</td>
<td align="right">3.3%</td>
<td align="right">128,266</td>
<td align="right">4.1%</td>
<td align="right">300.6%</td>
</tr>
<tr>
<td align="left">class no vectorcall</td>
<td align="right">77,643</td>
<td align="right">8.0%</td>
<td align="right">306,482</td>
<td align="right">9.7%</td>
<td align="right">294.7%</td>
</tr>
<tr>
<td align="left">init not python</td>
<td align="right">16,426</td>
<td align="right">1.7%</td>
<td align="right">60,200</td>
<td align="right">1.9%</td>
<td align="right">266.5%</td>
</tr>
<tr>
<td align="left">wrong number arguments</td>
<td align="right">13,773</td>
<td align="right">1.4%</td>
<td align="right">39,376</td>
<td align="right">1.2%</td>
<td align="right">185.9%</td>
</tr>
<tr>
<td align="left">bound method</td>
<td align="right">11,957</td>
<td align="right">1.2%</td>
<td align="right">28,925</td>
<td align="right">0.9%</td>
<td align="right">141.9%</td>
</tr>
<tr>
<td align="left">metaclass</td>
<td align="right">43,068</td>
<td align="right">4.5%</td>
<td align="right">92,155</td>
<td align="right">2.9%</td>
<td align="right">114.0%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">78,495</td>
<td align="right">8.1%</td>
<td align="right">161,459</td>
<td align="right">5.1%</td>
<td align="right">105.7%</td>
</tr>
<tr>
<td align="left">init not simple</td>
<td align="right">12,278</td>
<td align="right">1.3%</td>
<td align="right">23,523</td>
<td align="right">0.7%</td>
<td align="right">91.6%</td>
</tr>
<tr>
<td align="left">cmethod</td>
<td align="right">14,100</td>
<td align="right">1.5%</td>
<td align="right">24,430</td>
<td align="right">0.8%</td>
<td align="right">73.3%</td>
</tr>
<tr>
<td align="left">str</td>
<td align="right">3,200</td>
<td align="right">0.3%</td>
<td align="right">5,029</td>
<td align="right">0.2%</td>
<td align="right">57.2%</td>
</tr>
<tr>
<td align="left">init not inline values</td>
<td align="right">105,696</td>
<td align="right">10.9%</td>
<td align="right">130,230</td>
<td align="right">4.1%</td>
<td align="right">23.2%</td>
</tr>
<tr>
<td align="left">meth descr method fastcall keywords</td>
<td align="right">207,123</td>
<td align="right">21.4%</td>
<td align="right">254,430</td>
<td align="right">8.1%</td>
<td align="right">22.8%</td>
</tr>
<tr>
<td align="left">out of versions</td>
<td align="right">980</td>
<td align="right">0.1%</td>
<td align="right">990</td>
<td align="right">0.0%</td>
<td align="right">1.0%</td>
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
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">1,941,764</td>
<td align="right">0.0%</td>
<td align="right">2,787,466</td>
<td align="right">0.1%</td>
<td align="right">43.6%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">248,546,168</td>
<td align="right">5.1%</td>
<td align="right">266,315,100</td>
<td align="right">5.2%</td>
<td align="right">7.1%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">4,581,638,220</td>
<td align="right">94.8%</td>
<td align="right">4,813,695,750</td>
<td align="right">94.7%</td>
<td align="right">5.1%</td>
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
<td align="right">114,765</td>
<td align="right">30.4%</td>
<td align="right">598,055</td>
<td align="right">51.7%</td>
<td align="right">421.1%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">262,577</td>
<td align="right">69.6%</td>
<td align="right">558,455</td>
<td align="right">48.3%</td>
<td align="right">112.7%</td>
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
<td align="right">4,474</td>
<td align="right">1.7%</td>
<td align="right">46,496</td>
<td align="right">8.3%</td>
<td align="right">939.2%</td>
</tr>
<tr>
<td align="left">bytes</td>
<td align="right">4,860</td>
<td align="right">1.9%</td>
<td align="right">26,424</td>
<td align="right">4.7%</td>
<td align="right">443.7%</td>
</tr>
<tr>
<td align="left">big int</td>
<td align="right">63,959</td>
<td align="right">24.4%</td>
<td align="right">165,242</td>
<td align="right">29.6%</td>
<td align="right">158.4%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">25,190</td>
<td align="right">9.6%</td>
<td align="right">58,453</td>
<td align="right">10.5%</td>
<td align="right">132.0%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">15,082</td>
<td align="right">5.7%</td>
<td align="right">32,612</td>
<td align="right">5.8%</td>
<td align="right">116.2%</td>
</tr>
<tr>
<td align="left">different types</td>
<td align="right">59,257</td>
<td align="right">22.6%</td>
<td align="right">111,292</td>
<td align="right">19.9%</td>
<td align="right">87.8%</td>
</tr>
<tr>
<td align="left">float long</td>
<td align="right">21,076</td>
<td align="right">8.0%</td>
<td align="right">36,901</td>
<td align="right">6.6%</td>
<td align="right">75.1%</td>
</tr>
<tr>
<td align="left">bool</td>
<td align="right">5,863</td>
<td align="right">2.2%</td>
<td align="right">8,264</td>
<td align="right">1.5%</td>
<td align="right">41.0%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">10,363</td>
<td align="right">3.9%</td>
<td align="right">14,490</td>
<td align="right">2.6%</td>
<td align="right">39.8%</td>
</tr>
<tr>
<td align="left">baseobject</td>
<td align="right">39,746</td>
<td align="right">15.1%</td>
<td align="right">45,273</td>
<td align="right">8.1%</td>
<td align="right">13.9%</td>
</tr>
<tr>
<td align="left">long float</td>
<td align="right">1,587</td>
<td align="right">0.6%</td>
<td align="right">1,665</td>
<td align="right">0.3%</td>
<td align="right">4.9%</td>
</tr>
<tr>
<td align="left">string</td>
<td align="right">11,120</td>
<td align="right">4.2%</td>
<td align="right">11,343</td>
<td align="right">2.0%</td>
<td align="right">2.0%</td>
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
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">223,408,114</td>
<td align="right">8.3%</td>
<td align="right">266,086,252</td>
<td align="right">9.5%</td>
<td align="right">19.1%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">2,481,014,417</td>
<td align="right">91.7%</td>
<td align="right">2,525,139,759</td>
<td align="right">90.4%</td>
<td align="right">1.8%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">2,513,180</td>
<td align="right">0.1%</td>
<td align="right">2,520,987</td>
<td align="right">0.1%</td>
<td align="right">0.3%</td>
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
<td align="right">161,218</td>
<td align="right">70.6%</td>
<td align="right">651,752</td>
<td align="right">72.5%</td>
<td align="right">304.3%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">67,023</td>
<td align="right">29.4%</td>
<td align="right">246,828</td>
<td align="right">27.5%</td>
<td align="right">268.3%</td>
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
<td align="left">tuple</td>
<td align="right">49,401</td>
<td align="right">30.6%</td>
<td align="right">258,129</td>
<td align="right">39.6%</td>
<td align="right">422.5%</td>
</tr>
<tr>
<td align="left">str</td>
<td align="right">46,893</td>
<td align="right">29.1%</td>
<td align="right">168,334</td>
<td align="right">25.8%</td>
<td align="right">259.0%</td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">33,311</td>
<td align="right">20.7%</td>
<td align="right">116,836</td>
<td align="right">17.9%</td>
<td align="right">250.7%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">31,613</td>
<td align="right">19.6%</td>
<td align="right">108,453</td>
<td align="right">16.6%</td>
<td align="right">243.1%</td>
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
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">696,204,354</td>
<td align="right">17.0%</td>
<td align="right">826,214,304</td>
<td align="right">18.8%</td>
<td align="right">18.7%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">3,385,070,127</td>
<td align="right">82.9%</td>
<td align="right">3,571,225,764</td>
<td align="right">81.1%</td>
<td align="right">5.5%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">175,763,540</td>
<td align="right">4.3%</td>
<td align="right">177,222,693</td>
<td align="right">4.0%</td>
<td align="right">0.8%</td>
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
<td align="right">356,828</td>
<td align="right">9.5%</td>
<td align="right">907,099</td>
<td align="right">19.0%</td>
<td align="right">154.2%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">3,382,590</td>
<td align="right">90.5%</td>
<td align="right">3,878,083</td>
<td align="right">81.0%</td>
<td align="right">14.6%</td>
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
<td align="left">string</td>
<td align="right">20</td>
<td align="right">0.0%</td>
<td align="right">3,746</td>
<td align="right">0.4%</td>
<td align="right">18,630.0%</td>
</tr>
<tr>
<td align="left">map</td>
<td align="right">1,940</td>
<td align="right">0.5%</td>
<td align="right">36,326</td>
<td align="right">4.0%</td>
<td align="right">1,772.5%</td>
</tr>
<tr>
<td align="left">bytes</td>
<td align="right">880</td>
<td align="right">0.2%</td>
<td align="right">11,717</td>
<td align="right">1.3%</td>
<td align="right">1,231.5%</td>
</tr>
<tr>
<td align="left">ascii string</td>
<td align="right">5,960</td>
<td align="right">1.7%</td>
<td align="right">76,235</td>
<td align="right">8.4%</td>
<td align="right">1,179.1%</td>
</tr>
<tr>
<td align="left">callable</td>
<td align="right">502</td>
<td align="right">0.1%</td>
<td align="right">2,702</td>
<td align="right">0.3%</td>
<td align="right">438.2%</td>
</tr>
<tr>
<td align="left">dict values</td>
<td align="right">14,670</td>
<td align="right">4.1%</td>
<td align="right">67,552</td>
<td align="right">7.4%</td>
<td align="right">360.5%</td>
</tr>
<tr>
<td align="left">dict keys</td>
<td align="right">16,781</td>
<td align="right">4.7%</td>
<td align="right">70,090</td>
<td align="right">7.7%</td>
<td align="right">317.7%</td>
</tr>
<tr>
<td align="left">itertools</td>
<td align="right">9,088</td>
<td align="right">2.5%</td>
<td align="right">26,665</td>
<td align="right">2.9%</td>
<td align="right">193.4%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">28,379</td>
<td align="right">8.0%</td>
<td align="right">67,933</td>
<td align="right">7.5%</td>
<td align="right">139.4%</td>
</tr>
<tr>
<td align="left">dict items</td>
<td align="right">120,575</td>
<td align="right">33.8%</td>
<td align="right">278,166</td>
<td align="right">30.7%</td>
<td align="right">130.7%</td>
</tr>
<tr>
<td align="left">reversed list</td>
<td align="right">9,212</td>
<td align="right">2.6%</td>
<td align="right">21,211</td>
<td align="right">2.3%</td>
<td align="right">130.3%</td>
</tr>
<tr>
<td align="left">enumerate</td>
<td align="right">51,072</td>
<td align="right">14.3%</td>
<td align="right">97,713</td>
<td align="right">10.8%</td>
<td align="right">91.3%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">45,414</td>
<td align="right">12.7%</td>
<td align="right">71,081</td>
<td align="right">7.8%</td>
<td align="right">56.5%</td>
</tr>
<tr>
<td align="left">seq iter</td>
<td align="right">30,700</td>
<td align="right">8.6%</td>
<td align="right">45,596</td>
<td align="right">5.0%</td>
<td align="right">48.5%</td>
</tr>
<tr>
<td align="left">zip</td>
<td align="right">21,635</td>
<td align="right">6.1%</td>
<td align="right">30,366</td>
<td align="right">3.3%</td>
<td align="right">40.4%</td>
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
deopt
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">675,730</td>
<td align="right">0.0%</td>
<td align="right">763,506</td>
<td align="right">0.0%</td>
<td align="right">13.0%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">2,498,788,767</td>
<td align="right">14.4%</td>
<td align="right">2,710,031,859</td>
<td align="right">14.6%</td>
<td align="right">8.5%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">1,022,562,543</td>
<td align="right">5.9%</td>
<td align="right">1,108,237,196</td>
<td align="right">6.0%</td>
<td align="right">8.4%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">14,847,306,244</td>
<td align="right">85.5%</td>
<td align="right">15,795,366,578</td>
<td align="right">85.2%</td>
<td align="right">6.4%</td>
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
<td align="right">2,533,152</td>
<td align="right">11.2%</td>
<td align="right">4,584,072</td>
<td align="right">15.3%</td>
<td align="right">81.0%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">20,178,174</td>
<td align="right">88.8%</td>
<td align="right">25,408,474</td>
<td align="right">84.7%</td>
<td align="right">25.9%</td>
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
<td align="left">builtin class method</td>
<td align="right">3,997</td>
<td align="right">0.2%</td>
<td align="right">53,457</td>
<td align="right">1.2%</td>
<td align="right">1,237.4%</td>
</tr>
<tr>
<td align="left">module attr not found</td>
<td align="right">17,542</td>
<td align="right">0.7%</td>
<td align="right">159,458</td>
<td align="right">3.5%</td>
<td align="right">809.0%</td>
</tr>
<tr>
<td align="left">non overriding descriptor</td>
<td align="right">14,009</td>
<td align="right">0.6%</td>
<td align="right">119,426</td>
<td align="right">2.6%</td>
<td align="right">752.5%</td>
</tr>
<tr>
<td align="left">class method obj</td>
<td align="right">28,463</td>
<td align="right">1.1%</td>
<td align="right">212,089</td>
<td align="right">4.6%</td>
<td align="right">645.1%</td>
</tr>
<tr>
<td align="left">non object slot</td>
<td align="right">3,561</td>
<td align="right">0.1%</td>
<td align="right">18,959</td>
<td align="right">0.4%</td>
<td align="right">432.4%</td>
</tr>
<tr>
<td align="left">non string or split</td>
<td align="right">22,208</td>
<td align="right">0.9%</td>
<td align="right">116,687</td>
<td align="right">2.5%</td>
<td align="right">425.4%</td>
</tr>
<tr>
<td align="left">overridden</td>
<td align="right">21,091</td>
<td align="right">0.8%</td>
<td align="right">74,598</td>
<td align="right">1.6%</td>
<td align="right">253.7%</td>
</tr>
<tr>
<td align="left">metaclass attribute</td>
<td align="right">279,228</td>
<td align="right">11.0%</td>
<td align="right">910,759</td>
<td align="right">19.9%</td>
<td align="right">226.2%</td>
</tr>
<tr>
<td align="left">not in dict</td>
<td align="right">300</td>
<td align="right">0.0%</td>
<td align="right">674</td>
<td align="right">0.0%</td>
<td align="right">124.7%</td>
</tr>
<tr>
<td align="left">shadowed</td>
<td align="right">153,179</td>
<td align="right">6.0%</td>
<td align="right">297,858</td>
<td align="right">6.5%</td>
<td align="right">94.5%</td>
</tr>
<tr>
<td align="left">method</td>
<td align="right">170,400</td>
<td align="right">6.7%</td>
<td align="right">315,454</td>
<td align="right">6.9%</td>
<td align="right">85.1%</td>
</tr>
<tr>
<td align="left">class attr descriptor</td>
<td align="right">30,660</td>
<td align="right">1.2%</td>
<td align="right">54,684</td>
<td align="right">1.2%</td>
<td align="right">78.4%</td>
</tr>
<tr>
<td align="left">not managed dict</td>
<td align="right">966,468</td>
<td align="right">38.2%</td>
<td align="right">1,356,740</td>
<td align="right">29.6%</td>
<td align="right">40.4%</td>
</tr>
<tr>
<td align="left">mutable class</td>
<td align="right">83,627</td>
<td align="right">3.3%</td>
<td align="right">113,625</td>
<td align="right">2.5%</td>
<td align="right">35.9%</td>
</tr>
<tr>
<td align="left">not in keys</td>
<td align="right">16,920</td>
<td align="right">0.7%</td>
<td align="right">20,128</td>
<td align="right">0.4%</td>
<td align="right">19.0%</td>
</tr>
<tr>
<td align="left">class attr simple</td>
<td align="right">717,581</td>
<td align="right">28.3%</td>
<td align="right">747,557</td>
<td align="right">16.3%</td>
<td align="right">4.2%</td>
</tr>
<tr>
<td align="left">out of versions</td>
<td align="right">2,358</td>
<td align="right">0.1%</td>
<td align="right">2,358</td>
<td align="right">0.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">wrong number arguments</td>
<td align="right">1,200</td>
<td align="right">0.0%</td>
<td align="right">1,200</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
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
<tr>
<td align="left">property not py function</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">4,018</td>
<td align="right">0.1%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">expected error</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">3,953</td>
<td align="right">0.1%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">audited slot</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">30</td>
<td align="right">0.0%</td>
<td align="right"></td>
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
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">443,018</td>
<td align="right">0.0%</td>
<td align="right">28,081,108</td>
<td align="right">0.3%</td>
<td align="right">6,238.6%</td>
</tr>
<tr>
<td align="left">
deopt
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">13,043</td>
<td align="right">0.0%</td>
<td align="right">727,158</td>
<td align="right">0.0%</td>
<td align="right">5,475.1%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">20,571,382</td>
<td align="right">0.2%</td>
<td align="right">54,112,047</td>
<td align="right">0.5%</td>
<td align="right">163.0%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">10,467,992,067</td>
<td align="right">99.8%</td>
<td align="right">11,103,496,574</td>
<td align="right">99.5%</td>
<td align="right">6.1%</td>
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
<td align="right">669,294</td>
<td align="right">100.0%</td>
<td align="right">5,333,912</td>
<td align="right">100.0%</td>
<td align="right">696.9%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right">375</td>
<td align="right">0.0%</td>
<td align="right">375 / 0 !!</td>
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
<td align="right"></td>
<td align="right"></td>
<td align="right">375</td>
<td align="right">100.0%</td>
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
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">11,990</td>
<td align="right">0.0%</td>
<td align="right">108,248</td>
<td align="right">0.1%</td>
<td align="right">802.8%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">134,362,006</td>
<td align="right">100.0%</td>
<td align="right">144,111,350</td>
<td align="right">99.9%</td>
<td align="right">7.3%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">1</td>
<td align="right">0.0%</td>
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
<td align="right">11,817</td>
<td align="right">100.0%</td>
<td align="right">85,760</td>
<td align="right">100.0%</td>
<td align="right">625.7%</td>
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
<td align="right">787,140,407</td>
<td align="right">81.9%</td>
<td align="right">809,464,600</td>
<td align="right">82.3%</td>
<td align="right">2.8%</td>
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
<td align="right">31,284</td>
<td align="right">0.0%</td>
<td align="right">1.2%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">173,911,113</td>
<td align="right">18.1%</td>
<td align="right">174,180,771</td>
<td align="right">17.7%</td>
<td align="right">0.2%</td>
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
<td align="right">7,127</td>
<td align="right">10.3%</td>
<td align="right">9,698</td>
<td align="right">12.8%</td>
<td align="right">36.1%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">61,837</td>
<td align="right">89.7%</td>
<td align="right">65,984</td>
<td align="right">87.2%</td>
<td align="right">6.7%</td>
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
<td align="right">10,060</td>
<td align="right">16.3%</td>
<td align="right">14,013</td>
<td align="right">21.2%</td>
<td align="right">39.3%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">2,260</td>
<td align="right">3.7%</td>
<td align="right">2,344</td>
<td align="right">3.6%</td>
<td align="right">3.7%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">16,097</td>
<td align="right">26.0%</td>
<td align="right">16,207</td>
<td align="right">24.6%</td>
<td align="right">0.7%</td>
</tr>
<tr>
<td align="left">async generator send</td>
<td align="right">33,180</td>
<td align="right">53.7%</td>
<td align="right">33,180</td>
<td align="right">50.3%</td>
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
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">296,120,432</td>
<td align="right">9.6%</td>
<td align="right">326,986,919</td>
<td align="right">10.1%</td>
<td align="right">10.4%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">2,775,543,150</td>
<td align="right">90.2%</td>
<td align="right">2,908,347,931</td>
<td align="right">89.7%</td>
<td align="right">4.8%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">222,671,940</td>
<td align="right">7.2%</td>
<td align="right">229,112,252</td>
<td align="right">7.1%</td>
<td align="right">2.9%</td>
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
<td align="right">148,786</td>
<td align="right">3.3%</td>
<td align="right">821,461</td>
<td align="right">13.3%</td>
<td align="right">452.1%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">4,350,660</td>
<td align="right">96.7%</td>
<td align="right">5,351,011</td>
<td align="right">86.7%</td>
<td align="right">23.0%</td>
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
<td align="left">mutable class</td>
<td align="right">40</td>
<td align="right">0.0%</td>
<td align="right">3,130</td>
<td align="right">0.4%</td>
<td align="right">7,725.0%</td>
</tr>
<tr>
<td align="left">overridden</td>
<td align="right">6,832</td>
<td align="right">4.6%</td>
<td align="right">285,545</td>
<td align="right">34.8%</td>
<td align="right">4,079.5%</td>
</tr>
<tr>
<td align="left">no dict</td>
<td align="right">4,780</td>
<td align="right">3.2%</td>
<td align="right">44,188</td>
<td align="right">5.4%</td>
<td align="right">824.4%</td>
</tr>
<tr>
<td align="left">not in keys</td>
<td align="right">8,381</td>
<td align="right">5.6%</td>
<td align="right">64,683</td>
<td align="right">7.9%</td>
<td align="right">671.8%</td>
</tr>
<tr>
<td align="left">non string or split</td>
<td align="right">15,100</td>
<td align="right">10.1%</td>
<td align="right">92,938</td>
<td align="right">11.3%</td>
<td align="right">515.5%</td>
</tr>
<tr>
<td align="left">overriding descriptor</td>
<td align="right">10,860</td>
<td align="right">7.3%</td>
<td align="right">57,357</td>
<td align="right">7.0%</td>
<td align="right">428.1%</td>
</tr>
<tr>
<td align="left">not managed dict</td>
<td align="right">28,576</td>
<td align="right">19.2%</td>
<td align="right">120,478</td>
<td align="right">14.7%</td>
<td align="right">321.6%</td>
</tr>
<tr>
<td align="left">property</td>
<td align="right">5,640</td>
<td align="right">3.8%</td>
<td align="right">17,101</td>
<td align="right">2.1%</td>
<td align="right">203.2%</td>
</tr>
<tr>
<td align="left">method</td>
<td align="right">1,580</td>
<td align="right">1.1%</td>
<td align="right">4,582</td>
<td align="right">0.6%</td>
<td align="right">190.0%</td>
</tr>
<tr>
<td align="left">not in dict</td>
<td align="right">16,145</td>
<td align="right">10.9%</td>
<td align="right">34,559</td>
<td align="right">4.2%</td>
<td align="right">114.1%</td>
</tr>
<tr>
<td align="left">class attr simple</td>
<td align="right">50,238</td>
<td align="right">33.8%</td>
<td align="right">96,284</td>
<td align="right">11.7%</td>
<td align="right">91.7%</td>
</tr>
<tr>
<td align="left">out of versions</td>
<td align="right">614</td>
<td align="right">0.4%</td>
<td align="right">614</td>
<td align="right">0.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">class attr descriptor</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">2</td>
<td align="right">0.0%</td>
<td align="right"></td>
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
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">445,134,182</td>
<td align="right">34.0%</td>
<td align="right">478,903,433</td>
<td align="right">35.2%</td>
<td align="right">7.6%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">863,379,448</td>
<td align="right">66.0%</td>
<td align="right">880,513,321</td>
<td align="right">64.7%</td>
<td align="right">2.0%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">2,880</td>
<td align="right">0.0%</td>
<td align="right">2,880</td>
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
<td align="right">18,563</td>
<td align="right">10.3%</td>
<td align="right">212,061</td>
<td align="right">45.7%</td>
<td align="right">1,042.4%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">162,050</td>
<td align="right">89.7%</td>
<td align="right">252,462</td>
<td align="right">54.3%</td>
<td align="right">55.8%</td>
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
<td align="right">2,060</td>
<td align="right">1.3%</td>
<td align="right">12,765</td>
<td align="right">5.1%</td>
<td align="right">519.7%</td>
</tr>
<tr>
<td align="left">list slice</td>
<td align="right">40</td>
<td align="right">0.0%</td>
<td align="right">237</td>
<td align="right">0.1%</td>
<td align="right">492.5%</td>
</tr>
<tr>
<td align="left">bytearray int</td>
<td align="right">9,720</td>
<td align="right">6.0%</td>
<td align="right">51,738</td>
<td align="right">20.5%</td>
<td align="right">432.3%</td>
</tr>
<tr>
<td align="left">out of range</td>
<td align="right">3,788</td>
<td align="right">2.3%</td>
<td align="right">12,632</td>
<td align="right">5.0%</td>
<td align="right">233.5%</td>
</tr>
<tr>
<td align="left">py simple</td>
<td align="right">44,518</td>
<td align="right">27.5%</td>
<td align="right">69,866</td>
<td align="right">27.7%</td>
<td align="right">56.9%</td>
</tr>
<tr>
<td align="left">dict subclass no override</td>
<td align="right">35,684</td>
<td align="right">22.0%</td>
<td align="right">38,890</td>
<td align="right">15.4%</td>
<td align="right">9.0%</td>
</tr>
<tr>
<td align="left">array int</td>
<td align="right">66,240</td>
<td align="right">40.9%</td>
<td align="right">66,334</td>
<td align="right">26.3%</td>
<td align="right">0.1%</td>
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
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">541,746,683</td>
<td align="right">8.0%</td>
<td align="right">594,474,631</td>
<td align="right">8.3%</td>
<td align="right">9.7%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">6,254,768,942</td>
<td align="right">92.0%</td>
<td align="right">6,585,947,820</td>
<td align="right">91.6%</td>
<td align="right">5.3%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">147,736,138</td>
<td align="right">2.2%</td>
<td align="right">152,980,048</td>
<td align="right">2.1%</td>
<td align="right">3.5%</td>
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
<td align="right">3,072,407</td>
<td align="right">81.1%</td>
<td align="right">4,624,971</td>
<td align="right">82.8%</td>
<td align="right">50.5%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">718,164</td>
<td align="right">18.9%</td>
<td align="right">962,979</td>
<td align="right">17.2%</td>
<td align="right">34.1%</td>
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
<td align="left">dict</td>
<td align="right">41,078</td>
<td align="right">5.7%</td>
<td align="right">100,349</td>
<td align="right">10.4%</td>
<td align="right">144.3%</td>
</tr>
<tr>
<td align="left">bytearray</td>
<td align="right">1,234</td>
<td align="right">0.2%</td>
<td align="right">2,825</td>
<td align="right">0.3%</td>
<td align="right">128.9%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">43,930</td>
<td align="right">6.1%</td>
<td align="right">93,069</td>
<td align="right">9.7%</td>
<td align="right">111.9%</td>
</tr>
<tr>
<td align="left">sequence</td>
<td align="right">20,195</td>
<td align="right">2.8%</td>
<td align="right">36,040</td>
<td align="right">3.7%</td>
<td align="right">78.5%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">115,269</td>
<td align="right">16.1%</td>
<td align="right">169,115</td>
<td align="right">17.6%</td>
<td align="right">46.7%</td>
</tr>
<tr>
<td align="left">bytes</td>
<td align="right">33,166</td>
<td align="right">4.6%</td>
<td align="right">42,037</td>
<td align="right">4.4%</td>
<td align="right">26.7%</td>
</tr>
<tr>
<td align="left">mapping</td>
<td align="right">100,421</td>
<td align="right">14.0%</td>
<td align="right">127,010</td>
<td align="right">13.2%</td>
<td align="right">26.5%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">175,694</td>
<td align="right">24.5%</td>
<td align="right">194,080</td>
<td align="right">20.2%</td>
<td align="right">10.5%</td>
</tr>
<tr>
<td align="left">memory view</td>
<td align="right">420</td>
<td align="right">0.1%</td>
<td align="right">450</td>
<td align="right">0.0%</td>
<td align="right">7.1%</td>
</tr>
<tr>
<td align="left">number</td>
<td align="right">184,157</td>
<td align="right">25.6%</td>
<td align="right">195,363</td>
<td align="right">20.3%</td>
<td align="right">6.1%</td>
</tr>
<tr>
<td align="left">float</td>
<td align="right">2,600</td>
<td align="right">0.4%</td>
<td align="right">2,641</td>
<td align="right">0.3%</td>
<td align="right">1.6%</td>
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
<td align="right">2,056,280</td>
<td align="right">0.1%</td>
<td align="right">3,347,590</td>
<td align="right">0.2%</td>
<td align="right">62.8%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">1,561,033,346</td>
<td align="right">99.9%</td>
<td align="right">1,734,010,570</td>
<td align="right">99.8%</td>
<td align="right">11.1%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">4,240</td>
<td align="right">0.0%</td>
<td align="right">4,382</td>
<td align="right">0.0%</td>
<td align="right">3.3%</td>
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
<td align="right">40,117</td>
<td align="right">90.1%</td>
<td align="right">265,168</td>
<td align="right">91.3%</td>
<td align="right">561.0%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">4,400</td>
<td align="right">9.9%</td>
<td align="right">25,306</td>
<td align="right">8.7%</td>
<td align="right">475.1%</td>
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
<td align="right">761</td>
<td align="right">17.3%</td>
<td align="right">13,417</td>
<td align="right">53.0%</td>
<td align="right">1,663.1%</td>
</tr>
<tr>
<td align="left">sequence</td>
<td align="right">3,259</td>
<td align="right">74.1%</td>
<td align="right">11,460</td>
<td align="right">45.3%</td>
<td align="right">251.6%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">380</td>
<td align="right">8.6%</td>
<td align="right">380</td>
<td align="right">1.5%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">expected error</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">49</td>
<td align="right">0.2%</td>
<td align="right"></td>
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
Not specialized
<details>
<summary>ⓘ</summary>

Instructions that could be specialized but aren't, e.g. `LOAD_ATTR`, `BINARY_SLICE`.
</details>
</td>
<td align="right">24,362,054,564</td>
<td align="right">10.6%</td>
<td align="right">33,006,565,775</td>
<td align="right">13.6%</td>
<td align="right">35.5%</td>
</tr>
<tr>
<td align="left">
Specialized misses
<details>
<summary>ⓘ</summary>

Specialized instructions, e.g. `LOAD_ATTR_MODULE` that deopt.
</details>
</td>
<td align="right">1,890,788,451</td>
<td align="right">0.8%</td>
<td align="right">1,994,240,841</td>
<td align="right">0.8%</td>
<td align="right">5.5%</td>
</tr>
<tr>
<td align="left">
Basic
<details>
<summary>ⓘ</summary>

Instructions that are not and cannot be specialized, e.g. `LOAD_FAST`.
</details>
</td>
<td align="right">123,838,956,424</td>
<td align="right">53.9%</td>
<td align="right">130,434,714,878</td>
<td align="right">53.8%</td>
<td align="right">5.3%</td>
</tr>
<tr>
<td align="left">
Specialized hits
<details>
<summary>ⓘ</summary>

Specialized instructions, e.g. `LOAD_ATTR_MODULE` that complete.
</details>
</td>
<td align="right">79,851,644,216</td>
<td align="right">34.7%</td>
<td align="right">77,008,943,359</td>
<td align="right">31.8%</td>
<td align="right">-3.6%</td>
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
<td align="left">BINARY_OP</td>
<td align="right">1,443,865,082</td>
<td align="right">15.1%</td>
<td align="right">8,493,069,782</td>
<td align="right">49.0%</td>
<td align="right">488.2%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">223,408,114</td>
<td align="right">2.3%</td>
<td align="right">266,086,252</td>
<td align="right">1.5%</td>
<td align="right">19.1%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">696,204,354</td>
<td align="right">7.3%</td>
<td align="right">826,214,304</td>
<td align="right">4.8%</td>
<td align="right">18.7%</td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">296,120,432</td>
<td align="right">3.1%</td>
<td align="right">326,986,919</td>
<td align="right">1.9%</td>
<td align="right">10.4%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">541,746,683</td>
<td align="right">5.7%</td>
<td align="right">594,474,631</td>
<td align="right">3.4%</td>
<td align="right">9.7%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">1,449,963,227</td>
<td align="right">15.2%</td>
<td align="right">1,578,968,066</td>
<td align="right">9.1%</td>
<td align="right">8.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">2,498,788,767</td>
<td align="right">26.1%</td>
<td align="right">2,710,031,859</td>
<td align="right">15.6%</td>
<td align="right">8.5%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR</td>
<td align="right">445,134,182</td>
<td align="right">4.7%</td>
<td align="right">478,903,433</td>
<td align="right">2.8%</td>
<td align="right">7.6%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">248,546,168</td>
<td align="right">2.6%</td>
<td align="right">266,315,100</td>
<td align="right">1.5%</td>
<td align="right">7.1%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR</td>
<td align="right">1,528,858,497</td>
<td align="right">16.0%</td>
<td align="right">1,573,490,467</td>
<td align="right">9.1%</td>
<td align="right">2.9%</td>
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
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">133,187,505</td>
<td align="right">7.0%</td>
<td align="right">148,129,485</td>
<td align="right">7.4%</td>
<td align="right">11.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">381,885,864</td>
<td align="right">20.2%</td>
<td align="right">424,294,650</td>
<td align="right">21.3%</td>
<td align="right">11.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">365,702,785</td>
<td align="right">19.3%</td>
<td align="right">391,139,557</td>
<td align="right">19.6%</td>
<td align="right">7.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">116,424,944</td>
<td align="right">6.2%</td>
<td align="right">122,389,927</td>
<td align="right">6.1%</td>
<td align="right">5.1%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">123,707,831</td>
<td align="right">6.5%</td>
<td align="right">129,628,300</td>
<td align="right">6.5%</td>
<td align="right">4.8%</td>
</tr>
<tr>
<td align="left">TO_BOOL_NONE</td>
<td align="right">68,842,704</td>
<td align="right">3.6%</td>
<td align="right">71,073,247</td>
<td align="right">3.6%</td>
<td align="right">3.2%</td>
</tr>
<tr>
<td align="left">TO_BOOL_ALWAYS_TRUE</td>
<td align="right">70,000,027</td>
<td align="right">3.7%</td>
<td align="right">70,630,353</td>
<td align="right">3.5%</td>
<td align="right">0.9%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">87,924,011</td>
<td align="right">4.6%</td>
<td align="right">88,671,484</td>
<td align="right">4.4%</td>
<td align="right">0.9%</td>
</tr>
<tr>
<td align="left">FOR_ITER_TUPLE</td>
<td align="right">87,536,029</td>
<td align="right">4.6%</td>
<td align="right">88,157,041</td>
<td align="right">4.4%</td>
<td align="right">0.7%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_SLOT</td>
<td align="right">98,905,194</td>
<td align="right">5.2%</td>
<td align="right">99,383,737</td>
<td align="right">5.0%</td>
<td align="right">0.5%</td>
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
<td align="left">Calls via PyEval_EvalFrame (build class)</td>
<td align="right">28,806</td>
<td align="right">0.0%</td>
<td align="right">1,660,963</td>
<td align="right">0.0%</td>
<td align="right">5,666.0%</td>
</tr>
<tr>
<td align="left">Frame objects created</td>
<td align="right">88,574,094</td>
<td align="right">1.0%</td>
<td align="right">110,658,174</td>
<td align="right">1.2%</td>
<td align="right">24.9%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (slot)</td>
<td align="right">343,113,968</td>
<td align="right">3.9%</td>
<td align="right">394,336,588</td>
<td align="right">4.3%</td>
<td align="right">14.9%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (legacy)</td>
<td align="right">5,298,324</td>
<td align="right">0.1%</td>
<td align="right">5,837,787</td>
<td align="right">0.1%</td>
<td align="right">10.2%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (function ex)</td>
<td align="right">28,844,832</td>
<td align="right">0.3%</td>
<td align="right">31,765,945</td>
<td align="right">0.3%</td>
<td align="right">10.1%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (vector)</td>
<td align="right">1,303,138,405</td>
<td align="right">14.9%</td>
<td align="right">1,421,090,803</td>
<td align="right">15.5%</td>
<td align="right">9.1%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (function vectorcall)</td>
<td align="right">1,297,811,275</td>
<td align="right">14.9%</td>
<td align="right">1,413,592,803</td>
<td align="right">15.4%</td>
<td align="right">8.9%</td>
</tr>
<tr>
<td align="left">Calls to PyEval_EvalDefault</td>
<td align="right">2,163,365,378</td>
<td align="right">24.8%</td>
<td align="right">2,296,809,960</td>
<td align="right">25.0%</td>
<td align="right">6.2%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (total)</td>
<td align="right">2,163,365,378</td>
<td align="right">24.8%</td>
<td align="right">2,296,809,960</td>
<td align="right">25.0%</td>
<td align="right">6.2%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (api)</td>
<td align="right">243,732,357</td>
<td align="right">2.8%</td>
<td align="right">257,702,620</td>
<td align="right">2.8%</td>
<td align="right">5.7%</td>
</tr>
<tr>
<td align="left">Calls to Python functions inlined</td>
<td align="right">6,564,971,365</td>
<td align="right">75.2%</td>
<td align="right">6,893,702,514</td>
<td align="right">75.0%</td>
<td align="right">5.0%</td>
</tr>
<tr>
<td align="left">Frames pushed</td>
<td align="right">5,073,980,368</td>
<td align="right">58.1%</td>
<td align="right">5,319,666,275</td>
<td align="right">57.9%</td>
<td align="right">4.8%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (generator)</td>
<td align="right">860,226,973</td>
<td align="right">9.9%</td>
<td align="right">875,719,157</td>
<td align="right">9.5%</td>
<td align="right">1.8%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (method)</td>
<td align="right">213,114,059</td>
<td align="right">2.4%</td>
<td align="right">213,704,474</td>
<td align="right">2.3%</td>
<td align="right">0.3%</td>
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
<td align="left">Materialize dict (new key)</td>
<td align="right">133,555</td>
<td align="right">0.1%</td>
<td align="right">487,360</td>
<td align="right">0.2%</td>
<td align="right">264.9%</td>
</tr>
<tr>
<td align="left">Method cache dunder misses</td>
<td align="right">14,708,589</td>
<td align="right"></td>
<td align="right">19,535,460</td>
<td align="right"></td>
<td align="right">32.8%</td>
</tr>
<tr>
<td align="left">Method cache misses</td>
<td align="right">79,870,416</td>
<td align="right"></td>
<td align="right">102,765,393</td>
<td align="right"></td>
<td align="right">28.7%</td>
</tr>
<tr>
<td align="left">Materialize dict (on request)</td>
<td align="right">3,358,423</td>
<td align="right">1.8%</td>
<td align="right">4,192,620</td>
<td align="right">2.1%</td>
<td align="right">24.8%</td>
</tr>
<tr>
<td align="left">Frees to freelist</td>
<td align="right">6,765,795,398</td>
<td align="right"></td>
<td align="right">8,419,651,811</td>
<td align="right"></td>
<td align="right">24.4%</td>
</tr>
<tr>
<td align="left">Allocations from freelist</td>
<td align="right">6,763,852,590</td>
<td align="right">36.6%</td>
<td align="right">8,388,038,655</td>
<td align="right">39.0%</td>
<td align="right">24.0%</td>
</tr>
<tr>
<td align="left">Allocations over 4 kbytes</td>
<td align="right">21,168,666</td>
<td align="right">0.1%</td>
<td align="right">25,255,838</td>
<td align="right">0.1%</td>
<td align="right">19.3%</td>
</tr>
<tr>
<td align="left">Method cache collisions</td>
<td align="right">86,829,279</td>
<td align="right"></td>
<td align="right">102,291,619</td>
<td align="right"></td>
<td align="right">17.8%</td>
</tr>
<tr>
<td align="left">Allocations to 4 kbytes</td>
<td align="right">104,805,421</td>
<td align="right">0.6%</td>
<td align="right">122,003,981</td>
<td align="right">0.6%</td>
<td align="right">16.4%</td>
</tr>
<tr>
<td align="left">Allocations</td>
<td align="right">11,724,295,517</td>
<td align="right">63.4%</td>
<td align="right">13,102,650,345</td>
<td align="right">61.0%</td>
<td align="right">11.8%</td>
</tr>
<tr>
<td align="left">Allocations to 512 bytes</td>
<td align="right">11,598,321,430</td>
<td align="right">62.7%</td>
<td align="right">12,955,390,526</td>
<td align="right">60.3%</td>
<td align="right">11.7%</td>
</tr>
<tr>
<td align="left">Decrefs</td>
<td align="right">29,564,799,432</td>
<td align="right">22.3%</td>
<td align="right">32,906,458,483</td>
<td align="right">23.0%</td>
<td align="right">11.3%</td>
</tr>
<tr>
<td align="left">Frees</td>
<td align="right">12,053,615,480</td>
<td align="right"></td>
<td align="right">13,379,936,217</td>
<td align="right"></td>
<td align="right">11.0%</td>
</tr>
<tr>
<td align="left">Method cache dunder hits</td>
<td align="right">3,392,610,835</td>
<td align="right"></td>
<td align="right">3,745,136,789</td>
<td align="right"></td>
<td align="right">10.4%</td>
</tr>
<tr>
<td align="left">Increfs</td>
<td align="right">26,476,220,292</td>
<td align="right">23.0%</td>
<td align="right">29,107,655,313</td>
<td align="right">23.7%</td>
<td align="right">9.9%</td>
</tr>
<tr>
<td align="left">Method cache hits</td>
<td align="right">3,114,461,613</td>
<td align="right"></td>
<td align="right">3,400,402,176</td>
<td align="right"></td>
<td align="right">9.2%</td>
</tr>
<tr>
<td align="left">Inline values</td>
<td align="right">183,054,449</td>
<td align="right"></td>
<td align="right">197,163,197</td>
<td align="right"></td>
<td align="right">7.7%</td>
</tr>
<tr>
<td align="left">Interpreter decrefs</td>
<td align="right">103,051,197,332</td>
<td align="right">77.7%</td>
<td align="right">110,094,101,380</td>
<td align="right">77.0%</td>
<td align="right">6.8%</td>
</tr>
<tr>
<td align="left">Interpreter increfs</td>
<td align="right">88,737,255,575</td>
<td align="right">77.0%</td>
<td align="right">93,924,769,555</td>
<td align="right">76.3%</td>
<td align="right">5.8%</td>
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
<td align="right">115,784,669</td>
<td align="right">17,094,891,651</td>
<td align="right">0</td>
<td align="right">136,997,740</td>
<td align="right">18,833,069,453</td>
</tr>
<tr>
<td align="right">2</td>
<td align="right">0</td>
<td align="right">10,752,660</td>
<td align="right">6,950,472,470</td>
<td align="right">0</td>
<td align="right">51,097,247</td>
<td align="right">8,638,526,553</td>
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
Optimization attempts
<details>
<summary>ⓘ</summary>

The number of times a potential trace is identified.  Specifically, this occurs in the JUMP BACKWARD instruction when the counter reaches a threshold.
</details>
</td>
<td align="right">0</td>
<td align="right"></td>
<td align="right">0</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">
Traces created
<details>
<summary>ⓘ</summary>

The number of traces that were successfully created.
</details>
</td>
<td align="right">0</td>
<td align="right"></td>
<td align="right">0</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">
Trace stack overflow
<details>
<summary>ⓘ</summary>

A trace is truncated because it would require more than 5 stack frames.
</details>
</td>
<td align="right">0</td>
<td align="right"></td>
<td align="right">0</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">
Trace stack underflow
<details>
<summary>ⓘ</summary>

A potential trace is abandoned because it pops more frames than it pushes.
</details>
</td>
<td align="right">0</td>
<td align="right"></td>
<td align="right">0</td>
<td align="right"></td>
<td align="right"></td>
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
<td align="right"></td>
<td align="right">0</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">
Trace too short
<details>
<summary>ⓘ</summary>

A potential trace is abandoced because it it too short.
</details>
</td>
<td align="right">0</td>
<td align="right"></td>
<td align="right">0</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">
Inner loop found
<details>
<summary>ⓘ</summary>

A trace is truncated because it has an inner loop
</details>
</td>
<td align="right">0</td>
<td align="right"></td>
<td align="right">0</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">
Recursive call
<details>
<summary>ⓘ</summary>

A trace is truncated because it has a recursive call.
</details>
</td>
<td align="right">0</td>
<td align="right"></td>
<td align="right">0</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">
Low confidence
<details>
<summary>ⓘ</summary>

A trace is abandoned because the likelihood of the jump to top being taken is too low.
</details>
</td>
<td align="right">0</td>
<td align="right"></td>
<td align="right">0</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">
Executors invalidated
<details>
<summary>ⓘ</summary>

The number of executors that were invalidated due to watched dictionary changes.
</details>
</td>
<td align="right">0</td>
<td align="right"></td>
<td align="right">0</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">
Traces executed
<details>
<summary>ⓘ</summary>

The number of traces that were executed
</details>
</td>
<td align="right">0</td>
<td align="right"></td>
<td align="right">0</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">
Uops executed
<details>
<summary>ⓘ</summary>

The total number of uops (micro-operations) that were executed
</details>
</td>
<td align="right">0</td>
<td align="right"></td>
<td align="right">0</td>
<td align="right"></td>
<td align="right"></td>
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
Optimizer attempts
<details>
<summary>ⓘ</summary>

The number of times the trace optimizer (_Py_uop_analyze_and_optimize) was run.
</details>
</td>
<td align="right">0</td>
<td align="right"></td>
<td align="right">0</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">
Optimizer successes
<details>
<summary>ⓘ</summary>

The number of traces that were successfully optimized.
</details>
</td>
<td align="right">0</td>
<td align="right"></td>
<td align="right">0</td>
<td align="right"></td>
<td align="right"></td>
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
<td align="right"></td>
<td align="right">0</td>
<td align="right"></td>
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
<td align="right"></td>
<td align="right">0</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">
Remove globals incorrect keys
<details>
<summary>ⓘ</summary>

The keys in the globals dictionary aren't what was expected
</details>
</td>
<td align="right">0</td>
<td align="right"></td>
<td align="right">0</td>
<td align="right"></td>
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
<td align="right"></td>
<td align="right">0</td>
<td align="right"></td>
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
<td align="right"></td>
<td align="right">0</td>
<td align="right"></td>
<td align="right"></td>
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
<td align="right"></td>
<td align="right">0</td>
<td align="right"></td>
<td align="right"></td>
</tr>
</tbody>
</table>


</details>

### Uop execution stats

<details>
<summary> uop execution stats </summary>


</details>

### Unsupported opcodes

<details>
<summary> unsupported opcodes </summary>


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
func modification
<details>
<summary>ⓘ</summary>

Modifying a function, e.g. `func.__defaults__ = ...`, etc.
</details>
</td>
<td align="right">441</td>
<td align="right">39,231</td>
<td align="right">8,795.9%</td>
</tr>
<tr>
<td align="left">
set bases
<details>
<summary>ⓘ</summary>

Setting the bases of a class, `cls.__bases__ = ...`
</details>
</td>
<td align="right">261</td>
<td align="right">10,896</td>
<td align="right">4,074.7%</td>
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
<td align="right">484</td>
<td align="right">484 / 0 !!</td>
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
<td align="right">24</td>
<td align="right">24 / 0 !!</td>
</tr>
<tr>
<td align="left">
watched dict modification
<details>
<summary>ⓘ</summary>

A watched dict has been modified
</details>
</td>
<td align="right">0</td>
<td align="right">24</td>
<td align="right">24 / 0 !!</td>
</tr>
<tr>
<td align="left">
watched globals modification
<details>
<summary>ⓘ</summary>

A watched `globals()` dict has been modified
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
<td align="right">1,980</td>
<td align="right">10,623</td>
<td align="right">436.5%</td>
</tr>
</tbody>
</table>


</details>

---
Stats gathered on: 2024-04-08
