---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/Get-AzSqlInstanceTransparentDataEncryptionProtector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceTransparentDataEncryptionProtector.md
ms.openlocfilehash: 98538ba503b1fa31ae4c14897d56b0e0b9daffbc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914281"
---
# <span data-ttu-id="177bd-101">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="177bd-101">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="177bd-102">簡介</span><span class="sxs-lookup"><span data-stu-id="177bd-102">SYNOPSIS</span></span>
<span data-ttu-id="177bd-103">為 SQL 受管理實例 (TDE) 套用透明資料加密功能。</span><span class="sxs-lookup"><span data-stu-id="177bd-103">Gets the Transparent Data Encryption (TDE) protector for a SQL managed instance.</span></span>

## <span data-ttu-id="177bd-104">語法</span><span class="sxs-lookup"><span data-stu-id="177bd-104">SYNTAX</span></span>

### <span data-ttu-id="177bd-105">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="177bd-105">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet (Default)</span></span>
```
Get-AzSqlInstanceTransparentDataEncryptionProtector [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="177bd-106">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="177bd-106">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorInputObjectParameterSet</span></span>
```
Get-AzSqlInstanceTransparentDataEncryptionProtector [-Instance] <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="177bd-107">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="177bd-107">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorResourceIdParameterSet</span></span>
```
Get-AzSqlInstanceTransparentDataEncryptionProtector [-InstanceResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="177bd-108">描述</span><span class="sxs-lookup"><span data-stu-id="177bd-108">DESCRIPTION</span></span>
<span data-ttu-id="177bd-109">此Get-AzSqlInstanceTransparentDataEncryptionProtector Cmdlet 會為指定的 SQL 受管理實例獲得 TDE 小程式。</span><span class="sxs-lookup"><span data-stu-id="177bd-109">The Get-AzSqlInstanceTransparentDataEncryptionProtector cmdlet gets the TDE protector for the specified SQL managed instance.</span></span>

## <span data-ttu-id="177bd-110">例子</span><span class="sxs-lookup"><span data-stu-id="177bd-110">EXAMPLES</span></span>

### <span data-ttu-id="177bd-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="177bd-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlInstanceTransparentDataEncryptionProtector -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="177bd-112">此命令會針對名為 ContosoResourceGroup 的資源群組中名為 ContosoManagedInstanceName 的受管理實例，獲得 TDE 物件。</span><span class="sxs-lookup"><span data-stu-id="177bd-112">This command gets the TDE protector for the managed instance named ContosoManagedInstanceName in resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="177bd-113">範例 2：使用受管理的實例物件</span><span class="sxs-lookup"><span data-stu-id="177bd-113">Example 2: Using managed instance object</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Get-AzSqlInstanceTransparentDataEncryptionProtector -Instance $managedInstance 'ContosoManagedInstanceName'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="177bd-114">此命令會針對名為 ContosoResourceGroup 的資源群組中名為 ContosoManagedInstanceName 的受管理實例，獲得 TDE 物件。</span><span class="sxs-lookup"><span data-stu-id="177bd-114">This command gets the TDE protector for the managed instance named ContosoManagedInstanceName in resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="177bd-115">範例 3：使用受管理的實例資源識別碼</span><span class="sxs-lookup"><span data-stu-id="177bd-115">Example 3: Using managed instance resource id</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Get-AzSqlInstanceTransparentDataEncryptionProtector -InstanceResourceId $managedInstance.ResourceId

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="177bd-116">此命令會針對名為 ContosoResourceGroup 的資源群組中名為 ContosoManagedInstanceName 的受管理實例，獲得 TDE 物件。</span><span class="sxs-lookup"><span data-stu-id="177bd-116">This command gets the TDE protector for the managed instance named ContosoManagedInstanceName in resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="177bd-117">範例 4：使用管線</span><span class="sxs-lookup"><span data-stu-id="177bd-117">Example 4: Using piping</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> $managedInstance | Get-AzSqlInstanceTransparentDataEncryptionProtector

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="177bd-118">此命令會針對名為 ContosoResourceGroup 的資源群組中名為 ContosoManagedInstanceName 的受管理實例，獲得 TDE 物件。</span><span class="sxs-lookup"><span data-stu-id="177bd-118">This command gets the TDE protector for the managed instance named ContosoManagedInstanceName in resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="177bd-119">參數</span><span class="sxs-lookup"><span data-stu-id="177bd-119">PARAMETERS</span></span>

### <span data-ttu-id="177bd-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="177bd-120">-DefaultProfile</span></span>
<span data-ttu-id="177bd-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="177bd-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="177bd-122">-實例</span><span class="sxs-lookup"><span data-stu-id="177bd-122">-Instance</span></span>
<span data-ttu-id="177bd-123">實例輸入物件</span><span class="sxs-lookup"><span data-stu-id="177bd-123">The instance input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorInputObjectParameterSet
Aliases: InputObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="177bd-124">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="177bd-124">-InstanceName</span></span>
<span data-ttu-id="177bd-125">實例名稱</span><span class="sxs-lookup"><span data-stu-id="177bd-125">The instance name</span></span>

```yaml
Type: System.String
Parameter Sets: AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="177bd-126">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="177bd-126">-InstanceResourceId</span></span>
<span data-ttu-id="177bd-127">實例資源識別碼</span><span class="sxs-lookup"><span data-stu-id="177bd-127">The instance resource id</span></span>

```yaml
Type: System.String
Parameter Sets: AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorResourceIdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="177bd-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="177bd-128">-ResourceGroupName</span></span>
<span data-ttu-id="177bd-129">資源組名</span><span class="sxs-lookup"><span data-stu-id="177bd-129">The Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="177bd-130">-確認</span><span class="sxs-lookup"><span data-stu-id="177bd-130">-Confirm</span></span>
<span data-ttu-id="177bd-131">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="177bd-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="177bd-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="177bd-132">-WhatIf</span></span>
<span data-ttu-id="177bd-133">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="177bd-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="177bd-134">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="177bd-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="177bd-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="177bd-135">CommonParameters</span></span>
<span data-ttu-id="177bd-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="177bd-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="177bd-137">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="177bd-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="177bd-138">輸入</span><span class="sxs-lookup"><span data-stu-id="177bd-138">INPUTS</span></span>

### <span data-ttu-id="177bd-139">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="177bd-139">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="177bd-140">System.String</span><span class="sxs-lookup"><span data-stu-id="177bd-140">System.String</span></span>

## <span data-ttu-id="177bd-141">輸出</span><span class="sxs-lookup"><span data-stu-id="177bd-141">OUTPUTS</span></span>

### <span data-ttu-id="177bd-142">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceTransparentDataEncryptionProtectorModel</span><span class="sxs-lookup"><span data-stu-id="177bd-142">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceTransparentDataEncryptionProtectorModel</span></span>

## <span data-ttu-id="177bd-143">筆記</span><span class="sxs-lookup"><span data-stu-id="177bd-143">NOTES</span></span>

## <span data-ttu-id="177bd-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="177bd-144">RELATED LINKS</span></span>
