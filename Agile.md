출처: https://www.redhat.com/en/devops/what-is-agile-methodology
출처: https://learn.microsoft.com/devops/plan/what-is-agile
## Contents

1줄 요약: 병렬적인 S/W development에 대한 길잡이,사고방식

주의 : 'Continual' 계획이 중요
### 개요

애자일은 신속한 반복 작업을 통해 실제 작동 가능한 S/W를 개발하여 지속적으로 제공하기 위한 S/W 개발 방식입니다.

'애자일 방법론'이라는 용어는 Agile이 S/W 개발에 대하여 하나의 특정한 접근 방식을 의미한다는 오해를 일으킬 수 있습니다.
Agile은 S/W 개발에서 정확히 무엇을 해야 하는지를 명시한 지시서가 아닙니다. 
협업에과 workflow에 대한 하나의 관점이며, 우리가 무엇을 어떠한 방식으로 만들지에 관한 선택을 guide, 도와주는 set of values, 가치 체계입니다.

더 practical하게, 구체적으로 말하자면 Agile S/W development methodologies의 핵심은 고객을 더욱 만족시키기 위해서 신속하게 S/W의 small pieces를 전달하는 것입니다. 
이 방법들은 adaptive, 적응형 접근 방식과 팀워크를 활용한 지속적인 발전을 1순위로 합니다.

보통 Agile S/W 개발은 S/W 개발자와 비즈니스 담당자들이 self-organizing 자체적으로 구성한 팀에서 이루어집니다.
Agile 개발은 S/W documentation에 대한 가벼운 접근을 선호하며 life cycle 모든 단계에서의 변화를 적극적으로 embrace 수용합니다.

<details>
<summary>
S/W life cycle
</summary>
Software Development Lifecycle이란 개발 팀이 높은 품질의 software를 design하기 위해 사용하는 cost-effective and time-efficient 프로세스입니다.
SDLC의 목표는 S/W의 production과 이후에도 고객의 기대를 충족하도록 forward planning, 미리 계획을 통해 프로젝트의 위험을 최소화시키는 것입니다.
이 methodology, 방법론은 S/W 개발 과정을 할당, 완료, 측정할 수 있는 작업으로 나누는 일련의 단계들을 outline, 개략적으로 설계합니다.

What is SDLC?
Why is SDLC important?
How does SDLC work?
What are SDLC models?
How does SDLC address security?
How does SDLC compare with other lifecyclemanagement methodologies?
How can AWS help you with your SDLC requirements?

(출처:[What Is SDLC](https://aws.amazon.com/what-is/sdlc/?nc1=h_ls))
</details>

### Agile의 개념 및 가치
2001년 Waterfall 방식의 프로젝트 관리에 대응하여, S/W 개발자 그룹이 'The Manifesto for Agile Software Development'를 작성했습니다.
이 문서에는 S/W 개발에 대한 새로운 접근 방식을 제안하고, 다른 고려 사항보다 가치있다고 생각하는 4가지 주요 특성을 제안합니다.

1. Individuals and interactions over process and tools
    개인간의 상호작용 > 프로세스와 개발 도구
2. Working software over comprehensive documentation
    작동하는 S/W > 상세한 문서
3. Customer collaboration over contract negotiation
    고객과의 협동 > 계약 협상
4. Responding to change over following a plan
    변화에 대응 > 계획 이행

모든 항목에 본질적인 가치가 있지만, 위의 우선순위를 따르면 더 좋은 결과를 얻을 수 있습니다.
Agile 선언문(manifesto)은 행동 지침(practice)들을 규정하지는 않습니다. S/W dev에 대한 생각의 새로운 방법에 대한 길잡이(guidance)입니다.

Agile 선언문에서 기인한 결과들은 많습니다. 예를 들어 seqeuntial한 S/W dev, 즉 waterfall에서 product quality를 보장하는 방식과 다르게,
Agile method는 개발과 테스트를 동시에 연속적인 프로세스로 진행가능합니다.
즉(put another way), Waterfall development은 한 단계를 모두 완료해야 다음 단계로 이동할 수 있지만, Agile개발은 동시에 발생하는 multiple sequence를 지원 가능합니다.

[Create an agile infrastructure—and enable an adaptive organization](https://www.redhat.com/rhdc/managed-files/mi-agile-integration-ebook-f20123wg-201911-en_0.pdf)
<details>
<summary>
contents
</summary>
1. The role of integration in innovation 
2. Laying the foundation for agility
3. Implementing agile integration
</details>

### What Agile isn't
Agile은 "우리는 알아서 할테니까",(we'll figure it out as we go)라는 태도로 S/W를 develop하는 'Cowboy coding'이 아닙니다.
해야 할 일의 명확한 definition과 고객에게 보여줄 수 있는 명시적인 value를 필요로 합니다.
Agile은 개인과 팀의 자율성(autonomy)도 중시하지만, value와 함께 증가할 수 있는 자율성을 강조합니다.

Agile에서 엄격한(rigor)계획이 없는 것만은 아닙니다. Agile 방법론과 관행(methodologies and practices)은 일반적으로 계획에서의 규율(discipline)을 강조합니다.
핵심은 프로젝트 전반에 걸친 지속적인(continual) 계획입니다. Continual planning덕에 팀은 수행한 업무로부터 learn 할 수 있습니다.
이러한 접근을 통해서, ROI(Return On Investment), 투자 수익율을 극대화합니다

Agile이 loadmap이 없다고 오해하는 경우가 있지만, Continual planning과 loadmap이 없는 것은 다릅니다. 팀원들은 모두 이루고자 하는 결과물과 방향성을 인지하고 있어야 합니다.

(출처: https://learn.microsoft.com/devops/plan/what-is-agile)


<details>
<summary>
cowboy coding
</summary>
Cowboy coding 은 S/W 개발 방식 중 하나로, 혼자서 또는 적은 인원의 팀으로 S/W를 개발하는 경우를 가리키비낟. 
</details>