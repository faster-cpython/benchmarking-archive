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
<td align="left">JUMP_BACKWARD</td>
<td align="right">5,013,094,139</td>
<td align="right">1,676,216</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">1,877,873,127</td>
<td align="right">25,036,123</td>
<td align="right">-98.7%</td>
</tr>
<tr>
<td align="left">FOR_ITER_TUPLE</td>
<td align="right">680,415,295</td>
<td align="right">9,372,462</td>
<td align="right">-98.6%</td>
</tr>
<tr>
<td align="left">FOR_ITER_RANGE</td>
<td align="right">842,097,997</td>
<td align="right">30,115,379</td>
<td align="right">-96.4%</td>
</tr>
<tr>
<td align="left">GET_ANEXT</td>
<td align="right">133,515,680</td>
<td align="right">8,000,960</td>
<td align="right">-94.0%</td>
</tr>
<tr>
<td align="left">STORE_FAST_LOAD_FAST</td>
<td align="right">241,666,693</td>
<td align="right">15,893,526</td>
<td align="right">-93.4%</td>
</tr>
<tr>
<td align="left">STORE_SLICE</td>
<td align="right">162,467,568</td>
<td align="right">12,600,834</td>
<td align="right">-92.2%</td>
</tr>
<tr>
<td align="left">SET_ADD</td>
<td align="right">2,414,986</td>
<td align="right">240,265</td>
<td align="right">-90.1%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_LIST</td>
<td align="right">89,810,110</td>
<td align="right">9,009,911</td>
<td align="right">-90.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_MULTIPLY_FLOAT</td>
<td align="right">1,382,517,091</td>
<td align="right">146,545,575</td>
<td align="right">-89.4%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_FLOAT</td>
<td align="right">666,985,779</td>
<td align="right">72,564,769</td>
<td align="right">-89.1%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">488,846,863</td>
<td align="right">58,542,248</td>
<td align="right">-88.0%</td>
</tr>
<tr>
<td align="left">UNARY_INVERT</td>
<td align="right">15,171,009</td>
<td align="right">2,066,283</td>
<td align="right">-86.4%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_STR</td>
<td align="right">2,155,453,661</td>
<td align="right">314,791,231</td>
<td align="right">-85.4%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR</td>
<td align="right">451,851,453</td>
<td align="right">70,332,577</td>
<td align="right">-84.4%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_FLOAT</td>
<td align="right">458,483,378</td>
<td align="right">75,395,759</td>
<td align="right">-83.6%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_LIST_INT</td>
<td align="right">589,988,515</td>
<td align="right">99,278,642</td>
<td align="right">-83.2%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR</td>
<td align="right">1,530,405,122</td>
<td align="right">264,431,005</td>
<td align="right">-82.7%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP_SET</td>
<td align="right">1,944,989,564</td>
<td align="right">339,221,306</td>
<td align="right">-82.6%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_INT</td>
<td align="right">3,169,026,870</td>
<td align="right">640,947,696</td>
<td align="right">-79.8%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP_DICT</td>
<td align="right">538,292,478</td>
<td align="right">109,517,123</td>
<td align="right">-79.7%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE</td>
<td align="right">2,096,428</td>
<td align="right">452,951</td>
<td align="right">-78.4%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST_WITH_KEYWORDS</td>
<td align="right">198,649,934</td>
<td align="right">43,796,191</td>
<td align="right">-78.0%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">541,527,964</td>
<td align="right">120,242,688</td>
<td align="right">-77.8%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST</td>
<td align="right">1,340,514,559</td>
<td align="right">306,056,723</td>
<td align="right">-77.2%</td>
</tr>
<tr>
<td align="left">LIST_EXTEND</td>
<td align="right">127,769,871</td>
<td align="right">29,455,210</td>
<td align="right">-76.9%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">965,375,293</td>
<td align="right">259,198,997</td>
<td align="right">-73.2%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">1,819,941,281</td>
<td align="right">492,019,291</td>
<td align="right">-73.0%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_STR_INT</td>
<td align="right">1,675,423,423</td>
<td align="right">456,052,942</td>
<td align="right">-72.8%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_LIST_INT</td>
<td align="right">1,516,557,068</td>
<td align="right">415,642,246</td>
<td align="right">-72.6%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">1,652,647,708</td>
<td align="right">493,560,910</td>
<td align="right">-70.1%</td>
</tr>
<tr>
<td align="left">CALL_TYPE_1</td>
<td align="right">483,700,600</td>
<td align="right">147,591,661</td>
<td align="right">-69.5%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST_WITH_KEYWORDS</td>
<td align="right">131,891,145</td>
<td align="right">41,286,092</td>
<td align="right">-68.7%</td>
</tr>
<tr>
<td align="left">UNARY_NOT</td>
<td align="right">90,626,675</td>
<td align="right">28,369,246</td>
<td align="right">-68.7%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_GETITEM</td>
<td align="right">198,437,783</td>
<td align="right">62,207,954</td>
<td align="right">-68.7%</td>
</tr>
<tr>
<td align="left">LIST_APPEND</td>
<td align="right">298,819,963</td>
<td align="right">94,670,580</td>
<td align="right">-68.3%</td>
</tr>
<tr>
<td align="left">BUILD_SLICE</td>
<td align="right">211,876,338</td>
<td align="right">71,717,314</td>
<td align="right">-66.2%</td>
</tr>
<tr>
<td align="left">CALL_STR_1</td>
<td align="right">112,953,166</td>
<td align="right">38,335,373</td>
<td align="right">-66.1%</td>
</tr>
<tr>
<td align="left">FOR_ITER_GEN</td>
<td align="right">236,409,670</td>
<td align="right">83,330,230</td>
<td align="right">-64.8%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">14,854,717,243</td>
<td align="right">5,542,439,417</td>
<td align="right">-62.7%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">14,790,171,838</td>
<td align="right">5,720,830,306</td>
<td align="right">-61.3%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TUPLE</td>
<td align="right">507,133,223</td>
<td align="right">198,231,008</td>
<td align="right">-60.9%</td>
</tr>
<tr>
<td align="left">STORE_FAST_STORE_FAST</td>
<td align="right">973,933,056</td>
<td align="right">389,544,794</td>
<td align="right">-60.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">5,927,250,824</td>
<td align="right">2,377,777,241</td>
<td align="right">-59.9%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">12,657,520,242</td>
<td align="right">5,100,948,351</td>
<td align="right">-59.7%</td>
</tr>
<tr>
<td align="left">SET_FUNCTION_ATTRIBUTE</td>
<td align="right">131,922,258</td>
<td align="right">53,447,361</td>
<td align="right">-59.5%</td>
</tr>
<tr>
<td align="left">TO_BOOL_INT</td>
<td align="right">344,395,150</td>
<td align="right">141,729,063</td>
<td align="right">-58.8%</td>
</tr>
<tr>
<td align="left">MAKE_FUNCTION</td>
<td align="right">159,040,701</td>
<td align="right">65,541,398</td>
<td align="right">-58.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">11,677,872,156</td>
<td align="right">4,820,922,392</td>
<td align="right">-58.7%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_O</td>
<td align="right">1,272,364,718</td>
<td align="right">532,968,287</td>
<td align="right">-58.1%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">1,397,701,840</td>
<td align="right">589,148,069</td>
<td align="right">-57.8%</td>
</tr>
<tr>
<td align="left">NOP</td>
<td align="right">2,140,350,628</td>
<td align="right">938,189,006</td>
<td align="right">-56.2%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">1,189,984,272</td>
<td align="right">529,367,915</td>
<td align="right">-55.5%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_INT</td>
<td align="right">847,601,163</td>
<td align="right">383,334,217</td>
<td align="right">-54.8%</td>
</tr>
<tr>
<td align="left">BINARY_OP_MULTIPLY_INT</td>
<td align="right">361,392,740</td>
<td align="right">164,101,326</td>
<td align="right">-54.6%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">224,128,324</td>
<td align="right">104,919,541</td>
<td align="right">-53.2%</td>
</tr>
<tr>
<td align="left">BUILD_LIST</td>
<td align="right">488,368,574</td>
<td align="right">230,753,270</td>
<td align="right">-52.8%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_TUPLE_INT</td>
<td align="right">368,413,547</td>
<td align="right">178,750,716</td>
<td align="right">-51.5%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_DICT</td>
<td align="right">838,302,793</td>
<td align="right">409,591,029</td>
<td align="right">-51.1%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_DICT</td>
<td align="right">296,335,356</td>
<td align="right">146,780,167</td>
<td align="right">-50.5%</td>
</tr>
<tr>
<td align="left">IS_OP</td>
<td align="right">839,085,349</td>
<td align="right">416,008,653</td>
<td align="right">-50.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">2,907,217,313</td>
<td align="right">1,479,889,651</td>
<td align="right">-49.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">43,477,940,879</td>
<td align="right">22,260,838,455</td>
<td align="right">-48.8%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">5,114,363,907</td>
<td align="right">2,636,473,050</td>
<td align="right">-48.4%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">2,291,443,726</td>
<td align="right">1,187,756,139</td>
<td align="right">-48.2%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">1,015,961,235</td>
<td align="right">544,369,201</td>
<td align="right">-46.4%</td>
</tr>
<tr>
<td align="left">STORE_NAME</td>
<td align="right">1,187,062</td>
<td align="right">641,202</td>
<td align="right">-46.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">1,498,270,598</td>
<td align="right">815,075,918</td>
<td align="right">-45.6%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right">219,258,866</td>
<td align="right">119,444,162</td>
<td align="right">-45.5%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT</td>
<td align="right">2,178,095,431</td>
<td align="right">1,201,426,581</td>
<td align="right">-44.8%</td>
</tr>
<tr>
<td align="left">BINARY_OP_INPLACE_ADD_UNICODE</td>
<td align="right">8,738,017</td>
<td align="right">4,824,622</td>
<td align="right">-44.8%</td>
</tr>
<tr>
<td align="left">PUSH_NULL</td>
<td align="right">1,958,815,857</td>
<td align="right">1,100,357,714</td>
<td align="right">-43.8%</td>
</tr>
<tr>
<td align="left">BUILD_CONST_KEY_MAP</td>
<td align="right">13,544,131</td>
<td align="right">7,667,081</td>
<td align="right">-43.4%</td>
</tr>
<tr>
<td align="left">CALL_LEN</td>
<td align="right">504,673,006</td>
<td align="right">289,546,740</td>
<td align="right">-42.6%</td>
</tr>
<tr>
<td align="left">LOAD_NAME</td>
<td align="right">14,146,247</td>
<td align="right">8,145,287</td>
<td align="right">-42.4%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">450,978,319</td>
<td align="right">259,929,483</td>
<td align="right">-42.4%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">245,992,989</td>
<td align="right">143,792,883</td>
<td align="right">-41.5%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">4,341,510,226</td>
<td align="right">2,570,320,294</td>
<td align="right">-40.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">2,202,287,846</td>
<td align="right">1,312,564,443</td>
<td align="right">-40.4%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_FLOAT</td>
<td align="right">251,123,598</td>
<td align="right">149,877,842</td>
<td align="right">-40.3%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">397,139,390</td>
<td align="right">238,627,559</td>
<td align="right">-39.9%</td>
</tr>
<tr>
<td align="left">CALL_INTRINSIC_1</td>
<td align="right">252,090,797</td>
<td align="right">154,726,255</td>
<td align="right">-38.6%</td>
</tr>
<tr>
<td align="left">TO_BOOL_ALWAYS_TRUE</td>
<td align="right">296,005,040</td>
<td align="right">182,031,102</td>
<td align="right">-38.5%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">593,573,713</td>
<td align="right">368,571,669</td>
<td align="right">-37.9%</td>
</tr>
<tr>
<td align="left">CONVERT_VALUE</td>
<td align="right">139,688,818</td>
<td align="right">87,548,250</td>
<td align="right">-37.3%</td>
</tr>
<tr>
<td align="left">TO_BOOL_LIST</td>
<td align="right">181,401,815</td>
<td align="right">114,711,810</td>
<td align="right">-36.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">6,288,636,697</td>
<td align="right">4,067,441,187</td>
<td align="right">-35.3%</td>
</tr>
<tr>
<td align="left">MAP_ADD</td>
<td align="right">60,510,878</td>
<td align="right">39,180,859</td>
<td align="right">-35.2%</td>
</tr>
<tr>
<td align="left">BINARY_SLICE</td>
<td align="right">347,699,503</td>
<td align="right">225,313,670</td>
<td align="right">-35.2%</td>
</tr>
<tr>
<td align="left">FORMAT_SIMPLE</td>
<td align="right">150,307,488</td>
<td align="right">97,514,117</td>
<td align="right">-35.1%</td>
</tr>
<tr>
<td align="left">CALL_ISINSTANCE</td>
<td align="right">1,161,894,832</td>
<td align="right">766,848,191</td>
<td align="right">-34.0%</td>
</tr>
<tr>
<td align="left">BUILD_STRING</td>
<td align="right">76,313,355</td>
<td align="right">50,580,393</td>
<td align="right">-33.7%</td>
</tr>
<tr>
<td align="left">JUMP_FORWARD</td>
<td align="right">655,541,682</td>
<td align="right">437,760,825</td>
<td align="right">-33.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_NO_DICT</td>
<td align="right">99,873,515</td>
<td align="right">66,936,117</td>
<td align="right">-33.0%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">922,166,671</td>
<td align="right">619,955,209</td>
<td align="right">-32.8%</td>
</tr>
<tr>
<td align="left">CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">269,729,512</td>
<td align="right">186,706,165</td>
<td align="right">-30.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">2,457,304,140</td>
<td align="right">1,701,122,549</td>
<td align="right">-30.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_LAZY_DICT</td>
<td align="right">356,132,307</td>
<td align="right">247,724,846</td>
<td align="right">-30.4%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">4,699,573,727</td>
<td align="right">3,295,160,101</td>
<td align="right">-29.9%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_CLASS</td>
<td align="right">221,344,411</td>
<td align="right">159,420,564</td>
<td align="right">-28.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL_STR</td>
<td align="right">105,374,995</td>
<td align="right">76,949,761</td>
<td align="right">-27.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_UNICODE</td>
<td align="right">99,388,335</td>
<td align="right">72,647,145</td>
<td align="right">-26.9%</td>
</tr>
<tr>
<td align="left">CALL_TUPLE_1</td>
<td align="right">28,824,471</td>
<td align="right">21,369,014</td>
<td align="right">-25.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_WITH_HINT</td>
<td align="right">476,947,337</td>
<td align="right">364,881,810</td>
<td align="right">-23.5%</td>
</tr>
<tr>
<td align="left">COPY_FREE_VARS</td>
<td align="right">371,290,982</td>
<td align="right">287,179,573</td>
<td align="right">-22.7%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NONE</td>
<td align="right">499,707,032</td>
<td align="right">390,972,610</td>
<td align="right">-21.8%</td>
</tr>
<tr>
<td align="left">DICT_MERGE</td>
<td align="right">54,718,964</td>
<td align="right">42,862,124</td>
<td align="right">-21.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_MODULE</td>
<td align="right">661,243,297</td>
<td align="right">521,225,846</td>
<td align="right">-21.2%</td>
</tr>
<tr>
<td align="left">TO_BOOL_NONE</td>
<td align="right">643,037,869</td>
<td align="right">507,364,043</td>
<td align="right">-21.1%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">8,243,510,100</td>
<td align="right">6,594,068,708</td>
<td align="right">-20.0%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">4,230,285,760</td>
<td align="right">3,463,279,142</td>
<td align="right">-18.1%</td>
</tr>
<tr>
<td align="left">RETURN_GENERATOR</td>
<td align="right">505,536,077</td>
<td align="right">414,256,105</td>
<td align="right">-18.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_PROPERTY</td>
<td align="right">87,014,842</td>
<td align="right">71,574,326</td>
<td align="right">-17.7%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">4,798,770,021</td>
<td align="right">4,016,210,135</td>
<td align="right">-16.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_AND_CLEAR</td>
<td align="right">103,111,548</td>
<td align="right">86,519,891</td>
<td align="right">-16.1%</td>
</tr>
<tr>
<td align="left">STORE_GLOBAL</td>
<td align="right">8,205,260</td>
<td align="right">6,929,920</td>
<td align="right">-15.5%</td>
</tr>
<tr>
<td align="left">UNARY_NEGATIVE</td>
<td align="right">171,058,128</td>
<td align="right">145,910,224</td>
<td align="right">-14.7%</td>
</tr>
<tr>
<td align="left">BUILD_MAP</td>
<td align="right">143,314,610</td>
<td align="right">123,387,647</td>
<td align="right">-13.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_CLASS</td>
<td align="right">184,608,506</td>
<td align="right">159,685,507</td>
<td align="right">-13.5%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NOT_NONE</td>
<td align="right">768,766,968</td>
<td align="right">666,797,539</td>
<td align="right">-13.3%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">1,292,138,195</td>
<td align="right">1,133,083,327</td>
<td align="right">-12.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_CHECK</td>
<td align="right">12,074,663</td>
<td align="right">11,115,705</td>
<td align="right">-7.9%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_SLOT</td>
<td align="right">1,623,674,023</td>
<td align="right">1,498,178,353</td>
<td align="right">-7.7%</td>
</tr>
<tr>
<td align="left">INTERPRETER_EXIT</td>
<td align="right">2,165,958,960</td>
<td align="right">2,305,992,976</td>
<td align="right">6.5%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_O</td>
<td align="right">420,326,441</td>
<td align="right">393,932,139</td>
<td align="right">-6.3%</td>
</tr>
<tr>
<td align="left">MAKE_CELL</td>
<td align="right">110,362,288</td>
<td align="right">103,595,076</td>
<td align="right">-6.1%</td>
</tr>
<tr>
<td align="left">STORE_DEREF</td>
<td align="right">98,172,202</td>
<td align="right">94,311,474</td>
<td align="right">-3.9%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_WITH_HINT</td>
<td align="right">67,299,734</td>
<td align="right">64,723,774</td>
<td align="right">-3.8%</td>
</tr>
<tr>
<td align="left">YIELD_VALUE</td>
<td align="right">1,406,021,089</td>
<td align="right">1,355,146,974</td>
<td align="right">-3.6%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">2,121,481,334</td>
<td align="right">2,053,347,919</td>
<td align="right">-3.2%</td>
</tr>
<tr>
<td align="left">DICT_UPDATE</td>
<td align="right">70,933</td>
<td align="right">72,539</td>
<td align="right">2.3%</td>
</tr>
<tr>
<td align="left">CALL_PY_WITH_DEFAULTS</td>
<td align="right">221,155,575</td>
<td align="right">216,543,096</td>
<td align="right">-2.1%</td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">77,786,370</td>
<td align="right">76,738,067</td>
<td align="right">-1.3%</td>
</tr>
<tr>
<td align="left">DELETE_SUBSCR</td>
<td align="right">177,912,865</td>
<td align="right">176,285,792</td>
<td align="right">-0.9%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">1,216,560,160</td>
<td align="right">1,208,390,146</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">END_FOR</td>
<td align="right">82,846,489</td>
<td align="right">82,357,219</td>
<td align="right">-0.6%</td>
</tr>
<tr>
<td align="left">DELETE_FAST</td>
<td align="right">2,214,806</td>
<td align="right">2,226,016</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">CALL_KW</td>
<td align="right">275,165,119</td>
<td align="right">273,956,686</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">GET_YIELD_FROM_ITER</td>
<td align="right">47,508,639</td>
<td align="right">47,311,055</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">CALL_LIST_APPEND</td>
<td align="right">349,291,145</td>
<td align="right">348,148,759</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">BEFORE_WITH</td>
<td align="right">10,127,508</td>
<td align="right">10,097,565</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">GET_AWAITABLE</td>
<td align="right">229,778,700</td>
<td align="right">229,136,451</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">INSTRUMENTED_JUMP_BACKWARD</td>
<td align="right">6,256</td>
<td align="right">6,240</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">EXIT_INIT_CHECK</td>
<td align="right">94,927,684</td>
<td align="right">94,703,930</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">CALL_ALLOC_AND_ENTER_INIT</td>
<td align="right">97,216,326</td>
<td align="right">96,991,992</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR_METHOD</td>
<td align="right">126,988,809</td>
<td align="right">126,796,333</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">CALL_FUNCTION_EX</td>
<td align="right">219,021,884</td>
<td align="right">218,787,063</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">PUSH_EXC_INFO</td>
<td align="right">24,971,229</td>
<td align="right">24,975,243</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">POP_EXCEPT</td>
<td align="right">24,971,084</td>
<td align="right">24,975,095</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CHECK_EXC_MATCH</td>
<td align="right">24,459,719</td>
<td align="right">24,463,637</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">345,334</td>
<td align="right">345,381</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">UNPACK_EX</td>
<td align="right">1,129,926</td>
<td align="right">1,129,822</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">BUILD_SET</td>
<td align="right">2,329,882</td>
<td align="right">2,329,712</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">RAISE_VARARGS</td>
<td align="right">6,185,283</td>
<td align="right">6,185,625</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR</td>
<td align="right">23,564</td>
<td align="right">23,565</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR_ATTR</td>
<td align="right">7,752,015</td>
<td align="right">7,751,739</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">IMPORT_FROM</td>
<td align="right">13,104,211</td>
<td align="right">13,103,758</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">END_SEND</td>
<td align="right">402,606,775</td>
<td align="right">402,618,321</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">SEND</td>
<td align="right">173,833,052</td>
<td align="right">173,837,768</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">IMPORT_NAME</td>
<td align="right">12,436,140</td>
<td align="right">12,435,803</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">SEND_GEN</td>
<td align="right">787,087,768</td>
<td align="right">787,107,784</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">DELETE_ATTR</td>
<td align="right">6,692,853</td>
<td align="right">6,693,012</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD_NO_INTERRUPT</td>
<td align="right">556,666,639</td>
<td align="right">556,677,852</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">20,772,657</td>
<td align="right">20,772,759</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">RERAISE</td>
<td align="right">3,848,401</td>
<td align="right">3,848,387</td>
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
<td align="left">WITH_EXCEPT_START</td>
<td align="right">233,480</td>
<td align="right">233,480</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">SET_UPDATE</td>
<td align="right">200,488</td>
<td align="right">200,488</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CLEANUP_THROW</td>
<td align="right">152,060</td>
<td align="right">152,060</td>
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
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right"></td>
<td align="right">2,986,432,911</td>
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
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">6,943,721,563</td>
<td align="right">82.7%</td>
<td align="right">1,529,472,887</td>
<td align="right">71.2%</td>
<td align="right">-78.0%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">1,445,379,820</td>
<td align="right">17.2%</td>
<td align="right">618,171,252</td>
<td align="right">28.8%</td>
<td align="right">-57.2%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">50,411,810</td>
<td align="right">0.6%</td>
<td align="right">30,888,222</td>
<td align="right">1.4%</td>
<td align="right">-38.7%</td>
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
<td align="right">1,004,465</td>
<td align="right">36.7%</td>
<td align="right">636,046</td>
<td align="right">34.1%</td>
<td align="right">-36.7%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">1,729,365</td>
<td align="right">63.3%</td>
<td align="right">1,228,993</td>
<td align="right">65.9%</td>
<td align="right">-28.9%</td>
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
<td align="left">lshift</td>
<td align="right">29,566</td>
<td align="right">1.7%</td>
<td align="right">5,707</td>
<td align="right">0.5%</td>
<td align="right">-80.7%</td>
</tr>
<tr>
<td align="left">rshift</td>
<td align="right">37,333</td>
<td align="right">2.2%</td>
<td align="right">8,859</td>
<td align="right">0.7%</td>
<td align="right">-76.3%</td>
</tr>
<tr>
<td align="left">xor</td>
<td align="right">29,504</td>
<td align="right">1.7%</td>
<td align="right">8,725</td>
<td align="right">0.7%</td>
<td align="right">-70.4%</td>
</tr>
<tr>
<td align="left">true divide float</td>
<td align="right">18,164</td>
<td align="right">1.1%</td>
<td align="right">5,665</td>
<td align="right">0.5%</td>
<td align="right">-68.8%</td>
</tr>
<tr>
<td align="left">add different types</td>
<td align="right">217,975</td>
<td align="right">12.6%</td>
<td align="right">78,515</td>
<td align="right">6.4%</td>
<td align="right">-64.0%</td>
</tr>
<tr>
<td align="left">multiply different types</td>
<td align="right">252,336</td>
<td align="right">14.6%</td>
<td align="right">92,075</td>
<td align="right">7.5%</td>
<td align="right">-63.5%</td>
</tr>
<tr>
<td align="left">true divide different types</td>
<td align="right">31,464</td>
<td align="right">1.8%</td>
<td align="right">12,505</td>
<td align="right">1.0%</td>
<td align="right">-60.3%</td>
</tr>
<tr>
<td align="left">power</td>
<td align="right">13,748</td>
<td align="right">0.8%</td>
<td align="right">5,755</td>
<td align="right">0.5%</td>
<td align="right">-58.1%</td>
</tr>
<tr>
<td align="left">and int</td>
<td align="right">75,634</td>
<td align="right">4.4%</td>
<td align="right">37,205</td>
<td align="right">3.0%</td>
<td align="right">-50.8%</td>
</tr>
<tr>
<td align="left">floor divide</td>
<td align="right">53,496</td>
<td align="right">3.1%</td>
<td align="right">33,240</td>
<td align="right">2.7%</td>
<td align="right">-37.9%</td>
</tr>
<tr>
<td align="left">subtract other</td>
<td align="right">16,234</td>
<td align="right">0.9%</td>
<td align="right">12,352</td>
<td align="right">1.0%</td>
<td align="right">-23.9%</td>
</tr>
<tr>
<td align="left">remainder</td>
<td align="right">68,975</td>
<td align="right">4.0%</td>
<td align="right">53,213</td>
<td align="right">4.3%</td>
<td align="right">-22.9%</td>
</tr>
<tr>
<td align="left">or</td>
<td align="right">20,042</td>
<td align="right">1.2%</td>
<td align="right">17,134</td>
<td align="right">1.4%</td>
<td align="right">-14.5%</td>
</tr>
<tr>
<td align="left">add other</td>
<td align="right">74,405</td>
<td align="right">4.3%</td>
<td align="right">64,265</td>
<td align="right">5.2%</td>
<td align="right">-13.6%</td>
</tr>
<tr>
<td align="left">multiply other</td>
<td align="right">5,500</td>
<td align="right">0.3%</td>
<td align="right">5,220</td>
<td align="right">0.4%</td>
<td align="right">-5.1%</td>
</tr>
<tr>
<td align="left">true divide other</td>
<td align="right">3,520</td>
<td align="right">0.2%</td>
<td align="right">3,440</td>
<td align="right">0.3%</td>
<td align="right">-2.3%</td>
</tr>
<tr>
<td align="left">subtract different types</td>
<td align="right">778,833</td>
<td align="right">45.0%</td>
<td align="right">782,485</td>
<td align="right">63.7%</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">and other</td>
<td align="right">2,017</td>
<td align="right">0.1%</td>
<td align="right">2,014</td>
<td align="right">0.2%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">and different types</td>
<td align="right">619</td>
<td align="right">0.0%</td>
<td align="right">619</td>
<td align="right">0.1%</td>
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
<td align="right">1,534,851,910</td>
<td align="right">25.0%</td>
<td align="right">268,986,701</td>
<td align="right">15.1%</td>
<td align="right">-82.5%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">4,592,014,441</td>
<td align="right">74.9%</td>
<td align="right">1,517,343,366</td>
<td align="right">84.9%</td>
<td align="right">-67.0%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">5,120,173</td>
<td align="right">0.1%</td>
<td align="right">4,901,521</td>
<td align="right">0.3%</td>
<td align="right">-4.3%</td>
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
<td align="right">467,363</td>
<td align="right">69.4%</td>
<td align="right">143,998</td>
<td align="right">41.6%</td>
<td align="right">-69.2%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">206,022</td>
<td align="right">30.6%</td>
<td align="right">201,827</td>
<td align="right">58.4%</td>
<td align="right">-2.0%</td>
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
<td align="left">list slice</td>
<td align="right">35,320</td>
<td align="right">7.6%</td>
<td align="right">1,360</td>
<td align="right">0.9%</td>
<td align="right">-96.1%</td>
</tr>
<tr>
<td align="left">array int</td>
<td align="right">157,600</td>
<td align="right">33.7%</td>
<td align="right">15,880</td>
<td align="right">11.0%</td>
<td align="right">-89.9%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">126,051</td>
<td align="right">27.0%</td>
<td align="right">25,065</td>
<td align="right">17.4%</td>
<td align="right">-80.1%</td>
</tr>
<tr>
<td align="left">buffer int</td>
<td align="right">49,203</td>
<td align="right">10.5%</td>
<td align="right">22,303</td>
<td align="right">15.5%</td>
<td align="right">-54.7%</td>
</tr>
<tr>
<td align="left">out of range</td>
<td align="right">88,589</td>
<td align="right">19.0%</td>
<td align="right">68,907</td>
<td align="right">47.9%</td>
<td align="right">-22.2%</td>
</tr>
<tr>
<td align="left">buffer slice</td>
<td align="right">980</td>
<td align="right">0.2%</td>
<td align="right">900</td>
<td align="right">0.6%</td>
<td align="right">-8.2%</td>
</tr>
<tr>
<td align="left">code complex parameters</td>
<td align="right">5,036</td>
<td align="right">1.1%</td>
<td align="right">4,998</td>
<td align="right">3.5%</td>
<td align="right">-0.8%</td>
</tr>
<tr>
<td align="left">tuple slice</td>
<td align="right">184</td>
<td align="right">0.0%</td>
<td align="right">185</td>
<td align="right">0.1%</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">sequence int</td>
<td align="right">4,300</td>
<td align="right">0.9%</td>
<td align="right">4,300</td>
<td align="right">3.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">string slice</td>
<td align="right">100</td>
<td align="right">0.0%</td>
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
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">12,198,900,417</td>
<td align="right">89.2%</td>
<td align="right">6,715,478,848</td>
<td align="right">82.1%</td>
<td align="right">-45.0%</td>
</tr>
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
<td align="right">33,100</td>
<td align="right">0.0%</td>
<td align="right">-19.9%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">265,450,080</td>
<td align="right">1.9%</td>
<td align="right">252,573,451</td>
<td align="right">3.1%</td>
<td align="right">-4.9%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">1,475,408,638</td>
<td align="right">10.8%</td>
<td align="right">1,454,606,896</td>
<td align="right">17.8%</td>
<td align="right">-1.4%</td>
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
<td align="right">5,638,256</td>
<td align="right">85.4%</td>
<td align="right">5,395,385</td>
<td align="right">84.9%</td>
<td align="right">-4.3%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">963,346</td>
<td align="right">14.6%</td>
<td align="right">961,316</td>
<td align="right">15.1%</td>
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
<td align="left">cmethod</td>
<td align="right">14,100</td>
<td align="right">1.5%</td>
<td align="right">13,620</td>
<td align="right">1.4%</td>
<td align="right">-3.4%</td>
</tr>
<tr>
<td align="left">class mutable</td>
<td align="right">25,288</td>
<td align="right">2.6%</td>
<td align="right">24,743</td>
<td align="right">2.6%</td>
<td align="right">-2.2%</td>
</tr>
<tr>
<td align="left">cfunc noargs</td>
<td align="right">70,240</td>
<td align="right">7.3%</td>
<td align="right">69,462</td>
<td align="right">7.2%</td>
<td align="right">-1.1%</td>
</tr>
<tr>
<td align="left">bound method</td>
<td align="right">11,875</td>
<td align="right">1.2%</td>
<td align="right">11,994</td>
<td align="right">1.2%</td>
<td align="right">1.0%</td>
</tr>
<tr>
<td align="left">operator wrapper</td>
<td align="right">10,180</td>
<td align="right">1.1%</td>
<td align="right">10,136</td>
<td align="right">1.1%</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">method wrapper</td>
<td align="right">8,250</td>
<td align="right">0.9%</td>
<td align="right">8,224</td>
<td align="right">0.9%</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">wrong number arguments</td>
<td align="right">13,773</td>
<td align="right">1.4%</td>
<td align="right">13,753</td>
<td align="right">1.4%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">meth descr varargs keywords</td>
<td align="right">20,855</td>
<td align="right">2.2%</td>
<td align="right">20,884</td>
<td align="right">2.2%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">init not python</td>
<td align="right">16,406</td>
<td align="right">1.7%</td>
<td align="right">16,386</td>
<td align="right">1.7%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">meth descr varargs</td>
<td align="right">16,497</td>
<td align="right">1.7%</td>
<td align="right">16,516</td>
<td align="right">1.7%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">meth descr method fastcall keywords</td>
<td align="right">207,334</td>
<td align="right">21.5%</td>
<td align="right">207,157</td>
<td align="right">21.5%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">class no vectorcall</td>
<td align="right">89,233</td>
<td align="right">9.3%</td>
<td align="right">89,303</td>
<td align="right">9.3%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">cfunc varargs keywords</td>
<td align="right">32,282</td>
<td align="right">3.4%</td>
<td align="right">32,257</td>
<td align="right">3.4%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">65,839</td>
<td align="right">6.8%</td>
<td align="right">65,799</td>
<td align="right">6.8%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">code complex parameters</td>
<td align="right">185,222</td>
<td align="right">19.2%</td>
<td align="right">185,140</td>
<td align="right">19.3%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">init not inline values</td>
<td align="right">105,602</td>
<td align="right">11.0%</td>
<td align="right">105,557</td>
<td align="right">11.0%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">metaclass</td>
<td align="right">43,023</td>
<td align="right">4.5%</td>
<td align="right">43,038</td>
<td align="right">4.5%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">cfunc varargs</td>
<td align="right">14,249</td>
<td align="right">1.5%</td>
<td align="right">14,249</td>
<td align="right">1.5%</td>
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
<td align="left">out of versions</td>
<td align="right">980</td>
<td align="right">0.1%</td>
<td align="right">980</td>
<td align="right">0.1%</td>
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
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">4,582,717,667</td>
<td align="right">94.9%</td>
<td align="right">1,664,224,974</td>
<td align="right">92.0%</td>
<td align="right">-63.7%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">247,569,957</td>
<td align="right">5.1%</td>
<td align="right">145,320,409</td>
<td align="right">8.0%</td>
<td align="right">-41.3%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">1,955,023</td>
<td align="right">0.0%</td>
<td align="right">1,870,680</td>
<td align="right">0.1%</td>
<td align="right">-4.3%</td>
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
<td align="right">263,164</td>
<td align="right">69.6%</td>
<td align="right">229,924</td>
<td align="right">67.0%</td>
<td align="right">-12.6%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">114,891</td>
<td align="right">30.4%</td>
<td align="right">113,230</td>
<td align="right">33.0%</td>
<td align="right">-1.4%</td>
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
<td align="right">10,363</td>
<td align="right">3.9%</td>
<td align="right">1,663</td>
<td align="right">0.7%</td>
<td align="right">-84.0%</td>
</tr>
<tr>
<td align="left">bool</td>
<td align="right">5,865</td>
<td align="right">2.2%</td>
<td align="right">3,778</td>
<td align="right">1.6%</td>
<td align="right">-35.6%</td>
</tr>
<tr>
<td align="left">float long</td>
<td align="right">21,138</td>
<td align="right">8.0%</td>
<td align="right">16,454</td>
<td align="right">7.2%</td>
<td align="right">-22.2%</td>
</tr>
<tr>
<td align="left">bytes</td>
<td align="right">4,860</td>
<td align="right">1.8%</td>
<td align="right">3,920</td>
<td align="right">1.7%</td>
<td align="right">-19.3%</td>
</tr>
<tr>
<td align="left">baseobject</td>
<td align="right">39,483</td>
<td align="right">15.0%</td>
<td align="right">31,935</td>
<td align="right">13.9%</td>
<td align="right">-19.1%</td>
</tr>
<tr>
<td align="left">different types</td>
<td align="right">59,569</td>
<td align="right">22.6%</td>
<td align="right">54,786</td>
<td align="right">23.8%</td>
<td align="right">-8.0%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">25,175</td>
<td align="right">9.6%</td>
<td align="right">23,983</td>
<td align="right">10.4%</td>
<td align="right">-4.7%</td>
</tr>
<tr>
<td align="left">big int</td>
<td align="right">64,597</td>
<td align="right">24.5%</td>
<td align="right">62,045</td>
<td align="right">27.0%</td>
<td align="right">-4.0%</td>
</tr>
<tr>
<td align="left">long float</td>
<td align="right">1,580</td>
<td align="right">0.6%</td>
<td align="right">1,522</td>
<td align="right">0.7%</td>
<td align="right">-3.7%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">15,060</td>
<td align="right">5.7%</td>
<td align="right">14,544</td>
<td align="right">6.3%</td>
<td align="right">-3.4%</td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">4,354</td>
<td align="right">1.7%</td>
<td align="right">4,214</td>
<td align="right">1.8%</td>
<td align="right">-3.2%</td>
</tr>
<tr>
<td align="left">string</td>
<td align="right">11,120</td>
<td align="right">4.2%</td>
<td align="right">11,080</td>
<td align="right">4.8%</td>
<td align="right">-0.4%</td>
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
<td align="right">2,480,735,802</td>
<td align="right">91.6%</td>
<td align="right">446,192,189</td>
<td align="right">80.6%</td>
<td align="right">-82.0%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">226,444,233</td>
<td align="right">8.4%</td>
<td align="right">107,271,686</td>
<td align="right">19.4%</td>
<td align="right">-52.6%</td>
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
<td align="right">0.1%</td>
<td align="right">2,546,240</td>
<td align="right">0.5%</td>
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
<td align="right">162,822</td>
<td align="right">70.7%</td>
<td align="right">126,584</td>
<td align="right">65.2%</td>
<td align="right">-22.3%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">67,509</td>
<td align="right">29.3%</td>
<td align="right">67,511</td>
<td align="right">34.8%</td>
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
<td align="left">list</td>
<td align="right">33,251</td>
<td align="right">20.4%</td>
<td align="right">18,247</td>
<td align="right">14.4%</td>
<td align="right">-45.1%</td>
</tr>
<tr>
<td align="left">str</td>
<td align="right">46,753</td>
<td align="right">28.7%</td>
<td align="right">33,775</td>
<td align="right">26.7%</td>
<td align="right">-27.8%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">33,455</td>
<td align="right">20.5%</td>
<td align="right">27,874</td>
<td align="right">22.0%</td>
<td align="right">-16.7%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">49,363</td>
<td align="right">30.3%</td>
<td align="right">46,688</td>
<td align="right">36.9%</td>
<td align="right">-5.4%</td>
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
<td align="right">175,755,086</td>
<td align="right">4.2%</td>
<td align="right">332,481</td>
<td align="right">0.1%</td>
<td align="right">-99.8%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">3,461,041,003</td>
<td align="right">82.8%</td>
<td align="right">147,521,713</td>
<td align="right">55.0%</td>
<td align="right">-95.7%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">713,541,040</td>
<td align="right">17.1%</td>
<td align="right">120,337,048</td>
<td align="right">44.9%</td>
<td align="right">-83.1%</td>
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
<td align="right">3,382,215</td>
<td align="right">90.4%</td>
<td align="right">72,440</td>
<td align="right">30.4%</td>
<td align="right">-97.9%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">359,795</td>
<td align="right">9.6%</td>
<td align="right">165,681</td>
<td align="right">69.6%</td>
<td align="right">-54.0%</td>
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
<td align="right">30,660</td>
<td align="right">8.5%</td>
<td align="right">6,060</td>
<td align="right">3.7%</td>
<td align="right">-80.2%</td>
</tr>
<tr>
<td align="left">map</td>
<td align="right">2,280</td>
<td align="right">0.6%</td>
<td align="right">740</td>
<td align="right">0.4%</td>
<td align="right">-67.5%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">29,259</td>
<td align="right">8.1%</td>
<td align="right">10,999</td>
<td align="right">6.6%</td>
<td align="right">-62.4%</td>
</tr>
<tr>
<td align="left">enumerate</td>
<td align="right">52,073</td>
<td align="right">14.5%</td>
<td align="right">19,930</td>
<td align="right">12.0%</td>
<td align="right">-61.7%</td>
</tr>
<tr>
<td align="left">dict items</td>
<td align="right">118,506</td>
<td align="right">32.9%</td>
<td align="right">50,555</td>
<td align="right">30.5%</td>
<td align="right">-57.3%</td>
</tr>
<tr>
<td align="left">ascii string</td>
<td align="right">5,960</td>
<td align="right">1.7%</td>
<td align="right">2,680</td>
<td align="right">1.6%</td>
<td align="right">-55.0%</td>
</tr>
<tr>
<td align="left">dict values</td>
<td align="right">14,770</td>
<td align="right">4.1%</td>
<td align="right">6,990</td>
<td align="right">4.2%</td>
<td align="right">-52.7%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">45,542</td>
<td align="right">12.7%</td>
<td align="right">22,750</td>
<td align="right">13.7%</td>
<td align="right">-50.0%</td>
</tr>
<tr>
<td align="left">callable</td>
<td align="right">522</td>
<td align="right">0.1%</td>
<td align="right">282</td>
<td align="right">0.2%</td>
<td align="right">-46.0%</td>
</tr>
<tr>
<td align="left">zip</td>
<td align="right">21,604</td>
<td align="right">6.0%</td>
<td align="right">14,352</td>
<td align="right">8.7%</td>
<td align="right">-33.6%</td>
</tr>
<tr>
<td align="left">itertools</td>
<td align="right">10,806</td>
<td align="right">3.0%</td>
<td align="right">7,249</td>
<td align="right">4.4%</td>
<td align="right">-32.9%</td>
</tr>
<tr>
<td align="left">bytes</td>
<td align="right">880</td>
<td align="right">0.2%</td>
<td align="right">660</td>
<td align="right">0.4%</td>
<td align="right">-25.0%</td>
</tr>
<tr>
<td align="left">reversed list</td>
<td align="right">10,132</td>
<td align="right">2.8%</td>
<td align="right">7,865</td>
<td align="right">4.7%</td>
<td align="right">-22.4%</td>
</tr>
<tr>
<td align="left">dict keys</td>
<td align="right">16,781</td>
<td align="right">4.7%</td>
<td align="right">14,549</td>
<td align="right">8.8%</td>
<td align="right">-13.3%</td>
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
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">2,498,099,539</td>
<td align="right">14.3%</td>
<td align="right">1,370,379,838</td>
<td align="right">12.5%</td>
<td align="right">-45.1%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">1,022,536,296</td>
<td align="right">5.9%</td>
<td align="right">568,560,760</td>
<td align="right">5.2%</td>
<td align="right">-44.4%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">14,918,078,050</td>
<td align="right">85.5%</td>
<td align="right">9,544,019,364</td>
<td align="right">87.3%</td>
<td align="right">-36.0%</td>
</tr>
<tr>
<td align="left">
deopt
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">680,687</td>
<td align="right">0.0%</td>
<td align="right">681,008</td>
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
<td align="right">20,179,175</td>
<td align="right">88.9%</td>
<td align="right">11,614,387</td>
<td align="right">87.6%</td>
<td align="right">-42.4%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">2,528,180</td>
<td align="right">11.1%</td>
<td align="right">1,642,453</td>
<td align="right">12.4%</td>
<td align="right">-35.0%</td>
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
<td align="left">not managed dict</td>
<td align="right">959,386</td>
<td align="right">37.9%</td>
<td align="right">247,146</td>
<td align="right">15.0%</td>
<td align="right">-74.2%</td>
</tr>
<tr>
<td align="left">metaclass attribute</td>
<td align="right">280,505</td>
<td align="right">11.1%</td>
<td align="right">190,881</td>
<td align="right">11.6%</td>
<td align="right">-32.0%</td>
</tr>
<tr>
<td align="left">method</td>
<td align="right">171,007</td>
<td align="right">6.8%</td>
<td align="right">117,850</td>
<td align="right">7.2%</td>
<td align="right">-31.1%</td>
</tr>
<tr>
<td align="left">class method obj</td>
<td align="right">28,443</td>
<td align="right">1.1%</td>
<td align="right">21,933</td>
<td align="right">1.3%</td>
<td align="right">-22.9%</td>
</tr>
<tr>
<td align="left">overridden</td>
<td align="right">21,112</td>
<td align="right">0.8%</td>
<td align="right">19,310</td>
<td align="right">1.2%</td>
<td align="right">-8.5%</td>
</tr>
<tr>
<td align="left">shadowed</td>
<td align="right">150,462</td>
<td align="right">6.0%</td>
<td align="right">138,881</td>
<td align="right">8.5%</td>
<td align="right">-7.7%</td>
</tr>
<tr>
<td align="left">mutable class</td>
<td align="right">82,919</td>
<td align="right">3.3%</td>
<td align="right">77,298</td>
<td align="right">4.7%</td>
<td align="right">-6.8%</td>
</tr>
<tr>
<td align="left">not in keys</td>
<td align="right">16,660</td>
<td align="right">0.7%</td>
<td align="right">15,620</td>
<td align="right">1.0%</td>
<td align="right">-6.2%</td>
</tr>
<tr>
<td align="left">non overriding descriptor</td>
<td align="right">14,092</td>
<td align="right">0.6%</td>
<td align="right">13,514</td>
<td align="right">0.8%</td>
<td align="right">-4.1%</td>
</tr>
<tr>
<td align="left">out of versions</td>
<td align="right">2,358</td>
<td align="right">0.1%</td>
<td align="right">2,281</td>
<td align="right">0.1%</td>
<td align="right">-3.3%</td>
</tr>
<tr>
<td align="left">non string or split</td>
<td align="right">22,733</td>
<td align="right">0.9%</td>
<td align="right">22,013</td>
<td align="right">1.3%</td>
<td align="right">-3.2%</td>
</tr>
<tr>
<td align="left">builtin class method</td>
<td align="right">3,937</td>
<td align="right">0.2%</td>
<td align="right">3,817</td>
<td align="right">0.2%</td>
<td align="right">-3.0%</td>
</tr>
<tr>
<td align="left">class attr descriptor</td>
<td align="right">30,840</td>
<td align="right">1.2%</td>
<td align="right">30,160</td>
<td align="right">1.8%</td>
<td align="right">-2.2%</td>
</tr>
<tr>
<td align="left">non object slot</td>
<td align="right">3,600</td>
<td align="right">0.1%</td>
<td align="right">3,540</td>
<td align="right">0.2%</td>
<td align="right">-1.7%</td>
</tr>
<tr>
<td align="left">module attr not found</td>
<td align="right">17,959</td>
<td align="right">0.7%</td>
<td align="right">17,842</td>
<td align="right">1.1%</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">class attr simple</td>
<td align="right">720,387</td>
<td align="right">28.5%</td>
<td align="right">718,587</td>
<td align="right">43.8%</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">wrong number arguments</td>
<td align="right">1,100</td>
<td align="right">0.0%</td>
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
<td align="right">10,626,365,786</td>
<td align="right">99.8%</td>
<td align="right">5,672,480,694</td>
<td align="right">99.6%</td>
<td align="right">-46.6%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">458,765</td>
<td align="right">0.0%</td>
<td align="right">456,648</td>
<td align="right">0.0%</td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">20,563,280</td>
<td align="right">0.2%</td>
<td align="right">20,561,268</td>
<td align="right">0.4%</td>
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
<td align="right">668,142</td>
<td align="right">100.0%</td>
<td align="right">668,139</td>
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
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">134,740,824</td>
<td align="right">100.0%</td>
<td align="right">134,548,072</td>
<td align="right">100.0%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">11,847</td>
<td align="right">0.0%</td>
<td align="right">11,848</td>
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
<td align="right">11,717</td>
<td align="right">100.0%</td>
<td align="right">11,717</td>
<td align="right">100.0%</td>
<td align="right">0.0%</td>
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
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">173,795,102</td>
<td align="right">18.1%</td>
<td align="right">173,799,778</td>
<td align="right">18.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">787,056,868</td>
<td align="right">81.9%</td>
<td align="right">787,076,884</td>
<td align="right">81.9%</td>
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
<td align="left">Failure</td>
<td align="right">61,705</td>
<td align="right">89.6%</td>
<td align="right">61,742</td>
<td align="right">89.6%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">7,145</td>
<td align="right">10.4%</td>
<td align="right">7,148</td>
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
<td align="right">16,085</td>
<td align="right">26.1%</td>
<td align="right">16,122</td>
<td align="right">26.1%</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">async generator send</td>
<td align="right">33,180</td>
<td align="right">53.8%</td>
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
<td align="right">220,010,463</td>
<td align="right">7.2%</td>
<td align="right">166,035,576</td>
<td align="right">6.0%</td>
<td align="right">-24.5%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">293,347,483</td>
<td align="right">9.6%</td>
<td align="right">239,344,436</td>
<td align="right">8.6%</td>
<td align="right">-18.4%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">2,763,101,489</td>
<td align="right">90.3%</td>
<td align="right">2,529,949,878</td>
<td align="right">91.2%</td>
<td align="right">-8.4%</td>
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
<td align="right">4,300,070</td>
<td align="right">96.6%</td>
<td align="right">3,281,734</td>
<td align="right">95.7%</td>
<td align="right">-23.7%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">149,280</td>
<td align="right">3.4%</td>
<td align="right">147,473</td>
<td align="right">4.3%</td>
<td align="right">-1.2%</td>
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
<td align="right">614</td>
<td align="right">0.4%</td>
<td align="right">573</td>
<td align="right">0.4%</td>
<td align="right">-6.7%</td>
</tr>
<tr>
<td align="left">not in keys</td>
<td align="right">8,201</td>
<td align="right">5.5%</td>
<td align="right">7,781</td>
<td align="right">5.3%</td>
<td align="right">-5.1%</td>
</tr>
<tr>
<td align="left">method</td>
<td align="right">1,580</td>
<td align="right">1.1%</td>
<td align="right">1,500</td>
<td align="right">1.0%</td>
<td align="right">-5.1%</td>
</tr>
<tr>
<td align="left">not in dict</td>
<td align="right">16,065</td>
<td align="right">10.8%</td>
<td align="right">15,645</td>
<td align="right">10.6%</td>
<td align="right">-2.6%</td>
</tr>
<tr>
<td align="left">property</td>
<td align="right">5,720</td>
<td align="right">3.8%</td>
<td align="right">5,580</td>
<td align="right">3.8%</td>
<td align="right">-2.4%</td>
</tr>
<tr>
<td align="left">overriding descriptor</td>
<td align="right">10,860</td>
<td align="right">7.3%</td>
<td align="right">10,660</td>
<td align="right">7.2%</td>
<td align="right">-1.8%</td>
</tr>
<tr>
<td align="left">class attr simple</td>
<td align="right">50,038</td>
<td align="right">33.5%</td>
<td align="right">49,630</td>
<td align="right">33.7%</td>
<td align="right">-0.8%</td>
</tr>
<tr>
<td align="left">non string or split</td>
<td align="right">15,520</td>
<td align="right">10.4%</td>
<td align="right">15,440</td>
<td align="right">10.5%</td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">no dict</td>
<td align="right">5,200</td>
<td align="right">3.5%</td>
<td align="right">5,180</td>
<td align="right">3.5%</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">not managed dict</td>
<td align="right">28,510</td>
<td align="right">19.1%</td>
<td align="right">28,512</td>
<td align="right">19.3%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">overridden</td>
<td align="right">6,932</td>
<td align="right">4.6%</td>
<td align="right">6,932</td>
<td align="right">4.7%</td>
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
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">451,671,418</td>
<td align="right">33.8%</td>
<td align="right">70,250,254</td>
<td align="right">22.2%</td>
<td align="right">-84.4%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">886,320,971</td>
<td align="right">66.2%</td>
<td align="right">246,055,909</td>
<td align="right">77.8%</td>
<td align="right">-72.2%</td>
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
<td align="right">164,229</td>
<td align="right">89.8%</td>
<td align="right">66,517</td>
<td align="right">78.1%</td>
<td align="right">-59.5%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">18,706</td>
<td align="right">10.2%</td>
<td align="right">18,706</td>
<td align="right">21.9%</td>
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
<td align="left">array int</td>
<td align="right">66,240</td>
<td align="right">40.3%</td>
<td align="right">6,720</td>
<td align="right">10.1%</td>
<td align="right">-89.9%</td>
</tr>
<tr>
<td align="left">bytearray int</td>
<td align="right">9,720</td>
<td align="right">5.9%</td>
<td align="right">1,340</td>
<td align="right">2.0%</td>
<td align="right">-86.2%</td>
</tr>
<tr>
<td align="left">dict subclass no override</td>
<td align="right">36,664</td>
<td align="right">22.3%</td>
<td align="right">11,853</td>
<td align="right">17.8%</td>
<td align="right">-67.7%</td>
</tr>
<tr>
<td align="left">out of range</td>
<td align="right">3,828</td>
<td align="right">2.3%</td>
<td align="right">2,028</td>
<td align="right">3.0%</td>
<td align="right">-47.0%</td>
</tr>
<tr>
<td align="left">py simple</td>
<td align="right">45,697</td>
<td align="right">27.8%</td>
<td align="right">42,496</td>
<td align="right">63.9%</td>
<td align="right">-7.0%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">2,080</td>
<td align="right">1.3%</td>
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
<td align="right">6,311,174,768</td>
<td align="right">92.1%</td>
<td align="right">3,420,360,892</td>
<td align="right">90.9%</td>
<td align="right">-45.8%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">539,602,240</td>
<td align="right">7.9%</td>
<td align="right">340,137,844</td>
<td align="right">9.0%</td>
<td align="right">-37.0%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">146,218,194</td>
<td align="right">2.1%</td>
<td align="right">104,385,556</td>
<td align="right">2.8%</td>
<td align="right">-28.6%</td>
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
<td align="right">3,043,087</td>
<td align="right">81.0%</td>
<td align="right">2,253,976</td>
<td align="right">78.4%</td>
<td align="right">-25.9%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">712,257</td>
<td align="right">19.0%</td>
<td align="right">621,295</td>
<td align="right">21.6%</td>
<td align="right">-12.8%</td>
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
<td align="left">bytes</td>
<td align="right">33,159</td>
<td align="right">4.7%</td>
<td align="right">18,697</td>
<td align="right">3.0%</td>
<td align="right">-43.6%</td>
</tr>
<tr>
<td align="left">mapping</td>
<td align="right">100,401</td>
<td align="right">14.1%</td>
<td align="right">57,851</td>
<td align="right">9.3%</td>
<td align="right">-42.4%</td>
</tr>
<tr>
<td align="left">dict</td>
<td align="right">40,852</td>
<td align="right">5.7%</td>
<td align="right">31,550</td>
<td align="right">5.1%</td>
<td align="right">-22.8%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">114,358</td>
<td align="right">16.1%</td>
<td align="right">95,121</td>
<td align="right">15.3%</td>
<td align="right">-16.8%</td>
</tr>
<tr>
<td align="left">sequence</td>
<td align="right">20,201</td>
<td align="right">2.8%</td>
<td align="right">18,016</td>
<td align="right">2.9%</td>
<td align="right">-10.8%</td>
</tr>
<tr>
<td align="left">float</td>
<td align="right">2,600</td>
<td align="right">0.4%</td>
<td align="right">2,320</td>
<td align="right">0.4%</td>
<td align="right">-10.8%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">41,018</td>
<td align="right">5.8%</td>
<td align="right">40,251</td>
<td align="right">6.5%</td>
<td align="right">-1.9%</td>
</tr>
<tr>
<td align="left">bytearray</td>
<td align="right">1,252</td>
<td align="right">0.2%</td>
<td align="right">1,239</td>
<td align="right">0.2%</td>
<td align="right">-1.0%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">175,823</td>
<td align="right">24.7%</td>
<td align="right">174,307</td>
<td align="right">28.1%</td>
<td align="right">-0.9%</td>
</tr>
<tr>
<td align="left">number</td>
<td align="right">182,173</td>
<td align="right">25.6%</td>
<td align="right">181,523</td>
<td align="right">29.2%</td>
<td align="right">-0.4%</td>
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
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">2,056,373</td>
<td align="right">0.1%</td>
<td align="right">410,653</td>
<td align="right">0.1%</td>
<td align="right">-80.0%</td>
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
<td align="right">1,060</td>
<td align="right">0.0%</td>
<td align="right">-75.0%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">1,562,314,386</td>
<td align="right">99.9%</td>
<td align="right">466,438,856</td>
<td align="right">99.9%</td>
<td align="right">-70.1%</td>
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
<td align="right">4,402</td>
<td align="right">9.9%</td>
<td align="right">3,517</td>
<td align="right">8.1%</td>
<td align="right">-20.1%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">39,893</td>
<td align="right">90.1%</td>
<td align="right">39,841</td>
<td align="right">91.9%</td>
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
<td align="right">3,261</td>
<td align="right">74.1%</td>
<td align="right">2,496</td>
<td align="right">71.0%</td>
<td align="right">-23.5%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">380</td>
<td align="right">8.6%</td>
<td align="right">340</td>
<td align="right">9.7%</td>
<td align="right">-10.5%</td>
</tr>
<tr>
<td align="left">iterator</td>
<td align="right">761</td>
<td align="right">17.3%</td>
<td align="right">681</td>
<td align="right">19.4%</td>
<td align="right">-10.5%</td>
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
<td align="right">24,505,694,950</td>
<td align="right">10.6%</td>
<td align="right">11,411,174,639</td>
<td align="right">9.6%</td>
<td align="right">-53.4%</td>
</tr>
<tr>
<td align="left">
Specialized hits
<details>
<summary>ⓘ</summary>

Specialized instructions, e.g. `LOAD_ATTR_MODULE` that complete.
</details>
</td>
<td align="right">80,455,033,201</td>
<td align="right">34.7%</td>
<td align="right">41,369,880,675</td>
<td align="right">34.7%</td>
<td align="right">-48.6%</td>
</tr>
<tr>
<td align="left">
Basic
<details>
<summary>ⓘ</summary>

Instructions that are not and cannot be specialized, e.g. `LOAD_FAST`.
</details>
</td>
<td align="right">124,697,084,264</td>
<td align="right">53.9%</td>
<td align="right">65,221,083,047</td>
<td align="right">54.7%</td>
<td align="right">-47.7%</td>
</tr>
<tr>
<td align="left">
Specialized misses
<details>
<summary>ⓘ</summary>

Specialized instructions, e.g. `LOAD_ATTR_MODULE` that deopt.
</details>
</td>
<td align="right">1,890,688,520</td>
<td align="right">0.8%</td>
<td align="right">1,132,761,069</td>
<td align="right">1.0%</td>
<td align="right">-40.1%</td>
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
<td align="left">FOR_ITER</td>
<td align="right">713,541,040</td>
<td align="right">7.4%</td>
<td align="right">120,337,048</td>
<td align="right">2.4%</td>
<td align="right">-83.1%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR</td>
<td align="right">1,534,851,910</td>
<td align="right">16.0%</td>
<td align="right">268,986,701</td>
<td align="right">5.5%</td>
<td align="right">-82.5%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">1,445,379,820</td>
<td align="right">15.0%</td>
<td align="right">618,171,252</td>
<td align="right">12.5%</td>
<td align="right">-57.2%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">226,444,233</td>
<td align="right">2.4%</td>
<td align="right">107,271,686</td>
<td align="right">2.2%</td>
<td align="right">-52.6%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">2,498,099,539</td>
<td align="right">26.0%</td>
<td align="right">1,370,379,838</td>
<td align="right">27.8%</td>
<td align="right">-45.1%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">247,569,957</td>
<td align="right">2.6%</td>
<td align="right">145,320,409</td>
<td align="right">2.9%</td>
<td align="right">-41.3%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">539,602,240</td>
<td align="right">5.6%</td>
<td align="right">340,137,844</td>
<td align="right">6.9%</td>
<td align="right">-37.0%</td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">293,347,483</td>
<td align="right">3.0%</td>
<td align="right">239,344,436</td>
<td align="right">4.9%</td>
<td align="right">-18.4%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">1,475,408,638</td>
<td align="right">15.3%</td>
<td align="right">1,454,606,896</td>
<td align="right">29.5%</td>
<td align="right">-1.4%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR</td>
<td align="right">451,671,418</td>
<td align="right">4.7%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">SEND</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">173,799,778</td>
<td align="right">3.5%</td>
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
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">370,121,948</td>
<td align="right">19.6%</td>
<td align="right">155,848,797</td>
<td align="right">13.8%</td>
<td align="right">-57.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">380,276,139</td>
<td align="right">20.1%</td>
<td align="right">178,839,326</td>
<td align="right">15.8%</td>
<td align="right">-53.0%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">121,067,131</td>
<td align="right">6.4%</td>
<td align="right">70,593,748</td>
<td align="right">6.2%</td>
<td align="right">-41.7%</td>
</tr>
<tr>
<td align="left">TO_BOOL_ALWAYS_TRUE</td>
<td align="right">68,819,226</td>
<td align="right">3.6%</td>
<td align="right">47,518,721</td>
<td align="right">4.2%</td>
<td align="right">-31.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL_NONE</td>
<td align="right">68,532,716</td>
<td align="right">3.6%</td>
<td align="right">48,974,124</td>
<td align="right">4.3%</td>
<td align="right">-28.5%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">137,099,728</td>
<td align="right">7.3%</td>
<td align="right">128,093,291</td>
<td align="right">11.3%</td>
<td align="right">-6.6%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">115,534,067</td>
<td align="right">6.1%</td>
<td align="right">109,136,743</td>
<td align="right">9.6%</td>
<td align="right">-5.5%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_SLOT</td>
<td align="right">98,884,513</td>
<td align="right">5.2%</td>
<td align="right">95,389,063</td>
<td align="right">8.4%</td>
<td align="right">-3.5%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">87,927,346</td>
<td align="right">4.7%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">FOR_ITER_TUPLE</td>
<td align="right">87,526,560</td>
<td align="right">4.6%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">59,461,077</td>
<td align="right">5.2%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">42,411,145</td>
<td align="right">3.7%</td>
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
<td align="left">Calls via PyEval_EvalFrame (legacy)</td>
<td align="right">5,298,564</td>
<td align="right">0.1%</td>
<td align="right">2,658,324</td>
<td align="right">0.0%</td>
<td align="right">-49.8%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (slot)</td>
<td align="right">343,025,096</td>
<td align="right">3.9%</td>
<td align="right">479,270,080</td>
<td align="right">5.5%</td>
<td align="right">39.7%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (function vectorcall)</td>
<td align="right">1,297,125,595</td>
<td align="right">14.8%</td>
<td align="right">1,444,837,639</td>
<td align="right">16.6%</td>
<td align="right">11.4%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (vector)</td>
<td align="right">1,302,454,905</td>
<td align="right">14.8%</td>
<td align="right">1,447,526,709</td>
<td align="right">16.6%</td>
<td align="right">11.1%</td>
</tr>
<tr>
<td align="left">Calls to PyEval_EvalDefault</td>
<td align="right">2,169,600,932</td>
<td align="right">24.7%</td>
<td align="right">2,309,660,883</td>
<td align="right">26.6%</td>
<td align="right">6.5%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (total)</td>
<td align="right">2,169,600,932</td>
<td align="right">24.7%</td>
<td align="right">2,309,660,883</td>
<td align="right">26.6%</td>
<td align="right">6.5%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (api)</td>
<td align="right">242,868,742</td>
<td align="right">2.8%</td>
<td align="right">254,648,983</td>
<td align="right">2.9%</td>
<td align="right">4.9%</td>
</tr>
<tr>
<td align="left">Calls to Python functions inlined</td>
<td align="right">6,619,035,736</td>
<td align="right">75.3%</td>
<td align="right">6,389,074,991</td>
<td align="right">73.4%</td>
<td align="right">-3.5%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (generator)</td>
<td align="right">867,146,027</td>
<td align="right">9.9%</td>
<td align="right">862,134,174</td>
<td align="right">9.9%</td>
<td align="right">-0.6%</td>
</tr>
<tr>
<td align="left">Frames pushed</td>
<td align="right">6,993,165,062</td>
<td align="right">79.6%</td>
<td align="right">6,954,144,127</td>
<td align="right">79.9%</td>
<td align="right">-0.6%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (function ex)</td>
<td align="right">38,307,968</td>
<td align="right">0.4%</td>
<td align="right">38,349,537</td>
<td align="right">0.4%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">Frame objects created</td>
<td align="right">88,437,817</td>
<td align="right">1.0%</td>
<td align="right">88,452,198</td>
<td align="right">1.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (method)</td>
<td align="right">213,093,638</td>
<td align="right">2.4%</td>
<td align="right">213,127,787</td>
<td align="right">2.5%</td>
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
<td align="right">9,880,659</td>
<td align="right"></td>
<td align="right">10,640,200</td>
<td align="right"></td>
<td align="right">7.7%</td>
</tr>
<tr>
<td align="left">Interpreter increfs</td>
<td align="right">89,251,088,431</td>
<td align="right">76.9%</td>
<td align="right">93,349,555,966</td>
<td align="right">77.3%</td>
<td align="right">4.6%</td>
</tr>
<tr>
<td align="left">Interpreter decrefs</td>
<td align="right">103,739,377,526</td>
<td align="right">77.6%</td>
<td align="right">108,035,390,410</td>
<td align="right">78.1%</td>
<td align="right">4.1%</td>
</tr>
<tr>
<td align="left">Method cache dunder hits</td>
<td align="right">3,432,033,572</td>
<td align="right"></td>
<td align="right">3,560,731,224</td>
<td align="right"></td>
<td align="right">3.7%</td>
</tr>
<tr>
<td align="left">Increfs</td>
<td align="right">26,762,039,373</td>
<td align="right">23.1%</td>
<td align="right">27,416,745,093</td>
<td align="right">22.7%</td>
<td align="right">2.4%</td>
</tr>
<tr>
<td align="left">Method cache collisions</td>
<td align="right">79,743,150</td>
<td align="right"></td>
<td align="right">80,968,233</td>
<td align="right"></td>
<td align="right">1.5%</td>
</tr>
<tr>
<td align="left">Decrefs</td>
<td align="right">29,869,382,896</td>
<td align="right">22.4%</td>
<td align="right">30,281,145,718</td>
<td align="right">21.9%</td>
<td align="right">1.4%</td>
</tr>
<tr>
<td align="left">Method cache misses</td>
<td align="right">77,640,359</td>
<td align="right"></td>
<td align="right">78,108,664</td>
<td align="right"></td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">Method cache hits</td>
<td align="right">3,120,202,429</td>
<td align="right"></td>
<td align="right">3,102,756,031</td>
<td align="right"></td>
<td align="right">-0.6%</td>
</tr>
<tr>
<td align="left">Frees</td>
<td align="right">12,147,269,754</td>
<td align="right"></td>
<td align="right">12,095,382,284</td>
<td align="right"></td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">Allocations to 512 bytes</td>
<td align="right">11,671,886,055</td>
<td align="right">62.5%</td>
<td align="right">11,624,358,681</td>
<td align="right">62.4%</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">Allocations</td>
<td align="right">11,798,002,516</td>
<td align="right">63.2%</td>
<td align="right">11,750,439,598</td>
<td align="right">63.1%</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">Allocations from freelist</td>
<td align="right">6,878,865,809</td>
<td align="right">36.8%</td>
<td align="right">6,866,068,891</td>
<td align="right">36.9%</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">Frees to freelist</td>
<td align="right">6,880,853,817</td>
<td align="right"></td>
<td align="right">6,868,064,332</td>
<td align="right"></td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">Inline values</td>
<td align="right">182,902,185</td>
<td align="right"></td>
<td align="right">182,610,418</td>
<td align="right"></td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">Allocations to 4 kbytes</td>
<td align="right">104,948,306</td>
<td align="right">0.6%</td>
<td align="right">104,914,396</td>
<td align="right">0.6%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">Allocations over 4 kbytes</td>
<td align="right">21,168,155</td>
<td align="right">0.1%</td>
<td align="right">21,166,521</td>
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
<td align="right">116,176,681</td>
<td align="right">17,128,394,267</td>
<td align="right">0</td>
<td align="right">115,740,535</td>
<td align="right">17,106,513,389</td>
</tr>
<tr>
<td align="right">2</td>
<td align="right">0</td>
<td align="right">10,755,840</td>
<td align="right">6,957,362,370</td>
<td align="right">0</td>
<td align="right">10,755,840</td>
<td align="right">6,969,719,610</td>
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
<td align="right">735,297</td>
<td align="right"></td>
<td align="right">735,297 / 0 !!</td>
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
<td align="right">142,245</td>
<td align="right">19.3%</td>
<td align="right">142,245 / 0 !!</td>
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
<td align="right">1,085</td>
<td align="right">0.1%</td>
<td align="right">1,085 / 0 !!</td>
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
<td align="right">148,138</td>
<td align="right">20.1%</td>
<td align="right">148,138 / 0 !!</td>
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
<td align="right">0.0%</td>
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
<td align="right">593,052</td>
<td align="right">80.7%</td>
<td align="right">593,052 / 0 !!</td>
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
<td align="right">18,909</td>
<td align="right">2.6%</td>
<td align="right">18,909 / 0 !!</td>
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
<td align="right">2,353</td>
<td align="right">0.3%</td>
<td align="right">2,353 / 0 !!</td>
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
<td align="right">8,405</td>
<td align="right">1.1%</td>
<td align="right">8,405 / 0 !!</td>
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
<td align="right">5,640</td>
<td align="right">4.0%</td>
<td align="right">5,640 / 0 !!</td>
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
<td align="right">7,126,013,243</td>
<td align="right"></td>
<td align="right">7,126,013,243 / 0 !!</td>
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
<td align="right">192,413,997,463</td>
<td align="right">2,700.2%</td>
<td align="right">192,413,997,463 / 0 !!</td>
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
<td align="right">142,245</td>
<td align="right"></td>
<td align="right">142,245 / 0 !!</td>
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
<td align="right">140,065</td>
<td align="right">98.5%</td>
<td align="right">140,065 / 0 !!</td>
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
<td align="right"></td>
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
<td align="right">0</td>
<td align="right"></td>
<td align="right">2,120</td>
<td align="right">1.5%</td>
<td align="right">2,120 / 0 !!</td>
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
<td align="right">0.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 2</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 4</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 8</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">8,128</td>
<td align="right">5.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 16</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">22,647</td>
<td align="right">15.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 32</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">53,749</td>
<td align="right">37.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 64</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">32,067</td>
<td align="right">22.5%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 128</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">18,287</td>
<td align="right">12.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 256</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">6,018</td>
<td align="right">4.2%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 512</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">1,349</td>
<td align="right">0.9%</td>
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
<td align="right">0.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 2</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 4</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">848</td>
<td align="right">0.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 8</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">15,787</td>
<td align="right">11.1%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 16</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">43,357</td>
<td align="right">30.5%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 32</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">45,712</td>
<td align="right">32.1%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 64</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">22,433</td>
<td align="right">15.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 128</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">9,215</td>
<td align="right">6.5%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 256</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">2,573</td>
<td align="right">1.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 512</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">140</td>
<td align="right">0.1%</td>
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
<td align="right">0.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 2</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">25,847,900</td>
<td align="right">0.4%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 4</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">999,628,110</td>
<td align="right">14.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 8</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">732,903,231</td>
<td align="right">10.3%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 16</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">1,308,465,699</td>
<td align="right">18.4%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 32</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">1,032,713,798</td>
<td align="right">14.5%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 64</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">617,889,929</td>
<td align="right">8.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 128</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">316,788,783</td>
<td align="right">4.4%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 256</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">188,377,465</td>
<td align="right">2.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 512</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">23,679,597</td>
<td align="right">0.3%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 1,024</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">7,729,528</td>
<td align="right">0.1%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 2,048</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">18,403,079</td>
<td align="right">0.3%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 4,096</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">611,444</td>
<td align="right">0.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 8,192</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">747,331</td>
<td align="right">0.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 16,384</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">237,561</td>
<td align="right">0.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 32,768</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">43,860</td>
<td align="right">0.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 65,536</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">13,224</td>
<td align="right">0.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 131,072</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">776</td>
<td align="right">0.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 262,144</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">2,080</td>
<td align="right">0.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 524,288</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">461</td>
<td align="right">0.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 1,048,576</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">400</td>
<td align="right">0.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 2,097,152</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">301</td>
<td align="right">0.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 4,194,304</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">179</td>
<td align="right">0.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 8,388,608</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">240</td>
<td align="right">0.0%</td>
<td align="right"></td>
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
<td align="left">_SET_IP</td>
<td align="right"></td>
<td align="right">14,834,627,489</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_VALIDITY</td>
<td align="right"></td>
<td align="right">12,167,526,228</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_CONST_INLINE_BORROW</td>
<td align="right"></td>
<td align="right">9,504,041,260</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_FAST_1</td>
<td align="right"></td>
<td align="right">6,667,986,410</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_FAST</td>
<td align="right"></td>
<td align="right">6,132,643,285</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_TYPE_VERSION</td>
<td align="right"></td>
<td align="right">5,925,364,305</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_FAST_0</td>
<td align="right"></td>
<td align="right">5,754,677,102</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_IS_FALSE_POP</td>
<td align="right"></td>
<td align="right">5,638,129,164</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_START_EXECUTOR</td>
<td align="right"></td>
<td align="right">5,435,733,791</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_SIDE_EXIT</td>
<td align="right"></td>
<td align="right">4,138,002,629</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_FAST_3</td>
<td align="right"></td>
<td align="right">3,541,099,425</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_FAST</td>
<td align="right"></td>
<td align="right">3,450,617,605</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_FAST_7</td>
<td align="right"></td>
<td align="right">3,401,608,934</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_FAST_2</td>
<td align="right"></td>
<td align="right">3,127,671,199</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_IS_TRUE_POP</td>
<td align="right"></td>
<td align="right">2,664,345,759</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_EXIT_TRACE</td>
<td align="right"></td>
<td align="right">2,598,696,893</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_PERIODIC</td>
<td align="right"></td>
<td align="right">2,580,752,421</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_OP_ADD_INT</td>
<td align="right"></td>
<td align="right">2,524,266,645</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_FAST_5</td>
<td align="right"></td>
<td align="right">2,474,104,469</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_NOS_INT</td>
<td align="right"></td>
<td align="right">2,429,394,074</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_FAST_4</td>
<td align="right"></td>
<td align="right">2,330,138,993</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_JUMP_TO_TOP</td>
<td align="right"></td>
<td align="right">2,293,788,236</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_TO_BOOL_BOOL</td>
<td align="right"></td>
<td align="right">2,234,295,986</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_CONST_INLINE_WITH_NULL</td>
<td align="right"></td>
<td align="right">2,030,228,234</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_MANAGED_OBJECT_HAS_VALUES</td>
<td align="right"></td>
<td align="right">2,025,999,809</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_INSTANCE_VALUE_0</td>
<td align="right"></td>
<td align="right">2,022,082,650</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_FAST_1</td>
<td align="right"></td>
<td align="right">2,003,916,153</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_PUSH_FRAME</td>
<td align="right"></td>
<td align="right">1,933,805,297</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION_EXACT_ARGS</td>
<td align="right"></td>
<td align="right">1,892,460,848</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_COMPARE_OP_STR</td>
<td align="right"></td>
<td align="right">1,833,468,912</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_SAVE_RETURN_OFFSET</td>
<td align="right"></td>
<td align="right">1,826,876,856</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_FOR_ITER_TIER_TWO</td>
<td align="right"></td>
<td align="right">1,750,363,065</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_COLD_EXIT</td>
<td align="right"></td>
<td align="right">1,690,279,452</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CONTAINS_OP_SET</td>
<td align="right"></td>
<td align="right">1,600,210,444</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_RESUME_CHECK</td>
<td align="right"></td>
<td align="right">1,559,747,644</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_CONST_INLINE</td>
<td align="right"></td>
<td align="right">1,466,409,843</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_ITER_CHECK_LIST</td>
<td align="right"></td>
<td align="right">1,424,560,373</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_SUBSCR</td>
<td align="right"></td>
<td align="right">1,399,345,481</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_NOT_EXHAUSTED_LIST</td>
<td align="right"></td>
<td align="right">1,368,442,270</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_COPY</td>
<td align="right"></td>
<td align="right">1,325,537,045</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_DORV_VALUES_INST_ATTR_FROM_DICT</td>
<td align="right"></td>
<td align="right">1,304,332,808</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION</td>
<td align="right"></td>
<td align="right">1,302,416,055</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_FAST_6</td>
<td align="right"></td>
<td align="right">1,275,454,378</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_KEYS_VERSION</td>
<td align="right"></td>
<td align="right">1,255,460,837</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_FAST_7</td>
<td align="right"></td>
<td align="right">1,220,329,327</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_SUBSCR_STR_INT</td>
<td align="right"></td>
<td align="right">1,216,189,041</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_OP_MULTIPLY_FLOAT</td>
<td align="right"></td>
<td align="right">1,188,304,420</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right"></td>
<td align="right">1,154,510,000</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_SWAP</td>
<td align="right"></td>
<td align="right">1,153,964,817</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_VALIDITY_AND_SET_IP</td>
<td align="right"></td>
<td align="right">1,147,641,963</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_DEOPT</td>
<td align="right"></td>
<td align="right">1,135,496,588</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR</td>
<td align="right"></td>
<td align="right">1,133,090,033</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_ITER_NEXT_LIST</td>
<td align="right"></td>
<td align="right">1,101,045,084</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_SUBSCR_LIST_INT</td>
<td align="right"></td>
<td align="right">1,100,615,130</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_FAST</td>
<td align="right"></td>
<td align="right">1,025,890,719</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_BOTH_UNICODE</td>
<td align="right"></td>
<td align="right">975,211,591</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_COMPARE_OP_INT</td>
<td align="right"></td>
<td align="right">966,183,488</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_STACK_SPACE_OPERAND</td>
<td align="right"></td>
<td align="right">959,118,829</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_BOTH_FLOAT</td>
<td align="right"></td>
<td align="right">948,376,824</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_OP</td>
<td align="right"></td>
<td align="right">877,971,757</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right"></td>
<td align="right">863,828,365</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_PUSH_NULL</td>
<td align="right"></td>
<td align="right">836,103,577</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_POP_TOP</td>
<td align="right"></td>
<td align="right">826,751,805</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_FAST_2</td>
<td align="right"></td>
<td align="right">822,570,058</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_POP_FRAME</td>
<td align="right"></td>
<td align="right">811,649,773</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_FAST_5</td>
<td align="right"></td>
<td align="right">791,820,172</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_FAST_3</td>
<td align="right"></td>
<td align="right">761,677,638</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_FAST_4</td>
<td align="right"></td>
<td align="right">750,233,966</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_O</td>
<td align="right"></td>
<td align="right">735,624,403</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_ITER_CHECK_RANGE</td>
<td align="right"></td>
<td align="right">724,380,368</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_NOT_EXHAUSTED_RANGE</td>
<td align="right"></td>
<td align="right">723,843,048</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_SLOT_0</td>
<td align="right"></td>
<td align="right">722,763,763</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right"></td>
<td align="right">705,078,103</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_ITER_NEXT_RANGE</td>
<td align="right"></td>
<td align="right">680,648,383</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_DEREF</td>
<td align="right"></td>
<td align="right">660,743,764</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_NOS_FLOAT</td>
<td align="right"></td>
<td align="right">645,018,882</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_4</td>
<td align="right"></td>
<td align="right">624,689,663</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_1</td>
<td align="right"></td>
<td align="right">602,291,411</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_OP_ADD_FLOAT</td>
<td align="right"></td>
<td align="right">586,586,180</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_BOTH_INT</td>
<td align="right"></td>
<td align="right">585,151,243</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_FAST_6</td>
<td align="right"></td>
<td align="right">548,906,018</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_CONST_INLINE_BORROW_WITH_NULL</td>
<td align="right"></td>
<td align="right">504,887,819</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_SUBSCR_LIST_INT</td>
<td align="right"></td>
<td align="right">490,249,262</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBTRACT_INT</td>
<td align="right"></td>
<td align="right">464,007,105</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BUILD_TUPLE</td>
<td align="right"></td>
<td align="right">453,491,886</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CONTAINS_OP_DICT</td>
<td align="right"></td>
<td align="right">425,167,076</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_0</td>
<td align="right"></td>
<td align="right">419,777,464</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_SUBSCR_DICT</td>
<td align="right"></td>
<td align="right">416,049,474</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_ISINSTANCE</td>
<td align="right"></td>
<td align="right">387,328,069</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBTRACT_FLOAT</td>
<td align="right"></td>
<td align="right">383,046,880</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_SUBSCR</td>
<td align="right"></td>
<td align="right">381,420,009</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_ITER_CHECK_TUPLE</td>
<td align="right"></td>
<td align="right">362,562,463</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_IS_OP</td>
<td align="right"></td>
<td align="right">357,938,501</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_TYPE_1</td>
<td align="right"></td>
<td align="right">332,471,020</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_NOT_EXHAUSTED_TUPLE</td>
<td align="right"></td>
<td align="right">310,323,318</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GET_ITER</td>
<td align="right"></td>
<td align="right">293,864,461</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_UNPACK_SEQUENCE_TUPLE</td>
<td align="right"></td>
<td align="right">292,662,930</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BUILD_LIST</td>
<td align="right"></td>
<td align="right">255,679,889</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_TO_BOOL</td>
<td align="right"></td>
<td align="right">241,423,982</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right"></td>
<td align="right">232,894,744</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_TOS_INT</td>
<td align="right"></td>
<td align="right">226,765,957</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_LEN</td>
<td align="right"></td>
<td align="right">212,387,554</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_FAST_0</td>
<td align="right"></td>
<td align="right">208,510,875</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_ITER_NEXT_TUPLE</td>
<td align="right"></td>
<td align="right">204,450,129</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LIST_APPEND</td>
<td align="right"></td>
<td align="right">203,924,838</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_TO_BOOL_INT</td>
<td align="right"></td>
<td align="right">198,145,340</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right"></td>
<td align="right">190,045,446</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_OP_MULTIPLY_INT</td>
<td align="right"></td>
<td align="right">185,789,160</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_GLOBAL</td>
<td align="right"></td>
<td align="right">184,938,295</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_STACK_SPACE</td>
<td align="right"></td>
<td align="right">181,114,719</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_TO_BOOL_NONE</td>
<td align="right"></td>
<td align="right">173,809,362</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_SUBSCR_TUPLE_INT</td>
<td align="right"></td>
<td align="right">163,903,793</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_DYNAMIC_EXIT</td>
<td align="right"></td>
<td align="right">161,648,815</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_IS_NOT_NONE_POP</td>
<td align="right"></td>
<td align="right">159,499,493</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_FAST_WITH_KEYWORDS</td>
<td align="right"></td>
<td align="right">156,717,412</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_SLICE</td>
<td align="right"></td>
<td align="right">149,868,340</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_SUBSCR_DICT</td>
<td align="right"></td>
<td align="right">145,417,743</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BUILD_SLICE</td>
<td align="right"></td>
<td align="right">139,781,460</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GET_ANEXT</td>
<td align="right"></td>
<td align="right">125,514,720</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_ATTR_SLOT</td>
<td align="right"></td>
<td align="right">123,206,167</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_SLICE</td>
<td align="right"></td>
<td align="right">121,385,203</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CONTAINS_OP</td>
<td align="right"></td>
<td align="right">118,720,413</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_2</td>
<td align="right"></td>
<td align="right">108,997,370</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_ATTR_WITH_HINT</td>
<td align="right"></td>
<td align="right">108,606,246</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_WITH_HINT</td>
<td align="right"></td>
<td align="right">108,479,565</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_GLOBALS_VERSION</td>
<td align="right"></td>
<td align="right">107,555,345</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_FOR_ITER_GEN_FRAME</td>
<td align="right"></td>
<td align="right">107,033,061</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_DORV_NO_DICT</td>
<td align="right"></td>
<td align="right">105,368,089</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_ATTR_METHOD_LAZY_DICT</td>
<td align="right"></td>
<td align="right">104,225,446</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_METHOD_LAZY_DICT</td>
<td align="right"></td>
<td align="right">104,225,446</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_ATTR_INSTANCE_VALUE</td>
<td align="right"></td>
<td align="right">104,018,869</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_COMPARE_OP_FLOAT</td>
<td align="right"></td>
<td align="right">101,251,466</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_COMPARE_OP</td>
<td align="right"></td>
<td align="right">100,160,343</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LIST_EXTEND</td>
<td align="right"></td>
<td align="right">98,358,589</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_INTRINSIC_1</td>
<td align="right"></td>
<td align="right">97,434,789</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_MAKE_FUNCTION</td>
<td align="right"></td>
<td align="right">93,549,728</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right"></td>
<td align="right">91,721,607</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_RETURN_GENERATOR</td>
<td align="right"></td>
<td align="right">91,072,390</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_FAST_WITH_KEYWORDS</td>
<td align="right"></td>
<td align="right">90,626,997</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_COPY_FREE_VARS</td>
<td align="right"></td>
<td align="right">81,244,351</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_UNPACK_SEQUENCE_LIST</td>
<td align="right"></td>
<td align="right">80,800,669</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_SET_FUNCTION_ATTRIBUTE</td>
<td align="right"></td>
<td align="right">78,530,768</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right"></td>
<td align="right">77,770,233</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_INIT_CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right"></td>
<td align="right">77,703,233</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_STR_1</td>
<td align="right"></td>
<td align="right">67,904,176</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_TOS_FLOAT</td>
<td align="right"></td>
<td align="right">65,543,560</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_UNARY_NOT</td>
<td align="right"></td>
<td align="right">62,242,737</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_3</td>
<td align="right"></td>
<td align="right">61,056,719</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_CLASS</td>
<td align="right"></td>
<td align="right">60,889,895</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_GLOBAL_MODULE</td>
<td align="right"></td>
<td align="right">55,179,721</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_TO_BOOL_LIST</td>
<td align="right"></td>
<td align="right">54,729,420</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_GLOBAL_BUILTINS</td>
<td align="right"></td>
<td align="right">52,375,624</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_FORMAT_SIMPLE</td>
<td align="right"></td>
<td align="right">52,353,985</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CONVERT_VALUE</td>
<td align="right"></td>
<td align="right">51,694,900</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_ATTR</td>
<td align="right"></td>
<td align="right">50,774,848</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_BUILTINS_VERSION</td>
<td align="right"></td>
<td align="right">45,826,584</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_IS_NONE_POP</td>
<td align="right"></td>
<td align="right">41,994,053</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_REPLACE_WITH_TRUE</td>
<td align="right"></td>
<td align="right">32,624,600</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_TO_BOOL_STR</td>
<td align="right"></td>
<td align="right">27,829,281</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_ATTR_CLASS</td>
<td align="right"></td>
<td align="right">26,736,946</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BUILD_STRING</td>
<td align="right"></td>
<td align="right">25,514,804</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_UNARY_NEGATIVE</td>
<td align="right"></td>
<td align="right">25,147,720</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_OP_ADD_UNICODE</td>
<td align="right"></td>
<td align="right">25,000,310</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_CLASS_0</td>
<td align="right"></td>
<td align="right">24,834,278</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_O</td>
<td align="right"></td>
<td align="right">24,434,582</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_NONDESCRIPTOR_NO_DICT</td>
<td align="right"></td>
<td align="right">22,756,350</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_MAP_ADD</td>
<td align="right"></td>
<td align="right">21,327,265</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BUILD_MAP</td>
<td align="right"></td>
<td align="right">16,806,048</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_FAST_AND_CLEAR</td>
<td align="right"></td>
<td align="right">16,474,143</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_UNARY_INVERT</td>
<td align="right"></td>
<td align="right">13,004,140</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_DICT_MERGE</td>
<td align="right"></td>
<td align="right">11,664,341</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS</td>
<td align="right"></td>
<td align="right">10,064,229</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_ATTR_MODULE</td>
<td align="right"></td>
<td align="right">7,589,080</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_MODULE</td>
<td align="right"></td>
<td align="right">7,589,080</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_TUPLE_1</td>
<td align="right"></td>
<td align="right">7,455,000</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_MAKE_CELL</td>
<td align="right"></td>
<td align="right">6,824,672</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_DEREF</td>
<td align="right"></td>
<td align="right">3,878,811</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_INSTANCE_VALUE_1</td>
<td align="right"></td>
<td align="right">3,802,299</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BUILD_CONST_KEY_MAP</td>
<td align="right"></td>
<td align="right">2,484,290</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_SLOT_1</td>
<td align="right"></td>
<td align="right">2,396,080</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_SET_ADD</td>
<td align="right"></td>
<td align="right">2,174,721</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_UNPACK_SEQUENCE</td>
<td align="right"></td>
<td align="right">1,642,466</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_DELETE_SUBSCR</td>
<td align="right"></td>
<td align="right">1,629,645</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_POP_TOP_LOAD_CONST_INLINE_BORROW</td>
<td align="right"></td>
<td align="right">1,398,926</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_GLOBAL</td>
<td align="right"></td>
<td align="right">1,275,340</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GET_AWAITABLE</td>
<td align="right"></td>
<td align="right">653,795</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_ERROR_POP_N</td>
<td align="right"></td>
<td align="right">585,759</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_NAME</td>
<td align="right"></td>
<td align="right">545,860</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_FAST_CHECK</td>
<td align="right"></td>
<td align="right">251,804</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GET_YIELD_FROM_ITER</td>
<td align="right"></td>
<td align="right">197,536</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_SUPER_ATTR_METHOD</td>
<td align="right"></td>
<td align="right">95,960</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_CLASS_1</td>
<td align="right"></td>
<td align="right">3,840</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_UNPACK_EX</td>
<td align="right"></td>
<td align="right">104</td>
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
<td align="left">CALL</td>
<td align="right"></td>
<td align="right">172,872</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">YIELD_VALUE</td>
<td align="right"></td>
<td align="right">140,287</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right"></td>
<td align="right">84,346</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">SEND</td>
<td align="right"></td>
<td align="right">31,711</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_KW</td>
<td align="right"></td>
<td align="right">29,583</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_PY_WITH_DEFAULTS</td>
<td align="right"></td>
<td align="right">11,642</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_ATTR_PROPERTY</td>
<td align="right"></td>
<td align="right">8,008</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_LIST_APPEND</td>
<td align="right"></td>
<td align="right">7,607</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_FUNCTION_EX</td>
<td align="right"></td>
<td align="right">6,000</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_GETITEM</td>
<td align="right"></td>
<td align="right">3,240</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_ALLOC_AND_ENTER_INIT</td>
<td align="right"></td>
<td align="right">1,911</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_NAME</td>
<td align="right"></td>
<td align="right">1,360</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BINARY_OP_INPLACE_ADD_UNICODE</td>
<td align="right"></td>
<td align="right">703</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BUILD_SET</td>
<td align="right"></td>
<td align="right">525</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">IMPORT_NAME</td>
<td align="right"></td>
<td align="right">409</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">SEND_GEN</td>
<td align="right"></td>
<td align="right">260</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BEFORE_WITH</td>
<td align="right"></td>
<td align="right">240</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">STORE_ATTR_WITH_HINT</td>
<td align="right"></td>
<td align="right">240</td>
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
<td align="right">0</td>
<td align="right">1,120</td>
<td align="right">1,120 / 0 !!</td>
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
<td align="right">1,120</td>
<td align="right">1,120 / 0 !!</td>
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
Stats gathered on: 2024-04-28
