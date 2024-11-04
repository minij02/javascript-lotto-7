## 기능 목록

### 1. 입력 처리
- **구입 금액 입력**: 사용자는 1,000원 단위의 구입 금액을 입력할 수 있습니다.
  - 예외 처리: 1,000원 단위가 아닌 금액을 입력할 경우 `[ERROR] 구입 금액은 1,000원 단위여야 합니다.` 메시지를 출력하고 재입력을 요청합니다.
- **당첨 번호 입력**: 쉼표로 구분된 6개의 당첨 번호를 입력받습니다.
  - 예외 처리: 중복된 번호가 있거나 숫자가 1~45 범위를 벗어날 경우 `[ERROR] 로또 번호는 중복 없이 1부터 45 사이의 숫자여야 합니다.` 메시지를 출력합니다.
- **보너스 번호 입력**: 단일 숫자의 보너스 번호를 입력받습니다.
  - 예외 처리: 보너스 번호가 1~45 범위를 벗어나거나 당첨 번호와 중복되거나 여러 개의 보너스 번호가 입력된 경우 `[ERROR] 보너스 번호는 1부터 45 사이의 숫자이며, 당첨 번호와 중복되면 안 됩니다.` 메시지를 출력합니다.

### 2. 로또 발행
- 구입 금액에 따라 1,000원당 1개의 로또 번호를 발행합니다.
- 각 로또는 1~45 사이의 중복되지 않는 6개의 숫자로 구성됩니다.

### 3. 당첨 결과 계산
- 각 로또 번호를 당첨 번호와 비교하여 일치하는 숫자의 개수를 계산합니다.
- 보너스 번호 일치 여부를 확인하여 2등 결과를 처리합니다.

### 4. 당첨 통계 출력
- 일치하는 숫자 개수에 따라 3개, 4개, 5개, 5개+보너스, 6개 일치의 결과를 출력합니다.
- 각 당첨 개수는 적절한 포맷으로 출력됩니다. 예: `3개 일치 (5,000원) - 1개`
- 총 수익률을 소수점 둘째 자리까지 반올림하여 출력합니다. 예: `총 수익률은 62.5%입니다.`

### 5. 예외 상황 처리
- 모든 입력 및 처리 과정에서 예외 발생 시 `[ERROR]`로 시작하는 메시지를 출력하고 프로그램을 재시작합니다.