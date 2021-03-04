---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqlservertransparentdataencryptionprotector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerTransparentDataEncryptionProtector.md
ms.openlocfilehash: 992601b3a6d88c7aa424564189dc8af3efe6464d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905742"
---
# <span data-ttu-id="40509-101">Set-AzSqlServerTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="40509-101">Set-AzSqlServerTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="40509-102">簡介</span><span class="sxs-lookup"><span data-stu-id="40509-102">SYNOPSIS</span></span>
<span data-ttu-id="40509-103">設定 SQL 伺服器的透明資料加密 (TDE) 程式。</span><span class="sxs-lookup"><span data-stu-id="40509-103">Sets the Transparent Data Encryption (TDE) protector for a SQL server.</span></span>

## <span data-ttu-id="40509-104">語法</span><span class="sxs-lookup"><span data-stu-id="40509-104">SYNTAX</span></span>

```
Set-AzSqlServerTransparentDataEncryptionProtector [-Type] <EncryptionProtectorType> [[-KeyId] <String>]
 [-Force] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40509-105">描述</span><span class="sxs-lookup"><span data-stu-id="40509-105">DESCRIPTION</span></span>
<span data-ttu-id="40509-106">Cmdlet Set-AzSqlServerTransparentDataEncryptionProtector設定 SQL 伺服器的 TDE 載入器。</span><span class="sxs-lookup"><span data-stu-id="40509-106">The Set-AzSqlServerTransparentDataEncryptionProtector cmdlet sets the TDE protector for a SQL server.</span></span>
<span data-ttu-id="40509-107">變更 TDE 軸向類型會旋轉轉軸軸。</span><span class="sxs-lookup"><span data-stu-id="40509-107">Changing the TDE protector type will rotate the protector.</span></span>

## <span data-ttu-id="40509-108">例子</span><span class="sxs-lookup"><span data-stu-id="40509-108">EXAMPLES</span></span>

### <span data-ttu-id="40509-109">範例 1：將透明資料加密 (TDE) 類型設定為 ServiceManaged</span><span class="sxs-lookup"><span data-stu-id="40509-109">Example 1: Set the Transparent Data Encryption (TDE) protector type to ServiceManaged</span></span>
```
PS C:\> Set-AzSqlServerTransparentDataEncryptionProtector -Type ServiceManaged -ServerName 'ContosoServer' -ResourceGroup 'ContosoResourceGroup'
```

<span data-ttu-id="40509-110">此命令會補救伺服器的 TDE 用戶端類型至服務管理。</span><span class="sxs-lookup"><span data-stu-id="40509-110">This command updates a server's TDE protector type to Service Managed.</span></span>
<span data-ttu-id="40509-111">ResourceGroupName ServerName Type ServerKeyVaultKeyName</span><span class="sxs-lookup"><span data-stu-id="40509-111">ResourceGroupName ServerName                   Type ServerKeyVaultKeyName</span></span>
----------------- ----------                   ---- ---------------------
<span data-ttu-id="40509-112">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span><span class="sxs-lookup"><span data-stu-id="40509-112">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span></span>

### <span data-ttu-id="40509-113">範例 2：將透明資料加密機制類型設定為 Azure 金鑰庫</span><span class="sxs-lookup"><span data-stu-id="40509-113">Example 2: Set the Transparent Data Encryption protector type to Azure Key Vault</span></span>
```
PS C:\> Set-AzSqlServerTransparentDataEncryptionProtector -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroup 'ContosoResourceGroup'
```

<span data-ttu-id="40509-114">此命令會補救伺服器，以使用具有 Id ' '的 Server Key Vault 鍵 https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 做為 TDE 保護程式。</span><span class="sxs-lookup"><span data-stu-id="40509-114">This command updates a server to use the Server Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>
<span data-ttu-id="40509-115">ResourceGroupName ServerName Type ServerKeyVaultKeyName</span><span class="sxs-lookup"><span data-stu-id="40509-115">ResourceGroupName ServerName                   Type ServerKeyVaultKeyName</span></span>
----------------- ----------                   ---- ---------------------
<span data-ttu-id="40509-116">ContosoResourceGroup ContosoServer AzureKeyVault contoso_contosokey_01234567890123456789012345678901</span><span class="sxs-lookup"><span data-stu-id="40509-116">ContosoResourceGroup ContosoServer AzureKeyVault contoso_contosokey_01234567890123456789012345678901</span></span>

## <span data-ttu-id="40509-117">參數</span><span class="sxs-lookup"><span data-stu-id="40509-117">PARAMETERS</span></span>

### <span data-ttu-id="40509-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="40509-118">-AsJob</span></span>
<span data-ttu-id="40509-119">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="40509-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="40509-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40509-120">-DefaultProfile</span></span>
<span data-ttu-id="40509-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="40509-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="40509-122">-強制</span><span class="sxs-lookup"><span data-stu-id="40509-122">-Force</span></span>
<span data-ttu-id="40509-123">跳過執行動作的確認訊息</span><span class="sxs-lookup"><span data-stu-id="40509-123">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="40509-124">-KeyId</span><span class="sxs-lookup"><span data-stu-id="40509-124">-KeyId</span></span>
<span data-ttu-id="40509-125">Azure 金鑰庫 KeyId。</span><span class="sxs-lookup"><span data-stu-id="40509-125">The Azure Key Vault KeyId.</span></span>

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

### <span data-ttu-id="40509-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40509-126">-ResourceGroupName</span></span>
<span data-ttu-id="40509-127">資源組的名稱</span><span class="sxs-lookup"><span data-stu-id="40509-127">The name of the resource group</span></span>

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

### <span data-ttu-id="40509-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="40509-128">-ServerName</span></span>
<span data-ttu-id="40509-129">Azure Sql Server 名稱。</span><span class="sxs-lookup"><span data-stu-id="40509-129">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="40509-130">-類型</span><span class="sxs-lookup"><span data-stu-id="40509-130">-Type</span></span>
<span data-ttu-id="40509-131">Azure Sql Database TDE 載入數值型別。</span><span class="sxs-lookup"><span data-stu-id="40509-131">The Azure Sql Database TDE protector type.</span></span>

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

### <span data-ttu-id="40509-132">-確認</span><span class="sxs-lookup"><span data-stu-id="40509-132">-Confirm</span></span>
<span data-ttu-id="40509-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="40509-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40509-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40509-134">-WhatIf</span></span>
<span data-ttu-id="40509-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="40509-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40509-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="40509-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40509-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40509-137">CommonParameters</span></span>
<span data-ttu-id="40509-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="40509-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40509-139">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="40509-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40509-140">輸入</span><span class="sxs-lookup"><span data-stu-id="40509-140">INPUTS</span></span>

### <span data-ttu-id="40509-141">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.EncryptionProtectorType</span><span class="sxs-lookup"><span data-stu-id="40509-141">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.EncryptionProtectorType</span></span>

### <span data-ttu-id="40509-142">System.String</span><span class="sxs-lookup"><span data-stu-id="40509-142">System.String</span></span>

## <span data-ttu-id="40509-143">輸出</span><span class="sxs-lookup"><span data-stu-id="40509-143">OUTPUTS</span></span>

### <span data-ttu-id="40509-144">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlServerTransparentDataEncryptionProtectorModel</span><span class="sxs-lookup"><span data-stu-id="40509-144">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlServerTransparentDataEncryptionProtectorModel</span></span>

## <span data-ttu-id="40509-145">筆記</span><span class="sxs-lookup"><span data-stu-id="40509-145">NOTES</span></span>

## <span data-ttu-id="40509-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="40509-146">RELATED LINKS</span></span>

[<span data-ttu-id="40509-147">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="40509-147">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
