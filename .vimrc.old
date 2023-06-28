"-------基本設定--------
"タイトルをバッファ名に変更しない
set notitle
set shortmess+=I

"ターミナル接続を高速にする
set ttyfast

"ターミナルで256色表示を使う
set t_Co=256

if has ("viminfo")
  "フォールド設定(未使用)
  "set foldmethod=indent
  set foldmethod=manual
  "set foldopen=all
  "set foldclose=all
endif

"VIM互換にしない
set nocompatible

"内容が変更されたら自動的に再読み込み
set autoread

"Swapを作るまでの時間m秒
set updatetime=0

"Unicodeで行末が変になる問題を解決
set ambiwidth=double

"行間をシームレスに移動する
set whichwrap+=h,l,<,>,[,],b,s

"カーソルを常に画面の中央に表示させる
"set scrolloff=999

"バックスペースキーで行頭を削除する
set backspace=indent,eol,start

"カッコを閉じたとき対応するカッコに一時的に移動
set nostartofline

"C-X,C-Aを強制的に10進数認識させる
set nrformats=
"set nrformats=alpha

"titleを変更しない
set notitle

"コマンドラインでTABで補完できるようにする
set wildchar=<C-Z>

"改行後に「Backspace」キーを押すと上行末尾の文字を1文字消す
set backspace=2

"C-vの矩形選択で行末より後ろもカーソルを置ける
set virtualedit=block

"コマンド、検索パターンを50まで保存
set history=50

"履歴に保存する各種設定
set viminfo='100,/50,%,<1000,f50,s100,:100,c,h,!

"バックアップを作成しない
set nobackup

"暗い配色にする
set background=dark

" backup(mkdir ~/.vim mkdir ~/.vim/backup mkdir ~/.vim/swap)
set backup
set backupdir=~/.vim/backup
set swapfile
set directory=~/.vim/swap
set viminfo+=n~/.vim/.viminfo

"-------Search--------
"インクリメンタルサーチを有効にする
set incsearch

"大文字小文字を区別しない
set ignorecase

"大文字で検索されたら対象を大文字限定にする
set smartcase

"行末まで検索したら行頭に戻る
set wrapscan

"-------Format--------
"自動インデントを有効化する
set smartindent
set autoindent

"フォーマット揃えをコメント以外有効にする
set formatoptions-=c

"括弧の対応をハイライト
set showmatch

"行頭の余白内で Tab を打ち込むと、'shiftwidth' の数だけインデントする。
set smarttab

"ターミナル上からの張り付けを許可
set paste

"http://peace-pipe.blogspot.com/2006/05/vimrc-vim.html
set tabstop=2
set shiftwidth=2
set softtabstop=0
set expandtab

"-------Look&Feel-----
"TAB,EOFなどを可視化する
set list
set listchars=tab:>-,extends:<,trail:-,eol:$
" デフォルト不可視文字は美しくないのでUnicodeで綺麗に
"set listchars=tab:»-,trail:-,extends:»,precedes:«,nbsp:%,eol:

"検索結果をハイライトする
set hlsearch

"ルーラー,行番号を表示
set ruler
set number

"コマンドラインの高さ
set cmdheight=1

"マクロなどの途中経過を描写しない
set lazyredraw

"カーソルラインを表示する
set cursorline

"ウインドウタイトルを設定する
set title

"ステータスラインにコマンドを表示
set showcmd
"ステータスラインを常に表示
set laststatus=2
"ファイルナンバー表示
set statusline=[%n]
"ホスト名表示
set statusline+=%{matchstr(hostname(),'\\w\\+')}@
"ファイル名表示
set statusline+=%<%F
"変更のチェック表示
set statusline+=%m
"読み込み専用かどうか表示
set statusline+=%r
"ヘルプページなら[HELP]と表示
set statusline+=%h
"プレビューウインドウなら[Prevew]と表示
set statusline+=%w
"ファイルフォーマット表示
set statusline+=[%{&fileformat}]
"文字コード表示
set statusline+=[%{has('multi_byte')&&\&fileencoding!=''?&fileencoding:&encoding}]
"ファイルタイプ表示
set statusline+=%y
"ここからツールバー右側
set statusline+=%=
"skk.vimの状態
set statusline+=%{exists('*SkkGetModeStr')?SkkGetModeStr():''}
"文字バイト数/カラム番号
set statusline+=[%{col('.')-1}=ASCII=%B,HEX=%c]
"現在文字列/全体列表示
set statusline+=[C=%c/%{col('$')-1}]
"現在文字行/全体行表示
set statusline+=[L=%l/%L]
"現在のファイルの文字数をカウント
set statusline+=[WC=%{exists('*WordCount')?WordCount():[]}]
"現在行が全体行の何%目か表示
set statusline+=[%p%%]
"レジスタの中身を表示
"set statusline+=[RG=\"%{getreg()}\"]

"-------エンコード------
"エンコード設定
if has('unix')
  set fileformat=unix
  set fileformats=unix,dos,mac
  set fileencoding=utf-8
  set fileencodings=utf-8,iso-2022-jp,cp932,euc-jp
  set termencoding=
elseif has('win32')
  set fileformat=dos
  set fileformats=dos,unix,mac
  set fileencoding=utf-8
  set fileencodings=iso-2022-jp,utf-8,euc-jp,cp932
  set termencoding=
endif

"ファイルタイプに応じて挙動,色を変える
"syntax on
"filetype plugin on
"filetype indent on

"-------キー設定-------
"矢印キーでは表示行単位で行移動する
nmap <UP> gk
nmap <DOWN> gj
vmap <UP> gk
vmap <DOWN> gj

"他のvimにviminfoを送る
"http://nanasi.jp/articles/howto/editing/rviminfo.html
nmap ,vw :vw<CR>
nmap ,vr :vr<CR>

"ZZは強制的に書き込む
map ZZ :wq!<CR>

"C-Lでawkを呼び出す
nmap <C-C><C-L> :w !awk 'BEGIN{n=0}{n+=$1}END{print n}'

"C-P,C-Nでバッファ移動,C-Dでバッファ消去
nmap <C-P> :bp<CR>
nmap <C-N> :bn<CR>
nmap <C-D> :bd<CR>

"C-Nで新しいバッファを開く
nmap <C-C><C-N> :new<CR>

"C-L,C-Lでバッファリスト
nmap <C-L><C-L> :ls<CR>
"C-L,C-Rでレジスタリスト
nmap <C-L><C-R> :dis<CR>
"C-L,C-Kでキーマップリスト
nmap <C-L><C-K> :map<CR>
"C-L,C-Mでマークリスト
nmap <C-L><C-M> :marks<CR>
"C-L,C-Jでジャンプリスト
nmap <C-L><C-J> :jumps<CR>
"C-L,C-Hでコマンドヒストリ
nmap <C-L><C-H> :his<CR>
"C-L,C-Uでアンドゥヒストリ
nmap <C-L><C-U> :undolist<CR>

"C-W,sで横分割
nmap <C-W>s :sp<CR>
"C-W,vで縦分割
nmap <C-W>v :vsp<CR>

"C-W,oでファイルを指定して横分割、オープン
nmap <C-W>o :sp
"C-W,Oでファイルを指定して縦分割、オープン
nmap <C-W>O :vp

"C-W,好みの方向キーで新しくバッファを開く
nmap <C-W><C-h> :vne<cr>
nmap <c-w><c-j> :bel new<cr>
nmap <c-w><c-k> :new<cr>
nmap <c-w><c-l> :rightb vnew<cr>

"C-W,eでファイルブラウザを横分割起動
nmap <C-W>e :vsp<CR>:wincmd w<CR>:e! ./<CR>
"C-W,Eでファイルブラウザを縦分割起動
nmap <C-W>E :sp<CR>:wincmd w<CR>:e! ./<CR>

"C-W,C-Aで現在のウインドウのみの表示
nmap <C-W><C-A> :all<CR>

"C-C,C-Rでカーソル語の置き換え
nmap <C-C><C-R> yw:%s:<C-R>0::g<LEFT><LEFT>
"C-C,rでYankした文字列との置き換え
nmap <C-C>r :%s:<C-R>0::g<LEFT><LEFT>
"C-C,gでカーソル語が存在する行の削除
nmap <C-C>g yw:g:<C-R>0:d
"C-C,Gでカーソル語が存在する行以外の削除
nmap <C-C>G yw:v:<C-R>0:d
",celで空白行の削除
nmap ,cel :%s:^$\n:<CR>
",cclでコメント行の削除
nmap ,ccl :%s:^\("\\|#\\\|\*\).*$\n:<CR>
",cdで現在編集中のファイルのあるディレクトリに変更
nmap ,cd :cd %:h<CR>

"コマンドモード時にカーソル移動するのに便利
cnoremap <C-A> <Home>
cnoremap <C-B> <Left>
cnoremap <C-D> <Delete>
cnoremap <C-E> <End>
cnoremap <C-F> <Right>
cnoremap <C-N> <Down>
cnoremap <C-P> <Up>

"<ESC>hでハイライトをOFFにする
nmap <ESC><ESC> :noh<CR>

noremap j gj
noremap k gk
noremap <S-h> ^
noremap <S-j> }
noremap <S-k> {
noremap <S-l> $
noremap <Space> <PageDown>
noremap <S-Space> <PageUp>

"---NeoBundle set up---
"set nocompatible
"filetype plugin indent off
"
"if has('vim_starting')
"  set runtimepath+=~/.vim/bundle/neobundle.vim
"  call neobundle#begin(expand('~/.vim/bundle'))
"  "call neobundle#rc(expand('~/.vim/bundle'))
"
"  "GitHubリポジトリにあるプラグインを利用場合
"  NeoBundle 'tpope/vim-fugitive'
"  
"  "GitHub以外のGitリポジトリにあるプラグインを利用する場合
"  NeoBundle 'git://git.wincent.com/command-t.git'
"  
"  "Git以外のリポジトリにあるプラグインをを利用する場合
"  NeoBundle 'http://svn.macports.org/repository/macports/contrib/mpvim/'
"  NeoBundle 'https://bitbucket.org/ns9tks/vim-fuzzyfinder'
"  
"  " solarized
"  NeoBundle 'altercation/vim-colors-solarized'
"  " mustang
"  NeoBundle 'croaker/mustang-vim'
"  " wombat
"  NeoBundle 'jeffreyiacono/vim-colors-wombat'
"  " jellybeans
"  NeoBundle 'nanotech/jellybeans.vim'
"  " lucius
"  NeoBundle 'vim-scripts/Lucius'
"  " zenburn
"  NeoBundle 'vim-scripts/Zenburn'
"  " mrkn256
"  NeoBundle 'mrkn/mrkn256.vim'
"  " railscasts
"  NeoBundle 'jpo/vim-railscasts-theme'
"  " pyte
"  NeoBundle 'therubymug/vim-pyte'
"  " molokai
"  NeoBundle 'tomasr/molokai'
"  
"  "カラースキーム一覧表示にUnite.vimを使う
"  NeoBundle 'Shougo/unite.vim'
"  NeoBundle 'ujihisa/unite-colorscheme'
"
"
"endif 
"
"NeoBundleFetch 'Shougo/neobundle.vim'
"
"filetype plugin indent on
"
""ターミナルでも256色を用いてカラースキームを表示する
"if !has('gui_running') && filereadable($HOME . '/.vim/plugin/guicolorscheme.vim') && $TERM_PROGRAM ==# 'Apple_Terminal'
"    autocmd VimEnter * :GuiColorScheme badwolf
"elseif has('mac')
"    colorscheme badwolf
"else
"    "colorscheme pyte
"    colorscheme pablo
"endif

syntax enable

set nowritebackup
set nobackup
set noswapfile

set colorcolumn=100
