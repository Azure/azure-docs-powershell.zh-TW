---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/Set-AzSqlInstanceTransparentDataEncryptionProtector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceTransparentDataEncryptionProtector.md
ms.openlocfilehash: 4f3b0bccd8f352d6870899473440b690381bec10
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911278"
---
# <span data-ttu-id="7fba0-101">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="7fba0-101">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="7fba0-102">簡介</span><span class="sxs-lookup"><span data-stu-id="7fba0-102">SYNOPSIS</span></span>
<span data-ttu-id="7fba0-103">設定 SQL 受管理實例 (TDE) 的透明資料加密機制。</span><span class="sxs-lookup"><span data-stu-id="7fba0-103">Sets the Transparent Data Encryption (TDE) protector for a SQL managed instance.</span></span>

## <span data-ttu-id="7fba0-104">語法</span><span class="sxs-lookup"><span data-stu-id="7fba0-104">SYNTAX</span></span>

### <span data-ttu-id="7fba0-105">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="7fba0-105">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet (Default)</span></span>
```
Set-AzSqlInstanceTransparentDataEncryptionProtector [-Type] <EncryptionProtectorType> [[-KeyId] <String>]
 [-Force] [-ResourceGroupName] <String> [-InstanceName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7fba0-106">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7fba0-106">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorInputObjectParameterSet</span></span>
```
Set-AzSqlInstanceTransparentDataEncryptionProtector [-Type] <EncryptionProtectorType> [[-KeyId] <String>]
 [-Force] [-Instance] <AzureSqlManagedInstanceModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7fba0-107">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7fba0-107">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorResourceIdParameterSet</span></span>
```
Set-AzSqlInstanceTransparentDataEncryptionProtector [-Type] <EncryptionProtectorType> [[-KeyId] <String>]
 [-Force] [-InstanceResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7fba0-108">描述</span><span class="sxs-lookup"><span data-stu-id="7fba0-108">DESCRIPTION</span></span>
<span data-ttu-id="7fba0-109">Cmdlet Set-AzSqlInstanceTransparentDataEncryptionProtector設定 SQL 受管理實例的 TDE 小板。</span><span class="sxs-lookup"><span data-stu-id="7fba0-109">The Set-AzSqlInstanceTransparentDataEncryptionProtector cmdlet sets the TDE protector for a SQL managed instance.</span></span> <span data-ttu-id="7fba0-110">變更 TDE 軸向類型會旋轉轉軸軸。</span><span class="sxs-lookup"><span data-stu-id="7fba0-110">Changing the TDE protector type will rotate the protector.</span></span>

## <span data-ttu-id="7fba0-111">例子</span><span class="sxs-lookup"><span data-stu-id="7fba0-111">EXAMPLES</span></span>

### <span data-ttu-id="7fba0-112">範例 1：將透明資料加密 (TDE) 類型設定為 ServiceManaged</span><span class="sxs-lookup"><span data-stu-id="7fba0-112">Example 1: Set the Transparent Data Encryption (TDE) protector type to ServiceManaged</span></span>
```powershell
PS C:\> Set-AzSqlInstanceTransparentDataEncryptionProtector -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName' -Type ServiceManaged

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : ServiceManaged
ManagedInstanceKeyVaultKeyName : ServiceManaged
KeyId                          :
```

<span data-ttu-id="7fba0-113">此命令會更新受管理實例的 TDE 代管類型至服務管理。</span><span class="sxs-lookup"><span data-stu-id="7fba0-113">This command updates a managed instance's TDE protector type to Service Managed.</span></span>

### <span data-ttu-id="7fba0-114">範例 2：將透明資料加密機制類型設定為 Azure 金鑰庫</span><span class="sxs-lookup"><span data-stu-id="7fba0-114">Example 2: Set the Transparent Data Encryption protector type to Azure Key Vault</span></span>
```powershell
PS C:\> Set-AzSqlInstanceTransparentDataEncryptionProtector -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName' -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="7fba0-115">此命令會更新指定的受管理實例，以使用具有 Id ' '的 Managed 實例金鑰庫金鑰 https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 做為 TDE 保護程式。</span><span class="sxs-lookup"><span data-stu-id="7fba0-115">This command updates the specified managed instance to use the Managed instance Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>

### <span data-ttu-id="7fba0-116">範例 3：使用受管理的實例物件，將透明資料加密機制類型設定為 Azure 金鑰庫</span><span class="sxs-lookup"><span data-stu-id="7fba0-116">Example 3: Set the Transparent Data Encryption protector type to Azure Key Vault using managed instance object</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Set-AzSqlInstanceTransparentDataEncryptionProtector -Instance $managedInstance -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="7fba0-117">此命令會更新指定的受管理實例，以使用具有 Id ' '的 Managed 實例金鑰庫金鑰 https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 做為 TDE 保護程式。</span><span class="sxs-lookup"><span data-stu-id="7fba0-117">This command updates the specified managed instance to use the Managed instance Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>

### <span data-ttu-id="7fba0-118">範例 4：使用資源識別碼將透明資料加密機制類型設定為 Azure 金鑰庫</span><span class="sxs-lookup"><span data-stu-id="7fba0-118">Example 4: Set the Transparent Data Encryption protector type to Azure Key Vault using resource id</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Set-AzSqlInstanceTransparentDataEncryptionProtector -InstanceResourceId $managedInstance.ResourceId -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="7fba0-119">此命令會更新指定的受管理實例，以使用具有 Id ' '的 Managed 實例金鑰庫金鑰 https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 做為 TDE 保護程式。</span><span class="sxs-lookup"><span data-stu-id="7fba0-119">This command updates the specified managed instance to use the Managed instance Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>

### <span data-ttu-id="7fba0-120">範例 5：使用管道將透明資料加密加密工具類型設定為 Azure 金鑰庫</span><span class="sxs-lookup"><span data-stu-id="7fba0-120">Example 5: Set the Transparent Data Encryption protector type to Azure Key Vault using piping</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> $managedInstance | Set-AzSqlInstanceTransparentDataEncryptionProtector -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="7fba0-121">此命令會更新指定的受管理實例，以使用具有 Id ' '的 Managed 實例金鑰庫金鑰 https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 做為 TDE 保護程式。</span><span class="sxs-lookup"><span data-stu-id="7fba0-121">This command updates the specified managed instance to use the Managed instance Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>

## <span data-ttu-id="7fba0-122">參數</span><span class="sxs-lookup"><span data-stu-id="7fba0-122">PARAMETERS</span></span>

### <span data-ttu-id="7fba0-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fba0-123">-DefaultProfile</span></span>
<span data-ttu-id="7fba0-124">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="7fba0-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7fba0-125">-強制</span><span class="sxs-lookup"><span data-stu-id="7fba0-125">-Force</span></span>
<span data-ttu-id="7fba0-126">跳過執行動作的確認訊息</span><span class="sxs-lookup"><span data-stu-id="7fba0-126">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="7fba0-127">-實例</span><span class="sxs-lookup"><span data-stu-id="7fba0-127">-Instance</span></span>
<span data-ttu-id="7fba0-128">實例輸入物件</span><span class="sxs-lookup"><span data-stu-id="7fba0-128">The instance input object</span></span>

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

### <span data-ttu-id="7fba0-129">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="7fba0-129">-InstanceName</span></span>
<span data-ttu-id="7fba0-130">實例名稱</span><span class="sxs-lookup"><span data-stu-id="7fba0-130">The instance name</span></span>

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

### <span data-ttu-id="7fba0-131">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="7fba0-131">-InstanceResourceId</span></span>
<span data-ttu-id="7fba0-132">實例資源識別碼</span><span class="sxs-lookup"><span data-stu-id="7fba0-132">The instance resource id</span></span>

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

### <span data-ttu-id="7fba0-133">-KeyId</span><span class="sxs-lookup"><span data-stu-id="7fba0-133">-KeyId</span></span>
<span data-ttu-id="7fba0-134">Azure 金鑰庫 KeyId。</span><span class="sxs-lookup"><span data-stu-id="7fba0-134">The Azure Key Vault KeyId.</span></span>

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

### <span data-ttu-id="7fba0-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7fba0-135">-ResourceGroupName</span></span>
<span data-ttu-id="7fba0-136">資源組名</span><span class="sxs-lookup"><span data-stu-id="7fba0-136">The Resource Group Name</span></span>

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

### <span data-ttu-id="7fba0-137">-類型</span><span class="sxs-lookup"><span data-stu-id="7fba0-137">-Type</span></span>
<span data-ttu-id="7fba0-138">Azure Sql Database 透明資料加密保護程式類型。</span><span class="sxs-lookup"><span data-stu-id="7fba0-138">The Azure Sql Database Transparent Data Encryption Protector type.</span></span>

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

### <span data-ttu-id="7fba0-139">-確認</span><span class="sxs-lookup"><span data-stu-id="7fba0-139">-Confirm</span></span>
<span data-ttu-id="7fba0-140">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="7fba0-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7fba0-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7fba0-141">-WhatIf</span></span>
<span data-ttu-id="7fba0-142">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7fba0-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7fba0-143">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7fba0-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7fba0-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fba0-144">CommonParameters</span></span>
<span data-ttu-id="7fba0-145">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="7fba0-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fba0-146">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7fba0-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fba0-147">輸入</span><span class="sxs-lookup"><span data-stu-id="7fba0-147">INPUTS</span></span>

### <span data-ttu-id="7fba0-148">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="7fba0-148">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="7fba0-149">System.String</span><span class="sxs-lookup"><span data-stu-id="7fba0-149">System.String</span></span>

## <span data-ttu-id="7fba0-150">輸出</span><span class="sxs-lookup"><span data-stu-id="7fba0-150">OUTPUTS</span></span>

### <span data-ttu-id="7fba0-151">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceTransparentDataEncryptionProtectorModel</span><span class="sxs-lookup"><span data-stu-id="7fba0-151">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceTransparentDataEncryptionProtectorModel</span></span>

## <span data-ttu-id="7fba0-152">筆記</span><span class="sxs-lookup"><span data-stu-id="7fba0-152">NOTES</span></span>

## <span data-ttu-id="7fba0-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="7fba0-153">RELATED LINKS</span></span>
