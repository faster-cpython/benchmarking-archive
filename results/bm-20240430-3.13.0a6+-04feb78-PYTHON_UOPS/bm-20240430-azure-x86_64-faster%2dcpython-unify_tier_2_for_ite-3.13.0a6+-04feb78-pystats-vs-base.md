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
<td align="left">FOR_ITER_TUPLE</td>
<td align="right">9,322,669</td>
<td align="right">127,573,632</td>
<td align="right">1,268.4%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">25,033,007</td>
<td align="right">261,247,125</td>
<td align="right">943.6%</td>
</tr>
<tr>
<td align="left">SET_ADD</td>
<td align="right">240,278</td>
<td align="right">965,777</td>
<td align="right">301.9%</td>
</tr>
<tr>
<td align="left">STORE_FAST_LOAD_FAST</td>
<td align="right">15,894,646</td>
<td align="right">37,144,433</td>
<td align="right">133.7%</td>
</tr>
<tr>
<td align="left">FOR_ITER_RANGE</td>
<td align="right">30,114,263</td>
<td align="right">52,714,319</td>
<td align="right">75.0%</td>
</tr>
<tr>
<td align="left">DELETE_SUBSCR</td>
<td align="right">176,287,946</td>
<td align="right">79,744,868</td>
<td align="right">-54.8%</td>
</tr>
<tr>
<td align="left">CONVERT_VALUE</td>
<td align="right">87,548,384</td>
<td align="right">135,326,028</td>
<td align="right">54.6%</td>
</tr>
<tr>
<td align="left">FORMAT_SIMPLE</td>
<td align="right">97,516,060</td>
<td align="right">145,188,189</td>
<td align="right">48.9%</td>
</tr>
<tr>
<td align="left">BUILD_STRING</td>
<td align="right">50,582,232</td>
<td align="right">74,244,010</td>
<td align="right">46.8%</td>
</tr>
<tr>
<td align="left">STORE_SLICE</td>
<td align="right">12,601,781</td>
<td align="right">7,504,627</td>
<td align="right">-40.4%</td>
</tr>
<tr>
<td align="left">CALL_TYPE_1</td>
<td align="right">147,540,690</td>
<td align="right">198,129,132</td>
<td align="right">34.3%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP_DICT</td>
<td align="right">104,180,045</td>
<td align="right">138,841,860</td>
<td align="right">33.3%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST</td>
<td align="right">305,269,263</td>
<td align="right">403,755,829</td>
<td align="right">32.3%</td>
</tr>
<tr>
<td align="left">MAP_ADD</td>
<td align="right">39,181,116</td>
<td align="right">27,340,378</td>
<td align="right">-30.2%</td>
</tr>
<tr>
<td align="left">DELETE_ATTR</td>
<td align="right">6,693,199</td>
<td align="right">4,683,148</td>
<td align="right">-30.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_MULTIPLY_FLOAT</td>
<td align="right">146,529,174</td>
<td align="right">190,322,142</td>
<td align="right">29.9%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">254,275,371</td>
<td align="right">328,075,619</td>
<td align="right">29.0%</td>
</tr>
<tr>
<td align="left">BUILD_CONST_KEY_MAP</td>
<td align="right">7,422,984</td>
<td align="right">5,316,442</td>
<td align="right">-28.4%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_O</td>
<td align="right">391,910,533</td>
<td align="right">289,288,945</td>
<td align="right">-26.2%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TUPLE</td>
<td align="right">198,213,376</td>
<td align="right">246,274,994</td>
<td align="right">24.2%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR</td>
<td align="right">263,984,989</td>
<td align="right">324,754,187</td>
<td align="right">23.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL_STR</td>
<td align="right">76,383,941</td>
<td align="right">60,750,409</td>
<td align="right">-20.5%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">539,405,584</td>
<td align="right">436,473,441</td>
<td align="right">-19.1%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">101,980,758</td>
<td align="right">83,678,292</td>
<td align="right">-17.9%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">569,933,157</td>
<td align="right">472,289,955</td>
<td align="right">-17.1%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">529,282,057</td>
<td align="right">603,648,531</td>
<td align="right">14.1%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">118,806,903</td>
<td align="right">102,253,118</td>
<td align="right">-13.9%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">489,873,072</td>
<td align="right">425,022,432</td>
<td align="right">-13.2%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">2,342,080,774</td>
<td align="right">2,595,321,066</td>
<td align="right">10.8%</td>
</tr>
<tr>
<td align="left">UNARY_NOT</td>
<td align="right">28,362,762</td>
<td align="right">25,382,935</td>
<td align="right">-10.5%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">5,404,229,577</td>
<td align="right">5,948,241,263</td>
<td align="right">10.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_AND_CLEAR</td>
<td align="right">85,733,933</td>
<td align="right">77,900,752</td>
<td align="right">-9.1%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">3,374,250,446</td>
<td align="right">3,678,351,487</td>
<td align="right">9.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">1,282,500,727</td>
<td align="right">1,174,183,482</td>
<td align="right">-8.4%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_DICT</td>
<td align="right">400,497,462</td>
<td align="right">433,814,773</td>
<td align="right">8.3%</td>
</tr>
<tr>
<td align="left">STORE_FAST_STORE_FAST</td>
<td align="right">382,367,297</td>
<td align="right">413,926,093</td>
<td align="right">8.3%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">2,619,357,899</td>
<td align="right">2,817,033,905</td>
<td align="right">7.5%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP_SET</td>
<td align="right">340,817,414</td>
<td align="right">366,260,529</td>
<td align="right">7.5%</td>
</tr>
<tr>
<td align="left">BINARY_OP_INPLACE_ADD_UNICODE</td>
<td align="right">4,824,622</td>
<td align="right">5,184,215</td>
<td align="right">7.5%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">58,000,711</td>
<td align="right">62,107,085</td>
<td align="right">7.1%</td>
</tr>
<tr>
<td align="left">LIST_APPEND</td>
<td align="right">94,641,211</td>
<td align="right">101,208,725</td>
<td align="right">6.9%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">559,498,490</td>
<td align="right">524,892,076</td>
<td align="right">-6.2%</td>
</tr>
<tr>
<td align="left">DICT_MERGE</td>
<td align="right">42,881,386</td>
<td align="right">45,415,762</td>
<td align="right">5.9%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_CLASS</td>
<td align="right">158,275,650</td>
<td align="right">149,087,423</td>
<td align="right">-5.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">1,433,195,592</td>
<td align="right">1,513,936,004</td>
<td align="right">5.6%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">1,174,337,703</td>
<td align="right">1,240,377,925</td>
<td align="right">5.6%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">1,129,197,042</td>
<td align="right">1,065,717,649</td>
<td align="right">-5.6%</td>
</tr>
<tr>
<td align="left">TO_BOOL_INT</td>
<td align="right">127,908,705</td>
<td align="right">120,757,852</td>
<td align="right">-5.6%</td>
</tr>
<tr>
<td align="left">CALL_ISINSTANCE</td>
<td align="right">760,301,679</td>
<td align="right">800,277,378</td>
<td align="right">5.3%</td>
</tr>
<tr>
<td align="left">TO_BOOL_LIST</td>
<td align="right">113,081,354</td>
<td align="right">107,485,193</td>
<td align="right">-4.9%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">2,987,110,252</td>
<td align="right">2,839,356,248</td>
<td align="right">-4.9%</td>
</tr>
<tr>
<td align="left">LIST_EXTEND</td>
<td align="right">27,961,573</td>
<td align="right">29,277,767</td>
<td align="right">4.7%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_FLOAT</td>
<td align="right">72,562,392</td>
<td align="right">69,196,914</td>
<td align="right">-4.6%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_GETITEM</td>
<td align="right">62,131,885</td>
<td align="right">64,907,632</td>
<td align="right">4.5%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_TUPLE_INT</td>
<td align="right">178,749,971</td>
<td align="right">186,029,027</td>
<td align="right">4.1%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">131,239,575</td>
<td align="right">136,558,613</td>
<td align="right">4.1%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">5,001,385,717</td>
<td align="right">5,197,685,900</td>
<td align="right">3.9%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NOT_NONE</td>
<td align="right">658,766,873</td>
<td align="right">633,428,678</td>
<td align="right">-3.8%</td>
</tr>
<tr>
<td align="left">CALL_LEN</td>
<td align="right">286,030,880</td>
<td align="right">275,819,486</td>
<td align="right">-3.6%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NONE</td>
<td align="right">383,241,080</td>
<td align="right">370,275,289</td>
<td align="right">-3.4%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_DICT</td>
<td align="right">146,455,247</td>
<td align="right">142,315,983</td>
<td align="right">-2.8%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">2,537,825,959</td>
<td align="right">2,607,522,234</td>
<td align="right">2.7%</td>
</tr>
<tr>
<td align="left">CALL_TUPLE_1</td>
<td align="right">21,331,969</td>
<td align="right">20,747,115</td>
<td align="right">-2.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_LAZY_DICT</td>
<td align="right">246,013,453</td>
<td align="right">252,038,089</td>
<td align="right">2.4%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">364,381,894</td>
<td align="right">355,947,265</td>
<td align="right">-2.3%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">247,647,861</td>
<td align="right">241,919,079</td>
<td align="right">-2.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">3,966,061,266</td>
<td align="right">3,877,917,539</td>
<td align="right">-2.2%</td>
</tr>
<tr>
<td align="left">BUILD_MAP</td>
<td align="right">122,818,875</td>
<td align="right">120,193,253</td>
<td align="right">-2.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_WITH_HINT</td>
<td align="right">233,243,353</td>
<td align="right">238,206,691</td>
<td align="right">2.1%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE</td>
<td align="right">529,624</td>
<td align="right">540,674</td>
<td align="right">2.1%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST_WITH_KEYWORDS</td>
<td align="right">40,662,728</td>
<td align="right">41,407,081</td>
<td align="right">1.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_CHECK</td>
<td align="right">11,090,503</td>
<td align="right">10,887,552</td>
<td align="right">-1.8%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_UNICODE</td>
<td align="right">72,104,727</td>
<td align="right">70,801,336</td>
<td align="right">-1.8%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">232,286,164</td>
<td align="right">228,261,407</td>
<td align="right">-1.7%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">4,013,229,156</td>
<td align="right">4,082,638,860</td>
<td align="right">1.7%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_STR</td>
<td align="right">310,740,134</td>
<td align="right">316,064,943</td>
<td align="right">1.7%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">3,243,389,913</td>
<td align="right">3,298,068,800</td>
<td align="right">1.7%</td>
</tr>
<tr>
<td align="left">PUSH_NULL</td>
<td align="right">1,077,004,968</td>
<td align="right">1,094,820,431</td>
<td align="right">1.7%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">5,654,125,516</td>
<td align="right">5,566,987,205</td>
<td align="right">-1.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">21,804,805,898</td>
<td align="right">22,102,977,235</td>
<td align="right">1.4%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_O</td>
<td align="right">520,162,823</td>
<td align="right">526,947,516</td>
<td align="right">1.3%</td>
</tr>
<tr>
<td align="left">JUMP_FORWARD</td>
<td align="right">427,161,884</td>
<td align="right">422,047,167</td>
<td align="right">-1.2%</td>
</tr>
<tr>
<td align="left">MAKE_CELL</td>
<td align="right">103,581,938</td>
<td align="right">104,775,023</td>
<td align="right">1.2%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT</td>
<td align="right">1,150,572,046</td>
<td align="right">1,137,899,481</td>
<td align="right">-1.1%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_LIST_INT</td>
<td align="right">98,669,698</td>
<td align="right">99,720,415</td>
<td align="right">1.1%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_LIST_INT</td>
<td align="right">412,574,212</td>
<td align="right">408,466,445</td>
<td align="right">-1.0%</td>
</tr>
<tr>
<td align="left">IS_OP</td>
<td align="right">410,824,399</td>
<td align="right">414,907,435</td>
<td align="right">1.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">1,657,367,839</td>
<td align="right">1,641,274,888</td>
<td align="right">-1.0%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">6,333,687,206</td>
<td align="right">6,394,671,415</td>
<td align="right">1.0%</td>
</tr>
<tr>
<td align="left">CALL_INTRINSIC_1</td>
<td align="right">153,640,215</td>
<td align="right">154,993,917</td>
<td align="right">0.9%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">484,366,323</td>
<td align="right">488,620,388</td>
<td align="right">0.9%</td>
</tr>
<tr>
<td align="left">BUILD_LIST</td>
<td align="right">225,463,095</td>
<td align="right">223,661,783</td>
<td align="right">-0.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">782,190,528</td>
<td align="right">776,098,574</td>
<td align="right">-0.8%</td>
</tr>
<tr>
<td align="left">INSTRUMENTED_JUMP_BACKWARD</td>
<td align="right">6,212</td>
<td align="right">6,260</td>
<td align="right">0.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right">118,810,744</td>
<td align="right">117,983,367</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_INT</td>
<td align="right">383,212,750</td>
<td align="right">385,853,724</td>
<td align="right">0.7%</td>
</tr>
<tr>
<td align="left">STORE_DEREF</td>
<td align="right">94,323,245</td>
<td align="right">94,908,122</td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR</td>
<td align="right">69,679,233</td>
<td align="right">70,042,475</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">TO_BOOL_NONE</td>
<td align="right">500,872,015</td>
<td align="right">498,364,077</td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_SLOT</td>
<td align="right">1,497,125,190</td>
<td align="right">1,490,726,859</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_LIST</td>
<td align="right">8,183,835</td>
<td align="right">8,217,328</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_PROPERTY</td>
<td align="right">61,394,355</td>
<td align="right">61,148,893</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">4,749,113,161</td>
<td align="right">4,767,367,316</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">BINARY_SLICE</td>
<td align="right">223,892,264</td>
<td align="right">224,664,021</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">TO_BOOL_ALWAYS_TRUE</td>
<td align="right">180,195,901</td>
<td align="right">179,624,245</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_INT</td>
<td align="right">642,690,608</td>
<td align="right">644,697,470</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">UNARY_INVERT</td>
<td align="right">2,034,889</td>
<td align="right">2,040,849</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">SET_FUNCTION_ATTRIBUTE</td>
<td align="right">53,514,040</td>
<td align="right">53,357,309</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">CALL_STR_1</td>
<td align="right">38,332,258</td>
<td align="right">38,441,407</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_NO_DICT</td>
<td align="right">62,356,049</td>
<td align="right">62,525,004</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_CLASS</td>
<td align="right">139,134,463</td>
<td align="right">138,776,595</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">MAKE_FUNCTION</td>
<td align="right">65,589,446</td>
<td align="right">65,445,871</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">BINARY_OP_MULTIPLY_INT</td>
<td align="right">164,098,748</td>
<td align="right">163,744,691</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">STORE_GLOBAL</td>
<td align="right">6,929,920</td>
<td align="right">6,944,700</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">184,561,516</td>
<td align="right">184,297,981</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">2,050,103,455</td>
<td align="right">2,047,291,175</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">INTERPRETER_EXIT</td>
<td align="right">2,311,755,604</td>
<td align="right">2,308,964,439</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">71,038,424</td>
<td align="right">70,956,717</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_MODULE</td>
<td align="right">519,606,644</td>
<td align="right">519,027,833</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_STR_INT</td>
<td align="right">455,276,518</td>
<td align="right">455,665,370</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">RETURN_GENERATOR</td>
<td align="right">414,263,913</td>
<td align="right">413,941,955</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">UNARY_NEGATIVE</td>
<td align="right">145,893,407</td>
<td align="right">145,995,166</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST_WITH_KEYWORDS</td>
<td align="right">40,853,627</td>
<td align="right">40,828,851</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">DICT_UPDATE</td>
<td align="right">73,490</td>
<td align="right">73,452</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">COPY_FREE_VARS</td>
<td align="right">287,013,235</td>
<td align="right">287,157,800</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">BEFORE_WITH</td>
<td align="right">10,084,662</td>
<td align="right">10,080,720</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR</td>
<td align="right">23,573</td>
<td align="right">23,565</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">BUILD_SLICE</td>
<td align="right">71,719,213</td>
<td align="right">71,695,340</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">1,676,306</td>
<td align="right">1,676,799</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">DELETE_FAST</td>
<td align="right">2,232,572</td>
<td align="right">2,231,927</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">RERAISE</td>
<td align="right">4,244,585</td>
<td align="right">4,243,429</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">FOR_ITER_GEN</td>
<td align="right">83,330,318</td>
<td align="right">83,352,812</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR_METHOD</td>
<td align="right">126,670,852</td>
<td align="right">126,638,040</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">CHECK_EXC_MATCH</td>
<td align="right">24,470,055</td>
<td align="right">24,465,047</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">POP_EXCEPT</td>
<td align="right">24,973,885</td>
<td align="right">24,968,907</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">PUSH_EXC_INFO</td>
<td align="right">24,981,655</td>
<td align="right">24,976,679</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">YIELD_VALUE</td>
<td align="right">1,355,126,404</td>
<td align="right">1,354,906,614</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">345,460</td>
<td align="right">345,413</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_FLOAT</td>
<td align="right">75,390,063</td>
<td align="right">75,400,144</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">RAISE_VARARGS</td>
<td align="right">6,185,474</td>
<td align="right">6,185,044</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">IMPORT_FROM</td>
<td align="right">13,105,204</td>
<td align="right">13,104,308</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">CALL_PY_WITH_DEFAULTS</td>
<td align="right">216,506,294</td>
<td align="right">216,492,423</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">IMPORT_NAME</td>
<td align="right">12,437,044</td>
<td align="right">12,436,278</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_WITH_HINT</td>
<td align="right">62,856,298</td>
<td align="right">62,852,453</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_FLOAT</td>
<td align="right">149,894,275</td>
<td align="right">149,885,850</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">1,208,358,635</td>
<td align="right">1,208,305,125</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">NOP</td>
<td align="right">919,050,508</td>
<td align="right">919,010,219</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">BUILD_SET</td>
<td align="right">2,329,834</td>
<td align="right">2,329,757</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">WITH_EXCEPT_START</td>
<td align="right">233,490</td>
<td align="right">233,483</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">20,773,312</td>
<td align="right">20,772,741</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">CLEANUP_THROW</td>
<td align="right">152,063</td>
<td align="right">152,060</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">END_FOR</td>
<td align="right">82,357,285</td>
<td align="right">82,358,881</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD_NO_INTERRUPT</td>
<td align="right">556,686,303</td>
<td align="right">556,680,360</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">CALL_LIST_APPEND</td>
<td align="right">348,145,792</td>
<td align="right">348,142,568</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR_ATTR</td>
<td align="right">7,751,831</td>
<td align="right">7,751,767</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">SEND_GEN</td>
<td align="right">787,117,718</td>
<td align="right">787,115,718</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">BEFORE_ASYNC_WITH</td>
<td align="right">3,005,926</td>
<td align="right">3,005,920</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">GET_YIELD_FROM_ITER</td>
<td align="right">46,592,624</td>
<td align="right">46,592,542</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">GET_AWAITABLE</td>
<td align="right">229,143,065</td>
<td align="right">229,142,706</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">CALL_KW</td>
<td align="right">273,955,050</td>
<td align="right">273,954,712</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">END_SEND</td>
<td align="right">402,624,934</td>
<td align="right">402,624,579</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">SEND</td>
<td align="right">173,840,668</td>
<td align="right">173,840,612</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">CALL_FUNCTION_EX</td>
<td align="right">218,826,223</td>
<td align="right">218,826,202</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">EXIT_INIT_CHECK</td>
<td align="right">94,703,946</td>
<td align="right">94,703,938</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">CALL_ALLOC_AND_ENTER_INIT</td>
<td align="right">96,992,008</td>
<td align="right">96,992,000</td>
<td align="right">-0.0%</td>
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
<td align="left">LOAD_NAME</td>
<td align="right">8,145,287</td>
<td align="right">8,145,287</td>
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
<td align="left">UNPACK_EX</td>
<td align="right">1,129,822</td>
<td align="right">1,129,822</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_NAME</td>
<td align="right">641,202</td>
<td align="right">641,202</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">SET_UPDATE</td>
<td align="right">200,488</td>
<td align="right">200,488</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_GETATTRIBUTE_OVERRIDDEN</td>
<td align="right">89,680</td>
<td align="right">89,680</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_BUILD_CLASS</td>
<td align="right">30,746</td>
<td align="right">30,746</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_LOCALS</td>
<td align="right">2,260</td>
<td align="right">2,260</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_FROM_DICT_OR_DEREF</td>
<td align="right">2,240</td>
<td align="right">2,240</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">INSTRUMENTED_RETURN_CONST</td>
<td align="right">2,160</td>
<td align="right">2,160</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">FORMAT_WITH_SPEC</td>
<td align="right">1,760</td>
<td align="right">1,760</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">SETUP_ANNOTATIONS</td>
<td align="right">1,524</td>
<td align="right">1,524</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">DELETE_NAME</td>
<td align="right">1,100</td>
<td align="right">1,100</td>
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
<td align="right">598,961,048</td>
<td align="right">28.1%</td>
<td align="right">500,018,158</td>
<td align="right">24.1%</td>
<td align="right">-16.5%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">30,888,228</td>
<td align="right">1.4%</td>
<td align="right">29,508,393</td>
<td align="right">1.4%</td>
<td align="right">-4.5%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">1,530,524,856</td>
<td align="right">71.8%</td>
<td align="right">1,575,692,243</td>
<td align="right">75.8%</td>
<td align="right">3.0%</td>
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
<td align="right">1,224,146</td>
<td align="right">65.8%</td>
<td align="right">1,170,229</td>
<td align="right">65.7%</td>
<td align="right">-4.4%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">636,191</td>
<td align="right">34.2%</td>
<td align="right">609,961</td>
<td align="right">34.3%</td>
<td align="right">-4.1%</td>
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
<td align="left">remainder</td>
<td align="right">50,416</td>
<td align="right">4.1%</td>
<td align="right">26,614</td>
<td align="right">2.3%</td>
<td align="right">-47.2%</td>
</tr>
<tr>
<td align="left">add different types</td>
<td align="right">78,526</td>
<td align="right">6.4%</td>
<td align="right">51,069</td>
<td align="right">4.4%</td>
<td align="right">-35.0%</td>
</tr>
<tr>
<td align="left">and different types</td>
<td align="right">619</td>
<td align="right">0.1%</td>
<td align="right">580</td>
<td align="right">0.0%</td>
<td align="right">-6.3%</td>
</tr>
<tr>
<td align="left">multiply different types</td>
<td align="right">92,002</td>
<td align="right">7.5%</td>
<td align="right">88,216</td>
<td align="right">7.5%</td>
<td align="right">-4.1%</td>
</tr>
<tr>
<td align="left">and int</td>
<td align="right">36,727</td>
<td align="right">3.0%</td>
<td align="right">37,745</td>
<td align="right">3.2%</td>
<td align="right">2.8%</td>
</tr>
<tr>
<td align="left">lshift</td>
<td align="right">5,720</td>
<td align="right">0.5%</td>
<td align="right">5,828</td>
<td align="right">0.5%</td>
<td align="right">1.9%</td>
</tr>
<tr>
<td align="left">subtract other</td>
<td align="right">11,334</td>
<td align="right">0.9%</td>
<td align="right">11,534</td>
<td align="right">1.0%</td>
<td align="right">1.8%</td>
</tr>
<tr>
<td align="left">true divide float</td>
<td align="right">5,668</td>
<td align="right">0.5%</td>
<td align="right">5,764</td>
<td align="right">0.5%</td>
<td align="right">1.7%</td>
</tr>
<tr>
<td align="left">xor</td>
<td align="right">8,128</td>
<td align="right">0.7%</td>
<td align="right">8,264</td>
<td align="right">0.7%</td>
<td align="right">1.7%</td>
</tr>
<tr>
<td align="left">rshift</td>
<td align="right">8,863</td>
<td align="right">0.7%</td>
<td align="right">8,997</td>
<td align="right">0.8%</td>
<td align="right">1.5%</td>
</tr>
<tr>
<td align="left">true divide other</td>
<td align="right">3,441</td>
<td align="right">0.3%</td>
<td align="right">3,400</td>
<td align="right">0.3%</td>
<td align="right">-1.2%</td>
</tr>
<tr>
<td align="left">add other</td>
<td align="right">64,269</td>
<td align="right">5.3%</td>
<td align="right">63,871</td>
<td align="right">5.5%</td>
<td align="right">-0.6%</td>
</tr>
<tr>
<td align="left">power</td>
<td align="right">5,776</td>
<td align="right">0.5%</td>
<td align="right">5,748</td>
<td align="right">0.5%</td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">true divide different types</td>
<td align="right">12,523</td>
<td align="right">1.0%</td>
<td align="right">12,508</td>
<td align="right">1.1%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">or</td>
<td align="right">17,151</td>
<td align="right">1.4%</td>
<td align="right">17,170</td>
<td align="right">1.5%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">and other</td>
<td align="right">2,016</td>
<td align="right">0.2%</td>
<td align="right">2,014</td>
<td align="right">0.2%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">floor divide</td>
<td align="right">33,252</td>
<td align="right">2.7%</td>
<td align="right">33,236</td>
<td align="right">2.8%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">subtract different types</td>
<td align="right">782,495</td>
<td align="right">63.9%</td>
<td align="right">782,451</td>
<td align="right">66.9%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">multiply other</td>
<td align="right">5,220</td>
<td align="right">0.4%</td>
<td align="right">5,220</td>
<td align="right">0.4%</td>
<td align="right">0.0%</td>
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
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">268,540,656</td>
<td align="right">15.1%</td>
<td align="right">329,294,716</td>
<td align="right">17.6%</td>
<td align="right">22.6%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">1,504,328,633</td>
<td align="right">84.8%</td>
<td align="right">1,543,980,739</td>
<td align="right">82.4%</td>
<td align="right">2.6%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">4,901,415</td>
<td align="right">0.3%</td>
<td align="right">4,902,508</td>
<td align="right">0.3%</td>
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
<td align="right">143,901</td>
<td align="right">41.6%</td>
<td align="right">160,136</td>
<td align="right">44.2%</td>
<td align="right">11.3%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">201,847</td>
<td align="right">58.4%</td>
<td align="right">201,843</td>
<td align="right">55.8%</td>
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
<td align="right">25,085</td>
<td align="right">17.4%</td>
<td align="right">40,645</td>
<td align="right">25.4%</td>
<td align="right">62.0%</td>
</tr>
<tr>
<td align="left">buffer slice</td>
<td align="right">900</td>
<td align="right">0.6%</td>
<td align="right">880</td>
<td align="right">0.5%</td>
<td align="right">-2.2%</td>
</tr>
<tr>
<td align="left">tuple slice</td>
<td align="right">188</td>
<td align="right">0.1%</td>
<td align="right">184</td>
<td align="right">0.1%</td>
<td align="right">-2.1%</td>
</tr>
<tr>
<td align="left">array int</td>
<td align="right">15,880</td>
<td align="right">11.0%</td>
<td align="right">16,200</td>
<td align="right">10.1%</td>
<td align="right">2.0%</td>
</tr>
<tr>
<td align="left">buffer int</td>
<td align="right">22,243</td>
<td align="right">15.5%</td>
<td align="right">22,642</td>
<td align="right">14.1%</td>
<td align="right">1.8%</td>
</tr>
<tr>
<td align="left">code complex parameters</td>
<td align="right">4,998</td>
<td align="right">3.5%</td>
<td align="right">4,935</td>
<td align="right">3.1%</td>
<td align="right">-1.3%</td>
</tr>
<tr>
<td align="left">out of range</td>
<td align="right">68,847</td>
<td align="right">47.8%</td>
<td align="right">68,890</td>
<td align="right">43.0%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">sequence int</td>
<td align="right">4,300</td>
<td align="right">3.0%</td>
<td align="right">4,300</td>
<td align="right">2.7%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">list slice</td>
<td align="right">1,360</td>
<td align="right">0.9%</td>
<td align="right">1,360</td>
<td align="right">0.8%</td>
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
deopt
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">33,100</td>
<td align="right">0.0%</td>
<td align="right">28,860</td>
<td align="right">0.0%</td>
<td align="right">-12.8%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">6,639,625,657</td>
<td align="right">82.0%</td>
<td align="right">6,768,992,197</td>
<td align="right">82.3%</td>
<td align="right">1.9%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">245,109,647</td>
<td align="right">3.0%</td>
<td align="right">244,617,738</td>
<td align="right">3.0%</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">1,447,251,749</td>
<td align="right">17.9%</td>
<td align="right">1,446,715,956</td>
<td align="right">17.6%</td>
<td align="right">-0.0%</td>
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
<td align="right">5,254,767</td>
<td align="right">84.5%</td>
<td align="right">5,245,282</td>
<td align="right">84.5%</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">961,766</td>
<td align="right">15.5%</td>
<td align="right">961,625</td>
<td align="right">15.5%</td>
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
<td align="left">metaclass</td>
<td align="right">43,300</td>
<td align="right">4.5%</td>
<td align="right">43,182</td>
<td align="right">4.5%</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">bound method</td>
<td align="right">12,030</td>
<td align="right">1.3%</td>
<td align="right">12,014</td>
<td align="right">1.2%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">out of versions</td>
<td align="right">981</td>
<td align="right">0.1%</td>
<td align="right">980</td>
<td align="right">0.1%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">meth descr varargs keywords</td>
<td align="right">20,889</td>
<td align="right">2.2%</td>
<td align="right">20,904</td>
<td align="right">2.2%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">cfunc noargs</td>
<td align="right">69,472</td>
<td align="right">7.2%</td>
<td align="right">69,511</td>
<td align="right">7.2%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">cfunc varargs</td>
<td align="right">14,255</td>
<td align="right">1.5%</td>
<td align="right">14,249</td>
<td align="right">1.5%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">cfunc varargs keywords</td>
<td align="right">32,260</td>
<td align="right">3.4%</td>
<td align="right">32,250</td>
<td align="right">3.4%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">class no vectorcall</td>
<td align="right">89,332</td>
<td align="right">9.3%</td>
<td align="right">89,311</td>
<td align="right">9.3%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">65,816</td>
<td align="right">6.8%</td>
<td align="right">65,802</td>
<td align="right">6.8%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">class mutable</td>
<td align="right">24,739</td>
<td align="right">2.6%</td>
<td align="right">24,734</td>
<td align="right">2.6%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">code complex parameters</td>
<td align="right">185,195</td>
<td align="right">19.3%</td>
<td align="right">185,179</td>
<td align="right">19.3%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">meth descr varargs</td>
<td align="right">16,518</td>
<td align="right">1.7%</td>
<td align="right">16,517</td>
<td align="right">1.7%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">meth descr method fastcall keywords</td>
<td align="right">207,186</td>
<td align="right">21.5%</td>
<td align="right">207,198</td>
<td align="right">21.5%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">init not inline values</td>
<td align="right">105,557</td>
<td align="right">11.0%</td>
<td align="right">105,557</td>
<td align="right">11.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">init not python</td>
<td align="right">16,386</td>
<td align="right">1.7%</td>
<td align="right">16,386</td>
<td align="right">1.7%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">wrong number arguments</td>
<td align="right">13,753</td>
<td align="right">1.4%</td>
<td align="right">13,753</td>
<td align="right">1.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">cmethod</td>
<td align="right">13,620</td>
<td align="right">1.4%</td>
<td align="right">13,620</td>
<td align="right">1.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">init not simple</td>
<td align="right">12,278</td>
<td align="right">1.3%</td>
<td align="right">12,278</td>
<td align="right">1.3%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">operator wrapper</td>
<td align="right">10,136</td>
<td align="right">1.1%</td>
<td align="right">10,136</td>
<td align="right">1.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">method wrapper</td>
<td align="right">8,224</td>
<td align="right">0.9%</td>
<td align="right">8,224</td>
<td align="right">0.9%</td>
<td align="right">0.0%</td>
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
<td align="right">132,656,051</td>
<td align="right">7.6%</td>
<td align="right">138,038,672</td>
<td align="right">7.9%</td>
<td align="right">4.1%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">1,750,295</td>
<td align="right">0.1%</td>
<td align="right">1,819,394</td>
<td align="right">0.1%</td>
<td align="right">3.9%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">1,609,456,160</td>
<td align="right">92.4%</td>
<td align="right">1,602,030,880</td>
<td align="right">92.0%</td>
<td align="right">-0.5%</td>
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
<td align="right">222,832</td>
<td align="right">66.8%</td>
<td align="right">227,086</td>
<td align="right">66.9%</td>
<td align="right">1.9%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">110,987</td>
<td align="right">33.2%</td>
<td align="right">112,249</td>
<td align="right">33.1%</td>
<td align="right">1.1%</td>
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
<td align="left">set</td>
<td align="right">1,663</td>
<td align="right">0.7%</td>
<td align="right">2,343</td>
<td align="right">1.0%</td>
<td align="right">40.9%</td>
</tr>
<tr>
<td align="left">bytes</td>
<td align="right">3,680</td>
<td align="right">1.7%</td>
<td align="right">3,880</td>
<td align="right">1.7%</td>
<td align="right">5.4%</td>
</tr>
<tr>
<td align="left">big int</td>
<td align="right">58,961</td>
<td align="right">26.5%</td>
<td align="right">61,460</td>
<td align="right">27.1%</td>
<td align="right">4.2%</td>
</tr>
<tr>
<td align="left">baseobject</td>
<td align="right">31,179</td>
<td align="right">14.0%</td>
<td align="right">32,360</td>
<td align="right">14.3%</td>
<td align="right">3.8%</td>
</tr>
<tr>
<td align="left">float long</td>
<td align="right">16,209</td>
<td align="right">7.3%</td>
<td align="right">15,943</td>
<td align="right">7.0%</td>
<td align="right">-1.6%</td>
</tr>
<tr>
<td align="left">string</td>
<td align="right">11,080</td>
<td align="right">5.0%</td>
<td align="right">10,920</td>
<td align="right">4.8%</td>
<td align="right">-1.4%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">14,550</td>
<td align="right">6.5%</td>
<td align="right">14,406</td>
<td align="right">6.3%</td>
<td align="right">-1.0%</td>
</tr>
<tr>
<td align="left">bool</td>
<td align="right">3,788</td>
<td align="right">1.7%</td>
<td align="right">3,823</td>
<td align="right">1.7%</td>
<td align="right">0.9%</td>
</tr>
<tr>
<td align="left">different types</td>
<td align="right">54,033</td>
<td align="right">24.2%</td>
<td align="right">54,205</td>
<td align="right">23.9%</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">21,941</td>
<td align="right">9.8%</td>
<td align="right">21,999</td>
<td align="right">9.7%</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">long float</td>
<td align="right">1,534</td>
<td align="right">0.7%</td>
<td align="right">1,536</td>
<td align="right">0.7%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">4,214</td>
<td align="right">1.9%</td>
<td align="right">4,211</td>
<td align="right">1.9%</td>
<td align="right">-0.1%</td>
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
<td align="right">104,334,443</td>
<td align="right">19.1%</td>
<td align="right">86,033,546</td>
<td align="right">14.6%</td>
<td align="right">-17.5%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">442,451,219</td>
<td align="right">80.9%</td>
<td align="right">502,556,149</td>
<td align="right">85.4%</td>
<td align="right">13.6%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">2,546,240</td>
<td align="right">0.5%</td>
<td align="right">2,546,240</td>
<td align="right">0.4%</td>
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
<td align="right">125,043</td>
<td align="right">64.9%</td>
<td align="right">123,474</td>
<td align="right">64.7%</td>
<td align="right">-1.3%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">67,512</td>
<td align="right">35.1%</td>
<td align="right">67,512</td>
<td align="right">35.3%</td>
<td align="right">0.0%</td>
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
<td align="left">str</td>
<td align="right">33,285</td>
<td align="right">26.6%</td>
<td align="right">29,944</td>
<td align="right">24.3%</td>
<td align="right">-10.0%</td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">18,064</td>
<td align="right">14.4%</td>
<td align="right">19,199</td>
<td align="right">15.5%</td>
<td align="right">6.3%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">27,363</td>
<td align="right">21.9%</td>
<td align="right">27,835</td>
<td align="right">22.5%</td>
<td align="right">1.7%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">46,331</td>
<td align="right">37.1%</td>
<td align="right">46,496</td>
<td align="right">37.7%</td>
<td align="right">0.4%</td>
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
<td align="right">330,613</td>
<td align="right">0.1%</td>
<td align="right">2,929,312</td>
<td align="right">0.5%</td>
<td align="right">786.0%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">147,469,644</td>
<td align="right">55.3%</td>
<td align="right">521,958,576</td>
<td align="right">83.2%</td>
<td align="right">253.9%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">118,900,180</td>
<td align="right">44.6%</td>
<td align="right">104,901,985</td>
<td align="right">16.7%</td>
<td align="right">-11.8%</td>
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
<td align="right">72,427</td>
<td align="right">30.5%</td>
<td align="right">121,389</td>
<td align="right">43.3%</td>
<td align="right">67.6%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">164,909</td>
<td align="right">69.5%</td>
<td align="right">159,056</td>
<td align="right">56.7%</td>
<td align="right">-3.5%</td>
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
<td align="left">seq iter</td>
<td align="right">6,060</td>
<td align="right">3.7%</td>
<td align="right">3,780</td>
<td align="right">2.4%</td>
<td align="right">-37.6%</td>
</tr>
<tr>
<td align="left">dict items</td>
<td align="right">50,177</td>
<td align="right">30.4%</td>
<td align="right">47,485</td>
<td align="right">29.9%</td>
<td align="right">-5.4%</td>
</tr>
<tr>
<td align="left">enumerate</td>
<td align="right">19,752</td>
<td align="right">12.0%</td>
<td align="right">19,145</td>
<td align="right">12.0%</td>
<td align="right">-3.1%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">22,774</td>
<td align="right">13.8%</td>
<td align="right">22,429</td>
<td align="right">14.1%</td>
<td align="right">-1.5%</td>
</tr>
<tr>
<td align="left">dict values</td>
<td align="right">6,790</td>
<td align="right">4.1%</td>
<td align="right">6,706</td>
<td align="right">4.2%</td>
<td align="right">-1.2%</td>
</tr>
<tr>
<td align="left">dict keys</td>
<td align="right">14,549</td>
<td align="right">8.8%</td>
<td align="right">14,675</td>
<td align="right">9.2%</td>
<td align="right">0.9%</td>
</tr>
<tr>
<td align="left">ascii string</td>
<td align="right">2,640</td>
<td align="right">1.6%</td>
<td align="right">2,660</td>
<td align="right">1.7%</td>
<td align="right">0.8%</td>
</tr>
<tr>
<td align="left">itertools</td>
<td align="right">7,249</td>
<td align="right">4.4%</td>
<td align="right">7,258</td>
<td align="right">4.6%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">zip</td>
<td align="right">14,352</td>
<td align="right">8.7%</td>
<td align="right">14,352</td>
<td align="right">9.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">10,999</td>
<td align="right">6.7%</td>
<td align="right">10,999</td>
<td align="right">6.9%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">reversed list</td>
<td align="right">7,865</td>
<td align="right">4.8%</td>
<td align="right">7,865</td>
<td align="right">4.9%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">map</td>
<td align="right">740</td>
<td align="right">0.4%</td>
<td align="right">740</td>
<td align="right">0.5%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">bytes</td>
<td align="right">660</td>
<td align="right">0.4%</td>
<td align="right">660</td>
<td align="right">0.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">callable</td>
<td align="right">282</td>
<td align="right">0.2%</td>
<td align="right">282</td>
<td align="right">0.2%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">string</td>
<td align="right">20</td>
<td align="right">0.0%</td>
<td align="right">20</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
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
<td align="right">479,942,573</td>
<td align="right">4.6%</td>
<td align="right">429,534,631</td>
<td align="right">4.1%</td>
<td align="right">-10.5%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">1,251,113,517</td>
<td align="right">11.9%</td>
<td align="right">1,195,563,300</td>
<td align="right">11.5%</td>
<td align="right">-4.4%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">9,239,831,592</td>
<td align="right">88.0%</td>
<td align="right">9,167,573,434</td>
<td align="right">88.4%</td>
<td align="right">-0.8%</td>
</tr>
<tr>
<td align="left">
deopt
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">680,343</td>
<td align="right">0.0%</td>
<td align="right">680,516</td>
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
<td align="right">9,942,682</td>
<td align="right">90.2%</td>
<td align="right">8,991,663</td>
<td align="right">89.3%</td>
<td align="right">-9.6%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">1,076,902</td>
<td align="right">9.8%</td>
<td align="right">1,078,242</td>
<td align="right">10.7%</td>
<td align="right">0.1%</td>
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
<td align="left">non string or split</td>
<td align="right">21,933</td>
<td align="right">2.0%</td>
<td align="right">20,636</td>
<td align="right">1.9%</td>
<td align="right">-5.9%</td>
</tr>
<tr>
<td align="left">non object slot</td>
<td align="right">3,540</td>
<td align="right">0.3%</td>
<td align="right">3,382</td>
<td align="right">0.3%</td>
<td align="right">-4.5%</td>
</tr>
<tr>
<td align="left">builtin class method</td>
<td align="right">3,797</td>
<td align="right">0.4%</td>
<td align="right">3,681</td>
<td align="right">0.3%</td>
<td align="right">-3.1%</td>
</tr>
<tr>
<td align="left">metaclass attribute</td>
<td align="right">187,958</td>
<td align="right">17.5%</td>
<td align="right">191,420</td>
<td align="right">17.8%</td>
<td align="right">1.8%</td>
</tr>
<tr>
<td align="left">class method obj</td>
<td align="right">20,915</td>
<td align="right">1.9%</td>
<td align="right">20,538</td>
<td align="right">1.9%</td>
<td align="right">-1.8%</td>
</tr>
<tr>
<td align="left">not in keys</td>
<td align="right">15,620</td>
<td align="right">1.5%</td>
<td align="right">15,840</td>
<td align="right">1.5%</td>
<td align="right">1.4%</td>
</tr>
<tr>
<td align="left">out of versions</td>
<td align="right">2,281</td>
<td align="right">0.2%</td>
<td align="right">2,310</td>
<td align="right">0.2%</td>
<td align="right">1.3%</td>
</tr>
<tr>
<td align="left">non overriding descriptor</td>
<td align="right">13,434</td>
<td align="right">1.2%</td>
<td align="right">13,314</td>
<td align="right">1.2%</td>
<td align="right">-0.9%</td>
</tr>
<tr>
<td align="left">mutable class</td>
<td align="right">77,135</td>
<td align="right">7.2%</td>
<td align="right">77,683</td>
<td align="right">7.2%</td>
<td align="right">0.7%</td>
</tr>
<tr>
<td align="left">method</td>
<td align="right">114,182</td>
<td align="right">10.6%</td>
<td align="right">114,969</td>
<td align="right">10.7%</td>
<td align="right">0.7%</td>
</tr>
<tr>
<td align="left">overridden</td>
<td align="right">19,279</td>
<td align="right">1.8%</td>
<td align="right">19,150</td>
<td align="right">1.8%</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">class attr descriptor</td>
<td align="right">29,980</td>
<td align="right">2.8%</td>
<td align="right">29,840</td>
<td align="right">2.8%</td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">shadowed</td>
<td align="right">138,232</td>
<td align="right">12.8%</td>
<td align="right">137,644</td>
<td align="right">12.8%</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">not managed dict</td>
<td align="right">246,798</td>
<td align="right">22.9%</td>
<td align="right">246,102</td>
<td align="right">22.8%</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">module attr not found</td>
<td align="right">17,662</td>
<td align="right">1.6%</td>
<td align="right">17,682</td>
<td align="right">1.6%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">class attr simple</td>
<td align="right">162,376</td>
<td align="right">15.1%</td>
<td align="right">162,271</td>
<td align="right">15.0%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">wrong number arguments</td>
<td align="right">1,100</td>
<td align="right">0.1%</td>
<td align="right">1,100</td>
<td align="right">0.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">not in dict</td>
<td align="right">320</td>
<td align="right">0.0%</td>
<td align="right">320</td>
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
<td align="right">5,585,012,106</td>
<td align="right">99.6%</td>
<td align="right">5,892,932,179</td>
<td align="right">99.6%</td>
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
<td align="right">458,581</td>
<td align="right">0.0%</td>
<td align="right">457,687</td>
<td align="right">0.0%</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">20,563,462</td>
<td align="right">0.4%</td>
<td align="right">20,562,305</td>
<td align="right">0.3%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">
deopt
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">13,123</td>
<td align="right">0.0%</td>
<td align="right">13,123</td>
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
<td align="right">668,431</td>
<td align="right">100.0%</td>
<td align="right">668,123</td>
<td align="right">100.0%</td>
<td align="right">-0.0%</td>
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
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">11,855</td>
<td align="right">0.0%</td>
<td align="right">11,848</td>
<td align="right">0.0%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">134,422,683</td>
<td align="right">100.0%</td>
<td align="right">134,389,807</td>
<td align="right">100.0%</td>
<td align="right">-0.0%</td>
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
<td align="right">11,718</td>
<td align="right">100.0%</td>
<td align="right">11,717</td>
<td align="right">100.0%</td>
<td align="right">-0.0%</td>
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
<td align="right">787,086,818</td>
<td align="right">81.9%</td>
<td align="right">787,084,818</td>
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
<td align="right">173,802,667</td>
<td align="right">18.1%</td>
<td align="right">173,802,608</td>
<td align="right">18.1%</td>
<td align="right">-0.0%</td>
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
<td align="left">Failure</td>
<td align="right">61,749</td>
<td align="right">89.6%</td>
<td align="right">61,752</td>
<td align="right">89.6%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">7,152</td>
<td align="right">10.4%</td>
<td align="right">7,152</td>
<td align="right">10.4%</td>
<td align="right">0.0%</td>
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
<td align="right">16,129</td>
<td align="right">26.1%</td>
<td align="right">16,132</td>
<td align="right">26.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">async generator send</td>
<td align="right">33,180</td>
<td align="right">53.7%</td>
<td align="right">33,180</td>
<td align="right">53.7%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">9,980</td>
<td align="right">16.2%</td>
<td align="right">9,980</td>
<td align="right">16.2%</td>
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
<td align="right">165,625,661</td>
<td align="right">6.0%</td>
<td align="right">160,646,573</td>
<td align="right">6.0%</td>
<td align="right">-3.0%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">2,523,552,869</td>
<td align="right">91.4%</td>
<td align="right">2,458,650,388</td>
<td align="right">91.4%</td>
<td align="right">-2.6%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">233,244,086</td>
<td align="right">8.5%</td>
<td align="right">228,277,247</td>
<td align="right">8.5%</td>
<td align="right">-2.1%</td>
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
<td align="right">3,274,011</td>
<td align="right">95.7%</td>
<td align="right">3,180,122</td>
<td align="right">95.6%</td>
<td align="right">-2.9%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">145,988</td>
<td align="right">4.3%</td>
<td align="right">145,921</td>
<td align="right">4.4%</td>
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
<td align="left">out of versions</td>
<td align="right">573</td>
<td align="right">0.4%</td>
<td align="right">594</td>
<td align="right">0.4%</td>
<td align="right">3.7%</td>
</tr>
<tr>
<td align="left">not in keys</td>
<td align="right">7,781</td>
<td align="right">5.3%</td>
<td align="right">7,761</td>
<td align="right">5.3%</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">class attr simple</td>
<td align="right">48,279</td>
<td align="right">33.1%</td>
<td align="right">48,219</td>
<td align="right">33.0%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">not managed dict</td>
<td align="right">28,518</td>
<td align="right">19.5%</td>
<td align="right">28,510</td>
<td align="right">19.5%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">not in dict</td>
<td align="right">15,645</td>
<td align="right">10.7%</td>
<td align="right">15,645</td>
<td align="right">10.7%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">non string or split</td>
<td align="right">15,440</td>
<td align="right">10.6%</td>
<td align="right">15,440</td>
<td align="right">10.6%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">overriding descriptor</td>
<td align="right">10,660</td>
<td align="right">7.3%</td>
<td align="right">10,660</td>
<td align="right">7.3%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">overridden</td>
<td align="right">6,932</td>
<td align="right">4.7%</td>
<td align="right">6,932</td>
<td align="right">4.8%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">property</td>
<td align="right">5,440</td>
<td align="right">3.7%</td>
<td align="right">5,440</td>
<td align="right">3.7%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">no dict</td>
<td align="right">5,180</td>
<td align="right">3.5%</td>
<td align="right">5,180</td>
<td align="right">3.5%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">method</td>
<td align="right">1,500</td>
<td align="right">1.0%</td>
<td align="right">1,500</td>
<td align="right">1.0%</td>
<td align="right">0.0%</td>
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
<td align="right">245,122,045</td>
<td align="right">77.9%</td>
<td align="right">242,033,498</td>
<td align="right">77.6%</td>
<td align="right">-1.3%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">69,597,071</td>
<td align="right">22.1%</td>
<td align="right">69,959,658</td>
<td align="right">22.4%</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">2,900</td>
<td align="right">0.0%</td>
<td align="right">2,900</td>
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
<td align="left">Failure</td>
<td align="right">66,345</td>
<td align="right">78.0%</td>
<td align="right">67,008</td>
<td align="right">78.2%</td>
<td align="right">1.0%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">18,717</td>
<td align="right">22.0%</td>
<td align="right">18,709</td>
<td align="right">21.8%</td>
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
<td align="left">dict subclass no override</td>
<td align="right">11,838</td>
<td align="right">17.8%</td>
<td align="right">12,528</td>
<td align="right">18.7%</td>
<td align="right">5.8%</td>
</tr>
<tr>
<td align="left">bytearray int</td>
<td align="right">1,340</td>
<td align="right">2.0%</td>
<td align="right">1,400</td>
<td align="right">2.1%</td>
<td align="right">4.5%</td>
</tr>
<tr>
<td align="left">array int</td>
<td align="right">6,560</td>
<td align="right">9.9%</td>
<td align="right">6,480</td>
<td align="right">9.7%</td>
<td align="right">-1.2%</td>
</tr>
<tr>
<td align="left">out of range</td>
<td align="right">2,028</td>
<td align="right">3.1%</td>
<td align="right">2,006</td>
<td align="right">3.0%</td>
<td align="right">-1.1%</td>
</tr>
<tr>
<td align="left">py simple</td>
<td align="right">42,499</td>
<td align="right">64.1%</td>
<td align="right">42,514</td>
<td align="right">63.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">2,080</td>
<td align="right">3.1%</td>
<td align="right">2,080</td>
<td align="right">3.1%</td>
<td align="right">0.0%</td>
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
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">3,381,823,980</td>
<td align="right">91.0%</td>
<td align="right">3,549,031,429</td>
<td align="right">91.5%</td>
<td align="right">4.9%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">331,544,475</td>
<td align="right">8.9%</td>
<td align="right">326,891,261</td>
<td align="right">8.4%</td>
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
<td align="right">102,057,886</td>
<td align="right">2.7%</td>
<td align="right">101,415,739</td>
<td align="right">2.6%</td>
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
<td align="right">2,210,153</td>
<td align="right">78.9%</td>
<td align="right">2,197,847</td>
<td align="right">78.9%</td>
<td align="right">-0.6%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">589,422</td>
<td align="right">21.1%</td>
<td align="right">588,038</td>
<td align="right">21.1%</td>
<td align="right">-0.2%</td>
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
<td align="right">173,065</td>
<td align="right">29.4%</td>
<td align="right">171,191</td>
<td align="right">29.1%</td>
<td align="right">-1.1%</td>
</tr>
<tr>
<td align="left">dict</td>
<td align="right">30,974</td>
<td align="right">5.3%</td>
<td align="right">30,651</td>
<td align="right">5.2%</td>
<td align="right">-1.0%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">40,256</td>
<td align="right">6.8%</td>
<td align="right">40,469</td>
<td align="right">6.9%</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">mapping</td>
<td align="right">57,846</td>
<td align="right">9.8%</td>
<td align="right">58,032</td>
<td align="right">9.9%</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">95,114</td>
<td align="right">16.1%</td>
<td align="right">95,418</td>
<td align="right">16.2%</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">sequence</td>
<td align="right">17,242</td>
<td align="right">2.9%</td>
<td align="right">17,197</td>
<td align="right">2.9%</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">number</td>
<td align="right">152,245</td>
<td align="right">25.8%</td>
<td align="right">152,413</td>
<td align="right">25.9%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">bytes</td>
<td align="right">18,699</td>
<td align="right">3.2%</td>
<td align="right">18,687</td>
<td align="right">3.2%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">float</td>
<td align="right">2,321</td>
<td align="right">0.4%</td>
<td align="right">2,320</td>
<td align="right">0.4%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">bytearray</td>
<td align="right">1,240</td>
<td align="right">0.2%</td>
<td align="right">1,240</td>
<td align="right">0.2%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">memory view</td>
<td align="right">420</td>
<td align="right">0.1%</td>
<td align="right">420</td>
<td align="right">0.1%</td>
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
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">1,060</td>
<td align="right">0.0%</td>
<td align="right">3,160</td>
<td align="right">0.0%</td>
<td align="right">198.1%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">460,671,522</td>
<td align="right">99.9%</td>
<td align="right">582,564,781</td>
<td align="right">99.9%</td>
<td align="right">26.5%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">487,240</td>
<td align="right">0.1%</td>
<td align="right">500,400</td>
<td align="right">0.1%</td>
<td align="right">2.7%</td>
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
<td align="right">3,559</td>
<td align="right">8.2%</td>
<td align="right">3,577</td>
<td align="right">8.2%</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">39,885</td>
<td align="right">91.8%</td>
<td align="right">39,857</td>
<td align="right">91.8%</td>
<td align="right">-0.1%</td>
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
<td align="left">sequence</td>
<td align="right">2,498</td>
<td align="right">70.2%</td>
<td align="right">2,516</td>
<td align="right">70.3%</td>
<td align="right">0.7%</td>
</tr>
<tr>
<td align="left">iterator</td>
<td align="right">681</td>
<td align="right">19.1%</td>
<td align="right">681</td>
<td align="right">19.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">380</td>
<td align="right">10.7%</td>
<td align="right">380</td>
<td align="right">10.6%</td>
<td align="right">0.0%</td>
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
<td align="right">1,033,830,254</td>
<td align="right">0.9%</td>
<td align="right">978,600,154</td>
<td align="right">0.8%</td>
<td align="right">-5.3%</td>
</tr>
<tr>
<td align="left">
Specialized hits
<details>
<summary>ⓘ</summary>

Specialized instructions, e.g. `LOAD_ATTR_MODULE` that complete.
</details>
</td>
<td align="right">40,520,798,804</td>
<td align="right">34.6%</td>
<td align="right">41,679,959,845</td>
<td align="right">35.0%</td>
<td align="right">2.9%</td>
</tr>
<tr>
<td align="left">
Basic
<details>
<summary>ⓘ</summary>

Instructions that are not and cannot be specialized, e.g. `LOAD_FAST`.
</details>
</td>
<td align="right">64,246,803,202</td>
<td align="right">54.9%</td>
<td align="right">65,194,961,846</td>
<td align="right">54.7%</td>
<td align="right">1.5%</td>
</tr>
<tr>
<td align="left">
Not specialized
<details>
<summary>ⓘ</summary>

Instructions that could be specialized but aren't, e.g. `LOAD_ATTR`, `BINARY_SLICE`.
</details>
</td>
<td align="right">11,198,890,961</td>
<td align="right">9.6%</td>
<td align="right">11,342,312,495</td>
<td align="right">9.5%</td>
<td align="right">1.3%</td>
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
<td align="left">BINARY_SUBSCR</td>
<td align="right">268,540,656</td>
<td align="right">5.7%</td>
<td align="right">329,294,716</td>
<td align="right">7.1%</td>
<td align="right">22.6%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">104,334,443</td>
<td align="right">2.2%</td>
<td align="right">86,033,546</td>
<td align="right">1.9%</td>
<td align="right">-17.5%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">598,961,048</td>
<td align="right">12.6%</td>
<td align="right">500,018,158</td>
<td align="right">10.8%</td>
<td align="right">-16.5%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">118,900,180</td>
<td align="right">2.5%</td>
<td align="right">104,901,985</td>
<td align="right">2.3%</td>
<td align="right">-11.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">1,251,113,517</td>
<td align="right">26.3%</td>
<td align="right">1,195,563,300</td>
<td align="right">25.9%</td>
<td align="right">-4.4%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">132,656,051</td>
<td align="right">2.8%</td>
<td align="right">138,038,672</td>
<td align="right">3.0%</td>
<td align="right">4.1%</td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">233,244,086</td>
<td align="right">4.9%</td>
<td align="right">228,277,247</td>
<td align="right">4.9%</td>
<td align="right">-2.1%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">331,544,475</td>
<td align="right">7.0%</td>
<td align="right">326,891,261</td>
<td align="right">7.1%</td>
<td align="right">-1.4%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">1,447,251,749</td>
<td align="right">30.5%</td>
<td align="right">1,446,715,956</td>
<td align="right">31.3%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">SEND</td>
<td align="right">173,802,667</td>
<td align="right">3.7%</td>
<td align="right">173,802,608</td>
<td align="right">3.8%</td>
<td align="right">-0.0%</td>
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
<td align="right">134,088,685</td>
<td align="right">13.0%</td>
<td align="right">102,113,076</td>
<td align="right">10.4%</td>
<td align="right">-23.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">141,062,277</td>
<td align="right">13.6%</td>
<td align="right">125,541,985</td>
<td align="right">12.8%</td>
<td align="right">-11.0%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">70,593,778</td>
<td align="right">6.8%</td>
<td align="right">65,633,541</td>
<td align="right">6.7%</td>
<td align="right">-7.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">91,563,377</td>
<td align="right">8.9%</td>
<td align="right">89,027,071</td>
<td align="right">9.1%</td>
<td align="right">-2.8%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">42,377,083</td>
<td align="right">4.1%</td>
<td align="right">42,155,711</td>
<td align="right">4.3%</td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">TO_BOOL_ALWAYS_TRUE</td>
<td align="right">46,277,952</td>
<td align="right">4.5%</td>
<td align="right">46,055,732</td>
<td align="right">4.7%</td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">TO_BOOL_NONE</td>
<td align="right">47,895,264</td>
<td align="right">4.6%</td>
<td align="right">47,676,453</td>
<td align="right">4.9%</td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">121,187,940</td>
<td align="right">11.7%</td>
<td align="right">121,070,405</td>
<td align="right">12.4%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right">59,398,480</td>
<td align="right">5.7%</td>
<td align="right">59,350,778</td>
<td align="right">6.1%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_SLOT</td>
<td align="right">94,979,035</td>
<td align="right">9.2%</td>
<td align="right">94,960,180</td>
<td align="right">9.7%</td>
<td align="right">-0.0%</td>
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
<td align="left">Calls via PyEval_EvalFrame (slot)</td>
<td align="right">479,367,831</td>
<td align="right">5.5%</td>
<td align="right">476,589,902</td>
<td align="right">5.5%</td>
<td align="right">-0.6%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (function vectorcall)</td>
<td align="right">1,450,623,703</td>
<td align="right">16.7%</td>
<td align="right">1,448,054,238</td>
<td align="right">16.6%</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (vector)</td>
<td align="right">1,453,312,773</td>
<td align="right">16.7%</td>
<td align="right">1,450,743,308</td>
<td align="right">16.7%</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">Calls to PyEval_EvalDefault</td>
<td align="right">2,315,819,709</td>
<td align="right">26.6%</td>
<td align="right">2,313,027,745</td>
<td align="right">26.6%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (total)</td>
<td align="right">2,315,819,709</td>
<td align="right">26.6%</td>
<td align="right">2,313,027,745</td>
<td align="right">26.6%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (api)</td>
<td align="right">260,349,622</td>
<td align="right">3.0%</td>
<td align="right">260,583,960</td>
<td align="right">3.0%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">Calls to Python functions inlined</td>
<td align="right">6,383,054,501</td>
<td align="right">73.4%</td>
<td align="right">6,385,321,489</td>
<td align="right">73.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (generator)</td>
<td align="right">862,506,936</td>
<td align="right">9.9%</td>
<td align="right">862,284,437</td>
<td align="right">9.9%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">Frame objects created</td>
<td align="right">89,136,144</td>
<td align="right">1.0%</td>
<td align="right">89,129,530</td>
<td align="right">1.0%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">Frames pushed</td>
<td align="right">6,953,899,388</td>
<td align="right">79.9%</td>
<td align="right">6,953,595,581</td>
<td align="right">79.9%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (function ex)</td>
<td align="right">38,363,942</td>
<td align="right">0.4%</td>
<td align="right">38,365,534</td>
<td align="right">0.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (method)</td>
<td align="right">213,147,689</td>
<td align="right">2.5%</td>
<td align="right">213,146,646</td>
<td align="right">2.5%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (legacy)</td>
<td align="right">2,658,324</td>
<td align="right">0.0%</td>
<td align="right">2,658,324</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (build class)</td>
<td align="right">30,746</td>
<td align="right">0.0%</td>
<td align="right">30,746</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
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
<td align="right">11,379,543</td>
<td align="right"></td>
<td align="right">10,427,242</td>
<td align="right"></td>
<td align="right">-8.4%</td>
</tr>
<tr>
<td align="left">Method cache collisions</td>
<td align="right">82,020,930</td>
<td align="right"></td>
<td align="right">76,950,714</td>
<td align="right"></td>
<td align="right">-6.2%</td>
</tr>
<tr>
<td align="left">Method cache misses</td>
<td align="right">78,422,401</td>
<td align="right"></td>
<td align="right">74,307,084</td>
<td align="right"></td>
<td align="right">-5.2%</td>
</tr>
<tr>
<td align="left">Increfs</td>
<td align="right">27,330,270,170</td>
<td align="right">22.6%</td>
<td align="right">26,958,241,399</td>
<td align="right">22.4%</td>
<td align="right">-1.4%</td>
</tr>
<tr>
<td align="left">Interpreter decrefs</td>
<td align="right">108,049,204,455</td>
<td align="right">78.1%</td>
<td align="right">107,775,489,290</td>
<td align="right">78.1%</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">Method cache hits</td>
<td align="right">3,117,173,549</td>
<td align="right"></td>
<td align="right">3,124,716,376</td>
<td align="right"></td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">Interpreter increfs</td>
<td align="right">93,499,253,840</td>
<td align="right">77.4%</td>
<td align="right">93,585,718,597</td>
<td align="right">77.6%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">Method cache dunder hits</td>
<td align="right">3,564,283,563</td>
<td align="right"></td>
<td align="right">3,562,262,775</td>
<td align="right"></td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">Decrefs</td>
<td align="right">30,220,971,580</td>
<td align="right">21.9%</td>
<td align="right">30,209,082,350</td>
<td align="right">21.9%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">Allocations to 4 kbytes</td>
<td align="right">104,922,463</td>
<td align="right">0.6%</td>
<td align="right">104,903,887</td>
<td align="right">0.6%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">Inline values</td>
<td align="right">182,584,015</td>
<td align="right"></td>
<td align="right">182,576,430</td>
<td align="right"></td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">Allocations</td>
<td align="right">11,705,152,217</td>
<td align="right">63.2%</td>
<td align="right">11,704,809,855</td>
<td align="right">63.2%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">Allocations to 512 bytes</td>
<td align="right">11,579,061,580</td>
<td align="right">62.6%</td>
<td align="right">11,578,738,037</td>
<td align="right">62.6%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">Frees</td>
<td align="right">12,050,037,883</td>
<td align="right"></td>
<td align="right">12,049,702,708</td>
<td align="right"></td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">Frees to freelist</td>
<td align="right">6,803,915,075</td>
<td align="right"></td>
<td align="right">6,804,070,098</td>
<td align="right"></td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Allocations from freelist</td>
<td align="right">6,801,941,198</td>
<td align="right">36.8%</td>
<td align="right">6,802,077,167</td>
<td align="right">36.8%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Allocations over 4 kbytes</td>
<td align="right">21,168,174</td>
<td align="right">0.1%</td>
<td align="right">21,167,931</td>
<td align="right">0.1%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">Materialize dict (on request)</td>
<td align="right">6,618,866</td>
<td align="right">3.6%</td>
<td align="right">6,618,866</td>
<td align="right">3.6%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Materialize dict (new key)</td>
<td align="right">116,335</td>
<td align="right">0.1%</td>
<td align="right">116,335</td>
<td align="right">0.1%</td>
<td align="right">0.0%</td>
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
<td align="right">115,716,237</td>
<td align="right">17,100,240,259</td>
<td align="right">0</td>
<td align="right">115,761,631</td>
<td align="right">17,050,539,955</td>
</tr>
<tr>
<td align="right">2</td>
<td align="right">0</td>
<td align="right">10,755,840</td>
<td align="right">6,969,903,930</td>
<td align="right">0</td>
<td align="right">10,755,840</td>
<td align="right">6,971,425,880</td>
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
Trace stack underflow
<details>
<summary>ⓘ</summary>

A potential trace is abandoned because it pops more frames than it pushes.
</details>
</td>
<td align="right">176,430</td>
<td align="right">24.7%</td>
<td align="right">322,321</td>
<td align="right">38.4%</td>
<td align="right">82.7%</td>
</tr>
<tr>
<td align="left">
Inner loop found
<details>
<summary>ⓘ</summary>

A trace is truncated because it has an inner loop
</details>
</td>
<td align="right">35,230</td>
<td align="right">4.9%</td>
<td align="right">53,091</td>
<td align="right">6.3%</td>
<td align="right">50.7%</td>
</tr>
<tr>
<td align="left">
Recursive call
<details>
<summary>ⓘ</summary>

A trace is truncated because it has a recursive call.
</details>
</td>
<td align="right">2,674</td>
<td align="right">0.4%</td>
<td align="right">1,951</td>
<td align="right">0.2%</td>
<td align="right">-27.0%</td>
</tr>
<tr>
<td align="left">
Trace too short
<details>
<summary>ⓘ</summary>

A potential trace is abandoced because it it too short.
</details>
</td>
<td align="right">560,865</td>
<td align="right">78.6%</td>
<td align="right">691,751</td>
<td align="right">82.3%</td>
<td align="right">23.3%</td>
</tr>
<tr>
<td align="left">
Optimization attempts
<details>
<summary>ⓘ</summary>

The number of times a potential trace is identified.  Specifically, this occurs in the JUMP BACKWARD instruction when the counter reaches a threshold.
</details>
</td>
<td align="right">713,970</td>
<td align="right"></td>
<td align="right">840,159</td>
<td align="right"></td>
<td align="right">17.7%</td>
</tr>
<tr>
<td align="left">
Trace stack overflow
<details>
<summary>ⓘ</summary>

A trace is truncated because it would require more than 5 stack frames.
</details>
</td>
<td align="right">1,362</td>
<td align="right">0.2%</td>
<td align="right">1,165</td>
<td align="right">0.1%</td>
<td align="right">-14.5%</td>
</tr>
<tr>
<td align="left">
Low confidence
<details>
<summary>ⓘ</summary>

A trace is abandoned because the likelihood of the jump to top being taken is too low.
</details>
</td>
<td align="right">8,829</td>
<td align="right">1.2%</td>
<td align="right">8,210</td>
<td align="right">1.0%</td>
<td align="right">-7.0%</td>
</tr>
<tr>
<td align="left">
Traces created
<details>
<summary>ⓘ</summary>

The number of traces that were successfully created.
</details>
</td>
<td align="right">153,105</td>
<td align="right">21.4%</td>
<td align="right">148,408</td>
<td align="right">17.7%</td>
<td align="right">-3.1%</td>
</tr>
<tr>
<td align="left">
Executors invalidated
<details>
<summary>ⓘ</summary>

The number of executors that were invalidated due to watched dictionary changes.
</details>
</td>
<td align="right">5,660</td>
<td align="right">3.7%</td>
<td align="right">5,520</td>
<td align="right">3.7%</td>
<td align="right">-2.5%</td>
</tr>
<tr>
<td align="left">
Uops executed
<details>
<summary>ⓘ</summary>

The total number of uops (micro-operations) that were executed
</details>
</td>
<td align="right">196,164,310,397</td>
<td align="right">2,618.8%</td>
<td align="right">192,480,127,857</td>
<td align="right">2,540.6%</td>
<td align="right">-1.9%</td>
</tr>
<tr>
<td align="left">
Traces executed
<details>
<summary>ⓘ</summary>

The number of traces that were executed
</details>
</td>
<td align="right">7,490,619,043</td>
<td align="right"></td>
<td align="right">7,576,076,858</td>
<td align="right"></td>
<td align="right">1.1%</td>
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
<td align="right">0</td>
<td align="right">0.0%</td>
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
Optimizer successes
<details>
<summary>ⓘ</summary>

The number of traces that were successfully optimized.
</details>
</td>
<td align="right">150,925</td>
<td align="right">98.6%</td>
<td align="right">144,800</td>
<td align="right">97.6%</td>
<td align="right">-4.1%</td>
</tr>
<tr>
<td align="left">
Optimizer attempts
<details>
<summary>ⓘ</summary>

The number of times the trace optimizer (_Py_uop_analyze_and_optimize) was run.
</details>
</td>
<td align="right">153,105</td>
<td align="right"></td>
<td align="right">148,408</td>
<td align="right"></td>
<td align="right">-3.1%</td>
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
<tr>
<td align="left">
Remove globals incorrect keys
<details>
<summary>ⓘ</summary>

The keys in the globals dictionary aren't what was expected
</details>
</td>
<td align="right">2,120</td>
<td align="right">1.4%</td>
<td align="right">2,120</td>
<td align="right">1.4%</td>
<td align="right">0.0%</td>
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
<td align="right">10,035</td>
<td align="right">6.6%</td>
<td align="right">12,311</td>
<td align="right">8.3%</td>
<td align="right">22.7%</td>
</tr>
<tr>
<td align="left"><= 16</td>
<td align="right">24,722</td>
<td align="right">16.1%</td>
<td align="right">24,282</td>
<td align="right">16.4%</td>
<td align="right">-1.8%</td>
</tr>
<tr>
<td align="left"><= 32</td>
<td align="right">57,193</td>
<td align="right">37.4%</td>
<td align="right">52,479</td>
<td align="right">35.4%</td>
<td align="right">-8.2%</td>
</tr>
<tr>
<td align="left"><= 64</td>
<td align="right">33,800</td>
<td align="right">22.1%</td>
<td align="right">33,167</td>
<td align="right">22.3%</td>
<td align="right">-1.9%</td>
</tr>
<tr>
<td align="left"><= 128</td>
<td align="right">19,398</td>
<td align="right">12.7%</td>
<td align="right">18,285</td>
<td align="right">12.3%</td>
<td align="right">-5.7%</td>
</tr>
<tr>
<td align="left"><= 256</td>
<td align="right">6,590</td>
<td align="right">4.3%</td>
<td align="right">6,774</td>
<td align="right">4.6%</td>
<td align="right">2.8%</td>
</tr>
<tr>
<td align="left"><= 512</td>
<td align="right">1,367</td>
<td align="right">0.9%</td>
<td align="right">1,110</td>
<td align="right">0.7%</td>
<td align="right">-18.8%</td>
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
<td align="right">2,606</td>
<td align="right">1.7%</td>
<td align="right">5,105</td>
<td align="right">3.4%</td>
<td align="right">95.9%</td>
</tr>
<tr>
<td align="left"><= 8</td>
<td align="right">16,925</td>
<td align="right">11.1%</td>
<td align="right">19,699</td>
<td align="right">13.3%</td>
<td align="right">16.4%</td>
</tr>
<tr>
<td align="left"><= 16</td>
<td align="right">46,264</td>
<td align="right">30.2%</td>
<td align="right">41,017</td>
<td align="right">27.6%</td>
<td align="right">-11.3%</td>
</tr>
<tr>
<td align="left"><= 32</td>
<td align="right">48,610</td>
<td align="right">31.7%</td>
<td align="right">43,695</td>
<td align="right">29.4%</td>
<td align="right">-10.1%</td>
</tr>
<tr>
<td align="left"><= 64</td>
<td align="right">23,789</td>
<td align="right">15.5%</td>
<td align="right">23,142</td>
<td align="right">15.6%</td>
<td align="right">-2.7%</td>
</tr>
<tr>
<td align="left"><= 128</td>
<td align="right">9,961</td>
<td align="right">6.5%</td>
<td align="right">9,568</td>
<td align="right">6.4%</td>
<td align="right">-3.9%</td>
</tr>
<tr>
<td align="left"><= 256</td>
<td align="right">2,630</td>
<td align="right">1.7%</td>
<td align="right">2,434</td>
<td align="right">1.6%</td>
<td align="right">-7.5%</td>
</tr>
<tr>
<td align="left"><= 512</td>
<td align="right">140</td>
<td align="right">0.1%</td>
<td align="right">140</td>
<td align="right">0.1%</td>
<td align="right">0.0%</td>
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
<td align="right">25,847,900</td>
<td align="right">0.3%</td>
<td align="right">26,058,980</td>
<td align="right">0.3%</td>
<td align="right">0.8%</td>
</tr>
<tr>
<td align="left"><= 4</td>
<td align="right">1,003,440,469</td>
<td align="right">13.4%</td>
<td align="right">574,384,881</td>
<td align="right">7.6%</td>
<td align="right">-42.8%</td>
</tr>
<tr>
<td align="left"><= 8</td>
<td align="right">838,720,241</td>
<td align="right">11.2%</td>
<td align="right">881,036,706</td>
<td align="right">11.6%</td>
<td align="right">5.0%</td>
</tr>
<tr>
<td align="left"><= 16</td>
<td align="right">1,407,999,283</td>
<td align="right">18.8%</td>
<td align="right">1,409,577,432</td>
<td align="right">18.6%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left"><= 32</td>
<td align="right">1,109,220,641</td>
<td align="right">14.8%</td>
<td align="right">1,228,990,291</td>
<td align="right">16.2%</td>
<td align="right">10.8%</td>
</tr>
<tr>
<td align="left"><= 64</td>
<td align="right">625,090,399</td>
<td align="right">8.3%</td>
<td align="right">678,837,458</td>
<td align="right">9.0%</td>
<td align="right">8.6%</td>
</tr>
<tr>
<td align="left"><= 128</td>
<td align="right">319,576,877</td>
<td align="right">4.3%</td>
<td align="right">285,453,398</td>
<td align="right">3.8%</td>
<td align="right">-10.7%</td>
</tr>
<tr>
<td align="left"><= 256</td>
<td align="right">188,442,453</td>
<td align="right">2.5%</td>
<td align="right">166,398,596</td>
<td align="right">2.2%</td>
<td align="right">-11.7%</td>
</tr>
<tr>
<td align="left"><= 512</td>
<td align="right">23,552,775</td>
<td align="right">0.3%</td>
<td align="right">20,337,407</td>
<td align="right">0.3%</td>
<td align="right">-13.7%</td>
</tr>
<tr>
<td align="left"><= 1,024</td>
<td align="right">7,720,214</td>
<td align="right">0.1%</td>
<td align="right">7,692,265</td>
<td align="right">0.1%</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left"><= 2,048</td>
<td align="right">17,763,052</td>
<td align="right">0.2%</td>
<td align="right">17,762,089</td>
<td align="right">0.2%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left"><= 4,096</td>
<td align="right">611,448</td>
<td align="right">0.0%</td>
<td align="right">611,411</td>
<td align="right">0.0%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left"><= 8,192</td>
<td align="right">747,337</td>
<td align="right">0.0%</td>
<td align="right">747,421</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left"><= 16,384</td>
<td align="right">237,561</td>
<td align="right">0.0%</td>
<td align="right">237,561</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left"><= 32,768</td>
<td align="right">43,860</td>
<td align="right">0.0%</td>
<td align="right">43,860</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left"><= 65,536</td>
<td align="right">13,246</td>
<td align="right">0.0%</td>
<td align="right">13,266</td>
<td align="right">0.0%</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left"><= 131,072</td>
<td align="right">754</td>
<td align="right">0.0%</td>
<td align="right">734</td>
<td align="right">0.0%</td>
<td align="right">-2.7%</td>
</tr>
<tr>
<td align="left"><= 262,144</td>
<td align="right">2,080</td>
<td align="right">0.0%</td>
<td align="right">2,081</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left"><= 524,288</td>
<td align="right">462</td>
<td align="right">0.0%</td>
<td align="right">464</td>
<td align="right">0.0%</td>
<td align="right">0.4%</td>
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
<td align="right">302</td>
<td align="right">0.0%</td>
<td align="right">305</td>
<td align="right">0.0%</td>
<td align="right">1.0%</td>
</tr>
<tr>
<td align="left"><= 4,194,304</td>
<td align="right">178</td>
<td align="right">0.0%</td>
<td align="right">175</td>
<td align="right">0.0%</td>
<td align="right">-1.7%</td>
</tr>
<tr>
<td align="left"><= 8,388,608</td>
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
<td align="left">_DELETE_SUBSCR</td>
<td align="right">1,629,645</td>
<td align="right">98,172,948</td>
<td align="right">5,924.2%</td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_O</td>
<td align="right">26,486,020</td>
<td align="right">129,202,764</td>
<td align="right">387.8%</td>
</tr>
<tr>
<td align="left">_ERROR_POP_N</td>
<td align="right">698,627</td>
<td align="right">1,879,206</td>
<td align="right">169.0%</td>
</tr>
<tr>
<td align="left">_POP_TOP_LOAD_CONST_INLINE_BORROW</td>
<td align="right">1,404,746</td>
<td align="right">2,882,377</td>
<td align="right">105.2%</td>
</tr>
<tr>
<td align="left">_BUILD_STRING</td>
<td align="right">25,515,722</td>
<td align="right">1,853,708</td>
<td align="right">-92.7%</td>
</tr>
<tr>
<td align="left">_CONVERT_VALUE</td>
<td align="right">51,694,900</td>
<td align="right">3,917,200</td>
<td align="right">-92.4%</td>
</tr>
<tr>
<td align="left">_FORMAT_SIMPLE</td>
<td align="right">52,355,821</td>
<td align="right">4,683,386</td>
<td align="right">-91.1%</td>
</tr>
<tr>
<td align="left">_BUILD_CONST_KEY_MAP</td>
<td align="right">2,731,034</td>
<td align="right">4,837,300</td>
<td align="right">77.1%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_CHECK</td>
<td align="right">271,482</td>
<td align="right">472,431</td>
<td align="right">74.0%</td>
</tr>
<tr>
<td align="left">_FOR_ITER_TIER_TWO</td>
<td align="right">1,713,687,571</td>
<td align="right">632,044,649</td>
<td align="right">-63.1%</td>
</tr>
<tr>
<td align="left">_STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">107,883,929</td>
<td align="right">170,865,562</td>
<td align="right">58.4%</td>
</tr>
<tr>
<td align="left">_GUARD_DORV_NO_DICT</td>
<td align="right">109,233,149</td>
<td align="right">172,212,942</td>
<td align="right">57.7%</td>
</tr>
<tr>
<td align="left">_MAP_ADD</td>
<td align="right">21,327,744</td>
<td align="right">33,167,997</td>
<td align="right">55.5%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_NONE_POP</td>
<td align="right">46,920,922</td>
<td align="right">72,596,258</td>
<td align="right">54.7%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_AND_CLEAR</td>
<td align="right">17,241,896</td>
<td align="right">25,069,055</td>
<td align="right">45.4%</td>
</tr>
<tr>
<td align="left">_ITER_CHECK_TUPLE</td>
<td align="right">362,972,028</td>
<td align="right">518,337,094</td>
<td align="right">42.8%</td>
</tr>
<tr>
<td align="left">_DEOPT</td>
<td align="right">1,206,498,273</td>
<td align="right">701,253,172</td>
<td align="right">-41.9%</td>
</tr>
<tr>
<td align="left">_GUARD_NOT_EXHAUSTED_TUPLE</td>
<td align="right">310,723,263</td>
<td align="right">438,578,389</td>
<td align="right">41.1%</td>
</tr>
<tr>
<td align="left">_POP_TOP</td>
<td align="right">921,552,048</td>
<td align="right">1,270,454,632</td>
<td align="right">37.9%</td>
</tr>
<tr>
<td align="left">_SET_ADD</td>
<td align="right">2,174,708</td>
<td align="right">1,449,209</td>
<td align="right">-33.4%</td>
</tr>
<tr>
<td align="left">_ITER_NEXT_TUPLE</td>
<td align="right">204,701,448</td>
<td align="right">265,662,113</td>
<td align="right">29.8%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_STR</td>
<td align="right">28,328,345</td>
<td align="right">35,303,442</td>
<td align="right">24.6%</td>
</tr>
<tr>
<td align="left">_BUILD_TUPLE</td>
<td align="right">458,412,474</td>
<td align="right">561,260,970</td>
<td align="right">22.4%</td>
</tr>
<tr>
<td align="left">_DICT_MERGE</td>
<td align="right">11,664,360</td>
<td align="right">9,131,214</td>
<td align="right">-21.7%</td>
</tr>
<tr>
<td align="left">_COLD_EXIT</td>
<td align="right">1,736,168,475</td>
<td align="right">2,092,506,030</td>
<td align="right">20.5%</td>
</tr>
<tr>
<td align="left">_LOAD_GLOBAL</td>
<td align="right">184,430,413</td>
<td align="right">217,097,427</td>
<td align="right">17.7%</td>
</tr>
<tr>
<td align="left">_MAKE_CELL</td>
<td align="right">6,868,580</td>
<td align="right">5,676,439</td>
<td align="right">-17.4%</td>
</tr>
<tr>
<td align="left">_UNPACK_SEQUENCE_TUPLE</td>
<td align="right">292,682,630</td>
<td align="right">244,620,451</td>
<td align="right">-16.4%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_4</td>
<td align="right">624,859,666</td>
<td align="right">528,743,113</td>
<td align="right">-15.4%</td>
</tr>
<tr>
<td align="left">_CALL_TYPE_1</td>
<td align="right">332,534,251</td>
<td align="right">281,947,203</td>
<td align="right">-15.2%</td>
</tr>
<tr>
<td align="left">_STORE_DEREF</td>
<td align="right">3,878,811</td>
<td align="right">3,293,412</td>
<td align="right">-15.1%</td>
</tr>
<tr>
<td align="left">_BUILD_MAP</td>
<td align="right">17,382,991</td>
<td align="right">20,005,731</td>
<td align="right">15.1%</td>
</tr>
<tr>
<td align="left">_CONTAINS_OP</td>
<td align="right">121,537,621</td>
<td align="right">139,732,265</td>
<td align="right">15.0%</td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_CLASS</td>
<td align="right">61,371,139</td>
<td align="right">70,547,269</td>
<td align="right">15.0%</td>
</tr>
<tr>
<td align="left">_CHECK_VALIDITY_AND_SET_IP</td>
<td align="right">1,204,216,927</td>
<td align="right">1,364,355,486</td>
<td align="right">13.3%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">890,347,174</td>
<td align="right">997,010,577</td>
<td align="right">12.0%</td>
</tr>
<tr>
<td align="left">_LOAD_CONST_INLINE_BORROW_WITH_NULL</td>
<td align="right">505,532,430</td>
<td align="right">447,200,310</td>
<td align="right">-11.5%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_2</td>
<td align="right">111,429,389</td>
<td align="right">124,222,516</td>
<td align="right">11.5%</td>
</tr>
<tr>
<td align="left">_LOAD_DEREF</td>
<td align="right">660,691,799</td>
<td align="right">585,994,387</td>
<td align="right">-11.3%</td>
</tr>
<tr>
<td align="left">_BINARY_OP</td>
<td align="right">897,013,453</td>
<td align="right">995,790,954</td>
<td align="right">11.0%</td>
</tr>
<tr>
<td align="left">_LOAD_SUPER_ATTR_METHOD</td>
<td align="right">179,122</td>
<td align="right">198,576</td>
<td align="right">10.9%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_3</td>
<td align="right">789,513,251</td>
<td align="right">704,731,814</td>
<td align="right">-10.7%</td>
</tr>
<tr>
<td align="left">_UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">709,813,400</td>
<td align="right">635,650,370</td>
<td align="right">-10.4%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_5</td>
<td align="right">794,904,184</td>
<td align="right">713,558,220</td>
<td align="right">-10.2%</td>
</tr>
<tr>
<td align="left">_CALL_ISINSTANCE</td>
<td align="right">393,886,655</td>
<td align="right">353,897,522</td>
<td align="right">-10.2%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_LIST</td>
<td align="right">56,354,706</td>
<td align="right">61,895,013</td>
<td align="right">9.8%</td>
</tr>
<tr>
<td align="left">_GET_ITER</td>
<td align="right">353,635,432</td>
<td align="right">388,173,609</td>
<td align="right">9.8%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_4</td>
<td align="right">2,326,812,622</td>
<td align="right">2,099,936,523</td>
<td align="right">-9.8%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_SLOT_1</td>
<td align="right">2,633,440</td>
<td align="right">2,889,040</td>
<td align="right">9.7%</td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_FAST</td>
<td align="right">1,026,661,654</td>
<td align="right">928,169,796</td>
<td align="right">-9.6%</td>
</tr>
<tr>
<td align="left">_GUARD_NOT_EXHAUSTED_RANGE</td>
<td align="right">690,660,237</td>
<td align="right">756,069,034</td>
<td align="right">9.5%</td>
</tr>
<tr>
<td align="left">_ITER_CHECK_RANGE</td>
<td align="right">691,197,557</td>
<td align="right">756,606,354</td>
<td align="right">9.5%</td>
</tr>
<tr>
<td align="left">_ITER_NEXT_RANGE</td>
<td align="right">648,020,137</td>
<td align="right">708,493,900</td>
<td align="right">9.3%</td>
</tr>
<tr>
<td align="left">_LOAD_GLOBAL_MODULE</td>
<td align="right">58,250,421</td>
<td align="right">53,035,930</td>
<td align="right">-9.0%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_BOOL</td>
<td align="right">2,250,936,020</td>
<td align="right">2,052,456,367</td>
<td align="right">-8.8%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">1,183,580,122</td>
<td align="right">1,084,422,360</td>
<td align="right">-8.4%</td>
</tr>
<tr>
<td align="left">_POP_FRAME</td>
<td align="right">817,640,944</td>
<td align="right">750,783,287</td>
<td align="right">-8.2%</td>
</tr>
<tr>
<td align="left">_SET_IP</td>
<td align="right">15,025,157,536</td>
<td align="right">13,797,410,122</td>
<td align="right">-8.2%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_4</td>
<td align="right">773,167,508</td>
<td align="right">710,853,928</td>
<td align="right">-8.1%</td>
</tr>
<tr>
<td align="left">_CONTAINS_OP_DICT</td>
<td align="right">430,474,904</td>
<td align="right">395,802,463</td>
<td align="right">-8.1%</td>
</tr>
<tr>
<td align="left">_ITER_NEXT_LIST</td>
<td align="right">1,138,037,399</td>
<td align="right">1,229,195,767</td>
<td align="right">8.0%</td>
</tr>
<tr>
<td align="left">_LOAD_CONST_INLINE_WITH_NULL</td>
<td align="right">2,044,738,105</td>
<td align="right">1,881,684,186</td>
<td align="right">-8.0%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_5</td>
<td align="right">2,442,996,138</td>
<td align="right">2,251,466,057</td>
<td align="right">-7.8%</td>
</tr>
<tr>
<td align="left">_BINARY_SUBSCR_DICT</td>
<td align="right">425,159,720</td>
<td align="right">391,850,536</td>
<td align="right">-7.8%</td>
</tr>
<tr>
<td align="left">_CALL_TUPLE_1</td>
<td align="right">7,492,460</td>
<td align="right">8,077,187</td>
<td align="right">7.8%</td>
</tr>
<tr>
<td align="left">_GUARD_KEYS_VERSION</td>
<td align="right">1,282,500,845</td>
<td align="right">1,182,806,837</td>
<td align="right">-7.8%</td>
</tr>
<tr>
<td align="left">_GUARD_DORV_VALUES_INST_ATTR_FROM_DICT</td>
<td align="right">1,332,120,184</td>
<td align="right">1,229,258,462</td>
<td align="right">-7.7%</td>
</tr>
<tr>
<td align="left">_GUARD_NOT_EXHAUSTED_LIST</td>
<td align="right">1,409,307,992</td>
<td align="right">1,516,854,237</td>
<td align="right">7.6%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_NOT_NONE_POP</td>
<td align="right">169,509,762</td>
<td align="right">182,169,863</td>
<td align="right">7.5%</td>
</tr>
<tr>
<td align="left">_EXIT_TRACE</td>
<td align="right">2,751,406,663</td>
<td align="right">2,933,593,334</td>
<td align="right">6.6%</td>
</tr>
<tr>
<td align="left">_STORE_FAST</td>
<td align="right">3,392,399,502</td>
<td align="right">3,168,258,014</td>
<td align="right">-6.6%</td>
</tr>
<tr>
<td align="left">_CHECK_ATTR_METHOD_LAZY_DICT</td>
<td align="right">105,936,148</td>
<td align="right">99,492,825</td>
<td align="right">-6.1%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_METHOD_LAZY_DICT</td>
<td align="right">105,936,148</td>
<td align="right">99,492,825</td>
<td align="right">-6.1%</td>
</tr>
<tr>
<td align="left">_ITER_CHECK_LIST</td>
<td align="right">1,487,490,174</td>
<td align="right">1,574,078,946</td>
<td align="right">5.8%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_2</td>
<td align="right">894,075,757</td>
<td align="right">842,573,153</td>
<td align="right">-5.8%</td>
</tr>
<tr>
<td align="left">_SWAP</td>
<td align="right">1,157,627,317</td>
<td align="right">1,222,467,405</td>
<td align="right">5.6%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_INSTANCE_VALUE_1</td>
<td align="right">4,491,579</td>
<td align="right">4,742,001</td>
<td align="right">5.6%</td>
</tr>
<tr>
<td align="left">_TO_BOOL</td>
<td align="right">250,017,700</td>
<td align="right">263,642,044</td>
<td align="right">5.4%</td>
</tr>
<tr>
<td align="left">_SIDE_EXIT</td>
<td align="right">4,361,835,272</td>
<td align="right">4,595,055,043</td>
<td align="right">5.3%</td>
</tr>
<tr>
<td align="left">_CHECK_VALIDITY</td>
<td align="right">12,292,439,087</td>
<td align="right">11,646,235,379</td>
<td align="right">-5.3%</td>
</tr>
<tr>
<td align="left">_STORE_ATTR_SLOT</td>
<td align="right">123,910,785</td>
<td align="right">130,303,683</td>
<td align="right">5.2%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_ADD_UNICODE</td>
<td align="right">25,542,734</td>
<td align="right">26,846,119</td>
<td align="right">5.1%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR</td>
<td align="right">1,272,208,592</td>
<td align="right">1,336,815,432</td>
<td align="right">5.1%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_6</td>
<td align="right">1,277,810,831</td>
<td align="right">1,340,996,325</td>
<td align="right">4.9%</td>
</tr>
<tr>
<td align="left">_BINARY_SUBSCR</td>
<td align="right">1,302,322,297</td>
<td align="right">1,238,517,555</td>
<td align="right">-4.9%</td>
</tr>
<tr>
<td align="left">_COMPARE_OP</td>
<td align="right">112,689,910</td>
<td align="right">107,198,152</td>
<td align="right">-4.9%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_1</td>
<td align="right">2,017,329,070</td>
<td align="right">1,920,662,015</td>
<td align="right">-4.8%</td>
</tr>
<tr>
<td align="left">_UNARY_NOT</td>
<td align="right">62,242,739</td>
<td align="right">65,220,510</td>
<td align="right">4.8%</td>
</tr>
<tr>
<td align="left">_CALL_LEN</td>
<td align="right">215,922,722</td>
<td align="right">226,133,110</td>
<td align="right">4.7%</td>
</tr>
<tr>
<td align="left">_START_EXECUTOR</td>
<td align="right">5,754,450,568</td>
<td align="right">5,483,570,828</td>
<td align="right">-4.7%</td>
</tr>
<tr>
<td align="left">_LOAD_CONST_INLINE</td>
<td align="right">1,526,887,718</td>
<td align="right">1,597,845,531</td>
<td align="right">4.6%</td>
</tr>
<tr>
<td align="left">_BINARY_SUBSCR_TUPLE_INT</td>
<td align="right">163,912,061</td>
<td align="right">156,630,235</td>
<td align="right">-4.4%</td>
</tr>
<tr>
<td align="left">_GUARD_TOS_INT</td>
<td align="right">226,768,945</td>
<td align="right">216,774,768</td>
<td align="right">-4.4%</td>
</tr>
<tr>
<td align="left">_GUARD_BOTH_FLOAT</td>
<td align="right">916,378,215</td>
<td align="right">876,074,529</td>
<td align="right">-4.4%</td>
</tr>
<tr>
<td align="left">_JUMP_TO_TOP</td>
<td align="right">2,258,475,873</td>
<td align="right">2,160,460,416</td>
<td align="right">-4.3%</td>
</tr>
<tr>
<td align="left">_RESUME_CHECK</td>
<td align="right">1,570,653,117</td>
<td align="right">1,505,003,231</td>
<td align="right">-4.2%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_3</td>
<td align="right">3,578,537,936</td>
<td align="right">3,431,635,309</td>
<td align="right">-4.1%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_TRUE_POP</td>
<td align="right">2,726,629,696</td>
<td align="right">2,616,299,650</td>
<td align="right">-4.0%</td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION</td>
<td align="right">1,336,627,464</td>
<td align="right">1,389,729,504</td>
<td align="right">4.0%</td>
</tr>
<tr>
<td align="left">_GUARD_GLOBALS_VERSION</td>
<td align="right">111,287,105</td>
<td align="right">106,926,374</td>
<td align="right">-3.9%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_MULTIPLY_FLOAT</td>
<td align="right">1,156,319,872</td>
<td align="right">1,112,485,765</td>
<td align="right">-3.8%</td>
</tr>
<tr>
<td align="left">_SAVE_RETURN_OFFSET</td>
<td align="right">1,861,181,452</td>
<td align="right">1,791,494,238</td>
<td align="right">-3.7%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_NONDESCRIPTOR_NO_DICT</td>
<td align="right">26,842,850</td>
<td align="right">25,866,432</td>
<td align="right">-3.6%</td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION_EXACT_ARGS</td>
<td align="right">1,938,188,366</td>
<td align="right">1,867,994,094</td>
<td align="right">-3.6%</td>
</tr>
<tr>
<td align="left">_PUSH_FRAME</td>
<td align="right">1,968,110,195</td>
<td align="right">1,898,422,810</td>
<td align="right">-3.5%</td>
</tr>
<tr>
<td align="left">_STORE_SLICE</td>
<td align="right">149,868,340</td>
<td align="right">154,965,460</td>
<td align="right">3.4%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_INT</td>
<td align="right">211,819,967</td>
<td align="right">218,926,392</td>
<td align="right">3.4%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_7</td>
<td align="right">3,403,026,482</td>
<td align="right">3,515,932,445</td>
<td align="right">3.3%</td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">257,435,425</td>
<td align="right">265,842,026</td>
<td align="right">3.3%</td>
</tr>
<tr>
<td align="left">_LIST_APPEND</td>
<td align="right">203,935,784</td>
<td align="right">197,362,232</td>
<td align="right">-3.2%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_6</td>
<td align="right">551,771,484</td>
<td align="right">534,735,360</td>
<td align="right">-3.1%</td>
</tr>
<tr>
<td align="left">_CHECK_MANAGED_OBJECT_HAS_VALUES</td>
<td align="right">2,076,722,387</td>
<td align="right">2,139,565,267</td>
<td align="right">3.0%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_INSTANCE_VALUE_0</td>
<td align="right">2,071,746,168</td>
<td align="right">2,134,428,246</td>
<td align="right">3.0%</td>
</tr>
<tr>
<td align="left">_GUARD_BOTH_INT</td>
<td align="right">632,018,071</td>
<td align="right">613,076,930</td>
<td align="right">-3.0%</td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">202,360,745</td>
<td align="right">208,260,087</td>
<td align="right">2.9%</td>
</tr>
<tr>
<td align="left">_STORE_SUBSCR_DICT</td>
<td align="right">145,710,159</td>
<td align="right">149,843,383</td>
<td align="right">2.8%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_FALSE_POP</td>
<td align="right">5,682,504,863</td>
<td align="right">5,527,731,407</td>
<td align="right">-2.7%</td>
</tr>
<tr>
<td align="left">_CHECK_STACK_SPACE</td>
<td align="right">204,851,110</td>
<td align="right">199,692,966</td>
<td align="right">-2.5%</td>
</tr>
<tr>
<td align="left">_CHECK_ATTR_WITH_HINT</td>
<td align="right">235,751,587</td>
<td align="right">230,607,749</td>
<td align="right">-2.2%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_WITH_HINT</td>
<td align="right">235,571,326</td>
<td align="right">230,440,828</td>
<td align="right">-2.2%</td>
</tr>
<tr>
<td align="left">_PUSH_NULL</td>
<td align="right">859,534,481</td>
<td align="right">841,702,155</td>
<td align="right">-2.1%</td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_FAST_WITH_KEYWORDS</td>
<td align="right">159,855,766</td>
<td align="right">156,813,210</td>
<td align="right">-1.9%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS</td>
<td align="right">10,099,167</td>
<td align="right">9,917,903</td>
<td align="right">-1.8%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_1</td>
<td align="right">628,264,423</td>
<td align="right">639,167,037</td>
<td align="right">1.7%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_0</td>
<td align="right">209,073,552</td>
<td align="right">205,466,825</td>
<td align="right">-1.7%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_3</td>
<td align="right">61,665,724</td>
<td align="right">62,718,478</td>
<td align="right">1.7%</td>
</tr>
<tr>
<td align="left">_TIER2_RESUME_CHECK</td>
<td align="right">249,219,717</td>
<td align="right">253,404,181</td>
<td align="right">1.7%</td>
</tr>
<tr>
<td align="left">_LOAD_GLOBAL_BUILTINS</td>
<td align="right">53,036,684</td>
<td align="right">53,890,444</td>
<td align="right">1.6%</td>
</tr>
<tr>
<td align="left">_CONTAINS_OP_SET</td>
<td align="right">1,598,619,907</td>
<td align="right">1,573,176,643</td>
<td align="right">-1.6%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST</td>
<td align="right">6,035,374,704</td>
<td align="right">6,123,700,208</td>
<td align="right">1.5%</td>
</tr>
<tr>
<td align="left">_GUARD_TYPE_VERSION</td>
<td align="right">6,250,116,075</td>
<td align="right">6,339,744,595</td>
<td align="right">1.4%</td>
</tr>
<tr>
<td align="left">_CALL_INTRINSIC_1</td>
<td align="right">98,948,319</td>
<td align="right">97,594,619</td>
<td align="right">-1.4%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_CLASS_0</td>
<td align="right">24,915,216</td>
<td align="right">25,255,397</td>
<td align="right">1.4%</td>
</tr>
<tr>
<td align="left">_LIST_EXTEND</td>
<td align="right">99,872,119</td>
<td align="right">98,553,259</td>
<td align="right">-1.3%</td>
</tr>
<tr>
<td align="left">_COMPARE_OP_INT</td>
<td align="right">1,017,012,974</td>
<td align="right">1,029,652,880</td>
<td align="right">1.2%</td>
</tr>
<tr>
<td align="left">_CHECK_ATTR_CLASS</td>
<td align="right">47,539,242</td>
<td align="right">48,106,738</td>
<td align="right">1.2%</td>
</tr>
<tr>
<td align="left">_IS_OP</td>
<td align="right">363,109,893</td>
<td align="right">358,812,779</td>
<td align="right">-1.2%</td>
</tr>
<tr>
<td align="left">_STORE_GLOBAL</td>
<td align="right">1,275,340</td>
<td align="right">1,260,560</td>
<td align="right">-1.2%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_1</td>
<td align="right">6,835,782,429</td>
<td align="right">6,760,334,900</td>
<td align="right">-1.1%</td>
</tr>
<tr>
<td align="left">_LOAD_CONST_INLINE_BORROW</td>
<td align="right">9,580,449,638</td>
<td align="right">9,484,103,002</td>
<td align="right">-1.0%</td>
</tr>
<tr>
<td align="left">_GUARD_TOS_FLOAT</td>
<td align="right">65,543,560</td>
<td align="right">64,886,420</td>
<td align="right">-1.0%</td>
</tr>
<tr>
<td align="left">_GUARD_NOS_INT</td>
<td align="right">2,428,806,967</td>
<td align="right">2,450,126,764</td>
<td align="right">0.9%</td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_O</td>
<td align="right">748,424,032</td>
<td align="right">742,031,246</td>
<td align="right">-0.9%</td>
</tr>
<tr>
<td align="left">_REPLACE_WITH_TRUE</td>
<td align="right">33,298,851</td>
<td align="right">33,566,810</td>
<td align="right">0.8%</td>
</tr>
<tr>
<td align="left">_STORE_ATTR</td>
<td align="right">58,799,445</td>
<td align="right">59,269,457</td>
<td align="right">0.8%</td>
</tr>
<tr>
<td align="left">_CHECK_CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">80,146,413</td>
<td align="right">80,777,072</td>
<td align="right">0.8%</td>
</tr>
<tr>
<td align="left">_CHECK_ATTR_MODULE</td>
<td align="right">7,601,010</td>
<td align="right">7,542,108</td>
<td align="right">-0.8%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_MODULE</td>
<td align="right">7,601,010</td>
<td align="right">7,542,108</td>
<td align="right">-0.8%</td>
</tr>
<tr>
<td align="left">_CHECK_PERIODIC</td>
<td align="right">2,616,871,567</td>
<td align="right">2,637,017,069</td>
<td align="right">0.8%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right">92,256,199</td>
<td align="right">92,957,829</td>
<td align="right">0.8%</td>
</tr>
<tr>
<td align="left">_UNPACK_SEQUENCE</td>
<td align="right">1,566,268</td>
<td align="right">1,554,914</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">_BUILD_LIST</td>
<td align="right">260,972,178</td>
<td align="right">262,762,984</td>
<td align="right">0.7%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_7</td>
<td align="right">1,223,210,687</td>
<td align="right">1,214,962,327</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">_BINARY_SLICE</td>
<td align="right">122,812,761</td>
<td align="right">122,040,546</td>
<td align="right">-0.6%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBTRACT_INT</td>
<td align="right">464,143,424</td>
<td align="right">461,493,475</td>
<td align="right">-0.6%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">80,079,413</td>
<td align="right">80,532,952</td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">_CHECK_STACK_SPACE_OPERAND</td>
<td align="right">967,371,605</td>
<td align="right">972,033,169</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_0</td>
<td align="right">6,023,113,325</td>
<td align="right">6,051,023,057</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_0</td>
<td align="right">424,863,083</td>
<td align="right">426,725,191</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">_UNARY_NEGATIVE</td>
<td align="right">25,164,774</td>
<td align="right">25,062,818</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">_GUARD_BOTH_UNICODE</td>
<td align="right">978,992,454</td>
<td align="right">975,232,194</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_SLOT_0</td>
<td align="right">745,175,886</td>
<td align="right">747,927,634</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_ADD_FLOAT</td>
<td align="right">554,586,180</td>
<td align="right">556,453,880</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_NONE</td>
<td align="right">180,543,155</td>
<td align="right">181,141,367</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">_BINARY_SUBSCR_LIST_INT</td>
<td align="right">1,103,675,998</td>
<td align="right">1,107,225,336</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">_COPY</td>
<td align="right">1,333,131,499</td>
<td align="right">1,328,861,898</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_2</td>
<td align="right">3,182,707,165</td>
<td align="right">3,172,621,804</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">_RETURN_GENERATOR</td>
<td align="right">91,061,914</td>
<td align="right">91,340,939</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">_COMPARE_OP_STR</td>
<td align="right">1,837,494,440</td>
<td align="right">1,832,167,913</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">_COPY_FREE_VARS</td>
<td align="right">81,379,946</td>
<td align="right">81,177,795</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">_STORE_SUBSCR_LIST_INT</td>
<td align="right">490,870,022</td>
<td align="right">489,812,942</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_MULTIPLY_INT</td>
<td align="right">185,794,604</td>
<td align="right">186,148,084</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">_CALL_STR_1</td>
<td align="right">67,905,056</td>
<td align="right">67,798,674</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">_UNARY_INVERT</td>
<td align="right">12,990,812</td>
<td align="right">12,971,658</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">_SET_FUNCTION_ATTRIBUTE</td>
<td align="right">78,474,688</td>
<td align="right">78,588,666</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">_MAKE_FUNCTION</td>
<td align="right">93,509,902</td>
<td align="right">93,610,627</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">_STORE_SUBSCR</td>
<td align="right">381,433,900</td>
<td align="right">381,071,318</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">_GUARD_BUILTINS_VERSION</td>
<td align="right">45,866,884</td>
<td align="right">45,823,824</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_CLASS_1</td>
<td align="right">20,485,700</td>
<td align="right">20,502,900</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_ADD_INT</td>
<td align="right">2,521,904,335</td>
<td align="right">2,519,803,460</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">_UNPACK_SEQUENCE_LIST</td>
<td align="right">81,626,769</td>
<td align="right">81,592,260</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">_BINARY_SUBSCR_STR_INT</td>
<td align="right">1,216,990,883</td>
<td align="right">1,216,602,013</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_FAST_WITH_KEYWORDS</td>
<td align="right">91,072,135</td>
<td align="right">91,096,605</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_DYNAMIC_EXIT</td>
<td align="right">185,418,396</td>
<td align="right">185,383,407</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">_BUILD_SLICE</td>
<td align="right">139,781,460</td>
<td align="right">139,805,248</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_COMPARE_OP_FLOAT</td>
<td align="right">101,252,850</td>
<td align="right">101,264,171</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_GET_YIELD_FROM_ITER</td>
<td align="right">916,047</td>
<td align="right">916,129</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_GUARD_NOS_FLOAT</td>
<td align="right">613,674,313</td>
<td align="right">613,722,987</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBTRACT_FLOAT</td>
<td align="right">383,046,880</td>
<td align="right">383,035,460</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">_GET_AWAITABLE</td>
<td align="right">653,796</td>
<td align="right">653,798</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_FOR_ITER_GEN_FRAME</td>
<td align="right">107,033,363</td>
<td align="right">107,033,192</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">_GET_ANEXT</td>
<td align="right">125,514,720</td>
<td align="right">125,514,720</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_STORE_NAME</td>
<td align="right">545,860</td>
<td align="right">545,860</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_POP_EXCEPT</td>
<td align="right">7,620</td>
<td align="right">7,620</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_UNPACK_EX</td>
<td align="right">104</td>
<td align="right">104</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_DELETE_ATTR</td>
<td align="right"></td>
<td align="right">2,009,931</td>
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
<td align="left">SEND_GEN</td>
<td align="right">260</td>
<td align="right">1,400</td>
<td align="right">438.5%</td>
</tr>
<tr>
<td align="left">BUILD_SET</td>
<td align="right">525</td>
<td align="right">1,318</td>
<td align="right">151.0%</td>
</tr>
<tr>
<td align="left">CALL_FUNCTION_EX</td>
<td align="right">6,061</td>
<td align="right">11,215</td>
<td align="right">85.0%</td>
</tr>
<tr>
<td align="left">IMPORT_NAME</td>
<td align="right">731</td>
<td align="right">1,028</td>
<td align="right">40.6%</td>
</tr>
<tr>
<td align="left">BINARY_OP_INPLACE_ADD_UNICODE</td>
<td align="right">703</td>
<td align="right">603</td>
<td align="right">-14.2%</td>
</tr>
<tr>
<td align="left">YIELD_VALUE</td>
<td align="right">140,949</td>
<td align="right">121,092</td>
<td align="right">-14.1%</td>
</tr>
<tr>
<td align="left">CALL_LIST_APPEND</td>
<td align="right">8,041</td>
<td align="right">6,974</td>
<td align="right">-13.3%</td>
</tr>
<tr>
<td align="left">CALL_ALLOC_AND_ENTER_INIT</td>
<td align="right">1,911</td>
<td align="right">1,672</td>
<td align="right">-12.5%</td>
</tr>
<tr>
<td align="left">CALL_PY_WITH_DEFAULTS</td>
<td align="right">11,800</td>
<td align="right">10,425</td>
<td align="right">-11.7%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_GETITEM</td>
<td align="right">3,280</td>
<td align="right">2,940</td>
<td align="right">-10.4%</td>
</tr>
<tr>
<td align="left">CALL_KW</td>
<td align="right">30,710</td>
<td align="right">32,888</td>
<td align="right">7.1%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">184,032</td>
<td align="right">171,941</td>
<td align="right">-6.6%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_PROPERTY</td>
<td align="right">8,210</td>
<td align="right">7,808</td>
<td align="right">-4.9%</td>
</tr>
<tr>
<td align="left">SEND</td>
<td align="right">32,412</td>
<td align="right">32,414</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_NAME</td>
<td align="right">1,360</td>
<td align="right">1,360</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BEFORE_WITH</td>
<td align="right">400</td>
<td align="right">400</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_WITH_HINT</td>
<td align="right">300</td>
<td align="right">300</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">RAISE_VARARGS</td>
<td align="right"></td>
<td align="right">160</td>
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
set bases
<details>
<summary>ⓘ</summary>

Setting the bases of a class, `cls.__bases__ = ...`
</details>
</td>
<td align="right">281</td>
<td align="right">281</td>
<td align="right">0.0%</td>
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
<tr>
<td align="left">
func modification
<details>
<summary>ⓘ</summary>

Modifying a function, e.g. `func.__defaults__ = ...`, etc.
</details>
</td>
<td align="right">461</td>
<td align="right">461</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">
watched dict modification
<details>
<summary>ⓘ</summary>

A watched dict has been modified
</details>
</td>
<td align="right">1,120</td>
<td align="right">1,120</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">
watched globals modification
<details>
<summary>ⓘ</summary>

A watched `globals()` dict has been modified
</details>
</td>
<td align="right">1,120</td>
<td align="right">1,120</td>
<td align="right">0.0%</td>
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
<td align="right">2,000</td>
<td align="right">2,000</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

---
Stats gathered on: 2024-04-30
