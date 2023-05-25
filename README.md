---
수업에 도움이 될 수 있는 것(?)들을 정리 해논 repo 입니다.

---
========== 2023.05.25

1. 빈약한 컴퓨터를 위한 airflow .yml file

	- 기존 compose file은 airflow를 구성하는 components가 전부 포함되어있는 풀(?) 세트 같은 개념입니다. 따라서, 최소한의 실습에 필요한 component 만 추가하여 build 하였습니다.
	
	- 구성 요소 
		
			- web server : dag 있고, 구경하고, 실행 결과를 web으로 볼 수 있는 node
			- scheduler : worker_node와 같은 실제로 dag file을 컴파일하고, 실행시키는 node
			- postgre : 해야할 process들을 queued 해 저장하는 node

	- 사용법

		1. 기존 compose file 과 동일합니다.
		2. airflow directory >> docker-compose.yml 을 저장합니다. 
		3. docker desktop을 실행시킵니다. (deamon을 켜야해요)
		4. 해당 directory로 접근하여 docker compose up 입력!
		5. 그럼 기존에 사용하시던 것 과 같이 사용 가능합니다. 


	*추가*
		
		airflow excutor는 local excutor를 사용하였고, n개의 worker_node로 실습을 해야할 상황이 올때는 .yml file을 수정이 필요합니다.

	궁금한 내용들이 있다면, 편하게 여쭤보시면 아는 선에서는 말씀드리도록 하겠습니다 :)
---


