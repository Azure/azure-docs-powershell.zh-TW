---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/Remove-AzSqlInstanceKeyVaultKey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceKeyVaultKey.md
ms.openlocfilehash: 6812f6da3e32fd6074dc6958568bf3bd7eddeff0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98436093"
---
# <span data-ttu-id="61a2e-101">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="61a2e-101">Remove-AzSqlInstanceKeyVaultKey</span></span>

## <span data-ttu-id="61a2e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="61a2e-102">SYNOPSIS</span></span>
<span data-ttu-id="61a2e-103">從 SQL managed 實例中移除金鑰保存庫金鑰</span><span class="sxs-lookup"><span data-stu-id="61a2e-103">Removes a Key Vault key from a SQL managed instance</span></span>

## <span data-ttu-id="61a2e-104">句法</span><span class="sxs-lookup"><span data-stu-id="61a2e-104">SYNTAX</span></span>

### <span data-ttu-id="61a2e-105">AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="61a2e-105">AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet (Default)</span></span>
```
Remove-AzSqlInstanceKeyVaultKey [-ResourceGroupName] <String> [-InstanceName] <String> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61a2e-106">AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="61a2e-106">AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet</span></span>
```
Remove-AzSqlInstanceKeyVaultKey [-Instance] <AzureSqlManagedInstanceModel> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61a2e-107">AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="61a2e-107">AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet</span></span>
```
Remove-AzSqlInstanceKeyVaultKey [-InstanceResourceId] <String> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61a2e-108">說明</span><span class="sxs-lookup"><span data-stu-id="61a2e-108">DESCRIPTION</span></span>
<span data-ttu-id="61a2e-109">Remove-AzSqlInstanceKeyVaultKey Cmdlet 會從指定的受管理實例中移除金鑰保存庫金鑰。</span><span class="sxs-lookup"><span data-stu-id="61a2e-109">The Remove-AzSqlInstanceKeyVaultKey cmdlet  removes the Key Vault key from the specified Managed Instance.</span></span> <span data-ttu-id="61a2e-110">請注意，系統不會變更 SQL managed 實例對金鑰電子倉庫的許可權。</span><span class="sxs-lookup"><span data-stu-id="61a2e-110">Note that the SQL managed instance's permissions to the key's vault are not changed.</span></span> <span data-ttu-id="61a2e-111">若要變更許可權，請使用 [設定-AzKeyVaultAccessPolicy]。</span><span class="sxs-lookup"><span data-stu-id="61a2e-111">To change permissions, use Set-AzKeyVaultAccessPolicy.</span></span> <span data-ttu-id="61a2e-112">請注意，這個 Cmdlet 不會變更金鑰保存庫。</span><span class="sxs-lookup"><span data-stu-id="61a2e-112">Note that this cmdlet makes no changes to Key Vault.</span></span> <span data-ttu-id="61a2e-113">若要從 [主要電子倉庫] 移除金鑰，請使用 [移除-AzureKeyVaultKey]。</span><span class="sxs-lookup"><span data-stu-id="61a2e-113">To remove a key from Key Vault, use Remove-AzureKeyVaultKey.</span></span>

## <span data-ttu-id="61a2e-114">示例</span><span class="sxs-lookup"><span data-stu-id="61a2e-114">EXAMPLES</span></span>

### <span data-ttu-id="61a2e-115">範例1</span><span class="sxs-lookup"><span data-stu-id="61a2e-115">Example 1</span></span>
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

<span data-ttu-id="61a2e-116">此命令會 https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 從指定的受管理實例中移除 Id 為 "" 的主要保存庫金鑰。</span><span class="sxs-lookup"><span data-stu-id="61a2e-116">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified managed instance.</span></span> 

### <span data-ttu-id="61a2e-117">範例2：使用 managed 實例物件</span><span class="sxs-lookup"><span data-stu-id="61a2e-117">Example 2: Using managed instance object</span></span>
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

<span data-ttu-id="61a2e-118">此命令會 https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 從指定的受管理實例中移除 Id 為 "" 的主要保存庫金鑰。</span><span class="sxs-lookup"><span data-stu-id="61a2e-118">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified managed instance.</span></span> 

### <span data-ttu-id="61a2e-119">範例3：使用 managed 實例資源識別碼</span><span class="sxs-lookup"><span data-stu-id="61a2e-119">Example 3: Using managed instance resource id</span></span>
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

<span data-ttu-id="61a2e-120">此命令會 https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 從指定的受管理實例中移除 Id 為 "" 的主要保存庫金鑰。</span><span class="sxs-lookup"><span data-stu-id="61a2e-120">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified managed instance.</span></span> 

### <span data-ttu-id="61a2e-121">範例4：使用管道</span><span class="sxs-lookup"><span data-stu-id="61a2e-121">Example 4: Using piping</span></span>
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

<span data-ttu-id="61a2e-122">此命令會 https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 從指定的受管理實例中移除 Id 為 "" 的主要保存庫金鑰。</span><span class="sxs-lookup"><span data-stu-id="61a2e-122">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified managed instance.</span></span> 

## <span data-ttu-id="61a2e-123">參數</span><span class="sxs-lookup"><span data-stu-id="61a2e-123">PARAMETERS</span></span>

### <span data-ttu-id="61a2e-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61a2e-124">-DefaultProfile</span></span>
<span data-ttu-id="61a2e-125">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="61a2e-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61a2e-126">-實例</span><span class="sxs-lookup"><span data-stu-id="61a2e-126">-Instance</span></span>
<span data-ttu-id="61a2e-127">實例輸入物件</span><span class="sxs-lookup"><span data-stu-id="61a2e-127">The instance input object</span></span>

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

### <span data-ttu-id="61a2e-128">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="61a2e-128">-InstanceName</span></span>
<span data-ttu-id="61a2e-129">實例名稱</span><span class="sxs-lookup"><span data-stu-id="61a2e-129">The instance name</span></span>

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

### <span data-ttu-id="61a2e-130">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="61a2e-130">-InstanceResourceId</span></span>
<span data-ttu-id="61a2e-131">實例資源識別碼</span><span class="sxs-lookup"><span data-stu-id="61a2e-131">The instance resource id</span></span>

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

### <span data-ttu-id="61a2e-132">-KeyId</span><span class="sxs-lookup"><span data-stu-id="61a2e-132">-KeyId</span></span>
<span data-ttu-id="61a2e-133">AzureKeyVault 金鑰識別碼</span><span class="sxs-lookup"><span data-stu-id="61a2e-133">AzureKeyVault key id</span></span>

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

### <span data-ttu-id="61a2e-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61a2e-134">-ResourceGroupName</span></span>
<span data-ttu-id="61a2e-135">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="61a2e-135">The Resource Group Name</span></span>

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

### <span data-ttu-id="61a2e-136">-確認</span><span class="sxs-lookup"><span data-stu-id="61a2e-136">-Confirm</span></span>
<span data-ttu-id="61a2e-137">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="61a2e-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61a2e-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61a2e-138">-WhatIf</span></span>
<span data-ttu-id="61a2e-139">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="61a2e-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61a2e-140">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="61a2e-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61a2e-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61a2e-141">CommonParameters</span></span>
<span data-ttu-id="61a2e-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="61a2e-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61a2e-143">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="61a2e-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61a2e-144">輸入</span><span class="sxs-lookup"><span data-stu-id="61a2e-144">INPUTS</span></span>

### <span data-ttu-id="61a2e-145">AzureSqlManagedInstanceModel 中的 [ManagedInstance]</span><span class="sxs-lookup"><span data-stu-id="61a2e-145">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="61a2e-146">System.object</span><span class="sxs-lookup"><span data-stu-id="61a2e-146">System.String</span></span>

## <span data-ttu-id="61a2e-147">輸出</span><span class="sxs-lookup"><span data-stu-id="61a2e-147">OUTPUTS</span></span>

### <span data-ttu-id="61a2e-148">AzureRmSqlManagedInstanceKeyVaultKeyModel 中的 [TransparentDataEncryption]</span><span class="sxs-lookup"><span data-stu-id="61a2e-148">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceKeyVaultKeyModel</span></span>

## <span data-ttu-id="61a2e-149">筆記</span><span class="sxs-lookup"><span data-stu-id="61a2e-149">NOTES</span></span>

## <span data-ttu-id="61a2e-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="61a2e-150">RELATED LINKS</span></span>
