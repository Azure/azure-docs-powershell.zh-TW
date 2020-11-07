---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 636FAD5B-8C39-4E5C-8978-6845C6B89BC0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurermkeyvaultaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureRmKeyVaultAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureRmKeyVaultAccessPolicy.md
ms.openlocfilehash: d7cd2718377fee36b5aa49f91385de73e3ea6367
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623922"
---
# <span data-ttu-id="75044-101">Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="75044-101">Set-AzureRmKeyVaultAccessPolicy</span></span>

## <span data-ttu-id="75044-102">摘要</span><span class="sxs-lookup"><span data-stu-id="75044-102">SYNOPSIS</span></span>
<span data-ttu-id="75044-103">授與修改使用者、應用程式或安全性群組的現有許可權，以使用金鑰保存庫執行作業。</span><span class="sxs-lookup"><span data-stu-id="75044-103">Grants or modifies existing permissions for a user, application, or security group to perform operations with a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="75044-104">句法</span><span class="sxs-lookup"><span data-stu-id="75044-104">SYNTAX</span></span>

### <span data-ttu-id="75044-105">ByUserPrincipalName (預設) </span><span class="sxs-lookup"><span data-stu-id="75044-105">ByUserPrincipalName (Default)</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -UserPrincipalName <String> [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75044-106">ByObjectId</span><span class="sxs-lookup"><span data-stu-id="75044-106">ByObjectId</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ObjectId <String>
 [-ApplicationId <Guid>] [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75044-107">ByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="75044-107">ByServicePrincipalName</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -ServicePrincipalName <String> [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75044-108">ByEmailAddress</span><span class="sxs-lookup"><span data-stu-id="75044-108">ByEmailAddress</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -EmailAddress <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="75044-109">ForVault</span><span class="sxs-lookup"><span data-stu-id="75044-109">ForVault</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75044-110">InputObjectByObjectId</span><span class="sxs-lookup"><span data-stu-id="75044-110">InputObjectByObjectId</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -ObjectId <String>
 [-ApplicationId <Guid>] [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75044-111">InputObjectByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="75044-111">InputObjectByServicePrincipalName</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -ServicePrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="75044-112">InputObjectByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="75044-112">InputObjectByUserPrincipalName</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -UserPrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="75044-113">InputObjectByEmailAddress</span><span class="sxs-lookup"><span data-stu-id="75044-113">InputObjectByEmailAddress</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -EmailAddress <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="75044-114">InputObjectForVault</span><span class="sxs-lookup"><span data-stu-id="75044-114">InputObjectForVault</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75044-115">ResourceIdByObjectId</span><span class="sxs-lookup"><span data-stu-id="75044-115">ResourceIdByObjectId</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-ResourceId] <String> -ObjectId <String> [-ApplicationId <Guid>]
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75044-116">ResourceIdByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="75044-116">ResourceIdByServicePrincipalName</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-ResourceId] <String> -ServicePrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="75044-117">ResourceIdByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="75044-117">ResourceIdByUserPrincipalName</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-ResourceId] <String> -UserPrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="75044-118">ResourceIdByEmailAddress</span><span class="sxs-lookup"><span data-stu-id="75044-118">ResourceIdByEmailAddress</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-ResourceId] <String> -EmailAddress <String> [-PermissionsToKeys <String[]>]
 [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75044-119">ResourceIdForVault</span><span class="sxs-lookup"><span data-stu-id="75044-119">ResourceIdForVault</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-ResourceId] <String> [-EnabledForDeployment] [-EnabledForTemplateDeployment]
 [-EnabledForDiskEncryption] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="75044-120">說明</span><span class="sxs-lookup"><span data-stu-id="75044-120">DESCRIPTION</span></span>
<span data-ttu-id="75044-121">**AzureRmKeyVaultAccessPolicy** Cmdlet 會授權或修改使用者、應用程式或安全性群組的現有許可權，以使用金鑰保存庫執行指定的作業。</span><span class="sxs-lookup"><span data-stu-id="75044-121">The **Set-AzureRmKeyVaultAccessPolicy** cmdlet grants or modifies existing permissions for a user, application, or security group to perform the specified operations with a key vault.</span></span> <span data-ttu-id="75044-122">它不會修改其他使用者、應用程式或安全性群組在主要電子倉庫上所擁有的許可權。</span><span class="sxs-lookup"><span data-stu-id="75044-122">It does not modify the permissions that other users, applications, or security groups have on the key vault.</span></span>
<span data-ttu-id="75044-123">如果您要設定安全性群組的許可權，此操作只會影響該安全性群組中的使用者。</span><span class="sxs-lookup"><span data-stu-id="75044-123">If you are setting permissions for a security group, this operation affects only users in that security group.</span></span>
<span data-ttu-id="75044-124">下列目錄必須都是相同的 Azure 目錄：</span><span class="sxs-lookup"><span data-stu-id="75044-124">The following directories must all be the same Azure directory:</span></span> 
- <span data-ttu-id="75044-125">存放主要電子倉庫之 Azure 訂閱的預設目錄。</span><span class="sxs-lookup"><span data-stu-id="75044-125">The default directory of the Azure subscription in which the key vault resides.</span></span>
- <span data-ttu-id="75044-126">包含您要授予其許可權之使用者或應用程式群組的 Azure 目錄。</span><span class="sxs-lookup"><span data-stu-id="75044-126">The Azure directory that contains the user or application group that you are granting permissions to.</span></span>
<span data-ttu-id="75044-127">不符合這些條件的案例範例，且這個 Cmdlet 將無法運作：</span><span class="sxs-lookup"><span data-stu-id="75044-127">Examples of scenarios when these conditions are not met and this cmdlet will not work are:</span></span> 
- <span data-ttu-id="75044-128">授權其他組織的使用者管理您的主要電子倉庫。</span><span class="sxs-lookup"><span data-stu-id="75044-128">Authorizing a user from a different organization to manage your key vault.</span></span>
<span data-ttu-id="75044-129">每個組織都有自己的目錄。</span><span class="sxs-lookup"><span data-stu-id="75044-129">Each organization has its own directory.</span></span> 
- <span data-ttu-id="75044-130">您的 Azure 帳戶有多個目錄。</span><span class="sxs-lookup"><span data-stu-id="75044-130">Your Azure account has multiple directories.</span></span>
<span data-ttu-id="75044-131">如果您在預設目錄以外的目錄中登錄應用程式，您就無法授權該應用程式使用您的金鑰保存庫。</span><span class="sxs-lookup"><span data-stu-id="75044-131">If you register an application in a directory other than the default directory, you cannot authorize that application to use your key vault.</span></span>
<span data-ttu-id="75044-132">應用程式必須位於預設目錄中。</span><span class="sxs-lookup"><span data-stu-id="75044-132">The application must be in the default directory.</span></span>
<span data-ttu-id="75044-133">請注意，雖然為這個 Cmdlet 指定 [資源群組] 是選擇性的，但您應該這麼做，以取得較佳的效能。</span><span class="sxs-lookup"><span data-stu-id="75044-133">Note that although specifying the resource group is optional for this cmdlet, you should do so for better performance.</span></span>

## <span data-ttu-id="75044-134">示例</span><span class="sxs-lookup"><span data-stu-id="75044-134">EXAMPLES</span></span>

### <span data-ttu-id="75044-135">範例1：針對金鑰電子倉庫的使用者授與許可權，並修改許可權</span><span class="sxs-lookup"><span data-stu-id="75044-135">Example 1: Grant permissions to a user for a key vault and modify the permissions</span></span>
```powershell
PS C:\> Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToKeys create,import,delete,list -PermissionsToSecrets set,delete -PassThru

Vault Name                       : Contoso03Vault
Resource Group Name              : myrg
Location                         : westus
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers
                                   /Microsoft.KeyVault/vaults/contoso03vault
Vault URI                        : https://contoso03vault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Standard
Enabled For Deployment?          : True
Enabled For Template Deployment? : False
Enabled For Disk Encryption?     : False
Soft Delete Enabled?             : True
Access Policies                  :
                                   Tenant ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Object ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Application ID                             :
                                   Display Name                               : User Name (username@microsoft.com)
                                   Permissions to Keys                        : create, import, delete, list
                                   Permissions to Secrets                     : set, delete
                                   Permissions to Certificates                :
                                   Permissions to (Key Vault Managed) Storage :

Tags                             :

PS C:\> Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToSecrets set,delete,get -PassThru

Vault Name                       : Contoso03Vault
Resource Group Name              : myrg
Location                         : westus
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers
                                   /Microsoft.KeyVault/vaults/contoso03vault
Vault URI                        : https://contoso03vault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Standard
Enabled For Deployment?          : True
Enabled For Template Deployment? : False
Enabled For Disk Encryption?     : False
Soft Delete Enabled?             : True
Access Policies                  :
                                   Tenant ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Object ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Application ID                             :
                                   Display Name                               : User Name (username@microsoft.com)
                                   Permissions to Keys                        : create, import, delete, list
                                   Permissions to Secrets                     : set, delete, get
                                   Permissions to Certificates                :
                                   Permissions to (Key Vault Managed) Storage :

Tags                             :

PS C:\> Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToKeys @() -PassThru

Vault Name                       : Contoso03Vault
Resource Group Name              : myrg
Location                         : westus
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers
                                   /Microsoft.KeyVault/vaults/contoso03vault
Vault URI                        : https://contoso03vault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Standard
Enabled For Deployment?          : True
Enabled For Template Deployment? : False
Enabled For Disk Encryption?     : False
Soft Delete Enabled?             : True
Access Policies                  :
                                   Tenant ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Object ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Application ID                             :
                                   Display Name                               : User Name (username@microsoft.com)
                                   Permissions to Keys                        :
                                   Permissions to Secrets                     : set, delete, get
                                   Permissions to Certificates                :
                                   Permissions to (Key Vault Managed) Storage :

Tags                             :
```

<span data-ttu-id="75044-136">第一個命令會在您的 Azure Active Directory 中為使用者授予許可權， PattiFuller@contoso.com 以在名為 Contoso03Vault 的金鑰保存庫中執行金鑰和密碼的操作。</span><span class="sxs-lookup"><span data-stu-id="75044-136">The first command grants permissions for a user in your Azure Active Directory, PattiFuller@contoso.com, to perform operations on keys and secrets with a key vault named Contoso03Vault.</span></span> <span data-ttu-id="75044-137">*PassThru* 參數會產生 Cmdlet 傳回的更新物件。</span><span class="sxs-lookup"><span data-stu-id="75044-137">The *PassThru* parameter results in the updated object being returned by the cmdlet.</span></span>
<span data-ttu-id="75044-138">第二個命令會修改 PattiFuller@contoso.com 在第一個命令中所授的許可權，現在允許取得機密，除了設定及刪除密碼以外。</span><span class="sxs-lookup"><span data-stu-id="75044-138">The second command modifies the permissions that were granted to PattiFuller@contoso.com in the first command, to now allow getting secrets in addition to setting and deleting them.</span></span> <span data-ttu-id="75044-139">此命令之後，對主要作業的許可權會保持不變。</span><span class="sxs-lookup"><span data-stu-id="75044-139">The permissions to key operations remain unchanged after this command.</span></span>
<span data-ttu-id="75044-140">最後一個命令會進一步修改現有的許可權，以 PattiFuller@contoso.com 移除擁有權限的主要操作。</span><span class="sxs-lookup"><span data-stu-id="75044-140">The final command further modifies the existing permissions for PattiFuller@contoso.com to remove all permissions to key operations.</span></span> <span data-ttu-id="75044-141">此命令之後，機密作業的許可權會保持不變。</span><span class="sxs-lookup"><span data-stu-id="75044-141">The permissions to secret operations remain unchanged after this command.</span></span> 

### <span data-ttu-id="75044-142">範例2：將應用程式服務主體的許可權授予讀取及撰寫機密的許可權</span><span class="sxs-lookup"><span data-stu-id="75044-142">Example 2: Grant permissions for an application service principal to read and write secrets</span></span>
```powershell
PS C:\> Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ServicePrincipalName 'http://payroll.contoso.com' -PermissionsToSecrets Get,Set
```

<span data-ttu-id="75044-143">這個命令會為應用程式授予一個名為 Contoso03Vault 的金鑰保存庫的許可權。</span><span class="sxs-lookup"><span data-stu-id="75044-143">This command grants permissions for an application for a key vault named Contoso03Vault.</span></span> <span data-ttu-id="75044-144">*ServicePrincipalName* 參數會指定應用程式。</span><span class="sxs-lookup"><span data-stu-id="75044-144">The *ServicePrincipalName* parameter specifies the application.</span></span> <span data-ttu-id="75044-145">應用程式必須在您的 Azure Active Directory 中註冊。</span><span class="sxs-lookup"><span data-stu-id="75044-145">The application must be registered in your Azure Active Directory.</span></span> <span data-ttu-id="75044-146">*ServicePrincipalName* 參數的值必須是應用程式的服務主體名稱或應用程式識別碼 GUID。</span><span class="sxs-lookup"><span data-stu-id="75044-146">The value of the *ServicePrincipalName* parameter must be either the service principal name of the application or the application ID GUID.</span></span>
<span data-ttu-id="75044-147">這個範例會指定服務主體名稱 http://payroll.contoso.com ，且命令會授與寫入密碼的應用程式許可權。</span><span class="sxs-lookup"><span data-stu-id="75044-147">This example specifies the service principal name http://payroll.contoso.com, and the command grants the application permissions to read and write secrets.</span></span>

### <span data-ttu-id="75044-148">範例3：使用物件識別碼為應用程式授與許可權</span><span class="sxs-lookup"><span data-stu-id="75044-148">Example 3: Grant permissions for an application using its object ID</span></span>
```powershell
PS C:\> Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ObjectId 34595082-9346-41b6-8d6b-295a2808b8db -PermissionsToSecrets Get,Set
```

<span data-ttu-id="75044-149">這個命令會授與寫入密碼的應用程式許可權。</span><span class="sxs-lookup"><span data-stu-id="75044-149">This command grants the application permissions to read and write secrets.</span></span>
<span data-ttu-id="75044-150">這個範例會使用應用程式服務主體的物件識別碼來指定應用程式。</span><span class="sxs-lookup"><span data-stu-id="75044-150">This example specifies the application using the object ID of the service principal of the application.</span></span>

### <span data-ttu-id="75044-151">範例4：為使用者主要名稱授與許可權</span><span class="sxs-lookup"><span data-stu-id="75044-151">Example 4: Grant permissions for a user principal name</span></span>
```powershell
PS C:\> Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToSecrets Get,List,Set
```

<span data-ttu-id="75044-152">這個命令會針對針對密碼存取權的指定使用者主要名稱，授與 [取得]、[清單] 和 [設定] 許可權。</span><span class="sxs-lookup"><span data-stu-id="75044-152">This command grants get, list, and set permissions for the specified user principal name for access to secrets.</span></span>

### <span data-ttu-id="75044-153">範例5：讓 Microsoft 能從金鑰保存庫取得機密。計算資源提供者</span><span class="sxs-lookup"><span data-stu-id="75044-153">Example 5: Enable secrets to be retrieved from a key vault by the Microsoft.Compute resource provider</span></span>
```powershell
PS C:\> Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnabledForDeployment
```

<span data-ttu-id="75044-154">這個命令會授與 Microsoft. 計算資源提供者在 Contoso03Vault 金鑰保存庫中檢索的密碼許可權。</span><span class="sxs-lookup"><span data-stu-id="75044-154">This command grants the permissions for secrets to be retrieved from the Contoso03Vault key vault by the Microsoft.Compute resource provider.</span></span>

### <span data-ttu-id="75044-155">範例6：授與安全性群組的許可權</span><span class="sxs-lookup"><span data-stu-id="75044-155">Example 6: Grant permissions to a security group</span></span>
```powershell
PS C:\> Get-AzureRmADGroup
PS C:\> Set-AzureRmKeyVaultAccessPolicy -VaultName 'myownvault' -ObjectId (Get-AzureRmADGroup -SearchString 'group2')[0].Id -PermissionsToKeys get, set -PermissionsToSecrets get, set
```

<span data-ttu-id="75044-156">第一個命令使用 Get-AzureRmADGroup Cmdlet 來取得所有 Active Directory 群組。</span><span class="sxs-lookup"><span data-stu-id="75044-156">The first command uses the Get-AzureRmADGroup cmdlet to get all Active Directory groups.</span></span> <span data-ttu-id="75044-157">從輸出中，您會看到3個群組傳回、命名為 [ **group1** ]、[ **group2** ] 和 [ **group3** ]。</span><span class="sxs-lookup"><span data-stu-id="75044-157">From the output, you see 3 groups returned, named **group1** , **group2** , and **group3**.</span></span> <span data-ttu-id="75044-158">多個群組可以有相同的名稱，但永遠都是唯一的 ObjectId。</span><span class="sxs-lookup"><span data-stu-id="75044-158">Multiple groups can have the same name but always have a unique ObjectId.</span></span> <span data-ttu-id="75044-159">如果傳回多個同名的群組，請使用輸出中的 ObjectId 來識別您想要使用的群組。</span><span class="sxs-lookup"><span data-stu-id="75044-159">When more than one group that has the same name is returned, use the ObjectId in the output to identify the one you want to use.</span></span>
<span data-ttu-id="75044-160">接著，您可以使用此命令的輸出，將 group2 的許可權授 Set-AzureRmKeyVaultAccessPolicy 與您的主要保存庫（名為 **myownvault** ）。</span><span class="sxs-lookup"><span data-stu-id="75044-160">You then use the output of this command with Set-AzureRmKeyVaultAccessPolicy to grant permissions to group2 for your key vault, named **myownvault**.</span></span> <span data-ttu-id="75044-161">這個範例列舉了相同命令列中以「group2」為內聯的群組。</span><span class="sxs-lookup"><span data-stu-id="75044-161">This example enumerates the groups named 'group2' inline in the same command line.</span></span>
<span data-ttu-id="75044-162">傳回的清單中可能有多個名為「group2」的群組。</span><span class="sxs-lookup"><span data-stu-id="75044-162">There may be multiple groups in the returned list that are named 'group2'.</span></span>
<span data-ttu-id="75044-163">這個範例會選取第一個專案，並在 \[ \] 傳回的清單中以 index 0 所示。</span><span class="sxs-lookup"><span data-stu-id="75044-163">This example picks the first one, indicated by index \[0\] in the returned list.</span></span>

### <span data-ttu-id="75044-164">範例7：授與客戶管理的租使用者金鑰 (BYOK) 的 Azure 資訊保護存取權</span><span class="sxs-lookup"><span data-stu-id="75044-164">Example 7: Grant Azure Information Protection access to the customer-managed tenant key (BYOK)</span></span>
```powershell
PS C:\> Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso04Vault' -ServicePrincipalName 00000012-0000-0000-c000-000000000000 -PermissionsToKeys decrypt,sign,get
```

<span data-ttu-id="75044-165">這個命令授權 Azure 資訊保護使用客戶管理的金鑰 (將您自己的金鑰或 "BYOK" 案例) 為 Azure 資訊保護租使用者金鑰。</span><span class="sxs-lookup"><span data-stu-id="75044-165">This command authorizes Azure Information Protection to use a customer-managed key (the bring your own key, or "BYOK" scenario) as the Azure Information Protection tenant key.</span></span>
<span data-ttu-id="75044-166">當您執行此命令時，請指定您自己的金鑰保存庫名稱，但您必須指定具有 GUID **00000012-0000-0000-c000-000000000000** 的 *ServicePrincipalName* 參數，並指定範例中的許可權。</span><span class="sxs-lookup"><span data-stu-id="75044-166">When you run this command, specify your own key vault name but you must specify the *ServicePrincipalName* parameter with the GUID **00000012-0000-0000-c000-000000000000** and specify the permissions in the example.</span></span>

## <span data-ttu-id="75044-167">參數</span><span class="sxs-lookup"><span data-stu-id="75044-167">PARAMETERS</span></span>

### <span data-ttu-id="75044-168">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="75044-168">-ApplicationId</span></span>
<span data-ttu-id="75044-169">以供日後使用。</span><span class="sxs-lookup"><span data-stu-id="75044-169">For future use.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: ByObjectId, InputObjectByObjectId, ResourceIdByObjectId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75044-170">-BypassObjectIdValidation</span><span class="sxs-lookup"><span data-stu-id="75044-170">-BypassObjectIdValidation</span></span>
<span data-ttu-id="75044-171">可讓您指定物件識別碼，而不驗證該物件存在於 Azure Active Directory 中。</span><span class="sxs-lookup"><span data-stu-id="75044-171">Enables you to specify an object ID without validating that the object exists in Azure Active Directory.</span></span>
<span data-ttu-id="75044-172">如果您想要將您的金鑰保存庫存取權授予參照來自其他 Azure 租使用者的委派安全性群組的物件識別碼，請使用此參數。</span><span class="sxs-lookup"><span data-stu-id="75044-172">Use this parameter only if you want to grant access to your key vault to an object ID that refers to a delegated security group from another Azure tenant.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByObjectId, InputObjectByObjectId, ResourceIdByObjectId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75044-173">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75044-173">-DefaultProfile</span></span>
<span data-ttu-id="75044-174">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="75044-174">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75044-175">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="75044-175">-EmailAddress</span></span>
<span data-ttu-id="75044-176">指定要授與許可權的使用者的使用者電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="75044-176">Specifies the user email address of the user to whom to grant permissions.</span></span>
<span data-ttu-id="75044-177">此電子郵件地址必須存在於與目前訂閱相關聯的目錄中，且必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="75044-177">This email address must exist in the directory associated with the current subscription and be unique.</span></span>

```yaml
Type: System.String
Parameter Sets: ByEmailAddress, InputObjectByEmailAddress, ResourceIdByEmailAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75044-178">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="75044-178">-EnabledForDeployment</span></span>
<span data-ttu-id="75044-179">當在資源建立期間參照此金鑰保存庫時，可使用 Microsoft. 計算資源提供者來從此金鑰保存庫中取得機密資訊，例如建立虛擬機器時。</span><span class="sxs-lookup"><span data-stu-id="75044-179">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForVault, InputObjectForVault, ResourceIdForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75044-180">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="75044-180">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="75044-181">讓 Azure 磁片加密服務從此金鑰保存庫取得機密和解除解包金鑰。</span><span class="sxs-lookup"><span data-stu-id="75044-181">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForVault, InputObjectForVault, ResourceIdForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75044-182">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="75044-182">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="75044-183">在範本部署中參照此金鑰保存庫時，允許 Azure 資源管理員從該金鑰保存庫取得機密。</span><span class="sxs-lookup"><span data-stu-id="75044-183">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForVault, InputObjectForVault, ResourceIdForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75044-184">-InputObject</span><span class="sxs-lookup"><span data-stu-id="75044-184">-InputObject</span></span>
<span data-ttu-id="75044-185">金鑰保存庫物件</span><span class="sxs-lookup"><span data-stu-id="75044-185">Key Vault Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem
Parameter Sets: InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, InputObjectForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="75044-186">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="75044-186">-ObjectId</span></span>
<span data-ttu-id="75044-187">指定 Azure Active Directory 中要授與許可權的使用者或服務主體物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="75044-187">Specifies the object ID of the user or service principal in Azure Active Directory for which to grant permissions.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectId, InputObjectByObjectId, ResourceIdByObjectId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75044-188">-PassThru</span><span class="sxs-lookup"><span data-stu-id="75044-188">-PassThru</span></span>
<span data-ttu-id="75044-189">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="75044-189">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="75044-190">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="75044-190">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75044-191">-PermissionsToCertificates</span><span class="sxs-lookup"><span data-stu-id="75044-191">-PermissionsToCertificates</span></span>
<span data-ttu-id="75044-192">指定要授與使用者或服務主體的憑證許可權陣列。</span><span class="sxs-lookup"><span data-stu-id="75044-192">Specifies an array of certificate permissions to grant to a user or service principal.</span></span>
<span data-ttu-id="75044-193">此參數可接受的值：</span><span class="sxs-lookup"><span data-stu-id="75044-193">The acceptable values for this parameter:</span></span>
- <span data-ttu-id="75044-194">獲取</span><span class="sxs-lookup"><span data-stu-id="75044-194">Get</span></span>
- <span data-ttu-id="75044-195">清單</span><span class="sxs-lookup"><span data-stu-id="75044-195">List</span></span>
- <span data-ttu-id="75044-196">Delete</span><span class="sxs-lookup"><span data-stu-id="75044-196">Delete</span></span>
- <span data-ttu-id="75044-197">建立</span><span class="sxs-lookup"><span data-stu-id="75044-197">Create</span></span>
- <span data-ttu-id="75044-198">Import</span><span class="sxs-lookup"><span data-stu-id="75044-198">Import</span></span>
- <span data-ttu-id="75044-199">時更新</span><span class="sxs-lookup"><span data-stu-id="75044-199">Update</span></span>
- <span data-ttu-id="75044-200">Managecontacts</span><span class="sxs-lookup"><span data-stu-id="75044-200">Managecontacts</span></span>
- <span data-ttu-id="75044-201">Getissuers</span><span class="sxs-lookup"><span data-stu-id="75044-201">Getissuers</span></span>
- <span data-ttu-id="75044-202">Listissuers</span><span class="sxs-lookup"><span data-stu-id="75044-202">Listissuers</span></span>
- <span data-ttu-id="75044-203">Setissuers</span><span class="sxs-lookup"><span data-stu-id="75044-203">Setissuers</span></span>
- <span data-ttu-id="75044-204">Deleteissuers</span><span class="sxs-lookup"><span data-stu-id="75044-204">Deleteissuers</span></span>
- <span data-ttu-id="75044-205">Manageissuers</span><span class="sxs-lookup"><span data-stu-id="75044-205">Manageissuers</span></span>
- <span data-ttu-id="75044-206">找回</span><span class="sxs-lookup"><span data-stu-id="75044-206">Recover</span></span>
- <span data-ttu-id="75044-207">備份</span><span class="sxs-lookup"><span data-stu-id="75044-207">Backup</span></span>
- <span data-ttu-id="75044-208">還原</span><span class="sxs-lookup"><span data-stu-id="75044-208">Restore</span></span>
- <span data-ttu-id="75044-209">立即</span><span class="sxs-lookup"><span data-stu-id="75044-209">Purge</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress
Aliases:
Accepted values: get, list, delete, create, import, update, managecontacts, getissuers, listissuers, setissuers, deleteissuers, manageissuers, recover, purge, backup, restore

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75044-210">-PermissionsToKeys</span><span class="sxs-lookup"><span data-stu-id="75044-210">-PermissionsToKeys</span></span>
<span data-ttu-id="75044-211">指定要授與使用者或服務主體的主要操作許可權陣列。</span><span class="sxs-lookup"><span data-stu-id="75044-211">Specifies an array of key operation permissions to grant to a user or service principal.</span></span>
<span data-ttu-id="75044-212">此參數可接受的值：</span><span class="sxs-lookup"><span data-stu-id="75044-212">The acceptable values for this parameter:</span></span>
- <span data-ttu-id="75044-213">對</span><span class="sxs-lookup"><span data-stu-id="75044-213">Decrypt</span></span>
- <span data-ttu-id="75044-214">進行</span><span class="sxs-lookup"><span data-stu-id="75044-214">Encrypt</span></span>
- <span data-ttu-id="75044-215">UnwrapKey</span><span class="sxs-lookup"><span data-stu-id="75044-215">UnwrapKey</span></span>
- <span data-ttu-id="75044-216">WrapKey</span><span class="sxs-lookup"><span data-stu-id="75044-216">WrapKey</span></span>
- <span data-ttu-id="75044-217">是否</span><span class="sxs-lookup"><span data-stu-id="75044-217">Verify</span></span>
- <span data-ttu-id="75044-218">母音</span><span class="sxs-lookup"><span data-stu-id="75044-218">Sign</span></span>
- <span data-ttu-id="75044-219">獲取</span><span class="sxs-lookup"><span data-stu-id="75044-219">Get</span></span>
- <span data-ttu-id="75044-220">清單</span><span class="sxs-lookup"><span data-stu-id="75044-220">List</span></span>
- <span data-ttu-id="75044-221">時更新</span><span class="sxs-lookup"><span data-stu-id="75044-221">Update</span></span>
- <span data-ttu-id="75044-222">建立</span><span class="sxs-lookup"><span data-stu-id="75044-222">Create</span></span>
- <span data-ttu-id="75044-223">Import</span><span class="sxs-lookup"><span data-stu-id="75044-223">Import</span></span>
- <span data-ttu-id="75044-224">Delete</span><span class="sxs-lookup"><span data-stu-id="75044-224">Delete</span></span>
- <span data-ttu-id="75044-225">備份</span><span class="sxs-lookup"><span data-stu-id="75044-225">Backup</span></span>
- <span data-ttu-id="75044-226">還原</span><span class="sxs-lookup"><span data-stu-id="75044-226">Restore</span></span>
- <span data-ttu-id="75044-227">找回</span><span class="sxs-lookup"><span data-stu-id="75044-227">Recover</span></span>
- <span data-ttu-id="75044-228">立即</span><span class="sxs-lookup"><span data-stu-id="75044-228">Purge</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress
Aliases:
Accepted values: decrypt, encrypt, unwrapKey, wrapKey, verify, sign, get, list, update, create, import, delete, backup, restore, recover, purge

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75044-229">-PermissionsToSecrets</span><span class="sxs-lookup"><span data-stu-id="75044-229">-PermissionsToSecrets</span></span>
<span data-ttu-id="75044-230">指定要授與使用者或服務主體的機密操作許可權陣列。</span><span class="sxs-lookup"><span data-stu-id="75044-230">Specifies an array of secret operation permissions to grant to a user or service principal.</span></span>
<span data-ttu-id="75044-231">此參數可接受的值：</span><span class="sxs-lookup"><span data-stu-id="75044-231">The acceptable values for this parameter:</span></span>
- <span data-ttu-id="75044-232">獲取</span><span class="sxs-lookup"><span data-stu-id="75044-232">Get</span></span>
- <span data-ttu-id="75044-233">清單</span><span class="sxs-lookup"><span data-stu-id="75044-233">List</span></span>
- <span data-ttu-id="75044-234">設定</span><span class="sxs-lookup"><span data-stu-id="75044-234">Set</span></span>
- <span data-ttu-id="75044-235">Delete</span><span class="sxs-lookup"><span data-stu-id="75044-235">Delete</span></span>
- <span data-ttu-id="75044-236">備份</span><span class="sxs-lookup"><span data-stu-id="75044-236">Backup</span></span>
- <span data-ttu-id="75044-237">還原</span><span class="sxs-lookup"><span data-stu-id="75044-237">Restore</span></span>
- <span data-ttu-id="75044-238">找回</span><span class="sxs-lookup"><span data-stu-id="75044-238">Recover</span></span>
- <span data-ttu-id="75044-239">立即</span><span class="sxs-lookup"><span data-stu-id="75044-239">Purge</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress
Aliases:
Accepted values: get, list, set, delete, backup, restore, recover, purge

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75044-240">-PermissionsToStorage</span><span class="sxs-lookup"><span data-stu-id="75044-240">-PermissionsToStorage</span></span>
<span data-ttu-id="75044-241">指定受管理的儲存帳戶和 SaS 定義操作許可權，以授與使用者或服務主體。</span><span class="sxs-lookup"><span data-stu-id="75044-241">Specifies managed storage account and SaS-definition operation permissions to grant to a user or service principal.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress
Aliases:
Accepted values: get, list, delete, set, update, regeneratekey, getsas, listsas, deletesas, setsas, recover, backup, restore, purge

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75044-242">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75044-242">-ResourceGroupName</span></span>
<span data-ttu-id="75044-243">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="75044-243">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, ForVault
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75044-244">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="75044-244">-ResourceId</span></span>
<span data-ttu-id="75044-245">主要保存庫資源識別碼</span><span class="sxs-lookup"><span data-stu-id="75044-245">Key Vault Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress, ResourceIdForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75044-246">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="75044-246">-ServicePrincipalName</span></span>
<span data-ttu-id="75044-247">指定要授與許可權之應用程式的服務主體名稱。</span><span class="sxs-lookup"><span data-stu-id="75044-247">Specifies the service principal name of the application to which to grant permissions.</span></span>
<span data-ttu-id="75044-248">指定在 AzureActive 目錄中為應用程式註冊的應用程式識別碼（也稱為「用戶端識別碼」）。</span><span class="sxs-lookup"><span data-stu-id="75044-248">Specify the application ID, also known as client ID, registered for the application in AzureActive Directory.</span></span> <span data-ttu-id="75044-249">具有此參數指定之服務主體名稱的應用程式，必須在包含您目前訂閱的 Azure 目錄中註冊。</span><span class="sxs-lookup"><span data-stu-id="75044-249">The application with the service principal name that this parameter specifies must be registered in the Azure directory that contains your current subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServicePrincipalName, InputObjectByServicePrincipalName, ResourceIdByServicePrincipalName
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75044-250">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="75044-250">-UserPrincipalName</span></span>
<span data-ttu-id="75044-251">指定要授與許可權的使用者的使用者主要名稱。</span><span class="sxs-lookup"><span data-stu-id="75044-251">Specifies the user principal name of the user to whom to grant permissions.</span></span>
<span data-ttu-id="75044-252">此使用者主要名稱必須存在於與目前訂閱相關聯的目錄中。</span><span class="sxs-lookup"><span data-stu-id="75044-252">This user principal name must exist in the directory associated with the current subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ByUserPrincipalName, InputObjectByUserPrincipalName, ResourceIdByUserPrincipalName
Aliases: UPN

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75044-253">-VaultName</span><span class="sxs-lookup"><span data-stu-id="75044-253">-VaultName</span></span>
<span data-ttu-id="75044-254">指定主要電子倉庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="75044-254">Specifies the name of a key vault.</span></span>
<span data-ttu-id="75044-255">這個 Cmdlet 會修改此參數指定之金鑰保存庫的存取原則。</span><span class="sxs-lookup"><span data-stu-id="75044-255">This cmdlet modifies the access policy for the key vault that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, ForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75044-256">-確認</span><span class="sxs-lookup"><span data-stu-id="75044-256">-Confirm</span></span>
<span data-ttu-id="75044-257">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="75044-257">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75044-258">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75044-258">-WhatIf</span></span>
<span data-ttu-id="75044-259">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="75044-259">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="75044-260">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="75044-260">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75044-261">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75044-261">CommonParameters</span></span>
<span data-ttu-id="75044-262">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="75044-262">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75044-263">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="75044-263">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75044-264">輸入</span><span class="sxs-lookup"><span data-stu-id="75044-264">INPUTS</span></span>

### <span data-ttu-id="75044-265">PSKeyVaultIdentityItem 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="75044-265">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>
<span data-ttu-id="75044-266">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="75044-266">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="75044-267">System.object</span><span class="sxs-lookup"><span data-stu-id="75044-267">System.String</span></span>

## <span data-ttu-id="75044-268">輸出</span><span class="sxs-lookup"><span data-stu-id="75044-268">OUTPUTS</span></span>

### <span data-ttu-id="75044-269">PSKeyVault 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="75044-269">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="75044-270">筆記</span><span class="sxs-lookup"><span data-stu-id="75044-270">NOTES</span></span>

## <span data-ttu-id="75044-271">相關連結</span><span class="sxs-lookup"><span data-stu-id="75044-271">RELATED LINKS</span></span>

[<span data-ttu-id="75044-272">AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="75044-272">Get-AzureRmKeyVault</span></span>](./Get-AzureRmKeyVault.md)

[<span data-ttu-id="75044-273">移除-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="75044-273">Remove-AzureRmKeyVaultAccessPolicy</span></span>](./Remove-AzureRmKeyVaultAccessPolicy.md)

