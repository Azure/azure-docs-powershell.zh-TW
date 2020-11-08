---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlserverkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerKeyVaultKey.md
ms.openlocfilehash: 696f7bd0334039691301f8a4399362b9383ab2db
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94137966"
---
# <span data-ttu-id="30dac-101">Remove-AzSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="30dac-101">Remove-AzSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="30dac-102">摘要</span><span class="sxs-lookup"><span data-stu-id="30dac-102">SYNOPSIS</span></span>
<span data-ttu-id="30dac-103">從 SQL server 移除金鑰保存庫金鑰。</span><span class="sxs-lookup"><span data-stu-id="30dac-103">Removes a Key Vault key from a SQL server.</span></span>

## <span data-ttu-id="30dac-104">句法</span><span class="sxs-lookup"><span data-stu-id="30dac-104">SYNTAX</span></span>

```
Remove-AzSqlServerKeyVaultKey [-KeyId] <String> [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30dac-105">說明</span><span class="sxs-lookup"><span data-stu-id="30dac-105">DESCRIPTION</span></span>
<span data-ttu-id="30dac-106">Remove-AzSqlServerKeyVaultKey Cmdlet 會從指定的 SQL server 中移除金鑰保存庫金鑰。</span><span class="sxs-lookup"><span data-stu-id="30dac-106">The Remove-AzSqlServerKeyVaultKey cmdlet removes the Key Vault key from the specified SQL server.</span></span>
<span data-ttu-id="30dac-107">請注意，不會變更 SQL server 對金鑰電子倉庫的許可權。</span><span class="sxs-lookup"><span data-stu-id="30dac-107">Note that the SQL server's permissions to the key's vault are not changed.</span></span>
<span data-ttu-id="30dac-108">若要變更許可權，請使用 [設定-AzKeyVaultAccessPolicy]。</span><span class="sxs-lookup"><span data-stu-id="30dac-108">To change permissions, use Set-AzKeyVaultAccessPolicy.</span></span>
<span data-ttu-id="30dac-109">請注意，這個 Cmdlet 不會變更金鑰保存庫。</span><span class="sxs-lookup"><span data-stu-id="30dac-109">Note that this cmdlet makes no changes to Key Vault.</span></span>
<span data-ttu-id="30dac-110">若要從 [主要電子倉庫] 移除金鑰，請使用 [移除-AzKeyVaultKey]。</span><span class="sxs-lookup"><span data-stu-id="30dac-110">To remove a key from Key Vault, use Remove-AzKeyVaultKey.</span></span>

## <span data-ttu-id="30dac-111">示例</span><span class="sxs-lookup"><span data-stu-id="30dac-111">EXAMPLES</span></span>

### <span data-ttu-id="30dac-112">範例1：移除金鑰保存庫金鑰</span><span class="sxs-lookup"><span data-stu-id="30dac-112">Example 1: Remove a Key Vault key</span></span>
```
PS C:\> Remove-AzSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="30dac-113">這個命令會從指定的伺服器移除 Id 為 '」的主要保存庫金鑰 https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 。</span><span class="sxs-lookup"><span data-stu-id="30dac-113">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified server.</span></span>
<span data-ttu-id="30dac-114">ResourceGroupName： ContosoResourceGroup ServerName： ContosoServer ServerKeyName： contoso_contosokey_01234567890123456789012345678901 類型： AzureKeyVault Uri： https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 指紋： 1122334455667788990011223344556677889900 CreationDate： 1/1/2017 12:00:00 AM</span><span class="sxs-lookup"><span data-stu-id="30dac-114">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

## <span data-ttu-id="30dac-115">參數</span><span class="sxs-lookup"><span data-stu-id="30dac-115">PARAMETERS</span></span>

### <span data-ttu-id="30dac-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="30dac-116">-AsJob</span></span>
<span data-ttu-id="30dac-117">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="30dac-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="30dac-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30dac-118">-DefaultProfile</span></span>
<span data-ttu-id="30dac-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="30dac-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="30dac-120">-KeyId</span><span class="sxs-lookup"><span data-stu-id="30dac-120">-KeyId</span></span>
<span data-ttu-id="30dac-121">Azure 金鑰保存庫 KeyId。</span><span class="sxs-lookup"><span data-stu-id="30dac-121">The Azure Key Vault KeyId.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30dac-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30dac-122">-ResourceGroupName</span></span>
<span data-ttu-id="30dac-123">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="30dac-123">The name of the resource group</span></span>

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

### <span data-ttu-id="30dac-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="30dac-124">-ServerName</span></span>
<span data-ttu-id="30dac-125">Azure Sql Server 名稱。</span><span class="sxs-lookup"><span data-stu-id="30dac-125">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="30dac-126">-確認</span><span class="sxs-lookup"><span data-stu-id="30dac-126">-Confirm</span></span>
<span data-ttu-id="30dac-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="30dac-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30dac-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30dac-128">-WhatIf</span></span>
<span data-ttu-id="30dac-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="30dac-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30dac-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="30dac-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30dac-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30dac-131">CommonParameters</span></span>
<span data-ttu-id="30dac-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="30dac-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30dac-133">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="30dac-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30dac-134">輸入</span><span class="sxs-lookup"><span data-stu-id="30dac-134">INPUTS</span></span>

### <span data-ttu-id="30dac-135">System.object</span><span class="sxs-lookup"><span data-stu-id="30dac-135">System.String</span></span>

## <span data-ttu-id="30dac-136">輸出</span><span class="sxs-lookup"><span data-stu-id="30dac-136">OUTPUTS</span></span>

### <span data-ttu-id="30dac-137">AzureSqlServerKeyVaultKeyModel 中的 [ServerKeyVaultKey]</span><span class="sxs-lookup"><span data-stu-id="30dac-137">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span></span>

## <span data-ttu-id="30dac-138">筆記</span><span class="sxs-lookup"><span data-stu-id="30dac-138">NOTES</span></span>

## <span data-ttu-id="30dac-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="30dac-139">RELATED LINKS</span></span>

[<span data-ttu-id="30dac-140">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="30dac-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
