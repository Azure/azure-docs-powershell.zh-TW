---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: AE7B103B-23ED-4A66-A0DC-14FB0DF38FA8
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultAccessPolicy.md
ms.openlocfilehash: a0cf20ad9fafbae2ed6902226e396b3d732cee5c
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/08/2020
ms.locfileid: "93802685"
---
# <span data-ttu-id="50d3e-101">Remove-AzKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="50d3e-101">Remove-AzKeyVaultAccessPolicy</span></span>

## <span data-ttu-id="50d3e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="50d3e-102">SYNOPSIS</span></span>
<span data-ttu-id="50d3e-103">從金鑰保存庫移除使用者或應用程式的擁有權限。</span><span class="sxs-lookup"><span data-stu-id="50d3e-103">Removes all permissions for a user or application from a key vault.</span></span>

## <span data-ttu-id="50d3e-104">句法</span><span class="sxs-lookup"><span data-stu-id="50d3e-104">SYNTAX</span></span>

### <span data-ttu-id="50d3e-105">ByUserPrincipalName (預設) </span><span class="sxs-lookup"><span data-stu-id="50d3e-105">ByUserPrincipalName (Default)</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -UserPrincipalName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50d3e-106">ByObjectId</span><span class="sxs-lookup"><span data-stu-id="50d3e-106">ByObjectId</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ObjectId <String>
 [-ApplicationId <Guid>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="50d3e-107">ByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="50d3e-107">ByServicePrincipalName</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -ServicePrincipalName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="50d3e-108">ByEmail</span><span class="sxs-lookup"><span data-stu-id="50d3e-108">ByEmail</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -EmailAddress <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50d3e-109">ForVault</span><span class="sxs-lookup"><span data-stu-id="50d3e-109">ForVault</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50d3e-110">InputObjectByObjectId</span><span class="sxs-lookup"><span data-stu-id="50d3e-110">InputObjectByObjectId</span></span>
```
Remove-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -ObjectId <String> [-ApplicationId <Guid>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50d3e-111">InputObjectByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="50d3e-111">InputObjectByServicePrincipalName</span></span>
```
Remove-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -ServicePrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50d3e-112">InputObjectByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="50d3e-112">InputObjectByUserPrincipalName</span></span>
```
Remove-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -UserPrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50d3e-113">InputObjectByEmail</span><span class="sxs-lookup"><span data-stu-id="50d3e-113">InputObjectByEmail</span></span>
```
Remove-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -EmailAddress <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50d3e-114">InputObjectForVault</span><span class="sxs-lookup"><span data-stu-id="50d3e-114">InputObjectForVault</span></span>
```
Remove-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVault> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50d3e-115">ResourceIdByObjectId</span><span class="sxs-lookup"><span data-stu-id="50d3e-115">ResourceIdByObjectId</span></span>
```
Remove-AzKeyVaultAccessPolicy [-ResourceId] <String> -ObjectId <String> [-ApplicationId <Guid>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50d3e-116">ResourceIdByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="50d3e-116">ResourceIdByServicePrincipalName</span></span>
```
Remove-AzKeyVaultAccessPolicy [-ResourceId] <String> -ServicePrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50d3e-117">ResourceIdByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="50d3e-117">ResourceIdByUserPrincipalName</span></span>
```
Remove-AzKeyVaultAccessPolicy [-ResourceId] <String> -UserPrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50d3e-118">ResourceIdByEmail</span><span class="sxs-lookup"><span data-stu-id="50d3e-118">ResourceIdByEmail</span></span>
```
Remove-AzKeyVaultAccessPolicy [-ResourceId] <String> -EmailAddress <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50d3e-119">ResourceIdForVault</span><span class="sxs-lookup"><span data-stu-id="50d3e-119">ResourceIdForVault</span></span>
```
Remove-AzKeyVaultAccessPolicy [-ResourceId] <String> [-EnabledForDeployment] [-EnabledForTemplateDeployment]
 [-EnabledForDiskEncryption] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="50d3e-120">說明</span><span class="sxs-lookup"><span data-stu-id="50d3e-120">DESCRIPTION</span></span>
<span data-ttu-id="50d3e-121">**AzKeyVaultAccessPolicy** Cmdlet 會移除使用者或應用程式的擁有權限，或從金鑰保存庫中的所有使用者和應用程式。</span><span class="sxs-lookup"><span data-stu-id="50d3e-121">The **Remove-AzKeyVaultAccessPolicy** cmdlet removes all permissions for a user or application or for all users and applications from a key vault.</span></span>
<span data-ttu-id="50d3e-122">即使您移除擁有權限，包含金鑰保存庫的 Azure 訂閱擁有者也可以新增許可權給金鑰保存庫。</span><span class="sxs-lookup"><span data-stu-id="50d3e-122">Even if you remove all permissions, the owner of the Azure subscription that contains the key vault can add permissions to the key vault.</span></span>
<span data-ttu-id="50d3e-123">請注意，雖然為這個 Cmdlet 指定 [資源群組] 是選擇性的，但您應該這麼做，以取得較佳的效能。</span><span class="sxs-lookup"><span data-stu-id="50d3e-123">Note that although specifying the resource group is optional for this cmdlet, you should do so for better performance.</span></span>

## <span data-ttu-id="50d3e-124">示例</span><span class="sxs-lookup"><span data-stu-id="50d3e-124">EXAMPLES</span></span>

### <span data-ttu-id="50d3e-125">範例1：移除使用者的許可權</span><span class="sxs-lookup"><span data-stu-id="50d3e-125">Example 1: Remove permissions for a user</span></span>
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

<span data-ttu-id="50d3e-126">這個命令會移除使用者 PattiFuller@contoso.com 在名為 Contoso03Vault 的金鑰保存庫上擁有的擁有權限。</span><span class="sxs-lookup"><span data-stu-id="50d3e-126">This command removes all the permissions that a user PattiFuller@contoso.com has on the key vault named Contoso03Vault.</span></span>  <span data-ttu-id="50d3e-127">如果指定了-PassThru，則會傳回 KeyVault 物件。</span><span class="sxs-lookup"><span data-stu-id="50d3e-127">If -PassThru is specified, the KeyVault object is returned.</span></span>

### <span data-ttu-id="50d3e-128">範例2：移除應用程式的許可權</span><span class="sxs-lookup"><span data-stu-id="50d3e-128">Example 2: Remove permissions for an application</span></span>
```powershell
PS C:\> Remove-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ServicePrincipalName 'http://payroll.contoso.com'
```

<span data-ttu-id="50d3e-129">這個命令會移除應用程式在名為 Contoso03Vault 的金鑰保存庫上擁有的擁有權限。</span><span class="sxs-lookup"><span data-stu-id="50d3e-129">This command removes all the permissions that an application has on the key vault named Contoso03Vault.</span></span>
<span data-ttu-id="50d3e-130">這個範例會使用在 Azure Active Directory 中註冊的服務主體名稱來識別應用程式 `http://payroll.contoso.com` 。</span><span class="sxs-lookup"><span data-stu-id="50d3e-130">This example identifies the application by using the service principal name registered in Azure Active Directory, `http://payroll.contoso.com`.</span></span>

### <span data-ttu-id="50d3e-131">範例3：使用物件識別碼移除應用程式的許可權</span><span class="sxs-lookup"><span data-stu-id="50d3e-131">Example 3: Remove permissions for an application by using its object ID</span></span>
```powershell
PS C:\> Remove-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ObjectID 34595082-9346-41b6-8d6b-295a2808b8db
```

<span data-ttu-id="50d3e-132">這個命令會移除應用程式在名為 Contoso03Vault 的金鑰保存庫上擁有的擁有權限。</span><span class="sxs-lookup"><span data-stu-id="50d3e-132">This command removes all the permissions that an application has on the key vault named Contoso03Vault.</span></span>
<span data-ttu-id="50d3e-133">這個範例會依據服務主體的物件識別碼來識別應用程式。</span><span class="sxs-lookup"><span data-stu-id="50d3e-133">This example identifies the application by the object ID of the service principal.</span></span>

### <span data-ttu-id="50d3e-134">範例4：移除 Microsoft. 計算資源提供者的許可權</span><span class="sxs-lookup"><span data-stu-id="50d3e-134">Example 4: Remove permissions for the Microsoft.Compute resource provider</span></span>
```powershell
PS C:\> Remove-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnabledForDeployment
```

<span data-ttu-id="50d3e-135">這個命令會移除 Microsoft. 計算資源提供者的許可權，以便從 Contoso03Vault 取得機密。</span><span class="sxs-lookup"><span data-stu-id="50d3e-135">This command removes permission for the Microsoft.Compute resource provider to get secrets from the Contoso03Vault.</span></span>

## <span data-ttu-id="50d3e-136">參數</span><span class="sxs-lookup"><span data-stu-id="50d3e-136">PARAMETERS</span></span>

### <span data-ttu-id="50d3e-137">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="50d3e-137">-ApplicationId</span></span>
<span data-ttu-id="50d3e-138">指定應該移除其許可權的應用程式識別碼</span><span class="sxs-lookup"><span data-stu-id="50d3e-138">Specifies the ID of application whose permissions should be removed</span></span>

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

### <span data-ttu-id="50d3e-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50d3e-139">-DefaultProfile</span></span>
<span data-ttu-id="50d3e-140">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="50d3e-140">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="50d3e-141">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="50d3e-141">-EmailAddress</span></span>
<span data-ttu-id="50d3e-142">指定您想要移除其存取權的使用者的使用者電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="50d3e-142">Specifies the user email address of the user whose access you want to remove.</span></span>

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

### <span data-ttu-id="50d3e-143">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="50d3e-143">-EnabledForDeployment</span></span>
<span data-ttu-id="50d3e-144">如果已指定，則會停用 Microsoft 的此金鑰保存庫的密碼檢索。當在資源建立中參照時，計算資源提供者。</span><span class="sxs-lookup"><span data-stu-id="50d3e-144">If specified, disables the retrieval of secrets from this key vault by the Microsoft.Compute resource provider when referenced in resource creation.</span></span>

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

### <span data-ttu-id="50d3e-145">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="50d3e-145">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="50d3e-146">如果已指定，則會停用 Azure 磁片加密的來自此金鑰保存庫的密碼檢索。</span><span class="sxs-lookup"><span data-stu-id="50d3e-146">If specified, disables the retrieval of secrets from this key vault by Azure Disk Encryption.</span></span>

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

### <span data-ttu-id="50d3e-147">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="50d3e-147">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="50d3e-148">如果已指定，則會在範本中參照 Azure 資源管理員時，停用此金鑰保存庫的密碼檢索。</span><span class="sxs-lookup"><span data-stu-id="50d3e-148">If specified, disables the retrieval of secrets from this key vault by Azure Resource Manager when referenced in templates.</span></span>

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

### <span data-ttu-id="50d3e-149">-InputObject</span><span class="sxs-lookup"><span data-stu-id="50d3e-149">-InputObject</span></span>
<span data-ttu-id="50d3e-150">金鑰保存庫物件。</span><span class="sxs-lookup"><span data-stu-id="50d3e-150">Key Vault object.</span></span>

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

### <span data-ttu-id="50d3e-151">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="50d3e-151">-ObjectId</span></span>
<span data-ttu-id="50d3e-152">指定 Azure Active Directory 中要移除許可權的使用者或服務主體物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="50d3e-152">Specifies the object ID of the user or service principal in Azure Active Directory for which to remove permissions.</span></span>

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

### <span data-ttu-id="50d3e-153">-PassThru</span><span class="sxs-lookup"><span data-stu-id="50d3e-153">-PassThru</span></span>
<span data-ttu-id="50d3e-154">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="50d3e-154">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="50d3e-155">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="50d3e-155">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="50d3e-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50d3e-156">-ResourceGroupName</span></span>
<span data-ttu-id="50d3e-157">指定與要修改其存取原則之金鑰保存庫相關聯的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="50d3e-157">Specifies the name of the resource group associated with the key vault whose access policy is being modified.</span></span>
<span data-ttu-id="50d3e-158">如果未指定，此 Cmdlet 會在目前的訂閱中搜尋主要電子倉庫。</span><span class="sxs-lookup"><span data-stu-id="50d3e-158">If not specified, this cmdlet searches for the key vault in the current subscription.</span></span>

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

### <span data-ttu-id="50d3e-159">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="50d3e-159">-ResourceId</span></span>
<span data-ttu-id="50d3e-160">KeyVault 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="50d3e-160">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="50d3e-161">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="50d3e-161">-ServicePrincipalName</span></span>
<span data-ttu-id="50d3e-162">指定您要移除其許可權之應用程式的服務主體名稱。</span><span class="sxs-lookup"><span data-stu-id="50d3e-162">Specifies the service principal name of the application whose permissions you want to remove.</span></span>
<span data-ttu-id="50d3e-163">指定在 Azure Active Directory 中為應用程式註冊的應用程式識別碼（也稱為「用戶端識別碼」）。</span><span class="sxs-lookup"><span data-stu-id="50d3e-163">Specify the application ID, also known as client ID, registered for the application in Azure Active Directory.</span></span>

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

### <span data-ttu-id="50d3e-164">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="50d3e-164">-UserPrincipalName</span></span>
<span data-ttu-id="50d3e-165">指定您想要移除其存取權的使用者的使用者主要名稱。</span><span class="sxs-lookup"><span data-stu-id="50d3e-165">Specifies the user principal name of the user whose access you want to remove.</span></span>

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

### <span data-ttu-id="50d3e-166">-VaultName</span><span class="sxs-lookup"><span data-stu-id="50d3e-166">-VaultName</span></span>
<span data-ttu-id="50d3e-167">指定主要電子倉庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="50d3e-167">Specifies the name of the key vault.</span></span>
<span data-ttu-id="50d3e-168">這個 Cmdlet 會移除此參數指定之金鑰保存庫的許可權。</span><span class="sxs-lookup"><span data-stu-id="50d3e-168">This cmdlet removes permissions for the key vault that this parameter specifies.</span></span>

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

### <span data-ttu-id="50d3e-169">-確認</span><span class="sxs-lookup"><span data-stu-id="50d3e-169">-Confirm</span></span>
<span data-ttu-id="50d3e-170">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="50d3e-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50d3e-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50d3e-171">-WhatIf</span></span>
<span data-ttu-id="50d3e-172">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="50d3e-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50d3e-173">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="50d3e-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50d3e-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50d3e-174">CommonParameters</span></span>
<span data-ttu-id="50d3e-175">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="50d3e-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50d3e-176">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="50d3e-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50d3e-177">輸入</span><span class="sxs-lookup"><span data-stu-id="50d3e-177">INPUTS</span></span>

### <span data-ttu-id="50d3e-178">PSKeyVault 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="50d3e-178">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="50d3e-179">System.object</span><span class="sxs-lookup"><span data-stu-id="50d3e-179">System.String</span></span>

## <span data-ttu-id="50d3e-180">輸出</span><span class="sxs-lookup"><span data-stu-id="50d3e-180">OUTPUTS</span></span>

### <span data-ttu-id="50d3e-181">PSKeyVault 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="50d3e-181">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="50d3e-182">筆記</span><span class="sxs-lookup"><span data-stu-id="50d3e-182">NOTES</span></span>

## <span data-ttu-id="50d3e-183">相關連結</span><span class="sxs-lookup"><span data-stu-id="50d3e-183">RELATED LINKS</span></span>

[<span data-ttu-id="50d3e-184">Set-AzKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="50d3e-184">Set-AzKeyVaultAccessPolicy</span></span>](./Set-AzKeyVaultAccessPolicy.md)
