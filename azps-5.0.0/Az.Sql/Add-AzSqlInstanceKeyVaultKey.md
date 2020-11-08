---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Add-AzSqlInstanceKeyVaultKey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlInstanceKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlInstanceKeyVaultKey.md
ms.openlocfilehash: 0ceaf3906860916c4740c3d06d1c9ee91be421cb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94136648"
---
# <span data-ttu-id="b2525-101">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="b2525-101">Add-AzSqlInstanceKeyVaultKey</span></span>

## <span data-ttu-id="b2525-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b2525-102">SYNOPSIS</span></span>
<span data-ttu-id="b2525-103">將主要保存庫金鑰新增至提供的受管理實例。</span><span class="sxs-lookup"><span data-stu-id="b2525-103">Adds a key vault key to the provided Managed Instance.</span></span> 

## <span data-ttu-id="b2525-104">句法</span><span class="sxs-lookup"><span data-stu-id="b2525-104">SYNTAX</span></span>

### <span data-ttu-id="b2525-105">AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="b2525-105">AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet (Default)</span></span>
```
Add-AzSqlInstanceKeyVaultKey [-ResourceGroupName] <String> [-InstanceName] <String> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2525-106">AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b2525-106">AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet</span></span>
```
Add-AzSqlInstanceKeyVaultKey [-Instance] <AzureSqlManagedInstanceModel> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2525-107">AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b2525-107">AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet</span></span>
```
Add-AzSqlInstanceKeyVaultKey [-InstanceResourceId] <String> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2525-108">說明</span><span class="sxs-lookup"><span data-stu-id="b2525-108">DESCRIPTION</span></span>
<span data-ttu-id="b2525-109">Add-AzSqlInstanceKeyVaultKey Cmdlet 會將主要保存庫金鑰新增至提供的受管理實例。</span><span class="sxs-lookup"><span data-stu-id="b2525-109">The Add-AzSqlInstanceKeyVaultKey cmdlet adds a key vault key to the provided Managed Instance.</span></span> <span data-ttu-id="b2525-110">受管理的實例必須具有保存庫的「取得、wrapKey、unwrapKey」許可權，請使用下列腳本來授與受管理實例的許可權。</span><span class="sxs-lookup"><span data-stu-id="b2525-110">The managed instance must have 'get, wrapKey, unwrapKey' permissions to the vault, use the following script to grant permission to the managed instance.</span></span>
<span data-ttu-id="b2525-111">$managedInstance = Get-AzSqlInstance-Name "ContosoManagedInstanceName"-ResourceGroupName "ContosoResourceGroup" Set-AzKeyVaultAccessPolicy-VaultName ContosoVault-ObjectId $managedInstance. PrincipalId-PermissionsToKeys、wrapKey、unwrapKey</span><span class="sxs-lookup"><span data-stu-id="b2525-111">$managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup' Set-AzKeyVaultAccessPolicy -VaultName ContosoVault -ObjectId $managedInstance.Identity.PrincipalId -PermissionsToKeys get, wrapKey, unwrapKey</span></span>

## <span data-ttu-id="b2525-112">示例</span><span class="sxs-lookup"><span data-stu-id="b2525-112">EXAMPLES</span></span>

### <span data-ttu-id="b2525-113">範例1</span><span class="sxs-lookup"><span data-stu-id="b2525-113">Example 1</span></span>
```powershell
PS C:\> Add-AzSqlInstanceKeyVaultKey -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName' -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="b2525-114">這個命令會將 Id "" 的主要保存庫金鑰新增 https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 至資源群組 "ContosoResourceGroup" 中名為 "ContosoManagedInstanceName" 的 SQL managed 實例。</span><span class="sxs-lookup"><span data-stu-id="b2525-114">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL managed instance named 'ContosoManagedInstanceName' in the resource group 'ContosoResourceGroup'.</span></span> 

### <span data-ttu-id="b2525-115">範例2：使用 managed 實例物件</span><span class="sxs-lookup"><span data-stu-id="b2525-115">Example 2: Using managed instance object</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Add-AzSqlInstanceKeyVaultKey -Instance $managedInstance -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="b2525-116">這個命令會將 Id "" 的主要保存庫金鑰新增 https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 至資源群組 "ContosoResourceGroup" 中名為 "ContosoManagedInstanceName" 的 SQL managed 實例。</span><span class="sxs-lookup"><span data-stu-id="b2525-116">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL managed instance named 'ContosoManagedInstanceName' in the resource group 'ContosoResourceGroup'.</span></span> 

### <span data-ttu-id="b2525-117">範例3：使用 managed 實例資源識別碼</span><span class="sxs-lookup"><span data-stu-id="b2525-117">Example 3: Using managed instance resource id</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Add-AzSqlInstanceKeyVaultKey -InstanceResourceId $managedInstance.ResourceId -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="b2525-118">這個命令會將 Id "" 的主要保存庫金鑰新增 https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 至資源群組 "ContosoResourceGroup" 中名為 "ContosoManagedInstanceName" 的 SQL managed 實例。</span><span class="sxs-lookup"><span data-stu-id="b2525-118">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL managed instance named 'ContosoManagedInstanceName' in the resource group 'ContosoResourceGroup'.</span></span> 

### <span data-ttu-id="b2525-119">範例4：使用管道</span><span class="sxs-lookup"><span data-stu-id="b2525-119">Example 4: Using piping</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> $managedInstance | Add-AzSqlInstanceKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="b2525-120">這個命令會將 Id "" 的主要保存庫金鑰新增 https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 至資源群組 "ContosoResourceGroup" 中名為 "ContosoManagedInstanceName" 的 SQL managed 實例。</span><span class="sxs-lookup"><span data-stu-id="b2525-120">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL managed instance named 'ContosoManagedInstanceName' in the resource group 'ContosoResourceGroup'.</span></span> 

## <span data-ttu-id="b2525-121">參數</span><span class="sxs-lookup"><span data-stu-id="b2525-121">PARAMETERS</span></span>

### <span data-ttu-id="b2525-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2525-122">-DefaultProfile</span></span>
<span data-ttu-id="b2525-123">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b2525-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2525-124">-實例</span><span class="sxs-lookup"><span data-stu-id="b2525-124">-Instance</span></span>
<span data-ttu-id="b2525-125">實例輸入物件</span><span class="sxs-lookup"><span data-stu-id="b2525-125">The instance input object</span></span>

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

### <span data-ttu-id="b2525-126">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="b2525-126">-InstanceName</span></span>
<span data-ttu-id="b2525-127">實例名稱</span><span class="sxs-lookup"><span data-stu-id="b2525-127">The instance name</span></span>

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

### <span data-ttu-id="b2525-128">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="b2525-128">-InstanceResourceId</span></span>
<span data-ttu-id="b2525-129">實例資源識別碼</span><span class="sxs-lookup"><span data-stu-id="b2525-129">The instance resource id</span></span>

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

### <span data-ttu-id="b2525-130">-KeyId</span><span class="sxs-lookup"><span data-stu-id="b2525-130">-KeyId</span></span>
<span data-ttu-id="b2525-131">AzureKeyVault 金鑰識別碼</span><span class="sxs-lookup"><span data-stu-id="b2525-131">AzureKeyVault key id</span></span>

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

### <span data-ttu-id="b2525-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2525-132">-ResourceGroupName</span></span>
<span data-ttu-id="b2525-133">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="b2525-133">The Resource Group Name</span></span>

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

### <span data-ttu-id="b2525-134">-確認</span><span class="sxs-lookup"><span data-stu-id="b2525-134">-Confirm</span></span>
<span data-ttu-id="b2525-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b2525-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2525-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2525-136">-WhatIf</span></span>
<span data-ttu-id="b2525-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b2525-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2525-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b2525-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2525-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2525-139">CommonParameters</span></span>
<span data-ttu-id="b2525-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b2525-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2525-141">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b2525-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2525-142">輸入</span><span class="sxs-lookup"><span data-stu-id="b2525-142">INPUTS</span></span>

### <span data-ttu-id="b2525-143">AzureSqlManagedInstanceModel 中的 [ManagedInstance]</span><span class="sxs-lookup"><span data-stu-id="b2525-143">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="b2525-144">System.object</span><span class="sxs-lookup"><span data-stu-id="b2525-144">System.String</span></span>

## <span data-ttu-id="b2525-145">輸出</span><span class="sxs-lookup"><span data-stu-id="b2525-145">OUTPUTS</span></span>

### <span data-ttu-id="b2525-146">AzureRmSqlManagedInstanceKeyVaultKeyModel 中的 [TransparentDataEncryption]</span><span class="sxs-lookup"><span data-stu-id="b2525-146">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceKeyVaultKeyModel</span></span>

## <span data-ttu-id="b2525-147">筆記</span><span class="sxs-lookup"><span data-stu-id="b2525-147">NOTES</span></span>

## <span data-ttu-id="b2525-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="b2525-148">RELATED LINKS</span></span>
