---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDnsAlias.md
ms.openlocfilehash: 49a175606526979acb4c44ddc4cb23ca7bbc33ff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908442"
---
# <span data-ttu-id="6e520-101">Get-AzSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="6e520-101">Get-AzSqlServerDnsAlias</span></span>

## <span data-ttu-id="6e520-102">簡介</span><span class="sxs-lookup"><span data-stu-id="6e520-102">SYNOPSIS</span></span>
<span data-ttu-id="6e520-103">獲取或列出 Azure SQL Server DNS 別名。</span><span class="sxs-lookup"><span data-stu-id="6e520-103">Gets or lists Azure SQL Server DNS Alias.</span></span>

## <span data-ttu-id="6e520-104">語法</span><span class="sxs-lookup"><span data-stu-id="6e520-104">SYNTAX</span></span>

```
Get-AzSqlServerDnsAlias [-Name <String>] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e520-105">描述</span><span class="sxs-lookup"><span data-stu-id="6e520-105">DESCRIPTION</span></span>
<span data-ttu-id="6e520-106">取得特定的 Azure SQL Server DNS 別名或列出伺服器的所有伺服器 DNS 別名</span><span class="sxs-lookup"><span data-stu-id="6e520-106">Get the specific Azure SQL Server DNS Alias or lists all Server DNS Aliases for the server</span></span>

## <span data-ttu-id="6e520-107">例子</span><span class="sxs-lookup"><span data-stu-id="6e520-107">EXAMPLES</span></span>

### <span data-ttu-id="6e520-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="6e520-108">Example 1</span></span>
```
PS C:\> $serverDNSAliases = Get-AzSqlServerDNSAlias -ServerName servername -ResourceGroupName rgname

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
rgname             servername   dnsaliasname2
```

<span data-ttu-id="6e520-109">列出特定伺服器的所有伺服器 DNS 別名</span><span class="sxs-lookup"><span data-stu-id="6e520-109">Lists all Server DNS Aliases for the specific server</span></span>

### <span data-ttu-id="6e520-110">範例 2</span><span class="sxs-lookup"><span data-stu-id="6e520-110">Example 2</span></span>
```
PS C:\> $serverDNSAliases = Get-AzSqlServerDNSAlias -DnsAliasName dnsaliasname -ServerName servername -ResourceGroupName rgname

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
```

<span data-ttu-id="6e520-111">讓伺服器 DNS 別名由伺服器和別名名稱指定</span><span class="sxs-lookup"><span data-stu-id="6e520-111">Gets Server DNS Alias specified by server and alias name</span></span>

### <span data-ttu-id="6e520-112">範例 3</span><span class="sxs-lookup"><span data-stu-id="6e520-112">Example 3</span></span>
```
PS C:\> $serverDNSAliases = Get-AzSqlServerDNSAlias -ServerName servername -ResourceGroupName rgname -DnsAliasName "dnsaliasname*"

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
rgname             servername   dnsaliasname2
```

<span data-ttu-id="6e520-113">列出以 "dnsaliasname" 為起始之特定伺服器的所有伺服器 DNS 別名。</span><span class="sxs-lookup"><span data-stu-id="6e520-113">Lists all Server DNS Aliases for the specific server that start with "dnsaliasname".</span></span>

## <span data-ttu-id="6e520-114">參數</span><span class="sxs-lookup"><span data-stu-id="6e520-114">PARAMETERS</span></span>

### <span data-ttu-id="6e520-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e520-115">-DefaultProfile</span></span>
<span data-ttu-id="6e520-116">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="6e520-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6e520-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="6e520-117">-Name</span></span>
<span data-ttu-id="6e520-118">Azure Sql Server DNS 別名。</span><span class="sxs-lookup"><span data-stu-id="6e520-118">The Azure Sql Server DNS Alias name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DnsAliasName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e520-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e520-119">-ResourceGroupName</span></span>
<span data-ttu-id="6e520-120">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6e520-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="6e520-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="6e520-121">-ServerName</span></span>
<span data-ttu-id="6e520-122">Azure Sql Server 名稱。</span><span class="sxs-lookup"><span data-stu-id="6e520-122">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="6e520-123">-確認</span><span class="sxs-lookup"><span data-stu-id="6e520-123">-Confirm</span></span>
<span data-ttu-id="6e520-124">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="6e520-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e520-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e520-125">-WhatIf</span></span>
<span data-ttu-id="6e520-126">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6e520-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e520-127">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6e520-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e520-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e520-128">CommonParameters</span></span>
<span data-ttu-id="6e520-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="6e520-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e520-130">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6e520-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e520-131">輸入</span><span class="sxs-lookup"><span data-stu-id="6e520-131">INPUTS</span></span>

### <span data-ttu-id="6e520-132">System.String</span><span class="sxs-lookup"><span data-stu-id="6e520-132">System.String</span></span>

## <span data-ttu-id="6e520-133">輸出</span><span class="sxs-lookup"><span data-stu-id="6e520-133">OUTPUTS</span></span>

### <span data-ttu-id="6e520-134">Microsoft.Azure.Commands.sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="6e520-134">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="6e520-135">筆記</span><span class="sxs-lookup"><span data-stu-id="6e520-135">NOTES</span></span>

## <span data-ttu-id="6e520-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="6e520-136">RELATED LINKS</span></span>
