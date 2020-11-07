---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDnsAlias.md
ms.openlocfilehash: 516fd126b1015bca23c34a4eb295a03752e836f3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792753"
---
# <span data-ttu-id="56d5e-101">Get-AzSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="56d5e-101">Get-AzSqlServerDnsAlias</span></span>

## <span data-ttu-id="56d5e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="56d5e-102">SYNOPSIS</span></span>
<span data-ttu-id="56d5e-103">取得或列出 Azure SQL Server DNS 別名。</span><span class="sxs-lookup"><span data-stu-id="56d5e-103">Gets or lists Azure SQL Server DNS Alias.</span></span>

## <span data-ttu-id="56d5e-104">句法</span><span class="sxs-lookup"><span data-stu-id="56d5e-104">SYNTAX</span></span>

```
Get-AzSqlServerDnsAlias [-Name <String>] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56d5e-105">說明</span><span class="sxs-lookup"><span data-stu-id="56d5e-105">DESCRIPTION</span></span>
<span data-ttu-id="56d5e-106">取得特定的 Azure SQL Server DNS 別名，或列出伺服器的所有伺服器 DNS 別名</span><span class="sxs-lookup"><span data-stu-id="56d5e-106">Get the specific Azure SQL Server DNS Alias or lists all Server DNS Aliases for the server</span></span>

## <span data-ttu-id="56d5e-107">示例</span><span class="sxs-lookup"><span data-stu-id="56d5e-107">EXAMPLES</span></span>

### <span data-ttu-id="56d5e-108">範例1</span><span class="sxs-lookup"><span data-stu-id="56d5e-108">Example 1</span></span>
```
PS C:\> $serverDNSAliases = Get-AzSqlServerDNSAlias -ServerName servername -ResourceGroupName rgname

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
rgname             servername   dnsaliasname2
```

<span data-ttu-id="56d5e-109">列出特定伺服器的所有伺服器 DNS 別名</span><span class="sxs-lookup"><span data-stu-id="56d5e-109">Lists all Server DNS Aliases for the specific server</span></span>

### <span data-ttu-id="56d5e-110">範例2</span><span class="sxs-lookup"><span data-stu-id="56d5e-110">Example 2</span></span>
```
PS C:\> $serverDNSAliases = Get-AzSqlServerDNSAlias -DnsAliasName dnsaliasname -ServerName servername -ResourceGroupName rgname

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
```

<span data-ttu-id="56d5e-111">取得伺服器所指定的伺服器 DNS 別名及別名</span><span class="sxs-lookup"><span data-stu-id="56d5e-111">Gets Server DNS Alias specified by server and alias name</span></span>

### <span data-ttu-id="56d5e-112">範例3</span><span class="sxs-lookup"><span data-stu-id="56d5e-112">Example 3</span></span>
```
PS C:\> $serverDNSAliases = Get-AzSqlServerDNSAlias -ServerName servername -ResourceGroupName rgname -DnsAliasName "dnsaliasname*"

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
rgname             servername   dnsaliasname2
```

<span data-ttu-id="56d5e-113">針對以 "dnsaliasname" 開頭的特定伺服器列出所有伺服器 DNS 別名。</span><span class="sxs-lookup"><span data-stu-id="56d5e-113">Lists all Server DNS Aliases for the specific server that start with "dnsaliasname".</span></span>

## <span data-ttu-id="56d5e-114">參數</span><span class="sxs-lookup"><span data-stu-id="56d5e-114">PARAMETERS</span></span>

### <span data-ttu-id="56d5e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56d5e-115">-DefaultProfile</span></span>
<span data-ttu-id="56d5e-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="56d5e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="56d5e-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="56d5e-117">-Name</span></span>
<span data-ttu-id="56d5e-118">Azure Sql Server DNS 別名名稱。</span><span class="sxs-lookup"><span data-stu-id="56d5e-118">The Azure Sql Server DNS Alias name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DnsAliasName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="56d5e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56d5e-119">-ResourceGroupName</span></span>
<span data-ttu-id="56d5e-120">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="56d5e-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="56d5e-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="56d5e-121">-ServerName</span></span>
<span data-ttu-id="56d5e-122">Azure Sql Server 名稱。</span><span class="sxs-lookup"><span data-stu-id="56d5e-122">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="56d5e-123">-確認</span><span class="sxs-lookup"><span data-stu-id="56d5e-123">-Confirm</span></span>
<span data-ttu-id="56d5e-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="56d5e-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56d5e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56d5e-125">-WhatIf</span></span>
<span data-ttu-id="56d5e-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="56d5e-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56d5e-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="56d5e-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56d5e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56d5e-128">CommonParameters</span></span>
<span data-ttu-id="56d5e-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="56d5e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56d5e-130">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="56d5e-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56d5e-131">輸入</span><span class="sxs-lookup"><span data-stu-id="56d5e-131">INPUTS</span></span>

### <span data-ttu-id="56d5e-132">System.object</span><span class="sxs-lookup"><span data-stu-id="56d5e-132">System.String</span></span>

## <span data-ttu-id="56d5e-133">輸出</span><span class="sxs-lookup"><span data-stu-id="56d5e-133">OUTPUTS</span></span>

### <span data-ttu-id="56d5e-134">AzureSqlServerDnsAliasModel 中的 [ServerDnsAlias]</span><span class="sxs-lookup"><span data-stu-id="56d5e-134">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="56d5e-135">筆記</span><span class="sxs-lookup"><span data-stu-id="56d5e-135">NOTES</span></span>

## <span data-ttu-id="56d5e-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="56d5e-136">RELATED LINKS</span></span>
