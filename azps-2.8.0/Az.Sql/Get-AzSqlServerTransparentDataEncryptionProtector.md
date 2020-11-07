---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlservertransparentdataencryptionprotector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerTransparentDataEncryptionProtector.md
ms.openlocfilehash: c1571dd5d03f82da13feec115fb9da123c6e3f69
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792472"
---
# <span data-ttu-id="887d9-101">Get-AzSqlServerTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="887d9-101">Get-AzSqlServerTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="887d9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="887d9-102">SYNOPSIS</span></span>
<span data-ttu-id="887d9-103">取得透明的資料加密 (TDE) 保護器</span><span class="sxs-lookup"><span data-stu-id="887d9-103">Gets the Transparent Data Encryption (TDE) protector</span></span>

## <span data-ttu-id="887d9-104">句法</span><span class="sxs-lookup"><span data-stu-id="887d9-104">SYNTAX</span></span>

```
Get-AzSqlServerTransparentDataEncryptionProtector [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="887d9-105">說明</span><span class="sxs-lookup"><span data-stu-id="887d9-105">DESCRIPTION</span></span>
<span data-ttu-id="887d9-106">Get-AzSqlServerTransparentDataEncryptionProtector Cmdlet 會取得 TDE 保護程式的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="887d9-106">The Get-AzSqlServerTransparentDataEncryptionProtector cmdlet gets information about the TDE protector.</span></span>

## <span data-ttu-id="887d9-107">示例</span><span class="sxs-lookup"><span data-stu-id="887d9-107">EXAMPLES</span></span>

### <span data-ttu-id="887d9-108">範例1：取得透明的資料加密 (TDE) 保護器</span><span class="sxs-lookup"><span data-stu-id="887d9-108">Example 1: Get the Transparent Data Encryption (TDE) protector</span></span>
```
PS C:\> Get-AzSqlServerTransparentDataEncryptionProtector -ServerName 'ContosoServer' -ResourceGroup 'ContosoResourceGroup'
```

<span data-ttu-id="887d9-109">這個命令會取得名為 ContosoResourceGroup 之資源群組中名為 ContosoServer 之伺服器的 TDE 保護器。</span><span class="sxs-lookup"><span data-stu-id="887d9-109">This command gets the TDE protector for the server named ContosoServer in resource group named ContosoResourceGroup.</span></span>
<span data-ttu-id="887d9-110">ResourceGroupName ServerName 類型 ServerKeyVaultKeyName</span><span class="sxs-lookup"><span data-stu-id="887d9-110">ResourceGroupName ServerName                   Type ServerKeyVaultKeyName</span></span>
----------------- ----------                   ---- ---------------------
<span data-ttu-id="887d9-111">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span><span class="sxs-lookup"><span data-stu-id="887d9-111">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span></span>

## <span data-ttu-id="887d9-112">參數</span><span class="sxs-lookup"><span data-stu-id="887d9-112">PARAMETERS</span></span>

### <span data-ttu-id="887d9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="887d9-113">-DefaultProfile</span></span>
<span data-ttu-id="887d9-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="887d9-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="887d9-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="887d9-115">-ResourceGroupName</span></span>
<span data-ttu-id="887d9-116">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="887d9-116">The name of the resource group</span></span>

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

### <span data-ttu-id="887d9-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="887d9-117">-ServerName</span></span>
<span data-ttu-id="887d9-118">Azure Sql Server 名稱。</span><span class="sxs-lookup"><span data-stu-id="887d9-118">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="887d9-119">-確認</span><span class="sxs-lookup"><span data-stu-id="887d9-119">-Confirm</span></span>
<span data-ttu-id="887d9-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="887d9-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="887d9-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="887d9-121">-WhatIf</span></span>
<span data-ttu-id="887d9-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="887d9-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="887d9-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="887d9-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="887d9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="887d9-124">CommonParameters</span></span>
<span data-ttu-id="887d9-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="887d9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="887d9-126">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="887d9-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="887d9-127">輸入</span><span class="sxs-lookup"><span data-stu-id="887d9-127">INPUTS</span></span>

### <span data-ttu-id="887d9-128">System.object</span><span class="sxs-lookup"><span data-stu-id="887d9-128">System.String</span></span>

## <span data-ttu-id="887d9-129">輸出</span><span class="sxs-lookup"><span data-stu-id="887d9-129">OUTPUTS</span></span>

### <span data-ttu-id="887d9-130">AzureSqlServerTransparentDataEncryptionProtectorModel 中的 [TransparentDataEncryption]</span><span class="sxs-lookup"><span data-stu-id="887d9-130">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlServerTransparentDataEncryptionProtectorModel</span></span>

## <span data-ttu-id="887d9-131">筆記</span><span class="sxs-lookup"><span data-stu-id="887d9-131">NOTES</span></span>

## <span data-ttu-id="887d9-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="887d9-132">RELATED LINKS</span></span>

[<span data-ttu-id="887d9-133">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="887d9-133">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
