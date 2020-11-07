---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/add-azurermsqlserverkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Add-AzureRmSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Add-AzureRmSqlServerKeyVaultKey.md
ms.openlocfilehash: 96f6f6a2697117099a6710acec5be8018e492c42
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625560"
---
# <span data-ttu-id="c12cf-101">Add-AzureRmSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="c12cf-101">Add-AzureRmSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="c12cf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c12cf-102">SYNOPSIS</span></span>
<span data-ttu-id="c12cf-103">將主要保存庫金鑰新增至 SQL server。</span><span class="sxs-lookup"><span data-stu-id="c12cf-103">Adds a Key Vault key to a SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c12cf-104">句法</span><span class="sxs-lookup"><span data-stu-id="c12cf-104">SYNTAX</span></span>

```
Add-AzureRmSqlServerKeyVaultKey [-KeyId] <String> [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c12cf-105">說明</span><span class="sxs-lookup"><span data-stu-id="c12cf-105">DESCRIPTION</span></span>
<span data-ttu-id="c12cf-106">Add-AzureRmSqlServerKeyVaultKey Cmdlet 會將主要保存庫金鑰新增至提供的 SQL server。</span><span class="sxs-lookup"><span data-stu-id="c12cf-106">The Add-AzureRmSqlServerKeyVaultKey cmdlet adds a Key Vault key to the provided SQL server.</span></span>
<span data-ttu-id="c12cf-107">伺服器必須擁有保存庫的「取得、wrapKey、unwrapKey」許可權。</span><span class="sxs-lookup"><span data-stu-id="c12cf-107">The server must have 'get, wrapKey, unwrapKey' permissions to the vault.</span></span>

## <span data-ttu-id="c12cf-108">示例</span><span class="sxs-lookup"><span data-stu-id="c12cf-108">EXAMPLES</span></span>

### <span data-ttu-id="c12cf-109">範例1：新增主要電子倉庫金鑰</span><span class="sxs-lookup"><span data-stu-id="c12cf-109">Example 1: Add Key Vault key</span></span>
```
PS C:\> Add-AzureRmSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="c12cf-110">這個命令會將 Id "" 的主要保存庫金鑰新增 https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 至資源群組 ' ContosoResourceGroup ' 中名為 ' ContosoServer ' 的 SQL server。</span><span class="sxs-lookup"><span data-stu-id="c12cf-110">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL server named 'ContosoServer' in the resource group 'ContosoResourceGroup'.</span></span>
<span data-ttu-id="c12cf-111">ResourceGroupName： ContosoResourceGroup ServerName： ContosoServer ServerKeyName： contoso_contosokey_01234567890123456789012345678901 類型： AzureKeyVault Uri： https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 指紋： 1122334455667788990011223344556677889900 CreationDate： 1/1/2017 12:00:00 AM</span><span class="sxs-lookup"><span data-stu-id="c12cf-111">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

## <span data-ttu-id="c12cf-112">參數</span><span class="sxs-lookup"><span data-stu-id="c12cf-112">PARAMETERS</span></span>

### <span data-ttu-id="c12cf-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c12cf-113">-AsJob</span></span>
<span data-ttu-id="c12cf-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c12cf-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c12cf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c12cf-115">-DefaultProfile</span></span>
<span data-ttu-id="c12cf-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="c12cf-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c12cf-117">-KeyId</span><span class="sxs-lookup"><span data-stu-id="c12cf-117">-KeyId</span></span>
<span data-ttu-id="c12cf-118">Azure 金鑰保存庫 KeyId。</span><span class="sxs-lookup"><span data-stu-id="c12cf-118">The Azure Key Vault KeyId.</span></span>

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

### <span data-ttu-id="c12cf-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c12cf-119">-ResourceGroupName</span></span>
<span data-ttu-id="c12cf-120">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="c12cf-120">The name of the resource group</span></span>

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

### <span data-ttu-id="c12cf-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c12cf-121">-ServerName</span></span>
<span data-ttu-id="c12cf-122">Azure Sql Server 名稱。</span><span class="sxs-lookup"><span data-stu-id="c12cf-122">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="c12cf-123">-確認</span><span class="sxs-lookup"><span data-stu-id="c12cf-123">-Confirm</span></span>
<span data-ttu-id="c12cf-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c12cf-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c12cf-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c12cf-125">-WhatIf</span></span>
<span data-ttu-id="c12cf-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c12cf-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c12cf-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c12cf-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c12cf-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c12cf-128">CommonParameters</span></span>
<span data-ttu-id="c12cf-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c12cf-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c12cf-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c12cf-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c12cf-131">輸入</span><span class="sxs-lookup"><span data-stu-id="c12cf-131">INPUTS</span></span>

### <span data-ttu-id="c12cf-132">System.object</span><span class="sxs-lookup"><span data-stu-id="c12cf-132">System.String</span></span>

## <span data-ttu-id="c12cf-133">輸出</span><span class="sxs-lookup"><span data-stu-id="c12cf-133">OUTPUTS</span></span>

### <span data-ttu-id="c12cf-134">AzureSqlServerKeyVaultKeyModel 中的 [ServerKeyVaultKey]</span><span class="sxs-lookup"><span data-stu-id="c12cf-134">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span></span>

## <span data-ttu-id="c12cf-135">筆記</span><span class="sxs-lookup"><span data-stu-id="c12cf-135">NOTES</span></span>

## <span data-ttu-id="c12cf-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="c12cf-136">RELATED LINKS</span></span>

[<span data-ttu-id="c12cf-137">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="c12cf-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
