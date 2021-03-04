---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlserverkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerKeyVaultKey.md
ms.openlocfilehash: 523192b1632bf6ed67dff170b2ac94374c443299
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913709"
---
# <span data-ttu-id="7cc1f-101">Get-AzSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="7cc1f-101">Get-AzSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="7cc1f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="7cc1f-102">SYNOPSIS</span></span>
<span data-ttu-id="7cc1f-103">獲得 SQL 伺服器的 Key Vault 鍵。</span><span class="sxs-lookup"><span data-stu-id="7cc1f-103">Gets a SQL server's Key Vault keys.</span></span>

## <span data-ttu-id="7cc1f-104">語法</span><span class="sxs-lookup"><span data-stu-id="7cc1f-104">SYNTAX</span></span>

```
Get-AzSqlServerKeyVaultKey [[-KeyId] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7cc1f-105">描述</span><span class="sxs-lookup"><span data-stu-id="7cc1f-105">DESCRIPTION</span></span>
<span data-ttu-id="7cc1f-106">此Get-AzSqlServerKeyVaultKey Cmdlet 會獲得 SQL 伺服器上 Key Vault 鍵的資訊。</span><span class="sxs-lookup"><span data-stu-id="7cc1f-106">The Get-AzSqlServerKeyVaultKey cmdlet gets information about the Key Vault keys on a SQL server.</span></span>
<span data-ttu-id="7cc1f-107">您可以提供 KeyId 來查看伺服器上的所有金鑰，或查看特定金鑰。</span><span class="sxs-lookup"><span data-stu-id="7cc1f-107">You can view all keys on a server or view a specific key by providing the KeyId.</span></span>

## <span data-ttu-id="7cc1f-108">例子</span><span class="sxs-lookup"><span data-stu-id="7cc1f-108">EXAMPLES</span></span>

### <span data-ttu-id="7cc1f-109">範例 1：取得所有 Key Vault 鍵</span><span class="sxs-lookup"><span data-stu-id="7cc1f-109">Example 1: Get all Key Vault keys</span></span>
```
PS C:\> Get-AzSqlServerKeyVaultKey -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="7cc1f-110">此命令會獲得 SQL 伺服器上所有 Key Vault 鍵。</span><span class="sxs-lookup"><span data-stu-id="7cc1f-110">This command gets all the Key Vault keys on a SQL server.</span></span>
<span data-ttu-id="7cc1f-111">ResourceGroupName ： ContosoResourceGroup ServerName ： ContosoServer ServerKeyName ： contoso_contosokey_01234567890123456789012345678901 Type ： AzureKeyVault Uri ： https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint ： 112233445677899001122334455667788900 CreationDate ： 1/1/2017 12：00：00 AM 資源GroupName ： ContosoResourceGroup ServerName ： ContosoServer ServerKeyName ： contoso_contosokey2_01234567890123456789012345678901 Type ： AzureKeyVault Uri ： https://contoso.vault.azure.net/keys/contosokey2/09876543210987654321098765432109 Thumbprint ： 0099876654332110098877665543221 CreationDate ： 1/1/2017 12：00：00 AM</span><span class="sxs-lookup"><span data-stu-id="7cc1f-111">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey2_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey2/09876543210987654321098765432109 Thumbprint        : 0099887766554433221100998877665544332211 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

### <span data-ttu-id="7cc1f-112">範例 2：取得特定的金鑰庫金鑰</span><span class="sxs-lookup"><span data-stu-id="7cc1f-112">Example 2: Get a specific Key Vault key</span></span>
```
PS C:\> $MyServerKeyVaultKey = Get-AzSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="7cc1f-113">此命令會獲得具有 Id ' '的 Key Vault 鍵，然後將 https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 它儲存在$MyServerKeyVaultKey變數。</span><span class="sxs-lookup"><span data-stu-id="7cc1f-113">This command gets the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901', and then stores it in the $MyServerKeyVaultKey variable.</span></span>
<span data-ttu-id="7cc1f-114">您可以檢查資料$MyServerKeyVaultKey以取得金鑰庫的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="7cc1f-114">You can inspect the properties of $MyServerKeyVaultKey to get details about the key vault.</span></span>

## <span data-ttu-id="7cc1f-115">參數</span><span class="sxs-lookup"><span data-stu-id="7cc1f-115">PARAMETERS</span></span>

### <span data-ttu-id="7cc1f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cc1f-116">-DefaultProfile</span></span>
<span data-ttu-id="7cc1f-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="7cc1f-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7cc1f-118">-KeyId</span><span class="sxs-lookup"><span data-stu-id="7cc1f-118">-KeyId</span></span>
<span data-ttu-id="7cc1f-119">Azure 金鑰庫 KeyId。</span><span class="sxs-lookup"><span data-stu-id="7cc1f-119">The Azure Key Vault KeyId.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cc1f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7cc1f-120">-ResourceGroupName</span></span>
<span data-ttu-id="7cc1f-121">資源組的名稱</span><span class="sxs-lookup"><span data-stu-id="7cc1f-121">The name of the resource group</span></span>

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

### <span data-ttu-id="7cc1f-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7cc1f-122">-ServerName</span></span>
<span data-ttu-id="7cc1f-123">Azure Sql Server 名稱。</span><span class="sxs-lookup"><span data-stu-id="7cc1f-123">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="7cc1f-124">-確認</span><span class="sxs-lookup"><span data-stu-id="7cc1f-124">-Confirm</span></span>
<span data-ttu-id="7cc1f-125">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="7cc1f-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7cc1f-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7cc1f-126">-WhatIf</span></span>
<span data-ttu-id="7cc1f-127">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7cc1f-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7cc1f-128">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7cc1f-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7cc1f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cc1f-129">CommonParameters</span></span>
<span data-ttu-id="7cc1f-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="7cc1f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cc1f-131">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7cc1f-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cc1f-132">輸入</span><span class="sxs-lookup"><span data-stu-id="7cc1f-132">INPUTS</span></span>

### <span data-ttu-id="7cc1f-133">System.String</span><span class="sxs-lookup"><span data-stu-id="7cc1f-133">System.String</span></span>

## <span data-ttu-id="7cc1f-134">輸出</span><span class="sxs-lookup"><span data-stu-id="7cc1f-134">OUTPUTS</span></span>

### <span data-ttu-id="7cc1f-135">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="7cc1f-135">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span></span>

## <span data-ttu-id="7cc1f-136">筆記</span><span class="sxs-lookup"><span data-stu-id="7cc1f-136">NOTES</span></span>

## <span data-ttu-id="7cc1f-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="7cc1f-137">RELATED LINKS</span></span>

[<span data-ttu-id="7cc1f-138">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="7cc1f-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
