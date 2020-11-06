---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerDnsAlias.md
ms.openlocfilehash: 4a2b7de83036e274b9d53b701615e3c348c5f4df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444263"
---
# <span data-ttu-id="c9cc4-101">Get-AzureRmSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="c9cc4-101">Get-AzureRmSqlServerDnsAlias</span></span>

## <span data-ttu-id="c9cc4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c9cc4-102">SYNOPSIS</span></span>
<span data-ttu-id="c9cc4-103">取得或列出 Azure SQL Server DNS 別名。</span><span class="sxs-lookup"><span data-stu-id="c9cc4-103">Gets or lists Azure SQL Server DNS Alias.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c9cc4-104">句法</span><span class="sxs-lookup"><span data-stu-id="c9cc4-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerDnsAlias [-Name <String>] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9cc4-105">說明</span><span class="sxs-lookup"><span data-stu-id="c9cc4-105">DESCRIPTION</span></span>
<span data-ttu-id="c9cc4-106">取得特定的 Azure SQL Server DNS 別名，或列出伺服器的所有伺服器 DNS 別名</span><span class="sxs-lookup"><span data-stu-id="c9cc4-106">Get the specific Azure SQL Server DNS Alias or lists all Server DNS Aliases for the server</span></span>

## <span data-ttu-id="c9cc4-107">示例</span><span class="sxs-lookup"><span data-stu-id="c9cc4-107">EXAMPLES</span></span>

### <span data-ttu-id="c9cc4-108">範例1</span><span class="sxs-lookup"><span data-stu-id="c9cc4-108">Example 1</span></span>
```
PS C:\> $serverDNSAliases = Get-AzureRmSqlServerDNSAlias -ServerName servername -ResourceGroupName rgname

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
rgname             servername   dnsaliasname2
```

<span data-ttu-id="c9cc4-109">列出特定伺服器的所有伺服器 DNS 別名</span><span class="sxs-lookup"><span data-stu-id="c9cc4-109">Lists all Server DNS Aliases for the specific server</span></span>

### <span data-ttu-id="c9cc4-110">範例2</span><span class="sxs-lookup"><span data-stu-id="c9cc4-110">Example 2</span></span>
```
PS C:\> $serverDNSAliases = Get-AzureRmSqlServerDNSAlias -DnsAliasName dnsaliasname -ServerName servername -ResourceGroupName rgname

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
```

<span data-ttu-id="c9cc4-111">取得伺服器所指定的伺服器 DNS 別名及別名</span><span class="sxs-lookup"><span data-stu-id="c9cc4-111">Gets Server DNS Alias specified by server and alias name</span></span>

## <span data-ttu-id="c9cc4-112">參數</span><span class="sxs-lookup"><span data-stu-id="c9cc4-112">PARAMETERS</span></span>

### <span data-ttu-id="c9cc4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9cc4-113">-DefaultProfile</span></span>
<span data-ttu-id="c9cc4-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c9cc4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9cc4-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="c9cc4-115">-Name</span></span>
<span data-ttu-id="c9cc4-116">Azure Sql Server DNS 別名名稱。</span><span class="sxs-lookup"><span data-stu-id="c9cc4-116">The Azure Sql Server DNS Alias name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: DnsAliasName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9cc4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9cc4-117">-ResourceGroupName</span></span>
<span data-ttu-id="c9cc4-118">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c9cc4-118">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9cc4-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c9cc4-119">-ServerName</span></span>
<span data-ttu-id="c9cc4-120">Azure Sql Server 名稱。</span><span class="sxs-lookup"><span data-stu-id="c9cc4-120">The Azure Sql Server name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9cc4-121">-確認</span><span class="sxs-lookup"><span data-stu-id="c9cc4-121">-Confirm</span></span>
<span data-ttu-id="c9cc4-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c9cc4-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9cc4-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9cc4-123">-WhatIf</span></span>
<span data-ttu-id="c9cc4-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c9cc4-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9cc4-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c9cc4-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9cc4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9cc4-126">CommonParameters</span></span>
<span data-ttu-id="c9cc4-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c9cc4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9cc4-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c9cc4-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9cc4-129">輸入</span><span class="sxs-lookup"><span data-stu-id="c9cc4-129">INPUTS</span></span>

### <span data-ttu-id="c9cc4-130">System.object</span><span class="sxs-lookup"><span data-stu-id="c9cc4-130">System.String</span></span>

## <span data-ttu-id="c9cc4-131">輸出</span><span class="sxs-lookup"><span data-stu-id="c9cc4-131">OUTPUTS</span></span>

### <span data-ttu-id="c9cc4-132">AzureSqlServerDnsAliasModel 中的 [ServerDnsAlias]</span><span class="sxs-lookup"><span data-stu-id="c9cc4-132">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="c9cc4-133">筆記</span><span class="sxs-lookup"><span data-stu-id="c9cc4-133">NOTES</span></span>

## <span data-ttu-id="c9cc4-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="c9cc4-134">RELATED LINKS</span></span>
