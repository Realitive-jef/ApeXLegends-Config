# 目的:最適化と軽量化をしてフレームレートの向上を図る
## LanchArgument (steam/origin)
- -fullscreen：起動時にフルスクリーンモードにする。
- -novid：起動時のソースエンジンのムービーを飛ばす。
- +exec autoexec：自動読み込み設定をロードする。
- -preload：ゲーム開始時に様々なものをロードすることで、パフォーマンスが向上する。
- +m_rawinput 1：マウスの入力がWindowsを介さずに直接ゲームに反映される。
- -forcenovsync：垂直同期をオフにする。
- -refresh 144：リフレッシュレートを144Hzにする。
- -high：CPU使用率を高にする。
- +fps_max 0：0でフレームレートの上限をなくす。
- +cl_showfps 4：ゲームのフレームレートを表示する

## Config Files (steam/origin)
|Directory|Variable|
|:--|--:|
|%USERPROFILE%\SavedGames\Respawn\Apex\profile\profile.cfg|cl_fovScale|
|%USERPROFILE%\SavedGames\Respawn\Apex\local\settings.cfg|mouse_sensitivity mouse_zoomed_sensitivity_scalar_0|
|%USERPROFILE%\SavedGames\Respawn\Apex\local\videoconfig.txt|setting.defaultres setting.defaultresheight|

## Disable Origin Overlay (origin)
Originを起動→左上の「Origin」から「アプリケーション設定」→ORIGIN IN-GAMEのタブ→「Origin In-Gameを有効にする」のチェックを外す


# その他(Tips)
- FOV120 / paste this into autoexec- <br>
`cl_fovScale "1.7"` [CALCULATOR](https://jscalc.io/embed/Q1gf45VCY4tmm2dq?utm_medium=referral&utm_campaign=JSCalc%20Blog&utm_source=JSCalc%20blog)
