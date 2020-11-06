---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: AE7B103B-23ED-4A66-A0DC-14FB0DF38FA8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurermkeyvaultaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVaultAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVaultAccessPolicy.md
ms.openlocfilehash: ca175d0873b74d8b13d1755f3d0986580c5853ea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450591"
---
# <span data-ttu-id="bf24c-101">Remove-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="bf24c-101">Remove-AzureRmKeyVaultAccessPolicy</span></span>

## <span data-ttu-id="bf24c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bf24c-102">SYNOPSIS</span></span>
<span data-ttu-id="bf24c-103">從金鑰保存庫移除使用者或應用程式的擁有權限。</span><span class="sxs-lookup"><span data-stu-id="bf24c-103">Removes all permissions for a user or application from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bf24c-104">句法</span><span class="sxs-lookup"><span data-stu-id="bf24c-104">SYNTAX</span></span>

### <span data-ttu-id="bf24c-105">ByUserPrincipalName (預設) </span><span class="sxs-lookup"><span data-stu-id="bf24c-105">ByUserPrincipalName (Default)</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -UserPrincipalName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bf24c-106">ByObjectId</span><span class="sxs-lookup"><span data-stu-id="bf24c-106">ByObjectId</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ObjectId <String>
 [-ApplicationId <Guid>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bf24c-107">ByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="bf24c-107">ByServicePrincipalName</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -ServicePrincipalName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bf24c-108">ByEmail</span><span class="sxs-lookup"><span data-stu-id="bf24c-108">ByEmail</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -EmailAddress <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf24c-109">ForVault</span><span class="sxs-lookup"><span data-stu-id="bf24c-109">ForVault</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 [-EnabledForDeployment] [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf24c-110">InputObjectByObjectId</span><span class="sxs-lookup"><span data-stu-id="bf24c-110">InputObjectByObjectId</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -ObjectId <String> [-ApplicationId <Guid>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf24c-111">InputObjectByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="bf24c-111">InputObjectByServicePrincipalName</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -ServicePrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf24c-112">InputObjectByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="bf24c-112">InputObjectByUserPrincipalName</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -UserPrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf24c-113">InputObjectByEmail</span><span class="sxs-lookup"><span data-stu-id="bf24c-113">InputObjectByEmail</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -EmailAddress <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf24c-114">InputObjectForVault</span><span class="sxs-lookup"><span data-stu-id="bf24c-114">InputObjectForVault</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf24c-115">說明</span><span class="sxs-lookup"><span data-stu-id="bf24c-115">DESCRIPTION</span></span>
<span data-ttu-id="bf24c-116">**AzureRmKeyVaultAccessPolicy** Cmdlet 會移除使用者或應用程式的擁有權限，或從金鑰保存庫中的所有使用者和應用程式。</span><span class="sxs-lookup"><span data-stu-id="bf24c-116">The **Remove-AzureRmKeyVaultAccessPolicy** cmdlet removes all permissions for a user or application or for all users and applications from a key vault.</span></span>
<span data-ttu-id="bf24c-117">即使您移除擁有權限，包含金鑰保存庫的 Azure 訂閱擁有者也可以新增許可權給金鑰保存庫。</span><span class="sxs-lookup"><span data-stu-id="bf24c-117">Even if you remove all permissions, the owner of the Azure subscription that contains the key vault can add permissions to the key vault.</span></span>

<span data-ttu-id="bf24c-118">請注意，雖然為這個 Cmdlet 指定 [資源群組] 是選擇性的，但您應該這麼做，以取得較佳的效能。</span><span class="sxs-lookup"><span data-stu-id="bf24c-118">Note that although specifying the resource group is optional for this cmdlet, you should do so for better performance.</span></span>

## <span data-ttu-id="bf24c-119">示例</span><span class="sxs-lookup"><span data-stu-id="bf24c-119">EXAMPLES</span></span>

### <span data-ttu-id="bf24c-120">範例1：移除使用者的許可權</span><span class="sxs-lookup"><span data-stu-id="bf24c-120">Example 1: Remove permissions for a user</span></span>
```
PS C:\>Remove-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com'
```

<span data-ttu-id="bf24c-121">這個命令會移除使用者 PattiFuller@contoso.com 在名為 Contoso03Vault 的金鑰保存庫上擁有的擁有權限。</span><span class="sxs-lookup"><span data-stu-id="bf24c-121">This command removes all the permissions that a user PattiFuller@contoso.com has on the key vault named Contoso03Vault.</span></span>

### <span data-ttu-id="bf24c-122">範例2：移除應用程式的許可權</span><span class="sxs-lookup"><span data-stu-id="bf24c-122">Example 2: Remove permissions for an application</span></span>
```
PS C:\>Remove-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ServicePrincipalName 'http://payroll.contoso.com'
```

<span data-ttu-id="bf24c-123">這個命令會移除應用程式在名為 Contoso03Vault 的金鑰保存庫上擁有的擁有權限。</span><span class="sxs-lookup"><span data-stu-id="bf24c-123">This command removes all the permissions that an application has on the key vault named Contoso03Vault.</span></span>
<span data-ttu-id="bf24c-124">這個範例會使用在 Azure Active Directory 中註冊的服務主體名稱來識別應用程式 http://payroll.contoso.com 。</span><span class="sxs-lookup"><span data-stu-id="bf24c-124">This example identifies the application by using the service principal name registered in Azure Active Directory, http://payroll.contoso.com.</span></span>

### <span data-ttu-id="bf24c-125">範例3：使用物件識別碼移除應用程式的許可權</span><span class="sxs-lookup"><span data-stu-id="bf24c-125">Example 3: Remove permissions for an application by using its object ID</span></span>
```
PS C:\>Remove-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ObjectID 34595082-9346-41b6-8d6b-295a2808b8db
```

<span data-ttu-id="bf24c-126">這個命令會移除應用程式在名為 Contoso03Vault 的金鑰保存庫上擁有的擁有權限。</span><span class="sxs-lookup"><span data-stu-id="bf24c-126">This command removes all the permissions that an application has on the key vault named Contoso03Vault.</span></span>
<span data-ttu-id="bf24c-127">這個範例會依據服務主體的物件識別碼來識別應用程式。</span><span class="sxs-lookup"><span data-stu-id="bf24c-127">This example identifies the application by the object ID of the service principal.</span></span>

### <span data-ttu-id="bf24c-128">範例4：移除 Microsoft. 計算資源提供者的許可權</span><span class="sxs-lookup"><span data-stu-id="bf24c-128">Example 4: Remove permissions for the Microsoft.Compute resource provider</span></span>
```
PS C:\>Remove-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnabledForDeployment
```

<span data-ttu-id="bf24c-129">這個命令會移除 Microsoft. 計算資源提供者的許可權，以便從 Contoso03Vault 取得機密。</span><span class="sxs-lookup"><span data-stu-id="bf24c-129">This command removes permission for the Microsoft.Compute resource provider to get secrets from the Contoso03Vault.</span></span>

## <span data-ttu-id="bf24c-130">參數</span><span class="sxs-lookup"><span data-stu-id="bf24c-130">PARAMETERS</span></span>

### <span data-ttu-id="bf24c-131">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="bf24c-131">-ApplicationId</span></span>
<span data-ttu-id="bf24c-132">指定應該移除其許可權的應用程式識別碼</span><span class="sxs-lookup"><span data-stu-id="bf24c-132">Specifies the ID of application whose permissions should be removed</span></span>

```yaml
Type: Guid
Parameter Sets: ByObjectId, InputObjectByObjectId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf24c-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf24c-133">-DefaultProfile</span></span>
<span data-ttu-id="bf24c-134">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="bf24c-134">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf24c-135">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="bf24c-135">-EmailAddress</span></span>
<span data-ttu-id="bf24c-136">指定您想要移除其存取權的使用者的使用者電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="bf24c-136">Specifies the user email address of the user whose access you want to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByEmail, InputObjectByEmail
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf24c-137">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="bf24c-137">-EnabledForDeployment</span></span>
<span data-ttu-id="bf24c-138">如果已指定，則會停用 Microsoft 的此金鑰保存庫的密碼檢索。當在資源建立中參照時，計算資源提供者。</span><span class="sxs-lookup"><span data-stu-id="bf24c-138">If specified, disables the retrieval of secrets from this key vault by the Microsoft.Compute resource provider when referenced in resource creation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ForVault, InputObjectForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf24c-139">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="bf24c-139">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="bf24c-140">如果已指定，則會停用 Azure 磁片加密的來自此金鑰保存庫的密碼檢索。</span><span class="sxs-lookup"><span data-stu-id="bf24c-140">If specified, disables the retrieval of secrets from this key vault by Azure Disk Encryption.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ForVault, InputObjectForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf24c-141">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="bf24c-141">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="bf24c-142">如果已指定，則會在範本中參照 Azure 資源管理員時，停用此金鑰保存庫的密碼檢索。</span><span class="sxs-lookup"><span data-stu-id="bf24c-142">If specified, disables the retrieval of secrets from this key vault by Azure Resource Manager when referenced in templates.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ForVault, InputObjectForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf24c-143">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bf24c-143">-InputObject</span></span>
<span data-ttu-id="bf24c-144">金鑰保存庫物件。</span><span class="sxs-lookup"><span data-stu-id="bf24c-144">Key Vault object.</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmail, InputObjectForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bf24c-145">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="bf24c-145">-ObjectId</span></span>
<span data-ttu-id="bf24c-146">指定 Azure Active Directory 中要移除許可權的使用者或服務主體物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="bf24c-146">Specifies the object ID of the user or service principal in Azure Active Directory for which to remove permissions.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectId, InputObjectByObjectId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf24c-147">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bf24c-147">-PassThru</span></span>
<span data-ttu-id="bf24c-148">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="bf24c-148">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="bf24c-149">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="bf24c-149">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf24c-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf24c-150">-ResourceGroupName</span></span>
<span data-ttu-id="bf24c-151">指定與要修改其存取原則之金鑰保存庫相關聯的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="bf24c-151">Specifies the name of the resource group associated with the key vault whose access policy is being modified.</span></span>
<span data-ttu-id="bf24c-152">如果未指定，此 Cmdlet 會在目前的訂閱中搜尋主要電子倉庫。</span><span class="sxs-lookup"><span data-stu-id="bf24c-152">If not specified, this cmdlet searches for the key vault in the current subscription.</span></span>

```yaml
Type: String
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmail, ForVault
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf24c-153">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="bf24c-153">-ServicePrincipalName</span></span>
<span data-ttu-id="bf24c-154">指定您要移除其許可權之應用程式的服務主體名稱。</span><span class="sxs-lookup"><span data-stu-id="bf24c-154">Specifies the service principal name of the application whose permissions you want to remove.</span></span>
<span data-ttu-id="bf24c-155">指定在 Azure Active Directory 中為應用程式註冊的應用程式識別碼（也稱為「用戶端識別碼」）。</span><span class="sxs-lookup"><span data-stu-id="bf24c-155">Specify the application ID, also known as client ID, registered for the application in Azure Active Directory.</span></span>

```yaml
Type: String
Parameter Sets: ByServicePrincipalName, InputObjectByServicePrincipalName
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf24c-156">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="bf24c-156">-UserPrincipalName</span></span>
<span data-ttu-id="bf24c-157">指定您想要移除其存取權的使用者的使用者主要名稱。</span><span class="sxs-lookup"><span data-stu-id="bf24c-157">Specifies the user principal name of the user whose access you want to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByUserPrincipalName, InputObjectByUserPrincipalName
Aliases: UPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf24c-158">-VaultName</span><span class="sxs-lookup"><span data-stu-id="bf24c-158">-VaultName</span></span>
<span data-ttu-id="bf24c-159">指定主要電子倉庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="bf24c-159">Specifies the name of the key vault.</span></span>
<span data-ttu-id="bf24c-160">這個 Cmdlet 會移除此參數指定之金鑰保存庫的許可權。</span><span class="sxs-lookup"><span data-stu-id="bf24c-160">This cmdlet removes permissions for the key vault that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmail, ForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf24c-161">-確認</span><span class="sxs-lookup"><span data-stu-id="bf24c-161">-Confirm</span></span>
<span data-ttu-id="bf24c-162">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="bf24c-162">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf24c-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf24c-163">-WhatIf</span></span>
<span data-ttu-id="bf24c-164">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="bf24c-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf24c-165">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bf24c-165">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf24c-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf24c-166">CommonParameters</span></span>
<span data-ttu-id="bf24c-167">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bf24c-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf24c-168">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bf24c-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf24c-169">輸入</span><span class="sxs-lookup"><span data-stu-id="bf24c-169">INPUTS</span></span>

### <span data-ttu-id="bf24c-170">所有</span><span class="sxs-lookup"><span data-stu-id="bf24c-170">None</span></span>
<span data-ttu-id="bf24c-171">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="bf24c-171">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bf24c-172">輸出</span><span class="sxs-lookup"><span data-stu-id="bf24c-172">OUTPUTS</span></span>

### <span data-ttu-id="bf24c-173">PSKeyVault 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="bf24c-173">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="bf24c-174">筆記</span><span class="sxs-lookup"><span data-stu-id="bf24c-174">NOTES</span></span>

## <span data-ttu-id="bf24c-175">相關連結</span><span class="sxs-lookup"><span data-stu-id="bf24c-175">RELATED LINKS</span></span>

[<span data-ttu-id="bf24c-176">Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="bf24c-176">Set-AzureRmKeyVaultAccessPolicy</span></span>](./Set-AzureRmKeyVaultAccessPolicy.md)

