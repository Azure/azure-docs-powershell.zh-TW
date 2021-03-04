---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/Get-AzSqlInstanceKeyVaultKey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceKeyVaultKey.md
ms.openlocfilehash: 05c9565152063f10fb80d04fab0264807e9f3308
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914293"
---
# <span data-ttu-id="73f5b-101">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="73f5b-101">Get-AzSqlInstanceKeyVaultKey</span></span>

## <span data-ttu-id="73f5b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="73f5b-102">SYNOPSIS</span></span>
<span data-ttu-id="73f5b-103">獲得 SQL 受管理實例的 Key Vault 鍵。</span><span class="sxs-lookup"><span data-stu-id="73f5b-103">Gets a SQL managed instance's Key Vault keys.</span></span>

## <span data-ttu-id="73f5b-104">語法</span><span class="sxs-lookup"><span data-stu-id="73f5b-104">SYNTAX</span></span>

### <span data-ttu-id="73f5b-105">AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="73f5b-105">AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet (Default)</span></span>
```
Get-AzSqlInstanceKeyVaultKey [[-KeyId] <String>] [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73f5b-106">AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="73f5b-106">AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet</span></span>
```
Get-AzSqlInstanceKeyVaultKey [[-KeyId] <String>] [-Instance] <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73f5b-107">AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="73f5b-107">AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet</span></span>
```
Get-AzSqlInstanceKeyVaultKey [[-KeyId] <String>] [-InstanceResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73f5b-108">描述</span><span class="sxs-lookup"><span data-stu-id="73f5b-108">DESCRIPTION</span></span>
<span data-ttu-id="73f5b-109">此Get-AzSqlInstanceKeyVaultKey Cmdlet 會獲得 SQL 受管理實例上金鑰庫金鑰的資訊。</span><span class="sxs-lookup"><span data-stu-id="73f5b-109">The Get-AzSqlInstanceKeyVaultKey cmdlet gets information about the Key Vault keys on a SQL managed instance.</span></span> <span data-ttu-id="73f5b-110">您可以查看受管理實例上的所有金鑰，或提供 KeyId 來查看特定金鑰。</span><span class="sxs-lookup"><span data-stu-id="73f5b-110">You can view all keys on a managed instance or view a specific key by providing the KeyId.</span></span>

## <span data-ttu-id="73f5b-111">例子</span><span class="sxs-lookup"><span data-stu-id="73f5b-111">EXAMPLES</span></span>

### <span data-ttu-id="73f5b-112">範例 1：取得所有 Key Vault 鍵</span><span class="sxs-lookup"><span data-stu-id="73f5b-112">Example 1: Get all Key Vault keys</span></span>
```powershell
PS C:\> Get-AzSqlInstanceKeyVaultKey -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="73f5b-113">此命令會獲得 SQL 受管理實例上的所有 Key Vault 鍵。</span><span class="sxs-lookup"><span data-stu-id="73f5b-113">This command gets all the Key Vault keys on a SQL managed instance.</span></span>

### <span data-ttu-id="73f5b-114">範例 2：取得特定的金鑰庫金鑰</span><span class="sxs-lookup"><span data-stu-id="73f5b-114">Example 2: Get a specific Key Vault key</span></span>
```powershell
PS C:\> Get-AzSqlInstanceKeyVaultKey -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName' -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="73f5b-115">此命令會獲得具有 Id ' ''的 Key Vault https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 鍵。</span><span class="sxs-lookup"><span data-stu-id="73f5b-115">This command gets the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'.</span></span>

### <span data-ttu-id="73f5b-116">範例 3：使用實例物件</span><span class="sxs-lookup"><span data-stu-id="73f5b-116">Example 3: Using instance object</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Get-AzSqlInstanceKeyVaultKey -ManagedInstance $managedInstance -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="73f5b-117">此命令會獲得具有 Id ' ''的 Key Vault https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 鍵。</span><span class="sxs-lookup"><span data-stu-id="73f5b-117">This command gets the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'.</span></span>

### <span data-ttu-id="73f5b-118">範例 4：使用實例資源識別碼</span><span class="sxs-lookup"><span data-stu-id="73f5b-118">Example 4: Using instance resource id</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Get-AzSqlInstanceKeyVaultKey -InstanceResourceId $managedInstance.ResourceId -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="73f5b-119">此命令會獲得具有 Id ' ''的 Key Vault https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 鍵。</span><span class="sxs-lookup"><span data-stu-id="73f5b-119">This command gets the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'.</span></span>

### <span data-ttu-id="73f5b-120">範例 5：使用管線</span><span class="sxs-lookup"><span data-stu-id="73f5b-120">Example 5: Using piping</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> $managedInstance | Get-AzSqlInstanceKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="73f5b-121">此命令會獲得具有 Id ' ''的 Key Vault https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 鍵。</span><span class="sxs-lookup"><span data-stu-id="73f5b-121">This command gets the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'.</span></span>

## <span data-ttu-id="73f5b-122">參數</span><span class="sxs-lookup"><span data-stu-id="73f5b-122">PARAMETERS</span></span>

### <span data-ttu-id="73f5b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73f5b-123">-DefaultProfile</span></span>
<span data-ttu-id="73f5b-124">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="73f5b-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73f5b-125">-實例</span><span class="sxs-lookup"><span data-stu-id="73f5b-125">-Instance</span></span>
<span data-ttu-id="73f5b-126">實例輸入物件</span><span class="sxs-lookup"><span data-stu-id="73f5b-126">The instance input object</span></span>

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

### <span data-ttu-id="73f5b-127">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="73f5b-127">-InstanceName</span></span>
<span data-ttu-id="73f5b-128">實例名稱</span><span class="sxs-lookup"><span data-stu-id="73f5b-128">The instance name</span></span>

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

### <span data-ttu-id="73f5b-129">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="73f5b-129">-InstanceResourceId</span></span>
<span data-ttu-id="73f5b-130">實例資源識別碼</span><span class="sxs-lookup"><span data-stu-id="73f5b-130">The instance resource id</span></span>

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

### <span data-ttu-id="73f5b-131">-KeyId</span><span class="sxs-lookup"><span data-stu-id="73f5b-131">-KeyId</span></span>
<span data-ttu-id="73f5b-132">AzureKeyVault 金鑰識別碼</span><span class="sxs-lookup"><span data-stu-id="73f5b-132">AzureKeyVault key id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73f5b-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73f5b-133">-ResourceGroupName</span></span>
<span data-ttu-id="73f5b-134">資源組名</span><span class="sxs-lookup"><span data-stu-id="73f5b-134">The Resource Group Name</span></span>

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

### <span data-ttu-id="73f5b-135">-確認</span><span class="sxs-lookup"><span data-stu-id="73f5b-135">-Confirm</span></span>
<span data-ttu-id="73f5b-136">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="73f5b-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73f5b-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73f5b-137">-WhatIf</span></span>
<span data-ttu-id="73f5b-138">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="73f5b-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73f5b-139">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="73f5b-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73f5b-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73f5b-140">CommonParameters</span></span>
<span data-ttu-id="73f5b-141">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="73f5b-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73f5b-142">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="73f5b-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73f5b-143">輸入</span><span class="sxs-lookup"><span data-stu-id="73f5b-143">INPUTS</span></span>

### <span data-ttu-id="73f5b-144">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="73f5b-144">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="73f5b-145">System.String</span><span class="sxs-lookup"><span data-stu-id="73f5b-145">System.String</span></span>

## <span data-ttu-id="73f5b-146">輸出</span><span class="sxs-lookup"><span data-stu-id="73f5b-146">OUTPUTS</span></span>

### <span data-ttu-id="73f5b-147">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="73f5b-147">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceKeyVaultKeyModel</span></span>

## <span data-ttu-id="73f5b-148">筆記</span><span class="sxs-lookup"><span data-stu-id="73f5b-148">NOTES</span></span>

## <span data-ttu-id="73f5b-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="73f5b-149">RELATED LINKS</span></span>
