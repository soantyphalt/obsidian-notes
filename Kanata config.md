;; Kanata Extend Layer - minimal test configuration  
  
(defcfg  
 danger-enable-cmd yes  
 process-unmapped-keys no  
)  
  
(defsrc  
 esc  1 2 3 4 5 6 7 8 9 0 - = bspc  ][''[[[[]]]]]
 tab  q w e r t y u i o p [ ] \  
 caps a s d f g h j k l ; ' ret  
 lsft z x c v b n m , . /  
 lctl lmet lalt spc ralt rmet rctl  
)  
  
(defalias  
 ext (layer-while-held extend)  
 search C-f  
 redo C-y  
 undo C-z  
 cut C-x  
 open-readme (cmd xdg-open https://github.com/stevep99/keyboard-tweaks/blob/master/ExtendLayer/README.md)  
 scroll-up (mwheel-up 50 120)
 scroll-down (mwheel-down 50 120)
)  
  
(deflayer base  
 esc  1 2 3 4 5 6 7 8 9 0 - = bspc  
 tab  q w e r t y u i o p [ ] \  
 @ext a s d f g h j k l ; ' ret  
 lsft z x c v b n m , . /  
 lctl lmet lalt spc ralt rmet rctl  
)  
  
(deflayer extend  
 _    f1 f2 f3 f4 f5 f6 f7 f8 f9 f10 f11 f12 _  
 _    esc XX @search XX ins pgup home up end caps @scroll-up _ _  
 _    lalt lmet lsft lctl ralt pgdn left down rght del @scroll-down _  
 _    @undo @cut XX XX XX prtsc bspc tab menu ret  
 _ _ _ _ _ _ _  
)