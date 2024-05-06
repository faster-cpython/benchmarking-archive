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
<td align="left">CALL</td>
<td align="right">1,132,021,127</td>
<td align="right">126,860,638</td>
<td align="right">-88.8%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_LIST</td>
<td align="right">8,179,923</td>
<td align="right">987,229</td>
<td align="right">-87.9%</td>
</tr>
<tr>
<td align="left">DELETE_ATTR</td>
<td align="right">4,678,978</td>
<td align="right">670,888</td>
<td align="right">-85.7%</td>
</tr>
<tr>
<td align="left">BINARY_OP_INPLACE_ADD_UNICODE</td>
<td align="right">2,751,962</td>
<td align="right">484,780</td>
<td align="right">-82.4%</td>
</tr>
<tr>
<td align="left">FORMAT_WITH_SPEC</td>
<td align="right">1,760</td>
<td align="right">320</td>
<td align="right">-81.8%</td>
</tr>
<tr>
<td align="left">SET_ADD</td>
<td align="right">965,797</td>
<td align="right">238,480</td>
<td align="right">-75.3%</td>
</tr>
<tr>
<td align="left">UNARY_NOT</td>
<td align="right">25,398,543</td>
<td align="right">7,495,563</td>
<td align="right">-70.5%</td>
</tr>
<tr>
<td align="left">TO_BOOL_STR</td>
<td align="right">46,922,446</td>
<td align="right">15,789,608</td>
<td align="right">-66.3%</td>
</tr>
<tr>
<td align="left">MAP_ADD</td>
<td align="right">27,247,061</td>
<td align="right">11,637,534</td>
<td align="right">-57.3%</td>
</tr>
<tr>
<td align="left">CALL_TUPLE_1</td>
<td align="right">20,482,954</td>
<td align="right">9,856,383</td>
<td align="right">-51.9%</td>
</tr>
<tr>
<td align="left">STORE_GLOBAL</td>
<td align="right">6,944,168</td>
<td align="right">3,465,180</td>
<td align="right">-50.1%</td>
</tr>
<tr>
<td align="left">STORE_FAST_LOAD_FAST</td>
<td align="right">35,839,839</td>
<td align="right">19,444,317</td>
<td align="right">-45.7%</td>
</tr>
<tr>
<td align="left">BUILD_SET</td>
<td align="right">2,329,673</td>
<td align="right">1,332,836</td>
<td align="right">-42.8%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">335,850,460</td>
<td align="right">206,814,315</td>
<td align="right">-38.4%</td>
</tr>
<tr>
<td align="left">TO_BOOL_ALWAYS_TRUE</td>
<td align="right">172,239,844</td>
<td align="right">106,346,257</td>
<td align="right">-38.3%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">73,413,349</td>
<td align="right">45,599,631</td>
<td align="right">-37.9%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR_METHOD</td>
<td align="right">126,487,106</td>
<td align="right">82,003,615</td>
<td align="right">-35.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_NO_DICT</td>
<td align="right">62,522,878</td>
<td align="right">42,268,478</td>
<td align="right">-32.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">1,581,427,559</td>
<td align="right">1,096,792,826</td>
<td align="right">-30.6%</td>
</tr>
<tr>
<td align="left">BUILD_LIST</td>
<td align="right">165,460,303</td>
<td align="right">117,836,364</td>
<td align="right">-28.8%</td>
</tr>
<tr>
<td align="left">UNPACK_EX</td>
<td align="right">1,129,822</td>
<td align="right">807,420</td>
<td align="right">-28.5%</td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">47,056,735</td>
<td align="right">33,885,235</td>
<td align="right">-28.0%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_SLOT</td>
<td align="right">1,490,546,329</td>
<td align="right">1,075,666,512</td>
<td align="right">-27.8%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">58,731,501</td>
<td align="right">42,633,565</td>
<td align="right">-27.4%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_DICT</td>
<td align="right">390,878,742</td>
<td align="right">287,028,377</td>
<td align="right">-26.6%</td>
</tr>
<tr>
<td align="left">TO_BOOL_INT</td>
<td align="right">115,941,652</td>
<td align="right">85,186,746</td>
<td align="right">-26.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_AND_CLEAR</td>
<td align="right">75,393,415</td>
<td align="right">55,489,636</td>
<td align="right">-26.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">1,056,305,036</td>
<td align="right">783,633,121</td>
<td align="right">-25.8%</td>
</tr>
<tr>
<td align="left">TO_BOOL_LIST</td>
<td align="right">96,306,762</td>
<td align="right">71,778,639</td>
<td align="right">-25.5%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">409,412,408</td>
<td align="right">305,463,979</td>
<td align="right">-25.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_PROPERTY</td>
<td align="right">58,936,636</td>
<td align="right">45,227,883</td>
<td align="right">-23.3%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">135,645,058</td>
<td align="right">104,149,103</td>
<td align="right">-23.2%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NOT_NONE</td>
<td align="right">573,593,165</td>
<td align="right">448,037,038</td>
<td align="right">-21.9%</td>
</tr>
<tr>
<td align="left">IS_OP</td>
<td align="right">414,462,103</td>
<td align="right">324,953,284</td>
<td align="right">-21.6%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_LIST_INT</td>
<td align="right">99,797,992</td>
<td align="right">78,451,179</td>
<td align="right">-21.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right">56,169,306</td>
<td align="right">44,447,336</td>
<td align="right">-20.9%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR</td>
<td align="right">23,353</td>
<td align="right">18,486</td>
<td align="right">-20.8%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">1,139,735,807</td>
<td align="right">906,988,518</td>
<td align="right">-20.4%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_CLASS</td>
<td align="right">146,502,066</td>
<td align="right">116,771,467</td>
<td align="right">-20.3%</td>
</tr>
<tr>
<td align="left">CALL_TYPE_1</td>
<td align="right">192,659,258</td>
<td align="right">154,126,230</td>
<td align="right">-20.0%</td>
</tr>
<tr>
<td align="left">COPY_FREE_VARS</td>
<td align="right">286,512,235</td>
<td align="right">230,627,697</td>
<td align="right">-19.5%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">1,546,502</td>
<td align="right">1,842,284</td>
<td align="right">19.1%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NONE</td>
<td align="right">361,478,176</td>
<td align="right">293,644,805</td>
<td align="right">-18.8%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">422,465,737</td>
<td align="right">345,560,870</td>
<td align="right">-18.2%</td>
</tr>
<tr>
<td align="left">JUMP_FORWARD</td>
<td align="right">414,512,783</td>
<td align="right">342,033,152</td>
<td align="right">-17.5%</td>
</tr>
<tr>
<td align="left">CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">171,274,618</td>
<td align="right">141,357,750</td>
<td align="right">-17.5%</td>
</tr>
<tr>
<td align="left">BEFORE_WITH</td>
<td align="right">10,056,695</td>
<td align="right">8,334,519</td>
<td align="right">-17.1%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">2,375,110,327</td>
<td align="right">1,969,625,749</td>
<td align="right">-17.1%</td>
</tr>
<tr>
<td align="left">MAKE_CELL</td>
<td align="right">104,335,075</td>
<td align="right">86,568,804</td>
<td align="right">-17.0%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_DICT</td>
<td align="right">107,006,642</td>
<td align="right">88,835,628</td>
<td align="right">-17.0%</td>
</tr>
<tr>
<td align="left">UNARY_INVERT</td>
<td align="right">2,029,943</td>
<td align="right">1,688,278</td>
<td align="right">-16.8%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">97,722,571</td>
<td align="right">81,448,101</td>
<td align="right">-16.7%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">206,607,769</td>
<td align="right">172,304,201</td>
<td align="right">-16.6%</td>
</tr>
<tr>
<td align="left">CALL_ISINSTANCE</td>
<td align="right">711,569,989</td>
<td align="right">596,864,517</td>
<td align="right">-16.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">20,663,050,279</td>
<td align="right">17,408,291,944</td>
<td align="right">-15.8%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">469,501,067</td>
<td align="right">396,326,824</td>
<td align="right">-15.6%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">629,113,021</td>
<td align="right">531,909,575</td>
<td align="right">-15.5%</td>
</tr>
<tr>
<td align="left">LIST_APPEND</td>
<td align="right">99,250,825</td>
<td align="right">84,018,176</td>
<td align="right">-15.3%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE</td>
<td align="right">532,693</td>
<td align="right">452,262</td>
<td align="right">-15.1%</td>
</tr>
<tr>
<td align="left">NOP</td>
<td align="right">760,586,063</td>
<td align="right">646,235,311</td>
<td align="right">-15.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_CHECK</td>
<td align="right">10,796,301</td>
<td align="right">9,192,508</td>
<td align="right">-14.9%</td>
</tr>
<tr>
<td align="left">CALL_KW</td>
<td align="right">267,834,823</td>
<td align="right">228,424,982</td>
<td align="right">-14.7%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">997,258,337</td>
<td align="right">851,800,189</td>
<td align="right">-14.6%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_O</td>
<td align="right">523,084,618</td>
<td align="right">447,819,636</td>
<td align="right">-14.4%</td>
</tr>
<tr>
<td align="left">POP_EXCEPT</td>
<td align="right">16,927,662</td>
<td align="right">14,562,106</td>
<td align="right">-14.0%</td>
</tr>
<tr>
<td align="left">PUSH_EXC_INFO</td>
<td align="right">16,935,432</td>
<td align="right">14,569,875</td>
<td align="right">-14.0%</td>
</tr>
<tr>
<td align="left">CHECK_EXC_MATCH</td>
<td align="right">16,890,349</td>
<td align="right">14,533,504</td>
<td align="right">-14.0%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP_DICT</td>
<td align="right">131,387,820</td>
<td align="right">113,208,693</td>
<td align="right">-13.8%</td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">313,379</td>
<td align="right">270,579</td>
<td align="right">-13.7%</td>
</tr>
<tr>
<td align="left">FOR_ITER_TUPLE</td>
<td align="right">118,857,475</td>
<td align="right">102,772,944</td>
<td align="right">-13.5%</td>
</tr>
<tr>
<td align="left">TO_BOOL_NONE</td>
<td align="right">421,145,738</td>
<td align="right">364,247,303</td>
<td align="right">-13.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_LAZY_DICT</td>
<td align="right">252,037,778</td>
<td align="right">218,301,445</td>
<td align="right">-13.4%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">602,735,173</td>
<td align="right">523,710,774</td>
<td align="right">-13.1%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">454,303,373</td>
<td align="right">395,385,899</td>
<td align="right">-13.0%</td>
</tr>
<tr>
<td align="left">RERAISE</td>
<td align="right">2,392,216</td>
<td align="right">2,083,403</td>
<td align="right">-12.9%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">4,789,551,931</td>
<td align="right">4,175,590,867</td>
<td align="right">-12.8%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">3,223,834,685</td>
<td align="right">2,812,847,409</td>
<td align="right">-12.7%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">229,616,746</td>
<td align="right">200,352,127</td>
<td align="right">-12.7%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">2,657,818,745</td>
<td align="right">2,322,653,223</td>
<td align="right">-12.6%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">2,504,299,865</td>
<td align="right">2,189,460,075</td>
<td align="right">-12.6%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">1,849,244,675</td>
<td align="right">1,625,337,479</td>
<td align="right">-12.1%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">5,553,978,191</td>
<td align="right">4,896,669,796</td>
<td align="right">-11.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">4,442,105,486</td>
<td align="right">3,932,417,379</td>
<td align="right">-11.5%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST</td>
<td align="right">331,993,683</td>
<td align="right">294,190,535</td>
<td align="right">-11.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">1,413,162,716</td>
<td align="right">1,252,609,896</td>
<td align="right">-11.4%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_STR_INT</td>
<td align="right">368,326,352</td>
<td align="right">326,750,005</td>
<td align="right">-11.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_WITH_HINT</td>
<td align="right">304,037,023</td>
<td align="right">271,583,174</td>
<td align="right">-10.7%</td>
</tr>
<tr>
<td align="left">CALL_LEN</td>
<td align="right">251,492,358</td>
<td align="right">225,553,126</td>
<td align="right">-10.3%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_INT</td>
<td align="right">537,834,058</td>
<td align="right">482,423,784</td>
<td align="right">-10.3%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">222,365,133</td>
<td align="right">199,546,195</td>
<td align="right">-10.3%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">5,214,705,764</td>
<td align="right">4,687,772,249</td>
<td align="right">-10.1%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST_WITH_KEYWORDS</td>
<td align="right">31,246,133</td>
<td align="right">28,113,416</td>
<td align="right">-10.0%</td>
</tr>
<tr>
<td align="left">BUILD_MAP</td>
<td align="right">101,564,026</td>
<td align="right">91,498,940</td>
<td align="right">-9.9%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">6,106,116,910</td>
<td align="right">5,506,773,954</td>
<td align="right">-9.8%</td>
</tr>
<tr>
<td align="left">IMPORT_FROM</td>
<td align="right">13,090,748</td>
<td align="right">11,827,436</td>
<td align="right">-9.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">3,649,613,016</td>
<td align="right">3,322,141,413</td>
<td align="right">-9.0%</td>
</tr>
<tr>
<td align="left">FOR_ITER_RANGE</td>
<td align="right">52,310,870</td>
<td align="right">47,679,747</td>
<td align="right">-8.9%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_GETITEM</td>
<td align="right">54,066,091</td>
<td align="right">49,501,639</td>
<td align="right">-8.4%</td>
</tr>
<tr>
<td align="left">IMPORT_NAME</td>
<td align="right">12,410,755</td>
<td align="right">11,375,221</td>
<td align="right">-8.3%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_STR</td>
<td align="right">305,289,111</td>
<td align="right">279,899,519</td>
<td align="right">-8.3%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_LIST_INT</td>
<td align="right">386,626,543</td>
<td align="right">354,847,541</td>
<td align="right">-8.2%</td>
</tr>
<tr>
<td align="left">DICT_MERGE</td>
<td align="right">41,322,405</td>
<td align="right">38,019,604</td>
<td align="right">-8.0%</td>
</tr>
<tr>
<td align="left">UNARY_NEGATIVE</td>
<td align="right">145,761,000</td>
<td align="right">134,503,150</td>
<td align="right">-7.7%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">395,696,024</td>
<td align="right">365,514,212</td>
<td align="right">-7.6%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT</td>
<td align="right">1,163,155,371</td>
<td align="right">1,074,489,343</td>
<td align="right">-7.6%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">3,903,448,178</td>
<td align="right">3,610,669,063</td>
<td align="right">-7.5%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR_ATTR</td>
<td align="right">7,747,442</td>
<td align="right">7,171,352</td>
<td align="right">-7.4%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">3,357,560,178</td>
<td align="right">3,108,233,564</td>
<td align="right">-7.4%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_UNICODE</td>
<td align="right">48,325,838</td>
<td align="right">44,751,993</td>
<td align="right">-7.4%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR</td>
<td align="right">324,346,150</td>
<td align="right">300,734,972</td>
<td align="right">-7.3%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_INT</td>
<td align="right">378,953,552</td>
<td align="right">351,402,803</td>
<td align="right">-7.3%</td>
</tr>
<tr>
<td align="left">BUILD_SLICE</td>
<td align="right">71,112,575</td>
<td align="right">65,946,633</td>
<td align="right">-7.3%</td>
</tr>
<tr>
<td align="left">MAKE_FUNCTION</td>
<td align="right">65,058,084</td>
<td align="right">60,443,774</td>
<td align="right">-7.1%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">313,838,691</td>
<td align="right">292,322,462</td>
<td align="right">-6.9%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_O</td>
<td align="right">271,577,153</td>
<td align="right">253,007,937</td>
<td align="right">-6.8%</td>
</tr>
<tr>
<td align="left">DELETE_SUBSCR</td>
<td align="right">78,611,534</td>
<td align="right">73,425,354</td>
<td align="right">-6.6%</td>
</tr>
<tr>
<td align="left">PUSH_NULL</td>
<td align="right">1,055,213,050</td>
<td align="right">987,168,378</td>
<td align="right">-6.4%</td>
</tr>
<tr>
<td align="left">LIST_EXTEND</td>
<td align="right">25,710,890</td>
<td align="right">24,127,406</td>
<td align="right">-6.2%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">2,482,637,648</td>
<td align="right">2,331,442,516</td>
<td align="right">-6.1%</td>
</tr>
<tr>
<td align="left">CALL_LIST_APPEND</td>
<td align="right">293,758,779</td>
<td align="right">276,043,676</td>
<td align="right">-6.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_CLASS</td>
<td align="right">130,821,248</td>
<td align="right">123,059,051</td>
<td align="right">-5.9%</td>
</tr>
<tr>
<td align="left">SETUP_ANNOTATIONS</td>
<td align="right">1,524</td>
<td align="right">1,440</td>
<td align="right">-5.5%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST_WITH_KEYWORDS</td>
<td align="right">38,485,395</td>
<td align="right">36,407,004</td>
<td align="right">-5.4%</td>
</tr>
<tr>
<td align="left">BUILD_STRING</td>
<td align="right">55,607,776</td>
<td align="right">52,767,721</td>
<td align="right">-5.1%</td>
</tr>
<tr>
<td align="left">SET_FUNCTION_ATTRIBUTE</td>
<td align="right">53,133,464</td>
<td align="right">50,428,493</td>
<td align="right">-5.1%</td>
</tr>
<tr>
<td align="left">BINARY_SLICE</td>
<td align="right">204,215,869</td>
<td align="right">193,848,096</td>
<td align="right">-5.1%</td>
</tr>
<tr>
<td align="left">STORE_FAST_STORE_FAST</td>
<td align="right">395,441,788</td>
<td align="right">375,902,695</td>
<td align="right">-4.9%</td>
</tr>
<tr>
<td align="left">DELETE_FAST</td>
<td align="right">2,231,862</td>
<td align="right">2,131,596</td>
<td align="right">-4.5%</td>
</tr>
<tr>
<td align="left">RAISE_VARARGS</td>
<td align="right">4,645,811</td>
<td align="right">4,444,918</td>
<td align="right">-4.3%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR</td>
<td align="right">68,798,669</td>
<td align="right">65,935,563</td>
<td align="right">-4.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_MODULE</td>
<td align="right">506,562,787</td>
<td align="right">485,961,248</td>
<td align="right">-4.1%</td>
</tr>
<tr>
<td align="left">FORMAT_SIMPLE</td>
<td align="right">109,448,215</td>
<td align="right">105,804,790</td>
<td align="right">-3.3%</td>
</tr>
<tr>
<td align="left">STORE_DEREF</td>
<td align="right">94,893,850</td>
<td align="right">92,075,363</td>
<td align="right">-3.0%</td>
</tr>
<tr>
<td align="left">INTERPRETER_EXIT</td>
<td align="right">2,256,764,030</td>
<td align="right">2,191,152,149</td>
<td align="right">-2.9%</td>
</tr>
<tr>
<td align="left">CALL_STR_1</td>
<td align="right">31,215,689</td>
<td align="right">30,367,316</td>
<td align="right">-2.7%</td>
</tr>
<tr>
<td align="left">FOR_ITER_GEN</td>
<td align="right">35,007,769</td>
<td align="right">34,067,444</td>
<td align="right">-2.7%</td>
</tr>
<tr>
<td align="left">END_FOR</td>
<td align="right">34,063,396</td>
<td align="right">33,148,511</td>
<td align="right">-2.7%</td>
</tr>
<tr>
<td align="left">BUILD_CONST_KEY_MAP</td>
<td align="right">2,852,587</td>
<td align="right">2,776,669</td>
<td align="right">-2.7%</td>
</tr>
<tr>
<td align="left">CALL_ALLOC_AND_ENTER_INIT</td>
<td align="right">93,467,212</td>
<td align="right">91,083,350</td>
<td align="right">-2.6%</td>
</tr>
<tr>
<td align="left">EXIT_INIT_CHECK</td>
<td align="right">93,414,105</td>
<td align="right">91,077,090</td>
<td align="right">-2.5%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_FLOAT</td>
<td align="right">75,397,022</td>
<td align="right">73,523,961</td>
<td align="right">-2.5%</td>
</tr>
<tr>
<td align="left">CALL_FUNCTION_EX</td>
<td align="right">203,663,243</td>
<td align="right">198,889,770</td>
<td align="right">-2.3%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_WITH_HINT</td>
<td align="right">54,715,417</td>
<td align="right">53,598,159</td>
<td align="right">-2.0%</td>
</tr>
<tr>
<td align="left">RETURN_GENERATOR</td>
<td align="right">365,448,252</td>
<td align="right">358,111,932</td>
<td align="right">-2.0%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP_SET</td>
<td align="right">282,467,249</td>
<td align="right">277,047,712</td>
<td align="right">-1.9%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_TUPLE_INT</td>
<td align="right">174,164,247</td>
<td align="right">171,162,567</td>
<td align="right">-1.7%</td>
</tr>
<tr>
<td align="left">LOAD_BUILD_CLASS</td>
<td align="right">24,340</td>
<td align="right">23,960</td>
<td align="right">-1.6%</td>
</tr>
<tr>
<td align="left">BINARY_OP_MULTIPLY_INT</td>
<td align="right">163,723,460</td>
<td align="right">161,460,325</td>
<td align="right">-1.4%</td>
</tr>
<tr>
<td align="left">STORE_NAME</td>
<td align="right">548,554</td>
<td align="right">541,140</td>
<td align="right">-1.4%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">20,711,906</td>
<td align="right">20,462,780</td>
<td align="right">-1.2%</td>
</tr>
<tr>
<td align="left">DELETE_NAME</td>
<td align="right">910</td>
<td align="right">900</td>
<td align="right">-1.1%</td>
</tr>
<tr>
<td align="left">CALL_INTRINSIC_1</td>
<td align="right">151,431,512</td>
<td align="right">150,002,653</td>
<td align="right">-0.9%</td>
</tr>
<tr>
<td align="left">DICT_UPDATE</td>
<td align="right">72,046</td>
<td align="right">71,392</td>
<td align="right">-0.9%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TUPLE</td>
<td align="right">241,771,116</td>
<td align="right">239,622,281</td>
<td align="right">-0.9%</td>
</tr>
<tr>
<td align="left">CONVERT_VALUE</td>
<td align="right">99,560,125</td>
<td align="right">98,852,020</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">YIELD_VALUE</td>
<td align="right">1,348,815,936</td>
<td align="right">1,341,778,108</td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">INSTRUMENTED_JUMP_BACKWARD</td>
<td align="right">6,244</td>
<td align="right">6,228</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">SET_UPDATE</td>
<td align="right">200,412</td>
<td align="right">200,100</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_FLOAT</td>
<td align="right">69,194,267</td>
<td align="right">69,087,726</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">LOAD_FROM_DICT_OR_DEREF</td>
<td align="right">2,003</td>
<td align="right">2,000</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">LOAD_LOCALS</td>
<td align="right">2,023</td>
<td align="right">2,020</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">WITH_EXCEPT_START</td>
<td align="right">233,386</td>
<td align="right">233,075</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">GET_YIELD_FROM_ITER</td>
<td align="right">46,683,912</td>
<td align="right">46,635,168</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">STORE_SLICE</td>
<td align="right">7,301,451</td>
<td align="right">7,296,912</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">BINARY_OP_MULTIPLY_FLOAT</td>
<td align="right">190,327,519</td>
<td align="right">190,224,752</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">LOAD_NAME</td>
<td align="right">8,099,356</td>
<td align="right">8,095,240</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD_NO_INTERRUPT</td>
<td align="right">556,485,357</td>
<td align="right">556,271,884</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">SEND_GEN</td>
<td align="right">787,108,806</td>
<td align="right">786,865,632</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_FLOAT</td>
<td align="right">149,889,076</td>
<td align="right">149,861,858</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">END_SEND</td>
<td align="right">402,624,019</td>
<td align="right">402,575,731</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">CLEANUP_THROW</td>
<td align="right">152,071</td>
<td align="right">152,069</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">GET_AWAITABLE</td>
<td align="right">229,150,440</td>
<td align="right">229,148,727</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">BEFORE_ASYNC_WITH</td>
<td align="right">3,005,938</td>
<td align="right">3,005,950</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">SEND</td>
<td align="right">173,840,844</td>
<td align="right">173,841,167</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_PY_WITH_DEFAULTS</td>
<td align="right">180,846,939</td>
<td align="right"></td>
<td align="right"></td>
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
<td align="left">LOAD_ATTR_GETATTRIBUTE_OVERRIDDEN</td>
<td align="right">89,680</td>
<td align="right">89,680</td>
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
<td align="left">CALL_INTRINSIC_2</td>
<td align="right">80</td>
<td align="right">80</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_NON_PY_GENERAL</td>
<td align="right"></td>
<td align="right">601,678,882</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_PY_GENERAL</td>
<td align="right"></td>
<td align="right">211,674,737</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_BOUND_METHOD_GENERAL</td>
<td align="right"></td>
<td align="right">7,581,188</td>
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
<td align="right">482,069,877</td>
<td align="right">25.1%</td>
<td align="right">423,184,218</td>
<td align="right">23.9%</td>
<td align="right">-12.2%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">1,436,999,299</td>
<td align="right">74.8%</td>
<td align="right">1,343,853,499</td>
<td align="right">76.0%</td>
<td align="right">-6.5%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">29,508,379</td>
<td align="right">1.5%</td>
<td align="right">29,506,625</td>
<td align="right">1.7%</td>
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
<td align="right">1,138,661</td>
<td align="right">65.4%</td>
<td align="right">1,110,522</td>
<td align="right">65.0%</td>
<td align="right">-2.5%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">603,214</td>
<td align="right">34.6%</td>
<td align="right">597,784</td>
<td align="right">35.0%</td>
<td align="right">-0.9%</td>
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
<td align="left">multiply other</td>
<td align="right">5,220</td>
<td align="right">0.5%</td>
<td align="right">2,680</td>
<td align="right">0.2%</td>
<td align="right">-48.7%</td>
</tr>
<tr>
<td align="left">add other</td>
<td align="right">55,147</td>
<td align="right">4.8%</td>
<td align="right">39,315</td>
<td align="right">3.5%</td>
<td align="right">-28.7%</td>
</tr>
<tr>
<td align="left">and different types</td>
<td align="right">542</td>
<td align="right">0.0%</td>
<td align="right">420</td>
<td align="right">0.0%</td>
<td align="right">-22.5%</td>
</tr>
<tr>
<td align="left">true divide float</td>
<td align="right">5,762</td>
<td align="right">0.5%</td>
<td align="right">5,124</td>
<td align="right">0.5%</td>
<td align="right">-11.1%</td>
</tr>
<tr>
<td align="left">or</td>
<td align="right">15,985</td>
<td align="right">1.4%</td>
<td align="right">14,699</td>
<td align="right">1.3%</td>
<td align="right">-8.0%</td>
</tr>
<tr>
<td align="left">remainder</td>
<td align="right">18,560</td>
<td align="right">1.6%</td>
<td align="right">17,275</td>
<td align="right">1.6%</td>
<td align="right">-6.9%</td>
</tr>
<tr>
<td align="left">subtract other</td>
<td align="right">11,534</td>
<td align="right">1.0%</td>
<td align="right">10,780</td>
<td align="right">1.0%</td>
<td align="right">-6.5%</td>
</tr>
<tr>
<td align="left">multiply different types</td>
<td align="right">87,606</td>
<td align="right">7.7%</td>
<td align="right">83,720</td>
<td align="right">7.5%</td>
<td align="right">-4.4%</td>
</tr>
<tr>
<td align="left">and other</td>
<td align="right">2,020</td>
<td align="right">0.2%</td>
<td align="right">1,976</td>
<td align="right">0.2%</td>
<td align="right">-2.2%</td>
</tr>
<tr>
<td align="left">and int</td>
<td align="right">35,849</td>
<td align="right">3.1%</td>
<td align="right">35,165</td>
<td align="right">3.2%</td>
<td align="right">-1.9%</td>
</tr>
<tr>
<td align="left">add different types</td>
<td align="right">39,653</td>
<td align="right">3.5%</td>
<td align="right">39,102</td>
<td align="right">3.5%</td>
<td align="right">-1.4%</td>
</tr>
<tr>
<td align="left">floor divide</td>
<td align="right">33,038</td>
<td align="right">2.9%</td>
<td align="right">32,676</td>
<td align="right">2.9%</td>
<td align="right">-1.1%</td>
</tr>
<tr>
<td align="left">true divide different types</td>
<td align="right">12,512</td>
<td align="right">1.1%</td>
<td align="right">12,419</td>
<td align="right">1.1%</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">power</td>
<td align="right">5,715</td>
<td align="right">0.5%</td>
<td align="right">5,728</td>
<td align="right">0.5%</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">true divide other</td>
<td align="right">3,404</td>
<td align="right">0.3%</td>
<td align="right">3,407</td>
<td align="right">0.3%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">lshift</td>
<td align="right">5,824</td>
<td align="right">0.5%</td>
<td align="right">5,828</td>
<td align="right">0.5%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">xor</td>
<td align="right">8,843</td>
<td align="right">0.8%</td>
<td align="right">8,844</td>
<td align="right">0.8%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">subtract different types</td>
<td align="right">782,454</td>
<td align="right">68.7%</td>
<td align="right">782,371</td>
<td align="right">70.5%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">rshift</td>
<td align="right">8,993</td>
<td align="right">0.8%</td>
<td align="right">8,993</td>
<td align="right">0.8%</td>
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
<td align="right">1,372,174,554</td>
<td align="right">80.8%</td>
<td align="right">1,187,464,552</td>
<td align="right">79.7%</td>
<td align="right">-13.5%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">325,951,011</td>
<td align="right">19.2%</td>
<td align="right">302,315,030</td>
<td align="right">20.3%</td>
<td align="right">-7.3%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">1,887,421</td>
<td align="right">0.1%</td>
<td align="right">1,825,577</td>
<td align="right">0.1%</td>
<td align="right">-3.3%</td>
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
<td align="right">148,326</td>
<td align="right">52.5%</td>
<td align="right">125,393</td>
<td align="right">51.1%</td>
<td align="right">-15.5%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">134,234</td>
<td align="right">47.5%</td>
<td align="right">120,126</td>
<td align="right">48.9%</td>
<td align="right">-10.5%</td>
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
<td align="left">code complex parameters</td>
<td align="right">4,935</td>
<td align="right">3.3%</td>
<td align="right">1,400</td>
<td align="right">1.1%</td>
<td align="right">-71.6%</td>
</tr>
<tr>
<td align="left">tuple slice</td>
<td align="right">182</td>
<td align="right">0.1%</td>
<td align="right">124</td>
<td align="right">0.1%</td>
<td align="right">-31.9%</td>
</tr>
<tr>
<td align="left">out of range</td>
<td align="right">58,179</td>
<td align="right">39.2%</td>
<td align="right">44,940</td>
<td align="right">35.8%</td>
<td align="right">-22.8%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">39,604</td>
<td align="right">26.7%</td>
<td align="right">34,489</td>
<td align="right">27.5%</td>
<td align="right">-12.9%</td>
</tr>
<tr>
<td align="left">buffer slice</td>
<td align="right">842</td>
<td align="right">0.6%</td>
<td align="right">760</td>
<td align="right">0.6%</td>
<td align="right">-9.7%</td>
</tr>
<tr>
<td align="left">buffer int</td>
<td align="right">22,661</td>
<td align="right">15.3%</td>
<td align="right">21,760</td>
<td align="right">17.4%</td>
<td align="right">-4.0%</td>
</tr>
<tr>
<td align="left">list slice</td>
<td align="right">1,323</td>
<td align="right">0.9%</td>
<td align="right">1,320</td>
<td align="right">1.1%</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">array int</td>
<td align="right">16,200</td>
<td align="right">10.9%</td>
<td align="right">16,200</td>
<td align="right">12.9%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">sequence int</td>
<td align="right">4,300</td>
<td align="right">2.9%</td>
<td align="right">4,300</td>
<td align="right">3.4%</td>
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
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">1,349,624,072</td>
<td align="right">17.6%</td>
<td align="right">318,954,312</td>
<td align="right">5.7%</td>
<td align="right">-76.4%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">6,300,676,901</td>
<td align="right">82.3%</td>
<td align="right">5,250,495,004</td>
<td align="right">94.2%</td>
<td align="right">-16.7%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">223,301,919</td>
<td align="right">2.9%</td>
<td align="right">196,448,947</td>
<td align="right">3.5%</td>
<td align="right">-12.0%</td>
</tr>
<tr>
<td align="left">
deopt
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">28,860</td>
<td align="right">0.0%</td>
<td align="right">28,860</td>
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
<td align="right">906,720</td>
<td align="right">15.9%</td>
<td align="right">92,709</td>
<td align="right">2.1%</td>
<td align="right">-89.8%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">4,792,254</td>
<td align="right">84.1%</td>
<td align="right">4,262,564</td>
<td align="right">97.9%</td>
<td align="right">-11.1%</td>
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
<td align="left">init not python</td>
<td align="right">13,061</td>
<td align="right">1.4%</td>
<td align="right">200</td>
<td align="right">0.2%</td>
<td align="right">-98.5%</td>
</tr>
<tr>
<td align="left">init not inline values</td>
<td align="right">105,557</td>
<td align="right">11.6%</td>
<td align="right">3,440</td>
<td align="right">3.7%</td>
<td align="right">-96.7%</td>
</tr>
<tr>
<td align="left">init not simple</td>
<td align="right">4,824</td>
<td align="right">0.5%</td>
<td align="right">680</td>
<td align="right">0.7%</td>
<td align="right">-85.9%</td>
</tr>
<tr>
<td align="left">wrong number arguments</td>
<td align="right">12,662</td>
<td align="right">1.4%</td>
<td align="right">11,420</td>
<td align="right">12.3%</td>
<td align="right">-9.8%</td>
</tr>
<tr>
<td align="left">class no vectorcall</td>
<td align="right">88,692</td>
<td align="right">9.8%</td>
<td align="right">80,369</td>
<td align="right">86.7%</td>
<td align="right">-9.4%</td>
</tr>
<tr>
<td align="left">out of versions</td>
<td align="right">981</td>
<td align="right">0.1%</td>
<td align="right">920</td>
<td align="right">1.0%</td>
<td align="right">-6.2%</td>
</tr>
<tr>
<td align="left">meth descr method fastcall keywords</td>
<td align="right">196,449</td>
<td align="right">21.7%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">code complex parameters</td>
<td align="right">172,203</td>
<td align="right">19.0%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">cfunc noargs</td>
<td align="right">68,850</td>
<td align="right">7.6%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">62,623</td>
<td align="right">6.9%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">metaclass</td>
<td align="right">42,302</td>
<td align="right">4.7%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">cfunc varargs keywords</td>
<td align="right">30,711</td>
<td align="right">3.4%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">class mutable</td>
<td align="right">22,226</td>
<td align="right">2.5%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">meth descr varargs keywords</td>
<td align="right">17,386</td>
<td align="right">1.9%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">cfunc varargs</td>
<td align="right">13,658</td>
<td align="right">1.5%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">cmethod</td>
<td align="right">12,635</td>
<td align="right">1.4%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">meth descr varargs</td>
<td align="right">12,347</td>
<td align="right">1.4%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">bound method</td>
<td align="right">11,477</td>
<td align="right">1.3%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">operator wrapper</td>
<td align="right">10,006</td>
<td align="right">1.1%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">method wrapper</td>
<td align="right">8,231</td>
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
<td align="right">1,433,285</td>
<td align="right">0.1%</td>
<td align="right">763,033</td>
<td align="right">0.0%</td>
<td align="right">-46.8%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">136,772,478</td>
<td align="right">7.8%</td>
<td align="right">104,695,638</td>
<td align="right">6.5%</td>
<td align="right">-23.5%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">1,616,900,273</td>
<td align="right">92.2%</td>
<td align="right">1,503,487,687</td>
<td align="right">93.5%</td>
<td align="right">-7.0%</td>
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
<td align="right">206,380</td>
<td align="right">67.5%</td>
<td align="right">143,091</td>
<td align="right">66.1%</td>
<td align="right">-30.7%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">99,485</td>
<td align="right">32.5%</td>
<td align="right">73,407</td>
<td align="right">33.9%</td>
<td align="right">-26.2%</td>
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
<td align="left">big int</td>
<td align="right">62,749</td>
<td align="right">30.4%</td>
<td align="right">27,723</td>
<td align="right">19.4%</td>
<td align="right">-55.8%</td>
</tr>
<tr>
<td align="left">bool</td>
<td align="right">3,814</td>
<td align="right">1.8%</td>
<td align="right">1,710</td>
<td align="right">1.2%</td>
<td align="right">-55.2%</td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">3,574</td>
<td align="right">1.7%</td>
<td align="right">1,740</td>
<td align="right">1.2%</td>
<td align="right">-51.3%</td>
</tr>
<tr>
<td align="left">baseobject</td>
<td align="right">32,311</td>
<td align="right">15.7%</td>
<td align="right">19,740</td>
<td align="right">13.8%</td>
<td align="right">-38.9%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">21,731</td>
<td align="right">10.5%</td>
<td align="right">16,837</td>
<td align="right">11.8%</td>
<td align="right">-22.5%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">2,343</td>
<td align="right">1.1%</td>
<td align="right">1,940</td>
<td align="right">1.4%</td>
<td align="right">-17.2%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">14,030</td>
<td align="right">6.8%</td>
<td align="right">11,762</td>
<td align="right">8.2%</td>
<td align="right">-16.2%</td>
</tr>
<tr>
<td align="left">different types</td>
<td align="right">33,534</td>
<td align="right">16.2%</td>
<td align="right">29,471</td>
<td align="right">20.6%</td>
<td align="right">-12.1%</td>
</tr>
<tr>
<td align="left">string</td>
<td align="right">10,920</td>
<td align="right">5.3%</td>
<td align="right">10,680</td>
<td align="right">7.5%</td>
<td align="right">-2.2%</td>
</tr>
<tr>
<td align="left">float long</td>
<td align="right">15,976</td>
<td align="right">7.7%</td>
<td align="right">16,088</td>
<td align="right">11.2%</td>
<td align="right">0.7%</td>
</tr>
<tr>
<td align="left">long float</td>
<td align="right">1,537</td>
<td align="right">0.7%</td>
<td align="right">1,540</td>
<td align="right">1.1%</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">bytes</td>
<td align="right">3,861</td>
<td align="right">1.9%</td>
<td align="right">3,860</td>
<td align="right">2.7%</td>
<td align="right">-0.0%</td>
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
<td align="right">75,758,198</td>
<td align="right">15.5%</td>
<td align="right">47,977,427</td>
<td align="right">11.0%</td>
<td align="right">-36.7%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">411,337,809</td>
<td align="right">84.4%</td>
<td align="right">387,739,145</td>
<td align="right">89.0%</td>
<td align="right">-5.7%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">2,517,260</td>
<td align="right">0.5%</td>
<td align="right">2,517,260</td>
<td align="right">0.6%</td>
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
<td align="right">107,137</td>
<td align="right">62.1%</td>
<td align="right">78,207</td>
<td align="right">56.1%</td>
<td align="right">-27.0%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">65,274</td>
<td align="right">37.9%</td>
<td align="right">61,257</td>
<td align="right">43.9%</td>
<td align="right">-6.2%</td>
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
<td align="right">13,934</td>
<td align="right">13.0%</td>
<td align="right">9,400</td>
<td align="right">12.0%</td>
<td align="right">-32.5%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">41,357</td>
<td align="right">38.6%</td>
<td align="right">29,143</td>
<td align="right">37.3%</td>
<td align="right">-29.5%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">25,056</td>
<td align="right">23.4%</td>
<td align="right">18,964</td>
<td align="right">24.2%</td>
<td align="right">-24.3%</td>
</tr>
<tr>
<td align="left">str</td>
<td align="right">26,790</td>
<td align="right">25.0%</td>
<td align="right">20,700</td>
<td align="right">26.5%</td>
<td align="right">-22.7%</td>
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
<td align="right">551,019</td>
<td align="right">0.1%</td>
<td align="right">346,826</td>
<td align="right">0.1%</td>
<td align="right">-37.1%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">98,049,392</td>
<td align="right">19.2%</td>
<td align="right">81,614,653</td>
<td align="right">18.6%</td>
<td align="right">-16.8%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">412,232,864</td>
<td align="right">80.7%</td>
<td align="right">356,477,510</td>
<td align="right">81.3%</td>
<td align="right">-13.5%</td>
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
<td align="right">72,232</td>
<td align="right">32.2%</td>
<td align="right">55,784</td>
<td align="right">30.9%</td>
<td align="right">-22.8%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">151,966</td>
<td align="right">67.8%</td>
<td align="right">124,490</td>
<td align="right">69.1%</td>
<td align="right">-18.1%</td>
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
<td align="left">reversed list</td>
<td align="right">7,673</td>
<td align="right">5.0%</td>
<td align="right">3,860</td>
<td align="right">3.1%</td>
<td align="right">-49.7%</td>
</tr>
<tr>
<td align="left">zip</td>
<td align="right">14,237</td>
<td align="right">9.4%</td>
<td align="right">8,580</td>
<td align="right">6.9%</td>
<td align="right">-39.7%</td>
</tr>
<tr>
<td align="left">enumerate</td>
<td align="right">17,940</td>
<td align="right">11.8%</td>
<td align="right">11,171</td>
<td align="right">9.0%</td>
<td align="right">-37.7%</td>
</tr>
<tr>
<td align="left">ascii string</td>
<td align="right">2,202</td>
<td align="right">1.4%</td>
<td align="right">1,460</td>
<td align="right">1.2%</td>
<td align="right">-33.7%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">22,307</td>
<td align="right">14.7%</td>
<td align="right">19,219</td>
<td align="right">15.4%</td>
<td align="right">-13.8%</td>
</tr>
<tr>
<td align="left">dict values</td>
<td align="right">6,095</td>
<td align="right">4.0%</td>
<td align="right">5,260</td>
<td align="right">4.2%</td>
<td align="right">-13.7%</td>
</tr>
<tr>
<td align="left">dict keys</td>
<td align="right">13,832</td>
<td align="right">9.1%</td>
<td align="right">12,160</td>
<td align="right">9.8%</td>
<td align="right">-12.1%</td>
</tr>
<tr>
<td align="left">dict items</td>
<td align="right">46,105</td>
<td align="right">30.3%</td>
<td align="right">41,883</td>
<td align="right">33.6%</td>
<td align="right">-9.2%</td>
</tr>
<tr>
<td align="left">itertools</td>
<td align="right">7,258</td>
<td align="right">4.8%</td>
<td align="right">6,880</td>
<td align="right">5.5%</td>
<td align="right">-5.2%</td>
</tr>
<tr>
<td align="left">seq iter</td>
<td align="right">2,054</td>
<td align="right">1.4%</td>
<td align="right">1,980</td>
<td align="right">1.6%</td>
<td align="right">-3.6%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">10,884</td>
<td align="right">7.2%</td>
<td align="right">10,679</td>
<td align="right">8.6%</td>
<td align="right">-1.9%</td>
</tr>
<tr>
<td align="left">bytes</td>
<td align="right">527</td>
<td align="right">0.3%</td>
<td align="right">518</td>
<td align="right">0.4%</td>
<td align="right">-1.7%</td>
</tr>
<tr>
<td align="left">map</td>
<td align="right">569</td>
<td align="right">0.4%</td>
<td align="right">560</td>
<td align="right">0.4%</td>
<td align="right">-1.6%</td>
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
<td align="right">1</td>
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
<td align="right">310,545,016</td>
<td align="right">3.2%</td>
<td align="right">253,048,131</td>
<td align="right">3.1%</td>
<td align="right">-18.5%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">932,123,653</td>
<td align="right">9.6%</td>
<td align="right">778,788,966</td>
<td align="right">9.5%</td>
<td align="right">-16.5%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">8,761,140,647</td>
<td align="right">90.3%</td>
<td align="right">7,433,067,420</td>
<td align="right">90.4%</td>
<td align="right">-15.2%</td>
</tr>
<tr>
<td align="left">
deopt
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">679,367</td>
<td align="right">0.0%</td>
<td align="right">679,211</td>
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
<td align="right">6,664,358</td>
<td align="right">88.5%</td>
<td align="right">5,412,843</td>
<td align="right">87.7%</td>
<td align="right">-18.8%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">870,026</td>
<td align="right">11.5%</td>
<td align="right">755,897</td>
<td align="right">12.3%</td>
<td align="right">-13.1%</td>
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
<td align="right">1,910</td>
<td align="right">0.2%</td>
<td align="right">20</td>
<td align="right">0.0%</td>
<td align="right">-99.0%</td>
</tr>
<tr>
<td align="left">non overriding descriptor</td>
<td align="right">13,280</td>
<td align="right">1.5%</td>
<td align="right">7,280</td>
<td align="right">1.0%</td>
<td align="right">-45.2%</td>
</tr>
<tr>
<td align="left">shadowed</td>
<td align="right">91,503</td>
<td align="right">10.5%</td>
<td align="right">57,126</td>
<td align="right">7.6%</td>
<td align="right">-37.6%</td>
</tr>
<tr>
<td align="left">class method obj</td>
<td align="right">20,000</td>
<td align="right">2.3%</td>
<td align="right">15,360</td>
<td align="right">2.0%</td>
<td align="right">-23.2%</td>
</tr>
<tr>
<td align="left">builtin class method</td>
<td align="right">3,581</td>
<td align="right">0.4%</td>
<td align="right">2,960</td>
<td align="right">0.4%</td>
<td align="right">-17.3%</td>
</tr>
<tr>
<td align="left">not managed dict</td>
<td align="right">233,200</td>
<td align="right">26.8%</td>
<td align="right">195,707</td>
<td align="right">25.9%</td>
<td align="right">-16.1%</td>
</tr>
<tr>
<td align="left">module attr not found</td>
<td align="right">17,356</td>
<td align="right">2.0%</td>
<td align="right">14,660</td>
<td align="right">1.9%</td>
<td align="right">-15.5%</td>
</tr>
<tr>
<td align="left">class attr simple</td>
<td align="right">53,186</td>
<td align="right">6.1%</td>
<td align="right">46,155</td>
<td align="right">6.1%</td>
<td align="right">-13.2%</td>
</tr>
<tr>
<td align="left">metaclass attribute</td>
<td align="right">170,886</td>
<td align="right">19.6%</td>
<td align="right">159,514</td>
<td align="right">21.1%</td>
<td align="right">-6.7%</td>
</tr>
<tr>
<td align="left">method</td>
<td align="right">104,510</td>
<td align="right">12.0%</td>
<td align="right">97,980</td>
<td align="right">13.0%</td>
<td align="right">-6.2%</td>
</tr>
<tr>
<td align="left">overridden</td>
<td align="right">15,088</td>
<td align="right">1.7%</td>
<td align="right">14,864</td>
<td align="right">2.0%</td>
<td align="right">-1.5%</td>
</tr>
<tr>
<td align="left">non object slot</td>
<td align="right">3,380</td>
<td align="right">0.4%</td>
<td align="right">3,340</td>
<td align="right">0.4%</td>
<td align="right">-1.2%</td>
</tr>
<tr>
<td align="left">mutable class</td>
<td align="right">75,292</td>
<td align="right">8.7%</td>
<td align="right">74,463</td>
<td align="right">9.9%</td>
<td align="right">-1.1%</td>
</tr>
<tr>
<td align="left">class attr descriptor</td>
<td align="right">29,018</td>
<td align="right">3.3%</td>
<td align="right">28,760</td>
<td align="right">3.8%</td>
<td align="right">-0.9%</td>
</tr>
<tr>
<td align="left">non string or split</td>
<td align="right">20,216</td>
<td align="right">2.3%</td>
<td align="right">20,127</td>
<td align="right">2.7%</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">not in keys</td>
<td align="right">15,840</td>
<td align="right">1.8%</td>
<td align="right">15,801</td>
<td align="right">2.1%</td>
<td align="right">-0.2%</td>
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
<td align="right">5,598,515,651</td>
<td align="right">99.6%</td>
<td align="right">4,782,054,075</td>
<td align="right">99.6%</td>
<td align="right">-14.6%</td>
</tr>
<tr>
<td align="left">
deopt
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">11,926</td>
<td align="right">0.0%</td>
<td align="right">10,900</td>
<td align="right">0.0%</td>
<td align="right">-8.6%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">429,361</td>
<td align="right">0.0%</td>
<td align="right">419,083</td>
<td align="right">0.0%</td>
<td align="right">-2.4%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">20,503,962</td>
<td align="right">0.4%</td>
<td align="right">20,369,250</td>
<td align="right">0.4%</td>
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
<td align="left">Success</td>
<td align="right">637,305</td>
<td align="right">100.0%</td>
<td align="right">512,613</td>
<td align="right">100.0%</td>
<td align="right">-19.6%</td>
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
<td align="right">134,234,548</td>
<td align="right">100.0%</td>
<td align="right">89,174,967</td>
<td align="right">100.0%</td>
<td align="right">-33.6%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">11,731</td>
<td align="right">0.0%</td>
<td align="right">9,346</td>
<td align="right">0.0%</td>
<td align="right">-20.3%</td>
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
<td align="right">11,622</td>
<td align="right">100.0%</td>
<td align="right">9,140</td>
<td align="right">100.0%</td>
<td align="right">-21.4%</td>
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
<td align="right">787,077,906</td>
<td align="right">81.9%</td>
<td align="right">786,834,732</td>
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
<td align="right">173,802,912</td>
<td align="right">18.1%</td>
<td align="right">173,803,289</td>
<td align="right">18.1%</td>
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
<td align="right">7,101</td>
<td align="right">10.3%</td>
<td align="right">7,050</td>
<td align="right">10.3%</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">61,731</td>
<td align="right">89.7%</td>
<td align="right">61,728</td>
<td align="right">89.7%</td>
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
<td align="right">16,130</td>
<td align="right">26.1%</td>
<td align="right">16,128</td>
<td align="right">26.1%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">9,961</td>
<td align="right">16.1%</td>
<td align="right">9,960</td>
<td align="right">16.1%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">async generator send</td>
<td align="right">33,180</td>
<td align="right">53.7%</td>
<td align="right">33,180</td>
<td align="right">53.8%</td>
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
<td align="right">139,656,702</td>
<td align="right">5.4%</td>
<td align="right">69,508,548</td>
<td align="right">3.4%</td>
<td align="right">-50.2%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">183,822,374</td>
<td align="right">7.1%</td>
<td align="right">101,872,741</td>
<td align="right">5.1%</td>
<td align="right">-44.6%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">2,402,863,381</td>
<td align="right">92.8%</td>
<td align="right">1,911,556,312</td>
<td align="right">94.9%</td>
<td align="right">-20.4%</td>
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
<td align="right">2,774,834</td>
<td align="right">96.0%</td>
<td align="right">1,428,613</td>
<td align="right">93.9%</td>
<td align="right">-48.5%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">116,229</td>
<td align="right">4.0%</td>
<td align="right">92,429</td>
<td align="right">6.1%</td>
<td align="right">-20.5%</td>
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
<td align="right">25,928</td>
<td align="right">22.3%</td>
<td align="right">11,160</td>
<td align="right">12.1%</td>
<td align="right">-57.0%</td>
</tr>
<tr>
<td align="left">not in dict</td>
<td align="right">12,647</td>
<td align="right">10.9%</td>
<td align="right">7,780</td>
<td align="right">8.4%</td>
<td align="right">-38.5%</td>
</tr>
<tr>
<td align="left">overriding descriptor</td>
<td align="right">10,641</td>
<td align="right">9.2%</td>
<td align="right">8,721</td>
<td align="right">9.4%</td>
<td align="right">-18.0%</td>
</tr>
<tr>
<td align="left">not in keys</td>
<td align="right">5,207</td>
<td align="right">4.5%</td>
<td align="right">4,360</td>
<td align="right">4.7%</td>
<td align="right">-16.3%</td>
</tr>
<tr>
<td align="left">overridden</td>
<td align="right">6,569</td>
<td align="right">5.7%</td>
<td align="right">5,940</td>
<td align="right">6.4%</td>
<td align="right">-9.6%</td>
</tr>
<tr>
<td align="left">property</td>
<td align="right">4,987</td>
<td align="right">4.3%</td>
<td align="right">4,880</td>
<td align="right">5.3%</td>
<td align="right">-2.1%</td>
</tr>
<tr>
<td align="left">no dict</td>
<td align="right">5,009</td>
<td align="right">4.3%</td>
<td align="right">4,980</td>
<td align="right">5.4%</td>
<td align="right">-0.6%</td>
</tr>
<tr>
<td align="left">non string or split</td>
<td align="right">14,601</td>
<td align="right">12.6%</td>
<td align="right">14,560</td>
<td align="right">15.8%</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">not managed dict</td>
<td align="right">28,506</td>
<td align="right">24.5%</td>
<td align="right">28,508</td>
<td align="right">30.8%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">method</td>
<td align="right">1,500</td>
<td align="right">1.3%</td>
<td align="right">1,500</td>
<td align="right">1.6%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">out of versions</td>
<td align="right">594</td>
<td align="right">0.5%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
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
<td align="right">206,804,596</td>
<td align="right">75.0%</td>
<td align="right">167,286,807</td>
<td align="right">71.7%</td>
<td align="right">-19.1%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">68,723,649</td>
<td align="right">24.9%</td>
<td align="right">65,864,705</td>
<td align="right">28.2%</td>
<td align="right">-4.2%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">38</td>
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
<td align="right">16,514</td>
<td align="right">22.0%</td>
<td align="right">14,883</td>
<td align="right">21.0%</td>
<td align="right">-9.9%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">58,544</td>
<td align="right">78.0%</td>
<td align="right">55,975</td>
<td align="right">79.0%</td>
<td align="right">-4.4%</td>
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
<td align="right">1,315</td>
<td align="right">2.2%</td>
<td align="right">800</td>
<td align="right">1.4%</td>
<td align="right">-39.2%</td>
</tr>
<tr>
<td align="left">dict subclass no override</td>
<td align="right">12,516</td>
<td align="right">21.4%</td>
<td align="right">11,299</td>
<td align="right">20.2%</td>
<td align="right">-9.7%</td>
</tr>
<tr>
<td align="left">bytearray int</td>
<td align="right">925</td>
<td align="right">1.6%</td>
<td align="right">900</td>
<td align="right">1.6%</td>
<td align="right">-2.7%</td>
</tr>
<tr>
<td align="left">py simple</td>
<td align="right">35,438</td>
<td align="right">60.5%</td>
<td align="right">34,656</td>
<td align="right">61.9%</td>
<td align="right">-2.2%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">1,870</td>
<td align="right">3.2%</td>
<td align="right">1,840</td>
<td align="right">3.3%</td>
<td align="right">-1.6%</td>
</tr>
<tr>
<td align="left">array int</td>
<td align="right">6,480</td>
<td align="right">11.1%</td>
<td align="right">6,480</td>
<td align="right">11.6%</td>
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
<td align="right">88,000,620</td>
<td align="right">2.4%</td>
<td align="right">49,198,712</td>
<td align="right">1.6%</td>
<td align="right">-44.1%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">308,040,373</td>
<td align="right">8.6%</td>
<td align="right">247,417,721</td>
<td align="right">8.0%</td>
<td align="right">-19.7%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">3,291,697,745</td>
<td align="right">91.4%</td>
<td align="right">2,834,094,397</td>
<td align="right">91.9%</td>
<td align="right">-13.9%</td>
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
<td align="right">395,797</td>
<td align="right">17.0%</td>
<td align="right">190,286</td>
<td align="right">14.3%</td>
<td align="right">-51.9%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">1,929,583</td>
<td align="right">83.0%</td>
<td align="right">1,136,900</td>
<td align="right">85.7%</td>
<td align="right">-41.1%</td>
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
<td align="right">170,517</td>
<td align="right">43.1%</td>
<td align="right">5,019</td>
<td align="right">2.6%</td>
<td align="right">-97.1%</td>
</tr>
<tr>
<td align="left">number</td>
<td align="right">23,655</td>
<td align="right">6.0%</td>
<td align="right">4,734</td>
<td align="right">2.5%</td>
<td align="right">-80.0%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">42,082</td>
<td align="right">10.6%</td>
<td align="right">30,481</td>
<td align="right">16.0%</td>
<td align="right">-27.6%</td>
</tr>
<tr>
<td align="left">dict</td>
<td align="right">28,452</td>
<td align="right">7.2%</td>
<td align="right">22,316</td>
<td align="right">11.7%</td>
<td align="right">-21.6%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">40,460</td>
<td align="right">10.2%</td>
<td align="right">38,675</td>
<td align="right">20.3%</td>
<td align="right">-4.4%</td>
</tr>
<tr>
<td align="left">mapping</td>
<td align="right">50,718</td>
<td align="right">12.8%</td>
<td align="right">49,280</td>
<td align="right">25.9%</td>
<td align="right">-2.8%</td>
</tr>
<tr>
<td align="left">sequence</td>
<td align="right">17,241</td>
<td align="right">4.4%</td>
<td align="right">17,106</td>
<td align="right">9.0%</td>
<td align="right">-0.8%</td>
</tr>
<tr>
<td align="left">float</td>
<td align="right">2,323</td>
<td align="right">0.6%</td>
<td align="right">2,327</td>
<td align="right">1.2%</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">bytes</td>
<td align="right">18,689</td>
<td align="right">4.7%</td>
<td align="right">18,688</td>
<td align="right">9.8%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">bytearray</td>
<td align="right">1,240</td>
<td align="right">0.3%</td>
<td align="right">1,240</td>
<td align="right">0.7%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">memory view</td>
<td align="right">420</td>
<td align="right">0.1%</td>
<td align="right">420</td>
<td align="right">0.2%</td>
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
<td align="right">492,924</td>
<td align="right">0.1%</td>
<td align="right">418,785</td>
<td align="right">0.1%</td>
<td align="right">-15.0%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">563,789,703</td>
<td align="right">99.9%</td>
<td align="right">532,931,972</td>
<td align="right">99.9%</td>
<td align="right">-5.5%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">27</td>
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
<td align="left">Failure</td>
<td align="right">3,506</td>
<td align="right">8.8%</td>
<td align="right">2,776</td>
<td align="right">8.3%</td>
<td align="right">-20.8%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">36,290</td>
<td align="right">91.2%</td>
<td align="right">30,701</td>
<td align="right">91.7%</td>
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
<td align="left">iterator</td>
<td align="right">681</td>
<td align="right">19.4%</td>
<td align="right">500</td>
<td align="right">18.0%</td>
<td align="right">-26.6%</td>
</tr>
<tr>
<td align="left">sequence</td>
<td align="right">2,445</td>
<td align="right">69.7%</td>
<td align="right">1,896</td>
<td align="right">68.3%</td>
<td align="right">-22.5%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">380</td>
<td align="right">10.8%</td>
<td align="right">380</td>
<td align="right">13.7%</td>
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
<td align="right">798,041,789</td>
<td align="right">0.7%</td>
<td align="right">603,793,361</td>
<td align="right">0.6%</td>
<td align="right">-24.3%</td>
</tr>
<tr>
<td align="left">
Not specialized
<details>
<summary>ⓘ</summary>

Instructions that could be specialized but aren't, e.g. `LOAD_ATTR`, `BINARY_SLICE`.
</details>
</td>
<td align="right">10,455,770,381</td>
<td align="right">9.4%</td>
<td align="right">8,105,635,843</td>
<td align="right">8.3%</td>
<td align="right">-22.5%</td>
</tr>
<tr>
<td align="left">
Basic
<details>
<summary>ⓘ</summary>

Instructions that are not and cannot be specialized, e.g. `LOAD_FAST`.
</details>
</td>
<td align="right">60,826,318,628</td>
<td align="right">54.6%</td>
<td align="right">53,804,759,632</td>
<td align="right">55.3%</td>
<td align="right">-11.5%</td>
</tr>
<tr>
<td align="left">
Specialized hits
<details>
<summary>ⓘ</summary>

Specialized instructions, e.g. `LOAD_ATTR_MODULE` that complete.
</details>
</td>
<td align="right">39,368,504,862</td>
<td align="right">35.3%</td>
<td align="right">34,828,000,697</td>
<td align="right">35.8%</td>
<td align="right">-11.5%</td>
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
<td align="left">CALL</td>
<td align="right">1,349,624,072</td>
<td align="right">32.5%</td>
<td align="right">318,954,312</td>
<td align="right">12.0%</td>
<td align="right">-76.4%</td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">183,822,374</td>
<td align="right">4.4%</td>
<td align="right">101,872,741</td>
<td align="right">3.8%</td>
<td align="right">-44.6%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">136,772,478</td>
<td align="right">3.3%</td>
<td align="right">104,695,638</td>
<td align="right">3.9%</td>
<td align="right">-23.5%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">308,040,373</td>
<td align="right">7.4%</td>
<td align="right">247,417,721</td>
<td align="right">9.3%</td>
<td align="right">-19.7%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">98,049,392</td>
<td align="right">2.4%</td>
<td align="right">81,614,653</td>
<td align="right">3.1%</td>
<td align="right">-16.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">932,123,653</td>
<td align="right">22.4%</td>
<td align="right">778,788,966</td>
<td align="right">29.2%</td>
<td align="right">-16.5%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">482,069,877</td>
<td align="right">11.6%</td>
<td align="right">423,184,218</td>
<td align="right">15.9%</td>
<td align="right">-12.2%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR</td>
<td align="right">325,951,011</td>
<td align="right">7.8%</td>
<td align="right">302,315,030</td>
<td align="right">11.3%</td>
<td align="right">-7.3%</td>
</tr>
<tr>
<td align="left">SEND</td>
<td align="right">173,802,912</td>
<td align="right">4.2%</td>
<td align="right">173,803,289</td>
<td align="right">6.5%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">75,758,198</td>
<td align="right">1.8%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">STORE_SUBSCR</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">65,864,705</td>
<td align="right">2.5%</td>
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
<td align="left">STORE_ATTR_SLOT</td>
<td align="right">94,977,208</td>
<td align="right">11.9%</td>
<td align="right">26,140,940</td>
<td align="right">4.3%</td>
<td align="right">-72.5%</td>
</tr>
<tr>
<td align="left">TO_BOOL_ALWAYS_TRUE</td>
<td align="right">41,563,022</td>
<td align="right">5.2%</td>
<td align="right">23,637,590</td>
<td align="right">3.9%</td>
<td align="right">-43.1%</td>
</tr>
<tr>
<td align="left">CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">31,004,385</td>
<td align="right">3.9%</td>
<td align="right">23,621,391</td>
<td align="right">3.9%</td>
<td align="right">-23.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">50,699,156</td>
<td align="right">6.4%</td>
<td align="right">41,719,888</td>
<td align="right">6.9%</td>
<td align="right">-17.7%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">109,997,074</td>
<td align="right">13.8%</td>
<td align="right">90,555,233</td>
<td align="right">15.0%</td>
<td align="right">-17.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">119,899,100</td>
<td align="right">15.0%</td>
<td align="right">105,105,470</td>
<td align="right">17.4%</td>
<td align="right">-12.3%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">42,597,204</td>
<td align="right">5.3%</td>
<td align="right">39,098,232</td>
<td align="right">6.5%</td>
<td align="right">-8.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">77,654,673</td>
<td align="right">9.7%</td>
<td align="right">73,374,119</td>
<td align="right">12.1%</td>
<td align="right">-5.5%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">44,630,816</td>
<td align="right">5.6%</td>
<td align="right">43,343,856</td>
<td align="right">7.2%</td>
<td align="right">-2.9%</td>
</tr>
<tr>
<td align="left">TO_BOOL_NONE</td>
<td align="right">41,134,232</td>
<td align="right">5.2%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">27,796,555</td>
<td align="right">4.6%</td>
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
<td align="left">Frames pushed</td>
<td align="right">6,541,978,719</td>
<td align="right">79.5%</td>
<td align="right">6,164,672,282</td>
<td align="right">78.6%</td>
<td align="right">-5.8%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (api)</td>
<td align="right">247,995,284</td>
<td align="right">3.0%</td>
<td align="right">233,762,573</td>
<td align="right">3.0%</td>
<td align="right">-5.7%</td>
</tr>
<tr>
<td align="left">Calls to Python functions inlined</td>
<td align="right">5,973,953,571</td>
<td align="right">72.6%</td>
<td align="right">5,654,042,511</td>
<td align="right">72.0%</td>
<td align="right">-5.4%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (function vectorcall)</td>
<td align="right">1,394,463,644</td>
<td align="right">16.9%</td>
<td align="right">1,337,118,543</td>
<td align="right">17.0%</td>
<td align="right">-4.1%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (vector)</td>
<td align="right">1,397,140,401</td>
<td align="right">17.0%</td>
<td align="right">1,339,794,683</td>
<td align="right">17.1%</td>
<td align="right">-4.1%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (function ex)</td>
<td align="right">35,970,124</td>
<td align="right">0.4%</td>
<td align="right">34,551,509</td>
<td align="right">0.4%</td>
<td align="right">-3.9%</td>
</tr>
<tr>
<td align="left">Frame objects created</td>
<td align="right">76,558,142</td>
<td align="right">0.9%</td>
<td align="right">73,798,953</td>
<td align="right">0.9%</td>
<td align="right">-3.6%</td>
</tr>
<tr>
<td align="left">Calls to PyEval_EvalDefault</td>
<td align="right">2,259,449,033</td>
<td align="right">27.4%</td>
<td align="right">2,193,760,442</td>
<td align="right">28.0%</td>
<td align="right">-2.9%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (total)</td>
<td align="right">2,259,449,033</td>
<td align="right">27.4%</td>
<td align="right">2,193,760,442</td>
<td align="right">28.0%</td>
<td align="right">-2.9%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (build class)</td>
<td align="right">24,340</td>
<td align="right">0.0%</td>
<td align="right">23,960</td>
<td align="right">0.0%</td>
<td align="right">-1.6%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (slot)</td>
<td align="right">458,517,044</td>
<td align="right">5.6%</td>
<td align="right">453,928,569</td>
<td align="right">5.8%</td>
<td align="right">-1.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (generator)</td>
<td align="right">862,308,632</td>
<td align="right">10.5%</td>
<td align="right">853,965,759</td>
<td align="right">10.9%</td>
<td align="right">-1.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (legacy)</td>
<td align="right">2,652,417</td>
<td align="right">0.0%</td>
<td align="right">2,652,180</td>
<td align="right">0.0%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (method)</td>
<td align="right">213,149,994</td>
<td align="right">2.6%</td>
<td align="right">213,154,322</td>
<td align="right">2.7%</td>
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
<td align="right">9,626,638</td>
<td align="right"></td>
<td align="right">4,777,371</td>
<td align="right"></td>
<td align="right">-50.4%</td>
</tr>
<tr>
<td align="left">Method cache misses</td>
<td align="right">30,541,299</td>
<td align="right"></td>
<td align="right">19,776,041</td>
<td align="right"></td>
<td align="right">-35.2%</td>
</tr>
<tr>
<td align="left">Method cache collisions</td>
<td align="right">33,200,859</td>
<td align="right"></td>
<td align="right">24,345,744</td>
<td align="right"></td>
<td align="right">-26.7%</td>
</tr>
<tr>
<td align="left">Method cache hits</td>
<td align="right">2,505,709,683</td>
<td align="right"></td>
<td align="right">2,248,898,055</td>
<td align="right"></td>
<td align="right">-10.2%</td>
</tr>
<tr>
<td align="left">Increfs</td>
<td align="right">24,204,140,340</td>
<td align="right">21.4%</td>
<td align="right">22,779,151,933</td>
<td align="right">21.1%</td>
<td align="right">-5.9%</td>
</tr>
<tr>
<td align="left">Method cache dunder hits</td>
<td align="right">3,276,965,883</td>
<td align="right"></td>
<td align="right">3,088,215,284</td>
<td align="right"></td>
<td align="right">-5.8%</td>
</tr>
<tr>
<td align="left">Decrefs</td>
<td align="right">27,608,938,861</td>
<td align="right">21.3%</td>
<td align="right">26,137,377,857</td>
<td align="right">21.1%</td>
<td align="right">-5.3%</td>
</tr>
<tr>
<td align="left">Inline values</td>
<td align="right">170,892,029</td>
<td align="right"></td>
<td align="right">162,076,870</td>
<td align="right"></td>
<td align="right">-5.2%</td>
</tr>
<tr>
<td align="left">Materialize dict (new key)</td>
<td align="right">67,112</td>
<td align="right">0.0%</td>
<td align="right">64,160</td>
<td align="right">0.0%</td>
<td align="right">-4.4%</td>
</tr>
<tr>
<td align="left">Interpreter increfs</td>
<td align="right">89,071,532,359</td>
<td align="right">78.6%</td>
<td align="right">85,156,791,600</td>
<td align="right">78.9%</td>
<td align="right">-4.4%</td>
</tr>
<tr>
<td align="left">Interpreter decrefs</td>
<td align="right">102,304,538,510</td>
<td align="right">78.7%</td>
<td align="right">98,002,618,361</td>
<td align="right">78.9%</td>
<td align="right">-4.2%</td>
</tr>
<tr>
<td align="left">Allocations to 512 bytes</td>
<td align="right">10,804,661,736</td>
<td align="right">62.0%</td>
<td align="right">10,399,148,178</td>
<td align="right">61.7%</td>
<td align="right">-3.8%</td>
</tr>
<tr>
<td align="left">Allocations</td>
<td align="right">10,929,982,443</td>
<td align="right">62.7%</td>
<td align="right">10,524,699,499</td>
<td align="right">62.4%</td>
<td align="right">-3.7%</td>
</tr>
<tr>
<td align="left">Frees</td>
<td align="right">11,233,763,306</td>
<td align="right"></td>
<td align="right">10,849,480,940</td>
<td align="right"></td>
<td align="right">-3.4%</td>
</tr>
<tr>
<td align="left">Allocations from freelist</td>
<td align="right">6,508,859,461</td>
<td align="right">37.3%</td>
<td align="right">6,338,295,178</td>
<td align="right">37.6%</td>
<td align="right">-2.6%</td>
</tr>
<tr>
<td align="left">Frees to freelist</td>
<td align="right">6,510,772,905</td>
<td align="right"></td>
<td align="right">6,340,158,636</td>
<td align="right"></td>
<td align="right">-2.6%</td>
</tr>
<tr>
<td align="left">Allocations over 4 kbytes</td>
<td align="right">20,740,861</td>
<td align="right">0.1%</td>
<td align="right">20,540,470</td>
<td align="right">0.1%</td>
<td align="right">-1.0%</td>
</tr>
<tr>
<td align="left">Allocations to 4 kbytes</td>
<td align="right">104,579,846</td>
<td align="right">0.6%</td>
<td align="right">105,010,851</td>
<td align="right">0.6%</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">Materialize dict (on request)</td>
<td align="right">6,549,542</td>
<td align="right">3.8%</td>
<td align="right">6,547,420</td>
<td align="right">4.0%</td>
<td align="right">-0.0%</td>
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
<td align="right">21,246,877</td>
<td align="right">15,099,426,732</td>
<td align="right">0</td>
<td align="right">19,411,417</td>
<td align="right">14,510,980,089</td>
</tr>
<tr>
<td align="right">2</td>
<td align="right">0</td>
<td align="right">10,755,840</td>
<td align="right">6,973,328,432</td>
<td align="right">0</td>
<td align="right">10,755,840</td>
<td align="right">6,973,917,300</td>
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
<td align="right">564</td>
<td align="right">0.1%</td>
<td align="right">688</td>
<td align="right">0.1%</td>
<td align="right">22.0%</td>
</tr>
<tr>
<td align="left">
Traces created
<details>
<summary>ⓘ</summary>

The number of traces that were successfully created.
</details>
</td>
<td align="right">134,719</td>
<td align="right">15.6%</td>
<td align="right">108,816</td>
<td align="right">14.5%</td>
<td align="right">-19.2%</td>
</tr>
<tr>
<td align="left">
Low confidence
<details>
<summary>ⓘ</summary>

A trace is abandoned because the likelihood of the jump to top being taken is too low.
</details>
</td>
<td align="right">7,855</td>
<td align="right">0.9%</td>
<td align="right">6,430</td>
<td align="right">0.9%</td>
<td align="right">-18.1%</td>
</tr>
<tr>
<td align="left">
Recursive call
<details>
<summary>ⓘ</summary>

A trace is truncated because it has a recursive call.
</details>
</td>
<td align="right">1,522</td>
<td align="right">0.2%</td>
<td align="right">1,320</td>
<td align="right">0.2%</td>
<td align="right">-13.3%</td>
</tr>
<tr>
<td align="left">
Optimization attempts
<details>
<summary>ⓘ</summary>

The number of times a potential trace is identified.  Specifically, this occurs in the JUMP BACKWARD instruction when the counter reaches a threshold.
</details>
</td>
<td align="right">864,064</td>
<td align="right"></td>
<td align="right">752,716</td>
<td align="right"></td>
<td align="right">-12.9%</td>
</tr>
<tr>
<td align="left">
Trace too short
<details>
<summary>ⓘ</summary>

A potential trace is abandoced because it it too short.
</details>
</td>
<td align="right">729,345</td>
<td align="right">84.4%</td>
<td align="right">643,900</td>
<td align="right">85.5%</td>
<td align="right">-11.7%</td>
</tr>
<tr>
<td align="left">
Inner loop found
<details>
<summary>ⓘ</summary>

A trace is truncated because it has an inner loop
</details>
</td>
<td align="right">50,106</td>
<td align="right">5.8%</td>
<td align="right">46,319</td>
<td align="right">6.2%</td>
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
<td align="right">189,950,522,411</td>
<td align="right">2,632.7%</td>
<td align="right">200,241,763,770</td>
<td align="right">2,857.0%</td>
<td align="right">5.4%</td>
</tr>
<tr>
<td align="left">
Traces executed
<details>
<summary>ⓘ</summary>

The number of traces that were executed
</details>
</td>
<td align="right">7,215,098,788</td>
<td align="right"></td>
<td align="right">7,008,710,282</td>
<td align="right"></td>
<td align="right">-2.9%</td>
</tr>
<tr>
<td align="left">
Executors invalidated
<details>
<summary>ⓘ</summary>

The number of executors that were invalidated due to watched dictionary changes.
</details>
</td>
<td align="right">6,004</td>
<td align="right">4.5%</td>
<td align="right">6,100</td>
<td align="right">5.6%</td>
<td align="right">1.6%</td>
</tr>
<tr>
<td align="left">
Trace stack underflow
<details>
<summary>ⓘ</summary>

A potential trace is abandoned because it pops more frames than it pushes.
</details>
</td>
<td align="right">444,457</td>
<td align="right">51.4%</td>
<td align="right">445,214</td>
<td align="right">59.1%</td>
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
<td align="right">100</td>
<td align="right">0.0%</td>
<td align="right">100 / 0 !!</td>
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
<td align="right">131,228</td>
<td align="right">97.4%</td>
<td align="right">105,276</td>
<td align="right">96.7%</td>
<td align="right">-19.8%</td>
</tr>
<tr>
<td align="left">
Optimizer attempts
<details>
<summary>ⓘ</summary>

The number of times the trace optimizer (_Py_uop_analyze_and_optimize) was run.
</details>
</td>
<td align="right">134,719</td>
<td align="right"></td>
<td align="right">108,816</td>
<td align="right"></td>
<td align="right">-19.2%</td>
</tr>
<tr>
<td align="left">
Remove globals incorrect keys
<details>
<summary>ⓘ</summary>

The keys in the globals dictionary aren't what was expected
</details>
</td>
<td align="right">2,003</td>
<td align="right">1.5%</td>
<td align="right">2,320</td>
<td align="right">2.1%</td>
<td align="right">15.8%</td>
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
<td align="right">5,982</td>
<td align="right">4.4%</td>
<td align="right">4,923</td>
<td align="right">4.5%</td>
<td align="right">-17.7%</td>
</tr>
<tr>
<td align="left"><= 16</td>
<td align="right">25,140</td>
<td align="right">18.7%</td>
<td align="right">20,623</td>
<td align="right">19.0%</td>
<td align="right">-18.0%</td>
</tr>
<tr>
<td align="left"><= 32</td>
<td align="right">48,188</td>
<td align="right">35.8%</td>
<td align="right">35,135</td>
<td align="right">32.3%</td>
<td align="right">-27.1%</td>
</tr>
<tr>
<td align="left"><= 64</td>
<td align="right">31,074</td>
<td align="right">23.1%</td>
<td align="right">26,696</td>
<td align="right">24.5%</td>
<td align="right">-14.1%</td>
</tr>
<tr>
<td align="left"><= 128</td>
<td align="right">17,089</td>
<td align="right">12.7%</td>
<td align="right">14,038</td>
<td align="right">12.9%</td>
<td align="right">-17.9%</td>
</tr>
<tr>
<td align="left"><= 256</td>
<td align="right">6,290</td>
<td align="right">4.7%</td>
<td align="right">5,961</td>
<td align="right">5.5%</td>
<td align="right">-5.2%</td>
</tr>
<tr>
<td align="left"><= 512</td>
<td align="right">956</td>
<td align="right">0.7%</td>
<td align="right">1,300</td>
<td align="right">1.2%</td>
<td align="right">36.0%</td>
</tr>
<tr>
<td align="left"><= 1,024</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">140</td>
<td align="right">0.1%</td>
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
<td align="right">4,552</td>
<td align="right">3.4%</td>
<td align="right">3,963</td>
<td align="right">3.6%</td>
<td align="right">-12.9%</td>
</tr>
<tr>
<td align="left"><= 8</td>
<td align="right">16,673</td>
<td align="right">12.4%</td>
<td align="right">14,269</td>
<td align="right">13.1%</td>
<td align="right">-14.4%</td>
</tr>
<tr>
<td align="left"><= 16</td>
<td align="right">35,116</td>
<td align="right">26.1%</td>
<td align="right">23,828</td>
<td align="right">21.9%</td>
<td align="right">-32.1%</td>
</tr>
<tr>
<td align="left"><= 32</td>
<td align="right">41,756</td>
<td align="right">31.0%</td>
<td align="right">34,706</td>
<td align="right">31.9%</td>
<td align="right">-16.9%</td>
</tr>
<tr>
<td align="left"><= 64</td>
<td align="right">21,759</td>
<td align="right">16.2%</td>
<td align="right">17,382</td>
<td align="right">16.0%</td>
<td align="right">-20.1%</td>
</tr>
<tr>
<td align="left"><= 128</td>
<td align="right">8,951</td>
<td align="right">6.6%</td>
<td align="right">8,188</td>
<td align="right">7.5%</td>
<td align="right">-8.5%</td>
</tr>
<tr>
<td align="left"><= 256</td>
<td align="right">2,280</td>
<td align="right">1.7%</td>
<td align="right">2,600</td>
<td align="right">2.4%</td>
<td align="right">14.0%</td>
</tr>
<tr>
<td align="left"><= 512</td>
<td align="right">141</td>
<td align="right">0.1%</td>
<td align="right">340</td>
<td align="right">0.3%</td>
<td align="right">141.1%</td>
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
<td align="right">26,058,980</td>
<td align="right">0.4%</td>
<td align="right">27,717,760</td>
<td align="right">0.4%</td>
<td align="right">6.4%</td>
</tr>
<tr>
<td align="left"><= 4</td>
<td align="right">182,246,030</td>
<td align="right">2.5%</td>
<td align="right">189,602,321</td>
<td align="right">2.7%</td>
<td align="right">4.0%</td>
</tr>
<tr>
<td align="left"><= 8</td>
<td align="right">1,086,251,986</td>
<td align="right">15.1%</td>
<td align="right">1,035,405,242</td>
<td align="right">14.8%</td>
<td align="right">-4.7%</td>
</tr>
<tr>
<td align="left"><= 16</td>
<td align="right">1,213,870,786</td>
<td align="right">16.8%</td>
<td align="right">1,071,846,758</td>
<td align="right">15.3%</td>
<td align="right">-11.7%</td>
</tr>
<tr>
<td align="left"><= 32</td>
<td align="right">1,145,354,048</td>
<td align="right">15.9%</td>
<td align="right">1,155,223,592</td>
<td align="right">16.5%</td>
<td align="right">0.9%</td>
</tr>
<tr>
<td align="left"><= 64</td>
<td align="right">665,228,699</td>
<td align="right">9.2%</td>
<td align="right">695,563,858</td>
<td align="right">9.9%</td>
<td align="right">4.6%</td>
</tr>
<tr>
<td align="left"><= 128</td>
<td align="right">282,519,749</td>
<td align="right">3.9%</td>
<td align="right">339,872,702</td>
<td align="right">4.8%</td>
<td align="right">20.3%</td>
</tr>
<tr>
<td align="left"><= 256</td>
<td align="right">167,371,463</td>
<td align="right">2.3%</td>
<td align="right">184,227,991</td>
<td align="right">2.6%</td>
<td align="right">10.1%</td>
</tr>
<tr>
<td align="left"><= 512</td>
<td align="right">21,287,796</td>
<td align="right">0.3%</td>
<td align="right">27,503,252</td>
<td align="right">0.4%</td>
<td align="right">29.2%</td>
</tr>
<tr>
<td align="left"><= 1,024</td>
<td align="right">6,946,295</td>
<td align="right">0.1%</td>
<td align="right">7,342,942</td>
<td align="right">0.1%</td>
<td align="right">5.7%</td>
</tr>
<tr>
<td align="left"><= 2,048</td>
<td align="right">19,018,001</td>
<td align="right">0.3%</td>
<td align="right">19,033,944</td>
<td align="right">0.3%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left"><= 4,096</td>
<td align="right">622,409</td>
<td align="right">0.0%</td>
<td align="right">685,816</td>
<td align="right">0.0%</td>
<td align="right">10.2%</td>
</tr>
<tr>
<td align="left"><= 8,192</td>
<td align="right">742,086</td>
<td align="right">0.0%</td>
<td align="right">740,509</td>
<td align="right">0.0%</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left"><= 16,384</td>
<td align="right">243,843</td>
<td align="right">0.0%</td>
<td align="right">246,820</td>
<td align="right">0.0%</td>
<td align="right">1.2%</td>
</tr>
<tr>
<td align="left"><= 32,768</td>
<td align="right">42,533</td>
<td align="right">0.0%</td>
<td align="right">43,740</td>
<td align="right">0.0%</td>
<td align="right">2.8%</td>
</tr>
<tr>
<td align="left"><= 65,536</td>
<td align="right">12,521</td>
<td align="right">0.0%</td>
<td align="right">13,093</td>
<td align="right">0.0%</td>
<td align="right">4.6%</td>
</tr>
<tr>
<td align="left"><= 131,072</td>
<td align="right">377</td>
<td align="right">0.0%</td>
<td align="right">1,067</td>
<td align="right">0.0%</td>
<td align="right">183.0%</td>
</tr>
<tr>
<td align="left"><= 262,144</td>
<td align="right">2,002</td>
<td align="right">0.0%</td>
<td align="right">2,000</td>
<td align="right">0.0%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left"><= 524,288</td>
<td align="right">461</td>
<td align="right">0.0%</td>
<td align="right">466</td>
<td align="right">0.0%</td>
<td align="right">1.1%</td>
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
<td align="right">221</td>
<td align="right">0.0%</td>
<td align="right">386</td>
<td align="right">0.0%</td>
<td align="right">74.7%</td>
</tr>
<tr>
<td align="left"><= 4,194,304</td>
<td align="right">259</td>
<td align="right">0.0%</td>
<td align="right">254</td>
<td align="right">0.0%</td>
<td align="right">-1.9%</td>
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
<td align="left">_UNPACK_EX</td>
<td align="right">104</td>
<td align="right">322,020</td>
<td align="right">309,534.6%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_INSTANCE_VALUE_1</td>
<td align="right">4,701,081</td>
<td align="right">22,406,640</td>
<td align="right">376.6%</td>
</tr>
<tr>
<td align="left">_STORE_GLOBAL</td>
<td align="right">1,260,560</td>
<td align="right">4,739,520</td>
<td align="right">276.0%</td>
</tr>
<tr>
<td align="left">_BUILD_STRING</td>
<td align="right">713,844</td>
<td align="right">1,952,972</td>
<td align="right">173.6%</td>
</tr>
<tr>
<td align="left">_ERROR_POP_N</td>
<td align="right">1,874,527</td>
<td align="right">4,484,188</td>
<td align="right">139.2%</td>
</tr>
<tr>
<td align="left">_FORMAT_SIMPLE</td>
<td align="right">863,012</td>
<td align="right">2,006,692</td>
<td align="right">132.5%</td>
</tr>
<tr>
<td align="left">_STORE_ATTR</td>
<td align="right">7,541,824</td>
<td align="right">16,596,460</td>
<td align="right">120.1%</td>
</tr>
<tr>
<td align="left">_SET_ADD</td>
<td align="right">1,449,189</td>
<td align="right">41,100</td>
<td align="right">-97.2%</td>
</tr>
<tr>
<td align="left">_REPLACE_WITH_TRUE</td>
<td align="right">32,951,022</td>
<td align="right">61,835,180</td>
<td align="right">87.7%</td>
</tr>
<tr>
<td align="left">_LOAD_SUPER_ATTR_METHOD</td>
<td align="right">241,101</td>
<td align="right">29,920</td>
<td align="right">-87.6%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_STR</td>
<td align="right">28,965,911</td>
<td align="right">54,264,104</td>
<td align="right">87.3%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_NONE_POP</td>
<td align="right">70,314,144</td>
<td align="right">129,529,756</td>
<td align="right">84.2%</td>
</tr>
<tr>
<td align="left">_STORE_ATTR_SLOT</td>
<td align="right">130,415,769</td>
<td align="right">229,903,199</td>
<td align="right">76.3%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_NONDESCRIPTOR_NO_DICT</td>
<td align="right">25,846,486</td>
<td align="right">45,562,433</td>
<td align="right">76.3%</td>
</tr>
<tr>
<td align="left">_STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">162,176,225</td>
<td align="right">263,640,601</td>
<td align="right">62.6%</td>
</tr>
<tr>
<td align="left">_GUARD_DORV_NO_DICT</td>
<td align="right">163,403,045</td>
<td align="right">264,867,421</td>
<td align="right">62.1%</td>
</tr>
<tr>
<td align="left">_CHECK_STACK_SPACE</td>
<td align="right">105,843,535</td>
<td align="right">168,726,631</td>
<td align="right">59.4%</td>
</tr>
<tr>
<td align="left">_CHECK_ATTR_MODULE</td>
<td align="right">7,485,339</td>
<td align="right">11,394,087</td>
<td align="right">52.2%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_MODULE</td>
<td align="right">7,485,339</td>
<td align="right">11,394,087</td>
<td align="right">52.2%</td>
</tr>
<tr>
<td align="left">_CONVERT_VALUE</td>
<td align="right">125,883</td>
<td align="right">71,420</td>
<td align="right">-43.3%</td>
</tr>
<tr>
<td align="left">_UNARY_NEGATIVE</td>
<td align="right">25,063,629</td>
<td align="right">35,337,755</td>
<td align="right">41.0%</td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">249,980,376</td>
<td align="right">336,210,692</td>
<td align="right">34.5%</td>
</tr>
<tr>
<td align="left">_CHECK_ATTR_METHOD_LAZY_DICT</td>
<td align="right">99,488,401</td>
<td align="right">133,563,248</td>
<td align="right">34.3%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_METHOD_LAZY_DICT</td>
<td align="right">99,488,401</td>
<td align="right">133,563,248</td>
<td align="right">34.3%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_SLOT_0</td>
<td align="right">748,484,677</td>
<td align="right">974,144,368</td>
<td align="right">30.1%</td>
</tr>
<tr>
<td align="left">_TO_BOOL</td>
<td align="right">264,405,092</td>
<td align="right">324,414,274</td>
<td align="right">22.7%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_2</td>
<td align="right">114,690,558</td>
<td align="right">140,074,360</td>
<td align="right">22.1%</td>
</tr>
<tr>
<td align="left">_GUARD_BOTH_INT</td>
<td align="right">563,957,882</td>
<td align="right">686,202,145</td>
<td align="right">21.7%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_AND_CLEAR</td>
<td align="right">24,387,292</td>
<td align="right">29,479,075</td>
<td align="right">20.9%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">80,131,387</td>
<td align="right">96,809,710</td>
<td align="right">20.8%</td>
</tr>
<tr>
<td align="left">_CHECK_CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">80,375,507</td>
<td align="right">97,053,830</td>
<td align="right">20.8%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_NOT_NONE_POP</td>
<td align="right">166,106,037</td>
<td align="right">199,249,784</td>
<td align="right">20.0%</td>
</tr>
<tr>
<td align="left">_POP_FRAME</td>
<td align="right">721,135,268</td>
<td align="right">862,263,764</td>
<td align="right">19.6%</td>
</tr>
<tr>
<td align="left">_GUARD_TYPE_VERSION</td>
<td align="right">5,676,385,601</td>
<td align="right">6,673,753,490</td>
<td align="right">17.6%</td>
</tr>
<tr>
<td align="left">_BUILD_MAP</td>
<td align="right">19,364,103</td>
<td align="right">22,763,487</td>
<td align="right">17.6%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_NONE</td>
<td align="right">174,102,773</td>
<td align="right">203,259,698</td>
<td align="right">16.7%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_WITH_HINT</td>
<td align="right">53,372,543</td>
<td align="right">62,254,400</td>
<td align="right">16.6%</td>
</tr>
<tr>
<td align="left">_CHECK_ATTR_WITH_HINT</td>
<td align="right">53,485,925</td>
<td align="right">62,368,300</td>
<td align="right">16.6%</td>
</tr>
<tr>
<td align="left">_CHECK_PERIODIC</td>
<td align="right">2,546,247,589</td>
<td align="right">2,958,197,996</td>
<td align="right">16.2%</td>
</tr>
<tr>
<td align="left">_IS_OP</td>
<td align="right">358,536,611</td>
<td align="right">413,960,340</td>
<td align="right">15.5%</td>
</tr>
<tr>
<td align="left">_POP_TOP_LOAD_CONST_INLINE_BORROW</td>
<td align="right">1,847,973</td>
<td align="right">2,133,180</td>
<td align="right">15.4%</td>
</tr>
<tr>
<td align="left">_LOAD_GLOBAL_MODULE</td>
<td align="right">47,810,630</td>
<td align="right">55,151,953</td>
<td align="right">15.4%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">922,302,670</td>
<td align="right">1,058,788,974</td>
<td align="right">14.8%</td>
</tr>
<tr>
<td align="left">_RESUME_CHECK</td>
<td align="right">1,445,229,336</td>
<td align="right">1,654,652,872</td>
<td align="right">14.5%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_INT</td>
<td align="right">201,179,750</td>
<td align="right">228,561,329</td>
<td align="right">13.6%</td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">200,471,190</td>
<td align="right">227,468,199</td>
<td align="right">13.5%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_0</td>
<td align="right">5,734,280,533</td>
<td align="right">6,490,136,855</td>
<td align="right">13.2%</td>
</tr>
<tr>
<td align="left">_DICT_MERGE</td>
<td align="right">8,686,907</td>
<td align="right">9,803,543</td>
<td align="right">12.9%</td>
</tr>
<tr>
<td align="left">_CALL_ISINSTANCE</td>
<td align="right">318,670,361</td>
<td align="right">278,372,746</td>
<td align="right">-12.6%</td>
</tr>
<tr>
<td align="left">_PUSH_FRAME</td>
<td align="right">1,738,471,967</td>
<td align="right">1,955,706,291</td>
<td align="right">12.5%</td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_CLASS</td>
<td align="right">66,045,973</td>
<td align="right">74,028,187</td>
<td align="right">12.1%</td>
</tr>
<tr>
<td align="left">_BINARY_SUBSCR_DICT</td>
<td align="right">368,717,455</td>
<td align="right">411,174,487</td>
<td align="right">11.5%</td>
</tr>
<tr>
<td align="left">_CALL_TYPE_1</td>
<td align="right">281,987,909</td>
<td align="right">314,307,861</td>
<td align="right">11.5%</td>
</tr>
<tr>
<td align="left">_CHECK_MANAGED_OBJECT_HAS_VALUES</td>
<td align="right">2,034,688,341</td>
<td align="right">2,264,415,626</td>
<td align="right">11.3%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_1</td>
<td align="right">515,085,299</td>
<td align="right">572,691,740</td>
<td align="right">11.2%</td>
</tr>
<tr>
<td align="left">_STORE_SUBSCR_DICT</td>
<td align="right">130,453,112</td>
<td align="right">144,414,993</td>
<td align="right">10.7%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_INSTANCE_VALUE_0</td>
<td align="right">2,028,983,240</td>
<td align="right">2,241,003,946</td>
<td align="right">10.4%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_3</td>
<td align="right">645,279,066</td>
<td align="right">710,838,762</td>
<td align="right">10.2%</td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_O</td>
<td align="right">115,341,992</td>
<td align="right">126,936,573</td>
<td align="right">10.1%</td>
</tr>
<tr>
<td align="left">_STORE_DEREF</td>
<td align="right">3,292,994</td>
<td align="right">3,610,840</td>
<td align="right">9.7%</td>
</tr>
<tr>
<td align="left">_LOAD_CONST_INLINE_BORROW_WITH_NULL</td>
<td align="right">442,426,478</td>
<td align="right">484,477,391</td>
<td align="right">9.5%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">1,043,281,604</td>
<td align="right">1,140,612,688</td>
<td align="right">9.3%</td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_O</td>
<td align="right">722,720,654</td>
<td align="right">789,400,836</td>
<td align="right">9.2%</td>
</tr>
<tr>
<td align="left">_GUARD_KEYS_VERSION</td>
<td align="right">1,136,967,127</td>
<td align="right">1,240,737,999</td>
<td align="right">9.1%</td>
</tr>
<tr>
<td align="left">_GUARD_DORV_VALUES_INST_ATTR_FROM_DICT</td>
<td align="right">1,156,179,360</td>
<td align="right">1,259,930,430</td>
<td align="right">9.0%</td>
</tr>
<tr>
<td align="left">_COPY_FREE_VARS</td>
<td align="right">80,696,917</td>
<td align="right">87,569,833</td>
<td align="right">8.5%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_6</td>
<td align="right">511,806,552</td>
<td align="right">554,075,991</td>
<td align="right">8.3%</td>
</tr>
<tr>
<td align="left">_COMPARE_OP</td>
<td align="right">106,498,032</td>
<td align="right">115,227,052</td>
<td align="right">8.2%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_ADD_UNICODE</td>
<td align="right">23,910,917</td>
<td align="right">22,046,120</td>
<td align="right">-7.8%</td>
</tr>
<tr>
<td align="left">_GUARD_GLOBALS_VERSION</td>
<td align="right">101,080,154</td>
<td align="right">108,946,633</td>
<td align="right">7.8%</td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION</td>
<td align="right">1,313,709,196</td>
<td align="right">1,414,992,607</td>
<td align="right">7.7%</td>
</tr>
<tr>
<td align="left">_POP_TOP</td>
<td align="right">1,207,750,633</td>
<td align="right">1,299,017,308</td>
<td align="right">7.6%</td>
</tr>
<tr>
<td align="left">_CHECK_VALIDITY_AND_SET_IP</td>
<td align="right">1,253,890,792</td>
<td align="right">1,345,523,737</td>
<td align="right">7.3%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right">93,315,990</td>
<td align="right">99,814,860</td>
<td align="right">7.0%</td>
</tr>
<tr>
<td align="left">_COMPARE_OP_INT</td>
<td align="right">975,147,312</td>
<td align="right">1,039,870,022</td>
<td align="right">6.6%</td>
</tr>
<tr>
<td align="left">_COLD_EXIT</td>
<td align="right">2,227,407,747</td>
<td align="right">2,079,658,744</td>
<td align="right">-6.6%</td>
</tr>
<tr>
<td align="left">_UNARY_NOT</td>
<td align="right">64,718,143</td>
<td align="right">68,913,315</td>
<td align="right">6.5%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_TRUE_POP</td>
<td align="right">2,654,696,600</td>
<td align="right">2,825,849,249</td>
<td align="right">6.4%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_6</td>
<td align="right">1,313,345,297</td>
<td align="right">1,393,350,361</td>
<td align="right">6.1%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_4</td>
<td align="right">685,423,132</td>
<td align="right">726,980,815</td>
<td align="right">6.1%</td>
</tr>
<tr>
<td align="left">_BINARY_SLICE</td>
<td align="right">114,164,108</td>
<td align="right">121,007,963</td>
<td align="right">6.0%</td>
</tr>
<tr>
<td align="left">_CHECK_VALIDITY</td>
<td align="right">11,149,400,197</td>
<td align="right">11,801,845,623</td>
<td align="right">5.9%</td>
</tr>
<tr>
<td align="left">_SET_IP</td>
<td align="right">13,122,574,893</td>
<td align="right">13,863,144,450</td>
<td align="right">5.6%</td>
</tr>
<tr>
<td align="left">_PUSH_NULL</td>
<td align="right">801,002,110</td>
<td align="right">845,823,883</td>
<td align="right">5.6%</td>
</tr>
<tr>
<td align="left">_BINARY_OP</td>
<td align="right">987,348,943</td>
<td align="right">1,042,383,084</td>
<td align="right">5.6%</td>
</tr>
<tr>
<td align="left">_SAVE_RETURN_OFFSET</td>
<td align="right">1,637,835,188</td>
<td align="right">1,726,832,325</td>
<td align="right">5.4%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_1</td>
<td align="right">6,740,236,869</td>
<td align="right">7,102,651,153</td>
<td align="right">5.4%</td>
</tr>
<tr>
<td align="left">_DELETE_SUBSCR</td>
<td align="right">96,838,610</td>
<td align="right">101,918,933</td>
<td align="right">5.2%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBTRACT_INT</td>
<td align="right">461,122,481</td>
<td align="right">484,832,589</td>
<td align="right">5.1%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_BOOL</td>
<td align="right">1,995,932,246</td>
<td align="right">2,098,226,387</td>
<td align="right">5.1%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_2</td>
<td align="right">3,048,997,879</td>
<td align="right">3,198,663,258</td>
<td align="right">4.9%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST</td>
<td align="right">6,187,313,237</td>
<td align="right">6,487,344,720</td>
<td align="right">4.8%</td>
</tr>
<tr>
<td align="left">_SWAP</td>
<td align="right">1,215,770,880</td>
<td align="right">1,273,009,906</td>
<td align="right">4.7%</td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION_EXACT_ARGS</td>
<td align="right">1,710,959,996</td>
<td align="right">1,787,834,127</td>
<td align="right">4.5%</td>
</tr>
<tr>
<td align="left">_MAKE_CELL</td>
<td align="right">5,909,754</td>
<td align="right">6,169,365</td>
<td align="right">4.4%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_5</td>
<td align="right">659,238,836</td>
<td align="right">687,887,144</td>
<td align="right">4.3%</td>
</tr>
<tr>
<td align="left">_LOAD_GLOBAL</td>
<td align="right">213,740,867</td>
<td align="right">223,010,933</td>
<td align="right">4.3%</td>
</tr>
<tr>
<td align="left">_STORE_SUBSCR_LIST_INT</td>
<td align="right">488,609,786</td>
<td align="right">509,722,160</td>
<td align="right">4.3%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_4</td>
<td align="right">2,092,426,590</td>
<td align="right">2,181,084,388</td>
<td align="right">4.2%</td>
</tr>
<tr>
<td align="left">_GUARD_NOT_EXHAUSTED_LIST</td>
<td align="right">1,369,590,873</td>
<td align="right">1,312,849,897</td>
<td align="right">-4.1%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_FALSE_POP</td>
<td align="right">5,496,048,551</td>
<td align="right">5,720,801,972</td>
<td align="right">4.1%</td>
</tr>
<tr>
<td align="left">_ITER_CHECK_LIST</td>
<td align="right">1,426,536,024</td>
<td align="right">1,369,698,337</td>
<td align="right">-4.0%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_7</td>
<td align="right">1,193,583,772</td>
<td align="right">1,239,197,389</td>
<td align="right">3.8%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_3</td>
<td align="right">3,321,514,933</td>
<td align="right">3,446,455,029</td>
<td align="right">3.8%</td>
</tr>
<tr>
<td align="left">_BUILD_SLICE</td>
<td align="right">139,795,736</td>
<td align="right">144,941,180</td>
<td align="right">3.7%</td>
</tr>
<tr>
<td align="left">_CHECK_ATTR_CLASS</td>
<td align="right">35,273,483</td>
<td align="right">34,049,380</td>
<td align="right">-3.5%</td>
</tr>
<tr>
<td align="left">_COPY</td>
<td align="right">1,322,806,007</td>
<td align="right">1,367,691,655</td>
<td align="right">3.4%</td>
</tr>
<tr>
<td align="left">_STORE_FAST</td>
<td align="right">3,198,802,896</td>
<td align="right">3,301,010,544</td>
<td align="right">3.2%</td>
</tr>
<tr>
<td align="left">_BINARY_SUBSCR_STR_INT</td>
<td align="right">1,294,552,179</td>
<td align="right">1,335,257,342</td>
<td align="right">3.1%</td>
</tr>
<tr>
<td align="left">_ITER_NEXT_TUPLE</td>
<td align="right">225,690,260</td>
<td align="right">232,690,161</td>
<td align="right">3.1%</td>
</tr>
<tr>
<td align="left">_GET_ITER</td>
<td align="right">330,149,824</td>
<td align="right">340,104,307</td>
<td align="right">3.0%</td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_FAST</td>
<td align="right">908,503,301</td>
<td align="right">935,675,799</td>
<td align="right">3.0%</td>
</tr>
<tr>
<td align="left">_CALL_LEN</td>
<td align="right">211,304,799</td>
<td align="right">217,516,513</td>
<td align="right">2.9%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_7</td>
<td align="right">3,501,788,598</td>
<td align="right">3,603,764,679</td>
<td align="right">2.9%</td>
</tr>
<tr>
<td align="left">_LOAD_CONST_INLINE_WITH_NULL</td>
<td align="right">1,815,403,793</td>
<td align="right">1,867,704,572</td>
<td align="right">2.9%</td>
</tr>
<tr>
<td align="left">_EXIT_TRACE</td>
<td align="right">2,809,463,814</td>
<td align="right">2,728,808,757</td>
<td align="right">-2.9%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_2</td>
<td align="right">737,171,348</td>
<td align="right">757,735,673</td>
<td align="right">2.8%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_CLASS_0</td>
<td align="right">13,936,580</td>
<td align="right">13,549,260</td>
<td align="right">-2.8%</td>
</tr>
<tr>
<td align="left">_ITER_NEXT_LIST</td>
<td align="right">1,131,057,630</td>
<td align="right">1,101,910,418</td>
<td align="right">-2.6%</td>
</tr>
<tr>
<td align="left">_RETURN_GENERATOR</td>
<td align="right">91,250,983</td>
<td align="right">93,531,823</td>
<td align="right">2.5%</td>
</tr>
<tr>
<td align="left">_JUMP_TO_TOP</td>
<td align="right">2,133,431,252</td>
<td align="right">2,185,820,057</td>
<td align="right">2.5%</td>
</tr>
<tr>
<td align="left">_DYNAMIC_EXIT</td>
<td align="right">169,869,856</td>
<td align="right">173,976,385</td>
<td align="right">2.4%</td>
</tr>
<tr>
<td align="left">_CALL_TUPLE_1</td>
<td align="right">8,036,397</td>
<td align="right">8,226,550</td>
<td align="right">2.4%</td>
</tr>
<tr>
<td align="left">_DEOPT</td>
<td align="right">208,934,837</td>
<td align="right">204,235,407</td>
<td align="right">-2.2%</td>
</tr>
<tr>
<td align="left">_BUILD_TUPLE</td>
<td align="right">552,774,856</td>
<td align="right">564,478,803</td>
<td align="right">2.1%</td>
</tr>
<tr>
<td align="left">_UNARY_INVERT</td>
<td align="right">12,967,827</td>
<td align="right">12,693,500</td>
<td align="right">-2.1%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_CHECK</td>
<td align="right">458,272</td>
<td align="right">448,627</td>
<td align="right">-2.1%</td>
</tr>
<tr>
<td align="left">_MAP_ADD</td>
<td align="right">33,166,318</td>
<td align="right">32,501,668</td>
<td align="right">-2.0%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_3</td>
<td align="right">62,868,985</td>
<td align="right">61,625,400</td>
<td align="right">-2.0%</td>
</tr>
<tr>
<td align="left">_FOR_ITER_TIER_TWO</td>
<td align="right">553,721,683</td>
<td align="right">542,856,653</td>
<td align="right">-2.0%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_ADD_INT</td>
<td align="right">2,596,945,710</td>
<td align="right">2,647,649,761</td>
<td align="right">2.0%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_5</td>
<td align="right">2,195,396,243</td>
<td align="right">2,237,402,134</td>
<td align="right">1.9%</td>
</tr>
<tr>
<td align="left">_BINARY_SUBSCR_TUPLE_INT</td>
<td align="right">156,912,744</td>
<td align="right">154,000,060</td>
<td align="right">-1.9%</td>
</tr>
<tr>
<td align="left">_CALL_STR_1</td>
<td align="right">65,666,161</td>
<td align="right">64,594,900</td>
<td align="right">-1.6%</td>
</tr>
<tr>
<td align="left">_LOAD_DEREF</td>
<td align="right">586,095,674</td>
<td align="right">595,483,830</td>
<td align="right">1.6%</td>
</tr>
<tr>
<td align="left">_UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">610,589,936</td>
<td align="right">620,053,679</td>
<td align="right">1.5%</td>
</tr>
<tr>
<td align="left">_TIER2_RESUME_CHECK</td>
<td align="right">4,788,500,978</td>
<td align="right">4,717,403,836</td>
<td align="right">-1.5%</td>
</tr>
<tr>
<td align="left">_LOAD_CONST_INLINE_BORROW</td>
<td align="right">9,463,965,468</td>
<td align="right">9,603,156,186</td>
<td align="right">1.5%</td>
</tr>
<tr>
<td align="left">_SIDE_EXIT</td>
<td align="right">4,607,011,821</td>
<td align="right">4,546,355,558</td>
<td align="right">-1.3%</td>
</tr>
<tr>
<td align="left">_BINARY_SUBSCR_LIST_INT</td>
<td align="right">1,100,114,200</td>
<td align="right">1,114,479,484</td>
<td align="right">1.3%</td>
</tr>
<tr>
<td align="left">_CALL_INTRINSIC_1</td>
<td align="right">97,579,341</td>
<td align="right">98,843,448</td>
<td align="right">1.3%</td>
</tr>
<tr>
<td align="left">_LIST_EXTEND</td>
<td align="right">98,537,981</td>
<td align="right">99,802,088</td>
<td align="right">1.3%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_MULTIPLY_INT</td>
<td align="right">186,151,823</td>
<td align="right">188,411,676</td>
<td align="right">1.2%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_0</td>
<td align="right">406,320,971</td>
<td align="right">411,172,223</td>
<td align="right">1.2%</td>
</tr>
<tr>
<td align="left">_START_EXECUTOR</td>
<td align="right">4,987,691,041</td>
<td align="right">4,929,051,538</td>
<td align="right">-1.2%</td>
</tr>
<tr>
<td align="left">_GUARD_BUILTINS_VERSION</td>
<td align="right">45,823,824</td>
<td align="right">46,348,980</td>
<td align="right">1.1%</td>
</tr>
<tr>
<td align="left">_FOR_ITER_GEN_FRAME</td>
<td align="right">100,741,399</td>
<td align="right">99,637,590</td>
<td align="right">-1.1%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_LIST</td>
<td align="right">58,074,781</td>
<td align="right">58,654,390</td>
<td align="right">1.0%</td>
</tr>
<tr>
<td align="left">_LOAD_GLOBAL_BUILTINS</td>
<td align="right">53,269,524</td>
<td align="right">53,794,680</td>
<td align="right">1.0%</td>
</tr>
<tr>
<td align="left">_ITER_CHECK_TUPLE</td>
<td align="right">407,578,766</td>
<td align="right">403,743,818</td>
<td align="right">-0.9%</td>
</tr>
<tr>
<td align="left">_CHECK_STACK_SPACE_OPERAND</td>
<td align="right">940,551,797</td>
<td align="right">948,179,225</td>
<td align="right">0.8%</td>
</tr>
<tr>
<td align="left">_BUILD_LIST</td>
<td align="right">243,516,824</td>
<td align="right">245,415,442</td>
<td align="right">0.8%</td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_FAST_WITH_KEYWORDS</td>
<td align="right">148,537,940</td>
<td align="right">149,628,465</td>
<td align="right">0.7%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_1</td>
<td align="right">1,959,060,031</td>
<td align="right">1,972,698,746</td>
<td align="right">0.7%</td>
</tr>
<tr>
<td align="left">_GUARD_NOT_EXHAUSTED_TUPLE</td>
<td align="right">365,934,193</td>
<td align="right">363,699,258</td>
<td align="right">-0.6%</td>
</tr>
<tr>
<td align="left">_GET_AWAITABLE</td>
<td align="right">647,418</td>
<td align="right">651,232</td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">_GUARD_NOS_INT</td>
<td align="right">2,526,161,182</td>
<td align="right">2,539,551,872</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">_LIST_APPEND</td>
<td align="right">172,855,267</td>
<td align="right">172,031,937</td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">_LOAD_CONST_INLINE</td>
<td align="right">1,536,518,483</td>
<td align="right">1,543,808,071</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_4</td>
<td align="right">528,779,204</td>
<td align="right">531,150,840</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBTRACT_FLOAT</td>
<td align="right">383,035,460</td>
<td align="right">384,673,795</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">_GUARD_TOS_INT</td>
<td align="right">211,504,219</td>
<td align="right">212,390,614</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">_GUARD_BOTH_UNICODE</td>
<td align="right">964,436,696</td>
<td align="right">960,493,704</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_0</td>
<td align="right">200,194,940</td>
<td align="right">199,420,340</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">_BINARY_SUBSCR</td>
<td align="right">1,334,545,142</td>
<td align="right">1,339,137,151</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">_GUARD_NOT_EXHAUSTED_RANGE</td>
<td align="right">784,816,559</td>
<td align="right">782,383,580</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">_ITER_CHECK_RANGE</td>
<td align="right">785,353,879</td>
<td align="right">782,920,900</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">_BUILD_CONST_KEY_MAP</td>
<td align="right">4,837,300</td>
<td align="right">4,823,420</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS</td>
<td align="right">10,090,171</td>
<td align="right">10,117,762</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">_CONTAINS_OP_DICT</td>
<td align="right">332,019,477</td>
<td align="right">331,193,785</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">_STORE_SUBSCR</td>
<td align="right">381,490,198</td>
<td align="right">382,387,916</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">_UNPACK_SEQUENCE_TUPLE</td>
<td align="right">225,523,816</td>
<td align="right">226,004,301</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">_GET_YIELD_FROM_ITER</td>
<td align="right">822,821</td>
<td align="right">821,160</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">_UNPACK_SEQUENCE</td>
<td align="right">1,555,174</td>
<td align="right">1,552,126</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR</td>
<td align="right">1,006,541,552</td>
<td align="right">1,008,467,398</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">_COMPARE_OP_STR</td>
<td align="right">1,824,591,011</td>
<td align="right">1,821,100,234</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_FAST_WITH_KEYWORDS</td>
<td align="right">92,268,292</td>
<td align="right">92,091,902</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">_GUARD_BOTH_FLOAT</td>
<td align="right">908,068,547</td>
<td align="right">909,800,016</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">_CONTAINS_OP_SET</td>
<td align="right">1,656,674,097</td>
<td align="right">1,653,919,045</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">_ITER_NEXT_RANGE</td>
<td align="right">737,095,163</td>
<td align="right">736,190,853</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">_UNPACK_SEQUENCE_LIST</td>
<td align="right">81,488,884</td>
<td align="right">81,397,700</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">_SET_FUNCTION_ATTRIBUTE</td>
<td align="right">78,513,190</td>
<td align="right">78,425,626</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">_MAKE_FUNCTION</td>
<td align="right">93,530,068</td>
<td align="right">93,632,741</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">_CONTAINS_OP</td>
<td align="right">133,900,126</td>
<td align="right">134,032,974</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">_STORE_SLICE</td>
<td align="right">149,962,696</td>
<td align="right">149,868,340</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">_COMPARE_OP_FLOAT</td>
<td align="right">101,262,414</td>
<td align="right">101,293,295</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_SLOT_1</td>
<td align="right">2,865,975</td>
<td align="right">2,865,500</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_MULTIPLY_FLOAT</td>
<td align="right">1,144,480,435</td>
<td align="right">1,144,566,498</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_STORE_NAME</td>
<td align="right">543,659</td>
<td align="right">543,680</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_ADD_FLOAT</td>
<td align="right">588,453,700</td>
<td align="right">588,466,000</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_GUARD_NOS_FLOAT</td>
<td align="right">645,081,736</td>
<td align="right">645,091,096</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_CLASS_1</td>
<td align="right">20,499,134</td>
<td align="right">20,499,060</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">_GET_ANEXT</td>
<td align="right">125,514,720</td>
<td align="right">125,514,720</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_GUARD_TOS_FLOAT</td>
<td align="right">64,886,820</td>
<td align="right">64,886,820</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_DELETE_ATTR</td>
<td align="right">2,009,931</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_POP_EXCEPT</td>
<td align="right">7,620</td>
<td align="right">7,620</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_CHECK_IS_NOT_PY_CALLABLE</td>
<td align="right"></td>
<td align="right">186,757,918</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_NON_PY_GENERAL</td>
<td align="right"></td>
<td align="right">184,418,490</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_PY_GENERAL</td>
<td align="right"></td>
<td align="right">129,340,996</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION_VERSION</td>
<td align="right"></td>
<td align="right">128,218,356</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_CONST</td>
<td align="right"></td>
<td align="right">110,561,497</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_PEP_523</td>
<td align="right"></td>
<td align="right">108,129,923</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_METHOD_VERSION</td>
<td align="right"></td>
<td align="right">5,776,780</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_EXPAND_METHOD</td>
<td align="right"></td>
<td align="right">5,635,720</td>
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
<td align="left">RAISE_VARARGS</td>
<td align="right">63</td>
<td align="right">540</td>
<td align="right">757.1%</td>
</tr>
<tr>
<td align="left">BEFORE_WITH</td>
<td align="right">400</td>
<td align="right">1,767</td>
<td align="right">341.8%</td>
</tr>
<tr>
<td align="left">IMPORT_NAME</td>
<td align="right">989</td>
<td align="right">2,579</td>
<td align="right">160.8%</td>
</tr>
<tr>
<td align="left">BUILD_SET</td>
<td align="right">1,272</td>
<td align="right">400</td>
<td align="right">-68.6%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">184,460</td>
<td align="right">83,040</td>
<td align="right">-55.0%</td>
</tr>
<tr>
<td align="left">CALL_ALLOC_AND_ENTER_INIT</td>
<td align="right">1,484</td>
<td align="right">880</td>
<td align="right">-40.7%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_WITH_HINT</td>
<td align="right">220</td>
<td align="right">260</td>
<td align="right">18.2%</td>
</tr>
<tr>
<td align="left">CALL_LIST_APPEND</td>
<td align="right">6,366</td>
<td align="right">5,515</td>
<td align="right">-13.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_PROPERTY</td>
<td align="right">7,724</td>
<td align="right">6,761</td>
<td align="right">-12.5%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_GETITEM</td>
<td align="right">2,173</td>
<td align="right">2,340</td>
<td align="right">7.7%</td>
</tr>
<tr>
<td align="left">BINARY_OP_INPLACE_ADD_UNICODE</td>
<td align="right">469</td>
<td align="right">440</td>
<td align="right">-6.2%</td>
</tr>
<tr>
<td align="left">CALL_FUNCTION_EX</td>
<td align="right">39,436</td>
<td align="right">41,741</td>
<td align="right">5.8%</td>
</tr>
<tr>
<td align="left">SEND_GEN</td>
<td align="right">1,360</td>
<td align="right">1,380</td>
<td align="right">1.5%</td>
</tr>
<tr>
<td align="left">CALL_KW</td>
<td align="right">30,352</td>
<td align="right">30,170</td>
<td align="right">-0.6%</td>
</tr>
<tr>
<td align="left">LOAD_NAME</td>
<td align="right">1,664</td>
<td align="right">1,660</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">SEND</td>
<td align="right">32,233</td>
<td align="right">32,248</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_PY_WITH_DEFAULTS</td>
<td align="right">5,831</td>
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
<td align="right">240</td>
<td align="right">-14.6%</td>
</tr>
<tr>
<td align="left">
func modification
<details>
<summary>ⓘ</summary>

Modifying a function, e.g. `func.__defaults__ = ...`, etc.
</details>
</td>
<td align="right">442</td>
<td align="right">400</td>
<td align="right">-9.5%</td>
</tr>
<tr>
<td align="left">
watched dict modification
<details>
<summary>ⓘ</summary>

A watched dict has been modified
</details>
</td>
<td align="right">1,082</td>
<td align="right">1,080</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">
watched globals modification
<details>
<summary>ⓘ</summary>

A watched `globals()` dict has been modified
</details>
</td>
<td align="right">1,082</td>
<td align="right">1,080</td>
<td align="right">-0.2%</td>
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
<td align="right">1,981</td>
<td align="right">1,960</td>
<td align="right">-1.1%</td>
</tr>
</tbody>
</table>


</details>

---
Stats gathered on: 2024-05-03
