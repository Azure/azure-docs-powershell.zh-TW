---
title: 使用 Azure PowerShell 來登入
description: 使用 Azure PowerShell 來登入
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2017
ms.openlocfilehash: edbf17141cac4ea6e41282c8e1dd07c5b738351c
ms.sourcegitcommit: ac4b53bb42a25aae013a9d8cd9ae98ada9397274
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/08/2018
ms.locfileid: "51274699"
---
# <a name="log-in-with-azure-powershell"></a>使用 Azure PowerShell 來登入

Azure PowerShell 支援多種登入方法。 最簡單的入門方法是在命令列以互動方式登入。

## <a name="interactive-log-in"></a>互動式登入

1. 輸入 `Login-AzureRmAccount`。 您會看到對話方塊，裡面會要求您提供 Azure 認證。

2. 輸入與您帳戶相關聯的電子郵件地址和密碼。 Azure 會驗證並儲存認證資訊，然後關閉視窗。

## <a name="log-in-with-a-service-principal"></a>使用服務主體來登入

服務主體提供您建立非互動式帳戶的方式，以用來操控資源。 服務主體就像是使用者帳戶，您可以使用 Azure Active Directory 對其套用規則。 僅授與服務主體所需的最低權限，可確保您的自動化指令碼會更加安全。

1. 如果您還沒有服務主體，請[建立一個](create-azure-service-principal-azureps.md)。

2. 使用服務主體來登入。

    ```powershell-interactive
    Login-AzureRmAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
    ```

    若要取得您的 TenantId，請以互動方式登入，然後從您的訂用帳戶中取得 TenantId。

    ```powershell-interactive
    Get-AzureRmSubscription
    ```

    ```output
    Environment           : AzureCloud
    Account               : username@contoso.com
    TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionId        : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionName      : My Production Subscription
    CurrentStorageAccount :
    ```

### <a name="log-in-using-managed-identities-for-azure-resources"></a>使用適用於 Azure 資源的受控識別登入

適用於 Azure 資源的受控識別是 Azure Active Directory 的一項功能。 您可以使用受控識別服務主體進行登入，並取得僅限應用程式的存取權杖來存取其他資源。

若想進一步了解適用於 Azure 資源的受控識別，請參閱[如何在 Azure VM 上使用適用於 Azure 資源的受控識別取得存取權杖](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token)。

## <a name="log-in-to-another-cloud"></a>登入其他雲端

Azure 雲端服務提供不同的環境，以遵循各國政府的資料處理法規。 如果您的 Azure 帳戶位於某一個政府雲端，則需要在登入時指定環境。 例如，如果您的帳戶位於中國雲端，則可使用下列命令來登入：

```powershell-interactive
Login-AzureRmAccount -EnvironmentName AzureChinaCloud
```

使用下列命令來取得可用環境的清單：

```powershell-interactive
Get-AzureRmEnvironment | Select-Object Name
```

```output
Name
----
AzureCloud
AzureChinaCloud
AzureUSGovernment
AzureGermanCloud
```

## <a name="learn-more-about-managing-azure-role-based-access"></a>深入了解如何管理 Azure 角色型存取

如需 Azure 中的驗證與訂用帳戶管理的詳細資訊，請參閱[管理帳戶、訂用帳戶和管理角色](/azure/active-directory/role-based-access-control-configure)。

可用來管理角色的 Azure PowerShell Cmdlet

* [Get-AzureRmRoleAssignment](/powershell/module/AzureRM.Resources/Get-AzureRmRoleAssignment)
* [Get-AzureRmRoleDefinition](/powershell/module/AzureRM.Resources/Get-AzureRmRoleDefinition)
* [New-AzureRmRoleAssignment](/powershell/module/AzureRM.Resources/New-AzureRmRoleAssignment)
* [New-AzureRmRoleDefinition](/powershell/module/AzureRM.Resources/New-AzureRmRoleDefinition)
* [Remove-AzureRmRoleAssignment](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleAssignment)
* [Remove-AzureRmRoleDefinition](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleDefinition)
* [Set-AzureRmRoleDefinition](/powershell/moduel/AzureRM.Resources/Set-AzureRmRoleDefinition)
