---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerDnsAlias.md
ms.openlocfilehash: 3ce18369645705f78722f7505c8dd1e46f2514b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445419"
---
# <span data-ttu-id="80d0a-101">New-AzureRmSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="80d0a-101">New-AzureRmSqlServerDnsAlias</span></span>

## <span data-ttu-id="80d0a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="80d0a-102">SYNOPSIS</span></span>
<span data-ttu-id="80d0a-103">這個命令會建立新的 Azure SQL Server DNS 別名。</span><span class="sxs-lookup"><span data-stu-id="80d0a-103">This command creates a new Azure SQL Server DNS Alias.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="80d0a-104">句法</span><span class="sxs-lookup"><span data-stu-id="80d0a-104">SYNTAX</span></span>

```
New-AzureRmSqlServerDnsAlias -Name <String> [-AsJob] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80d0a-105">說明</span><span class="sxs-lookup"><span data-stu-id="80d0a-105">DESCRIPTION</span></span>
<span data-ttu-id="80d0a-106">建立指向指定伺服器的新 Azure SQL Server DNS 別名。</span><span class="sxs-lookup"><span data-stu-id="80d0a-106">Creates new Azure SQL Server DNS Alias that is pointing to specified server.</span></span>

## <span data-ttu-id="80d0a-107">示例</span><span class="sxs-lookup"><span data-stu-id="80d0a-107">EXAMPLES</span></span>

### <span data-ttu-id="80d0a-108">範例1</span><span class="sxs-lookup"><span data-stu-id="80d0a-108">Example 1</span></span>
```
PS C:\> $serverDNSAlias = New-AzureRmSqlServerDnsAlias -ResourceGroupName rg -ServerName serverName -DnsAliasName aliasName

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
```

<span data-ttu-id="80d0a-109">這個命令會使用指向伺服器 serverName 的名稱 aliasName 來建立 Azure SQL Server DNS 別名</span><span class="sxs-lookup"><span data-stu-id="80d0a-109">This command creates Azure SQL Server DNS Alias with the name aliasName that is pointing to server serverName</span></span>

## <span data-ttu-id="80d0a-110">參數</span><span class="sxs-lookup"><span data-stu-id="80d0a-110">PARAMETERS</span></span>

### <span data-ttu-id="80d0a-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="80d0a-111">-AsJob</span></span>
<span data-ttu-id="80d0a-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="80d0a-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="80d0a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80d0a-113">-DefaultProfile</span></span>
<span data-ttu-id="80d0a-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="80d0a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="80d0a-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="80d0a-115">-Name</span></span>
<span data-ttu-id="80d0a-116">Azure Sql Server Dns 別名名稱。</span><span class="sxs-lookup"><span data-stu-id="80d0a-116">The Azure Sql Server Dns Alias name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DnsAliasName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80d0a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80d0a-117">-ResourceGroupName</span></span>
<span data-ttu-id="80d0a-118">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="80d0a-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="80d0a-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="80d0a-119">-ServerName</span></span>
<span data-ttu-id="80d0a-120">Azure Sql Server 名稱。</span><span class="sxs-lookup"><span data-stu-id="80d0a-120">The Azure Sql Server name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80d0a-121">-確認</span><span class="sxs-lookup"><span data-stu-id="80d0a-121">-Confirm</span></span>
<span data-ttu-id="80d0a-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="80d0a-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80d0a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80d0a-123">-WhatIf</span></span>
<span data-ttu-id="80d0a-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="80d0a-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80d0a-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="80d0a-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80d0a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80d0a-126">CommonParameters</span></span>
<span data-ttu-id="80d0a-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="80d0a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80d0a-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="80d0a-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80d0a-129">輸入</span><span class="sxs-lookup"><span data-stu-id="80d0a-129">INPUTS</span></span>

### <span data-ttu-id="80d0a-130">System.object</span><span class="sxs-lookup"><span data-stu-id="80d0a-130">System.String</span></span>

## <span data-ttu-id="80d0a-131">輸出</span><span class="sxs-lookup"><span data-stu-id="80d0a-131">OUTPUTS</span></span>

### <span data-ttu-id="80d0a-132">AzureSqlServerDnsAliasModel 中的 [ServerDnsAlias]</span><span class="sxs-lookup"><span data-stu-id="80d0a-132">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="80d0a-133">筆記</span><span class="sxs-lookup"><span data-stu-id="80d0a-133">NOTES</span></span>

## <span data-ttu-id="80d0a-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="80d0a-134">RELATED LINKS</span></span>
