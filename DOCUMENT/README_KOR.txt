�� Ŭ���̾�Ʈ ���� ��� ��
python3 client.py [groupID]		EX. python3 client.py testgroup01

�� groupID ���� ��� ��
python3 FaceAPI.py �Է� �� �ȳ��� ���� ����
������ group�� MS ������ ����Ǹ�, ���� Ű 1���� 1000���� group ���� ����
���⼭ ���ϴ� group�� LargePersonGroup �̶� Ī��

�� cfg_var.py ��
����� ȯ�濡 ���� ����� �� �ִ� ���� (���丮, ���� ��ġ ��) ���� ����
cfg_var.py ���� ������ ������ cfg_ �� �����ϰ� �Ͽ� ���� ����

�� msg_var.py ��
�ܱ��� ������ �����ϰ� ���������, �ѱ�/��� ��ȯ�ϴ� ����� �������� �ʾ���
cfg_var.py�� ���������� �������� msg_ �� ����

�ѤѤѤѤѤѤѤѤѤѤѤѤѤѤѤѤѤѤѤѤѤѤѤѤѤѤѤѤѤѤѤ�

�� ȸ������ �� �α��� �� API ȣ�� ���� ��
1. �ϴ� ī�޶� ���� ������ ������ ��� ����, �ش� ������ Detect API�� ���� MS ������ ���۵ǰ�, ������ ���� ������ �� ������ �ĺ�ID�� ��ȯ�Ѵ�. �� ID�� faceID ��� �θ���, 24�ð� ��� �� MS �������� �����ȴ�.

2-1-1. ������ ȸ�������� �õ��� ���, ���� Create_personid API�� ȣ��Ǿ� ������ �Է��� �г������κ��� ������ personID�� �����Ѵ�.
2-1-2. group ������ ������ ������ personID�� ���������, Addface API�� ȣ��Ǿ� group ���� ���� ������ personID �� �� ������ �Բ� �����ϸ�, �� ������ �ĺ� ID�� ��ȯ�Ѵ�. �� ID�� persistedfaceid ��� �θ��� �ش� ������ �����ϴ� API�� ȣ����� �ʴ� �� MS ������ ���������� �����ȴ�. (�ش� ���� API ȣ�� �ڵ�� �������� ����)
2-1-3. group ���� ���� ������ �߰��� �ڿ�, Train API�� ȣ��ȴ�. group�� train�� ������� ������ �α��� �� ȣ���� Identify API�� ȣ���� �� ����
cf. �帧��.pdf

2-2-1. ������ �α����� �õ��� ���, Identify API�� ȣ��Ǿ� 1������ Ȯ���� �������� ��Ī�Ǵ� ���� group ������ ã�� ��, ���� ���� ��ġ�� ��Ī�Ǵ� ����� personID�� ��ȯ�Ѵ�.

+@. FaceAPI.py�� ������ �����Ǿ� �ִ� get_userData �Լ��� personID�� �Է¹ް� �ش� ������ �г����� ��ȯ�ϴ� API�� ȣ���Ѵ�. ������ �α����� �� �� ������ �г����� �ҷ��ֱ� ���� �������. ������ ȸ�������� ���� ������ ���� �г����� �Է��ϱ� ������ �� API�� ȣ����� �ʴ´�.

�ѤѤѤѤѤѤѤѤѤѤѤѤѤѤѤѤѤѤѤѤѤѤѤѤѤѤѤѤѤѤѤ�

�� ���� ���� ��
1. ī�޶� ȭ�󿡼� ���� ���� �����ϴ� ���� OpenCV�� ���� �����Ǿ��µ�, OpenCV���� ���̶�� ������ MS �������� ���� �ƴ϶�� �ϴ� ��찡 ��Ȥ �����, ī�޶� ���� ���� �� �󵵰� ��������.

2. Ŭ���̾�Ʈ������ Detect API�� ��ȯ�ϴ� �� ���� �� �� ������ ��� dict Ÿ������ �����ϵ��� �Ͽ���. (FaceAPI.py 74~80 Line ����)

3. ���� ���������� ������ ������ �ڵ�� client.py 491~493 Line�� �ۼ��Ǿ� ������ ���� �۵����� �ʴ´�.