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
<td align="left">UNARY_INVERT</td>
<td align="right">1,882,777</td>
<td align="right">2,613,747</td>
<td align="right">38.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_WITH_HINT</td>
<td align="right">376,019,382</td>
<td align="right">255,054,949</td>
<td align="right">-32.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_PROPERTY</td>
<td align="right">72,062,376</td>
<td align="right">62,565,389</td>
<td align="right">-13.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_CLASS</td>
<td align="right">161,115,860</td>
<td align="right">140,637,471</td>
<td align="right">-12.7%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">150,711,732</td>
<td align="right">139,418,830</td>
<td align="right">-7.5%</td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">76,839,182</td>
<td align="right">71,360,891</td>
<td align="right">-7.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_NO_DICT</td>
<td align="right">67,107,369</td>
<td align="right">62,518,982</td>
<td align="right">-6.8%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST_WITH_KEYWORDS</td>
<td align="right">44,470,981</td>
<td align="right">42,318,829</td>
<td align="right">-4.8%</td>
</tr>
<tr>
<td align="left">TO_BOOL_INT</td>
<td align="right">143,052,411</td>
<td align="right">136,441,945</td>
<td align="right">-4.6%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">109,139,845</td>
<td align="right">104,540,831</td>
<td align="right">-4.2%</td>
</tr>
<tr>
<td align="left">LIST_EXTEND</td>
<td align="right">30,687,156</td>
<td align="right">29,404,478</td>
<td align="right">-4.2%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT</td>
<td align="right">1,223,125,799</td>
<td align="right">1,172,538,302</td>
<td align="right">-4.1%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">265,357,308</td>
<td align="right">255,156,096</td>
<td align="right">-3.8%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">116,276,917</td>
<td align="right">111,884,279</td>
<td align="right">-3.8%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_WITH_HINT</td>
<td align="right">64,723,786</td>
<td align="right">62,856,330</td>
<td align="right">-2.9%</td>
</tr>
<tr>
<td align="left">BEFORE_WITH</td>
<td align="right">9,838,594</td>
<td align="right">10,119,505</td>
<td align="right">2.9%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP_DICT</td>
<td align="right">176,171,106</td>
<td align="right">171,438,844</td>
<td align="right">-2.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">854,764,814</td>
<td align="right">833,550,728</td>
<td align="right">-2.5%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">6,879,071,749</td>
<td align="right">6,716,838,273</td>
<td align="right">-2.4%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">609,012,693</td>
<td align="right">595,360,930</td>
<td align="right">-2.2%</td>
</tr>
<tr>
<td align="left">IS_OP</td>
<td align="right">473,924,151</td>
<td align="right">463,623,126</td>
<td align="right">-2.2%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">345,046,985</td>
<td align="right">337,670,159</td>
<td align="right">-2.1%</td>
</tr>
<tr>
<td align="left">BUILD_LIST</td>
<td align="right">223,526,871</td>
<td align="right">218,787,317</td>
<td align="right">-2.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">1,725,305,420</td>
<td align="right">1,690,024,137</td>
<td align="right">-2.0%</td>
</tr>
<tr>
<td align="left">STORE_FAST_STORE_FAST</td>
<td align="right">443,671,613</td>
<td align="right">434,776,054</td>
<td align="right">-2.0%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_O</td>
<td align="right">655,873,798</td>
<td align="right">642,957,275</td>
<td align="right">-2.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">1,728,916,222</td>
<td align="right">1,695,792,734</td>
<td align="right">-1.9%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">6,690,573,003</td>
<td align="right">6,565,404,158</td>
<td align="right">-1.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">1,347,705,062</td>
<td align="right">1,322,601,534</td>
<td align="right">-1.9%</td>
</tr>
<tr>
<td align="left">NOP</td>
<td align="right">987,755,381</td>
<td align="right">971,592,230</td>
<td align="right">-1.6%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">127,708,258</td>
<td align="right">125,635,774</td>
<td align="right">-1.6%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_DICT</td>
<td align="right">569,076,369</td>
<td align="right">559,880,046</td>
<td align="right">-1.6%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">5,571,883,644</td>
<td align="right">5,484,528,513</td>
<td align="right">-1.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">24,437,171,869</td>
<td align="right">24,055,289,510</td>
<td align="right">-1.6%</td>
</tr>
<tr>
<td align="left">DICT_UPDATE</td>
<td align="right">72,689</td>
<td align="right">73,817</td>
<td align="right">1.6%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">3,548,508,603</td>
<td align="right">3,494,024,398</td>
<td align="right">-1.5%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NONE</td>
<td align="right">397,290,508</td>
<td align="right">391,725,407</td>
<td align="right">-1.4%</td>
</tr>
<tr>
<td align="left">PUSH_NULL</td>
<td align="right">1,219,277,864</td>
<td align="right">1,202,431,708</td>
<td align="right">-1.4%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">656,141,664</td>
<td align="right">647,740,176</td>
<td align="right">-1.3%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">563,771,024</td>
<td align="right">556,577,713</td>
<td align="right">-1.3%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">1,155,758,560</td>
<td align="right">1,141,811,715</td>
<td align="right">-1.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">5,399,792,883</td>
<td align="right">5,335,145,571</td>
<td align="right">-1.2%</td>
</tr>
<tr>
<td align="left">CALL_LEN</td>
<td align="right">305,994,150</td>
<td align="right">302,344,592</td>
<td align="right">-1.2%</td>
</tr>
<tr>
<td align="left">TO_BOOL_LIST</td>
<td align="right">117,177,661</td>
<td align="right">115,782,677</td>
<td align="right">-1.2%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">2,744,457,993</td>
<td align="right">2,776,496,938</td>
<td align="right">1.2%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">374,272,069</td>
<td align="right">369,906,487</td>
<td align="right">-1.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_CHECK</td>
<td align="right">10,989,976</td>
<td align="right">11,108,185</td>
<td align="right">1.1%</td>
</tr>
<tr>
<td align="left">TO_BOOL_NONE</td>
<td align="right">507,689,511</td>
<td align="right">502,331,744</td>
<td align="right">-1.1%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">3,026,528,897</td>
<td align="right">2,995,675,657</td>
<td align="right">-1.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">4,200,907,032</td>
<td align="right">4,160,355,069</td>
<td align="right">-1.0%</td>
</tr>
<tr>
<td align="left">CALL_INTRINSIC_1</td>
<td align="right">156,144,462</td>
<td align="right">154,651,343</td>
<td align="right">-1.0%</td>
</tr>
<tr>
<td align="left">INSTRUMENTED_FOR_ITER</td>
<td align="right">3,184</td>
<td align="right">3,212</td>
<td align="right">0.9%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP_SET</td>
<td align="right">461,989,899</td>
<td align="right">457,931,837</td>
<td align="right">-0.9%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">2,869,326,814</td>
<td align="right">2,844,186,316</td>
<td align="right">-0.9%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_UNICODE</td>
<td align="right">74,034,949</td>
<td align="right">73,426,028</td>
<td align="right">-0.8%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_LIST_INT</td>
<td align="right">459,808,101</td>
<td align="right">456,180,365</td>
<td align="right">-0.8%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NOT_NONE</td>
<td align="right">671,954,551</td>
<td align="right">666,813,105</td>
<td align="right">-0.8%</td>
</tr>
<tr>
<td align="left">TO_BOOL_STR</td>
<td align="right">80,121,282</td>
<td align="right">79,517,949</td>
<td align="right">-0.8%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">6,262,334,594</td>
<td align="right">6,216,244,658</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">194,597,330</td>
<td align="right">193,190,472</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">629,327,314</td>
<td align="right">624,867,344</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_STR</td>
<td align="right">323,190,414</td>
<td align="right">320,960,091</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">JUMP_FORWARD</td>
<td align="right">447,747,276</td>
<td align="right">444,711,064</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">663,804,533</td>
<td align="right">659,499,255</td>
<td align="right">-0.6%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_LIST</td>
<td align="right">12,242,301</td>
<td align="right">12,164,433</td>
<td align="right">-0.6%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_CLASS</td>
<td align="right">162,684,374</td>
<td align="right">161,668,414</td>
<td align="right">-0.6%</td>
</tr>
<tr>
<td align="left">BINARY_SLICE</td>
<td align="right">227,313,494</td>
<td align="right">225,924,507</td>
<td align="right">-0.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_AND_CLEAR</td>
<td align="right">70,117,962</td>
<td align="right">69,707,301</td>
<td align="right">-0.6%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR_METHOD</td>
<td align="right">126,140,293</td>
<td align="right">126,865,105</td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_LIST_INT</td>
<td align="right">110,665,687</td>
<td align="right">110,052,125</td>
<td align="right">-0.6%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">468,057,315</td>
<td align="right">465,668,828</td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">FOR_ITER_RANGE</td>
<td align="right">107,578,740</td>
<td align="right">107,045,446</td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR</td>
<td align="right">134,417,908</td>
<td align="right">133,772,504</td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">CALL_ISINSTANCE</td>
<td align="right">846,793,747</td>
<td align="right">842,918,321</td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">CALL_PY_WITH_DEFAULTS</td>
<td align="right">217,384,268</td>
<td align="right">218,369,984</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">INSTRUMENTED_JUMP_BACKWARD</td>
<td align="right">6,224</td>
<td align="right">6,252</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR_ATTR</td>
<td align="right">7,717,162</td>
<td align="right">7,751,723</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_INT</td>
<td align="right">674,967,129</td>
<td align="right">672,261,888</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">249,321,151</td>
<td align="right">248,329,223</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">2,947,350,111</td>
<td align="right">2,936,142,380</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">UNARY_NOT</td>
<td align="right">28,307,691</td>
<td align="right">28,412,744</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">DELETE_FAST</td>
<td align="right">2,227,065</td>
<td align="right">2,235,107</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST_WITH_KEYWORDS</td>
<td align="right">109,851,737</td>
<td align="right">109,459,244</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_DICT</td>
<td align="right">149,628,529</td>
<td align="right">150,130,803</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">TO_BOOL_ALWAYS_TRUE</td>
<td align="right">181,990,523</td>
<td align="right">181,389,885</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">INSTRUMENTED_POP_JUMP_IF_TRUE</td>
<td align="right">8,704</td>
<td align="right">8,732</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">INTERPRETER_EXIT</td>
<td align="right">2,301,737,622</td>
<td align="right">2,308,618,970</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">124,808,772</td>
<td align="right">125,161,199</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_LAZY_DICT</td>
<td align="right">253,863,509</td>
<td align="right">253,172,237</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">COPY_FREE_VARS</td>
<td align="right">320,022,498</td>
<td align="right">320,748,742</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">1,182,874,954</td>
<td align="right">1,185,340,483</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">FOR_ITER_GEN</td>
<td align="right">216,203,472</td>
<td align="right">216,556,194</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_FLOAT</td>
<td align="right">75,746,651</td>
<td align="right">75,851,701</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_MODULE</td>
<td align="right">540,241,367</td>
<td align="right">539,494,618</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">WITH_EXCEPT_START</td>
<td align="right">233,161</td>
<td align="right">233,483</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_INT</td>
<td align="right">405,086,440</td>
<td align="right">404,533,834</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">1,133,352,518</td>
<td align="right">1,131,809,306</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_FLOAT</td>
<td align="right">87,691,536</td>
<td align="right">87,801,578</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">CALL_TUPLE_1</td>
<td align="right">28,218,600</td>
<td align="right">28,251,677</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">LIST_APPEND</td>
<td align="right">73,630,423</td>
<td align="right">73,716,387</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">4,282,984,687</td>
<td align="right">4,287,685,839</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right">121,680,125</td>
<td align="right">121,813,530</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_O</td>
<td align="right">396,069,265</td>
<td align="right">395,656,304</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR</td>
<td align="right">418,650,455</td>
<td align="right">418,217,882</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">741,910,146</td>
<td align="right">742,605,466</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">CHECK_EXC_MATCH</td>
<td align="right">24,452,584</td>
<td align="right">24,471,417</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">PUSH_EXC_INFO</td>
<td align="right">24,963,793</td>
<td align="right">24,982,920</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">POP_EXCEPT</td>
<td align="right">24,963,645</td>
<td align="right">24,982,768</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">DELETE_ATTR</td>
<td align="right">6,688,241</td>
<td align="right">6,693,091</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">CALL_FUNCTION_EX</td>
<td align="right">202,093,737</td>
<td align="right">202,233,979</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">BUILD_MAP</td>
<td align="right">132,230,973</td>
<td align="right">132,317,321</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">FOR_ITER_TUPLE</td>
<td align="right">307,612,325</td>
<td align="right">307,411,875</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">CALL_TYPE_1</td>
<td align="right">244,413,149</td>
<td align="right">244,271,684</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_SLOT</td>
<td align="right">1,496,501,793</td>
<td align="right">1,495,653,021</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">BUILD_CONST_KEY_MAP</td>
<td align="right">11,832,643</td>
<td align="right">11,826,321</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_TUPLE_INT</td>
<td align="right">210,848,134</td>
<td align="right">210,957,407</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">2,052,458,138</td>
<td align="right">2,053,464,892</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_KW</td>
<td align="right">273,846,175</td>
<td align="right">273,971,776</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST</td>
<td align="right">544,628,916</td>
<td align="right">544,855,826</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_GETITEM</td>
<td align="right">65,669,930</td>
<td align="right">65,696,484</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">MAKE_CELL</td>
<td align="right">104,793,077</td>
<td align="right">104,834,838</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">IMPORT_NAME</td>
<td align="right">12,432,878</td>
<td align="right">12,437,025</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">IMPORT_FROM</td>
<td align="right">13,100,791</td>
<td align="right">13,104,905</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_LIST_APPEND</td>
<td align="right">348,055,049</td>
<td align="right">348,162,408</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">DICT_MERGE</td>
<td align="right">47,490,483</td>
<td align="right">47,504,808</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">SET_FUNCTION_ATTRIBUTE</td>
<td align="right">84,886,824</td>
<td align="right">84,912,159</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_FAST_LOAD_FAST</td>
<td align="right">43,015,595</td>
<td align="right">43,027,364</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">RERAISE</td>
<td align="right">3,847,310</td>
<td align="right">3,848,264</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_DEREF</td>
<td align="right">95,257,323</td>
<td align="right">95,275,580</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_INPLACE_ADD_UNICODE</td>
<td align="right">5,183,255</td>
<td align="right">5,184,215</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TUPLE</td>
<td align="right">307,919,955</td>
<td align="right">307,972,497</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_STR_INT</td>
<td align="right">456,452,859</td>
<td align="right">456,386,356</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">UNARY_NEGATIVE</td>
<td align="right">146,012,201</td>
<td align="right">145,995,212</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE</td>
<td align="right">540,615</td>
<td align="right">540,676</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_FLOAT</td>
<td align="right">181,052,864</td>
<td align="right">181,072,755</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">345,228</td>
<td align="right">345,265</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">MAKE_FUNCTION</td>
<td align="right">98,414,353</td>
<td align="right">98,423,163</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_SLICE</td>
<td align="right">12,600,984</td>
<td align="right">12,602,112</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">YIELD_VALUE</td>
<td align="right">1,380,675,039</td>
<td align="right">1,380,563,472</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">RETURN_GENERATOR</td>
<td align="right">505,452,392</td>
<td align="right">505,490,655</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">3,619,549,322</td>
<td align="right">3,619,821,761</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BUILD_STRING</td>
<td align="right">75,496,658</td>
<td align="right">75,501,970</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">FORMAT_SIMPLE</td>
<td align="right">148,456,193</td>
<td align="right">148,463,669</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">SET_ADD</td>
<td align="right">965,774</td>
<td align="right">965,726</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR</td>
<td align="right">23,564</td>
<td align="right">23,563</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD_NO_INTERRUPT</td>
<td align="right">556,665,355</td>
<td align="right">556,687,536</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">RAISE_VARARGS</td>
<td align="right">6,185,088</td>
<td align="right">6,185,334</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">GET_AWAITABLE</td>
<td align="right">229,790,988</td>
<td align="right">229,799,059</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">EXIT_INIT_CHECK</td>
<td align="right">94,700,610</td>
<td align="right">94,703,820</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_ALLOC_AND_ENTER_INIT</td>
<td align="right">96,988,672</td>
<td align="right">96,991,882</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_NAME</td>
<td align="right">12,145,407</td>
<td align="right">12,145,807</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">DELETE_SUBSCR</td>
<td align="right">176,484,381</td>
<td align="right">176,490,036</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BUILD_SLICE</td>
<td align="right">71,717,563</td>
<td align="right">71,719,840</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_STR_1</td>
<td align="right">46,758,056</td>
<td align="right">46,759,449</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CONVERT_VALUE</td>
<td align="right">138,448,656</td>
<td align="right">138,452,570</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BUILD_SET</td>
<td align="right">2,329,722</td>
<td align="right">2,329,780</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">END_SEND</td>
<td align="right">402,619,044</td>
<td align="right">402,627,115</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">SEND</td>
<td align="right">173,838,365</td>
<td align="right">173,841,677</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_MULTIPLY_INT</td>
<td align="right">164,920,166</td>
<td align="right">164,923,167</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">SEND_GEN</td>
<td align="right">787,107,140</td>
<td align="right">787,119,920</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">END_FOR</td>
<td align="right">82,765,554</td>
<td align="right">82,766,179</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_MULTIPLY_FLOAT</td>
<td align="right">210,108,258</td>
<td align="right">210,107,307</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">20,772,507</td>
<td align="right">20,772,467</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">MAP_ADD</td>
<td align="right">39,903,176</td>
<td align="right">39,903,205</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">GET_YIELD_FROM_ITER</td>
<td align="right">47,328,739</td>
<td align="right">47,328,739</td>
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
<td align="left">STORE_GLOBAL</td>
<td align="right">6,944,700</td>
<td align="right">6,944,700</td>
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
<td align="right">638,582</td>
<td align="right">638,582</td>
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
<td align="right">152,057</td>
<td align="right">152,057</td>
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
<tr>
<td align="left">FUNCTION_START</td>
<td align="right"></td>
<td align="right">5,337,914,944</td>
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
<td align="right">638,025,385</td>
<td align="right">27.7%</td>
<td align="right">624,378,116</td>
<td align="right">27.3%</td>
<td align="right">-2.1%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">1,666,850,159</td>
<td align="right">72.3%</td>
<td align="right">1,663,201,496</td>
<td align="right">72.6%</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">30,888,225</td>
<td align="right">1.3%</td>
<td align="right">30,888,222</td>
<td align="right">1.3%</td>
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
<td align="right">1,239,519</td>
<td align="right">66.1%</td>
<td align="right">1,235,057</td>
<td align="right">66.0%</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">636,014</td>
<td align="right">33.9%</td>
<td align="right">635,979</td>
<td align="right">34.0%</td>
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
<td align="left">subtract other</td>
<td align="right">12,554</td>
<td align="right">1.0%</td>
<td align="right">11,534</td>
<td align="right">0.9%</td>
<td align="right">-8.1%</td>
</tr>
<tr>
<td align="left">xor</td>
<td align="right">9,864</td>
<td align="right">0.8%</td>
<td align="right">9,263</td>
<td align="right">0.8%</td>
<td align="right">-6.1%</td>
</tr>
<tr>
<td align="left">and int</td>
<td align="right">40,869</td>
<td align="right">3.3%</td>
<td align="right">39,536</td>
<td align="right">3.2%</td>
<td align="right">-3.3%</td>
</tr>
<tr>
<td align="left">remainder</td>
<td align="right">54,095</td>
<td align="right">4.4%</td>
<td align="right">52,598</td>
<td align="right">4.3%</td>
<td align="right">-2.8%</td>
</tr>
<tr>
<td align="left">power</td>
<td align="right">5,748</td>
<td align="right">0.5%</td>
<td align="right">5,741</td>
<td align="right">0.5%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">multiply different types</td>
<td align="right">92,314</td>
<td align="right">7.4%</td>
<td align="right">92,232</td>
<td align="right">7.5%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">or</td>
<td align="right">17,469</td>
<td align="right">1.4%</td>
<td align="right">17,483</td>
<td align="right">1.4%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">true divide different types</td>
<td align="right">13,429</td>
<td align="right">1.1%</td>
<td align="right">13,421</td>
<td align="right">1.1%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">and other</td>
<td align="right">2,013</td>
<td align="right">0.2%</td>
<td align="right">2,012</td>
<td align="right">0.2%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">add different types</td>
<td align="right">78,761</td>
<td align="right">6.4%</td>
<td align="right">78,797</td>
<td align="right">6.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">add other</td>
<td align="right">64,746</td>
<td align="right">5.2%</td>
<td align="right">64,771</td>
<td align="right">5.2%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">true divide other</td>
<td align="right">3,441</td>
<td align="right">0.3%</td>
<td align="right">3,440</td>
<td align="right">0.3%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">true divide float</td>
<td align="right">5,764</td>
<td align="right">0.5%</td>
<td align="right">5,763</td>
<td align="right">0.5%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">lshift</td>
<td align="right">5,826</td>
<td align="right">0.5%</td>
<td align="right">5,825</td>
<td align="right">0.5%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">floor divide</td>
<td align="right">33,516</td>
<td align="right">2.7%</td>
<td align="right">33,512</td>
<td align="right">2.7%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">rshift</td>
<td align="right">9,988</td>
<td align="right">0.8%</td>
<td align="right">9,989</td>
<td align="right">0.8%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">subtract different types</td>
<td align="right">783,283</td>
<td align="right">63.2%</td>
<td align="right">783,301</td>
<td align="right">63.4%</td>
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
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">1,756,952,291</td>
<td align="right">80.6%</td>
<td align="right">1,744,197,917</td>
<td align="right">80.5%</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">423,166,656</td>
<td align="right">19.4%</td>
<td align="right">422,733,883</td>
<td align="right">19.5%</td>
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
<td align="right">4,903,102</td>
<td align="right">0.2%</td>
<td align="right">4,902,741</td>
<td align="right">0.2%</td>
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
<td align="right">185,037</td>
<td align="right">47.8%</td>
<td align="right">184,903</td>
<td align="right">47.8%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">201,864</td>
<td align="right">52.2%</td>
<td align="right">201,837</td>
<td align="right">52.2%</td>
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
<td align="left">tuple slice</td>
<td align="right">184</td>
<td align="right">0.1%</td>
<td align="right">183</td>
<td align="right">0.1%</td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">57,114</td>
<td align="right">30.9%</td>
<td align="right">57,008</td>
<td align="right">30.8%</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">buffer int</td>
<td align="right">22,681</td>
<td align="right">12.3%</td>
<td align="right">22,664</td>
<td align="right">12.3%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">out of range</td>
<td align="right">76,542</td>
<td align="right">41.4%</td>
<td align="right">76,532</td>
<td align="right">41.4%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">array int</td>
<td align="right">16,820</td>
<td align="right">9.1%</td>
<td align="right">16,820</td>
<td align="right">9.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">code complex parameters</td>
<td align="right">5,036</td>
<td align="right">2.7%</td>
<td align="right">5,036</td>
<td align="right">2.7%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">sequence int</td>
<td align="right">4,300</td>
<td align="right">2.3%</td>
<td align="right">4,300</td>
<td align="right">2.3%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">list slice</td>
<td align="right">1,360</td>
<td align="right">0.7%</td>
<td align="right">1,360</td>
<td align="right">0.7%</td>
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
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">254,310,155</td>
<td align="right">2.8%</td>
<td align="right">248,057,828</td>
<td align="right">2.7%</td>
<td align="right">-2.5%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">7,685,009,335</td>
<td align="right">84.2%</td>
<td align="right">7,625,528,241</td>
<td align="right">84.2%</td>
<td align="right">-0.8%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">1,430,805,721</td>
<td align="right">15.7%</td>
<td align="right">1,427,134,753</td>
<td align="right">15.8%</td>
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
<td align="right">5,427,869</td>
<td align="right">85.1%</td>
<td align="right">5,309,882</td>
<td align="right">84.8%</td>
<td align="right">-2.2%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">951,519</td>
<td align="right">14.9%</td>
<td align="right">953,676</td>
<td align="right">15.2%</td>
<td align="right">0.2%</td>
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
<td align="left">class mutable</td>
<td align="right">24,591</td>
<td align="right">2.6%</td>
<td align="right">24,760</td>
<td align="right">2.6%</td>
<td align="right">0.7%</td>
</tr>
<tr>
<td align="left">bound method</td>
<td align="right">12,012</td>
<td align="right">1.3%</td>
<td align="right">12,092</td>
<td align="right">1.3%</td>
<td align="right">0.7%</td>
</tr>
<tr>
<td align="left">cfunc noargs</td>
<td align="right">69,550</td>
<td align="right">7.3%</td>
<td align="right">69,997</td>
<td align="right">7.3%</td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">meth descr varargs keywords</td>
<td align="right">20,756</td>
<td align="right">2.2%</td>
<td align="right">20,871</td>
<td align="right">2.2%</td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">method wrapper</td>
<td align="right">8,269</td>
<td align="right">0.9%</td>
<td align="right">8,224</td>
<td align="right">0.9%</td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">operator wrapper</td>
<td align="right">10,086</td>
<td align="right">1.1%</td>
<td align="right">10,136</td>
<td align="right">1.1%</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">cfunc varargs keywords</td>
<td align="right">32,127</td>
<td align="right">3.4%</td>
<td align="right">32,275</td>
<td align="right">3.4%</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">cfunc varargs</td>
<td align="right">14,189</td>
<td align="right">1.5%</td>
<td align="right">14,251</td>
<td align="right">1.5%</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">class no vectorcall</td>
<td align="right">78,532</td>
<td align="right">8.3%</td>
<td align="right">78,840</td>
<td align="right">8.3%</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">code complex parameters</td>
<td align="right">184,535</td>
<td align="right">19.4%</td>
<td align="right">185,212</td>
<td align="right">19.4%</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">wrong number arguments</td>
<td align="right">13,713</td>
<td align="right">1.4%</td>
<td align="right">13,753</td>
<td align="right">1.4%</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">metaclass</td>
<td align="right">43,324</td>
<td align="right">4.6%</td>
<td align="right">43,255</td>
<td align="right">4.5%</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">meth descr varargs</td>
<td align="right">16,499</td>
<td align="right">1.7%</td>
<td align="right">16,523</td>
<td align="right">1.7%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">meth descr method fastcall keywords</td>
<td align="right">207,093</td>
<td align="right">21.8%</td>
<td align="right">207,213</td>
<td align="right">21.7%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">67,542</td>
<td align="right">7.1%</td>
<td align="right">67,573</td>
<td align="right">7.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">init not inline values</td>
<td align="right">105,577</td>
<td align="right">11.1%</td>
<td align="right">105,577</td>
<td align="right">11.1%</td>
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
<td align="right">152,203,812</td>
<td align="right">8.1%</td>
<td align="right">140,893,605</td>
<td align="right">7.8%</td>
<td align="right">-7.4%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">1,725,533,503</td>
<td align="right">91.9%</td>
<td align="right">1,672,755,705</td>
<td align="right">92.2%</td>
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
<td align="right">1,835,574</td>
<td align="right">0.1%</td>
<td align="right">1,815,443</td>
<td align="right">0.1%</td>
<td align="right">-1.1%</td>
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
<td align="right">230,795</td>
<td align="right">67.2%</td>
<td align="right">228,370</td>
<td align="right">67.0%</td>
<td align="right">-1.1%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">112,699</td>
<td align="right">32.8%</td>
<td align="right">112,298</td>
<td align="right">33.0%</td>
<td align="right">-0.4%</td>
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
<td align="right">24,183</td>
<td align="right">10.5%</td>
<td align="right">22,142</td>
<td align="right">9.7%</td>
<td align="right">-8.4%</td>
</tr>
<tr>
<td align="left">baseobject</td>
<td align="right">33,725</td>
<td align="right">14.6%</td>
<td align="right">32,975</td>
<td align="right">14.4%</td>
<td align="right">-2.2%</td>
</tr>
<tr>
<td align="left">big int</td>
<td align="right">59,694</td>
<td align="right">25.9%</td>
<td align="right">60,957</td>
<td align="right">26.7%</td>
<td align="right">2.1%</td>
</tr>
<tr>
<td align="left">float long</td>
<td align="right">16,414</td>
<td align="right">7.1%</td>
<td align="right">16,204</td>
<td align="right">7.1%</td>
<td align="right">-1.3%</td>
</tr>
<tr>
<td align="left">different types</td>
<td align="right">55,040</td>
<td align="right">23.8%</td>
<td align="right">54,348</td>
<td align="right">23.8%</td>
<td align="right">-1.3%</td>
</tr>
<tr>
<td align="left">long float</td>
<td align="right">1,522</td>
<td align="right">0.7%</td>
<td align="right">1,540</td>
<td align="right">0.7%</td>
<td align="right">1.2%</td>
</tr>
<tr>
<td align="left">bool</td>
<td align="right">3,820</td>
<td align="right">1.7%</td>
<td align="right">3,829</td>
<td align="right">1.7%</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">14,620</td>
<td align="right">6.3%</td>
<td align="right">14,598</td>
<td align="right">6.4%</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">string</td>
<td align="right">11,080</td>
<td align="right">4.8%</td>
<td align="right">11,080</td>
<td align="right">4.9%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">4,234</td>
<td align="right">1.8%</td>
<td align="right">4,234</td>
<td align="right">1.9%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">bytes</td>
<td align="right">4,120</td>
<td align="right">1.8%</td>
<td align="right">4,120</td>
<td align="right">1.8%</td>
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
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">118,622,848</td>
<td align="right">15.7%</td>
<td align="right">114,231,864</td>
<td align="right">15.4%</td>
<td align="right">-3.7%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">635,614,765</td>
<td align="right">84.3%</td>
<td align="right">626,824,441</td>
<td align="right">84.6%</td>
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
<td align="right">2,546,240</td>
<td align="right">0.3%</td>
<td align="right">2,546,240</td>
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
<td align="right">132,797</td>
<td align="right">66.3%</td>
<td align="right">131,142</td>
<td align="right">66.0%</td>
<td align="right">-1.2%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">67,512</td>
<td align="right">33.7%</td>
<td align="right">67,513</td>
<td align="right">34.0%</td>
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
<td align="right">28,888</td>
<td align="right">21.8%</td>
<td align="right">28,106</td>
<td align="right">21.4%</td>
<td align="right">-2.7%</td>
</tr>
<tr>
<td align="left">str</td>
<td align="right">37,064</td>
<td align="right">27.9%</td>
<td align="right">36,594</td>
<td align="right">27.9%</td>
<td align="right">-1.3%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">47,184</td>
<td align="right">35.5%</td>
<td align="right">46,818</td>
<td align="right">35.7%</td>
<td align="right">-0.8%</td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">19,661</td>
<td align="right">14.8%</td>
<td align="right">19,624</td>
<td align="right">15.0%</td>
<td align="right">-0.2%</td>
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
<td align="right">227,481,670</td>
<td align="right">16.0%</td>
<td align="right">225,417,739</td>
<td align="right">15.9%</td>
<td align="right">-0.9%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">1,193,242,099</td>
<td align="right">83.9%</td>
<td align="right">1,188,544,693</td>
<td align="right">83.9%</td>
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
<td align="right">101,956,971</td>
<td align="right">7.2%</td>
<td align="right">101,968,077</td>
<td align="right">7.2%</td>
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
<td align="right">193,846</td>
<td align="right">8.9%</td>
<td align="right">196,232</td>
<td align="right">9.0%</td>
<td align="right">1.2%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">1,989,713</td>
<td align="right">91.1%</td>
<td align="right">1,989,880</td>
<td align="right">91.0%</td>
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
<td align="left">seq iter</td>
<td align="right">10,300</td>
<td align="right">5.3%</td>
<td align="right">13,660</td>
<td align="right">7.0%</td>
<td align="right">32.6%</td>
</tr>
<tr>
<td align="left">dict items</td>
<td align="right">67,526</td>
<td align="right">34.8%</td>
<td align="right">66,399</td>
<td align="right">33.8%</td>
<td align="right">-1.7%</td>
</tr>
<tr>
<td align="left">ascii string</td>
<td align="right">2,700</td>
<td align="right">1.4%</td>
<td align="right">2,660</td>
<td align="right">1.4%</td>
<td align="right">-1.5%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">25,736</td>
<td align="right">13.3%</td>
<td align="right">26,084</td>
<td align="right">13.3%</td>
<td align="right">1.4%</td>
</tr>
<tr>
<td align="left">enumerate</td>
<td align="right">19,929</td>
<td align="right">10.3%</td>
<td align="right">19,754</td>
<td align="right">10.1%</td>
<td align="right">-0.9%</td>
</tr>
<tr>
<td align="left">itertools</td>
<td align="right">7,451</td>
<td align="right">3.8%</td>
<td align="right">7,471</td>
<td align="right">3.8%</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">dict keys</td>
<td align="right">14,756</td>
<td align="right">7.6%</td>
<td align="right">14,756</td>
<td align="right">7.5%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">14,459</td>
<td align="right">7.5%</td>
<td align="right">14,459</td>
<td align="right">7.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">zip</td>
<td align="right">14,352</td>
<td align="right">7.4%</td>
<td align="right">14,352</td>
<td align="right">7.3%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">reversed list</td>
<td align="right">7,885</td>
<td align="right">4.1%</td>
<td align="right">7,885</td>
<td align="right">4.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">dict values</td>
<td align="right">7,050</td>
<td align="right">3.6%</td>
<td align="right">7,050</td>
<td align="right">3.6%</td>
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
<td align="right">580,578,991</td>
<td align="right">5.1%</td>
<td align="right">545,535,218</td>
<td align="right">4.9%</td>
<td align="right">-6.0%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">1,421,796,115</td>
<td align="right">12.4%</td>
<td align="right">1,366,206,347</td>
<td align="right">12.3%</td>
<td align="right">-3.9%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">10,014,434,413</td>
<td align="right">87.5%</td>
<td align="right">9,758,585,112</td>
<td align="right">87.6%</td>
<td align="right">-2.6%</td>
</tr>
<tr>
<td align="left">
deopt
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">685,161</td>
<td align="right">0.0%</td>
<td align="right">684,111</td>
<td align="right">0.0%</td>
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
<td align="right">11,838,299</td>
<td align="right">87.4%</td>
<td align="right">11,177,234</td>
<td align="right">86.8%</td>
<td align="right">-5.6%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">1,709,391</td>
<td align="right">12.6%</td>
<td align="right">1,702,365</td>
<td align="right">13.2%</td>
<td align="right">-0.4%</td>
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
<td align="left">method</td>
<td align="right">120,032</td>
<td align="right">7.0%</td>
<td align="right">116,830</td>
<td align="right">6.9%</td>
<td align="right">-2.7%</td>
</tr>
<tr>
<td align="left">class method obj</td>
<td align="right">25,113</td>
<td align="right">1.5%</td>
<td align="right">24,775</td>
<td align="right">1.5%</td>
<td align="right">-1.3%</td>
</tr>
<tr>
<td align="left">non object slot</td>
<td align="right">3,500</td>
<td align="right">0.2%</td>
<td align="right">3,540</td>
<td align="right">0.2%</td>
<td align="right">1.1%</td>
</tr>
<tr>
<td align="left">module attr not found</td>
<td align="right">17,842</td>
<td align="right">1.0%</td>
<td align="right">17,662</td>
<td align="right">1.0%</td>
<td align="right">-1.0%</td>
</tr>
<tr>
<td align="left">non overriding descriptor</td>
<td align="right">13,572</td>
<td align="right">0.8%</td>
<td align="right">13,695</td>
<td align="right">0.8%</td>
<td align="right">0.9%</td>
</tr>
<tr>
<td align="left">out of versions</td>
<td align="right">2,331</td>
<td align="right">0.1%</td>
<td align="right">2,310</td>
<td align="right">0.1%</td>
<td align="right">-0.9%</td>
</tr>
<tr>
<td align="left">metaclass attribute</td>
<td align="right">195,112</td>
<td align="right">11.4%</td>
<td align="right">193,455</td>
<td align="right">11.4%</td>
<td align="right">-0.8%</td>
</tr>
<tr>
<td align="left">builtin class method</td>
<td align="right">3,818</td>
<td align="right">0.2%</td>
<td align="right">3,798</td>
<td align="right">0.2%</td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">shadowed</td>
<td align="right">140,489</td>
<td align="right">8.2%</td>
<td align="right">139,813</td>
<td align="right">8.2%</td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">class attr descriptor</td>
<td align="right">30,100</td>
<td align="right">1.8%</td>
<td align="right">30,020</td>
<td align="right">1.8%</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">mutable class</td>
<td align="right">78,082</td>
<td align="right">4.6%</td>
<td align="right">77,947</td>
<td align="right">4.6%</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">non string or split</td>
<td align="right">22,085</td>
<td align="right">1.3%</td>
<td align="right">22,050</td>
<td align="right">1.3%</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">overridden</td>
<td align="right">19,285</td>
<td align="right">1.1%</td>
<td align="right">19,306</td>
<td align="right">1.1%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">class attr simple</td>
<td align="right">718,869</td>
<td align="right">42.1%</td>
<td align="right">718,173</td>
<td align="right">42.2%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">not managed dict</td>
<td align="right">300,821</td>
<td align="right">17.6%</td>
<td align="right">300,651</td>
<td align="right">17.7%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">not in keys</td>
<td align="right">16,560</td>
<td align="right">1.0%</td>
<td align="right">16,560</td>
<td align="right">1.0%</td>
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
<td align="right">6,574,582,995</td>
<td align="right">99.7%</td>
<td align="right">6,489,243,241</td>
<td align="right">99.7%</td>
<td align="right">-1.3%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">454,505</td>
<td align="right">0.0%</td>
<td align="right">456,814</td>
<td align="right">0.0%</td>
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
<td align="right">20,559,005</td>
<td align="right">0.3%</td>
<td align="right">20,561,295</td>
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
<td align="right">668,007</td>
<td align="right">100.0%</td>
<td align="right">667,986</td>
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
<td align="right">133,857,455</td>
<td align="right">100.0%</td>
<td align="right">134,616,828</td>
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
<td align="right">11,847</td>
<td align="right">0.0%</td>
<td align="right">11,846</td>
<td align="right">0.0%</td>
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
<td align="right">173,800,368</td>
<td align="right">18.1%</td>
<td align="right">173,803,673</td>
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
<td align="right">787,076,240</td>
<td align="right">81.9%</td>
<td align="right">787,089,020</td>
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
<td align="right">7,151</td>
<td align="right">10.4%</td>
<td align="right">7,152</td>
<td align="right">10.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">61,746</td>
<td align="right">89.6%</td>
<td align="right">61,752</td>
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
<td align="right">16,126</td>
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
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">239,029,316</td>
<td align="right">8.6%</td>
<td align="right">233,591,794</td>
<td align="right">8.5%</td>
<td align="right">-2.3%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">2,528,966,733</td>
<td align="right">91.3%</td>
<td align="right">2,524,667,048</td>
<td align="right">91.4%</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">165,611,364</td>
<td align="right">6.0%</td>
<td align="right">165,651,609</td>
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
<td align="right">147,521</td>
<td align="right">4.3%</td>
<td align="right">146,224</td>
<td align="right">4.3%</td>
<td align="right">-0.9%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">3,273,709</td>
<td align="right">95.7%</td>
<td align="right">3,274,482</td>
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
<td align="left">class attr simple</td>
<td align="right">49,739</td>
<td align="right">33.7%</td>
<td align="right">48,324</td>
<td align="right">33.0%</td>
<td align="right">-2.8%</td>
</tr>
<tr>
<td align="left">property</td>
<td align="right">5,480</td>
<td align="right">3.7%</td>
<td align="right">5,580</td>
<td align="right">3.8%</td>
<td align="right">1.8%</td>
</tr>
<tr>
<td align="left">no dict</td>
<td align="right">5,160</td>
<td align="right">3.5%</td>
<td align="right">5,180</td>
<td align="right">3.5%</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">not managed dict</td>
<td align="right">28,510</td>
<td align="right">19.3%</td>
<td align="right">28,508</td>
<td align="right">19.5%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">not in dict</td>
<td align="right">15,645</td>
<td align="right">10.6%</td>
<td align="right">15,645</td>
<td align="right">10.7%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">non string or split</td>
<td align="right">15,440</td>
<td align="right">10.5%</td>
<td align="right">15,440</td>
<td align="right">10.6%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">overriding descriptor</td>
<td align="right">10,660</td>
<td align="right">7.2%</td>
<td align="right">10,660</td>
<td align="right">7.3%</td>
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
<td align="left">method</td>
<td align="right">1,540</td>
<td align="right">1.0%</td>
<td align="right">1,540</td>
<td align="right">1.1%</td>
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
<td align="right">134,318,115</td>
<td align="right">34.0%</td>
<td align="right">133,672,824</td>
<td align="right">33.9%</td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">260,291,316</td>
<td align="right">65.9%</td>
<td align="right">260,180,028</td>
<td align="right">66.0%</td>
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
<td align="right">83,987</td>
<td align="right">81.8%</td>
<td align="right">83,873</td>
<td align="right">81.8%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">18,706</td>
<td align="right">18.2%</td>
<td align="right">18,707</td>
<td align="right">18.2%</td>
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
<td align="right">8.7%</td>
<td align="right">7,160</td>
<td align="right">8.5%</td>
<td align="right">-2.2%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">2,060</td>
<td align="right">2.5%</td>
<td align="right">2,080</td>
<td align="right">2.5%</td>
<td align="right">1.0%</td>
</tr>
<tr>
<td align="left">py simple</td>
<td align="right">42,817</td>
<td align="right">51.0%</td>
<td align="right">42,838</td>
<td align="right">51.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">dict subclass no override</td>
<td align="right">28,282</td>
<td align="right">33.7%</td>
<td align="right">28,287</td>
<td align="right">33.7%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">out of range</td>
<td align="right">2,108</td>
<td align="right">2.5%</td>
<td align="right">2,108</td>
<td align="right">2.5%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">bytearray int</td>
<td align="right">1,400</td>
<td align="right">1.7%</td>
<td align="right">1,400</td>
<td align="right">1.7%</td>
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
<td align="right">104,428,598</td>
<td align="right">2.6%</td>
<td align="right">103,032,325</td>
<td align="right">2.5%</td>
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
<td align="right">350,870,048</td>
<td align="right">8.6%</td>
<td align="right">348,538,354</td>
<td align="right">8.6%</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">3,738,496,011</td>
<td align="right">91.4%</td>
<td align="right">3,714,387,865</td>
<td align="right">91.4%</td>
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
<td align="left">Failure</td>
<td align="right">625,007</td>
<td align="right">21.7%</td>
<td align="right">594,854</td>
<td align="right">21.1%</td>
<td align="right">-4.8%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">2,254,694</td>
<td align="right">78.3%</td>
<td align="right">2,228,340</td>
<td align="right">78.9%</td>
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
<td align="left">number</td>
<td align="right">181,606</td>
<td align="right">29.1%</td>
<td align="right">152,374</td>
<td align="right">25.6%</td>
<td align="right">-16.1%</td>
</tr>
<tr>
<td align="left">sequence</td>
<td align="right">17,977</td>
<td align="right">2.9%</td>
<td align="right">17,500</td>
<td align="right">2.9%</td>
<td align="right">-2.7%</td>
</tr>
<tr>
<td align="left">mapping</td>
<td align="right">58,865</td>
<td align="right">9.4%</td>
<td align="right">58,516</td>
<td align="right">9.8%</td>
<td align="right">-0.6%</td>
</tr>
<tr>
<td align="left">dict</td>
<td align="right">33,532</td>
<td align="right">5.4%</td>
<td align="right">33,353</td>
<td align="right">5.6%</td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">40,632</td>
<td align="right">6.5%</td>
<td align="right">40,668</td>
<td align="right">6.8%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">bytearray</td>
<td align="right">1,239</td>
<td align="right">0.2%</td>
<td align="right">1,240</td>
<td align="right">0.2%</td>
<td align="right">0.1%</td>
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
<td align="left">tuple</td>
<td align="right">95,410</td>
<td align="right">15.3%</td>
<td align="right">95,431</td>
<td align="right">16.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">bytes</td>
<td align="right">18,691</td>
<td align="right">3.0%</td>
<td align="right">18,694</td>
<td align="right">3.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">174,314</td>
<td align="right">27.9%</td>
<td align="right">174,338</td>
<td align="right">29.3%</td>
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
<td align="right">665,206,081</td>
<td align="right">99.9%</td>
<td align="right">657,803,929</td>
<td align="right">99.9%</td>
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
<td align="right">500,345</td>
<td align="right">0.1%</td>
<td align="right">500,416</td>
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
<td align="right">3,576</td>
<td align="right">8.2%</td>
<td align="right">3,575</td>
<td align="right">8.2%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">39,854</td>
<td align="right">91.8%</td>
<td align="right">39,845</td>
<td align="right">91.8%</td>
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
<td align="left">sequence</td>
<td align="right">2,515</td>
<td align="right">70.3%</td>
<td align="right">2,514</td>
<td align="right">70.3%</td>
<td align="right">-0.0%</td>
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
<td align="right">12,152,554,856</td>
<td align="right">9.3%</td>
<td align="right">17,319,370,210</td>
<td align="right">12.9%</td>
<td align="right">42.5%</td>
</tr>
<tr>
<td align="left">
Specialized misses
<details>
<summary>ⓘ</summary>

Specialized instructions, e.g. `LOAD_ATTR_MODULE` that deopt.
</details>
</td>
<td align="right">1,247,736,574</td>
<td align="right">1.0%</td>
<td align="right">1,205,077,157</td>
<td align="right">0.9%</td>
<td align="right">-3.4%</td>
</tr>
<tr>
<td align="left">
Specialized hits
<details>
<summary>ⓘ</summary>

Specialized instructions, e.g. `LOAD_ATTR_MODULE` that complete.
</details>
</td>
<td align="right">46,191,874,939</td>
<td align="right">35.4%</td>
<td align="right">45,512,303,738</td>
<td align="right">33.9%</td>
<td align="right">-1.5%</td>
</tr>
<tr>
<td align="left">
Basic
<details>
<summary>ⓘ</summary>

Instructions that are not and cannot be specialized, e.g. `LOAD_FAST`.
</details>
</td>
<td align="right">71,059,793,805</td>
<td align="right">54.4%</td>
<td align="right">70,400,314,775</td>
<td align="right">52.4%</td>
<td align="right">-0.9%</td>
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
<td align="left">COMPARE_OP</td>
<td align="right">152,203,812</td>
<td align="right">2.9%</td>
<td align="right">140,893,605</td>
<td align="right">2.7%</td>
<td align="right">-7.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">1,421,796,115</td>
<td align="right">26.7%</td>
<td align="right">1,366,206,347</td>
<td align="right">26.1%</td>
<td align="right">-3.9%</td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">239,029,316</td>
<td align="right">4.5%</td>
<td align="right">233,591,794</td>
<td align="right">4.5%</td>
<td align="right">-2.3%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">638,025,385</td>
<td align="right">12.0%</td>
<td align="right">624,378,116</td>
<td align="right">11.9%</td>
<td align="right">-2.1%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">227,481,670</td>
<td align="right">4.3%</td>
<td align="right">225,417,739</td>
<td align="right">4.3%</td>
<td align="right">-0.9%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">350,870,048</td>
<td align="right">6.6%</td>
<td align="right">348,538,354</td>
<td align="right">6.7%</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR</td>
<td align="right">134,318,115</td>
<td align="right">2.5%</td>
<td align="right">133,672,824</td>
<td align="right">2.6%</td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">1,430,805,721</td>
<td align="right">26.8%</td>
<td align="right">1,427,134,753</td>
<td align="right">27.3%</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR</td>
<td align="right">423,166,656</td>
<td align="right">7.9%</td>
<td align="right">422,733,883</td>
<td align="right">8.1%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">SEND</td>
<td align="right">173,800,368</td>
<td align="right">3.3%</td>
<td align="right">173,803,673</td>
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
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">109,398,572</td>
<td align="right">8.8%</td>
<td align="right">96,254,589</td>
<td align="right">8.0%</td>
<td align="right">-12.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">164,332,773</td>
<td align="right">13.2%</td>
<td align="right">153,726,480</td>
<td align="right">12.8%</td>
<td align="right">-6.5%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">129,592,377</td>
<td align="right">10.4%</td>
<td align="right">123,927,089</td>
<td align="right">10.3%</td>
<td align="right">-4.4%</td>
</tr>
<tr>
<td align="left">TO_BOOL_NONE</td>
<td align="right">48,998,335</td>
<td align="right">3.9%</td>
<td align="right">47,941,189</td>
<td align="right">4.0%</td>
<td align="right">-2.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">180,880,440</td>
<td align="right">14.5%</td>
<td align="right">178,517,364</td>
<td align="right">14.8%</td>
<td align="right">-1.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right">59,618,554</td>
<td align="right">4.8%</td>
<td align="right">59,553,412</td>
<td align="right">4.9%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_SLOT</td>
<td align="right">94,979,188</td>
<td align="right">7.6%</td>
<td align="right">95,019,319</td>
<td align="right">7.9%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">50,932,588</td>
<td align="right">4.1%</td>
<td align="right">50,941,844</td>
<td align="right">4.2%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">FOR_ITER_TUPLE</td>
<td align="right">50,782,663</td>
<td align="right">4.1%</td>
<td align="right">50,784,513</td>
<td align="right">4.2%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">70,579,416</td>
<td align="right">5.7%</td>
<td align="right">70,579,421</td>
<td align="right">5.9%</td>
<td align="right">0.0%</td>
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
<td align="left">Calls via PyEval_EvalFrame (api)</td>
<td align="right">253,586,653</td>
<td align="right">2.9%</td>
<td align="right">259,283,087</td>
<td align="right">3.0%</td>
<td align="right">2.2%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (function vectorcall)</td>
<td align="right">1,439,039,767</td>
<td align="right">16.5%</td>
<td align="right">1,446,388,648</td>
<td align="right">16.5%</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (vector)</td>
<td align="right">1,443,488,857</td>
<td align="right">16.5%</td>
<td align="right">1,450,837,738</td>
<td align="right">16.6%</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">Calls to PyEval_EvalDefault</td>
<td align="right">2,305,404,265</td>
<td align="right">26.4%</td>
<td align="right">2,312,285,932</td>
<td align="right">26.5%</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (total)</td>
<td align="right">2,305,404,265</td>
<td align="right">26.4%</td>
<td align="right">2,312,285,932</td>
<td align="right">26.5%</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">Frames pushed</td>
<td align="right">6,961,733,261</td>
<td align="right">79.7%</td>
<td align="right">6,969,970,426</td>
<td align="right">79.7%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (generator)</td>
<td align="right">861,915,408</td>
<td align="right">9.9%</td>
<td align="right">861,448,194</td>
<td align="right">9.9%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">Frame objects created</td>
<td align="right">88,441,264</td>
<td align="right">1.0%</td>
<td align="right">88,466,328</td>
<td align="right">1.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls to Python functions inlined</td>
<td align="right">6,426,612,458</td>
<td align="right">73.6%</td>
<td align="right">6,427,863,034</td>
<td align="right">73.5%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (function ex)</td>
<td align="right">38,356,839</td>
<td align="right">0.4%</td>
<td align="right">38,364,011</td>
<td align="right">0.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (method)</td>
<td align="right">213,131,237</td>
<td align="right">2.4%</td>
<td align="right">213,154,352</td>
<td align="right">2.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (slot)</td>
<td align="right">475,775,065</td>
<td align="right">5.4%</td>
<td align="right">475,811,054</td>
<td align="right">5.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (legacy)</td>
<td align="right">4,418,464</td>
<td align="right">0.1%</td>
<td align="right">4,418,464</td>
<td align="right">0.1%</td>
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
<td align="left">Method cache dunder misses</td>
<td align="right">15,121,696</td>
<td align="right"></td>
<td align="right">14,743,665</td>
<td align="right"></td>
<td align="right">-2.5%</td>
</tr>
<tr>
<td align="left">Method cache collisions</td>
<td align="right">84,531,473</td>
<td align="right"></td>
<td align="right">83,739,910</td>
<td align="right"></td>
<td align="right">-0.9%</td>
</tr>
<tr>
<td align="left">Allocations from freelist</td>
<td align="right">6,815,486,730</td>
<td align="right">36.7%</td>
<td align="right">6,756,537,928</td>
<td align="right">36.6%</td>
<td align="right">-0.9%</td>
</tr>
<tr>
<td align="left">Frees to freelist</td>
<td align="right">6,817,461,648</td>
<td align="right"></td>
<td align="right">6,758,540,716</td>
<td align="right"></td>
<td align="right">-0.9%</td>
</tr>
<tr>
<td align="left">Method cache misses</td>
<td align="right">77,186,643</td>
<td align="right"></td>
<td align="right">76,769,870</td>
<td align="right"></td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">Method cache hits</td>
<td align="right">3,123,015,516</td>
<td align="right"></td>
<td align="right">3,136,878,132</td>
<td align="right"></td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">Allocations to 512 bytes</td>
<td align="right">11,619,343,672</td>
<td align="right">62.6%</td>
<td align="right">11,578,294,439</td>
<td align="right">62.7%</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">Allocations</td>
<td align="right">11,745,210,897</td>
<td align="right">63.3%</td>
<td align="right">11,704,271,086</td>
<td align="right">63.4%</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">Frees</td>
<td align="right">12,073,066,526</td>
<td align="right"></td>
<td align="right">12,032,552,778</td>
<td align="right"></td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">Allocations over 4 kbytes</td>
<td align="right">21,097,803</td>
<td align="right">0.1%</td>
<td align="right">21,168,263</td>
<td align="right">0.1%</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">Inline values</td>
<td align="right">182,223,730</td>
<td align="right"></td>
<td align="right">182,651,815</td>
<td align="right"></td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">Method cache dunder hits</td>
<td align="right">3,554,009,443</td>
<td align="right"></td>
<td align="right">3,560,753,058</td>
<td align="right"></td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">Increfs</td>
<td align="right">26,928,614,004</td>
<td align="right">22.4%</td>
<td align="right">26,887,876,137</td>
<td align="right">22.4%</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">Decrefs</td>
<td align="right">29,777,474,382</td>
<td align="right">21.6%</td>
<td align="right">29,733,931,391</td>
<td align="right">21.6%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">Interpreter increfs</td>
<td align="right">93,264,173,821</td>
<td align="right">77.6%</td>
<td align="right">93,316,709,505</td>
<td align="right">77.6%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">Interpreter decrefs</td>
<td align="right">107,905,997,248</td>
<td align="right">78.4%</td>
<td align="right">107,860,101,880</td>
<td align="right">78.4%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">Allocations to 4 kbytes</td>
<td align="right">104,769,422</td>
<td align="right">0.6%</td>
<td align="right">104,808,384</td>
<td align="right">0.6%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Materialize dict (on request)</td>
<td align="right">6,618,746</td>
<td align="right">3.6%</td>
<td align="right">6,618,746</td>
<td align="right">3.6%</td>
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
<td align="right">115,780,116</td>
<td align="right">17,033,683,899</td>
<td align="right">0</td>
<td align="right">115,764,966</td>
<td align="right">17,066,972,016</td>
</tr>
<tr>
<td align="right">2</td>
<td align="right">0</td>
<td align="right">10,755,840</td>
<td align="right">6,967,056,310</td>
<td align="right">0</td>
<td align="right">10,755,840</td>
<td align="right">6,967,056,910</td>
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
<td align="right">1,531</td>
<td align="right">0.2%</td>
<td align="right">1,829</td>
<td align="right">0.3%</td>
<td align="right">19.5%</td>
</tr>
<tr>
<td align="left">
Trace stack underflow
<details>
<summary>ⓘ</summary>

A potential trace is abandoned because it pops more frames than it pushes.
</details>
</td>
<td align="right">132,414</td>
<td align="right">20.2%</td>
<td align="right">156,675</td>
<td align="right">23.8%</td>
<td align="right">18.3%</td>
</tr>
<tr>
<td align="left">
Low confidence
<details>
<summary>ⓘ</summary>

A trace is abandoned because the likelihood of the jump to top being taken is too low.
</details>
</td>
<td align="right">6,783</td>
<td align="right">1.0%</td>
<td align="right">7,344</td>
<td align="right">1.1%</td>
<td align="right">8.3%</td>
</tr>
<tr>
<td align="left">
Traces created
<details>
<summary>ⓘ</summary>

The number of traces that were successfully created.
</details>
</td>
<td align="right">108,430</td>
<td align="right">16.5%</td>
<td align="right">116,177</td>
<td align="right">17.7%</td>
<td align="right">7.1%</td>
</tr>
<tr>
<td align="left">
Traces executed
<details>
<summary>ⓘ</summary>

The number of traces that were executed
</details>
</td>
<td align="right">6,370,249,272</td>
<td align="right"></td>
<td align="right">6,554,634,258</td>
<td align="right"></td>
<td align="right">2.9%</td>
</tr>
<tr>
<td align="left">
Inner loop found
<details>
<summary>ⓘ</summary>

A trace is truncated because it has an inner loop
</details>
</td>
<td align="right">16,419</td>
<td align="right">2.5%</td>
<td align="right">16,773</td>
<td align="right">2.5%</td>
<td align="right">2.2%</td>
</tr>
<tr>
<td align="left">
Uops executed
<details>
<summary>ⓘ</summary>

The total number of uops (micro-operations) that were executed
</details>
</td>
<td align="right">175,486,485,789</td>
<td align="right">2,754.8%</td>
<td align="right">178,167,114,485</td>
<td align="right">2,718.2%</td>
<td align="right">1.5%</td>
</tr>
<tr>
<td align="left">
Trace too short
<details>
<summary>ⓘ</summary>

A potential trace is abandoced because it it too short.
</details>
</td>
<td align="right">548,303</td>
<td align="right">83.5%</td>
<td align="right">541,722</td>
<td align="right">82.3%</td>
<td align="right">-1.2%</td>
</tr>
<tr>
<td align="left">
Trace stack overflow
<details>
<summary>ⓘ</summary>

A trace is truncated because it would require more than 5 stack frames.
</details>
</td>
<td align="right">614</td>
<td align="right">0.1%</td>
<td align="right">608</td>
<td align="right">0.1%</td>
<td align="right">-1.0%</td>
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
<td align="right">5,480</td>
<td align="right">4.7%</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">
Optimization attempts
<details>
<summary>ⓘ</summary>

The number of times a potential trace is identified.  Specifically, this occurs in the JUMP BACKWARD instruction when the counter reaches a threshold.
</details>
</td>
<td align="right">656,733</td>
<td align="right"></td>
<td align="right">657,899</td>
<td align="right"></td>
<td align="right">0.2%</td>
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
<td align="right">106,270</td>
<td align="right">98.0%</td>
<td align="right">114,017</td>
<td align="right">98.1%</td>
<td align="right">7.3%</td>
</tr>
<tr>
<td align="left">
Optimizer attempts
<details>
<summary>ⓘ</summary>

The number of times the trace optimizer (_Py_uop_analyze_and_optimize) was run.
</details>
</td>
<td align="right">108,430</td>
<td align="right"></td>
<td align="right">116,177</td>
<td align="right"></td>
<td align="right">7.1%</td>
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
<td align="right">1.8%</td>
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
<td align="right">2,790</td>
<td align="right">2.6%</td>
<td align="right">3,293</td>
<td align="right">2.8%</td>
<td align="right">18.0%</td>
</tr>
<tr>
<td align="left"><= 16</td>
<td align="right">16,891</td>
<td align="right">15.6%</td>
<td align="right">18,399</td>
<td align="right">15.8%</td>
<td align="right">8.9%</td>
</tr>
<tr>
<td align="left"><= 32</td>
<td align="right">41,758</td>
<td align="right">38.5%</td>
<td align="right">44,125</td>
<td align="right">38.0%</td>
<td align="right">5.7%</td>
</tr>
<tr>
<td align="left"><= 64</td>
<td align="right">26,580</td>
<td align="right">24.5%</td>
<td align="right">28,264</td>
<td align="right">24.3%</td>
<td align="right">6.3%</td>
</tr>
<tr>
<td align="left"><= 128</td>
<td align="right">14,961</td>
<td align="right">13.8%</td>
<td align="right">15,959</td>
<td align="right">13.7%</td>
<td align="right">6.7%</td>
</tr>
<tr>
<td align="left"><= 256</td>
<td align="right">4,585</td>
<td align="right">4.2%</td>
<td align="right">5,268</td>
<td align="right">4.5%</td>
<td align="right">14.9%</td>
</tr>
<tr>
<td align="left"><= 512</td>
<td align="right">865</td>
<td align="right">0.8%</td>
<td align="right">849</td>
<td align="right">0.7%</td>
<td align="right">-1.8%</td>
</tr>
<tr>
<td align="left"><= 1,024</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">20</td>
<td align="right">0.0%</td>
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
<td align="right">618</td>
<td align="right">0.6%</td>
<td align="right">1,040</td>
<td align="right">0.9%</td>
<td align="right">68.3%</td>
</tr>
<tr>
<td align="left"><= 8</td>
<td align="right">8,936</td>
<td align="right">8.2%</td>
<td align="right">9,670</td>
<td align="right">8.3%</td>
<td align="right">8.2%</td>
</tr>
<tr>
<td align="left"><= 16</td>
<td align="right">34,198</td>
<td align="right">31.5%</td>
<td align="right">36,564</td>
<td align="right">31.5%</td>
<td align="right">6.9%</td>
</tr>
<tr>
<td align="left"><= 32</td>
<td align="right">35,010</td>
<td align="right">32.3%</td>
<td align="right">37,125</td>
<td align="right">32.0%</td>
<td align="right">6.0%</td>
</tr>
<tr>
<td align="left"><= 64</td>
<td align="right">18,078</td>
<td align="right">16.7%</td>
<td align="right">19,508</td>
<td align="right">16.8%</td>
<td align="right">7.9%</td>
</tr>
<tr>
<td align="left"><= 128</td>
<td align="right">7,361</td>
<td align="right">6.8%</td>
<td align="right">8,001</td>
<td align="right">6.9%</td>
<td align="right">8.7%</td>
</tr>
<tr>
<td align="left"><= 256</td>
<td align="right">1,849</td>
<td align="right">1.7%</td>
<td align="right">1,889</td>
<td align="right">1.6%</td>
<td align="right">2.2%</td>
</tr>
<tr>
<td align="left"><= 512</td>
<td align="right">220</td>
<td align="right">0.2%</td>
<td align="right">220</td>
<td align="right">0.2%</td>
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
<td align="right">25,552,980</td>
<td align="right">0.4%</td>
<td align="right">25,552,980</td>
<td align="right">0.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left"><= 4</td>
<td align="right">558,472,421</td>
<td align="right">8.8%</td>
<td align="right">560,908,480</td>
<td align="right">8.6%</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left"><= 8</td>
<td align="right">798,530,236</td>
<td align="right">12.5%</td>
<td align="right">837,924,163</td>
<td align="right">12.8%</td>
<td align="right">4.9%</td>
</tr>
<tr>
<td align="left"><= 16</td>
<td align="right">1,156,938,584</td>
<td align="right">18.2%</td>
<td align="right">1,226,789,227</td>
<td align="right">18.7%</td>
<td align="right">6.0%</td>
</tr>
<tr>
<td align="left"><= 32</td>
<td align="right">1,124,779,519</td>
<td align="right">17.7%</td>
<td align="right">1,194,874,849</td>
<td align="right">18.2%</td>
<td align="right">6.2%</td>
</tr>
<tr>
<td align="left"><= 64</td>
<td align="right">591,882,059</td>
<td align="right">9.3%</td>
<td align="right">602,375,316</td>
<td align="right">9.2%</td>
<td align="right">1.8%</td>
</tr>
<tr>
<td align="left"><= 128</td>
<td align="right">280,246,879</td>
<td align="right">4.4%</td>
<td align="right">283,141,178</td>
<td align="right">4.3%</td>
<td align="right">1.0%</td>
</tr>
<tr>
<td align="left"><= 256</td>
<td align="right">145,385,655</td>
<td align="right">2.3%</td>
<td align="right">145,718,532</td>
<td align="right">2.2%</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left"><= 512</td>
<td align="right">15,935,642</td>
<td align="right">0.3%</td>
<td align="right">15,930,836</td>
<td align="right">0.2%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left"><= 1,024</td>
<td align="right">6,387,361</td>
<td align="right">0.1%</td>
<td align="right">6,387,328</td>
<td align="right">0.1%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left"><= 2,048</td>
<td align="right">18,353,584</td>
<td align="right">0.3%</td>
<td align="right">17,713,572</td>
<td align="right">0.3%</td>
<td align="right">-3.5%</td>
</tr>
<tr>
<td align="left"><= 4,096</td>
<td align="right">644,608</td>
<td align="right">0.0%</td>
<td align="right">644,614</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left"><= 8,192</td>
<td align="right">744,956</td>
<td align="right">0.0%</td>
<td align="right">744,940</td>
<td align="right">0.0%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left"><= 16,384</td>
<td align="right">245,681</td>
<td align="right">0.0%</td>
<td align="right">245,681</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left"><= 32,768</td>
<td align="right">42,640</td>
<td align="right">0.0%</td>
<td align="right">42,640</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left"><= 65,536</td>
<td align="right">13,496</td>
<td align="right">0.0%</td>
<td align="right">13,584</td>
<td align="right">0.0%</td>
<td align="right">0.7%</td>
</tr>
<tr>
<td align="left"><= 131,072</td>
<td align="right">745</td>
<td align="right">0.0%</td>
<td align="right">657</td>
<td align="right">0.0%</td>
<td align="right">-11.8%</td>
</tr>
<tr>
<td align="left"><= 262,144</td>
<td align="right">2,080</td>
<td align="right">0.0%</td>
<td align="right">2,080</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left"><= 524,288</td>
<td align="right">460</td>
<td align="right">0.0%</td>
<td align="right">476</td>
<td align="right">0.0%</td>
<td align="right">3.5%</td>
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
<td align="right">220</td>
<td align="right">0.0%</td>
<td align="right">236</td>
<td align="right">0.0%</td>
<td align="right">7.3%</td>
</tr>
<tr>
<td align="left"><= 4,194,304</td>
<td align="right">260</td>
<td align="right">0.0%</td>
<td align="right">244</td>
<td align="right">0.0%</td>
<td align="right">-6.2%</td>
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
<td align="left">_LOAD_ATTR_CLASS_1</td>
<td align="right">3,840</td>
<td align="right">20,485,700</td>
<td align="right">533,381.8%</td>
</tr>
<tr>
<td align="left">_CHECK_ATTR_WITH_HINT</td>
<td align="right">97,384,385</td>
<td align="right">217,276,368</td>
<td align="right">123.1%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_WITH_HINT</td>
<td align="right">97,273,524</td>
<td align="right">216,695,767</td>
<td align="right">122.8%</td>
</tr>
<tr>
<td align="left">_CHECK_ATTR_CLASS</td>
<td align="right">25,021,813</td>
<td align="right">45,487,933</td>
<td align="right">81.8%</td>
</tr>
<tr>
<td align="left">_ERROR_POP_N</td>
<td align="right">486,517</td>
<td align="right">598,968</td>
<td align="right">23.1%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_NONDESCRIPTOR_NO_DICT</td>
<td align="right">21,767,657</td>
<td align="right">25,851,335</td>
<td align="right">18.8%</td>
</tr>
<tr>
<td align="left">_STORE_ATTR</td>
<td align="right">51,270,753</td>
<td align="right">58,620,909</td>
<td align="right">14.3%</td>
</tr>
<tr>
<td align="left">_CHECK_STACK_SPACE</td>
<td align="right">164,088,539</td>
<td align="right">186,159,738</td>
<td align="right">13.5%</td>
</tr>
<tr>
<td align="left">_RESUME_CHECK</td>
<td align="right">1,307,901,186</td>
<td align="right">1,478,227,491</td>
<td align="right">13.0%</td>
</tr>
<tr>
<td align="left">_COMPARE_OP</td>
<td align="right">92,895,496</td>
<td align="right">104,419,913</td>
<td align="right">12.4%</td>
</tr>
<tr>
<td align="left">_LOAD_GLOBAL_MODULE</td>
<td align="right">44,267,468</td>
<td align="right">49,492,448</td>
<td align="right">11.8%</td>
</tr>
<tr>
<td align="left">_BUILD_CONST_KEY_MAP</td>
<td align="right">79,650</td>
<td align="right">89,034</td>
<td align="right">11.8%</td>
</tr>
<tr>
<td align="left">_GUARD_GLOBALS_VERSION</td>
<td align="right">50,855,144</td>
<td align="right">56,700,884</td>
<td align="right">11.5%</td>
</tr>
<tr>
<td align="left">_LOAD_SUPER_ATTR_METHOD</td>
<td align="right">95,777</td>
<td align="right">106,527</td>
<td align="right">11.2%</td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">226,344,840</td>
<td align="right">251,191,887</td>
<td align="right">11.0%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_2</td>
<td align="right">705,063,855</td>
<td align="right">774,803,247</td>
<td align="right">9.9%</td>
</tr>
<tr>
<td align="left">_LOAD_GLOBAL_BUILTINS</td>
<td align="right">6,587,676</td>
<td align="right">7,208,436</td>
<td align="right">9.4%</td>
</tr>
<tr>
<td align="left">_GUARD_BOTH_INT</td>
<td align="right">533,783,127</td>
<td align="right">582,308,938</td>
<td align="right">9.1%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_NONE_POP</td>
<td align="right">41,580,210</td>
<td align="right">45,258,921</td>
<td align="right">8.8%</td>
</tr>
<tr>
<td align="left">_BINARY_SUBSCR</td>
<td align="right">1,241,225,463</td>
<td align="right">1,144,392,363</td>
<td align="right">-7.8%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_CHECK</td>
<td align="right">251,821</td>
<td align="right">271,348</td>
<td align="right">7.8%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR</td>
<td align="right">1,096,188,816</td>
<td align="right">1,166,698,274</td>
<td align="right">6.4%</td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">184,291,813</td>
<td align="right">194,888,838</td>
<td align="right">5.8%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_ADD_FLOAT</td>
<td align="right">571,783,760</td>
<td align="right">539,783,780</td>
<td align="right">-5.6%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_NOT_NONE_POP</td>
<td align="right">148,449,755</td>
<td align="right">156,628,160</td>
<td align="right">5.5%</td>
</tr>
<tr>
<td align="left">_COMPARE_OP_INT</td>
<td align="right">943,369,556</td>
<td align="right">995,155,545</td>
<td align="right">5.5%</td>
</tr>
<tr>
<td align="left">_GUARD_TYPE_VERSION</td>
<td align="right">5,365,738,963</td>
<td align="right">5,649,014,769</td>
<td align="right">5.3%</td>
</tr>
<tr>
<td align="left">_GUARD_NOS_FLOAT</td>
<td align="right">628,576,613</td>
<td align="right">597,231,690</td>
<td align="right">-5.0%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_1</td>
<td align="right">526,176,020</td>
<td align="right">551,777,818</td>
<td align="right">4.9%</td>
</tr>
<tr>
<td align="left">_LOAD_CONST_INLINE</td>
<td align="right">1,233,829,076</td>
<td align="right">1,291,305,073</td>
<td align="right">4.7%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_AND_CLEAR</td>
<td align="right">15,829,691</td>
<td align="right">16,556,286</td>
<td align="right">4.6%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_INT</td>
<td align="right">194,774,966</td>
<td align="right">203,710,223</td>
<td align="right">4.6%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_0</td>
<td align="right">5,321,119,176</td>
<td align="right">5,562,010,597</td>
<td align="right">4.5%</td>
</tr>
<tr>
<td align="left">_ITER_NEXT_RANGE</td>
<td align="right">734,215,481</td>
<td align="right">701,805,848</td>
<td align="right">-4.4%</td>
</tr>
<tr>
<td align="left">_SIDE_EXIT</td>
<td align="right">3,625,665,320</td>
<td align="right">3,777,999,574</td>
<td align="right">4.2%</td>
</tr>
<tr>
<td align="left">_GUARD_NOT_EXHAUSTED_RANGE</td>
<td align="right">782,320,734</td>
<td align="right">750,021,973</td>
<td align="right">-4.1%</td>
</tr>
<tr>
<td align="left">_START_EXECUTOR</td>
<td align="right">4,724,160,706</td>
<td align="right">4,919,012,253</td>
<td align="right">4.1%</td>
</tr>
<tr>
<td align="left">_ITER_CHECK_RANGE</td>
<td align="right">783,678,494</td>
<td align="right">751,379,733</td>
<td align="right">-4.1%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_3</td>
<td align="right">624,584,885</td>
<td align="right">650,117,616</td>
<td align="right">4.1%</td>
</tr>
<tr>
<td align="left">_CONTAINS_OP</td>
<td align="right">107,368,579</td>
<td align="right">111,574,399</td>
<td align="right">3.9%</td>
</tr>
<tr>
<td align="left">_DEOPT</td>
<td align="right">1,098,008,869</td>
<td align="right">1,140,413,711</td>
<td align="right">3.9%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_4</td>
<td align="right">656,319,488</td>
<td align="right">680,966,602</td>
<td align="right">3.8%</td>
</tr>
<tr>
<td align="left">_GUARD_BOTH_FLOAT</td>
<td align="right">867,639,459</td>
<td align="right">835,641,069</td>
<td align="right">-3.7%</td>
</tr>
<tr>
<td align="left">_BINARY_SUBSCR_DICT</td>
<td align="right">258,322,890</td>
<td align="right">267,542,371</td>
<td align="right">3.6%</td>
</tr>
<tr>
<td align="left">_GET_ITER</td>
<td align="right">244,368,133</td>
<td align="right">252,908,005</td>
<td align="right">3.5%</td>
</tr>
<tr>
<td align="left">_EXIT_TRACE</td>
<td align="right">2,744,167,695</td>
<td align="right">2,839,539,396</td>
<td align="right">3.5%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_NONE</td>
<td align="right">173,061,678</td>
<td align="right">178,692,857</td>
<td align="right">3.3%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_LIST</td>
<td align="right">54,119,756</td>
<td align="right">55,737,123</td>
<td align="right">3.0%</td>
</tr>
<tr>
<td align="left">_IS_OP</td>
<td align="right">332,330,456</td>
<td align="right">341,830,497</td>
<td align="right">2.9%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_SLOT_0</td>
<td align="right">705,159,041</td>
<td align="right">725,310,784</td>
<td align="right">2.9%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_MULTIPLY_FLOAT</td>
<td align="right">1,124,307,821</td>
<td align="right">1,092,322,913</td>
<td align="right">-2.8%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">828,952,622</td>
<td align="right">852,188,573</td>
<td align="right">2.8%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">909,966,021</td>
<td align="right">934,485,659</td>
<td align="right">2.7%</td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION</td>
<td align="right">1,272,278,513</td>
<td align="right">1,306,286,274</td>
<td align="right">2.7%</td>
</tr>
<tr>
<td align="left">_STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">102,700,557</td>
<td align="right">105,443,200</td>
<td align="right">2.7%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_2</td>
<td align="right">104,654,791</td>
<td align="right">107,449,439</td>
<td align="right">2.7%</td>
</tr>
<tr>
<td align="left">_GUARD_DORV_NO_DICT</td>
<td align="right">104,008,317</td>
<td align="right">106,750,960</td>
<td align="right">2.6%</td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_O</td>
<td align="right">22,166,196</td>
<td align="right">22,748,655</td>
<td align="right">2.6%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS</td>
<td align="right">9,518,262</td>
<td align="right">9,765,743</td>
<td align="right">2.6%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_ADD_UNICODE</td>
<td align="right">23,610,827</td>
<td align="right">24,221,027</td>
<td align="right">2.6%</td>
</tr>
<tr>
<td align="left">_GUARD_DORV_VALUES_INST_ATTR_FROM_DICT</td>
<td align="right">1,045,858,166</td>
<td align="right">1,072,807,619</td>
<td align="right">2.6%</td>
</tr>
<tr>
<td align="left">_GUARD_KEYS_VERSION</td>
<td align="right">1,002,734,585</td>
<td align="right">1,028,344,121</td>
<td align="right">2.6%</td>
</tr>
<tr>
<td align="left">_PUSH_NULL</td>
<td align="right">727,518,075</td>
<td align="right">745,547,917</td>
<td align="right">2.5%</td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION_EXACT_ARGS</td>
<td align="right">1,586,931,055</td>
<td align="right">1,625,539,599</td>
<td align="right">2.4%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_1</td>
<td align="right">6,198,544,866</td>
<td align="right">6,346,987,377</td>
<td align="right">2.4%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_INSTANCE_VALUE_0</td>
<td align="right">1,883,312,840</td>
<td align="right">1,926,523,160</td>
<td align="right">2.3%</td>
</tr>
<tr>
<td align="left">_CHECK_MANAGED_OBJECT_HAS_VALUES</td>
<td align="right">1,887,087,596</td>
<td align="right">1,930,297,956</td>
<td align="right">2.3%</td>
</tr>
<tr>
<td align="left">_BUILD_LIST</td>
<td align="right">245,589,497</td>
<td align="right">250,995,314</td>
<td align="right">2.2%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_TRUE_POP</td>
<td align="right">2,564,803,552</td>
<td align="right">2,620,036,651</td>
<td align="right">2.2%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_STR</td>
<td align="right">24,373,592</td>
<td align="right">24,898,272</td>
<td align="right">2.2%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">73,594,906</td>
<td align="right">75,153,257</td>
<td align="right">2.1%</td>
</tr>
<tr>
<td align="left">_CHECK_CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">73,648,346</td>
<td align="right">75,206,697</td>
<td align="right">2.1%</td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_O</td>
<td align="right">614,581,396</td>
<td align="right">627,549,605</td>
<td align="right">2.1%</td>
</tr>
<tr>
<td align="left">_PUSH_FRAME</td>
<td align="right">1,526,983,882</td>
<td align="right">1,558,053,745</td>
<td align="right">2.0%</td>
</tr>
<tr>
<td align="left">_SAVE_RETURN_OFFSET</td>
<td align="right">1,526,983,882</td>
<td align="right">1,558,053,745</td>
<td align="right">2.0%</td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_FAST_WITH_KEYWORDS</td>
<td align="right">21,929,524</td>
<td align="right">22,371,821</td>
<td align="right">2.0%</td>
</tr>
<tr>
<td align="left">_CALL_LEN</td>
<td align="right">195,711,717</td>
<td align="right">199,630,608</td>
<td align="right">2.0%</td>
</tr>
<tr>
<td align="left">_BINARY_OP</td>
<td align="right">855,018,408</td>
<td align="right">871,750,401</td>
<td align="right">2.0%</td>
</tr>
<tr>
<td align="left">_STORE_FAST</td>
<td align="right">2,959,460,528</td>
<td align="right">2,904,886,419</td>
<td align="right">-1.8%</td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_CLASS</td>
<td align="right">57,228,439</td>
<td align="right">58,243,490</td>
<td align="right">1.8%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_2</td>
<td align="right">2,704,959,534</td>
<td align="right">2,751,961,476</td>
<td align="right">1.7%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST</td>
<td align="right">5,464,387,738</td>
<td align="right">5,371,473,309</td>
<td align="right">-1.7%</td>
</tr>
<tr>
<td align="left">_CALL_INTRINSIC_1</td>
<td align="right">96,027,810</td>
<td align="right">97,546,522</td>
<td align="right">1.6%</td>
</tr>
<tr>
<td align="left">_LIST_EXTEND</td>
<td align="right">96,951,610</td>
<td align="right">98,470,322</td>
<td align="right">1.6%</td>
</tr>
<tr>
<td align="left">_CHECK_PERIODIC</td>
<td align="right">2,127,267,169</td>
<td align="right">2,160,080,124</td>
<td align="right">1.5%</td>
</tr>
<tr>
<td align="left">_JUMP_TO_TOP</td>
<td align="right">2,101,489,287</td>
<td align="right">2,070,617,121</td>
<td align="right">-1.5%</td>
</tr>
<tr>
<td align="left">_CONTAINS_OP_DICT</td>
<td align="right">360,094,553</td>
<td align="right">365,381,840</td>
<td align="right">1.5%</td>
</tr>
<tr>
<td align="left">_CALL_ISINSTANCE</td>
<td align="right">310,095,538</td>
<td align="right">314,544,567</td>
<td align="right">1.4%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_5</td>
<td align="right">2,051,596,597</td>
<td align="right">2,022,464,242</td>
<td align="right">-1.4%</td>
</tr>
<tr>
<td align="left">_BUILD_TUPLE</td>
<td align="right">373,172,533</td>
<td align="right">378,439,075</td>
<td align="right">1.4%</td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_FAST_WITH_KEYWORDS</td>
<td align="right">153,743,212</td>
<td align="right">155,902,235</td>
<td align="right">1.4%</td>
</tr>
<tr>
<td align="left">_BUILD_MAP</td>
<td align="right">9,870,212</td>
<td align="right">10,002,140</td>
<td align="right">1.3%</td>
</tr>
<tr>
<td align="left">_POP_TOP</td>
<td align="right">698,416,247</td>
<td align="right">707,666,364</td>
<td align="right">1.3%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_3</td>
<td align="right">3,096,466,782</td>
<td align="right">3,135,142,541</td>
<td align="right">1.2%</td>
</tr>
<tr>
<td align="left">_UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">618,687,772</td>
<td align="right">626,080,621</td>
<td align="right">1.2%</td>
</tr>
<tr>
<td align="left">_BINARY_SLICE</td>
<td align="right">119,832,365</td>
<td align="right">121,229,833</td>
<td align="right">1.2%</td>
</tr>
<tr>
<td align="left">_TO_BOOL</td>
<td align="right">235,150,980</td>
<td align="right">237,804,667</td>
<td align="right">1.1%</td>
</tr>
<tr>
<td align="left">_CHECK_VALIDITY</td>
<td align="right">9,837,811,400</td>
<td align="right">9,931,250,176</td>
<td align="right">0.9%</td>
</tr>
<tr>
<td align="left">_CHECK_ATTR_METHOD_LAZY_DICT</td>
<td align="right">97,309,736</td>
<td align="right">98,230,337</td>
<td align="right">0.9%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_METHOD_LAZY_DICT</td>
<td align="right">97,309,736</td>
<td align="right">98,230,337</td>
<td align="right">0.9%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_FALSE_POP</td>
<td align="right">5,302,773,802</td>
<td align="right">5,350,803,608</td>
<td align="right">0.9%</td>
</tr>
<tr>
<td align="left">_SET_IP</td>
<td align="right">16,376,669,986</td>
<td align="right">16,511,264,507</td>
<td align="right">0.8%</td>
</tr>
<tr>
<td align="left">_STORE_ATTR_SLOT</td>
<td align="right">124,257,302</td>
<td align="right">125,277,724</td>
<td align="right">0.8%</td>
</tr>
<tr>
<td align="left">_CHECK_STACK_SPACE_OPERAND</td>
<td align="right">866,748,880</td>
<td align="right">873,691,394</td>
<td align="right">0.8%</td>
</tr>
<tr>
<td align="left">_LOAD_CONST_INLINE_BORROW</td>
<td align="right">8,893,985,470</td>
<td align="right">8,961,665,289</td>
<td align="right">0.8%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_BOOL</td>
<td align="right">1,935,295,670</td>
<td align="right">1,948,608,580</td>
<td align="right">0.7%</td>
</tr>
<tr>
<td align="left">_COPY</td>
<td align="right">1,252,534,966</td>
<td align="right">1,261,118,691</td>
<td align="right">0.7%</td>
</tr>
<tr>
<td align="left">_COLD_EXIT</td>
<td align="right">1,646,088,566</td>
<td align="right">1,635,622,005</td>
<td align="right">-0.6%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right">88,597,947</td>
<td align="right">89,145,067</td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_6</td>
<td align="right">417,209,519</td>
<td align="right">419,763,861</td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">_LOAD_CONST_INLINE_WITH_NULL</td>
<td align="right">1,653,573,531</td>
<td align="right">1,663,661,411</td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_0</td>
<td align="right">381,700,101</td>
<td align="right">383,978,660</td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_1</td>
<td align="right">1,849,722,297</td>
<td align="right">1,860,581,940</td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">_ITER_NEXT_LIST</td>
<td align="right">1,205,991,704</td>
<td align="right">1,212,132,560</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">_GUARD_NOT_EXHAUSTED_LIST</td>
<td align="right">1,491,239,283</td>
<td align="right">1,498,604,596</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">_ITER_CHECK_LIST</td>
<td align="right">1,505,536,215</td>
<td align="right">1,512,744,151</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_5</td>
<td align="right">647,090,222</td>
<td align="right">650,175,037</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">_POP_FRAME</td>
<td align="right">553,391,333</td>
<td align="right">555,891,946</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">_REPLACE_WITH_TRUE</td>
<td align="right">32,284,850</td>
<td align="right">32,423,807</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">_FOR_ITER_TIER_TWO</td>
<td align="right">409,448,843</td>
<td align="right">411,177,926</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">_BINARY_SUBSCR_LIST_INT</td>
<td align="right">1,055,881,073</td>
<td align="right">1,059,758,340</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">_LOAD_GLOBAL</td>
<td align="right">188,828,426</td>
<td align="right">189,485,121</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">_GUARD_BOTH_UNICODE</td>
<td align="right">965,850,642</td>
<td align="right">968,707,550</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">_SWAP</td>
<td align="right">1,130,160,487</td>
<td align="right">1,133,445,230</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">_LOAD_CONST_INLINE_BORROW_WITH_NULL</td>
<td align="right">364,441,929</td>
<td align="right">365,470,971</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">_CONTAINS_OP_SET</td>
<td align="right">1,477,442,065</td>
<td align="right">1,481,506,334</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_0</td>
<td align="right">204,628,371</td>
<td align="right">205,184,387</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">_CHECK_VALIDITY_AND_SET_IP</td>
<td align="right">1,034,049,186</td>
<td align="right">1,031,570,941</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_7</td>
<td align="right">1,202,304,630</td>
<td align="right">1,204,798,579</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">_COPY_FREE_VARS</td>
<td align="right">49,438,149</td>
<td align="right">49,533,496</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_4</td>
<td align="right">1,969,094,726</td>
<td align="right">1,965,375,045</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">_GUARD_NOS_INT</td>
<td align="right">2,421,611,649</td>
<td align="right">2,425,358,358</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBTRACT_INT</td>
<td align="right">442,139,368</td>
<td align="right">442,822,959</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">_BUILD_STRING</td>
<td align="right">595,780</td>
<td align="right">596,698</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">_LIST_APPEND</td>
<td align="right">182,495,573</td>
<td align="right">182,737,607</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">_COMPARE_OP_STR</td>
<td align="right">1,825,064,208</td>
<td align="right">1,827,453,015</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">_FORMAT_SIMPLE</td>
<td align="right">1,407,265</td>
<td align="right">1,409,101</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">_STORE_SUBSCR_LIST_INT</td>
<td align="right">478,864,182</td>
<td align="right">479,484,942</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_6</td>
<td align="right">1,242,695,754</td>
<td align="right">1,244,235,871</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">_UNPACK_SEQUENCE_LIST</td>
<td align="right">77,567,280</td>
<td align="right">77,645,160</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_ADD_INT</td>
<td align="right">2,490,219,529</td>
<td align="right">2,492,336,283</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">_LOAD_DEREF</td>
<td align="right">447,488,881</td>
<td align="right">447,123,054</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">_MAKE_FUNCTION</td>
<td align="right">60,639,050</td>
<td align="right">60,683,103</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">_BINARY_SUBSCR_TUPLE_INT</td>
<td align="right">147,485,036</td>
<td align="right">147,384,356</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">_UNARY_NEGATIVE</td>
<td align="right">25,045,777</td>
<td align="right">25,062,819</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_7</td>
<td align="right">3,376,624,538</td>
<td align="right">3,378,823,489</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_FAST</td>
<td align="right">789,068,744</td>
<td align="right">789,563,493</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">_SET_FUNCTION_ATTRIBUTE</td>
<td align="right">47,058,000</td>
<td align="right">47,085,793</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">_CHECK_ATTR_MODULE</td>
<td align="right">6,479,263</td>
<td align="right">6,483,078</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_MODULE</td>
<td align="right">6,479,263</td>
<td align="right">6,483,078</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_3</td>
<td align="right">56,651,034</td>
<td align="right">56,623,938</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_4</td>
<td align="right">448,283,674</td>
<td align="right">448,458,147</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_MAKE_CELL</td>
<td align="right">5,622,718</td>
<td align="right">5,624,614</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_GUARD_NOT_EXHAUSTED_TUPLE</td>
<td align="right">466,195,401</td>
<td align="right">466,320,164</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_ITER_CHECK_TUPLE</td>
<td align="right">543,433,786</td>
<td align="right">543,559,421</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_STORE_SUBSCR_DICT</td>
<td align="right">143,857,203</td>
<td align="right">143,884,206</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_CALL_TYPE_1</td>
<td align="right">237,600,389</td>
<td align="right">237,561,036</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">_STORE_NAME</td>
<td align="right">545,860</td>
<td align="right">545,940</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_ITER_NEXT_TUPLE</td>
<td align="right">311,608,715</td>
<td align="right">311,652,158</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_CLASS_0</td>
<td align="right">23,413,597</td>
<td align="right">23,416,157</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_BINARY_SUBSCR_STR_INT</td>
<td align="right">1,215,773,770</td>
<td align="right">1,215,880,867</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_UNPACK_SEQUENCE_TUPLE</td>
<td align="right">188,189,848</td>
<td align="right">188,204,269</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_SET_ADD</td>
<td align="right">1,449,212</td>
<td align="right">1,449,260</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_MAP_ADD</td>
<td align="right">20,605,006</td>
<td align="right">20,605,624</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_STORE_SUBSCR</td>
<td align="right">317,350,202</td>
<td align="right">317,357,609</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_COMPARE_OP_FLOAT</td>
<td align="right">70,082,490</td>
<td align="right">70,084,086</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_UNPACK_SEQUENCE</td>
<td align="right">1,554,886</td>
<td align="right">1,554,918</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_CALL_STR_1</td>
<td align="right">66,199,794</td>
<td align="right">66,200,274</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_MULTIPLY_INT</td>
<td align="right">184,971,238</td>
<td align="right">184,970,024</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">_DICT_MERGE</td>
<td align="right">7,203,048</td>
<td align="right">7,203,059</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_GUARD_TOS_INT</td>
<td align="right">209,266,121</td>
<td align="right">209,266,355</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_UNARY_NOT</td>
<td align="right">62,209,908</td>
<td align="right">62,209,885</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBTRACT_FLOAT</td>
<td align="right">382,602,700</td>
<td align="right">382,602,700</td>
<td align="right">0.0%</td>
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
<td align="left">_GUARD_TOS_FLOAT</td>
<td align="right">58,173,820</td>
<td align="right">58,173,820</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_UNARY_INVERT</td>
<td align="right">12,534,740</td>
<td align="right">12,534,740</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_INSTANCE_VALUE_1</td>
<td align="right">3,664,036</td>
<td align="right">3,664,036</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_STORE_DEREF</td>
<td align="right">2,930,205</td>
<td align="right">2,930,205</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_DELETE_SUBSCR</td>
<td align="right">1,428,140</td>
<td align="right">1,428,140</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_STORE_GLOBAL</td>
<td align="right">1,260,560</td>
<td align="right">1,260,560</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_POP_TOP_LOAD_CONST_INLINE_BORROW</td>
<td align="right">1,239,857</td>
<td align="right">1,239,857</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_CONVERT_VALUE</td>
<td align="right">790,640</td>
<td align="right">790,640</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_CALL_TUPLE_1</td>
<td align="right">572,540</td>
<td align="right">572,540</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_GET_YIELD_FROM_ITER</td>
<td align="right">179,880</td>
<td align="right">179,880</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_GUARD_BUILTINS_VERSION</td>
<td align="right">38,636</td>
<td align="right">38,636</td>
<td align="right">0.0%</td>
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
<td align="left">IMPORT_NAME</td>
<td align="right">266</td>
<td align="right">586</td>
<td align="right">120.3%</td>
</tr>
<tr>
<td align="left">BEFORE_WITH</td>
<td align="right">220</td>
<td align="right">400</td>
<td align="right">81.8%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_WITH_HINT</td>
<td align="right">180</td>
<td align="right">240</td>
<td align="right">33.3%</td>
</tr>
<tr>
<td align="left">CALL_LIST_APPEND</td>
<td align="right">5,994</td>
<td align="right">6,394</td>
<td align="right">6.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_PROPERTY</td>
<td align="right">6,644</td>
<td align="right">6,925</td>
<td align="right">4.2%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">126,873</td>
<td align="right">132,121</td>
<td align="right">4.1%</td>
</tr>
<tr>
<td align="left">CALL_KW</td>
<td align="right">25,949</td>
<td align="right">26,868</td>
<td align="right">3.5%</td>
</tr>
<tr>
<td align="left">CALL_PY_WITH_DEFAULTS</td>
<td align="right">9,120</td>
<td align="right">9,280</td>
<td align="right">1.8%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_GETITEM</td>
<td align="right">2,540</td>
<td align="right">2,580</td>
<td align="right">1.6%</td>
</tr>
<tr>
<td align="left">CALL_FUNCTION_EX</td>
<td align="right">2,780</td>
<td align="right">2,821</td>
<td align="right">1.5%</td>
</tr>
<tr>
<td align="left">CALL_ALLOC_AND_ENTER_INIT</td>
<td align="right">1,424</td>
<td align="right">1,444</td>
<td align="right">1.4%</td>
</tr>
<tr>
<td align="left">FOR_ITER_GEN</td>
<td align="right">52,183</td>
<td align="right">52,303</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">RETURN_GENERATOR</td>
<td align="right">40,951</td>
<td align="right">40,996</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">YIELD_VALUE</td>
<td align="right">118,956</td>
<td align="right">119,069</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">34,295</td>
<td align="right"></td>
<td align="right"></td>
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
<td align="left">BINARY_OP_INPLACE_ADD_UNICODE</td>
<td align="right">583</td>
<td align="right">583</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BUILD_SET</td>
<td align="right">226</td>
<td align="right">226</td>
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
Stats gathered on: 2024-04-23
