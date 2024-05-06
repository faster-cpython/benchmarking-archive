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
<td align="left">STORE_GLOBAL</td>
<td align="right">6,929,920</td>
<td align="right">33,782</td>
<td align="right">-99.5%</td>
</tr>
<tr>
<td align="left">CLEANUP_THROW</td>
<td align="right">152,060</td>
<td align="right">1,522</td>
<td align="right">-99.0%</td>
</tr>
<tr>
<td align="left">DELETE_ATTR</td>
<td align="right">6,693,060</td>
<td align="right">290,612</td>
<td align="right">-95.7%</td>
</tr>
<tr>
<td align="left">FORMAT_WITH_SPEC</td>
<td align="right">1,760</td>
<td align="right">80</td>
<td align="right">-95.5%</td>
</tr>
<tr>
<td align="left">RERAISE</td>
<td align="right">3,848,390</td>
<td align="right">684,461</td>
<td align="right">-82.2%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_LIST</td>
<td align="right">9,009,900</td>
<td align="right">1,808,085</td>
<td align="right">-79.9%</td>
</tr>
<tr>
<td align="left">SETUP_ANNOTATIONS</td>
<td align="right">1,524</td>
<td align="right">460</td>
<td align="right">-69.8%</td>
</tr>
<tr>
<td align="left">END_FOR</td>
<td align="right">82,356,329</td>
<td align="right">26,938,949</td>
<td align="right">-67.3%</td>
</tr>
<tr>
<td align="left">BUILD_SET</td>
<td align="right">2,329,655</td>
<td align="right">765,347</td>
<td align="right">-67.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right">119,493,976</td>
<td align="right">46,474,319</td>
<td align="right">-61.1%</td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">76,738,033</td>
<td align="right">30,825,676</td>
<td align="right">-59.8%</td>
</tr>
<tr>
<td align="left">LOAD_BUILD_CLASS</td>
<td align="right">30,746</td>
<td align="right">13,679</td>
<td align="right">-55.5%</td>
</tr>
<tr>
<td align="left">UNARY_INVERT</td>
<td align="right">2,109,611</td>
<td align="right">986,151</td>
<td align="right">-53.3%</td>
</tr>
<tr>
<td align="left">CALL_TUPLE_1</td>
<td align="right">21,369,089</td>
<td align="right">10,300,606</td>
<td align="right">-51.8%</td>
</tr>
<tr>
<td align="left">BUILD_LIST</td>
<td align="right">230,908,895</td>
<td align="right">115,058,556</td>
<td align="right">-50.2%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">1,208,646,430</td>
<td align="right">624,481,509</td>
<td align="right">-48.3%</td>
</tr>
<tr>
<td align="left">UNARY_NOT</td>
<td align="right">28,377,716</td>
<td align="right">14,674,218</td>
<td align="right">-48.3%</td>
</tr>
<tr>
<td align="left">POP_EXCEPT</td>
<td align="right">24,977,435</td>
<td align="right">13,267,498</td>
<td align="right">-46.9%</td>
</tr>
<tr>
<td align="left">PUSH_EXC_INFO</td>
<td align="right">24,977,584</td>
<td align="right">13,267,649</td>
<td align="right">-46.9%</td>
</tr>
<tr>
<td align="left">CHECK_EXC_MATCH</td>
<td align="right">24,465,946</td>
<td align="right">13,077,130</td>
<td align="right">-46.5%</td>
</tr>
<tr>
<td align="left">SET_UPDATE</td>
<td align="right">200,488</td>
<td align="right">108,764</td>
<td align="right">-45.8%</td>
</tr>
<tr>
<td align="left">DICT_MERGE</td>
<td align="right">42,874,101</td>
<td align="right">23,775,894</td>
<td align="right">-44.5%</td>
</tr>
<tr>
<td align="left">BUILD_STRING</td>
<td align="right">50,581,612</td>
<td align="right">28,225,108</td>
<td align="right">-44.2%</td>
</tr>
<tr>
<td align="left">CONVERT_VALUE</td>
<td align="right">87,548,282</td>
<td align="right">49,015,735</td>
<td align="right">-44.0%</td>
</tr>
<tr>
<td align="left">FORMAT_SIMPLE</td>
<td align="right">97,515,762</td>
<td align="right">55,007,253</td>
<td align="right">-43.6%</td>
</tr>
<tr>
<td align="left">STORE_NAME</td>
<td align="right">641,202</td>
<td align="right">365,599</td>
<td align="right">-43.0%</td>
</tr>
<tr>
<td align="left">STORE_SLICE</td>
<td align="right">12,601,241</td>
<td align="right">7,302,431</td>
<td align="right">-42.0%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">619,987,296</td>
<td align="right">363,641,752</td>
<td align="right">-41.3%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">25,036,765</td>
<td align="right">14,826,933</td>
<td align="right">-40.8%</td>
</tr>
<tr>
<td align="left">MAP_ADD</td>
<td align="right">39,181,018</td>
<td align="right">23,470,430</td>
<td align="right">-40.1%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_UNICODE</td>
<td align="right">72,654,450</td>
<td align="right">44,316,263</td>
<td align="right">-39.0%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR</td>
<td align="right">23,564</td>
<td align="right">14,432</td>
<td align="right">-38.8%</td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">345,405</td>
<td align="right">211,962</td>
<td align="right">-38.6%</td>
</tr>
<tr>
<td align="left">FOR_ITER_GEN</td>
<td align="right">187,384,056</td>
<td align="right">115,909,307</td>
<td align="right">-38.1%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR_METHOD</td>
<td align="right">126,857,657</td>
<td align="right">78,565,035</td>
<td align="right">-38.1%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">104,764,863</td>
<td align="right">65,548,447</td>
<td align="right">-37.4%</td>
</tr>
<tr>
<td align="left">BUILD_CONST_KEY_MAP</td>
<td align="right">7,668,413</td>
<td align="right">4,898,544</td>
<td align="right">-36.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_AND_CLEAR</td>
<td align="right">86,541,970</td>
<td align="right">55,519,311</td>
<td align="right">-35.8%</td>
</tr>
<tr>
<td align="left">DELETE_NAME</td>
<td align="right">1,100</td>
<td align="right">710</td>
<td align="right">-35.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_WITH_HINT</td>
<td align="right">364,885,851</td>
<td align="right">235,830,935</td>
<td align="right">-35.4%</td>
</tr>
<tr>
<td align="left">TO_BOOL_LIST</td>
<td align="right">114,731,353</td>
<td align="right">75,283,796</td>
<td align="right">-34.4%</td>
</tr>
<tr>
<td align="left">BUILD_MAP</td>
<td align="right">123,390,926</td>
<td align="right">82,253,846</td>
<td align="right">-33.3%</td>
</tr>
<tr>
<td align="left">RAISE_VARARGS</td>
<td align="right">6,185,208</td>
<td align="right">4,184,008</td>
<td align="right">-32.4%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_DICT</td>
<td align="right">146,822,843</td>
<td align="right">102,762,577</td>
<td align="right">-30.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_PROPERTY</td>
<td align="right">71,582,986</td>
<td align="right">50,318,695</td>
<td align="right">-29.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">815,247,777</td>
<td align="right">577,491,388</td>
<td align="right">-29.2%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_WITH_HINT</td>
<td align="right">64,723,850</td>
<td align="right">46,774,661</td>
<td align="right">-27.7%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST</td>
<td align="right">306,079,417</td>
<td align="right">223,976,814</td>
<td align="right">-26.8%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST_WITH_KEYWORDS</td>
<td align="right">43,721,406</td>
<td align="right">32,216,193</td>
<td align="right">-26.3%</td>
</tr>
<tr>
<td align="left">CALL_ISINSTANCE</td>
<td align="right">766,787,638</td>
<td align="right">567,408,768</td>
<td align="right">-26.0%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_DICT</td>
<td align="right">409,530,576</td>
<td align="right">305,328,239</td>
<td align="right">-25.4%</td>
</tr>
<tr>
<td align="left">FOR_ITER_TUPLE</td>
<td align="right">9,303,063</td>
<td align="right">6,945,592</td>
<td align="right">-25.3%</td>
</tr>
<tr>
<td align="left">NOP</td>
<td align="right">938,409,684</td>
<td align="right">712,431,054</td>
<td align="right">-24.1%</td>
</tr>
<tr>
<td align="left">COPY_FREE_VARS</td>
<td align="right">287,245,702</td>
<td align="right">218,401,685</td>
<td align="right">-24.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL_STR</td>
<td align="right">76,953,826</td>
<td align="right">58,574,733</td>
<td align="right">-23.9%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">71,548,312</td>
<td align="right">54,637,566</td>
<td align="right">-23.6%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP_DICT</td>
<td align="right">109,550,340</td>
<td align="right">83,830,631</td>
<td align="right">-23.5%</td>
</tr>
<tr>
<td align="left">GET_YIELD_FROM_ITER</td>
<td align="right">47,310,775</td>
<td align="right">36,496,606</td>
<td align="right">-22.9%</td>
</tr>
<tr>
<td align="left">SET_ADD</td>
<td align="right">240,229</td>
<td align="right">185,960</td>
<td align="right">-22.6%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE</td>
<td align="right">452,884</td>
<td align="right">354,594</td>
<td align="right">-21.7%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_SLOT</td>
<td align="right">1,498,227,190</td>
<td align="right">1,177,891,874</td>
<td align="right">-21.4%</td>
</tr>
<tr>
<td align="left">CALL_LIST_APPEND</td>
<td align="right">348,157,849</td>
<td align="right">273,858,935</td>
<td align="right">-21.3%</td>
</tr>
<tr>
<td align="left">CALL_STR_1</td>
<td align="right">38,333,898</td>
<td align="right">30,263,815</td>
<td align="right">-21.1%</td>
</tr>
<tr>
<td align="left">MAKE_CELL</td>
<td align="right">103,472,601</td>
<td align="right">81,976,108</td>
<td align="right">-20.8%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">2,377,717,516</td>
<td align="right">1,887,972,958</td>
<td align="right">-20.6%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">493,623,594</td>
<td align="right">393,755,668</td>
<td align="right">-20.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">1,312,457,436</td>
<td align="right">1,047,174,219</td>
<td align="right">-20.2%</td>
</tr>
<tr>
<td align="left">TO_BOOL_NONE</td>
<td align="right">507,380,319</td>
<td align="right">405,333,066</td>
<td align="right">-20.1%</td>
</tr>
<tr>
<td align="left">CALL_KW</td>
<td align="right">273,966,274</td>
<td align="right">219,029,322</td>
<td align="right">-20.1%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_CLASS</td>
<td align="right">159,358,681</td>
<td align="right">127,599,801</td>
<td align="right">-19.9%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">1,187,774,521</td>
<td align="right">957,011,344</td>
<td align="right">-19.4%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">2,053,370,971</td>
<td align="right">1,656,355,082</td>
<td align="right">-19.3%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_GETITEM</td>
<td align="right">62,209,216</td>
<td align="right">50,356,483</td>
<td align="right">-19.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_CHECK</td>
<td align="right">11,124,430</td>
<td align="right">9,023,211</td>
<td align="right">-18.9%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">143,818,781</td>
<td align="right">117,005,972</td>
<td align="right">-18.6%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">1,701,185,800</td>
<td align="right">1,385,688,920</td>
<td align="right">-18.5%</td>
</tr>
<tr>
<td align="left">BEFORE_WITH</td>
<td align="right">10,114,991</td>
<td align="right">8,263,783</td>
<td align="right">-18.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">1,480,365,421</td>
<td align="right">1,213,917,211</td>
<td align="right">-18.0%</td>
</tr>
<tr>
<td align="left">RETURN_GENERATOR</td>
<td align="right">414,256,741</td>
<td align="right">342,839,978</td>
<td align="right">-17.2%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">529,390,436</td>
<td align="right">438,324,087</td>
<td align="right">-17.2%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">120,156,167</td>
<td align="right">99,517,485</td>
<td align="right">-17.2%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">2,570,492,370</td>
<td align="right">2,132,322,619</td>
<td align="right">-17.0%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">368,481,204</td>
<td align="right">305,974,115</td>
<td align="right">-17.0%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NOT_NONE</td>
<td align="right">666,882,339</td>
<td align="right">554,635,573</td>
<td align="right">-16.8%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">2,881,871,460</td>
<td align="right">2,417,276,603</td>
<td align="right">-16.1%</td>
</tr>
<tr>
<td align="left">CALL_LEN</td>
<td align="right">289,479,867</td>
<td align="right">245,017,969</td>
<td align="right">-15.4%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">492,119,451</td>
<td align="right">417,758,000</td>
<td align="right">-15.1%</td>
</tr>
<tr>
<td align="left">TO_BOOL_ALWAYS_TRUE</td>
<td align="right">182,031,197</td>
<td align="right">154,802,805</td>
<td align="right">-15.0%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">108,201,951</td>
<td align="right">92,117,944</td>
<td align="right">-14.9%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">2,636,687,515</td>
<td align="right">2,247,691,703</td>
<td align="right">-14.8%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_STR</td>
<td align="right">314,812,057</td>
<td align="right">268,993,824</td>
<td align="right">-14.6%</td>
</tr>
<tr>
<td align="left">LIST_APPEND</td>
<td align="right">94,650,474</td>
<td align="right">81,054,677</td>
<td align="right">-14.4%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">22,247,432,164</td>
<td align="right">19,056,799,746</td>
<td align="right">-14.3%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NONE</td>
<td align="right">391,011,760</td>
<td align="right">337,132,354</td>
<td align="right">-13.8%</td>
</tr>
<tr>
<td align="left">IMPORT_FROM</td>
<td align="right">13,102,915</td>
<td align="right">11,313,548</td>
<td align="right">-13.7%</td>
</tr>
<tr>
<td align="left">CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">186,731,095</td>
<td align="right">161,332,826</td>
<td align="right">-13.6%</td>
</tr>
<tr>
<td align="left">LIST_EXTEND</td>
<td align="right">29,490,549</td>
<td align="right">25,554,331</td>
<td align="right">-13.3%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">541,598,880</td>
<td align="right">470,609,485</td>
<td align="right">-13.1%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">5,720,718,985</td>
<td align="right">4,971,201,602</td>
<td align="right">-13.1%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">1,133,187,061</td>
<td align="right">986,798,995</td>
<td align="right">-12.9%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">6,594,559,155</td>
<td align="right">5,750,621,951</td>
<td align="right">-12.8%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">3,463,192,568</td>
<td align="right">3,021,107,318</td>
<td align="right">-12.8%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST_WITH_KEYWORDS</td>
<td align="right">41,295,900</td>
<td align="right">36,059,808</td>
<td align="right">-12.7%</td>
</tr>
<tr>
<td align="left">IMPORT_NAME</td>
<td align="right">12,435,121</td>
<td align="right">10,862,839</td>
<td align="right">-12.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">4,817,674,938</td>
<td align="right">4,209,728,341</td>
<td align="right">-12.6%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_CLASS</td>
<td align="right">159,691,677</td>
<td align="right">140,357,205</td>
<td align="right">-12.1%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">3,284,208,857</td>
<td align="right">2,907,053,862</td>
<td align="right">-11.5%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">5,539,794,934</td>
<td align="right">4,921,775,946</td>
<td align="right">-11.2%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">4,016,577,902</td>
<td align="right">3,569,624,878</td>
<td align="right">-11.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">4,067,755,438</td>
<td align="right">3,617,105,359</td>
<td align="right">-11.1%</td>
</tr>
<tr>
<td align="left">BINARY_SLICE</td>
<td align="right">225,315,218</td>
<td align="right">200,929,502</td>
<td align="right">-10.8%</td>
</tr>
<tr>
<td align="left">MAKE_FUNCTION</td>
<td align="right">65,553,216</td>
<td align="right">58,468,533</td>
<td align="right">-10.8%</td>
</tr>
<tr>
<td align="left">LOAD_FROM_DICT_OR_DEREF</td>
<td align="right">2,240</td>
<td align="right">2,000</td>
<td align="right">-10.7%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">5,051,082,775</td>
<td align="right">4,513,806,361</td>
<td align="right">-10.6%</td>
</tr>
<tr>
<td align="left">LOAD_LOCALS</td>
<td align="right">2,260</td>
<td align="right">2,020</td>
<td align="right">-10.6%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR_ATTR</td>
<td align="right">7,751,712</td>
<td align="right">6,947,125</td>
<td align="right">-10.4%</td>
</tr>
<tr>
<td align="left">CALL_TYPE_1</td>
<td align="right">147,600,612</td>
<td align="right">132,366,699</td>
<td align="right">-10.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_MODULE</td>
<td align="right">521,293,394</td>
<td align="right">468,558,902</td>
<td align="right">-10.1%</td>
</tr>
<tr>
<td align="left">CALL_FUNCTION_EX</td>
<td align="right">218,806,985</td>
<td align="right">197,340,666</td>
<td align="right">-9.8%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_LIST_INT</td>
<td align="right">415,568,450</td>
<td align="right">374,840,600</td>
<td align="right">-9.8%</td>
</tr>
<tr>
<td align="left">SET_FUNCTION_ATTRIBUTE</td>
<td align="right">53,468,126</td>
<td align="right">48,262,222</td>
<td align="right">-9.7%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR</td>
<td align="right">264,420,994</td>
<td align="right">239,226,624</td>
<td align="right">-9.5%</td>
</tr>
<tr>
<td align="left">BINARY_OP_INPLACE_ADD_UNICODE</td>
<td align="right">4,824,622</td>
<td align="right">4,372,173</td>
<td align="right">-9.4%</td>
</tr>
<tr>
<td align="left">STORE_FAST_STORE_FAST</td>
<td align="right">386,624,164</td>
<td align="right">352,422,384</td>
<td align="right">-8.8%</td>
</tr>
<tr>
<td align="left">JUMP_FORWARD</td>
<td align="right">437,806,427</td>
<td align="right">399,597,786</td>
<td align="right">-8.7%</td>
</tr>
<tr>
<td align="left">IS_OP</td>
<td align="right">404,700,690</td>
<td align="right">370,999,541</td>
<td align="right">-8.3%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">259,941,483</td>
<td align="right">238,531,246</td>
<td align="right">-8.2%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">589,371,051</td>
<td align="right">542,735,056</td>
<td align="right">-7.9%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">259,154,778</td>
<td align="right">238,889,297</td>
<td align="right">-7.8%</td>
</tr>
<tr>
<td align="left">DELETE_FAST</td>
<td align="right">2,228,809</td>
<td align="right">2,055,549</td>
<td align="right">-7.8%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_O</td>
<td align="right">393,943,941</td>
<td align="right">364,823,527</td>
<td align="right">-7.4%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_TUPLE_INT</td>
<td align="right">178,751,948</td>
<td align="right">165,894,885</td>
<td align="right">-7.2%</td>
</tr>
<tr>
<td align="left">CALL_ALLOC_AND_ENTER_INIT</td>
<td align="right">96,991,994</td>
<td align="right">90,183,174</td>
<td align="right">-7.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">238,636,254</td>
<td align="right">222,024,195</td>
<td align="right">-7.0%</td>
</tr>
<tr>
<td align="left">PUSH_NULL</td>
<td align="right">1,100,442,894</td>
<td align="right">1,025,500,837</td>
<td align="right">-6.8%</td>
</tr>
<tr>
<td align="left">INTERPRETER_EXIT</td>
<td align="right">2,309,026,215</td>
<td align="right">2,154,197,574</td>
<td align="right">-6.7%</td>
</tr>
<tr>
<td align="left">TO_BOOL_INT</td>
<td align="right">141,906,959</td>
<td align="right">133,152,447</td>
<td align="right">-6.2%</td>
</tr>
<tr>
<td align="left">STORE_FAST_LOAD_FAST</td>
<td align="right">15,893,888</td>
<td align="right">15,016,389</td>
<td align="right">-5.5%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_INT</td>
<td align="right">640,957,617</td>
<td align="right">606,909,908</td>
<td align="right">-5.3%</td>
</tr>
<tr>
<td align="left">SEND</td>
<td align="right">173,838,953</td>
<td align="right">165,326,282</td>
<td align="right">-4.9%</td>
</tr>
<tr>
<td align="left">EXIT_INIT_CHECK</td>
<td align="right">94,703,932</td>
<td align="right">90,176,804</td>
<td align="right">-4.8%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR</td>
<td align="right">69,692,743</td>
<td align="right">66,521,443</td>
<td align="right">-4.6%</td>
</tr>
<tr>
<td align="left">DICT_UPDATE</td>
<td align="right">72,946</td>
<td align="right">69,705</td>
<td align="right">-4.4%</td>
</tr>
<tr>
<td align="left">FOR_ITER_RANGE</td>
<td align="right">30,114,679</td>
<td align="right">28,837,475</td>
<td align="right">-4.2%</td>
</tr>
<tr>
<td align="left">STORE_DEREF</td>
<td align="right">94,322,631</td>
<td align="right">90,838,330</td>
<td align="right">-3.7%</td>
</tr>
<tr>
<td align="left">WITH_EXCEPT_START</td>
<td align="right">233,483</td>
<td align="right">225,147</td>
<td align="right">-3.6%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TUPLE</td>
<td align="right">195,353,133</td>
<td align="right">188,739,935</td>
<td align="right">-3.4%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT</td>
<td align="right">1,201,483,879</td>
<td align="right">1,161,250,871</td>
<td align="right">-3.3%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_O</td>
<td align="right">532,968,795</td>
<td align="right">518,115,112</td>
<td align="right">-2.8%</td>
</tr>
<tr>
<td align="left">CALL_INTRINSIC_1</td>
<td align="right">154,743,765</td>
<td align="right">150,570,052</td>
<td align="right">-2.7%</td>
</tr>
<tr>
<td align="left">END_SEND</td>
<td align="right">402,621,319</td>
<td align="right">391,966,021</td>
<td align="right">-2.6%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP_SET</td>
<td align="right">339,223,409</td>
<td align="right">330,950,468</td>
<td align="right">-2.4%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">20,772,701</td>
<td align="right">20,267,925</td>
<td align="right">-2.4%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_INT</td>
<td align="right">383,263,041</td>
<td align="right">374,624,302</td>
<td align="right">-2.3%</td>
</tr>
<tr>
<td align="left">YIELD_VALUE</td>
<td align="right">1,355,102,340</td>
<td align="right">1,325,749,279</td>
<td align="right">-2.2%</td>
</tr>
<tr>
<td align="left">LOAD_NAME</td>
<td align="right">8,145,287</td>
<td align="right">7,998,336</td>
<td align="right">-1.8%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_STR_INT</td>
<td align="right">456,052,952</td>
<td align="right">449,348,176</td>
<td align="right">-1.5%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_LIST_INT</td>
<td align="right">99,279,361</td>
<td align="right">98,066,555</td>
<td align="right">-1.2%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD_NO_INTERRUPT</td>
<td align="right">556,677,959</td>
<td align="right">551,296,663</td>
<td align="right">-1.0%</td>
</tr>
<tr>
<td align="left">SEND_GEN</td>
<td align="right">787,108,999</td>
<td align="right">779,995,407</td>
<td align="right">-0.9%</td>
</tr>
<tr>
<td align="left">BUILD_SLICE</td>
<td align="right">71,718,129</td>
<td align="right">71,096,961</td>
<td align="right">-0.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_NO_DICT</td>
<td align="right">66,925,716</td>
<td align="right">66,350,473</td>
<td align="right">-0.9%</td>
</tr>
<tr>
<td align="left">UNARY_NEGATIVE</td>
<td align="right">145,910,186</td>
<td align="right">144,672,938</td>
<td align="right">-0.8%</td>
</tr>
<tr>
<td align="left">DELETE_SUBSCR</td>
<td align="right">176,287,007</td>
<td align="right">175,157,044</td>
<td align="right">-0.6%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_FLOAT</td>
<td align="right">75,404,604</td>
<td align="right">75,190,162</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">INSTRUMENTED_FOR_ITER</td>
<td align="right">3,224</td>
<td align="right">3,216</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">INSTRUMENTED_JUMP_BACKWARD</td>
<td align="right">6,264</td>
<td align="right">6,256</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">INSTRUMENTED_POP_JUMP_IF_TRUE</td>
<td align="right">8,744</td>
<td align="right">8,736</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">BINARY_OP_MULTIPLY_FLOAT</td>
<td align="right">146,544,932</td>
<td align="right">146,444,056</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_FLOAT</td>
<td align="right">72,575,182</td>
<td align="right">72,527,615</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">UNPACK_EX</td>
<td align="right">1,129,822</td>
<td align="right">1,129,440</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_FLOAT</td>
<td align="right">149,885,136</td>
<td align="right">149,842,938</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_LAZY_DICT</td>
<td align="right">247,735,812</td>
<td align="right">247,674,735</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_MULTIPLY_INT</td>
<td align="right">164,103,831</td>
<td align="right">164,065,801</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">GET_AWAITABLE</td>
<td align="right">229,139,445</td>
<td align="right">229,138,706</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">CALL_PY_WITH_DEFAULTS</td>
<td align="right">216,589,171</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">INSTRUMENTED_POP_JUMP_IF_FALSE</td>
<td align="right">38,876,080</td>
<td align="right">38,876,080</td>
<td align="right">0.0%</td>
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
<td align="left">BEFORE_ASYNC_WITH</td>
<td align="right">3,005,920</td>
<td align="right">3,005,920</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_GETATTRIBUTE_OVERRIDDEN</td>
<td align="right">89,680</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">INSTRUMENTED_POP_JUMP_IF_NOT_NONE</td>
<td align="right">4,800</td>
<td align="right">4,800</td>
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
<td align="left">INSTRUMENTED_POP_JUMP_IF_NONE</td>
<td align="right">720</td>
<td align="right">720</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_INTRINSIC_2</td>
<td align="right">80</td>
<td align="right">80</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_PY_GENERAL</td>
<td align="right"></td>
<td align="right">265,833,312</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_NON_PY_GENERAL</td>
<td align="right"></td>
<td align="right">234,409,238</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_BOUND_METHOD_GENERAL</td>
<td align="right"></td>
<td align="right">8,367,521</td>
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
<td align="right">618,394,108</td>
<td align="right">28.8%</td>
<td align="right">571,831,160</td>
<td align="right">28.2%</td>
<td align="right">-7.5%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">1,529,440,076</td>
<td align="right">71.1%</td>
<td align="right">1,457,563,895</td>
<td align="right">71.8%</td>
<td align="right">-4.7%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">30,888,203</td>
<td align="right">1.4%</td>
<td align="right">30,886,385</td>
<td align="right">1.5%</td>
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
<td align="left">Failure</td>
<td align="right">1,229,133</td>
<td align="right">65.9%</td>
<td align="right">1,169,612</td>
<td align="right">65.3%</td>
<td align="right">-4.8%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">636,013</td>
<td align="right">34.1%</td>
<td align="right">620,669</td>
<td align="right">34.7%</td>
<td align="right">-2.4%</td>
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
<td align="left">and different types</td>
<td align="right">619</td>
<td align="right">0.1%</td>
<td align="right">382</td>
<td align="right">0.0%</td>
<td align="right">-38.3%</td>
</tr>
<tr>
<td align="left">multiply other</td>
<td align="right">5,220</td>
<td align="right">0.4%</td>
<td align="right">3,560</td>
<td align="right">0.3%</td>
<td align="right">-31.8%</td>
</tr>
<tr>
<td align="left">add other</td>
<td align="right">64,269</td>
<td align="right">5.2%</td>
<td align="right">46,613</td>
<td align="right">4.0%</td>
<td align="right">-27.5%</td>
</tr>
<tr>
<td align="left">remainder</td>
<td align="right">53,257</td>
<td align="right">4.3%</td>
<td align="right">40,446</td>
<td align="right">3.5%</td>
<td align="right">-24.1%</td>
</tr>
<tr>
<td align="left">or</td>
<td align="right">17,160</td>
<td align="right">1.4%</td>
<td align="right">13,582</td>
<td align="right">1.2%</td>
<td align="right">-20.9%</td>
</tr>
<tr>
<td align="left">and other</td>
<td align="right">2,010</td>
<td align="right">0.2%</td>
<td align="right">1,674</td>
<td align="right">0.1%</td>
<td align="right">-16.7%</td>
</tr>
<tr>
<td align="left">xor</td>
<td align="right">8,724</td>
<td align="right">0.7%</td>
<td align="right">7,464</td>
<td align="right">0.6%</td>
<td align="right">-14.4%</td>
</tr>
<tr>
<td align="left">add different types</td>
<td align="right">78,511</td>
<td align="right">6.4%</td>
<td align="right">67,211</td>
<td align="right">5.7%</td>
<td align="right">-14.4%</td>
</tr>
<tr>
<td align="left">and int</td>
<td align="right">37,256</td>
<td align="right">3.0%</td>
<td align="right">33,679</td>
<td align="right">2.9%</td>
<td align="right">-9.6%</td>
</tr>
<tr>
<td align="left">subtract other</td>
<td align="right">12,354</td>
<td align="right">1.0%</td>
<td align="right">11,500</td>
<td align="right">1.0%</td>
<td align="right">-6.9%</td>
</tr>
<tr>
<td align="left">multiply different types</td>
<td align="right">92,076</td>
<td align="right">7.5%</td>
<td align="right">87,013</td>
<td align="right">7.4%</td>
<td align="right">-5.5%</td>
</tr>
<tr>
<td align="left">lshift</td>
<td align="right">5,706</td>
<td align="right">0.5%</td>
<td align="right">5,503</td>
<td align="right">0.5%</td>
<td align="right">-3.6%</td>
</tr>
<tr>
<td align="left">true divide different types</td>
<td align="right">12,504</td>
<td align="right">1.0%</td>
<td align="right">12,102</td>
<td align="right">1.0%</td>
<td align="right">-3.2%</td>
</tr>
<tr>
<td align="left">true divide other</td>
<td align="right">3,441</td>
<td align="right">0.3%</td>
<td align="right">3,380</td>
<td align="right">0.3%</td>
<td align="right">-1.8%</td>
</tr>
<tr>
<td align="left">floor divide</td>
<td align="right">33,276</td>
<td align="right">2.7%</td>
<td align="right">33,002</td>
<td align="right">2.8%</td>
<td align="right">-0.8%</td>
</tr>
<tr>
<td align="left">power</td>
<td align="right">5,748</td>
<td align="right">0.5%</td>
<td align="right">5,702</td>
<td align="right">0.5%</td>
<td align="right">-0.8%</td>
</tr>
<tr>
<td align="left">rshift</td>
<td align="right">8,855</td>
<td align="right">0.7%</td>
<td align="right">8,791</td>
<td align="right">0.8%</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">true divide float</td>
<td align="right">5,664</td>
<td align="right">0.5%</td>
<td align="right">5,663</td>
<td align="right">0.5%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">subtract different types</td>
<td align="right">782,483</td>
<td align="right">63.7%</td>
<td align="right">782,345</td>
<td align="right">66.9%</td>
<td align="right">-0.0%</td>
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
<td align="right">4,901,503</td>
<td align="right">0.3%</td>
<td align="right">1,796,970</td>
<td align="right">0.1%</td>
<td align="right">-63.3%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">1,517,211,639</td>
<td align="right">84.9%</td>
<td align="right">1,343,971,413</td>
<td align="right">84.8%</td>
<td align="right">-11.4%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">268,976,663</td>
<td align="right">15.1%</td>
<td align="right">240,811,563</td>
<td align="right">15.2%</td>
<td align="right">-10.5%</td>
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
<td align="right">201,822</td>
<td align="right">58.4%</td>
<td align="right">111,215</td>
<td align="right">52.5%</td>
<td align="right">-44.9%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">144,012</td>
<td align="right">41.6%</td>
<td align="right">100,816</td>
<td align="right">47.5%</td>
<td align="right">-30.0%</td>
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
<td align="left">tuple slice</td>
<td align="right">184</td>
<td align="right">0.1%</td>
<td align="right">23</td>
<td align="right">0.0%</td>
<td align="right">-87.5%</td>
</tr>
<tr>
<td align="left">code complex parameters</td>
<td align="right">5,017</td>
<td align="right">3.5%</td>
<td align="right">1,140</td>
<td align="right">1.1%</td>
<td align="right">-77.3%</td>
</tr>
<tr>
<td align="left">out of range</td>
<td align="right">68,919</td>
<td align="right">47.9%</td>
<td align="right">40,819</td>
<td align="right">40.5%</td>
<td align="right">-40.8%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">25,049</td>
<td align="right">17.4%</td>
<td align="right">16,590</td>
<td align="right">16.5%</td>
<td align="right">-33.8%</td>
</tr>
<tr>
<td align="left">list slice</td>
<td align="right">1,360</td>
<td align="right">0.9%</td>
<td align="right">1,122</td>
<td align="right">1.1%</td>
<td align="right">-17.5%</td>
</tr>
<tr>
<td align="left">buffer int</td>
<td align="right">22,303</td>
<td align="right">15.5%</td>
<td align="right">20,020</td>
<td align="right">19.9%</td>
<td align="right">-10.2%</td>
</tr>
<tr>
<td align="left">buffer slice</td>
<td align="right">900</td>
<td align="right">0.6%</td>
<td align="right">842</td>
<td align="right">0.8%</td>
<td align="right">-6.4%</td>
</tr>
<tr>
<td align="left">sequence int</td>
<td align="right">4,300</td>
<td align="right">3.0%</td>
<td align="right">4,280</td>
<td align="right">4.2%</td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">array int</td>
<td align="right">15,880</td>
<td align="right">11.0%</td>
<td align="right">15,880</td>
<td align="right">15.8%</td>
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
<td align="right">6,080</td>
<td align="right">0.0%</td>
<td align="right">-81.6%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">1,454,778,256</td>
<td align="right">17.8%</td>
<td align="right">801,399,825</td>
<td align="right">12.8%</td>
<td align="right">-44.9%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">252,487,017</td>
<td align="right">3.1%</td>
<td align="right">181,207,321</td>
<td align="right">2.9%</td>
<td align="right">-28.2%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">6,715,550,479</td>
<td align="right">82.1%</td>
<td align="right">5,469,976,795</td>
<td align="right">87.2%</td>
<td align="right">-18.5%</td>
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
<td align="right">961,578</td>
<td align="right">15.1%</td>
<td align="right">452,057</td>
<td align="right">10.5%</td>
<td align="right">-53.0%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">5,393,613</td>
<td align="right">84.9%</td>
<td align="right">3,836,948</td>
<td align="right">89.5%</td>
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
<td align="left">init not simple</td>
<td align="right">12,278</td>
<td align="right">1.3%</td>
<td align="right">1,267</td>
<td align="right">0.3%</td>
<td align="right">-89.7%</td>
</tr>
<tr>
<td align="left">init not inline values</td>
<td align="right">105,557</td>
<td align="right">11.0%</td>
<td align="right">71,780</td>
<td align="right">15.9%</td>
<td align="right">-32.0%</td>
</tr>
<tr>
<td align="left">class mutable</td>
<td align="right">24,753</td>
<td align="right">2.6%</td>
<td align="right">17,162</td>
<td align="right">3.8%</td>
<td align="right">-30.7%</td>
</tr>
<tr>
<td align="left">meth descr varargs</td>
<td align="right">16,516</td>
<td align="right">1.7%</td>
<td align="right">12,008</td>
<td align="right">2.7%</td>
<td align="right">-27.3%</td>
</tr>
<tr>
<td align="left">init not python</td>
<td align="right">16,386</td>
<td align="right">1.7%</td>
<td align="right">12,420</td>
<td align="right">2.7%</td>
<td align="right">-24.2%</td>
</tr>
<tr>
<td align="left">wrong number arguments</td>
<td align="right">13,753</td>
<td align="right">1.4%</td>
<td align="right">10,872</td>
<td align="right">2.4%</td>
<td align="right">-20.9%</td>
</tr>
<tr>
<td align="left">meth descr varargs keywords</td>
<td align="right">20,881</td>
<td align="right">2.2%</td>
<td align="right">17,486</td>
<td align="right">3.9%</td>
<td align="right">-16.3%</td>
</tr>
<tr>
<td align="left">class no vectorcall</td>
<td align="right">89,309</td>
<td align="right">9.3%</td>
<td align="right">75,899</td>
<td align="right">16.8%</td>
<td align="right">-15.0%</td>
</tr>
<tr>
<td align="left">metaclass</td>
<td align="right">43,171</td>
<td align="right">4.5%</td>
<td align="right">39,255</td>
<td align="right">8.7%</td>
<td align="right">-9.1%</td>
</tr>
<tr>
<td align="left">meth descr method fastcall keywords</td>
<td align="right">207,170</td>
<td align="right">21.5%</td>
<td align="right">193,088</td>
<td align="right">42.7%</td>
<td align="right">-6.8%</td>
</tr>
<tr>
<td align="left">out of versions</td>
<td align="right">980</td>
<td align="right">0.1%</td>
<td align="right">920</td>
<td align="right">0.2%</td>
<td align="right">-6.1%</td>
</tr>
<tr>
<td align="left">code complex parameters</td>
<td align="right">185,149</td>
<td align="right">19.3%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">cfunc noargs</td>
<td align="right">69,443</td>
<td align="right">7.2%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">65,843</td>
<td align="right">6.8%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">cfunc varargs keywords</td>
<td align="right">32,269</td>
<td align="right">3.4%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">cfunc varargs</td>
<td align="right">14,247</td>
<td align="right">1.5%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">cmethod</td>
<td align="right">13,620</td>
<td align="right">1.4%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">bound method</td>
<td align="right">12,053</td>
<td align="right">1.3%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">operator wrapper</td>
<td align="right">10,136</td>
<td align="right">1.1%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">method wrapper</td>
<td align="right">8,224</td>
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
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">1,859,985</td>
<td align="right">0.1%</td>
<td align="right">998,836</td>
<td align="right">0.1%</td>
<td align="right">-46.3%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">145,336,316</td>
<td align="right">8.0%</td>
<td align="right">117,791,165</td>
<td align="right">6.9%</td>
<td align="right">-19.0%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">1,664,321,087</td>
<td align="right">92.0%</td>
<td align="right">1,579,088,797</td>
<td align="right">93.0%</td>
<td align="right">-5.1%</td>
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
<td align="right">113,044</td>
<td align="right">33.0%</td>
<td align="right">66,449</td>
<td align="right">31.1%</td>
<td align="right">-41.2%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">229,406</td>
<td align="right">67.0%</td>
<td align="right">147,194</td>
<td align="right">68.9%</td>
<td align="right">-35.8%</td>
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
<td align="right">4,214</td>
<td align="right">1.8%</td>
<td align="right">1,014</td>
<td align="right">0.7%</td>
<td align="right">-75.9%</td>
</tr>
<tr>
<td align="left">bool</td>
<td align="right">3,782</td>
<td align="right">1.6%</td>
<td align="right">1,446</td>
<td align="right">1.0%</td>
<td align="right">-61.8%</td>
</tr>
<tr>
<td align="left">big int</td>
<td align="right">61,419</td>
<td align="right">26.8%</td>
<td align="right">33,002</td>
<td align="right">22.4%</td>
<td align="right">-46.3%</td>
</tr>
<tr>
<td align="left">different types</td>
<td align="right">54,894</td>
<td align="right">23.9%</td>
<td align="right">30,515</td>
<td align="right">20.7%</td>
<td align="right">-44.4%</td>
</tr>
<tr>
<td align="left">baseobject</td>
<td align="right">31,919</td>
<td align="right">13.9%</td>
<td align="right">17,921</td>
<td align="right">12.2%</td>
<td align="right">-43.9%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">1,663</td>
<td align="right">0.7%</td>
<td align="right">1,180</td>
<td align="right">0.8%</td>
<td align="right">-29.0%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">23,991</td>
<td align="right">10.5%</td>
<td align="right">18,044</td>
<td align="right">12.3%</td>
<td align="right">-24.8%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">14,548</td>
<td align="right">6.3%</td>
<td align="right">11,586</td>
<td align="right">7.9%</td>
<td align="right">-20.4%</td>
</tr>
<tr>
<td align="left">string</td>
<td align="right">11,080</td>
<td align="right">4.8%</td>
<td align="right">10,680</td>
<td align="right">7.3%</td>
<td align="right">-3.6%</td>
</tr>
<tr>
<td align="left">long float</td>
<td align="right">1,525</td>
<td align="right">0.7%</td>
<td align="right">1,483</td>
<td align="right">1.0%</td>
<td align="right">-2.8%</td>
</tr>
<tr>
<td align="left">bytes</td>
<td align="right">3,920</td>
<td align="right">1.7%</td>
<td align="right">3,901</td>
<td align="right">2.7%</td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">float long</td>
<td align="right">16,451</td>
<td align="right">7.2%</td>
<td align="right">16,422</td>
<td align="right">11.2%</td>
<td align="right">-0.2%</td>
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
<td align="right">107,117,016</td>
<td align="right">19.4%</td>
<td align="right">67,937,897</td>
<td align="right">14.1%</td>
<td align="right">-36.6%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">446,227,509</td>
<td align="right">80.6%</td>
<td align="right">412,268,079</td>
<td align="right">85.8%</td>
<td align="right">-7.6%</td>
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
<td align="right">2,513,020</td>
<td align="right">0.5%</td>
<td align="right">-1.3%</td>
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
<td align="right">126,576</td>
<td align="right">65.2%</td>
<td align="right">66,449</td>
<td align="right">53.8%</td>
<td align="right">-47.5%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">67,511</td>
<td align="right">34.8%</td>
<td align="right">57,121</td>
<td align="right">46.2%</td>
<td align="right">-15.4%</td>
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
<td align="right">18,249</td>
<td align="right">14.4%</td>
<td align="right">5,748</td>
<td align="right">8.7%</td>
<td align="right">-68.5%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">46,699</td>
<td align="right">36.9%</td>
<td align="right">22,737</td>
<td align="right">34.2%</td>
<td align="right">-51.3%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">27,872</td>
<td align="right">22.0%</td>
<td align="right">17,014</td>
<td align="right">25.6%</td>
<td align="right">-39.0%</td>
</tr>
<tr>
<td align="left">str</td>
<td align="right">33,756</td>
<td align="right">26.7%</td>
<td align="right">20,950</td>
<td align="right">31.5%</td>
<td align="right">-37.9%</td>
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
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">251,514,229</td>
<td align="right">67.6%</td>
<td align="right">166,249,694</td>
<td align="right">62.5%</td>
<td align="right">-33.9%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">120,243,391</td>
<td align="right">32.3%</td>
<td align="right">99,629,186</td>
<td align="right">37.4%</td>
<td align="right">-17.1%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">324,334</td>
<td align="right">0.1%</td>
<td align="right">269,613</td>
<td align="right">0.1%</td>
<td align="right">-16.9%</td>
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
<td align="right">72,254</td>
<td align="right">30.5%</td>
<td align="right">41,769</td>
<td align="right">26.5%</td>
<td align="right">-42.2%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">164,856</td>
<td align="right">69.5%</td>
<td align="right">116,143</td>
<td align="right">73.5%</td>
<td align="right">-29.5%</td>
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
<td align="left">enumerate</td>
<td align="right">19,930</td>
<td align="right">12.1%</td>
<td align="right">8,605</td>
<td align="right">7.4%</td>
<td align="right">-56.8%</td>
</tr>
<tr>
<td align="left">zip</td>
<td align="right">14,352</td>
<td align="right">8.7%</td>
<td align="right">7,564</td>
<td align="right">6.5%</td>
<td align="right">-47.3%</td>
</tr>
<tr>
<td align="left">reversed list</td>
<td align="right">7,885</td>
<td align="right">4.8%</td>
<td align="right">4,180</td>
<td align="right">3.6%</td>
<td align="right">-47.0%</td>
</tr>
<tr>
<td align="left">map</td>
<td align="right">740</td>
<td align="right">0.4%</td>
<td align="right">429</td>
<td align="right">0.4%</td>
<td align="right">-42.0%</td>
</tr>
<tr>
<td align="left">bytes</td>
<td align="right">660</td>
<td align="right">0.4%</td>
<td align="right">387</td>
<td align="right">0.3%</td>
<td align="right">-41.4%</td>
</tr>
<tr>
<td align="left">dict values</td>
<td align="right">6,990</td>
<td align="right">4.2%</td>
<td align="right">4,799</td>
<td align="right">4.1%</td>
<td align="right">-31.3%</td>
</tr>
<tr>
<td align="left">seq iter</td>
<td align="right">6,060</td>
<td align="right">3.7%</td>
<td align="right">4,293</td>
<td align="right">3.7%</td>
<td align="right">-29.2%</td>
</tr>
<tr>
<td align="left">itertools</td>
<td align="right">7,249</td>
<td align="right">4.4%</td>
<td align="right">5,220</td>
<td align="right">4.5%</td>
<td align="right">-28.0%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">22,734</td>
<td align="right">13.8%</td>
<td align="right">16,742</td>
<td align="right">14.4%</td>
<td align="right">-26.4%</td>
</tr>
<tr>
<td align="left">ascii string</td>
<td align="right">2,680</td>
<td align="right">1.6%</td>
<td align="right">2,087</td>
<td align="right">1.8%</td>
<td align="right">-22.1%</td>
</tr>
<tr>
<td align="left">dict items</td>
<td align="right">50,326</td>
<td align="right">30.5%</td>
<td align="right">40,115</td>
<td align="right">34.5%</td>
<td align="right">-20.3%</td>
</tr>
<tr>
<td align="left">dict keys</td>
<td align="right">14,549</td>
<td align="right">8.8%</td>
<td align="right">11,620</td>
<td align="right">10.0%</td>
<td align="right">-20.1%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">10,399</td>
<td align="right">6.3%</td>
<td align="right">9,822</td>
<td align="right">8.5%</td>
<td align="right">-5.5%</td>
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
<td align="right">20</td>
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
<td align="right">571,500,696</td>
<td align="right">5.2%</td>
<td align="right">232,234,477</td>
<td align="right">2.6%</td>
<td align="right">-59.4%</td>
</tr>
<tr>
<td align="left">
deopt
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">681,360</td>
<td align="right">0.0%</td>
<td align="right">357,671</td>
<td align="right">0.0%</td>
<td align="right">-47.5%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">1,373,437,511</td>
<td align="right">12.6%</td>
<td align="right">804,202,237</td>
<td align="right">8.8%</td>
<td align="right">-41.4%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">9,541,962,491</td>
<td align="right">87.3%</td>
<td align="right">8,287,216,496</td>
<td align="right">91.1%</td>
<td align="right">-13.1%</td>
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
<td align="right">1,643,825</td>
<td align="right">12.3%</td>
<td align="right">622,113</td>
<td align="right">11.3%</td>
<td align="right">-62.2%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">11,667,137</td>
<td align="right">87.7%</td>
<td align="right">4,901,515</td>
<td align="right">88.7%</td>
<td align="right">-58.0%</td>
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
<td align="right">2,281</td>
<td align="right">0.1%</td>
<td align="right">20</td>
<td align="right">0.0%</td>
<td align="right">-99.1%</td>
</tr>
<tr>
<td align="left">class attr simple</td>
<td align="right">718,710</td>
<td align="right">43.7%</td>
<td align="right">30,095</td>
<td align="right">4.8%</td>
<td align="right">-95.8%</td>
</tr>
<tr>
<td align="left">shadowed</td>
<td align="right">138,848</td>
<td align="right">8.4%</td>
<td align="right">27,602</td>
<td align="right">4.4%</td>
<td align="right">-80.1%</td>
</tr>
<tr>
<td align="left">non overriding descriptor</td>
<td align="right">13,519</td>
<td align="right">0.8%</td>
<td align="right">5,441</td>
<td align="right">0.9%</td>
<td align="right">-59.8%</td>
</tr>
<tr>
<td align="left">builtin class method</td>
<td align="right">3,817</td>
<td align="right">0.2%</td>
<td align="right">1,622</td>
<td align="right">0.3%</td>
<td align="right">-57.5%</td>
</tr>
<tr>
<td align="left">not in keys</td>
<td align="right">15,540</td>
<td align="right">0.9%</td>
<td align="right">6,960</td>
<td align="right">1.1%</td>
<td align="right">-55.2%</td>
</tr>
<tr>
<td align="left">module attr not found</td>
<td align="right">17,842</td>
<td align="right">1.1%</td>
<td align="right">9,529</td>
<td align="right">1.5%</td>
<td align="right">-46.6%</td>
</tr>
<tr>
<td align="left">class attr descriptor</td>
<td align="right">30,160</td>
<td align="right">1.8%</td>
<td align="right">17,763</td>
<td align="right">2.9%</td>
<td align="right">-41.1%</td>
</tr>
<tr>
<td align="left">class method obj</td>
<td align="right">21,933</td>
<td align="right">1.3%</td>
<td align="right">13,904</td>
<td align="right">2.2%</td>
<td align="right">-36.6%</td>
</tr>
<tr>
<td align="left">not managed dict</td>
<td align="right">248,535</td>
<td align="right">15.1%</td>
<td align="right">162,595</td>
<td align="right">26.1%</td>
<td align="right">-34.6%</td>
</tr>
<tr>
<td align="left">overridden</td>
<td align="right">19,303</td>
<td align="right">1.2%</td>
<td align="right">14,312</td>
<td align="right">2.3%</td>
<td align="right">-25.9%</td>
</tr>
<tr>
<td align="left">metaclass attribute</td>
<td align="right">190,853</td>
<td align="right">11.6%</td>
<td align="right">147,345</td>
<td align="right">23.7%</td>
<td align="right">-22.8%</td>
</tr>
<tr>
<td align="left">mutable class</td>
<td align="right">77,291</td>
<td align="right">4.7%</td>
<td align="right">61,504</td>
<td align="right">9.9%</td>
<td align="right">-20.4%</td>
</tr>
<tr>
<td align="left">method</td>
<td align="right">117,858</td>
<td align="right">7.2%</td>
<td align="right">98,530</td>
<td align="right">15.8%</td>
<td align="right">-16.4%</td>
</tr>
<tr>
<td align="left">non string or split</td>
<td align="right">22,015</td>
<td align="right">1.3%</td>
<td align="right">21,011</td>
<td align="right">3.4%</td>
<td align="right">-4.6%</td>
</tr>
<tr>
<td align="left">non object slot</td>
<td align="right">3,540</td>
<td align="right">0.2%</td>
<td align="right">3,520</td>
<td align="right">0.6%</td>
<td align="right">-0.6%</td>
</tr>
<tr>
<td align="left">wrong number arguments</td>
<td align="right">1,100</td>
<td align="right">0.1%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">not in dict</td>
<td align="right">320</td>
<td align="right">0.0%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
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
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">458,375</td>
<td align="right">0.0%</td>
<td align="right">300,584</td>
<td align="right">0.0%</td>
<td align="right">-34.4%</td>
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
<td align="right">9,003</td>
<td align="right">0.0%</td>
<td align="right">-31.4%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">5,661,467,998</td>
<td align="right">99.6%</td>
<td align="right">4,794,726,236</td>
<td align="right">99.6%</td>
<td align="right">-15.3%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">20,562,966</td>
<td align="right">0.4%</td>
<td align="right">20,152,824</td>
<td align="right">0.4%</td>
<td align="right">-2.0%</td>
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
<td align="right">668,110</td>
<td align="right">100.0%</td>
<td align="right">415,685</td>
<td align="right">100.0%</td>
<td align="right">-37.8%</td>
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
<td align="right">11,847</td>
<td align="right">0.0%</td>
<td align="right">7,288</td>
<td align="right">0.0%</td>
<td align="right">-38.5%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">134,609,369</td>
<td align="right">100.0%</td>
<td align="right">85,512,160</td>
<td align="right">100.0%</td>
<td align="right">-36.5%</td>
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
<td align="right">7,144</td>
<td align="right">100.0%</td>
<td align="right">-39.0%</td>
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
<td align="right">173,800,951</td>
<td align="right">18.1%</td>
<td align="right">165,298,418</td>
<td align="right">17.5%</td>
<td align="right">-4.9%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">787,078,099</td>
<td align="right">81.9%</td>
<td align="right">779,964,507</td>
<td align="right">82.5%</td>
<td align="right">-0.9%</td>
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
<td align="right">52,571</td>
<td align="right">89.5%</td>
<td align="right">-14.9%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">7,153</td>
<td align="right">10.4%</td>
<td align="right">6,193</td>
<td align="right">10.5%</td>
<td align="right">-13.4%</td>
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
<td align="right">9,980</td>
<td align="right">16.2%</td>
<td align="right">3,241</td>
<td align="right">6.2%</td>
<td align="right">-67.5%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">16,129</td>
<td align="right">26.1%</td>
<td align="right">15,910</td>
<td align="right">30.3%</td>
<td align="right">-1.4%</td>
</tr>
<tr>
<td align="left">async generator send</td>
<td align="right">33,180</td>
<td align="right">53.7%</td>
<td align="right">33,180</td>
<td align="right">63.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">2,220</td>
<td align="right">3.6%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">dict keys</td>
<td align="right">240</td>
<td align="right">0.4%</td>
<td align="right">240</td>
<td align="right">0.5%</td>
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
<td align="right">166,050,435</td>
<td align="right">6.0%</td>
<td align="right">63,124,606</td>
<td align="right">2.8%</td>
<td align="right">-62.0%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">239,359,015</td>
<td align="right">8.6%</td>
<td align="right">92,576,128</td>
<td align="right">4.1%</td>
<td align="right">-61.3%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">2,530,087,666</td>
<td align="right">91.2%</td>
<td align="right">2,148,340,924</td>
<td align="right">95.8%</td>
<td align="right">-15.1%</td>
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
<td align="right">3,281,982</td>
<td align="right">95.7%</td>
<td align="right">1,295,952</td>
<td align="right">94.3%</td>
<td align="right">-60.5%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">147,471</td>
<td align="right">4.3%</td>
<td align="right">78,202</td>
<td align="right">5.7%</td>
<td align="right">-47.0%</td>
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
<td align="right">49,630</td>
<td align="right">33.7%</td>
<td align="right">8,322</td>
<td align="right">10.6%</td>
<td align="right">-83.2%</td>
</tr>
<tr>
<td align="left">not in dict</td>
<td align="right">15,645</td>
<td align="right">10.6%</td>
<td align="right">7,078</td>
<td align="right">9.1%</td>
<td align="right">-54.8%</td>
</tr>
<tr>
<td align="left">not in keys</td>
<td align="right">7,781</td>
<td align="right">5.3%</td>
<td align="right">3,699</td>
<td align="right">4.7%</td>
<td align="right">-52.5%</td>
</tr>
<tr>
<td align="left">mutable class</td>
<td align="right">40</td>
<td align="right">0.0%</td>
<td align="right">20</td>
<td align="right">0.0%</td>
<td align="right">-50.0%</td>
</tr>
<tr>
<td align="left">overridden</td>
<td align="right">6,932</td>
<td align="right">4.7%</td>
<td align="right">4,509</td>
<td align="right">5.8%</td>
<td align="right">-35.0%</td>
</tr>
<tr>
<td align="left">not managed dict</td>
<td align="right">28,510</td>
<td align="right">19.3%</td>
<td align="right">21,266</td>
<td align="right">27.2%</td>
<td align="right">-25.4%</td>
</tr>
<tr>
<td align="left">overriding descriptor</td>
<td align="right">10,660</td>
<td align="right">7.2%</td>
<td align="right">8,421</td>
<td align="right">10.8%</td>
<td align="right">-21.0%</td>
</tr>
<tr>
<td align="left">property</td>
<td align="right">5,580</td>
<td align="right">3.8%</td>
<td align="right">4,529</td>
<td align="right">5.8%</td>
<td align="right">-18.8%</td>
</tr>
<tr>
<td align="left">non string or split</td>
<td align="right">15,440</td>
<td align="right">10.5%</td>
<td align="right">14,149</td>
<td align="right">18.1%</td>
<td align="right">-8.4%</td>
</tr>
<tr>
<td align="left">no dict</td>
<td align="right">5,180</td>
<td align="right">3.5%</td>
<td align="right">4,749</td>
<td align="right">6.1%</td>
<td align="right">-8.3%</td>
</tr>
<tr>
<td align="left">method</td>
<td align="right">1,500</td>
<td align="right">1.0%</td>
<td align="right">1,460</td>
<td align="right">1.9%</td>
<td align="right">-2.7%</td>
</tr>
<tr>
<td align="left">out of versions</td>
<td align="right">573</td>
<td align="right">0.4%</td>
<td align="right"></td>
<td align="right"></td>
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
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">246,099,304</td>
<td align="right">77.9%</td>
<td align="right">200,829,132</td>
<td align="right">75.1%</td>
<td align="right">-18.4%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">69,610,565</td>
<td align="right">22.0%</td>
<td align="right">66,453,698</td>
<td align="right">24.9%</td>
<td align="right">-4.5%</td>
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
<td align="right">18,707</td>
<td align="right">22.0%</td>
<td align="right">13,108</td>
<td align="right">19.3%</td>
<td align="right">-29.9%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">66,371</td>
<td align="right">78.0%</td>
<td align="right">54,637</td>
<td align="right">80.7%</td>
<td align="right">-17.7%</td>
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
<td align="right">2,028</td>
<td align="right">3.1%</td>
<td align="right">648</td>
<td align="right">1.2%</td>
<td align="right">-68.0%</td>
</tr>
<tr>
<td align="left">bytearray int</td>
<td align="right">1,340</td>
<td align="right">2.0%</td>
<td align="right">644</td>
<td align="right">1.2%</td>
<td align="right">-51.9%</td>
</tr>
<tr>
<td align="left">py simple</td>
<td align="right">42,498</td>
<td align="right">64.0%</td>
<td align="right">35,208</td>
<td align="right">64.4%</td>
<td align="right">-17.2%</td>
</tr>
<tr>
<td align="left">dict subclass no override</td>
<td align="right">11,865</td>
<td align="right">17.9%</td>
<td align="right">9,831</td>
<td align="right">18.0%</td>
<td align="right">-17.1%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">2,080</td>
<td align="right">3.1%</td>
<td align="right">1,746</td>
<td align="right">3.2%</td>
<td align="right">-16.1%</td>
</tr>
<tr>
<td align="left">array int</td>
<td align="right">6,560</td>
<td align="right">9.9%</td>
<td align="right">6,560</td>
<td align="right">12.0%</td>
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
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">104,385,646</td>
<td align="right">2.8%</td>
<td align="right">79,698,883</td>
<td align="right">2.5%</td>
<td align="right">-23.6%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">3,420,793,297</td>
<td align="right">90.9%</td>
<td align="right">2,877,151,060</td>
<td align="right">90.5%</td>
<td align="right">-15.9%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">340,146,613</td>
<td align="right">9.0%</td>
<td align="right">299,708,244</td>
<td align="right">9.4%</td>
<td align="right">-11.9%</td>
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
<td align="right">621,325</td>
<td align="right">21.6%</td>
<td align="right">346,866</td>
<td align="right">17.2%</td>
<td align="right">-44.2%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">2,253,962</td>
<td align="right">78.4%</td>
<td align="right">1,667,968</td>
<td align="right">82.8%</td>
<td align="right">-26.0%</td>
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
<td align="left">number</td>
<td align="right">181,557</td>
<td align="right">29.2%</td>
<td align="right">3,855</td>
<td align="right">1.1%</td>
<td align="right">-97.9%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">95,107</td>
<td align="right">15.3%</td>
<td align="right">28,769</td>
<td align="right">8.3%</td>
<td align="right">-69.8%</td>
</tr>
<tr>
<td align="left">dict</td>
<td align="right">31,552</td>
<td align="right">5.1%</td>
<td align="right">23,739</td>
<td align="right">6.8%</td>
<td align="right">-24.8%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">40,243</td>
<td align="right">6.5%</td>
<td align="right">31,131</td>
<td align="right">9.0%</td>
<td align="right">-22.6%</td>
</tr>
<tr>
<td align="left">mapping</td>
<td align="right">57,852</td>
<td align="right">9.3%</td>
<td align="right">48,111</td>
<td align="right">13.9%</td>
<td align="right">-16.8%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">174,318</td>
<td align="right">28.1%</td>
<td align="right">170,887</td>
<td align="right">49.3%</td>
<td align="right">-2.0%</td>
</tr>
<tr>
<td align="left">bytes</td>
<td align="right">18,695</td>
<td align="right">3.0%</td>
<td align="right">18,494</td>
<td align="right">5.3%</td>
<td align="right">-1.1%</td>
</tr>
<tr>
<td align="left">sequence</td>
<td align="right">18,020</td>
<td align="right">2.9%</td>
<td align="right">17,900</td>
<td align="right">5.2%</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">float</td>
<td align="right">2,321</td>
<td align="right">0.4%</td>
<td align="right">2,320</td>
<td align="right">0.7%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">bytearray</td>
<td align="right">1,240</td>
<td align="right">0.2%</td>
<td align="right">1,240</td>
<td align="right">0.4%</td>
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
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">410,598</td>
<td align="right">0.1%</td>
<td align="right">325,525</td>
<td align="right">0.1%</td>
<td align="right">-20.7%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">463,516,751</td>
<td align="right">99.9%</td>
<td align="right">429,437,317</td>
<td align="right">99.9%</td>
<td align="right">-7.4%</td>
</tr>
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
<td align="right">39,833</td>
<td align="right">91.9%</td>
<td align="right">26,655</td>
<td align="right">91.7%</td>
<td align="right">-33.1%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">3,513</td>
<td align="right">8.1%</td>
<td align="right">2,414</td>
<td align="right">8.3%</td>
<td align="right">-31.3%</td>
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
<td align="right">420</td>
<td align="right">17.4%</td>
<td align="right">-38.3%</td>
</tr>
<tr>
<td align="left">sequence</td>
<td align="right">2,492</td>
<td align="right">70.9%</td>
<td align="right">1,654</td>
<td align="right">68.5%</td>
<td align="right">-33.6%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">340</td>
<td align="right">9.7%</td>
<td align="right">340</td>
<td align="right">14.1%</td>
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
<td align="right">1,135,621,871</td>
<td align="right">1.0%</td>
<td align="right">593,238,073</td>
<td align="right">0.6%</td>
<td align="right">-47.8%</td>
</tr>
<tr>
<td align="left">
Not specialized
<details>
<summary>ⓘ</summary>

Instructions that could be specialized but aren't, e.g. `LOAD_ATTR`, `BINARY_SLICE`.
</details>
</td>
<td align="right">11,361,249,049</td>
<td align="right">9.5%</td>
<td align="right">9,342,158,593</td>
<td align="right">9.1%</td>
<td align="right">-17.8%</td>
</tr>
<tr>
<td align="left">
Basic
<details>
<summary>ⓘ</summary>

Instructions that are not and cannot be specialized, e.g. `LOAD_FAST`.
</details>
</td>
<td align="right">65,242,741,383</td>
<td align="right">54.7%</td>
<td align="right">56,335,812,053</td>
<td align="right">55.0%</td>
<td align="right">-13.7%</td>
</tr>
<tr>
<td align="left">
Specialized hits
<details>
<summary>ⓘ</summary>

Specialized instructions, e.g. `LOAD_ATTR_MODULE` that complete.
</details>
</td>
<td align="right">41,459,053,712</td>
<td align="right">34.8%</td>
<td align="right">36,248,508,567</td>
<td align="right">35.4%</td>
<td align="right">-12.6%</td>
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
<td align="left">STORE_ATTR</td>
<td align="right">239,359,015</td>
<td align="right">4.9%</td>
<td align="right">92,576,128</td>
<td align="right">2.8%</td>
<td align="right">-61.3%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">1,454,778,256</td>
<td align="right">29.5%</td>
<td align="right">801,399,825</td>
<td align="right">23.9%</td>
<td align="right">-44.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">1,373,437,511</td>
<td align="right">27.8%</td>
<td align="right">804,202,237</td>
<td align="right">24.0%</td>
<td align="right">-41.4%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">107,117,016</td>
<td align="right">2.2%</td>
<td align="right">67,937,897</td>
<td align="right">2.0%</td>
<td align="right">-36.6%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">145,336,316</td>
<td align="right">2.9%</td>
<td align="right">117,791,165</td>
<td align="right">3.5%</td>
<td align="right">-19.0%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">120,243,391</td>
<td align="right">2.4%</td>
<td align="right">99,629,186</td>
<td align="right">3.0%</td>
<td align="right">-17.1%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">340,146,613</td>
<td align="right">6.9%</td>
<td align="right">299,708,244</td>
<td align="right">9.0%</td>
<td align="right">-11.9%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR</td>
<td align="right">268,976,663</td>
<td align="right">5.5%</td>
<td align="right">240,811,563</td>
<td align="right">7.2%</td>
<td align="right">-10.5%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">618,394,108</td>
<td align="right">12.5%</td>
<td align="right">571,831,160</td>
<td align="right">17.1%</td>
<td align="right">-7.5%</td>
</tr>
<tr>
<td align="left">SEND</td>
<td align="right">173,800,951</td>
<td align="right">3.5%</td>
<td align="right">165,298,418</td>
<td align="right">4.9%</td>
<td align="right">-4.9%</td>
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
<td align="left">STORE_ATTR_SLOT</td>
<td align="right">95,403,887</td>
<td align="right">8.4%</td>
<td align="right">27,978,611</td>
<td align="right">4.7%</td>
<td align="right">-70.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">158,642,718</td>
<td align="right">14.0%</td>
<td align="right">66,749,172</td>
<td align="right">11.2%</td>
<td align="right">-57.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">178,839,859</td>
<td align="right">15.7%</td>
<td align="right">86,316,070</td>
<td align="right">14.5%</td>
<td align="right">-51.7%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">70,593,756</td>
<td align="right">6.2%</td>
<td align="right">35,128,823</td>
<td align="right">5.9%</td>
<td align="right">-50.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">109,139,507</td>
<td align="right">9.6%</td>
<td align="right">54,591,601</td>
<td align="right">9.2%</td>
<td align="right">-50.0%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">128,055,084</td>
<td align="right">11.3%</td>
<td align="right">83,189,005</td>
<td align="right">14.0%</td>
<td align="right">-35.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL_ALWAYS_TRUE</td>
<td align="right">47,518,971</td>
<td align="right">4.2%</td>
<td align="right">36,814,198</td>
<td align="right">6.2%</td>
<td align="right">-22.5%</td>
</tr>
<tr>
<td align="left">TO_BOOL_NONE</td>
<td align="right">48,974,005</td>
<td align="right">4.3%</td>
<td align="right">39,121,467</td>
<td align="right">6.6%</td>
<td align="right">-20.1%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">42,363,830</td>
<td align="right">3.7%</td>
<td align="right">38,616,808</td>
<td align="right">6.5%</td>
<td align="right">-8.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right">59,607,376</td>
<td align="right">5.2%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">27,788,692</td>
<td align="right">4.7%</td>
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
<td align="left">Calls via PyEval_EvalFrame (build class)</td>
<td align="right">30,746</td>
<td align="right">0.0%</td>
<td align="right">13,679</td>
<td align="right">0.0%</td>
<td align="right">-55.5%</td>
</tr>
<tr>
<td align="left">Frame objects created</td>
<td align="right">88,456,229</td>
<td align="right">1.0%</td>
<td align="right">71,309,182</td>
<td align="right">0.9%</td>
<td align="right">-19.4%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (api)</td>
<td align="right">254,693,391</td>
<td align="right">2.9%</td>
<td align="right">220,766,169</td>
<td align="right">2.9%</td>
<td align="right">-13.3%</td>
</tr>
<tr>
<td align="left">Calls to Python functions inlined</td>
<td align="right">6,386,384,527</td>
<td align="right">73.4%</td>
<td align="right">5,568,147,945</td>
<td align="right">72.1%</td>
<td align="right">-12.8%</td>
</tr>
<tr>
<td align="left">Frames pushed</td>
<td align="right">6,954,529,106</td>
<td align="right">79.9%</td>
<td align="right">6,070,641,507</td>
<td align="right">78.6%</td>
<td align="right">-12.7%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (function ex)</td>
<td align="right">38,359,643</td>
<td align="right">0.4%</td>
<td align="right">33,741,740</td>
<td align="right">0.4%</td>
<td align="right">-12.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (function vectorcall)</td>
<td align="right">1,445,035,646</td>
<td align="right">16.6%</td>
<td align="right">1,305,351,694</td>
<td align="right">16.9%</td>
<td align="right">-9.7%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (vector)</td>
<td align="right">1,447,724,716</td>
<td align="right">16.6%</td>
<td align="right">1,308,013,905</td>
<td align="right">16.9%</td>
<td align="right">-9.7%</td>
</tr>
<tr>
<td align="left">Calls to PyEval_EvalDefault</td>
<td align="right">2,312,694,118</td>
<td align="right">26.6%</td>
<td align="right">2,155,991,870</td>
<td align="right">27.9%</td>
<td align="right">-6.8%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (total)</td>
<td align="right">2,312,694,118</td>
<td align="right">26.6%</td>
<td align="right">2,155,991,870</td>
<td align="right">27.9%</td>
<td align="right">-6.8%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (slot)</td>
<td align="right">479,278,358</td>
<td align="right">5.5%</td>
<td align="right">452,227,778</td>
<td align="right">5.9%</td>
<td align="right">-5.6%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (generator)</td>
<td align="right">864,969,402</td>
<td align="right">9.9%</td>
<td align="right">847,977,965</td>
<td align="right">11.0%</td>
<td align="right">-2.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (legacy)</td>
<td align="right">2,658,324</td>
<td align="right">0.0%</td>
<td align="right">2,648,532</td>
<td align="right">0.0%</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (method)</td>
<td align="right">213,135,997</td>
<td align="right">2.5%</td>
<td align="right">213,132,297</td>
<td align="right">2.8%</td>
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
<td align="left">Method cache misses</td>
<td align="right">76,877,937</td>
<td align="right"></td>
<td align="right">15,484,422</td>
<td align="right"></td>
<td align="right">-79.9%</td>
</tr>
<tr>
<td align="left">Method cache collisions</td>
<td align="right">84,812,125</td>
<td align="right"></td>
<td align="right">23,810,599</td>
<td align="right"></td>
<td align="right">-71.9%</td>
</tr>
<tr>
<td align="left">Materialize dict (new key)</td>
<td align="right">116,335</td>
<td align="right">0.1%</td>
<td align="right">38,516</td>
<td align="right">0.0%</td>
<td align="right">-66.9%</td>
</tr>
<tr>
<td align="left">Method cache dunder misses</td>
<td align="right">15,694,415</td>
<td align="right"></td>
<td align="right">8,520,058</td>
<td align="right"></td>
<td align="right">-45.7%</td>
</tr>
<tr>
<td align="left">Method cache hits</td>
<td align="right">3,108,422,451</td>
<td align="right"></td>
<td align="right">2,149,029,488</td>
<td align="right"></td>
<td align="right">-30.9%</td>
</tr>
<tr>
<td align="left">Increfs</td>
<td align="right">27,335,797,969</td>
<td align="right">22.7%</td>
<td align="right">22,532,422,558</td>
<td align="right">21.3%</td>
<td align="right">-17.6%</td>
</tr>
<tr>
<td align="left">Decrefs</td>
<td align="right">30,197,222,469</td>
<td align="right">21.9%</td>
<td align="right">25,600,061,493</td>
<td align="right">21.0%</td>
<td align="right">-15.2%</td>
</tr>
<tr>
<td align="left">Method cache dunder hits</td>
<td align="right">3,555,502,339</td>
<td align="right"></td>
<td align="right">3,025,962,972</td>
<td align="right"></td>
<td align="right">-14.9%</td>
</tr>
<tr>
<td align="left">Inline values</td>
<td align="right">182,644,502</td>
<td align="right"></td>
<td align="right">158,696,755</td>
<td align="right"></td>
<td align="right">-13.1%</td>
</tr>
<tr>
<td align="left">Materialize dict (on request)</td>
<td align="right">6,618,866</td>
<td align="right">3.6%</td>
<td align="right">5,826,044</td>
<td align="right">3.7%</td>
<td align="right">-12.0%</td>
</tr>
<tr>
<td align="left">Allocations to 512 bytes</td>
<td align="right">11,577,667,881</td>
<td align="right">62.6%</td>
<td align="right">10,219,814,068</td>
<td align="right">61.7%</td>
<td align="right">-11.7%</td>
</tr>
<tr>
<td align="left">Allocations</td>
<td align="right">11,703,736,042</td>
<td align="right">63.2%</td>
<td align="right">10,343,328,284</td>
<td align="right">62.4%</td>
<td align="right">-11.6%</td>
</tr>
<tr>
<td align="left">Frees</td>
<td align="right">12,048,758,880</td>
<td align="right"></td>
<td align="right">10,679,158,787</td>
<td align="right"></td>
<td align="right">-11.4%</td>
</tr>
<tr>
<td align="left">Interpreter decrefs</td>
<td align="right">107,625,268,126</td>
<td align="right">78.1%</td>
<td align="right">96,072,891,512</td>
<td align="right">79.0%</td>
<td align="right">-10.7%</td>
</tr>
<tr>
<td align="left">Interpreter increfs</td>
<td align="right">93,046,830,382</td>
<td align="right">77.3%</td>
<td align="right">83,189,272,816</td>
<td align="right">78.7%</td>
<td align="right">-10.6%</td>
</tr>
<tr>
<td align="left">Allocations from freelist</td>
<td align="right">6,802,440,437</td>
<td align="right">36.8%</td>
<td align="right">6,220,872,389</td>
<td align="right">37.6%</td>
<td align="right">-8.5%</td>
</tr>
<tr>
<td align="left">Frees to freelist</td>
<td align="right">6,804,436,572</td>
<td align="right"></td>
<td align="right">6,222,701,617</td>
<td align="right"></td>
<td align="right">-8.5%</td>
</tr>
<tr>
<td align="left">Allocations over 4 kbytes</td>
<td align="right">21,166,914</td>
<td align="right">0.1%</td>
<td align="right">20,369,350</td>
<td align="right">0.1%</td>
<td align="right">-3.8%</td>
</tr>
<tr>
<td align="left">Allocations to 4 kbytes</td>
<td align="right">104,901,247</td>
<td align="right">0.6%</td>
<td align="right">103,144,866</td>
<td align="right">0.6%</td>
<td align="right">-1.7%</td>
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
<td align="right">115,752,239</td>
<td align="right">17,050,117,473</td>
<td align="right">0</td>
<td align="right">19,464,364</td>
<td align="right">14,237,123,419</td>
</tr>
<tr>
<td align="right">2</td>
<td align="right">0</td>
<td align="right">10,755,840</td>
<td align="right">6,969,689,460</td>
<td align="right">0</td>
<td align="right">10,755,840</td>
<td align="right">6,969,724,980</td>
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
Trace stack overflow
<details>
<summary>ⓘ</summary>

A trace is truncated because it would require more than 5 stack frames.
</details>
</td>
<td align="right">1,094</td>
<td align="right">0.1%</td>
<td align="right">260</td>
<td align="right">0.0%</td>
<td align="right">-76.2%</td>
</tr>
<tr>
<td align="left">
Recursive call
<details>
<summary>ⓘ</summary>

A trace is truncated because it has a recursive call.
</details>
</td>
<td align="right">2,353</td>
<td align="right">0.3%</td>
<td align="right">1,229</td>
<td align="right">0.2%</td>
<td align="right">-47.8%</td>
</tr>
<tr>
<td align="left">
Low confidence
<details>
<summary>ⓘ</summary>

A trace is abandoned because the likelihood of the jump to top being taken is too low.
</details>
</td>
<td align="right">8,461</td>
<td align="right">1.1%</td>
<td align="right">4,688</td>
<td align="right">0.9%</td>
<td align="right">-44.6%</td>
</tr>
<tr>
<td align="left">
Traces created
<details>
<summary>ⓘ</summary>

The number of traces that were successfully created.
</details>
</td>
<td align="right">137,943</td>
<td align="right">18.7%</td>
<td align="right">77,247</td>
<td align="right">14.2%</td>
<td align="right">-44.0%</td>
</tr>
<tr>
<td align="left">
Inner loop found
<details>
<summary>ⓘ</summary>

A trace is truncated because it has an inner loop
</details>
</td>
<td align="right">18,948</td>
<td align="right">2.6%</td>
<td align="right">13,419</td>
<td align="right">2.5%</td>
<td align="right">-29.2%</td>
</tr>
<tr>
<td align="left">
Optimization attempts
<details>
<summary>ⓘ</summary>

The number of times a potential trace is identified.  Specifically, this occurs in the JUMP BACKWARD instruction when the counter reaches a threshold.
</details>
</td>
<td align="right">739,436</td>
<td align="right"></td>
<td align="right">544,512</td>
<td align="right"></td>
<td align="right">-26.4%</td>
</tr>
<tr>
<td align="left">
Trace too short
<details>
<summary>ⓘ</summary>

A potential trace is abandoced because it it too short.
</details>
</td>
<td align="right">601,493</td>
<td align="right">81.3%</td>
<td align="right">467,265</td>
<td align="right">85.8%</td>
<td align="right">-22.3%</td>
</tr>
<tr>
<td align="left">
Trace stack underflow
<details>
<summary>ⓘ</summary>

A potential trace is abandoned because it pops more frames than it pushes.
</details>
</td>
<td align="right">147,922</td>
<td align="right">20.0%</td>
<td align="right">120,195</td>
<td align="right">22.1%</td>
<td align="right">-18.7%</td>
</tr>
<tr>
<td align="left">
Traces executed
<details>
<summary>ⓘ</summary>

The number of traces that were executed
</details>
</td>
<td align="right">7,078,019,566</td>
<td align="right"></td>
<td align="right">5,932,657,537</td>
<td align="right"></td>
<td align="right">-16.2%</td>
</tr>
<tr>
<td align="left">
Executors invalidated
<details>
<summary>ⓘ</summary>

The number of executors that were invalidated due to watched dictionary changes.
</details>
</td>
<td align="right">5,640</td>
<td align="right">4.1%</td>
<td align="right">5,122</td>
<td align="right">6.6%</td>
<td align="right">-9.2%</td>
</tr>
<tr>
<td align="left">
Uops executed
<details>
<summary>ⓘ</summary>

The total number of uops (micro-operations) that were executed
</details>
</td>
<td align="right">191,290,465,842</td>
<td align="right">2,702.6%</td>
<td align="right">180,521,731,081</td>
<td align="right">3,042.8%</td>
<td align="right">-5.6%</td>
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
<td align="right">135,763</td>
<td align="right">98.4%</td>
<td align="right">75,427</td>
<td align="right">97.6%</td>
<td align="right">-44.4%</td>
</tr>
<tr>
<td align="left">
Optimizer attempts
<details>
<summary>ⓘ</summary>

The number of times the trace optimizer (_Py_uop_analyze_and_optimize) was run.
</details>
</td>
<td align="right">137,943</td>
<td align="right"></td>
<td align="right">77,247</td>
<td align="right"></td>
<td align="right">-44.0%</td>
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
<td align="right">1.5%</td>
<td align="right">1,780</td>
<td align="right">2.3%</td>
<td align="right">-16.0%</td>
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
<td align="right">3,250</td>
<td align="right">2.4%</td>
<td align="right">1,603</td>
<td align="right">2.1%</td>
<td align="right">-50.7%</td>
</tr>
<tr>
<td align="left"><= 16</td>
<td align="right">22,788</td>
<td align="right">16.5%</td>
<td align="right">13,019</td>
<td align="right">16.9%</td>
<td align="right">-42.9%</td>
</tr>
<tr>
<td align="left"><= 32</td>
<td align="right">53,890</td>
<td align="right">39.1%</td>
<td align="right">29,210</td>
<td align="right">37.8%</td>
<td align="right">-45.8%</td>
</tr>
<tr>
<td align="left"><= 64</td>
<td align="right">32,300</td>
<td align="right">23.4%</td>
<td align="right">18,561</td>
<td align="right">24.0%</td>
<td align="right">-42.5%</td>
</tr>
<tr>
<td align="left"><= 128</td>
<td align="right">18,238</td>
<td align="right">13.2%</td>
<td align="right">10,531</td>
<td align="right">13.6%</td>
<td align="right">-42.3%</td>
</tr>
<tr>
<td align="left"><= 256</td>
<td align="right">6,106</td>
<td align="right">4.4%</td>
<td align="right">3,583</td>
<td align="right">4.6%</td>
<td align="right">-41.3%</td>
</tr>
<tr>
<td align="left"><= 512</td>
<td align="right">1,371</td>
<td align="right">1.0%</td>
<td align="right">740</td>
<td align="right">1.0%</td>
<td align="right">-46.0%</td>
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
<td align="right">852</td>
<td align="right">0.6%</td>
<td align="right">241</td>
<td align="right">0.3%</td>
<td align="right">-71.7%</td>
</tr>
<tr>
<td align="left"><= 8</td>
<td align="right">10,926</td>
<td align="right">7.9%</td>
<td align="right">7,569</td>
<td align="right">9.8%</td>
<td align="right">-30.7%</td>
</tr>
<tr>
<td align="left"><= 16</td>
<td align="right">44,778</td>
<td align="right">32.5%</td>
<td align="right">23,249</td>
<td align="right">30.1%</td>
<td align="right">-48.1%</td>
</tr>
<tr>
<td align="left"><= 32</td>
<td align="right">44,911</td>
<td align="right">32.6%</td>
<td align="right">24,345</td>
<td align="right">31.5%</td>
<td align="right">-45.8%</td>
</tr>
<tr>
<td align="left"><= 64</td>
<td align="right">22,285</td>
<td align="right">16.2%</td>
<td align="right">12,979</td>
<td align="right">16.8%</td>
<td align="right">-41.8%</td>
</tr>
<tr>
<td align="left"><= 128</td>
<td align="right">9,242</td>
<td align="right">6.7%</td>
<td align="right">5,244</td>
<td align="right">6.8%</td>
<td align="right">-43.3%</td>
</tr>
<tr>
<td align="left"><= 256</td>
<td align="right">2,629</td>
<td align="right">1.9%</td>
<td align="right">1,640</td>
<td align="right">2.1%</td>
<td align="right">-37.6%</td>
</tr>
<tr>
<td align="left"><= 512</td>
<td align="right">140</td>
<td align="right">0.1%</td>
<td align="right">160</td>
<td align="right">0.2%</td>
<td align="right">14.3%</td>
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
<td align="right">0.4%</td>
<td align="right">25,847,900</td>
<td align="right">0.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left"><= 4</td>
<td align="right">999,246,618</td>
<td align="right">14.1%</td>
<td align="right">741,672,254</td>
<td align="right">12.5%</td>
<td align="right">-25.8%</td>
</tr>
<tr>
<td align="left"><= 8</td>
<td align="right">733,504,022</td>
<td align="right">10.4%</td>
<td align="right">580,779,774</td>
<td align="right">9.8%</td>
<td align="right">-20.8%</td>
</tr>
<tr>
<td align="left"><= 16</td>
<td align="right">1,332,912,203</td>
<td align="right">18.8%</td>
<td align="right">984,390,612</td>
<td align="right">16.6%</td>
<td align="right">-26.1%</td>
</tr>
<tr>
<td align="left"><= 32</td>
<td align="right">1,056,004,278</td>
<td align="right">14.9%</td>
<td align="right">965,037,988</td>
<td align="right">16.3%</td>
<td align="right">-8.6%</td>
</tr>
<tr>
<td align="left"><= 64</td>
<td align="right">628,280,500</td>
<td align="right">8.9%</td>
<td align="right">602,544,492</td>
<td align="right">10.2%</td>
<td align="right">-4.1%</td>
</tr>
<tr>
<td align="left"><= 128</td>
<td align="right">316,812,988</td>
<td align="right">4.5%</td>
<td align="right">318,510,793</td>
<td align="right">5.4%</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left"><= 256</td>
<td align="right">188,377,767</td>
<td align="right">2.7%</td>
<td align="right">187,727,001</td>
<td align="right">3.2%</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left"><= 512</td>
<td align="right">23,675,678</td>
<td align="right">0.3%</td>
<td align="right">23,327,522</td>
<td align="right">0.4%</td>
<td align="right">-1.5%</td>
</tr>
<tr>
<td align="left"><= 1,024</td>
<td align="right">7,729,381</td>
<td align="right">0.1%</td>
<td align="right">7,493,138</td>
<td align="right">0.1%</td>
<td align="right">-3.1%</td>
</tr>
<tr>
<td align="left"><= 2,048</td>
<td align="right">17,763,082</td>
<td align="right">0.3%</td>
<td align="right">17,607,118</td>
<td align="right">0.3%</td>
<td align="right">-0.9%</td>
</tr>
<tr>
<td align="left"><= 4,096</td>
<td align="right">611,448</td>
<td align="right">0.0%</td>
<td align="right">632,058</td>
<td align="right">0.0%</td>
<td align="right">3.4%</td>
</tr>
<tr>
<td align="left"><= 8,192</td>
<td align="right">747,332</td>
<td align="right">0.0%</td>
<td align="right">737,224</td>
<td align="right">0.0%</td>
<td align="right">-1.4%</td>
</tr>
<tr>
<td align="left"><= 16,384</td>
<td align="right">237,561</td>
<td align="right">0.0%</td>
<td align="right">235,403</td>
<td align="right">0.0%</td>
<td align="right">-0.9%</td>
</tr>
<tr>
<td align="left"><= 32,768</td>
<td align="right">43,860</td>
<td align="right">0.0%</td>
<td align="right">42,341</td>
<td align="right">0.0%</td>
<td align="right">-3.5%</td>
</tr>
<tr>
<td align="left"><= 65,536</td>
<td align="right">13,235</td>
<td align="right">0.0%</td>
<td align="right">12,420</td>
<td align="right">0.0%</td>
<td align="right">-6.2%</td>
</tr>
<tr>
<td align="left"><= 131,072</td>
<td align="right">765</td>
<td align="right">0.0%</td>
<td align="right">382</td>
<td align="right">0.0%</td>
<td align="right">-50.1%</td>
</tr>
<tr>
<td align="left"><= 262,144</td>
<td align="right">2,080</td>
<td align="right">0.0%</td>
<td align="right">2,000</td>
<td align="right">0.0%</td>
<td align="right">-3.8%</td>
</tr>
<tr>
<td align="left"><= 524,288</td>
<td align="right">463</td>
<td align="right">0.0%</td>
<td align="right">461</td>
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
<td align="right">303</td>
<td align="right">0.0%</td>
<td align="right">301</td>
<td align="right">0.0%</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left"><= 4,194,304</td>
<td align="right">177</td>
<td align="right">0.0%</td>
<td align="right">179</td>
<td align="right">0.0%</td>
<td align="right">1.1%</td>
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
<td align="left">_LOAD_SUPER_ATTR_METHOD</td>
<td align="right">95,960</td>
<td align="right">945,454</td>
<td align="right">885.3%</td>
</tr>
<tr>
<td align="left">_STORE_GLOBAL</td>
<td align="right">1,275,340</td>
<td align="right">8,170,580</td>
<td align="right">540.7%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_CLASS_1</td>
<td align="right">3,840</td>
<td align="right">9</td>
<td align="right">-99.8%</td>
</tr>
<tr>
<td align="left">_DELETE_SUBSCR</td>
<td align="right">1,629,645</td>
<td align="right">6,256</td>
<td align="right">-99.6%</td>
</tr>
<tr>
<td align="left">_SET_ADD</td>
<td align="right">2,174,757</td>
<td align="right">49,480</td>
<td align="right">-97.7%</td>
</tr>
<tr>
<td align="left">_UNPACK_SEQUENCE</td>
<td align="right">1,642,519</td>
<td align="right">93,597</td>
<td align="right">-94.3%</td>
</tr>
<tr>
<td align="left">_DICT_MERGE</td>
<td align="right">11,664,329</td>
<td align="right">22,318,410</td>
<td align="right">91.3%</td>
</tr>
<tr>
<td align="left">_POP_TOP_LOAD_CONST_INLINE_BORROW</td>
<td align="right">1,398,926</td>
<td align="right">162,600</td>
<td align="right">-88.4%</td>
</tr>
<tr>
<td align="left">_MAKE_CELL</td>
<td align="right">6,958,429</td>
<td align="right">2,637,198</td>
<td align="right">-62.1%</td>
</tr>
<tr>
<td align="left">_STORE_ATTR</td>
<td align="right">50,774,848</td>
<td align="right">19,659,823</td>
<td align="right">-61.3%</td>
</tr>
<tr>
<td align="left">_BUILD_MAP</td>
<td align="right">16,832,732</td>
<td align="right">27,024,503</td>
<td align="right">60.5%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_AND_CLEAR</td>
<td align="right">16,478,059</td>
<td align="right">26,267,008</td>
<td align="right">59.4%</td>
</tr>
<tr>
<td align="left">_CHECK_ATTR_CLASS</td>
<td align="right">26,735,818</td>
<td align="right">12,878,036</td>
<td align="right">-51.8%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_CLASS_0</td>
<td align="right">24,833,150</td>
<td align="right">12,876,772</td>
<td align="right">-48.1%</td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_O</td>
<td align="right">24,435,964</td>
<td align="right">13,763,778</td>
<td align="right">-43.7%</td>
</tr>
<tr>
<td align="left">_CHECK_STACK_SPACE</td>
<td align="right">181,147,482</td>
<td align="right">105,685,450</td>
<td align="right">-41.7%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_NOT_NONE_POP</td>
<td align="right">159,134,572</td>
<td align="right">100,250,837</td>
<td align="right">-37.0%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_STR</td>
<td align="right">27,825,219</td>
<td align="right">17,740,729</td>
<td align="right">-36.2%</td>
</tr>
<tr>
<td align="left">_CALL_ISINSTANCE</td>
<td align="right">387,448,621</td>
<td align="right">274,657,441</td>
<td align="right">-29.1%</td>
</tr>
<tr>
<td align="left">_CHECK_ATTR_WITH_HINT</td>
<td align="right">108,606,005</td>
<td align="right">80,917,165</td>
<td align="right">-25.5%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_WITH_HINT</td>
<td align="right">108,479,324</td>
<td align="right">80,917,165</td>
<td align="right">-25.4%</td>
</tr>
<tr>
<td align="left">_FOR_ITER_TIER_TWO</td>
<td align="right">1,752,365,919</td>
<td align="right">1,379,367,887</td>
<td align="right">-21.3%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR</td>
<td align="right">1,134,342,525</td>
<td align="right">897,462,727</td>
<td align="right">-20.9%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_1</td>
<td align="right">602,475,585</td>
<td align="right">483,621,326</td>
<td align="right">-19.7%</td>
</tr>
<tr>
<td align="left">_LOAD_GLOBAL_MODULE</td>
<td align="right">55,172,989</td>
<td align="right">65,062,356</td>
<td align="right">17.9%</td>
</tr>
<tr>
<td align="left">_DEOPT</td>
<td align="right">1,135,244,908</td>
<td align="right">940,796,205</td>
<td align="right">-17.1%</td>
</tr>
<tr>
<td align="left">_START_EXECUTOR</td>
<td align="right">5,331,812,281</td>
<td align="right">4,456,602,001</td>
<td align="right">-16.4%</td>
</tr>
<tr>
<td align="left">_SIDE_EXIT</td>
<td align="right">4,195,981,376</td>
<td align="right">3,515,288,453</td>
<td align="right">-16.2%</td>
</tr>
<tr>
<td align="left">_ITER_CHECK_TUPLE</td>
<td align="right">362,446,075</td>
<td align="right">304,282,194</td>
<td align="right">-16.0%</td>
</tr>
<tr>
<td align="left">_CONTAINS_OP_DICT</td>
<td align="right">425,177,073</td>
<td align="right">357,047,587</td>
<td align="right">-16.0%</td>
</tr>
<tr>
<td align="left">_COLD_EXIT</td>
<td align="right">1,746,207,285</td>
<td align="right">1,476,055,536</td>
<td align="right">-15.5%</td>
</tr>
<tr>
<td align="left">_LIST_APPEND</td>
<td align="right">203,971,349</td>
<td align="right">172,417,560</td>
<td align="right">-15.5%</td>
</tr>
<tr>
<td align="left">_COPY_FREE_VARS</td>
<td align="right">81,215,062</td>
<td align="right">93,707,202</td>
<td align="right">15.4%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_NONE_POP</td>
<td align="right">42,013,964</td>
<td align="right">35,610,337</td>
<td align="right">-15.2%</td>
</tr>
<tr>
<td align="left">_GUARD_NOT_EXHAUSTED_TUPLE</td>
<td align="right">310,251,496</td>
<td align="right">264,268,144</td>
<td align="right">-14.8%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_2</td>
<td align="right">822,633,267</td>
<td align="right">700,965,977</td>
<td align="right">-14.8%</td>
</tr>
<tr>
<td align="left">_ITER_NEXT_TUPLE</td>
<td align="right">204,381,123</td>
<td align="right">174,692,807</td>
<td align="right">-14.5%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_ADD_UNICODE</td>
<td align="right">24,993,006</td>
<td align="right">21,382,562</td>
<td align="right">-14.4%</td>
</tr>
<tr>
<td align="left">_GUARD_NOT_EXHAUSTED_LIST</td>
<td align="right">1,368,693,616</td>
<td align="right">1,173,181,250</td>
<td align="right">-14.3%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_3</td>
<td align="right">761,858,759</td>
<td align="right">656,865,195</td>
<td align="right">-13.8%</td>
</tr>
<tr>
<td align="left">_ITER_CHECK_LIST</td>
<td align="right">1,425,043,636</td>
<td align="right">1,229,380,923</td>
<td align="right">-13.7%</td>
</tr>
<tr>
<td align="left">_CHECK_CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">77,770,394</td>
<td align="right">67,519,305</td>
<td align="right">-13.2%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">77,703,394</td>
<td align="right">67,465,865</td>
<td align="right">-13.2%</td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION</td>
<td align="right">1,304,667,213</td>
<td align="right">1,146,526,284</td>
<td align="right">-12.1%</td>
</tr>
<tr>
<td align="left">_STORE_SUBSCR_DICT</td>
<td align="right">145,417,684</td>
<td align="right">128,263,755</td>
<td align="right">-11.8%</td>
</tr>
<tr>
<td align="left">_ERROR_POP_N</td>
<td align="right">585,997</td>
<td align="right">517,343</td>
<td align="right">-11.7%</td>
</tr>
<tr>
<td align="left">_ITER_NEXT_LIST</td>
<td align="right">1,101,205,414</td>
<td align="right">978,818,150</td>
<td align="right">-11.1%</td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">232,953,899</td>
<td align="right">208,424,052</td>
<td align="right">-10.5%</td>
</tr>
<tr>
<td align="left">_LOAD_CONST_INLINE</td>
<td align="right">1,477,104,682</td>
<td align="right">1,327,814,226</td>
<td align="right">-10.1%</td>
</tr>
<tr>
<td align="left">_EXIT_TRACE</td>
<td align="right">2,655,917,498</td>
<td align="right">2,387,783,111</td>
<td align="right">-10.1%</td>
</tr>
<tr>
<td align="left">_GUARD_TYPE_VERSION</td>
<td align="right">5,925,866,356</td>
<td align="right">5,359,637,943</td>
<td align="right">-9.6%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_4</td>
<td align="right">750,239,043</td>
<td align="right">678,994,773</td>
<td align="right">-9.5%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">864,101,416</td>
<td align="right">782,814,960</td>
<td align="right">-9.4%</td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION_EXACT_ARGS</td>
<td align="right">1,892,147,386</td>
<td align="right">1,715,782,780</td>
<td align="right">-9.3%</td>
</tr>
<tr>
<td align="left">_GUARD_GLOBALS_VERSION</td>
<td align="right">107,548,521</td>
<td align="right">117,312,116</td>
<td align="right">9.1%</td>
</tr>
<tr>
<td align="left">_LOAD_CONST_INLINE_WITH_NULL</td>
<td align="right">2,030,467,629</td>
<td align="right">1,851,553,965</td>
<td align="right">-8.8%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_INT</td>
<td align="right">198,163,215</td>
<td align="right">180,897,239</td>
<td align="right">-8.7%</td>
</tr>
<tr>
<td align="left">_STORE_DEREF</td>
<td align="right">3,872,310</td>
<td align="right">4,195,742</td>
<td align="right">8.4%</td>
</tr>
<tr>
<td align="left">_CONTAINS_OP</td>
<td align="right">118,545,047</td>
<td align="right">108,818,762</td>
<td align="right">-8.2%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_5</td>
<td align="right">791,838,323</td>
<td align="right">727,446,321</td>
<td align="right">-8.1%</td>
</tr>
<tr>
<td align="left">_SAVE_RETURN_OFFSET</td>
<td align="right">1,826,760,147</td>
<td align="right">1,679,583,356</td>
<td align="right">-8.1%</td>
</tr>
<tr>
<td align="left">_CALL_LEN</td>
<td align="right">212,475,804</td>
<td align="right">195,639,041</td>
<td align="right">-7.9%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_2</td>
<td align="right">108,720,455</td>
<td align="right">100,432,640</td>
<td align="right">-7.6%</td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_FAST_WITH_KEYWORDS</td>
<td align="right">156,794,268</td>
<td align="right">144,979,761</td>
<td align="right">-7.5%</td>
</tr>
<tr>
<td align="left">_BINARY_SLICE</td>
<td align="right">121,386,098</td>
<td align="right">112,249,750</td>
<td align="right">-7.5%</td>
</tr>
<tr>
<td align="left">_UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">704,751,937</td>
<td align="right">651,853,212</td>
<td align="right">-7.5%</td>
</tr>
<tr>
<td align="left">_BINARY_SUBSCR_DICT</td>
<td align="right">416,119,370</td>
<td align="right">384,932,014</td>
<td align="right">-7.5%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_2</td>
<td align="right">3,095,666,147</td>
<td align="right">2,865,326,093</td>
<td align="right">-7.4%</td>
</tr>
<tr>
<td align="left">_PUSH_NULL</td>
<td align="right">836,104,718</td>
<td align="right">778,917,888</td>
<td align="right">-6.8%</td>
</tr>
<tr>
<td align="left">_SET_IP</td>
<td align="right">14,664,732,953</td>
<td align="right">13,668,825,332</td>
<td align="right">-6.8%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_0</td>
<td align="right">5,753,965,103</td>
<td align="right">5,364,091,988</td>
<td align="right">-6.8%</td>
</tr>
<tr>
<td align="left">_UNARY_INVERT</td>
<td align="right">13,021,174</td>
<td align="right">13,879,912</td>
<td align="right">6.6%</td>
</tr>
<tr>
<td align="left">_UNPACK_SEQUENCE_TUPLE</td>
<td align="right">295,541,170</td>
<td align="right">276,833,078</td>
<td align="right">-6.3%</td>
</tr>
<tr>
<td align="left">_CHECK_VALIDITY</td>
<td align="right">12,105,561,033</td>
<td align="right">11,353,208,331</td>
<td align="right">-6.2%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_BOOL</td>
<td align="right">2,234,413,222</td>
<td align="right">2,099,630,952</td>
<td align="right">-6.0%</td>
</tr>
<tr>
<td align="left">_BUILD_LIST</td>
<td align="right">255,596,563</td>
<td align="right">240,369,141</td>
<td align="right">-6.0%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_LIST</td>
<td align="right">54,730,067</td>
<td align="right">51,576,036</td>
<td align="right">-5.8%</td>
</tr>
<tr>
<td align="left">_CHECK_MANAGED_OBJECT_HAS_VALUES</td>
<td align="right">2,026,238,792</td>
<td align="right">1,917,075,379</td>
<td align="right">-5.4%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_INSTANCE_VALUE_0</td>
<td align="right">2,022,321,633</td>
<td align="right">1,913,457,419</td>
<td align="right">-5.4%</td>
</tr>
<tr>
<td align="left">_STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">104,018,599</td>
<td align="right">98,632,422</td>
<td align="right">-5.2%</td>
</tr>
<tr>
<td align="left">_GUARD_DORV_NO_DICT</td>
<td align="right">105,367,819</td>
<td align="right">99,981,642</td>
<td align="right">-5.1%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_6</td>
<td align="right">548,963,765</td>
<td align="right">521,071,810</td>
<td align="right">-5.1%</td>
</tr>
<tr>
<td align="left">_CALL_STR_1</td>
<td align="right">67,904,176</td>
<td align="right">64,584,317</td>
<td align="right">-4.9%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_INSTANCE_VALUE_1</td>
<td align="right">3,802,299</td>
<td align="right">3,617,960</td>
<td align="right">-4.8%</td>
</tr>
<tr>
<td align="left">_FORMAT_SIMPLE</td>
<td align="right">52,353,985</td>
<td align="right">49,891,001</td>
<td align="right">-4.7%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_4</td>
<td align="right">2,298,300,773</td>
<td align="right">2,191,081,857</td>
<td align="right">-4.7%</td>
</tr>
<tr>
<td align="left">_CHECK_STACK_SPACE_OPERAND</td>
<td align="right">959,163,359</td>
<td align="right">914,550,077</td>
<td align="right">-4.7%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_0</td>
<td align="right">419,743,825</td>
<td align="right">400,420,735</td>
<td align="right">-4.6%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS</td>
<td align="right">10,074,831</td>
<td align="right">9,617,294</td>
<td align="right">-4.5%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_TRUE_POP</td>
<td align="right">2,663,174,158</td>
<td align="right">2,543,659,823</td>
<td align="right">-4.5%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_SLOT_0</td>
<td align="right">722,841,390</td>
<td align="right">690,546,807</td>
<td align="right">-4.5%</td>
</tr>
<tr>
<td align="left">_BINARY_SUBSCR_TUPLE_INT</td>
<td align="right">163,904,625</td>
<td align="right">156,727,060</td>
<td align="right">-4.4%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_3</td>
<td align="right">3,539,978,743</td>
<td align="right">3,396,167,135</td>
<td align="right">-4.1%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_5</td>
<td align="right">2,442,144,774</td>
<td align="right">2,345,953,059</td>
<td align="right">-3.9%</td>
</tr>
<tr>
<td align="left">_RESUME_CHECK</td>
<td align="right">1,559,628,151</td>
<td align="right">1,498,247,264</td>
<td align="right">-3.9%</td>
</tr>
<tr>
<td align="left">_POP_FRAME</td>
<td align="right">811,675,893</td>
<td align="right">780,327,752</td>
<td align="right">-3.9%</td>
</tr>
<tr>
<td align="left">_GUARD_DORV_VALUES_INST_ATTR_FROM_DICT</td>
<td align="right">1,304,323,379</td>
<td align="right">1,254,353,073</td>
<td align="right">-3.8%</td>
</tr>
<tr>
<td align="left">_JUMP_TO_TOP</td>
<td align="right">2,262,196,185</td>
<td align="right">2,176,927,327</td>
<td align="right">-3.8%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_1</td>
<td align="right">6,667,328,699</td>
<td align="right">6,421,096,435</td>
<td align="right">-3.7%</td>
</tr>
<tr>
<td align="left">_GUARD_KEYS_VERSION</td>
<td align="right">1,255,404,060</td>
<td align="right">1,210,238,610</td>
<td align="right">-3.6%</td>
</tr>
<tr>
<td align="left">_CONVERT_VALUE</td>
<td align="right">51,694,900</td>
<td align="right">49,836,987</td>
<td align="right">-3.6%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_FALSE_POP</td>
<td align="right">5,650,227,438</td>
<td align="right">5,457,306,645</td>
<td align="right">-3.4%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_6</td>
<td align="right">1,275,518,517</td>
<td align="right">1,233,234,615</td>
<td align="right">-3.3%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_1</td>
<td align="right">2,003,926,102</td>
<td align="right">1,938,389,898</td>
<td align="right">-3.3%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_NONE</td>
<td align="right">173,809,342</td>
<td align="right">168,133,004</td>
<td align="right">-3.3%</td>
</tr>
<tr>
<td align="left">_POP_TOP</td>
<td align="right">826,790,291</td>
<td align="right">800,242,580</td>
<td align="right">-3.2%</td>
</tr>
<tr>
<td align="left">_MAP_ADD</td>
<td align="right">21,327,010</td>
<td align="right">20,657,924</td>
<td align="right">-3.1%</td>
</tr>
<tr>
<td align="left">_REPLACE_WITH_TRUE</td>
<td align="right">32,649,902</td>
<td align="right">31,644,348</td>
<td align="right">-3.1%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_0</td>
<td align="right">208,515,623</td>
<td align="right">202,293,688</td>
<td align="right">-3.0%</td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_FAST_WITH_KEYWORDS</td>
<td align="right">90,623,382</td>
<td align="right">88,017,698</td>
<td align="right">-2.9%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">1,152,987,019</td>
<td align="right">1,120,575,672</td>
<td align="right">-2.8%</td>
</tr>
<tr>
<td align="left">_GUARD_BOTH_UNICODE</td>
<td align="right">975,198,962</td>
<td align="right">948,148,675</td>
<td align="right">-2.8%</td>
</tr>
<tr>
<td align="left">_LOAD_GLOBAL</td>
<td align="right">184,958,931</td>
<td align="right">180,126,292</td>
<td align="right">-2.6%</td>
</tr>
<tr>
<td align="left">_PUSH_FRAME</td>
<td align="right">1,826,760,147</td>
<td align="right">1,779,073,204</td>
<td align="right">-2.6%</td>
</tr>
<tr>
<td align="left">_GUARD_TOS_INT</td>
<td align="right">226,763,506</td>
<td align="right">220,930,143</td>
<td align="right">-2.6%</td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_O</td>
<td align="right">735,589,706</td>
<td align="right">716,765,993</td>
<td align="right">-2.6%</td>
</tr>
<tr>
<td align="left">_RETURN_GENERATOR</td>
<td align="right">91,043,080</td>
<td align="right">93,330,529</td>
<td align="right">2.5%</td>
</tr>
<tr>
<td align="left">_COMPARE_OP_INT</td>
<td align="right">966,178,590</td>
<td align="right">942,952,172</td>
<td align="right">-2.4%</td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_FAST</td>
<td align="right">1,025,914,657</td>
<td align="right">1,001,596,319</td>
<td align="right">-2.4%</td>
</tr>
<tr>
<td align="left">_GET_ITER</td>
<td align="right">293,199,548</td>
<td align="right">300,141,966</td>
<td align="right">2.4%</td>
</tr>
<tr>
<td align="left">_CHECK_PERIODIC</td>
<td align="right">2,580,395,675</td>
<td align="right">2,519,514,673</td>
<td align="right">-2.4%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_7</td>
<td align="right">1,220,389,995</td>
<td align="right">1,192,887,961</td>
<td align="right">-2.3%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right">91,557,181</td>
<td align="right">89,606,575</td>
<td align="right">-2.1%</td>
</tr>
<tr>
<td align="left">_BUILD_STRING</td>
<td align="right">25,514,804</td>
<td align="right">24,973,687</td>
<td align="right">-2.1%</td>
</tr>
<tr>
<td align="left">_CHECK_ATTR_MODULE</td>
<td align="right">7,589,611</td>
<td align="right">7,431,025</td>
<td align="right">-2.1%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_MODULE</td>
<td align="right">7,589,611</td>
<td align="right">7,431,025</td>
<td align="right">-2.1%</td>
</tr>
<tr>
<td align="left">_COMPARE_OP</td>
<td align="right">99,844,028</td>
<td align="right">97,759,999</td>
<td align="right">-2.1%</td>
</tr>
<tr>
<td align="left">_GUARD_BOTH_INT</td>
<td align="right">585,148,804</td>
<td align="right">573,135,917</td>
<td align="right">-2.1%</td>
</tr>
<tr>
<td align="left">_CHECK_VALIDITY_AND_SET_IP</td>
<td align="right">1,113,853,676</td>
<td align="right">1,091,414,776</td>
<td align="right">-2.0%</td>
</tr>
<tr>
<td align="left">_TO_BOOL</td>
<td align="right">241,406,053</td>
<td align="right">236,590,990</td>
<td align="right">-2.0%</td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">190,070,584</td>
<td align="right">186,455,508</td>
<td align="right">-1.9%</td>
</tr>
<tr>
<td align="left">_SWAP</td>
<td align="right">1,153,983,842</td>
<td align="right">1,175,099,711</td>
<td align="right">1.8%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_NONDESCRIPTOR_NO_DICT</td>
<td align="right">22,756,373</td>
<td align="right">22,358,930</td>
<td align="right">-1.7%</td>
</tr>
<tr>
<td align="left">_IS_OP</td>
<td align="right">369,211,901</td>
<td align="right">363,060,715</td>
<td align="right">-1.7%</td>
</tr>
<tr>
<td align="left">_BUILD_TUPLE</td>
<td align="right">456,226,595</td>
<td align="right">449,685,627</td>
<td align="right">-1.4%</td>
</tr>
<tr>
<td align="left">_COMPARE_OP_STR</td>
<td align="right">1,833,456,283</td>
<td align="right">1,808,011,044</td>
<td align="right">-1.4%</td>
</tr>
<tr>
<td align="left">_BINARY_OP</td>
<td align="right">878,003,957</td>
<td align="right">889,288,925</td>
<td align="right">1.3%</td>
</tr>
<tr>
<td align="left">_BINARY_SUBSCR_LIST_INT</td>
<td align="right">1,100,676,745</td>
<td align="right">1,087,325,337</td>
<td align="right">-1.2%</td>
</tr>
<tr>
<td align="left">_GUARD_NOT_EXHAUSTED_RANGE</td>
<td align="right">690,672,614</td>
<td align="right">682,395,249</td>
<td align="right">-1.2%</td>
</tr>
<tr>
<td align="left">_ITER_CHECK_RANGE</td>
<td align="right">691,209,934</td>
<td align="right">682,932,569</td>
<td align="right">-1.2%</td>
</tr>
<tr>
<td align="left">_CALL_TUPLE_1</td>
<td align="right">7,455,000</td>
<td align="right">7,365,780</td>
<td align="right">-1.2%</td>
</tr>
<tr>
<td align="left">_LOAD_CONST_INLINE_BORROW</td>
<td align="right">9,503,738,755</td>
<td align="right">9,391,127,955</td>
<td align="right">-1.2%</td>
</tr>
<tr>
<td align="left">_STORE_FAST</td>
<td align="right">3,393,235,938</td>
<td align="right">3,353,547,875</td>
<td align="right">-1.2%</td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_CLASS</td>
<td align="right">60,370,784</td>
<td align="right">59,667,198</td>
<td align="right">-1.2%</td>
</tr>
<tr>
<td align="left">_GET_YIELD_FROM_ITER</td>
<td align="right">197,864</td>
<td align="right">195,560</td>
<td align="right">-1.2%</td>
</tr>
<tr>
<td align="left">_ITER_NEXT_RANGE</td>
<td align="right">648,032,462</td>
<td align="right">640,694,661</td>
<td align="right">-1.1%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBTRACT_INT</td>
<td align="right">464,084,585</td>
<td align="right">458,866,815</td>
<td align="right">-1.1%</td>
</tr>
<tr>
<td align="left">_UNARY_NOT</td>
<td align="right">62,242,682</td>
<td align="right">61,556,200</td>
<td align="right">-1.1%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST</td>
<td align="right">6,054,313,987</td>
<td align="right">5,997,528,190</td>
<td align="right">-0.9%</td>
</tr>
<tr>
<td align="left">_STORE_ATTR_SLOT</td>
<td align="right">123,206,600</td>
<td align="right">122,058,758</td>
<td align="right">-0.9%</td>
</tr>
<tr>
<td align="left">_STORE_NAME</td>
<td align="right">545,860</td>
<td align="right">541,028</td>
<td align="right">-0.9%</td>
</tr>
<tr>
<td align="left">_LOAD_CONST_INLINE_BORROW_WITH_NULL</td>
<td align="right">504,369,545</td>
<td align="right">500,353,407</td>
<td align="right">-0.8%</td>
</tr>
<tr>
<td align="left">_CALL_TYPE_1</td>
<td align="right">332,470,967</td>
<td align="right">334,961,799</td>
<td align="right">0.7%</td>
</tr>
<tr>
<td align="left">_LOAD_DEREF</td>
<td align="right">660,425,034</td>
<td align="right">665,200,163</td>
<td align="right">0.7%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_7</td>
<td align="right">3,401,658,201</td>
<td align="right">3,378,746,172</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">_MAKE_FUNCTION</td>
<td align="right">93,513,184</td>
<td align="right">93,021,690</td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">_GUARD_NOS_INT</td>
<td align="right">2,429,476,878</td>
<td align="right">2,418,752,944</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">_SET_FUNCTION_ATTRIBUTE</td>
<td align="right">78,486,390</td>
<td align="right">78,190,262</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">_BINARY_SUBSCR_STR_INT</td>
<td align="right">1,216,189,037</td>
<td align="right">1,211,950,186</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">_STORE_SUBSCR_LIST_INT</td>
<td align="right">490,249,262</td>
<td align="right">488,619,558</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">_UNPACK_SEQUENCE_LIST</td>
<td align="right">80,800,669</td>
<td align="right">80,570,420</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">_GUARD_BUILTINS_VERSION</td>
<td align="right">45,826,492</td>
<td align="right">45,700,720</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">_CONTAINS_OP_SET</td>
<td align="right">1,600,210,780</td>
<td align="right">1,596,109,826</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">_LOAD_GLOBAL_BUILTINS</td>
<td align="right">52,375,532</td>
<td align="right">52,249,760</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_ADD_INT</td>
<td align="right">2,523,624,526</td>
<td align="right">2,518,480,983</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">_BINARY_SUBSCR</td>
<td align="right">1,301,348,424</td>
<td align="right">1,299,302,492</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">_STORE_SUBSCR</td>
<td align="right">381,419,975</td>
<td align="right">380,933,447</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_3</td>
<td align="right">61,056,756</td>
<td align="right">61,130,769</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">_COPY</td>
<td align="right">1,325,547,540</td>
<td align="right">1,326,726,714</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_4</td>
<td align="right">624,688,695</td>
<td align="right">624,360,592</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">_BUILD_CONST_KEY_MAP</td>
<td align="right">2,484,290</td>
<td align="right">2,483,360</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">_COMPARE_OP_FLOAT</td>
<td align="right">101,252,026</td>
<td align="right">101,280,861</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_UNARY_NEGATIVE</td>
<td align="right">25,147,714</td>
<td align="right">25,142,379</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">_BUILD_SLICE</td>
<td align="right">139,781,460</td>
<td align="right">139,757,225</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">_GUARD_BOTH_FLOAT</td>
<td align="right">916,377,398</td>
<td align="right">916,510,940</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_LIST_EXTEND</td>
<td align="right">98,358,428</td>
<td align="right">98,344,613</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_CHECK</td>
<td align="right">251,942</td>
<td align="right">251,920</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_MULTIPLY_FLOAT</td>
<td align="right">1,156,304,420</td>
<td align="right">1,156,404,380</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBTRACT_FLOAT</td>
<td align="right">383,046,880</td>
<td align="right">383,075,426</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_CALL_INTRINSIC_1</td>
<td align="right">97,434,628</td>
<td align="right">97,427,533</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_MULTIPLY_INT</td>
<td align="right">185,788,044</td>
<td align="right">185,790,966</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_GET_AWAITABLE</td>
<td align="right">653,799</td>
<td align="right">653,791</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_ADD_FLOAT</td>
<td align="right">554,586,180</td>
<td align="right">554,588,340</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_CHECK_ATTR_METHOD_LAZY_DICT</td>
<td align="right">104,226,630</td>
<td align="right">104,226,343</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_METHOD_LAZY_DICT</td>
<td align="right">104,226,630</td>
<td align="right">104,226,343</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">_GUARD_NOS_FLOAT</td>
<td align="right">613,658,850</td>
<td align="right">613,658,455</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">_STORE_SLICE</td>
<td align="right">149,868,340</td>
<td align="right">149,868,340</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_GET_ANEXT</td>
<td align="right">125,514,720</td>
<td align="right">125,514,720</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_GUARD_TOS_FLOAT</td>
<td align="right">65,543,560</td>
<td align="right">65,543,560</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_SLOT_1</td>
<td align="right">2,396,080</td>
<td align="right">2,396,080</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_UNPACK_EX</td>
<td align="right">104</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_PY_GENERAL</td>
<td align="right"></td>
<td align="right">99,489,848</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_IS_FUNCTION</td>
<td align="right"></td>
<td align="right">94,460,848</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_NON_PY_GENERAL</td>
<td align="right"></td>
<td align="right">37,542,131</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_IS_NOT_PY_CALLABLE</td>
<td align="right"></td>
<td align="right">37,542,131</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_IS_METHOD</td>
<td align="right"></td>
<td align="right">5,029,034</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_EXPAND_METHOD</td>
<td align="right"></td>
<td align="right">5,029,000</td>
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
<td align="left">BEFORE_WITH</td>
<td align="right">240</td>
<td align="right">480</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">173,044</td>
<td align="right">73,875</td>
<td align="right">-57.3%</td>
</tr>
<tr>
<td align="left">CALL_ALLOC_AND_ENTER_INIT</td>
<td align="right">1,911</td>
<td align="right">887</td>
<td align="right">-53.6%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_WITH_HINT</td>
<td align="right">240</td>
<td align="right">360</td>
<td align="right">50.0%</td>
</tr>
<tr>
<td align="left">CALL_FUNCTION_EX</td>
<td align="right">6,000</td>
<td align="right">3,164</td>
<td align="right">-47.3%</td>
</tr>
<tr>
<td align="left">CALL_LIST_APPEND</td>
<td align="right">7,668</td>
<td align="right">4,293</td>
<td align="right">-44.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_INPLACE_ADD_UNICODE</td>
<td align="right">703</td>
<td align="right">423</td>
<td align="right">-39.8%</td>
</tr>
<tr>
<td align="left">BUILD_SET</td>
<td align="right">525</td>
<td align="right">340</td>
<td align="right">-35.2%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_GETITEM</td>
<td align="right">3,240</td>
<td align="right">2,129</td>
<td align="right">-34.3%</td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">44,367</td>
<td align="right">58,578</td>
<td align="right">32.0%</td>
</tr>
<tr>
<td align="left">FOR_ITER_GEN</td>
<td align="right">48,123</td>
<td align="right">33,056</td>
<td align="right">-31.3%</td>
</tr>
<tr>
<td align="left">CALL_KW</td>
<td align="right">29,556</td>
<td align="right">21,715</td>
<td align="right">-26.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_PROPERTY</td>
<td align="right">8,068</td>
<td align="right">6,055</td>
<td align="right">-25.0%</td>
</tr>
<tr>
<td align="left">SEND_GEN</td>
<td align="right">260</td>
<td align="right">220</td>
<td align="right">-15.4%</td>
</tr>
<tr>
<td align="left">LOAD_NAME</td>
<td align="right">1,360</td>
<td align="right">1,282</td>
<td align="right">-5.7%</td>
</tr>
<tr>
<td align="left">YIELD_VALUE</td>
<td align="right">140,969</td>
<td align="right">134,846</td>
<td align="right">-4.3%</td>
</tr>
<tr>
<td align="left">IMPORT_NAME</td>
<td align="right">409</td>
<td align="right">420</td>
<td align="right">2.7%</td>
</tr>
<tr>
<td align="left">SEND</td>
<td align="right">31,713</td>
<td align="right">31,700</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">CALL_PY_WITH_DEFAULTS</td>
<td align="right">11,562</td>
<td align="right"></td>
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
<td align="right">0</td>
<td align="right">-100.0%</td>
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
<td align="right">161</td>
<td align="right">-65.1%</td>
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
<td align="right">761</td>
<td align="right">-32.1%</td>
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
<td align="right">761</td>
<td align="right">-32.1%</td>
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
<td align="right">2,000</td>
<td align="right">1,941</td>
<td align="right">-2.9%</td>
</tr>
</tbody>
</table>


</details>

---
Stats gathered on: 2024-04-27
