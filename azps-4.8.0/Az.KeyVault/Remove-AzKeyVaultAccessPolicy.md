---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: AE7B103B-23ED-4A66-A0DC-14FB0DF38FA8
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultAccessPolicy.md
ms.openlocfilehash: e19565aa8ae249acf61fce67f0a2b54e20143758
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100410152"
---
# <span data-ttu-id="48109-101">Remove-AzKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="48109-101">Remove-AzKeyVaultAccessPolicy</span></span>

## <span data-ttu-id="48109-102">簡介</span><span class="sxs-lookup"><span data-stu-id="48109-102">SYNOPSIS</span></span>
<span data-ttu-id="48109-103">從金鑰庫移除使用者或應用程式的擁有權限。</span><span class="sxs-lookup"><span data-stu-id="48109-103">Removes all permissions for a user or application from a key vault.</span></span>

## <span data-ttu-id="48109-104">語法</span><span class="sxs-lookup"><span data-stu-id="48109-104">SYNTAX</span></span>

### <span data-ttu-id="48109-105">ByUserPrincipalName (預設) </span><span class="sxs-lookup"><span data-stu-id="48109-105">ByUserPrincipalName (Default)</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -UserPrincipalName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48109-106">ByObjectId</span><span class="sxs-lookup"><span data-stu-id="48109-106">ByObjectId</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ObjectId <String>
 [-ApplicationId <Guid>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="48109-107">ByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="48109-107">ByServicePrincipalName</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -ServicePrincipalName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="48109-108">ByEmail</span><span class="sxs-lookup"><span data-stu-id="48109-108">ByEmail</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -EmailAddress <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48109-109">ForVault</span><span class="sxs-lookup"><span data-stu-id="48109-109">ForVault</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48109-110">InputObjectByObjectId</span><span class="sxs-lookup"><span data-stu-id="48109-110">InputObjectByObjectId</span></span>
```
Remove-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -ObjectId <String> [-ApplicationId <Guid>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48109-111">InputObjectByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="48109-111">InputObjectByServicePrincipalName</span></span>
```
Remove-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -ServicePrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48109-112">InputObjectByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="48109-112">InputObjectByUserPrincipalName</span></span>
```
Remove-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -UserPrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48109-113">InputObjectByEmail</span><span class="sxs-lookup"><span data-stu-id="48109-113">InputObjectByEmail</span></span>
```
Remove-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -EmailAddress <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48109-114">InputObjectForVault</span><span class="sxs-lookup"><span data-stu-id="48109-114">InputObjectForVault</span></span>
```
Remove-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVault> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48109-115">ResourceIdByObjectId</span><span class="sxs-lookup"><span data-stu-id="48109-115">ResourceIdByObjectId</span></span>
```
Remove-AzKeyVaultAccessPolicy [-ResourceId] <String> -ObjectId <String> [-ApplicationId <Guid>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48109-116">ResourceIdByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="48109-116">ResourceIdByServicePrincipalName</span></span>
```
Remove-AzKeyVaultAccessPolicy [-ResourceId] <String> -ServicePrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48109-117">ResourceIdByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="48109-117">ResourceIdByUserPrincipalName</span></span>
```
Remove-AzKeyVaultAccessPolicy [-ResourceId] <String> -UserPrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48109-118">ResourceIdByEmail</span><span class="sxs-lookup"><span data-stu-id="48109-118">ResourceIdByEmail</span></span>
```
Remove-AzKeyVaultAccessPolicy [-ResourceId] <String> -EmailAddress <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48109-119">ResourceIdForVault</span><span class="sxs-lookup"><span data-stu-id="48109-119">ResourceIdForVault</span></span>
```
Remove-AzKeyVaultAccessPolicy [-ResourceId] <String> [-EnabledForDeployment] [-EnabledForTemplateDeployment]
 [-EnabledForDiskEncryption] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="48109-120">描述</span><span class="sxs-lookup"><span data-stu-id="48109-120">DESCRIPTION</span></span>
<span data-ttu-id="48109-121">**Remove-AzKeyVaultAccessPolicy** Cmdlet 會從金鑰庫移除使用者或應用程式或所有使用者和應用程式的擁有權限。</span><span class="sxs-lookup"><span data-stu-id="48109-121">The **Remove-AzKeyVaultAccessPolicy** cmdlet removes all permissions for a user or application or for all users and applications from a key vault.</span></span>
<span data-ttu-id="48109-122">即使您移除擁有權限，包含金鑰庫的 Azure 訂閱擁有者也可以新增金鑰庫的許可權。</span><span class="sxs-lookup"><span data-stu-id="48109-122">Even if you remove all permissions, the owner of the Azure subscription that contains the key vault can add permissions to the key vault.</span></span>
<span data-ttu-id="48109-123">請注意，雖然指定資源群組是這個 Cmdlet 的選擇性專案，但您應這麼做以提升績效。</span><span class="sxs-lookup"><span data-stu-id="48109-123">Note that although specifying the resource group is optional for this cmdlet, you should do so for better performance.</span></span>

## <span data-ttu-id="48109-124">例子</span><span class="sxs-lookup"><span data-stu-id="48109-124">EXAMPLES</span></span>

### <span data-ttu-id="48109-125">範例 1：移除使用者的許可權</span><span class="sxs-lookup"><span data-stu-id="48109-125">Example 1: Remove permissions for a user</span></span>
```powershell
PS C:\> Remove-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PassThru

Vault Name                       : Contoso03Vault
Resource Group Name              : myrg
Location                         : westus
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers
                                   /Microsoft.KeyVault/vaults/contoso03vault
Vault URI                        : https://contoso03vault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Standard
Enabled For Deployment?          : False
Enabled For Template Deployment? : False
Enabled For Disk Encryption?     : False
Soft Delete Enabled?             :
Access Policies                  :
                                   Tenant ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Object ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Application ID                             :
                                   Display Name                               : User Name (username@microsoft.com)
                                   Permissions to Keys                        :
                                   Permissions to Secrets                     :
                                   Permissions to Certificates                : get, create
                                   Permissions to (Key Vault Managed) Storage :


Network Rule Set                 :
                                   Default Action                             : Allow
                                   Bypass                                     : AzureServices
                                   IP Rules                                   :
                                   Virtual Network Rules                      :

Tags                             :
```

<span data-ttu-id="48109-126">此命令會移除使用者在名為 PattiFuller@contoso.com Contoso03Vault 之金鑰庫上擁有的擁有權限。</span><span class="sxs-lookup"><span data-stu-id="48109-126">This command removes all the permissions that a user PattiFuller@contoso.com has on the key vault named Contoso03Vault.</span></span>  <span data-ttu-id="48109-127">如果指定 -PassThru，會傳回 KeyVault 物件。</span><span class="sxs-lookup"><span data-stu-id="48109-127">If -PassThru is specified, the KeyVault object is returned.</span></span>

### <span data-ttu-id="48109-128">範例 2：移除應用程式的許可權</span><span class="sxs-lookup"><span data-stu-id="48109-128">Example 2: Remove permissions for an application</span></span>
```powershell
PS C:\> Remove-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ServicePrincipalName 'http://payroll.contoso.com'
```

<span data-ttu-id="48109-129">此命令會移除應用程式在名為 Contoso03Vault 的金鑰庫上擁有的擁有權限。</span><span class="sxs-lookup"><span data-stu-id="48109-129">This command removes all the permissions that an application has on the key vault named Contoso03Vault.</span></span>
<span data-ttu-id="48109-130">此範例使用在 Azure Active Directory 中註冊的服務主體名稱來識別應用程式 `http://payroll.contoso.com` 。</span><span class="sxs-lookup"><span data-stu-id="48109-130">This example identifies the application by using the service principal name registered in Azure Active Directory, `http://payroll.contoso.com`.</span></span>

### <span data-ttu-id="48109-131">範例 3：使用應用程式的物件識別碼移除其許可權</span><span class="sxs-lookup"><span data-stu-id="48109-131">Example 3: Remove permissions for an application by using its object ID</span></span>
```powershell
PS C:\> Remove-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ObjectID 34595082-9346-41b6-8d6b-295a2808b8db
```

<span data-ttu-id="48109-132">此命令會移除應用程式在名為 Contoso03Vault 的金鑰庫上擁有的擁有權限。</span><span class="sxs-lookup"><span data-stu-id="48109-132">This command removes all the permissions that an application has on the key vault named Contoso03Vault.</span></span>
<span data-ttu-id="48109-133">此範例會以服務主體的物件識別碼識別應用程式。</span><span class="sxs-lookup"><span data-stu-id="48109-133">This example identifies the application by the object ID of the service principal.</span></span>

### <span data-ttu-id="48109-134">範例 4：移除 Microsoft.Compute 資源提供者的許可權</span><span class="sxs-lookup"><span data-stu-id="48109-134">Example 4: Remove permissions for the Microsoft.Compute resource provider</span></span>
```powershell
PS C:\> Remove-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnabledForDeployment
```

<span data-ttu-id="48109-135">此命令會移除 Microsoft.Compute 資源提供者從 Contoso03Vault 取得秘訣的許可權。</span><span class="sxs-lookup"><span data-stu-id="48109-135">This command removes permission for the Microsoft.Compute resource provider to get secrets from the Contoso03Vault.</span></span>

## <span data-ttu-id="48109-136">參數</span><span class="sxs-lookup"><span data-stu-id="48109-136">PARAMETERS</span></span>

### <span data-ttu-id="48109-137">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="48109-137">-ApplicationId</span></span>
<span data-ttu-id="48109-138">指定應移除其許可權的應用程式識別碼</span><span class="sxs-lookup"><span data-stu-id="48109-138">Specifies the ID of application whose permissions should be removed</span></span>

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

### <span data-ttu-id="48109-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48109-139">-DefaultProfile</span></span>
<span data-ttu-id="48109-140">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="48109-140">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="48109-141">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="48109-141">-EmailAddress</span></span>
<span data-ttu-id="48109-142">指定您想要移除其存取權之使用者的使用者電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="48109-142">Specifies the user email address of the user whose access you want to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByEmail, InputObjectByEmail, ResourceIdByEmail
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48109-143">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="48109-143">-EnabledForDeployment</span></span>
<span data-ttu-id="48109-144">如果指定，Microsoft.Compute 資源提供者在建立資源時參照時，會停用從這個金鑰庫中的機密內容。</span><span class="sxs-lookup"><span data-stu-id="48109-144">If specified, disables the retrieval of secrets from this key vault by the Microsoft.Compute resource provider when referenced in resource creation.</span></span>

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

### <span data-ttu-id="48109-145">-EnabledForCryptEncryption</span><span class="sxs-lookup"><span data-stu-id="48109-145">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="48109-146">如果指定，Azure 磁片加密會停用此金鑰庫中的機密內容。</span><span class="sxs-lookup"><span data-stu-id="48109-146">If specified, disables the retrieval of secrets from this key vault by Azure Disk Encryption.</span></span>

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

### <span data-ttu-id="48109-147">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="48109-147">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="48109-148">如果指定，當在範本中參照時，Azure Resource Manager 會停用從此索引鍵庫中的機密內容。</span><span class="sxs-lookup"><span data-stu-id="48109-148">If specified, disables the retrieval of secrets from this key vault by Azure Resource Manager when referenced in templates.</span></span>

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

### <span data-ttu-id="48109-149">-InputObject</span><span class="sxs-lookup"><span data-stu-id="48109-149">-InputObject</span></span>
<span data-ttu-id="48109-150">Key Vault 物件。</span><span class="sxs-lookup"><span data-stu-id="48109-150">Key Vault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmail, InputObjectForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="48109-151">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="48109-151">-ObjectId</span></span>
<span data-ttu-id="48109-152">指定 Azure Active Directory 中使用者或服務主體的物件識別碼，以移除其許可權。</span><span class="sxs-lookup"><span data-stu-id="48109-152">Specifies the object ID of the user or service principal in Azure Active Directory for which to remove permissions.</span></span>

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

### <span data-ttu-id="48109-153">-PassThru</span><span class="sxs-lookup"><span data-stu-id="48109-153">-PassThru</span></span>
<span data-ttu-id="48109-154">會返回代表您處理之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="48109-154">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="48109-155">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="48109-155">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="48109-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48109-156">-ResourceGroupName</span></span>
<span data-ttu-id="48109-157">指定與正在修改其存取策略之金鑰庫相關聯的資源組名。</span><span class="sxs-lookup"><span data-stu-id="48109-157">Specifies the name of the resource group associated with the key vault whose access policy is being modified.</span></span>
<span data-ttu-id="48109-158">如果未指定，此 Cmdlet 會搜尋目前訂閱中的金鑰保存庫。</span><span class="sxs-lookup"><span data-stu-id="48109-158">If not specified, this cmdlet searches for the key vault in the current subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmail, ForVault
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48109-159">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="48109-159">-ResourceId</span></span>
<span data-ttu-id="48109-160">KeyVault 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="48109-160">KeyVault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmail, ResourceIdForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48109-161">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="48109-161">-ServicePrincipalName</span></span>
<span data-ttu-id="48109-162">指定您想要移除其許可權之應用程式的服務主體名稱。</span><span class="sxs-lookup"><span data-stu-id="48109-162">Specifies the service principal name of the application whose permissions you want to remove.</span></span>
<span data-ttu-id="48109-163">指定在 Azure Active Directory 中為應用程式註冊的應用程式識別碼 ，也稱為用戶端識別碼。</span><span class="sxs-lookup"><span data-stu-id="48109-163">Specify the application ID, also known as client ID, registered for the application in Azure Active Directory.</span></span>

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

### <span data-ttu-id="48109-164">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="48109-164">-UserPrincipalName</span></span>
<span data-ttu-id="48109-165">指定您想要移除其存取權之使用者的使用者主體名稱。</span><span class="sxs-lookup"><span data-stu-id="48109-165">Specifies the user principal name of the user whose access you want to remove.</span></span>

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

### <span data-ttu-id="48109-166">-VaultName</span><span class="sxs-lookup"><span data-stu-id="48109-166">-VaultName</span></span>
<span data-ttu-id="48109-167">指定金鑰庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="48109-167">Specifies the name of the key vault.</span></span>
<span data-ttu-id="48109-168">此 Cmdlet 會移除此參數指定的金鑰庫許可權。</span><span class="sxs-lookup"><span data-stu-id="48109-168">This cmdlet removes permissions for the key vault that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmail, ForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48109-169">-確認</span><span class="sxs-lookup"><span data-stu-id="48109-169">-Confirm</span></span>
<span data-ttu-id="48109-170">執行 Cmdlet 之前，系統會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="48109-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48109-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48109-171">-WhatIf</span></span>
<span data-ttu-id="48109-172">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="48109-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48109-173">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="48109-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48109-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48109-174">CommonParameters</span></span>
<span data-ttu-id="48109-175">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="48109-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48109-176">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="48109-176">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48109-177">輸入</span><span class="sxs-lookup"><span data-stu-id="48109-177">INPUTS</span></span>

### <span data-ttu-id="48109-178">Microsoft.Azure.Commands.KeyVault.models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="48109-178">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="48109-179">System.String</span><span class="sxs-lookup"><span data-stu-id="48109-179">System.String</span></span>

## <span data-ttu-id="48109-180">輸出</span><span class="sxs-lookup"><span data-stu-id="48109-180">OUTPUTS</span></span>

### <span data-ttu-id="48109-181">Microsoft.Azure.Commands.KeyVault.models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="48109-181">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="48109-182">筆記</span><span class="sxs-lookup"><span data-stu-id="48109-182">NOTES</span></span>

## <span data-ttu-id="48109-183">相關連結</span><span class="sxs-lookup"><span data-stu-id="48109-183">RELATED LINKS</span></span>

[<span data-ttu-id="48109-184">Set-AzKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="48109-184">Set-AzKeyVaultAccessPolicy</span></span>](./Set-AzKeyVaultAccessPolicy.md)

