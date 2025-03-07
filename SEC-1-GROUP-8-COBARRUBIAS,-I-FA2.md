1.  An experiment consists of tossing two fair coins. Use R to simulate
    this experiment 100 times and obtain the relative frequency of each
    possible outcome. Hence, estimate the probability of getting one
    head and one tail in any order.

<!-- -->

    toss <- replicate(100, sample(c(1, 0), size = 2, replace = TRUE))
    toss

    ##      [,1] [,2] [,3] [,4] [,5] [,6] [,7] [,8] [,9] [,10] [,11] [,12] [,13] [,14]
    ## [1,]    1    0    1    1    1    0    0    1    1     0     0     0     0     0
    ## [2,]    0    1    0    1    0    1    1    0    1     0     0     1     0     0
    ##      [,15] [,16] [,17] [,18] [,19] [,20] [,21] [,22] [,23] [,24] [,25] [,26]
    ## [1,]     1     0     0     1     1     0     1     0     0     0     1     1
    ## [2,]     0     0     0     0     1     1     0     0     0     1     1     1
    ##      [,27] [,28] [,29] [,30] [,31] [,32] [,33] [,34] [,35] [,36] [,37] [,38]
    ## [1,]     1     1     0     1     0     1     0     1     1     0     1     1
    ## [2,]     0     1     0     0     1     0     0     1     1     0     0     0
    ##      [,39] [,40] [,41] [,42] [,43] [,44] [,45] [,46] [,47] [,48] [,49] [,50]
    ## [1,]     1     0     0     0     1     0     1     1     1     1     0     1
    ## [2,]     1     1     0     0     0     1     1     1     0     0     0     1
    ##      [,51] [,52] [,53] [,54] [,55] [,56] [,57] [,58] [,59] [,60] [,61] [,62]
    ## [1,]     0     0     0     1     0     1     0     0     1     1     0     1
    ## [2,]     0     1     0     1     1     1     0     0     1     0     1     1
    ##      [,63] [,64] [,65] [,66] [,67] [,68] [,69] [,70] [,71] [,72] [,73] [,74]
    ## [1,]     0     1     1     1     1     0     1     1     1     0     1     0
    ## [2,]     1     0     0     0     1     0     1     1     1     1     0     0
    ##      [,75] [,76] [,77] [,78] [,79] [,80] [,81] [,82] [,83] [,84] [,85] [,86]
    ## [1,]     1     1     0     0     0     1     1     1     0     1     1     0
    ## [2,]     0     1     1     1     0     0     1     1     0     0     1     0
    ##      [,87] [,88] [,89] [,90] [,91] [,92] [,93] [,94] [,95] [,96] [,97] [,98]
    ## [1,]     1     1     1     1     0     0     1     0     1     0     1     1
    ## [2,]     0     0     0     0     0     1     1     0     0     1     1     1
    ##      [,99] [,100]
    ## [1,]     1      1
    ## [2,]     0      0

Results of the tosses The experiment assigns heads as 1 and tails as 0.

    x <- sum((toss[1, ] == 1 & toss[2, ] == 0) | (toss[1, ] == 0 & toss[2, ] == 1))
    x/100

    ## [1] 0.48

Experimental probability of 1 heads and 1 tails calculated from the
simulated 100 tosses. Out of the 100 tosses, 51% yielded a result of
having exactly 1 heads and 1 tails in any order.

1.  An experiment consists of rolling a die. Use R to simulate this
    experiment 600 times and obtain the relative frequency of each
    possible outcome. Hence, estimate the probability of getting each of
    1, 2, 3, 4, 5, and 6.

<!-- -->

    dice <- replicate(600, sample(c(1, 2, 3, 4, 5, 6), size = 2, replace = TRUE))
    dice

    ##      [,1] [,2] [,3] [,4] [,5] [,6] [,7] [,8] [,9] [,10] [,11] [,12] [,13] [,14]
    ## [1,]    2    6    3    6    4    6    1    1    6     3     5     1     6     5
    ## [2,]    2    1    1    2    3    5    3    1    2     3     6     6     1     2
    ##      [,15] [,16] [,17] [,18] [,19] [,20] [,21] [,22] [,23] [,24] [,25] [,26]
    ## [1,]     6     4     3     6     4     6     6     2     2     4     1     2
    ## [2,]     1     1     3     1     5     6     1     5     2     6     4     6
    ##      [,27] [,28] [,29] [,30] [,31] [,32] [,33] [,34] [,35] [,36] [,37] [,38]
    ## [1,]     5     1     3     1     1     6     5     3     1     4     6     4
    ## [2,]     1     3     4     6     6     3     3     4     2     2     3     3
    ##      [,39] [,40] [,41] [,42] [,43] [,44] [,45] [,46] [,47] [,48] [,49] [,50]
    ## [1,]     3     2     4     2     6     2     2     2     6     6     3     3
    ## [2,]     6     2     6     3     5     5     3     6     6     1     5     1
    ##      [,51] [,52] [,53] [,54] [,55] [,56] [,57] [,58] [,59] [,60] [,61] [,62]
    ## [1,]     5     2     1     3     5     4     1     2     3     3     6     4
    ## [2,]     6     2     2     6     6     5     6     4     2     1     2     2
    ##      [,63] [,64] [,65] [,66] [,67] [,68] [,69] [,70] [,71] [,72] [,73] [,74]
    ## [1,]     6     3     1     6     1     1     3     6     1     4     4     4
    ## [2,]     3     5     6     5     6     5     6     2     4     2     1     3
    ##      [,75] [,76] [,77] [,78] [,79] [,80] [,81] [,82] [,83] [,84] [,85] [,86]
    ## [1,]     4     6     3     3     4     3     2     5     4     6     6     1
    ## [2,]     2     1     6     4     4     1     2     5     3     3     2     6
    ##      [,87] [,88] [,89] [,90] [,91] [,92] [,93] [,94] [,95] [,96] [,97] [,98]
    ## [1,]     4     6     6     5     6     5     1     1     6     2     5     1
    ## [2,]     1     4     4     1     6     6     3     6     5     2     2     5
    ##      [,99] [,100] [,101] [,102] [,103] [,104] [,105] [,106] [,107] [,108]
    ## [1,]     2      3      6      5      3      5      1      4      3      2
    ## [2,]     3      1      4      4      6      6      4      3      3      3
    ##      [,109] [,110] [,111] [,112] [,113] [,114] [,115] [,116] [,117] [,118]
    ## [1,]      3      5      2      4      2      6      1      5      4      5
    ## [2,]      1      5      3      6      5      3      6      1      6      1
    ##      [,119] [,120] [,121] [,122] [,123] [,124] [,125] [,126] [,127] [,128]
    ## [1,]      4      3      2      3      3      4      2      6      5      5
    ## [2,]      4      3      6      1      4      1      6      2      3      2
    ##      [,129] [,130] [,131] [,132] [,133] [,134] [,135] [,136] [,137] [,138]
    ## [1,]      5      4      4      1      4      6      2      1      3      6
    ## [2,]      6      4      2      6      5      5      1      4      6      6
    ##      [,139] [,140] [,141] [,142] [,143] [,144] [,145] [,146] [,147] [,148]
    ## [1,]      5      6      4      6      3      3      6      5      2      1
    ## [2,]      6      4      1      3      1      2      3      5      4      1
    ##      [,149] [,150] [,151] [,152] [,153] [,154] [,155] [,156] [,157] [,158]
    ## [1,]      4      4      3      3      3      3      4      3      6      2
    ## [2,]      6      2      4      1      6      3      6      3      2      6
    ##      [,159] [,160] [,161] [,162] [,163] [,164] [,165] [,166] [,167] [,168]
    ## [1,]      6      2      5      4      1      1      2      2      4      5
    ## [2,]      5      4      4      1      1      4      5      5      6      6
    ##      [,169] [,170] [,171] [,172] [,173] [,174] [,175] [,176] [,177] [,178]
    ## [1,]      4      4      3      6      6      2      1      4      1      4
    ## [2,]      3      3      6      3      6      2      2      5      4      5
    ##      [,179] [,180] [,181] [,182] [,183] [,184] [,185] [,186] [,187] [,188]
    ## [1,]      3      6      2      3      2      1      4      5      6      2
    ## [2,]      1      1      6      3      6      6      6      5      1      3
    ##      [,189] [,190] [,191] [,192] [,193] [,194] [,195] [,196] [,197] [,198]
    ## [1,]      5      4      5      3      6      1      2      4      2      6
    ## [2,]      1      1      5      4      3      1      1      1      6      5
    ##      [,199] [,200] [,201] [,202] [,203] [,204] [,205] [,206] [,207] [,208]
    ## [1,]      5      1      6      4      3      5      3      1      5      4
    ## [2,]      4      5      4      4      6      5      3      2      6      5
    ##      [,209] [,210] [,211] [,212] [,213] [,214] [,215] [,216] [,217] [,218]
    ## [1,]      2      2      4      2      6      3      6      3      5      2
    ## [2,]      2      6      4      1      6      5      4      2      2      4
    ##      [,219] [,220] [,221] [,222] [,223] [,224] [,225] [,226] [,227] [,228]
    ## [1,]      1      4      5      1      6      1      5      3      3      5
    ## [2,]      2      4      6      2      2      6      6      6      2      2
    ##      [,229] [,230] [,231] [,232] [,233] [,234] [,235] [,236] [,237] [,238]
    ## [1,]      3      3      2      5      5      1      5      5      4      5
    ## [2,]      2      1      3      6      4      2      3      3      1      2
    ##      [,239] [,240] [,241] [,242] [,243] [,244] [,245] [,246] [,247] [,248]
    ## [1,]      1      4      3      2      2      3      4      3      1      4
    ## [2,]      2      4      4      2      1      1      5      3      6      5
    ##      [,249] [,250] [,251] [,252] [,253] [,254] [,255] [,256] [,257] [,258]
    ## [1,]      1      2      2      3      3      6      6      5      5      6
    ## [2,]      3      3      4      4      3      6      2      3      2      4
    ##      [,259] [,260] [,261] [,262] [,263] [,264] [,265] [,266] [,267] [,268]
    ## [1,]      4      6      5      3      6      1      3      6      6      2
    ## [2,]      6      3      4      5      2      1      1      6      3      3
    ##      [,269] [,270] [,271] [,272] [,273] [,274] [,275] [,276] [,277] [,278]
    ## [1,]      2      3      5      3      4      5      6      2      5      3
    ## [2,]      4      2      2      3      6      5      5      3      3      6
    ##      [,279] [,280] [,281] [,282] [,283] [,284] [,285] [,286] [,287] [,288]
    ## [1,]      3      4      6      6      3      2      6      6      6      5
    ## [2,]      3      3      6      2      5      6      1      3      5      2
    ##      [,289] [,290] [,291] [,292] [,293] [,294] [,295] [,296] [,297] [,298]
    ## [1,]      4      2      4      2      6      4      1      1      5      6
    ## [2,]      1      6      1      3      4      3      4      4      6      1
    ##      [,299] [,300] [,301] [,302] [,303] [,304] [,305] [,306] [,307] [,308]
    ## [1,]      1      5      1      4      6      6      2      3      5      4
    ## [2,]      1      3      3      1      3      5      5      1      4      4
    ##      [,309] [,310] [,311] [,312] [,313] [,314] [,315] [,316] [,317] [,318]
    ## [1,]      2      3      1      4      5      6      5      3      2      6
    ## [2,]      4      4      2      2      5      2      4      4      5      3
    ##      [,319] [,320] [,321] [,322] [,323] [,324] [,325] [,326] [,327] [,328]
    ## [1,]      5      5      2      6      3      1      4      3      4      4
    ## [2,]      1      1      4      5      6      3      1      4      6      3
    ##      [,329] [,330] [,331] [,332] [,333] [,334] [,335] [,336] [,337] [,338]
    ## [1,]      3      1      1      1      1      2      6      1      6      2
    ## [2,]      2      5      5      5      6      1      2      5      2      5
    ##      [,339] [,340] [,341] [,342] [,343] [,344] [,345] [,346] [,347] [,348]
    ## [1,]      1      6      6      4      2      3      2      6      1      5
    ## [2,]      4      2      3      2      1      1      5      6      1      6
    ##      [,349] [,350] [,351] [,352] [,353] [,354] [,355] [,356] [,357] [,358]
    ## [1,]      3      2      6      1      1      3      2      2      4      3
    ## [2,]      2      1      6      6      3      1      6      1      4      4
    ##      [,359] [,360] [,361] [,362] [,363] [,364] [,365] [,366] [,367] [,368]
    ## [1,]      2      3      6      3      1      4      3      6      5      3
    ## [2,]      5      5      3      1      1      3      4      3      2      6
    ##      [,369] [,370] [,371] [,372] [,373] [,374] [,375] [,376] [,377] [,378]
    ## [1,]      5      5      3      3      6      3      4      3      1      4
    ## [2,]      6      6      3      2      4      4      3      5      2      4
    ##      [,379] [,380] [,381] [,382] [,383] [,384] [,385] [,386] [,387] [,388]
    ## [1,]      2      6      1      6      6      3      6      2      6      1
    ## [2,]      6      3      6      4      2      3      3      2      6      6
    ##      [,389] [,390] [,391] [,392] [,393] [,394] [,395] [,396] [,397] [,398]
    ## [1,]      6      3      5      4      2      1      1      5      5      2
    ## [2,]      3      6      1      3      1      4      6      4      2      4
    ##      [,399] [,400] [,401] [,402] [,403] [,404] [,405] [,406] [,407] [,408]
    ## [1,]      4      5      3      1      2      3      6      2      6      1
    ## [2,]      2      6      3      6      2      6      4      4      6      5
    ##      [,409] [,410] [,411] [,412] [,413] [,414] [,415] [,416] [,417] [,418]
    ## [1,]      6      5      5      2      2      1      6      6      6      3
    ## [2,]      6      5      3      4      2      5      3      5      4      2
    ##      [,419] [,420] [,421] [,422] [,423] [,424] [,425] [,426] [,427] [,428]
    ## [1,]      6      2      2      5      2      6      5      4      3      6
    ## [2,]      5      4      2      4      1      3      3      5      4      3
    ##      [,429] [,430] [,431] [,432] [,433] [,434] [,435] [,436] [,437] [,438]
    ## [1,]      5      1      2      1      2      4      5      5      1      1
    ## [2,]      3      6      1      1      2      3      3      2      2      1
    ##      [,439] [,440] [,441] [,442] [,443] [,444] [,445] [,446] [,447] [,448]
    ## [1,]      2      4      4      4      4      3      3      5      5      1
    ## [2,]      4      5      5      3      6      4      3      6      6      3
    ##      [,449] [,450] [,451] [,452] [,453] [,454] [,455] [,456] [,457] [,458]
    ## [1,]      6      4      4      2      3      6      5      3      2      3
    ## [2,]      4      4      4      2      3      4      3      3      6      3
    ##      [,459] [,460] [,461] [,462] [,463] [,464] [,465] [,466] [,467] [,468]
    ## [1,]      5      4      6      2      2      5      1      6      6      5
    ## [2,]      6      3      1      3      5      3      1      2      4      5
    ##      [,469] [,470] [,471] [,472] [,473] [,474] [,475] [,476] [,477] [,478]
    ## [1,]      6      2      1      2      2      4      5      4      4      2
    ## [2,]      6      1      5      2      5      2      2      4      5      2
    ##      [,479] [,480] [,481] [,482] [,483] [,484] [,485] [,486] [,487] [,488]
    ## [1,]      4      5      6      1      6      1      3      6      4      4
    ## [2,]      3      5      4      6      1      1      1      3      5      4
    ##      [,489] [,490] [,491] [,492] [,493] [,494] [,495] [,496] [,497] [,498]
    ## [1,]      3      2      4      4      1      1      3      4      1      2
    ## [2,]      4      3      1      4      3      6      3      3      5      2
    ##      [,499] [,500] [,501] [,502] [,503] [,504] [,505] [,506] [,507] [,508]
    ## [1,]      2      4      4      4      6      5      5      5      5      5
    ## [2,]      2      2      4      2      5      5      6      5      1      2
    ##      [,509] [,510] [,511] [,512] [,513] [,514] [,515] [,516] [,517] [,518]
    ## [1,]      3      3      5      4      2      1      4      6      2      3
    ## [2,]      3      2      2      2      2      2      4      2      4      3
    ##      [,519] [,520] [,521] [,522] [,523] [,524] [,525] [,526] [,527] [,528]
    ## [1,]      6      6      2      3      6      3      4      5      5      6
    ## [2,]      3      4      6      5      3      3      2      1      6      1
    ##      [,529] [,530] [,531] [,532] [,533] [,534] [,535] [,536] [,537] [,538]
    ## [1,]      5      4      4      4      4      5      4      3      6      1
    ## [2,]      2      1      2      4      2      5      3      2      1      5
    ##      [,539] [,540] [,541] [,542] [,543] [,544] [,545] [,546] [,547] [,548]
    ## [1,]      1      4      6      6      2      1      5      2      3      5
    ## [2,]      4      1      3      6      5      2      3      5      1      1
    ##      [,549] [,550] [,551] [,552] [,553] [,554] [,555] [,556] [,557] [,558]
    ## [1,]      1      6      5      2      3      2      4      1      6      1
    ## [2,]      6      2      1      4      2      5      1      6      1      5
    ##      [,559] [,560] [,561] [,562] [,563] [,564] [,565] [,566] [,567] [,568]
    ## [1,]      5      3      3      6      2      5      6      2      2      3
    ## [2,]      4      2      2      1      4      5      3      3      4      3
    ##      [,569] [,570] [,571] [,572] [,573] [,574] [,575] [,576] [,577] [,578]
    ## [1,]      1      6      3      3      2      3      5      2      1      6
    ## [2,]      3      1      3      3      4      5      3      2      6      4
    ##      [,579] [,580] [,581] [,582] [,583] [,584] [,585] [,586] [,587] [,588]
    ## [1,]      2      4      4      2      4      5      6      4      2      2
    ## [2,]      6      3      4      2      5      4      6      5      1      5
    ##      [,589] [,590] [,591] [,592] [,593] [,594] [,595] [,596] [,597] [,598]
    ## [1,]      6      2      5      5      3      4      6      6      1      5
    ## [2,]      2      2      1      5      3      4      4      5      3      1
    ##      [,599] [,600]
    ## [1,]      3      4
    ## [2,]      4      2

Results of the 600 dice rolls

    probresult_1 <- sum(dice[1,] == 1)/600
    probresult_2 <- sum(dice[1,] == 2)/600
    probresult_3 <- sum(dice[1,] == 3)/600
    probresult_4 <- sum(dice[1,] == 4)/600
    probresult_5 <- sum(dice[1,] == 5)/600
    probresult_6 <- sum(dice[1,] == 6)/600

    probresult_1

    ## [1] 0.1416667

    probresult_2

    ## [1] 0.1666667

    probresult_3

    ## [1] 0.1716667

    probresult_4

    ## [1] 0.1683333

    probresult_5

    ## [1] 0.1566667

    probresult_6

    ## [1] 0.195

Calculated experimental probability of all the possible outcomes. The
expected value was ~0.1667
