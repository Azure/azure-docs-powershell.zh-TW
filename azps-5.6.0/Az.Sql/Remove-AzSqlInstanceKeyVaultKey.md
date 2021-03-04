---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/Remove-AzSqlInstanceKeyVaultKey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceKeyVaultKey.md
ms.openlocfilehash: a7c8b4943299ed4cd81e09099191193f396cde5e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905777"
---
# <span data-ttu-id="125bd-101">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="125bd-101">Remove-AzSqlInstanceKeyVaultKey</span></span>

## <span data-ttu-id="125bd-102">簡介</span><span class="sxs-lookup"><span data-stu-id="125bd-102">SYNOPSIS</span></span>
<span data-ttu-id="125bd-103">從 SQL 受管理的實例移除金鑰庫金鑰</span><span class="sxs-lookup"><span data-stu-id="125bd-103">Removes a Key Vault key from a SQL managed instance</span></span>

## <span data-ttu-id="125bd-104">語法</span><span class="sxs-lookup"><span data-stu-id="125bd-104">SYNTAX</span></span>

### <span data-ttu-id="125bd-105">AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="125bd-105">AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet (Default)</span></span>
```
Remove-AzSqlInstanceKeyVaultKey [-ResourceGroupName] <String> [-InstanceName] <String> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="125bd-106">AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="125bd-106">AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet</span></span>
```
Remove-AzSqlInstanceKeyVaultKey [-Instance] <AzureSqlManagedInstanceModel> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="125bd-107">AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="125bd-107">AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet</span></span>
```
Remove-AzSqlInstanceKeyVaultKey [-InstanceResourceId] <String> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="125bd-108">描述</span><span class="sxs-lookup"><span data-stu-id="125bd-108">DESCRIPTION</span></span>
<span data-ttu-id="125bd-109">此Remove-AzSqlInstanceKeyVaultKey Cmdlet 會從指定的受管理實例移除金鑰庫金鑰。</span><span class="sxs-lookup"><span data-stu-id="125bd-109">The Remove-AzSqlInstanceKeyVaultKey cmdlet  removes the Key Vault key from the specified Managed Instance.</span></span> <span data-ttu-id="125bd-110">請注意，SQL 受管理實例對金鑰庫的許可權不會變更。</span><span class="sxs-lookup"><span data-stu-id="125bd-110">Note that the SQL managed instance's permissions to the key's vault are not changed.</span></span> <span data-ttu-id="125bd-111">若要變更許可權，請使用 Set-AzKeyVaultAccessPolicy。</span><span class="sxs-lookup"><span data-stu-id="125bd-111">To change permissions, use Set-AzKeyVaultAccessPolicy.</span></span> <span data-ttu-id="125bd-112">請注意，此 Cmdlet 不會變更金鑰保存庫。</span><span class="sxs-lookup"><span data-stu-id="125bd-112">Note that this cmdlet makes no changes to Key Vault.</span></span> <span data-ttu-id="125bd-113">若要從 Key Vault 移除金鑰，請使用 Remove-AzureKeyVaultKey。</span><span class="sxs-lookup"><span data-stu-id="125bd-113">To remove a key from Key Vault, use Remove-AzureKeyVaultKey.</span></span>

## <span data-ttu-id="125bd-114">例子</span><span class="sxs-lookup"><span data-stu-id="125bd-114">EXAMPLES</span></span>

### <span data-ttu-id="125bd-115">範例 1</span><span class="sxs-lookup"><span data-stu-id="125bd-115">Example 1</span></span>
```powershell
PS C:\> Remove-AzSqlInstanceKeyVaultKey -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName' -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="125bd-116">此命令會從指定的受管理實例移除具有 Id ' ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 的 Key Vault 金鑰。</span><span class="sxs-lookup"><span data-stu-id="125bd-116">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified managed instance.</span></span> 

### <span data-ttu-id="125bd-117">範例 2：使用受管理的實例物件</span><span class="sxs-lookup"><span data-stu-id="125bd-117">Example 2: Using managed instance object</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Remove-AzSqlInstanceKeyVaultKey -Instance $managedInstance -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="125bd-118">此命令會從指定的受管理實例移除具有 Id ' ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 的 Key Vault 金鑰。</span><span class="sxs-lookup"><span data-stu-id="125bd-118">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified managed instance.</span></span> 

### <span data-ttu-id="125bd-119">範例 3：使用受管理的實例資源識別碼</span><span class="sxs-lookup"><span data-stu-id="125bd-119">Example 3: Using managed instance resource id</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Remove-AzSqlInstanceKeyVaultKey -InstanceResourceId $managedInstance.ResourceId -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="125bd-120">此命令會從指定的受管理實例移除具有 Id ' ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 的 Key Vault 金鑰。</span><span class="sxs-lookup"><span data-stu-id="125bd-120">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified managed instance.</span></span> 

### <span data-ttu-id="125bd-121">範例 4：使用管線</span><span class="sxs-lookup"><span data-stu-id="125bd-121">Example 4: Using piping</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> $managedInstance | Remove-AzSqlInstanceKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="125bd-122">此命令會從指定的受管理實例移除具有 Id ' ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 的 Key Vault 金鑰。</span><span class="sxs-lookup"><span data-stu-id="125bd-122">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified managed instance.</span></span> 

## <span data-ttu-id="125bd-123">參數</span><span class="sxs-lookup"><span data-stu-id="125bd-123">PARAMETERS</span></span>

### <span data-ttu-id="125bd-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="125bd-124">-DefaultProfile</span></span>
<span data-ttu-id="125bd-125">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="125bd-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="125bd-126">-實例</span><span class="sxs-lookup"><span data-stu-id="125bd-126">-Instance</span></span>
<span data-ttu-id="125bd-127">實例輸入物件</span><span class="sxs-lookup"><span data-stu-id="125bd-127">The instance input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet
Aliases: InputObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="125bd-128">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="125bd-128">-InstanceName</span></span>
<span data-ttu-id="125bd-129">實例名稱</span><span class="sxs-lookup"><span data-stu-id="125bd-129">The instance name</span></span>

```yaml
Type: System.String
Parameter Sets: AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="125bd-130">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="125bd-130">-InstanceResourceId</span></span>
<span data-ttu-id="125bd-131">實例資源識別碼</span><span class="sxs-lookup"><span data-stu-id="125bd-131">The instance resource id</span></span>

```yaml
Type: System.String
Parameter Sets: AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="125bd-132">-KeyId</span><span class="sxs-lookup"><span data-stu-id="125bd-132">-KeyId</span></span>
<span data-ttu-id="125bd-133">AzureKeyVault 金鑰識別碼</span><span class="sxs-lookup"><span data-stu-id="125bd-133">AzureKeyVault key id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="125bd-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="125bd-134">-ResourceGroupName</span></span>
<span data-ttu-id="125bd-135">資源組名</span><span class="sxs-lookup"><span data-stu-id="125bd-135">The Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="125bd-136">-確認</span><span class="sxs-lookup"><span data-stu-id="125bd-136">-Confirm</span></span>
<span data-ttu-id="125bd-137">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="125bd-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="125bd-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="125bd-138">-WhatIf</span></span>
<span data-ttu-id="125bd-139">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="125bd-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="125bd-140">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="125bd-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="125bd-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="125bd-141">CommonParameters</span></span>
<span data-ttu-id="125bd-142">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="125bd-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="125bd-143">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="125bd-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="125bd-144">輸入</span><span class="sxs-lookup"><span data-stu-id="125bd-144">INPUTS</span></span>

### <span data-ttu-id="125bd-145">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="125bd-145">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="125bd-146">System.String</span><span class="sxs-lookup"><span data-stu-id="125bd-146">System.String</span></span>

## <span data-ttu-id="125bd-147">輸出</span><span class="sxs-lookup"><span data-stu-id="125bd-147">OUTPUTS</span></span>

### <span data-ttu-id="125bd-148">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="125bd-148">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceKeyVaultKeyModel</span></span>

## <span data-ttu-id="125bd-149">筆記</span><span class="sxs-lookup"><span data-stu-id="125bd-149">NOTES</span></span>

## <span data-ttu-id="125bd-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="125bd-150">RELATED LINKS</span></span>
