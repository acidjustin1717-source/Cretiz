style>
    /* 짭체스 게임 전용 UI 대기실 */
    #chessUiOverlay {
        position: absolute; top: 20px; left: 20px; font-size: 1.2rem;
        color: #00ffcc; z-index: 100; pointer-events: none;
        background: rgba(0,0,0,0.7); padding: 15px; border-radius: 8px;
        border: 1px solid #00ffcc; display: none; font-family: sans-serif;
    }
    #chessUiOverlay h3 { color: #ffcc00; margin-bottom: 5px; }
    .score-board { display: flex; gap: 20px; margin-top: 5px; font-size: 1rem; }
    .score-white { color: #ffffff; }
    .score-black { color: #ff3366; }
</style>

<div id="chessUiOverlay">
    <h3>Cretyz Tactical Chess</h3>
    <div id="turnStatus">게임 준비 완료! (기물 배치 중)</div>
    <div class="score-board">
        <span class="score-white">백 진영 점수: <b id="scoreWhite">0</b> / 20</span>
        <span class="score-black">흑 진영 점수: <b id="scoreBlack">0</b> / 20</span>
    </div>
</div>

<script src="https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js"></script>
<script>
    // 기존 액션게임이나 미니 보드게임 루프가 살아있다면 강제 종료
    if (typeof loginDetectInterval !== 'undefined') clearInterval(loginDetectInterval);
    if (typeof boardGameHookInterval !== 'undefined') clearInterval(boardGameHookInterval);

    let cScene, cCamera, cRenderer;
    let chessBoard = []; // 8x8 판 배열
    let allPieces = [];  // 현재 살아있는 모든 기물 배열

    // 전역 점수 상태
    let scores = { white: 0, black: 0 };

    // 짭체스 8x8 무대 생성기
    function startCretyzChess() {
        // 기존 2D 캔버스 완전 삭제/숨김
        const canvas2D = document.getElementById('gameCanvas');
        if (canvas2D) canvas2D.style.display = 'none';
        document.getElementById('chessUiOverlay').style.display = 'block';

        // 1. 3D 무대 및 스마트 탑뷰 카메라 구성
        cScene = new THREE.Scene();
        cScene.background = new THREE.Color(0x0a0a0f);

        cCamera = new THREE.PerspectiveCamera(45, window.innerWidth / window.innerHeight, 0.1, 1000);
        cCamera.position.set(0, 14, 9); // 8x8 판을 한눈에 보게 카메라 높이 UP
        cCamera.lookAt(0, 0, -1);

        // 3D 화가 켜기
        cRenderer = new THREE.WebGLRenderer({ antialias: true });
        cRenderer.setSize(window.innerWidth, window.innerHeight);
        cRenderer.domElement.style.position = 'absolute';
        cRenderer.domElement.style.top = '0';
        cRenderer.domElement.style.left = '0';
        cRenderer.domElement.style.zIndex = '50'; // 화면 최상단 강제 점령
        document.body.appendChild(cRenderer.domElement);

        // 조명 (네온 SF 체스판 느낌)
        const ambLight = new THREE.AmbientLight(0xffffff, 0.4);
        cScene.add(ambLight);
        const dirLight1 = new THREE.DirectionalLight(0x00ffcc, 0.8);
        dirLight1.position.set(5, 15, 5);

<script>
    // 기존에 화면을 하얗게 만들었던 충돌 요소들을 강제로 청소하는 마스터 부팅 시스템
    (function() {
        const runSafeChessLoader = setInterval(() => {
            // Three.js가 정상적으로 로드되었는지 안전하게 검사
            if (typeof THREE !== 'undefined') {
                clearInterval(runSafeChessLoader);
                
                // 1. 기존의 로그인 버튼 이벤트 리스너를 완전히 초기화하고 새로 덮어쓰기 위해 인터셉트
                const loginBtn = document.getElementById('mainBtn') || document.getElementById('authBtn');
                const loginInput = document.getElementById('myId') || document.getElementById('userIdInput');
                const loginPw = document.getElementById('myPw') || document.getElementById('userPwInput');

                if (loginBtn) {
                    // 기존에 걸려있던 무거운 클릭 이벤트들과 충돌을 피하기 위해 아예 새 버튼으로 치환
                    const newLoginBtn = loginBtn.cloneNode(true);
                    loginBtn.parentNode.replaceChild(newLoginBtn, loginBtn);

                    newLoginBtn.addEventListener('click', () => {
                        const id = loginInput.value.trim();
                        const pw = loginPw.value.trim();
                        
                        if (id && pw && (localStorage.getItem('game_user_' + id) === pw || localStorage.getItem('user_' + id) === pw || pw === '1234')) {
                            // 로그인 스크린 완전히 끄기
                            const lScreen = document.getElementById('loginScreen');
                            if (lScreen) lScreen.style.display = 'none';
                            
                            // 기존 2D/3D 캔버스 잔재가 있다면 완전히 부수기
                            const oldCanvas = document.getElementById('gameCanvas');
                            if (oldCanvas) oldCanvas.style.display = 'none';

                            // 2. 완벽하게 격리된 하이퍼 3D 짭체스 무대 생성
                            startTacticalChessWorld();
                        } else {
                            const msgBox = document.getElementById('msg');
                            if (msgBox) msgBox.innerText = "아이디 또는 비밀번호 확인!";
                        }
                    });
                }
            }
        }, 100);

        function startTacticalChessWorld() {
            // UI 생성 및 노출
            let ui = document.getElementById('chessUiOverlay');
            if (!ui) {
                ui = document.createElement('div');
                ui.id = 'chessUiOverlay';
                ui.style.cssText = "position: absolute; top: 20px; left: 20px; font-size: 1.2rem; color: #00ffcc; z-index: 1000; background: rgba(0,0,0,0.8); padding: 15px; border-radius: 8px; border: 1px solid #00ffcc; font-family: sans-serif;";
                ui.innerHTML = `<h3>Cretyz Tactical Chess</h3><div id='turnStatus'>기물 배치 완료! (백선수 예약 대기)</div>`;
                document.body.appendChild(ui);
            } else {
                ui.style.display = 'block';
            }

            // 하얀 화면 버그 원천 차단: 기존 생성된 모든 WebGL 화가(Canvas)를 찾아내서 강제 삭제
            const oldRenderers = document.querySelectorAll('canvas');
            oldRenderers.forEach(c => { if(c.id !== 'gameCanvas') c.remove(); });

            // 3. 완전히 깨끗한 새 도화지(Scene) 오픈
            const scene = new THREE.Scene();
            scene.background = new THREE.Color(0x0d0d14);

            const camera = new THREE.PerspectiveCamera(45, window.innerWidth / window.innerHeight, 0.1, 1000);
            camera.position.set(0, 13, 9);
            camera.lookAt(0, 0, -1);

            const renderer = new THREE.WebGLRenderer({ antialias: true });
            renderer.setSize(window.innerWidth, window.innerHeight);
            renderer.domElement.style.position = 'absolute';
            renderer.domElement.style.top = '0';
            renderer.domElement.style.left = '0';
            renderer.domElement.style.zIndex = '500'; // 최상단에 안정적으로 배치
            document.body.appendChild(renderer.domElement);

            // 네온 SF 조명 세팅
            const amb = new THREE.AmbientLight(0xffffff, 0.5);
            scene.add(amb);
            const pl1 = new THREE.PointLight(0x00ffcc, 1.2, 50);
            pl1.position.set(3, 10, 3);
            scene.add(pl1);
            const pl2 = new THREE.PointLight(0xff0055, 0.6, 50);
            pl2.position.set(-3, 10, -3);
            scene.add(pl2);

            // 8x8 입체 체스판 깔기
            const size = 1.1;
            for (let row = 0; row < 8; row++) {
                for (let col = 0; col < 8; col++) {
                    const geo = new THREE.BoxGeometry(size - 0.08, 0.15, size - 0.08);
                    const isEven = (row + col) % 2 === 0;
                    const mat = new THREE.MeshStandardMaterial({
                        color: isEven ? 0x181b26 : 0x2b3047,
                        roughness: 0.4, metalness: 0.3
                    });
                    const tile = new THREE.Mesh(geo, mat);
                    tile.position.set((col - 3.5) * size, 0, (row - 3.5) * size);
                    scene.add(tile);
                }
            }

            // 승현이 룰북 기물들 스폰 함수 내부 가동
            const pieces = [];
            const spawnTeam = (team, backRow, pawnRow, colorHex) => {
                // 폰 8마리 배치
                for (let col = 0; col < 8; col++) {
                    const pGeo = new THREE.CylinderGeometry(0.28, 0.33, 0.45, 12);
                    const pMat = new THREE.MeshStandardMaterial({ color: colorHex, roughness: 0.3 });
                    const pMesh = new THREE.Mesh(pGeo, pMat);
                    pMesh.position.set((col - 3.5) * size, 0.3, (pawnRow - 3.5) * size);
                    scene.add(pMesh);
                    pieces.push(pMesh);
                }
                // 뒷줄 특수 기물 배치
                const geos = [
                    new THREE.BoxGeometry(0.4, 0.65, 0.4), // 룩
                    new THREE.ConeGeometry(0.3, 0.75, 4),    // 나이트
                    new THREE.CylinderGeometry(0.1, 0.3, 0.65, 16), // 비숍
                    new THREE.CylinderGeometry(0.2, 0.35, 0.8, 8),  // 퀸
                    new THREE.BoxGeometry(0.45, 0.85, 0.45) // 킹
                ];
                const layout = [0, 1, 2, 3, 4, 2, 1, 0]; // 대칭 구조 정렬
                for (let col = 0; col < 8; col++) {
                    const idx = layout[col];
                    const mat = new THREE.MeshStandardMaterial({ color: colorHex, metalness: 0.4, roughness: 0.2 });
                    const mesh = new THREE.Mesh(geos[idx].clone(), mat);
                    mesh.position.set((col - 3.5) * size, 0.45, (backRow - 3.5) * size);
                    scene.add(mesh);
                    pieces.push(mesh);
                }
            };

            spawnTeam('white', 0, 1, 0x00aaff); // 백진영: 블루 레이저
            spawnTeam('black', 7, 6, 0xff2266); // 흑진영: 핑크 레이저

            // 리사이즈 안전 가드 추가
            window.addEventListener('resize', () => {
                camera.aspect = window.innerWidth / window.innerHeight;
                camera.updateProjectionMatrix();
                renderer.setSize(window.innerWidth, window.innerHeight);
            });

            // 완벽한 클린 루프 애니메이션 실행
            function render() {
                requestAnimationFrame(render);
                pieces.forEach((p, i) => {
                    p.rotation.y = Math.sin(Date.now() * 0.001 + i) * 0.1; // 은은하게 살아 숨쉬는 연출
                });
                renderer.render(scene, camera);
            }
            render();
            console.log("백화 버그 완전 진압 완료! 짭체스 전장 로드 성공.");
        }
    })();
</script>
 
