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
<td align="right">4,970,482,120</td>
<td align="right">141,931,073</td>
<td align="right">-97.1%</td>
</tr>
<tr>
<td align="left">GET_ANEXT</td>
<td align="right">133,515,680</td>
<td align="right">8,000,960</td>
<td align="right">-94.0%</td>
</tr>
<tr>
<td align="left">STORE_SLICE</td>
<td align="right">162,467,576</td>
<td align="right">12,601,193</td>
<td align="right">-92.2%</td>
</tr>
<tr>
<td align="left">UNARY_INVERT</td>
<td align="right">15,124,476</td>
<td align="right">1,811,973</td>
<td align="right">-88.0%</td>
</tr>
<tr>
<td align="left">FOR_ITER_RANGE</td>
<td align="right">842,075,185</td>
<td align="right">107,570,933</td>
<td align="right">-87.2%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_FLOAT</td>
<td align="right">666,979,654</td>
<td align="right">87,683,400</td>
<td align="right">-86.9%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_LIST</td>
<td align="right">89,810,095</td>
<td align="right">12,242,285</td>
<td align="right">-86.4%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_STR</td>
<td align="right">2,155,606,708</td>
<td align="right">323,191,445</td>
<td align="right">-85.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_MULTIPLY_FLOAT</td>
<td align="right">1,382,516,993</td>
<td align="right">210,107,680</td>
<td align="right">-84.8%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_FLOAT</td>
<td align="right">458,477,110</td>
<td align="right">75,737,248</td>
<td align="right">-83.5%</td>
</tr>
<tr>
<td align="left">STORE_FAST_LOAD_FAST</td>
<td align="right">241,664,605</td>
<td align="right">43,015,603</td>
<td align="right">-82.2%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_LIST_INT</td>
<td align="right">589,982,414</td>
<td align="right">110,676,000</td>
<td align="right">-81.2%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_INT</td>
<td align="right">3,169,026,069</td>
<td align="right">674,997,012</td>
<td align="right">-78.7%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST_WITH_KEYWORDS</td>
<td align="right">198,650,322</td>
<td align="right">44,953,393</td>
<td align="right">-77.4%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">541,316,553</td>
<td align="right">128,513,256</td>
<td align="right">-76.3%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP_SET</td>
<td align="right">1,944,989,375</td>
<td align="right">462,870,543</td>
<td align="right">-76.2%</td>
</tr>
<tr>
<td align="left">LIST_EXTEND</td>
<td align="right">127,764,631</td>
<td align="right">30,677,921</td>
<td align="right">-76.0%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">488,840,245</td>
<td align="right">121,008,921</td>
<td align="right">-75.2%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE</td>
<td align="right">2,096,375</td>
<td align="right">540,541</td>
<td align="right">-74.2%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_STR_INT</td>
<td align="right">1,675,423,423</td>
<td align="right">456,452,865</td>
<td align="right">-72.8%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR</td>
<td align="right">1,530,485,333</td>
<td align="right">418,654,890</td>
<td align="right">-72.6%</td>
</tr>
<tr>
<td align="left">LIST_APPEND</td>
<td align="right">256,444,248</td>
<td align="right">73,627,306</td>
<td align="right">-71.3%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">1,602,081,234</td>
<td align="right">468,857,474</td>
<td align="right">-70.7%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR</td>
<td align="right">451,850,910</td>
<td align="right">134,419,192</td>
<td align="right">-70.3%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_LIST_INT</td>
<td align="right">1,516,541,158</td>
<td align="right">459,900,634</td>
<td align="right">-69.7%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">1,819,831,092</td>
<td align="right">563,651,124</td>
<td align="right">-69.0%</td>
</tr>
<tr>
<td align="left">UNARY_NOT</td>
<td align="right">90,619,773</td>
<td align="right">28,297,434</td>
<td align="right">-68.8%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP_DICT</td>
<td align="right">538,256,268</td>
<td align="right">177,089,135</td>
<td align="right">-67.1%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_GETITEM</td>
<td align="right">198,437,621</td>
<td align="right">65,670,426</td>
<td align="right">-66.9%</td>
</tr>
<tr>
<td align="left">BUILD_SLICE</td>
<td align="right">211,876,334</td>
<td align="right">71,718,254</td>
<td align="right">-66.2%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">1,877,754,961</td>
<td align="right">665,444,500</td>
<td align="right">-64.6%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">965,157,850</td>
<td align="right">344,791,449</td>
<td align="right">-64.3%</td>
</tr>
<tr>
<td align="left">SET_ADD</td>
<td align="right">2,414,986</td>
<td align="right">965,800</td>
<td align="right">-60.0%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST</td>
<td align="right">1,340,478,488</td>
<td align="right">549,471,707</td>
<td align="right">-59.0%</td>
</tr>
<tr>
<td align="left">CALL_STR_1</td>
<td align="right">112,950,980</td>
<td align="right">46,758,222</td>
<td align="right">-58.6%</td>
</tr>
<tr>
<td align="left">TO_BOOL_INT</td>
<td align="right">344,244,691</td>
<td align="right">143,790,878</td>
<td align="right">-58.2%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">14,790,772,395</td>
<td align="right">6,282,591,961</td>
<td align="right">-57.5%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">1,397,508,594</td>
<td align="right">608,739,616</td>
<td align="right">-56.4%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">12,618,433,633</td>
<td align="right">5,604,658,825</td>
<td align="right">-55.6%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">14,795,454,245</td>
<td align="right">6,726,111,291</td>
<td align="right">-54.5%</td>
</tr>
<tr>
<td align="left">BINARY_OP_MULTIPLY_INT</td>
<td align="right">361,393,588</td>
<td align="right">164,920,672</td>
<td align="right">-54.4%</td>
</tr>
<tr>
<td align="left">NOP</td>
<td align="right">2,140,202,235</td>
<td align="right">987,677,531</td>
<td align="right">-53.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">11,677,862,974</td>
<td align="right">5,413,441,962</td>
<td align="right">-53.6%</td>
</tr>
<tr>
<td align="left">STORE_FAST_STORE_FAST</td>
<td align="right">973,715,358</td>
<td align="right">451,656,687</td>
<td align="right">-53.6%</td>
</tr>
<tr>
<td align="left">BUILD_LIST</td>
<td align="right">471,497,231</td>
<td align="right">223,493,991</td>
<td align="right">-52.6%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_INT</td>
<td align="right">847,600,707</td>
<td align="right">405,102,505</td>
<td align="right">-52.2%</td>
</tr>
<tr>
<td align="left">FOR_ITER_TUPLE</td>
<td align="right">621,302,374</td>
<td align="right">308,343,569</td>
<td align="right">-50.4%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">2,291,517,012</td>
<td align="right">1,160,009,884</td>
<td align="right">-49.4%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_DICT</td>
<td align="right">296,300,057</td>
<td align="right">150,458,341</td>
<td align="right">-49.2%</td>
</tr>
<tr>
<td align="left">CALL_TYPE_1</td>
<td align="right">483,744,196</td>
<td align="right">246,138,135</td>
<td align="right">-49.1%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">5,927,109,656</td>
<td align="right">3,033,622,371</td>
<td align="right">-48.8%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_O</td>
<td align="right">1,272,362,051</td>
<td align="right">656,843,291</td>
<td align="right">-48.4%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">224,197,027</td>
<td align="right">115,770,395</td>
<td align="right">-48.4%</td>
</tr>
<tr>
<td align="left">STORE_NAME</td>
<td align="right">1,184,382</td>
<td align="right">638,522</td>
<td align="right">-46.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right">219,213,483</td>
<td align="right">121,445,462</td>
<td align="right">-44.6%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT</td>
<td align="right">2,178,017,153</td>
<td align="right">1,223,157,460</td>
<td align="right">-43.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">43,433,953,594</td>
<td align="right">24,541,978,725</td>
<td align="right">-43.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">1,497,908,434</td>
<td align="right">856,388,480</td>
<td align="right">-42.8%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">5,114,165,980</td>
<td align="right">2,951,574,958</td>
<td align="right">-42.3%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">450,963,872</td>
<td align="right">265,379,214</td>
<td align="right">-41.2%</td>
</tr>
<tr>
<td align="left">BINARY_OP_INPLACE_ADD_UNICODE</td>
<td align="right">8,738,017</td>
<td align="right">5,183,255</td>
<td align="right">-40.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">2,907,060,825</td>
<td align="right">1,730,186,883</td>
<td align="right">-40.5%</td>
</tr>
<tr>
<td align="left">IS_OP</td>
<td align="right">838,970,919</td>
<td align="right">500,516,161</td>
<td align="right">-40.3%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_TUPLE_INT</td>
<td align="right">368,413,041</td>
<td align="right">220,929,300</td>
<td align="right">-40.0%</td>
</tr>
<tr>
<td align="left">CALL_LEN</td>
<td align="right">504,670,034</td>
<td align="right">306,006,422</td>
<td align="right">-39.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">2,202,216,475</td>
<td align="right">1,349,908,177</td>
<td align="right">-38.7%</td>
</tr>
<tr>
<td align="left">TO_BOOL_ALWAYS_TRUE</td>
<td align="right">296,002,438</td>
<td align="right">182,114,147</td>
<td align="right">-38.5%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">246,038,802</td>
<td align="right">151,478,693</td>
<td align="right">-38.4%</td>
</tr>
<tr>
<td align="left">MAKE_FUNCTION</td>
<td align="right">159,041,332</td>
<td align="right">98,416,992</td>
<td align="right">-38.1%</td>
</tr>
<tr>
<td align="left">CALL_INTRINSIC_1</td>
<td align="right">252,098,840</td>
<td align="right">156,148,461</td>
<td align="right">-38.1%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">1,189,776,300</td>
<td align="right">741,616,221</td>
<td align="right">-37.7%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TUPLE</td>
<td align="right">507,133,133</td>
<td align="right">316,161,348</td>
<td align="right">-37.7%</td>
</tr>
<tr>
<td align="left">PUSH_NULL</td>
<td align="right">1,958,757,469</td>
<td align="right">1,227,185,740</td>
<td align="right">-37.3%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">1,016,025,868</td>
<td align="right">640,154,687</td>
<td align="right">-37.0%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">593,349,893</td>
<td align="right">374,361,696</td>
<td align="right">-36.9%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">397,132,737</td>
<td align="right">253,217,694</td>
<td align="right">-36.2%</td>
</tr>
<tr>
<td align="left">SET_FUNCTION_ATTRIBUTE</td>
<td align="right">131,923,863</td>
<td align="right">84,891,037</td>
<td align="right">-35.7%</td>
</tr>
<tr>
<td align="left">BINARY_SLICE</td>
<td align="right">347,987,132</td>
<td align="right">227,394,836</td>
<td align="right">-34.7%</td>
</tr>
<tr>
<td align="left">MAP_ADD</td>
<td align="right">60,510,860</td>
<td align="right">39,903,091</td>
<td align="right">-34.1%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">4,341,218,535</td>
<td align="right">2,873,436,060</td>
<td align="right">-33.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">6,288,282,734</td>
<td align="right">4,202,915,774</td>
<td align="right">-33.2%</td>
</tr>
<tr>
<td align="left">TO_BOOL_LIST</td>
<td align="right">181,388,407</td>
<td align="right">121,341,142</td>
<td align="right">-33.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_NO_DICT</td>
<td align="right">99,872,579</td>
<td align="right">67,106,635</td>
<td align="right">-32.8%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_DICT</td>
<td align="right">838,302,373</td>
<td align="right">569,954,716</td>
<td align="right">-32.0%</td>
</tr>
<tr>
<td align="left">JUMP_FORWARD</td>
<td align="right">655,522,211</td>
<td align="right">448,624,489</td>
<td align="right">-31.6%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">2,457,290,821</td>
<td align="right">1,729,457,968</td>
<td align="right">-29.6%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_LAZY_DICT</td>
<td align="right">356,130,810</td>
<td align="right">253,946,615</td>
<td align="right">-28.7%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_FLOAT</td>
<td align="right">251,124,746</td>
<td align="right">181,055,257</td>
<td align="right">-27.9%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">905,301,092</td>
<td align="right">658,890,322</td>
<td align="right">-27.2%</td>
</tr>
<tr>
<td align="left">CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">269,740,725</td>
<td align="right">196,519,073</td>
<td align="right">-27.1%</td>
</tr>
<tr>
<td align="left">CALL_ISINSTANCE</td>
<td align="right">1,161,830,688</td>
<td align="right">850,300,392</td>
<td align="right">-26.8%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_CLASS</td>
<td align="right">221,308,914</td>
<td align="right">162,744,394</td>
<td align="right">-26.5%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_UNICODE</td>
<td align="right">99,387,935</td>
<td align="right">74,034,968</td>
<td align="right">-25.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_PROPERTY</td>
<td align="right">86,987,967</td>
<td align="right">64,908,918</td>
<td align="right">-25.4%</td>
</tr>
<tr>
<td align="left">TO_BOOL_STR</td>
<td align="right">105,374,052</td>
<td align="right">80,634,026</td>
<td align="right">-23.5%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">4,656,969,832</td>
<td align="right">3,582,704,269</td>
<td align="right">-23.1%</td>
</tr>
<tr>
<td align="left">TO_BOOL_NONE</td>
<td align="right">643,027,657</td>
<td align="right">502,407,669</td>
<td align="right">-21.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_WITH_HINT</td>
<td align="right">476,933,251</td>
<td align="right">375,389,855</td>
<td align="right">-21.3%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NONE</td>
<td align="right">499,692,384</td>
<td align="right">401,922,187</td>
<td align="right">-19.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_AND_CLEAR</td>
<td align="right">86,253,288</td>
<td align="right">70,087,398</td>
<td align="right">-18.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_MODULE</td>
<td align="right">661,166,094</td>
<td align="right">540,994,252</td>
<td align="right">-18.2%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST_WITH_KEYWORDS</td>
<td align="right">131,796,159</td>
<td align="right">109,860,064</td>
<td align="right">-16.6%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">8,242,916,204</td>
<td align="right">6,913,530,807</td>
<td align="right">-16.1%</td>
</tr>
<tr>
<td align="left">STORE_GLOBAL</td>
<td align="right">8,205,260</td>
<td align="right">6,944,700</td>
<td align="right">-15.4%</td>
</tr>
<tr>
<td align="left">UNARY_NEGATIVE</td>
<td align="right">171,058,013</td>
<td align="right">146,012,123</td>
<td align="right">-14.6%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">4,229,895,465</td>
<td align="right">3,647,663,968</td>
<td align="right">-13.8%</td>
</tr>
<tr>
<td align="left">COPY_FREE_VARS</td>
<td align="right">371,243,436</td>
<td align="right">320,835,170</td>
<td align="right">-13.6%</td>
</tr>
<tr>
<td align="left">DICT_MERGE</td>
<td align="right">54,726,550</td>
<td align="right">47,572,476</td>
<td align="right">-13.1%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NOT_NONE</td>
<td align="right">768,661,654</td>
<td align="right">670,534,281</td>
<td align="right">-12.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_CLASS</td>
<td align="right">184,616,870</td>
<td align="right">161,061,243</td>
<td align="right">-12.8%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">1,292,051,571</td>
<td align="right">1,133,258,020</td>
<td align="right">-12.3%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">4,798,486,453</td>
<td align="right">4,290,430,176</td>
<td align="right">-10.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_CHECK</td>
<td align="right">12,067,680</td>
<td align="right">10,979,505</td>
<td align="right">-9.0%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_SLOT</td>
<td align="right">1,623,674,124</td>
<td align="right">1,497,241,138</td>
<td align="right">-7.8%</td>
</tr>
<tr>
<td align="left">BUILD_MAP</td>
<td align="right">143,317,082</td>
<td align="right">133,196,162</td>
<td align="right">-7.1%</td>
</tr>
<tr>
<td align="left">INTERPRETER_EXIT</td>
<td align="right">2,165,651,884</td>
<td align="right">2,310,255,204</td>
<td align="right">6.7%</td>
</tr>
<tr>
<td align="left">BUILD_CONST_KEY_MAP</td>
<td align="right">13,544,436</td>
<td align="right">12,713,377</td>
<td align="right">-6.1%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_O</td>
<td align="right">420,324,314</td>
<td align="right">396,031,613</td>
<td align="right">-5.8%</td>
</tr>
<tr>
<td align="left">MAKE_CELL</td>
<td align="right">110,355,085</td>
<td align="right">104,798,557</td>
<td align="right">-5.0%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_WITH_HINT</td>
<td align="right">67,299,770</td>
<td align="right">64,723,853</td>
<td align="right">-3.8%</td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">77,785,753</td>
<td align="right">75,207,326</td>
<td align="right">-3.3%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">2,121,352,076</td>
<td align="right">2,052,944,515</td>
<td align="right">-3.2%</td>
</tr>
<tr>
<td align="left">STORE_DEREF</td>
<td align="right">98,172,024</td>
<td align="right">95,259,718</td>
<td align="right">-3.0%</td>
</tr>
<tr>
<td align="left">BEFORE_WITH</td>
<td align="right">10,114,208</td>
<td align="right">9,817,203</td>
<td align="right">-2.9%</td>
</tr>
<tr>
<td align="left">DICT_UPDATE</td>
<td align="right">70,941</td>
<td align="right">72,898</td>
<td align="right">2.8%</td>
</tr>
<tr>
<td align="left">CALL_TUPLE_1</td>
<td align="right">28,824,447</td>
<td align="right">28,218,494</td>
<td align="right">-2.1%</td>
</tr>
<tr>
<td align="left">INSTRUMENTED_FOR_ITER</td>
<td align="right">3,208</td>
<td align="right">3,168</td>
<td align="right">-1.2%</td>
</tr>
<tr>
<td align="left">FORMAT_SIMPLE</td>
<td align="right">150,307,450</td>
<td align="right">148,457,316</td>
<td align="right">-1.2%</td>
</tr>
<tr>
<td align="left">BUILD_STRING</td>
<td align="right">76,313,426</td>
<td align="right">75,497,554</td>
<td align="right">-1.1%</td>
</tr>
<tr>
<td align="left">CALL_PY_WITH_DEFAULTS</td>
<td align="right">221,085,475</td>
<td align="right">219,008,850</td>
<td align="right">-0.9%</td>
</tr>
<tr>
<td align="left">CONVERT_VALUE</td>
<td align="right">139,688,804</td>
<td align="right">138,448,696</td>
<td align="right">-0.9%</td>
</tr>
<tr>
<td align="left">DELETE_SUBSCR</td>
<td align="right">177,912,901</td>
<td align="right">176,484,944</td>
<td align="right">-0.8%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR_METHOD</td>
<td align="right">126,940,527</td>
<td align="right">126,070,035</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">INSTRUMENTED_JUMP_BACKWARD</td>
<td align="right">6,248</td>
<td align="right">6,208</td>
<td align="right">-0.6%</td>
</tr>
<tr>
<td align="left">DELETE_FAST</td>
<td align="right">2,214,836</td>
<td align="right">2,227,654</td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">INSTRUMENTED_POP_JUMP_IF_TRUE</td>
<td align="right">8,728</td>
<td align="right">8,688</td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR_ATTR</td>
<td align="right">7,751,926</td>
<td align="right">7,717,092</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">FOR_ITER_GEN</td>
<td align="right">236,409,368</td>
<td align="right">235,406,031</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">GET_YIELD_FROM_ITER</td>
<td align="right">47,508,635</td>
<td align="right">47,328,707</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">1,191,078,547</td>
<td align="right">1,186,810,858</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">CALL_LIST_APPEND</td>
<td align="right">349,282,964</td>
<td align="right">348,043,791</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">EXIT_INIT_CHECK</td>
<td align="right">94,927,574</td>
<td align="right">94,700,604</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">CALL_ALLOC_AND_ENTER_INIT</td>
<td align="right">97,216,216</td>
<td align="right">96,988,666</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">WITH_EXCEPT_START</td>
<td align="right">233,480</td>
<td align="right">233,162</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">CALL_KW</td>
<td align="right">275,151,435</td>
<td align="right">274,796,744</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">DELETE_ATTR</td>
<td align="right">6,692,913</td>
<td align="right">6,688,266</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">CHECK_EXC_MATCH</td>
<td align="right">24,459,430</td>
<td align="right">24,451,227</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">PUSH_EXC_INFO</td>
<td align="right">24,971,012</td>
<td align="right">24,962,707</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">POP_EXCEPT</td>
<td align="right">24,970,863</td>
<td align="right">24,962,560</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">YIELD_VALUE</td>
<td align="right">1,405,840,292</td>
<td align="right">1,405,377,935</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">IMPORT_NAME</td>
<td align="right">12,435,901</td>
<td align="right">12,432,629</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">IMPORT_FROM</td>
<td align="right">13,103,677</td>
<td align="right">13,100,266</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">RERAISE</td>
<td align="right">3,848,278</td>
<td align="right">3,847,301</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR</td>
<td align="right">23,562</td>
<td align="right">23,566</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BUILD_SET</td>
<td align="right">2,329,841</td>
<td align="right">2,329,594</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">UNPACK_EX</td>
<td align="right">1,129,926</td>
<td align="right">1,129,822</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">CALL_FUNCTION_EX</td>
<td align="right">202,194,719</td>
<td align="right">202,177,632</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">GET_AWAITABLE</td>
<td align="right">229,779,192</td>
<td align="right">229,792,959</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">END_SEND</td>
<td align="right">402,607,247</td>
<td align="right">402,621,014</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">SEND</td>
<td align="right">173,832,869</td>
<td align="right">173,838,729</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">SEND_GEN</td>
<td align="right">787,088,975</td>
<td align="right">787,112,290</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">RAISE_VARARGS</td>
<td align="right">6,185,049</td>
<td align="right">6,185,149</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">RETURN_GENERATOR</td>
<td align="right">505,539,309</td>
<td align="right">505,545,497</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">20,772,434</td>
<td align="right">20,772,582</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">END_FOR</td>
<td align="right">82,846,452</td>
<td align="right">82,846,083</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD_NO_INTERRUPT</td>
<td align="right">556,667,170</td>
<td align="right">556,667,316</td>
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
<td align="left">LOAD_NAME</td>
<td align="right">14,145,667</td>
<td align="right">14,145,667</td>
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
<td align="left">RESUME</td>
<td align="right">345,223</td>
<td align="right">345,223</td>
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
<td align="left">ENTER_EXECUTOR</td>
<td align="right"></td>
<td align="right">2,757,266,355</td>
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
<td align="right">6,943,708,281</td>
<td align="right">82.7%</td>
<td align="right">1,666,878,513</td>
<td align="right">72.3%</td>
<td align="right">-76.0%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">1,445,186,716</td>
<td align="right">17.2%</td>
<td align="right">637,752,172</td>
<td align="right">27.7%</td>
<td align="right">-55.9%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">50,411,792</td>
<td align="right">0.6%</td>
<td align="right">30,888,227</td>
<td align="right">1.3%</td>
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
<td align="right">1,004,425</td>
<td align="right">36.7%</td>
<td align="right">636,053</td>
<td align="right">33.9%</td>
<td align="right">-36.7%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">1,729,245</td>
<td align="right">63.3%</td>
<td align="right">1,239,618</td>
<td align="right">66.1%</td>
<td align="right">-28.3%</td>
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
<td align="right">29,563</td>
<td align="right">1.7%</td>
<td align="right">5,829</td>
<td align="right">0.5%</td>
<td align="right">-80.3%</td>
</tr>
<tr>
<td align="left">rshift</td>
<td align="right">37,328</td>
<td align="right">2.2%</td>
<td align="right">9,995</td>
<td align="right">0.8%</td>
<td align="right">-73.2%</td>
</tr>
<tr>
<td align="left">true divide float</td>
<td align="right">18,163</td>
<td align="right">1.1%</td>
<td align="right">5,765</td>
<td align="right">0.5%</td>
<td align="right">-68.3%</td>
</tr>
<tr>
<td align="left">xor</td>
<td align="right">29,503</td>
<td align="right">1.7%</td>
<td align="right">9,865</td>
<td align="right">0.8%</td>
<td align="right">-66.6%</td>
</tr>
<tr>
<td align="left">add different types</td>
<td align="right">217,973</td>
<td align="right">12.6%</td>
<td align="right">78,773</td>
<td align="right">6.4%</td>
<td align="right">-63.9%</td>
</tr>
<tr>
<td align="left">multiply different types</td>
<td align="right">252,333</td>
<td align="right">14.6%</td>
<td align="right">92,376</td>
<td align="right">7.5%</td>
<td align="right">-63.4%</td>
</tr>
<tr>
<td align="left">power</td>
<td align="right">13,741</td>
<td align="right">0.8%</td>
<td align="right">5,755</td>
<td align="right">0.5%</td>
<td align="right">-58.1%</td>
</tr>
<tr>
<td align="left">true divide different types</td>
<td align="right">31,463</td>
<td align="right">1.8%</td>
<td align="right">13,425</td>
<td align="right">1.1%</td>
<td align="right">-57.3%</td>
</tr>
<tr>
<td align="left">and int</td>
<td align="right">75,574</td>
<td align="right">4.4%</td>
<td align="right">40,838</td>
<td align="right">3.3%</td>
<td align="right">-46.0%</td>
</tr>
<tr>
<td align="left">floor divide</td>
<td align="right">53,492</td>
<td align="right">3.1%</td>
<td align="right">33,520</td>
<td align="right">2.7%</td>
<td align="right">-37.3%</td>
</tr>
<tr>
<td align="left">subtract other</td>
<td align="right">16,234</td>
<td align="right">0.9%</td>
<td align="right">12,554</td>
<td align="right">1.0%</td>
<td align="right">-22.7%</td>
</tr>
<tr>
<td align="left">remainder</td>
<td align="right">68,971</td>
<td align="right">4.0%</td>
<td align="right">54,093</td>
<td align="right">4.4%</td>
<td align="right">-21.6%</td>
</tr>
<tr>
<td align="left">add other</td>
<td align="right">74,403</td>
<td align="right">4.3%</td>
<td align="right">64,809</td>
<td align="right">5.2%</td>
<td align="right">-12.9%</td>
</tr>
<tr>
<td align="left">or</td>
<td align="right">20,016</td>
<td align="right">1.2%</td>
<td align="right">17,451</td>
<td align="right">1.4%</td>
<td align="right">-12.8%</td>
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
<td align="right">778,830</td>
<td align="right">45.0%</td>
<td align="right">783,280</td>
<td align="right">63.2%</td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">and other</td>
<td align="right">2,019</td>
<td align="right">0.1%</td>
<td align="right">2,011</td>
<td align="right">0.2%</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">and different types</td>
<td align="right">619</td>
<td align="right">0.0%</td>
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
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">1,534,932,125</td>
<td align="right">25.0%</td>
<td align="right">423,171,083</td>
<td align="right">19.3%</td>
<td align="right">-72.4%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">4,591,997,441</td>
<td align="right">74.9%</td>
<td align="right">1,768,004,864</td>
<td align="right">80.7%</td>
<td align="right">-61.5%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">5,120,175</td>
<td align="right">0.1%</td>
<td align="right">4,903,077</td>
<td align="right">0.2%</td>
<td align="right">-4.2%</td>
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
<td align="right">467,367</td>
<td align="right">69.4%</td>
<td align="right">185,016</td>
<td align="right">47.8%</td>
<td align="right">-60.4%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">206,016</td>
<td align="right">30.6%</td>
<td align="right">201,868</td>
<td align="right">52.2%</td>
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
<td align="right">0.7%</td>
<td align="right">-96.1%</td>
</tr>
<tr>
<td align="left">array int</td>
<td align="right">157,600</td>
<td align="right">33.7%</td>
<td align="right">16,820</td>
<td align="right">9.1%</td>
<td align="right">-89.3%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">126,056</td>
<td align="right">27.0%</td>
<td align="right">57,097</td>
<td align="right">30.9%</td>
<td align="right">-54.7%</td>
</tr>
<tr>
<td align="left">buffer int</td>
<td align="right">49,203</td>
<td align="right">10.5%</td>
<td align="right">22,681</td>
<td align="right">12.3%</td>
<td align="right">-53.9%</td>
</tr>
<tr>
<td align="left">out of range</td>
<td align="right">88,589</td>
<td align="right">19.0%</td>
<td align="right">76,537</td>
<td align="right">41.4%</td>
<td align="right">-13.6%</td>
</tr>
<tr>
<td align="left">buffer slice</td>
<td align="right">980</td>
<td align="right">0.2%</td>
<td align="right">900</td>
<td align="right">0.5%</td>
<td align="right">-8.2%</td>
</tr>
<tr>
<td align="left">tuple slice</td>
<td align="right">183</td>
<td align="right">0.0%</td>
<td align="right">185</td>
<td align="right">0.1%</td>
<td align="right">1.1%</td>
</tr>
<tr>
<td align="left">code complex parameters</td>
<td align="right">5,036</td>
<td align="right">1.1%</td>
<td align="right">5,036</td>
<td align="right">2.7%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">sequence int</td>
<td align="right">4,300</td>
<td align="right">0.9%</td>
<td align="right">4,300</td>
<td align="right">2.3%</td>
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
<td align="right">12,198,376,666</td>
<td align="right">89.3%</td>
<td align="right">7,706,066,655</td>
<td align="right">84.2%</td>
<td align="right">-36.8%</td>
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
<td align="right">265,188,634</td>
<td align="right">1.9%</td>
<td align="right">254,501,006</td>
<td align="right">2.8%</td>
<td align="right">-4.0%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">1,449,679,256</td>
<td align="right">10.6%</td>
<td align="right">1,434,927,639</td>
<td align="right">15.7%</td>
<td align="right">-1.0%</td>
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
<td align="right">5,633,148</td>
<td align="right">85.5%</td>
<td align="right">5,431,714</td>
<td align="right">85.1%</td>
<td align="right">-3.6%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">954,777</td>
<td align="right">14.5%</td>
<td align="right">952,511</td>
<td align="right">14.9%</td>
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
<td align="left">operator wrapper</td>
<td align="right">10,182</td>
<td align="right">1.1%</td>
<td align="right">10,072</td>
<td align="right">1.1%</td>
<td align="right">-1.1%</td>
</tr>
<tr>
<td align="left">method wrapper</td>
<td align="right">8,263</td>
<td align="right">0.9%</td>
<td align="right">8,178</td>
<td align="right">0.9%</td>
<td align="right">-1.0%</td>
</tr>
<tr>
<td align="left">class mutable</td>
<td align="right">25,279</td>
<td align="right">2.6%</td>
<td align="right">25,079</td>
<td align="right">2.6%</td>
<td align="right">-0.8%</td>
</tr>
<tr>
<td align="left">cfunc noargs</td>
<td align="right">70,290</td>
<td align="right">7.4%</td>
<td align="right">69,924</td>
<td align="right">7.3%</td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">cfunc varargs keywords</td>
<td align="right">32,273</td>
<td align="right">3.4%</td>
<td align="right">32,113</td>
<td align="right">3.4%</td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">cfunc varargs</td>
<td align="right">14,251</td>
<td align="right">1.5%</td>
<td align="right">14,187</td>
<td align="right">1.5%</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">bound method</td>
<td align="right">12,068</td>
<td align="right">1.3%</td>
<td align="right">12,016</td>
<td align="right">1.3%</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">code complex parameters</td>
<td align="right">185,213</td>
<td align="right">19.4%</td>
<td align="right">184,556</td>
<td align="right">19.4%</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">wrong number arguments</td>
<td align="right">13,773</td>
<td align="right">1.4%</td>
<td align="right">13,733</td>
<td align="right">1.4%</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">meth descr varargs keywords</td>
<td align="right">20,857</td>
<td align="right">2.2%</td>
<td align="right">20,801</td>
<td align="right">2.2%</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">67,619</td>
<td align="right">7.1%</td>
<td align="right">67,487</td>
<td align="right">7.1%</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">meth descr method fastcall keywords</td>
<td align="right">207,336</td>
<td align="right">21.7%</td>
<td align="right">207,102</td>
<td align="right">21.7%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">class no vectorcall</td>
<td align="right">78,663</td>
<td align="right">8.2%</td>
<td align="right">78,588</td>
<td align="right">8.3%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">metaclass</td>
<td align="right">42,986</td>
<td align="right">4.5%</td>
<td align="right">42,961</td>
<td align="right">4.5%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">meth descr varargs</td>
<td align="right">16,496</td>
<td align="right">1.7%</td>
<td align="right">16,493</td>
<td align="right">1.7%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">init not inline values</td>
<td align="right">105,604</td>
<td align="right">11.1%</td>
<td align="right">105,597</td>
<td align="right">11.1%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">init not python</td>
<td align="right">16,426</td>
<td align="right">1.7%</td>
<td align="right">16,426</td>
<td align="right">1.7%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">cmethod</td>
<td align="right">14,100</td>
<td align="right">1.5%</td>
<td align="right">14,100</td>
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
<td align="right">4,582,811,893</td>
<td align="right">94.9%</td>
<td align="right">1,725,515,731</td>
<td align="right">91.8%</td>
<td align="right">-62.3%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">247,598,798</td>
<td align="right">5.1%</td>
<td align="right">153,018,858</td>
<td align="right">8.1%</td>
<td align="right">-38.2%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">1,936,714</td>
<td align="right">0.0%</td>
<td align="right">1,888,431</td>
<td align="right">0.1%</td>
<td align="right">-2.5%</td>
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
<td align="right">262,082</td>
<td align="right">69.6%</td>
<td align="right">234,570</td>
<td align="right">67.4%</td>
<td align="right">-10.5%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">114,636</td>
<td align="right">30.4%</td>
<td align="right">113,696</td>
<td align="right">32.6%</td>
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
<td align="left">set</td>
<td align="right">10,363</td>
<td align="right">4.0%</td>
<td align="right">2,343</td>
<td align="right">1.0%</td>
<td align="right">-77.4%</td>
</tr>
<tr>
<td align="left">bool</td>
<td align="right">5,862</td>
<td align="right">2.2%</td>
<td align="right">3,811</td>
<td align="right">1.6%</td>
<td align="right">-35.0%</td>
</tr>
<tr>
<td align="left">float long</td>
<td align="right">21,129</td>
<td align="right">8.1%</td>
<td align="right">16,423</td>
<td align="right">7.0%</td>
<td align="right">-22.3%</td>
</tr>
<tr>
<td align="left">bytes</td>
<td align="right">4,860</td>
<td align="right">1.9%</td>
<td align="right">4,120</td>
<td align="right">1.8%</td>
<td align="right">-15.2%</td>
</tr>
<tr>
<td align="left">baseobject</td>
<td align="right">39,404</td>
<td align="right">15.0%</td>
<td align="right">33,714</td>
<td align="right">14.4%</td>
<td align="right">-14.4%</td>
</tr>
<tr>
<td align="left">different types</td>
<td align="right">59,528</td>
<td align="right">22.7%</td>
<td align="right">55,121</td>
<td align="right">23.5%</td>
<td align="right">-7.4%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">25,233</td>
<td align="right">9.6%</td>
<td align="right">24,207</td>
<td align="right">10.3%</td>
<td align="right">-4.1%</td>
</tr>
<tr>
<td align="left">long float</td>
<td align="right">1,580</td>
<td align="right">0.6%</td>
<td align="right">1,526</td>
<td align="right">0.7%</td>
<td align="right">-3.4%</td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">4,374</td>
<td align="right">1.7%</td>
<td align="right">4,234</td>
<td align="right">1.8%</td>
<td align="right">-3.2%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">15,072</td>
<td align="right">5.8%</td>
<td align="right">14,614</td>
<td align="right">6.2%</td>
<td align="right">-3.0%</td>
</tr>
<tr>
<td align="left">string</td>
<td align="right">11,120</td>
<td align="right">4.2%</td>
<td align="right">11,080</td>
<td align="right">4.7%</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">big int</td>
<td align="right">63,557</td>
<td align="right">24.3%</td>
<td align="right">63,377</td>
<td align="right">27.0%</td>
<td align="right">-0.3%</td>
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
<td align="right">2,480,699,403</td>
<td align="right">91.6%</td>
<td align="right">637,413,438</td>
<td align="right">84.3%</td>
<td align="right">-74.3%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">226,512,926</td>
<td align="right">8.4%</td>
<td align="right">118,116,442</td>
<td align="right">15.6%</td>
<td align="right">-47.9%</td>
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
<td align="right">162,832</td>
<td align="right">70.7%</td>
<td align="right">132,687</td>
<td align="right">66.3%</td>
<td align="right">-18.5%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">67,509</td>
<td align="right">29.3%</td>
<td align="right">67,506</td>
<td align="right">33.7%</td>
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
<td align="right">33,251</td>
<td align="right">20.4%</td>
<td align="right">19,661</td>
<td align="right">14.8%</td>
<td align="right">-40.9%</td>
</tr>
<tr>
<td align="left">str</td>
<td align="right">46,753</td>
<td align="right">28.7%</td>
<td align="right">37,064</td>
<td align="right">27.9%</td>
<td align="right">-20.7%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">33,467</td>
<td align="right">20.6%</td>
<td align="right">28,788</td>
<td align="right">21.7%</td>
<td align="right">-14.0%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">49,361</td>
<td align="right">30.3%</td>
<td align="right">47,174</td>
<td align="right">35.6%</td>
<td align="right">-4.4%</td>
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
<td align="right">713,371,848</td>
<td align="right">17.3%</td>
<td align="right">228,167,768</td>
<td align="right">15.8%</td>
<td align="right">-68.0%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">3,401,741,408</td>
<td align="right">82.6%</td>
<td align="right">1,214,934,713</td>
<td align="right">84.1%</td>
<td align="right">-64.3%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">175,800,480</td>
<td align="right">4.3%</td>
<td align="right">101,830,320</td>
<td align="right">7.0%</td>
<td align="right">-42.1%</td>
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
<td align="right">362,164</td>
<td align="right">9.7%</td>
<td align="right">188,476</td>
<td align="right">8.7%</td>
<td align="right">-48.0%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">3,383,021</td>
<td align="right">90.3%</td>
<td align="right">1,987,332</td>
<td align="right">91.3%</td>
<td align="right">-41.3%</td>
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
<td align="right">2,280</td>
<td align="right">0.6%</td>
<td align="right">740</td>
<td align="right">0.4%</td>
<td align="right">-67.5%</td>
</tr>
<tr>
<td align="left">seq iter</td>
<td align="right">30,660</td>
<td align="right">8.5%</td>
<td align="right">10,300</td>
<td align="right">5.5%</td>
<td align="right">-66.4%</td>
</tr>
<tr>
<td align="left">enumerate</td>
<td align="right">52,074</td>
<td align="right">14.4%</td>
<td align="right">20,047</td>
<td align="right">10.6%</td>
<td align="right">-61.5%</td>
</tr>
<tr>
<td align="left">ascii string</td>
<td align="right">5,960</td>
<td align="right">1.6%</td>
<td align="right">2,700</td>
<td align="right">1.4%</td>
<td align="right">-54.7%</td>
</tr>
<tr>
<td align="left">dict values</td>
<td align="right">14,770</td>
<td align="right">4.1%</td>
<td align="right">7,070</td>
<td align="right">3.8%</td>
<td align="right">-52.1%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">29,259</td>
<td align="right">8.1%</td>
<td align="right">14,699</td>
<td align="right">7.8%</td>
<td align="right">-49.8%</td>
</tr>
<tr>
<td align="left">dict items</td>
<td align="right">120,869</td>
<td align="right">33.4%</td>
<td align="right">61,497</td>
<td align="right">32.6%</td>
<td align="right">-49.1%</td>
</tr>
<tr>
<td align="left">callable</td>
<td align="right">522</td>
<td align="right">0.1%</td>
<td align="right">282</td>
<td align="right">0.1%</td>
<td align="right">-46.0%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">45,545</td>
<td align="right">12.6%</td>
<td align="right">26,017</td>
<td align="right">13.8%</td>
<td align="right">-42.9%</td>
</tr>
<tr>
<td align="left">zip</td>
<td align="right">21,604</td>
<td align="right">6.0%</td>
<td align="right">14,352</td>
<td align="right">7.6%</td>
<td align="right">-33.6%</td>
</tr>
<tr>
<td align="left">itertools</td>
<td align="right">10,808</td>
<td align="right">3.0%</td>
<td align="right">7,451</td>
<td align="right">4.0%</td>
<td align="right">-31.1%</td>
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
<td align="right">7,885</td>
<td align="right">4.2%</td>
<td align="right">-22.2%</td>
</tr>
<tr>
<td align="left">dict keys</td>
<td align="right">16,781</td>
<td align="right">4.6%</td>
<td align="right">14,756</td>
<td align="right">7.8%</td>
<td align="right">-12.1%</td>
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
<td align="right">1,025,787,509</td>
<td align="right">5.9%</td>
<td align="right">575,772,824</td>
<td align="right">5.0%</td>
<td align="right">-43.9%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">2,500,931,351</td>
<td align="right">14.3%</td>
<td align="right">1,418,703,644</td>
<td align="right">12.4%</td>
<td align="right">-43.3%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">14,914,074,080</td>
<td align="right">85.5%</td>
<td align="right">10,021,638,638</td>
<td align="right">87.5%</td>
<td align="right">-32.8%</td>
</tr>
<tr>
<td align="left">
deopt
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">685,352</td>
<td align="right">0.0%</td>
<td align="right">686,043</td>
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
<td align="right">20,237,859</td>
<td align="right">88.9%</td>
<td align="right">11,747,568</td>
<td align="right">87.3%</td>
<td align="right">-42.0%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">2,526,733</td>
<td align="right">11.1%</td>
<td align="right">1,710,092</td>
<td align="right">12.7%</td>
<td align="right">-32.3%</td>
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
<td align="right">957,853</td>
<td align="right">37.9%</td>
<td align="right">300,747</td>
<td align="right">17.6%</td>
<td align="right">-68.6%</td>
</tr>
<tr>
<td align="left">metaclass attribute</td>
<td align="right">280,485</td>
<td align="right">11.1%</td>
<td align="right">195,038</td>
<td align="right">11.4%</td>
<td align="right">-30.5%</td>
</tr>
<tr>
<td align="left">method</td>
<td align="right">171,027</td>
<td align="right">6.8%</td>
<td align="right">120,224</td>
<td align="right">7.0%</td>
<td align="right">-29.7%</td>
</tr>
<tr>
<td align="left">class method obj</td>
<td align="right">28,443</td>
<td align="right">1.1%</td>
<td align="right">25,773</td>
<td align="right">1.5%</td>
<td align="right">-9.4%</td>
</tr>
<tr>
<td align="left">overridden</td>
<td align="right">21,112</td>
<td align="right">0.8%</td>
<td align="right">19,286</td>
<td align="right">1.1%</td>
<td align="right">-8.6%</td>
</tr>
<tr>
<td align="left">shadowed</td>
<td align="right">150,350</td>
<td align="right">6.0%</td>
<td align="right">140,600</td>
<td align="right">8.2%</td>
<td align="right">-6.5%</td>
</tr>
<tr>
<td align="left">mutable class</td>
<td align="right">82,911</td>
<td align="right">3.3%</td>
<td align="right">78,081</td>
<td align="right">4.6%</td>
<td align="right">-5.8%</td>
</tr>
<tr>
<td align="left">non overriding descriptor</td>
<td align="right">14,092</td>
<td align="right">0.6%</td>
<td align="right">13,582</td>
<td align="right">0.8%</td>
<td align="right">-3.6%</td>
</tr>
<tr>
<td align="left">builtin class method</td>
<td align="right">3,937</td>
<td align="right">0.2%</td>
<td align="right">3,818</td>
<td align="right">0.2%</td>
<td align="right">-3.0%</td>
</tr>
<tr>
<td align="left">non string or split</td>
<td align="right">22,733</td>
<td align="right">0.9%</td>
<td align="right">22,088</td>
<td align="right">1.3%</td>
<td align="right">-2.8%</td>
</tr>
<tr>
<td align="left">non object slot</td>
<td align="right">3,600</td>
<td align="right">0.1%</td>
<td align="right">3,500</td>
<td align="right">0.2%</td>
<td align="right">-2.8%</td>
</tr>
<tr>
<td align="left">class attr descriptor</td>
<td align="right">30,840</td>
<td align="right">1.2%</td>
<td align="right">30,100</td>
<td align="right">1.8%</td>
<td align="right">-2.4%</td>
</tr>
<tr>
<td align="left">out of versions</td>
<td align="right">2,358</td>
<td align="right">0.1%</td>
<td align="right">2,331</td>
<td align="right">0.1%</td>
<td align="right">-1.1%</td>
</tr>
<tr>
<td align="left">not in keys</td>
<td align="right">16,740</td>
<td align="right">0.7%</td>
<td align="right">16,560</td>
<td align="right">1.0%</td>
<td align="right">-1.1%</td>
</tr>
<tr>
<td align="left">module attr not found</td>
<td align="right">17,957</td>
<td align="right">0.7%</td>
<td align="right">17,842</td>
<td align="right">1.0%</td>
<td align="right">-0.6%</td>
</tr>
<tr>
<td align="left">class attr simple</td>
<td align="right">720,515</td>
<td align="right">28.5%</td>
<td align="right">718,742</td>
<td align="right">42.0%</td>
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
<td align="right">10,583,620,465</td>
<td align="right">99.8%</td>
<td align="right">6,615,872,922</td>
<td align="right">99.7%</td>
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
<td align="right">459,023</td>
<td align="right">0.0%</td>
<td align="right">453,718</td>
<td align="right">0.0%</td>
<td align="right">-1.2%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">20,563,425</td>
<td align="right">0.2%</td>
<td align="right">20,558,259</td>
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
<td align="right">668,032</td>
<td align="right">100.0%</td>
<td align="right">668,041</td>
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
<td align="right">134,692,453</td>
<td align="right">100.0%</td>
<td align="right">133,787,127</td>
<td align="right">100.0%</td>
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
<td align="right">11,845</td>
<td align="right">0.0%</td>
<td align="right">11,849</td>
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
<td align="right">173,794,911</td>
<td align="right">18.1%</td>
<td align="right">173,800,738</td>
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
<td align="right">787,058,075</td>
<td align="right">81.9%</td>
<td align="right">787,081,390</td>
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
<td align="right">61,709</td>
<td align="right">89.6%</td>
<td align="right">61,745</td>
<td align="right">89.6%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">7,149</td>
<td align="right">10.4%</td>
<td align="right">7,146</td>
<td align="right">10.4%</td>
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
<td align="right">16,089</td>
<td align="right">26.1%</td>
<td align="right">16,125</td>
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
<td align="right">219,981,204</td>
<td align="right">7.2%</td>
<td align="right">165,631,531</td>
<td align="right">6.0%</td>
<td align="right">-24.7%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">293,318,117</td>
<td align="right">9.6%</td>
<td align="right">237,417,637</td>
<td align="right">8.6%</td>
<td align="right">-19.1%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">2,763,044,261</td>
<td align="right">90.3%</td>
<td align="right">2,529,591,480</td>
<td align="right">91.3%</td>
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
<td align="right">4,299,562</td>
<td align="right">96.6%</td>
<td align="right">3,274,057</td>
<td align="right">95.7%</td>
<td align="right">-23.9%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">149,278</td>
<td align="right">3.4%</td>
<td align="right">147,163</td>
<td align="right">4.3%</td>
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
<td align="left">property</td>
<td align="right">5,720</td>
<td align="right">3.8%</td>
<td align="right">5,180</td>
<td align="right">3.5%</td>
<td align="right">-9.4%</td>
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
<td align="left">out of versions</td>
<td align="right">614</td>
<td align="right">0.4%</td>
<td align="right">594</td>
<td align="right">0.4%</td>
<td align="right">-3.3%</td>
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
<td align="right">49,639</td>
<td align="right">33.7%</td>
<td align="right">-0.8%</td>
</tr>
<tr>
<td align="left">no dict</td>
<td align="right">5,200</td>
<td align="right">3.5%</td>
<td align="right">5,160</td>
<td align="right">3.5%</td>
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
<td align="left">not managed dict</td>
<td align="right">28,508</td>
<td align="right">19.1%</td>
<td align="right">28,512</td>
<td align="right">19.4%</td>
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
<td align="left">method</td>
<td align="right">1,580</td>
<td align="right">1.1%</td>
<td align="right">1,580</td>
<td align="right">1.1%</td>
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
<td align="right">886,279,571</td>
<td align="right">66.2%</td>
<td align="right">261,131,441</td>
<td align="right">66.0%</td>
<td align="right">-70.5%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">451,670,879</td>
<td align="right">33.8%</td>
<td align="right">134,319,385</td>
<td align="right">34.0%</td>
<td align="right">-70.3%</td>
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
<td align="right">164,226</td>
<td align="right">89.8%</td>
<td align="right">83,999</td>
<td align="right">81.8%</td>
<td align="right">-48.9%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">18,705</td>
<td align="right">10.2%</td>
<td align="right">18,708</td>
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
<td align="right">66,240</td>
<td align="right">40.3%</td>
<td align="right">7,320</td>
<td align="right">8.7%</td>
<td align="right">-88.9%</td>
</tr>
<tr>
<td align="left">bytearray int</td>
<td align="right">9,720</td>
<td align="right">5.9%</td>
<td align="right">1,400</td>
<td align="right">1.7%</td>
<td align="right">-85.6%</td>
</tr>
<tr>
<td align="left">out of range</td>
<td align="right">3,828</td>
<td align="right">2.3%</td>
<td align="right">2,108</td>
<td align="right">2.5%</td>
<td align="right">-44.9%</td>
</tr>
<tr>
<td align="left">dict subclass no override</td>
<td align="right">36,664</td>
<td align="right">22.3%</td>
<td align="right">28,293</td>
<td align="right">33.7%</td>
<td align="right">-22.8%</td>
</tr>
<tr>
<td align="left">py simple</td>
<td align="right">45,694</td>
<td align="right">27.8%</td>
<td align="right">42,818</td>
<td align="right">51.0%</td>
<td align="right">-6.3%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">2,080</td>
<td align="right">1.3%</td>
<td align="right">2,060</td>
<td align="right">2.5%</td>
<td align="right">-1.0%</td>
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
<td align="right">6,310,808,242</td>
<td align="right">92.1%</td>
<td align="right">3,743,464,095</td>
<td align="right">91.3%</td>
<td align="right">-40.7%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">539,587,228</td>
<td align="right">7.9%</td>
<td align="right">354,156,234</td>
<td align="right">8.6%</td>
<td align="right">-34.4%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">146,209,617</td>
<td align="right">2.1%</td>
<td align="right">103,818,415</td>
<td align="right">2.5%</td>
<td align="right">-29.0%</td>
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
<td align="right">3,042,907</td>
<td align="right">81.0%</td>
<td align="right">2,243,195</td>
<td align="right">77.9%</td>
<td align="right">-26.3%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">712,219</td>
<td align="right">19.0%</td>
<td align="right">636,680</td>
<td align="right">22.1%</td>
<td align="right">-10.6%</td>
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
<td align="right">18,701</td>
<td align="right">2.9%</td>
<td align="right">-43.6%</td>
</tr>
<tr>
<td align="left">dict</td>
<td align="right">40,852</td>
<td align="right">5.7%</td>
<td align="right">33,971</td>
<td align="right">5.3%</td>
<td align="right">-16.8%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">114,343</td>
<td align="right">16.1%</td>
<td align="right">95,436</td>
<td align="right">15.0%</td>
<td align="right">-16.5%</td>
</tr>
<tr>
<td align="left">number</td>
<td align="right">182,158</td>
<td align="right">25.6%</td>
<td align="right">152,374</td>
<td align="right">23.9%</td>
<td align="right">-16.4%</td>
</tr>
<tr>
<td align="left">sequence</td>
<td align="right">20,200</td>
<td align="right">2.8%</td>
<td align="right">17,976</td>
<td align="right">2.8%</td>
<td align="right">-11.0%</td>
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
<td align="left">mapping</td>
<td align="right">100,391</td>
<td align="right">14.1%</td>
<td align="right">99,303</td>
<td align="right">15.6%</td>
<td align="right">-1.1%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">41,019</td>
<td align="right">5.8%</td>
<td align="right">40,628</td>
<td align="right">6.4%</td>
<td align="right">-1.0%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">175,833</td>
<td align="right">24.7%</td>
<td align="right">174,311</td>
<td align="right">27.4%</td>
<td align="right">-0.9%</td>
</tr>
<tr>
<td align="left">bytearray</td>
<td align="right">1,244</td>
<td align="right">0.2%</td>
<td align="right">1,240</td>
<td align="right">0.2%</td>
<td align="right">-0.3%</td>
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
<td align="right">2,056,330</td>
<td align="right">0.1%</td>
<td align="right">500,262</td>
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
<td align="right">1,562,096,838</td>
<td align="right">99.9%</td>
<td align="right">673,191,922</td>
<td align="right">99.9%</td>
<td align="right">-56.9%</td>
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
<td align="right">3,160</td>
<td align="right">0.0%</td>
<td align="right">-25.5%</td>
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
<td align="right">4,404</td>
<td align="right">9.9%</td>
<td align="right">3,574</td>
<td align="right">8.2%</td>
<td align="right">-18.8%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">39,881</td>
<td align="right">90.1%</td>
<td align="right">39,865</td>
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
<td align="right">3,263</td>
<td align="right">74.1%</td>
<td align="right">2,513</td>
<td align="right">70.3%</td>
<td align="right">-23.0%</td>
</tr>
<tr>
<td align="left">iterator</td>
<td align="right">761</td>
<td align="right">17.3%</td>
<td align="right">681</td>
<td align="right">19.1%</td>
<td align="right">-10.5%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">380</td>
<td align="right">8.6%</td>
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
<td align="right">24,440,787,321</td>
<td align="right">10.6%</td>
<td align="right">12,201,497,024</td>
<td align="right">9.3%</td>
<td align="right">-50.1%</td>
</tr>
<tr>
<td align="left">
Basic
<details>
<summary>ⓘ</summary>

Instructions that are not and cannot be specialized, e.g. `LOAD_FAST`.
</details>
</td>
<td align="right">124,428,102,997</td>
<td align="right">53.8%</td>
<td align="right">71,408,143,149</td>
<td align="right">54.4%</td>
<td align="right">-42.6%</td>
</tr>
<tr>
<td align="left">
Specialized hits
<details>
<summary>ⓘ</summary>

Specialized instructions, e.g. `LOAD_ATTR_MODULE` that complete.
</details>
</td>
<td align="right">80,347,154,877</td>
<td align="right">34.8%</td>
<td align="right">46,342,993,831</td>
<td align="right">35.3%</td>
<td align="right">-42.3%</td>
</tr>
<tr>
<td align="left">
Specialized misses
<details>
<summary>ⓘ</summary>

Specialized instructions, e.g. `LOAD_ATTR_MODULE` that deopt.
</details>
</td>
<td align="right">1,893,668,171</td>
<td align="right">0.8%</td>
<td align="right">1,242,456,780</td>
<td align="right">0.9%</td>
<td align="right">-34.4%</td>
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
<td align="right">1,534,932,125</td>
<td align="right">16.0%</td>
<td align="right">423,171,083</td>
<td align="right">7.9%</td>
<td align="right">-72.4%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR</td>
<td align="right">451,670,879</td>
<td align="right">4.7%</td>
<td align="right">134,319,385</td>
<td align="right">2.5%</td>
<td align="right">-70.3%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">713,371,848</td>
<td align="right">7.4%</td>
<td align="right">228,167,768</td>
<td align="right">4.3%</td>
<td align="right">-68.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">1,445,186,716</td>
<td align="right">15.1%</td>
<td align="right">637,752,172</td>
<td align="right">12.0%</td>
<td align="right">-55.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">2,500,931,351</td>
<td align="right">26.1%</td>
<td align="right">1,418,703,644</td>
<td align="right">26.6%</td>
<td align="right">-43.3%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">247,598,798</td>
<td align="right">2.6%</td>
<td align="right">153,018,858</td>
<td align="right">2.9%</td>
<td align="right">-38.2%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">539,587,228</td>
<td align="right">5.6%</td>
<td align="right">354,156,234</td>
<td align="right">6.6%</td>
<td align="right">-34.4%</td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">293,318,117</td>
<td align="right">3.1%</td>
<td align="right">237,417,637</td>
<td align="right">4.5%</td>
<td align="right">-19.1%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">1,449,679,256</td>
<td align="right">15.1%</td>
<td align="right">1,434,927,639</td>
<td align="right">26.9%</td>
<td align="right">-1.0%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">226,512,926</td>
<td align="right">2.4%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">SEND</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">173,800,738</td>
<td align="right">3.3%</td>
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
<td align="right">373,185,842</td>
<td align="right">19.7%</td>
<td align="right">164,451,805</td>
<td align="right">13.2%</td>
<td align="right">-55.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">380,279,573</td>
<td align="right">20.1%</td>
<td align="right">180,881,674</td>
<td align="right">14.6%</td>
<td align="right">-52.4%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">87,940,416</td>
<td align="right">4.6%</td>
<td align="right">50,861,482</td>
<td align="right">4.1%</td>
<td align="right">-42.2%</td>
</tr>
<tr>
<td align="left">FOR_ITER_TUPLE</td>
<td align="right">87,558,884</td>
<td align="right">4.6%</td>
<td align="right">50,726,878</td>
<td align="right">4.1%</td>
<td align="right">-42.1%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">121,052,788</td>
<td align="right">6.4%</td>
<td align="right">70,579,417</td>
<td align="right">5.7%</td>
<td align="right">-41.7%</td>
</tr>
<tr>
<td align="left">TO_BOOL_NONE</td>
<td align="right">68,526,462</td>
<td align="right">3.6%</td>
<td align="right">47,963,955</td>
<td align="right">3.9%</td>
<td align="right">-30.0%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">137,034,838</td>
<td align="right">7.2%</td>
<td align="right">129,645,497</td>
<td align="right">10.4%</td>
<td align="right">-5.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">115,532,910</td>
<td align="right">6.1%</td>
<td align="right">109,403,543</td>
<td align="right">8.8%</td>
<td align="right">-5.3%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_SLOT</td>
<td align="right">98,869,581</td>
<td align="right">5.2%</td>
<td align="right">94,999,311</td>
<td align="right">7.6%</td>
<td align="right">-3.9%</td>
</tr>
<tr>
<td align="left">TO_BOOL_ALWAYS_TRUE</td>
<td align="right">68,817,072</td>
<td align="right">3.6%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">59,618,556</td>
<td align="right">4.8%</td>
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
<td align="left">Calls via PyEval_EvalFrame (slot)</td>
<td align="right">343,022,077</td>
<td align="right">3.9%</td>
<td align="right">475,777,910</td>
<td align="right">5.4%</td>
<td align="right">38.7%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (function vectorcall)</td>
<td align="right">1,297,000,935</td>
<td align="right">14.8%</td>
<td align="right">1,441,100,195</td>
<td align="right">16.4%</td>
<td align="right">11.1%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (vector)</td>
<td align="right">1,302,330,105</td>
<td align="right">14.8%</td>
<td align="right">1,446,429,365</td>
<td align="right">16.5%</td>
<td align="right">11.1%</td>
</tr>
<tr>
<td align="left">Calls to PyEval_EvalDefault</td>
<td align="right">2,169,293,815</td>
<td align="right">24.7%</td>
<td align="right">2,313,921,846</td>
<td align="right">26.4%</td>
<td align="right">6.7%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (total)</td>
<td align="right">2,169,293,815</td>
<td align="right">24.7%</td>
<td align="right">2,313,921,846</td>
<td align="right">26.4%</td>
<td align="right">6.7%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (api)</td>
<td align="right">242,845,874</td>
<td align="right">2.8%</td>
<td align="right">255,687,440</td>
<td align="right">2.9%</td>
<td align="right">5.3%</td>
</tr>
<tr>
<td align="left">Calls to Python functions inlined</td>
<td align="right">6,618,752,044</td>
<td align="right">75.3%</td>
<td align="right">6,451,105,424</td>
<td align="right">73.6%</td>
<td align="right">-2.5%</td>
</tr>
<tr>
<td align="left">Frames pushed</td>
<td align="right">6,992,755,551</td>
<td align="right">79.6%</td>
<td align="right">6,969,959,266</td>
<td align="right">79.5%</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (function ex)</td>
<td align="right">38,315,743</td>
<td align="right">0.4%</td>
<td align="right">38,357,360</td>
<td align="right">0.4%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (generator)</td>
<td align="right">866,963,710</td>
<td align="right">9.9%</td>
<td align="right">867,492,481</td>
<td align="right">9.9%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (method)</td>
<td align="right">213,093,461</td>
<td align="right">2.4%</td>
<td align="right">213,134,834</td>
<td align="right">2.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Frame objects created</td>
<td align="right">88,437,238</td>
<td align="right">1.0%</td>
<td align="right">88,442,403</td>
<td align="right">1.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (legacy)</td>
<td align="right">5,298,544</td>
<td align="right">0.1%</td>
<td align="right">5,298,544</td>
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
<td align="right">15,004,732</td>
<td align="right"></td>
<td align="right">15,755,115</td>
<td align="right"></td>
<td align="right">5.0%</td>
</tr>
<tr>
<td align="left">Interpreter increfs</td>
<td align="right">89,217,491,888</td>
<td align="right">77.0%</td>
<td align="right">93,543,114,800</td>
<td align="right">77.6%</td>
<td align="right">4.8%</td>
</tr>
<tr>
<td align="left">Interpreter decrefs</td>
<td align="right">103,650,586,723</td>
<td align="right">77.7%</td>
<td align="right">108,185,670,199</td>
<td align="right">78.4%</td>
<td align="right">4.4%</td>
</tr>
<tr>
<td align="left">Method cache dunder hits</td>
<td align="right">3,426,986,387</td>
<td align="right"></td>
<td align="right">3,554,769,689</td>
<td align="right"></td>
<td align="right">3.7%</td>
</tr>
<tr>
<td align="left">Method cache misses</td>
<td align="right">81,544,552</td>
<td align="right"></td>
<td align="right">79,842,995</td>
<td align="right"></td>
<td align="right">-2.1%</td>
</tr>
<tr>
<td align="left">Increfs</td>
<td align="right">26,674,904,479</td>
<td align="right">23.0%</td>
<td align="right">26,986,225,560</td>
<td align="right">22.4%</td>
<td align="right">1.2%</td>
</tr>
<tr>
<td align="left">Method cache collisions</td>
<td align="right">88,794,330</td>
<td align="right"></td>
<td align="right">87,843,461</td>
<td align="right"></td>
<td align="right">-1.1%</td>
</tr>
<tr>
<td align="left">Inline values</td>
<td align="right">182,873,415</td>
<td align="right"></td>
<td align="right">182,183,374</td>
<td align="right"></td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">Decrefs</td>
<td align="right">29,761,520,222</td>
<td align="right">22.3%</td>
<td align="right">29,861,830,949</td>
<td align="right">21.6%</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">Allocations over 4 kbytes</td>
<td align="right">21,168,149</td>
<td align="right">0.1%</td>
<td align="right">21,097,850</td>
<td align="right">0.1%</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">Method cache hits</td>
<td align="right">3,119,052,144</td>
<td align="right"></td>
<td align="right">3,128,564,803</td>
<td align="right"></td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">Allocations from freelist</td>
<td align="right">6,819,489,018</td>
<td align="right">36.7%</td>
<td align="right">6,833,826,883</td>
<td align="right">36.8%</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">Frees to freelist</td>
<td align="right">6,821,491,193</td>
<td align="right"></td>
<td align="right">6,835,803,100</td>
<td align="right"></td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">Frees</td>
<td align="right">12,113,401,403</td>
<td align="right"></td>
<td align="right">12,092,582,539</td>
<td align="right"></td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">Allocations to 512 bytes</td>
<td align="right">11,654,988,225</td>
<td align="right">62.7%</td>
<td align="right">11,634,983,380</td>
<td align="right">62.6%</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">Allocations</td>
<td align="right">11,781,020,021</td>
<td align="right">63.3%</td>
<td align="right">11,760,849,533</td>
<td align="right">63.2%</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">Allocations to 4 kbytes</td>
<td align="right">104,863,647</td>
<td align="right">0.6%</td>
<td align="right">104,768,303</td>
<td align="right">0.6%</td>
<td align="right">-0.1%</td>
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
<td align="right">116,159,172</td>
<td align="right">17,122,673,331</td>
<td align="right">0</td>
<td align="right">115,787,623</td>
<td align="right">17,058,381,675</td>
</tr>
<tr>
<td align="right">2</td>
<td align="right">0</td>
<td align="right">10,754,820</td>
<td align="right">6,955,936,900</td>
<td align="right">0</td>
<td align="right">10,755,840</td>
<td align="right">6,965,888,990</td>
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
<td align="right">663,813</td>
<td align="right"></td>
<td align="right">663,813 / 0 !!</td>
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
<td align="right">108,509</td>
<td align="right">16.3%</td>
<td align="right">108,509 / 0 !!</td>
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
<td align="right">612</td>
<td align="right">0.1%</td>
<td align="right">612 / 0 !!</td>
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
<td align="right">133,815</td>
<td align="right">20.2%</td>
<td align="right">133,815 / 0 !!</td>
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
<td align="right">555,304</td>
<td align="right">83.7%</td>
<td align="right">555,304 / 0 !!</td>
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
<td align="right">16,452</td>
<td align="right">2.5%</td>
<td align="right">16,452 / 0 !!</td>
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
<td align="right">1,491</td>
<td align="right">0.2%</td>
<td align="right">1,491 / 0 !!</td>
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
<td align="right">6,758</td>
<td align="right">1.0%</td>
<td align="right">6,758 / 0 !!</td>
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
<td align="right">5,460</td>
<td align="right">5.0%</td>
<td align="right">5,460 / 0 !!</td>
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
<td align="right">6,398,488,373</td>
<td align="right"></td>
<td align="right">6,398,488,373 / 0 !!</td>
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
<td align="right">175,694,798,639</td>
<td align="right">2,745.9%</td>
<td align="right">175,694,798,639 / 0 !!</td>
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
<td align="right">108,509</td>
<td align="right"></td>
<td align="right">108,509 / 0 !!</td>
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
<td align="right">106,349</td>
<td align="right">98.0%</td>
<td align="right">106,349 / 0 !!</td>
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
<td align="right">2.0%</td>
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
<td align="right">2,801</td>
<td align="right">2.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 16</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">16,954</td>
<td align="right">15.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 32</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">41,748</td>
<td align="right">38.5%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 64</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">26,817</td>
<td align="right">24.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 128</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">14,849</td>
<td align="right">13.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 256</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">4,475</td>
<td align="right">4.1%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 512</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">865</td>
<td align="right">0.8%</td>
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
<td align="right">618</td>
<td align="right">0.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 8</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">8,971</td>
<td align="right">8.3%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 16</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">34,225</td>
<td align="right">31.5%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 32</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">35,243</td>
<td align="right">32.5%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 64</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">17,961</td>
<td align="right">16.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 128</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">7,287</td>
<td align="right">6.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 256</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">1,824</td>
<td align="right">1.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 512</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">220</td>
<td align="right">0.2%</td>
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
<td align="right">25,552,980</td>
<td align="right">0.4%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 4</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">561,110,979</td>
<td align="right">8.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 8</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">805,939,216</td>
<td align="right">12.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 16</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">1,161,656,418</td>
<td align="right">18.2%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 32</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">1,127,948,387</td>
<td align="right">17.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 64</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">592,103,741</td>
<td align="right">9.3%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 128</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">280,198,095</td>
<td align="right">4.4%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 256</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">145,371,069</td>
<td align="right">2.3%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 512</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">15,954,863</td>
<td align="right">0.2%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 1,024</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">6,387,281</td>
<td align="right">0.1%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 2,048</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">18,353,633</td>
<td align="right">0.3%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 4,096</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">644,601</td>
<td align="right">0.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 8,192</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">744,934</td>
<td align="right">0.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 16,384</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">245,681</td>
<td align="right">0.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 32,768</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">42,640</td>
<td align="right">0.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 65,536</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">13,568</td>
<td align="right">0.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 131,072</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">672</td>
<td align="right">0.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 262,144</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">2,081</td>
<td align="right">0.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 524,288</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">474</td>
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
<td align="right">234</td>
<td align="right">0.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 4,194,304</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">246</td>
<td align="right">0.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 8,388,608</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">160</td>
<td align="right">0.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 16,777,216</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">80</td>
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
<td align="right">16,395,815,807</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_VALIDITY</td>
<td align="right"></td>
<td align="right">9,857,138,637</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_CONST_INLINE_BORROW</td>
<td align="right"></td>
<td align="right">8,896,231,711</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_FAST_1</td>
<td align="right"></td>
<td align="right">6,199,616,141</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_FAST</td>
<td align="right"></td>
<td align="right">5,486,967,108</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_TYPE_VERSION</td>
<td align="right"></td>
<td align="right">5,361,888,680</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_FAST_0</td>
<td align="right"></td>
<td align="right">5,319,979,979</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_IS_FALSE_POP</td>
<td align="right"></td>
<td align="right">5,310,075,365</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_START_EXECUTOR</td>
<td align="right"></td>
<td align="right">4,742,272,433</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_SIDE_EXIT</td>
<td align="right"></td>
<td align="right">3,641,096,155</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_FAST_7</td>
<td align="right"></td>
<td align="right">3,378,579,827</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_BOTH_INT</td>
<td align="right"></td>
<td align="right">3,165,592,898</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_FAST_3</td>
<td align="right"></td>
<td align="right">3,097,293,914</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_FAST</td>
<td align="right"></td>
<td align="right">2,973,055,080</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_EXIT_TRACE</td>
<td align="right"></td>
<td align="right">2,752,204,939</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_FAST_2</td>
<td align="right"></td>
<td align="right">2,703,142,499</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_IS_TRUE_POP</td>
<td align="right"></td>
<td align="right">2,575,400,329</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_OP_ADD_INT</td>
<td align="right"></td>
<td align="right">2,490,192,300</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_PERIODIC</td>
<td align="right"></td>
<td align="right">2,129,140,057</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_JUMP_TO_TOP</td>
<td align="right"></td>
<td align="right">2,101,526,446</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_FAST_5</td>
<td align="right"></td>
<td align="right">2,051,600,218</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_FAST_4</td>
<td align="right"></td>
<td align="right">1,969,111,419</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_TO_BOOL_BOOL</td>
<td align="right"></td>
<td align="right">1,936,392,361</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_MANAGED_OBJECT_HAS_VALUES</td>
<td align="right"></td>
<td align="right">1,885,633,703</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_INSTANCE_VALUE_0</td>
<td align="right"></td>
<td align="right">1,881,858,947</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_FAST_1</td>
<td align="right"></td>
<td align="right">1,849,831,425</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_COMPARE_OP_STR</td>
<td align="right"></td>
<td align="right">1,825,052,815</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_COLD_EXIT</td>
<td align="right"></td>
<td align="right">1,656,215,940</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_CONST_INLINE_WITH_NULL</td>
<td align="right"></td>
<td align="right">1,654,300,545</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION_EXACT_ARGS</td>
<td align="right"></td>
<td align="right">1,585,551,279</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_BOTH_FLOAT</td>
<td align="right"></td>
<td align="right">1,554,390,278</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_PUSH_FRAME</td>
<td align="right"></td>
<td align="right">1,525,825,195</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_SAVE_RETURN_OFFSET</td>
<td align="right"></td>
<td align="right">1,525,825,195</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_ITER_CHECK_LIST</td>
<td align="right"></td>
<td align="right">1,509,526,289</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_NOT_EXHAUSTED_LIST</td>
<td align="right"></td>
<td align="right">1,493,607,802</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CONTAINS_OP_SET</td>
<td align="right"></td>
<td align="right">1,478,322,166</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_RESUME_CHECK</td>
<td align="right"></td>
<td align="right">1,306,359,543</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION</td>
<td align="right"></td>
<td align="right">1,277,451,072</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_COPY</td>
<td align="right"></td>
<td align="right">1,252,536,430</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_FAST_6</td>
<td align="right"></td>
<td align="right">1,243,716,445</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_SUBSCR</td>
<td align="right"></td>
<td align="right">1,241,271,137</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_CONST_INLINE</td>
<td align="right"></td>
<td align="right">1,239,365,772</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_SUBSCR_STR_INT</td>
<td align="right"></td>
<td align="right">1,215,773,758</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_ITER_NEXT_LIST</td>
<td align="right"></td>
<td align="right">1,207,594,907</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_FAST_7</td>
<td align="right"></td>
<td align="right">1,202,531,758</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_SWAP</td>
<td align="right"></td>
<td align="right">1,130,160,267</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_OP_MULTIPLY_FLOAT</td>
<td align="right"></td>
<td align="right">1,124,307,820</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR</td>
<td align="right"></td>
<td align="right">1,104,628,178</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_DEOPT</td>
<td align="right"></td>
<td align="right">1,100,689,846</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_SUBSCR_LIST_INT</td>
<td align="right"></td>
<td align="right">1,055,865,195</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_DORV_VALUES_INST_ATTR_FROM_DICT</td>
<td align="right"></td>
<td align="right">1,045,617,864</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_VALIDITY_AND_SET_IP</td>
<td align="right"></td>
<td align="right">1,039,733,647</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_KEYS_VERSION</td>
<td align="right"></td>
<td align="right">1,002,494,249</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_BOTH_UNICODE</td>
<td align="right"></td>
<td align="right">965,839,714</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_COMPARE_OP_INT</td>
<td align="right"></td>
<td align="right">944,333,414</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right"></td>
<td align="right">909,559,282</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_STACK_SPACE_OPERAND</td>
<td align="right"></td>
<td align="right">866,248,380</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_OP</td>
<td align="right"></td>
<td align="right">855,000,595</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right"></td>
<td align="right">829,731,230</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_FAST</td>
<td align="right"></td>
<td align="right">790,018,684</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_ITER_CHECK_RANGE</td>
<td align="right"></td>
<td align="right">783,652,135</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_NOT_EXHAUSTED_RANGE</td>
<td align="right"></td>
<td align="right">782,294,375</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_ITER_NEXT_RANGE</td>
<td align="right"></td>
<td align="right">734,197,878</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_PUSH_NULL</td>
<td align="right"></td>
<td align="right">730,163,584</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_FAST_2</td>
<td align="right"></td>
<td align="right">704,090,642</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_SLOT_0</td>
<td align="right"></td>
<td align="right">702,944,195</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_POP_TOP</td>
<td align="right"></td>
<td align="right">699,581,177</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_FAST_4</td>
<td align="right"></td>
<td align="right">656,316,537</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_FAST_5</td>
<td align="right"></td>
<td align="right">647,095,599</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_FAST_3</td>
<td align="right"></td>
<td align="right">624,535,281</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right"></td>
<td align="right">619,963,813</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_O</td>
<td align="right"></td>
<td align="right">615,543,479</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_OP_ADD_FLOAT</td>
<td align="right"></td>
<td align="right">571,783,760</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_POP_FRAME</td>
<td align="right"></td>
<td align="right">553,674,063</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_ITER_CHECK_TUPLE</td>
<td align="right"></td>
<td align="right">543,250,670</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_1</td>
<td align="right"></td>
<td align="right">524,773,442</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_SUBSCR_LIST_INT</td>
<td align="right"></td>
<td align="right">478,857,462</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_NOT_EXHAUSTED_TUPLE</td>
<td align="right"></td>
<td align="right">466,003,489</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_4</td>
<td align="right"></td>
<td align="right">448,283,625</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_DEREF</td>
<td align="right"></td>
<td align="right">447,877,918</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBTRACT_INT</td>
<td align="right"></td>
<td align="right">442,127,818</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_FAST_6</td>
<td align="right"></td>
<td align="right">417,435,709</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_FOR_ITER_TIER_TWO</td>
<td align="right"></td>
<td align="right">413,877,706</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBTRACT_FLOAT</td>
<td align="right"></td>
<td align="right">382,602,700</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_0</td>
<td align="right"></td>
<td align="right">381,712,504</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BUILD_TUPLE</td>
<td align="right"></td>
<td align="right">374,072,388</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_CONST_INLINE_BORROW_WITH_NULL</td>
<td align="right"></td>
<td align="right">364,261,433</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CONTAINS_OP_DICT</td>
<td align="right"></td>
<td align="right">360,165,932</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_IS_OP</td>
<td align="right"></td>
<td align="right">337,692,252</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_SUBSCR</td>
<td align="right"></td>
<td align="right">317,348,382</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_ITER_NEXT_TUPLE</td>
<td align="right"></td>
<td align="right">311,466,834</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_ISINSTANCE</td>
<td align="right"></td>
<td align="right">310,064,721</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_SUBSCR_DICT</td>
<td align="right"></td>
<td align="right">258,326,950</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BUILD_LIST</td>
<td align="right"></td>
<td align="right">245,568,525</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GET_ITER</td>
<td align="right"></td>
<td align="right">244,470,651</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_TO_BOOL</td>
<td align="right"></td>
<td align="right">241,392,670</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_TYPE_1</td>
<td align="right"></td>
<td align="right">237,456,933</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right"></td>
<td align="right">226,470,861</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_FAST_0</td>
<td align="right"></td>
<td align="right">204,628,371</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_LEN</td>
<td align="right"></td>
<td align="right">196,658,155</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_TO_BOOL_INT</td>
<td align="right"></td>
<td align="right">196,532,514</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_UNPACK_SEQUENCE_TUPLE</td>
<td align="right"></td>
<td align="right">190,910,408</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_GLOBAL</td>
<td align="right"></td>
<td align="right">188,820,357</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_OP_MULTIPLY_INT</td>
<td align="right"></td>
<td align="right">184,971,238</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right"></td>
<td align="right">184,242,890</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LIST_APPEND</td>
<td align="right"></td>
<td align="right">182,468,107</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_TO_BOOL_NONE</td>
<td align="right"></td>
<td align="right">173,061,678</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_STACK_SPACE</td>
<td align="right"></td>
<td align="right">164,461,248</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_FAST_WITH_KEYWORDS</td>
<td align="right"></td>
<td align="right">153,743,229</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_SLICE</td>
<td align="right"></td>
<td align="right">149,868,340</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_IS_NOT_NONE_POP</td>
<td align="right"></td>
<td align="right">148,460,430</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_SUBSCR_TUPLE_INT</td>
<td align="right"></td>
<td align="right">147,485,716</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_SUBSCR_DICT</td>
<td align="right"></td>
<td align="right">143,857,037</td>
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
<td align="right">123,538,652</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_SLICE</td>
<td align="right"></td>
<td align="right">119,832,492</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CONTAINS_OP</td>
<td align="right"></td>
<td align="right">107,647,577</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_2</td>
<td align="right"></td>
<td align="right">104,915,272</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_DORV_NO_DICT</td>
<td align="right"></td>
<td align="right">104,007,661</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_ATTR_INSTANCE_VALUE</td>
<td align="right"></td>
<td align="right">102,699,901</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_ATTR_WITH_HINT</td>
<td align="right"></td>
<td align="right">98,013,239</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_WITH_HINT</td>
<td align="right"></td>
<td align="right">97,902,378</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_ATTR_METHOD_LAZY_DICT</td>
<td align="right"></td>
<td align="right">97,230,586</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_METHOD_LAZY_DICT</td>
<td align="right"></td>
<td align="right">97,230,586</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LIST_EXTEND</td>
<td align="right"></td>
<td align="right">96,944,162</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_INTRINSIC_1</td>
<td align="right"></td>
<td align="right">96,027,082</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_COMPARE_OP</td>
<td align="right"></td>
<td align="right">92,916,457</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right"></td>
<td align="right">88,764,007</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_UNPACK_SEQUENCE_LIST</td>
<td align="right"></td>
<td align="right">77,567,280</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right"></td>
<td align="right">73,648,495</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_INIT_CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right"></td>
<td align="right">73,595,055</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_COMPARE_OP_FLOAT</td>
<td align="right"></td>
<td align="right">70,082,878</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_STR_1</td>
<td align="right"></td>
<td align="right">66,199,794</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_UNARY_NOT</td>
<td align="right"></td>
<td align="right">62,209,868</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_MAKE_FUNCTION</td>
<td align="right"></td>
<td align="right">60,651,073</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_CLASS</td>
<td align="right"></td>
<td align="right">57,189,981</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_3</td>
<td align="right"></td>
<td align="right">56,632,278</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_TO_BOOL_LIST</td>
<td align="right"></td>
<td align="right">55,459,650</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_ATTR</td>
<td align="right"></td>
<td align="right">52,902,273</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_GLOBALS_VERSION</td>
<td align="right"></td>
<td align="right">50,855,144</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_COPY_FREE_VARS</td>
<td align="right"></td>
<td align="right">49,448,432</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_SET_FUNCTION_ATTRIBUTE</td>
<td align="right"></td>
<td align="right">47,068,689</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_GLOBAL_MODULE</td>
<td align="right"></td>
<td align="right">44,267,468</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_IS_NONE_POP</td>
<td align="right"></td>
<td align="right">42,593,727</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_REPLACE_WITH_TRUE</td>
<td align="right"></td>
<td align="right">32,161,270</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_UNARY_NEGATIVE</td>
<td align="right"></td>
<td align="right">25,045,762</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_ATTR_CLASS</td>
<td align="right"></td>
<td align="right">25,003,513</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_TO_BOOL_STR</td>
<td align="right"></td>
<td align="right">24,373,105</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_OP_ADD_UNICODE</td>
<td align="right"></td>
<td align="right">23,610,807</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_CLASS_0</td>
<td align="right"></td>
<td align="right">23,413,597</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_O</td>
<td align="right"></td>
<td align="right">22,209,021</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_FAST_WITH_KEYWORDS</td>
<td align="right"></td>
<td align="right">21,922,819</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_NONDESCRIPTOR_NO_DICT</td>
<td align="right"></td>
<td align="right">21,767,658</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_MAP_ADD</td>
<td align="right"></td>
<td align="right">20,604,765</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_FAST_AND_CLEAR</td>
<td align="right"></td>
<td align="right">15,829,714</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_UNARY_INVERT</td>
<td align="right"></td>
<td align="right">12,534,740</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BUILD_MAP</td>
<td align="right"></td>
<td align="right">9,870,324</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS</td>
<td align="right"></td>
<td align="right">9,508,074</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_DICT_MERGE</td>
<td align="right"></td>
<td align="right">7,203,142</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_GLOBAL_BUILTINS</td>
<td align="right"></td>
<td align="right">6,587,676</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_ATTR_MODULE</td>
<td align="right"></td>
<td align="right">6,483,293</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_MODULE</td>
<td align="right"></td>
<td align="right">6,479,853</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_MAKE_CELL</td>
<td align="right"></td>
<td align="right">5,622,925</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_INSTANCE_VALUE_1</td>
<td align="right"></td>
<td align="right">3,664,036</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_DEREF</td>
<td align="right"></td>
<td align="right">2,930,205</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_UNPACK_SEQUENCE</td>
<td align="right"></td>
<td align="right">1,554,903</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_SET_ADD</td>
<td align="right"></td>
<td align="right">1,449,186</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_DELETE_SUBSCR</td>
<td align="right"></td>
<td align="right">1,428,140</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_FORMAT_SIMPLE</td>
<td align="right"></td>
<td align="right">1,407,265</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_GLOBAL</td>
<td align="right"></td>
<td align="right">1,260,560</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_POP_TOP_LOAD_CONST_INLINE_BORROW</td>
<td align="right"></td>
<td align="right">1,239,857</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CONVERT_VALUE</td>
<td align="right"></td>
<td align="right">790,640</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BUILD_STRING</td>
<td align="right"></td>
<td align="right">595,780</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_TUPLE_1</td>
<td align="right"></td>
<td align="right">572,540</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_NAME</td>
<td align="right"></td>
<td align="right">545,860</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_ERROR_POP_N</td>
<td align="right"></td>
<td align="right">486,432</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_FAST_CHECK</td>
<td align="right"></td>
<td align="right">252,093</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GET_YIELD_FROM_ITER</td>
<td align="right"></td>
<td align="right">179,880</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_SUPER_ATTR_METHOD</td>
<td align="right"></td>
<td align="right">95,777</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BUILD_CONST_KEY_MAP</td>
<td align="right"></td>
<td align="right">79,650</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_BUILTINS_VERSION</td>
<td align="right"></td>
<td align="right">38,636</td>
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
<td align="right">127,132</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">YIELD_VALUE</td>
<td align="right"></td>
<td align="right">119,625</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">FOR_ITER_GEN</td>
<td align="right"></td>
<td align="right">56,423</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">RETURN_GENERATOR</td>
<td align="right"></td>
<td align="right">40,948</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right"></td>
<td align="right">34,709</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">SEND</td>
<td align="right"></td>
<td align="right">31,240</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_KW</td>
<td align="right"></td>
<td align="right">25,595</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_PY_WITH_DEFAULTS</td>
<td align="right"></td>
<td align="right">9,160</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_ATTR_PROPERTY</td>
<td align="right"></td>
<td align="right">6,927</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_LIST_APPEND</td>
<td align="right"></td>
<td align="right">5,990</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_FUNCTION_EX</td>
<td align="right"></td>
<td align="right">2,800</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_GETITEM</td>
<td align="right"></td>
<td align="right">2,520</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_ALLOC_AND_ENTER_INIT</td>
<td align="right"></td>
<td align="right">1,424</td>
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
<td align="right">583</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">IMPORT_NAME</td>
<td align="right"></td>
<td align="right">266</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BUILD_SET</td>
<td align="right"></td>
<td align="right">226</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BEFORE_WITH</td>
<td align="right"></td>
<td align="right">220</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">STORE_ATTR_WITH_HINT</td>
<td align="right"></td>
<td align="right">180</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">SEND_GEN</td>
<td align="right"></td>
<td align="right">60</td>
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
Stats gathered on: 2024-04-21
