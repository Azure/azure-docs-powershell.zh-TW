---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDnsAlias.md
ms.openlocfilehash: 417bab5679da4607cc42468fc4620cf392323919
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94126765"
---
# <span data-ttu-id="6c00f-101">Get-AzSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="6c00f-101">Get-AzSqlServerDnsAlias</span></span>

## <span data-ttu-id="6c00f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6c00f-102">SYNOPSIS</span></span>
<span data-ttu-id="6c00f-103">取得或列出 Azure SQL Server DNS 別名。</span><span class="sxs-lookup"><span data-stu-id="6c00f-103">Gets or lists Azure SQL Server DNS Alias.</span></span>

## <span data-ttu-id="6c00f-104">句法</span><span class="sxs-lookup"><span data-stu-id="6c00f-104">SYNTAX</span></span>

```
Get-AzSqlServerDnsAlias [-Name <String>] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c00f-105">說明</span><span class="sxs-lookup"><span data-stu-id="6c00f-105">DESCRIPTION</span></span>
<span data-ttu-id="6c00f-106">取得特定的 Azure SQL Server DNS 別名，或列出伺服器的所有伺服器 DNS 別名</span><span class="sxs-lookup"><span data-stu-id="6c00f-106">Get the specific Azure SQL Server DNS Alias or lists all Server DNS Aliases for the server</span></span>

## <span data-ttu-id="6c00f-107">示例</span><span class="sxs-lookup"><span data-stu-id="6c00f-107">EXAMPLES</span></span>

### <span data-ttu-id="6c00f-108">範例1</span><span class="sxs-lookup"><span data-stu-id="6c00f-108">Example 1</span></span>
```
PS C:\> $serverDNSAliases = Get-AzSqlServerDNSAlias -ServerName servername -ResourceGroupName rgname

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
rgname             servername   dnsaliasname2
```

<span data-ttu-id="6c00f-109">列出特定伺服器的所有伺服器 DNS 別名</span><span class="sxs-lookup"><span data-stu-id="6c00f-109">Lists all Server DNS Aliases for the specific server</span></span>

### <span data-ttu-id="6c00f-110">範例2</span><span class="sxs-lookup"><span data-stu-id="6c00f-110">Example 2</span></span>
```
PS C:\> $serverDNSAliases = Get-AzSqlServerDNSAlias -DnsAliasName dnsaliasname -ServerName servername -ResourceGroupName rgname

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
```

<span data-ttu-id="6c00f-111">取得伺服器所指定的伺服器 DNS 別名及別名</span><span class="sxs-lookup"><span data-stu-id="6c00f-111">Gets Server DNS Alias specified by server and alias name</span></span>

### <span data-ttu-id="6c00f-112">範例3</span><span class="sxs-lookup"><span data-stu-id="6c00f-112">Example 3</span></span>
```
PS C:\> $serverDNSAliases = Get-AzSqlServerDNSAlias -ServerName servername -ResourceGroupName rgname -DnsAliasName "dnsaliasname*"

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
rgname             servername   dnsaliasname2
```

<span data-ttu-id="6c00f-113">針對以 "dnsaliasname" 開頭的特定伺服器列出所有伺服器 DNS 別名。</span><span class="sxs-lookup"><span data-stu-id="6c00f-113">Lists all Server DNS Aliases for the specific server that start with "dnsaliasname".</span></span>

## <span data-ttu-id="6c00f-114">參數</span><span class="sxs-lookup"><span data-stu-id="6c00f-114">PARAMETERS</span></span>

### <span data-ttu-id="6c00f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c00f-115">-DefaultProfile</span></span>
<span data-ttu-id="6c00f-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6c00f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6c00f-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="6c00f-117">-Name</span></span>
<span data-ttu-id="6c00f-118">Azure Sql Server DNS 別名名稱。</span><span class="sxs-lookup"><span data-stu-id="6c00f-118">The Azure Sql Server DNS Alias name.</span></span>

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

### <span data-ttu-id="6c00f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c00f-119">-ResourceGroupName</span></span>
<span data-ttu-id="6c00f-120">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6c00f-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="6c00f-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="6c00f-121">-ServerName</span></span>
<span data-ttu-id="6c00f-122">Azure Sql Server 名稱。</span><span class="sxs-lookup"><span data-stu-id="6c00f-122">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="6c00f-123">-確認</span><span class="sxs-lookup"><span data-stu-id="6c00f-123">-Confirm</span></span>
<span data-ttu-id="6c00f-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6c00f-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c00f-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c00f-125">-WhatIf</span></span>
<span data-ttu-id="6c00f-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6c00f-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c00f-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6c00f-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c00f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c00f-128">CommonParameters</span></span>
<span data-ttu-id="6c00f-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6c00f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c00f-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="6c00f-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c00f-131">輸入</span><span class="sxs-lookup"><span data-stu-id="6c00f-131">INPUTS</span></span>

### <span data-ttu-id="6c00f-132">System.object</span><span class="sxs-lookup"><span data-stu-id="6c00f-132">System.String</span></span>

## <span data-ttu-id="6c00f-133">輸出</span><span class="sxs-lookup"><span data-stu-id="6c00f-133">OUTPUTS</span></span>

### <span data-ttu-id="6c00f-134">AzureSqlServerDnsAliasModel 中的 [ServerDnsAlias]</span><span class="sxs-lookup"><span data-stu-id="6c00f-134">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="6c00f-135">筆記</span><span class="sxs-lookup"><span data-stu-id="6c00f-135">NOTES</span></span>

## <span data-ttu-id="6c00f-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="6c00f-136">RELATED LINKS</span></span>
