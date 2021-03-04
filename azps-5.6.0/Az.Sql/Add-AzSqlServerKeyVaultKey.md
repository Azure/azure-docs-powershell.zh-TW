---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/add-azsqlserverkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlServerKeyVaultKey.md
ms.openlocfilehash: f354fe8ad1876eb756cdf78378dbf7048e53932d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904290"
---
# <span data-ttu-id="4a09c-101">Add-AzSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="4a09c-101">Add-AzSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="4a09c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4a09c-102">SYNOPSIS</span></span>
<span data-ttu-id="4a09c-103">新增金鑰庫金鑰至 SQL 伺服器。</span><span class="sxs-lookup"><span data-stu-id="4a09c-103">Adds a Key Vault key to a SQL server.</span></span>

## <span data-ttu-id="4a09c-104">語法</span><span class="sxs-lookup"><span data-stu-id="4a09c-104">SYNTAX</span></span>

```
Add-AzSqlServerKeyVaultKey [-KeyId] <String> [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a09c-105">描述</span><span class="sxs-lookup"><span data-stu-id="4a09c-105">DESCRIPTION</span></span>
<span data-ttu-id="4a09c-106">Cmdlet Add-AzSqlServerKeyVaultKey新增金鑰庫金鑰至提供的 SQL 伺服器。</span><span class="sxs-lookup"><span data-stu-id="4a09c-106">The Add-AzSqlServerKeyVaultKey cmdlet adds a Key Vault key to the provided SQL server.</span></span>
<span data-ttu-id="4a09c-107">伺服器必須具有對儲存庫的 'get， wrapKey， unwrapKey' 許可權。</span><span class="sxs-lookup"><span data-stu-id="4a09c-107">The server must have 'get, wrapKey, unwrapKey' permissions to the vault.</span></span>

## <span data-ttu-id="4a09c-108">例子</span><span class="sxs-lookup"><span data-stu-id="4a09c-108">EXAMPLES</span></span>

### <span data-ttu-id="4a09c-109">範例 1：新增金鑰庫金鑰</span><span class="sxs-lookup"><span data-stu-id="4a09c-109">Example 1: Add Key Vault key</span></span>
```
PS C:\> Add-AzSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="4a09c-110">此命令會將 Id 為 '' 的 Key Vault 鍵新增到資源群組 https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 'ContosoResourceGroup'中名為 'ContosoServer'的 SQL 伺服器。</span><span class="sxs-lookup"><span data-stu-id="4a09c-110">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL server named 'ContosoServer' in the resource group 'ContosoResourceGroup'.</span></span>
<span data-ttu-id="4a09c-111">ResourceGroupName ： ContosoResourceGroup ServerName ： ContosoServer ServerKeyName ： contoso_contosokey_01234567890123456789012345678901 Type ： AzureKeyVault Uri ： https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint ： 112233455677899001122334455667788900 CreationDate ： 1/1/2017 12：00：00 AM</span><span class="sxs-lookup"><span data-stu-id="4a09c-111">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

## <span data-ttu-id="4a09c-112">參數</span><span class="sxs-lookup"><span data-stu-id="4a09c-112">PARAMETERS</span></span>

### <span data-ttu-id="4a09c-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4a09c-113">-AsJob</span></span>
<span data-ttu-id="4a09c-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="4a09c-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4a09c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a09c-115">-DefaultProfile</span></span>
<span data-ttu-id="4a09c-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="4a09c-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4a09c-117">-KeyId</span><span class="sxs-lookup"><span data-stu-id="4a09c-117">-KeyId</span></span>
<span data-ttu-id="4a09c-118">Azure 金鑰庫 KeyId。</span><span class="sxs-lookup"><span data-stu-id="4a09c-118">The Azure Key Vault KeyId.</span></span>

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

### <span data-ttu-id="4a09c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a09c-119">-ResourceGroupName</span></span>
<span data-ttu-id="4a09c-120">資源組的名稱</span><span class="sxs-lookup"><span data-stu-id="4a09c-120">The name of the resource group</span></span>

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

### <span data-ttu-id="4a09c-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4a09c-121">-ServerName</span></span>
<span data-ttu-id="4a09c-122">Azure Sql Server 名稱。</span><span class="sxs-lookup"><span data-stu-id="4a09c-122">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="4a09c-123">-確認</span><span class="sxs-lookup"><span data-stu-id="4a09c-123">-Confirm</span></span>
<span data-ttu-id="4a09c-124">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="4a09c-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a09c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a09c-125">-WhatIf</span></span>
<span data-ttu-id="4a09c-126">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4a09c-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a09c-127">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4a09c-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a09c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a09c-128">CommonParameters</span></span>
<span data-ttu-id="4a09c-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4a09c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a09c-130">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4a09c-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a09c-131">輸入</span><span class="sxs-lookup"><span data-stu-id="4a09c-131">INPUTS</span></span>

### <span data-ttu-id="4a09c-132">System.String</span><span class="sxs-lookup"><span data-stu-id="4a09c-132">System.String</span></span>

## <span data-ttu-id="4a09c-133">輸出</span><span class="sxs-lookup"><span data-stu-id="4a09c-133">OUTPUTS</span></span>

### <span data-ttu-id="4a09c-134">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="4a09c-134">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span></span>

## <span data-ttu-id="4a09c-135">筆記</span><span class="sxs-lookup"><span data-stu-id="4a09c-135">NOTES</span></span>

## <span data-ttu-id="4a09c-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="4a09c-136">RELATED LINKS</span></span>

[<span data-ttu-id="4a09c-137">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="4a09c-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
