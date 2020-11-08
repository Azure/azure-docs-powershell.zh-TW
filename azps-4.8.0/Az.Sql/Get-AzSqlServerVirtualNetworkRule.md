---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerVirtualNetworkRule.md
ms.openlocfilehash: f8ac34526691f3bdacdd0736189e063c969f63ff
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93970109"
---
# <span data-ttu-id="a4973-101">Get-AzSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="a4973-101">Get-AzSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="a4973-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a4973-102">SYNOPSIS</span></span>
<span data-ttu-id="a4973-103">取得或列出 Azure SQL Server 虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="a4973-103">Gets or lists Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="a4973-104">句法</span><span class="sxs-lookup"><span data-stu-id="a4973-104">SYNTAX</span></span>

```
Get-AzSqlServerVirtualNetworkRule [-VirtualNetworkRuleName <String>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a4973-105">說明</span><span class="sxs-lookup"><span data-stu-id="a4973-105">DESCRIPTION</span></span>
<span data-ttu-id="a4973-106">這個命令會在伺服器上取得特定的 Azure SQL Server 虛擬網路規則或 Azure SQL Server 虛擬網路規則清單。</span><span class="sxs-lookup"><span data-stu-id="a4973-106">This command gets a specific Azure SQL Server Virtual Network Rule or a list of Azure SQL Server Virtual Network Rules under a server.</span></span>

## <span data-ttu-id="a4973-107">示例</span><span class="sxs-lookup"><span data-stu-id="a4973-107">EXAMPLES</span></span>

### <span data-ttu-id="a4973-108">範例1</span><span class="sxs-lookup"><span data-stu-id="a4973-108">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Get-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName
```

<span data-ttu-id="a4973-109">取得單一 Azure SQL Server 虛擬網路規則</span><span class="sxs-lookup"><span data-stu-id="a4973-109">Gets an single Azure SQL Server virtual network rule</span></span>

### <span data-ttu-id="a4973-110">範例2</span><span class="sxs-lookup"><span data-stu-id="a4973-110">Example 2</span></span>
```
PS C:\> $virtualNetworkRules = Get-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName
```

<span data-ttu-id="a4973-111">在指定的伺服器下取得 Azure SQL Server 虛擬網路規則清單</span><span class="sxs-lookup"><span data-stu-id="a4973-111">Gets the list of Azure SQL Server virtual network rules under the specified server</span></span>

### <span data-ttu-id="a4973-112">範例3</span><span class="sxs-lookup"><span data-stu-id="a4973-112">Example 3</span></span>
```
PS C:\> $virtualNetworkRules = Get-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRule*
```

<span data-ttu-id="a4973-113">取得以 "virtualNetworkRule" 開頭的指定伺服器的 Azure SQL Server 虛擬網路規則清單。</span><span class="sxs-lookup"><span data-stu-id="a4973-113">Gets the list of Azure SQL Server virtual network rules under the specified server that start with "virtualNetworkRule".</span></span>

## <span data-ttu-id="a4973-114">參數</span><span class="sxs-lookup"><span data-stu-id="a4973-114">PARAMETERS</span></span>

### <span data-ttu-id="a4973-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4973-115">-DefaultProfile</span></span>
<span data-ttu-id="a4973-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="a4973-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a4973-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4973-117">-ResourceGroupName</span></span>
<span data-ttu-id="a4973-118">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a4973-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="a4973-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a4973-119">-ServerName</span></span>
<span data-ttu-id="a4973-120">Azure Sql Server 名稱。</span><span class="sxs-lookup"><span data-stu-id="a4973-120">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="a4973-121">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="a4973-121">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="a4973-122">Azure Sql Server 虛擬網路規則名稱。</span><span class="sxs-lookup"><span data-stu-id="a4973-122">The Azure Sql Server Virtual Network Rule name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4973-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4973-123">CommonParameters</span></span>
<span data-ttu-id="a4973-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a4973-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4973-125">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a4973-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4973-126">輸入</span><span class="sxs-lookup"><span data-stu-id="a4973-126">INPUTS</span></span>

### <span data-ttu-id="a4973-127">System.object</span><span class="sxs-lookup"><span data-stu-id="a4973-127">System.String</span></span>

## <span data-ttu-id="a4973-128">輸出</span><span class="sxs-lookup"><span data-stu-id="a4973-128">OUTPUTS</span></span>

### <span data-ttu-id="a4973-129">AzureSqlServerVirtualNetworkRuleModel 中的 [VirtualNetworkRule]</span><span class="sxs-lookup"><span data-stu-id="a4973-129">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="a4973-130">筆記</span><span class="sxs-lookup"><span data-stu-id="a4973-130">NOTES</span></span>

## <span data-ttu-id="a4973-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="a4973-131">RELATED LINKS</span></span>
