---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlservertransparentdataencryptionprotector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerTransparentDataEncryptionProtector.md
ms.openlocfilehash: b93167e0e0a089595cb45710072c670c1cdb7af0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98434972"
---
# <span data-ttu-id="c53c0-101">Set-AzSqlServerTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="c53c0-101">Set-AzSqlServerTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="c53c0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c53c0-102">SYNOPSIS</span></span>
<span data-ttu-id="c53c0-103">針對 SQL server 設定透明的資料加密 (TDE) 保護程式。</span><span class="sxs-lookup"><span data-stu-id="c53c0-103">Sets the Transparent Data Encryption (TDE) protector for a SQL server.</span></span>

## <span data-ttu-id="c53c0-104">句法</span><span class="sxs-lookup"><span data-stu-id="c53c0-104">SYNTAX</span></span>

```
Set-AzSqlServerTransparentDataEncryptionProtector [-Type] <EncryptionProtectorType> [[-KeyId] <String>]
 [-Force] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c53c0-105">說明</span><span class="sxs-lookup"><span data-stu-id="c53c0-105">DESCRIPTION</span></span>
<span data-ttu-id="c53c0-106">Set-AzSqlServerTransparentDataEncryptionProtector Cmdlet 會設定 SQL server 的 TDE 保護程式。</span><span class="sxs-lookup"><span data-stu-id="c53c0-106">The Set-AzSqlServerTransparentDataEncryptionProtector cmdlet sets the TDE protector for a SQL server.</span></span>
<span data-ttu-id="c53c0-107">變更 TDE 保護器類型將會旋轉保護器。</span><span class="sxs-lookup"><span data-stu-id="c53c0-107">Changing the TDE protector type will rotate the protector.</span></span>

## <span data-ttu-id="c53c0-108">示例</span><span class="sxs-lookup"><span data-stu-id="c53c0-108">EXAMPLES</span></span>

### <span data-ttu-id="c53c0-109">範例1：將透明資料加密 (TDE) 保護器類型設定為 ServiceManaged</span><span class="sxs-lookup"><span data-stu-id="c53c0-109">Example 1: Set the Transparent Data Encryption (TDE) protector type to ServiceManaged</span></span>
```
PS C:\> Set-AzSqlServerTransparentDataEncryptionProtector -Type ServiceManaged -ServerName 'ContosoServer' -ResourceGroup 'ContosoResourceGroup'
```

<span data-ttu-id="c53c0-110">這個命令會將伺服器的 TDE 保護者類型更新為 [服務管理]。</span><span class="sxs-lookup"><span data-stu-id="c53c0-110">This command updates a server's TDE protector type to Service Managed.</span></span>
<span data-ttu-id="c53c0-111">ResourceGroupName ServerName 類型 ServerKeyVaultKeyName</span><span class="sxs-lookup"><span data-stu-id="c53c0-111">ResourceGroupName ServerName                   Type ServerKeyVaultKeyName</span></span>
----------------- ----------                   ---- ---------------------
<span data-ttu-id="c53c0-112">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span><span class="sxs-lookup"><span data-stu-id="c53c0-112">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span></span>

### <span data-ttu-id="c53c0-113">範例2：將透明的資料加密保護器類型設定至 Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="c53c0-113">Example 2: Set the Transparent Data Encryption protector type to Azure Key Vault</span></span>
```
PS C:\> Set-AzSqlServerTransparentDataEncryptionProtector -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroup 'ContosoResourceGroup'
```

<span data-ttu-id="c53c0-114">這個命令會補救伺服器，以使用 Id 為 "" 的伺服器金鑰保存庫金鑰 https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 作為 TDE 保護器。</span><span class="sxs-lookup"><span data-stu-id="c53c0-114">This command updates a server to use the Server Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>
<span data-ttu-id="c53c0-115">ResourceGroupName ServerName 類型 ServerKeyVaultKeyName</span><span class="sxs-lookup"><span data-stu-id="c53c0-115">ResourceGroupName ServerName                   Type ServerKeyVaultKeyName</span></span>
----------------- ----------                   ---- ---------------------
<span data-ttu-id="c53c0-116">ContosoResourceGroup ContosoServer AzureKeyVault contoso_contosokey_01234567890123456789012345678901</span><span class="sxs-lookup"><span data-stu-id="c53c0-116">ContosoResourceGroup ContosoServer AzureKeyVault contoso_contosokey_01234567890123456789012345678901</span></span>

## <span data-ttu-id="c53c0-117">參數</span><span class="sxs-lookup"><span data-stu-id="c53c0-117">PARAMETERS</span></span>

### <span data-ttu-id="c53c0-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c53c0-118">-AsJob</span></span>
<span data-ttu-id="c53c0-119">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c53c0-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c53c0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c53c0-120">-DefaultProfile</span></span>
<span data-ttu-id="c53c0-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="c53c0-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c53c0-122">-Force</span><span class="sxs-lookup"><span data-stu-id="c53c0-122">-Force</span></span>
<span data-ttu-id="c53c0-123">略過確認訊息以執行動作</span><span class="sxs-lookup"><span data-stu-id="c53c0-123">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="c53c0-124">-KeyId</span><span class="sxs-lookup"><span data-stu-id="c53c0-124">-KeyId</span></span>
<span data-ttu-id="c53c0-125">Azure 金鑰保存庫 KeyId。</span><span class="sxs-lookup"><span data-stu-id="c53c0-125">The Azure Key Vault KeyId.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c53c0-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c53c0-126">-ResourceGroupName</span></span>
<span data-ttu-id="c53c0-127">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="c53c0-127">The name of the resource group</span></span>

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

### <span data-ttu-id="c53c0-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c53c0-128">-ServerName</span></span>
<span data-ttu-id="c53c0-129">Azure Sql Server 名稱。</span><span class="sxs-lookup"><span data-stu-id="c53c0-129">The Azure Sql Server name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c53c0-130">-類型</span><span class="sxs-lookup"><span data-stu-id="c53c0-130">-Type</span></span>
<span data-ttu-id="c53c0-131">Azure Sql Database TDE 保護器類型。</span><span class="sxs-lookup"><span data-stu-id="c53c0-131">The Azure Sql Database TDE protector type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.EncryptionProtectorType
Parameter Sets: (All)
Aliases:
Accepted values: AzureKeyVault, ServiceManaged

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c53c0-132">-確認</span><span class="sxs-lookup"><span data-stu-id="c53c0-132">-Confirm</span></span>
<span data-ttu-id="c53c0-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c53c0-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c53c0-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c53c0-134">-WhatIf</span></span>
<span data-ttu-id="c53c0-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c53c0-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c53c0-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c53c0-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c53c0-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c53c0-137">CommonParameters</span></span>
<span data-ttu-id="c53c0-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c53c0-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c53c0-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c53c0-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c53c0-140">輸入</span><span class="sxs-lookup"><span data-stu-id="c53c0-140">INPUTS</span></span>

### <span data-ttu-id="c53c0-141">EncryptionProtectorType 中的 [TransparentDataEncryption]</span><span class="sxs-lookup"><span data-stu-id="c53c0-141">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.EncryptionProtectorType</span></span>

### <span data-ttu-id="c53c0-142">System.object</span><span class="sxs-lookup"><span data-stu-id="c53c0-142">System.String</span></span>

## <span data-ttu-id="c53c0-143">輸出</span><span class="sxs-lookup"><span data-stu-id="c53c0-143">OUTPUTS</span></span>

### <span data-ttu-id="c53c0-144">AzureSqlServerTransparentDataEncryptionProtectorModel 中的 [TransparentDataEncryption]</span><span class="sxs-lookup"><span data-stu-id="c53c0-144">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlServerTransparentDataEncryptionProtectorModel</span></span>

## <span data-ttu-id="c53c0-145">筆記</span><span class="sxs-lookup"><span data-stu-id="c53c0-145">NOTES</span></span>

## <span data-ttu-id="c53c0-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="c53c0-146">RELATED LINKS</span></span>

[<span data-ttu-id="c53c0-147">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="c53c0-147">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
