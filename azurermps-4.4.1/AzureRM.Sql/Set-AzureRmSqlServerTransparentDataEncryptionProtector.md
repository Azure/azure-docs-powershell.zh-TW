---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerTransparentDataEncryptionProtector.md
ms.openlocfilehash: b13a09a018ff85a48dd2baf3cf8837950a325cfc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626473"
---
# <span data-ttu-id="17e0d-101">Set-AzureRmSqlServerTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="17e0d-101">Set-AzureRmSqlServerTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="17e0d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="17e0d-102">SYNOPSIS</span></span>
<span data-ttu-id="17e0d-103">針對 SQL server 設定透明的資料加密 (TDE) 保護程式。</span><span class="sxs-lookup"><span data-stu-id="17e0d-103">Sets the Transparent Data Encryption (TDE) protector for a SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="17e0d-104">句法</span><span class="sxs-lookup"><span data-stu-id="17e0d-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerTransparentDataEncryptionProtector [-Type] <EncryptionProtectorType> [[-KeyId] <String>]
 [-Force] [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17e0d-105">說明</span><span class="sxs-lookup"><span data-stu-id="17e0d-105">DESCRIPTION</span></span>
<span data-ttu-id="17e0d-106">Set-AzureRmSqlServerTransparentDataEncryptionProtector Cmdlet 會設定 SQL server 的 TDE 保護程式。</span><span class="sxs-lookup"><span data-stu-id="17e0d-106">The Set-AzureRmSqlServerTransparentDataEncryptionProtector cmdlet sets the TDE protector for a SQL server.</span></span>
<span data-ttu-id="17e0d-107">變更 TDE 保護器類型將會旋轉保護器。</span><span class="sxs-lookup"><span data-stu-id="17e0d-107">Changing the TDE protector type will rotate the protector.</span></span>

## <span data-ttu-id="17e0d-108">示例</span><span class="sxs-lookup"><span data-stu-id="17e0d-108">EXAMPLES</span></span>

### <span data-ttu-id="17e0d-109">--------------------------範例1：將透明的資料加密 (TDE) 保護器類型設定為 ServiceManaged--------------------------</span><span class="sxs-lookup"><span data-stu-id="17e0d-109">--------------------------  Example 1: Set the Transparent Data Encryption (TDE) protector type to ServiceManaged  --------------------------</span></span>
```
PS C:\> Set-AzureRmSqlServerTransparentDataEncryptionProtector -Type ServiceManaged -ServerName 'ContosoServer' -ResourceGroup 'ContosoResourceGroup'
```

<span data-ttu-id="17e0d-110">這個命令會將伺服器的 TDE 保護者類型更新為 [服務管理]。</span><span class="sxs-lookup"><span data-stu-id="17e0d-110">This command updates a server's TDE protector type to Service Managed.</span></span>

<span data-ttu-id="17e0d-111">ResourceGroupName ServerName 類型 ServerKeyVaultKeyName</span><span class="sxs-lookup"><span data-stu-id="17e0d-111">ResourceGroupName ServerName                   Type ServerKeyVaultKeyName</span></span>
----------------- ----------                   ---- ---------------------
<span data-ttu-id="17e0d-112">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span><span class="sxs-lookup"><span data-stu-id="17e0d-112">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span></span>

### <span data-ttu-id="17e0d-113">--------------------------範例2：將透明的資料加密保護器類型設定為 Azure 金鑰保存庫--------------------------</span><span class="sxs-lookup"><span data-stu-id="17e0d-113">--------------------------  Example 2: Set the Transparent Data Encryption protector type to Azure Key Vault  --------------------------</span></span>
```
PS C:\> Set-AzureRmSqlServerTransparentDataEncryptionProtector -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroup 'ContosoResourceGroup'
```

<span data-ttu-id="17e0d-114">這個命令會補救伺服器，以使用 Id 為 "" 的伺服器金鑰保存庫金鑰 https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 作為 TDE 保護器。</span><span class="sxs-lookup"><span data-stu-id="17e0d-114">This command updates a server to use the Server Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>

<span data-ttu-id="17e0d-115">ResourceGroupName ServerName 類型 ServerKeyVaultKeyName</span><span class="sxs-lookup"><span data-stu-id="17e0d-115">ResourceGroupName ServerName                   Type ServerKeyVaultKeyName</span></span>
----------------- ----------                   ---- ---------------------
<span data-ttu-id="17e0d-116">ContosoResourceGroup ContosoServer AzureKeyVault contoso_contosokey_01234567890123456789012345678901</span><span class="sxs-lookup"><span data-stu-id="17e0d-116">ContosoResourceGroup ContosoServer AzureKeyVault contoso_contosokey_01234567890123456789012345678901</span></span>

## <span data-ttu-id="17e0d-117">參數</span><span class="sxs-lookup"><span data-stu-id="17e0d-117">PARAMETERS</span></span>

### <span data-ttu-id="17e0d-118">-Force</span><span class="sxs-lookup"><span data-stu-id="17e0d-118">-Force</span></span>
<span data-ttu-id="17e0d-119">略過確認訊息以執行動作</span><span class="sxs-lookup"><span data-stu-id="17e0d-119">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="17e0d-120">-KeyId</span><span class="sxs-lookup"><span data-stu-id="17e0d-120">-KeyId</span></span>
<span data-ttu-id="17e0d-121">Azure 金鑰保存庫 KeyId。</span><span class="sxs-lookup"><span data-stu-id="17e0d-121">The Azure Key Vault KeyId.</span></span>

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

### <span data-ttu-id="17e0d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17e0d-122">-ResourceGroupName</span></span>
<span data-ttu-id="17e0d-123">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="17e0d-123">The name of the resource group</span></span>

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

### <span data-ttu-id="17e0d-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="17e0d-124">-ServerName</span></span>
<span data-ttu-id="17e0d-125">Azure Sql Server 名稱。</span><span class="sxs-lookup"><span data-stu-id="17e0d-125">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="17e0d-126">-類型</span><span class="sxs-lookup"><span data-stu-id="17e0d-126">-Type</span></span>
<span data-ttu-id="17e0d-127">Azure Sql Database TDE 保護器類型。</span><span class="sxs-lookup"><span data-stu-id="17e0d-127">The Azure Sql Database TDE protector type.</span></span>

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

### <span data-ttu-id="17e0d-128">-確認</span><span class="sxs-lookup"><span data-stu-id="17e0d-128">-Confirm</span></span>
<span data-ttu-id="17e0d-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="17e0d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17e0d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17e0d-130">-WhatIf</span></span>
<span data-ttu-id="17e0d-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="17e0d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17e0d-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="17e0d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17e0d-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17e0d-133">-DefaultProfile</span></span>
<span data-ttu-id="17e0d-134">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="17e0d-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17e0d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17e0d-135">CommonParameters</span></span>
<span data-ttu-id="17e0d-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="17e0d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17e0d-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="17e0d-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17e0d-138">輸入</span><span class="sxs-lookup"><span data-stu-id="17e0d-138">INPUTS</span></span>

### <span data-ttu-id="17e0d-139">EncryptionProtectorType 中的 [TransparentDataEncryption]</span><span class="sxs-lookup"><span data-stu-id="17e0d-139">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.EncryptionProtectorType</span></span>
<span data-ttu-id="17e0d-140">System.object</span><span class="sxs-lookup"><span data-stu-id="17e0d-140">System.String</span></span>

## <span data-ttu-id="17e0d-141">輸出</span><span class="sxs-lookup"><span data-stu-id="17e0d-141">OUTPUTS</span></span>

### <span data-ttu-id="17e0d-142">System.object</span><span class="sxs-lookup"><span data-stu-id="17e0d-142">System.Object</span></span>

## <span data-ttu-id="17e0d-143">筆記</span><span class="sxs-lookup"><span data-stu-id="17e0d-143">NOTES</span></span>

## <span data-ttu-id="17e0d-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="17e0d-144">RELATED LINKS</span></span>

[<span data-ttu-id="17e0d-145">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="17e0d-145">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
