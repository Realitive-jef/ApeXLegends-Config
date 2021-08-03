# 目的:最適化と軽量化をしてフレームレートの向上を図る
## LanchArgument (steam/origin)
|引数|内容|
|:--|--:|
|-fullscreen|起動時にフルスクリーンモードにする。|
|-novid|起動時のソースエンジンのムービーを飛ばす。|
|+exec autoexec|自動読み込み設定をロードする。|
|-preload|ゲーム開始時に様々なものをロードすることで、パフォーマンスが向上する。|
|+m_rawinput 1|マウスの入力がWindowsを介さずに直接ゲームに反映される。|
|-forcenovsync|垂直同期をオフにする。|
|-refresh 144|リフレッシュレートを144Hzにする。|
|-high|CPU使用率を高にする。|
|+fps_max 0|0でフレームレートの上限をなくす。|
|+cl_showfps 4|ゲームのフレームレートを表示する|

## Config Files (steam/origin)
|パス|主な設定項目|
|:--|--:|
|%USERPROFILE%\SavedGames\Respawn\Apex\profile\profile.cfg|cl_fovScale|
|%USERPROFILE%\SavedGames\Respawn\Apex\local\settings.cfg|mouse_sensitivity mouse_zoomed_sensitivity_scalar_0|
|%USERPROFILE%\SavedGames\Respawn\Apex\local\videoconfig.txt|setting.defaultres setting.defaultresheight|

## Videoconfig.txt  (steam/origin)
- Videoconfig.txtの中に以下の記述を追加する

|設定項目|内容|
|:--|--:|
|"mat_disable_bloom" "1"|ブルームの無効化|
|"mat_specular" "0"|スぺキュラマップの使用|
|"mat_bumpmap" "0"|バンプマップの使用|
|"r_dynamic" "0" |ダイナミックエフェクトの使用|

- さらに最適化するには・・・（任意）

`"setting.dvs_enable" "0"`を`"1"`へ変更する

次に

gpuframetime_min と gpuframetime_max の値を変更する

setting.dvs_gpuframetime_max = 1/target framerate*1000000 <br>
setting.dvs_gpuframetime_min = (setting.dvs_gpuframetime_max * 0.97) 

144Hzなら

`"setting.dvs_gpuframetime_min"      "6735"`<br>
`"setting.dvs_gpuframetime_max"      "6944"`

に設定する （この数値は小さいほど描画品質は劣化するが軽量化に大きく左右する）

`"setting.stream_memory"`は`"5000"`がテクスチャが潰れない最低ライン
（0が最軽量ではあるがテクスチャが潰れる。VRAMが足りてないとかではない限りパフォーマンスにはほぼ影響しないはず？)

## Disable Origin Overlay (origin)
Originを起動→左上の「Origin」から「アプリケーション設定」→ORIGIN IN-GAMEのタブ→「Origin In-Gameを有効にする」のチェックを外す


## その他(Tips)
- FOV120 / paste this into autoexec- <br>
`cl_fovScale "1.7"` [CALCULATOR](https://jscalc.io/embed/Q1gf45VCY4tmm2dq?utm_medium=referral&utm_campaign=JSCalc%20Blog&utm_source=JSCalc%20blog)
