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
<td align="right">356,339,758</td>
<td align="right">10,736,255</td>
<td align="right">-97.0%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">670,609,075</td>
<td align="right">22,276,279</td>
<td align="right">-96.7%</td>
</tr>
<tr>
<td align="left">SET_ADD</td>
<td align="right">957,631</td>
<td align="right">219,616</td>
<td align="right">-77.1%</td>
</tr>
<tr>
<td align="left">FOR_ITER_RANGE</td>
<td align="right">107,659,358</td>
<td align="right">29,617,133</td>
<td align="right">-72.5%</td>
</tr>
<tr>
<td align="left">STORE_FAST_LOAD_FAST</td>
<td align="right">43,099,146</td>
<td align="right">15,442,903</td>
<td align="right">-64.2%</td>
</tr>
<tr>
<td align="left">CALL_TYPE_1</td>
<td align="right">294,458,159</td>
<td align="right">149,555,317</td>
<td align="right">-49.2%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST</td>
<td align="right">598,562,352</td>
<td align="right">307,169,584</td>
<td align="right">-48.7%</td>
</tr>
<tr>
<td align="left">BINARY_OP_MULTIPLY_FLOAT</td>
<td align="right">137,016,612</td>
<td align="right">74,261,589</td>
<td align="right">-45.8%</td>
</tr>
<tr>
<td align="left">BINARY_OP_INPLACE_ADD_UNICODE</td>
<td align="right">6,409,655</td>
<td align="right">3,591,975</td>
<td align="right">-44.0%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">121,651,852</td>
<td align="right">72,958,290</td>
<td align="right">-40.0%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP_DICT</td>
<td align="right">176,723,468</td>
<td align="right">110,862,613</td>
<td align="right">-37.3%</td>
</tr>
<tr>
<td align="left">BUILD_CONST_KEY_MAP</td>
<td align="right">13,477,463</td>
<td align="right">8,595,861</td>
<td align="right">-36.2%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP_SET</td>
<td align="right">520,627,375</td>
<td align="right">348,448,046</td>
<td align="right">-33.1%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TUPLE</td>
<td align="right">341,488,819</td>
<td align="right">244,604,313</td>
<td align="right">-28.4%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">346,870,320</td>
<td align="right">259,666,560</td>
<td align="right">-25.1%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_FLOAT</td>
<td align="right">58,491,765</td>
<td align="right">43,797,915</td>
<td align="right">-25.1%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">3,168,074,754</td>
<td align="right">2,437,114,380</td>
<td align="right">-23.1%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR</td>
<td align="right">422,466,664</td>
<td align="right">330,675,557</td>
<td align="right">-21.7%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_DICT</td>
<td align="right">576,200,426</td>
<td align="right">457,970,229</td>
<td align="right">-20.5%</td>
</tr>
<tr>
<td align="left">UNARY_INVERT</td>
<td align="right">2,683,304</td>
<td align="right">2,186,617</td>
<td align="right">-18.5%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">6,879,784,097</td>
<td align="right">5,672,411,027</td>
<td align="right">-17.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">1,821,929,696</td>
<td align="right">1,510,232,029</td>
<td align="right">-17.1%</td>
</tr>
<tr>
<td align="left">IS_OP</td>
<td align="right">499,886,670</td>
<td align="right">418,437,884</td>
<td align="right">-16.3%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE</td>
<td align="right">558,173</td>
<td align="right">476,911</td>
<td align="right">-14.6%</td>
</tr>
<tr>
<td align="left">LOAD_NAME</td>
<td align="right">14,134,687</td>
<td align="right">12,134,367</td>
<td align="right">-14.2%</td>
</tr>
<tr>
<td align="left">FOR_ITER_GEN</td>
<td align="right">239,979,994</td>
<td align="right">206,980,872</td>
<td align="right">-13.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">5,590,350,435</td>
<td align="right">4,865,258,828</td>
<td align="right">-13.0%</td>
</tr>
<tr>
<td align="left">LIST_APPEND</td>
<td align="right">75,575,522</td>
<td align="right">66,002,335</td>
<td align="right">-12.7%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_TUPLE_INT</td>
<td align="right">220,466,943</td>
<td align="right">193,556,119</td>
<td align="right">-12.2%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">742,533,884</td>
<td align="right">655,316,869</td>
<td align="right">-11.7%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">146,251,424</td>
<td align="right">129,131,124</td>
<td align="right">-11.7%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_O</td>
<td align="right">681,334,573</td>
<td align="right">602,277,297</td>
<td align="right">-11.6%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">3,206,720,107</td>
<td align="right">2,840,023,329</td>
<td align="right">-11.4%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">2,964,956,545</td>
<td align="right">2,634,854,849</td>
<td align="right">-11.1%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_LIST_INT</td>
<td align="right">111,076,389</td>
<td align="right">99,707,325</td>
<td align="right">-10.2%</td>
</tr>
<tr>
<td align="left">CALL_ISINSTANCE</td>
<td align="right">853,187,157</td>
<td align="right">769,147,484</td>
<td align="right">-9.9%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">1,534,297,673</td>
<td align="right">1,383,638,310</td>
<td align="right">-9.8%</td>
</tr>
<tr>
<td align="left">DICT_MERGE</td>
<td align="right">47,714,220</td>
<td align="right">43,047,689</td>
<td align="right">-9.8%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_LIST_INT</td>
<td align="right">433,384,441</td>
<td align="right">392,349,471</td>
<td align="right">-9.5%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">5,596,484,762</td>
<td align="right">5,082,568,609</td>
<td align="right">-9.2%</td>
</tr>
<tr>
<td align="left">CALL_STR_1</td>
<td align="right">48,531,779</td>
<td align="right">44,082,561</td>
<td align="right">-9.2%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">3,640,621,853</td>
<td align="right">3,311,326,688</td>
<td align="right">-9.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">25,257,171,181</td>
<td align="right">23,042,733,508</td>
<td align="right">-8.8%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">643,808,001</td>
<td align="right">588,886,248</td>
<td align="right">-8.5%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">6,336,222,829</td>
<td align="right">5,799,036,642</td>
<td align="right">-8.5%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">117,153,675</td>
<td align="right">107,818,556</td>
<td align="right">-8.0%</td>
</tr>
<tr>
<td align="left">PUSH_NULL</td>
<td align="right">1,256,324,622</td>
<td align="right">1,158,516,242</td>
<td align="right">-7.8%</td>
</tr>
<tr>
<td align="left">BUILD_MAP</td>
<td align="right">133,968,145</td>
<td align="right">124,296,407</td>
<td align="right">-7.2%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">142,713,050</td>
<td align="right">134,061,637</td>
<td align="right">-6.1%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">257,454,377</td>
<td align="right">242,878,122</td>
<td align="right">-5.7%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_GETITEM</td>
<td align="right">64,884,021</td>
<td align="right">61,316,192</td>
<td align="right">-5.5%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_INT</td>
<td align="right">402,290,561</td>
<td align="right">380,814,905</td>
<td align="right">-5.3%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">472,844,119</td>
<td align="right">448,161,938</td>
<td align="right">-5.2%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">130,757,955</td>
<td align="right">123,935,178</td>
<td align="right">-5.2%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_INT</td>
<td align="right">677,480,582</td>
<td align="right">642,452,014</td>
<td align="right">-5.2%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">7,034,367,347</td>
<td align="right">6,681,606,452</td>
<td align="right">-5.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right">151,197,548</td>
<td align="right">143,642,349</td>
<td align="right">-5.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL_STR</td>
<td align="right">79,053,279</td>
<td align="right">75,175,787</td>
<td align="right">-4.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">1,047,201,098</td>
<td align="right">996,442,978</td>
<td align="right">-4.8%</td>
</tr>
<tr>
<td align="left">BUILD_LIST</td>
<td align="right">230,823,562</td>
<td align="right">219,690,582</td>
<td align="right">-4.8%</td>
</tr>
<tr>
<td align="left">LIST_EXTEND</td>
<td align="right">30,919,861</td>
<td align="right">29,535,182</td>
<td align="right">-4.5%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">568,244,022</td>
<td align="right">543,494,300</td>
<td align="right">-4.4%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">613,455,282</td>
<td align="right">587,334,260</td>
<td align="right">-4.3%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">4,364,499,573</td>
<td align="right">4,186,589,588</td>
<td align="right">-4.1%</td>
</tr>
<tr>
<td align="left">CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">194,390,206</td>
<td align="right">186,910,026</td>
<td align="right">-3.8%</td>
</tr>
<tr>
<td align="left">STORE_FAST_STORE_FAST</td>
<td align="right">1,753,734,099</td>
<td align="right">1,687,148,420</td>
<td align="right">-3.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_WITH_HINT</td>
<td align="right">380,939,744</td>
<td align="right">366,738,534</td>
<td align="right">-3.7%</td>
</tr>
<tr>
<td align="left">TO_BOOL_LIST</td>
<td align="right">122,502,784</td>
<td align="right">117,942,210</td>
<td align="right">-3.7%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST_WITH_KEYWORDS</td>
<td align="right">110,465,089</td>
<td align="right">106,455,023</td>
<td align="right">-3.6%</td>
</tr>
<tr>
<td align="left">TO_BOOL_INT</td>
<td align="right">146,634,475</td>
<td align="right">141,967,112</td>
<td align="right">-3.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_NO_DICT</td>
<td align="right">68,441,496</td>
<td align="right">66,390,972</td>
<td align="right">-3.0%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">663,248,969</td>
<td align="right">644,639,998</td>
<td align="right">-2.8%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_STR</td>
<td align="right">334,143,116</td>
<td align="right">324,911,621</td>
<td align="right">-2.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">1,363,220,342</td>
<td align="right">1,325,670,608</td>
<td align="right">-2.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_MODULE</td>
<td align="right">548,190,421</td>
<td align="right">534,042,804</td>
<td align="right">-2.6%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">267,512,235</td>
<td align="right">261,104,910</td>
<td align="right">-2.4%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NONE</td>
<td align="right">400,321,961</td>
<td align="right">390,894,910</td>
<td align="right">-2.4%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">3,674,315,030</td>
<td align="right">3,589,439,384</td>
<td align="right">-2.3%</td>
</tr>
<tr>
<td align="left">NOP</td>
<td align="right">1,022,796,234</td>
<td align="right">1,000,581,765</td>
<td align="right">-2.2%</td>
</tr>
<tr>
<td align="left">CONVERT_VALUE</td>
<td align="right">138,885,424</td>
<td align="right">135,964,714</td>
<td align="right">-2.1%</td>
</tr>
<tr>
<td align="left">FORMAT_SIMPLE</td>
<td align="right">149,231,113</td>
<td align="right">146,264,518</td>
<td align="right">-2.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL_ALWAYS_TRUE</td>
<td align="right">185,358,738</td>
<td align="right">181,890,123</td>
<td align="right">-1.9%</td>
</tr>
<tr>
<td align="left">MAP_ADD</td>
<td align="right">39,918,894</td>
<td align="right">39,192,093</td>
<td align="right">-1.8%</td>
</tr>
<tr>
<td align="left">CALL_LEN</td>
<td align="right">307,502,040</td>
<td align="right">301,986,039</td>
<td align="right">-1.8%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT</td>
<td align="right">1,235,709,660</td>
<td align="right">1,213,688,403</td>
<td align="right">-1.8%</td>
</tr>
<tr>
<td align="left">YIELD_VALUE</td>
<td align="right">1,409,023,371</td>
<td align="right">1,384,358,184</td>
<td align="right">-1.8%</td>
</tr>
<tr>
<td align="left">MAKE_FUNCTION</td>
<td align="right">98,752,283</td>
<td align="right">97,025,319</td>
<td align="right">-1.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">4,048,450,219</td>
<td align="right">3,979,458,438</td>
<td align="right">-1.7%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_UNICODE</td>
<td align="right">76,126,969</td>
<td align="right">74,878,339</td>
<td align="right">-1.6%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_DICT</td>
<td align="right">152,591,955</td>
<td align="right">150,161,718</td>
<td align="right">-1.6%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">1,745,415,596</td>
<td align="right">1,718,869,935</td>
<td align="right">-1.5%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST_WITH_KEYWORDS</td>
<td align="right">44,498,227</td>
<td align="right">43,848,371</td>
<td align="right">-1.5%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">324,190,427</td>
<td align="right">319,625,095</td>
<td align="right">-1.4%</td>
</tr>
<tr>
<td align="left">BUILD_STRING</td>
<td align="right">75,887,428</td>
<td align="right">74,964,642</td>
<td align="right">-1.2%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_LIST</td>
<td align="right">273,423,963</td>
<td align="right">270,185,075</td>
<td align="right">-1.2%</td>
</tr>
<tr>
<td align="left">MAKE_CELL</td>
<td align="right">104,951,662</td>
<td align="right">103,806,944</td>
<td align="right">-1.1%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR</td>
<td align="right">134,296,929</td>
<td align="right">132,860,834</td>
<td align="right">-1.1%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NOT_NONE</td>
<td align="right">672,298,548</td>
<td align="right">665,123,584</td>
<td align="right">-1.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_AND_CLEAR</td>
<td align="right">70,684,178</td>
<td align="right">69,944,864</td>
<td align="right">-1.0%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_CLASS</td>
<td align="right">158,193,319</td>
<td align="right">156,586,640</td>
<td align="right">-1.0%</td>
</tr>
<tr>
<td align="left">STORE_DEREF</td>
<td align="right">95,280,668</td>
<td align="right">94,353,507</td>
<td align="right">-1.0%</td>
</tr>
<tr>
<td align="left">CALL_INTRINSIC_1</td>
<td align="right">156,188,037</td>
<td align="right">154,794,680</td>
<td align="right">-0.9%</td>
</tr>
<tr>
<td align="left">BINARY_SLICE</td>
<td align="right">228,762,892</td>
<td align="right">226,774,991</td>
<td align="right">-0.9%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">2,879,529,572</td>
<td align="right">2,904,002,476</td>
<td align="right">0.8%</td>
</tr>
<tr>
<td align="left">CALL_PY_WITH_DEFAULTS</td>
<td align="right">221,360,210</td>
<td align="right">219,620,910</td>
<td align="right">-0.8%</td>
</tr>
<tr>
<td align="left">UNARY_NOT</td>
<td align="right">28,458,239</td>
<td align="right">28,239,631</td>
<td align="right">-0.8%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_FLOAT</td>
<td align="right">59,479,611</td>
<td align="right">59,045,083</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">DICT_UPDATE</td>
<td align="right">73,043</td>
<td align="right">73,574</td>
<td align="right">0.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_PROPERTY</td>
<td align="right">81,419,668</td>
<td align="right">80,864,968</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">TO_BOOL_NONE</td>
<td align="right">508,752,496</td>
<td align="right">505,319,122</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_CHECK</td>
<td align="right">11,845,190</td>
<td align="right">11,771,195</td>
<td align="right">-0.6%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_O</td>
<td align="right">402,130,760</td>
<td align="right">399,737,679</td>
<td align="right">-0.6%</td>
</tr>
<tr>
<td align="left">END_FOR</td>
<td align="right">82,992,174</td>
<td align="right">82,502,317</td>
<td align="right">-0.6%</td>
</tr>
<tr>
<td align="left">BINARY_OP_MULTIPLY_INT</td>
<td align="right">161,281,756</td>
<td align="right">160,439,935</td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">INTERPRETER_EXIT</td>
<td align="right">2,320,475,714</td>
<td align="right">2,331,956,748</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">1,263,977,823</td>
<td align="right">1,259,012,117</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">COPY_FREE_VARS</td>
<td align="right">323,834,215</td>
<td align="right">322,573,495</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_CLASS</td>
<td align="right">166,253,857</td>
<td align="right">166,877,320</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">CALL_KW</td>
<td align="right">276,607,386</td>
<td align="right">275,655,547</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">SET_FUNCTION_ATTRIBUTE</td>
<td align="right">85,255,409</td>
<td align="right">84,988,262</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">JUMP_FORWARD</td>
<td align="right">451,530,010</td>
<td align="right">450,291,230</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">STORE_GLOBAL</td>
<td align="right">6,944,680</td>
<td align="right">6,928,920</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">DELETE_FAST</td>
<td align="right">2,236,682</td>
<td align="right">2,240,312</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">DELETE_SUBSCR</td>
<td align="right">176,500,199</td>
<td align="right">176,278,419</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">2,066,622,518</td>
<td align="right">2,064,395,426</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">73,173,074</td>
<td align="right">73,100,663</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">INSTRUMENTED_JUMP_BACKWARD</td>
<td align="right">9,996</td>
<td align="right">9,988</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">BEFORE_WITH</td>
<td align="right">10,165,107</td>
<td align="right">10,172,419</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">INSTRUMENTED_FOR_ITER</td>
<td align="right">11,356</td>
<td align="right">11,348</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">INSTRUMENTED_POP_JUMP_IF_TRUE</td>
<td align="right">13,436</td>
<td align="right">13,428</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">1,150,673,515</td>
<td align="right">1,150,112,347</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">UNARY_NEGATIVE</td>
<td align="right">122,296,158</td>
<td align="right">122,236,552</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_STR_INT</td>
<td align="right">466,436,477</td>
<td align="right">466,278,469</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_SLOT</td>
<td align="right">1,503,854,500</td>
<td align="right">1,504,289,362</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_FUNCTION_EX</td>
<td align="right">202,468,282</td>
<td align="right">202,409,964</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR_METHOD</td>
<td align="right">127,396,960</td>
<td align="right">127,426,298</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_NAME</td>
<td align="right">610,362</td>
<td align="right">610,242</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">CHECK_EXC_MATCH</td>
<td align="right">24,585,653</td>
<td align="right">24,590,143</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">PUSH_EXC_INFO</td>
<td align="right">25,073,668</td>
<td align="right">25,078,195</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">POP_EXCEPT</td>
<td align="right">25,073,521</td>
<td align="right">25,078,047</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">RETURN_GENERATOR</td>
<td align="right">506,021,131</td>
<td align="right">505,953,931</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR</td>
<td align="right">23,843</td>
<td align="right">23,846</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">343,725</td>
<td align="right">343,756</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">IMPORT_FROM</td>
<td align="right">13,159,134</td>
<td align="right">13,158,147</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">IMPORT_NAME</td>
<td align="right">12,487,693</td>
<td align="right">12,486,953</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">BUILD_SET</td>
<td align="right">2,388,927</td>
<td align="right">2,388,805</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_FLOAT</td>
<td align="right">181,060,215</td>
<td align="right">181,069,164</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CLEANUP_THROW</td>
<td align="right">160,103</td>
<td align="right">160,097</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_LAZY_DICT</td>
<td align="right">36,683,308</td>
<td align="right">36,682,300</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">RAISE_VARARGS</td>
<td align="right">6,196,606</td>
<td align="right">6,196,764</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_SLICE</td>
<td align="right">12,595,334</td>
<td align="right">12,595,549</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">GET_AWAITABLE</td>
<td align="right">229,793,613</td>
<td align="right">229,797,419</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_LIST_APPEND</td>
<td align="right">349,482,734</td>
<td align="right">349,487,116</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">20,803,810</td>
<td align="right">20,804,038</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_TUPLE_1</td>
<td align="right">28,291,393</td>
<td align="right">28,291,115</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">DELETE_ATTR</td>
<td align="right">6,775,778</td>
<td align="right">6,775,844</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">END_SEND</td>
<td align="right">402,761,286</td>
<td align="right">402,765,095</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">SEND</td>
<td align="right">173,952,571</td>
<td align="right">173,954,154</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BUILD_SLICE</td>
<td align="right">72,060,282</td>
<td align="right">72,060,879</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD_NO_INTERRUPT</td>
<td align="right">556,726,439</td>
<td align="right">556,730,594</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">SEND_GEN</td>
<td align="right">787,183,622</td>
<td align="right">787,188,175</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">WITH_EXCEPT_START</td>
<td align="right">235,322</td>
<td align="right">235,323</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">GET_YIELD_FROM_ITER</td>
<td align="right">47,471,383</td>
<td align="right">47,471,287</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">BEFORE_ASYNC_WITH</td>
<td align="right">3,005,926</td>
<td align="right">3,005,920</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_WITH_HINT</td>
<td align="right">64,671,276</td>
<td align="right">64,671,405</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR_ATTR</td>
<td align="right">7,773,584</td>
<td align="right">7,773,570</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">RERAISE</td>
<td align="right">3,993,465</td>
<td align="right">3,993,461</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">EXIT_INIT_CHECK</td>
<td align="right">95,010,778</td>
<td align="right">95,010,772</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">CALL_ALLOC_AND_ENTER_INIT</td>
<td align="right">97,298,660</td>
<td align="right">97,298,654</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">INSTRUMENTED_POP_JUMP_IF_FALSE</td>
<td align="right">38,888,640</td>
<td align="right">38,888,640</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">INSTRUMENTED_RESUME</td>
<td align="right">38,866,420</td>
<td align="right">38,866,420</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">INSTRUMENTED_RETURN_VALUE</td>
<td align="right">38,857,520</td>
<td align="right">38,857,520</td>
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
<td align="left">SET_UPDATE</td>
<td align="right">200,448</td>
<td align="right">200,448</td>
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
<td align="right">28,786</td>
<td align="right">28,786</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">INSTRUMENTED_RETURN_CONST</td>
<td align="right">7,200</td>
<td align="right">7,200</td>
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
<td align="left">FORMAT_WITH_SPEC</td>
<td align="right">1,080</td>
<td align="right">1,080</td>
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
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">633,642,282</td>
<td align="right">8.4%</td>
<td align="right">607,534,730</td>
<td align="right">8.1%</td>
<td align="right">-4.1%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">6,864,373,652</td>
<td align="right">91.5%</td>
<td align="right">6,862,013,586</td>
<td align="right">91.8%</td>
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
<td align="right">21,800,813</td>
<td align="right">0.3%</td>
<td align="right">21,800,781</td>
<td align="right">0.3%</td>
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
<td align="right">1,149,136</td>
<td align="right">71.2%</td>
<td align="right">1,135,589</td>
<td align="right">71.0%</td>
<td align="right">-1.2%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">464,677</td>
<td align="right">28.8%</td>
<td align="right">464,722</td>
<td align="right">29.0%</td>
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
<td align="left">and int</td>
<td align="right">40,765</td>
<td align="right">3.5%</td>
<td align="right">35,637</td>
<td align="right">3.1%</td>
<td align="right">-12.6%</td>
</tr>
<tr>
<td align="left">xor</td>
<td align="right">9,863</td>
<td align="right">0.9%</td>
<td align="right">8,644</td>
<td align="right">0.8%</td>
<td align="right">-12.4%</td>
</tr>
<tr>
<td align="left">rshift</td>
<td align="right">9,826</td>
<td align="right">0.9%</td>
<td align="right">8,633</td>
<td align="right">0.8%</td>
<td align="right">-12.1%</td>
</tr>
<tr>
<td align="left">true divide different types</td>
<td align="right">11,822</td>
<td align="right">1.0%</td>
<td align="right">11,034</td>
<td align="right">1.0%</td>
<td align="right">-6.7%</td>
</tr>
<tr>
<td align="left">or</td>
<td align="right">17,521</td>
<td align="right">1.5%</td>
<td align="right">16,725</td>
<td align="right">1.5%</td>
<td align="right">-4.5%</td>
</tr>
<tr>
<td align="left">true divide other</td>
<td align="right">3,401</td>
<td align="right">0.3%</td>
<td align="right">3,521</td>
<td align="right">0.3%</td>
<td align="right">3.5%</td>
</tr>
<tr>
<td align="left">lshift</td>
<td align="right">5,645</td>
<td align="right">0.5%</td>
<td align="right">5,488</td>
<td align="right">0.5%</td>
<td align="right">-2.8%</td>
</tr>
<tr>
<td align="left">add different types</td>
<td align="right">63,405</td>
<td align="right">5.5%</td>
<td align="right">61,984</td>
<td align="right">5.5%</td>
<td align="right">-2.2%</td>
</tr>
<tr>
<td align="left">subtract other</td>
<td align="right">12,174</td>
<td align="right">1.1%</td>
<td align="right">11,954</td>
<td align="right">1.1%</td>
<td align="right">-1.8%</td>
</tr>
<tr>
<td align="left">true divide float</td>
<td align="right">5,763</td>
<td align="right">0.5%</td>
<td align="right">5,664</td>
<td align="right">0.5%</td>
<td align="right">-1.7%</td>
</tr>
<tr>
<td align="left">remainder</td>
<td align="right">53,154</td>
<td align="right">4.6%</td>
<td align="right">52,254</td>
<td align="right">4.6%</td>
<td align="right">-1.7%</td>
</tr>
<tr>
<td align="left">add other</td>
<td align="right">65,602</td>
<td align="right">5.7%</td>
<td align="right">65,145</td>
<td align="right">5.7%</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">floor divide</td>
<td align="right">32,512</td>
<td align="right">2.8%</td>
<td align="right">32,316</td>
<td align="right">2.8%</td>
<td align="right">-0.6%</td>
</tr>
<tr>
<td align="left">multiply different types</td>
<td align="right">67,673</td>
<td align="right">5.9%</td>
<td align="right">67,378</td>
<td align="right">5.9%</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">power</td>
<td align="right">5,721</td>
<td align="right">0.5%</td>
<td align="right">5,728</td>
<td align="right">0.5%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">subtract different types</td>
<td align="right">736,434</td>
<td align="right">64.1%</td>
<td align="right">735,631</td>
<td align="right">64.8%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">and other</td>
<td align="right">2,036</td>
<td align="right">0.2%</td>
<td align="right">2,034</td>
<td align="right">0.2%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">multiply other</td>
<td align="right">5,200</td>
<td align="right">0.5%</td>
<td align="right">5,200</td>
<td align="right">0.5%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">and different types</td>
<td align="right">619</td>
<td align="right">0.1%</td>
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
<td align="right">426,978,523</td>
<td align="right">8.7%</td>
<td align="right">335,212,593</td>
<td align="right">7.0%</td>
<td align="right">-21.5%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">4,459,765,808</td>
<td align="right">91.3%</td>
<td align="right">4,445,216,056</td>
<td align="right">93.0%</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">4,898,707</td>
<td align="right">0.1%</td>
<td align="right">4,898,237</td>
<td align="right">0.1%</td>
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
<td align="right">184,811</td>
<td align="right">47.8%</td>
<td align="right">159,176</td>
<td align="right">44.1%</td>
<td align="right">-13.9%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">202,037</td>
<td align="right">52.2%</td>
<td align="right">202,025</td>
<td align="right">55.9%</td>
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
<td align="right">56,777</td>
<td align="right">30.7%</td>
<td align="right">40,371</td>
<td align="right">25.4%</td>
<td align="right">-28.9%</td>
</tr>
<tr>
<td align="left">out of range</td>
<td align="right">77,454</td>
<td align="right">41.9%</td>
<td align="right">69,944</td>
<td align="right">43.9%</td>
<td align="right">-9.7%</td>
</tr>
<tr>
<td align="left">array int</td>
<td align="right">16,680</td>
<td align="right">9.0%</td>
<td align="right">15,640</td>
<td align="right">9.8%</td>
<td align="right">-6.2%</td>
</tr>
<tr>
<td align="left">buffer int</td>
<td align="right">22,583</td>
<td align="right">12.2%</td>
<td align="right">21,921</td>
<td align="right">13.8%</td>
<td align="right">-2.9%</td>
</tr>
<tr>
<td align="left">tuple slice</td>
<td align="right">183</td>
<td align="right">0.1%</td>
<td align="right">185</td>
<td align="right">0.1%</td>
<td align="right">1.1%</td>
</tr>
<tr>
<td align="left">code complex parameters</td>
<td align="right">5,034</td>
<td align="right">2.7%</td>
<td align="right">5,015</td>
<td align="right">3.2%</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">sequence int</td>
<td align="right">4,300</td>
<td align="right">2.3%</td>
<td align="right">4,300</td>
<td align="right">2.7%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">buffer slice</td>
<td align="right">980</td>
<td align="right">0.5%</td>
<td align="right">980</td>
<td align="right">0.6%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">list slice</td>
<td align="right">720</td>
<td align="right">0.4%</td>
<td align="right">720</td>
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
deopt
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">31,200</td>
<td align="right">0.0%</td>
<td align="right">23,440</td>
<td align="right">0.0%</td>
<td align="right">-24.9%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">1,513,892,655</td>
<td align="right">11.1%</td>
<td align="right">1,508,086,889</td>
<td align="right">11.0%</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">256,401,690</td>
<td align="right">1.9%</td>
<td align="right">255,544,179</td>
<td align="right">1.9%</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">12,175,429,738</td>
<td align="right">88.9%</td>
<td align="right">12,152,219,142</td>
<td align="right">88.9%</td>
<td align="right">-0.2%</td>
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
<td align="right">5,462,215</td>
<td align="right">84.2%</td>
<td align="right">5,445,952</td>
<td align="right">84.2%</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">1,024,643</td>
<td align="right">15.8%</td>
<td align="right">1,023,455</td>
<td align="right">15.8%</td>
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
<td align="left">cmethod</td>
<td align="right">14,100</td>
<td align="right">1.4%</td>
<td align="right">13,620</td>
<td align="right">1.3%</td>
<td align="right">-3.4%</td>
</tr>
<tr>
<td align="left">class mutable</td>
<td align="right">25,311</td>
<td align="right">2.5%</td>
<td align="right">24,816</td>
<td align="right">2.4%</td>
<td align="right">-2.0%</td>
</tr>
<tr>
<td align="left">method wrapper</td>
<td align="right">8,236</td>
<td align="right">0.8%</td>
<td align="right">8,197</td>
<td align="right">0.8%</td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">cfunc noargs</td>
<td align="right">70,318</td>
<td align="right">6.9%</td>
<td align="right">70,054</td>
<td align="right">6.8%</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">metaclass</td>
<td align="right">43,084</td>
<td align="right">4.2%</td>
<td align="right">43,241</td>
<td align="right">4.2%</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">wrong number arguments</td>
<td align="right">14,014</td>
<td align="right">1.4%</td>
<td align="right">13,994</td>
<td align="right">1.4%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">init not python</td>
<td align="right">16,426</td>
<td align="right">1.6%</td>
<td align="right">16,406</td>
<td align="right">1.6%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">bound method</td>
<td align="right">11,893</td>
<td align="right">1.2%</td>
<td align="right">11,901</td>
<td align="right">1.2%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">operator wrapper</td>
<td align="right">10,184</td>
<td align="right">1.0%</td>
<td align="right">10,178</td>
<td align="right">1.0%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">73,827</td>
<td align="right">7.2%</td>
<td align="right">73,791</td>
<td align="right">7.2%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">class no vectorcall</td>
<td align="right">79,108</td>
<td align="right">7.7%</td>
<td align="right">79,084</td>
<td align="right">7.7%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">cfunc varargs keywords</td>
<td align="right">32,185</td>
<td align="right">3.1%</td>
<td align="right">32,193</td>
<td align="right">3.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">meth descr varargs keywords</td>
<td align="right">20,875</td>
<td align="right">2.0%</td>
<td align="right">20,871</td>
<td align="right">2.0%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">no dict</td>
<td align="right">105,276</td>
<td align="right">10.3%</td>
<td align="right">105,256</td>
<td align="right">10.3%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">meth descr method fastcall keywords</td>
<td align="right">207,220</td>
<td align="right">20.2%</td>
<td align="right">207,256</td>
<td align="right">20.3%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">cfunc varargs</td>
<td align="right">14,149</td>
<td align="right">1.4%</td>
<td align="right">14,151</td>
<td align="right">1.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">code complex parameters</td>
<td align="right">186,799</td>
<td align="right">18.2%</td>
<td align="right">186,811</td>
<td align="right">18.3%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">meth descr varargs</td>
<td align="right">75,340</td>
<td align="right">7.4%</td>
<td align="right">75,337</td>
<td align="right">7.4%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">init not simple</td>
<td align="right">12,278</td>
<td align="right">1.2%</td>
<td align="right">12,278</td>
<td align="right">1.2%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">str</td>
<td align="right">3,200</td>
<td align="right">0.3%</td>
<td align="right">3,200</td>
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
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">144,081,294</td>
<td align="right">3.0%</td>
<td align="right">135,458,565</td>
<td align="right">2.9%</td>
<td align="right">-6.0%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">1,701,460</td>
<td align="right">0.0%</td>
<td align="right">1,728,588</td>
<td align="right">0.0%</td>
<td align="right">1.6%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">4,588,558,348</td>
<td align="right">96.9%</td>
<td align="right">4,587,781,006</td>
<td align="right">97.1%</td>
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
<td align="right">222,907</td>
<td align="right">66.9%</td>
<td align="right">220,827</td>
<td align="right">66.6%</td>
<td align="right">-0.9%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">110,309</td>
<td align="right">33.1%</td>
<td align="right">110,833</td>
<td align="right">33.4%</td>
<td align="right">0.5%</td>
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
<td align="right">2,343</td>
<td align="right">1.1%</td>
<td align="right">1,643</td>
<td align="right">0.7%</td>
<td align="right">-29.9%</td>
</tr>
<tr>
<td align="left">baseobject</td>
<td align="right">34,213</td>
<td align="right">15.3%</td>
<td align="right">31,655</td>
<td align="right">14.3%</td>
<td align="right">-7.5%</td>
</tr>
<tr>
<td align="left">bytes</td>
<td align="right">4,220</td>
<td align="right">1.9%</td>
<td align="right">3,980</td>
<td align="right">1.8%</td>
<td align="right">-5.7%</td>
</tr>
<tr>
<td align="left">big int</td>
<td align="right">60,725</td>
<td align="right">27.2%</td>
<td align="right">63,094</td>
<td align="right">28.6%</td>
<td align="right">3.9%</td>
</tr>
<tr>
<td align="left">bool</td>
<td align="right">3,747</td>
<td align="right">1.7%</td>
<td align="right">3,680</td>
<td align="right">1.7%</td>
<td align="right">-1.8%</td>
</tr>
<tr>
<td align="left">different types</td>
<td align="right">48,998</td>
<td align="right">22.0%</td>
<td align="right">48,378</td>
<td align="right">21.9%</td>
<td align="right">-1.3%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">23,865</td>
<td align="right">10.7%</td>
<td align="right">23,662</td>
<td align="right">10.7%</td>
<td align="right">-0.9%</td>
</tr>
<tr>
<td align="left">long float</td>
<td align="right">1,565</td>
<td align="right">0.7%</td>
<td align="right">1,576</td>
<td align="right">0.7%</td>
<td align="right">0.7%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">14,552</td>
<td align="right">6.5%</td>
<td align="right">14,482</td>
<td align="right">6.6%</td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">4,371</td>
<td align="right">2.0%</td>
<td align="right">4,370</td>
<td align="right">2.0%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">float long</td>
<td align="right">13,188</td>
<td align="right">5.9%</td>
<td align="right">13,187</td>
<td align="right">6.0%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">string</td>
<td align="right">11,120</td>
<td align="right">5.0%</td>
<td align="right">11,120</td>
<td align="right">5.0%</td>
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
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">119,499,668</td>
<td align="right">4.6%</td>
<td align="right">110,171,859</td>
<td align="right">4.3%</td>
<td align="right">-7.8%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">2,481,712,730</td>
<td align="right">95.4%</td>
<td align="right">2,478,938,876</td>
<td align="right">95.7%</td>
<td align="right">-0.1%</td>
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
<td align="right">0.1%</td>
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
<td align="right">132,580</td>
<td align="right">66.2%</td>
<td align="right">125,263</td>
<td align="right">64.9%</td>
<td align="right">-5.5%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">67,667</td>
<td align="right">33.8%</td>
<td align="right">67,674</td>
<td align="right">35.1%</td>
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
<td align="right">36,842</td>
<td align="right">27.8%</td>
<td align="right">32,734</td>
<td align="right">26.1%</td>
<td align="right">-11.2%</td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">19,661</td>
<td align="right">14.8%</td>
<td align="right">18,084</td>
<td align="right">14.4%</td>
<td align="right">-8.0%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">28,900</td>
<td align="right">21.8%</td>
<td align="right">27,933</td>
<td align="right">22.3%</td>
<td align="right">-3.3%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">47,177</td>
<td align="right">35.6%</td>
<td align="right">46,512</td>
<td align="right">37.1%</td>
<td align="right">-1.4%</td>
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
<td align="right">123,355,422</td>
<td align="right">8.2%</td>
<td align="right">3,341,963</td>
<td align="right">0.8%</td>
<td align="right">-97.3%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">1,251,232,763</td>
<td align="right">83.1%</td>
<td align="right">266,268,576</td>
<td align="right">67.7%</td>
<td align="right">-78.7%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">251,522,372</td>
<td align="right">16.7%</td>
<td align="right">126,981,225</td>
<td align="right">32.3%</td>
<td align="right">-49.5%</td>
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
<td align="right">2,393,842</td>
<td align="right">92.4%</td>
<td align="right">129,598</td>
<td align="right">43.8%</td>
<td align="right">-94.6%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">197,163</td>
<td align="right">7.6%</td>
<td align="right">166,318</td>
<td align="right">56.2%</td>
<td align="right">-15.6%</td>
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
<td align="right">10,600</td>
<td align="right">5.4%</td>
<td align="right">6,240</td>
<td align="right">3.8%</td>
<td align="right">-41.1%</td>
</tr>
<tr>
<td align="left">dict items</td>
<td align="right">68,672</td>
<td align="right">34.8%</td>
<td align="right">49,866</td>
<td align="right">30.0%</td>
<td align="right">-27.4%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">15,139</td>
<td align="right">7.7%</td>
<td align="right">11,299</td>
<td align="right">6.8%</td>
<td align="right">-25.4%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">25,904</td>
<td align="right">13.1%</td>
<td align="right">22,575</td>
<td align="right">13.6%</td>
<td align="right">-12.9%</td>
</tr>
<tr>
<td align="left">itertools</td>
<td align="right">7,491</td>
<td align="right">3.8%</td>
<td align="right">7,269</td>
<td align="right">4.4%</td>
<td align="right">-3.0%</td>
</tr>
<tr>
<td align="left">dict keys</td>
<td align="right">14,776</td>
<td align="right">7.5%</td>
<td align="right">14,510</td>
<td align="right">8.7%</td>
<td align="right">-1.8%</td>
</tr>
<tr>
<td align="left">ascii string</td>
<td align="right">2,680</td>
<td align="right">1.4%</td>
<td align="right">2,640</td>
<td align="right">1.6%</td>
<td align="right">-1.5%</td>
</tr>
<tr>
<td align="left">reversed list</td>
<td align="right">8,065</td>
<td align="right">4.1%</td>
<td align="right">8,105</td>
<td align="right">4.9%</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">dict values</td>
<td align="right">7,010</td>
<td align="right">3.6%</td>
<td align="right">6,990</td>
<td align="right">4.2%</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">enumerate</td>
<td align="right">19,892</td>
<td align="right">10.1%</td>
<td align="right">19,890</td>
<td align="right">12.0%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">zip</td>
<td align="right">14,352</td>
<td align="right">7.3%</td>
<td align="right">14,352</td>
<td align="right">8.6%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">map</td>
<td align="right">1,600</td>
<td align="right">0.8%</td>
<td align="right">1,600</td>
<td align="right">1.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">bytes</td>
<td align="right">660</td>
<td align="right">0.3%</td>
<td align="right">660</td>
<td align="right">0.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">callable</td>
<td align="right">282</td>
<td align="right">0.1%</td>
<td align="right">282</td>
<td align="right">0.2%</td>
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
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">1,536,965,406</td>
<td align="right">9.5%</td>
<td align="right">1,482,359,125</td>
<td align="right">9.2%</td>
<td align="right">-3.6%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">501,498,224</td>
<td align="right">3.1%</td>
<td align="right">497,536,905</td>
<td align="right">3.1%</td>
<td align="right">-0.8%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">14,609,744,727</td>
<td align="right">90.4%</td>
<td align="right">14,584,242,463</td>
<td align="right">90.7%</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">
deopt
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">2,133,101</td>
<td align="right">0.0%</td>
<td align="right">2,134,283</td>
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
<td align="left">Failure</td>
<td align="right">1,405,876</td>
<td align="right">12.0%</td>
<td align="right">1,367,571</td>
<td align="right">11.8%</td>
<td align="right">-2.7%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">10,328,040</td>
<td align="right">88.0%</td>
<td align="right">10,253,187</td>
<td align="right">88.2%</td>
<td align="right">-0.7%</td>
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
<td align="left">class method obj</td>
<td align="right">25,553</td>
<td align="right">1.8%</td>
<td align="right">21,673</td>
<td align="right">1.6%</td>
<td align="right">-15.2%</td>
</tr>
<tr>
<td align="left">has managed dict</td>
<td align="right">527,176</td>
<td align="right">37.5%</td>
<td align="right">509,890</td>
<td align="right">37.3%</td>
<td align="right">-3.3%</td>
</tr>
<tr>
<td align="left">metaclass attribute</td>
<td align="right">193,661</td>
<td align="right">13.8%</td>
<td align="right">187,959</td>
<td align="right">13.7%</td>
<td align="right">-2.9%</td>
</tr>
<tr>
<td align="left">method</td>
<td align="right">120,872</td>
<td align="right">8.6%</td>
<td align="right">117,707</td>
<td align="right">8.6%</td>
<td align="right">-2.6%</td>
</tr>
<tr>
<td align="left">out of versions</td>
<td align="right">2,341</td>
<td align="right">0.2%</td>
<td align="right">2,281</td>
<td align="right">0.2%</td>
<td align="right">-2.6%</td>
</tr>
<tr>
<td align="left">mutable class</td>
<td align="right">77,611</td>
<td align="right">5.5%</td>
<td align="right">75,860</td>
<td align="right">5.5%</td>
<td align="right">-2.3%</td>
</tr>
<tr>
<td align="left">not managed dict</td>
<td align="right">212,955</td>
<td align="right">15.1%</td>
<td align="right">209,024</td>
<td align="right">15.3%</td>
<td align="right">-1.8%</td>
</tr>
<tr>
<td align="left">non overriding descriptor</td>
<td align="right">13,769</td>
<td align="right">1.0%</td>
<td align="right">13,540</td>
<td align="right">1.0%</td>
<td align="right">-1.7%</td>
</tr>
<tr>
<td align="left">shadowed</td>
<td align="right">110,724</td>
<td align="right">7.9%</td>
<td align="right">108,994</td>
<td align="right">8.0%</td>
<td align="right">-1.6%</td>
</tr>
<tr>
<td align="left">class attr simple</td>
<td align="right">28,181</td>
<td align="right">2.0%</td>
<td align="right">27,876</td>
<td align="right">2.0%</td>
<td align="right">-1.1%</td>
</tr>
<tr>
<td align="left">not in keys</td>
<td align="right">13,280</td>
<td align="right">0.9%</td>
<td align="right">13,160</td>
<td align="right">1.0%</td>
<td align="right">-0.9%</td>
</tr>
<tr>
<td align="left">class attr descriptor</td>
<td align="right">29,520</td>
<td align="right">2.1%</td>
<td align="right">29,400</td>
<td align="right">2.1%</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">overridden</td>
<td align="right">19,454</td>
<td align="right">1.4%</td>
<td align="right">19,427</td>
<td align="right">1.4%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">non object slot</td>
<td align="right">3,601</td>
<td align="right">0.3%</td>
<td align="right">3,603</td>
<td align="right">0.3%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">builtin class method</td>
<td align="right">3,836</td>
<td align="right">0.3%</td>
<td align="right">3,835</td>
<td align="right">0.3%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">module attr not found</td>
<td align="right">17,522</td>
<td align="right">1.2%</td>
<td align="right">17,522</td>
<td align="right">1.3%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">non string or split</td>
<td align="right">4,260</td>
<td align="right">0.3%</td>
<td align="right">4,260</td>
<td align="right">0.3%</td>
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
<td align="right">6,874,130,485</td>
<td align="right">99.7%</td>
<td align="right">5,822,356,927</td>
<td align="right">99.6%</td>
<td align="right">-15.3%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">434,786</td>
<td align="right">0.0%</td>
<td align="right">434,604</td>
<td align="right">0.0%</td>
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
<td align="right">20,567,959</td>
<td align="right">0.3%</td>
<td align="right">20,567,908</td>
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
<td align="right">670,637</td>
<td align="right">100.0%</td>
<td align="right">670,734</td>
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
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">135,268,161</td>
<td align="right">100.0%</td>
<td align="right">135,297,485</td>
<td align="right">100.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">12,006</td>
<td align="right">0.0%</td>
<td align="right">12,008</td>
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
<td align="right">11,837</td>
<td align="right">100.0%</td>
<td align="right">11,838</td>
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
<td align="right">173,914,474</td>
<td align="right">18.1%</td>
<td align="right">173,916,055</td>
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
<td align="right">787,152,722</td>
<td align="right">81.9%</td>
<td align="right">787,157,275</td>
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
<td align="right">7,130</td>
<td align="right">10.3%</td>
<td align="right">7,131</td>
<td align="right">10.3%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">61,867</td>
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
<td align="right">16,127</td>
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
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">167,809,025</td>
<td align="right">5.6%</td>
<td align="right">168,567,518</td>
<td align="right">5.6%</td>
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
<td align="right">237,528,762</td>
<td align="right">7.9%</td>
<td align="right">238,200,773</td>
<td align="right">7.9%</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">2,781,665,040</td>
<td align="right">92.0%</td>
<td align="right">2,782,431,495</td>
<td align="right">92.0%</td>
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
<td align="right">3,321,939</td>
<td align="right">96.2%</td>
<td align="right">3,336,249</td>
<td align="right">96.2%</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">131,398</td>
<td align="right">3.8%</td>
<td align="right">131,159</td>
<td align="right">3.8%</td>
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
<td align="left">out of versions</td>
<td align="right">594</td>
<td align="right">0.5%</td>
<td align="right">573</td>
<td align="right">0.4%</td>
<td align="right">-3.5%</td>
</tr>
<tr>
<td align="left">method</td>
<td align="right">1,580</td>
<td align="right">1.2%</td>
<td align="right">1,540</td>
<td align="right">1.2%</td>
<td align="right">-2.5%</td>
</tr>
<tr>
<td align="left">overriding descriptor</td>
<td align="right">10,800</td>
<td align="right">8.2%</td>
<td align="right">10,760</td>
<td align="right">8.2%</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">class attr simple</td>
<td align="right">50,098</td>
<td align="right">38.1%</td>
<td align="right">49,958</td>
<td align="right">38.1%</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">not managed dict</td>
<td align="right">28,568</td>
<td align="right">21.7%</td>
<td align="right">28,570</td>
<td align="right">21.8%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">not in dict</td>
<td align="right">15,725</td>
<td align="right">12.0%</td>
<td align="right">15,725</td>
<td align="right">12.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">not in keys</td>
<td align="right">7,981</td>
<td align="right">6.1%</td>
<td align="right">7,981</td>
<td align="right">6.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">overridden</td>
<td align="right">6,832</td>
<td align="right">5.2%</td>
<td align="right">6,832</td>
<td align="right">5.2%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">property</td>
<td align="right">5,740</td>
<td align="right">4.4%</td>
<td align="right">5,740</td>
<td align="right">4.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">no dict</td>
<td align="right">3,440</td>
<td align="right">2.6%</td>
<td align="right">3,440</td>
<td align="right">2.6%</td>
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
<td align="right">134,197,858</td>
<td align="right">13.1%</td>
<td align="right">132,763,448</td>
<td align="right">13.0%</td>
<td align="right">-1.1%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">886,580,343</td>
<td align="right">86.8%</td>
<td align="right">885,739,684</td>
<td align="right">87.0%</td>
<td align="right">-0.1%</td>
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
<td align="right">83,245</td>
<td align="right">81.7%</td>
<td align="right">81,557</td>
<td align="right">81.3%</td>
<td align="right">-2.0%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">18,706</td>
<td align="right">18.3%</td>
<td align="right">18,709</td>
<td align="right">18.7%</td>
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
<td align="right">7,200</td>
<td align="right">8.6%</td>
<td align="right">6,520</td>
<td align="right">8.0%</td>
<td align="right">-9.4%</td>
</tr>
<tr>
<td align="left">out of range</td>
<td align="right">2,008</td>
<td align="right">2.4%</td>
<td align="right">1,888</td>
<td align="right">2.3%</td>
<td align="right">-6.0%</td>
</tr>
<tr>
<td align="left">bytearray int</td>
<td align="right">1,080</td>
<td align="right">1.3%</td>
<td align="right">1,020</td>
<td align="right">1.3%</td>
<td align="right">-5.6%</td>
</tr>
<tr>
<td align="left">dict subclass no override</td>
<td align="right">28,202</td>
<td align="right">33.9%</td>
<td align="right">27,655</td>
<td align="right">33.9%</td>
<td align="right">-1.9%</td>
</tr>
<tr>
<td align="left">py simple</td>
<td align="right">42,635</td>
<td align="right">51.2%</td>
<td align="right">42,354</td>
<td align="right">51.9%</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">2,080</td>
<td align="right">2.5%</td>
<td align="right">2,080</td>
<td align="right">2.6%</td>
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
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">361,041,342</td>
<td align="right">5.6%</td>
<td align="right">343,191,357</td>
<td align="right">5.3%</td>
<td align="right">-4.9%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">106,553,914</td>
<td align="right">1.6%</td>
<td align="right">103,170,921</td>
<td align="right">1.6%</td>
<td align="right">-3.2%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">6,112,016,328</td>
<td align="right">94.4%</td>
<td align="right">6,103,204,968</td>
<td align="right">94.6%</td>
<td align="right">-0.1%</td>
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
<td align="right">670,800</td>
<td align="right">22.6%</td>
<td align="right">625,471</td>
<td align="right">21.9%</td>
<td align="right">-6.8%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">2,296,149</td>
<td align="right">77.4%</td>
<td align="right">2,232,215</td>
<td align="right">78.1%</td>
<td align="right">-2.8%</td>
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
<td align="left">mapping</td>
<td align="right">99,107</td>
<td align="right">14.8%</td>
<td align="right">57,311</td>
<td align="right">9.2%</td>
<td align="right">-42.2%</td>
</tr>
<tr>
<td align="left">dict</td>
<td align="right">33,672</td>
<td align="right">5.0%</td>
<td align="right">31,272</td>
<td align="right">5.0%</td>
<td align="right">-7.1%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">43,634</td>
<td align="right">6.5%</td>
<td align="right">43,120</td>
<td align="right">6.9%</td>
<td align="right">-1.2%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">95,684</td>
<td align="right">14.3%</td>
<td align="right">95,169</td>
<td align="right">15.2%</td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">number</td>
<td align="right">183,555</td>
<td align="right">27.4%</td>
<td align="right">183,503</td>
<td align="right">29.3%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">173,754</td>
<td align="right">25.9%</td>
<td align="right">173,707</td>
<td align="right">27.8%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">sequence</td>
<td align="right">18,094</td>
<td align="right">2.7%</td>
<td align="right">18,090</td>
<td align="right">2.9%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">bytes</td>
<td align="right">19,039</td>
<td align="right">2.8%</td>
<td align="right">19,038</td>
<td align="right">3.0%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">float</td>
<td align="right">2,601</td>
<td align="right">0.4%</td>
<td align="right">2,601</td>
<td align="right">0.4%</td>
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
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">926,409</td>
<td align="right">0.0%</td>
<td align="right">843,136</td>
<td align="right">0.0%</td>
<td align="right">-9.0%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">2,090,659,367</td>
<td align="right">100.0%</td>
<td align="right">2,078,843,293</td>
<td align="right">100.0%</td>
<td align="right">-0.6%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">427,900</td>
<td align="right">0.0%</td>
<td align="right">425,800</td>
<td align="right">0.0%</td>
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
<td align="right">3,599</td>
<td align="right">6.0%</td>
<td align="right">3,517</td>
<td align="right">5.9%</td>
<td align="right">-2.3%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">56,065</td>
<td align="right">94.0%</td>
<td align="right">56,058</td>
<td align="right">94.1%</td>
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
<td align="right">380</td>
<td align="right">10.6%</td>
<td align="right">340</td>
<td align="right">9.7%</td>
<td align="right">-10.5%</td>
</tr>
<tr>
<td align="left">sequence</td>
<td align="right">2,518</td>
<td align="right">70.0%</td>
<td align="right">2,476</td>
<td align="right">70.4%</td>
<td align="right">-1.7%</td>
</tr>
<tr>
<td align="left">iterator</td>
<td align="right">701</td>
<td align="right">19.5%</td>
<td align="right">701</td>
<td align="right">19.9%</td>
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
<td align="right">1,187,637,997</td>
<td align="right">0.9%</td>
<td align="right">1,060,203,155</td>
<td align="right">0.9%</td>
<td align="right">-10.7%</td>
</tr>
<tr>
<td align="left">
Specialized hits
<details>
<summary>ⓘ</summary>

Specialized instructions, e.g. `LOAD_ATTR_MODULE` that complete.
</details>
</td>
<td align="right">47,292,842,137</td>
<td align="right">34.9%</td>
<td align="right">42,264,899,544</td>
<td align="right">34.1%</td>
<td align="right">-10.6%</td>
</tr>
<tr>
<td align="left">
Basic
<details>
<summary>ⓘ</summary>

Instructions that are not and cannot be specialized, e.g. `LOAD_FAST`.
</details>
</td>
<td align="right">74,149,617,261</td>
<td align="right">54.7%</td>
<td align="right">68,577,195,464</td>
<td align="right">55.4%</td>
<td align="right">-7.5%</td>
</tr>
<tr>
<td align="left">
Not specialized
<details>
<summary>ⓘ</summary>

Instructions that could be specialized but aren't, e.g. `LOAD_ATTR`, `BINARY_SLICE`.
</details>
</td>
<td align="right">12,842,749,494</td>
<td align="right">9.5%</td>
<td align="right">11,944,974,804</td>
<td align="right">9.6%</td>
<td align="right">-7.0%</td>
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
<td align="right">251,522,372</td>
<td align="right">4.5%</td>
<td align="right">126,981,225</td>
<td align="right">2.4%</td>
<td align="right">-49.5%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR</td>
<td align="right">426,978,523</td>
<td align="right">7.7%</td>
<td align="right">335,212,593</td>
<td align="right">6.4%</td>
<td align="right">-21.5%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">144,081,294</td>
<td align="right">2.6%</td>
<td align="right">135,458,565</td>
<td align="right">2.6%</td>
<td align="right">-6.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">361,041,342</td>
<td align="right">6.5%</td>
<td align="right">343,191,357</td>
<td align="right">6.6%</td>
<td align="right">-4.9%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">633,642,282</td>
<td align="right">11.4%</td>
<td align="right">607,534,730</td>
<td align="right">11.6%</td>
<td align="right">-4.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">1,536,965,406</td>
<td align="right">27.7%</td>
<td align="right">1,482,359,125</td>
<td align="right">28.4%</td>
<td align="right">-3.6%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR</td>
<td align="right">134,197,858</td>
<td align="right">2.4%</td>
<td align="right">132,763,448</td>
<td align="right">2.5%</td>
<td align="right">-1.1%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">1,513,892,655</td>
<td align="right">27.3%</td>
<td align="right">1,508,086,889</td>
<td align="right">28.9%</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">237,528,762</td>
<td align="right">4.3%</td>
<td align="right">238,200,773</td>
<td align="right">4.6%</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">SEND</td>
<td align="right">173,914,474</td>
<td align="right">3.1%</td>
<td align="right">173,916,055</td>
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
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">98,032,811</td>
<td align="right">8.3%</td>
<td align="right">96,993,146</td>
<td align="right">9.1%</td>
<td align="right">-1.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">161,272,754</td>
<td align="right">13.6%</td>
<td align="right">159,577,605</td>
<td align="right">15.0%</td>
<td align="right">-1.1%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">72,763,833</td>
<td align="right">6.1%</td>
<td align="right">73,480,362</td>
<td align="right">6.9%</td>
<td align="right">1.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL_NONE</td>
<td align="right">49,196,924</td>
<td align="right">4.1%</td>
<td align="right">48,762,113</td>
<td align="right">4.6%</td>
<td align="right">-0.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">110,412,702</td>
<td align="right">9.3%</td>
<td align="right">109,625,588</td>
<td align="right">10.3%</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">132,657,271</td>
<td align="right">11.2%</td>
<td align="right">131,808,091</td>
<td align="right">12.4%</td>
<td align="right">-0.6%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right">69,143,640</td>
<td align="right">5.8%</td>
<td align="right">69,068,299</td>
<td align="right">6.5%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_SLOT</td>
<td align="right">94,992,413</td>
<td align="right">8.0%</td>
<td align="right">95,034,305</td>
<td align="right">9.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">61,639,187</td>
<td align="right">5.2%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">FOR_ITER_TUPLE</td>
<td align="right">61,476,575</td>
<td align="right">5.2%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">TO_BOOL_ALWAYS_TRUE</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">46,573,599</td>
<td align="right">4.4%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">41,954,228</td>
<td align="right">4.0%</td>
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
<td align="right">5,298,324</td>
<td align="right">0.1%</td>
<td align="right">4,418,244</td>
<td align="right">0.1%</td>
<td align="right">-16.6%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (generator)</td>
<td align="right">866,951,116</td>
<td align="right">9.8%</td>
<td align="right">875,168,898</td>
<td align="right">10.0%</td>
<td align="right">0.9%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (slot)</td>
<td align="right">480,026,884</td>
<td align="right">5.4%</td>
<td align="right">483,605,466</td>
<td align="right">5.5%</td>
<td align="right">0.7%</td>
</tr>
<tr>
<td align="left">Calls to Python functions inlined</td>
<td align="right">6,498,599,868</td>
<td align="right">73.7%</td>
<td align="right">6,453,481,267</td>
<td align="right">73.4%</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">Calls to PyEval_EvalDefault</td>
<td align="right">2,324,194,151</td>
<td align="right">26.3%</td>
<td align="right">2,335,676,293</td>
<td align="right">26.6%</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (total)</td>
<td align="right">2,324,194,151</td>
<td align="right">26.3%</td>
<td align="right">2,335,676,293</td>
<td align="right">26.6%</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (function vectorcall)</td>
<td align="right">1,451,915,925</td>
<td align="right">16.5%</td>
<td align="right">1,456,060,365</td>
<td align="right">16.6%</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (vector)</td>
<td align="right">1,457,243,035</td>
<td align="right">16.5%</td>
<td align="right">1,460,507,395</td>
<td align="right">16.6%</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (api)</td>
<td align="right">259,018,203</td>
<td align="right">2.9%</td>
<td align="right">259,573,950</td>
<td align="right">3.0%</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">Frames pushed</td>
<td align="right">7,023,929,954</td>
<td align="right">79.6%</td>
<td align="right">7,015,035,635</td>
<td align="right">79.8%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (function ex)</td>
<td align="right">38,450,181</td>
<td align="right">0.4%</td>
<td align="right">38,459,440</td>
<td align="right">0.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Frame objects created</td>
<td align="right">88,595,196</td>
<td align="right">1.0%</td>
<td align="right">88,602,839</td>
<td align="right">1.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (method)</td>
<td align="right">213,138,138</td>
<td align="right">2.4%</td>
<td align="right">213,149,299</td>
<td align="right">2.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (build class)</td>
<td align="right">28,786</td>
<td align="right">0.0%</td>
<td align="right">28,786</td>
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
<td align="left">Increfs</td>
<td align="right">62,619,070,488</td>
<td align="right">51.5%</td>
<td align="right">67,222,389,269</td>
<td align="right">55.1%</td>
<td align="right">7.4%</td>
</tr>
<tr>
<td align="left">Interpreter increfs</td>
<td align="right">58,978,886,073</td>
<td align="right">48.5%</td>
<td align="right">54,786,219,019</td>
<td align="right">44.9%</td>
<td align="right">-7.1%</td>
</tr>
<tr>
<td align="left">Decrefs</td>
<td align="right">65,376,043,258</td>
<td align="right">47.0%</td>
<td align="right">69,344,970,605</td>
<td align="right">49.7%</td>
<td align="right">6.1%</td>
</tr>
<tr>
<td align="left">Interpreter decrefs</td>
<td align="right">73,843,951,907</td>
<td align="right">53.0%</td>
<td align="right">70,257,890,435</td>
<td align="right">50.3%</td>
<td align="right">-4.9%</td>
</tr>
<tr>
<td align="left">Method cache misses</td>
<td align="right">79,551,232</td>
<td align="right"></td>
<td align="right">76,716,295</td>
<td align="right"></td>
<td align="right">-3.6%</td>
</tr>
<tr>
<td align="left">Method cache collisions</td>
<td align="right">83,831,177</td>
<td align="right"></td>
<td align="right">81,226,639</td>
<td align="right"></td>
<td align="right">-3.1%</td>
</tr>
<tr>
<td align="left">Method cache dunder misses</td>
<td align="right">12,050,198</td>
<td align="right"></td>
<td align="right">12,277,964</td>
<td align="right"></td>
<td align="right">1.9%</td>
</tr>
<tr>
<td align="left">Dematerialize dict</td>
<td align="right">2,710,060</td>
<td align="right">2,710,060 / 0 !!</td>
<td align="right">2,721,480</td>
<td align="right">2,721,480 / 0 !!</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">Allocations to 4 kbytes</td>
<td align="right">104,981,979</td>
<td align="right">0.6%</td>
<td align="right">105,381,984</td>
<td align="right">0.6%</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">Allocations from freelist</td>
<td align="right">6,919,499,080</td>
<td align="right">36.6%</td>
<td align="right">6,899,934,956</td>
<td align="right">36.6%</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">Frees to freelist</td>
<td align="right">6,921,459,607</td>
<td align="right"></td>
<td align="right">6,901,892,588</td>
<td align="right"></td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">Materialize dict (on request)</td>
<td align="right">4,312,725</td>
<td align="right">4,312,725 / 0 !!</td>
<td align="right">4,324,185</td>
<td align="right">4,324,185 / 0 !!</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">Frees</td>
<td align="right">12,308,013,279</td>
<td align="right"></td>
<td align="right">12,289,451,755</td>
<td align="right"></td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">Allocations over 4 kbytes</td>
<td align="right">21,241,208</td>
<td align="right">0.1%</td>
<td align="right">21,270,541</td>
<td align="right">0.1%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">Allocations to 512 bytes</td>
<td align="right">11,856,364,546</td>
<td align="right">62.7%</td>
<td align="right">11,841,301,246</td>
<td align="right">62.8%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">Allocations</td>
<td align="right">11,982,587,733</td>
<td align="right">63.4%</td>
<td align="right">11,967,953,771</td>
<td align="right">63.4%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">Method cache dunder hits</td>
<td align="right">3,577,323,142</td>
<td align="right"></td>
<td align="right">3,578,870,891</td>
<td align="right"></td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Method cache hits</td>
<td align="right">3,372,783,697</td>
<td align="right"></td>
<td align="right">3,374,160,892</td>
<td align="right"></td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">New values</td>
<td align="right">91,405,163</td>
<td align="right"></td>
<td align="right">91,419,688</td>
<td align="right"></td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Materialize dict (new key)</td>
<td align="right">233,295</td>
<td align="right">233,295 / 0 !!</td>
<td align="right">233,295</td>
<td align="right">233,295 / 0 !!</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Materialize dict (too big)</td>
<td align="right">0</td>
<td align="right"></td>
<td align="right">0</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">Materialize dict (str subclass)</td>
<td align="right">0</td>
<td align="right"></td>
<td align="right">0</td>
<td align="right"></td>
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
<td align="right">114,438,547</td>
<td align="right">16,970,894,128</td>
<td align="right">0</td>
<td align="right">114,456,633</td>
<td align="right">16,961,359,593</td>
</tr>
<tr>
<td align="right">2</td>
<td align="right">0</td>
<td align="right">10,753,920</td>
<td align="right">6,958,338,520</td>
<td align="right">0</td>
<td align="right">10,752,000</td>
<td align="right">6,963,419,790</td>
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
<td align="right">418</td>
<td align="right">0.0%</td>
<td align="right">2,621</td>
<td align="right">0.0%</td>
<td align="right">527.0%</td>
</tr>
<tr>
<td align="left">
Recursive call
<details>
<summary>ⓘ</summary>

A trace is truncated because it has a recursive call.
</details>
</td>
<td align="right">1,453</td>
<td align="right">0.0%</td>
<td align="right">2,373</td>
<td align="right">0.0%</td>
<td align="right">63.3%</td>
</tr>
<tr>
<td align="left">
Traces created
<details>
<summary>ⓘ</summary>

The number of traces that were successfully created.
</details>
</td>
<td align="right">115,940</td>
<td align="right">0.2%</td>
<td align="right">154,198</td>
<td align="right">0.2%</td>
<td align="right">33.0%</td>
</tr>
<tr>
<td align="left">
Low confidence
<details>
<summary>ⓘ</summary>

A trace is abandoned because the likelihood of the jump to top being taken is too low.
</details>
</td>
<td align="right">7,040</td>
<td align="right">0.0%</td>
<td align="right">8,704</td>
<td align="right">0.0%</td>
<td align="right">23.6%</td>
</tr>
<tr>
<td align="left">
Optimization attempts
<details>
<summary>ⓘ</summary>

The number of times a potential trace is identified.  Specifically, this occurs in the JUMP BACKWARD instruction when the counter reaches a threshold.
</details>
</td>
<td align="right">52,389,268</td>
<td align="right"></td>
<td align="right">64,672,938</td>
<td align="right"></td>
<td align="right">23.4%</td>
</tr>
<tr>
<td align="left">
Trace too short
<details>
<summary>ⓘ</summary>

A potential trace is abandoced because it it too short.
</details>
</td>
<td align="right">52,273,328</td>
<td align="right">99.8%</td>
<td align="right">64,518,740</td>
<td align="right">99.8%</td>
<td align="right">23.4%</td>
</tr>
<tr>
<td align="left">
Traces executed
<details>
<summary>ⓘ</summary>

The number of traces that were executed
</details>
</td>
<td align="right">6,388,348,566</td>
<td align="right"></td>
<td align="right">7,511,177,665</td>
<td align="right"></td>
<td align="right">17.6%</td>
</tr>
<tr>
<td align="left">
Uops executed
<details>
<summary>ⓘ</summary>

The total number of uops (micro-operations) that were executed
</details>
</td>
<td align="right">187,169,309,249</td>
<td align="right">2,929.9%</td>
<td align="right">208,478,852,930</td>
<td align="right">2,775.6%</td>
<td align="right">11.4%</td>
</tr>
<tr>
<td align="left">
Executors invalidated
<details>
<summary>ⓘ</summary>

The number of executors that were invalidated due to watched dictionary changes.
</details>
</td>
<td align="right">5,800</td>
<td align="right">5.0%</td>
<td align="right">6,180</td>
<td align="right">4.0%</td>
<td align="right">6.6%</td>
</tr>
<tr>
<td align="left">
Trace stack underflow
<details>
<summary>ⓘ</summary>

A potential trace is abandoned because it pops more frames than it pushes.
</details>
</td>
<td align="right">14,817,659</td>
<td align="right">28.3%</td>
<td align="right">14,472,737</td>
<td align="right">22.4%</td>
<td align="right">-2.3%</td>
</tr>
<tr>
<td align="left">
Inner loop found
<details>
<summary>ⓘ</summary>

A trace is truncated because it has an inner loop
</details>
</td>
<td align="right">361,062</td>
<td align="right">0.7%</td>
<td align="right">364,610</td>
<td align="right">0.6%</td>
<td align="right">1.0%</td>
</tr>
<tr>
<td align="left">
Trace too long
<details>
<summary>ⓘ</summary>

A trace is truncated because it is longer than the instruction buffer.
</details>
</td>
<td align="right">260</td>
<td align="right">0.0%</td>
<td align="right">260</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
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
<td align="right">113,815</td>
<td align="right">98.2%</td>
<td align="right">152,048</td>
<td align="right">98.6%</td>
<td align="right">33.6%</td>
</tr>
<tr>
<td align="left">
Optimizer attempts
<details>
<summary>ⓘ</summary>

The number of times the trace optimizer (_Py_uop_analyze_and_optimize) was run.
</details>
</td>
<td align="right">115,940</td>
<td align="right"></td>
<td align="right">154,198</td>
<td align="right"></td>
<td align="right">33.0%</td>
</tr>
<tr>
<td align="left">
Remove globals incorrect keys
<details>
<summary>ⓘ</summary>

The keys in the globals dictionary aren't what was expected
</details>
</td>
<td align="right">2,060</td>
<td align="right">1.8%</td>
<td align="right">2,081</td>
<td align="right">1.3%</td>
<td align="right">1.0%</td>
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
<td align="right">3,035</td>
<td align="right">2.6%</td>
<td align="right">3,996</td>
<td align="right">2.6%</td>
<td align="right">31.7%</td>
</tr>
<tr>
<td align="left"><= 16</td>
<td align="right">19,358</td>
<td align="right">16.7%</td>
<td align="right">27,109</td>
<td align="right">17.6%</td>
<td align="right">40.0%</td>
</tr>
<tr>
<td align="left"><= 32</td>
<td align="right">44,174</td>
<td align="right">38.1%</td>
<td align="right">59,878</td>
<td align="right">38.8%</td>
<td align="right">35.6%</td>
</tr>
<tr>
<td align="left"><= 64</td>
<td align="right">27,772</td>
<td align="right">24.0%</td>
<td align="right">35,518</td>
<td align="right">23.0%</td>
<td align="right">27.9%</td>
</tr>
<tr>
<td align="left"><= 128</td>
<td align="right">15,723</td>
<td align="right">13.6%</td>
<td align="right">20,114</td>
<td align="right">13.0%</td>
<td align="right">27.9%</td>
</tr>
<tr>
<td align="left"><= 256</td>
<td align="right">4,831</td>
<td align="right">4.2%</td>
<td align="right">6,415</td>
<td align="right">4.2%</td>
<td align="right">32.8%</td>
</tr>
<tr>
<td align="left"><= 512</td>
<td align="right">787</td>
<td align="right">0.7%</td>
<td align="right">908</td>
<td align="right">0.6%</td>
<td align="right">15.4%</td>
</tr>
<tr>
<td align="left"><= 1,024</td>
<td align="right">260</td>
<td align="right">0.2%</td>
<td align="right">260</td>
<td align="right">0.2%</td>
<td align="right">0.0%</td>
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
<td align="right">81</td>
<td align="right">0.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left"><= 8</td>
<td align="right">9,267</td>
<td align="right">8.0%</td>
<td align="right">11,263</td>
<td align="right">7.3%</td>
<td align="right">21.5%</td>
</tr>
<tr>
<td align="left"><= 16</td>
<td align="right">34,970</td>
<td align="right">30.2%</td>
<td align="right">48,756</td>
<td align="right">31.6%</td>
<td align="right">39.4%</td>
</tr>
<tr>
<td align="left"><= 32</td>
<td align="right">38,200</td>
<td align="right">32.9%</td>
<td align="right">51,561</td>
<td align="right">33.4%</td>
<td align="right">35.0%</td>
</tr>
<tr>
<td align="left"><= 64</td>
<td align="right">20,560</td>
<td align="right">17.7%</td>
<td align="right">26,725</td>
<td align="right">17.3%</td>
<td align="right">30.0%</td>
</tr>
<tr>
<td align="left"><= 128</td>
<td align="right">7,964</td>
<td align="right">6.9%</td>
<td align="right">10,297</td>
<td align="right">6.7%</td>
<td align="right">29.3%</td>
</tr>
<tr>
<td align="left"><= 256</td>
<td align="right">2,233</td>
<td align="right">1.9%</td>
<td align="right">2,825</td>
<td align="right">1.8%</td>
<td align="right">26.5%</td>
</tr>
<tr>
<td align="left"><= 512</td>
<td align="right">540</td>
<td align="right">0.5%</td>
<td align="right">540</td>
<td align="right">0.4%</td>
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
<td align="left">_BUILD_CONST_KEY_MAP</td>
<td align="right">80,811</td>
<td align="right">4,083,812</td>
<td align="right">4,953.5%</td>
</tr>
<tr>
<td align="left">_CONVERT_VALUE</td>
<td align="right">798,700</td>
<td align="right">3,719,460</td>
<td align="right">365.7%</td>
</tr>
<tr>
<td align="left">_FOR_ITER_TIER_TWO</td>
<td align="right">407,939,240</td>
<td align="right">1,704,902,571</td>
<td align="right">317.9%</td>
</tr>
<tr>
<td align="left">_GUARD_BUILTINS_VERSION</td>
<td align="right">91,276</td>
<td align="right">216,621</td>
<td align="right">137.3%</td>
</tr>
<tr>
<td align="left">_BUILD_MAP</td>
<td align="right">9,982,091</td>
<td align="right">18,608,509</td>
<td align="right">86.4%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_4</td>
<td align="right">352,362,651</td>
<td align="right">625,054,597</td>
<td align="right">77.4%</td>
</tr>
<tr>
<td align="left">_CALL_TYPE_1</td>
<td align="right">189,633,677</td>
<td align="right">332,592,869</td>
<td align="right">75.4%</td>
</tr>
<tr>
<td align="left">_DICT_MERGE</td>
<td align="right">7,246,276</td>
<td align="right">11,844,119</td>
<td align="right">63.5%</td>
</tr>
<tr>
<td align="left">_CHECK_VALIDITY_AND_SET_IP</td>
<td align="right">2,399,217,510</td>
<td align="right">3,855,210,199</td>
<td align="right">60.7%</td>
</tr>
<tr>
<td align="left">_SET_ADD</td>
<td align="right">1,466,735</td>
<td align="right">2,204,750</td>
<td align="right">50.3%</td>
</tr>
<tr>
<td align="left">_LOAD_CONST_INLINE_BORROW_WITH_NULL</td>
<td align="right">319,530,614</td>
<td align="right">465,389,709</td>
<td align="right">45.6%</td>
</tr>
<tr>
<td align="left">_BINARY_SUBSCR_DICT</td>
<td align="right">263,124,977</td>
<td align="right">380,494,431</td>
<td align="right">44.6%</td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_FAST</td>
<td align="right">742,969,731</td>
<td align="right">1,028,545,462</td>
<td align="right">38.4%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">876,232,108</td>
<td align="right">1,185,848,292</td>
<td align="right">35.3%</td>
</tr>
<tr>
<td align="left">_GUARD_DORV_VALUES_INST_ATTR_FROM_DICT</td>
<td align="right">970,856,294</td>
<td align="right">1,293,426,152</td>
<td align="right">33.2%</td>
</tr>
<tr>
<td align="left">_GUARD_KEYS_VERSION</td>
<td align="right">970,775,828</td>
<td align="right">1,293,177,930</td>
<td align="right">33.2%</td>
</tr>
<tr>
<td align="left">_ERROR_POP_N</td>
<td align="right">489,260</td>
<td align="right">651,235</td>
<td align="right">33.1%</td>
</tr>
<tr>
<td align="left">_POP_FRAME</td>
<td align="right">519,807,098</td>
<td align="right">691,039,795</td>
<td align="right">32.9%</td>
</tr>
<tr>
<td align="left">_STORE_DEREF</td>
<td align="right">2,944,426</td>
<td align="right">3,877,031</td>
<td align="right">31.7%</td>
</tr>
<tr>
<td align="left">_SIDE_EXIT</td>
<td align="right">3,508,680,522</td>
<td align="right">4,606,980,161</td>
<td align="right">31.3%</td>
</tr>
<tr>
<td align="left">_FORMAT_SIMPLE</td>
<td align="right">9,565,825</td>
<td align="right">12,534,591</td>
<td align="right">31.0%</td>
</tr>
<tr>
<td align="left">_DEOPT</td>
<td align="right">1,208,455,915</td>
<td align="right">839,710,113</td>
<td align="right">-30.5%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_CHECK</td>
<td align="right">256,481</td>
<td align="right">334,717</td>
<td align="right">30.5%</td>
</tr>
<tr>
<td align="left">_BUILD_STRING</td>
<td align="right">3,310,060</td>
<td align="right">4,234,463</td>
<td align="right">27.9%</td>
</tr>
<tr>
<td align="left">_LOAD_CONST_INLINE_WITH_NULL</td>
<td align="right">1,614,292,002</td>
<td align="right">2,046,446,384</td>
<td align="right">26.8%</td>
</tr>
<tr>
<td align="left">_RESUME_CHECK</td>
<td align="right">1,242,754,124</td>
<td align="right">1,561,945,538</td>
<td align="right">25.7%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_5</td>
<td align="right">1,956,554,369</td>
<td align="right">2,458,961,807</td>
<td align="right">25.7%</td>
</tr>
<tr>
<td align="left">_CALL_ISINSTANCE</td>
<td align="right">314,814,555</td>
<td align="right">395,375,364</td>
<td align="right">25.6%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_4</td>
<td align="right">1,891,504,683</td>
<td align="right">2,354,890,926</td>
<td align="right">24.5%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_6</td>
<td align="right">655,083,440</td>
<td align="right">811,856,512</td>
<td align="right">23.9%</td>
</tr>
<tr>
<td align="left">_COLD_EXIT</td>
<td align="right">1,670,722,869</td>
<td align="right">2,063,836,156</td>
<td align="right">23.5%</td>
</tr>
<tr>
<td align="left">_PUSH_FRAME</td>
<td align="right">1,462,892,936</td>
<td align="right">1,795,083,783</td>
<td align="right">22.7%</td>
</tr>
<tr>
<td align="left">_SAVE_RETURN_OFFSET</td>
<td align="right">1,462,892,936</td>
<td align="right">1,795,083,783</td>
<td align="right">22.7%</td>
</tr>
<tr>
<td align="left">_CHECK_STACK_SPACE</td>
<td align="right">1,462,953,009</td>
<td align="right">1,795,155,170</td>
<td align="right">22.7%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_3</td>
<td align="right">627,869,277</td>
<td align="right">767,976,752</td>
<td align="right">22.3%</td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION_EXACT_ARGS</td>
<td align="right">1,522,181,371</td>
<td align="right">1,861,331,015</td>
<td align="right">22.3%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_5</td>
<td align="right">860,747,349</td>
<td align="right">1,051,267,631</td>
<td align="right">22.1%</td>
</tr>
<tr>
<td align="left">_LOAD_CONST_INLINE</td>
<td align="right">1,193,764,953</td>
<td align="right">1,448,671,765</td>
<td align="right">21.4%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_BOOL</td>
<td align="right">1,709,897,436</td>
<td align="right">2,066,138,724</td>
<td align="right">20.8%</td>
</tr>
<tr>
<td align="left">_UNPACK_SEQUENCE_TUPLE</td>
<td align="right">437,123,608</td>
<td align="right">523,047,553</td>
<td align="right">19.7%</td>
</tr>
<tr>
<td align="left">_LOAD_DEREF</td>
<td align="right">444,667,470</td>
<td align="right">531,941,046</td>
<td align="right">19.6%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_2</td>
<td align="right">2,639,569,022</td>
<td align="right">3,142,446,530</td>
<td align="right">19.1%</td>
</tr>
<tr>
<td align="left">_CHECK_PERIODIC</td>
<td align="right">2,052,215,362</td>
<td align="right">2,438,208,919</td>
<td align="right">18.8%</td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_FAST_WITH_KEYWORDS</td>
<td align="right">21,540,934</td>
<td align="right">25,558,198</td>
<td align="right">18.6%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_3</td>
<td align="right">3,018,596,535</td>
<td align="right">3,562,322,351</td>
<td align="right">18.0%</td>
</tr>
<tr>
<td align="left">_CONTAINS_OP_DICT</td>
<td align="right">362,301,438</td>
<td align="right">427,145,304</td>
<td align="right">17.9%</td>
</tr>
<tr>
<td align="left">_MAKE_CELL</td>
<td align="right">6,605,601</td>
<td align="right">7,767,971</td>
<td align="right">17.6%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_2</td>
<td align="right">709,895,658</td>
<td align="right">832,839,981</td>
<td align="right">17.3%</td>
</tr>
<tr>
<td align="left">_POP_TOP_LOAD_CONST_INLINE_BORROW</td>
<td align="right">827,831</td>
<td align="right">961,628</td>
<td align="right">16.2%</td>
</tr>
<tr>
<td align="left">_START_EXECUTOR</td>
<td align="right">4,717,625,697</td>
<td align="right">5,447,341,509</td>
<td align="right">15.5%</td>
</tr>
<tr>
<td align="left">_CHECK_ATTR_WITH_HINT</td>
<td align="right">93,587,154</td>
<td align="right">107,982,661</td>
<td align="right">15.4%</td>
</tr>
<tr>
<td align="left">_DELETE_SUBSCR</td>
<td align="right">1,445,940</td>
<td align="right">1,668,331</td>
<td align="right">15.4%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_WITH_HINT</td>
<td align="right">93,578,534</td>
<td align="right">107,967,841</td>
<td align="right">15.4%</td>
</tr>
<tr>
<td align="left">_ITER_CHECK_TUPLE</td>
<td align="right">496,240,115</td>
<td align="right">421,162,639</td>
<td align="right">-15.1%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_4</td>
<td align="right">667,945,871</td>
<td align="right">765,967,928</td>
<td align="right">14.7%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_NONDESCRIPTOR_NO_DICT</td>
<td align="right">20,128,677</td>
<td align="right">23,073,548</td>
<td align="right">14.6%</td>
</tr>
<tr>
<td align="left">_IS_OP</td>
<td align="right">339,353,647</td>
<td align="right">388,276,664</td>
<td align="right">14.4%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_STR</td>
<td align="right">25,843,326</td>
<td align="right">29,545,276</td>
<td align="right">14.3%</td>
</tr>
<tr>
<td align="left">_LOAD_GLOBAL_MODULE</td>
<td align="right">59,264,468</td>
<td align="right">67,620,922</td>
<td align="right">14.1%</td>
</tr>
<tr>
<td align="left">_UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">623,892,877</td>
<td align="right">710,239,025</td>
<td align="right">13.8%</td>
</tr>
<tr>
<td align="left">_ITER_CHECK_LIST</td>
<td align="right">1,569,137,794</td>
<td align="right">1,363,266,439</td>
<td align="right">-13.1%</td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_O</td>
<td align="right">591,112,575</td>
<td align="right">668,289,939</td>
<td align="right">13.1%</td>
</tr>
<tr>
<td align="left">_GUARD_GLOBALS_VERSION</td>
<td align="right">65,868,664</td>
<td align="right">74,350,463</td>
<td align="right">12.9%</td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_O</td>
<td align="right">18,831,771</td>
<td align="right">21,241,827</td>
<td align="right">12.8%</td>
</tr>
<tr>
<td align="left">_PUSH_NULL</td>
<td align="right">709,885,277</td>
<td align="right">797,122,410</td>
<td align="right">12.3%</td>
</tr>
<tr>
<td align="left">_CONTAINS_OP_SET</td>
<td align="right">1,424,638,549</td>
<td align="right">1,595,061,013</td>
<td align="right">12.0%</td>
</tr>
<tr>
<td align="left">_GUARD_NOT_EXHAUSTED_TUPLE</td>
<td align="right">419,009,817</td>
<td align="right">368,962,447</td>
<td align="right">-11.9%</td>
</tr>
<tr>
<td align="left">_BUILD_TUPLE</td>
<td align="right">373,068,169</td>
<td align="right">416,297,041</td>
<td align="right">11.6%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_3</td>
<td align="right">53,233,920</td>
<td align="right">59,360,600</td>
<td align="right">11.5%</td>
</tr>
<tr>
<td align="left">_BINARY_SUBSCR_TUPLE_INT</td>
<td align="right">148,032,297</td>
<td align="right">164,864,885</td>
<td align="right">11.4%</td>
</tr>
<tr>
<td align="left">_ITER_NEXT_LIST</td>
<td align="right">1,216,976,767</td>
<td align="right">1,079,602,318</td>
<td align="right">-11.3%</td>
</tr>
<tr>
<td align="left">_GUARD_NOT_EXHAUSTED_LIST</td>
<td align="right">1,504,818,072</td>
<td align="right">1,349,063,751</td>
<td align="right">-10.4%</td>
</tr>
<tr>
<td align="left">_CHECK_VALIDITY</td>
<td align="right">17,941,355,399</td>
<td align="right">19,765,696,988</td>
<td align="right">10.2%</td>
</tr>
<tr>
<td align="left">_POP_TOP</td>
<td align="right">682,894,660</td>
<td align="right">751,355,520</td>
<td align="right">10.0%</td>
</tr>
<tr>
<td align="left">_SET_IP</td>
<td align="right">16,365,584,625</td>
<td align="right">17,956,060,099</td>
<td align="right">9.7%</td>
</tr>
<tr>
<td align="left">_ITER_CHECK_RANGE</td>
<td align="right">785,877,552</td>
<td align="right">709,982,005</td>
<td align="right">-9.7%</td>
</tr>
<tr>
<td align="left">_GUARD_TYPE_VERSION</td>
<td align="right">5,464,402,746</td>
<td align="right">5,991,902,891</td>
<td align="right">9.7%</td>
</tr>
<tr>
<td align="left">_STORE_FAST</td>
<td align="right">4,792,898,342</td>
<td align="right">5,253,930,925</td>
<td align="right">9.6%</td>
</tr>
<tr>
<td align="left">_GUARD_NOT_EXHAUSTED_RANGE</td>
<td align="right">784,519,792</td>
<td align="right">709,356,125</td>
<td align="right">-9.6%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST</td>
<td align="right">5,299,421,067</td>
<td align="right">5,805,098,607</td>
<td align="right">9.5%</td>
</tr>
<tr>
<td align="left">_ITER_NEXT_RANGE</td>
<td align="right">735,786,131</td>
<td align="right">666,267,134</td>
<td align="right">-9.4%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_0</td>
<td align="right">5,322,112,268</td>
<td align="right">5,784,678,744</td>
<td align="right">8.7%</td>
</tr>
<tr>
<td align="left">_CONTAINS_OP</td>
<td align="right">107,271,482</td>
<td align="right">116,591,490</td>
<td align="right">8.7%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right">89,236,167</td>
<td align="right">96,727,479</td>
<td align="right">8.4%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_FALSE_POP</td>
<td align="right">5,123,035,263</td>
<td align="right">5,537,740,951</td>
<td align="right">8.1%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_1</td>
<td align="right">550,177,138</td>
<td align="right">593,008,283</td>
<td align="right">7.8%</td>
</tr>
<tr>
<td align="left">_LOAD_CONST_INLINE_BORROW</td>
<td align="right">8,856,201,193</td>
<td align="right">9,542,129,587</td>
<td align="right">7.7%</td>
</tr>
<tr>
<td align="left">_BINARY_SUBSCR</td>
<td align="right">1,241,900,852</td>
<td align="right">1,337,446,577</td>
<td align="right">7.7%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_1</td>
<td align="right">6,485,149,611</td>
<td align="right">6,978,743,306</td>
<td align="right">7.6%</td>
</tr>
<tr>
<td align="left">_JUMP_TO_TOP</td>
<td align="right">2,096,880,281</td>
<td align="right">2,254,879,590</td>
<td align="right">7.5%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_NONE</td>
<td align="right">173,300,239</td>
<td align="right">186,071,058</td>
<td align="right">7.4%</td>
</tr>
<tr>
<td align="left">_COMPARE_OP</td>
<td align="right">105,806,358</td>
<td align="right">113,540,711</td>
<td align="right">7.3%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_TRUE_POP</td>
<td align="right">2,483,348,247</td>
<td align="right">2,664,130,300</td>
<td align="right">7.3%</td>
</tr>
<tr>
<td align="left">_CHECK_CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">81,660,503</td>
<td align="right">87,119,235</td>
<td align="right">6.7%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">81,599,983</td>
<td align="right">87,053,015</td>
<td align="right">6.7%</td>
</tr>
<tr>
<td align="left">_CALL_STR_1</td>
<td align="right">67,796,874</td>
<td align="right">72,247,876</td>
<td align="right">6.6%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_NOT_NONE_POP</td>
<td align="right">161,115,257</td>
<td align="right">171,492,141</td>
<td align="right">6.4%</td>
</tr>
<tr>
<td align="left">_GET_ITER</td>
<td align="right">245,124,544</td>
<td align="right">260,805,119</td>
<td align="right">6.4%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_1</td>
<td align="right">1,849,677,601</td>
<td align="right">1,963,414,494</td>
<td align="right">6.1%</td>
</tr>
<tr>
<td align="left">_EXIT_TRACE</td>
<td align="right">2,560,072,974</td>
<td align="right">2,707,739,971</td>
<td align="right">5.8%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_ADD_UNICODE</td>
<td align="right">22,881,513</td>
<td align="right">24,130,138</td>
<td align="right">5.5%</td>
</tr>
<tr>
<td align="left">_LIST_APPEND</td>
<td align="right">178,910,244</td>
<td align="right">188,496,676</td>
<td align="right">5.4%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_MULTIPLY_FLOAT</td>
<td align="right">1,192,924,540</td>
<td align="right">1,256,098,360</td>
<td align="right">5.3%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBTRACT_INT</td>
<td align="right">443,726,152</td>
<td align="right">465,208,862</td>
<td align="right">4.8%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_NONE_POP</td>
<td align="right">42,287,890</td>
<td align="right">44,298,407</td>
<td align="right">4.8%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR</td>
<td align="right">1,228,942,044</td>
<td align="right">1,285,405,168</td>
<td align="right">4.6%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_AND_CLEAR</td>
<td align="right">16,437,114</td>
<td align="right">17,187,711</td>
<td align="right">4.6%</td>
</tr>
<tr>
<td align="left">_BUILD_LIST</td>
<td align="right">245,405,157</td>
<td align="right">256,583,096</td>
<td align="right">4.6%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">819,551,425</td>
<td align="right">855,915,625</td>
<td align="right">4.4%</td>
</tr>
<tr>
<td align="left">_GUARD_BOTH_FLOAT</td>
<td align="right">1,640,102,229</td>
<td align="right">1,712,548,195</td>
<td align="right">4.4%</td>
</tr>
<tr>
<td align="left">_CHECK_ATTR_CLASS</td>
<td align="right">19,940,992</td>
<td align="right">19,077,498</td>
<td align="right">-4.3%</td>
</tr>
<tr>
<td align="left">_UNARY_INVERT</td>
<td align="right">12,537,420</td>
<td align="right">13,062,054</td>
<td align="right">4.2%</td>
</tr>
<tr>
<td align="left">_UNPACK_SEQUENCE_LIST</td>
<td align="right">77,463,760</td>
<td align="right">80,703,647</td>
<td align="right">4.2%</td>
</tr>
<tr>
<td align="left">_CHECK_ATTR_MODULE</td>
<td align="right">9,367,155</td>
<td align="right">9,755,496</td>
<td align="right">4.1%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_MODULE</td>
<td align="right">9,363,655</td>
<td align="right">9,751,556</td>
<td align="right">4.1%</td>
</tr>
<tr>
<td align="left">_BINARY_SUBSCR_LIST_INT</td>
<td align="right">1,083,263,972</td>
<td align="right">1,124,847,803</td>
<td align="right">3.8%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS</td>
<td align="right">9,760,213</td>
<td align="right">10,112,677</td>
<td align="right">3.6%</td>
</tr>
<tr>
<td align="left">_MAP_ADD</td>
<td align="right">20,588,202</td>
<td align="right">21,314,892</td>
<td align="right">3.5%</td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">183,792,197</td>
<td align="right">190,240,096</td>
<td align="right">3.5%</td>
</tr>
<tr>
<td align="left">_ITER_NEXT_TUPLE</td>
<td align="right">264,339,502</td>
<td align="right">255,113,962</td>
<td align="right">-3.5%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_CLASS_0</td>
<td align="right">18,778,668</td>
<td align="right">18,137,293</td>
<td align="right">-3.4%</td>
</tr>
<tr>
<td align="left">_BINARY_OP</td>
<td align="right">893,308,203</td>
<td align="right">921,938,447</td>
<td align="right">3.2%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_INSTANCE_VALUE_0</td>
<td align="right">2,024,295,614</td>
<td align="right">2,085,151,141</td>
<td align="right">3.0%</td>
</tr>
<tr>
<td align="left">_CHECK_MANAGED_OBJECT_HAS_VALUES</td>
<td align="right">2,030,748,480</td>
<td align="right">2,091,673,167</td>
<td align="right">3.0%</td>
</tr>
<tr>
<td align="left">_MAKE_FUNCTION</td>
<td align="right">60,392,677</td>
<td align="right">62,138,411</td>
<td align="right">2.9%</td>
</tr>
<tr>
<td align="left">_UNPACK_SEQUENCE</td>
<td align="right">2,863,740</td>
<td align="right">2,944,895</td>
<td align="right">2.8%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_2</td>
<td align="right">104,376,498</td>
<td align="right">107,247,916</td>
<td align="right">2.8%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_6</td>
<td align="right">1,248,019,259</td>
<td align="right">1,281,738,528</td>
<td align="right">2.7%</td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_CLASS</td>
<td align="right">58,211,009</td>
<td align="right">59,772,754</td>
<td align="right">2.7%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_SLOT_0</td>
<td align="right">683,999,798</td>
<td align="right">701,727,511</td>
<td align="right">2.6%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_ADD_FLOAT</td>
<td align="right">577,839,960</td>
<td align="right">592,539,140</td>
<td align="right">2.5%</td>
</tr>
<tr>
<td align="left">_STORE_ATTR</td>
<td align="right">54,035,536</td>
<td align="right">52,722,352</td>
<td align="right">-2.4%</td>
</tr>
<tr>
<td align="left">_GUARD_BOTH_INT</td>
<td align="right">3,162,328,728</td>
<td align="right">3,238,299,272</td>
<td align="right">2.4%</td>
</tr>
<tr>
<td align="left">_STORE_SUBSCR_LIST_INT</td>
<td align="right">478,927,182</td>
<td align="right">490,314,122</td>
<td align="right">2.4%</td>
</tr>
<tr>
<td align="left">_CALL_LEN</td>
<td align="right">197,311,691</td>
<td align="right">201,884,710</td>
<td align="right">2.3%</td>
</tr>
<tr>
<td align="left">_COMPARE_OP_INT</td>
<td align="right">942,485,396</td>
<td align="right">963,780,822</td>
<td align="right">2.3%</td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">221,587,950</td>
<td align="right">226,517,861</td>
<td align="right">2.2%</td>
</tr>
<tr>
<td align="left">_SWAP</td>
<td align="right">1,131,726,144</td>
<td align="right">1,155,585,858</td>
<td align="right">2.1%</td>
</tr>
<tr>
<td align="left">_GUARD_DORV_VALUES</td>
<td align="right">102,535,633</td>
<td align="right">104,611,557</td>
<td align="right">2.0%</td>
</tr>
<tr>
<td align="left">_STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">101,839,693</td>
<td align="right">103,875,137</td>
<td align="right">2.0%</td>
</tr>
<tr>
<td align="left">_COPY</td>
<td align="right">1,253,472,046</td>
<td align="right">1,278,281,421</td>
<td align="right">2.0%</td>
</tr>
<tr>
<td align="left">_LOAD_GLOBAL_BUILTINS</td>
<td align="right">6,604,196</td>
<td align="right">6,729,541</td>
<td align="right">1.9%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_0</td>
<td align="right">204,685,282</td>
<td align="right">208,552,178</td>
<td align="right">1.9%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_0</td>
<td align="right">392,982,516</td>
<td align="right">400,299,710</td>
<td align="right">1.9%</td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION</td>
<td align="right">1,297,918,483</td>
<td align="right">1,319,772,390</td>
<td align="right">1.7%</td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_FAST_WITH_KEYWORDS</td>
<td align="right">154,143,409</td>
<td align="right">156,613,893</td>
<td align="right">1.6%</td>
</tr>
<tr>
<td align="left">_BINARY_SLICE</td>
<td align="right">119,377,836</td>
<td align="right">121,288,912</td>
<td align="right">1.6%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_LIST</td>
<td align="right">61,544,526</td>
<td align="right">60,598,905</td>
<td align="right">-1.5%</td>
</tr>
<tr>
<td align="left">_CALL_INTRINSIC_1</td>
<td align="right">96,034,895</td>
<td align="right">97,447,036</td>
<td align="right">1.5%</td>
</tr>
<tr>
<td align="left">_LIST_EXTEND</td>
<td align="right">96,960,655</td>
<td align="right">98,372,796</td>
<td align="right">1.5%</td>
</tr>
<tr>
<td align="left">_TO_BOOL</td>
<td align="right">249,153,612</td>
<td align="right">252,702,617</td>
<td align="right">1.4%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_ADD_INT</td>
<td align="right">2,491,444,411</td>
<td align="right">2,526,493,410</td>
<td align="right">1.4%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_INSTANCE_VALUE_1</td>
<td align="right">6,299,066</td>
<td align="right">6,380,245</td>
<td align="right">1.3%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_7</td>
<td align="right">1,466,925,077</td>
<td align="right">1,485,388,668</td>
<td align="right">1.3%</td>
</tr>
<tr>
<td align="left">_STORE_GLOBAL</td>
<td align="right">1,260,560</td>
<td align="right">1,276,320</td>
<td align="right">1.3%</td>
</tr>
<tr>
<td align="left">_STORE_SUBSCR_DICT</td>
<td align="right">143,987,697</td>
<td align="right">145,559,399</td>
<td align="right">1.1%</td>
</tr>
<tr>
<td align="left">_GUARD_BOTH_UNICODE</td>
<td align="right">967,075,409</td>
<td align="right">976,827,892</td>
<td align="right">1.0%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_INT</td>
<td align="right">196,462,531</td>
<td align="right">198,429,584</td>
<td align="right">1.0%</td>
</tr>
<tr>
<td align="left">_COPY_FREE_VARS</td>
<td align="right">48,217,311</td>
<td align="right">48,647,533</td>
<td align="right">0.9%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_7</td>
<td align="right">3,381,385,081</td>
<td align="right">3,406,647,811</td>
<td align="right">0.7%</td>
</tr>
<tr>
<td align="left">_SET_FUNCTION_ATTRIBUTE</td>
<td align="right">46,788,824</td>
<td align="right">47,076,587</td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">_LOAD_GLOBAL</td>
<td align="right">192,425,813</td>
<td align="right">191,308,733</td>
<td align="right">-0.6%</td>
</tr>
<tr>
<td align="left">_COMPARE_OP_STR</td>
<td align="right">1,826,792,992</td>
<td align="right">1,836,027,391</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_MULTIPLY_INT</td>
<td align="right">184,995,238</td>
<td align="right">185,838,662</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">_STORE_SUBSCR</td>
<td align="right">317,466,612</td>
<td align="right">318,901,451</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">_UNARY_NOT</td>
<td align="right">62,208,047</td>
<td align="right">62,430,263</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">_STORE_ATTR_SLOT</td>
<td align="right">128,435,081</td>
<td align="right">128,050,762</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">_REPLACE_WITH_TRUE</td>
<td align="right">27,646,351</td>
<td align="right">27,715,385</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">_UNARY_NEGATIVE</td>
<td align="right">48,761,828</td>
<td align="right">48,821,410</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBTRACT_FLOAT</td>
<td align="right">393,785,140</td>
<td align="right">394,224,040</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">_STORE_NAME</td>
<td align="right">545,860</td>
<td align="right">545,980</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_BINARY_SUBSCR_STR_INT</td>
<td align="right">1,209,309,464</td>
<td align="right">1,209,468,020</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_CHECK_ATTR_METHOD_LAZY_DICT</td>
<td align="right">57,535,680</td>
<td align="right">57,536,640</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_METHOD_LAZY_DICT</td>
<td align="right">57,535,680</td>
<td align="right">57,536,640</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_COMPARE_OP_FLOAT</td>
<td align="right">70,081,863</td>
<td align="right">70,082,913</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_STORE_SLICE</td>
<td align="right">149,874,320</td>
<td align="right">149,874,640</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_BUILD_SLICE</td>
<td align="right">139,785,940</td>
<td align="right">139,786,180</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_GET_ANEXT</td>
<td align="right">125,514,720</td>
<td align="right">125,514,720</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_CALL_TUPLE_1</td>
<td align="right">586,240</td>
<td align="right">586,240</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_GET_YIELD_FROM_ITER</td>
<td align="right">185,480</td>
<td align="right">185,480</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_LOAD_SUPER_ATTR_METHOD</td>
<td align="right">97,617</td>
<td align="right">97,617</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_CLASS_1</td>
<td align="right">3,840</td>
<td align="right">3,840</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_FORMAT_WITH_SPEC</td>
<td align="right">680</td>
<td align="right">680</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_UNPACK_EX</td>
<td align="right">104</td>
<td align="right">104</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_SLOT_1</td>
<td align="right"></td>
<td align="right">3,993,400</td>
<td align="right"></td>
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
<td align="left">CALL_FUNCTION_EX</td>
<td align="right">33,120</td>
<td align="right">3,726,198</td>
<td align="right">11,150.6%</td>
</tr>
<tr>
<td align="left">LOAD_NAME</td>
<td align="right">2,340</td>
<td align="right">11,160</td>
<td align="right">376.9%</td>
</tr>
<tr>
<td align="left">IMPORT_NAME</td>
<td align="right">4,383</td>
<td align="right">7,503</td>
<td align="right">71.2%</td>
</tr>
<tr>
<td align="left">BUILD_SET</td>
<td align="right">467</td>
<td align="right">732</td>
<td align="right">56.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_PROPERTY</td>
<td align="right">13,494</td>
<td align="right">19,071</td>
<td align="right">41.3%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">10,470,275</td>
<td align="right">14,495,627</td>
<td align="right">38.4%</td>
</tr>
<tr>
<td align="left">CALL_LIST_APPEND</td>
<td align="right">6,920</td>
<td align="right">9,359</td>
<td align="right">35.2%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_WITH_HINT</td>
<td align="right">200</td>
<td align="right">260</td>
<td align="right">30.0%</td>
</tr>
<tr>
<td align="left">YIELD_VALUE</td>
<td align="right">13,696,614</td>
<td align="right">17,657,914</td>
<td align="right">28.9%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_GETITEM</td>
<td align="right">2,860</td>
<td align="right">3,520</td>
<td align="right">23.1%</td>
</tr>
<tr>
<td align="left">BINARY_OP_INPLACE_ADD_UNICODE</td>
<td align="right">583</td>
<td align="right">683</td>
<td align="right">17.2%</td>
</tr>
<tr>
<td align="left">RETURN_GENERATOR</td>
<td align="right">4,057,872</td>
<td align="right">4,663,702</td>
<td align="right">14.9%</td>
</tr>
<tr>
<td align="left">CALL_PY_WITH_DEFAULTS</td>
<td align="right">90,949</td>
<td align="right">100,922</td>
<td align="right">11.0%</td>
</tr>
<tr>
<td align="left">FOR_ITER_GEN</td>
<td align="right">93,426</td>
<td align="right">85,049</td>
<td align="right">-9.0%</td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">2,546,263</td>
<td align="right">2,754,949</td>
<td align="right">8.2%</td>
</tr>
<tr>
<td align="left">CALL_KW</td>
<td align="right">2,138,676</td>
<td align="right">2,226,128</td>
<td align="right">4.1%</td>
</tr>
<tr>
<td align="left">BEFORE_WITH</td>
<td align="right">3,480</td>
<td align="right">3,520</td>
<td align="right">1.1%</td>
</tr>
<tr>
<td align="left">CALL_ALLOC_AND_ENTER_INIT</td>
<td align="right">74,205</td>
<td align="right">74,783</td>
<td align="right">0.8%</td>
</tr>
<tr>
<td align="left">SEND</td>
<td align="right">3,928,200</td>
<td align="right">3,928,200</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">SEND_GEN</td>
<td align="right">80</td>
<td align="right">80</td>
<td align="right">0.0%</td>
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
<td align="right">2,020</td>
<td align="right">2,020</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

---
Stats gathered on: 2024-04-03
