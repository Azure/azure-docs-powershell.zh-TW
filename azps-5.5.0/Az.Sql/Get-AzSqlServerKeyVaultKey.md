---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerKeyVaultKey.md
ms.openlocfilehash: 93e8e4a5bb45fce59e10b6fdde37f2bd6122f2fd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100139763"
---
# <span data-ttu-id="b5e5c-101">Get-AzSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="b5e5c-101">Get-AzSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="b5e5c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b5e5c-102">SYNOPSIS</span></span>
<span data-ttu-id="b5e5c-103">取得 SQL server 的主要保存庫金鑰。</span><span class="sxs-lookup"><span data-stu-id="b5e5c-103">Gets a SQL server's Key Vault keys.</span></span>

## <span data-ttu-id="b5e5c-104">句法</span><span class="sxs-lookup"><span data-stu-id="b5e5c-104">SYNTAX</span></span>

```
Get-AzSqlServerKeyVaultKey [[-KeyId] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5e5c-105">說明</span><span class="sxs-lookup"><span data-stu-id="b5e5c-105">DESCRIPTION</span></span>
<span data-ttu-id="b5e5c-106">Get-AzSqlServerKeyVaultKey Cmdlet 會取得有關 SQL server 上的主要保存庫金鑰的資訊。</span><span class="sxs-lookup"><span data-stu-id="b5e5c-106">The Get-AzSqlServerKeyVaultKey cmdlet gets information about the Key Vault keys on a SQL server.</span></span>
<span data-ttu-id="b5e5c-107">您可以透過提供 KeyId 來查看伺服器上的所有金鑰，或查看特定的金鑰。</span><span class="sxs-lookup"><span data-stu-id="b5e5c-107">You can view all keys on a server or view a specific key by providing the KeyId.</span></span>

## <span data-ttu-id="b5e5c-108">示例</span><span class="sxs-lookup"><span data-stu-id="b5e5c-108">EXAMPLES</span></span>

### <span data-ttu-id="b5e5c-109">範例1：取得所有的主要保存庫金鑰</span><span class="sxs-lookup"><span data-stu-id="b5e5c-109">Example 1: Get all Key Vault keys</span></span>
```
PS C:\> Get-AzSqlServerKeyVaultKey -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="b5e5c-110">這個命令會取得 SQL server 上的所有主要保存庫金鑰。</span><span class="sxs-lookup"><span data-stu-id="b5e5c-110">This command gets all the Key Vault keys on a SQL server.</span></span>
<span data-ttu-id="b5e5c-111">ResourceGroupName： ContosoResourceGroup ServerName： ContosoServer ServerKeyName： contoso_contosokey_01234567890123456789012345678901 類型： AzureKeyVault Uri： https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 指紋： 1122334455667788990011223344556677889900 CreationDate： 1/1/2017 12:00:00 AM ResourceGroupName： ContosoResourceGroup ServerName： ContosoServer ServerKeyName： Contoso_contosokey2_01234567890123456789012345678901 類型： AzureKeyVault uri： https://contoso.vault.azure.net/keys/contosokey2/09876543210987654321098765432109 指紋： 0099887766554433221100998877665544332211 CreationDate： 1/1/2017 12:00:00 AM</span><span class="sxs-lookup"><span data-stu-id="b5e5c-111">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey2_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey2/09876543210987654321098765432109 Thumbprint        : 0099887766554433221100998877665544332211 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

### <span data-ttu-id="b5e5c-112">範例2：取得特定的金鑰保存庫金鑰</span><span class="sxs-lookup"><span data-stu-id="b5e5c-112">Example 2: Get a specific Key Vault key</span></span>
```
PS C:\> $MyServerKeyVaultKey = Get-AzSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="b5e5c-113">這個命令會取得 Id 為 "" 的主要保存庫金鑰 https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ，然後將它儲存在 $MyServerKeyVaultKey 變數中。</span><span class="sxs-lookup"><span data-stu-id="b5e5c-113">This command gets the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901', and then stores it in the $MyServerKeyVaultKey variable.</span></span>
<span data-ttu-id="b5e5c-114">您可以檢查 $MyServerKeyVaultKey 的屬性，以取得關於主要電子倉庫的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="b5e5c-114">You can inspect the properties of $MyServerKeyVaultKey to get details about the key vault.</span></span>

## <span data-ttu-id="b5e5c-115">參數</span><span class="sxs-lookup"><span data-stu-id="b5e5c-115">PARAMETERS</span></span>

### <span data-ttu-id="b5e5c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5e5c-116">-DefaultProfile</span></span>
<span data-ttu-id="b5e5c-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="b5e5c-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b5e5c-118">-KeyId</span><span class="sxs-lookup"><span data-stu-id="b5e5c-118">-KeyId</span></span>
<span data-ttu-id="b5e5c-119">Azure 金鑰保存庫 KeyId。</span><span class="sxs-lookup"><span data-stu-id="b5e5c-119">The Azure Key Vault KeyId.</span></span>

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

### <span data-ttu-id="b5e5c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5e5c-120">-ResourceGroupName</span></span>
<span data-ttu-id="b5e5c-121">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="b5e5c-121">The name of the resource group</span></span>

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

### <span data-ttu-id="b5e5c-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b5e5c-122">-ServerName</span></span>
<span data-ttu-id="b5e5c-123">Azure Sql Server 名稱。</span><span class="sxs-lookup"><span data-stu-id="b5e5c-123">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="b5e5c-124">-確認</span><span class="sxs-lookup"><span data-stu-id="b5e5c-124">-Confirm</span></span>
<span data-ttu-id="b5e5c-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b5e5c-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5e5c-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5e5c-126">-WhatIf</span></span>
<span data-ttu-id="b5e5c-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b5e5c-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5e5c-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b5e5c-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5e5c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5e5c-129">CommonParameters</span></span>
<span data-ttu-id="b5e5c-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b5e5c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5e5c-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b5e5c-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5e5c-132">輸入</span><span class="sxs-lookup"><span data-stu-id="b5e5c-132">INPUTS</span></span>

### <span data-ttu-id="b5e5c-133">System.object</span><span class="sxs-lookup"><span data-stu-id="b5e5c-133">System.String</span></span>

## <span data-ttu-id="b5e5c-134">輸出</span><span class="sxs-lookup"><span data-stu-id="b5e5c-134">OUTPUTS</span></span>

### <span data-ttu-id="b5e5c-135">AzureSqlServerKeyVaultKeyModel 中的 [ServerKeyVaultKey]</span><span class="sxs-lookup"><span data-stu-id="b5e5c-135">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span></span>

## <span data-ttu-id="b5e5c-136">筆記</span><span class="sxs-lookup"><span data-stu-id="b5e5c-136">NOTES</span></span>

## <span data-ttu-id="b5e5c-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="b5e5c-137">RELATED LINKS</span></span>

[<span data-ttu-id="b5e5c-138">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="b5e5c-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
