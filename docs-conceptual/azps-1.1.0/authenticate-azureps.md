---
title: 使用 Azure PowerShell 登入
description: 如何使用 Azure PowerShell 以使用者身分登入、使用服務主體登入，或使用適用於 Azure 資源的受控識別登入。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/29/2018
ms.openlocfilehash: 80c59a10666c6e3a01e6c33716fce40094fb14be
ms.sourcegitcommit: c6fd0e490fa0e33b8b768b679682a47d8faae1cf
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/16/2019
ms.locfileid: "54341953"
---
# <a name="sign-in-with-azure-powershell"></a>使用 Azure PowerShell 登入

Azure PowerShell 支援數種驗證方法。 要開始使用的最簡單方法是透過 [Azure Cloud Shell](/azure/cloud-shell/overview)，這會自動將您登入。 您可以使用本機安裝，以互動方式透過瀏覽器登入。 在撰寫自動化指令碼時，建議的方法是使用[服務主體](create-azure-service-principal-azureps.md)搭配必要權限。 當您依自身的使用案例儘可能地限制登入權限時，同時也是在協助維護 Azure 資源的安全。

在登入之後，系統會針對您的預設訂用帳戶來執行命令。 若要變更工作階段作用中的訂用帳戶，請使用 [Set-AzContext](/powershell/module/az.accounts/set-azcontext) Cmdlet。 若要變更登入 Azure PowerShell 時使用的預設訂用帳戶，請使用 [Set-AzDefault](/powershell/module/az.accounts/set-azdefault)。

> [!IMPORTANT]
>
> 只要您保持登入，認證就會在多個 PowerShell 工作階段之間共用。
> 如需詳細資訊，請參閱[持續性認證](context-persistence.md)中的文章。

## <a name="sign-in-interactively"></a>以互動方式登入

若要以互動方式登入，請使用 [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount) Cmdlet。

```azurepowershell-interactive
Connect-AzAccount
```

執行時，此 Cmdlet 會出示權杖字串。 若要登入，請複製這個字串並將它貼至瀏覽器中的 https://microsoft.com/devicelogin。 PowerShell 工作階段會進行驗證以便連線至 Azure。

## <a name="sign-in-with-credentials"></a>使用認證登入

您也可以使用已授權的 `PSCredential` 物件登入，以連線到 Azure。
取得認證物件最簡單的方式是使用[](/powershell/module/Microsoft.PowerShell.Security/Get-Credential) Cmdlet。 執行時，此 Cmdlet 會提示您輸入使用者名稱/密碼認證組。

> [!Note]
> 這個方法不適用於 Microsoft 帳戶或啟用雙重要素驗證的帳戶。

```azurepowershell-interactive
$creds = Get-Credential
Connect-AzAccount -Credential $creds
```

## <a name="sign-in-with-a-service-principal"></a>使用服務主體來登入

服務主體為非互動式 Azure 帳戶。 如同其他使用者帳戶，其權限也受到 Azure Active Directory 的管理。 藉由僅為服務主體授與其所需的權限，您的自動化指令碼得以受到保護。

若要了解如何建立與 Azure PowerShell 搭配使用的服務主體，請參閱[使用 Azure PowerShell 建立 Azure 服務主體](create-azure-service-principal-azureps.md)。

若要使用服務主體來登入，請使用 `-ServicePrincipal` 引數和 `Connect-AzAccount` Cmdlet。 您也需要服務主體的應用程式識別碼、登入認證，以及與服務主體相關聯的租用戶識別碼。 若要取得服務主體的認證作為適當物件，請使用 [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) Cmdlet。 這個 Cmdlet 會顯示請您輸入服務主體使用者識別碼和密碼的提示。

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
```

## <a name="sign-in-using-a-managed-identity"></a>使用受控識別登入 

受控識別是 Azure Active Directory 的功能。 受控識別是指派給在 Azure 中執行之資源的服務主體。 您可以使用受控識別服務主體進行登入，並取得僅限應用程式的存取權杖來存取其他資源。 只有在 Azure 雲端中執行的虛擬機器才能使用受控識別。

若想進一步了解適用於 Azure 資源的受控識別，請參閱[如何在 Azure VM 上使用適用於 Azure 資源的受控識別取得存取權杖](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token)。

## <a name="sign-in-with-a-non-default-tenant-or-as-a-cloud-solution-provider-csp"></a>以非預設租用戶或雲端解決方案提供者 (CSP) 登入

如果您的帳戶與多個租用戶相關聯，則需要使用連線時的 `-TenantId` 參數方可登入。 此參數可使用任何其他登入方法。 登入時，此參數值可以是租用戶的 Azure 物件識別碼 (租用戶識別碼)，或租用戶的完整的網域名稱。

如果您是[雲端解決方案提供者 (CSP)](https://azure.microsoft.com/en-us/offers/ms-azr-0145p/)，則 `-TenantId` 值**必須**是租用戶的識別碼。

```azurepowershell-interactive
Connect-AzAccount -TenantId 'xxxx-xxxx-xxxx-xxxx'
```

## <a name="sign-in-to-another-cloud"></a>登入其他雲端

Azure 雲端服務提供符合區域資料處理法規的環境。
針對區域雲端中的帳戶，使用 `-Environment` 引數設定您登入時的環境。
例如，如果您的帳戶位於中國雲端：

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

下列命令可取得可用環境的清單：

```azurepowershell-interactive
Get-AzEnvironment | Select-Object Name
```