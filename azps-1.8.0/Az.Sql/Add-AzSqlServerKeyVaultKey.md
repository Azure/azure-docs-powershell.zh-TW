---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/add-azsqlserverkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlServerKeyVaultKey.md
ms.openlocfilehash: 9b07a7d9113411b83c97818d6d34c5a7df40c8fd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93620526"
---
# <span data-ttu-id="2e312-101">Add-AzSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="2e312-101">Add-AzSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="2e312-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2e312-102">SYNOPSIS</span></span>
<span data-ttu-id="2e312-103">將主要保存庫金鑰新增至 SQL server。</span><span class="sxs-lookup"><span data-stu-id="2e312-103">Adds a Key Vault key to a SQL server.</span></span>

## <span data-ttu-id="2e312-104">句法</span><span class="sxs-lookup"><span data-stu-id="2e312-104">SYNTAX</span></span>

```
Add-AzSqlServerKeyVaultKey [-KeyId] <String> [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e312-105">說明</span><span class="sxs-lookup"><span data-stu-id="2e312-105">DESCRIPTION</span></span>
<span data-ttu-id="2e312-106">Add-AzSqlServerKeyVaultKey Cmdlet 會將主要保存庫金鑰新增至提供的 SQL server。</span><span class="sxs-lookup"><span data-stu-id="2e312-106">The Add-AzSqlServerKeyVaultKey cmdlet adds a Key Vault key to the provided SQL server.</span></span>
<span data-ttu-id="2e312-107">伺服器必須擁有保存庫的「取得、wrapKey、unwrapKey」許可權。</span><span class="sxs-lookup"><span data-stu-id="2e312-107">The server must have 'get, wrapKey, unwrapKey' permissions to the vault.</span></span>

## <span data-ttu-id="2e312-108">示例</span><span class="sxs-lookup"><span data-stu-id="2e312-108">EXAMPLES</span></span>

### <span data-ttu-id="2e312-109">範例1：新增主要電子倉庫金鑰</span><span class="sxs-lookup"><span data-stu-id="2e312-109">Example 1: Add Key Vault key</span></span>
```
PS C:\> Add-AzSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="2e312-110">這個命令會將 Id "" 的主要保存庫金鑰新增 https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 至資源群組 ' ContosoResourceGroup ' 中名為 ' ContosoServer ' 的 SQL server。</span><span class="sxs-lookup"><span data-stu-id="2e312-110">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL server named 'ContosoServer' in the resource group 'ContosoResourceGroup'.</span></span>
<span data-ttu-id="2e312-111">ResourceGroupName： ContosoResourceGroup ServerName： ContosoServer ServerKeyName： contoso_contosokey_01234567890123456789012345678901 類型： AzureKeyVault Uri： https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 指紋： 1122334455667788990011223344556677889900 CreationDate： 1/1/2017 12:00:00 AM</span><span class="sxs-lookup"><span data-stu-id="2e312-111">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

## <span data-ttu-id="2e312-112">參數</span><span class="sxs-lookup"><span data-stu-id="2e312-112">PARAMETERS</span></span>

### <span data-ttu-id="2e312-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2e312-113">-AsJob</span></span>
<span data-ttu-id="2e312-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="2e312-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2e312-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e312-115">-DefaultProfile</span></span>
<span data-ttu-id="2e312-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="2e312-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2e312-117">-KeyId</span><span class="sxs-lookup"><span data-stu-id="2e312-117">-KeyId</span></span>
<span data-ttu-id="2e312-118">Azure 金鑰保存庫 KeyId。</span><span class="sxs-lookup"><span data-stu-id="2e312-118">The Azure Key Vault KeyId.</span></span>

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

### <span data-ttu-id="2e312-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e312-119">-ResourceGroupName</span></span>
<span data-ttu-id="2e312-120">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="2e312-120">The name of the resource group</span></span>

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

### <span data-ttu-id="2e312-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="2e312-121">-ServerName</span></span>
<span data-ttu-id="2e312-122">Azure Sql Server 名稱。</span><span class="sxs-lookup"><span data-stu-id="2e312-122">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="2e312-123">-確認</span><span class="sxs-lookup"><span data-stu-id="2e312-123">-Confirm</span></span>
<span data-ttu-id="2e312-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2e312-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e312-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e312-125">-WhatIf</span></span>
<span data-ttu-id="2e312-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2e312-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e312-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2e312-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e312-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e312-128">CommonParameters</span></span>
<span data-ttu-id="2e312-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2e312-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e312-130">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="2e312-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e312-131">輸入</span><span class="sxs-lookup"><span data-stu-id="2e312-131">INPUTS</span></span>

### <span data-ttu-id="2e312-132">System.object</span><span class="sxs-lookup"><span data-stu-id="2e312-132">System.String</span></span>

## <span data-ttu-id="2e312-133">輸出</span><span class="sxs-lookup"><span data-stu-id="2e312-133">OUTPUTS</span></span>

### <span data-ttu-id="2e312-134">AzureSqlServerKeyVaultKeyModel 中的 [ServerKeyVaultKey]</span><span class="sxs-lookup"><span data-stu-id="2e312-134">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span></span>

## <span data-ttu-id="2e312-135">筆記</span><span class="sxs-lookup"><span data-stu-id="2e312-135">NOTES</span></span>

## <span data-ttu-id="2e312-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="2e312-136">RELATED LINKS</span></span>

[<span data-ttu-id="2e312-137">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="2e312-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
