---
title: 使用 Azure PowerShell 登入
description: 如何使用 Azure PowerShell 以使用者身分登入、使用服務主體登入，或使用適用於 Azure 資源的受控識別登入。
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2017
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: b0abbeb0eb54db010193c4676465b9359a355627
ms.sourcegitcommit: 038cb42a3bd8c009bc57c8c1c252e66fa170c84b
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/24/2020
ms.locfileid: "92523269"
---
# <a name="sign-in-with-azure-powershell"></a>使用 Azure PowerShell 登入

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

Azure PowerShell 支援多種驗證方法。 最簡單的入門方法是在命令列以互動方式登入。

## <a name="sign-in-interactively"></a>以互動方式登入

若要以互動方式登入，請使用 [Connect-AzureRmAccount](/powershell/module/azurerm.profile/connect-azurermaccount) Cmdlet。

```azurepowershell-interactive
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

## <a name="sign-in-using-managed-identities-for-azure-resources"></a>使用適用於 Azure 資源的受控識別登入

適用於 Azure 資源的受控識別是 Azure Active Directory 的一項功能。 您可以使用受控識別服務主體進行登入，並取得僅限應用程式的存取權杖來存取其他資源。 受控識別僅適用於在 Azure 雲端中執行的虛擬機器。

若想進一步了解適用於 Azure 資源的受控識別，請參閱[如何在 Azure VM 上使用適用於 Azure 資源的受控識別取得存取權杖](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token)。

## <a name="sign-in-to-another-cloud"></a>登入其他雲端

Azure 雲端服務提供不同的環境，以遵循各個區域的資料處理法規。 如果您的 Azure 帳戶位於與其中一個區域相關聯的雲端，則需要在登入時指定環境。 例如，如果您的帳戶位於中國雲端，則可使用下列命令來登入：

```azurepowershell-interactive
Login-AzureRmAccount -EnvironmentName AzureChinaCloud
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
* [Set-AzureRmRoleDefinition](/powershell/module/AzureRM.Resources/Set-AzureRmRoleDefinition)
