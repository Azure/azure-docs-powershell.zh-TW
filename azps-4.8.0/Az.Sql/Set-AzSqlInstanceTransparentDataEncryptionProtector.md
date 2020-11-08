---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/Set-AzSqlInstanceTransparentDataEncryptionProtector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceTransparentDataEncryptionProtector.md
ms.openlocfilehash: 15462ea79b5499818d71b145e0faaa35c09baf0b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94129812"
---
# <span data-ttu-id="b51e9-101">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="b51e9-101">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="b51e9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b51e9-102">SYNOPSIS</span></span>
<span data-ttu-id="b51e9-103">針對 SQL managed 實例 (TDE) 保護器設定透明的資料加密。</span><span class="sxs-lookup"><span data-stu-id="b51e9-103">Sets the Transparent Data Encryption (TDE) protector for a SQL managed instance.</span></span>

## <span data-ttu-id="b51e9-104">句法</span><span class="sxs-lookup"><span data-stu-id="b51e9-104">SYNTAX</span></span>

### <span data-ttu-id="b51e9-105">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="b51e9-105">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet (Default)</span></span>
```
Set-AzSqlInstanceTransparentDataEncryptionProtector [-Type] <EncryptionProtectorType> [[-KeyId] <String>]
 [-Force] [-ResourceGroupName] <String> [-InstanceName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b51e9-106">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b51e9-106">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorInputObjectParameterSet</span></span>
```
Set-AzSqlInstanceTransparentDataEncryptionProtector [-Type] <EncryptionProtectorType> [[-KeyId] <String>]
 [-Force] [-Instance] <AzureSqlManagedInstanceModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b51e9-107">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b51e9-107">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorResourceIdParameterSet</span></span>
```
Set-AzSqlInstanceTransparentDataEncryptionProtector [-Type] <EncryptionProtectorType> [[-KeyId] <String>]
 [-Force] [-InstanceResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b51e9-108">說明</span><span class="sxs-lookup"><span data-stu-id="b51e9-108">DESCRIPTION</span></span>
<span data-ttu-id="b51e9-109">Set-AzSqlInstanceTransparentDataEncryptionProtector Cmdlet 會針對 SQL managed 實例設定 TDE 保護程式。</span><span class="sxs-lookup"><span data-stu-id="b51e9-109">The Set-AzSqlInstanceTransparentDataEncryptionProtector cmdlet sets the TDE protector for a SQL managed instance.</span></span> <span data-ttu-id="b51e9-110">變更 TDE 保護器類型將會旋轉保護器。</span><span class="sxs-lookup"><span data-stu-id="b51e9-110">Changing the TDE protector type will rotate the protector.</span></span>

## <span data-ttu-id="b51e9-111">示例</span><span class="sxs-lookup"><span data-stu-id="b51e9-111">EXAMPLES</span></span>

### <span data-ttu-id="b51e9-112">範例1：將透明資料加密 (TDE) 保護器類型設定為 ServiceManaged</span><span class="sxs-lookup"><span data-stu-id="b51e9-112">Example 1: Set the Transparent Data Encryption (TDE) protector type to ServiceManaged</span></span>
```powershell
PS C:\> Set-AzSqlInstanceTransparentDataEncryptionProtector -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName' -Type ServiceManaged

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : ServiceManaged
ManagedInstanceKeyVaultKeyName : ServiceManaged
KeyId                          :
```

<span data-ttu-id="b51e9-113">這個命令會將受管理實例的 TDE 保護器類型更新為 [服務管理]。</span><span class="sxs-lookup"><span data-stu-id="b51e9-113">This command updates a managed instance's TDE protector type to Service Managed.</span></span>

### <span data-ttu-id="b51e9-114">範例2：將透明的資料加密保護器類型設定至 Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="b51e9-114">Example 2: Set the Transparent Data Encryption protector type to Azure Key Vault</span></span>
```powershell
PS C:\> Set-AzSqlInstanceTransparentDataEncryptionProtector -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName' -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="b51e9-115">這個命令會更新指定的受管理實例，以使用受管理的實例金鑰保存庫金鑰，並使用 Id " https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 " 作為 TDE 保護器。</span><span class="sxs-lookup"><span data-stu-id="b51e9-115">This command updates the specified managed instance to use the Managed instance Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>

### <span data-ttu-id="b51e9-116">範例3：使用 managed 實例物件將透明資料加密保護器類型設定為 Azure 金鑰保存庫</span><span class="sxs-lookup"><span data-stu-id="b51e9-116">Example 3: Set the Transparent Data Encryption protector type to Azure Key Vault using managed instance object</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Set-AzSqlInstanceTransparentDataEncryptionProtector -Instance $managedInstance -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="b51e9-117">這個命令會更新指定的受管理實例，以使用受管理的實例金鑰保存庫金鑰，並使用 Id " https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 " 作為 TDE 保護器。</span><span class="sxs-lookup"><span data-stu-id="b51e9-117">This command updates the specified managed instance to use the Managed instance Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>

### <span data-ttu-id="b51e9-118">範例4：使用資源識別碼將透明資料加密保護器類型設定為 Azure 金鑰保存庫</span><span class="sxs-lookup"><span data-stu-id="b51e9-118">Example 4: Set the Transparent Data Encryption protector type to Azure Key Vault using resource id</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Set-AzSqlInstanceTransparentDataEncryptionProtector -InstanceResourceId $managedInstance.ResourceId -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="b51e9-119">這個命令會更新指定的受管理實例，以使用受管理的實例金鑰保存庫金鑰，並使用 Id " https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 " 作為 TDE 保護器。</span><span class="sxs-lookup"><span data-stu-id="b51e9-119">This command updates the specified managed instance to use the Managed instance Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>

### <span data-ttu-id="b51e9-120">範例5：使用管道將透明資料加密保護器類型設定至 Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="b51e9-120">Example 5: Set the Transparent Data Encryption protector type to Azure Key Vault using piping</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> $managedInstance | Set-AzSqlInstanceTransparentDataEncryptionProtector -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="b51e9-121">這個命令會更新指定的受管理實例，以使用受管理的實例金鑰保存庫金鑰，並使用 Id " https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 " 作為 TDE 保護器。</span><span class="sxs-lookup"><span data-stu-id="b51e9-121">This command updates the specified managed instance to use the Managed instance Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>

## <span data-ttu-id="b51e9-122">參數</span><span class="sxs-lookup"><span data-stu-id="b51e9-122">PARAMETERS</span></span>

### <span data-ttu-id="b51e9-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b51e9-123">-DefaultProfile</span></span>
<span data-ttu-id="b51e9-124">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b51e9-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b51e9-125">-Force</span><span class="sxs-lookup"><span data-stu-id="b51e9-125">-Force</span></span>
<span data-ttu-id="b51e9-126">略過確認訊息以執行動作</span><span class="sxs-lookup"><span data-stu-id="b51e9-126">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="b51e9-127">-實例</span><span class="sxs-lookup"><span data-stu-id="b51e9-127">-Instance</span></span>
<span data-ttu-id="b51e9-128">實例輸入物件</span><span class="sxs-lookup"><span data-stu-id="b51e9-128">The instance input object</span></span>

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

### <span data-ttu-id="b51e9-129">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="b51e9-129">-InstanceName</span></span>
<span data-ttu-id="b51e9-130">實例名稱</span><span class="sxs-lookup"><span data-stu-id="b51e9-130">The instance name</span></span>

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

### <span data-ttu-id="b51e9-131">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="b51e9-131">-InstanceResourceId</span></span>
<span data-ttu-id="b51e9-132">實例資源識別碼</span><span class="sxs-lookup"><span data-stu-id="b51e9-132">The instance resource id</span></span>

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

### <span data-ttu-id="b51e9-133">-KeyId</span><span class="sxs-lookup"><span data-stu-id="b51e9-133">-KeyId</span></span>
<span data-ttu-id="b51e9-134">Azure 金鑰保存庫 KeyId。</span><span class="sxs-lookup"><span data-stu-id="b51e9-134">The Azure Key Vault KeyId.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b51e9-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b51e9-135">-ResourceGroupName</span></span>
<span data-ttu-id="b51e9-136">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="b51e9-136">The Resource Group Name</span></span>

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

### <span data-ttu-id="b51e9-137">-類型</span><span class="sxs-lookup"><span data-stu-id="b51e9-137">-Type</span></span>
<span data-ttu-id="b51e9-138">Azure Sql Database 透明資料加密保護器類型。</span><span class="sxs-lookup"><span data-stu-id="b51e9-138">The Azure Sql Database Transparent Data Encryption Protector type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.EncryptionProtectorType
Parameter Sets: (All)
Aliases:
Accepted values: AzureKeyVault, ServiceManaged

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b51e9-139">-確認</span><span class="sxs-lookup"><span data-stu-id="b51e9-139">-Confirm</span></span>
<span data-ttu-id="b51e9-140">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b51e9-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b51e9-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b51e9-141">-WhatIf</span></span>
<span data-ttu-id="b51e9-142">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b51e9-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b51e9-143">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b51e9-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b51e9-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b51e9-144">CommonParameters</span></span>
<span data-ttu-id="b51e9-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b51e9-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b51e9-146">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b51e9-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b51e9-147">輸入</span><span class="sxs-lookup"><span data-stu-id="b51e9-147">INPUTS</span></span>

### <span data-ttu-id="b51e9-148">AzureSqlManagedInstanceModel 中的 [ManagedInstance]</span><span class="sxs-lookup"><span data-stu-id="b51e9-148">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="b51e9-149">System.object</span><span class="sxs-lookup"><span data-stu-id="b51e9-149">System.String</span></span>

## <span data-ttu-id="b51e9-150">輸出</span><span class="sxs-lookup"><span data-stu-id="b51e9-150">OUTPUTS</span></span>

### <span data-ttu-id="b51e9-151">AzureRmSqlManagedInstanceTransparentDataEncryptionProtectorModel 中的 [TransparentDataEncryption]</span><span class="sxs-lookup"><span data-stu-id="b51e9-151">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceTransparentDataEncryptionProtectorModel</span></span>

## <span data-ttu-id="b51e9-152">筆記</span><span class="sxs-lookup"><span data-stu-id="b51e9-152">NOTES</span></span>

## <span data-ttu-id="b51e9-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="b51e9-153">RELATED LINKS</span></span>
