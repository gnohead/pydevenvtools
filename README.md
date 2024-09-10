# Python development environment tools

이 저장소에는 Python 개발을 하다가 필요하게 되었던 매번 만들어쓰기는 귀찮아도 있으면 편리한 도구들을 모아놓았습니다. 지극히 개인적인 용도로 공유하기 위한 도구이므로 상황에 따라 알맞게 개조하여 활용해야합니다.

## virtualenv 자동 구축 도구

다음 스크립트는 윈도우 시스템의 `PowerShell`과 Linux/Unix 계열 시스템의 `bash` 에서 Python virtualenv 개발 환경을 빠르게 설정할 수 있도록 도와줍니다.

- `env.sh`: Linux/Unix 계열 시스템에서 Python virtualenv 구축 및 activate를 위한 bash 스크립트
- `env.ps1`: Windows PowerShell에서 Python virtualenv 구축 및 activate를 위한 bash 스크립트

### 참고

- 쉘에서 `python3.11` 또는 `python` 과 같이 명령어로 실행할 수 있는 환경에서만 동작합니다.
- `pip`으로 `virtualenv` 설치 및 `requirements.txt`를 통한 환경을 구축하므로 기본적으로 pip(pypi) 저장소 서버와 통신 가능한 네트워크 환경이 필요합니다.
- 스크립트를 통해 virtualenv 에 진입 할 때, `env.conf` 의 환경변수는 `bash`쉘에서만 자동으로 등록됩니다.
- 스크립트를 실행하기 전에 스크립트 내부의 환경 변수나 경로 설정을 프로젝트 환경에 맞게 수정해야 할 수 있습니다.
- PowerShell의 실행 정책에 따라 스크립트를 실행할 수 없는 경우, 위의 명령어로 실행 정책을 변경해야 합니다.

### 스크립트 설명

#### 1. `env.sh` (Linux/Unix)

이 스크립트는 Linux 또는 Unix 기반 시스템에서 사용됩니다. 프로젝트의 환경 변수를 설정하고, 필요한 의존성을 설치하거나 초기화할 때 사용됩니다.

##### 사용 방법:

1. 스크립트에 실행 권한 부여:
   ```bash
   chmod +x env.sh
   ```

2. 스크립트 실행:
   ```bash
   ./env.sh
   ```

스크립트는 시스템의 쉘 환경에 여러 설정을 적용하여 프로젝트가 원활히 동작할 수 있도록 지원합니다.

#### 2. `env.ps1` (Windows PowerShell)

이 스크립트는 Windows PowerShell 환경에서 실행됩니다. Windows 시스템에서 프로젝트 개발 환경을 자동으로 설정하고 필요한 의존성을 구성합니다.

##### 사용 방법:

1. PowerShell에서 스크립트 실행 권한을 설정합니다 (필요한 경우):
   ```powershell
   Set-ExecutionPolicy RemoteSigned -Scope CurrentUser
   ```

2. 스크립트 실행:
   ```powershell
   ./env.ps1
   ```

스크립트는 Windows PowerShell 환경에서 필요한 환경 변수를 설정하고, 초기 설정 작업을 자동화합니다.

## 라이선스

이 프로젝트는 MIT 라이선스 하에 제공됩니다. 자세한 내용은 `LICENSE` 파일을 참조하십시오.
