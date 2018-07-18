---
title: 使用 Azure PowerShell 登入
description: 如何使用 Azure PowerShell 以使用者、服務主體身分登入，或使用 MSI 登入。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2017
ms.openlocfilehash: 20194ac2282d602ba61bf130791edac9f4ffae6c
ms.sourcegitcommit: 990f82648b0aa2e970f96c02466a7134077c8c56
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/11/2018
ms.locfileid: "38100217"
---
# <a name="sign-in-with-azure-powershell"></a>使用 Azure PowerShell 登入

Azure PowerShell 支援多種驗證方法。 最簡單的入門方法是在命令列以互動方式登入。

## <a name="sign-in-interactively"></a>以互動方式登入

若要以互動方式登入，請使用 [Connect-AzureRmAccount](/powershell/module/azurerm.profile/connect-azurermaccount) Cmdlet。

```azurepowershell
Connect-AzureRmAccount
```

執行時，此 Cmdlet 會顯示對話方塊，提示您輸入與 Azure 帳戶相關聯的電子郵件地址和密碼。 驗證時，會針對目前的 PowerShell 工作階段儲存該資訊，關閉對話方塊，您就具有所有 Azure PowerShell Cmdlet 的存取權。

> [!IMPORTANT]
> 從 Azure PowerShell 6.3.0 開始，只要您保持登入 Windows，您的認證就會在多個 PowerShell 工作階段之間共用。 如需詳細資訊，請參閱[持續性認證](context-persistence.md)中的文章。

## <a name="sign-in-with-a-service-principal"></a>使用服務主體來登入

服務主體提供您建立非互動式帳戶的方式，以用來操控資源。 服務主體就像是使用者帳戶，您可以使用 Azure Active Directory 對其套用規則。 僅授與服務主體所需的最低權限，可確保您的自動化指令碼會更加安全。

如果您需要建立服務主體以便與 Azure PowerShell 搭配使用，請參閱[使用 Azure PowerShell 建立 Azure 服務主體](create-azure-service-principal-azureps.md)。

若要使用服務主體來登入，請使用 `-ServicePrincipal` 引數和 `Connect-AzureRmAccount` Cmdlet。 您也需要服務主體的應用程式識別碼、登入認證，以及與服務主體相關聯的租用戶識別碼。 若要取得服務主體的認證作為適當物件，請使用 [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) Cmdlet。 這個 Cmdlet 會顯示對話方塊，讓您在其中輸入服務主體使用者識別碼和密碼。

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzureRmAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
```

## <a name="sign-in-using-an-azure-vm-managed-service-identity"></a>使用 Azure 虛擬機受控服務識別登入

受控服務識別 (MSI) 是 Azure Active Directory 的預覽功能。 您可以使用 MSI 服務主體進行登入，並取得僅限應用程式的存取權杖來存取其他資源。 MSI 僅適用於在 Azure 雲端中執行的虛擬機器。

如需 MSI 的詳細資訊，請參閱[如何使用 Azure VM 受控服務識別登入 (MSI) 進行登入和取得權杖](/azure/active-directory/msi-how-to-get-access-token-using-msi)。

## <a name="sign-in-to-another-cloud"></a>登入其他雲端

Azure 雲端服務提供不同的環境，以遵循各個區域的資料處理法規。 如果您的 Azure 帳戶位於與其中一個區域相關聯的雲端，則需要在登入時指定環境。 例如，如果您的帳戶位於中國雲端，則可使用下列命令來登入：

```azurepowershell-interactive
Connect-AzureRmAccount -Environment AzureChinaCloud
```

使用下列命令來取得可用環境的清單：

```azurepowershell-interactive
Get-AzureRmEnvironment | Select-Object Name
```

## <a name="learn-more-about-managing-azure-role-based-access"></a>深入了解如何管理 Azure 角色型存取

如需 Azure 中的驗證與訂用帳戶管理的詳細資訊，請參閱[管理帳戶、訂用帳戶和管理角色](/azure/active-directory/role-based-access-control-configure)。

可用來管理角色的 Azure PowerShell Cmdlet：

* [Get-AzureRmRoleAssignment](/powershell/module/AzureRM.Resources/Get-AzureRmRoleAssignment)
* [Get-AzureRmRoleDefinition](/powershell/module/AzureRM.Resources/Get-AzureRmRoleDefinition)
* [New-AzureRmRoleAssignment](/powershell/module/AzureRM.Resources/New-AzureRmRoleAssignment)
* [New-AzureRmRoleDefinition](/powershell/module/AzureRM.Resources/New-AzureRmRoleDefinition)
* [Remove-AzureRmRoleAssignment](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleAssignment)
* [Remove-AzureRmRoleDefinition](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleDefinition)
* [Set-AzureRmRoleDefinition](/powershell/moduel/AzureRM.Resources/Set-AzureRmRoleDefinition)
