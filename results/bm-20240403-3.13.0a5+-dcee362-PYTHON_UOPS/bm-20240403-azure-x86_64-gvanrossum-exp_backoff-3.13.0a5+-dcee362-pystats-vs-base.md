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
<td align="left">BINARY_OP_MULTIPLY_FLOAT</td>
<td align="right">137,015,917</td>
<td align="right">210,122,434</td>
<td align="right">53.4%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_FLOAT</td>
<td align="right">58,476,422</td>
<td align="right">87,792,844</td>
<td align="right">50.1%</td>
</tr>
<tr>
<td align="left">FORMAT_WITH_SPEC</td>
<td align="right">1,320</td>
<td align="right">1,760</td>
<td align="right">33.3%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_FLOAT</td>
<td align="right">59,462,312</td>
<td align="right">77,484,235</td>
<td align="right">30.3%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">1,512,244,095</td>
<td align="right">1,148,180,491</td>
<td align="right">-24.1%</td>
</tr>
<tr>
<td align="left">UNARY_NEGATIVE</td>
<td align="right">122,295,999</td>
<td align="right">146,012,217</td>
<td align="right">19.4%</td>
</tr>
<tr>
<td align="left">CALL_TYPE_1</td>
<td align="right">289,372,787</td>
<td align="right">241,466,566</td>
<td align="right">-16.6%</td>
</tr>
<tr>
<td align="left">FOR_ITER_TUPLE</td>
<td align="right">348,911,791</td>
<td align="right">300,761,660</td>
<td align="right">-13.8%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP_SET</td>
<td align="right">516,432,098</td>
<td align="right">462,233,419</td>
<td align="right">-10.5%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST</td>
<td align="right">570,800,806</td>
<td align="right">522,944,688</td>
<td align="right">-8.4%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">140,722,500</td>
<td align="right">152,051,737</td>
<td align="right">8.1%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">3,120,835,268</td>
<td align="right">2,893,867,676</td>
<td align="right">-7.3%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TUPLE</td>
<td align="right">331,968,615</td>
<td align="right">308,023,098</td>
<td align="right">-7.2%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_LIST_INT</td>
<td align="right">426,387,331</td>
<td align="right">453,543,175</td>
<td align="right">6.4%</td>
</tr>
<tr>
<td align="left">BINARY_OP_INPLACE_ADD_UNICODE</td>
<td align="right">5,917,877</td>
<td align="right">6,288,208</td>
<td align="right">6.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">3,971,002,092</td>
<td align="right">4,179,043,817</td>
<td align="right">5.2%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">3,075,173,698</td>
<td align="right">2,960,374,809</td>
<td align="right">-3.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">1,780,476,284</td>
<td align="right">1,716,538,309</td>
<td align="right">-3.6%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_O</td>
<td align="right">670,744,411</td>
<td align="right">646,755,067</td>
<td align="right">-3.6%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_CLASS</td>
<td align="right">166,157,698</td>
<td align="right">161,457,279</td>
<td align="right">-2.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">5,538,926,695</td>
<td align="right">5,392,985,098</td>
<td align="right">-2.6%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">107,288,074</td>
<td align="right">110,076,172</td>
<td align="right">2.6%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">2,822,423,637</td>
<td align="right">2,749,234,682</td>
<td align="right">-2.6%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">2,914,227,320</td>
<td align="right">2,840,860,848</td>
<td align="right">-2.5%</td>
</tr>
<tr>
<td align="left">BINARY_OP_MULTIPLY_INT</td>
<td align="right">161,283,139</td>
<td align="right">164,921,385</td>
<td align="right">2.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_NO_DICT</td>
<td align="right">68,612,104</td>
<td align="right">67,113,443</td>
<td align="right">-2.2%</td>
</tr>
<tr>
<td align="left">CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">191,288,853</td>
<td align="right">195,033,427</td>
<td align="right">2.0%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST_WITH_KEYWORDS</td>
<td align="right">27,907,727</td>
<td align="right">28,443,502</td>
<td align="right">1.9%</td>
</tr>
<tr>
<td align="left">PUSH_NULL</td>
<td align="right">1,230,759,017</td>
<td align="right">1,207,276,608</td>
<td align="right">-1.9%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">6,749,594,305</td>
<td align="right">6,645,114,025</td>
<td align="right">-1.5%</td>
</tr>
<tr>
<td align="left">LIST_APPEND</td>
<td align="right">75,548,770</td>
<td align="right">74,410,724</td>
<td align="right">-1.5%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_STR_INT</td>
<td align="right">462,878,176</td>
<td align="right">456,861,927</td>
<td align="right">-1.3%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_GETITEM</td>
<td align="right">61,614,110</td>
<td align="right">62,395,995</td>
<td align="right">1.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">24,566,136,017</td>
<td align="right">24,300,016,213</td>
<td align="right">-1.1%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">112,381,607</td>
<td align="right">113,586,555</td>
<td align="right">1.1%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_STR</td>
<td align="right">326,425,982</td>
<td align="right">329,863,831</td>
<td align="right">1.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_PROPERTY</td>
<td align="right">78,797,604</td>
<td align="right">79,604,319</td>
<td align="right">1.0%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">6,900,824,113</td>
<td align="right">6,832,198,440</td>
<td align="right">-1.0%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NONE</td>
<td align="right">390,311,773</td>
<td align="right">394,176,675</td>
<td align="right">1.0%</td>
</tr>
<tr>
<td align="left">SET_ADD</td>
<td align="right">957,782</td>
<td align="right">966,838</td>
<td align="right">0.9%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">3,539,510,870</td>
<td align="right">3,507,499,847</td>
<td align="right">-0.9%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_DICT</td>
<td align="right">565,316,359</td>
<td align="right">570,124,587</td>
<td align="right">0.9%</td>
</tr>
<tr>
<td align="left">JUMP_FORWARD</td>
<td align="right">439,114,340</td>
<td align="right">442,580,564</td>
<td align="right">0.8%</td>
</tr>
<tr>
<td align="left">NOP</td>
<td align="right">995,083,989</td>
<td align="right">987,552,489</td>
<td align="right">-0.8%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">4,275,718,986</td>
<td align="right">4,243,548,874</td>
<td align="right">-0.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_WITH_HINT</td>
<td align="right">379,832,789</td>
<td align="right">377,212,595</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">CALL_LEN</td>
<td align="right">305,545,043</td>
<td align="right">307,621,080</td>
<td align="right">0.7%</td>
</tr>
<tr>
<td align="left">TO_BOOL_ALWAYS_TRUE</td>
<td align="right">183,889,697</td>
<td align="right">182,708,597</td>
<td align="right">-0.6%</td>
</tr>
<tr>
<td align="left">TO_BOOL_STR</td>
<td align="right">77,607,834</td>
<td align="right">77,135,760</td>
<td align="right">-0.6%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">5,499,559,808</td>
<td align="right">5,532,488,354</td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NOT_NONE</td>
<td align="right">670,477,456</td>
<td align="right">674,465,425</td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_CLASS</td>
<td align="right">150,813,914</td>
<td align="right">151,549,195</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">373,167,312</td>
<td align="right">374,912,076</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_INT</td>
<td align="right">401,891,789</td>
<td align="right">403,510,017</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">BUILD_LIST</td>
<td align="right">222,511,919</td>
<td align="right">221,619,183</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">BINARY_SLICE</td>
<td align="right">226,420,268</td>
<td align="right">227,274,337</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP_DICT</td>
<td align="right">176,614,826</td>
<td align="right">177,171,668</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">CALL_ISINSTANCE</td>
<td align="right">822,797,365</td>
<td align="right">825,256,566</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_TUPLE_INT</td>
<td align="right">210,390,707</td>
<td align="right">211,016,694</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">251,092,280</td>
<td align="right">250,360,572</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">3,630,988,147</td>
<td align="right">3,620,674,044</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">SET_FUNCTION_ATTRIBUTE</td>
<td align="right">85,221,584</td>
<td align="right">84,991,511</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">122,592,908</td>
<td align="right">122,266,012</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_SLOT</td>
<td align="right">1,503,921,063</td>
<td align="right">1,507,582,055</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">DICT_UPDATE</td>
<td align="right">73,642</td>
<td align="right">73,816</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">COPY_FREE_VARS</td>
<td align="right">316,140,764</td>
<td align="right">315,395,366</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">MAKE_FUNCTION</td>
<td align="right">95,516,406</td>
<td align="right">95,307,906</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_UNICODE</td>
<td align="right">74,372,519</td>
<td align="right">74,215,741</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">UNARY_INVERT</td>
<td align="right">2,560,622</td>
<td align="right">2,555,306</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">468,066,486</td>
<td align="right">467,133,534</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">6,197,926,400</td>
<td align="right">6,185,856,680</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">263,586,307</td>
<td align="right">263,081,688</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_MODULE</td>
<td align="right">540,418,439</td>
<td align="right">539,413,669</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">IS_OP</td>
<td align="right">472,914,946</td>
<td align="right">473,781,466</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">1,137,405,530</td>
<td align="right">1,139,371,343</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">631,652,551</td>
<td align="right">630,715,380</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">654,971,507</td>
<td align="right">654,194,688</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">2,051,499,870</td>
<td align="right">2,053,928,195</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">1,738,832,380</td>
<td align="right">1,740,838,930</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">TO_BOOL_LIST</td>
<td align="right">117,826,042</td>
<td align="right">117,699,877</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_AND_CLEAR</td>
<td align="right">70,759,813</td>
<td align="right">70,829,491</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR</td>
<td align="right">412,608,393</td>
<td align="right">412,998,310</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_LAZY_DICT</td>
<td align="right">250,569,159</td>
<td align="right">250,804,764</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">343,016,924</td>
<td align="right">342,698,168</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">UNARY_NOT</td>
<td align="right">28,411,354</td>
<td align="right">28,437,573</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">TO_BOOL_INT</td>
<td align="right">145,036,085</td>
<td align="right">145,160,566</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR</td>
<td align="right">130,321,337</td>
<td align="right">130,426,353</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right">122,656,971</td>
<td align="right">122,754,033</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">128,478,163</td>
<td align="right">128,579,110</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_O</td>
<td align="right">396,402,814</td>
<td align="right">396,714,201</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_DICT</td>
<td align="right">149,996,446</td>
<td align="right">150,114,113</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT</td>
<td align="right">1,225,200,664</td>
<td align="right">1,226,110,550</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">LIST_EXTEND</td>
<td align="right">27,671,375</td>
<td align="right">27,691,343</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">563,960,771</td>
<td align="right">563,566,882</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">INTERPRETER_EXIT</td>
<td align="right">2,304,052,341</td>
<td align="right">2,302,484,033</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">DELETE_FAST</td>
<td align="right">2,240,354</td>
<td align="right">2,241,825</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">642,951,705</td>
<td align="right">642,534,849</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_LIST_INT</td>
<td align="right">107,440,409</td>
<td align="right">107,505,853</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">BUILD_MAP</td>
<td align="right">126,406,579</td>
<td align="right">126,480,579</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">STORE_SLICE</td>
<td align="right">12,595,933</td>
<td align="right">12,602,087</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_TUPLE_1</td>
<td align="right">28,291,102</td>
<td align="right">28,304,924</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_CHECK</td>
<td align="right">11,100,534</td>
<td align="right">11,105,846</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">612,857,157</td>
<td align="right">613,149,710</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_INT</td>
<td align="right">675,289,225</td>
<td align="right">674,973,965</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">INSTRUMENTED_JUMP_BACKWARD</td>
<td align="right">10,004</td>
<td align="right">10,000</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">1,332,685,373</td>
<td align="right">1,333,216,866</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">INSTRUMENTED_FOR_ITER</td>
<td align="right">11,364</td>
<td align="right">11,360</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">FOR_ITER_RANGE</td>
<td align="right">106,999,895</td>
<td align="right">107,037,111</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">FOR_ITER_GEN</td>
<td align="right">220,126,704</td>
<td align="right">220,200,157</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_FAST_STORE_FAST</td>
<td align="right">441,547,445</td>
<td align="right">441,401,257</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">CALL_STR_1</td>
<td align="right">40,992,011</td>
<td align="right">41,005,573</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">735,751,182</td>
<td align="right">735,512,393</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">DICT_MERGE</td>
<td align="right">41,215,923</td>
<td align="right">41,228,764</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">INSTRUMENTED_POP_JUMP_IF_TRUE</td>
<td align="right">13,444</td>
<td align="right">13,440</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL_NONE</td>
<td align="right">508,534,016</td>
<td align="right">508,679,580</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_LIST</td>
<td align="right">12,239,127</td>
<td align="right">12,242,351</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">MAKE_CELL</td>
<td align="right">104,851,044</td>
<td align="right">104,878,455</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BEFORE_WITH</td>
<td align="right">10,097,085</td>
<td align="right">10,094,511</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">861,297,880</td>
<td align="right">861,513,234</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_FAST_LOAD_FAST</td>
<td align="right">43,188,809</td>
<td align="right">43,198,831</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE</td>
<td align="right">541,232</td>
<td align="right">541,357</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">342,855</td>
<td align="right">342,932</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BUILD_STRING</td>
<td align="right">75,650,870</td>
<td align="right">75,667,381</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">END_FOR</td>
<td align="right">82,911,547</td>
<td align="right">82,928,846</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_DEREF</td>
<td align="right">95,287,154</td>
<td align="right">95,303,063</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">FORMAT_SIMPLE</td>
<td align="right">148,772,328</td>
<td align="right">148,796,832</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">1,192,132,375</td>
<td align="right">1,192,317,076</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">76,989,224</td>
<td align="right">76,999,779</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BUILD_CONST_KEY_MAP</td>
<td align="right">11,843,525</td>
<td align="right">11,845,095</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_INTRINSIC_1</td>
<td align="right">152,973,509</td>
<td align="right">152,993,519</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST_WITH_KEYWORDS</td>
<td align="right">110,268,495</td>
<td align="right">110,282,834</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR</td>
<td align="right">23,802</td>
<td align="right">23,805</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">GET_YIELD_FROM_ITER</td>
<td align="right">47,471,383</td>
<td align="right">47,476,919</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">IMPORT_FROM</td>
<td align="right">13,157,364</td>
<td align="right">13,158,846</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">IMPORT_NAME</td>
<td align="right">12,486,287</td>
<td align="right">12,487,555</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CONVERT_VALUE</td>
<td align="right">138,439,732</td>
<td align="right">138,451,998</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BUILD_SLICE</td>
<td align="right">71,680,672</td>
<td align="right">71,685,837</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">RAISE_VARARGS</td>
<td align="right">6,196,167</td>
<td align="right">6,196,599</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_FLOAT</td>
<td align="right">181,067,849</td>
<td align="right">181,079,954</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_FUNCTION_EX</td>
<td align="right">192,741,974</td>
<td align="right">192,754,487</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">WITH_EXCEPT_START</td>
<td align="right">235,325</td>
<td align="right">235,337</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_WITH_HINT</td>
<td align="right">64,671,408</td>
<td align="right">64,674,533</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR_METHOD</td>
<td align="right">127,275,558</td>
<td align="right">127,269,979</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">DELETE_SUBSCR</td>
<td align="right">176,501,535</td>
<td align="right">176,508,853</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">DELETE_ATTR</td>
<td align="right">6,773,963</td>
<td align="right">6,774,171</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">RETURN_GENERATOR</td>
<td align="right">502,730,324</td>
<td align="right">502,745,593</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CHECK_EXC_MATCH</td>
<td align="right">24,590,698</td>
<td align="right">24,591,428</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BUILD_SET</td>
<td align="right">2,388,801</td>
<td align="right">2,388,863</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">PUSH_EXC_INFO</td>
<td align="right">25,078,789</td>
<td align="right">25,079,433</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">POP_EXCEPT</td>
<td align="right">25,078,643</td>
<td align="right">25,079,286</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">MAP_ADD</td>
<td align="right">39,901,206</td>
<td align="right">39,902,079</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">YIELD_VALUE</td>
<td align="right">1,380,767,588</td>
<td align="right">1,380,741,372</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">CALL_PY_WITH_DEFAULTS</td>
<td align="right">212,001,048</td>
<td align="right">212,004,824</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">20,797,186</td>
<td align="right">20,797,537</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_KW</td>
<td align="right">268,947,549</td>
<td align="right">268,950,210</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR_ATTR</td>
<td align="right">7,740,757</td>
<td align="right">7,740,825</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_LIST_APPEND</td>
<td align="right">338,605,271</td>
<td align="right">338,607,979</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">GET_AWAITABLE</td>
<td align="right">229,797,754</td>
<td align="right">229,799,226</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">END_SEND</td>
<td align="right">402,765,427</td>
<td align="right">402,766,899</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">SEND</td>
<td align="right">173,954,391</td>
<td align="right">173,954,830</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">RERAISE</td>
<td align="right">3,993,479</td>
<td align="right">3,993,489</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">SEND_GEN</td>
<td align="right">787,190,378</td>
<td align="right">787,192,023</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD_NO_INTERRUPT</td>
<td align="right">556,733,970</td>
<td align="right">556,734,574</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">EXIT_INIT_CHECK</td>
<td align="right">94,785,878</td>
<td align="right">94,785,880</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_ALLOC_AND_ENTER_INIT</td>
<td align="right">97,073,760</td>
<td align="right">97,073,762</td>
<td align="right">0.0%</td>
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
<td align="left">LOAD_NAME</td>
<td align="right">12,134,387</td>
<td align="right">12,134,387</td>
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
<td align="left">STORE_GLOBAL</td>
<td align="right">6,944,680</td>
<td align="right">6,944,680</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BEFORE_ASYNC_WITH</td>
<td align="right">3,005,926</td>
<td align="right">3,005,926</td>
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
<td align="right">610,642</td>
<td align="right">610,642</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">SET_UPDATE</td>
<td align="right">200,448</td>
<td align="right">200,448</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CLEANUP_THROW</td>
<td align="right">160,103</td>
<td align="right">160,103</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_GETATTRIBUTE_OVERRIDDEN</td>
<td align="right">99,800</td>
<td align="right">99,800</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_BUILD_CLASS</td>
<td align="right">28,806</td>
<td align="right">28,806</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">INSTRUMENTED_RETURN_CONST</td>
<td align="right">6,240</td>
<td align="right">6,240</td>
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
<td align="left">SETUP_ANNOTATIONS</td>
<td align="right">1,504</td>
<td align="right">1,504</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">DELETE_NAME</td>
<td align="right">980</td>
<td align="right">980</td>
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
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">21,800,778</td>
<td align="right">1.0%</td>
<td align="right">30,888,231</td>
<td align="right">1.3%</td>
<td align="right">41.7%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">1,551,908,422</td>
<td align="right">71.0%</td>
<td align="right">1,668,420,598</td>
<td align="right">72.1%</td>
<td align="right">7.5%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">633,044,585</td>
<td align="right">29.0%</td>
<td align="right">642,161,309</td>
<td align="right">27.8%</td>
<td align="right">1.4%</td>
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
<td align="right">464,485</td>
<td align="right">28.8%</td>
<td align="right">635,976</td>
<td align="right">33.9%</td>
<td align="right">36.9%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">1,148,865</td>
<td align="right">71.2%</td>
<td align="right">1,240,656</td>
<td align="right">66.1%</td>
<td align="right">8.0%</td>
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
<td align="left">multiply different types</td>
<td align="right">67,633</td>
<td align="right">5.9%</td>
<td align="right">94,183</td>
<td align="right">7.6%</td>
<td align="right">39.3%</td>
</tr>
<tr>
<td align="left">add different types</td>
<td align="right">63,405</td>
<td align="right">5.5%</td>
<td align="right">78,780</td>
<td align="right">6.3%</td>
<td align="right">24.2%</td>
</tr>
<tr>
<td align="left">subtract different types</td>
<td align="right">736,427</td>
<td align="right">64.1%</td>
<td align="right">784,194</td>
<td align="right">63.2%</td>
<td align="right">6.5%</td>
</tr>
<tr>
<td align="left">true divide other</td>
<td align="right">3,401</td>
<td align="right">0.3%</td>
<td align="right">3,523</td>
<td align="right">0.3%</td>
<td align="right">3.6%</td>
</tr>
<tr>
<td align="left">lshift</td>
<td align="right">5,644</td>
<td align="right">0.5%</td>
<td align="right">5,826</td>
<td align="right">0.5%</td>
<td align="right">3.2%</td>
</tr>
<tr>
<td align="left">subtract other</td>
<td align="right">12,174</td>
<td align="right">1.1%</td>
<td align="right">12,554</td>
<td align="right">1.0%</td>
<td align="right">3.1%</td>
</tr>
<tr>
<td align="left">and int</td>
<td align="right">40,671</td>
<td align="right">3.5%</td>
<td align="right">41,347</td>
<td align="right">3.3%</td>
<td align="right">1.7%</td>
</tr>
<tr>
<td align="left">rshift</td>
<td align="right">9,828</td>
<td align="right">0.9%</td>
<td align="right">9,990</td>
<td align="right">0.8%</td>
<td align="right">1.6%</td>
</tr>
<tr>
<td align="left">true divide different types</td>
<td align="right">11,827</td>
<td align="right">1.0%</td>
<td align="right">11,668</td>
<td align="right">0.9%</td>
<td align="right">-1.3%</td>
</tr>
<tr>
<td align="left">or</td>
<td align="right">17,473</td>
<td align="right">1.5%</td>
<td align="right">17,637</td>
<td align="right">1.4%</td>
<td align="right">0.9%</td>
</tr>
<tr>
<td align="left">add other</td>
<td align="right">65,585</td>
<td align="right">5.7%</td>
<td align="right">65,853</td>
<td align="right">5.3%</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">multiply other</td>
<td align="right">5,200</td>
<td align="right">0.5%</td>
<td align="right">5,220</td>
<td align="right">0.4%</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">floor divide</td>
<td align="right">32,508</td>
<td align="right">2.8%</td>
<td align="right">32,616</td>
<td align="right">2.6%</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">remainder</td>
<td align="right">53,117</td>
<td align="right">4.6%</td>
<td align="right">53,257</td>
<td align="right">4.3%</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">power</td>
<td align="right">5,714</td>
<td align="right">0.5%</td>
<td align="right">5,728</td>
<td align="right">0.5%</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">xor</td>
<td align="right">9,842</td>
<td align="right">0.9%</td>
<td align="right">9,864</td>
<td align="right">0.8%</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">and other</td>
<td align="right">2,035</td>
<td align="right">0.2%</td>
<td align="right">2,033</td>
<td align="right">0.2%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">true divide float</td>
<td align="right">5,762</td>
<td align="right">0.5%</td>
<td align="right">5,764</td>
<td align="right">0.5%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">and different types</td>
<td align="right">619</td>
<td align="right">0.1%</td>
<td align="right">619</td>
<td align="right">0.0%</td>
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
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">1,721,688,151</td>
<td align="right">80.5%</td>
<td align="right">1,749,041,717</td>
<td align="right">80.7%</td>
<td align="right">1.6%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">417,123,575</td>
<td align="right">19.5%</td>
<td align="right">417,513,835</td>
<td align="right">19.3%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">4,898,532</td>
<td align="right">0.2%</td>
<td align="right">4,900,661</td>
<td align="right">0.2%</td>
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
<td align="right">181,418</td>
<td align="right">47.3%</td>
<td align="right">183,194</td>
<td align="right">47.6%</td>
<td align="right">1.0%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">201,932</td>
<td align="right">52.7%</td>
<td align="right">201,942</td>
<td align="right">52.4%</td>
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
<td align="left">list slice</td>
<td align="right">680</td>
<td align="right">0.4%</td>
<td align="right">720</td>
<td align="right">0.4%</td>
<td align="right">5.9%</td>
</tr>
<tr>
<td align="left">tuple slice</td>
<td align="right">182</td>
<td align="right">0.1%</td>
<td align="right">185</td>
<td align="right">0.1%</td>
<td align="right">1.6%</td>
</tr>
<tr>
<td align="left">buffer int</td>
<td align="right">22,402</td>
<td align="right">12.3%</td>
<td align="right">22,721</td>
<td align="right">12.4%</td>
<td align="right">1.4%</td>
</tr>
<tr>
<td align="left">out of range</td>
<td align="right">75,352</td>
<td align="right">41.5%</td>
<td align="right">76,144</td>
<td align="right">41.6%</td>
<td align="right">1.1%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">55,788</td>
<td align="right">30.8%</td>
<td align="right">56,268</td>
<td align="right">30.7%</td>
<td align="right">0.9%</td>
</tr>
<tr>
<td align="left">array int</td>
<td align="right">16,680</td>
<td align="right">9.2%</td>
<td align="right">16,820</td>
<td align="right">9.2%</td>
<td align="right">0.8%</td>
</tr>
<tr>
<td align="left">code complex parameters</td>
<td align="right">5,034</td>
<td align="right">2.8%</td>
<td align="right">5,036</td>
<td align="right">2.7%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">sequence int</td>
<td align="right">4,300</td>
<td align="right">2.4%</td>
<td align="right">4,300</td>
<td align="right">2.3%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">buffer slice</td>
<td align="right">900</td>
<td align="right">0.5%</td>
<td align="right">900</td>
<td align="right">0.5%</td>
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
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">7,739,296,195</td>
<td align="right">84.3%</td>
<td align="right">7,559,539,657</td>
<td align="right">84.0%</td>
<td align="right">-2.3%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">248,944,778</td>
<td align="right">2.7%</td>
<td align="right">250,369,689</td>
<td align="right">2.8%</td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">1,434,783,202</td>
<td align="right">15.6%</td>
<td align="right">1,436,365,510</td>
<td align="right">16.0%</td>
<td align="right">0.1%</td>
</tr>
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
<td align="right">33,100</td>
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
<td align="right">5,326,440</td>
<td align="right">84.6%</td>
<td align="right">5,353,458</td>
<td align="right">84.7%</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">967,511</td>
<td align="right">15.4%</td>
<td align="right">967,797</td>
<td align="right">15.3%</td>
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
<td align="left">metaclass</td>
<td align="right">43,041</td>
<td align="right">4.4%</td>
<td align="right">43,185</td>
<td align="right">4.5%</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">method wrapper</td>
<td align="right">8,197</td>
<td align="right">0.8%</td>
<td align="right">8,223</td>
<td align="right">0.8%</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">bound method</td>
<td align="right">12,048</td>
<td align="right">1.2%</td>
<td align="right">12,055</td>
<td align="right">1.2%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">meth descr varargs keywords</td>
<td align="right">20,900</td>
<td align="right">2.2%</td>
<td align="right">20,888</td>
<td align="right">2.2%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">cfunc varargs keywords</td>
<td align="right">32,145</td>
<td align="right">3.3%</td>
<td align="right">32,161</td>
<td align="right">3.3%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">operator wrapper</td>
<td align="right">10,138</td>
<td align="right">1.0%</td>
<td align="right">10,142</td>
<td align="right">1.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">class mutable</td>
<td align="right">23,769</td>
<td align="right">2.5%</td>
<td align="right">23,778</td>
<td align="right">2.5%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">class no vectorcall</td>
<td align="right">77,998</td>
<td align="right">8.1%</td>
<td align="right">78,026</td>
<td align="right">8.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">78,545</td>
<td align="right">8.1%</td>
<td align="right">78,573</td>
<td align="right">8.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">cfunc noargs</td>
<td align="right">69,957</td>
<td align="right">7.2%</td>
<td align="right">69,942</td>
<td align="right">7.2%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">meth descr varargs</td>
<td align="right">18,595</td>
<td align="right">1.9%</td>
<td align="right">18,598</td>
<td align="right">1.9%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">code complex parameters</td>
<td align="right">185,238</td>
<td align="right">19.1%</td>
<td align="right">185,267</td>
<td align="right">19.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">cfunc varargs</td>
<td align="right">14,151</td>
<td align="right">1.5%</td>
<td align="right">14,153</td>
<td align="right">1.5%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">meth descr method fastcall keywords</td>
<td align="right">207,035</td>
<td align="right">21.4%</td>
<td align="right">207,052</td>
<td align="right">21.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">init not inline values</td>
<td align="right">105,657</td>
<td align="right">10.9%</td>
<td align="right">105,657</td>
<td align="right">10.9%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">init not python</td>
<td align="right">16,406</td>
<td align="right">1.7%</td>
<td align="right">16,406</td>
<td align="right">1.7%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">wrong number arguments</td>
<td align="right">13,793</td>
<td align="right">1.4%</td>
<td align="right">13,793</td>
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
<td align="left">str</td>
<td align="right">3,180</td>
<td align="right">0.3%</td>
<td align="right">3,180</td>
<td align="right">0.3%</td>
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
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">1,724,600</td>
<td align="right">0.1%</td>
<td align="right">1,876,553</td>
<td align="right">0.1%</td>
<td align="right">8.8%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">142,112,321</td>
<td align="right">7.6%</td>
<td align="right">153,580,758</td>
<td align="right">8.1%</td>
<td align="right">8.1%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">1,730,969,895</td>
<td align="right">92.4%</td>
<td align="right">1,735,177,782</td>
<td align="right">91.9%</td>
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
<td align="left">Failure</td>
<td align="right">224,163</td>
<td align="right">67.0%</td>
<td align="right">234,047</td>
<td align="right">67.3%</td>
<td align="right">4.4%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">110,616</td>
<td align="right">33.0%</td>
<td align="right">113,485</td>
<td align="right">32.7%</td>
<td align="right">2.6%</td>
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
<td align="left">float long</td>
<td align="right">13,259</td>
<td align="right">5.9%</td>
<td align="right">16,430</td>
<td align="right">7.0%</td>
<td align="right">23.9%</td>
</tr>
<tr>
<td align="left">different types</td>
<td align="right">48,433</td>
<td align="right">21.6%</td>
<td align="right">55,018</td>
<td align="right">23.5%</td>
<td align="right">13.6%</td>
</tr>
<tr>
<td align="left">bool</td>
<td align="right">3,740</td>
<td align="right">1.7%</td>
<td align="right">3,823</td>
<td align="right">1.6%</td>
<td align="right">2.2%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">23,908</td>
<td align="right">10.7%</td>
<td align="right">24,200</td>
<td align="right">10.3%</td>
<td align="right">1.2%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">14,466</td>
<td align="right">6.5%</td>
<td align="right">14,616</td>
<td align="right">6.2%</td>
<td align="right">1.0%</td>
</tr>
<tr>
<td align="left">bytes</td>
<td align="right">4,100</td>
<td align="right">1.8%</td>
<td align="right">4,120</td>
<td align="right">1.8%</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">big int</td>
<td align="right">62,782</td>
<td align="right">28.0%</td>
<td align="right">62,499</td>
<td align="right">26.7%</td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">string</td>
<td align="right">11,120</td>
<td align="right">5.0%</td>
<td align="right">11,080</td>
<td align="right">4.7%</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">baseobject</td>
<td align="right">34,140</td>
<td align="right">15.2%</td>
<td align="right">34,044</td>
<td align="right">14.5%</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">long float</td>
<td align="right">1,538</td>
<td align="right">0.7%</td>
<td align="right">1,540</td>
<td align="right">0.7%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">4,334</td>
<td align="right">1.9%</td>
<td align="right">4,334</td>
<td align="right">1.9%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">2,343</td>
<td align="right">1.0%</td>
<td align="right">2,343</td>
<td align="right">1.0%</td>
<td align="right">0.0%</td>
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
<td align="right">690,533,744</td>
<td align="right">85.7%</td>
<td align="right">636,891,907</td>
<td align="right">84.6%</td>
<td align="right">-7.8%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">114,697,556</td>
<td align="right">14.2%</td>
<td align="right">115,901,249</td>
<td align="right">15.4%</td>
<td align="right">1.0%</td>
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
<td align="right">0.3%</td>
<td align="right">2,513,180</td>
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
<td align="right">130,199</td>
<td align="right">66.0%</td>
<td align="right">131,456</td>
<td align="right">66.2%</td>
<td align="right">1.0%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">67,032</td>
<td align="right">34.0%</td>
<td align="right">67,030</td>
<td align="right">33.8%</td>
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
<td align="left">list</td>
<td align="right">19,361</td>
<td align="right">14.9%</td>
<td align="right">19,801</td>
<td align="right">15.1%</td>
<td align="right">2.3%</td>
</tr>
<tr>
<td align="left">str</td>
<td align="right">36,842</td>
<td align="right">28.3%</td>
<td align="right">37,356</td>
<td align="right">28.4%</td>
<td align="right">1.4%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">47,010</td>
<td align="right">36.1%</td>
<td align="right">47,239</td>
<td align="right">35.9%</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">26,986</td>
<td align="right">20.7%</td>
<td align="right">27,060</td>
<td align="right">20.6%</td>
<td align="right">0.3%</td>
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
<td align="right">123,305,255</td>
<td align="right">8.5%</td>
<td align="right">101,955,291</td>
<td align="right">7.3%</td>
<td align="right">-17.3%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">243,313,270</td>
<td align="right">16.7%</td>
<td align="right">222,039,068</td>
<td align="right">15.8%</td>
<td align="right">-8.7%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">1,207,704,642</td>
<td align="right">83.1%</td>
<td align="right">1,180,238,325</td>
<td align="right">84.0%</td>
<td align="right">-2.3%</td>
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
<td align="right">2,392,693</td>
<td align="right">92.6%</td>
<td align="right">1,989,873</td>
<td align="right">91.2%</td>
<td align="right">-16.8%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">192,200</td>
<td align="right">7.4%</td>
<td align="right">192,362</td>
<td align="right">8.8%</td>
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
<td align="left">map</td>
<td align="right">1,600</td>
<td align="right">0.8%</td>
<td align="right">1,380</td>
<td align="right">0.7%</td>
<td align="right">-13.8%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">14,899</td>
<td align="right">7.8%</td>
<td align="right">14,379</td>
<td align="right">7.5%</td>
<td align="right">-3.5%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">25,823</td>
<td align="right">13.4%</td>
<td align="right">26,061</td>
<td align="right">13.5%</td>
<td align="right">0.9%</td>
</tr>
<tr>
<td align="left">dict items</td>
<td align="right">66,251</td>
<td align="right">34.5%</td>
<td align="right">66,855</td>
<td align="right">34.8%</td>
<td align="right">0.9%</td>
</tr>
<tr>
<td align="left">enumerate</td>
<td align="right">19,711</td>
<td align="right">10.3%</td>
<td align="right">19,791</td>
<td align="right">10.3%</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">dict keys</td>
<td align="right">14,776</td>
<td align="right">7.7%</td>
<td align="right">14,756</td>
<td align="right">7.7%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">zip</td>
<td align="right">14,352</td>
<td align="right">7.5%</td>
<td align="right">14,352</td>
<td align="right">7.5%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">seq iter</td>
<td align="right">10,600</td>
<td align="right">5.5%</td>
<td align="right">10,600</td>
<td align="right">5.5%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">dict values</td>
<td align="right">6,990</td>
<td align="right">3.6%</td>
<td align="right">6,990</td>
<td align="right">3.6%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">reversed list</td>
<td align="right">6,985</td>
<td align="right">3.6%</td>
<td align="right">6,985</td>
<td align="right">3.6%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">itertools</td>
<td align="right">6,551</td>
<td align="right">3.4%</td>
<td align="right">6,551</td>
<td align="right">3.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">ascii string</td>
<td align="right">2,680</td>
<td align="right">1.4%</td>
<td align="right">2,680</td>
<td align="right">1.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">bytes</td>
<td align="right">660</td>
<td align="right">0.3%</td>
<td align="right">660</td>
<td align="right">0.3%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">callable</td>
<td align="right">282</td>
<td align="right">0.1%</td>
<td align="right">282</td>
<td align="right">0.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">string</td>
<td align="right">40</td>
<td align="right">0.0%</td>
<td align="right">40</td>
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
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">9,856,425,425</td>
<td align="right">87.3%</td>
<td align="right">9,991,322,478</td>
<td align="right">87.4%</td>
<td align="right">1.4%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">573,715,268</td>
<td align="right">5.1%</td>
<td align="right">576,775,346</td>
<td align="right">5.0%</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">1,421,601,236</td>
<td align="right">12.6%</td>
<td align="right">1,424,810,644</td>
<td align="right">12.5%</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">
deopt
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">674,901</td>
<td align="right">0.0%</td>
<td align="right">675,833</td>
<td align="right">0.0%</td>
<td align="right">0.1%</td>
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
<td align="right">11,708,422</td>
<td align="right">87.3%</td>
<td align="right">11,767,826</td>
<td align="right">87.3%</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">1,703,490</td>
<td align="right">12.7%</td>
<td align="right">1,710,110</td>
<td align="right">12.7%</td>
<td align="right">0.4%</td>
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
<td align="left">not in keys</td>
<td align="right">15,860</td>
<td align="right">0.9%</td>
<td align="right">16,660</td>
<td align="right">1.0%</td>
<td align="right">5.0%</td>
</tr>
<tr>
<td align="left">mutable class</td>
<td align="right">77,506</td>
<td align="right">4.5%</td>
<td align="right">78,891</td>
<td align="right">4.6%</td>
<td align="right">1.8%</td>
</tr>
<tr>
<td align="left">class method obj</td>
<td align="right">24,892</td>
<td align="right">1.5%</td>
<td align="right">25,233</td>
<td align="right">1.5%</td>
<td align="right">1.4%</td>
</tr>
<tr>
<td align="left">class attr descriptor</td>
<td align="right">29,540</td>
<td align="right">1.7%</td>
<td align="right">29,880</td>
<td align="right">1.7%</td>
<td align="right">1.2%</td>
</tr>
<tr>
<td align="left">builtin class method</td>
<td align="right">3,836</td>
<td align="right">0.2%</td>
<td align="right">3,878</td>
<td align="right">0.2%</td>
<td align="right">1.1%</td>
</tr>
<tr>
<td align="left">non object slot</td>
<td align="right">3,520</td>
<td align="right">0.2%</td>
<td align="right">3,540</td>
<td align="right">0.2%</td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">shadowed</td>
<td align="right">142,779</td>
<td align="right">8.4%</td>
<td align="right">143,576</td>
<td align="right">8.4%</td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">method</td>
<td align="right">119,418</td>
<td align="right">7.0%</td>
<td align="right">120,001</td>
<td align="right">7.0%</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">out of versions</td>
<td align="right">2,341</td>
<td align="right">0.1%</td>
<td align="right">2,331</td>
<td align="right">0.1%</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">overridden</td>
<td align="right">19,247</td>
<td align="right">1.1%</td>
<td align="right">19,314</td>
<td align="right">1.1%</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">module attr not found</td>
<td align="right">17,362</td>
<td align="right">1.0%</td>
<td align="right">17,422</td>
<td align="right">1.0%</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">not managed dict</td>
<td align="right">301,146</td>
<td align="right">17.7%</td>
<td align="right">301,884</td>
<td align="right">17.7%</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">non overriding descriptor</td>
<td align="right">13,794</td>
<td align="right">0.8%</td>
<td align="right">13,820</td>
<td align="right">0.8%</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">metaclass attribute</td>
<td align="right">193,670</td>
<td align="right">11.4%</td>
<td align="right">193,977</td>
<td align="right">11.3%</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">class attr simple</td>
<td align="right">715,071</td>
<td align="right">42.0%</td>
<td align="right">716,195</td>
<td align="right">41.9%</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">non string or split</td>
<td align="right">21,648</td>
<td align="right">1.3%</td>
<td align="right">21,648</td>
<td align="right">1.3%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">wrong number arguments</td>
<td align="right">1,200</td>
<td align="right">0.1%</td>
<td align="right">1,200</td>
<td align="right">0.1%</td>
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
<td align="left">not in dict</td>
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
<td align="right">6,614,240,264</td>
<td align="right">99.7%</td>
<td align="right">6,467,428,766</td>
<td align="right">99.7%</td>
<td align="right">-2.2%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">444,304</td>
<td align="right">0.0%</td>
<td align="right">445,890</td>
<td align="right">0.0%</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">20,572,356</td>
<td align="right">0.3%</td>
<td align="right">20,574,151</td>
<td align="right">0.3%</td>
<td align="right">0.0%</td>
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
<td align="right">13,043</td>
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
<td align="right">669,134</td>
<td align="right">100.0%</td>
<td align="right">669,276</td>
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
<td align="right">11,985</td>
<td align="right">0.0%</td>
<td align="right">11,987</td>
<td align="right">0.0%</td>
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
<td align="right">135,016,315</td>
<td align="right">100.0%</td>
<td align="right">135,010,804</td>
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
<td align="right">11,817</td>
<td align="right">100.0%</td>
<td align="right">11,818</td>
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
<td align="right">173,916,296</td>
<td align="right">18.1%</td>
<td align="right">173,916,725</td>
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
<td align="right">787,159,478</td>
<td align="right">81.9%</td>
<td align="right">787,161,123</td>
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
<td align="left">Success</td>
<td align="right">7,129</td>
<td align="right">10.3%</td>
<td align="right">7,137</td>
<td align="right">10.3%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">61,866</td>
<td align="right">89.7%</td>
<td align="right">61,868</td>
<td align="right">89.7%</td>
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
<td align="right">16,126</td>
<td align="right">26.1%</td>
<td align="right">16,128</td>
<td align="right">26.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">async generator send</td>
<td align="right">33,180</td>
<td align="right">53.6%</td>
<td align="right">33,180</td>
<td align="right">53.6%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">10,060</td>
<td align="right">16.3%</td>
<td align="right">10,060</td>
<td align="right">16.3%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">2,260</td>
<td align="right">3.7%</td>
<td align="right">2,260</td>
<td align="right">3.7%</td>
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
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">2,537,910,286</td>
<td align="right">91.2%</td>
<td align="right">2,543,324,607</td>
<td align="right">91.2%</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">168,087,715</td>
<td align="right">6.0%</td>
<td align="right">168,303,324</td>
<td align="right">6.0%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">241,608,938</td>
<td align="right">8.7%</td>
<td align="right">241,830,904</td>
<td align="right">8.7%</td>
<td align="right">0.1%</td>
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
<td align="right">3,320,805</td>
<td align="right">95.8%</td>
<td align="right">3,324,898</td>
<td align="right">95.8%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">147,196</td>
<td align="right">4.2%</td>
<td align="right">147,301</td>
<td align="right">4.2%</td>
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
<td align="left">overriding descriptor</td>
<td align="right">10,640</td>
<td align="right">7.2%</td>
<td align="right">10,660</td>
<td align="right">7.2%</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">class attr simple</td>
<td align="right">49,898</td>
<td align="right">33.9%</td>
<td align="right">49,979</td>
<td align="right">33.9%</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">not managed dict</td>
<td align="right">28,566</td>
<td align="right">19.4%</td>
<td align="right">28,570</td>
<td align="right">19.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">not in dict</td>
<td align="right">15,725</td>
<td align="right">10.7%</td>
<td align="right">15,725</td>
<td align="right">10.7%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">non string or split</td>
<td align="right">15,020</td>
<td align="right">10.2%</td>
<td align="right">15,020</td>
<td align="right">10.2%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">not in keys</td>
<td align="right">7,961</td>
<td align="right">5.4%</td>
<td align="right">7,961</td>
<td align="right">5.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">overridden</td>
<td align="right">6,832</td>
<td align="right">4.6%</td>
<td align="right">6,832</td>
<td align="right">4.6%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">property</td>
<td align="right">5,600</td>
<td align="right">3.8%</td>
<td align="right">5,600</td>
<td align="right">3.8%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">no dict</td>
<td align="right">4,780</td>
<td align="right">3.2%</td>
<td align="right">4,780</td>
<td align="right">3.2%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">method</td>
<td align="right">1,540</td>
<td align="right">1.0%</td>
<td align="right">1,540</td>
<td align="right">1.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">out of versions</td>
<td align="right">594</td>
<td align="right">0.4%</td>
<td align="right">594</td>
<td align="right">0.4%</td>
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
<td align="right">130,223,954</td>
<td align="right">33.6%</td>
<td align="right">130,328,184</td>
<td align="right">33.6%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">257,433,975</td>
<td align="right">66.4%</td>
<td align="right">257,617,086</td>
<td align="right">66.4%</td>
<td align="right">0.1%</td>
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
<td align="left">Failure</td>
<td align="right">81,696</td>
<td align="right">81.5%</td>
<td align="right">82,482</td>
<td align="right">81.6%</td>
<td align="right">1.0%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">18,567</td>
<td align="right">18.5%</td>
<td align="right">18,567</td>
<td align="right">18.4%</td>
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
<td align="left">bytearray int</td>
<td align="right">1,080</td>
<td align="right">1.3%</td>
<td align="right">1,400</td>
<td align="right">1.7%</td>
<td align="right">29.6%</td>
</tr>
<tr>
<td align="left">out of range</td>
<td align="right">1,948</td>
<td align="right">2.4%</td>
<td align="right">2,048</td>
<td align="right">2.5%</td>
<td align="right">5.1%</td>
</tr>
<tr>
<td align="left">array int</td>
<td align="right">7,040</td>
<td align="right">8.6%</td>
<td align="right">7,160</td>
<td align="right">8.7%</td>
<td align="right">1.7%</td>
</tr>
<tr>
<td align="left">py simple</td>
<td align="right">42,279</td>
<td align="right">51.8%</td>
<td align="right">42,440</td>
<td align="right">51.5%</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">dict subclass no override</td>
<td align="right">27,229</td>
<td align="right">33.3%</td>
<td align="right">27,314</td>
<td align="right">33.1%</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">2,080</td>
<td align="right">2.5%</td>
<td align="right">2,080</td>
<td align="right">2.5%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">list slice</td>
<td align="right">40</td>
<td align="right">0.0%</td>
<td align="right">40</td>
<td align="right">0.0%</td>
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
<td align="right">3,912,799,491</td>
<td align="right">91.6%</td>
<td align="right">3,685,505,220</td>
<td align="right">91.2%</td>
<td align="right">-5.8%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">106,092,209</td>
<td align="right">2.5%</td>
<td align="right">105,039,604</td>
<td align="right">2.6%</td>
<td align="right">-1.0%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">354,268,629</td>
<td align="right">8.3%</td>
<td align="right">352,501,951</td>
<td align="right">8.7%</td>
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
<td align="left">Success</td>
<td align="right">2,286,810</td>
<td align="right">78.4%</td>
<td align="right">2,266,876</td>
<td align="right">78.2%</td>
<td align="right">-0.9%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">629,050</td>
<td align="right">21.6%</td>
<td align="right">631,349</td>
<td align="right">21.8%</td>
<td align="right">0.4%</td>
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
<td align="left">float</td>
<td align="right">2,601</td>
<td align="right">0.4%</td>
<td align="right">2,323</td>
<td align="right">0.4%</td>
<td align="right">-10.7%</td>
</tr>
<tr>
<td align="left">dict</td>
<td align="right">33,112</td>
<td align="right">5.3%</td>
<td align="right">33,776</td>
<td align="right">5.3%</td>
<td align="right">2.0%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">95,644</td>
<td align="right">15.2%</td>
<td align="right">96,418</td>
<td align="right">15.3%</td>
<td align="right">0.8%</td>
</tr>
<tr>
<td align="left">mapping</td>
<td align="right">58,563</td>
<td align="right">9.3%</td>
<td align="right">59,027</td>
<td align="right">9.3%</td>
<td align="right">0.8%</td>
</tr>
<tr>
<td align="left">sequence</td>
<td align="right">17,936</td>
<td align="right">2.9%</td>
<td align="right">18,022</td>
<td align="right">2.9%</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">bytes</td>
<td align="right">18,614</td>
<td align="right">3.0%</td>
<td align="right">18,693</td>
<td align="right">3.0%</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">173,728</td>
<td align="right">27.6%</td>
<td align="right">174,191</td>
<td align="right">27.6%</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">number</td>
<td align="right">183,559</td>
<td align="right">29.2%</td>
<td align="right">183,606</td>
<td align="right">29.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">43,633</td>
<td align="right">6.9%</td>
<td align="right">43,633</td>
<td align="right">6.9%</td>
<td align="right">0.0%</td>
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
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">687,221,506</td>
<td align="right">99.9%</td>
<td align="right">662,960,457</td>
<td align="right">99.9%</td>
<td align="right">-3.5%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">500,777</td>
<td align="right">0.1%</td>
<td align="right">500,888</td>
<td align="right">0.1%</td>
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
<td align="right">3,160</td>
<td align="right">0.0%</td>
<td align="right">3,160</td>
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
<td align="right">3,578</td>
<td align="right">8.2%</td>
<td align="right">3,576</td>
<td align="right">8.2%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">40,037</td>
<td align="right">91.8%</td>
<td align="right">40,053</td>
<td align="right">91.8%</td>
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
<td align="left">sequence</td>
<td align="right">2,517</td>
<td align="right">70.3%</td>
<td align="right">2,515</td>
<td align="right">70.3%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">iterator</td>
<td align="right">681</td>
<td align="right">19.0%</td>
<td align="right">681</td>
<td align="right">19.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">380</td>
<td align="right">10.6%</td>
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
Not specialized
<details>
<summary>ⓘ</summary>

Instructions that could be specialized but aren't, e.g. `LOAD_ATTR`, `BINARY_SLICE`.
</details>
</td>
<td align="right">12,419,921,605</td>
<td align="right">9.5%</td>
<td align="right">12,110,174,236</td>
<td align="right">9.3%</td>
<td align="right">-2.5%</td>
</tr>
<tr>
<td align="left">
Specialized hits
<details>
<summary>ⓘ</summary>

Specialized instructions, e.g. `LOAD_ATTR_MODULE` that complete.
</details>
</td>
<td align="right">46,281,427,413</td>
<td align="right">35.3%</td>
<td align="right">45,838,368,402</td>
<td align="right">35.3%</td>
<td align="right">-1.0%</td>
</tr>
<tr>
<td align="left">
Basic
<details>
<summary>ⓘ</summary>

Instructions that are not and cannot be specialized, e.g. `LOAD_FAST`.
</details>
</td>
<td align="right">71,337,507,831</td>
<td align="right">54.3%</td>
<td align="right">70,688,115,773</td>
<td align="right">54.4%</td>
<td align="right">-0.9%</td>
</tr>
<tr>
<td align="left">
Specialized misses
<details>
<summary>ⓘ</summary>

Specialized instructions, e.g. `LOAD_ATTR_MODULE` that deopt.
</details>
</td>
<td align="right">1,251,750,663</td>
<td align="right">1.0%</td>
<td align="right">1,243,291,960</td>
<td align="right">1.0%</td>
<td align="right">-0.7%</td>
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
<td align="right">243,313,270</td>
<td align="right">4.6%</td>
<td align="right">222,039,068</td>
<td align="right">4.2%</td>
<td align="right">-8.7%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">142,112,321</td>
<td align="right">2.7%</td>
<td align="right">153,580,758</td>
<td align="right">2.9%</td>
<td align="right">8.1%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">633,044,585</td>
<td align="right">11.9%</td>
<td align="right">642,161,309</td>
<td align="right">12.0%</td>
<td align="right">1.4%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">354,268,629</td>
<td align="right">6.6%</td>
<td align="right">352,501,951</td>
<td align="right">6.6%</td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">1,421,601,236</td>
<td align="right">26.7%</td>
<td align="right">1,424,810,644</td>
<td align="right">26.7%</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">1,434,783,202</td>
<td align="right">26.9%</td>
<td align="right">1,436,365,510</td>
<td align="right">26.9%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR</td>
<td align="right">417,123,575</td>
<td align="right">7.8%</td>
<td align="right">417,513,835</td>
<td align="right">7.8%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">241,608,938</td>
<td align="right">4.5%</td>
<td align="right">241,830,904</td>
<td align="right">4.5%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR</td>
<td align="right">130,223,954</td>
<td align="right">2.4%</td>
<td align="right">130,328,184</td>
<td align="right">2.4%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">SEND</td>
<td align="right">173,916,296</td>
<td align="right">3.3%</td>
<td align="right">173,916,725</td>
<td align="right">3.3%</td>
<td align="right">0.0%</td>
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
<td align="left">FOR_ITER_TUPLE</td>
<td align="right">61,453,324</td>
<td align="right">4.9%</td>
<td align="right">50,778,395</td>
<td align="right">4.1%</td>
<td align="right">-17.4%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">61,612,511</td>
<td align="right">4.9%</td>
<td align="right">50,933,916</td>
<td align="right">4.1%</td>
<td align="right">-17.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">180,282,983</td>
<td align="right">14.4%</td>
<td align="right">182,072,668</td>
<td align="right">14.6%</td>
<td align="right">1.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">157,101,087</td>
<td align="right">12.5%</td>
<td align="right">157,636,841</td>
<td align="right">12.7%</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">73,010,771</td>
<td align="right">5.8%</td>
<td align="right">73,234,089</td>
<td align="right">5.9%</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right">59,826,597</td>
<td align="right">4.8%</td>
<td align="right">59,991,115</td>
<td align="right">4.8%</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">110,424,907</td>
<td align="right">8.8%</td>
<td align="right">110,295,684</td>
<td align="right">8.9%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">TO_BOOL_NONE</td>
<td align="right">49,180,791</td>
<td align="right">3.9%</td>
<td align="right">49,125,295</td>
<td align="right">4.0%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">125,810,426</td>
<td align="right">10.0%</td>
<td align="right">125,670,311</td>
<td align="right">10.1%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_SLOT</td>
<td align="right">95,024,083</td>
<td align="right">7.6%</td>
<td align="right">95,016,349</td>
<td align="right">7.6%</td>
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
<td align="left">Calls to Python functions inlined</td>
<td align="right">4,926,169,086</td>
<td align="right">68.1%</td>
<td align="right">4,858,075,688</td>
<td align="right">67.8%</td>
<td align="right">-1.4%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (api)</td>
<td align="right">258,846,278</td>
<td align="right">3.6%</td>
<td align="right">258,144,271</td>
<td align="right">3.6%</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (slot)</td>
<td align="right">476,729,694</td>
<td align="right">6.6%</td>
<td align="right">475,955,466</td>
<td align="right">6.6%</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (function vectorcall)</td>
<td align="right">1,448,060,953</td>
<td align="right">20.0%</td>
<td align="right">1,446,587,165</td>
<td align="right">20.2%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (vector)</td>
<td align="right">1,452,508,003</td>
<td align="right">20.1%</td>
<td align="right">1,451,034,215</td>
<td align="right">20.3%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">Calls to PyEval_EvalDefault</td>
<td align="right">2,307,770,777</td>
<td align="right">31.9%</td>
<td align="right">2,306,202,396</td>
<td align="right">32.2%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (total)</td>
<td align="right">2,307,770,777</td>
<td align="right">31.9%</td>
<td align="right">2,306,202,396</td>
<td align="right">32.2%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (function ex)</td>
<td align="right">28,856,148</td>
<td align="right">0.4%</td>
<td align="right">28,863,941</td>
<td align="right">0.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (generator)</td>
<td align="right">855,262,774</td>
<td align="right">11.8%</td>
<td align="right">855,168,181</td>
<td align="right">11.9%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">Frames pushed</td>
<td align="right">4,922,390,862</td>
<td align="right">68.0%</td>
<td align="right">4,922,628,180</td>
<td align="right">68.7%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Frame objects created</td>
<td align="right">88,603,613</td>
<td align="right">1.2%</td>
<td align="right">88,605,172</td>
<td align="right">1.2%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (method)</td>
<td align="right">213,150,848</td>
<td align="right">2.9%</td>
<td align="right">213,154,383</td>
<td align="right">3.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (legacy)</td>
<td align="right">4,418,244</td>
<td align="right">0.1%</td>
<td align="right">4,418,244</td>
<td align="right">0.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (build class)</td>
<td align="right">28,806</td>
<td align="right">0.0%</td>
<td align="right">28,806</td>
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
<td align="left">Method cache hits</td>
<td align="right">3,216,635,471</td>
<td align="right"></td>
<td align="right">3,123,304,204</td>
<td align="right"></td>
<td align="right">-2.9%</td>
</tr>
<tr>
<td align="left">Method cache dunder misses</td>
<td align="right">14,712,669</td>
<td align="right"></td>
<td align="right">14,898,366</td>
<td align="right"></td>
<td align="right">1.3%</td>
</tr>
<tr>
<td align="left">Method cache collisions</td>
<td align="right">84,368,584</td>
<td align="right"></td>
<td align="right">84,885,949</td>
<td align="right"></td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">Method cache misses</td>
<td align="right">77,402,360</td>
<td align="right"></td>
<td align="right">77,732,822</td>
<td align="right"></td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">Allocations from freelist</td>
<td align="right">6,732,816,191</td>
<td align="right">36.6%</td>
<td align="right">6,705,941,223</td>
<td align="right">36.5%</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">Frees to freelist</td>
<td align="right">6,734,737,916</td>
<td align="right"></td>
<td align="right">6,707,857,453</td>
<td align="right"></td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">Increfs</td>
<td align="right">26,572,921,713</td>
<td align="right">22.3%</td>
<td align="right">26,507,427,367</td>
<td align="right">22.2%</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">Interpreter increfs</td>
<td align="right">92,774,268,182</td>
<td align="right">77.7%</td>
<td align="right">92,878,933,844</td>
<td align="right">77.8%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">Decrefs</td>
<td align="right">29,578,597,871</td>
<td align="right">21.6%</td>
<td align="right">29,555,561,677</td>
<td align="right">21.6%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">Interpreter decrefs</td>
<td align="right">107,076,514,457</td>
<td align="right">78.4%</td>
<td align="right">107,111,853,289</td>
<td align="right">78.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Method cache dunder hits</td>
<td align="right">3,525,648,346</td>
<td align="right"></td>
<td align="right">3,525,018,570</td>
<td align="right"></td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">Allocations over 4 kbytes</td>
<td align="right">21,235,374</td>
<td align="right">0.1%</td>
<td align="right">21,235,942</td>
<td align="right">0.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Inline values</td>
<td align="right">183,238,526</td>
<td align="right"></td>
<td align="right">183,233,791</td>
<td align="right"></td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">Allocations to 512 bytes</td>
<td align="right">11,526,232,755</td>
<td align="right">62.7%</td>
<td align="right">11,526,364,883</td>
<td align="right">62.8%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Allocations</td>
<td align="right">11,652,249,169</td>
<td align="right">63.4%</td>
<td align="right">11,652,380,737</td>
<td align="right">63.5%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Allocations to 4 kbytes</td>
<td align="right">104,781,040</td>
<td align="right">0.6%</td>
<td align="right">104,779,912</td>
<td align="right">0.6%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">Frees</td>
<td align="right">11,978,146,628</td>
<td align="right"></td>
<td align="right">11,978,154,383</td>
<td align="right"></td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Materialize dict (on request)</td>
<td align="right">3,358,423</td>
<td align="right">1.8%</td>
<td align="right">3,358,423</td>
<td align="right">1.8%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Materialize dict (new key)</td>
<td align="right">133,555</td>
<td align="right">0.1%</td>
<td align="right">133,555</td>
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
<td align="right">115,370,970</td>
<td align="right">17,087,077,482</td>
<td align="right">0</td>
<td align="right">115,324,213</td>
<td align="right">17,088,159,120</td>
</tr>
<tr>
<td align="right">2</td>
<td align="right">0</td>
<td align="right">10,755,240</td>
<td align="right">6,963,227,260</td>
<td align="right">0</td>
<td align="right">10,754,880</td>
<td align="right">6,960,151,200</td>
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
<td align="right">14,388,579</td>
<td align="right">27.6%</td>
<td align="right">132,359</td>
<td align="right">20.3%</td>
<td align="right">-99.1%</td>
</tr>
<tr>
<td align="left">
Trace too short
<details>
<summary>ⓘ</summary>

A potential trace is abandoced because it it too short.
</details>
</td>
<td align="right">52,021,387</td>
<td align="right">99.8%</td>
<td align="right">544,619</td>
<td align="right">83.4%</td>
<td align="right">-99.0%</td>
</tr>
<tr>
<td align="left">
Optimization attempts
<details>
<summary>ⓘ</summary>

The number of times a potential trace is identified.  Specifically, this occurs in the JUMP BACKWARD instruction when the counter reaches a threshold.
</details>
</td>
<td align="right">52,138,540</td>
<td align="right"></td>
<td align="right">652,908</td>
<td align="right"></td>
<td align="right">-98.7%</td>
</tr>
<tr>
<td align="left">
Inner loop found
<details>
<summary>ⓘ</summary>

A trace is truncated because it has an inner loop
</details>
</td>
<td align="right">316,324</td>
<td align="right">0.6%</td>
<td align="right">16,142</td>
<td align="right">2.5%</td>
<td align="right">-94.9%</td>
</tr>
<tr>
<td align="left">
Trace stack overflow
<details>
<summary>ⓘ</summary>

A trace is truncated because it would require more than 5 stack frames.
</details>
</td>
<td align="right">422</td>
<td align="right">0.0%</td>
<td align="right">813</td>
<td align="right">0.1%</td>
<td align="right">92.7%</td>
</tr>
<tr>
<td align="left">
Low confidence
<details>
<summary>ⓘ</summary>

A trace is abandoned because the likelihood of the jump to top being taken is too low.
</details>
</td>
<td align="right">7,259</td>
<td align="right">0.0%</td>
<td align="right">6,701</td>
<td align="right">1.0%</td>
<td align="right">-7.7%</td>
</tr>
<tr>
<td align="left">
Executors invalidated
<details>
<summary>ⓘ</summary>

The number of executors that were invalidated due to watched dictionary changes.
</details>
</td>
<td align="right">6,000</td>
<td align="right">5.1%</td>
<td align="right">5,540</td>
<td align="right">5.1%</td>
<td align="right">-7.7%</td>
</tr>
<tr>
<td align="left">
Traces created
<details>
<summary>ⓘ</summary>

The number of traces that were successfully created.
</details>
</td>
<td align="right">117,153</td>
<td align="right">0.2%</td>
<td align="right">108,289</td>
<td align="right">16.6%</td>
<td align="right">-7.6%</td>
</tr>
<tr>
<td align="left">
Uops executed
<details>
<summary>ⓘ</summary>

The total number of uops (micro-operations) that were executed
</details>
</td>
<td align="right">181,537,283,117</td>
<td align="right">2,879.5%</td>
<td align="right">183,663,206,047</td>
<td align="right">2,896.7%</td>
<td align="right">1.2%</td>
</tr>
<tr>
<td align="left">
Traces executed
<details>
<summary>ⓘ</summary>

The number of traces that were executed
</details>
</td>
<td align="right">6,304,456,616</td>
<td align="right"></td>
<td align="right">6,340,503,016</td>
<td align="right"></td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">
Recursive call
<details>
<summary>ⓘ</summary>

A trace is truncated because it has a recursive call.
</details>
</td>
<td align="right">1,354</td>
<td align="right">0.0%</td>
<td align="right">1,351</td>
<td align="right">0.2%</td>
<td align="right">-0.2%</td>
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
<td align="right">114,933</td>
<td align="right">98.1%</td>
<td align="right">106,149</td>
<td align="right">98.0%</td>
<td align="right">-7.6%</td>
</tr>
<tr>
<td align="left">
Optimizer attempts
<details>
<summary>ⓘ</summary>

The number of times the trace optimizer (_Py_uop_analyze_and_optimize) was run.
</details>
</td>
<td align="right">117,153</td>
<td align="right"></td>
<td align="right">108,289</td>
<td align="right"></td>
<td align="right">-7.6%</td>
</tr>
<tr>
<td align="left">
Remove globals incorrect keys
<details>
<summary>ⓘ</summary>

The keys in the globals dictionary aren't what was expected
</details>
</td>
<td align="right">2,160</td>
<td align="right">1.8%</td>
<td align="right">2,100</td>
<td align="right">1.9%</td>
<td align="right">-2.8%</td>
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
<td align="right">3,264</td>
<td align="right">2.8%</td>
<td align="right">2,871</td>
<td align="right">2.7%</td>
<td align="right">-12.0%</td>
</tr>
<tr>
<td align="left"><= 16</td>
<td align="right">19,436</td>
<td align="right">16.6%</td>
<td align="right">16,801</td>
<td align="right">15.5%</td>
<td align="right">-13.6%</td>
</tr>
<tr>
<td align="left"><= 32</td>
<td align="right">43,815</td>
<td align="right">37.4%</td>
<td align="right">41,713</td>
<td align="right">38.5%</td>
<td align="right">-4.8%</td>
</tr>
<tr>
<td align="left"><= 64</td>
<td align="right">28,516</td>
<td align="right">24.3%</td>
<td align="right">26,528</td>
<td align="right">24.5%</td>
<td align="right">-7.0%</td>
</tr>
<tr>
<td align="left"><= 128</td>
<td align="right">16,430</td>
<td align="right">14.0%</td>
<td align="right">14,930</td>
<td align="right">13.8%</td>
<td align="right">-9.1%</td>
</tr>
<tr>
<td align="left"><= 256</td>
<td align="right">4,905</td>
<td align="right">4.2%</td>
<td align="right">4,581</td>
<td align="right">4.2%</td>
<td align="right">-6.6%</td>
</tr>
<tr>
<td align="left"><= 512</td>
<td align="right">787</td>
<td align="right">0.7%</td>
<td align="right">865</td>
<td align="right">0.8%</td>
<td align="right">9.9%</td>
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
<td align="right">81</td>
<td align="right">0.1%</td>
<td align="right">80</td>
<td align="right">0.1%</td>
<td align="right">-1.2%</td>
</tr>
<tr>
<td align="left"><= 8</td>
<td align="right">9,442</td>
<td align="right">8.1%</td>
<td align="right">8,173</td>
<td align="right">7.5%</td>
<td align="right">-13.4%</td>
</tr>
<tr>
<td align="left"><= 16</td>
<td align="right">34,612</td>
<td align="right">29.5%</td>
<td align="right">31,567</td>
<td align="right">29.2%</td>
<td align="right">-8.8%</td>
</tr>
<tr>
<td align="left"><= 32</td>
<td align="right">38,768</td>
<td align="right">33.1%</td>
<td align="right">37,004</td>
<td align="right">34.2%</td>
<td align="right">-4.6%</td>
</tr>
<tr>
<td align="left"><= 64</td>
<td align="right">21,310</td>
<td align="right">18.2%</td>
<td align="right">19,157</td>
<td align="right">17.7%</td>
<td align="right">-10.1%</td>
</tr>
<tr>
<td align="left"><= 128</td>
<td align="right">8,388</td>
<td align="right">7.2%</td>
<td align="right">7,919</td>
<td align="right">7.3%</td>
<td align="right">-5.6%</td>
</tr>
<tr>
<td align="left"><= 256</td>
<td align="right">2,072</td>
<td align="right">1.8%</td>
<td align="right">2,029</td>
<td align="right">1.9%</td>
<td align="right">-2.1%</td>
</tr>
<tr>
<td align="left"><= 512</td>
<td align="right">260</td>
<td align="right">0.2%</td>
<td align="right">220</td>
<td align="right">0.2%</td>
<td align="right">-15.4%</td>
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
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 4</td>
<td align="right">161,724,246</td>
<td align="right">2.6%</td>
<td align="right">164,936,861</td>
<td align="right">2.6%</td>
<td align="right">2.0%</td>
</tr>
<tr>
<td align="left"><= 8</td>
<td align="right">833,230,611</td>
<td align="right">13.2%</td>
<td align="right">1,082,881,413</td>
<td align="right">17.1%</td>
<td align="right">30.0%</td>
</tr>
<tr>
<td align="left"><= 16</td>
<td align="right">1,352,315,187</td>
<td align="right">21.5%</td>
<td align="right">1,171,457,007</td>
<td align="right">18.5%</td>
<td align="right">-13.4%</td>
</tr>
<tr>
<td align="left"><= 32</td>
<td align="right">1,224,062,096</td>
<td align="right">19.4%</td>
<td align="right">1,213,639,476</td>
<td align="right">19.1%</td>
<td align="right">-0.9%</td>
</tr>
<tr>
<td align="left"><= 64</td>
<td align="right">592,106,713</td>
<td align="right">9.4%</td>
<td align="right">606,414,230</td>
<td align="right">9.6%</td>
<td align="right">2.4%</td>
</tr>
<tr>
<td align="left"><= 128</td>
<td align="right">311,469,239</td>
<td align="right">4.9%</td>
<td align="right">280,261,580</td>
<td align="right">4.4%</td>
<td align="right">-10.0%</td>
</tr>
<tr>
<td align="left"><= 256</td>
<td align="right">122,115,647</td>
<td align="right">1.9%</td>
<td align="right">145,836,087</td>
<td align="right">2.3%</td>
<td align="right">19.4%</td>
</tr>
<tr>
<td align="left"><= 512</td>
<td align="right">17,328,109</td>
<td align="right">0.3%</td>
<td align="right">17,326,310</td>
<td align="right">0.3%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left"><= 1,024</td>
<td align="right">7,562,433</td>
<td align="right">0.1%</td>
<td align="right">7,562,528</td>
<td align="right">0.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left"><= 2,048</td>
<td align="right">17,828,906</td>
<td align="right">0.3%</td>
<td align="right">17,832,473</td>
<td align="right">0.3%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left"><= 4,096</td>
<td align="right">677,628</td>
<td align="right">0.0%</td>
<td align="right">681,714</td>
<td align="right">0.0%</td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left"><= 8,192</td>
<td align="right">739,459</td>
<td align="right">0.0%</td>
<td align="right">739,528</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left"><= 16,384</td>
<td align="right">263,681</td>
<td align="right">0.0%</td>
<td align="right">263,661</td>
<td align="right">0.0%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left"><= 32,768</td>
<td align="right">41,360</td>
<td align="right">0.0%</td>
<td align="right">41,360</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left"><= 65,536</td>
<td align="right">13,202</td>
<td align="right">0.0%</td>
<td align="right">13,202</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left"><= 131,072</td>
<td align="right">958</td>
<td align="right">0.0%</td>
<td align="right">958</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left"><= 262,144</td>
<td align="right">2,160</td>
<td align="right">0.0%</td>
<td align="right">2,160</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left"><= 524,288</td>
<td align="right">461</td>
<td align="right">0.0%</td>
<td align="right">464</td>
<td align="right">0.0%</td>
<td align="right">0.7%</td>
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
<td align="right">200</td>
<td align="right">0.0%</td>
<td align="right">203</td>
<td align="right">0.0%</td>
<td align="right">1.5%</td>
</tr>
<tr>
<td align="left"><= 4,194,304</td>
<td align="right">280</td>
<td align="right">0.0%</td>
<td align="right">277</td>
<td align="right">0.0%</td>
<td align="right">-1.1%</td>
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
<td align="left">_LOAD_ATTR_CLASS_1</td>
<td align="right">3,840</td>
<td align="right">86,360</td>
<td align="right">2,149.0%</td>
</tr>
<tr>
<td align="left">_GUARD_BUILTINS_VERSION</td>
<td align="right">91,276</td>
<td align="right">38,636</td>
<td align="right">-57.7%</td>
</tr>
<tr>
<td align="left">_UNARY_NEGATIVE</td>
<td align="right">48,761,814</td>
<td align="right">25,045,781</td>
<td align="right">-48.6%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_4</td>
<td align="right">352,322,712</td>
<td align="right">448,283,731</td>
<td align="right">27.2%</td>
</tr>
<tr>
<td align="left">_CHECK_ATTR_CLASS</td>
<td align="right">19,931,620</td>
<td align="right">25,078,333</td>
<td align="right">25.8%</td>
</tr>
<tr>
<td align="left">_LOAD_GLOBAL_MODULE</td>
<td align="right">59,324,968</td>
<td align="right">44,267,468</td>
<td align="right">-25.4%</td>
</tr>
<tr>
<td align="left">_CALL_TYPE_1</td>
<td align="right">189,572,142</td>
<td align="right">237,559,238</td>
<td align="right">25.3%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_CLASS_0</td>
<td align="right">18,769,274</td>
<td align="right">23,405,957</td>
<td align="right">24.7%</td>
</tr>
<tr>
<td align="left">_GUARD_GLOBALS_VERSION</td>
<td align="right">65,969,604</td>
<td align="right">50,855,144</td>
<td align="right">-22.9%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_NONDESCRIPTOR_NO_DICT</td>
<td align="right">20,158,504</td>
<td align="right">24,529,415</td>
<td align="right">21.7%</td>
</tr>
<tr>
<td align="left">_ITER_NEXT_TUPLE</td>
<td align="right">264,265,930</td>
<td align="right">312,306,134</td>
<td align="right">18.2%</td>
</tr>
<tr>
<td align="left">_REPLACE_WITH_TRUE</td>
<td align="right">27,646,191</td>
<td align="right">32,343,438</td>
<td align="right">17.0%</td>
</tr>
<tr>
<td align="left">_LOAD_CONST_INLINE_BORROW_WITH_NULL</td>
<td align="right">319,932,947</td>
<td align="right">366,703,848</td>
<td align="right">14.6%</td>
</tr>
<tr>
<td align="left">_UNPACK_SEQUENCE_TUPLE</td>
<td align="right">164,605,429</td>
<td align="right">188,552,249</td>
<td align="right">14.5%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_BOOL</td>
<td align="right">1,707,480,658</td>
<td align="right">1,936,912,291</td>
<td align="right">13.4%</td>
</tr>
<tr>
<td align="left">_COMPARE_OP</td>
<td align="right">105,260,838</td>
<td align="right">92,870,655</td>
<td align="right">-11.8%</td>
</tr>
<tr>
<td align="left">_GUARD_NOT_EXHAUSTED_TUPLE</td>
<td align="right">415,682,820</td>
<td align="right">463,738,475</td>
<td align="right">11.6%</td>
</tr>
<tr>
<td align="left">_ITER_CHECK_TUPLE</td>
<td align="right">492,891,574</td>
<td align="right">540,951,400</td>
<td align="right">9.8%</td>
</tr>
<tr>
<td align="left">_EXIT_TRACE</td>
<td align="right">2,518,153,847</td>
<td align="right">2,745,222,408</td>
<td align="right">9.0%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_5</td>
<td align="right">598,958,280</td>
<td align="right">647,272,346</td>
<td align="right">8.1%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR</td>
<td align="right">1,189,259,368</td>
<td align="right">1,096,169,533</td>
<td align="right">-7.8%</td>
</tr>
<tr>
<td align="left">_GUARD_DORV_VALUES_INST_ATTR_FROM_DICT</td>
<td align="right">978,126,519</td>
<td align="right">1,044,905,944</td>
<td align="right">6.8%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_INSTANCE_VALUE_0</td>
<td align="right">2,006,046,990</td>
<td align="right">1,872,670,182</td>
<td align="right">-6.6%</td>
</tr>
<tr>
<td align="left">_CHECK_MANAGED_OBJECT_HAS_VALUES</td>
<td align="right">2,009,852,003</td>
<td align="right">1,876,455,638</td>
<td align="right">-6.6%</td>
</tr>
<tr>
<td align="left">_CHECK_CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">78,931,881</td>
<td align="right">73,701,809</td>
<td align="right">-6.6%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">78,864,081</td>
<td align="right">73,648,369</td>
<td align="right">-6.6%</td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_FAST</td>
<td align="right">742,022,794</td>
<td align="right">789,872,607</td>
<td align="right">6.4%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_3</td>
<td align="right">53,297,891</td>
<td align="right">56,636,458</td>
<td align="right">6.3%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_6</td>
<td align="right">392,830,349</td>
<td align="right">417,228,007</td>
<td align="right">6.2%</td>
</tr>
<tr>
<td align="left">_STORE_ATTR</td>
<td align="right">54,648,696</td>
<td align="right">51,333,313</td>
<td align="right">-6.1%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_MULTIPLY_FLOAT</td>
<td align="right">1,160,924,560</td>
<td align="right">1,092,307,841</td>
<td align="right">-5.9%</td>
</tr>
<tr>
<td align="left">_POP_FRAME</td>
<td align="right">520,785,692</td>
<td align="right">550,704,158</td>
<td align="right">5.7%</td>
</tr>
<tr>
<td align="left">_RESUME_CHECK</td>
<td align="right">1,245,341,781</td>
<td align="right">1,314,118,253</td>
<td align="right">5.5%</td>
</tr>
<tr>
<td align="left">_GUARD_BOTH_FLOAT</td>
<td align="right">1,576,743,139</td>
<td align="right">1,491,022,988</td>
<td align="right">-5.4%</td>
</tr>
<tr>
<td align="left">_POP_TOP_LOAD_CONST_INLINE_BORROW</td>
<td align="right">827,831</td>
<td align="right">872,577</td>
<td align="right">5.4%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">862,148,441</td>
<td align="right">908,474,308</td>
<td align="right">5.4%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_TRUE_POP</td>
<td align="right">2,447,158,138</td>
<td align="right">2,571,794,082</td>
<td align="right">5.1%</td>
</tr>
<tr>
<td align="left">_CHECK_VALIDITY_AND_SET_IP</td>
<td align="right">2,389,224,272</td>
<td align="right">2,269,822,147</td>
<td align="right">-5.0%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_5</td>
<td align="right">1,915,717,509</td>
<td align="right">2,010,675,351</td>
<td align="right">5.0%</td>
</tr>
<tr>
<td align="left">_GUARD_KEYS_VERSION</td>
<td align="right">955,757,341</td>
<td align="right">1,001,736,162</td>
<td align="right">4.8%</td>
</tr>
<tr>
<td align="left">_PUSH_FRAME</td>
<td align="right">1,454,604,879</td>
<td align="right">1,524,433,346</td>
<td align="right">4.8%</td>
</tr>
<tr>
<td align="left">_SAVE_RETURN_OFFSET</td>
<td align="right">1,454,604,879</td>
<td align="right">1,524,433,346</td>
<td align="right">4.8%</td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION_EXACT_ARGS</td>
<td align="right">1,511,905,436</td>
<td align="right">1,582,448,135</td>
<td align="right">4.7%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_4</td>
<td align="right">1,848,215,339</td>
<td align="right">1,933,089,095</td>
<td align="right">4.6%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_NOT_NONE_POP</td>
<td align="right">162,046,311</td>
<td align="right">154,785,918</td>
<td align="right">-4.5%</td>
</tr>
<tr>
<td align="left">_BINARY_OP</td>
<td align="right">893,310,924</td>
<td align="right">854,776,963</td>
<td align="right">-4.3%</td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_O</td>
<td align="right">590,114,436</td>
<td align="right">614,111,543</td>
<td align="right">4.1%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_FALSE_POP</td>
<td align="right">5,100,330,447</td>
<td align="right">5,301,970,690</td>
<td align="right">4.0%</td>
</tr>
<tr>
<td align="left">_TO_BOOL</td>
<td align="right">245,844,315</td>
<td align="right">236,133,802</td>
<td align="right">-3.9%</td>
</tr>
<tr>
<td align="left">_LOAD_CONST_INLINE</td>
<td align="right">1,187,306,520</td>
<td align="right">1,233,336,913</td>
<td align="right">3.9%</td>
</tr>
<tr>
<td align="left">_CONTAINS_OP_SET</td>
<td align="right">1,423,270,558</td>
<td align="right">1,477,470,283</td>
<td align="right">3.8%</td>
</tr>
<tr>
<td align="left">_CHECK_ATTR_WITH_HINT</td>
<td align="right">94,469,252</td>
<td align="right">97,861,813</td>
<td align="right">3.6%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST</td>
<td align="right">5,128,468,928</td>
<td align="right">5,312,163,645</td>
<td align="right">3.6%</td>
</tr>
<tr>
<td align="left">_DEOPT</td>
<td align="right">1,159,100,394</td>
<td align="right">1,118,262,861</td>
<td align="right">-3.5%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_2</td>
<td align="right">2,588,926,601</td>
<td align="right">2,679,151,090</td>
<td align="right">3.5%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_WITH_HINT</td>
<td align="right">94,467,052</td>
<td align="right">97,694,192</td>
<td align="right">3.4%</td>
</tr>
<tr>
<td align="left">_CHECK_PERIODIC</td>
<td align="right">2,059,760,041</td>
<td align="right">2,128,729,356</td>
<td align="right">3.3%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_1</td>
<td align="right">542,629,752</td>
<td align="right">524,541,647</td>
<td align="right">-3.3%</td>
</tr>
<tr>
<td align="left">_PUSH_NULL</td>
<td align="right">708,099,725</td>
<td align="right">731,618,151</td>
<td align="right">3.3%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_STR</td>
<td align="right">26,758,879</td>
<td align="right">27,645,552</td>
<td align="right">3.3%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_0</td>
<td align="right">392,614,961</td>
<td align="right">379,728,693</td>
<td align="right">-3.3%</td>
</tr>
<tr>
<td align="left">_SIDE_EXIT</td>
<td align="right">3,481,892,694</td>
<td align="right">3,591,143,357</td>
<td align="right">3.1%</td>
</tr>
<tr>
<td align="left">_ITER_CHECK_LIST</td>
<td align="right">1,547,751,446</td>
<td align="right">1,500,464,232</td>
<td align="right">-3.1%</td>
</tr>
<tr>
<td align="left">_GET_YIELD_FROM_ITER</td>
<td align="right">185,480</td>
<td align="right">179,880</td>
<td align="right">-3.0%</td>
</tr>
<tr>
<td align="left">_STORE_ATTR_SLOT</td>
<td align="right">128,435,779</td>
<td align="right">124,670,305</td>
<td align="right">-2.9%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBTRACT_FLOAT</td>
<td align="right">393,785,140</td>
<td align="right">382,602,700</td>
<td align="right">-2.8%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_SLOT_0</td>
<td align="right">684,663,756</td>
<td align="right">703,989,660</td>
<td align="right">2.8%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_3</td>
<td align="right">3,016,952,721</td>
<td align="right">3,101,685,228</td>
<td align="right">2.8%</td>
</tr>
<tr>
<td align="left">_CHECK_STACK_SPACE_OPERAND</td>
<td align="right">850,201,964</td>
<td align="right">874,062,769</td>
<td align="right">2.8%</td>
</tr>
<tr>
<td align="left">_LOAD_CONST_INLINE_WITH_NULL</td>
<td align="right">1,612,586,602</td>
<td align="right">1,656,443,430</td>
<td align="right">2.7%</td>
</tr>
<tr>
<td align="left">_BINARY_SUBSCR_LIST_INT</td>
<td align="right">1,080,083,899</td>
<td align="right">1,052,941,107</td>
<td align="right">-2.5%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_CHECK</td>
<td align="right">258,140</td>
<td align="right">251,861</td>
<td align="right">-2.4%</td>
</tr>
<tr>
<td align="left">_GUARD_TYPE_VERSION</td>
<td align="right">5,474,244,948</td>
<td align="right">5,344,571,158</td>
<td align="right">-2.4%</td>
</tr>
<tr>
<td align="left">_CALL_TUPLE_1</td>
<td align="right">586,240</td>
<td align="right">572,540</td>
<td align="right">-2.3%</td>
</tr>
<tr>
<td align="left">_POP_TOP</td>
<td align="right">682,063,136</td>
<td align="right">697,268,651</td>
<td align="right">2.2%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_MODULE</td>
<td align="right">9,385,049</td>
<td align="right">9,200,310</td>
<td align="right">-2.0%</td>
</tr>
<tr>
<td align="left">_CHECK_ATTR_MODULE</td>
<td align="right">9,388,549</td>
<td align="right">9,203,750</td>
<td align="right">-2.0%</td>
</tr>
<tr>
<td align="left">_COLD_EXIT</td>
<td align="right">1,662,973,400</td>
<td align="right">1,630,610,884</td>
<td align="right">-1.9%</td>
</tr>
<tr>
<td align="left">_LOAD_SUPER_ATTR_METHOD</td>
<td align="right">97,617</td>
<td align="right">95,777</td>
<td align="right">-1.9%</td>
</tr>
<tr>
<td align="left">_LOAD_GLOBAL</td>
<td align="right">192,437,245</td>
<td align="right">188,838,722</td>
<td align="right">-1.9%</td>
</tr>
<tr>
<td align="left">_BINARY_SUBSCR_DICT</td>
<td align="right">263,121,120</td>
<td align="right">258,330,241</td>
<td align="right">-1.8%</td>
</tr>
<tr>
<td align="left">_COPY_FREE_VARS</td>
<td align="right">48,289,826</td>
<td align="right">49,046,267</td>
<td align="right">1.6%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_4</td>
<td align="right">666,681,546</td>
<td align="right">656,308,968</td>
<td align="right">-1.6%</td>
</tr>
<tr>
<td align="left">_CONVERT_VALUE</td>
<td align="right">798,700</td>
<td align="right">786,540</td>
<td align="right">-1.5%</td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION</td>
<td align="right">1,293,051,043</td>
<td align="right">1,273,789,380</td>
<td align="right">-1.5%</td>
</tr>
<tr>
<td align="left">_START_EXECUTOR</td>
<td align="right">4,641,483,216</td>
<td align="right">4,709,892,132</td>
<td align="right">1.5%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_2</td>
<td align="right">103,996,981</td>
<td align="right">105,525,758</td>
<td align="right">1.5%</td>
</tr>
<tr>
<td align="left">_STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">101,236,041</td>
<td align="right">102,695,921</td>
<td align="right">1.4%</td>
</tr>
<tr>
<td align="left">_GUARD_DORV_NO_DICT</td>
<td align="right">102,545,261</td>
<td align="right">104,003,681</td>
<td align="right">1.4%</td>
</tr>
<tr>
<td align="left">_BUILD_CONST_KEY_MAP</td>
<td align="right">80,781</td>
<td align="right">79,650</td>
<td align="right">-1.4%</td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_O</td>
<td align="right">22,532,250</td>
<td align="right">22,226,087</td>
<td align="right">-1.4%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_NONE_POP</td>
<td align="right">42,285,482</td>
<td align="right">41,725,556</td>
<td align="right">-1.3%</td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_CLASS</td>
<td align="right">57,537,674</td>
<td align="right">56,800,967</td>
<td align="right">-1.3%</td>
</tr>
<tr>
<td align="left">_STORE_FAST</td>
<td align="right">2,837,682,091</td>
<td align="right">2,873,843,238</td>
<td align="right">1.3%</td>
</tr>
<tr>
<td align="left">_CHECK_VALIDITY</td>
<td align="right">17,587,623,671</td>
<td align="right">17,798,211,091</td>
<td align="right">1.2%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">811,805,427</td>
<td align="right">820,925,293</td>
<td align="right">1.1%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_ADD_FLOAT</td>
<td align="right">545,839,980</td>
<td align="right">539,783,780</td>
<td align="right">-1.1%</td>
</tr>
<tr>
<td align="left">_CALL_LEN</td>
<td align="right">196,395,519</td>
<td align="right">194,322,516</td>
<td align="right">-1.1%</td>
</tr>
<tr>
<td align="left">_CONTAINS_OP</td>
<td align="right">107,997,032</td>
<td align="right">106,929,863</td>
<td align="right">-1.0%</td>
</tr>
<tr>
<td align="left">_SET_IP</td>
<td align="right">16,046,649,348</td>
<td align="right">16,190,753,381</td>
<td align="right">0.9%</td>
</tr>
<tr>
<td align="left">_ERROR_POP_N</td>
<td align="right">490,128</td>
<td align="right">485,914</td>
<td align="right">-0.9%</td>
</tr>
<tr>
<td align="left">_LOAD_GLOBAL_BUILTINS</td>
<td align="right">6,644,636</td>
<td align="right">6,587,676</td>
<td align="right">-0.9%</td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">227,390,638</td>
<td align="right">225,547,757</td>
<td align="right">-0.8%</td>
</tr>
<tr>
<td align="left">_CALL_ISINSTANCE</td>
<td align="right">314,933,299</td>
<td align="right">312,479,076</td>
<td align="right">-0.8%</td>
</tr>
<tr>
<td align="left">_BINARY_SLICE</td>
<td align="right">120,874,549</td>
<td align="right">120,022,077</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_ADD_UNICODE</td>
<td align="right">22,895,083</td>
<td align="right">23,051,863</td>
<td align="right">0.7%</td>
</tr>
<tr>
<td align="left">_LIST_APPEND</td>
<td align="right">178,885,433</td>
<td align="right">180,018,626</td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">_SET_ADD</td>
<td align="right">1,466,584</td>
<td align="right">1,457,528</td>
<td align="right">-0.6%</td>
</tr>
<tr>
<td align="left">_CHECK_STACK_SPACE</td>
<td align="right">155,336,232</td>
<td align="right">156,243,338</td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">_SET_FUNCTION_ATTRIBUTE</td>
<td align="right">46,821,599</td>
<td align="right">47,068,527</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">_DELETE_SUBSCR</td>
<td align="right">1,445,940</td>
<td align="right">1,438,480</td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">_BUILD_MAP</td>
<td align="right">9,950,834</td>
<td align="right">9,899,959</td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">_BINARY_SUBSCR_STR_INT</td>
<td align="right">1,209,423,285</td>
<td align="right">1,215,369,666</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">_BUILD_STRING</td>
<td align="right">3,325,488</td>
<td align="right">3,309,660</td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">_STORE_DEREF</td>
<td align="right">2,944,426</td>
<td align="right">2,930,525</td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_AND_CLEAR</td>
<td align="right">16,308,231</td>
<td align="right">16,235,161</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">_LOAD_CONST_INLINE_BORROW</td>
<td align="right">8,816,454,397</td>
<td align="right">8,855,672,009</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_NONE</td>
<td align="right">173,299,535</td>
<td align="right">174,051,058</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">_BINARY_SUBSCR_TUPLE_INT</td>
<td align="right">148,030,433</td>
<td align="right">147,409,364</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_3</td>
<td align="right">628,645,867</td>
<td align="right">631,181,991</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBTRACT_INT</td>
<td align="right">430,940,764</td>
<td align="right">429,323,291</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">_MAKE_FUNCTION</td>
<td align="right">60,425,676</td>
<td align="right">60,650,904</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_6</td>
<td align="right">1,247,136,893</td>
<td align="right">1,242,505,879</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">_BUILD_LIST</td>
<td align="right">245,276,601</td>
<td align="right">246,174,471</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_FAST_WITH_KEYWORDS</td>
<td align="right">154,293,088</td>
<td align="right">153,757,663</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_INSTANCE_VALUE_1</td>
<td align="right">3,651,373</td>
<td align="right">3,664,036</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">_MAKE_CELL</td>
<td align="right">6,689,649</td>
<td align="right">6,669,825</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">183,443,360</td>
<td align="right">183,950,906</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">_CHECK_ATTR_METHOD_LAZY_DICT</td>
<td align="right">97,129,608</td>
<td align="right">97,397,465</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_METHOD_LAZY_DICT</td>
<td align="right">97,129,608</td>
<td align="right">97,397,465</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS</td>
<td align="right">9,742,582</td>
<td align="right">9,717,059</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">_BUILD_TUPLE</td>
<td align="right">372,268,700</td>
<td align="right">373,236,767</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">_FORMAT_SIMPLE</td>
<td align="right">9,581,253</td>
<td align="right">9,557,665</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_LIST</td>
<td align="right">56,330,342</td>
<td align="right">56,460,053</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_0</td>
<td align="right">5,312,063,403</td>
<td align="right">5,324,291,588</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">_IS_OP</td>
<td align="right">333,077,289</td>
<td align="right">332,316,387</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_1</td>
<td align="right">6,201,587,770</td>
<td align="right">6,214,698,194</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_1</td>
<td align="right">1,849,736,586</td>
<td align="right">1,853,288,719</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">_GET_ITER</td>
<td align="right">241,110,594</td>
<td align="right">241,564,110</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">_GUARD_BOTH_UNICODE</td>
<td align="right">967,581,625</td>
<td align="right">965,838,815</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">_CONTAINS_OP_DICT</td>
<td align="right">360,706,396</td>
<td align="right">360,145,388</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">_COMPARE_OP_STR</td>
<td align="right">1,827,283,822</td>
<td align="right">1,824,994,577</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">_COMPARE_OP_INT</td>
<td align="right">936,160,023</td>
<td align="right">935,234,331</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">_STORE_SUBSCR_DICT</td>
<td align="right">124,790,163</td>
<td align="right">124,670,994</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">_BINARY_SUBSCR</td>
<td align="right">1,144,583,108</td>
<td align="right">1,143,545,529</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right">88,620,587</td>
<td align="right">88,699,067</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">_SWAP</td>
<td align="right">1,130,019,744</td>
<td align="right">1,130,958,407</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">_GUARD_NOT_EXHAUSTED_RANGE</td>
<td align="right">749,892,292</td>
<td align="right">749,342,322</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">_ITER_CHECK_RANGE</td>
<td align="right">751,250,052</td>
<td align="right">750,700,082</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_INT</td>
<td align="right">194,666,161</td>
<td align="right">194,792,377</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">_LOAD_DEREF</td>
<td align="right">444,852,980</td>
<td align="right">445,133,022</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_2</td>
<td align="right">711,053,632</td>
<td align="right">711,498,047</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">_GUARD_BOTH_INT</td>
<td align="right">3,154,663,683</td>
<td align="right">3,156,583,943</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">_UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">620,126,064</td>
<td align="right">620,483,559</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">_DICT_MERGE</td>
<td align="right">7,207,149</td>
<td align="right">7,203,012</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">_FOR_ITER_TIER_TWO</td>
<td align="right">397,481,727</td>
<td align="right">397,705,920</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">_ITER_NEXT_LIST</td>
<td align="right">1,205,195,954</td>
<td align="right">1,205,812,854</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_FAST_WITH_KEYWORDS</td>
<td align="right">21,543,904</td>
<td align="right">21,534,304</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">_UNARY_NOT</td>
<td align="right">62,237,657</td>
<td align="right">62,210,416</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">_GUARD_NOT_EXHAUSTED_LIST</td>
<td align="right">1,485,492,310</td>
<td align="right">1,486,112,002</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_STORE_SUBSCR</td>
<td align="right">314,272,305</td>
<td align="right">314,167,933</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">_COPY</td>
<td align="right">1,252,165,036</td>
<td align="right">1,252,553,940</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_0</td>
<td align="right">204,685,282</td>
<td align="right">204,626,452</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_7</td>
<td align="right">1,205,131,184</td>
<td align="right">1,204,872,735</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">_UNARY_INVERT</td>
<td align="right">12,537,420</td>
<td align="right">12,534,740</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">_UNPACK_SEQUENCE</td>
<td align="right">1,554,489</td>
<td align="right">1,554,759</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_CALL_STR_1</td>
<td align="right">68,933,774</td>
<td align="right">68,922,154</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_MULTIPLY_INT</td>
<td align="right">184,995,274</td>
<td align="right">184,971,382</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">_STORE_SUBSCR_LIST_INT</td>
<td align="right">478,927,182</td>
<td align="right">478,865,502</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">_LIST_EXTEND</td>
<td align="right">96,960,211</td>
<td align="right">96,948,653</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_7</td>
<td align="right">3,377,208,481</td>
<td align="right">3,376,853,400</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">_COMPARE_OP_FLOAT</td>
<td align="right">70,082,753</td>
<td align="right">70,075,558</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">_CALL_INTRINSIC_1</td>
<td align="right">96,034,451</td>
<td align="right">96,024,853</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_ADD_INT</td>
<td align="right">2,486,238,881</td>
<td align="right">2,486,469,312</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_ITER_NEXT_RANGE</td>
<td align="right">701,816,008</td>
<td align="right">701,780,995</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">_UNPACK_SEQUENCE_LIST</td>
<td align="right">77,570,460</td>
<td align="right">77,567,260</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">_STORE_SLICE</td>
<td align="right">149,874,320</td>
<td align="right">149,868,340</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">_BUILD_SLICE</td>
<td align="right">139,785,940</td>
<td align="right">139,781,160</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">_MAP_ADD</td>
<td align="right">20,603,859</td>
<td align="right">20,603,183</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">_JUMP_TO_TOP</td>
<td align="right">2,067,243,367</td>
<td align="right">2,067,224,123</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">_GET_ANEXT</td>
<td align="right">125,514,720</td>
<td align="right">125,514,720</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_STORE_GLOBAL</td>
<td align="right">1,260,560</td>
<td align="right">1,260,560</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_STORE_NAME</td>
<td align="right">545,860</td>
<td align="right">545,860</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_FORMAT_WITH_SPEC</td>
<td align="right">440</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_UNPACK_EX</td>
<td align="right">104</td>
<td align="right">104</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


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
<td align="left">SEND</td>
<td align="right">3,928,200</td>
<td align="right">31,240</td>
<td align="right">-99.2%</td>
</tr>
<tr>
<td align="left">YIELD_VALUE</td>
<td align="right">13,610,669</td>
<td align="right">118,750</td>
<td align="right">-99.1%</td>
</tr>
<tr>
<td align="left">RETURN_GENERATOR</td>
<td align="right">4,057,727</td>
<td align="right">36,807</td>
<td align="right">-99.1%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">10,811,640</td>
<td align="right">128,161</td>
<td align="right">-98.8%</td>
</tr>
<tr>
<td align="left">CALL_KW</td>
<td align="right">2,113,372</td>
<td align="right">25,597</td>
<td align="right">-98.8%</td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">2,206,823</td>
<td align="right">32,388</td>
<td align="right">-98.5%</td>
</tr>
<tr>
<td align="left">CALL_ALLOC_AND_ENTER_INIT</td>
<td align="right">74,203</td>
<td align="right">1,446</td>
<td align="right">-98.1%</td>
</tr>
<tr>
<td align="left">CALL_PY_WITH_DEFAULTS</td>
<td align="right">430,507</td>
<td align="right">9,021</td>
<td align="right">-97.9%</td>
</tr>
<tr>
<td align="left">IMPORT_NAME</td>
<td align="right">4,383</td>
<td align="right">246</td>
<td align="right">-94.4%</td>
</tr>
<tr>
<td align="left">CALL_FUNCTION_EX</td>
<td align="right">33,140</td>
<td align="right">2,740</td>
<td align="right">-91.7%</td>
</tr>
<tr>
<td align="left">BEFORE_WITH</td>
<td align="right">3,480</td>
<td align="right">320</td>
<td align="right">-90.8%</td>
</tr>
<tr>
<td align="left">BUILD_SET</td>
<td align="right">552</td>
<td align="right">226</td>
<td align="right">-59.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_PROPERTY</td>
<td align="right">13,645</td>
<td align="right">6,794</td>
<td align="right">-50.2%</td>
</tr>
<tr>
<td align="left">LOAD_NAME</td>
<td align="right">2,340</td>
<td align="right">1,360</td>
<td align="right">-41.9%</td>
</tr>
<tr>
<td align="left">FOR_ITER_GEN</td>
<td align="right">84,972</td>
<td align="right">53,903</td>
<td align="right">-36.6%</td>
</tr>
<tr>
<td align="left">SEND_GEN</td>
<td align="right">80</td>
<td align="right">60</td>
<td align="right">-25.0%</td>
</tr>
<tr>
<td align="left">CALL_LIST_APPEND</td>
<td align="right">7,179</td>
<td align="right">5,913</td>
<td align="right">-17.6%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_WITH_HINT</td>
<td align="right">180</td>
<td align="right">200</td>
<td align="right">11.1%</td>
</tr>
<tr>
<td align="left">BINARY_OP_INPLACE_ADD_UNICODE</td>
<td align="right">783</td>
<td align="right">703</td>
<td align="right">-10.2%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_GETITEM</td>
<td align="right">2,840</td>
<td align="right">2,580</td>
<td align="right">-9.2%</td>
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
<td align="right">261</td>
<td align="right">261</td>
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
<td align="right">441</td>
<td align="right">441</td>
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
<td align="right">1,980</td>
<td align="right">1,980</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

---
Stats gathered on: 2024-04-04
