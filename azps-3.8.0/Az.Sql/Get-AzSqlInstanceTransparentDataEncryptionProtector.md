---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/Get-AzSqlInstanceTransparentDataEncryptionProtector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceTransparentDataEncryptionProtector.md
ms.openlocfilehash: 8307581d1e3627be5cb2ab9fc146327342ced187
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93956527"
---
# <span data-ttu-id="61beb-101">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="61beb-101">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="61beb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="61beb-102">SYNOPSIS</span></span>
<span data-ttu-id="61beb-103">取得 SQL managed 實例的透明資料加密 (TDE) 保護程式。</span><span class="sxs-lookup"><span data-stu-id="61beb-103">Gets the Transparent Data Encryption (TDE) protector for a SQL managed instance.</span></span>

## <span data-ttu-id="61beb-104">句法</span><span class="sxs-lookup"><span data-stu-id="61beb-104">SYNTAX</span></span>

### <span data-ttu-id="61beb-105">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="61beb-105">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet (Default)</span></span>
```
Get-AzSqlInstanceTransparentDataEncryptionProtector [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61beb-106">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="61beb-106">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorInputObjectParameterSet</span></span>
```
Get-AzSqlInstanceTransparentDataEncryptionProtector [-Instance] <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61beb-107">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="61beb-107">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorResourceIdParameterSet</span></span>
```
Get-AzSqlInstanceTransparentDataEncryptionProtector [-InstanceResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61beb-108">說明</span><span class="sxs-lookup"><span data-stu-id="61beb-108">DESCRIPTION</span></span>
<span data-ttu-id="61beb-109">Get-AzSqlInstanceTransparentDataEncryptionProtector Cmdlet 會取得指定的 SQL managed 實例的 TDE 保護程式。</span><span class="sxs-lookup"><span data-stu-id="61beb-109">The Get-AzSqlInstanceTransparentDataEncryptionProtector cmdlet gets the TDE protector for the specified SQL managed instance.</span></span>

## <span data-ttu-id="61beb-110">示例</span><span class="sxs-lookup"><span data-stu-id="61beb-110">EXAMPLES</span></span>

### <span data-ttu-id="61beb-111">範例1</span><span class="sxs-lookup"><span data-stu-id="61beb-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlInstanceTransparentDataEncryptionProtector -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="61beb-112">這個命令會取得名為 ContosoResourceGroup 之資源群組中名為 ContosoManagedInstanceName 之受管理實例的 TDE 保護器。</span><span class="sxs-lookup"><span data-stu-id="61beb-112">This command gets the TDE protector for the managed instance named ContosoManagedInstanceName in resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="61beb-113">範例2：使用 managed 實例物件</span><span class="sxs-lookup"><span data-stu-id="61beb-113">Example 2: Using managed instance object</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Get-AzSqlInstanceTransparentDataEncryptionProtector -Instance $managedInstance 'ContosoManagedInstanceName'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="61beb-114">這個命令會取得名為 ContosoResourceGroup 之資源群組中名為 ContosoManagedInstanceName 之受管理實例的 TDE 保護器。</span><span class="sxs-lookup"><span data-stu-id="61beb-114">This command gets the TDE protector for the managed instance named ContosoManagedInstanceName in resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="61beb-115">範例3：使用 managed 實例資源識別碼</span><span class="sxs-lookup"><span data-stu-id="61beb-115">Example 3: Using managed instance resource id</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Get-AzSqlInstanceTransparentDataEncryptionProtector -InstanceResourceId $managedInstance.ResourceId

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="61beb-116">這個命令會取得名為 ContosoResourceGroup 之資源群組中名為 ContosoManagedInstanceName 之受管理實例的 TDE 保護器。</span><span class="sxs-lookup"><span data-stu-id="61beb-116">This command gets the TDE protector for the managed instance named ContosoManagedInstanceName in resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="61beb-117">範例4：使用管道</span><span class="sxs-lookup"><span data-stu-id="61beb-117">Example 4: Using piping</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> $managedInstance | Get-AzSqlInstanceTransparentDataEncryptionProtector

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="61beb-118">這個命令會取得名為 ContosoResourceGroup 之資源群組中名為 ContosoManagedInstanceName 之受管理實例的 TDE 保護器。</span><span class="sxs-lookup"><span data-stu-id="61beb-118">This command gets the TDE protector for the managed instance named ContosoManagedInstanceName in resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="61beb-119">參數</span><span class="sxs-lookup"><span data-stu-id="61beb-119">PARAMETERS</span></span>

### <span data-ttu-id="61beb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61beb-120">-DefaultProfile</span></span>
<span data-ttu-id="61beb-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="61beb-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61beb-122">-實例</span><span class="sxs-lookup"><span data-stu-id="61beb-122">-Instance</span></span>
<span data-ttu-id="61beb-123">實例輸入物件</span><span class="sxs-lookup"><span data-stu-id="61beb-123">The instance input object</span></span>

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

### <span data-ttu-id="61beb-124">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="61beb-124">-InstanceName</span></span>
<span data-ttu-id="61beb-125">實例名稱</span><span class="sxs-lookup"><span data-stu-id="61beb-125">The instance name</span></span>

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

### <span data-ttu-id="61beb-126">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="61beb-126">-InstanceResourceId</span></span>
<span data-ttu-id="61beb-127">實例資源識別碼</span><span class="sxs-lookup"><span data-stu-id="61beb-127">The instance resource id</span></span>

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

### <span data-ttu-id="61beb-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61beb-128">-ResourceGroupName</span></span>
<span data-ttu-id="61beb-129">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="61beb-129">The Resource Group Name</span></span>

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

### <span data-ttu-id="61beb-130">-確認</span><span class="sxs-lookup"><span data-stu-id="61beb-130">-Confirm</span></span>
<span data-ttu-id="61beb-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="61beb-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61beb-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61beb-132">-WhatIf</span></span>
<span data-ttu-id="61beb-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="61beb-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61beb-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="61beb-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61beb-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61beb-135">CommonParameters</span></span>
<span data-ttu-id="61beb-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="61beb-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61beb-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="61beb-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61beb-138">輸入</span><span class="sxs-lookup"><span data-stu-id="61beb-138">INPUTS</span></span>

### <span data-ttu-id="61beb-139">AzureSqlManagedInstanceModel 中的 [ManagedInstance]</span><span class="sxs-lookup"><span data-stu-id="61beb-139">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="61beb-140">System.object</span><span class="sxs-lookup"><span data-stu-id="61beb-140">System.String</span></span>

## <span data-ttu-id="61beb-141">輸出</span><span class="sxs-lookup"><span data-stu-id="61beb-141">OUTPUTS</span></span>

### <span data-ttu-id="61beb-142">AzureRmSqlManagedInstanceTransparentDataEncryptionProtectorModel 中的 [TransparentDataEncryption]</span><span class="sxs-lookup"><span data-stu-id="61beb-142">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceTransparentDataEncryptionProtectorModel</span></span>

## <span data-ttu-id="61beb-143">筆記</span><span class="sxs-lookup"><span data-stu-id="61beb-143">NOTES</span></span>

## <span data-ttu-id="61beb-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="61beb-144">RELATED LINKS</span></span>
