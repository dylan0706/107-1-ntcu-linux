�Ĥ@�D
#examuser1.2.3
��Juseradd examuser1
��Jpasswd examuser1
���New Password:�ÿ�J�s�K�X
�ڳ]�w��ItIsExam
�t�η|�A�T�{�@�M�K�X
�M�᭫�Ƥ@�˪��ʧ@�s�Wexamuser2�Mexamuser3�A�K�X�Ҭ�ItIsExam
 
#�R��examuser3	
��Juserdel -r examuser3�R���ϥΪ�
�ˬd�O�_���\�R��
#��_examuser1 
��Juserdel examuser1

��Jsudo useradd -u 1001 -m examuser1</li>
��Jsudo passwd examuser1</li>
���New Password:�ÿ�JItIsExam</li></li>
��Jid examuser1</li>
���
	uid=1001(examuser1) gid=1001(examuser1) groups=1001(examuser1)</li>
�ĤG�D
#�إ�examuser4 
��Juseradd examuser4
���New Password:�ÿ�J�s�K�X
�ڳ]�w��sotired
#�ƻs�ɮרç���v�� 
��Jcp /etc/securetty /home/examuser4
��Jls /home/examuser4�ˬd�O�_��securetty
��Jchmod u=rwx,g=rwx,o=rwx /home/examuser4/securetty
#�ˬd
��Jsu - examuser4�����ϥΪ�
��Jll�ˬd�O�_����v��
#�s���ɮ� 
��Jcd /home/examuser4/�i�J�ؿ�
��Jmkdir examdata�إ߸�Ƨ�
��Jls
�|���
examdata	securetty 
��Jcd examdata�i�J
�A��Jtouch change.txt�إ��ɮ�
��Jll�ˬd
#����v�� 
�Φ^ROOT
��Jcd /home/examuser4/examdata/
��Jchown sshd change.txt���֦��̬�sshd
��Jchgrp users change.txt���s�լ�users
��Jchmod u=rw,g=r,o= change.txt����v����-rw-r
��Jll�ˬd
���|���
	-rw-r. 1	sshd users 0	���	�ɶ�	change.txt
#���ɶ� 
��Jtouch -t 20121231 change.txt

�ĤT�D
 #root�����إ��ɮ׻P�v�� 
��Jcd /dev/�i�Jdev
�A��Jcd shm/�i�Jshm
��Jmkdir unit05/ �إ�unit05�ؿ���
��Jchmod u=rwx,g=rwx,o=rx unit05 �ק�unit05���v��
��Jmkdir ���O�[�W�إߥ|�Ӹ�Ƨ�
�ק�dir1,dir2,dir3,dir4�v��
	chmod u=rwx,g=rx,o=r dir1
	chmod u=rwx,g=rx,o=x dir2 
	chmod u=rwx,g=rx,o=rx dir3
	chmod u=rwx,g=rwx,o=rwx dir4 </li>
�ƻs/etc/hosts�� dir1,dir2,dir3,dir4�A�N�ɦW�אּ file1,file2,file3,file4
	cp /etc/hosts /dev/shm/unit05/dir1/file1
	cp /etc/hosts /dev/shm/unit05/dir2/file2
	cp /etc/hosts /dev/shm/unit05/dir3/file3
	cp /etc/hosts /dev/shm/unit05/dir4/file4 
#�i�Jdir1�ק�file1�v��
��Jcd dir1/
�A��Jchmod u=rw,g=r,o=r file1</li>
#�ק�file2�v��
��Jcd dir2/
��Jchmod u=rw,g=r,o=r file2
#�ק�file3�v��
��Jcd dir3/
��Jchmod u=rw,g=r,o=r file3
#�ק�file4�v��
��Jcd dir4/
��Jchmod u=rw,g=r,o=r file4
#�Шϥ� ls -l /dev/shm/unit05/dir[1-4] �̾ڿ�X�����G��������|���ͳo�ǰ��D�H
�������������]�����S�����檺�v��
#�ϥ� vim /dev/shm/unit05/dir1/file1 ~ vim /dev/shm/unit05/dir4/file4�A�����x�s (�αj���x�s)
��������i�H/���i�H�x�s�H
�u��file3�i�H�x�s �]��other��file3���ק��v��