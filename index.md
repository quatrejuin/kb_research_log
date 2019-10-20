
- 2019-10-17
  - Train and test TransE and DistMult with Type Constraint
    - Result
  
      | Model    | MRR      | MR        | hit@10   |
      | -------- | -------- | --------- | -------- |
      | TransE   | 0.276643 | 94.304749 | 0.463378 |
      | DistMult | 0.302933 | 73.647980 | 0.499145 |
    - hd#2,3 TransE
      ```log
        metric: MRR MR hit@10 hit@3 hit@1
        l(raw): 0.042457 1232.688965 0.117072 0.036206 0.004446
        r(raw): 0.086375 424.292572 0.256718 0.095866 0.004446
        averaged(raw): 0.064416 828.490784 0.186895 0.066036 0.004446

        l(filter): 0.074815 852.634521 0.211522 0.090736 0.004446
        r(filter): 0.186090 394.911987 0.370908 0.205023 0.097821
        averaged(filter): 0.130453 623.773254 0.291215 0.147879 0.051134
        type constraint results:
        metric: MRR MR hit@10 hit@3 hit@1
        l(raw): 0.097070 312.879547 0.218851 0.092104 0.040506
        r(raw): 0.248925 79.947281 0.437946 0.260432 0.159826
        averaged(raw): 0.172998 196.413422 0.328398 0.176268 0.100166

        l(filter): 0.215429 122.863380 0.381120 0.228086 0.135298
        r(filter): 0.337856 65.746117 0.545637 0.369198 0.237125
        averaged(filter): 0.276643 94.304749 0.463378 0.298642 0.186211
      ```
    - hd#4,5 DistMult
      ```log
      no type constraint results:
      metric: MRR MR hit@10 hit@3 hit@1
      l(raw): 0.042414 1696.429810 0.098309 0.033812 0.013877
      r(raw): 0.057320 2223.440186 0.126063 0.051207 0.023356
      averaged(raw): 0.049867 1959.935059 0.112186 0.042510 0.018616

      l(filter): 0.132650 1301.728882 0.240692 0.142969 0.080231
      r(filter): 0.146626 2190.695312 0.250122 0.159533 0.095133
      averaged(filter): 0.139638 1746.212158 0.245407 0.151251 0.087682
      type constraint results:
      metric: MRR MR hit@10 hit@3 hit@1
      l(raw): 0.097769 291.067322 0.232825 0.095085 0.036255
      r(raw): 0.218119 69.893234 0.409069 0.228134 0.126942
      averaged(raw): 0.157944 180.480286 0.320947 0.161610 0.081599

      l(filter): 0.262460 93.742744 0.444444 0.281980 0.173996
      r(filter): 0.343407 53.553211 0.553845 0.376380 0.238347
      averaged(filter): 0.302933 73.647980 0.499145 0.329180 0.206171
      ```



- 2019-10-12

  - test version 5 on epoch 666 of version 68, hd#335
    - result
      - no type constraint results:
      - metric: MRR MR hit@10 hit@3 hit@1
      - l(raw): 0.029710 1263.511841 0.072413 0.018519 0.004788
      - r(raw): 0.079407 488.204010 0.193883 0.070019 0.022965
      - averaged(raw): 0.054559 875.857910 0.133148 0.044269 0.013877
      - 
      - l(filter): 0.049523 869.156921 0.117268 0.041679 0.012264
      - r(filter): 0.111769 455.589325 0.275530 0.109352 0.039578
      - averaged(filter): 0.080646 662.373108 0.196399 0.075515 0.025921
      - type constraint results:
      - metric: MRR MR hit@10 hit@3 hit@1
      - l(raw): 0.098260 305.326019 0.225838 0.096941 0.040066
      - r(raw): 0.272824 76.951233 0.467409 0.292876 0.181276
      - averaged(raw): 0.185542 191.138626 0.346624 0.194909 0.110671
      - 
      - l(filter): 0.242131 108.164177 0.412880 0.262533 0.157774
      - r(filter): 0.416580 60.661144 0.599531 0.455145 0.323512
      - averaged(filter): 0.329356 84.412659 0.506205 0.358839 0.240643

- 2019-10-11

  - Version 68 folks version 67, change alpha from 0.8 to 0.9, (hd#327,#328), Ends at Epoch: 666, loss: 4698.188301563263,
  - version 69 folks version 66, train on adam 0.001 (hd#329,#330),Ends at Epoch: 151, loss: 9055.616076946259,
  - test version 2, test on epoch 263 of version 66, hd#332,
    - no type constraint results:
    - metric: MRR MR hit@10 hit@3 hit@1
    - l(raw): 0.021713 1208.497437 0.053015 0.005521 0.000489
    - r(raw): 0.051533 508.821014 0.148832 0.023454 0.003420
    - averaged(raw): 0.036623 858.659241 0.100923 0.014487 0.001954
    - 
    - l(filter): 0.037891 816.116211 0.101485 0.020375 0.004056
    - r(filter): 0.071125 476.089844 0.230431 0.041874 0.007622
    - averaged(filter): 0.054508 646.103027 0.165958 0.031125 0.005839
    - type constraint results:
    - metric: MRR MR hit@10 hit@3 hit@1
    - l(raw): 0.102386 289.001709 0.233949 0.101290 0.041044
    - r(raw): 0.281420 69.016174 0.480749 0.306557 0.185478
    - averaged(raw): 0.191903 179.008942 0.357349 0.203924 0.113261
    - 
    - l(filter): 0.270987 92.826538 0.449624 0.293804 0.182938
    - r(filter): 0.458211 52.676880 0.638864 0.503616 0.363579
    - averaged(filter): 0.364599 72.751709 0.544244 0.398710 0.273258

- 2019-10-10

  - Version 63 folks version 62, alpha change from 0.6 to 0.7, (hd#319,320), final loss at epoch 661, loss 4773
  - Version 65 folks version 61, train on adam 0.005 (hd#321,#322), 3 hrs 37 mihs, final loss at epoch 136, loss 9751.
  - Version 66 folks version 65, train on adam 0.002 (hd#323,#324), end at epoch 263, loss 9116
  - Version 67 folks version 63, alpha change from 0.7 to 0.8, (hd#325,#326), end at epoch 668, loss 4736

- 2019-10-09

  - version 59, upload the code of version 47, alpha change from 0.5 to 0.4, hd#311-312 is worer than Version 47
  - version 60, upload the code of version 47, alpha change from 0.5 to 0.1, hd#313-314 is worse than version 59
  - Dimension 200, adam alpha 0.01 final loss 11687 is better than alpha 0.02 final loss 14335 (hd#310,hd#307)
  - Version 61, train on adam 0.008 (hd#315,#316), 3hrs 38mins, final loss at epoch 136, 10775.
  - Version 62 folks version 47, alpha change from 0.5 to 0.6, (hd#317,hd#318), at final loss 4835

- 2019-10-08

  - Version 57, test on version 54 epoche 103 with loss 4857

- 2019-10-07

  - Version 42 training result seems very good. It ends at loss 65.
  - Version 43 test on version 42 epoch 235.
  - Version 47 the same as version 42, training without hinge loss nor negative sampling, 9 hours stopped at epoche 664. hd#281
  - Version 54 continue training of version 47 from epoche 664.

- 2019-10-06

  - Change beta to 0.001 from 0.01 , loss becomes nan at epoch 3
  - Change alpha to 0.1, loss decreases slowly and bounces a lot.
  - Change alpha to 0.05, loss decreases slowly and bounces a lot
  - Change alpha to 0.02, loss decreases slowly and bounces a lot
  - Change alpha to 0.01, loss decreases slowly and bounces a lot
  - It seems alpha 0.008 works best.
  - Remove the negative sampling, loss 9k, doesn't decrease.
  - Try beta 0.0001, loss 7k, doesn't decrease
  - Try hinge loss without the negative sampling, loss 10k doesn't decrease
  - Alpha 0.2, Try hinge loss without the negatives ampling, loss 10k doesn't decrease
  - Vesion 42, return back to the begining. SGD, with negative sampling. #266 on hyperdash

- 2019-10-05

  - Version 30 learning rate is too small
  - Version 34 training final loss 4k
    - Version 35 train on version 34 epoch 5

- 2019-10-04

  - In embedding.vec.json, the embeddings are all NaN
  - It's may be due to the exploding gradient problem
    - https://stackoverflow.com/questions/51038266/why-my-tensorflow-model-outputs-become-nan-after-x-epochs

- 2019-10-02

  - test result openke_word2vec version 18
    - 1 hr 17mins
      no type constraint results: 
      metric: MRR MR hit@10 hit@3 hit@1 
      l(raw): 0.028714 1154.996826 0.077299 0.021597 0.003713 
      r(raw): 0.098217 554.068909 0.242793 0.113359 0.027802 
      averaged(raw): 0.063465 854.532837 0.160046 0.067478 0.015758 
      l(filter): 0.035007 849.547546 0.093472 0.028437 0.004007 
      r(filter): 0.108639 532.859009 0.268299 0.129972 0.030441 
      averaged(filter): 0.071823 691.203247 0.180885 0.079205 0.017224 
      type constraint results: 
      metric: MRR MR hit@10 hit@3 hit@1 
      l(raw): 0.091450 313.823456 0.186700 0.090003 0.041972 
      r(raw): 0.268340 105.762825 0.437555 0.285987 0.186602 
      averaged(raw): 0.179895 209.793137 0.312127 0.187995 0.114287 
      l(filter): 0.172822 161.105255 0.301524 0.176732 0.108619 
      r(filter): 0.321689 95.164764 0.513583 0.353806 0.230431 
      averaged(filter): 0.247255 128.135010 0.407554 0.265269 0.16952
  - `self.saver = tf.train.Saver(max_to_keep = 20)` to keep more checkpoints

- 2019-09-30

  - kaggle will rename test_openke to test-openke

- 2019-09-27

  - Test from checkpoint get loss array [nan nan nan ... nan nan nan]

- 2019-09-25

  - Different opt method will affect the loss of first epoch?
    - SGD: ~900
    - adam: ~65
  - Without negative sampling and margin loss, the learning rate is quite hard to tune.

- 2019-09-24

  - performance result
    - 3 hrs 55mins
      no type constraint results: metric: MRR MR hit@10 hit@3 hit@1 l(raw): 0.035857 3088.653564 0.073634 0.036646 0.016417 r(raw): 0.176729 1972.872314 0.285498 0.186798 0.127919 averaged(raw): 0.106293 2530.762939 0.179566 0.111722 0.072168 l(filter): 0.045567 2856.652100 0.082967 0.048422 0.024382 r(filter): 0.215069 1953.115356 0.339734 0.237565 0.158311 averaged(filter): 0.130318 2404.883789 0.211351 0.142993 0.091347 type constraint results: metric: MRR MR hit@10 hit@3 hit@1 l(raw): 0.071169 640.897400 0.138132 0.068748 0.034154 r(raw): 0.230529 233.559174 0.362846 0.246116 0.163491 averaged(raw): 0.150849 437.228271 0.250489 0.157432 0.098822 l(filter): 0.158843 408.915131 0.252077 0.163100 0.109010 r(filter): 0.301488 213.801620 0.449477 0.327421 0.226717 averaged(filter): 0.230165 311.358368 0.350777 0.245260 0.167864

- 2019-09-23

  - Download the model in kaggle

    - method 1
      `
      from IPython.display import FileLink, FileLinks
      FileLinks('.') #lists all downloadable files on server
      `

  - Performance result

    - 1 hr 33 mins
      no type constraint results:
      metric: MRR MR hit@10 hit@3 hit@1 
      l(raw): 0.008282 4673.078125 0.009333 0.005375 0.005375 
      r(raw): 0.058605 3029.861084 0.119124 0.058292 0.022183 
      averaged(raw): 0.033444 3851.469727 0.064228 0.031833 0.013779 

      l(filter): 0.008357 4450.305664 0.009528 0.005375 0.005375 
      r(filter): 0.059085 3011.388672 0.119857 0.058292 0.022183 
      averaged(filter): 0.033721 3730.847168 0.064693 0.031833 0.013779 
      type constraint results:
      metric: MRR MR hit@10 hit@3 hit@1 
      l(raw): 0.064264 663.311951 0.130167 0.061859 0.028877 
      r(raw): 0.223904 241.954559 0.343741 0.230724 0.164370 
      averaged(raw): 0.144084 452.633240 0.236954 0.146291 0.096624 

      l(filter): 0.133146 440.550415 0.220805 0.136324 0.087462 
      r(filter): 0.271826 223.478745 0.418304 0.286377 0.202922 
      averaged(filter): 0.202486 332.014587 0.319554 0.211351 0.145192 

- 2019-09-22

  - https://github.com/googlecolab/colabtools/issues/661
    - Tesla T4 is not accessible any more for me on colab. According to my test, K80(colab) is about 6 times slower than P100(kaggle).
    - for openke_word2vec each epoch
      - colab 517s
      - kaggle 97s
      - vast.ai 188s (GTX 1070ti, P8Z68, Core i5-2500 2.0/4 cores 8/16 GB, Samsung 517MB/s, 6.2 DLPerf, $0.068/hr)
      - colab-cpu 7250s (around 2 hours)
  - Parameters for openke to run on colab and kaggle
    - colab
      - dimension = 100
      - nbatches = 1500
    - kaggle
      - dimension = 100
      - nbatches = 1000
  - openke_word2vec run on colab takes around 2 hours/epoch
    - Epoch: 0, loss: 200.00305849313736, time: 7250.3890788555145
    - Epoch: 1, loss: 199.99601310491562, time: 7256.021113157272
    - Epoch: 2, loss: 199.98996078968048, time: 7288.72056388855 Epoch: 3, loss: 199.98503702878952, time: 7285.004914283752
  - 

- 2019-09-19

  - Noise-contrastive estimation
    - https://datascience.stackexchange.com/questions/13216/intuitive-explanation-of-noise-contrastive-estimation-nce-loss
      The issue
      There are some issues with learning the word vectors using an "standard" neural network. In this way, the word vectors are learned while the network learns to predict the next word given a window of words (the input of the network).
      Predicting the next word is like predicting the class. That is, such a network is just a "standard" multinomial (multi-class) classifier. And this network must have as many output neurons as classes there are. When classes are actual words, the number of neurons is, well, huge.
      A "standard" neural network is usually trained with a cross-entropy cost function which requires the values of the output neurons to represent probabilities - which means that the output "scores" computed by the network for each class have to be normalized, converted into actual probabilities for each class. This normalization step is achieved by means of the softmax function. Softmax is very costly when applied to a huge output layer.
      The (a) solution
      In order to deal with this issue, that is, the expensive computation of the softmax, Word2Vec uses a technique called noise-contrastive estimation. This technique was introduced by [A] (reformulated by [B]) then used in [C], [D], [E] to learn word embeddings from unlabelled natural language text.
      The basic idea is to convert a multinomial classification problem (as it is the problem of predicting the next word) to a binary classification problem. That is, instead of using softmax to estimate a true probability distribution of the output word, a binary logistic regression (binary classification) is used instead.
      For each training sample, the enhanced (optimized) classifier is fed a true pair (a center word and another word that appears in its context) and a number of kk randomly corrupted pairs (consisting of the center word and a randomly chosen word from the vocabulary). By learning to distinguish the true pairs from corrupted ones, the classifier will ultimately learn the word vectors.
      This is important: instead of predicting the next word (the "standard" training technique), the optimized classifier simply predicts whether a pair of words is good or bad.
      Word2Vec slightly customizes the process and calls it negative sampling. In Word2Vec, the words for the negative samples (used for the corrupted pairs) are drawn from a specially designed distribution, which favours less frequent words to be drawn more often.
  - git largfe files
    - https://git-lfs.github.com/
  - OpenKE can't show output from the Base.so, which is the c library, in jupyter.
    - https://github.com/QuantStack/xeus-cling/issues/112
    - https://github.com/ipython/ipykernel/issues/110

- 2019-09-17

  - Get output embedding matrix in gensim `model.syn1`
    - https://stackoverflow.com/questions/41162876/get-weight-matrices-from-gensim-word2vec

- 2019-09-13

  - plotly bsample line
    - `trace2 = PlotlyJS.scatter(;x=x2,y=y2, mode="line", name="average mr",line= attr(shape "spline"),)`

- 2019-09-10

  - Predict a word using word2vec model
    - https://datascience.stackexchange.com/questions/9785/predicting-a-word-using-word2vec-model

- 2019-09-09

  - Make dataframe not truncated in jupyter
    - https://github.com/JuliaData/DataFrames.jl/issues/886
      When Julia displays a large data structure such as a matrix, by default it truncates the display to a given number of lines and columns. In IJulia, this truncation is to 30 lines and 80 columns by default. You can change this default by the LINES and COLUMNS environment variables, respectively, which can also be changed within IJulia via ENV (e.g. ENV["LINES"] = 60). (Like in the REPL, you can also display non-truncated data structures via print(x).)
    - `ENV["COLUMNS"] = 160`

- 2019-09-05

  - entity 14516 exist in test but not in train for FB15K-237.

- 2019-09-03

  - xp152 DistMult FB15K
  - xp153 TranseE FB15K
  - Redo xp152,xp153 at xp161,xp162 but use all the test examples instead of 10000

- 2019-08-27

  - [Paper with code WN18RR](https://paperswithcode.com/sota/link-prediction-on-wn18rr)

  - [machine epsilon in c language](https://bytes.com/topic/c/answers/670460-machine-epsilon)

  - REAL is defined as float in ./OpenKE/base/Setting.h

  - Modify Test.h in testHead() and testTail()
    ` for (INT j = 0; j < entityTotal; j++) {
    REAL value = con[j];
    if (j != h && value < minimal) {
    l_s += 1;
    if (not _find(j, t, r))
    l_filter_s += 1;
    }
    }`
    ==>
    `
    \#include "float.h"
    ....

    for (INT j = 0; j < entityTotal; j++) {
    REAL value = con[j];
    if (j != h && value < minimal + FLT_EPSILON) {
    l_s += 1;
    if (not _find(j, t, r))
    l_filter_s += 1;
    }
    }`

  - Test xp152 the best DISTMULT over FB15K with epsilon as xp160

    - The strick rank doesn't affect DISTMULT

- 2019-08-14

  - Parle avec Philippe
    - Try strict ranking in TransE,DISTMULT
    - Try LinkFeat on FB15K-selected
    - Optional try the Naive Bayse with link and node feat.

- 2019-08-12

  - There are some rank #1 with a deviation very small
    (14946, 0.030303573)
    (1, 5.5513004e-17) 
    (1, 5.5513004e-17) 
    (2, 0.0014666952) 
    (1, 0.023063548) 
    (14929, 0.040659655)
    (1, 0.0013072524) 
    (18, 0.026367811) 
    (18, 0.026367811) 
    (1, 0.014130712) 
    (9, 0.016517866) 

- 2019-08-11

  - Check the test method in OpenKE.

    - https://github.com/thunlp/OpenKE/blob/master/base/Test.h
      `
      REAL minimal = con[h];
      INT l_s = 0;
      INT l_filter_s = 0;
      INT l_s_constrain = 0;
      INT l_filter_s_constrain = 0;

      for (INT j = 0; j < entityTotal; j++) {
      if (j != h) {
      REAL value = con[j];
      if (value < minimal) {
      l_s += 1;
      if (not _find(j, t, r))
      l_filter_s += 1;
      }
      while (lef < rig && head_type[lef] < j) lef ++;
      if (lef < rig && j == head_type[lef]) {
      if (value < minimal) {
      l_s_constrain += 1;
      if (not _find(j, t, r)) {
      l_filter_s_constrain += 1;
      }
      } 
      }
      }
      }

      
      `

    - If every triple gets the same score, than they all will be ranked as #1

- 2019-08-09

  - GC.gc() doesn't work in the same function
    `function foo()
    A = zeros(Int64,10^9)
    A = nothing
    GC.gc() # Doesn't work
    end
    foo()`

- 2019-08-08

  - In `_lookup_feature()`, annotate `feat_idx` and `feat_idx_inv` as Float32

  - dictionary of tuple , string , int `haskey()` performance.

    `A = collect(1:70000)

    dict1 = Dict{Tuple{Int64,Int64},Int64}()

    dict2 = Dict{String,Int64}()

    dict3 = Dict{Int64,Int64}()

    n = length(A)

    shift = ceil(log10(n))

    for i in 1:length(A)

    dict1[(i,i)]=i

    dict2["$i&$i"]=i

    dict3[i*10^shift+i]=i

    end

    x = 100

    @btime haskey(dict1,(x,x))

    @btime haskey(dict2,"$x&$x")

    @btime haskey(dict3,x*10^shift+x)

    `

    223.346 ns (1 allocation: 32 bytes)

    1.192 μs (9 allocations: 400 bytes)

    103.101 ns (3 allocations: 48 bytes)

    - if we apply this we will save 100ns for each test mask(about 15000 entites) over 50000 test triples. So it will save totally 0.0000001*15000*50000 = 750s. It doesn't worth it

  - We may use `GC.enable(false)` to disable the gc collector and enable it after with `GC.enable(true)`. And run the collector aLLLLLLny time with `GC.gc()`
    `GC.enable(false)
    test_once([0,348,0])
    GC.enable(true)
    GC.gc()`

- 2019-08-07

  - optimise `get_test_candidats()`
    method 1: 811.356 μs (14968 allocations: 2.74 MiB)
    `if TEST_ARG == "TAIL"
    test_once_candidats = hcat([ [arg1,mask,rel] for mask in entity_list]...)
    else
    test_once_candidats = hcat([ [mask,arg2,rel] for mask in entity_list]...)
    end`

    method 2: 14.572 ms (221716 allocations: 5.78 MiB)
    `if TEST_ARG == "TAIL"
    for i in 1:length(entity_list)
    test_once_candidats[:,i] = [arg1;entity_list[i];rel]
    end
    else
    for i in length(entity_list)
    test_once_candidats[:,i] = [entity_list[i];arg2;rel]
    end
    end`

    method 3: 78.292 μs (15 allocations: 935.08 KiB)
    `if TEST_ARG == "TAIL"
    test_once_candidats = vcat(fill(arg1,n),entity_list,fill(rel,n))
    else
    test_once_candidats = vcat(entity_list,fill(arg2,n),fill(rel,n))
    end`

- 2019-08-05

  - How to deal with the rank of entities with the same score?
  - Add l1 penalty, it shows `back!` was already used error during training.

- 2019-08-02

  - `isInTrain()` dataframe version takes 1.25ms while set version takes 72.584ns ONLY!
    ` return size(df_train[(df_train.arg1 .== arg1) .& 
    (df_train.rel .== rel) .& 
    (df_train.arg2 .== arg2),:],1) > 0`

    vs

    `return (arg1,arg2,rel) in train_triple_set`

  - broadcasting is quite slower than loop

    - https://github.com/JuliaLang/julia/issues/28126

  - Lookup value

    - dictionary vs array vs dataframe
      - @btime feat_tuple_dict[(134,172)]
        - 34.760 ns (1 allocation: 16 bytes)
      - @btime findall(x->x==(134,172), A)
        - 2.386 μs (6 allocations: 272 bytes)
      - @btime df_feat_idx[in(["134&172"]).(df_feat_idx.label),:]
        - 34.771 μs (34 allocations: 6.69 KiB)

- 2019-08-01

  - How to properly mix the operation between Tracked Array and Array of TrackeReal
    - https://github.com/FluxML/Flux.jl/issues/205
    - Tracker.collect()
  - Training is very slow. 100 examples take 6 mins. Then half million examples will take 500 hours (20 days)

- 2019-07-31

  - julia broadcasting problem
    `A = collect(1:12)
    A = reshape(A,(3,:))'

    add(x,y,z) = x+y+z
    myadd = x -> add(x...)
    add.(eachcol(A)...)
    myadd.(eachrow(A))

    add.([1, 4, 7, 10],[2, 5, 8, 11],[3, 6, 9, 12])
    myadd.([[1, 2, 3],[4, 5, 6],[7, 8, 9],[10, 11, 12]])
    `

- 2019-07-23

  - Rendez-vous avec Philippe
    - Concentrer sur:
      - bias dans Frequence
      - bias dans donnes
      - graph (probablement, random walk)

- 2019-07-19

  - Use `corssentopy(x)` to replace the `-sum(log.(x))`
  - `sum((loss(d...) for d in data))` will consume much memory
    - Because the `loss(d...)` return a tracked value and accumulate this value will take lots memory
    - Use `sum((Tracker.data(loss(d...)) for d in data))` instead
  - Wrong loss
    - `loss(x) = max.(0,crossentropy(m(x),ones(1,size(x,2))/size(x,2)))`

- 2019-07-18

  - The length methode is quite important to the definition of iterator.

- 2019-07-16

  - Resolved the errors in training.
  - `xs[2:end,1]=1` is much slower than `xs[:,1]=1` when xs is big
  - `Flux.params()` works with those predefined layers like `Dense`

- 2019-07-08

  - `df_by_ent_pair = by(df_train, [:arg1,:arg2], rels = :rel=> x -> collect(x), rels_count = :rel=>length)` is incorrect!
    - `df_by_ent_pair = by(df_train, [:arg1,:arg2], rels = :rel=> x -> collect.([x]), rels_count = :rel=>length)`

- 2019-07-05

  - Link feature summary
    Summary Stats:
    Length: 394804
    Missing Count: 0
    Mean: 1.223752
    Minimum: 1.000000
    1st Quartile: 1.000000
    Median: 1.000000
    3rd Quartile: 1.000000
    Maximum: 10.000000
    Type: Int64

- 2019-07-04

  - Construct Link and node feature
    - https://www.overleaf.com/read/gfkywhhpwtfn

- 2019-06-26

  - Finish relation frequence distribution hitorgram on FB15K-237
  - Found [qgrid](https://github.com/quantopian/qgrid)to interact with table grid

- 2019-06-25

  - plotlyjs.jl
    - SyncPlots example doesn't work
      - http://spencerlyon.com/PlotlyJS.jl/syncplots/#syncplots

- 2019-06-22

  - `cp -r WebIO.jl-master/packages/webio/ ./.julia/packages/WebIO/nNJPv/packages/`

  - in julia pkg mode, `build WebIO` no error but it shows still `WebIO not detected.`
    `using WebIO
    display(Node(:input, attributes = Dict("type" => "range")))` shows the rang input bar

  - Discussion related to this problem

    - https://github.com/sglyon/PlotlyJS.jl/issues/255
    - https://github.com/sglyon/PlotlyJS.jl/issues/278#issuecomment-499970113
    - https://github.com/JuliaGizmos/WebIO.jl/issues/281

  - plotly offline charts show blank

    - code
      `
      def enable_plotly_in_cell():
      import IPython
      from plotly.offline import init_notebook_mode
      display(IPython.core.display.HTML('''
      <script src="/static/components/requirejs/require.js"></script>
      '''))
      init_notebook_mode(connected=False)

      from plotly.offline import iplot
      import plotly.graph_objs as go

      enable_plotly_in_cell()

      data = [
      go.Contour(
      z=[[10, 10.625, 12.5, 15.625, 20],
      [5.625, 6.25, 8.125, 11.25, 15.625],
      [2.5, 3.125, 5., 8.125, 12.5],
      [0.625, 1.25, 3.125, 6.25, 10.625],
      [0, 0.625, 2.5, 5.625, 10]]
      )
      ]
      iplot(data)
      `

    - In browser console, it shows:

      - `Uncaught ReferenceError: require is not defined`

    - Jupyterlab and Plotly offline: requirejs is not defined

    - https://stackoverflow.com/questions/54148668/jupyterlab-and-plotly-offline-requirejs-is-not-defined

    - Follow the instruction to install the [plotly extension for Jupyter Lab](https://github.com/jupyterlab/jupyter-renderers/tree/master/packages/plotly-extension) it resolves the problems. (It resolves the WebIO not dected problem)

- 2019-06-21

  - Encounter WebIO not detected problem.

  - command log

    - `conda install -c conda-forge nodejs`

    - `npm install --save core-js@^3`

    - `jupyter labextension install @webio/jupyter-lab-provider`

      - Segmentation fault (core dumped)
      - error Command failed with exit code 139.

    - `jupyter lab build`

      - Segmentation fault (core dumped)
      - error Command failed with exit code 139.
      - Node v6.12.2 resolved the jupyter lab build problem

    - `npm i @webio/webio`

    - `pkg> build WebIO`

      Errored, use --debug for full output:

      ValueError: Can install "/u/wujieche/.julia/packages/WebIO/nNJPv/packages/webio" only link local directories

      [ Info: Copying WebIO nbextension files to /u/wujieche/.local/share/jupyter/nbextensions/webio.

      ┌ Warning: Unable to install Jupyter Lab extension; make sure jupyter is in your PATH and rebuild WebIO if you want to use Jupyter Lab.

      │ exception = failed process: Process(`/u/wujieche/miniconda3/bin/jupyter labextension link --no-build /u/wujieche/.julia/packages/WebIO/nNJPv/packages/webio`, ProcessExited(1)) [1]

      └ @ Main ~/.julia/packages/WebIO/nNJPv/deps/build.jl:9

      - I believe it's because folder `/u/wujieche/.julia/packages/WebIO/nNJPv/packages/webio` doesn't exist.
      - https://github.com/JuliaGizmos/WebIO.jl/tree/18d6c6bbcf2eaab19fab3de6ada4e3339ac3e6b5/packages/webio

- 2019-05-30

  - Initial

     

    Apache Jena Fuseki

    - The local machine path `/part/01/Tmp/Freebase/Index` may not work. Use `/data/rali6/Tmp/Freebase/Index` instead.
    - Resolve [ERROR Exception in initialization:GC overhead limit exceeded](https://dynalist.io/d/dNMnL9fQPpbbUwiykSJawFiU#z=I3lcYzwLLRUmFg6d23jKX8de)

  - Try SPARQL

    - actor <-> film

      - `12 years a slave freebase mid: m.0h32y7j / wikidata id:Q3023357`

      - `Brad Pitt freebase mid: m.0c6qh / wikidata id: Q35332`

      - Aprroved [The performance.film and performance.actor should be switched](https://dynalist.io/d/dNMnL9fQPpbbUwiykSJawFiU#z=YuEgfruWp8ENZrFPEjncGX2w) [Local jena link](http://localhost:8080/dataset.html?query= PREFIX+freebase%3A+ SELECT+* WHERE+{ ++%3Factor+freebase%3Atype.object.name+"Brad+Pitt"%40en. ++%3Factor+freebase%3Afilm.actor.film+%3Fmed. ++%3Fmed+freebase%3Afilm.performance.film+%3Ffilm. ++%3Ffilm+freebase%3Atype.object.name+"12+Years+a+Slave"%40en. } LIMIT+25 )

        PREFIX fb: <http://rdf.freebase.com/ns/>
        SELECT *
        WHERE {
        ?actor fb:type.object.name "Brad Pitt"@en.
        ?actor fb:film.actor.film ?med.
        ?med fb:film.performance.film ?film.
        ?film fb:type.object.name "12 Years a Slave"@en.
        }

        ///////////////////////////////////////////////////////////////////
        // obsolete

        PREFIX freebase: <http://rdf.freebase.com/ns/>
        SELECT *
        WHERE {
        freebase:m.0c6qh freebase:film.actor.film ?med.
        ?med freebase:film.performance.film freebase:m.0h32y7j
        }
        LIMIT 25

        
        SELECT *
        WHERE {
        <http://rdf.freebase.com/ns/m.0c6qh> <http://rdf.freebase.com/ns/film.actor.film> ?med.
        ?med <http://rdf.freebase.com/ns/film.performance.film> <http://rdf.freebase.com/ns/m.0h32y7j>
        }
        LIMIT 25
        // <http://rdf.freebase.com/ns/m.0hgdwjl>

        
        SELECT *
        WHERE {
        <http://rdf.freebase.com/ns/m.0h32y7j> <http://rdf.freebase.com/ns/type.object.name> ?o.
        FILTER (lang(?o) = 'en')
        }
        LIMIT 25
        // "12 Years a Slave"@en

    - award <-> nominee

  - Upload freebase to wikidata mapping to fuseki

    - 

- 2019-05-29

  - Found CVT relation graph [CVT relation](https://dynalist.io/d/dNMnL9fQPpbbUwiykSJawFiU#z=4z0QhWzO2PnDdm8UqbCYy994)

- 2019-05-28

  - Found freebase shema wiki page
    - [freebase-schema](https://dynalist.io/d/dNMnL9fQPpbbUwiykSJawFiU#z=bQOEAVbmTTYX4JPDgacQTxUr)

- 2019-05-27

  - Find example in Freebase easy
  - Data strange
  - Find archived freebase doc page
    - [Freebase Docs](https://dynalist.io/d/dNMnL9fQPpbbUwiykSJawFiU#z=alU1XVdeAqEB8sVDr_jCTUlP)
    - [Freebase Schema Explorer](https://dynalist.io/d/dNMnL9fQPpbbUwiykSJawFiU#z=pq02BoBUnR1ay3yqZBsHFzDW)

- 2019-05-24

  - Comme le Freebase est désapprouvé, peut-être wikidata est un meilleur choix? E.g.: WD40k and WD40k_nl from wikidata.

- 2019-05-23

  - succeeded loading wembedder's word2vec model

    - Should use get(model.wv,"Q2") instead of model.wv["Q2"\] Refer to this page [https://github.com/JuliaPy/PyCall.jl](https://github.com/JuliaPy/PyCall.jl)
      Given o::PyObject, get(o, key) is equivalent to o[key] in Python, with automatic type conversion. 

    - Read

       

      freebase guide page

      - /Domain_ID/Type_ID/Property_ID

    - data strange

      - Billy Boyd,/award/award_nominee/award_nominations./award/award_nomination/award_nominee,Sean Bean
      - 

- 2019-05-22

  - Downloaded the wembedder model(gensim word2vec) and try to load it in julia

- 2019-05-21

  - Wembedder web service

     

    Wembedder: Wikidata entity embedding web service

    - https://tools.wmflabs.org/wembedder/api/most-similar/Q2

- 2019-05-20

  - Found pretrained wikidata [Pretrained wikipedia embeddings with word2vec](https://dynalist.io/d/5xiJQiY9VxhxatwvZVDVPCyO#z=i3X6rUqXhciONPVXLYGwXr3d)

- 2019-05-17

  - Fabrizio found there are dot in the relatiosns
    - e.g: /award/award_nominee/award_nominations./award/award_nomination/award
    - It shows some relations contains two sub relations
  - /award/award_nominee & /award_nominee/award
  - Write indexation_kb.ipynb to seperate sub relations
    - Out in FB15k_sprel and FB15k-237_sprel
    - 1389 entities for FB15k_sprel
    - 302 entities for FB15K-237_sprel

- 2019-05-16

  - Finish lexicalize_fb15k.ipynb
  - Can't find the ralations with 97% intersections

- 2019-05-15

  - 50K valids
    - 13292 unique entities
  - There are some entities not included in Freebase to wikidata mappings
    - e.g: `/m/07kcvl`

- 2019-05-14

  - Found

     

    - [Freebase/Wikidata Mappings](https://dynalist.io/d/dNMnL9fQPpbbUwiykSJawFiU#z=D7yUNwGaYBiNyVsK5qWiZp9S)
    - and [wikidata API](https://dynalist.io/d/dNMnL9fQPpbbUwiykSJawFiU#z=G08zBucTUT0ovBLOsygBNuGE)

- 2019-05-13

  - FB Search API
    - [MID search API](https://dynalist.io/d/dNMnL9fQPpbbUwiykSJawFiU#z=XGhuyD_8DcYG_UyDYQzchl8S)
  - /m/06cx9 does not exist!
    - https://developers.google.com/apis-explorer/#p/kgsearch/v1/kgsearch.entities.search?ids=%252Fm%252F06cx9&_h=1&
      - return json is
        {
        "@context": {
        "@vocab": "http://schema.org/",
        "goog": "http://schema.googleapis.com/",
        "EntitySearchResult": "goog:EntitySearchResult",
        "detailedDescription": "goog:detailedDescription",
        "kg": "http://g.co/kg"
        },
        "@type": "ItemList",
        "itemListElement": []
        }
    - according to https://www.wikidata.org/wiki/Q7270it means republic

- 2019-05-12

  - Know more about FB15K source
    - [FB15K Source](https://dynalist.io/d/dNMnL9fQPpbbUwiykSJawFiU#z=9-iY-WFFGVZds9ktowtGKolj)

- 2019-05-01

  - Entity type
    Entity: Boss
    Entity type: [{eat, work},{report}]

    Entity: Developper
    Entity type: [{sleep, work},{blame}]

    Entity: Human
    Entity type: [{eat, work},{research}]

    Entity: Dog
    Entity type: [{eat, work, play},{feed}]

    Entity: Cat
    Entity type: [{eat, work, play},{feed}]

    Eat allowable entity type top 1: [{eat, work, play},{feed}]

- 2019-04-30

  - ![](https://imgur.com/tdoJIje.png)
  - FB15K-237
    - train 272115
    - valid 17535
    - test 20466
  - FB15K in OpenKE
    - train 483142
    - valid 50000
    - test 59071

- 2019-04-25

  - Question:
    - La fonction `getBestThreshold()` sert à quoi?
  - Rendez-vous avec Philippe
    - Verifier les papier Toutanova sur les problémes de corpus
    - Faire une version lisible pour FB15K-237
    - Essayer word2vec comme baseline sur FB15K-237

- 2019-04-23

  - lettre a prof
    Salut prof,

    Selon les expériences que j'ai fait l'année passée, j'ai mean rank 38 qui surpasse le single DsitMult in Kadlec et Al. 2017 (mean rank 42) sur FB15K, qui comprend 15K entities. Le baseline basé sur la fréquence a nous donnée mean rank 3449. J'ai pas trouvé les points intéressant. Est-ce que tu penses que il faut encore vérifier les détail? E.g: On regarde si les examples qui ne donnent pas très bien résultats dans DistMult/TransE peuvent donnent meilleure résultat dans baseline pour confirmer que DistMult/TransE portent déjà toutes des information de fréquence?

    Je essaye de comprendre plus sur le knowledge embeddings. Je trouve que la partie negative sampling est intéressante. Et je trouve que, dans word2vec, TransE, OpenKE, il semble qu'il utilise différentes méthodes de negative sampling. Selon Han et al. 2018, les triplets ont grande influence sur résultat final. Je veux prendre plus de temps pour comprendre cette partie.

    Ensuit, je trouve que les variants du TransE m'intéressent aussi. TransH, TransR, TransD, TransA, TransG, Transparse, ils servent à résoudre différents problème de TransE. Fondamentalement ils font la sommation de arg1 et relation. Si tu ne rejette pas, je vais mettre un peu de temps sur eux. Mais Ils sont aussi presque proposés par chinois! C'est vraiment bizarre.

    Du coup, la recherche de géométrie de knowledge graph embeddings m'intéresse aussi. Dans le travail de Chandrahas et al. 2018, ils ont montré le conicity (la moyenne de similarité de chaque vecteur par rapport à la moyenne des vecteurs) des models. Je crois que ce travail nous aidera à comparer les différences entre le model additive et celui multiplicative.

    Je vais commencer à faire la cross-validation pour confirmer mon meilleur résultat. J'espère que je peux obtenir un bon résultat dans deux semaines. 

    Quand tu seras disponible cette semaine? Nous pourrions en parler.

    

- 2019-04-20

  - outline for the email to Philippe:

    - baseline on FB15K

      - MR AVG = 3449.13735

         

        - MR arg1 = 3742.7826
        - MR arg2 = 3155.4921

      - Est-ce qu'il faut vérifier encore les détail?

      - DistMult: nbatches = 500, train_times = 100, Adam, lr= 0.001, n=1000,(max-margin + NLL + softmax as the loss, 5 mins train on GPU, MR=38 outperformed single distmult in Kadlec et Al. 2017 /MR= 42, MRR = 0.798/, our MRR= 0.535 is a little worse.)

        - il faut faire de la cross-validation

    - Negative Sampling

      - negative sampling in word2vec
        - [Part 2 Negative sampling](https://dynalist.io/d/pjG8fAbeOPV-j8Yr1b-i_FkU#z=kIVIn1KOI47ldnFeD9oFvMxr)
      - negative sampling in TransE
      - negative sampling in OpenKE

    - D'autres recherches

      - Les variants de TransE ( TransH, TransR, TransD, TransA, TransG, Transparse)
      - Lire plus de survey
      - 

  - [CBOW vs skip-gram](https://dynalist.io/d/pjG8fAbeOPV-j8Yr1b-i_FkU#z=cmG-O-0BErZDXzQZT6oOSU9M)

- 2019-04-19

  - negative sampling
    - in Han Xu's paper

- 2019-04-16

  - How does OpenKE do when the test entity has not been seen in training?
    - In file Test.h line 50-57
      - It shows it will return the max+1
  - Baseline on FB15K
    - MR AVG = 3449.13735
    - MR arg1 = 3742.7826
    - MR arg2 = 3155.4921

- 2019-04-01

  - Add f.flush into Configure.py
  - Succeeded xp069-2

- 2019-03-26

  - xp069-2-test at 09:14 run on malaga02 succeeded
  - Run xp069-2 at 21:38 on malaga02

- 2019-03-16

  - xp069-2-test(train times 1 instead of 500) Failed

- 2019-03-13

  - xp069-2 Failed

- 2019-03-11

  - xp042-2 Finished
  - xp069-2 Failed
  - Run xp069-2 at 11:13 on malaga02

- 2019-03-08

  - Found xp042-2 on ilar01 and xp069-2 on malaga01 **error**
  - Run xp042-2 at 18:41 on malaga02 
  - Run xp069-2 at 18:41 on malaga01

- 2019-03-06

  - Get Baseline V2+ cluster V4 OpenKE format log:

     

    - sim_freq_rank_2_cluster
    - baseline_v2_cluster_v4.log

- 2019-03-05

  - Run xp069-2 at 17:49 on malaga01

  - Get Baseline V2 OpenKE format log:

     

    - sim_freq_rank_2.ipynb
    - baseline_v2.log

- 2019-03-04

  - Run xp042-2 at 13:29 on ilar01 
  - Run xp069-2 at 21:32 on malaga01 **disconnected**

- 2019-03-03

  - Refer to this report
    - https://nbviewer.jupyter.org/github/quatrejuin/try_ke_models/blob/master/report/report.ipynb
    - Best TransE: xp069
    - Best TransE+cluster V2: xp042
    - Best Baseline V2:
    - Best Baseline V2+ cluster V4: 
  - Run xp069-2 at 23:30 on otctal03 **killed**

- 2019-02-27

  - je comprends déjà le "negative sampling" dans word2vec. D'après ce tutoriel ([http://mccormickml.com/2017/01/11/word2vec-tutorial-part-2-negative-sampling/](http://mccormickml.com/2017/01/11/word2vec-tutorial-part-2-negative-sampling/)). Le "negative sampling" sert simplement à faciliter le calcul quand on met à jour des paramètres.
  - Je suis en train d'essayer de comprendre le "negative sampling" in OpenKE (Dans la fonction getBatch() du fichier base.cpp) #openke
