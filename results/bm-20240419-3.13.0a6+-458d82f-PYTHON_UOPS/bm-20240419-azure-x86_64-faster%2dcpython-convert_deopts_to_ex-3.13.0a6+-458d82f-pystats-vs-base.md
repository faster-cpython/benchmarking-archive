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
<td align="right">307,536,495</td>
<td align="right">9,334,309</td>
<td align="right">-97.0%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">665,029,112</td>
<td align="right">25,021,447</td>
<td align="right">-96.2%</td>
</tr>
<tr>
<td align="left">SET_ADD</td>
<td align="right">965,831</td>
<td align="right">240,462</td>
<td align="right">-75.1%</td>
</tr>
<tr>
<td align="left">FOR_ITER_RANGE</td>
<td align="right">107,046,275</td>
<td align="right">30,114,713</td>
<td align="right">-71.9%</td>
</tr>
<tr>
<td align="left">STORE_FAST_LOAD_FAST</td>
<td align="right">43,013,283</td>
<td align="right">15,894,887</td>
<td align="right">-63.0%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST</td>
<td align="right">545,226,907</td>
<td align="right">306,038,150</td>
<td align="right">-43.9%</td>
</tr>
<tr>
<td align="left">CALL_TYPE_1</td>
<td align="right">244,352,110</td>
<td align="right">147,630,431</td>
<td align="right">-39.6%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP_DICT</td>
<td align="right">176,687,189</td>
<td align="right">109,439,084</td>
<td align="right">-38.1%</td>
</tr>
<tr>
<td align="left">CONVERT_VALUE</td>
<td align="right">138,452,550</td>
<td align="right">87,548,490</td>
<td align="right">-36.8%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TUPLE</td>
<td align="right">307,985,540</td>
<td align="right">195,355,694</td>
<td align="right">-36.6%</td>
</tr>
<tr>
<td align="left">BUILD_CONST_KEY_MAP</td>
<td align="right">11,833,367</td>
<td align="right">7,670,962</td>
<td align="right">-35.2%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">109,154,512</td>
<td align="right">71,547,549</td>
<td align="right">-34.5%</td>
</tr>
<tr>
<td align="left">FORMAT_SIMPLE</td>
<td align="right">148,463,238</td>
<td align="right">97,518,792</td>
<td align="right">-34.3%</td>
</tr>
<tr>
<td align="left">BUILD_STRING</td>
<td align="right">75,501,177</td>
<td align="right">50,583,854</td>
<td align="right">-33.0%</td>
</tr>
<tr>
<td align="left">LOAD_NAME</td>
<td align="right">12,145,347</td>
<td align="right">8,144,707</td>
<td align="right">-32.9%</td>
</tr>
<tr>
<td align="left">BINARY_OP_MULTIPLY_FLOAT</td>
<td align="right">210,123,065</td>
<td align="right">146,544,305</td>
<td align="right">-30.3%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP_SET</td>
<td align="right">461,992,634</td>
<td align="right">339,223,765</td>
<td align="right">-26.6%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_LIST</td>
<td align="right">12,242,315</td>
<td align="right">9,009,909</td>
<td align="right">-26.4%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">345,542,139</td>
<td align="right">259,469,537</td>
<td align="right">-24.9%</td>
</tr>
<tr>
<td align="left">UNARY_INVERT</td>
<td align="right">2,598,484</td>
<td align="right">1,998,083</td>
<td align="right">-23.1%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR</td>
<td align="right">418,694,142</td>
<td align="right">326,702,423</td>
<td align="right">-22.0%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_DICT</td>
<td align="right">569,083,954</td>
<td align="right">452,539,894</td>
<td align="right">-20.5%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">3,028,913,207</td>
<td align="right">2,422,742,885</td>
<td align="right">-20.0%</td>
</tr>
<tr>
<td align="left">CALL_STR_1</td>
<td align="right">46,761,009</td>
<td align="right">38,335,102</td>
<td align="right">-18.0%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">6,697,224,378</td>
<td align="right">5,524,583,518</td>
<td align="right">-17.5%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_FLOAT</td>
<td align="right">87,797,803</td>
<td align="right">72,658,990</td>
<td align="right">-17.2%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE</td>
<td align="right">540,775</td>
<td align="right">453,076</td>
<td align="right">-16.2%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_O</td>
<td align="right">655,890,387</td>
<td align="right">552,118,957</td>
<td align="right">-15.8%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_TUPLE_INT</td>
<td align="right">210,853,286</td>
<td align="right">178,753,410</td>
<td align="right">-15.2%</td>
</tr>
<tr>
<td align="left">IS_OP</td>
<td align="right">473,259,912</td>
<td align="right">404,749,642</td>
<td align="right">-14.5%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">125,161,366</td>
<td align="right">108,200,657</td>
<td align="right">-13.6%</td>
</tr>
<tr>
<td align="left">FOR_ITER_GEN</td>
<td align="right">216,556,160</td>
<td align="right">187,384,391</td>
<td align="right">-13.5%</td>
</tr>
<tr>
<td align="left">STORE_FAST_STORE_FAST</td>
<td align="right">444,228,787</td>
<td align="right">386,941,922</td>
<td align="right">-12.9%</td>
</tr>
<tr>
<td align="left">LIST_APPEND</td>
<td align="right">73,755,837</td>
<td align="right">64,279,828</td>
<td align="right">-12.8%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">565,117,870</td>
<td align="right">492,605,156</td>
<td align="right">-12.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">1,730,881,850</td>
<td align="right">1,510,359,749</td>
<td align="right">-12.7%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">742,743,395</td>
<td align="right">656,368,061</td>
<td align="right">-11.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">5,403,454,722</td>
<td align="right">4,829,729,038</td>
<td align="right">-10.6%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">2,949,146,133</td>
<td align="right">2,644,311,710</td>
<td align="right">-10.3%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_LIST_INT</td>
<td align="right">110,674,162</td>
<td align="right">99,289,568</td>
<td align="right">-10.3%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">116,169,524</td>
<td align="right">104,621,265</td>
<td align="right">-9.9%</td>
</tr>
<tr>
<td align="left">PUSH_NULL</td>
<td align="right">1,220,347,480</td>
<td align="right">1,100,373,597</td>
<td align="right">-9.8%</td>
</tr>
<tr>
<td align="left">DICT_MERGE</td>
<td align="right">47,501,465</td>
<td align="right">42,885,905</td>
<td align="right">-9.7%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">5,572,824,234</td>
<td align="right">5,047,006,057</td>
<td align="right">-9.4%</td>
</tr>
<tr>
<td align="left">CALL_ISINSTANCE</td>
<td align="right">847,322,843</td>
<td align="right">767,737,576</td>
<td align="right">-9.4%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_LIST_INT</td>
<td align="right">459,821,224</td>
<td align="right">417,491,685</td>
<td align="right">-9.2%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">2,874,819,144</td>
<td align="right">2,633,689,554</td>
<td align="right">-8.4%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">6,266,916,404</td>
<td align="right">5,753,036,830</td>
<td align="right">-8.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">24,463,259,234</td>
<td align="right">22,543,291,643</td>
<td align="right">-7.8%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">3,554,152,670</td>
<td align="right">3,285,421,419</td>
<td align="right">-7.6%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">629,990,434</td>
<td align="right">584,612,824</td>
<td align="right">-7.2%</td>
</tr>
<tr>
<td align="left">BINARY_OP_INPLACE_ADD_UNICODE</td>
<td align="right">5,184,215</td>
<td align="right">4,824,622</td>
<td align="right">-6.9%</td>
</tr>
<tr>
<td align="left">BUILD_MAP</td>
<td align="right">132,417,005</td>
<td align="right">123,384,151</td>
<td align="right">-6.8%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">1,156,123,652</td>
<td align="right">1,226,847,767</td>
<td align="right">6.1%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">127,796,308</td>
<td align="right">120,198,302</td>
<td align="right">-5.9%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">468,892,081</td>
<td align="right">443,175,697</td>
<td align="right">-5.5%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_INT</td>
<td align="right">405,218,980</td>
<td align="right">383,282,398</td>
<td align="right">-5.4%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">4,288,051,307</td>
<td align="right">4,059,887,493</td>
<td align="right">-5.3%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_GETITEM</td>
<td align="right">65,671,849</td>
<td align="right">62,211,858</td>
<td align="right">-5.3%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_INT</td>
<td align="right">675,036,378</td>
<td align="right">640,996,668</td>
<td align="right">-5.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">856,098,414</td>
<td align="right">813,538,461</td>
<td align="right">-5.0%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">150,906,546</td>
<td align="right">143,755,008</td>
<td align="right">-4.7%</td>
</tr>
<tr>
<td align="left">LIST_EXTEND</td>
<td align="right">30,913,993</td>
<td align="right">29,475,086</td>
<td align="right">-4.7%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">2,751,522,273</td>
<td align="right">2,878,527,067</td>
<td align="right">4.6%</td>
</tr>
<tr>
<td align="left">BUILD_LIST</td>
<td align="right">224,167,795</td>
<td align="right">214,021,259</td>
<td align="right">-4.5%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">3,624,190,357</td>
<td align="right">3,460,544,546</td>
<td align="right">-4.5%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">249,403,786</td>
<td align="right">238,533,742</td>
<td align="right">-4.4%</td>
</tr>
<tr>
<td align="left">CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">194,633,593</td>
<td align="right">186,732,615</td>
<td align="right">-4.1%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST_WITH_KEYWORDS</td>
<td align="right">109,901,835</td>
<td align="right">105,472,243</td>
<td align="right">-4.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL_STR</td>
<td align="right">80,121,891</td>
<td align="right">76,953,205</td>
<td align="right">-4.0%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">6,888,435,350</td>
<td align="right">6,625,570,204</td>
<td align="right">-3.8%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">612,039,533</td>
<td align="right">588,931,611</td>
<td align="right">-3.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_MODULE</td>
<td align="right">541,081,798</td>
<td align="right">521,774,138</td>
<td align="right">-3.6%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">656,766,754</td>
<td align="right">635,503,755</td>
<td align="right">-3.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_WITH_HINT</td>
<td align="right">375,389,324</td>
<td align="right">364,277,134</td>
<td align="right">-3.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL_INT</td>
<td align="right">145,304,587</td>
<td align="right">141,457,593</td>
<td align="right">-2.6%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">1,349,969,615</td>
<td align="right">1,314,277,589</td>
<td align="right">-2.6%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_STR</td>
<td align="right">323,375,771</td>
<td align="right">314,958,382</td>
<td align="right">-2.6%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_LAZY_DICT</td>
<td align="right">254,158,260</td>
<td align="right">247,793,515</td>
<td align="right">-2.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right">122,239,867</td>
<td align="right">119,259,236</td>
<td align="right">-2.4%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_DICT</td>
<td align="right">150,147,413</td>
<td align="right">146,724,586</td>
<td align="right">-2.3%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">265,759,635</td>
<td align="right">259,803,575</td>
<td align="right">-2.2%</td>
</tr>
<tr>
<td align="left">NOP</td>
<td align="right">990,447,803</td>
<td align="right">969,449,391</td>
<td align="right">-2.1%</td>
</tr>
<tr>
<td align="left">TO_BOOL_LIST</td>
<td align="right">117,813,414</td>
<td align="right">115,332,615</td>
<td align="right">-2.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">4,208,176,497</td>
<td align="right">4,124,033,112</td>
<td align="right">-2.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_UNICODE</td>
<td align="right">74,036,228</td>
<td align="right">72,654,257</td>
<td align="right">-1.9%</td>
</tr>
<tr>
<td align="left">YIELD_VALUE</td>
<td align="right">1,380,637,122</td>
<td align="right">1,354,963,453</td>
<td align="right">-1.9%</td>
</tr>
<tr>
<td align="left">MAP_ADD</td>
<td align="right">39,903,235</td>
<td align="right">39,181,168</td>
<td align="right">-1.8%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT</td>
<td align="right">1,224,318,114</td>
<td align="right">1,203,326,262</td>
<td align="right">-1.7%</td>
</tr>
<tr>
<td align="left">MAKE_FUNCTION</td>
<td align="right">98,427,974</td>
<td align="right">96,740,376</td>
<td align="right">-1.7%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST_WITH_KEYWORDS</td>
<td align="right">44,476,081</td>
<td align="right">43,724,943</td>
<td align="right">-1.7%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_CLASS</td>
<td align="right">163,109,351</td>
<td align="right">160,416,791</td>
<td align="right">-1.7%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">374,504,478</td>
<td align="right">368,328,502</td>
<td align="right">-1.6%</td>
</tr>
<tr>
<td align="left">CALL_LEN</td>
<td align="right">306,152,679</td>
<td align="right">301,295,375</td>
<td align="right">-1.6%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NONE</td>
<td align="right">398,011,492</td>
<td align="right">391,967,889</td>
<td align="right">-1.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">1,727,598,308</td>
<td align="right">1,705,021,479</td>
<td align="right">-1.3%</td>
</tr>
<tr>
<td align="left">MAKE_CELL</td>
<td align="right">104,817,252</td>
<td align="right">103,498,498</td>
<td align="right">-1.3%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR</td>
<td align="right">133,782,895</td>
<td align="right">132,261,570</td>
<td align="right">-1.1%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NOT_NONE</td>
<td align="right">671,739,644</td>
<td align="right">664,864,416</td>
<td align="right">-1.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_AND_CLEAR</td>
<td align="right">70,409,762</td>
<td align="right">69,714,244</td>
<td align="right">-1.0%</td>
</tr>
<tr>
<td align="left">STORE_DEREF</td>
<td align="right">95,269,206</td>
<td align="right">94,332,003</td>
<td align="right">-1.0%</td>
</tr>
<tr>
<td align="left">CALL_INTRINSIC_1</td>
<td align="right">156,159,312</td>
<td align="right">154,765,274</td>
<td align="right">-0.9%</td>
</tr>
<tr>
<td align="left">CALL_PY_WITH_DEFAULTS</td>
<td align="right">218,350,989</td>
<td align="right">216,429,597</td>
<td align="right">-0.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_CLASS</td>
<td align="right">161,123,314</td>
<td align="right">159,727,205</td>
<td align="right">-0.9%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_O</td>
<td align="right">396,181,132</td>
<td align="right">393,010,037</td>
<td align="right">-0.8%</td>
</tr>
<tr>
<td align="left">COPY_FREE_VARS</td>
<td align="right">320,788,617</td>
<td align="right">318,264,988</td>
<td align="right">-0.8%</td>
</tr>
<tr>
<td align="left">BINARY_SLICE</td>
<td align="right">227,318,281</td>
<td align="right">225,606,968</td>
<td align="right">-0.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_PROPERTY</td>
<td align="right">64,919,974</td>
<td align="right">64,433,597</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_FLOAT</td>
<td align="right">75,850,126</td>
<td align="right">75,383,424</td>
<td align="right">-0.6%</td>
</tr>
<tr>
<td align="left">DICT_UPDATE</td>
<td align="right">73,270</td>
<td align="right">73,719</td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">END_FOR</td>
<td align="right">82,766,201</td>
<td align="right">82,356,380</td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">BINARY_OP_MULTIPLY_INT</td>
<td align="right">164,921,246</td>
<td align="right">164,106,094</td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">BEFORE_WITH</td>
<td align="right">10,114,048</td>
<td align="right">10,069,540</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">SET_FUNCTION_ATTRIBUTE</td>
<td align="right">84,900,569</td>
<td align="right">84,658,060</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_NO_DICT</td>
<td align="right">67,107,354</td>
<td align="right">66,934,129</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">INTERPRETER_EXIT</td>
<td align="right">2,305,730,427</td>
<td align="right">2,310,663,465</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">STORE_GLOBAL</td>
<td align="right">6,944,700</td>
<td align="right">6,929,920</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_CHECK</td>
<td align="right">11,125,025</td>
<td align="right">11,102,914</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">UNARY_NOT</td>
<td align="right">28,410,763</td>
<td align="right">28,355,101</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">2,055,305,412</td>
<td align="right">2,051,421,020</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">1,185,352,475</td>
<td align="right">1,183,185,508</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">DELETE_FAST</td>
<td align="right">2,230,377</td>
<td align="right">2,233,759</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">1,134,503,852</td>
<td align="right">1,132,978,584</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">INSTRUMENTED_FOR_ITER</td>
<td align="right">3,208</td>
<td align="right">3,212</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR_METHOD</td>
<td align="right">126,859,282</td>
<td align="right">126,701,256</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">75,212,980</td>
<td align="right">75,125,922</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">DELETE_SUBSCR</td>
<td align="right">176,488,563</td>
<td align="right">176,288,189</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">JUMP_FORWARD</td>
<td align="right">448,187,326</td>
<td align="right">447,733,245</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_STR_INT</td>
<td align="right">456,468,227</td>
<td align="right">456,053,029</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">TO_BOOL_ALWAYS_TRUE</td>
<td align="right">182,115,332</td>
<td align="right">181,976,180</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">CALL_FUNCTION_EX</td>
<td align="right">202,217,596</td>
<td align="right">202,073,711</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">UNARY_NEGATIVE</td>
<td align="right">146,012,301</td>
<td align="right">145,910,327</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">TO_BOOL_NONE</td>
<td align="right">502,436,739</td>
<td align="right">502,112,623</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">INSTRUMENTED_JUMP_BACKWARD</td>
<td align="right">6,248</td>
<td align="right">6,252</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_SLOT</td>
<td align="right">1,497,373,137</td>
<td align="right">1,498,123,725</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">INSTRUMENTED_POP_JUMP_IF_TRUE</td>
<td align="right">8,728</td>
<td align="right">8,732</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR</td>
<td align="right">23,570</td>
<td align="right">23,563</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">RETURN_GENERATOR</td>
<td align="right">505,456,543</td>
<td align="right">505,316,780</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">WITH_EXCEPT_START</td>
<td align="right">233,482</td>
<td align="right">233,508</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_KW</td>
<td align="right">273,966,124</td>
<td align="right">273,945,850</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">CHECK_EXC_MATCH</td>
<td align="right">24,467,337</td>
<td align="right">24,469,011</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">345,227</td>
<td align="right">345,249</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">RAISE_VARARGS</td>
<td align="right">6,185,641</td>
<td align="right">6,185,262</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_FLOAT</td>
<td align="right">181,060,689</td>
<td align="right">181,071,646</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">PUSH_EXC_INFO</td>
<td align="right">24,979,133</td>
<td align="right">24,980,622</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">POP_EXCEPT</td>
<td align="right">24,978,989</td>
<td align="right">24,980,476</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CLEANUP_THROW</td>
<td align="right">152,060</td>
<td align="right">152,069</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_LIST_APPEND</td>
<td align="right">348,157,774</td>
<td align="right">348,139,627</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">DELETE_ATTR</td>
<td align="right">6,693,090</td>
<td align="right">6,693,438</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">IMPORT_FROM</td>
<td align="right">13,104,379</td>
<td align="right">13,104,877</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_SLICE</td>
<td align="right">12,601,565</td>
<td align="right">12,601,994</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">IMPORT_NAME</td>
<td align="right">12,436,601</td>
<td align="right">12,436,886</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">GET_AWAITABLE</td>
<td align="right">229,795,045</td>
<td align="right">229,798,662</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">RERAISE</td>
<td align="right">3,848,270</td>
<td align="right">3,848,329</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_TUPLE_1</td>
<td align="right">28,251,738</td>
<td align="right">28,252,130</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BUILD_SET</td>
<td align="right">2,329,822</td>
<td align="right">2,329,791</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">BUILD_SLICE</td>
<td align="right">71,718,771</td>
<td align="right">71,719,579</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BEFORE_ASYNC_WITH</td>
<td align="right">3,005,920</td>
<td align="right">3,005,950</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">END_SEND</td>
<td align="right">402,623,100</td>
<td align="right">402,626,709</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">20,772,768</td>
<td align="right">20,772,591</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">SEND</td>
<td align="right">173,840,099</td>
<td align="right">173,841,266</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">SEND_GEN</td>
<td align="right">787,115,348</td>
<td align="right">787,120,260</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD_NO_INTERRUPT</td>
<td align="right">556,683,686</td>
<td align="right">556,686,256</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR_ATTR</td>
<td align="right">7,751,782</td>
<td align="right">7,751,753</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_WITH_HINT</td>
<td align="right">64,723,862</td>
<td align="right">64,724,040</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">GET_YIELD_FROM_ITER</td>
<td align="right">47,328,771</td>
<td align="right">47,328,803</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">EXIT_INIT_CHECK</td>
<td align="right">94,703,804</td>
<td align="right">94,703,860</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_ALLOC_AND_ENTER_INIT</td>
<td align="right">96,991,866</td>
<td align="right">96,991,922</td>
<td align="right">0.0%</td>
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
<td align="left">UNPACK_EX</td>
<td align="right">1,129,822</td>
<td align="right">1,129,822</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_NAME</td>
<td align="right">638,522</td>
<td align="right">638,522</td>
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
<td align="right">30,626</td>
<td align="right">30,626</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">INSTRUMENTED_POP_JUMP_IF_NOT_NONE</td>
<td align="right">4,800</td>
<td align="right">4,800</td>
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
<td align="right">1,667,279,825</td>
<td align="right">72.2%</td>
<td align="right">1,529,562,505</td>
<td align="right">71.2%</td>
<td align="right">-8.3%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">641,051,029</td>
<td align="right">27.7%</td>
<td align="right">617,954,600</td>
<td align="right">28.8%</td>
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
<td align="right">30,888,216</td>
<td align="right">1.3%</td>
<td align="right">30,888,253</td>
<td align="right">1.4%</td>
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
<td align="right">1,240,581</td>
<td align="right">66.1%</td>
<td align="right">1,229,276</td>
<td align="right">65.9%</td>
<td align="right">-0.9%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">636,139</td>
<td align="right">33.9%</td>
<td align="right">635,988</td>
<td align="right">34.1%</td>
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
<td align="left">xor</td>
<td align="right">9,867</td>
<td align="right">0.8%</td>
<td align="right">8,723</td>
<td align="right">0.7%</td>
<td align="right">-11.6%</td>
</tr>
<tr>
<td align="left">rshift</td>
<td align="right">9,996</td>
<td align="right">0.8%</td>
<td align="right">8,848</td>
<td align="right">0.7%</td>
<td align="right">-11.5%</td>
</tr>
<tr>
<td align="left">and int</td>
<td align="right">41,317</td>
<td align="right">3.3%</td>
<td align="right">37,109</td>
<td align="right">3.0%</td>
<td align="right">-10.2%</td>
</tr>
<tr>
<td align="left">true divide different types</td>
<td align="right">13,426</td>
<td align="right">1.1%</td>
<td align="right">12,673</td>
<td align="right">1.0%</td>
<td align="right">-5.6%</td>
</tr>
<tr>
<td align="left">or</td>
<td align="right">17,752</td>
<td align="right">1.4%</td>
<td align="right">17,114</td>
<td align="right">1.4%</td>
<td align="right">-3.6%</td>
</tr>
<tr>
<td align="left">lshift</td>
<td align="right">5,835</td>
<td align="right">0.5%</td>
<td align="right">5,705</td>
<td align="right">0.5%</td>
<td align="right">-2.2%</td>
</tr>
<tr>
<td align="left">true divide float</td>
<td align="right">5,767</td>
<td align="right">0.5%</td>
<td align="right">5,663</td>
<td align="right">0.5%</td>
<td align="right">-1.8%</td>
</tr>
<tr>
<td align="left">remainder</td>
<td align="right">54,155</td>
<td align="right">4.4%</td>
<td align="right">53,263</td>
<td align="right">4.3%</td>
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
<td align="left">add other</td>
<td align="right">64,835</td>
<td align="right">5.2%</td>
<td align="right">64,320</td>
<td align="right">5.2%</td>
<td align="right">-0.8%</td>
</tr>
<tr>
<td align="left">floor divide</td>
<td align="right">33,528</td>
<td align="right">2.7%</td>
<td align="right">33,272</td>
<td align="right">2.7%</td>
<td align="right">-0.8%</td>
</tr>
<tr>
<td align="left">power</td>
<td align="right">5,769</td>
<td align="right">0.5%</td>
<td align="right">5,741</td>
<td align="right">0.5%</td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">add different types</td>
<td align="right">78,819</td>
<td align="right">6.4%</td>
<td align="right">78,536</td>
<td align="right">6.4%</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">multiply different types</td>
<td align="right">92,379</td>
<td align="right">7.4%</td>
<td align="right">92,147</td>
<td align="right">7.5%</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">true divide other</td>
<td align="right">3,440</td>
<td align="right">0.3%</td>
<td align="right">3,447</td>
<td align="right">0.3%</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">subtract different types</td>
<td align="right">783,288</td>
<td align="right">63.1%</td>
<td align="right">782,506</td>
<td align="right">63.7%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">and other</td>
<td align="right">2,015</td>
<td align="right">0.2%</td>
<td align="right">2,016</td>
<td align="right">0.2%</td>
<td align="right">0.0%</td>
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
<td align="right">423,210,313</td>
<td align="right">19.4%</td>
<td align="right">331,242,561</td>
<td align="right">17.5%</td>
<td align="right">-21.7%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">1,756,995,427</td>
<td align="right">80.6%</td>
<td align="right">1,562,148,355</td>
<td align="right">82.5%</td>
<td align="right">-11.1%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">4,903,113</td>
<td align="right">0.2%</td>
<td align="right">4,901,521</td>
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
<td align="right">185,062</td>
<td align="right">47.8%</td>
<td align="right">159,564</td>
<td align="right">44.2%</td>
<td align="right">-13.8%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">201,880</td>
<td align="right">52.2%</td>
<td align="right">201,819</td>
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
<td align="right">57,099</td>
<td align="right">30.9%</td>
<td align="right">40,695</td>
<td align="right">25.5%</td>
<td align="right">-28.7%</td>
</tr>
<tr>
<td align="left">out of range</td>
<td align="right">76,537</td>
<td align="right">41.4%</td>
<td align="right">68,826</td>
<td align="right">43.1%</td>
<td align="right">-10.1%</td>
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
<td align="right">187</td>
<td align="right">0.1%</td>
<td align="right">183</td>
<td align="right">0.1%</td>
<td align="right">-2.1%</td>
</tr>
<tr>
<td align="left">buffer int</td>
<td align="right">22,723</td>
<td align="right">12.3%</td>
<td align="right">22,303</td>
<td align="right">14.0%</td>
<td align="right">-1.8%</td>
</tr>
<tr>
<td align="left">code complex parameters</td>
<td align="right">5,036</td>
<td align="right">2.7%</td>
<td align="right">5,017</td>
<td align="right">3.1%</td>
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
<td align="left">list slice</td>
<td align="right">1,360</td>
<td align="right">0.7%</td>
<td align="right">1,360</td>
<td align="right">0.9%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">buffer slice</td>
<td align="right">900</td>
<td align="right">0.5%</td>
<td align="right">900</td>
<td align="right">0.6%</td>
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
<td align="right">7,694,575,720</td>
<td align="right">84.2%</td>
<td align="right">6,881,491,783</td>
<td align="right">82.7%</td>
<td align="right">-10.6%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">253,885,648</td>
<td align="right">2.8%</td>
<td align="right">252,368,866</td>
<td align="right">3.0%</td>
<td align="right">-0.6%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">1,432,864,548</td>
<td align="right">15.7%</td>
<td align="right">1,429,209,889</td>
<td align="right">17.2%</td>
<td align="right">-0.3%</td>
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
<td align="right">5,419,952</td>
<td align="right">85.0%</td>
<td align="right">5,391,311</td>
<td align="right">85.0%</td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">953,623</td>
<td align="right">15.0%</td>
<td align="right">953,174</td>
<td align="right">15.0%</td>
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
<td align="left">cfunc noargs</td>
<td align="right">70,071</td>
<td align="right">7.3%</td>
<td align="right">69,578</td>
<td align="right">7.3%</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">method wrapper</td>
<td align="right">8,237</td>
<td align="right">0.9%</td>
<td align="right">8,263</td>
<td align="right">0.9%</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">bound method</td>
<td align="right">12,107</td>
<td align="right">1.3%</td>
<td align="right">12,089</td>
<td align="right">1.3%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">metaclass</td>
<td align="right">43,158</td>
<td align="right">4.5%</td>
<td align="right">43,202</td>
<td align="right">4.5%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">class mutable</td>
<td align="right">24,756</td>
<td align="right">2.6%</td>
<td align="right">24,738</td>
<td align="right">2.6%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">operator wrapper</td>
<td align="right">10,138</td>
<td align="right">1.1%</td>
<td align="right">10,142</td>
<td align="right">1.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">cfunc varargs keywords</td>
<td align="right">32,272</td>
<td align="right">3.4%</td>
<td align="right">32,261</td>
<td align="right">3.4%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">meth descr varargs</td>
<td align="right">16,509</td>
<td align="right">1.7%</td>
<td align="right">16,514</td>
<td align="right">1.7%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">cfunc varargs</td>
<td align="right">14,251</td>
<td align="right">1.5%</td>
<td align="right">14,255</td>
<td align="right">1.5%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">meth descr varargs keywords</td>
<td align="right">20,922</td>
<td align="right">2.2%</td>
<td align="right">20,917</td>
<td align="right">2.2%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">class no vectorcall</td>
<td align="right">78,833</td>
<td align="right">8.3%</td>
<td align="right">78,817</td>
<td align="right">8.3%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">init not inline values</td>
<td align="right">105,577</td>
<td align="right">11.1%</td>
<td align="right">105,558</td>
<td align="right">11.1%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">meth descr method fastcall keywords</td>
<td align="right">207,176</td>
<td align="right">21.7%</td>
<td align="right">207,203</td>
<td align="right">21.7%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">67,585</td>
<td align="right">7.1%</td>
<td align="right">67,593</td>
<td align="right">7.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">code complex parameters</td>
<td align="right">185,154</td>
<td align="right">19.4%</td>
<td align="right">185,167</td>
<td align="right">19.4%</td>
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
<td align="right">152,424,372</td>
<td align="right">8.1%</td>
<td align="right">145,283,096</td>
<td align="right">7.9%</td>
<td align="right">-4.7%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">1,726,890,514</td>
<td align="right">91.9%</td>
<td align="right">1,697,484,782</td>
<td align="right">92.1%</td>
<td align="right">-1.7%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">1,864,060</td>
<td align="right">0.1%</td>
<td align="right">1,871,508</td>
<td align="right">0.1%</td>
<td align="right">0.4%</td>
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
<td align="right">232,970</td>
<td align="right">67.3%</td>
<td align="right">230,023</td>
<td align="right">67.0%</td>
<td align="right">-1.3%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">113,264</td>
<td align="right">32.7%</td>
<td align="right">113,397</td>
<td align="right">33.0%</td>
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
<td align="left">set</td>
<td align="right">2,342</td>
<td align="right">1.0%</td>
<td align="right">1,663</td>
<td align="right">0.7%</td>
<td align="right">-29.0%</td>
</tr>
<tr>
<td align="left">baseobject</td>
<td align="right">33,713</td>
<td align="right">14.5%</td>
<td align="right">31,858</td>
<td align="right">13.8%</td>
<td align="right">-5.5%</td>
</tr>
<tr>
<td align="left">bytes</td>
<td align="right">4,120</td>
<td align="right">1.8%</td>
<td align="right">3,920</td>
<td align="right">1.7%</td>
<td align="right">-4.9%</td>
</tr>
<tr>
<td align="left">bool</td>
<td align="right">3,815</td>
<td align="right">1.6%</td>
<td align="right">3,780</td>
<td align="right">1.6%</td>
<td align="right">-0.9%</td>
</tr>
<tr>
<td align="left">different types</td>
<td align="right">55,125</td>
<td align="right">23.7%</td>
<td align="right">54,749</td>
<td align="right">23.8%</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">big int</td>
<td align="right">61,747</td>
<td align="right">26.5%</td>
<td align="right">62,135</td>
<td align="right">27.0%</td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">24,182</td>
<td align="right">10.4%</td>
<td align="right">24,075</td>
<td align="right">10.5%</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">14,616</td>
<td align="right">6.3%</td>
<td align="right">14,552</td>
<td align="right">6.3%</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">long float</td>
<td align="right">1,531</td>
<td align="right">0.7%</td>
<td align="right">1,537</td>
<td align="right">0.7%</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">float long</td>
<td align="right">16,465</td>
<td align="right">7.1%</td>
<td align="right">16,440</td>
<td align="right">7.1%</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">string</td>
<td align="right">11,080</td>
<td align="right">4.8%</td>
<td align="right">11,080</td>
<td align="right">4.8%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">4,234</td>
<td align="right">1.8%</td>
<td align="right">4,234</td>
<td align="right">1.8%</td>
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
<td align="right">636,133,583</td>
<td align="right">84.3%</td>
<td align="right">446,116,609</td>
<td align="right">80.6%</td>
<td align="right">-29.9%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">118,515,484</td>
<td align="right">15.7%</td>
<td align="right">106,973,611</td>
<td align="right">19.3%</td>
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
<td align="right">2,546,240</td>
<td align="right">0.3%</td>
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
<td align="right">132,774</td>
<td align="right">66.3%</td>
<td align="right">126,382</td>
<td align="right">65.2%</td>
<td align="right">-4.8%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">67,506</td>
<td align="right">33.7%</td>
<td align="right">67,512</td>
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
<td align="left">str</td>
<td align="right">37,064</td>
<td align="right">27.9%</td>
<td align="right">33,604</td>
<td align="right">26.6%</td>
<td align="right">-9.3%</td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">19,661</td>
<td align="right">14.8%</td>
<td align="right">18,148</td>
<td align="right">14.4%</td>
<td align="right">-7.7%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">28,868</td>
<td align="right">21.7%</td>
<td align="right">27,923</td>
<td align="right">22.1%</td>
<td align="right">-3.3%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">47,181</td>
<td align="right">35.5%</td>
<td align="right">46,707</td>
<td align="right">37.0%</td>
<td align="right">-1.0%</td>
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
<td align="right">101,947,356</td>
<td align="right">7.2%</td>
<td align="right">333,912</td>
<td align="right">0.1%</td>
<td align="right">-99.7%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">1,194,220,686</td>
<td align="right">83.9%</td>
<td align="right">251,520,948</td>
<td align="right">67.6%</td>
<td align="right">-78.9%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">227,560,293</td>
<td align="right">16.0%</td>
<td align="right">120,294,586</td>
<td align="right">32.3%</td>
<td align="right">-47.1%</td>
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
<td align="right">1,989,549</td>
<td align="right">91.1%</td>
<td align="right">72,390</td>
<td align="right">30.5%</td>
<td align="right">-96.4%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">193,822</td>
<td align="right">8.9%</td>
<td align="right">165,238</td>
<td align="right">69.5%</td>
<td align="right">-14.7%</td>
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
<td align="right">10,300</td>
<td align="right">5.3%</td>
<td align="right">6,060</td>
<td align="right">3.7%</td>
<td align="right">-41.2%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">14,459</td>
<td align="right">7.5%</td>
<td align="right">10,399</td>
<td align="right">6.3%</td>
<td align="right">-28.1%</td>
</tr>
<tr>
<td align="left">dict items</td>
<td align="right">67,030</td>
<td align="right">34.6%</td>
<td align="right">50,583</td>
<td align="right">30.6%</td>
<td align="right">-24.5%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">26,065</td>
<td align="right">13.4%</td>
<td align="right">22,757</td>
<td align="right">13.8%</td>
<td align="right">-12.7%</td>
</tr>
<tr>
<td align="left">itertools</td>
<td align="right">7,471</td>
<td align="right">3.9%</td>
<td align="right">7,249</td>
<td align="right">4.4%</td>
<td align="right">-3.0%</td>
</tr>
<tr>
<td align="left">dict keys</td>
<td align="right">14,756</td>
<td align="right">7.6%</td>
<td align="right">14,530</td>
<td align="right">8.8%</td>
<td align="right">-1.5%</td>
</tr>
<tr>
<td align="left">dict values</td>
<td align="right">7,050</td>
<td align="right">3.6%</td>
<td align="right">6,990</td>
<td align="right">4.2%</td>
<td align="right">-0.9%</td>
</tr>
<tr>
<td align="left">ascii string</td>
<td align="right">2,700</td>
<td align="right">1.4%</td>
<td align="right">2,680</td>
<td align="right">1.6%</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">enumerate</td>
<td align="right">20,052</td>
<td align="right">10.3%</td>
<td align="right">20,051</td>
<td align="right">12.1%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">zip</td>
<td align="right">14,352</td>
<td align="right">7.4%</td>
<td align="right">14,352</td>
<td align="right">8.7%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">reversed list</td>
<td align="right">7,885</td>
<td align="right">4.1%</td>
<td align="right">7,885</td>
<td align="right">4.8%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">map</td>
<td align="right">740</td>
<td align="right">0.4%</td>
<td align="right">740</td>
<td align="right">0.4%</td>
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
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">10,027,553,097</td>
<td align="right">87.5%</td>
<td align="right">9,631,507,452</td>
<td align="right">87.5%</td>
<td align="right">-3.9%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">1,417,833,832</td>
<td align="right">12.4%</td>
<td align="right">1,366,795,723</td>
<td align="right">12.4%</td>
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
<td align="right">575,182,744</td>
<td align="right">5.0%</td>
<td align="right">566,473,111</td>
<td align="right">5.1%</td>
<td align="right">-1.5%</td>
</tr>
<tr>
<td align="left">
deopt
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">684,621</td>
<td align="right">0.0%</td>
<td align="right">685,231</td>
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
<td align="right">1,710,778</td>
<td align="right">12.7%</td>
<td align="right">1,643,438</td>
<td align="right">12.4%</td>
<td align="right">-3.9%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">11,736,548</td>
<td align="right">87.3%</td>
<td align="right">11,572,411</td>
<td align="right">87.6%</td>
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
<td align="left">not managed dict</td>
<td align="right">301,304</td>
<td align="right">17.6%</td>
<td align="right">248,449</td>
<td align="right">15.1%</td>
<td align="right">-17.5%</td>
</tr>
<tr>
<td align="left">class method obj</td>
<td align="right">25,191</td>
<td align="right">1.5%</td>
<td align="right">21,933</td>
<td align="right">1.3%</td>
<td align="right">-12.9%</td>
</tr>
<tr>
<td align="left">not in keys</td>
<td align="right">16,560</td>
<td align="right">1.0%</td>
<td align="right">15,540</td>
<td align="right">0.9%</td>
<td align="right">-6.2%</td>
</tr>
<tr>
<td align="left">metaclass attribute</td>
<td align="right">195,161</td>
<td align="right">11.4%</td>
<td align="right">190,936</td>
<td align="right">11.6%</td>
<td align="right">-2.2%</td>
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
<td align="left">method</td>
<td align="right">120,344</td>
<td align="right">7.0%</td>
<td align="right">117,870</td>
<td align="right">7.2%</td>
<td align="right">-2.1%</td>
</tr>
<tr>
<td align="left">shadowed</td>
<td align="right">140,535</td>
<td align="right">8.2%</td>
<td align="right">138,628</td>
<td align="right">8.4%</td>
<td align="right">-1.4%</td>
</tr>
<tr>
<td align="left">non overriding descriptor</td>
<td align="right">13,710</td>
<td align="right">0.8%</td>
<td align="right">13,527</td>
<td align="right">0.8%</td>
<td align="right">-1.3%</td>
</tr>
<tr>
<td align="left">mutable class</td>
<td align="right">78,116</td>
<td align="right">4.6%</td>
<td align="right">77,297</td>
<td align="right">4.7%</td>
<td align="right">-1.0%</td>
</tr>
<tr>
<td align="left">non string or split</td>
<td align="right">22,112</td>
<td align="right">1.3%</td>
<td align="right">22,005</td>
<td align="right">1.3%</td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">class attr descriptor</td>
<td align="right">30,200</td>
<td align="right">1.8%</td>
<td align="right">30,160</td>
<td align="right">1.8%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">class attr simple</td>
<td align="right">718,919</td>
<td align="right">42.0%</td>
<td align="right">718,511</td>
<td align="right">43.7%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">overridden</td>
<td align="right">19,314</td>
<td align="right">1.1%</td>
<td align="right">19,321</td>
<td align="right">1.2%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">builtin class method</td>
<td align="right">3,818</td>
<td align="right">0.2%</td>
<td align="right">3,817</td>
<td align="right">0.2%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">module attr not found</td>
<td align="right">17,842</td>
<td align="right">1.0%</td>
<td align="right">17,842</td>
<td align="right">1.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">non object slot</td>
<td align="right">3,541</td>
<td align="right">0.2%</td>
<td align="right">3,541</td>
<td align="right">0.2%</td>
<td align="right">0.0%</td>
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
<td align="right">6,582,609,726</td>
<td align="right">99.7%</td>
<td align="right">5,707,707,580</td>
<td align="right">99.6%</td>
<td align="right">-13.3%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">456,151</td>
<td align="right">0.0%</td>
<td align="right">456,724</td>
<td align="right">0.0%</td>
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
<td align="right">20,560,749</td>
<td align="right">0.3%</td>
<td align="right">20,561,251</td>
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
<td align="right">13,103</td>
<td align="right">0.0%</td>
<td align="right">13,103</td>
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
<td align="right">668,170</td>
<td align="right">100.0%</td>
<td align="right">668,064</td>
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
<td align="right">134,611,064</td>
<td align="right">100.0%</td>
<td align="right">134,453,009</td>
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
<td align="right">11,853</td>
<td align="right">0.0%</td>
<td align="right">11,846</td>
<td align="right">0.0%</td>
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
<td align="right">173,802,111</td>
<td align="right">18.1%</td>
<td align="right">173,803,252</td>
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
<td align="right">787,084,448</td>
<td align="right">81.9%</td>
<td align="right">787,089,360</td>
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
<td align="right">7,144</td>
<td align="right">10.4%</td>
<td align="right">7,167</td>
<td align="right">10.4%</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">61,744</td>
<td align="right">89.6%</td>
<td align="right">61,747</td>
<td align="right">89.6%</td>
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
<td align="right">16,124</td>
<td align="right">26.1%</td>
<td align="right">16,127</td>
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
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">2,530,971,109</td>
<td align="right">91.3%</td>
<td align="right">2,530,171,835</td>
<td align="right">91.3%</td>
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
<td align="right">237,421,345</td>
<td align="right">8.6%</td>
<td align="right">237,358,811</td>
<td align="right">8.6%</td>
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
<td align="right">165,629,742</td>
<td align="right">6.0%</td>
<td align="right">165,654,514</td>
<td align="right">6.0%</td>
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
<td align="right">147,287</td>
<td align="right">4.3%</td>
<td align="right">147,078</td>
<td align="right">4.3%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">3,274,090</td>
<td align="right">95.7%</td>
<td align="right">3,274,547</td>
<td align="right">95.7%</td>
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
<td align="right">1,540</td>
<td align="right">1.0%</td>
<td align="right">1,500</td>
<td align="right">1.0%</td>
<td align="right">-2.6%</td>
</tr>
<tr>
<td align="left">class attr simple</td>
<td align="right">49,679</td>
<td align="right">33.7%</td>
<td align="right">49,539</td>
<td align="right">33.7%</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">not managed dict</td>
<td align="right">28,516</td>
<td align="right">19.4%</td>
<td align="right">28,508</td>
<td align="right">19.4%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">not in dict</td>
<td align="right">15,645</td>
<td align="right">10.6%</td>
<td align="right">15,645</td>
<td align="right">10.6%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">non string or split</td>
<td align="right">15,440</td>
<td align="right">10.5%</td>
<td align="right">15,440</td>
<td align="right">10.5%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">overriding descriptor</td>
<td align="right">10,660</td>
<td align="right">7.2%</td>
<td align="right">10,660</td>
<td align="right">7.2%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">not in keys</td>
<td align="right">7,781</td>
<td align="right">5.3%</td>
<td align="right">7,781</td>
<td align="right">5.3%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">overridden</td>
<td align="right">6,932</td>
<td align="right">4.7%</td>
<td align="right">6,932</td>
<td align="right">4.7%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">property</td>
<td align="right">5,280</td>
<td align="right">3.6%</td>
<td align="right">5,280</td>
<td align="right">3.6%</td>
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
<td align="right">260,818,675</td>
<td align="right">66.1%</td>
<td align="right">246,011,254</td>
<td align="right">65.0%</td>
<td align="right">-5.7%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">133,683,208</td>
<td align="right">33.9%</td>
<td align="right">132,163,647</td>
<td align="right">34.9%</td>
<td align="right">-1.1%</td>
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
<td align="right">83,875</td>
<td align="right">81.8%</td>
<td align="right">82,116</td>
<td align="right">81.4%</td>
<td align="right">-2.1%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">18,712</td>
<td align="right">18.2%</td>
<td align="right">18,707</td>
<td align="right">18.6%</td>
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
<td align="left">array int</td>
<td align="right">7,160</td>
<td align="right">8.5%</td>
<td align="right">6,560</td>
<td align="right">8.0%</td>
<td align="right">-8.4%</td>
</tr>
<tr>
<td align="left">bytearray int</td>
<td align="right">1,400</td>
<td align="right">1.7%</td>
<td align="right">1,340</td>
<td align="right">1.6%</td>
<td align="right">-4.3%</td>
</tr>
<tr>
<td align="left">out of range</td>
<td align="right">2,108</td>
<td align="right">2.5%</td>
<td align="right">2,028</td>
<td align="right">2.5%</td>
<td align="right">-3.8%</td>
</tr>
<tr>
<td align="left">dict subclass no override</td>
<td align="right">28,291</td>
<td align="right">33.7%</td>
<td align="right">27,610</td>
<td align="right">33.6%</td>
<td align="right">-2.4%</td>
</tr>
<tr>
<td align="left">py simple</td>
<td align="right">42,836</td>
<td align="right">51.1%</td>
<td align="right">42,498</td>
<td align="right">51.8%</td>
<td align="right">-0.8%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">2,080</td>
<td align="right">2.5%</td>
<td align="right">2,080</td>
<td align="right">2.5%</td>
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
<td align="right">3,738,961,837</td>
<td align="right">91.4%</td>
<td align="right">3,424,334,949</td>
<td align="right">90.9%</td>
<td align="right">-8.4%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">349,967,609</td>
<td align="right">8.6%</td>
<td align="right">339,054,734</td>
<td align="right">9.0%</td>
<td align="right">-3.1%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">103,395,125</td>
<td align="right">2.5%</td>
<td align="right">103,347,483</td>
<td align="right">2.7%</td>
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
<td align="right">596,035</td>
<td align="right">21.1%</td>
<td align="right">592,120</td>
<td align="right">20.9%</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">2,235,267</td>
<td align="right">78.9%</td>
<td align="right">2,234,371</td>
<td align="right">79.1%</td>
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
<td align="left">dict</td>
<td align="right">33,533</td>
<td align="right">5.6%</td>
<td align="right">31,561</td>
<td align="right">5.3%</td>
<td align="right">-5.9%</td>
</tr>
<tr>
<td align="left">mapping</td>
<td align="right">58,941</td>
<td align="right">9.9%</td>
<td align="right">57,852</td>
<td align="right">9.8%</td>
<td align="right">-1.8%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">40,673</td>
<td align="right">6.8%</td>
<td align="right">40,254</td>
<td align="right">6.8%</td>
<td align="right">-1.0%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">95,464</td>
<td align="right">16.0%</td>
<td align="right">95,112</td>
<td align="right">16.1%</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">float</td>
<td align="right">2,320</td>
<td align="right">0.4%</td>
<td align="right">2,327</td>
<td align="right">0.4%</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">number</td>
<td align="right">152,394</td>
<td align="right">25.6%</td>
<td align="right">152,317</td>
<td align="right">25.7%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">sequence</td>
<td align="right">18,019</td>
<td align="right">3.0%</td>
<td align="right">18,027</td>
<td align="right">3.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">174,331</td>
<td align="right">29.2%</td>
<td align="right">174,312</td>
<td align="right">29.4%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">bytes</td>
<td align="right">18,700</td>
<td align="right">3.1%</td>
<td align="right">18,698</td>
<td align="right">3.2%</td>
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
<td align="right">3,160</td>
<td align="right">0.0%</td>
<td align="right">1,060</td>
<td align="right">0.0%</td>
<td align="right">-66.5%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">665,766,834</td>
<td align="right">99.9%</td>
<td align="right">463,834,080</td>
<td align="right">99.9%</td>
<td align="right">-30.3%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">500,468</td>
<td align="right">0.1%</td>
<td align="right">410,791</td>
<td align="right">0.1%</td>
<td align="right">-17.9%</td>
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
<td align="right">3,519</td>
<td align="right">8.1%</td>
<td align="right">-1.6%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">39,889</td>
<td align="right">91.8%</td>
<td align="right">39,826</td>
<td align="right">91.9%</td>
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
<td align="right">380</td>
<td align="right">10.6%</td>
<td align="right">340</td>
<td align="right">9.7%</td>
<td align="right">-10.5%</td>
</tr>
<tr>
<td align="left">sequence</td>
<td align="right">2,517</td>
<td align="right">70.3%</td>
<td align="right">2,498</td>
<td align="right">71.0%</td>
<td align="right">-0.8%</td>
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
<td align="right">46,239,685,214</td>
<td align="right">35.4%</td>
<td align="right">41,873,567,967</td>
<td align="right">34.8%</td>
<td align="right">-9.4%</td>
</tr>
<tr>
<td align="left">
Specialized misses
<details>
<summary>ⓘ</summary>

Specialized instructions, e.g. `LOAD_ATTR_MODULE` that deopt.
</details>
</td>
<td align="right">1,240,921,353</td>
<td align="right">0.9%</td>
<td align="right">1,129,061,702</td>
<td align="right">0.9%</td>
<td align="right">-9.0%</td>
</tr>
<tr>
<td align="left">
Basic
<details>
<summary>ⓘ</summary>

Instructions that are not and cannot be specialized, e.g. `LOAD_FAST`.
</details>
</td>
<td align="right">71,137,032,440</td>
<td align="right">54.4%</td>
<td align="right">65,885,615,331</td>
<td align="right">54.7%</td>
<td align="right">-7.4%</td>
</tr>
<tr>
<td align="left">
Not specialized
<details>
<summary>ⓘ</summary>

Instructions that could be specialized but aren't, e.g. `LOAD_ATTR`, `BINARY_SLICE`.
</details>
</td>
<td align="right">12,159,252,683</td>
<td align="right">9.3%</td>
<td align="right">11,490,839,399</td>
<td align="right">9.5%</td>
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
<td align="right">227,560,293</td>
<td align="right">4.3%</td>
<td align="right">120,294,586</td>
<td align="right">2.4%</td>
<td align="right">-47.1%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR</td>
<td align="right">423,210,313</td>
<td align="right">7.9%</td>
<td align="right">331,242,561</td>
<td align="right">6.6%</td>
<td align="right">-21.7%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">152,424,372</td>
<td align="right">2.9%</td>
<td align="right">145,283,096</td>
<td align="right">2.9%</td>
<td align="right">-4.7%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">641,051,029</td>
<td align="right">12.0%</td>
<td align="right">617,954,600</td>
<td align="right">12.3%</td>
<td align="right">-3.6%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">1,417,833,832</td>
<td align="right">26.6%</td>
<td align="right">1,366,795,723</td>
<td align="right">27.2%</td>
<td align="right">-3.6%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">349,967,609</td>
<td align="right">6.6%</td>
<td align="right">339,054,734</td>
<td align="right">6.8%</td>
<td align="right">-3.1%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR</td>
<td align="right">133,683,208</td>
<td align="right">2.5%</td>
<td align="right">132,163,647</td>
<td align="right">2.6%</td>
<td align="right">-1.1%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">1,432,864,548</td>
<td align="right">26.9%</td>
<td align="right">1,429,209,889</td>
<td align="right">28.5%</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">237,421,345</td>
<td align="right">4.5%</td>
<td align="right">237,358,811</td>
<td align="right">4.7%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">SEND</td>
<td align="right">173,802,111</td>
<td align="right">3.3%</td>
<td align="right">173,803,252</td>
<td align="right">3.5%</td>
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
<td align="right">163,858,931</td>
<td align="right">13.2%</td>
<td align="right">158,326,195</td>
<td align="right">14.0%</td>
<td align="right">-3.4%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">129,607,366</td>
<td align="right">10.4%</td>
<td align="right">128,102,568</td>
<td align="right">11.3%</td>
<td align="right">-1.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">180,881,840</td>
<td align="right">14.6%</td>
<td align="right">178,852,325</td>
<td align="right">15.8%</td>
<td align="right">-1.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">109,404,539</td>
<td align="right">8.8%</td>
<td align="right">109,151,218</td>
<td align="right">9.7%</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">TO_BOOL_NONE</td>
<td align="right">47,964,450</td>
<td align="right">3.9%</td>
<td align="right">47,940,123</td>
<td align="right">4.2%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_SLOT</td>
<td align="right">94,997,512</td>
<td align="right">7.7%</td>
<td align="right">95,022,161</td>
<td align="right">8.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right">59,618,556</td>
<td align="right">4.8%</td>
<td align="right">59,605,263</td>
<td align="right">5.3%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">70,579,429</td>
<td align="right">5.7%</td>
<td align="right">70,579,480</td>
<td align="right">6.3%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">50,928,041</td>
<td align="right">4.1%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">FOR_ITER_TUPLE</td>
<td align="right">50,777,595</td>
<td align="right">4.1%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">TO_BOOL_ALWAYS_TRUE</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">47,514,686</td>
<td align="right">4.2%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">42,208,207</td>
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
<td align="right">4,418,464</td>
<td align="right">0.1%</td>
<td align="right">2,658,304</td>
<td align="right">0.0%</td>
<td align="right">-39.8%</td>
</tr>
<tr>
<td align="left">Calls to Python functions inlined</td>
<td align="right">6,430,564,768</td>
<td align="right">73.6%</td>
<td align="right">6,383,607,238</td>
<td align="right">73.4%</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (slot)</td>
<td align="right">475,820,883</td>
<td align="right">5.4%</td>
<td align="right">479,291,261</td>
<td align="right">5.5%</td>
<td align="right">0.7%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (generator)</td>
<td align="right">861,521,757</td>
<td align="right">9.9%</td>
<td align="right">864,825,196</td>
<td align="right">9.9%</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (function vectorcall)</td>
<td align="right">1,443,426,549</td>
<td align="right">16.5%</td>
<td align="right">1,446,817,201</td>
<td align="right">16.6%</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">Frames pushed</td>
<td align="right">6,969,714,659</td>
<td align="right">79.7%</td>
<td align="right">6,953,521,544</td>
<td align="right">79.9%</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">Calls to PyEval_EvalDefault</td>
<td align="right">2,309,397,396</td>
<td align="right">26.4%</td>
<td align="right">2,314,331,327</td>
<td align="right">26.6%</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (total)</td>
<td align="right">2,309,397,396</td>
<td align="right">26.4%</td>
<td align="right">2,314,331,327</td>
<td align="right">26.6%</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (api)</td>
<td align="right">256,376,850</td>
<td align="right">2.9%</td>
<td align="right">256,719,844</td>
<td align="right">3.0%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (vector)</td>
<td align="right">1,447,875,639</td>
<td align="right">16.6%</td>
<td align="right">1,449,506,131</td>
<td align="right">16.7%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (function ex)</td>
<td align="right">38,363,616</td>
<td align="right">0.4%</td>
<td align="right">38,367,785</td>
<td align="right">0.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (method)</td>
<td align="right">213,142,814</td>
<td align="right">2.4%</td>
<td align="right">213,152,055</td>
<td align="right">2.5%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Frame objects created</td>
<td align="right">88,460,474</td>
<td align="right">1.0%</td>
<td align="right">88,463,456</td>
<td align="right">1.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (build class)</td>
<td align="right">30,626</td>
<td align="right">0.0%</td>
<td align="right">30,626</td>
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
<td align="left">Method cache misses</td>
<td align="right">80,240,775</td>
<td align="right"></td>
<td align="right">77,919,356</td>
<td align="right"></td>
<td align="right">-2.9%</td>
</tr>
<tr>
<td align="left">Method cache collisions</td>
<td align="right">84,170,022</td>
<td align="right"></td>
<td align="right">81,786,425</td>
<td align="right"></td>
<td align="right">-2.8%</td>
</tr>
<tr>
<td align="left">Increfs</td>
<td align="right">26,874,476,919</td>
<td align="right">22.4%</td>
<td align="right">27,229,276,154</td>
<td align="right">22.6%</td>
<td align="right">1.3%</td>
</tr>
<tr>
<td align="left">Decrefs</td>
<td align="right">29,727,046,882</td>
<td align="right">21.6%</td>
<td align="right">30,083,899,156</td>
<td align="right">21.9%</td>
<td align="right">1.2%</td>
</tr>
<tr>
<td align="left">Method cache hits</td>
<td align="right">3,127,433,204</td>
<td align="right"></td>
<td align="right">3,108,439,650</td>
<td align="right"></td>
<td align="right">-0.6%</td>
</tr>
<tr>
<td align="left">Method cache dunder misses</td>
<td align="right">11,685,328</td>
<td align="right"></td>
<td align="right">11,621,008</td>
<td align="right"></td>
<td align="right">-0.6%</td>
</tr>
<tr>
<td align="left">Allocations from freelist</td>
<td align="right">6,756,403,250</td>
<td align="right">36.6%</td>
<td align="right">6,743,157,728</td>
<td align="right">36.6%</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">Frees to freelist</td>
<td align="right">6,758,378,990</td>
<td align="right"></td>
<td align="right">6,745,154,055</td>
<td align="right"></td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">Allocations to 512 bytes</td>
<td align="right">11,577,940,055</td>
<td align="right">62.7%</td>
<td align="right">11,560,542,167</td>
<td align="right">62.7%</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">Interpreter decrefs</td>
<td align="right">107,670,742,345</td>
<td align="right">78.4%</td>
<td align="right">107,510,686,470</td>
<td align="right">78.1%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">Allocations</td>
<td align="right">11,703,910,640</td>
<td align="right">63.4%</td>
<td align="right">11,686,539,129</td>
<td align="right">63.4%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">Frees</td>
<td align="right">12,032,406,012</td>
<td align="right"></td>
<td align="right">12,014,689,291</td>
<td align="right"></td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">Interpreter increfs</td>
<td align="right">93,134,166,259</td>
<td align="right">77.6%</td>
<td align="right">93,001,395,448</td>
<td align="right">77.4%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">Inline values</td>
<td align="right">182,643,696</td>
<td align="right"></td>
<td align="right">182,552,122</td>
<td align="right"></td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">Allocations to 4 kbytes</td>
<td align="right">104,803,839</td>
<td align="right">0.6%</td>
<td align="right">104,828,878</td>
<td align="right">0.6%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Method cache dunder hits</td>
<td align="right">3,560,202,170</td>
<td align="right"></td>
<td align="right">3,559,830,074</td>
<td align="right"></td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">Allocations over 4 kbytes</td>
<td align="right">21,166,746</td>
<td align="right">0.1%</td>
<td align="right">21,168,084</td>
<td align="right">0.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Materialize dict (on request)</td>
<td align="right">3,309,383</td>
<td align="right">1.8%</td>
<td align="right">3,309,383</td>
<td align="right">1.8%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Materialize dict (new key)</td>
<td align="right">116,295</td>
<td align="right">0.1%</td>
<td align="right">116,295</td>
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
<td align="right">115,793,224</td>
<td align="right">17,037,827,159</td>
<td align="right">0</td>
<td align="right">115,768,569</td>
<td align="right">17,039,091,424</td>
</tr>
<tr>
<td align="right">2</td>
<td align="right">0</td>
<td align="right">10,755,840</td>
<td align="right">6,965,888,980</td>
<td align="right">0</td>
<td align="right">10,755,840</td>
<td align="right">6,968,307,060</td>
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
<td align="right">1,491</td>
<td align="right">0.2%</td>
<td align="right">2,273</td>
<td align="right">0.3%</td>
<td align="right">52.4%</td>
</tr>
<tr>
<td align="left">
Trace stack overflow
<details>
<summary>ⓘ</summary>

A trace is truncated because it would require more than 5 stack frames.
</details>
</td>
<td align="right">610</td>
<td align="right">0.1%</td>
<td align="right">861</td>
<td align="right">0.1%</td>
<td align="right">41.1%</td>
</tr>
<tr>
<td align="left">
Traces created
<details>
<summary>ⓘ</summary>

The number of traces that were successfully created.
</details>
</td>
<td align="right">108,613</td>
<td align="right">16.5%</td>
<td align="right">137,911</td>
<td align="right">18.5%</td>
<td align="right">27.0%</td>
</tr>
<tr>
<td align="left">
Low confidence
<details>
<summary>ⓘ</summary>

A trace is abandoned because the likelihood of the jump to top being taken is too low.
</details>
</td>
<td align="right">6,776</td>
<td align="right">1.0%</td>
<td align="right">7,984</td>
<td align="right">1.1%</td>
<td align="right">17.8%</td>
</tr>
<tr>
<td align="left">
Optimization attempts
<details>
<summary>ⓘ</summary>

The number of times a potential trace is identified.  Specifically, this occurs in the JUMP BACKWARD instruction when the counter reaches a threshold.
</details>
</td>
<td align="right">658,747</td>
<td align="right"></td>
<td align="right">745,667</td>
<td align="right"></td>
<td align="right">13.2%</td>
</tr>
<tr>
<td align="left">
Inner loop found
<details>
<summary>ⓘ</summary>

A trace is truncated because it has an inner loop
</details>
</td>
<td align="right">16,397</td>
<td align="right">2.5%</td>
<td align="right">18,273</td>
<td align="right">2.5%</td>
<td align="right">11.4%</td>
</tr>
<tr>
<td align="left">
Traces executed
<details>
<summary>ⓘ</summary>

The number of traces that were executed
</details>
</td>
<td align="right">6,384,678,694</td>
<td align="right"></td>
<td align="right">7,064,740,082</td>
<td align="right"></td>
<td align="right">10.7%</td>
</tr>
<tr>
<td align="left">
Trace too short
<details>
<summary>ⓘ</summary>

A potential trace is abandoced because it it too short.
</details>
</td>
<td align="right">550,134</td>
<td align="right">83.5%</td>
<td align="right">607,756</td>
<td align="right">81.5%</td>
<td align="right">10.5%</td>
</tr>
<tr>
<td align="left">
Uops executed
<details>
<summary>ⓘ</summary>

The total number of uops (micro-operations) that were executed
</details>
</td>
<td align="right">174,740,783,936</td>
<td align="right">2,736.9%</td>
<td align="right">192,652,703,788</td>
<td align="right">2,727.0%</td>
<td align="right">10.3%</td>
</tr>
<tr>
<td align="left">
Trace stack underflow
<details>
<summary>ⓘ</summary>

A potential trace is abandoned because it pops more frames than it pushes.
</details>
</td>
<td align="right">133,876</td>
<td align="right">20.3%</td>
<td align="right">124,922</td>
<td align="right">16.8%</td>
<td align="right">-6.7%</td>
</tr>
<tr>
<td align="left">
Executors invalidated
<details>
<summary>ⓘ</summary>

The number of executors that were invalidated due to watched dictionary changes.
</details>
</td>
<td align="right">5,460</td>
<td align="right">5.0%</td>
<td align="right">5,640</td>
<td align="right">4.1%</td>
<td align="right">3.3%</td>
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
<td align="right">106,453</td>
<td align="right">98.0%</td>
<td align="right">135,731</td>
<td align="right">98.4%</td>
<td align="right">27.5%</td>
</tr>
<tr>
<td align="left">
Optimizer attempts
<details>
<summary>ⓘ</summary>

The number of times the trace optimizer (_Py_uop_analyze_and_optimize) was run.
</details>
</td>
<td align="right">108,613</td>
<td align="right"></td>
<td align="right">137,911</td>
<td align="right"></td>
<td align="right">27.0%</td>
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
<td align="right">2.0%</td>
<td align="right">2,120</td>
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
<td align="right">2,800</td>
<td align="right">2.6%</td>
<td align="right">3,248</td>
<td align="right">2.4%</td>
<td align="right">16.0%</td>
</tr>
<tr>
<td align="left"><= 16</td>
<td align="right">16,970</td>
<td align="right">15.6%</td>
<td align="right">22,957</td>
<td align="right">16.6%</td>
<td align="right">35.3%</td>
</tr>
<tr>
<td align="left"><= 32</td>
<td align="right">41,823</td>
<td align="right">38.5%</td>
<td align="right">53,514</td>
<td align="right">38.8%</td>
<td align="right">28.0%</td>
</tr>
<tr>
<td align="left"><= 64</td>
<td align="right">26,806</td>
<td align="right">24.7%</td>
<td align="right">32,817</td>
<td align="right">23.8%</td>
<td align="right">22.4%</td>
</tr>
<tr>
<td align="left"><= 128</td>
<td align="right">14,872</td>
<td align="right">13.7%</td>
<td align="right">18,619</td>
<td align="right">13.5%</td>
<td align="right">25.2%</td>
</tr>
<tr>
<td align="left"><= 256</td>
<td align="right">4,477</td>
<td align="right">4.1%</td>
<td align="right">5,705</td>
<td align="right">4.1%</td>
<td align="right">27.4%</td>
</tr>
<tr>
<td align="left"><= 512</td>
<td align="right">865</td>
<td align="right">0.8%</td>
<td align="right">1,051</td>
<td align="right">0.8%</td>
<td align="right">21.5%</td>
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
<td align="right">618</td>
<td align="right">0.6%</td>
<td align="right">588</td>
<td align="right">0.4%</td>
<td align="right">-4.9%</td>
</tr>
<tr>
<td align="left"><= 8</td>
<td align="right">8,987</td>
<td align="right">8.3%</td>
<td align="right">10,311</td>
<td align="right">7.5%</td>
<td align="right">14.7%</td>
</tr>
<tr>
<td align="left"><= 16</td>
<td align="right">34,262</td>
<td align="right">31.5%</td>
<td align="right">44,559</td>
<td align="right">32.3%</td>
<td align="right">30.1%</td>
</tr>
<tr>
<td align="left"><= 32</td>
<td align="right">35,268</td>
<td align="right">32.5%</td>
<td align="right">45,771</td>
<td align="right">33.2%</td>
<td align="right">29.8%</td>
</tr>
<tr>
<td align="left"><= 64</td>
<td align="right">17,969</td>
<td align="right">16.5%</td>
<td align="right">22,745</td>
<td align="right">16.5%</td>
<td align="right">26.6%</td>
</tr>
<tr>
<td align="left"><= 128</td>
<td align="right">7,304</td>
<td align="right">6.7%</td>
<td align="right">9,294</td>
<td align="right">6.7%</td>
<td align="right">27.2%</td>
</tr>
<tr>
<td align="left"><= 256</td>
<td align="right">1,825</td>
<td align="right">1.7%</td>
<td align="right">2,283</td>
<td align="right">1.7%</td>
<td align="right">25.1%</td>
</tr>
<tr>
<td align="left"><= 512</td>
<td align="right">220</td>
<td align="right">0.2%</td>
<td align="right">180</td>
<td align="right">0.1%</td>
<td align="right">-18.2%</td>
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
<td align="right">25,552,980</td>
<td align="right">0.4%</td>
<td align="right">25,847,900</td>
<td align="right">0.4%</td>
<td align="right">1.2%</td>
</tr>
<tr>
<td align="left"><= 4</td>
<td align="right">558,987,328</td>
<td align="right">8.8%</td>
<td align="right">934,633,179</td>
<td align="right">13.2%</td>
<td align="right">67.2%</td>
</tr>
<tr>
<td align="left"><= 8</td>
<td align="right">805,881,078</td>
<td align="right">12.6%</td>
<td align="right">750,157,748</td>
<td align="right">10.6%</td>
<td align="right">-6.9%</td>
</tr>
<tr>
<td align="left"><= 16</td>
<td align="right">1,158,943,194</td>
<td align="right">18.2%</td>
<td align="right">1,249,410,003</td>
<td align="right">17.7%</td>
<td align="right">7.8%</td>
</tr>
<tr>
<td align="left"><= 32</td>
<td align="right">1,126,019,934</td>
<td align="right">17.6%</td>
<td align="right">1,119,710,540</td>
<td align="right">15.8%</td>
<td align="right">-0.6%</td>
</tr>
<tr>
<td align="left"><= 64</td>
<td align="right">590,288,587</td>
<td align="right">9.2%</td>
<td align="right">633,305,790</td>
<td align="right">9.0%</td>
<td align="right">7.3%</td>
</tr>
<tr>
<td align="left"><= 128</td>
<td align="right">280,212,423</td>
<td align="right">4.4%</td>
<td align="right">346,214,276</td>
<td align="right">4.9%</td>
<td align="right">23.6%</td>
</tr>
<tr>
<td align="left"><= 256</td>
<td align="right">145,394,037</td>
<td align="right">2.3%</td>
<td align="right">193,798,715</td>
<td align="right">2.7%</td>
<td align="right">33.3%</td>
</tr>
<tr>
<td align="left"><= 512</td>
<td align="right">15,941,920</td>
<td align="right">0.2%</td>
<td align="right">19,329,949</td>
<td align="right">0.3%</td>
<td align="right">21.3%</td>
</tr>
<tr>
<td align="left"><= 1,024</td>
<td align="right">6,387,288</td>
<td align="right">0.1%</td>
<td align="right">6,475,163</td>
<td align="right">0.1%</td>
<td align="right">1.4%</td>
</tr>
<tr>
<td align="left"><= 2,048</td>
<td align="right">17,713,607</td>
<td align="right">0.3%</td>
<td align="right">17,716,418</td>
<td align="right">0.3%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left"><= 4,096</td>
<td align="right">644,610</td>
<td align="right">0.0%</td>
<td align="right">644,613</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left"><= 8,192</td>
<td align="right">744,953</td>
<td align="right">0.0%</td>
<td align="right">744,854</td>
<td align="right">0.0%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left"><= 16,384</td>
<td align="right">245,680</td>
<td align="right">0.0%</td>
<td align="right">245,641</td>
<td align="right">0.0%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left"><= 32,768</td>
<td align="right">42,640</td>
<td align="right">0.0%</td>
<td align="right">43,742</td>
<td align="right">0.0%</td>
<td align="right">2.6%</td>
</tr>
<tr>
<td align="left"><= 65,536</td>
<td align="right">13,522</td>
<td align="right">0.0%</td>
<td align="right">13,474</td>
<td align="right">0.0%</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left"><= 131,072</td>
<td align="right">718</td>
<td align="right">0.0%</td>
<td align="right">726</td>
<td align="right">0.0%</td>
<td align="right">1.1%</td>
</tr>
<tr>
<td align="left"><= 262,144</td>
<td align="right">2,081</td>
<td align="right">0.0%</td>
<td align="right">2,080</td>
<td align="right">0.0%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left"><= 524,288</td>
<td align="right">465</td>
<td align="right">0.0%</td>
<td align="right">463</td>
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
<td align="right">226</td>
<td align="right">0.0%</td>
<td align="right">223</td>
<td align="right">0.0%</td>
<td align="right">-1.3%</td>
</tr>
<tr>
<td align="left"><= 4,194,304</td>
<td align="right">254</td>
<td align="right">0.0%</td>
<td align="right">257</td>
<td align="right">0.0%</td>
<td align="right">1.2%</td>
</tr>
<tr>
<td align="left"><= 8,388,608</td>
<td align="right">160</td>
<td align="right">0.0%</td>
<td align="right">160</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left"><= 16,777,216</td>
<td align="right">80</td>
<td align="right">0.0%</td>
<td align="right">80</td>
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
<td align="left">_CONVERT_VALUE</td>
<td align="right">790,640</td>
<td align="right">51,694,900</td>
<td align="right">6,438.4%</td>
</tr>
<tr>
<td align="left">_BUILD_STRING</td>
<td align="right">595,780</td>
<td align="right">25,514,709</td>
<td align="right">4,182.6%</td>
</tr>
<tr>
<td align="left">_FORMAT_SIMPLE</td>
<td align="right">1,407,265</td>
<td align="right">52,353,890</td>
<td align="right">3,620.3%</td>
</tr>
<tr>
<td align="left">_BUILD_CONST_KEY_MAP</td>
<td align="right">79,650</td>
<td align="right">2,484,290</td>
<td align="right">3,019.0%</td>
</tr>
<tr>
<td align="left">_FOR_ITER_TIER_TWO</td>
<td align="right">409,001,924</td>
<td align="right">1,721,015,791</td>
<td align="right">320.8%</td>
</tr>
<tr>
<td align="left">_GUARD_BUILTINS_VERSION</td>
<td align="right">38,636</td>
<td align="right">104,126</td>
<td align="right">169.5%</td>
</tr>
<tr>
<td align="left">_BUILD_MAP</td>
<td align="right">9,901,904</td>
<td align="right">16,832,714</td>
<td align="right">70.0%</td>
</tr>
<tr>
<td align="left">_DICT_MERGE</td>
<td align="right">7,203,052</td>
<td align="right">11,664,351</td>
<td align="right">61.9%</td>
</tr>
<tr>
<td align="left">_UNPACK_SEQUENCE_TUPLE</td>
<td align="right">188,189,848</td>
<td align="right">295,541,170</td>
<td align="right">57.0%</td>
</tr>
<tr>
<td align="left">_SET_ADD</td>
<td align="right">1,449,155</td>
<td align="right">2,174,524</td>
<td align="right">50.1%</td>
</tr>
<tr>
<td align="left">_BINARY_SUBSCR_DICT</td>
<td align="right">258,335,884</td>
<td align="right">373,130,637</td>
<td align="right">44.4%</td>
</tr>
<tr>
<td align="left">_ITER_NEXT_TUPLE</td>
<td align="right">311,537,512</td>
<td align="right">179,076,706</td>
<td align="right">-42.5%</td>
</tr>
<tr>
<td align="left">_GUARD_NOT_EXHAUSTED_TUPLE</td>
<td align="right">466,113,547</td>
<td align="right">268,226,001</td>
<td align="right">-42.5%</td>
</tr>
<tr>
<td align="left">_ITER_CHECK_TUPLE</td>
<td align="right">543,325,254</td>
<td align="right">320,389,252</td>
<td align="right">-41.0%</td>
</tr>
<tr>
<td align="left">_CALL_TYPE_1</td>
<td align="right">237,518,532</td>
<td align="right">332,556,982</td>
<td align="right">40.0%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_4</td>
<td align="right">448,283,677</td>
<td align="right">624,688,605</td>
<td align="right">39.4%</td>
</tr>
<tr>
<td align="left">_POP_FRAME</td>
<td align="right">553,459,322</td>
<td align="right">769,297,991</td>
<td align="right">39.0%</td>
</tr>
<tr>
<td align="left">_STORE_DEREF</td>
<td align="right">2,930,205</td>
<td align="right">3,872,310</td>
<td align="right">32.2%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_6</td>
<td align="right">417,149,373</td>
<td align="right">548,863,820</td>
<td align="right">31.6%</td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_FAST</td>
<td align="right">789,171,882</td>
<td align="right">1,025,852,443</td>
<td align="right">30.0%</td>
</tr>
<tr>
<td align="left">_LOAD_CONST_INLINE_BORROW_WITH_NULL</td>
<td align="right">363,952,069</td>
<td align="right">462,221,550</td>
<td align="right">27.0%</td>
</tr>
<tr>
<td align="left">_CALL_ISINSTANCE</td>
<td align="right">310,101,290</td>
<td align="right">386,394,018</td>
<td align="right">24.6%</td>
</tr>
<tr>
<td align="left">_MAKE_CELL</td>
<td align="right">5,624,238</td>
<td align="right">6,955,737</td>
<td align="right">23.7%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">909,957,339</td>
<td align="right">1,121,968,670</td>
<td align="right">23.3%</td>
</tr>
<tr>
<td align="left">_LOAD_CONST_INLINE_WITH_NULL</td>
<td align="right">1,652,778,714</td>
<td align="right">2,031,005,453</td>
<td align="right">22.9%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_5</td>
<td align="right">647,138,016</td>
<td align="right">791,519,693</td>
<td align="right">22.3%</td>
</tr>
<tr>
<td align="left">_GUARD_KEYS_VERSION</td>
<td align="right">1,002,892,547</td>
<td align="right">1,224,297,548</td>
<td align="right">22.1%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_3</td>
<td align="right">625,069,614</td>
<td align="right">761,692,746</td>
<td align="right">21.9%</td>
</tr>
<tr>
<td align="left">_LOAD_GLOBAL_MODULE</td>
<td align="right">44,267,468</td>
<td align="right">53,900,910</td>
<td align="right">21.8%</td>
</tr>
<tr>
<td align="left">_GUARD_DORV_VALUES_INST_ATTR_FROM_DICT</td>
<td align="right">1,046,016,143</td>
<td align="right">1,273,163,997</td>
<td align="right">21.7%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_5</td>
<td align="right">2,019,775,156</td>
<td align="right">2,429,986,325</td>
<td align="right">20.3%</td>
</tr>
<tr>
<td align="left">_ERROR_POP_N</td>
<td align="right">486,581</td>
<td align="right">585,251</td>
<td align="right">20.3%</td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_FAST_WITH_KEYWORDS</td>
<td align="right">21,923,504</td>
<td align="right">26,360,067</td>
<td align="right">20.2%</td>
</tr>
<tr>
<td align="left">_LOAD_DEREF</td>
<td align="right">447,044,593</td>
<td align="right">533,364,626</td>
<td align="right">19.3%</td>
</tr>
<tr>
<td align="left">_GUARD_GLOBALS_VERSION</td>
<td align="right">50,855,144</td>
<td align="right">60,554,076</td>
<td align="right">19.1%</td>
</tr>
<tr>
<td align="left">_POP_TOP</td>
<td align="right">698,656,321</td>
<td align="right">828,752,072</td>
<td align="right">18.6%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_4</td>
<td align="right">1,937,249,037</td>
<td align="right">2,296,653,419</td>
<td align="right">18.6%</td>
</tr>
<tr>
<td align="left">_CONTAINS_OP_DICT</td>
<td align="right">360,120,901</td>
<td align="right">425,175,935</td>
<td align="right">18.1%</td>
</tr>
<tr>
<td align="left">_CHECK_VALIDITY</td>
<td align="right">9,784,804,309</td>
<td align="right">11,552,040,861</td>
<td align="right">18.1%</td>
</tr>
<tr>
<td align="left">_LOAD_CONST_INLINE</td>
<td align="right">1,232,540,884</td>
<td align="right">1,445,764,519</td>
<td align="right">17.3%</td>
</tr>
<tr>
<td align="left">_STORE_FAST</td>
<td align="right">2,894,267,668</td>
<td align="right">3,391,673,904</td>
<td align="right">17.2%</td>
</tr>
<tr>
<td align="left">_CHECK_PERIODIC</td>
<td align="right">2,126,956,931</td>
<td align="right">2,489,804,182</td>
<td align="right">17.1%</td>
</tr>
<tr>
<td align="left">_RESUME_CHECK</td>
<td align="right">1,306,478,467</td>
<td align="right">1,527,459,523</td>
<td align="right">16.9%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_2</td>
<td align="right">704,141,268</td>
<td align="right">822,636,930</td>
<td align="right">16.8%</td>
</tr>
<tr>
<td align="left">_SET_IP</td>
<td align="right">16,290,625,093</td>
<td align="right">18,992,094,348</td>
<td align="right">16.6%</td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_O</td>
<td align="right">614,587,265</td>
<td align="right">716,453,885</td>
<td align="right">16.6%</td>
</tr>
<tr>
<td align="left">_PUSH_FRAME</td>
<td align="right">1,525,952,108</td>
<td align="right">1,763,028,362</td>
<td align="right">15.5%</td>
</tr>
<tr>
<td align="left">_SAVE_RETURN_OFFSET</td>
<td align="right">1,525,952,108</td>
<td align="right">1,763,028,362</td>
<td align="right">15.5%</td>
</tr>
<tr>
<td align="left">_SIDE_EXIT</td>
<td align="right">3,633,030,464</td>
<td align="right">4,186,046,862</td>
<td align="right">15.2%</td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION_EXACT_ARGS</td>
<td align="right">1,587,721,494</td>
<td align="right">1,828,422,701</td>
<td align="right">15.2%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_BOOL</td>
<td align="right">1,935,626,673</td>
<td align="right">2,226,877,663</td>
<td align="right">15.0%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_2</td>
<td align="right">2,672,145,754</td>
<td align="right">3,072,894,235</td>
<td align="right">15.0%</td>
</tr>
<tr>
<td align="left">_PUSH_NULL</td>
<td align="right">727,573,282</td>
<td align="right">836,133,800</td>
<td align="right">14.9%</td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_O</td>
<td align="right">22,210,757</td>
<td align="right">25,391,224</td>
<td align="right">14.3%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_3</td>
<td align="right">3,095,907,163</td>
<td align="right">3,539,019,330</td>
<td align="right">14.3%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_4</td>
<td align="right">656,367,168</td>
<td align="right">749,914,238</td>
<td align="right">14.3%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_STR</td>
<td align="right">24,373,012</td>
<td align="right">27,824,955</td>
<td align="right">14.2%</td>
</tr>
<tr>
<td align="left">_DELETE_SUBSCR</td>
<td align="right">1,428,140</td>
<td align="right">1,629,645</td>
<td align="right">14.1%</td>
</tr>
<tr>
<td align="left">_UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">618,279,498</td>
<td align="right">704,360,980</td>
<td align="right">13.9%</td>
</tr>
<tr>
<td align="left">_POP_TOP_LOAD_CONST_INLINE_BORROW</td>
<td align="right">1,239,857</td>
<td align="right">1,398,926</td>
<td align="right">12.8%</td>
</tr>
<tr>
<td align="left">_START_EXECUTOR</td>
<td align="right">4,733,018,165</td>
<td align="right">5,298,296,394</td>
<td align="right">11.9%</td>
</tr>
<tr>
<td align="left">_CHECK_ATTR_WITH_HINT</td>
<td align="right">98,013,587</td>
<td align="right">109,202,342</td>
<td align="right">11.4%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_WITH_HINT</td>
<td align="right">97,902,726</td>
<td align="right">109,076,561</td>
<td align="right">11.4%</td>
</tr>
<tr>
<td align="left">_BINARY_SUBSCR_TUPLE_INT</td>
<td align="right">147,486,496</td>
<td align="right">163,913,333</td>
<td align="right">11.1%</td>
</tr>
<tr>
<td align="left">_IS_OP</td>
<td align="right">332,331,159</td>
<td align="right">369,208,696</td>
<td align="right">11.1%</td>
</tr>
<tr>
<td align="left">_CHECK_STACK_SPACE_OPERAND</td>
<td align="right">866,198,719</td>
<td align="right">961,080,486</td>
<td align="right">11.0%</td>
</tr>
<tr>
<td align="left">_CONTAINS_OP</td>
<td align="right">107,359,752</td>
<td align="right">118,970,640</td>
<td align="right">10.8%</td>
</tr>
<tr>
<td align="left">_BUILD_TUPLE</td>
<td align="right">373,249,696</td>
<td align="right">413,249,458</td>
<td align="right">10.7%</td>
</tr>
<tr>
<td align="left">_CHECK_STACK_SPACE</td>
<td align="right">164,482,661</td>
<td align="right">180,825,139</td>
<td align="right">9.9%</td>
</tr>
<tr>
<td align="left">_ITER_CHECK_RANGE</td>
<td align="right">750,712,552</td>
<td align="right">677,811,660</td>
<td align="right">-9.7%</td>
</tr>
<tr>
<td align="left">_GUARD_NOT_EXHAUSTED_RANGE</td>
<td align="right">749,354,792</td>
<td align="right">677,274,340</td>
<td align="right">-9.6%</td>
</tr>
<tr>
<td align="left">_ITER_NEXT_RANGE</td>
<td align="right">701,785,981</td>
<td align="right">634,773,165</td>
<td align="right">-9.5%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST</td>
<td align="right">5,367,690,266</td>
<td align="right">5,863,545,677</td>
<td align="right">9.2%</td>
</tr>
<tr>
<td align="left">_GUARD_TYPE_VERSION</td>
<td align="right">5,361,511,474</td>
<td align="right">5,832,046,788</td>
<td align="right">8.8%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_1</td>
<td align="right">524,960,453</td>
<td align="right">570,501,489</td>
<td align="right">8.7%</td>
</tr>
<tr>
<td align="left">_BINARY_SUBSCR</td>
<td align="right">1,143,996,653</td>
<td align="right">1,239,459,801</td>
<td align="right">8.3%</td>
</tr>
<tr>
<td align="left">_CONTAINS_OP_SET</td>
<td align="right">1,477,441,867</td>
<td align="right">1,600,213,639</td>
<td align="right">8.3%</td>
</tr>
<tr>
<td align="left">_ITER_NEXT_LIST</td>
<td align="right">1,206,685,719</td>
<td align="right">1,111,881,877</td>
<td align="right">-7.9%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_MODULE</td>
<td align="right">6,480,220</td>
<td align="right">6,988,910</td>
<td align="right">7.8%</td>
</tr>
<tr>
<td align="left">_CHECK_ATTR_MODULE</td>
<td align="right">6,483,660</td>
<td align="right">6,992,350</td>
<td align="right">7.8%</td>
</tr>
<tr>
<td align="left">_CHECK_VALIDITY_AND_SET_IP</td>
<td align="right">1,005,675,852</td>
<td align="right">1,084,285,992</td>
<td align="right">7.8%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_3</td>
<td align="right">56,641,656</td>
<td align="right">61,047,407</td>
<td align="right">7.8%</td>
</tr>
<tr>
<td align="left">_COMPARE_OP</td>
<td align="right">92,916,486</td>
<td align="right">100,002,260</td>
<td align="right">7.6%</td>
</tr>
<tr>
<td align="left">_GUARD_NOT_EXHAUSTED_LIST</td>
<td align="right">1,492,507,133</td>
<td align="right">1,379,251,849</td>
<td align="right">-7.6%</td>
</tr>
<tr>
<td align="left">_JUMP_TO_TOP</td>
<td align="right">2,070,178,009</td>
<td align="right">2,225,729,509</td>
<td align="right">7.5%</td>
</tr>
<tr>
<td align="left">_GET_ITER</td>
<td align="right">243,838,951</td>
<td align="right">260,822,011</td>
<td align="right">7.0%</td>
</tr>
<tr>
<td align="left">_COLD_EXIT</td>
<td align="right">1,651,660,529</td>
<td align="right">1,766,443,688</td>
<td align="right">6.9%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_0</td>
<td align="right">5,322,375,744</td>
<td align="right">5,690,782,768</td>
<td align="right">6.9%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_NOT_NONE_POP</td>
<td align="right">148,443,222</td>
<td align="right">158,684,759</td>
<td align="right">6.9%</td>
</tr>
<tr>
<td align="left">_CHECK_ATTR_METHOD_LAZY_DICT</td>
<td align="right">97,230,587</td>
<td align="right">103,932,440</td>
<td align="right">6.9%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_METHOD_LAZY_DICT</td>
<td align="right">97,230,587</td>
<td align="right">103,932,440</td>
<td align="right">6.9%</td>
</tr>
<tr>
<td align="left">_CHECK_ATTR_CLASS</td>
<td align="right">25,012,663</td>
<td align="right">26,734,220</td>
<td align="right">6.9%</td>
</tr>
<tr>
<td align="left">_LOAD_CONST_INLINE_BORROW</td>
<td align="right">8,893,101,302</td>
<td align="right">9,504,717,903</td>
<td align="right">6.9%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_1</td>
<td align="right">6,198,949,157</td>
<td align="right">6,593,454,630</td>
<td align="right">6.4%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_CLASS_0</td>
<td align="right">23,413,597</td>
<td align="right">24,831,552</td>
<td align="right">6.1%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_1</td>
<td align="right">1,849,536,227</td>
<td align="right">1,961,531,354</td>
<td align="right">6.1%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_FALSE_POP</td>
<td align="right">5,302,587,128</td>
<td align="right">5,618,019,699</td>
<td align="right">5.9%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_MULTIPLY_FLOAT</td>
<td align="right">1,092,307,840</td>
<td align="right">1,156,304,421</td>
<td align="right">5.9%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_ADD_UNICODE</td>
<td align="right">23,610,827</td>
<td align="right">24,992,830</td>
<td align="right">5.9%</td>
</tr>
<tr>
<td align="left">_COPY</td>
<td align="right">1,252,538,335</td>
<td align="right">1,324,785,964</td>
<td align="right">5.8%</td>
</tr>
<tr>
<td align="left">_UNPACK_SEQUENCE</td>
<td align="right">1,554,949</td>
<td align="right">1,642,976</td>
<td align="right">5.7%</td>
</tr>
<tr>
<td align="left">_CHECK_CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">73,679,783</td>
<td align="right">77,771,562</td>
<td align="right">5.6%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">73,626,343</td>
<td align="right">77,704,562</td>
<td align="right">5.5%</td>
</tr>
<tr>
<td align="left">_LIST_APPEND</td>
<td align="right">182,692,353</td>
<td align="right">192,098,901</td>
<td align="right">5.1%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBTRACT_INT</td>
<td align="right">442,127,853</td>
<td align="right">464,073,644</td>
<td align="right">5.0%</td>
</tr>
<tr>
<td align="left">_GUARD_BOTH_FLOAT</td>
<td align="right">1,491,030,657</td>
<td align="right">1,564,304,650</td>
<td align="right">4.9%</td>
</tr>
<tr>
<td align="left">_ITER_CHECK_LIST</td>
<td align="right">1,506,885,886</td>
<td align="right">1,435,417,721</td>
<td align="right">-4.7%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_NONDESCRIPTOR_NO_DICT</td>
<td align="right">21,767,672</td>
<td align="right">22,756,360</td>
<td align="right">4.5%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_INSTANCE_VALUE_0</td>
<td align="right">1,881,863,722</td>
<td align="right">1,965,191,981</td>
<td align="right">4.4%</td>
</tr>
<tr>
<td align="left">_CHECK_MANAGED_OBJECT_HAS_VALUES</td>
<td align="right">1,885,638,478</td>
<td align="right">1,969,109,140</td>
<td align="right">4.4%</td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_CLASS</td>
<td align="right">56,786,823</td>
<td align="right">59,187,329</td>
<td align="right">4.2%</td>
</tr>
<tr>
<td align="left">_UNPACK_SEQUENCE_LIST</td>
<td align="right">77,567,280</td>
<td align="right">80,800,669</td>
<td align="right">4.2%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">828,889,024</td>
<td align="right">863,086,288</td>
<td align="right">4.1%</td>
</tr>
<tr>
<td align="left">_BUILD_LIST</td>
<td align="right">245,586,305</td>
<td align="right">255,612,085</td>
<td align="right">4.1%</td>
</tr>
<tr>
<td align="left">_BINARY_SUBSCR_LIST_INT</td>
<td align="right">1,056,076,314</td>
<td align="right">1,098,725,631</td>
<td align="right">4.0%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_AND_CLEAR</td>
<td align="right">15,847,431</td>
<td align="right">16,474,902</td>
<td align="right">4.0%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_INSTANCE_VALUE_1</td>
<td align="right">3,664,036</td>
<td align="right">3,802,299</td>
<td align="right">3.8%</td>
</tr>
<tr>
<td align="left">_UNARY_INVERT</td>
<td align="right">12,534,740</td>
<td align="right">12,975,938</td>
<td align="right">3.5%</td>
</tr>
<tr>
<td align="left">_MAP_ADD</td>
<td align="right">20,604,990</td>
<td align="right">21,327,549</td>
<td align="right">3.5%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_TRUE_POP</td>
<td align="right">2,570,092,598</td>
<td align="right">2,660,098,150</td>
<td align="right">3.5%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_2</td>
<td align="right">104,642,778</td>
<td align="right">108,251,150</td>
<td align="right">3.4%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS</td>
<td align="right">9,619,674</td>
<td align="right">9,944,690</td>
<td align="right">3.4%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right">88,764,007</td>
<td align="right">91,641,185</td>
<td align="right">3.2%</td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">184,249,586</td>
<td align="right">190,176,597</td>
<td align="right">3.2%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR</td>
<td align="right">1,106,604,588</td>
<td align="right">1,142,167,372</td>
<td align="right">3.2%</td>
</tr>
<tr>
<td align="left">_EXIT_TRACE</td>
<td align="right">2,746,755,367</td>
<td align="right">2,662,193,268</td>
<td align="right">-3.1%</td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">225,929,108</td>
<td align="right">232,652,705</td>
<td align="right">3.0%</td>
</tr>
<tr>
<td align="left">_MAKE_FUNCTION</td>
<td align="right">60,638,547</td>
<td align="right">62,350,401</td>
<td align="right">2.8%</td>
</tr>
<tr>
<td align="left">_TO_BOOL</td>
<td align="right">240,513,128</td>
<td align="right">247,168,895</td>
<td align="right">2.8%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_ADD_FLOAT</td>
<td align="right">539,783,780</td>
<td align="right">554,482,740</td>
<td align="right">2.7%</td>
</tr>
<tr>
<td align="left">_BINARY_OP</td>
<td align="right">855,001,077</td>
<td align="right">877,810,819</td>
<td align="right">2.7%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_6</td>
<td align="right">1,242,739,475</td>
<td align="right">1,275,401,630</td>
<td align="right">2.6%</td>
</tr>
<tr>
<td align="left">_CALL_STR_1</td>
<td align="right">66,199,794</td>
<td align="right">67,904,176</td>
<td align="right">2.6%</td>
</tr>
<tr>
<td align="left">_CALL_LEN</td>
<td align="right">195,811,121</td>
<td align="right">200,655,326</td>
<td align="right">2.5%</td>
</tr>
<tr>
<td align="left">_STORE_SUBSCR_LIST_INT</td>
<td align="right">478,857,462</td>
<td align="right">490,242,542</td>
<td align="right">2.4%</td>
</tr>
<tr>
<td align="left">_GUARD_BOTH_INT</td>
<td align="right">3,164,640,474</td>
<td align="right">3,239,439,364</td>
<td align="right">2.4%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_SLOT_0</td>
<td align="right">702,980,631</td>
<td align="right">719,063,101</td>
<td align="right">2.3%</td>
</tr>
<tr>
<td align="left">_LOAD_GLOBAL</td>
<td align="right">188,824,192</td>
<td align="right">184,590,013</td>
<td align="right">-2.2%</td>
</tr>
<tr>
<td align="left">_COMPARE_OP_INT</td>
<td align="right">943,376,513</td>
<td align="right">964,241,962</td>
<td align="right">2.2%</td>
</tr>
<tr>
<td align="left">_SWAP</td>
<td align="right">1,130,197,428</td>
<td align="right">1,153,978,759</td>
<td align="right">2.1%</td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_FAST_WITH_KEYWORDS</td>
<td align="right">153,743,278</td>
<td align="right">156,794,722</td>
<td align="right">2.0%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_0</td>
<td align="right">204,628,651</td>
<td align="right">208,513,314</td>
<td align="right">1.9%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_0</td>
<td align="right">381,803,870</td>
<td align="right">388,595,021</td>
<td align="right">1.8%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_INT</td>
<td align="right">194,777,207</td>
<td align="right">198,114,158</td>
<td align="right">1.7%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_7</td>
<td align="right">1,202,244,236</td>
<td align="right">1,220,278,224</td>
<td align="right">1.5%</td>
</tr>
<tr>
<td align="left">_CALL_INTRINSIC_1</td>
<td align="right">96,026,990</td>
<td align="right">97,434,652</td>
<td align="right">1.5%</td>
</tr>
<tr>
<td align="left">_LIST_EXTEND</td>
<td align="right">96,944,070</td>
<td align="right">98,351,732</td>
<td align="right">1.5%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_ADD_INT</td>
<td align="right">2,489,554,504</td>
<td align="right">2,523,603,431</td>
<td align="right">1.4%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_NONE_POP</td>
<td align="right">42,856,522</td>
<td align="right">43,434,351</td>
<td align="right">1.3%</td>
</tr>
<tr>
<td align="left">_GUARD_DORV_NO_DICT</td>
<td align="right">104,009,177</td>
<td align="right">105,368,269</td>
<td align="right">1.3%</td>
</tr>
<tr>
<td align="left">_BINARY_SLICE</td>
<td align="right">119,832,775</td>
<td align="right">121,387,397</td>
<td align="right">1.3%</td>
</tr>
<tr>
<td align="left">_STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">102,701,417</td>
<td align="right">104,019,049</td>
<td align="right">1.3%</td>
</tr>
<tr>
<td align="left">_COPY_FREE_VARS</td>
<td align="right">49,435,693</td>
<td align="right">50,066,785</td>
<td align="right">1.3%</td>
</tr>
<tr>
<td align="left">_STORE_GLOBAL</td>
<td align="right">1,260,560</td>
<td align="right">1,275,340</td>
<td align="right">1.2%</td>
</tr>
<tr>
<td align="left">_DEOPT</td>
<td align="right">1,099,501,120</td>
<td align="right">1,111,664,281</td>
<td align="right">1.1%</td>
</tr>
<tr>
<td align="left">_STORE_SUBSCR_DICT</td>
<td align="right">143,857,088</td>
<td align="right">145,407,146</td>
<td align="right">1.1%</td>
</tr>
<tr>
<td align="left">_LOAD_GLOBAL_BUILTINS</td>
<td align="right">6,587,676</td>
<td align="right">6,653,166</td>
<td align="right">1.0%</td>
</tr>
<tr>
<td align="left">_GUARD_BOTH_UNICODE</td>
<td align="right">965,839,847</td>
<td align="right">975,191,161</td>
<td align="right">1.0%</td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION</td>
<td align="right">1,272,011,416</td>
<td align="right">1,261,878,320</td>
<td align="right">-0.8%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_7</td>
<td align="right">3,376,749,538</td>
<td align="right">3,401,477,326</td>
<td align="right">0.7%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_LIST</td>
<td align="right">53,699,886</td>
<td align="right">54,088,192</td>
<td align="right">0.7%</td>
</tr>
<tr>
<td align="left">_SET_FUNCTION_ATTRIBUTE</td>
<td align="right">47,055,823</td>
<td align="right">47,323,773</td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">_STORE_ATTR_SLOT</td>
<td align="right">123,486,482</td>
<td align="right">122,797,264</td>
<td align="right">-0.6%</td>
</tr>
<tr>
<td align="left">_STORE_SUBSCR</td>
<td align="right">317,347,295</td>
<td align="right">318,866,682</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">_COMPARE_OP_STR</td>
<td align="right">1,825,052,835</td>
<td align="right">1,833,448,642</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_MULTIPLY_INT</td>
<td align="right">184,971,256</td>
<td align="right">185,788,242</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_NONE</td>
<td align="right">173,061,678</td>
<td align="right">173,801,642</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">_UNARY_NEGATIVE</td>
<td align="right">25,045,790</td>
<td align="right">25,147,729</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">_REPLACE_WITH_TRUE</td>
<td align="right">32,161,270</td>
<td align="right">32,271,177</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">_STORE_ATTR</td>
<td align="right">52,902,273</td>
<td align="right">52,986,941</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBTRACT_FLOAT</td>
<td align="right">382,602,700</td>
<td align="right">383,046,880</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_CHECK</td>
<td align="right">252,123</td>
<td align="right">251,912</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">_UNARY_NOT</td>
<td align="right">62,209,899</td>
<td align="right">62,242,721</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">_BINARY_SUBSCR_STR_INT</td>
<td align="right">1,215,773,756</td>
<td align="right">1,216,189,056</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_COMPARE_OP_FLOAT</td>
<td align="right">70,083,237</td>
<td align="right">70,080,276</td>
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
<td align="right">139,781,460</td>
<td align="right">139,781,460</td>
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
<td align="left">_LOAD_ATTR_CLASS_1</td>
<td align="right">3,840</td>
<td align="right">3,840</td>
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
<td align="right">2,396,080</td>
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
<td align="left">CALL_FUNCTION_EX</td>
<td align="right">2,780</td>
<td align="right">6,000</td>
<td align="right">115.8%</td>
</tr>
<tr>
<td align="left">IMPORT_NAME</td>
<td align="right">266</td>
<td align="right">409</td>
<td align="right">53.8%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_WITH_HINT</td>
<td align="right">180</td>
<td align="right">240</td>
<td align="right">33.3%</td>
</tr>
<tr>
<td align="left">CALL_ALLOC_AND_ENTER_INIT</td>
<td align="right">1,424</td>
<td align="right">1,884</td>
<td align="right">32.3%</td>
</tr>
<tr>
<td align="left">CALL_LIST_APPEND</td>
<td align="right">5,991</td>
<td align="right">7,671</td>
<td align="right">28.0%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">126,902</td>
<td align="right">161,454</td>
<td align="right">27.2%</td>
</tr>
<tr>
<td align="left">CALL_PY_WITH_DEFAULTS</td>
<td align="right">9,180</td>
<td align="right">11,678</td>
<td align="right">27.2%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_GETITEM</td>
<td align="right">2,521</td>
<td align="right">3,200</td>
<td align="right">26.9%</td>
</tr>
<tr>
<td align="left">BUILD_SET</td>
<td align="right">226</td>
<td align="right">285</td>
<td align="right">26.1%</td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">34,739</td>
<td align="right">43,581</td>
<td align="right">25.5%</td>
</tr>
<tr>
<td align="left">BINARY_OP_INPLACE_ADD_UNICODE</td>
<td align="right">583</td>
<td align="right">703</td>
<td align="right">20.6%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_PROPERTY</td>
<td align="right">6,943</td>
<td align="right">8,349</td>
<td align="right">20.3%</td>
</tr>
<tr>
<td align="left">YIELD_VALUE</td>
<td align="right">119,078</td>
<td align="right">140,949</td>
<td align="right">18.4%</td>
</tr>
<tr>
<td align="left">CALL_KW</td>
<td align="right">25,327</td>
<td align="right">29,176</td>
<td align="right">15.2%</td>
</tr>
<tr>
<td align="left">RETURN_GENERATOR</td>
<td align="right">40,954</td>
<td align="right">44,675</td>
<td align="right">9.1%</td>
</tr>
<tr>
<td align="left">FOR_ITER_GEN</td>
<td align="right">52,303</td>
<td align="right">48,123</td>
<td align="right">-8.0%</td>
</tr>
<tr>
<td align="left">SEND</td>
<td align="right">31,240</td>
<td align="right">31,240</td>
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
<td align="right">240</td>
<td align="right">240</td>
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
Stats gathered on: 2024-04-19
