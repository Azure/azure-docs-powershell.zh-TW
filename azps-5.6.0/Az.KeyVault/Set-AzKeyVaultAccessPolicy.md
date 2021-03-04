---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 636FAD5B-8C39-4E5C-8978-6845C6B89BC0
online version: https://docs.microsoft.com/powershell/module/az.keyvault/set-azkeyvaultaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultAccessPolicy.md
ms.openlocfilehash: 77f6ac36f756e89859d38a0c608139dfe28c9667
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902569"
---
# <span data-ttu-id="e5422-101">Set-AzKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e5422-101">Set-AzKeyVaultAccessPolicy</span></span>

## <span data-ttu-id="e5422-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e5422-102">SYNOPSIS</span></span>
<span data-ttu-id="e5422-103">授予或修改使用者、應用程式或安全性群組的現有許可權，以使用金鑰庫執行作業。</span><span class="sxs-lookup"><span data-stu-id="e5422-103">Grants or modifies existing permissions for a user, application, or security group to perform operations with a key vault.</span></span>

## <span data-ttu-id="e5422-104">語法</span><span class="sxs-lookup"><span data-stu-id="e5422-104">SYNTAX</span></span>

### <span data-ttu-id="e5422-105">ByUserPrincipalName (預設) </span><span class="sxs-lookup"><span data-stu-id="e5422-105">ByUserPrincipalName (Default)</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -UserPrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e5422-106">ByObjectId</span><span class="sxs-lookup"><span data-stu-id="e5422-106">ByObjectId</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ObjectId <String>
 [-ApplicationId <Guid>] [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5422-107">ByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="e5422-107">ByServicePrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ServicePrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e5422-108">ByEmailAddress</span><span class="sxs-lookup"><span data-stu-id="e5422-108">ByEmailAddress</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -EmailAddress <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e5422-109">ForVault</span><span class="sxs-lookup"><span data-stu-id="e5422-109">ForVault</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5422-110">InputObjectByObjectId</span><span class="sxs-lookup"><span data-stu-id="e5422-110">InputObjectByObjectId</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -ObjectId <String> [-ApplicationId <Guid>]
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5422-111">InputObjectByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="e5422-111">InputObjectByServicePrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -ServicePrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e5422-112">InputObjectByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="e5422-112">InputObjectByUserPrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -UserPrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e5422-113">InputObjectByEmailAddress</span><span class="sxs-lookup"><span data-stu-id="e5422-113">InputObjectByEmailAddress</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -EmailAddress <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e5422-114">InputObjectForVault</span><span class="sxs-lookup"><span data-stu-id="e5422-114">InputObjectForVault</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5422-115">ResourceIdByObjectId</span><span class="sxs-lookup"><span data-stu-id="e5422-115">ResourceIdByObjectId</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -ObjectId <String> [-ApplicationId <Guid>]
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5422-116">ResourceIdByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="e5422-116">ResourceIdByServicePrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -ServicePrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e5422-117">ResourceIdByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="e5422-117">ResourceIdByUserPrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -UserPrincipalName <String> [-PermissionsToKeys <String[]>]
 [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5422-118">ResourceIdByEmailAddress</span><span class="sxs-lookup"><span data-stu-id="e5422-118">ResourceIdByEmailAddress</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -EmailAddress <String> [-PermissionsToKeys <String[]>]
 [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5422-119">ResourceIdForVault</span><span class="sxs-lookup"><span data-stu-id="e5422-119">ResourceIdForVault</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> [-EnabledForDeployment] [-EnabledForTemplateDeployment]
 [-EnabledForDiskEncryption] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e5422-120">描述</span><span class="sxs-lookup"><span data-stu-id="e5422-120">DESCRIPTION</span></span>
<span data-ttu-id="e5422-121">**Set-AzKeyVaultAccessPolicy** Cmdlet 會授予或修改使用者、應用程式或安全性群組的現有許可權，以使用金鑰庫執行指定的作業。</span><span class="sxs-lookup"><span data-stu-id="e5422-121">The **Set-AzKeyVaultAccessPolicy** cmdlet grants or modifies existing permissions for a user, application, or security group to perform the specified operations with a key vault.</span></span> <span data-ttu-id="e5422-122">它不會修改其他使用者、應用程式或安全性群組在金鑰庫上擁有的許可權。</span><span class="sxs-lookup"><span data-stu-id="e5422-122">It does not modify the permissions that other users, applications, or security groups have on the key vault.</span></span>
<span data-ttu-id="e5422-123">如果您要為安全性群組設定許可權，此作業只會影響該安全性群組的使用者。</span><span class="sxs-lookup"><span data-stu-id="e5422-123">If you are setting permissions for a security group, this operation affects only users in that security group.</span></span>
<span data-ttu-id="e5422-124">下列目錄必須都是相同的 Azure 目錄：</span><span class="sxs-lookup"><span data-stu-id="e5422-124">The following directories must all be the same Azure directory:</span></span>
- <span data-ttu-id="e5422-125">金鑰庫所在的 Azure 訂閱預設目錄。</span><span class="sxs-lookup"><span data-stu-id="e5422-125">The default directory of the Azure subscription in which the key vault resides.</span></span>
- <span data-ttu-id="e5422-126">包含您授予許可權之使用者或應用程式群組的 Azure 目錄。</span><span class="sxs-lookup"><span data-stu-id="e5422-126">The Azure directory that contains the user or application group that you are granting permissions to.</span></span>
<span data-ttu-id="e5422-127">這些條件未符合且此 Cmdlet 無法工作的範例如下：</span><span class="sxs-lookup"><span data-stu-id="e5422-127">Examples of scenarios when these conditions are not met and this cmdlet will not work are:</span></span>
- <span data-ttu-id="e5422-128">授權不同組織的使用者管理您的金鑰庫。</span><span class="sxs-lookup"><span data-stu-id="e5422-128">Authorizing a user from a different organization to manage your key vault.</span></span>
<span data-ttu-id="e5422-129">每個組織都有自己的目錄。</span><span class="sxs-lookup"><span data-stu-id="e5422-129">Each organization has its own directory.</span></span>
- <span data-ttu-id="e5422-130">您的 Azure 帳戶有多個目錄。</span><span class="sxs-lookup"><span data-stu-id="e5422-130">Your Azure account has multiple directories.</span></span>
<span data-ttu-id="e5422-131">如果您在預設目錄外的其他目錄中註冊應用程式，您無法授權該應用程式使用您的金鑰庫。</span><span class="sxs-lookup"><span data-stu-id="e5422-131">If you register an application in a directory other than the default directory, you cannot authorize that application to use your key vault.</span></span>
<span data-ttu-id="e5422-132">應用程式必須位在預設目錄中。</span><span class="sxs-lookup"><span data-stu-id="e5422-132">The application must be in the default directory.</span></span>
<span data-ttu-id="e5422-133">請注意，雖然指定資源群組是這個 Cmdlet 的選擇性專案，但您應這麼做以提升績效。</span><span class="sxs-lookup"><span data-stu-id="e5422-133">Note that although specifying the resource group is optional for this cmdlet, you should do so for better performance.</span></span>

> [!NOTE]
> <span data-ttu-id="e5422-134">使用服務主體來授予存取策略許可權時，您必須使用 `-BypassObjectIdValidation` 參數。</span><span class="sxs-lookup"><span data-stu-id="e5422-134">When using a service principal to grant access policy permissions, you must use the `-BypassObjectIdValidation` parameter.</span></span>

## <span data-ttu-id="e5422-135">例子</span><span class="sxs-lookup"><span data-stu-id="e5422-135">EXAMPLES</span></span>

### <span data-ttu-id="e5422-136">範例 1：將金鑰庫的許可權授予使用者，並修改許可權</span><span class="sxs-lookup"><span data-stu-id="e5422-136">Example 1: Grant permissions to a user for a key vault and modify the permissions</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToKeys create,import,delete,list -PermissionsToSecrets set,delete -PassThru

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

PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToSecrets set,delete,get -PassThru

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

PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToKeys @() -PassThru

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

<span data-ttu-id="e5422-137">第一個命令會授予您 Azure Active Directory 中使用者的許可權，以使用名稱為 PattiFuller@contoso.com Contoso03Vault 的金鑰庫來執行金鑰和機密作業。</span><span class="sxs-lookup"><span data-stu-id="e5422-137">The first command grants permissions for a user in your Azure Active Directory, PattiFuller@contoso.com, to perform operations on keys and secrets with a key vault named Contoso03Vault.</span></span> <span data-ttu-id="e5422-138">*PassThru 參數* 會導致 Cmdlet 傳回更新的物件。</span><span class="sxs-lookup"><span data-stu-id="e5422-138">The *PassThru* parameter results in the updated object being returned by the cmdlet.</span></span>
<span data-ttu-id="e5422-139">第二個命令會修改第一個命令中授予的許可權，現在除了設定和刪除外，也允許取得 PattiFuller@contoso.com 機密。</span><span class="sxs-lookup"><span data-stu-id="e5422-139">The second command modifies the permissions that were granted to PattiFuller@contoso.com in the first command, to now allow getting secrets in addition to setting and deleting them.</span></span> <span data-ttu-id="e5422-140">此命令之後，按鍵作業的許可權會維持不變。</span><span class="sxs-lookup"><span data-stu-id="e5422-140">The permissions to key operations remain unchanged after this command.</span></span>
<span data-ttu-id="e5422-141">最後一個命令會進一步修改現有許可權， PattiFuller@contoso.com 以移除金鑰作業的擁有權限。</span><span class="sxs-lookup"><span data-stu-id="e5422-141">The final command further modifies the existing permissions for PattiFuller@contoso.com to remove all permissions to key operations.</span></span> <span data-ttu-id="e5422-142">此命令之後，機密作業的許可權會維持不變。</span><span class="sxs-lookup"><span data-stu-id="e5422-142">The permissions to secret operations remain unchanged after this command.</span></span>

### <span data-ttu-id="e5422-143">範例 2：授予應用程式服務主體讀取和寫入機密的許可權</span><span class="sxs-lookup"><span data-stu-id="e5422-143">Example 2: Grant permissions for an application service principal to read and write secrets</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ServicePrincipalName 'http://payroll.contoso.com' -PermissionsToSecrets Get,Set
```

<span data-ttu-id="e5422-144">此命令會為名為 Contoso03Vault 之金鑰庫的應用程式授予許可權。</span><span class="sxs-lookup"><span data-stu-id="e5422-144">This command grants permissions for an application for a key vault named Contoso03Vault.</span></span>
<span data-ttu-id="e5422-145">*ServicePrincipalName* 參數會指定應用程式。</span><span class="sxs-lookup"><span data-stu-id="e5422-145">The *ServicePrincipalName* parameter specifies the application.</span></span> <span data-ttu-id="e5422-146">應用程式必須在 Azure Active Directory 中註冊。</span><span class="sxs-lookup"><span data-stu-id="e5422-146">The application must be registered in your Azure Active Directory.</span></span> <span data-ttu-id="e5422-147">*ServicePrincipalName* 參數的值必須是應用程式的服務主體名稱或應用程式識別碼 GUID。</span><span class="sxs-lookup"><span data-stu-id="e5422-147">The value of the *ServicePrincipalName* parameter must be either the service principal name of the application or the application ID GUID.</span></span>
<span data-ttu-id="e5422-148">此範例會指定服務主體名稱，而命令會授予應用程式讀取及寫入機密 `http://payroll.contoso.com` 的許可權。</span><span class="sxs-lookup"><span data-stu-id="e5422-148">This example specifies the service principal name `http://payroll.contoso.com`, and the command grants the application permissions to read and write secrets.</span></span>

### <span data-ttu-id="e5422-149">範例 3：使用應用程式的物件識別碼授予許可權</span><span class="sxs-lookup"><span data-stu-id="e5422-149">Example 3: Grant permissions for an application using its object ID</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ObjectId 34595082-9346-41b6-8d6b-295a2808b8db -PermissionsToSecrets Get,Set
```

<span data-ttu-id="e5422-150">此命令會授予應用程式讀取及撰寫秘訣的許可權。</span><span class="sxs-lookup"><span data-stu-id="e5422-150">This command grants the application permissions to read and write secrets.</span></span>
<span data-ttu-id="e5422-151">此範例會使用應用程式服務主體的物件識別碼指定應用程式。</span><span class="sxs-lookup"><span data-stu-id="e5422-151">This example specifies the application using the object ID of the service principal of the application.</span></span>

### <span data-ttu-id="e5422-152">範例 4：授予使用者主體名稱的許可權</span><span class="sxs-lookup"><span data-stu-id="e5422-152">Example 4: Grant permissions for a user principal name</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToSecrets Get,List,Set
```

<span data-ttu-id="e5422-153">此命令會為指定的使用者主體名稱轉移存取機密的許可權、清單和設定許可權。</span><span class="sxs-lookup"><span data-stu-id="e5422-153">This command grants get, list, and set permissions for the specified user principal name for access to secrets.</span></span>

### <span data-ttu-id="e5422-154">範例 5：啟用 Microsoft.Compute 資源提供者從金鑰庫取回機密</span><span class="sxs-lookup"><span data-stu-id="e5422-154">Example 5: Enable secrets to be retrieved from a key vault by the Microsoft.Compute resource provider</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnabledForDeployment
```

<span data-ttu-id="e5422-155">此命令會授予 Microsoft.Compute 資源提供者從 Contoso03Vault 金鑰庫所取之機密的許可權。</span><span class="sxs-lookup"><span data-stu-id="e5422-155">This command grants the permissions for secrets to be retrieved from the Contoso03Vault key vault by the Microsoft.Compute resource provider.</span></span>

### <span data-ttu-id="e5422-156">範例 6：將許可權授予安全性群組</span><span class="sxs-lookup"><span data-stu-id="e5422-156">Example 6: Grant permissions to a security group</span></span>
```powershell
PS C:\> Get-AzADGroup
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'myownvault' -ObjectId (Get-AzADGroup -SearchString 'group2')[0].Id -PermissionsToKeys get, set -PermissionsToSecrets get, set
```

<span data-ttu-id="e5422-157">第一個命令會使用 Get-AzADGroup Cmdlet 取得所有 Active Directory 群組。</span><span class="sxs-lookup"><span data-stu-id="e5422-157">The first command uses the Get-AzADGroup cmdlet to get all Active Directory groups.</span></span> <span data-ttu-id="e5422-158">在輸出中，您看到 3 個已返回的群組，名稱為 **group1、group2** 和 **group3。** </span><span class="sxs-lookup"><span data-stu-id="e5422-158">From the output, you see 3 groups returned, named **group1**, **group2**, and **group3**.</span></span> <span data-ttu-id="e5422-159">多個群組可以有相同的名稱，但永遠都有唯一的 ObjectId。</span><span class="sxs-lookup"><span data-stu-id="e5422-159">Multiple groups can have the same name but always have a unique ObjectId.</span></span> <span data-ttu-id="e5422-160">當多個具有相同名稱的群組被退回時，請使用輸出中的 ObjectId 來識別您想要使用的物件。</span><span class="sxs-lookup"><span data-stu-id="e5422-160">When more than one group that has the same name is returned, use the ObjectId in the output to identify the one you want to use.</span></span>
<span data-ttu-id="e5422-161">接著，您將此命令的輸出與 Set-AzKeyVaultAccessPolicy，以將許可權授予名為 **myownvault** 的金鑰庫群組 2。</span><span class="sxs-lookup"><span data-stu-id="e5422-161">You then use the output of this command with Set-AzKeyVaultAccessPolicy to grant permissions to group2 for your key vault, named **myownvault**.</span></span> <span data-ttu-id="e5422-162">此範例會列舉同一命令列中名為 "group2" 的內嵌群組。</span><span class="sxs-lookup"><span data-stu-id="e5422-162">This example enumerates the groups named 'group2' inline in the same command line.</span></span>
<span data-ttu-id="e5422-163">在所退回的清單中，可能有多個群組被命名為'group2'。</span><span class="sxs-lookup"><span data-stu-id="e5422-163">There may be multiple groups in the returned list that are named 'group2'.</span></span>
<span data-ttu-id="e5422-164">此範例會挑選第一個，以所返回清單中的索引 \[ 0 \] 表示。</span><span class="sxs-lookup"><span data-stu-id="e5422-164">This example picks the first one, indicated by index \[0\] in the returned list.</span></span>

### <span data-ttu-id="e5422-165">範例 7：將 Azure 資訊保護存取權授予客戶管理的租使用者金鑰 (BYOK) </span><span class="sxs-lookup"><span data-stu-id="e5422-165">Example 7: Grant Azure Information Protection access to the customer-managed tenant key (BYOK)</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso04Vault' -ServicePrincipalName 00000012-0000-0000-c000-000000000000 -PermissionsToKeys decrypt,sign,get
```

<span data-ttu-id="e5422-166">此命令授權 Azure 資訊保護使用客戶管理的金鑰 (您攜帶的金鑰，或「BYOK」案例) 做為 Azure 資訊保護租使用者金鑰。</span><span class="sxs-lookup"><span data-stu-id="e5422-166">This command authorizes Azure Information Protection to use a customer-managed key (the bring your own key, or "BYOK" scenario) as the Azure Information Protection tenant key.</span></span>
<span data-ttu-id="e5422-167">當您執行此命令時，請指定您自己的金鑰庫名稱，但您必須使用 GUID **00000012-0000-c000-0000-00000000000** 指定 *ServicePrincipalName* 參數，並指定範例中的許可權。</span><span class="sxs-lookup"><span data-stu-id="e5422-167">When you run this command, specify your own key vault name but you must specify the *ServicePrincipalName* parameter with the GUID **00000012-0000-0000-c000-000000000000** and specify the permissions in the example.</span></span>

## <span data-ttu-id="e5422-168">參數</span><span class="sxs-lookup"><span data-stu-id="e5422-168">PARAMETERS</span></span>

### <span data-ttu-id="e5422-169">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="e5422-169">-ApplicationId</span></span>
<span data-ttu-id="e5422-170">供日後使用。</span><span class="sxs-lookup"><span data-stu-id="e5422-170">For future use.</span></span>

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

### <span data-ttu-id="e5422-171">-BypassObjectIdValidation</span><span class="sxs-lookup"><span data-stu-id="e5422-171">-BypassObjectIdValidation</span></span>
<span data-ttu-id="e5422-172">可讓您指定物件識別碼，而不驗證該物件存在於 Azure Active Directory 中。</span><span class="sxs-lookup"><span data-stu-id="e5422-172">Enables you to specify an object ID without validating that the object exists in Azure Active Directory.</span></span>
<span data-ttu-id="e5422-173">只有在您想要將金鑰庫存取權授予參照另一個 Azure 租使用者委派安全性群組的物件識別碼時，才使用此參數。</span><span class="sxs-lookup"><span data-stu-id="e5422-173">Use this parameter only if you want to grant access to your key vault to an object ID that refers to a delegated security group from another Azure tenant.</span></span>

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

### <span data-ttu-id="e5422-174">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5422-174">-DefaultProfile</span></span>
<span data-ttu-id="e5422-175">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="e5422-175">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5422-176">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="e5422-176">-EmailAddress</span></span>
<span data-ttu-id="e5422-177">指定要授予許可權之使用者的使用者電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="e5422-177">Specifies the user email address of the user to whom to grant permissions.</span></span>
<span data-ttu-id="e5422-178">這個電子郵件地址必須存在於與目前訂閱相關聯的目錄中，而且是唯一的。</span><span class="sxs-lookup"><span data-stu-id="e5422-178">This email address must exist in the directory associated with the current subscription and be unique.</span></span>

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

### <span data-ttu-id="e5422-179">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="e5422-179">-EnabledForDeployment</span></span>
<span data-ttu-id="e5422-180">當資源建立中參照此金鑰庫時 ，例如建立虛擬機器時，可讓 Microsoft.Compute 資源提供者從這個金鑰庫中取回秘訣。</span><span class="sxs-lookup"><span data-stu-id="e5422-180">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

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

### <span data-ttu-id="e5422-181">-EnabledForCryptEncryption</span><span class="sxs-lookup"><span data-stu-id="e5422-181">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="e5422-182">啟用 Azure 磁片加密服務，以取得金鑰庫中的金鑰和解包金鑰。</span><span class="sxs-lookup"><span data-stu-id="e5422-182">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

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

### <span data-ttu-id="e5422-183">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="e5422-183">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="e5422-184">當範本部署中參照此金鑰庫時，可讓 Azure Resource Manager 從此金鑰庫取得秘訣。</span><span class="sxs-lookup"><span data-stu-id="e5422-184">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

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

### <span data-ttu-id="e5422-185">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e5422-185">-InputObject</span></span>
<span data-ttu-id="e5422-186">Key Vault 物件</span><span class="sxs-lookup"><span data-stu-id="e5422-186">Key Vault Object</span></span>

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

### <span data-ttu-id="e5422-187">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="e5422-187">-ObjectId</span></span>
<span data-ttu-id="e5422-188">指定 Azure Active Directory 中使用者或服務主體的物件識別碼，以授予許可權。</span><span class="sxs-lookup"><span data-stu-id="e5422-188">Specifies the object ID of the user or service principal in Azure Active Directory for which to grant permissions.</span></span>

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

### <span data-ttu-id="e5422-189">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e5422-189">-PassThru</span></span>
<span data-ttu-id="e5422-190">會返回代表您處理之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="e5422-190">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e5422-191">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="e5422-191">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e5422-192">-PermissionsToCertificates</span><span class="sxs-lookup"><span data-stu-id="e5422-192">-PermissionsToCertificates</span></span>
<span data-ttu-id="e5422-193">指定要授予使用者或服務主體的憑證許可權陣列。</span><span class="sxs-lookup"><span data-stu-id="e5422-193">Specifies an array of certificate permissions to grant to a user or service principal.</span></span>
<span data-ttu-id="e5422-194">此參數可接受的值：</span><span class="sxs-lookup"><span data-stu-id="e5422-194">The acceptable values for this parameter:</span></span>
- <span data-ttu-id="e5422-195">所有</span><span class="sxs-lookup"><span data-stu-id="e5422-195">All</span></span>
- <span data-ttu-id="e5422-196">獲取</span><span class="sxs-lookup"><span data-stu-id="e5422-196">Get</span></span>
- <span data-ttu-id="e5422-197">清單</span><span class="sxs-lookup"><span data-stu-id="e5422-197">List</span></span>
- <span data-ttu-id="e5422-198">刪除</span><span class="sxs-lookup"><span data-stu-id="e5422-198">Delete</span></span>
- <span data-ttu-id="e5422-199">創建</span><span class="sxs-lookup"><span data-stu-id="e5422-199">Create</span></span>
- <span data-ttu-id="e5422-200">進口</span><span class="sxs-lookup"><span data-stu-id="e5422-200">Import</span></span>
- <span data-ttu-id="e5422-201">更新</span><span class="sxs-lookup"><span data-stu-id="e5422-201">Update</span></span>
- <span data-ttu-id="e5422-202">Managecontacts</span><span class="sxs-lookup"><span data-stu-id="e5422-202">Managecontacts</span></span>
- <span data-ttu-id="e5422-203">Getissuers</span><span class="sxs-lookup"><span data-stu-id="e5422-203">Getissuers</span></span>
- <span data-ttu-id="e5422-204">Listissuers</span><span class="sxs-lookup"><span data-stu-id="e5422-204">Listissuers</span></span>
- <span data-ttu-id="e5422-205">Setissuers</span><span class="sxs-lookup"><span data-stu-id="e5422-205">Setissuers</span></span>
- <span data-ttu-id="e5422-206">Deleteissuers</span><span class="sxs-lookup"><span data-stu-id="e5422-206">Deleteissuers</span></span>
- <span data-ttu-id="e5422-207">Manageissuers</span><span class="sxs-lookup"><span data-stu-id="e5422-207">Manageissuers</span></span>
- <span data-ttu-id="e5422-208">恢復</span><span class="sxs-lookup"><span data-stu-id="e5422-208">Recover</span></span>
- <span data-ttu-id="e5422-209">備份</span><span class="sxs-lookup"><span data-stu-id="e5422-209">Backup</span></span>
- <span data-ttu-id="e5422-210">恢復</span><span class="sxs-lookup"><span data-stu-id="e5422-210">Restore</span></span>
- <span data-ttu-id="e5422-211">清除</span><span class="sxs-lookup"><span data-stu-id="e5422-211">Purge</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress
Aliases:
Accepted values: all, get, list, delete, create, import, update, managecontacts, getissuers, listissuers, setissuers, deleteissuers, manageissuers, recover, purge, backup, restore

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5422-212">-PermissionsToKeys</span><span class="sxs-lookup"><span data-stu-id="e5422-212">-PermissionsToKeys</span></span>
<span data-ttu-id="e5422-213">指定要授予使用者或服務主體之金鑰作業許可權的陣列。</span><span class="sxs-lookup"><span data-stu-id="e5422-213">Specifies an array of key operation permissions to grant to a user or service principal.</span></span>
<span data-ttu-id="e5422-214">此參數可接受的值：</span><span class="sxs-lookup"><span data-stu-id="e5422-214">The acceptable values for this parameter:</span></span>
- <span data-ttu-id="e5422-215">所有</span><span class="sxs-lookup"><span data-stu-id="e5422-215">All</span></span>
- <span data-ttu-id="e5422-216">解密</span><span class="sxs-lookup"><span data-stu-id="e5422-216">Decrypt</span></span>
- <span data-ttu-id="e5422-217">加密</span><span class="sxs-lookup"><span data-stu-id="e5422-217">Encrypt</span></span>
- <span data-ttu-id="e5422-218">UnwrapKey</span><span class="sxs-lookup"><span data-stu-id="e5422-218">UnwrapKey</span></span>
- <span data-ttu-id="e5422-219">WrapKey</span><span class="sxs-lookup"><span data-stu-id="e5422-219">WrapKey</span></span>
- <span data-ttu-id="e5422-220">驗證</span><span class="sxs-lookup"><span data-stu-id="e5422-220">Verify</span></span>
- <span data-ttu-id="e5422-221">標誌</span><span class="sxs-lookup"><span data-stu-id="e5422-221">Sign</span></span>
- <span data-ttu-id="e5422-222">獲取</span><span class="sxs-lookup"><span data-stu-id="e5422-222">Get</span></span>
- <span data-ttu-id="e5422-223">清單</span><span class="sxs-lookup"><span data-stu-id="e5422-223">List</span></span>
- <span data-ttu-id="e5422-224">更新</span><span class="sxs-lookup"><span data-stu-id="e5422-224">Update</span></span>
- <span data-ttu-id="e5422-225">創建</span><span class="sxs-lookup"><span data-stu-id="e5422-225">Create</span></span>
- <span data-ttu-id="e5422-226">進口</span><span class="sxs-lookup"><span data-stu-id="e5422-226">Import</span></span>
- <span data-ttu-id="e5422-227">刪除</span><span class="sxs-lookup"><span data-stu-id="e5422-227">Delete</span></span>
- <span data-ttu-id="e5422-228">備份</span><span class="sxs-lookup"><span data-stu-id="e5422-228">Backup</span></span>
- <span data-ttu-id="e5422-229">恢復</span><span class="sxs-lookup"><span data-stu-id="e5422-229">Restore</span></span>
- <span data-ttu-id="e5422-230">恢復</span><span class="sxs-lookup"><span data-stu-id="e5422-230">Recover</span></span>
- <span data-ttu-id="e5422-231">清除</span><span class="sxs-lookup"><span data-stu-id="e5422-231">Purge</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress
Aliases:
Accepted values: all, decrypt, encrypt, unwrapKey, wrapKey, verify, sign, get, list, update, create, import, delete, backup, restore, recover, purge

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5422-232">-PermissionsToSecrets</span><span class="sxs-lookup"><span data-stu-id="e5422-232">-PermissionsToSecrets</span></span>
<span data-ttu-id="e5422-233">指定一組機密作業許可權陣列，以授予使用者或服務主體。</span><span class="sxs-lookup"><span data-stu-id="e5422-233">Specifies an array of secret operation permissions to grant to a user or service principal.</span></span>
<span data-ttu-id="e5422-234">此參數可接受的值：</span><span class="sxs-lookup"><span data-stu-id="e5422-234">The acceptable values for this parameter:</span></span>
- <span data-ttu-id="e5422-235">所有</span><span class="sxs-lookup"><span data-stu-id="e5422-235">All</span></span>
- <span data-ttu-id="e5422-236">獲取</span><span class="sxs-lookup"><span data-stu-id="e5422-236">Get</span></span>
- <span data-ttu-id="e5422-237">清單</span><span class="sxs-lookup"><span data-stu-id="e5422-237">List</span></span>
- <span data-ttu-id="e5422-238">設置</span><span class="sxs-lookup"><span data-stu-id="e5422-238">Set</span></span>
- <span data-ttu-id="e5422-239">刪除</span><span class="sxs-lookup"><span data-stu-id="e5422-239">Delete</span></span>
- <span data-ttu-id="e5422-240">備份</span><span class="sxs-lookup"><span data-stu-id="e5422-240">Backup</span></span>
- <span data-ttu-id="e5422-241">恢復</span><span class="sxs-lookup"><span data-stu-id="e5422-241">Restore</span></span>
- <span data-ttu-id="e5422-242">恢復</span><span class="sxs-lookup"><span data-stu-id="e5422-242">Recover</span></span>
- <span data-ttu-id="e5422-243">清除</span><span class="sxs-lookup"><span data-stu-id="e5422-243">Purge</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress
Aliases:
Accepted values: all, get, list, set, delete, backup, restore, recover, purge

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5422-244">-PermissionsToStorage</span><span class="sxs-lookup"><span data-stu-id="e5422-244">-PermissionsToStorage</span></span>
<span data-ttu-id="e5422-245">指定受管理的儲存空間帳戶和 SaS 定義作業許可權，以授予使用者或服務主體。</span><span class="sxs-lookup"><span data-stu-id="e5422-245">Specifies managed storage account and SaS-definition operation permissions to grant to a user or service principal.</span></span>
<span data-ttu-id="e5422-246">此參數可接受的值：</span><span class="sxs-lookup"><span data-stu-id="e5422-246">The acceptable values for this parameter:</span></span>
- <span data-ttu-id="e5422-247">所有</span><span class="sxs-lookup"><span data-stu-id="e5422-247">all</span></span>
- <span data-ttu-id="e5422-248">獲取</span><span class="sxs-lookup"><span data-stu-id="e5422-248">get</span></span>
- <span data-ttu-id="e5422-249">清單</span><span class="sxs-lookup"><span data-stu-id="e5422-249">list</span></span>
- <span data-ttu-id="e5422-250">刪除</span><span class="sxs-lookup"><span data-stu-id="e5422-250">delete</span></span>
- <span data-ttu-id="e5422-251">設置</span><span class="sxs-lookup"><span data-stu-id="e5422-251">set</span></span>
- <span data-ttu-id="e5422-252">更新</span><span class="sxs-lookup"><span data-stu-id="e5422-252">update</span></span>
- <span data-ttu-id="e5422-253">重新產生金鑰</span><span class="sxs-lookup"><span data-stu-id="e5422-253">regeneratekey</span></span>
- <span data-ttu-id="e5422-254">getsas</span><span class="sxs-lookup"><span data-stu-id="e5422-254">getsas</span></span>
- <span data-ttu-id="e5422-255">listsas</span><span class="sxs-lookup"><span data-stu-id="e5422-255">listsas</span></span>
- <span data-ttu-id="e5422-256">deletesas</span><span class="sxs-lookup"><span data-stu-id="e5422-256">deletesas</span></span>
- <span data-ttu-id="e5422-257">setsas</span><span class="sxs-lookup"><span data-stu-id="e5422-257">setsas</span></span>
- <span data-ttu-id="e5422-258">恢復</span><span class="sxs-lookup"><span data-stu-id="e5422-258">recover</span></span>
- <span data-ttu-id="e5422-259">備份</span><span class="sxs-lookup"><span data-stu-id="e5422-259">backup</span></span>
- <span data-ttu-id="e5422-260">恢復</span><span class="sxs-lookup"><span data-stu-id="e5422-260">restore</span></span>
- <span data-ttu-id="e5422-261">清除</span><span class="sxs-lookup"><span data-stu-id="e5422-261">purge</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress
Aliases:
Accepted values: all, get, list, delete, set, update, regeneratekey, getsas, listsas, deletesas, setsas, recover, backup, restore, purge

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5422-262">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5422-262">-ResourceGroupName</span></span>
<span data-ttu-id="e5422-263">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e5422-263">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="e5422-264">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e5422-264">-ResourceId</span></span>
<span data-ttu-id="e5422-265">金鑰庫資源識別碼</span><span class="sxs-lookup"><span data-stu-id="e5422-265">Key Vault Resource Id</span></span>

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

### <span data-ttu-id="e5422-266">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="e5422-266">-ServicePrincipalName</span></span>
<span data-ttu-id="e5422-267">指定要授予許可權之應用程式的服務主體名稱。</span><span class="sxs-lookup"><span data-stu-id="e5422-267">Specifies the service principal name of the application to which to grant permissions.</span></span>
<span data-ttu-id="e5422-268">指定在 AzureActive Directory 中為應用程式註冊的應用程式識別碼 ，也稱為用戶端識別碼。</span><span class="sxs-lookup"><span data-stu-id="e5422-268">Specify the application ID, also known as client ID, registered for the application in AzureActive Directory.</span></span> <span data-ttu-id="e5422-269">具有此參數指定之服務主體名稱的應用程式必須在包含您目前訂閱的 Azure 目錄中註冊。</span><span class="sxs-lookup"><span data-stu-id="e5422-269">The application with the service principal name that this parameter specifies must be registered in the Azure directory that contains your current subscription.</span></span>

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

### <span data-ttu-id="e5422-270">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="e5422-270">-UserPrincipalName</span></span>
<span data-ttu-id="e5422-271">指定要授予許可權之使用者的使用者主體名稱。</span><span class="sxs-lookup"><span data-stu-id="e5422-271">Specifies the user principal name of the user to whom to grant permissions.</span></span>
<span data-ttu-id="e5422-272">此使用者主體名稱必須存在於與目前訂閱相關聯的目錄中。</span><span class="sxs-lookup"><span data-stu-id="e5422-272">This user principal name must exist in the directory associated with the current subscription.</span></span>

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

### <span data-ttu-id="e5422-273">-VaultName</span><span class="sxs-lookup"><span data-stu-id="e5422-273">-VaultName</span></span>
<span data-ttu-id="e5422-274">指定金鑰庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="e5422-274">Specifies the name of a key vault.</span></span>
<span data-ttu-id="e5422-275">此 Cmdlet 會修改此參數指定之金鑰庫的存取策略。</span><span class="sxs-lookup"><span data-stu-id="e5422-275">This cmdlet modifies the access policy for the key vault that this parameter specifies.</span></span>

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

### <span data-ttu-id="e5422-276">-確認</span><span class="sxs-lookup"><span data-stu-id="e5422-276">-Confirm</span></span>
<span data-ttu-id="e5422-277">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="e5422-277">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5422-278">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5422-278">-WhatIf</span></span>
<span data-ttu-id="e5422-279">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e5422-279">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e5422-280">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e5422-280">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5422-281">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5422-281">CommonParameters</span></span>
<span data-ttu-id="e5422-282">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e5422-282">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5422-283">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e5422-283">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5422-284">輸入</span><span class="sxs-lookup"><span data-stu-id="e5422-284">INPUTS</span></span>

### <span data-ttu-id="e5422-285">Microsoft.Azure.Commands.KeyVault.models.PSKeyVaultIdentityItem</span><span class="sxs-lookup"><span data-stu-id="e5422-285">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

### <span data-ttu-id="e5422-286">System.String</span><span class="sxs-lookup"><span data-stu-id="e5422-286">System.String</span></span>

## <span data-ttu-id="e5422-287">輸出</span><span class="sxs-lookup"><span data-stu-id="e5422-287">OUTPUTS</span></span>

### <span data-ttu-id="e5422-288">Microsoft.Azure.Commands.KeyVault.models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="e5422-288">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="e5422-289">筆記</span><span class="sxs-lookup"><span data-stu-id="e5422-289">NOTES</span></span>

## <span data-ttu-id="e5422-290">相關連結</span><span class="sxs-lookup"><span data-stu-id="e5422-290">RELATED LINKS</span></span>

[<span data-ttu-id="e5422-291">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="e5422-291">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)

[<span data-ttu-id="e5422-292">Remove-AzKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e5422-292">Remove-AzKeyVaultAccessPolicy</span></span>](./Remove-AzKeyVaultAccessPolicy.md)

