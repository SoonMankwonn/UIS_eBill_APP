[2012.04.26]

1. 테이블 변경 내역
	********************************************************************************************
	TABLE NAME                  COLUMN                                 DATATYPE
	********************************************************************************************
  CARD_INFO										[CARD_INFO_FUSER_WorkstationID]				 VARCHAR(20) 	
															[CARD_INFO_LUSER_WorkstationID]				 VARCHAR(20) 	
	
	********************************************************************************************
	
[2012.04.26]

PGServer

1. MainFunc.CS
   - 신용카드 한도 확보 처리시, KICC recvCode= "0000"이 아닐때 (오류 일때)
     	kicc.recvErrorMsg를 전달하도록 수정함.
     	--> 메시지 내용 중 = .....=를 제외한 뒷 부분의 공백을 제거하고 전송처리함.
   - 신용카드 승인 처리시, KICC recvCode= "0000"이 아닐때 (오류 일때)
   		kicc.recvErrorMsg를 전달하도록 수정함.
   		--> 메시지 내용 중 = .....=를 제외한 뒷 부분의 공백을 제거하고 전송처리함.
   		
2. 카드 승인 처리시   		
   - WorkstationID 저장되도록 수정.		



