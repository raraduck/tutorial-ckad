# tutorial-ckad

```bash
# .bashrc

# 1. kubectl 자동완성 활성화
echo 'source <(kubectl completion bash)' >> ~/.bashrc

# 2. kubectl을 'k'로 줄여 쓰기
echo 'alias k=kubectl' >> ~/.bashrc

# 3. 'k'를 쳐도 kubectl처럼 자동완성이 먹히도록 연동 (매우 중요!)
echo 'complete -o default -F __start_kubectl k' >> ~/.bashrc

# 4. (강력 추천) dry-run 옵션 변수화 - YAML 파일 뽑아낼 때 타이핑 시간 단축
echo 'export do="--dry-run=client -o yaml"' >> ~/.bashrc

# 5. (강력 추천) 파드 강제 즉시 삭제 변수화 - 파드 지워질 때까지 기다리는 시간 단축
echo 'export now="--force --grace-period=0"' >> ~/.bashrc

# 6. 변경된 bashrc 즉시 적용
source ~/.bashrc
```
```bash
# .vimrc

echo 'set tabstop=2 expandtab shiftwidth=2' >> ~/.vimrc
```
