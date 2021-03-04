---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/Add-AzSqlInstanceKeyVaultKey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlInstanceKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlInstanceKeyVaultKey.md
ms.openlocfilehash: 5a83d442f0b12731de3a00468283a8539b529fa7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904302"
---
# <span data-ttu-id="cc4fc-101">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="cc4fc-101">Add-AzSqlInstanceKeyVaultKey</span></span>

## <span data-ttu-id="cc4fc-102">簡介</span><span class="sxs-lookup"><span data-stu-id="cc4fc-102">SYNOPSIS</span></span>
<span data-ttu-id="cc4fc-103">在提供的受管理實例中新增金鑰庫金鑰。</span><span class="sxs-lookup"><span data-stu-id="cc4fc-103">Adds a key vault key to the provided Managed Instance.</span></span> 

## <span data-ttu-id="cc4fc-104">語法</span><span class="sxs-lookup"><span data-stu-id="cc4fc-104">SYNTAX</span></span>

### <span data-ttu-id="cc4fc-105">AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="cc4fc-105">AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet (Default)</span></span>
```
Add-AzSqlInstanceKeyVaultKey [-ResourceGroupName] <String> [-InstanceName] <String> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc4fc-106">AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc4fc-106">AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet</span></span>
```
Add-AzSqlInstanceKeyVaultKey [-Instance] <AzureSqlManagedInstanceModel> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc4fc-107">AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc4fc-107">AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet</span></span>
```
Add-AzSqlInstanceKeyVaultKey [-InstanceResourceId] <String> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc4fc-108">描述</span><span class="sxs-lookup"><span data-stu-id="cc4fc-108">DESCRIPTION</span></span>
<span data-ttu-id="cc4fc-109">Cmdlet Add-AzSqlInstanceKeyVaultKey在提供的受管理實例中新增金鑰庫金鑰。</span><span class="sxs-lookup"><span data-stu-id="cc4fc-109">The Add-AzSqlInstanceKeyVaultKey cmdlet adds a key vault key to the provided Managed Instance.</span></span> <span data-ttu-id="cc4fc-110">受管理實例必須具有對儲存庫的'get、wrapKey、unwrapKey'許可權，請使用下列腳本將許可權授予受管理實例。</span><span class="sxs-lookup"><span data-stu-id="cc4fc-110">The managed instance must have 'get, wrapKey, unwrapKey' permissions to the vault, use the following script to grant permission to the managed instance.</span></span>
<span data-ttu-id="cc4fc-111">$managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup' Set-AzKeyVaultAccessPolicy -VaultName ContosoVault -ObjectId $managedInstance.Identity.PrincipalId -PermissionsToKeys get， wrapKey， unw片Key</span><span class="sxs-lookup"><span data-stu-id="cc4fc-111">$managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup' Set-AzKeyVaultAccessPolicy -VaultName ContosoVault -ObjectId $managedInstance.Identity.PrincipalId -PermissionsToKeys get, wrapKey, unwrapKey</span></span>

## <span data-ttu-id="cc4fc-112">例子</span><span class="sxs-lookup"><span data-stu-id="cc4fc-112">EXAMPLES</span></span>

### <span data-ttu-id="cc4fc-113">範例 1</span><span class="sxs-lookup"><span data-stu-id="cc4fc-113">Example 1</span></span>
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

<span data-ttu-id="cc4fc-114">此命令會將 Id 為 '' 的 Key Vault 鍵新增到資源群組 https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 'ContosoResourceGroup'中名為 'ContosoManagedInstanceName'的 SQL 受管理實例。</span><span class="sxs-lookup"><span data-stu-id="cc4fc-114">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL managed instance named 'ContosoManagedInstanceName' in the resource group 'ContosoResourceGroup'.</span></span> 

### <span data-ttu-id="cc4fc-115">範例 2：使用受管理的實例物件</span><span class="sxs-lookup"><span data-stu-id="cc4fc-115">Example 2: Using managed instance object</span></span>
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

<span data-ttu-id="cc4fc-116">此命令會將 Id 為 '' 的 Key Vault 鍵新增到資源群組 https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 'ContosoResourceGroup'中名為 'ContosoManagedInstanceName'的 SQL 受管理實例。</span><span class="sxs-lookup"><span data-stu-id="cc4fc-116">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL managed instance named 'ContosoManagedInstanceName' in the resource group 'ContosoResourceGroup'.</span></span> 

### <span data-ttu-id="cc4fc-117">範例 3：使用受管理的實例資源識別碼</span><span class="sxs-lookup"><span data-stu-id="cc4fc-117">Example 3: Using managed instance resource id</span></span>
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

<span data-ttu-id="cc4fc-118">此命令會將 Id 為 '' 的 Key Vault 鍵新增到資源群組 https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 'ContosoResourceGroup'中名為 'ContosoManagedInstanceName'的 SQL 受管理實例。</span><span class="sxs-lookup"><span data-stu-id="cc4fc-118">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL managed instance named 'ContosoManagedInstanceName' in the resource group 'ContosoResourceGroup'.</span></span> 

### <span data-ttu-id="cc4fc-119">範例 4：使用管線</span><span class="sxs-lookup"><span data-stu-id="cc4fc-119">Example 4: Using piping</span></span>
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

<span data-ttu-id="cc4fc-120">此命令會將 Id 為 '' 的 Key Vault 鍵新增到資源群組 https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 'ContosoResourceGroup'中名為 'ContosoManagedInstanceName'的 SQL 受管理實例。</span><span class="sxs-lookup"><span data-stu-id="cc4fc-120">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL managed instance named 'ContosoManagedInstanceName' in the resource group 'ContosoResourceGroup'.</span></span> 

## <span data-ttu-id="cc4fc-121">參數</span><span class="sxs-lookup"><span data-stu-id="cc4fc-121">PARAMETERS</span></span>

### <span data-ttu-id="cc4fc-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc4fc-122">-DefaultProfile</span></span>
<span data-ttu-id="cc4fc-123">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="cc4fc-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc4fc-124">-實例</span><span class="sxs-lookup"><span data-stu-id="cc4fc-124">-Instance</span></span>
<span data-ttu-id="cc4fc-125">實例輸入物件</span><span class="sxs-lookup"><span data-stu-id="cc4fc-125">The instance input object</span></span>

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

### <span data-ttu-id="cc4fc-126">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="cc4fc-126">-InstanceName</span></span>
<span data-ttu-id="cc4fc-127">實例名稱</span><span class="sxs-lookup"><span data-stu-id="cc4fc-127">The instance name</span></span>

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

### <span data-ttu-id="cc4fc-128">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="cc4fc-128">-InstanceResourceId</span></span>
<span data-ttu-id="cc4fc-129">實例資源識別碼</span><span class="sxs-lookup"><span data-stu-id="cc4fc-129">The instance resource id</span></span>

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

### <span data-ttu-id="cc4fc-130">-KeyId</span><span class="sxs-lookup"><span data-stu-id="cc4fc-130">-KeyId</span></span>
<span data-ttu-id="cc4fc-131">AzureKeyVault 金鑰識別碼</span><span class="sxs-lookup"><span data-stu-id="cc4fc-131">AzureKeyVault key id</span></span>

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

### <span data-ttu-id="cc4fc-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc4fc-132">-ResourceGroupName</span></span>
<span data-ttu-id="cc4fc-133">資源組名</span><span class="sxs-lookup"><span data-stu-id="cc4fc-133">The Resource Group Name</span></span>

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

### <span data-ttu-id="cc4fc-134">-確認</span><span class="sxs-lookup"><span data-stu-id="cc4fc-134">-Confirm</span></span>
<span data-ttu-id="cc4fc-135">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="cc4fc-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc4fc-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc4fc-136">-WhatIf</span></span>
<span data-ttu-id="cc4fc-137">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cc4fc-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc4fc-138">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cc4fc-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc4fc-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc4fc-139">CommonParameters</span></span>
<span data-ttu-id="cc4fc-140">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="cc4fc-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc4fc-141">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cc4fc-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc4fc-142">輸入</span><span class="sxs-lookup"><span data-stu-id="cc4fc-142">INPUTS</span></span>

### <span data-ttu-id="cc4fc-143">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="cc4fc-143">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="cc4fc-144">System.String</span><span class="sxs-lookup"><span data-stu-id="cc4fc-144">System.String</span></span>

## <span data-ttu-id="cc4fc-145">輸出</span><span class="sxs-lookup"><span data-stu-id="cc4fc-145">OUTPUTS</span></span>

### <span data-ttu-id="cc4fc-146">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="cc4fc-146">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceKeyVaultKeyModel</span></span>

## <span data-ttu-id="cc4fc-147">筆記</span><span class="sxs-lookup"><span data-stu-id="cc4fc-147">NOTES</span></span>

## <span data-ttu-id="cc4fc-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="cc4fc-148">RELATED LINKS</span></span>
