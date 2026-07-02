<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>앙상블 스타즈 재화 계산기 (단계별 버전)</title>
    <style>
        body { font-family: 'Malgun Gothic', sans-serif; background-color: #f4f7f6; color: #333; padding: 20px; margin: 0; }
        .container { max-width: 600px; margin: 0 auto; background: white; padding: 25px; border-radius: 15px; box-shadow: 0 4px 15px rgba(0,0,0,0.1); }
        h2 { text-align: center; color: #00bcd4; margin-bottom: 25px; }
        
        /* 단계(Step) 제어 */
        .step-panel { display: none; }
        .step-panel.active { display: block; }
        
        .form-group { margin-bottom: 15px; display: flex; flex-direction: column; }
        label { font-weight: bold; margin-bottom: 5px; color: #555; }
        input[type="date"] { padding: 10px; border: 1px solid #ddd; border-radius: 8px; font-size: 16px; }
        
        .pack-selection { background: #fafafa; border: 1px solid #e0e0e0; border-radius: 10px; padding: 15px; margin-bottom: 20px; }
        .pack-header { display: flex; justify-content: space-between; align-items: center; margin-bottom: 12px; }
        .pack-title { font-weight: bold; color: #00bcd4; font-size: 15px; margin: 0; }
        
        .btn-max-all { background-color: #e0f7fa; color: #00838f; border: 1px solid #00bcd4; padding: 5px 10px; border-radius: 5px; font-size: 12px; font-weight: bold; cursor: pointer; }
        .btn-max-all:hover { background-color: #b2ebf2; }

        .count-group { display: flex; flex-direction: column; gap: 12px; }
        .count-item { display: flex; align-items: center; justify-content: space-between; font-size: 14px; background: #fff; padding: 10px; border-radius: 6px; border: 1px solid #eee; }
        .count-label { display: flex; flex-direction: column; gap: 2px; }
        .count-label span.title { font-weight: bold; color: #333; }
        .count-label span.desc { font-size: 11px; color: #888; }
        .count-label span.max-hint { font-size: 11px; color: #e53935; font-weight: bold; }
        
        .input-counter { display: flex; align-items: center; gap: 5px; }
        .input-counter input { width: 50px; padding: 6px; text-align: center; border: 1px solid #ccc; border-radius: 4px; font-size: 14px; }
        .input-counter span.unit { font-size: 13px; color: #555; font-weight: bold; }

        .btn-group { display: flex; gap: 10px; margin-top: 20px; }
        button { background-color: #00bcd4; color: white; border: none; padding: 12px; border-radius: 8px; font-size: 16px; font-weight: bold; cursor: pointer; transition: 0.2s; flex: 1; }
        button:hover { background-color: #0097a7; }
        button.btn-prev { background-color: #b0bec5; }
        button.btn-prev:hover { background-color: #90a4ae; }
        
        .result-box { padding: 20px; background-color: #e0f7fa; border-radius: 10px; border-left: 5px solid #00bcd4; }
        .result-title { font-size: 18px; font-weight: bold; margin-bottom: 15px; color: #006064; border-bottom: 1px solid #b2ebf2; padding-bottom: 5px; }
        .result-item { display: flex; justify-content: space-between; margin-bottom: 10px; font-size: 15px; }
        .result-item span.value { font-weight: bold; color: #004d40; }
        .total-cost { font-size: 18px; font-weight: bold; color: #d32f2f; border-top: 1px dashed #b2ebf2; padding-top: 10px; margin-top: 10px; }
        
        /* 상세 영수증 스타일 */
        .breakdown-box { margin-top: 20px; padding: 15px; background-color: #f9f9f9; border-radius: 10px; border: 1px dashed #ccc; font-size: 13px; color: #555; line-height: 1.6; }
        .breakdown-title { font-weight: bold; color: #333; margin-bottom: 8px; font-size: 14px; border-bottom: 1px solid #eee; padding-bottom: 4px; }
        .breakdown-section { margin-bottom: 10px; }
        .breakdown-section-title { font-weight: bold; color: #00bcd4; margin-bottom: 2px; }
    </style>
</head>
<body>

<div class="container">
    <h2>✨ 앙스타 재화 예측 계산기 ✨</h2>
    
    <div class="step-panel active" id="step1">
        <div class="form-group">
            <label for="startDate">시작 날짜</label>
            <input type="date" id="startDate">
        </div>
        <div class="form-group">
            <label for="endDate">종료 날짜</label>
            <input type="date" id="endDate">
        </div>
        <div class="btn-group">
            <button onclick="nextStep(2)">다음 단계로 (패키지 설정) ➡️</button>
        </div>
    </div>

    <div class="step-panel" id="step2">
        <div class="pack-selection">
            <div class="pack-header">
                <div class="pack-title">🛍️ 패키지 구매 횟수 설정</div>
                <button class="btn-max-all" onclick="setAllMax()">슬롯 모두 Max 설정 ⚡</button>
            </div>
            <div class="count-group">
                <div class="count-item">
                    <div class="count-label">
                        <span class="title">깜짝 스카우트 패키지 (4,500원)</span>
                        <span class="max-hint" id="maxSurpriseHint">달력 기준 최대: 0회</span>
                    </div>
                    <div class="input-counter">
                        <input type="number" id="cntSurprise" value="0" min="0">
                        <span class="unit">번</span>
                    </div>
                </div>
                
                <div class="count-item">
                    <div class="count-label">
                        <span class="title">응원 멤버십 (30,000원)</span>
                        <span class="max-hint" id="maxCheerHint">달력 기준 최대: 0회</span>
                    </div>
                    <div class="input-counter">
                        <input type="number" id="cntCheer" value="0" min="0">
                        <span class="unit">번</span>
                    </div>
                </div>
                
                <div class="count-item">
                    <div class="count-label">
                        <span class="title">다이아 멤버십 (7,500원)</span>
                        <span class="max-hint" id="maxDiaHint">달력 기준 최대: 0회</span>
                    </div>
                    <div class="input-counter">
                        <input type="number" id="cntDia" value="0" min="0">
                        <span class="unit">번</span>
                    </div>
                </div>
                
                <div class="count-item">
                    <div class="count-label">
                        <span class="title">핵심 업무 계획 (14,000원)</span>
                        <span class="max-hint" id="maxCoreHint">달력 기준 최대: 0회</span>
                    </div>
                    <div class="input-counter">
                        <input type="number" id="cntCore" value="0" min="0">
                        <span class="unit">번</span>
                    </div>
                </div>
            </div>
        </div>
        <div class="btn-group">
            <button class="btn-prev" onclick="prevStep(1)">⬅️ 이전으로</button>
            <button onclick="calculateResources()">결과 보기 📊</button>
        </div>
    </div>

    <div class="step-panel" id="step3">
        <div class="result-box">
            <div class="result-title">📊 예상 획득 재화 & 비용 결과</div>
            <div class="result-item"><span>총 기간:</span><span class="value" id="resPeriod">0일 / 0주 / 0개월</span></div>
            <hr style="border: 0; border-top: 1px solid #b2ebf2; margin: 15px 0;">
            <div class="result-item"><span>💎 유료 다이아:</span><span class="value" id="resPaidDia">0개</span></div>
            <div class="result-item"><span>💎 무료 다이아:</span><span class="value" id="resFreeDia">0개</span></div>
            <div class="result-item"><span>🎫 다이아 티켓:</span><span class="value" id="resTickets">0개</span></div>
            <div class="result-item"><span>🃏 더블 카드:</span><span class="value" id="resDoubleCards">0개</span></div>
            <div class="result-item total-cost"><span>💰 총 소요 비용:</span><span id="resCost">0원</span></div>
        </div>
        
        <div class="breakdown-box" id="breakdownBox">
            </div>

        <div class="btn-group">
            <button class="btn-prev" onclick="prevStep(2)">⬅️ 조건 수정하기</button>
            <button onclick="nextStep(1)">처음부터 다시하기 🔄</button>
        </div>
    </div>
</div>

<script>
const birthdays = [
    { m: 1, d: 4 }, { m: 1, d: 10 }, { m: 1, d: 13 }, { m: 1, d: 26 },
    { m: 2, d: 4 }, { m: 2, d: 5 }, { m: 2, d: 21 }, { m: 2, d: 25 },
    { m: 3, d: 3 }, { m: 3, d: 5 }, { m: 3, d: 16 }, { m: 3, d: 29 },
    { m: 4, d: 6 }, { m: 4, d: 20 }, { m: 4, d: 27 }, { m: 4, d: 30 },
    { m: 5, d: 5 }, { m: 5, d: 16 }, { m: 5, d: 18 }, { m: 5, d: 22 },
    { m: 6, d: 1 },
    { m: 6, d: 6 }, { m: 6, d: 9 }, { m: 6, d: 15 }, { m: 6, d: 22 },
    { m: 7, d: 1 }, { m: 7, d: 7 }, { m: 7, d: 15 }, { m: 7, d: 18 }, { m: 7, d: 24 },
    { m: 8, d: 7 }, { m: 8, d: 16 }, { m: 8, d: 29 }, { m: 8, d: 30 },
    { m: 9, d: 6 }, { m: 9, d: 7 }, { m: 9, d: 12 },
    { m: 9, d: 18 }, { m: 9, d: 22 },
    { m: 10, d: 5 }, { m: 10, d: 18 }, { m: 10, d: 27 }, { m: 10, d: 30 },
    { m: 11, d: 2 }, { m: 11, d: 3 }, { m: 11, d: 14 }, { m: 11, d: 27 },
    { m: 12, d: 2 },
    { m: 12, d: 11 }, { m: 12, d: 17 }, { m: 12, d: 26 }, { m: 12, d: 28 }
];

document.getElementById('startDate').valueAsDate = new Date();
let tomorrow = new Date();
tomorrow.setDate(tomorrow.getDate() + 30);
document.getElementById('endDate').valueAsDate = tomorrow;

let maxCalculated = { surprise: 0, cheer: 0, dia: 0, core: 0 };

function showPanel(stepNum) {
    document.querySelectorAll('.step-panel').forEach(p => p.classList.remove('active'));
    document.getElementById('step' + stepNum).classList.add('active');
}

function prevStep(stepNum) {
    showPanel(stepNum);
}

function nextStep(stepNum) {
    if (stepNum === 2) {
        const startInput = document.getElementById('startDate').value;
        const endInput = document.getElementById('endDate').value;
        
        if (!startInput || !endInput) {
            alert("시작 날짜와 종료 날짜를 모두 선택해주세요!");
            return;
        }
        let start = new Date(startInput);
        let end = new Date(endInput);
        if (start > end) {
            alert("종료 날짜는 시작 날짜보다 미래여야 합니다.");
            return;
        }
        
        // 가예산 루프 돌려서 Max 가이드 한계값 먼저 뽑기
        preCalculateMaxLimits(start, end);
    }
    showPanel(stepNum);
}

// 캘린더 일수 기준 가입 제한 횟수 한계 측정 함수
function preCalculateMaxLimits(start, end) {
    let days = 0;
    let weeks = 0;
    let months = 0;
    let current = new Date(start);
    let previousMonth = -1;
    
    while(current <= end) {
        days++;
        if (days === 1 || current.getDay() === 1) { weeks++; }
        let currentMonth = current.getFullYear() * 12 + current.getMonth();
        if (currentMonth !== previousMonth) { months++; previousMonth = currentMonth; }
        current.setDate(current.getDate() + 1);
    }
    
    maxCalculated.surprise = weeks;
    maxCalculated.cheer = Math.ceil(days / 30);
    maxCalculated.dia = Math.ceil(days / 30);
    maxCalculated.core = months;
    
    document.getElementById('maxSurpriseHint').innerText = `달력 기준 최대 추천: ${maxCalculated.surprise}회`;
    document.getElementById('maxCheerHint').innerText = `달력 기준 최대 추천: ${maxCalculated.cheer}회`;
    document.getElementById('maxDiaHint').innerText = `달력 기준 최대 추천: ${maxCalculated.dia}회`;
    document.getElementById('maxCoreHint').innerText = `달력 기준 최대 추천: ${maxCalculated.core}회`;
}

// 한번에 모든 값 최댓값 자동 매핑
function setAllMax() {
    document.getElementById('cntSurprise').value = maxCalculated.surprise;
    document.getElementById('cntCheer').value = maxCalculated.cheer;
    document.getElementById('cntDia').value = maxCalculated.dia;
    document.getElementById('cntCore').value = maxCalculated.core;
}

function calculateResources() {
    let start = new Date(document.getElementById('startDate').value);
    let end = new Date(document.getElementById('endDate').value);

    const cntSurprise = Math.max(0, parseInt(document.getElementById('cntSurprise').value) || 0);
    const cntCheer = Math.max(0, parseInt(document.getElementById('cntCheer').value) || 0);
    const cntDia = Math.max(0, parseInt(document.getElementById('cntDia').value) || 0);
    const cntCore = Math.max(0, parseInt(document.getElementById('cntCore').value) || 0);
    
    let totalDays = 0;
    let totalWeeks = 0;
    let totalMonths = 0;
    let birthdayCount = 0;
    
    let current = new Date(start);
    let previousMonth = -1;
    
    while (current <= end) {
        totalDays++;
        if (totalDays === 1 || current.getDay() === 1) { totalWeeks++; }
        let currentMonth = current.getFullYear() * 12 + current.getMonth();
        if (currentMonth !== previousMonth) { totalMonths++; previousMonth = currentMonth; }
        
        let m = current.getMonth() + 1;
        let d = current.getDate();
        birthdayCount += birthdays.filter(b => b.m === m && b.d === d).length;
        
        current.setDate(current.getDate() + 1);
    }
    
    // 계산식 조립 프로세스 시작
    let dailyFreeDiaSum = totalDays * 130; // 50+30+50
    let membershipDiaSum = Math.min(cntDia * 30, totalDays) * 150;
    let weeklyFreeDiaSum = totalWeeks * 350; // 250+100
    let coreFreeDiaSum = cntCore * 1000;
    let bdayFreeDiaSum = birthdayCount * 350;
    
    let totalFreeDia = dailyFreeDiaSum + membershipDiaSum + weeklyFreeDiaSum + coreFreeDiaSum + bdayFreeDiaSum;
    let totalPaidDia = (cntCheer * 1640) + (cntDia * 420);
    let totalTickets = (totalWeeks * 2) + (cntSurprise * 6) + (cntCore * 10);
    let totalDoubleCards = Math.min(cntCheer * 30, totalDays) * 15;
    let totalCost = (cntSurprise * 4500) + (cntCheer * 30000) + (cntDia * 7500) + (cntCore * 14000);

    // 상단 요약 매핑
    document.getElementById('resPeriod').innerText = `${totalDays}일 / ${totalWeeks}주 / ${totalMonths}개월 분량`;
    document.getElementById('resPaidDia').innerText = totalPaidDia.toLocaleString() + "개";
    document.getElementById('resFreeDia').innerText = totalFreeDia.toLocaleString() + "개";
    document.getElementById('resTickets').innerText = totalTickets.toLocaleString() + "개";
    document.getElementById('resDoubleCards').innerText = totalDoubleCards.toLocaleString() + "개";
    document.getElementById('resCost').innerText = totalCost.toLocaleString() + "원";
    
    // 하단 상세 설명 영수증 텍스트 빌드
    let breakdownHtml = `<div class="breakdown-title">🧾 어떻게 계산되었나요? (정밀 영수증)</div>`;
    
    // 1. 무료 다이아 상세
    breakdownHtml += `
    <div class="breakdown-section">
        <div class="breakdown-section-title">■ 무료 다이아 수식 총합: ${totalFreeDia.toLocaleString()}개</div>
        • 인게임 일일 기본 콘텐츠: ${totalDays}일 × 130개 (포토 50 + 별빛 30 + 솔로 50) = <b>${dailyFreeDiaSum.toLocaleString()}개</b><br>
        • 인게임 주간 기본 보상: ${totalWeeks}주 × 350개 (길드 250 + 공유 100) = <b>${weeklyFreeDiaSum.toLocaleString()}개</b><br>
        • 다이아 멤버십 매일 혜택: 보상 유효일 ${Math.min(cntDia * 30, totalDays)}일 × 150개 = <b>${membershipDiaSum.toLocaleString()}개</b><br>
        • 핵심 업무 계획 계약 보상: 구매 ${cntCore}회 × 1,000개 = <b>${coreFreeDiaSum.toLocaleString()}개</b><br>
        • 기간 내 아이돌 생일: 총 ${birthdayCount}명의 생일 × 350개 = <b>${bdayFreeDiaSum.toLocaleString()}개</b>
    </div>`;

    // 2. 다른 재화 상세
    breakdownHtml += `
    <div class="breakdown-section">
        <div class="breakdown-section-title">■ 다이아 티켓 & 더블 카드</div>
        • 다이아 티켓: 주간 무료 기본 (${totalWeeks * 2}개) + 깜짝팩 구매 (${cntSurprise * 6}개) + 핵심 계획 (${cntCore * 10}개) = <b>${totalTickets}개</b><br>
        • 더블 카드: 응원 멤버십 유효일 ${Math.min(cntCheer * 30, totalDays)}일 × 15개 = <b>${totalDoubleCards.toLocaleString()}개</b>
    </div>`;

    // 3. 결제 총액 상세
    breakdownHtml += `
    <div class="breakdown-section">
        <div class="breakdown-section-title">■ 소비 금액 계산 상세: ${totalCost.toLocaleString()}원</div>
        • 깜짝 스카우트: ${cntSurprise}회 × 4,500원 = ${(cntSurprise * 4500).toLocaleString()}원<br>
        • 응원 멤버십: ${cntCheer}회 × 30,000원 = ${(cntCheer * 30000).toLocaleString()}원<br>
        • 다이아 멤버십: ${cntDia}회 × 7,500원 = ${(cntDia * 7500).toLocaleString()}원<br>
        • 핵심 업무 계획: ${cntCore}회 × 14,000원 = ${(cntCore * 14000).toLocaleString()}원
    </div>`;
    
    document.getElementById('breakdownBox').innerHTML = breakdownHtml;
    showPanel(3);
}
</script>

</body>
</html>
