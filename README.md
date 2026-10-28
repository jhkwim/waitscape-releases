# Waitscape 받기 / Download

AI 코딩 에이전트 세션을 귀여운 픽셀 화면으로 보여 주는 데스크톱 앱 **Waitscape**의 설치 파일을 올리는 곳입니다.
This repository only hosts **Waitscape** installers and update files.

👉 **[최신 버전 받기 / Latest release](https://github.com/jhkwim/waitscape-releases/releases/latest)**

소스 코드·이슈·기여 / Source code, issues and contributing: **[jhkwim/waitscape](https://github.com/jhkwim/waitscape)**

| | 파일 |
|---|---|
| macOS 13+ (Apple 칩·Intel) | `Waitscape_x.y.z_universal.dmg` |
| Windows 10 1809+ (x64) | `Waitscape_x.y.z_x64-setup.exe` (또는 `.msi`) |

설치된 앱은 이 저장소의 `latest.json`만 읽어 새 버전을 알려 줍니다(보내는 것: IP·User-Agent). [지금 업데이트하고 다시 시작]을 누를 때만 내려받고 서명을 확인한 뒤 설치합니다.

## 한국어

설치 파일은 아직 **코드 서명·공증이 되어 있지 않아** 처음 열 때 OS가 경고를 띄웁니다.

### 체크섬 확인 (권장)
`SHA256SUMS.txt`를 같은 폴더에 두고:
- macOS: `shasum -a 256 -c SHA256SUMS.txt --ignore-missing`
- Windows (PowerShell): `Get-FileHash .\<파일이름> -Algorithm SHA256` 결과를 `SHA256SUMS.txt`의 해당 줄과 비교

### macOS
1. `.dmg`를 열고 Waitscape를 응용 프로그램 폴더로 끌어다 놓습니다.
2. 경고가 나오면 **시스템 설정 → 개인정보 보호 및 보안** 아래쪽 "Waitscape이(가) 차단되었습니다" 옆 **그래도 열기**. (또는 우클릭 → 열기 → 열기)
3. 그래도 "손상되었다"고 나오면: `xattr -dr com.apple.quarantine /Applications/Waitscape.app`

### Windows
1. `.exe`(사용자 단위 설치) 또는 `.msi`를 실행합니다.
2. "Windows의 PC 보호" 창이 뜨면 **추가 정보 → 실행**.

### 업데이트
앱이 시작할 때와 하루 1번 새 버전을 확인합니다. 설정 → 일반 → 업데이트에서 끌 수 있습니다. 앱 안 업데이트가 안 되는 옛 버전은 새 설치 파일을 그대로 덮어 설치하면 됩니다(데이터 유지).

## English

Installers are **not code-signed or notarized yet**, so the OS warns on first launch.

- **Checksum:** put `SHA256SUMS.txt` next to the download and run `shasum -a 256 -c SHA256SUMS.txt --ignore-missing` (macOS) or compare `Get-FileHash` output (Windows).
- **macOS:** drag Waitscape to Applications. If blocked, use **System Settings → Privacy & Security → Open Anyway**. If it says "damaged": `xattr -dr com.apple.quarantine /Applications/Waitscape.app`
- **Windows:** run the `.exe` or `.msi`; on SmartScreen click **More info → Run anyway**.
- **Updates:** the app checks this repository's `latest.json` at start and once a day, and installs only when you press **Update now and restart** (signature verified). Turn it off in Settings → General → Updates.
