learning git
git init ��ʼ��git�ֿ⡣
git add �ļ��� ��ֿ�����ļ���
git commit -m "comment"   ���ļ��ύ���ֿ⡣
git status �鿴��ǰ״̬
git diff �鿴�޸�����
git log �鿴��ʷ�ύ��¼  --pretty=oneline����
git reflog �鿴������ʷ
git reset --hard head^ �ص���һ���汾  head~100 �ص���һ�ٸ��汾
git reset --hard commit_id �ص�ָ���İ汾��
���������ݴ�������
���������������ڵ������ܿ�����Ŀ¼��
�汾�⣺��������һ������Ŀ¼.git��������㹤����������Git�İ汾�⡣
�ݴ�����Git�İ汾������˺ܶණ������������Ҫ�ľ��ǳ�Ϊstage�����߽�index�����ݴ�����
����GitΪ�����Զ������ĵ�һ����֧master���Լ�ָ��master��һ��ָ���HEAD��
���ļ���汾�����ʱ����Ϊ������
��һ������git add���ļ���ӽ�ȥ��ʵ���Ͼ��ǰ��ļ��޸���ӵ��ݴ�����
�ڶ�������git commit�ύ���ģ�ʵ���Ͼ��ǰ��ݴ��������������ύ����ǰ��֧
git checkout -- file  �����������޸� �����е�--����Ҫ��û��--���ͱ���ˡ�����һ���·�֧��������
git reset HEAD file���԰��ݴ������޸ĳ�������unstage�������·Żع�����
Զ�̲���
git remote add origin Զ�ֿ̲��ַ  ����Զ�̿�
git push -u origin master ��һ����Զ�̿�����master��֧����������
git push origin master ��Զ�̿����������޸�
git clone Զ�̿��ַ  ��¡һ�����ؿ�
git checkout -b ��֧����  ������֧���л����÷�֧
git branch ������г����з�֧����ǰ��֧ǰ����һ��*��
git merge ָ����֧�� ��ָ����֧�ϲ�����ǰ��֧Fast forwardģʽ
git branch ��֧�� ������֧
git branch -d ��֧�� ɾ���÷�֧
git log --graph --pretty=oneline ������Կ�����֧�ϲ�ͼ
git merge --no-ff <name> �ϲ���֧����Fast forwardģʽ
�ϲ���֧ʱ������--no-ff�����Ϳ�������ͨģʽ�ϲ����ϲ������ʷ�з�֧���ܿ��������������ϲ�����fast forward�ϲ��Ϳ����������������ϲ���
git stash �ѵ�ǰ�����ֳ������ء����������Ժ�ָ��ֳ����������
git stash list �鿴��ǰ�洢�Ĺ���
git stash apply �ָ���ǰ�洢�Ĺ���
git stash drop ɾ��stash����
git stash pop �ָ�ͬʱ��stash����Ҳɾ��
git branch -D <name> ǿ��ɾ��û�кϲ��ķ�֧
git remote -v ��ʾԶ�ֿ̲���ϸ����Ϣ
git checkout -b <name> <name> �ڱ��ش�����Զ�̷�֧��Ӧ�ķ�֧�����غ�Զ�̷�֧���������һ�£�
git branch --set-upstream <name> <name>ָ�����ط�֧��Զ�̷�֧������
����Э����ͻ������裺
���ȣ�������ͼ��git push origin branch-name�����Լ����޸ģ�
�������ʧ�ܣ�����ΪԶ�̷�֧����ı��ظ��£���Ҫ����git pull��ͼ�ϲ���
����ϲ��г�ͻ��������ͻ�����ڱ����ύ��
û�г�ͻ���߽������ͻ������git push origin branch-name���;��ܳɹ���
���git pull��ʾ��no tracking information������˵�����ط�֧��Զ�̷�֧�����ӹ�ϵû�д�����
������git branch --set-upstream <name> <name>
��ǩ��
git tag <name> ������ǩ
git tag �鿴���б�ǩ
git tag <name>  <commit id>  ������ʷ�汾��ǩ
git tag -a <tagname> -m "blablabla..."����ָ����ǩ��Ϣ��
git tag -s <tagname> -m "blablabla..."������PGPǩ����ǩ��
git show <tagname>�鿴��ǩ��Ϣ
git push origin <tagname>��������һ�����ر�ǩ��
git push origin --tags��������ȫ��δ���͹��ı��ر�ǩ��
git tag -d <tagname>����ɾ��һ�����ر�ǩ��
git push origin :refs/tags/<tagname>����ɾ��һ��Զ�̱�ǩ��