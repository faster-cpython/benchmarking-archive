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
<td align="right">301,569,271</td>
<td align="right">11,392,865</td>
<td align="right">-96.2%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">655,586,896</td>
<td align="right">26,722,922</td>
<td align="right">-95.9%</td>
</tr>
<tr>
<td align="left">SET_ADD</td>
<td align="right">966,863</td>
<td align="right">241,069</td>
<td align="right">-75.1%</td>
</tr>
<tr>
<td align="left">FOR_ITER_RANGE</td>
<td align="right">107,578,213</td>
<td align="right">30,120,087</td>
<td align="right">-72.0%</td>
</tr>
<tr>
<td align="left">STORE_FAST_LOAD_FAST</td>
<td align="right">43,200,722</td>
<td align="right">15,903,985</td>
<td align="right">-63.2%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST</td>
<td align="right">527,559,880</td>
<td align="right">284,766,445</td>
<td align="right">-46.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_INPLACE_ADD_UNICODE</td>
<td align="right">6,289,328</td>
<td align="right">3,476,348</td>
<td align="right">-44.7%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP_SET</td>
<td align="right">466,421,558</td>
<td align="right">261,037,526</td>
<td align="right">-44.0%</td>
</tr>
<tr>
<td align="left">CALL_TYPE_1</td>
<td align="right">243,254,294</td>
<td align="right">146,477,609</td>
<td align="right">-39.8%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">124,423,886</td>
<td align="right">75,428,084</td>
<td align="right">-39.4%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP_DICT</td>
<td align="right">178,091,476</td>
<td align="right">112,133,689</td>
<td align="right">-37.0%</td>
</tr>
<tr>
<td align="left">CONVERT_VALUE</td>
<td align="right">138,893,720</td>
<td align="right">87,993,367</td>
<td align="right">-36.6%</td>
</tr>
<tr>
<td align="left">BUILD_CONST_KEY_MAP</td>
<td align="right">13,478,609</td>
<td align="right">8,609,814</td>
<td align="right">-36.1%</td>
</tr>
<tr>
<td align="left">FORMAT_SIMPLE</td>
<td align="right">149,234,487</td>
<td align="right">98,302,479</td>
<td align="right">-34.1%</td>
</tr>
<tr>
<td align="left">BUILD_STRING</td>
<td align="right">75,884,940</td>
<td align="right">50,978,082</td>
<td align="right">-32.8%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TUPLE</td>
<td align="right">316,196,832</td>
<td align="right">219,414,646</td>
<td align="right">-30.6%</td>
</tr>
<tr>
<td align="left">BINARY_OP_MULTIPLY_FLOAT</td>
<td align="right">210,107,814</td>
<td align="right">146,549,839</td>
<td align="right">-30.3%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_LIST</td>
<td align="right">12,244,415</td>
<td align="right">9,010,112</td>
<td align="right">-26.4%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">342,742,795</td>
<td align="right">260,036,310</td>
<td align="right">-24.1%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR</td>
<td align="right">416,313,022</td>
<td align="right">324,489,700</td>
<td align="right">-22.1%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">2,969,553,357</td>
<td align="right">2,364,622,111</td>
<td align="right">-20.4%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_DICT</td>
<td align="right">581,014,610</td>
<td align="right">463,881,572</td>
<td align="right">-20.2%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_STR_INT</td>
<td align="right">460,281,749</td>
<td align="right">377,277,853</td>
<td align="right">-18.0%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">6,701,794,879</td>
<td align="right">5,535,651,412</td>
<td align="right">-17.4%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_FLOAT</td>
<td align="right">87,691,788</td>
<td align="right">72,681,459</td>
<td align="right">-17.1%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_INT</td>
<td align="right">678,460,878</td>
<td align="right">562,705,610</td>
<td align="right">-17.1%</td>
</tr>
<tr>
<td align="left">IS_OP</td>
<td align="right">501,618,880</td>
<td align="right">419,661,005</td>
<td align="right">-16.3%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE</td>
<td align="right">541,320</td>
<td align="right">453,703</td>
<td align="right">-16.2%</td>
</tr>
<tr>
<td align="left">LOAD_NAME</td>
<td align="right">14,134,707</td>
<td align="right">12,134,387</td>
<td align="right">-14.2%</td>
</tr>
<tr>
<td align="left">STORE_FAST_STORE_FAST</td>
<td align="right">449,621,380</td>
<td align="right">387,635,041</td>
<td align="right">-13.8%</td>
</tr>
<tr>
<td align="left">FOR_ITER_GEN</td>
<td align="right">239,700,672</td>
<td align="right">207,092,235</td>
<td align="right">-13.6%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">5,594,041,748</td>
<td align="right">4,833,337,718</td>
<td align="right">-13.6%</td>
</tr>
<tr>
<td align="left">UNARY_INVERT</td>
<td align="right">1,871,111</td>
<td align="right">2,112,579</td>
<td align="right">12.9%</td>
</tr>
<tr>
<td align="left">LIST_APPEND</td>
<td align="right">74,296,592</td>
<td align="right">64,952,450</td>
<td align="right">-12.6%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_TUPLE_INT</td>
<td align="right">221,091,862</td>
<td align="right">193,598,588</td>
<td align="right">-12.4%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">564,426,914</td>
<td align="right">494,440,045</td>
<td align="right">-12.4%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">5,411,761,512</td>
<td align="right">4,756,616,251</td>
<td align="right">-12.1%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_O</td>
<td align="right">647,713,675</td>
<td align="right">571,910,713</td>
<td align="right">-11.7%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">734,975,820</td>
<td align="right">649,163,590</td>
<td align="right">-11.7%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">146,000,025</td>
<td align="right">129,232,101</td>
<td align="right">-11.5%</td>
</tr>
<tr>
<td align="left">DICT_MERGE</td>
<td align="right">41,297,766</td>
<td align="right">36,605,009</td>
<td align="right">-11.4%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">1,157,539,262</td>
<td align="right">1,283,403,920</td>
<td align="right">10.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">1,721,931,913</td>
<td align="right">1,538,566,161</td>
<td align="right">-10.6%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_LIST_INT</td>
<td align="right">107,949,050</td>
<td align="right">96,560,605</td>
<td align="right">-10.5%</td>
</tr>
<tr>
<td align="left">CALL_ISINSTANCE</td>
<td align="right">829,275,741</td>
<td align="right">746,202,874</td>
<td align="right">-10.0%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">113,982,921</td>
<td align="right">102,747,789</td>
<td align="right">-9.9%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">6,233,716,374</td>
<td align="right">5,648,046,421</td>
<td align="right">-9.4%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_LIST_INT</td>
<td align="right">454,075,722</td>
<td align="right">412,637,986</td>
<td align="right">-9.1%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">642,102,731</td>
<td align="right">586,547,702</td>
<td align="right">-8.7%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">2,903,844,490</td>
<td align="right">2,653,817,514</td>
<td align="right">-8.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">24,481,854,491</td>
<td align="right">22,502,549,869</td>
<td align="right">-8.1%</td>
</tr>
<tr>
<td align="left">PUSH_NULL</td>
<td align="right">1,214,570,044</td>
<td align="right">1,117,929,621</td>
<td align="right">-8.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">3,545,622,655</td>
<td align="right">3,272,224,736</td>
<td align="right">-7.7%</td>
</tr>
<tr>
<td align="left">BUILD_MAP</td>
<td align="right">127,289,163</td>
<td align="right">117,855,625</td>
<td align="right">-7.4%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">2,849,291,397</td>
<td align="right">2,642,719,808</td>
<td align="right">-7.2%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">255,515,905</td>
<td align="right">240,984,629</td>
<td align="right">-5.7%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_INT</td>
<td align="right">403,648,528</td>
<td align="right">380,931,681</td>
<td align="right">-5.6%</td>
</tr>
<tr>
<td align="left">TO_BOOL_STR</td>
<td align="right">77,667,932</td>
<td align="right">73,706,272</td>
<td align="right">-5.1%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">153,744,764</td>
<td align="right">146,140,248</td>
<td align="right">-4.9%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">2,759,553,465</td>
<td align="right">2,894,184,851</td>
<td align="right">4.9%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">123,855,599</td>
<td align="right">117,852,861</td>
<td align="right">-4.8%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">469,390,927</td>
<td align="right">447,190,651</td>
<td align="right">-4.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">865,719,547</td>
<td align="right">827,562,730</td>
<td align="right">-4.4%</td>
</tr>
<tr>
<td align="left">LIST_EXTEND</td>
<td align="right">27,475,985</td>
<td align="right">26,288,937</td>
<td align="right">-4.3%</td>
</tr>
<tr>
<td align="left">CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">198,072,246</td>
<td align="right">189,891,883</td>
<td align="right">-4.1%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">4,254,191,524</td>
<td align="right">4,079,528,901</td>
<td align="right">-4.1%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST_WITH_KEYWORDS</td>
<td align="right">28,924,268</td>
<td align="right">27,784,217</td>
<td align="right">-3.9%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">610,357,178</td>
<td align="right">587,363,476</td>
<td align="right">-3.8%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">6,872,929,119</td>
<td align="right">6,624,106,717</td>
<td align="right">-3.6%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST_WITH_KEYWORDS</td>
<td align="right">110,238,497</td>
<td align="right">106,335,011</td>
<td align="right">-3.5%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">3,649,052,521</td>
<td align="right">3,520,939,573</td>
<td align="right">-3.5%</td>
</tr>
<tr>
<td align="left">TO_BOOL_LIST</td>
<td align="right">122,162,863</td>
<td align="right">117,881,106</td>
<td align="right">-3.5%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_STR</td>
<td align="right">336,892,877</td>
<td align="right">326,208,534</td>
<td align="right">-3.2%</td>
</tr>
<tr>
<td align="left">CALL_STR_1</td>
<td align="right">41,002,170</td>
<td align="right">39,821,975</td>
<td align="right">-2.9%</td>
</tr>
<tr>
<td align="left">BEFORE_WITH</td>
<td align="right">9,827,117</td>
<td align="right">10,107,142</td>
<td align="right">2.8%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NONE</td>
<td align="right">399,465,450</td>
<td align="right">388,799,630</td>
<td align="right">-2.7%</td>
</tr>
<tr>
<td align="left">BUILD_LIST</td>
<td align="right">222,863,050</td>
<td align="right">217,074,501</td>
<td align="right">-2.6%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">1,339,256,956</td>
<td align="right">1,305,894,597</td>
<td align="right">-2.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_LAZY_DICT</td>
<td align="right">250,779,173</td>
<td align="right">244,543,038</td>
<td align="right">-2.5%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">645,907,841</td>
<td align="right">630,478,296</td>
<td align="right">-2.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_MODULE</td>
<td align="right">539,635,335</td>
<td align="right">527,301,105</td>
<td align="right">-2.3%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">263,106,085</td>
<td align="right">257,165,435</td>
<td align="right">-2.3%</td>
</tr>
<tr>
<td align="left">CALL_LEN</td>
<td align="right">309,278,340</td>
<td align="right">303,048,372</td>
<td align="right">-2.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">4,214,999,535</td>
<td align="right">4,133,603,546</td>
<td align="right">-1.9%</td>
</tr>
<tr>
<td align="left">MAP_ADD</td>
<td align="right">39,903,906</td>
<td align="right">39,181,783</td>
<td align="right">-1.8%</td>
</tr>
<tr>
<td align="left">MAKE_FUNCTION</td>
<td align="right">95,292,605</td>
<td align="right">93,618,535</td>
<td align="right">-1.8%</td>
</tr>
<tr>
<td align="left">YIELD_VALUE</td>
<td align="right">1,405,650,195</td>
<td align="right">1,381,287,110</td>
<td align="right">-1.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right">122,059,350</td>
<td align="right">120,001,150</td>
<td align="right">-1.7%</td>
</tr>
<tr>
<td align="left">TO_BOOL_INT</td>
<td align="right">144,217,311</td>
<td align="right">141,970,754</td>
<td align="right">-1.6%</td>
</tr>
<tr>
<td align="left">NOP</td>
<td align="right">985,066,041</td>
<td align="right">970,253,719</td>
<td align="right">-1.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_CLASS</td>
<td align="right">161,478,797</td>
<td align="right">159,269,313</td>
<td align="right">-1.4%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT</td>
<td align="right">1,234,239,372</td>
<td align="right">1,217,553,914</td>
<td align="right">-1.4%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_GETITEM</td>
<td align="right">62,401,177</td>
<td align="right">61,565,260</td>
<td align="right">-1.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">1,746,502,293</td>
<td align="right">1,723,216,697</td>
<td align="right">-1.3%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_DICT</td>
<td align="right">151,922,051</td>
<td align="right">150,022,124</td>
<td align="right">-1.3%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR</td>
<td align="right">131,065,010</td>
<td align="right">129,441,434</td>
<td align="right">-1.2%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">375,490,344</td>
<td align="right">370,944,511</td>
<td align="right">-1.2%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_CLASS</td>
<td align="right">151,986,518</td>
<td align="right">150,161,842</td>
<td align="right">-1.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_CHECK</td>
<td align="right">11,666,746</td>
<td align="right">11,800,777</td>
<td align="right">1.1%</td>
</tr>
<tr>
<td align="left">MAKE_CELL</td>
<td align="right">104,849,366</td>
<td align="right">103,759,873</td>
<td align="right">-1.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL_ALWAYS_TRUE</td>
<td align="right">184,176,325</td>
<td align="right">182,383,164</td>
<td align="right">-1.0%</td>
</tr>
<tr>
<td align="left">STORE_DEREF</td>
<td align="right">95,289,935</td>
<td align="right">94,370,150</td>
<td align="right">-1.0%</td>
</tr>
<tr>
<td align="left">CALL_INTRINSIC_1</td>
<td align="right">152,975,103</td>
<td align="right">151,579,251</td>
<td align="right">-0.9%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_UNICODE</td>
<td align="right">75,955,265</td>
<td align="right">75,273,195</td>
<td align="right">-0.9%</td>
</tr>
<tr>
<td align="left">BINARY_SLICE</td>
<td align="right">228,113,311</td>
<td align="right">226,106,071</td>
<td align="right">-0.9%</td>
</tr>
<tr>
<td align="left">DICT_UPDATE</td>
<td align="right">73,061</td>
<td align="right">73,610</td>
<td align="right">0.8%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NOT_NONE</td>
<td align="right">674,982,804</td>
<td align="right">670,308,944</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">END_FOR</td>
<td align="right">83,008,844</td>
<td align="right">82,521,485</td>
<td align="right">-0.6%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR_METHOD</td>
<td align="right">126,581,860</td>
<td align="right">127,313,275</td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_PROPERTY</td>
<td align="right">82,053,972</td>
<td align="right">81,609,745</td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">BINARY_OP_MULTIPLY_INT</td>
<td align="right">164,919,348</td>
<td align="right">164,098,133</td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">INTERPRETER_EXIT</td>
<td align="right">2,307,035,679</td>
<td align="right">2,317,731,639</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR_ATTR</td>
<td align="right">7,706,507</td>
<td align="right">7,740,929</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_FLOAT</td>
<td align="right">77,385,661</td>
<td align="right">77,046,347</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_AND_CLEAR</td>
<td align="right">70,534,047</td>
<td align="right">70,226,234</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_O</td>
<td align="right">398,564,290</td>
<td align="right">400,031,156</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_WITH_HINT</td>
<td align="right">377,212,260</td>
<td align="right">378,563,585</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">COPY_FREE_VARS</td>
<td align="right">315,763,466</td>
<td align="right">314,708,545</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">CALL_PY_WITH_DEFAULTS</td>
<td align="right">213,800,775</td>
<td align="right">213,099,509</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">CALL_KW</td>
<td align="right">270,042,541</td>
<td align="right">269,205,789</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">JUMP_FORWARD</td>
<td align="right">447,956,843</td>
<td align="right">446,708,496</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_NO_DICT</td>
<td align="right">67,111,483</td>
<td align="right">66,930,505</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">SET_FUNCTION_ATTRIBUTE</td>
<td align="right">84,975,204</td>
<td align="right">84,753,513</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">STORE_GLOBAL</td>
<td align="right">6,944,680</td>
<td align="right">6,929,900</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">TO_BOOL_NONE</td>
<td align="right">508,883,310</td>
<td align="right">507,831,167</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">DELETE_FAST</td>
<td align="right">2,236,811</td>
<td align="right">2,240,556</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">WITH_EXCEPT_START</td>
<td align="right">235,001</td>
<td align="right">235,328</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">1,195,105,106</td>
<td align="right">1,193,546,088</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">1,146,799,073</td>
<td align="right">1,145,352,348</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">DELETE_SUBSCR</td>
<td align="right">176,504,753</td>
<td align="right">176,288,280</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">CALL_TUPLE_1</td>
<td align="right">28,271,899</td>
<td align="right">28,304,977</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">UNARY_NOT</td>
<td align="right">28,338,162</td>
<td align="right">28,368,911</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_SLOT</td>
<td align="right">1,507,466,430</td>
<td align="right">1,509,084,324</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">77,713,918</td>
<td align="right">77,645,793</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">DELETE_ATTR</td>
<td align="right">6,769,042</td>
<td align="right">6,773,930</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">UNARY_NEGATIVE</td>
<td align="right">146,012,265</td>
<td align="right">145,909,431</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">PUSH_EXC_INFO</td>
<td align="right">25,065,181</td>
<td align="right">25,080,344</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">POP_EXCEPT</td>
<td align="right">25,065,038</td>
<td align="right">25,080,198</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">CHECK_EXC_MATCH</td>
<td align="right">24,577,557</td>
<td align="right">24,592,416</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">342,817</td>
<td align="right">342,964</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">INSTRUMENTED_JUMP_BACKWARD</td>
<td align="right">10,004</td>
<td align="right">10,000</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">INSTRUMENTED_FOR_ITER</td>
<td align="right">11,364</td>
<td align="right">11,360</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">CALL_LIST_APPEND</td>
<td align="right">339,635,345</td>
<td align="right">339,741,845</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">IMPORT_NAME</td>
<td align="right">12,483,865</td>
<td align="right">12,487,582</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">INSTRUMENTED_POP_JUMP_IF_TRUE</td>
<td align="right">13,444</td>
<td align="right">13,440</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR</td>
<td align="right">23,802</td>
<td align="right">23,809</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">IMPORT_FROM</td>
<td align="right">13,155,117</td>
<td align="right">13,158,818</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">RERAISE</td>
<td align="right">3,992,517</td>
<td align="right">3,993,479</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_FUNCTION_EX</td>
<td align="right">192,706,629</td>
<td align="right">192,746,524</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">RETURN_GENERATOR</td>
<td align="right">502,837,818</td>
<td align="right">502,760,906</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">BUILD_SET</td>
<td align="right">2,389,012</td>
<td align="right">2,388,830</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_FLOAT</td>
<td align="right">181,067,866</td>
<td align="right">181,077,913</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">2,059,074,414</td>
<td align="right">2,058,974,170</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">STORE_SLICE</td>
<td align="right">12,601,336</td>
<td align="right">12,601,885</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">EXIT_INIT_CHECK</td>
<td align="right">95,006,420</td>
<td align="right">95,009,624</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">20,797,086</td>
<td align="right">20,797,775</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_ALLOC_AND_ENTER_INIT</td>
<td align="right">97,294,302</td>
<td align="right">97,297,506</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">RAISE_VARARGS</td>
<td align="right">6,196,102</td>
<td align="right">6,196,285</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD_NO_INTERRUPT</td>
<td align="right">556,718,169</td>
<td align="right">556,732,909</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">GET_AWAITABLE</td>
<td align="right">229,793,719</td>
<td align="right">229,797,695</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BUILD_SLICE</td>
<td align="right">72,065,122</td>
<td align="right">72,065,996</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">END_SEND</td>
<td align="right">402,761,394</td>
<td align="right">402,765,371</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">SEND</td>
<td align="right">173,952,622</td>
<td align="right">173,954,218</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">SEND_GEN</td>
<td align="right">787,182,861</td>
<td align="right">787,188,253</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_WITH_HINT</td>
<td align="right">64,674,340</td>
<td align="right">64,674,488</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">GET_YIELD_FROM_ITER</td>
<td align="right">47,476,919</td>
<td align="right">47,476,936</td>
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
<td align="right">160,100</td>
<td align="right">160,100</td>
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
<td align="left">FORMAT_WITH_SPEC</td>
<td align="right">1,760</td>
<td align="right">1,760</td>
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
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">639,369,647</td>
<td align="right">8.5%</td>
<td align="right">616,386,911</td>
<td align="right">8.2%</td>
<td align="right">-3.6%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">6,876,719,168</td>
<td align="right">91.5%</td>
<td align="right">6,874,301,604</td>
<td align="right">91.7%</td>
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
<td align="right">30,888,242</td>
<td align="right">0.4%</td>
<td align="right">30,888,224</td>
<td align="right">0.4%</td>
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
<td align="right">1,239,870</td>
<td align="right">66.1%</td>
<td align="right">1,228,699</td>
<td align="right">65.9%</td>
<td align="right">-0.9%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">635,903</td>
<td align="right">33.9%</td>
<td align="right">636,090</td>
<td align="right">34.1%</td>
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
<td align="left">xor</td>
<td align="right">9,882</td>
<td align="right">0.8%</td>
<td align="right">8,727</td>
<td align="right">0.7%</td>
<td align="right">-11.7%</td>
</tr>
<tr>
<td align="left">rshift</td>
<td align="right">9,991</td>
<td align="right">0.8%</td>
<td align="right">8,856</td>
<td align="right">0.7%</td>
<td align="right">-11.4%</td>
</tr>
<tr>
<td align="left">and int</td>
<td align="right">40,916</td>
<td align="right">3.3%</td>
<td align="right">37,103</td>
<td align="right">3.0%</td>
<td align="right">-9.3%</td>
</tr>
<tr>
<td align="left">true divide different types</td>
<td align="right">11,622</td>
<td align="right">0.9%</td>
<td align="right">10,832</td>
<td align="right">0.9%</td>
<td align="right">-6.8%</td>
</tr>
<tr>
<td align="left">or</td>
<td align="right">17,370</td>
<td align="right">1.4%</td>
<td align="right">17,019</td>
<td align="right">1.4%</td>
<td align="right">-2.0%</td>
</tr>
<tr>
<td align="left">lshift</td>
<td align="right">5,824</td>
<td align="right">0.5%</td>
<td align="right">5,713</td>
<td align="right">0.5%</td>
<td align="right">-1.9%</td>
</tr>
<tr>
<td align="left">true divide float</td>
<td align="right">5,762</td>
<td align="right">0.5%</td>
<td align="right">5,667</td>
<td align="right">0.5%</td>
<td align="right">-1.6%</td>
</tr>
<tr>
<td align="left">add different types</td>
<td align="right">78,740</td>
<td align="right">6.4%</td>
<td align="right">77,464</td>
<td align="right">6.3%</td>
<td align="right">-1.6%</td>
</tr>
<tr>
<td align="left">subtract other</td>
<td align="right">12,554</td>
<td align="right">1.0%</td>
<td align="right">12,354</td>
<td align="right">1.0%</td>
<td align="right">-1.6%</td>
</tr>
<tr>
<td align="left">remainder</td>
<td align="right">53,239</td>
<td align="right">4.3%</td>
<td align="right">52,474</td>
<td align="right">4.3%</td>
<td align="right">-1.4%</td>
</tr>
<tr>
<td align="left">power</td>
<td align="right">5,714</td>
<td align="right">0.5%</td>
<td align="right">5,749</td>
<td align="right">0.5%</td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">add other</td>
<td align="right">65,852</td>
<td align="right">5.3%</td>
<td align="right">65,486</td>
<td align="right">5.3%</td>
<td align="right">-0.6%</td>
</tr>
<tr>
<td align="left">floor divide</td>
<td align="right">32,608</td>
<td align="right">2.6%</td>
<td align="right">32,448</td>
<td align="right">2.6%</td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">multiply different types</td>
<td align="right">94,212</td>
<td align="right">7.6%</td>
<td align="right">94,021</td>
<td align="right">7.7%</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">and other</td>
<td align="right">2,038</td>
<td align="right">0.2%</td>
<td align="right">2,034</td>
<td align="right">0.2%</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">subtract different types</td>
<td align="right">784,187</td>
<td align="right">63.2%</td>
<td align="right">783,393</td>
<td align="right">63.8%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">multiply other</td>
<td align="right">5,220</td>
<td align="right">0.4%</td>
<td align="right">5,220</td>
<td align="right">0.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">true divide other</td>
<td align="right">3,520</td>
<td align="right">0.3%</td>
<td align="right">3,520</td>
<td align="right">0.3%</td>
<td align="right">0.0%</td>
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
<td align="right">420,827,620</td>
<td align="right">8.6%</td>
<td align="right">329,029,688</td>
<td align="right">6.9%</td>
<td align="right">-21.8%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">4,447,452,721</td>
<td align="right">91.3%</td>
<td align="right">4,435,795,385</td>
<td align="right">93.1%</td>
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
<td align="right">4,900,819</td>
<td align="right">0.1%</td>
<td align="right">4,900,640</td>
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
<td align="right">184,289</td>
<td align="right">47.7%</td>
<td align="right">158,713</td>
<td align="right">44.0%</td>
<td align="right">-13.9%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">201,932</td>
<td align="right">52.3%</td>
<td align="right">201,939</td>
<td align="right">56.0%</td>
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
<td align="right">56,269</td>
<td align="right">30.5%</td>
<td align="right">40,026</td>
<td align="right">25.2%</td>
<td align="right">-28.9%</td>
</tr>
<tr>
<td align="left">out of range</td>
<td align="right">76,980</td>
<td align="right">41.8%</td>
<td align="right">68,980</td>
<td align="right">43.5%</td>
<td align="right">-10.4%</td>
</tr>
<tr>
<td align="left">array int</td>
<td align="right">16,820</td>
<td align="right">9.1%</td>
<td align="right">15,880</td>
<td align="right">10.0%</td>
<td align="right">-5.6%</td>
</tr>
<tr>
<td align="left">tuple slice</td>
<td align="right">182</td>
<td align="right">0.1%</td>
<td align="right">187</td>
<td align="right">0.1%</td>
<td align="right">2.7%</td>
</tr>
<tr>
<td align="left">buffer int</td>
<td align="right">22,862</td>
<td align="right">12.4%</td>
<td align="right">22,483</td>
<td align="right">14.2%</td>
<td align="right">-1.7%</td>
</tr>
<tr>
<td align="left">code complex parameters</td>
<td align="right">5,036</td>
<td align="right">2.7%</td>
<td align="right">5,017</td>
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
<td align="right">760</td>
<td align="right">0.4%</td>
<td align="right">760</td>
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
<td align="right">33,100</td>
<td align="right">0.0%</td>
<td align="right">28,380</td>
<td align="right">0.0%</td>
<td align="right">-14.3%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">253,830,792</td>
<td align="right">1.9%</td>
<td align="right">251,344,388</td>
<td align="right">1.9%</td>
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
<td align="right">1,442,550,038</td>
<td align="right">10.7%</td>
<td align="right">1,438,550,239</td>
<td align="right">10.7%</td>
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
<td align="right">12,066,868,593</td>
<td align="right">89.3%</td>
<td align="right">12,054,990,785</td>
<td align="right">89.3%</td>
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
<td align="left">Success</td>
<td align="right">5,418,919</td>
<td align="right">84.9%</td>
<td align="right">5,372,029</td>
<td align="right">84.7%</td>
<td align="right">-0.9%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">966,941</td>
<td align="right">15.1%</td>
<td align="right">968,208</td>
<td align="right">15.3%</td>
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
<td align="left">cmethod</td>
<td align="right">14,100</td>
<td align="right">1.5%</td>
<td align="right">13,620</td>
<td align="right">1.4%</td>
<td align="right">-3.4%</td>
</tr>
<tr>
<td align="left">bound method</td>
<td align="right">11,968</td>
<td align="right">1.2%</td>
<td align="right">12,183</td>
<td align="right">1.3%</td>
<td align="right">1.8%</td>
</tr>
<tr>
<td align="left">class mutable</td>
<td align="right">24,148</td>
<td align="right">2.5%</td>
<td align="right">23,818</td>
<td align="right">2.5%</td>
<td align="right">-1.4%</td>
</tr>
<tr>
<td align="left">method wrapper</td>
<td align="right">8,164</td>
<td align="right">0.8%</td>
<td align="right">8,236</td>
<td align="right">0.9%</td>
<td align="right">0.9%</td>
</tr>
<tr>
<td align="left">operator wrapper</td>
<td align="right">10,116</td>
<td align="right">1.0%</td>
<td align="right">10,184</td>
<td align="right">1.1%</td>
<td align="right">0.7%</td>
</tr>
<tr>
<td align="left">meth descr varargs keywords</td>
<td align="right">20,749</td>
<td align="right">2.1%</td>
<td align="right">20,878</td>
<td align="right">2.2%</td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">cfunc varargs keywords</td>
<td align="right">32,024</td>
<td align="right">3.3%</td>
<td align="right">32,177</td>
<td align="right">3.3%</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">cfunc varargs</td>
<td align="right">14,089</td>
<td align="right">1.5%</td>
<td align="right">14,148</td>
<td align="right">1.5%</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">code complex parameters</td>
<td align="right">184,641</td>
<td align="right">19.1%</td>
<td align="right">185,280</td>
<td align="right">19.1%</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">metaclass</td>
<td align="right">42,920</td>
<td align="right">4.4%</td>
<td align="right">43,066</td>
<td align="right">4.4%</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">class no vectorcall</td>
<td align="right">77,856</td>
<td align="right">8.1%</td>
<td align="right">78,101</td>
<td align="right">8.1%</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">cfunc noargs</td>
<td align="right">69,709</td>
<td align="right">7.2%</td>
<td align="right">69,876</td>
<td align="right">7.2%</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">wrong number arguments</td>
<td align="right">13,773</td>
<td align="right">1.4%</td>
<td align="right">13,793</td>
<td align="right">1.4%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">78,498</td>
<td align="right">8.1%</td>
<td align="right">78,602</td>
<td align="right">8.1%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">init not python</td>
<td align="right">16,426</td>
<td align="right">1.7%</td>
<td align="right">16,406</td>
<td align="right">1.7%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">meth descr varargs</td>
<td align="right">18,600</td>
<td align="right">1.9%</td>
<td align="right">18,620</td>
<td align="right">1.9%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">meth descr method fastcall keywords</td>
<td align="right">207,165</td>
<td align="right">21.4%</td>
<td align="right">207,245</td>
<td align="right">21.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">init not inline values</td>
<td align="right">105,697</td>
<td align="right">10.9%</td>
<td align="right">105,677</td>
<td align="right">10.9%</td>
<td align="right">-0.0%</td>
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
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">1,866,614</td>
<td align="right">0.0%</td>
<td align="right">1,752,752</td>
<td align="right">0.0%</td>
<td align="right">-6.1%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">155,264,205</td>
<td align="right">3.3%</td>
<td align="right">147,555,217</td>
<td align="right">3.1%</td>
<td align="right">-5.0%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">4,581,602,322</td>
<td align="right">96.7%</td>
<td align="right">4,581,377,141</td>
<td align="right">96.9%</td>
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
<td align="right">233,903</td>
<td align="right">67.4%</td>
<td align="right">226,596</td>
<td align="right">67.1%</td>
<td align="right">-3.1%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">113,270</td>
<td align="right">32.6%</td>
<td align="right">111,187</td>
<td align="right">32.9%</td>
<td align="right">-1.8%</td>
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
<td align="right">1.0%</td>
<td align="right">1,663</td>
<td align="right">0.7%</td>
<td align="right">-29.0%</td>
</tr>
<tr>
<td align="left">different types</td>
<td align="right">55,463</td>
<td align="right">23.7%</td>
<td align="right">50,666</td>
<td align="right">22.4%</td>
<td align="right">-8.6%</td>
</tr>
<tr>
<td align="left">baseobject</td>
<td align="right">34,114</td>
<td align="right">14.6%</td>
<td align="right">32,162</td>
<td align="right">14.2%</td>
<td align="right">-5.7%</td>
</tr>
<tr>
<td align="left">bytes</td>
<td align="right">4,240</td>
<td align="right">1.8%</td>
<td align="right">4,040</td>
<td align="right">1.8%</td>
<td align="right">-4.7%</td>
</tr>
<tr>
<td align="left">long float</td>
<td align="right">1,567</td>
<td align="right">0.7%</td>
<td align="right">1,616</td>
<td align="right">0.7%</td>
<td align="right">3.1%</td>
</tr>
<tr>
<td align="left">bool</td>
<td align="right">3,822</td>
<td align="right">1.6%</td>
<td align="right">3,786</td>
<td align="right">1.7%</td>
<td align="right">-0.9%</td>
</tr>
<tr>
<td align="left">big int</td>
<td align="right">61,681</td>
<td align="right">26.4%</td>
<td align="right">62,119</td>
<td align="right">27.4%</td>
<td align="right">0.7%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">14,702</td>
<td align="right">6.3%</td>
<td align="right">14,622</td>
<td align="right">6.5%</td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">24,179</td>
<td align="right">10.3%</td>
<td align="right">24,074</td>
<td align="right">10.6%</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">float long</td>
<td align="right">16,378</td>
<td align="right">7.0%</td>
<td align="right">16,435</td>
<td align="right">7.3%</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">4,334</td>
<td align="right">1.9%</td>
<td align="right">4,333</td>
<td align="right">1.9%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">string</td>
<td align="right">11,080</td>
<td align="right">4.7%</td>
<td align="right">11,080</td>
<td align="right">4.9%</td>
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
<td align="right">116,297,274</td>
<td align="right">4.5%</td>
<td align="right">105,041,485</td>
<td align="right">4.1%</td>
<td align="right">-9.7%</td>
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
<td align="right">2,484,200</td>
<td align="right">0.1%</td>
<td align="right">-1.2%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">2,481,036,448</td>
<td align="right">95.5%</td>
<td align="right">2,478,792,690</td>
<td align="right">95.9%</td>
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
<td align="right">131,801</td>
<td align="right">66.3%</td>
<td align="right">124,035</td>
<td align="right">65.1%</td>
<td align="right">-5.9%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">67,026</td>
<td align="right">33.7%</td>
<td align="right">66,469</td>
<td align="right">34.9%</td>
<td align="right">-0.8%</td>
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
<td align="right">37,356</td>
<td align="right">28.3%</td>
<td align="right">33,855</td>
<td align="right">27.3%</td>
<td align="right">-9.4%</td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">19,922</td>
<td align="right">15.1%</td>
<td align="right">18,247</td>
<td align="right">14.7%</td>
<td align="right">-8.4%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">47,475</td>
<td align="right">36.0%</td>
<td align="right">45,602</td>
<td align="right">36.8%</td>
<td align="right">-3.9%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">27,048</td>
<td align="right">20.5%</td>
<td align="right">26,331</td>
<td align="right">21.2%</td>
<td align="right">-2.7%</td>
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
<td align="right">101,932,499</td>
<td align="right">7.1%</td>
<td align="right">3,429,744</td>
<td align="right">0.9%</td>
<td align="right">-96.6%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">1,202,502,553</td>
<td align="right">84.2%</td>
<td align="right">271,898,365</td>
<td align="right">69.2%</td>
<td align="right">-77.4%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">223,606,545</td>
<td align="right">15.7%</td>
<td align="right">120,985,648</td>
<td align="right">30.8%</td>
<td align="right">-45.9%</td>
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
<td align="right">1,989,443</td>
<td align="right">91.2%</td>
<td align="right">131,038</td>
<td align="right">44.1%</td>
<td align="right">-93.4%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">192,110</td>
<td align="right">8.8%</td>
<td align="right">165,919</td>
<td align="right">55.9%</td>
<td align="right">-13.6%</td>
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
<td align="right">5.5%</td>
<td align="right">6,720</td>
<td align="right">4.1%</td>
<td align="right">-36.6%</td>
</tr>
<tr>
<td align="left">dict items</td>
<td align="right">66,280</td>
<td align="right">34.5%</td>
<td align="right">50,522</td>
<td align="right">30.4%</td>
<td align="right">-23.8%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">14,619</td>
<td align="right">7.6%</td>
<td align="right">11,179</td>
<td align="right">6.7%</td>
<td align="right">-23.5%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">26,042</td>
<td align="right">13.6%</td>
<td align="right">23,376</td>
<td align="right">14.1%</td>
<td align="right">-10.2%</td>
</tr>
<tr>
<td align="left">itertools</td>
<td align="right">6,531</td>
<td align="right">3.4%</td>
<td align="right">6,332</td>
<td align="right">3.8%</td>
<td align="right">-3.0%</td>
</tr>
<tr>
<td align="left">dict keys</td>
<td align="right">14,756</td>
<td align="right">7.7%</td>
<td align="right">14,530</td>
<td align="right">8.8%</td>
<td align="right">-1.5%</td>
</tr>
<tr>
<td align="left">ascii string</td>
<td align="right">2,680</td>
<td align="right">1.4%</td>
<td align="right">2,660</td>
<td align="right">1.6%</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">reversed list</td>
<td align="right">7,085</td>
<td align="right">3.7%</td>
<td align="right">7,126</td>
<td align="right">4.3%</td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">dict values</td>
<td align="right">7,010</td>
<td align="right">3.6%</td>
<td align="right">6,970</td>
<td align="right">4.2%</td>
<td align="right">-0.6%</td>
</tr>
<tr>
<td align="left">enumerate</td>
<td align="right">19,793</td>
<td align="right">10.3%</td>
<td align="right">19,790</td>
<td align="right">11.9%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">zip</td>
<td align="right">14,352</td>
<td align="right">7.5%</td>
<td align="right">14,352</td>
<td align="right">8.7%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">map</td>
<td align="right">1,380</td>
<td align="right">0.7%</td>
<td align="right">1,380</td>
<td align="right">0.8%</td>
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
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">577,214,459</td>
<td align="right">3.6%</td>
<td align="right">610,242,741</td>
<td align="right">3.8%</td>
<td align="right">5.7%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">1,429,446,386</td>
<td align="right">8.8%</td>
<td align="right">1,423,713,059</td>
<td align="right">8.8%</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">
deopt
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">674,142</td>
<td align="right">0.0%</td>
<td align="right">674,844</td>
<td align="right">0.0%</td>
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
<td align="right">14,712,356,035</td>
<td align="right">91.1%</td>
<td align="right">14,709,964,780</td>
<td align="right">91.1%</td>
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
<td align="right">11,775,974</td>
<td align="right">87.3%</td>
<td align="right">12,399,369</td>
<td align="right">88.0%</td>
<td align="right">5.3%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">1,711,646</td>
<td align="right">12.7%</td>
<td align="right">1,693,043</td>
<td align="right">12.0%</td>
<td align="right">-1.1%</td>
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
<td align="right">25,813</td>
<td align="right">1.5%</td>
<td align="right">22,153</td>
<td align="right">1.3%</td>
<td align="right">-14.2%</td>
</tr>
<tr>
<td align="left">not in keys</td>
<td align="right">16,660</td>
<td align="right">1.0%</td>
<td align="right">16,200</td>
<td align="right">1.0%</td>
<td align="right">-2.8%</td>
</tr>
<tr>
<td align="left">out of versions</td>
<td align="right">2,331</td>
<td align="right">0.1%</td>
<td align="right">2,281</td>
<td align="right">0.1%</td>
<td align="right">-2.1%</td>
</tr>
<tr>
<td align="left">metaclass attribute</td>
<td align="right">193,968</td>
<td align="right">11.3%</td>
<td align="right">189,810</td>
<td align="right">11.2%</td>
<td align="right">-2.1%</td>
</tr>
<tr>
<td align="left">method</td>
<td align="right">121,269</td>
<td align="right">7.1%</td>
<td align="right">118,839</td>
<td align="right">7.0%</td>
<td align="right">-2.0%</td>
</tr>
<tr>
<td align="left">not managed dict</td>
<td align="right">301,646</td>
<td align="right">17.6%</td>
<td align="right">296,075</td>
<td align="right">17.5%</td>
<td align="right">-1.8%</td>
</tr>
<tr>
<td align="left">mutable class</td>
<td align="right">78,948</td>
<td align="right">4.6%</td>
<td align="right">77,866</td>
<td align="right">4.6%</td>
<td align="right">-1.4%</td>
</tr>
<tr>
<td align="left">non object slot</td>
<td align="right">3,500</td>
<td align="right">0.2%</td>
<td align="right">3,543</td>
<td align="right">0.2%</td>
<td align="right">1.2%</td>
</tr>
<tr>
<td align="left">shadowed</td>
<td align="right">143,638</td>
<td align="right">8.4%</td>
<td align="right">142,765</td>
<td align="right">8.4%</td>
<td align="right">-0.6%</td>
</tr>
<tr>
<td align="left">class attr descriptor</td>
<td align="right">29,780</td>
<td align="right">1.7%</td>
<td align="right">29,900</td>
<td align="right">1.8%</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">non string or split</td>
<td align="right">21,750</td>
<td align="right">1.3%</td>
<td align="right">21,670</td>
<td align="right">1.3%</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">non overriding descriptor</td>
<td align="right">13,640</td>
<td align="right">0.8%</td>
<td align="right">13,590</td>
<td align="right">0.8%</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">overridden</td>
<td align="right">19,336</td>
<td align="right">1.1%</td>
<td align="right">19,351</td>
<td align="right">1.1%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">class attr simple</td>
<td align="right">716,207</td>
<td align="right">41.8%</td>
<td align="right">715,840</td>
<td align="right">42.3%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">module attr not found</td>
<td align="right">17,422</td>
<td align="right">1.0%</td>
<td align="right">17,422</td>
<td align="right">1.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">builtin class method</td>
<td align="right">3,878</td>
<td align="right">0.2%</td>
<td align="right">3,878</td>
<td align="right">0.2%</td>
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
<td align="right">6,565,587,350</td>
<td align="right">99.7%</td>
<td align="right">5,696,929,443</td>
<td align="right">99.6%</td>
<td align="right">-13.2%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">443,806</td>
<td align="right">0.0%</td>
<td align="right">445,257</td>
<td align="right">0.0%</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">20,571,786</td>
<td align="right">0.3%</td>
<td align="right">20,573,675</td>
<td align="right">0.4%</td>
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
<td align="right">669,106</td>
<td align="right">100.0%</td>
<td align="right">669,357</td>
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
<td align="right">134,384,144</td>
<td align="right">100.0%</td>
<td align="right">135,149,981</td>
<td align="right">100.0%</td>
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
<td align="right">11,985</td>
<td align="right">0.0%</td>
<td align="right">11,992</td>
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
<td align="right">11,817</td>
<td align="right">100.0%</td>
<td align="right">11,817</td>
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
<td align="right">173,914,537</td>
<td align="right">18.1%</td>
<td align="right">173,916,125</td>
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
<td align="right">787,151,961</td>
<td align="right">81.9%</td>
<td align="right">787,157,353</td>
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
<td align="right">7,123</td>
<td align="right">10.3%</td>
<td align="right">7,127</td>
<td align="right">10.3%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">61,862</td>
<td align="right">89.7%</td>
<td align="right">61,866</td>
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
<td align="right">16,122</td>
<td align="right">26.1%</td>
<td align="right">16,126</td>
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
<td align="right">168,299,435</td>
<td align="right">5.6%</td>
<td align="right">169,689,447</td>
<td align="right">5.6%</td>
<td align="right">0.8%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">242,540,990</td>
<td align="right">8.0%</td>
<td align="right">243,836,633</td>
<td align="right">8.1%</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">2,778,007,553</td>
<td align="right">91.9%</td>
<td align="right">2,779,264,912</td>
<td align="right">91.8%</td>
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
<td align="right">3,324,786</td>
<td align="right">95.7%</td>
<td align="right">3,351,022</td>
<td align="right">95.8%</td>
<td align="right">0.8%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">147,577</td>
<td align="right">4.3%</td>
<td align="right">147,585</td>
<td align="right">4.2%</td>
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
<td align="left">out of versions</td>
<td align="right">594</td>
<td align="right">0.4%</td>
<td align="right">573</td>
<td align="right">0.4%</td>
<td align="right">-3.5%</td>
</tr>
<tr>
<td align="left">method</td>
<td align="right">1,580</td>
<td align="right">1.1%</td>
<td align="right">1,540</td>
<td align="right">1.0%</td>
<td align="right">-2.5%</td>
</tr>
<tr>
<td align="left">property</td>
<td align="right">5,640</td>
<td align="right">3.8%</td>
<td align="right">5,740</td>
<td align="right">3.9%</td>
<td align="right">1.8%</td>
</tr>
<tr>
<td align="left">no dict</td>
<td align="right">4,780</td>
<td align="right">3.2%</td>
<td align="right">4,800</td>
<td align="right">3.3%</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">class attr simple</td>
<td align="right">49,939</td>
<td align="right">33.8%</td>
<td align="right">49,878</td>
<td align="right">33.8%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">not managed dict</td>
<td align="right">28,566</td>
<td align="right">19.4%</td>
<td align="right">28,576</td>
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
<td align="right">15,100</td>
<td align="right">10.2%</td>
<td align="right">15,100</td>
<td align="right">10.2%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">overriding descriptor</td>
<td align="right">10,820</td>
<td align="right">7.3%</td>
<td align="right">10,820</td>
<td align="right">7.3%</td>
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
<td align="right">130,966,728</td>
<td align="right">13.2%</td>
<td align="right">129,344,810</td>
<td align="right">13.0%</td>
<td align="right">-1.2%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">863,407,007</td>
<td align="right">86.8%</td>
<td align="right">863,054,286</td>
<td align="right">87.0%</td>
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
<td align="right">82,597</td>
<td align="right">81.6%</td>
<td align="right">80,933</td>
<td align="right">81.3%</td>
<td align="right">-2.0%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">18,565</td>
<td align="right">18.4%</td>
<td align="right">18,571</td>
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
<td align="right">7,320</td>
<td align="right">8.9%</td>
<td align="right">6,720</td>
<td align="right">8.3%</td>
<td align="right">-8.2%</td>
</tr>
<tr>
<td align="left">out of range</td>
<td align="right">2,048</td>
<td align="right">2.5%</td>
<td align="right">1,968</td>
<td align="right">2.4%</td>
<td align="right">-3.9%</td>
</tr>
<tr>
<td align="left">bytearray int</td>
<td align="right">1,400</td>
<td align="right">1.7%</td>
<td align="right">1,360</td>
<td align="right">1.7%</td>
<td align="right">-2.9%</td>
</tr>
<tr>
<td align="left">dict subclass no override</td>
<td align="right">27,313</td>
<td align="right">33.1%</td>
<td align="right">26,609</td>
<td align="right">32.9%</td>
<td align="right">-2.6%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">2,060</td>
<td align="right">2.5%</td>
<td align="right">2,080</td>
<td align="right">2.6%</td>
<td align="right">1.0%</td>
</tr>
<tr>
<td align="left">py simple</td>
<td align="right">42,416</td>
<td align="right">51.4%</td>
<td align="right">42,156</td>
<td align="right">52.1%</td>
<td align="right">-0.6%</td>
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
<td align="right">358,064,238</td>
<td align="right">5.6%</td>
<td align="right">341,607,154</td>
<td align="right">5.4%</td>
<td align="right">-4.6%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">105,496,216</td>
<td align="right">1.6%</td>
<td align="right">103,488,193</td>
<td align="right">1.6%</td>
<td align="right">-1.9%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">6,041,876,358</td>
<td align="right">94.4%</td>
<td align="right">6,026,789,411</td>
<td align="right">94.6%</td>
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
<td align="left">Failure</td>
<td align="right">672,451</td>
<td align="right">22.8%</td>
<td align="right">627,951</td>
<td align="right">21.9%</td>
<td align="right">-6.6%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">2,275,432</td>
<td align="right">77.2%</td>
<td align="right">2,237,717</td>
<td align="right">78.1%</td>
<td align="right">-1.7%</td>
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
<td align="right">99,487</td>
<td align="right">14.8%</td>
<td align="right">57,852</td>
<td align="right">9.2%</td>
<td align="right">-41.8%</td>
</tr>
<tr>
<td align="left">dict</td>
<td align="right">34,332</td>
<td align="right">5.1%</td>
<td align="right">32,011</td>
<td align="right">5.1%</td>
<td align="right">-6.8%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">43,599</td>
<td align="right">6.5%</td>
<td align="right">43,211</td>
<td align="right">6.9%</td>
<td align="right">-0.9%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">96,404</td>
<td align="right">14.3%</td>
<td align="right">96,098</td>
<td align="right">15.3%</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">sequence</td>
<td align="right">18,139</td>
<td align="right">2.7%</td>
<td align="right">18,181</td>
<td align="right">2.9%</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">number</td>
<td align="right">183,601</td>
<td align="right">27.3%</td>
<td align="right">183,685</td>
<td align="right">29.3%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">bytes</td>
<td align="right">18,732</td>
<td align="right">2.8%</td>
<td align="right">18,735</td>
<td align="right">3.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">174,177</td>
<td align="right">25.9%</td>
<td align="right">174,198</td>
<td align="right">27.7%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">float</td>
<td align="right">2,320</td>
<td align="right">0.3%</td>
<td align="right">2,320</td>
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
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">3,160</td>
<td align="right">0.0%</td>
<td align="right">1,060</td>
<td align="right">0.0%</td>
<td align="right">-66.5%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">500,862</td>
<td align="right">0.0%</td>
<td align="right">411,181</td>
<td align="right">0.0%</td>
<td align="right">-17.9%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">1,561,644,017</td>
<td align="right">100.0%</td>
<td align="right">1,550,172,620</td>
<td align="right">100.0%</td>
<td align="right">-0.7%</td>
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
<td align="right">3,581</td>
<td align="right">8.2%</td>
<td align="right">3,517</td>
<td align="right">8.1%</td>
<td align="right">-1.8%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">40,037</td>
<td align="right">91.8%</td>
<td align="right">40,065</td>
<td align="right">91.9%</td>
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
<td align="left">other</td>
<td align="right">380</td>
<td align="right">10.6%</td>
<td align="right">340</td>
<td align="right">9.7%</td>
<td align="right">-10.5%</td>
</tr>
<tr>
<td align="left">sequence</td>
<td align="right">2,520</td>
<td align="right">70.4%</td>
<td align="right">2,496</td>
<td align="right">71.0%</td>
<td align="right">-1.0%</td>
</tr>
<tr>
<td align="left">iterator</td>
<td align="right">681</td>
<td align="right">19.0%</td>
<td align="right">681</td>
<td align="right">19.4%</td>
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
Specialized hits
<details>
<summary>ⓘ</summary>

Specialized instructions, e.g. `LOAD_ATTR_MODULE` that complete.
</details>
</td>
<td align="right">46,113,266,076</td>
<td align="right">35.3%</td>
<td align="right">41,696,424,067</td>
<td align="right">34.7%</td>
<td align="right">-9.6%</td>
</tr>
<tr>
<td align="left">
Basic
<details>
<summary>ⓘ</summary>

Instructions that are not and cannot be specialized, e.g. `LOAD_FAST`.
</details>
</td>
<td align="right">71,180,307,626</td>
<td align="right">54.4%</td>
<td align="right">65,840,358,194</td>
<td align="right">54.8%</td>
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
<td align="right">12,205,431,711</td>
<td align="right">9.3%</td>
<td align="right">11,357,562,421</td>
<td align="right">9.5%</td>
<td align="right">-6.9%</td>
</tr>
<tr>
<td align="left">
Specialized misses
<details>
<summary>ⓘ</summary>

Specialized instructions, e.g. `LOAD_ATTR_MODULE` that deopt.
</details>
</td>
<td align="right">1,247,610,364</td>
<td align="right">1.0%</td>
<td align="right">1,178,885,374</td>
<td align="right">1.0%</td>
<td align="right">-5.5%</td>
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
<td align="right">223,606,545</td>
<td align="right">4.2%</td>
<td align="right">120,985,648</td>
<td align="right">2.4%</td>
<td align="right">-45.9%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR</td>
<td align="right">420,827,620</td>
<td align="right">7.9%</td>
<td align="right">329,029,688</td>
<td align="right">6.5%</td>
<td align="right">-21.8%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">155,264,205</td>
<td align="right">2.9%</td>
<td align="right">147,555,217</td>
<td align="right">2.9%</td>
<td align="right">-5.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">358,064,238</td>
<td align="right">6.7%</td>
<td align="right">341,607,154</td>
<td align="right">6.7%</td>
<td align="right">-4.6%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">639,369,647</td>
<td align="right">11.9%</td>
<td align="right">616,386,911</td>
<td align="right">12.1%</td>
<td align="right">-3.6%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR</td>
<td align="right">130,966,728</td>
<td align="right">2.4%</td>
<td align="right">129,344,810</td>
<td align="right">2.5%</td>
<td align="right">-1.2%</td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">242,540,990</td>
<td align="right">4.5%</td>
<td align="right">243,836,633</td>
<td align="right">4.8%</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">1,429,446,386</td>
<td align="right">26.7%</td>
<td align="right">1,423,713,059</td>
<td align="right">28.0%</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">1,442,550,038</td>
<td align="right">26.9%</td>
<td align="right">1,438,550,239</td>
<td align="right">28.3%</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">SEND</td>
<td align="right">173,914,537</td>
<td align="right">3.2%</td>
<td align="right">173,916,125</td>
<td align="right">3.4%</td>
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
<td align="right">158,067,080</td>
<td align="right">12.7%</td>
<td align="right">190,040,038</td>
<td align="right">16.1%</td>
<td align="right">20.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right">59,991,114</td>
<td align="right">4.8%</td>
<td align="right">63,999,834</td>
<td align="right">5.4%</td>
<td align="right">6.7%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">73,235,951</td>
<td align="right">5.9%</td>
<td align="right">74,608,526</td>
<td align="right">6.3%</td>
<td align="right">1.9%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">128,225,966</td>
<td align="right">10.3%</td>
<td align="right">126,028,635</td>
<td align="right">10.7%</td>
<td align="right">-1.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">182,069,631</td>
<td align="right">14.6%</td>
<td align="right">180,201,319</td>
<td align="right">15.3%</td>
<td align="right">-1.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL_NONE</td>
<td align="right">49,141,734</td>
<td align="right">3.9%</td>
<td align="right">48,907,493</td>
<td align="right">4.1%</td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">110,292,645</td>
<td align="right">8.8%</td>
<td align="right">109,903,631</td>
<td align="right">9.3%</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_SLOT</td>
<td align="right">95,010,706</td>
<td align="right">7.6%</td>
<td align="right">95,028,062</td>
<td align="right">8.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">50,925,450</td>
<td align="right">4.1%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">FOR_ITER_TUPLE</td>
<td align="right">50,763,829</td>
<td align="right">4.1%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">TO_BOOL_ALWAYS_TRUE</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">46,690,423</td>
<td align="right">4.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">42,180,998</td>
<td align="right">3.6%</td>
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
<td align="right">860,658,463</td>
<td align="right">9.9%</td>
<td align="right">868,791,248</td>
<td align="right">10.0%</td>
<td align="right">0.9%</td>
</tr>
<tr>
<td align="left">Calls to Python functions inlined</td>
<td align="right">6,418,626,793</td>
<td align="right">73.5%</td>
<td align="right">6,382,758,737</td>
<td align="right">73.3%</td>
<td align="right">-0.6%</td>
</tr>
<tr>
<td align="left">Calls to PyEval_EvalDefault</td>
<td align="right">2,310,753,716</td>
<td align="right">26.5%</td>
<td align="right">2,321,450,891</td>
<td align="right">26.7%</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (total)</td>
<td align="right">2,310,753,716</td>
<td align="right">26.5%</td>
<td align="right">2,321,450,891</td>
<td align="right">26.7%</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (api)</td>
<td align="right">257,771,441</td>
<td align="right">3.0%</td>
<td align="right">258,841,266</td>
<td align="right">3.0%</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (function vectorcall)</td>
<td align="right">1,444,768,123</td>
<td align="right">16.6%</td>
<td align="right">1,448,212,593</td>
<td align="right">16.6%</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (slot)</td>
<td align="right">475,916,773</td>
<td align="right">5.5%</td>
<td align="right">476,798,867</td>
<td align="right">5.5%</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (vector)</td>
<td align="right">1,450,095,253</td>
<td align="right">16.6%</td>
<td align="right">1,452,659,643</td>
<td align="right">16.7%</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">Frame objects created</td>
<td align="right">88,585,902</td>
<td align="right">1.0%</td>
<td align="right">88,604,518</td>
<td align="right">1.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Frames pushed</td>
<td align="right">6,937,088,390</td>
<td align="right">79.5%</td>
<td align="right">6,936,357,849</td>
<td align="right">79.7%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (function ex)</td>
<td align="right">28,857,401</td>
<td align="right">0.3%</td>
<td align="right">28,859,891</td>
<td align="right">0.3%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (method)</td>
<td align="right">213,138,723</td>
<td align="right">2.4%</td>
<td align="right">213,150,322</td>
<td align="right">2.4%</td>
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
<td align="left">Increfs</td>
<td align="right">62,094,052,413</td>
<td align="right">51.7%</td>
<td align="right">66,490,120,728</td>
<td align="right">55.1%</td>
<td align="right">7.1%</td>
</tr>
<tr>
<td align="left">Method cache dunder misses</td>
<td align="right">15,146,241</td>
<td align="right"></td>
<td align="right">14,108,319</td>
<td align="right"></td>
<td align="right">-6.9%</td>
</tr>
<tr>
<td align="left">Interpreter increfs</td>
<td align="right">58,081,442,470</td>
<td align="right">48.3%</td>
<td align="right">54,146,711,618</td>
<td align="right">44.9%</td>
<td align="right">-6.8%</td>
</tr>
<tr>
<td align="left">Decrefs</td>
<td align="right">64,648,371,592</td>
<td align="right">47.0%</td>
<td align="right">68,875,470,005</td>
<td align="right">49.9%</td>
<td align="right">6.5%</td>
</tr>
<tr>
<td align="left">Interpreter decrefs</td>
<td align="right">72,957,778,829</td>
<td align="right">53.0%</td>
<td align="right">69,175,503,542</td>
<td align="right">50.1%</td>
<td align="right">-5.2%</td>
</tr>
<tr>
<td align="left">Method cache collisions</td>
<td align="right">83,325,843</td>
<td align="right"></td>
<td align="right">80,436,093</td>
<td align="right"></td>
<td align="right">-3.5%</td>
</tr>
<tr>
<td align="left">Method cache misses</td>
<td align="right">75,925,228</td>
<td align="right"></td>
<td align="right">74,077,179</td>
<td align="right"></td>
<td align="right">-2.4%</td>
</tr>
<tr>
<td align="left">Allocations over 4 kbytes</td>
<td align="right">21,171,775</td>
<td align="right">0.1%</td>
<td align="right">21,269,723</td>
<td align="right">0.1%</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">Allocations to 4 kbytes</td>
<td align="right">104,891,766</td>
<td align="right">0.6%</td>
<td align="right">105,308,270</td>
<td align="right">0.6%</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">Inline values</td>
<td align="right">183,063,584</td>
<td align="right"></td>
<td align="right">183,490,205</td>
<td align="right"></td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">Allocations from freelist</td>
<td align="right">6,790,846,801</td>
<td align="right">36.7%</td>
<td align="right">6,777,653,103</td>
<td align="right">36.6%</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">Frees to freelist</td>
<td align="right">6,792,790,645</td>
<td align="right"></td>
<td align="right">6,779,601,166</td>
<td align="right"></td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">Frees</td>
<td align="right">12,054,962,042</td>
<td align="right"></td>
<td align="right">12,042,797,513</td>
<td align="right"></td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">Method cache hits</td>
<td align="right">3,131,202,284</td>
<td align="right"></td>
<td align="right">3,128,252,339</td>
<td align="right"></td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">Method cache dunder hits</td>
<td align="right">3,525,403,798</td>
<td align="right"></td>
<td align="right">3,528,332,735</td>
<td align="right"></td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">Allocations to 512 bytes</td>
<td align="right">11,599,747,460</td>
<td align="right">62.6%</td>
<td align="right">11,590,286,380</td>
<td align="right">62.7%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">Allocations</td>
<td align="right">11,725,811,001</td>
<td align="right">63.3%</td>
<td align="right">11,716,864,373</td>
<td align="right">63.4%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">Materialize dict (on request)</td>
<td align="right">3,358,423</td>
<td align="right">1.8%</td>
<td align="right">3,358,424</td>
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
<td align="right">115,743,716</td>
<td align="right">17,150,434,564</td>
<td align="right">0</td>
<td align="right">115,859,783</td>
<td align="right">17,157,795,120</td>
</tr>
<tr>
<td align="right">2</td>
<td align="right">0</td>
<td align="right">10,754,820</td>
<td align="right">6,960,150,490</td>
<td align="right">0</td>
<td align="right">10,754,880</td>
<td align="right">6,963,265,050</td>
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
Recursive call
<details>
<summary>ⓘ</summary>

A trace is truncated because it has a recursive call.
</details>
</td>
<td align="right">1,351</td>
<td align="right">0.2%</td>
<td align="right">1,990</td>
<td align="right">0.2%</td>
<td align="right">47.3%</td>
</tr>
<tr>
<td align="left">
Traces created
<details>
<summary>ⓘ</summary>

The number of traces that were successfully created.
</details>
</td>
<td align="right">108,316</td>
<td align="right">16.5%</td>
<td align="right">137,111</td>
<td align="right">16.5%</td>
<td align="right">26.6%</td>
</tr>
<tr>
<td align="left">
Optimization attempts
<details>
<summary>ⓘ</summary>

The number of times a potential trace is identified.  Specifically, this occurs in the JUMP BACKWARD instruction when the counter reaches a threshold.
</details>
</td>
<td align="right">658,068</td>
<td align="right"></td>
<td align="right">829,473</td>
<td align="right"></td>
<td align="right">26.0%</td>
</tr>
<tr>
<td align="left">
Trace too short
<details>
<summary>ⓘ</summary>

A potential trace is abandoced because it it too short.
</details>
</td>
<td align="right">549,752</td>
<td align="right">83.5%</td>
<td align="right">692,362</td>
<td align="right">83.5%</td>
<td align="right">25.9%</td>
</tr>
<tr>
<td align="left">
Low confidence
<details>
<summary>ⓘ</summary>

A trace is abandoned because the likelihood of the jump to top being taken is too low.
</details>
</td>
<td align="right">6,683</td>
<td align="right">1.0%</td>
<td align="right">8,223</td>
<td align="right">1.0%</td>
<td align="right">23.0%</td>
</tr>
<tr>
<td align="left">
Trace stack underflow
<details>
<summary>ⓘ</summary>

A potential trace is abandoned because it pops more frames than it pushes.
</details>
</td>
<td align="right">132,402</td>
<td align="right">20.1%</td>
<td align="right">158,451</td>
<td align="right">19.1%</td>
<td align="right">19.7%</td>
</tr>
<tr>
<td align="left">
Traces executed
<details>
<summary>ⓘ</summary>

The number of traces that were executed
</details>
</td>
<td align="right">6,359,831,769</td>
<td align="right"></td>
<td align="right">7,486,462,719</td>
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
<td align="right">810</td>
<td align="right">0.1%</td>
<td align="right">930</td>
<td align="right">0.1%</td>
<td align="right">14.8%</td>
</tr>
<tr>
<td align="left">
Inner loop found
<details>
<summary>ⓘ</summary>

A trace is truncated because it has an inner loop
</details>
</td>
<td align="right">16,110</td>
<td align="right">2.4%</td>
<td align="right">18,062</td>
<td align="right">2.2%</td>
<td align="right">12.1%</td>
</tr>
<tr>
<td align="left">
Uops executed
<details>
<summary>ⓘ</summary>

The total number of uops (micro-operations) that were executed
</details>
</td>
<td align="right">184,780,713,440</td>
<td align="right">2,905.4%</td>
<td align="right">204,175,237,960</td>
<td align="right">2,727.3%</td>
<td align="right">10.5%</td>
</tr>
<tr>
<td align="left">
Executors invalidated
<details>
<summary>ⓘ</summary>

The number of executors that were invalidated due to watched dictionary changes.
</details>
</td>
<td align="right">5,540</td>
<td align="right">5.1%</td>
<td align="right">5,660</td>
<td align="right">4.1%</td>
<td align="right">2.2%</td>
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
<td align="right">106,176</td>
<td align="right">98.0%</td>
<td align="right">134,951</td>
<td align="right">98.4%</td>
<td align="right">27.1%</td>
</tr>
<tr>
<td align="left">
Optimizer attempts
<details>
<summary>ⓘ</summary>

The number of times the trace optimizer (_Py_uop_analyze_and_optimize) was run.
</details>
</td>
<td align="right">108,316</td>
<td align="right"></td>
<td align="right">137,111</td>
<td align="right"></td>
<td align="right">26.6%</td>
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
<td align="right">2,100</td>
<td align="right">1.9%</td>
<td align="right">2,100</td>
<td align="right">1.5%</td>
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
<td align="right">2,870</td>
<td align="right">2.6%</td>
<td align="right">3,369</td>
<td align="right">2.5%</td>
<td align="right">17.4%</td>
</tr>
<tr>
<td align="left"><= 16</td>
<td align="right">16,800</td>
<td align="right">15.5%</td>
<td align="right">22,437</td>
<td align="right">16.4%</td>
<td align="right">33.6%</td>
</tr>
<tr>
<td align="left"><= 32</td>
<td align="right">41,692</td>
<td align="right">38.5%</td>
<td align="right">53,616</td>
<td align="right">39.1%</td>
<td align="right">28.6%</td>
</tr>
<tr>
<td align="left"><= 64</td>
<td align="right">26,592</td>
<td align="right">24.6%</td>
<td align="right">32,185</td>
<td align="right">23.5%</td>
<td align="right">21.0%</td>
</tr>
<tr>
<td align="left"><= 128</td>
<td align="right">14,907</td>
<td align="right">13.8%</td>
<td align="right">18,644</td>
<td align="right">13.6%</td>
<td align="right">25.1%</td>
</tr>
<tr>
<td align="left"><= 256</td>
<td align="right">4,590</td>
<td align="right">4.2%</td>
<td align="right">5,817</td>
<td align="right">4.2%</td>
<td align="right">26.7%</td>
</tr>
<tr>
<td align="left"><= 512</td>
<td align="right">865</td>
<td align="right">0.8%</td>
<td align="right">1,043</td>
<td align="right">0.8%</td>
<td align="right">20.6%</td>
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
<td align="right">80</td>
<td align="right">0.1%</td>
<td align="right">80</td>
<td align="right">0.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left"><= 8</td>
<td align="right">8,162</td>
<td align="right">7.5%</td>
<td align="right">9,445</td>
<td align="right">6.9%</td>
<td align="right">15.7%</td>
</tr>
<tr>
<td align="left"><= 16</td>
<td align="right">31,579</td>
<td align="right">29.2%</td>
<td align="right">41,773</td>
<td align="right">30.5%</td>
<td align="right">32.3%</td>
</tr>
<tr>
<td align="left"><= 32</td>
<td align="right">37,025</td>
<td align="right">34.2%</td>
<td align="right">47,294</td>
<td align="right">34.5%</td>
<td align="right">27.7%</td>
</tr>
<tr>
<td align="left"><= 64</td>
<td align="right">19,161</td>
<td align="right">17.7%</td>
<td align="right">23,646</td>
<td align="right">17.2%</td>
<td align="right">23.4%</td>
</tr>
<tr>
<td align="left"><= 128</td>
<td align="right">7,898</td>
<td align="right">7.3%</td>
<td align="right">9,753</td>
<td align="right">7.1%</td>
<td align="right">23.5%</td>
</tr>
<tr>
<td align="left"><= 256</td>
<td align="right">2,051</td>
<td align="right">1.9%</td>
<td align="right">2,760</td>
<td align="right">2.0%</td>
<td align="right">34.6%</td>
</tr>
<tr>
<td align="left"><= 512</td>
<td align="right">220</td>
<td align="right">0.2%</td>
<td align="right">200</td>
<td align="right">0.1%</td>
<td align="right">-9.1%</td>
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
<td align="left">_CONVERT_VALUE</td>
<td align="right">786,540</td>
<td align="right">51,690,800</td>
<td align="right">6,471.9%</td>
</tr>
<tr>
<td align="left">_BUILD_CONST_KEY_MAP</td>
<td align="right">79,650</td>
<td align="right">4,070,010</td>
<td align="right">5,009.9%</td>
</tr>
<tr>
<td align="left">_BUILD_STRING</td>
<td align="right">3,309,660</td>
<td align="right">28,221,129</td>
<td align="right">752.7%</td>
</tr>
<tr>
<td align="left">_FORMAT_SIMPLE</td>
<td align="right">9,557,665</td>
<td align="right">60,496,790</td>
<td align="right">533.0%</td>
</tr>
<tr>
<td align="left">_FOR_ITER_TIER_TWO</td>
<td align="right">402,385,935</td>
<td align="right">1,653,736,187</td>
<td align="right">311.0%</td>
</tr>
<tr>
<td align="left">_GUARD_BUILTINS_VERSION</td>
<td align="right">38,636</td>
<td align="right">101,651</td>
<td align="right">163.1%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_CLASS_1</td>
<td align="right">86,360</td>
<td align="right">3,840</td>
<td align="right">-95.6%</td>
</tr>
<tr>
<td align="left">_BUILD_MAP</td>
<td align="right">9,868,382</td>
<td align="right">18,544,067</td>
<td align="right">87.9%</td>
</tr>
<tr>
<td align="left">_POP_TOP_LOAD_CONST_INLINE_BORROW</td>
<td align="right">872,577</td>
<td align="right">1,447,966</td>
<td align="right">65.9%</td>
</tr>
<tr>
<td align="left">_DICT_MERGE</td>
<td align="right">7,203,107</td>
<td align="right">11,822,285</td>
<td align="right">64.1%</td>
</tr>
<tr>
<td align="left">_CHECK_VALIDITY_AND_SET_IP</td>
<td align="right">2,301,656,714</td>
<td align="right">3,684,272,340</td>
<td align="right">60.1%</td>
</tr>
<tr>
<td align="left">_SET_ADD</td>
<td align="right">1,457,503</td>
<td align="right">2,183,297</td>
<td align="right">49.8%</td>
</tr>
<tr>
<td align="left">_BINARY_SUBSCR_DICT</td>
<td align="right">258,305,741</td>
<td align="right">374,582,639</td>
<td align="right">45.0%</td>
</tr>
<tr>
<td align="left">_UNPACK_SEQUENCE_TUPLE</td>
<td align="right">191,272,809</td>
<td align="right">277,159,890</td>
<td align="right">44.9%</td>
</tr>
<tr>
<td align="left">_CALL_TYPE_1</td>
<td align="right">237,497,937</td>
<td align="right">332,581,722</td>
<td align="right">40.0%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_4</td>
<td align="right">448,283,678</td>
<td align="right">624,865,536</td>
<td align="right">39.4%</td>
</tr>
<tr>
<td align="left">_STORE_DEREF</td>
<td align="right">2,930,525</td>
<td align="right">3,861,131</td>
<td align="right">31.8%</td>
</tr>
<tr>
<td align="left">_POP_FRAME</td>
<td align="right">550,804,432</td>
<td align="right">724,839,525</td>
<td align="right">31.6%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_6</td>
<td align="right">417,767,338</td>
<td align="right">545,717,222</td>
<td align="right">30.6%</td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_FAST</td>
<td align="right">790,735,290</td>
<td align="right">1,028,397,004</td>
<td align="right">30.1%</td>
</tr>
<tr>
<td align="left">_SIDE_EXIT</td>
<td align="right">3,600,153,301</td>
<td align="right">4,592,110,789</td>
<td align="right">27.6%</td>
</tr>
<tr>
<td align="left">_LOAD_CONST_INLINE_BORROW_WITH_NULL</td>
<td align="right">367,031,526</td>
<td align="right">462,741,384</td>
<td align="right">26.1%</td>
</tr>
<tr>
<td align="left">_CALL_ISINSTANCE</td>
<td align="right">312,453,779</td>
<td align="right">392,548,625</td>
<td align="right">25.6%</td>
</tr>
<tr>
<td align="left">_COLD_EXIT</td>
<td align="right">1,635,322,150</td>
<td align="right">2,052,393,346</td>
<td align="right">25.5%</td>
</tr>
<tr>
<td align="left">_DEOPT</td>
<td align="right">1,123,870,322</td>
<td align="right">841,372,963</td>
<td align="right">-25.1%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">908,082,073</td>
<td align="right">1,123,199,114</td>
<td align="right">23.7%</td>
</tr>
<tr>
<td align="left">_ITER_CHECK_TUPLE</td>
<td align="right">540,961,965</td>
<td align="right">413,790,781</td>
<td align="right">-23.5%</td>
</tr>
<tr>
<td align="left">_LOAD_CONST_INLINE_WITH_NULL</td>
<td align="right">1,657,970,041</td>
<td align="right">2,037,444,853</td>
<td align="right">22.9%</td>
</tr>
<tr>
<td align="left">_GUARD_KEYS_VERSION</td>
<td align="right">1,001,342,908</td>
<td align="right">1,230,384,249</td>
<td align="right">22.9%</td>
</tr>
<tr>
<td align="left">_GUARD_NOT_EXHAUSTED_TUPLE</td>
<td align="right">463,659,054</td>
<td align="right">361,579,798</td>
<td align="right">-22.0%</td>
</tr>
<tr>
<td align="left">_LOAD_GLOBAL_MODULE</td>
<td align="right">44,267,468</td>
<td align="right">53,877,162</td>
<td align="right">21.7%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_3</td>
<td align="right">630,732,248</td>
<td align="right">767,617,060</td>
<td align="right">21.7%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_5</td>
<td align="right">647,223,478</td>
<td align="right">785,789,100</td>
<td align="right">21.4%</td>
</tr>
<tr>
<td align="left">_ERROR_POP_N</td>
<td align="right">485,996</td>
<td align="right">585,621</td>
<td align="right">20.5%</td>
</tr>
<tr>
<td align="left">_GUARD_DORV_VALUES_INST_ATTR_FROM_DICT</td>
<td align="right">1,044,512,679</td>
<td align="right">1,255,601,608</td>
<td align="right">20.2%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_5</td>
<td align="right">2,042,993,246</td>
<td align="right">2,449,366,789</td>
<td align="right">19.9%</td>
</tr>
<tr>
<td align="left">_ITER_NEXT_TUPLE</td>
<td align="right">312,247,965</td>
<td align="right">251,641,056</td>
<td align="right">-19.4%</td>
</tr>
<tr>
<td align="left">_LOAD_DEREF</td>
<td align="right">445,349,749</td>
<td align="right">531,786,054</td>
<td align="right">19.4%</td>
</tr>
<tr>
<td align="left">_GUARD_GLOBALS_VERSION</td>
<td align="right">50,855,144</td>
<td align="right">60,527,853</td>
<td align="right">19.0%</td>
</tr>
<tr>
<td align="left">_LOAD_CONST_INLINE</td>
<td align="right">1,240,189,744</td>
<td align="right">1,469,524,090</td>
<td align="right">18.5%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_4</td>
<td align="right">1,965,445,305</td>
<td align="right">2,328,545,056</td>
<td align="right">18.5%</td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_FAST_WITH_KEYWORDS</td>
<td align="right">21,536,199</td>
<td align="right">25,483,540</td>
<td align="right">18.3%</td>
</tr>
<tr>
<td align="left">_CONTAINS_OP_DICT</td>
<td align="right">360,191,979</td>
<td align="right">425,660,449</td>
<td align="right">18.2%</td>
</tr>
<tr>
<td align="left">_RESUME_CHECK</td>
<td align="right">1,313,965,249</td>
<td align="right">1,537,692,912</td>
<td align="right">17.0%</td>
</tr>
<tr>
<td align="left">_MAKE_CELL</td>
<td align="right">6,668,432</td>
<td align="right">7,783,489</td>
<td align="right">16.7%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_2</td>
<td align="right">2,710,355,526</td>
<td align="right">3,159,317,950</td>
<td align="right">16.6%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_2</td>
<td align="right">710,955,808</td>
<td align="right">824,922,711</td>
<td align="right">16.0%</td>
</tr>
<tr>
<td align="left">_CHECK_PERIODIC</td>
<td align="right">2,131,601,509</td>
<td align="right">2,461,323,083</td>
<td align="right">15.5%</td>
</tr>
<tr>
<td align="left">_DELETE_SUBSCR</td>
<td align="right">1,438,480</td>
<td align="right">1,659,025</td>
<td align="right">15.3%</td>
</tr>
<tr>
<td align="left">_POP_TOP</td>
<td align="right">698,268,171</td>
<td align="right">803,312,296</td>
<td align="right">15.0%</td>
</tr>
<tr>
<td align="left">_START_EXECUTOR</td>
<td align="right">4,724,509,619</td>
<td align="right">5,434,069,373</td>
<td align="right">15.0%</td>
</tr>
<tr>
<td align="left">_STORE_FAST</td>
<td align="right">2,952,971,034</td>
<td align="right">3,390,535,304</td>
<td align="right">14.8%</td>
</tr>
<tr>
<td align="left">_IS_OP</td>
<td align="right">337,679,309</td>
<td align="right">387,456,326</td>
<td align="right">14.7%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_4</td>
<td align="right">656,261,580</td>
<td align="right">752,343,983</td>
<td align="right">14.6%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_3</td>
<td align="right">3,104,176,357</td>
<td align="right">3,546,821,190</td>
<td align="right">14.3%</td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION_EXACT_ARGS</td>
<td align="right">1,583,632,006</td>
<td align="right">1,806,210,375</td>
<td align="right">14.1%</td>
</tr>
<tr>
<td align="left">_PUSH_FRAME</td>
<td align="right">1,524,223,369</td>
<td align="right">1,738,304,898</td>
<td align="right">14.0%</td>
</tr>
<tr>
<td align="left">_SAVE_RETURN_OFFSET</td>
<td align="right">1,524,223,369</td>
<td align="right">1,738,304,898</td>
<td align="right">14.0%</td>
</tr>
<tr>
<td align="left">_CONTAINS_OP_SET</td>
<td align="right">1,478,844,615</td>
<td align="right">1,682,445,226</td>
<td align="right">13.8%</td>
</tr>
<tr>
<td align="left">_UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">621,623,626</td>
<td align="right">703,751,693</td>
<td align="right">13.2%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_BOOL</td>
<td align="right">1,938,689,345</td>
<td align="right">2,179,880,316</td>
<td align="right">12.4%</td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_O</td>
<td align="right">615,071,156</td>
<td align="right">688,982,747</td>
<td align="right">12.0%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_STR</td>
<td align="right">27,646,370</td>
<td align="right">30,948,007</td>
<td align="right">11.9%</td>
</tr>
<tr>
<td align="left">_BUILD_TUPLE</td>
<td align="right">374,038,738</td>
<td align="right">418,579,867</td>
<td align="right">11.9%</td>
</tr>
<tr>
<td align="left">_PUSH_NULL</td>
<td align="right">734,228,906</td>
<td align="right">821,417,077</td>
<td align="right">11.9%</td>
</tr>
<tr>
<td align="left">_BINARY_SUBSCR_TUPLE_INT</td>
<td align="right">147,403,798</td>
<td align="right">164,822,483</td>
<td align="right">11.8%</td>
</tr>
<tr>
<td align="left">_CONTAINS_OP</td>
<td align="right">107,186,254</td>
<td align="right">118,578,993</td>
<td align="right">10.6%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_1</td>
<td align="right">1,853,144,977</td>
<td align="right">2,046,752,439</td>
<td align="right">10.4%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_3</td>
<td align="right">56,645,836</td>
<td align="right">62,555,172</td>
<td align="right">10.4%</td>
</tr>
<tr>
<td align="left">_CHECK_STACK_SPACE_OPERAND</td>
<td align="right">874,110,397</td>
<td align="right">965,185,036</td>
<td align="right">10.4%</td>
</tr>
<tr>
<td align="left">_CHECK_ATTR_CLASS</td>
<td align="right">25,087,483</td>
<td align="right">27,673,208</td>
<td align="right">10.3%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_CLASS_0</td>
<td align="right">23,405,957</td>
<td align="right">25,770,600</td>
<td align="right">10.1%</td>
</tr>
<tr>
<td align="left">_SET_IP</td>
<td align="right">16,306,814,387</td>
<td align="right">17,922,835,138</td>
<td align="right">9.9%</td>
</tr>
<tr>
<td align="left">_ITER_NEXT_LIST</td>
<td align="right">1,206,905,185</td>
<td align="right">1,090,125,944</td>
<td align="right">-9.7%</td>
</tr>
<tr>
<td align="left">_CHECK_VALIDITY</td>
<td align="right">17,924,404,248</td>
<td align="right">19,634,136,680</td>
<td align="right">9.5%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_1</td>
<td align="right">6,215,755,272</td>
<td align="right">6,803,162,191</td>
<td align="right">9.5%</td>
</tr>
<tr>
<td align="left">_ITER_CHECK_LIST</td>
<td align="right">1,503,804,443</td>
<td align="right">1,363,148,764</td>
<td align="right">-9.4%</td>
</tr>
<tr>
<td align="left">_ITER_CHECK_RANGE</td>
<td align="right">783,671,138</td>
<td align="right">711,606,083</td>
<td align="right">-9.2%</td>
</tr>
<tr>
<td align="left">_GUARD_NOT_EXHAUSTED_LIST</td>
<td align="right">1,487,637,357</td>
<td align="right">1,351,212,587</td>
<td align="right">-9.2%</td>
</tr>
<tr>
<td align="left">_GUARD_NOT_EXHAUSTED_RANGE</td>
<td align="right">782,313,378</td>
<td align="right">710,659,203</td>
<td align="right">-9.2%</td>
</tr>
<tr>
<td align="left">_ITER_NEXT_RANGE</td>
<td align="right">734,209,963</td>
<td align="right">667,573,379</td>
<td align="right">-9.1%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_0</td>
<td align="right">5,333,132,426</td>
<td align="right">5,805,052,435</td>
<td align="right">8.8%</td>
</tr>
<tr>
<td align="left">_GUARD_TYPE_VERSION</td>
<td align="right">5,360,302,605</td>
<td align="right">5,806,050,931</td>
<td align="right">8.3%</td>
</tr>
<tr>
<td align="left">_CHECK_CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">76,409,138</td>
<td align="right">82,752,396</td>
<td align="right">8.3%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">76,355,698</td>
<td align="right">82,691,896</td>
<td align="right">8.3%</td>
</tr>
<tr>
<td align="left">_COMPARE_OP</td>
<td align="right">93,559,095</td>
<td align="right">101,236,128</td>
<td align="right">8.2%</td>
</tr>
<tr>
<td align="left">_LOAD_CONST_INLINE_BORROW</td>
<td align="right">8,858,702,319</td>
<td align="right">9,554,148,839</td>
<td align="right">7.9%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST</td>
<td align="right">5,431,845,233</td>
<td align="right">5,855,819,082</td>
<td align="right">7.8%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right">88,699,067</td>
<td align="right">95,554,029</td>
<td align="right">7.7%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_NOT_NONE_POP</td>
<td align="right">154,910,572</td>
<td align="right">166,706,459</td>
<td align="right">7.6%</td>
</tr>
<tr>
<td align="left">_BINARY_SUBSCR</td>
<td align="right">1,241,166,687</td>
<td align="right">1,333,884,262</td>
<td align="right">7.5%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_FALSE_POP</td>
<td align="right">5,318,100,358</td>
<td align="right">5,713,012,141</td>
<td align="right">7.4%</td>
</tr>
<tr>
<td align="left">_JUMP_TO_TOP</td>
<td align="right">2,099,053,100</td>
<td align="right">2,254,283,386</td>
<td align="right">7.4%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_TRUE_POP</td>
<td align="right">2,577,418,275</td>
<td align="right">2,766,747,317</td>
<td align="right">7.3%</td>
</tr>
<tr>
<td align="left">_CHECK_ATTR_METHOD_LAZY_DICT</td>
<td align="right">97,397,289</td>
<td align="right">104,174,626</td>
<td align="right">7.0%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_METHOD_LAZY_DICT</td>
<td align="right">97,397,289</td>
<td align="right">104,174,626</td>
<td align="right">7.0%</td>
</tr>
<tr>
<td align="left">_BINARY_SUBSCR_STR_INT</td>
<td align="right">1,215,378,934</td>
<td align="right">1,298,401,750</td>
<td align="right">6.8%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS</td>
<td align="right">9,619,982</td>
<td align="right">10,219,185</td>
<td align="right">6.2%</td>
</tr>
<tr>
<td align="left">_CHECK_STACK_SPACE</td>
<td align="right">156,125,310</td>
<td align="right">146,628,710</td>
<td align="right">-6.1%</td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_O</td>
<td align="right">22,228,051</td>
<td align="right">20,915,013</td>
<td align="right">-5.9%</td>
</tr>
<tr>
<td align="left">_COPY</td>
<td align="right">1,252,545,849</td>
<td align="right">1,323,907,321</td>
<td align="right">5.7%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_MULTIPLY_FLOAT</td>
<td align="right">1,124,307,820</td>
<td align="right">1,188,299,080</td>
<td align="right">5.7%</td>
</tr>
<tr>
<td align="left">_UNPACK_SEQUENCE</td>
<td align="right">1,554,383</td>
<td align="right">1,642,065</td>
<td align="right">5.6%</td>
</tr>
<tr>
<td align="left">_GET_ITER</td>
<td align="right">242,201,658</td>
<td align="right">255,474,250</td>
<td align="right">5.5%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_MODULE</td>
<td align="right">9,198,765</td>
<td align="right">9,697,984</td>
<td align="right">5.4%</td>
</tr>
<tr>
<td align="left">_CHECK_ATTR_MODULE</td>
<td align="right">9,202,205</td>
<td align="right">9,701,424</td>
<td align="right">5.4%</td>
</tr>
<tr>
<td align="left">_LIST_APPEND</td>
<td align="right">179,824,900</td>
<td align="right">189,496,886</td>
<td align="right">5.4%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBTRACT_INT</td>
<td align="right">429,323,514</td>
<td align="right">452,164,233</td>
<td align="right">5.3%</td>
</tr>
<tr>
<td align="left">_GUARD_BOTH_INT</td>
<td align="right">3,157,556,485</td>
<td align="right">3,311,053,176</td>
<td align="right">4.9%</td>
</tr>
<tr>
<td align="left">_TO_BOOL</td>
<td align="right">240,445,999</td>
<td align="right">252,026,781</td>
<td align="right">4.8%</td>
</tr>
<tr>
<td align="left">_GUARD_BOTH_FLOAT</td>
<td align="right">1,554,381,757</td>
<td align="right">1,627,650,308</td>
<td align="right">4.7%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_INSTANCE_VALUE_0</td>
<td align="right">1,884,603,112</td>
<td align="right">1,972,908,799</td>
<td align="right">4.7%</td>
</tr>
<tr>
<td align="left">_CHECK_MANAGED_OBJECT_HAS_VALUES</td>
<td align="right">1,891,089,328</td>
<td align="right">1,979,566,055</td>
<td align="right">4.7%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_ADD_INT</td>
<td align="right">2,487,107,849</td>
<td align="right">2,602,905,571</td>
<td align="right">4.7%</td>
</tr>
<tr>
<td align="left">_UNPACK_SEQUENCE_LIST</td>
<td align="right">77,567,820</td>
<td align="right">80,802,889</td>
<td align="right">4.2%</td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_CLASS</td>
<td align="right">57,223,695</td>
<td align="right">59,600,885</td>
<td align="right">4.2%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">822,430,211</td>
<td align="right">855,920,982</td>
<td align="right">4.1%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_NONDESCRIPTOR_NO_DICT</td>
<td align="right">24,529,367</td>
<td align="right">25,518,103</td>
<td align="right">4.0%</td>
</tr>
<tr>
<td align="left">_BINARY_SUBSCR_LIST_INT</td>
<td align="right">1,052,767,370</td>
<td align="right">1,094,838,557</td>
<td align="right">4.0%</td>
</tr>
<tr>
<td align="left">_STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">102,698,339</td>
<td align="right">106,686,774</td>
<td align="right">3.9%</td>
</tr>
<tr>
<td align="left">_UNARY_INVERT</td>
<td align="right">12,534,740</td>
<td align="right">13,021,302</td>
<td align="right">3.9%</td>
</tr>
<tr>
<td align="left">_GUARD_DORV_NO_DICT</td>
<td align="right">104,006,099</td>
<td align="right">108,035,994</td>
<td align="right">3.9%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_AND_CLEAR</td>
<td align="right">16,235,053</td>
<td align="right">16,856,696</td>
<td align="right">3.8%</td>
</tr>
<tr>
<td align="left">_MAP_ADD</td>
<td align="right">20,602,922</td>
<td align="right">21,325,259</td>
<td align="right">3.5%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_1</td>
<td align="right">524,317,723</td>
<td align="right">542,560,126</td>
<td align="right">3.5%</td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">184,627,612</td>
<td align="right">190,939,454</td>
<td align="right">3.4%</td>
</tr>
<tr>
<td align="left">_BINARY_OP</td>
<td align="right">855,265,815</td>
<td align="right">884,127,739</td>
<td align="right">3.4%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_ADD_UNICODE</td>
<td align="right">23,051,931</td>
<td align="right">23,735,282</td>
<td align="right">3.0%</td>
</tr>
<tr>
<td align="left">_CALL_LEN</td>
<td align="right">195,186,143</td>
<td align="right">200,709,529</td>
<td align="right">2.8%</td>
</tr>
<tr>
<td align="left">_MAKE_FUNCTION</td>
<td align="right">60,668,230</td>
<td align="right">62,353,516</td>
<td align="right">2.8%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_0</td>
<td align="right">379,647,164</td>
<td align="right">389,973,747</td>
<td align="right">2.7%</td>
</tr>
<tr>
<td align="left">_BUILD_LIST</td>
<td align="right">246,174,458</td>
<td align="right">252,605,235</td>
<td align="right">2.6%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_ADD_FLOAT</td>
<td align="right">571,783,760</td>
<td align="right">586,482,580</td>
<td align="right">2.6%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_INSTANCE_VALUE_1</td>
<td align="right">6,364,796</td>
<td align="right">6,526,316</td>
<td align="right">2.5%</td>
</tr>
<tr>
<td align="left">_STORE_ATTR</td>
<td align="right">51,333,313</td>
<td align="right">50,057,902</td>
<td align="right">-2.5%</td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">225,607,948</td>
<td align="right">231,126,116</td>
<td align="right">2.4%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_SLOT_0</td>
<td align="right">703,989,724</td>
<td align="right">720,932,696</td>
<td align="right">2.4%</td>
</tr>
<tr>
<td align="left">_STORE_SUBSCR_LIST_INT</td>
<td align="right">478,865,502</td>
<td align="right">490,250,402</td>
<td align="right">2.4%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_6</td>
<td align="right">1,244,228,952</td>
<td align="right">1,273,036,867</td>
<td align="right">2.3%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_2</td>
<td align="right">105,708,986</td>
<td align="right">108,131,132</td>
<td align="right">2.3%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_NONE_POP</td>
<td align="right">41,555,384</td>
<td align="right">42,421,439</td>
<td align="right">2.1%</td>
</tr>
<tr>
<td align="left">_SWAP</td>
<td align="right">1,130,952,146</td>
<td align="right">1,153,155,198</td>
<td align="right">2.0%</td>
</tr>
<tr>
<td align="left">_COPY_FREE_VARS</td>
<td align="right">49,023,781</td>
<td align="right">49,971,661</td>
<td align="right">1.9%</td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_FAST_WITH_KEYWORDS</td>
<td align="right">153,715,656</td>
<td align="right">156,677,212</td>
<td align="right">1.9%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_0</td>
<td align="right">204,626,151</td>
<td align="right">208,486,206</td>
<td align="right">1.9%</td>
</tr>
<tr>
<td align="left">_COMPARE_OP_INT</td>
<td align="right">936,205,539</td>
<td align="right">953,180,509</td>
<td align="right">1.8%</td>
</tr>
<tr>
<td align="left">_CALL_STR_1</td>
<td align="right">68,922,154</td>
<td align="right">70,106,996</td>
<td align="right">1.7%</td>
</tr>
<tr>
<td align="left">_BINARY_SLICE</td>
<td align="right">120,026,703</td>
<td align="right">121,958,707</td>
<td align="right">1.6%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_LIST</td>
<td align="right">61,652,049</td>
<td align="right">60,662,577</td>
<td align="right">-1.6%</td>
</tr>
<tr>
<td align="left">_CALL_INTRINSIC_1</td>
<td align="right">96,025,245</td>
<td align="right">97,432,273</td>
<td align="right">1.5%</td>
</tr>
<tr>
<td align="left">_LIST_EXTEND</td>
<td align="right">96,949,045</td>
<td align="right">98,356,073</td>
<td align="right">1.5%</td>
</tr>
<tr>
<td align="left">_EXIT_TRACE</td>
<td align="right">2,751,631,558</td>
<td align="right">2,790,582,759</td>
<td align="right">1.4%</td>
</tr>
<tr>
<td align="left">_LOAD_GLOBAL</td>
<td align="right">188,842,338</td>
<td align="right">186,240,081</td>
<td align="right">-1.4%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_WITH_HINT</td>
<td align="right">97,694,722</td>
<td align="right">96,456,061</td>
<td align="right">-1.3%</td>
</tr>
<tr>
<td align="left">_CHECK_ATTR_WITH_HINT</td>
<td align="right">97,862,344</td>
<td align="right">96,638,482</td>
<td align="right">-1.3%</td>
</tr>
<tr>
<td align="left">_STORE_SUBSCR_DICT</td>
<td align="right">124,673,284</td>
<td align="right">126,224,035</td>
<td align="right">1.2%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_7</td>
<td align="right">1,204,910,396</td>
<td align="right">1,219,597,169</td>
<td align="right">1.2%</td>
</tr>
<tr>
<td align="left">_STORE_ATTR_SLOT</td>
<td align="right">124,668,806</td>
<td align="right">123,156,425</td>
<td align="right">-1.2%</td>
</tr>
<tr>
<td align="left">_STORE_GLOBAL</td>
<td align="right">1,260,560</td>
<td align="right">1,275,340</td>
<td align="right">1.2%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_CHECK</td>
<td align="right">253,564</td>
<td align="right">256,459</td>
<td align="right">1.1%</td>
</tr>
<tr>
<td align="left">_GUARD_BOTH_UNICODE</td>
<td align="right">965,844,830</td>
<td align="right">975,799,529</td>
<td align="right">1.0%</td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION</td>
<td align="right">1,279,303,451</td>
<td align="right">1,291,741,945</td>
<td align="right">1.0%</td>
</tr>
<tr>
<td align="left">_LOAD_GLOBAL_BUILTINS</td>
<td align="right">6,587,676</td>
<td align="right">6,650,691</td>
<td align="right">1.0%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_INT</td>
<td align="right">196,564,490</td>
<td align="right">198,383,696</td>
<td align="right">0.9%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_7</td>
<td align="right">3,378,463,039</td>
<td align="right">3,401,838,044</td>
<td align="right">0.7%</td>
</tr>
<tr>
<td align="left">_COMPARE_OP_STR</td>
<td align="right">1,825,001,352</td>
<td align="right">1,835,050,395</td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">_REPLACE_WITH_TRUE</td>
<td align="right">32,343,598</td>
<td align="right">32,514,251</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">_STORE_SUBSCR</td>
<td align="right">314,167,777</td>
<td align="right">315,791,613</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">_SET_FUNCTION_ATTRIBUTE</td>
<td align="right">47,087,487</td>
<td align="right">47,319,506</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_MULTIPLY_INT</td>
<td align="right">184,971,226</td>
<td align="right">185,793,590</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">_UNARY_NEGATIVE</td>
<td align="right">25,045,806</td>
<td align="right">25,148,519</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_NONE</td>
<td align="right">174,051,018</td>
<td align="right">174,638,308</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR</td>
<td align="right">1,094,470,210</td>
<td align="right">1,096,659,391</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">_UNARY_NOT</td>
<td align="right">62,210,447</td>
<td align="right">62,284,430</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBTRACT_FLOAT</td>
<td align="right">382,602,700</td>
<td align="right">383,046,880</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">_COMPARE_OP_FLOAT</td>
<td align="right">70,074,357</td>
<td align="right">70,071,448</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">_STORE_SLICE</td>
<td align="right">149,868,340</td>
<td align="right">149,868,340</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_BUILD_SLICE</td>
<td align="right">139,781,160</td>
<td align="right">139,781,160</td>
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
<td align="right">572,540</td>
<td align="right">572,540</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_STORE_NAME</td>
<td align="right">545,860</td>
<td align="right">545,860</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_GET_YIELD_FROM_ITER</td>
<td align="right">179,880</td>
<td align="right">179,880</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_LOAD_SUPER_ATTR_METHOD</td>
<td align="right">95,777</td>
<td align="right">95,777</td>
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
<td align="right">3,981,440</td>
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
<td align="right">2,760</td>
<td align="right">36,761</td>
<td align="right">1,231.9%</td>
</tr>
<tr>
<td align="left">IMPORT_NAME</td>
<td align="right">246</td>
<td align="right">447</td>
<td align="right">81.7%</td>
</tr>
<tr>
<td align="left">YIELD_VALUE</td>
<td align="right">119,312</td>
<td align="right">163,026</td>
<td align="right">36.6%</td>
</tr>
<tr>
<td align="left">CALL_ALLOC_AND_ENTER_INIT</td>
<td align="right">1,446</td>
<td align="right">1,965</td>
<td align="right">35.9%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">128,446</td>
<td align="right">169,182</td>
<td align="right">31.7%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_GETITEM</td>
<td align="right">2,580</td>
<td align="right">3,340</td>
<td align="right">29.5%</td>
</tr>
<tr>
<td align="left">CALL_LIST_APPEND</td>
<td align="right">5,910</td>
<td align="right">7,632</td>
<td align="right">29.1%</td>
</tr>
<tr>
<td align="left">LOAD_NAME</td>
<td align="right">1,360</td>
<td align="right">1,700</td>
<td align="right">25.0%</td>
</tr>
<tr>
<td align="left">RETURN_GENERATOR</td>
<td align="right">36,809</td>
<td align="right">44,296</td>
<td align="right">20.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_PROPERTY</td>
<td align="right">6,805</td>
<td align="right">8,173</td>
<td align="right">20.1%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_WITH_HINT</td>
<td align="right">200</td>
<td align="right">240</td>
<td align="right">20.0%</td>
</tr>
<tr>
<td align="left">CALL_PY_WITH_DEFAULTS</td>
<td align="right">9,041</td>
<td align="right">7,267</td>
<td align="right">-19.6%</td>
</tr>
<tr>
<td align="left">BUILD_SET</td>
<td align="right">226</td>
<td align="right">260</td>
<td align="right">15.0%</td>
</tr>
<tr>
<td align="left">FOR_ITER_GEN</td>
<td align="right">57,963</td>
<td align="right">53,843</td>
<td align="right">-7.1%</td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">32,344</td>
<td align="right">34,419</td>
<td align="right">6.4%</td>
</tr>
<tr>
<td align="left">CALL_KW</td>
<td align="right">25,835</td>
<td align="right">27,376</td>
<td align="right">6.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_INPLACE_ADD_UNICODE</td>
<td align="right">723</td>
<td align="right">763</td>
<td align="right">5.5%</td>
</tr>
<tr>
<td align="left">SEND</td>
<td align="right">31,240</td>
<td align="right">31,240</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BEFORE_WITH</td>
<td align="right">320</td>
<td align="right">320</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">SEND_GEN</td>
<td align="right">60</td>
<td align="right">60</td>
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
<td align="right">1,980</td>
<td align="right">1,980</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

---
Stats gathered on: 2024-04-05
