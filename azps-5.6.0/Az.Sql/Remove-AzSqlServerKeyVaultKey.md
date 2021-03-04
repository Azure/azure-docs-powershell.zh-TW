---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqlserverkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerKeyVaultKey.md
ms.openlocfilehash: 5b394909df0469c37a0217b3eb861ce4a1146e60
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905758"
---
# <span data-ttu-id="7a1bf-101">Remove-AzSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="7a1bf-101">Remove-AzSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="7a1bf-102">簡介</span><span class="sxs-lookup"><span data-stu-id="7a1bf-102">SYNOPSIS</span></span>
<span data-ttu-id="7a1bf-103">從 SQL 伺服器移除金鑰庫金鑰。</span><span class="sxs-lookup"><span data-stu-id="7a1bf-103">Removes a Key Vault key from a SQL server.</span></span>

## <span data-ttu-id="7a1bf-104">語法</span><span class="sxs-lookup"><span data-stu-id="7a1bf-104">SYNTAX</span></span>

```
Remove-AzSqlServerKeyVaultKey [-KeyId] <String> [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a1bf-105">描述</span><span class="sxs-lookup"><span data-stu-id="7a1bf-105">DESCRIPTION</span></span>
<span data-ttu-id="7a1bf-106">此Remove-AzSqlServerKeyVaultKey Cmdlet 會從指定的 SQL 伺服器移除 Key Vault 鍵。</span><span class="sxs-lookup"><span data-stu-id="7a1bf-106">The Remove-AzSqlServerKeyVaultKey cmdlet removes the Key Vault key from the specified SQL server.</span></span>
<span data-ttu-id="7a1bf-107">請注意，SQL 伺服器對金鑰庫的許可權不會變更。</span><span class="sxs-lookup"><span data-stu-id="7a1bf-107">Note that the SQL server's permissions to the key's vault are not changed.</span></span>
<span data-ttu-id="7a1bf-108">若要變更許可權，請使用 Set-AzKeyVaultAccessPolicy。</span><span class="sxs-lookup"><span data-stu-id="7a1bf-108">To change permissions, use Set-AzKeyVaultAccessPolicy.</span></span>
<span data-ttu-id="7a1bf-109">請注意，此 Cmdlet 不會變更金鑰保存庫。</span><span class="sxs-lookup"><span data-stu-id="7a1bf-109">Note that this cmdlet makes no changes to Key Vault.</span></span>
<span data-ttu-id="7a1bf-110">若要從 Key Vault 移除金鑰，請使用 Remove-AzKeyVaultKey。</span><span class="sxs-lookup"><span data-stu-id="7a1bf-110">To remove a key from Key Vault, use Remove-AzKeyVaultKey.</span></span>

## <span data-ttu-id="7a1bf-111">例子</span><span class="sxs-lookup"><span data-stu-id="7a1bf-111">EXAMPLES</span></span>

### <span data-ttu-id="7a1bf-112">範例 1：移除金鑰庫金鑰</span><span class="sxs-lookup"><span data-stu-id="7a1bf-112">Example 1: Remove a Key Vault key</span></span>
```
PS C:\> Remove-AzSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="7a1bf-113">此命令會從指定的伺服器移除具有 Id ' '的 Key Vault https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 鍵。</span><span class="sxs-lookup"><span data-stu-id="7a1bf-113">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified server.</span></span>
<span data-ttu-id="7a1bf-114">ResourceGroupName ： ContosoResourceGroup ServerName ： ContosoServer ServerKeyName ： contoso_contosokey_01234567890123456789012345678901 Type ： AzureKeyVault Uri ： https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint ： 112233455677899001122334455667788900 CreationDate ： 1/1/2017 12：00：00 AM</span><span class="sxs-lookup"><span data-stu-id="7a1bf-114">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

## <span data-ttu-id="7a1bf-115">參數</span><span class="sxs-lookup"><span data-stu-id="7a1bf-115">PARAMETERS</span></span>

### <span data-ttu-id="7a1bf-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7a1bf-116">-AsJob</span></span>
<span data-ttu-id="7a1bf-117">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="7a1bf-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7a1bf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a1bf-118">-DefaultProfile</span></span>
<span data-ttu-id="7a1bf-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="7a1bf-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7a1bf-120">-KeyId</span><span class="sxs-lookup"><span data-stu-id="7a1bf-120">-KeyId</span></span>
<span data-ttu-id="7a1bf-121">Azure 金鑰庫 KeyId。</span><span class="sxs-lookup"><span data-stu-id="7a1bf-121">The Azure Key Vault KeyId.</span></span>

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

### <span data-ttu-id="7a1bf-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a1bf-122">-ResourceGroupName</span></span>
<span data-ttu-id="7a1bf-123">資源組的名稱</span><span class="sxs-lookup"><span data-stu-id="7a1bf-123">The name of the resource group</span></span>

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

### <span data-ttu-id="7a1bf-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7a1bf-124">-ServerName</span></span>
<span data-ttu-id="7a1bf-125">Azure Sql Server 名稱。</span><span class="sxs-lookup"><span data-stu-id="7a1bf-125">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="7a1bf-126">-確認</span><span class="sxs-lookup"><span data-stu-id="7a1bf-126">-Confirm</span></span>
<span data-ttu-id="7a1bf-127">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="7a1bf-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a1bf-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a1bf-128">-WhatIf</span></span>
<span data-ttu-id="7a1bf-129">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7a1bf-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a1bf-130">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7a1bf-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a1bf-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a1bf-131">CommonParameters</span></span>
<span data-ttu-id="7a1bf-132">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="7a1bf-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a1bf-133">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7a1bf-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a1bf-134">輸入</span><span class="sxs-lookup"><span data-stu-id="7a1bf-134">INPUTS</span></span>

### <span data-ttu-id="7a1bf-135">System.String</span><span class="sxs-lookup"><span data-stu-id="7a1bf-135">System.String</span></span>

## <span data-ttu-id="7a1bf-136">輸出</span><span class="sxs-lookup"><span data-stu-id="7a1bf-136">OUTPUTS</span></span>

### <span data-ttu-id="7a1bf-137">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="7a1bf-137">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span></span>

## <span data-ttu-id="7a1bf-138">筆記</span><span class="sxs-lookup"><span data-stu-id="7a1bf-138">NOTES</span></span>

## <span data-ttu-id="7a1bf-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="7a1bf-139">RELATED LINKS</span></span>

[<span data-ttu-id="7a1bf-140">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="7a1bf-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
