---
title: Atualizar uma chave GPG expirada
intro: Ao verificar uma assinatura, o {% data variables.product.product_name %} confere se a chave foi revogada ou está expirada. Caso a chave de assinatura tenha sido revogada ou esteja expirada, o {% data variables.product.product_name %} não poderá verificar as assinaturas. Se a chave foi revogada, use a chave principal ou outra chave que não tenha sido revogada para assinar os commits.
redirect_from:
- /articles/updating-an-expired-gpg-key
- /github/authenticating-to-github/updating-an-expired-gpg-key
- /github/authenticating-to-github/troubleshooting-commit-signature-verification/updating-an-expired-gpg-key
versions:
  fpt: '*'
  ghes: '*'
  ghae: '*'
  ghec: '*'
topics:
- Identity
- Access management
shortTitle: Update expired GPG key
ms.openlocfilehash: daf4f225426ccb67d2fa536afbd9a1f6517e4913
ms.sourcegitcommit: 22d665055b1bee7a5df630385e734e3a149fc720
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/13/2022
ms.locfileid: "145083569"
---
Se a chave tiver vencido, você precisará [atualizar o vencimento](https://www.gnupg.org/gph/en/manual/c235.html#AEN328), exportar a nova chave, excluir a chave vencida da sua conta do GitHub e [carregar a nova chave no GitHub](/articles/adding-a-new-gpg-key-to-your-github-account/). As tags e os commits anteriores serão exibidos como verificados, desde que a chave atenda a todos os outros requisitos de verificação.

Se a chave for inválida, você não usar outra chave válida no conjunto de chaves e ainda gerar uma nova chave GPG com um novo conjunto de credenciais, os commits feitos com a chave revogada ou expirada continuarão sendo exibidos como não verificados. Além disso, as novas credenciais não conseguirão assinar novamente ou verificar tags e commits antigos.

## <a name="further-reading"></a>Leitura adicional

- "[Sobre a verificação da assinatura de commit](/articles/about-commit-signature-verification)"
