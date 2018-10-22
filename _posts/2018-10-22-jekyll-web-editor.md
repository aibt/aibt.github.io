---
title: Jekyll에 Web Editor를 달아보기
categories: jekyll jekyll-admin
layout: post
---

**Jekyll**를 팀 블로그에 적용하여 사용해 보려고 했다. 

그 이유는 Github page와 궁합이 좋아 git에 넣고 업로드 하면 Github page에 적용 된다니 말이다.

혼자 하는 블로그에서는 개인 관리가 가장 크기 때문에 단체로 사용하기 어렵지만, 팀원들이 모두 개발자 이기 때문에 git으로 뭔가를 작성하고 공유하는 것이 가장 간편했다. 그러므로 **Github page**으로 가는건 당연한 수순이었다.

Jekyll를 설치하고 사용하며, Github page에 배포하는 건 검색 몇번하면, 좋은 자료를 많이 볼 수 있고, 이를 통해 진행하면 손쉽게 해 볼 수 도 있다. 근데 문제는, Local에서 Jekyll을 돌릴 때 웹서버처럼 보여주기만 하면 별 쓸모가 있는 것인가 하는 생각이 들었다. 따로 Editor를 두어 Jekyll에 적용하는 방식이 아닌, jekyll 자체적으로 Web Editor가 있어서 적용하면 어떨까? 하는 생각이 들었다.

다행이 관련어로 검색해 보니 바로 답이 나왔다. [Jekyll-admin](https://github.com/jekyll/jekyll-admin)녀석이 눈에 띄였다. 이름도 맘에 든다. **Admin**이라니?

### 설치하기
`Gemfile`에 아래의 내용을 입력한다.
```ruby
gem 'jekyll-admin', group: :jekyll_plugins
```
그리고, 해당 디렉토리에서 **CLI**를 통해 설치 명령을 수 행한다.
```bash
bundle install
```
### 사용하기
로컬 도메인에 `/admin`만 붙여주면 admin page로 들어가게 되고, 이곳에서 간단하게 설정 파일 수정과 블로그 포스트들을 관리 할 수 있다.