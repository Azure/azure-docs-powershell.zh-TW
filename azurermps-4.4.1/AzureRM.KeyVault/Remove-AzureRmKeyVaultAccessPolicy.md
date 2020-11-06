---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: AE7B103B-23ED-4A66-A0DC-14FB0DF38FA8
online version: https://go.microsoft.com/fwlink/?LinkId=690164
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVaultAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVaultAccessPolicy.md
ms.openlocfilehash: 4e46c100984a9e50794130b3de6e30ce5f664ea4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454351"
---
# <span data-ttu-id="3e838-101">Remove-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3e838-101">Remove-AzureRmKeyVaultAccessPolicy</span></span>

## <span data-ttu-id="3e838-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3e838-102">SYNOPSIS</span></span>
<span data-ttu-id="3e838-103">從金鑰保存庫移除使用者或應用程式的擁有權限。</span><span class="sxs-lookup"><span data-stu-id="3e838-103">Removes all permissions for a user or application from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3e838-104">句法</span><span class="sxs-lookup"><span data-stu-id="3e838-104">SYNTAX</span></span>

### <span data-ttu-id="3e838-105">ByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="3e838-105">ByServicePrincipalName</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -ServicePrincipalName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3e838-106">ByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="3e838-106">ByUserPrincipalName</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -UserPrincipalName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3e838-107">ByObjectId</span><span class="sxs-lookup"><span data-stu-id="3e838-107">ByObjectId</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ObjectId <String>
 [-ApplicationId <Guid>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3e838-108">ByEmail</span><span class="sxs-lookup"><span data-stu-id="3e838-108">ByEmail</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -EmailAddress <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e838-109">ForVault</span><span class="sxs-lookup"><span data-stu-id="3e838-109">ForVault</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 [-EnabledForDeployment] [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e838-110">說明</span><span class="sxs-lookup"><span data-stu-id="3e838-110">DESCRIPTION</span></span>
<span data-ttu-id="3e838-111">**AzureRmKeyVaultAccessPolicy** Cmdlet 會移除使用者或應用程式的擁有權限，或從金鑰保存庫中的所有使用者和應用程式。</span><span class="sxs-lookup"><span data-stu-id="3e838-111">The **Remove-AzureRmKeyVaultAccessPolicy** cmdlet removes all permissions for a user or application or for all users and applications from a key vault.</span></span>
<span data-ttu-id="3e838-112">即使您移除擁有權限，包含金鑰保存庫的 Azure 訂閱擁有者也可以新增許可權給金鑰保存庫。</span><span class="sxs-lookup"><span data-stu-id="3e838-112">Even if you remove all permissions, the owner of the Azure subscription that contains the key vault can add permissions to the key vault.</span></span>

<span data-ttu-id="3e838-113">請注意，雖然為這個 Cmdlet 指定 [資源群組] 是選擇性的，但您應該這麼做，以取得較佳的效能。</span><span class="sxs-lookup"><span data-stu-id="3e838-113">Note that although specifying the resource group is optional for this cmdlet, you should do so for better performance.</span></span>

## <span data-ttu-id="3e838-114">示例</span><span class="sxs-lookup"><span data-stu-id="3e838-114">EXAMPLES</span></span>

### <span data-ttu-id="3e838-115">範例1：移除使用者的許可權</span><span class="sxs-lookup"><span data-stu-id="3e838-115">Example 1: Remove permissions for a user</span></span>
```
PS C:\>Remove-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com'
```

<span data-ttu-id="3e838-116">這個命令會移除使用者 PattiFuller@contoso.com 在名為 Contoso03Vault 的金鑰保存庫上擁有的擁有權限。</span><span class="sxs-lookup"><span data-stu-id="3e838-116">This command removes all the permissions that a user PattiFuller@contoso.com has on the key vault named Contoso03Vault.</span></span>

### <span data-ttu-id="3e838-117">範例2：移除應用程式的許可權</span><span class="sxs-lookup"><span data-stu-id="3e838-117">Example 2: Remove permissions for an application</span></span>
```
PS C:\>Remove-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ServicePrincipalName 'http://payroll.contoso.com'
```

<span data-ttu-id="3e838-118">這個命令會移除應用程式在名為 Contoso03Vault 的金鑰保存庫上擁有的擁有權限。</span><span class="sxs-lookup"><span data-stu-id="3e838-118">This command removes all the permissions that an application has on the key vault named Contoso03Vault.</span></span>
<span data-ttu-id="3e838-119">這個範例會使用在 Azure Active Directory 中註冊的服務主體名稱來識別應用程式 http://payroll.contoso.com 。</span><span class="sxs-lookup"><span data-stu-id="3e838-119">This example identifies the application by using the service principal name registered in Azure Active Directory, http://payroll.contoso.com.</span></span>

### <span data-ttu-id="3e838-120">範例3：使用物件識別碼移除應用程式的許可權</span><span class="sxs-lookup"><span data-stu-id="3e838-120">Example 3: Remove permissions for an application by using its object ID</span></span>
```
PS C:\>Remove-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ObjectID 34595082-9346-41b6-8d6b-295a2808b8db
```

<span data-ttu-id="3e838-121">這個命令會移除應用程式在名為 Contoso03Vault 的金鑰保存庫上擁有的擁有權限。</span><span class="sxs-lookup"><span data-stu-id="3e838-121">This command removes all the permissions that an application has on the key vault named Contoso03Vault.</span></span>
<span data-ttu-id="3e838-122">這個範例會依據服務主體的物件識別碼來識別應用程式。</span><span class="sxs-lookup"><span data-stu-id="3e838-122">This example identifies the application by the object ID of the service principal.</span></span>

### <span data-ttu-id="3e838-123">範例4：移除 Microsoft. 計算資源提供者的許可權</span><span class="sxs-lookup"><span data-stu-id="3e838-123">Example 4: Remove permissions for the Microsoft.Compute resource provider</span></span>
```
PS C:\>Remove-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnabledForDeployment
```

<span data-ttu-id="3e838-124">這個命令會移除 Microsoft. 計算資源提供者的許可權，以便從 Contoso03Vault 取得機密。</span><span class="sxs-lookup"><span data-stu-id="3e838-124">This command removes permission for the Microsoft.Compute resource provider to get secrets from the Contoso03Vault.</span></span>

## <span data-ttu-id="3e838-125">參數</span><span class="sxs-lookup"><span data-stu-id="3e838-125">PARAMETERS</span></span>

### <span data-ttu-id="3e838-126">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="3e838-126">-ApplicationId</span></span>
<span data-ttu-id="3e838-127">以供日後使用。</span><span class="sxs-lookup"><span data-stu-id="3e838-127">For future use.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: ByObjectId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e838-128">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="3e838-128">-EmailAddress</span></span>
<span data-ttu-id="3e838-129">指定您想要移除其存取權的使用者的使用者電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="3e838-129">Specifies the user email address of the user whose access you want to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByEmail
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e838-130">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="3e838-130">-EnabledForDeployment</span></span>
<span data-ttu-id="3e838-131">當在資源建立期間參照此金鑰保存庫時，可使用 Microsoft. 計算資源提供者來從此金鑰保存庫中取得機密資訊，例如建立虛擬機器時。</span><span class="sxs-lookup"><span data-stu-id="3e838-131">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForVault
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e838-132">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="3e838-132">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="3e838-133">讓 Azure 磁片加密服務從此金鑰保存庫取得機密和解除解包金鑰。</span><span class="sxs-lookup"><span data-stu-id="3e838-133">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForVault
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e838-134">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="3e838-134">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="3e838-135">在範本部署中參照此金鑰保存庫時，允許 Azure 資源管理員從該金鑰保存庫取得機密。</span><span class="sxs-lookup"><span data-stu-id="3e838-135">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForVault
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e838-136">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="3e838-136">-ObjectId</span></span>
<span data-ttu-id="3e838-137">指定 Azure Active Directory 中要移除許可權的使用者或服務主體物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="3e838-137">Specifies the object ID of the user or service principal in Azure Active Directory for which to remove permissions.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e838-138">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3e838-138">-PassThru</span></span>
<span data-ttu-id="3e838-139">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="3e838-139">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3e838-140">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="3e838-140">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3e838-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e838-141">-ResourceGroupName</span></span>
<span data-ttu-id="3e838-142">指定與要修改其存取原則之金鑰保存庫相關聯的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3e838-142">Specifies the name of the resource group associated with the key vault whose access policy is being modified.</span></span>
<span data-ttu-id="3e838-143">如果未指定，此 Cmdlet 會在目前的訂閱中搜尋主要電子倉庫。</span><span class="sxs-lookup"><span data-stu-id="3e838-143">If not specified, this cmdlet searches for the key vault in the current subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e838-144">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="3e838-144">-ServicePrincipalName</span></span>
<span data-ttu-id="3e838-145">指定您要移除其許可權之應用程式的服務主體名稱。</span><span class="sxs-lookup"><span data-stu-id="3e838-145">Specifies the service principal name of the application whose permissions you want to remove.</span></span>
<span data-ttu-id="3e838-146">指定在 Azure Active Directory 中為應用程式註冊的應用程式識別碼（也稱為「用戶端識別碼」）。</span><span class="sxs-lookup"><span data-stu-id="3e838-146">Specify the application ID, also known as client ID, registered for the application in Azure Active Directory.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServicePrincipalName
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e838-147">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="3e838-147">-UserPrincipalName</span></span>
<span data-ttu-id="3e838-148">指定您想要移除其存取權的使用者的使用者主要名稱。</span><span class="sxs-lookup"><span data-stu-id="3e838-148">Specifies the user principal name of the user whose access you want to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByUserPrincipalName
Aliases: UPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e838-149">-VaultName</span><span class="sxs-lookup"><span data-stu-id="3e838-149">-VaultName</span></span>
<span data-ttu-id="3e838-150">指定主要電子倉庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="3e838-150">Specifies the name of the key vault.</span></span>
<span data-ttu-id="3e838-151">這個 Cmdlet 會移除此參數指定之金鑰保存庫的許可權。</span><span class="sxs-lookup"><span data-stu-id="3e838-151">This cmdlet removes permissions for the key vault that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e838-152">-確認</span><span class="sxs-lookup"><span data-stu-id="3e838-152">-Confirm</span></span>
<span data-ttu-id="3e838-153">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3e838-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e838-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e838-154">-WhatIf</span></span>
<span data-ttu-id="3e838-155">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3e838-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e838-156">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3e838-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e838-157">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e838-157">-DefaultProfile</span></span>
<span data-ttu-id="3e838-158">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3e838-158">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3e838-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e838-159">CommonParameters</span></span>
<span data-ttu-id="3e838-160">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3e838-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e838-161">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3e838-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e838-162">輸入</span><span class="sxs-lookup"><span data-stu-id="3e838-162">INPUTS</span></span>

## <span data-ttu-id="3e838-163">輸出</span><span class="sxs-lookup"><span data-stu-id="3e838-163">OUTPUTS</span></span>

### <span data-ttu-id="3e838-164">PSVault 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="3e838-164">Microsoft.Azure.Commands.KeyVault.Models.PSVault</span></span>

## <span data-ttu-id="3e838-165">筆記</span><span class="sxs-lookup"><span data-stu-id="3e838-165">NOTES</span></span>

## <span data-ttu-id="3e838-166">相關連結</span><span class="sxs-lookup"><span data-stu-id="3e838-166">RELATED LINKS</span></span>

[<span data-ttu-id="3e838-167">Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3e838-167">Set-AzureRmKeyVaultAccessPolicy</span></span>](./Set-AzureRmKeyVaultAccessPolicy.md)

