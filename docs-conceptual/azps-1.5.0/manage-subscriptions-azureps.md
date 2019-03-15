---
title: 使用 Azure PowerShell 來管理 Azure 訂用帳戶
description: 使用 Azure PowerShell 來管理 Azure 訂用帳戶
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 02/04/2019
ms.openlocfilehash: 29d7c84d0ca9ae8d3e4e22f407b007d2d582f8bc
ms.sourcegitcommit: 447276d46ffeeb37f0c07a570536665e36c5ddb8
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/14/2019
ms.locfileid: "57882193"
---
# <a name="use-multiple-azure-subscriptions"></a>使用多個 Azure 訂用帳戶

大部分的 Azure 使用者永遠只會有單一訂用帳戶。 不過，如果您是多個組織的成員，或貴組織跨多個群組分割了特定資源的存取權，您可能會在 Azure 中擁有多個訂用帳戶。 CLI 支援全域及依命令選取訂用帳戶。

## <a name="tenants-users-and-subscriptions"></a>租用戶、使用者和訂用帳戶

您可能對於 Azure 中租用戶、使用者和訂用帳戶之間的差異感到混淆。 _租用戶_是指包含整個組織的 Azure Active Directory 實體。 租用戶至少有一個_訂用帳戶_和_使用者_。 使用者為個人，且只與一個租用戶相關，也就是其所屬的組織。 使用者是會登入 Azure 來建立、管理並使用資源的帳戶。
使用者可能擁有多個_訂用帳戶_的存取權，訂用帳戶是與 Microsoft 的協議，可使用包括 Azure 等雲端服務。 每個資源會與訂用帳戶相關聯。

若要深入了解租用戶、使用者和訂用帳戶之間的差異，請參閱 [Azure 雲端術語字典](/azure/azure-glossary-cloud-terminology)。  若要了解如何將新訂用帳戶新增至您的 Azure Active Directory 租用戶，請參閱[如何將 Azure 訂用帳戶新增至 Azure Active Directory](/azure/active-directory/active-directory-how-subscriptions-associated-directory)。
若要了解如何登入特定租用戶，請參閱[使用 Azure PowerShell 登入](/powershell/azure/authenticate-azureps)。

## <a name="change-the-active-subscription"></a>變更使用中的訂用帳戶

在 Azure PowerShell 中，存取訂用帳戶資源需要變更與目前 Azure 工作階段相關聯的訂用帳戶。
可透過修改使用中工作階段內容、租用戶資訊、訂用帳戶及應該執行的使用者 Cmdlet 完成。
為了變更訂用帳戶，首先需要使用 [Get-AzSubscription](/powershell/module/az.accounts/get-azsubscription) 擷取 Azure PowerShell Context 物件，並使用 [Set-AzContext](/powershell/module/az.accounts/set-azcontext) 變更目前內容。

接下來的範例顯示如何取得目前使用中租用戶中的訂用帳戶，並將其設為使用中工作階段：

```powershell-interactive
$context = Get-AzSubscription -SubscriptionId ...
Set-AzContext $context
```

若要了解更多 Azure PowerShell 內容的詳細資訊，包含如何儲存並快速在不同內容間切換以輕鬆搭配多個訂用帳戶使用，請參閱[用 Azure PowerShell 內容保存認證](context-persistence.md)。
