It is custom treeselect for itg media
Here is only two differences from original package:
1) :enable-country-searching="true" - changed searching algorithm///For example, at first we try to find country by alpha2 code?
, if did not find then try to find by alpha3 code, if did not find too then we try to find by occurencies in name of country/
2) :hide-selected - if true, selected leafs will be hidden from branch

Website of original extension https://vue-treeselect.js.org/