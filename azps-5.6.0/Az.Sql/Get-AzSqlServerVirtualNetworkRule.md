---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerVirtualNetworkRule.md
ms.openlocfilehash: f4744eee1e93867ea150819a8f4bcadc5ac8a35b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915221"
---
# <span data-ttu-id="7495a-101">Get-AzSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="7495a-101">Get-AzSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="7495a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="7495a-102">SYNOPSIS</span></span>
<span data-ttu-id="7495a-103">獲取或列出 Azure SQL Server 虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="7495a-103">Gets or lists Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="7495a-104">語法</span><span class="sxs-lookup"><span data-stu-id="7495a-104">SYNTAX</span></span>

```
Get-AzSqlServerVirtualNetworkRule [-VirtualNetworkRuleName <String>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7495a-105">描述</span><span class="sxs-lookup"><span data-stu-id="7495a-105">DESCRIPTION</span></span>
<span data-ttu-id="7495a-106">此命令會獲得特定的 Azure SQL Server 虛擬網路規則，或伺服器下的 Azure SQL Server 虛擬網路規則清單。</span><span class="sxs-lookup"><span data-stu-id="7495a-106">This command gets a specific Azure SQL Server Virtual Network Rule or a list of Azure SQL Server Virtual Network Rules under a server.</span></span>

## <span data-ttu-id="7495a-107">例子</span><span class="sxs-lookup"><span data-stu-id="7495a-107">EXAMPLES</span></span>

### <span data-ttu-id="7495a-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="7495a-108">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Get-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName
```

<span data-ttu-id="7495a-109">獲得單一 Azure SQL Server 虛擬網路規則</span><span class="sxs-lookup"><span data-stu-id="7495a-109">Gets an single Azure SQL Server virtual network rule</span></span>

### <span data-ttu-id="7495a-110">範例 2</span><span class="sxs-lookup"><span data-stu-id="7495a-110">Example 2</span></span>
```
PS C:\> $virtualNetworkRules = Get-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName
```

<span data-ttu-id="7495a-111">在指定的伺服器下，獲得 Azure SQL Server 虛擬網路規則清單</span><span class="sxs-lookup"><span data-stu-id="7495a-111">Gets the list of Azure SQL Server virtual network rules under the specified server</span></span>

### <span data-ttu-id="7495a-112">範例 3</span><span class="sxs-lookup"><span data-stu-id="7495a-112">Example 3</span></span>
```
PS C:\> $virtualNetworkRules = Get-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRule*
```

<span data-ttu-id="7495a-113">在以 "virtualNetworkRule" 為開始的指定伺服器下，獲得 Azure SQL Server 虛擬網路規則的清單。</span><span class="sxs-lookup"><span data-stu-id="7495a-113">Gets the list of Azure SQL Server virtual network rules under the specified server that start with "virtualNetworkRule".</span></span>

## <span data-ttu-id="7495a-114">參數</span><span class="sxs-lookup"><span data-stu-id="7495a-114">PARAMETERS</span></span>

### <span data-ttu-id="7495a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7495a-115">-DefaultProfile</span></span>
<span data-ttu-id="7495a-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="7495a-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7495a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7495a-117">-ResourceGroupName</span></span>
<span data-ttu-id="7495a-118">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7495a-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="7495a-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7495a-119">-ServerName</span></span>
<span data-ttu-id="7495a-120">Azure Sql Server 名稱。</span><span class="sxs-lookup"><span data-stu-id="7495a-120">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="7495a-121">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="7495a-121">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="7495a-122">Azure Sql Server 虛擬網路規則名稱。</span><span class="sxs-lookup"><span data-stu-id="7495a-122">The Azure Sql Server Virtual Network Rule name.</span></span>

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

### <span data-ttu-id="7495a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7495a-123">CommonParameters</span></span>
<span data-ttu-id="7495a-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="7495a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7495a-125">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7495a-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7495a-126">輸入</span><span class="sxs-lookup"><span data-stu-id="7495a-126">INPUTS</span></span>

### <span data-ttu-id="7495a-127">System.String</span><span class="sxs-lookup"><span data-stu-id="7495a-127">System.String</span></span>

## <span data-ttu-id="7495a-128">輸出</span><span class="sxs-lookup"><span data-stu-id="7495a-128">OUTPUTS</span></span>

### <span data-ttu-id="7495a-129">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="7495a-129">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="7495a-130">筆記</span><span class="sxs-lookup"><span data-stu-id="7495a-130">NOTES</span></span>

## <span data-ttu-id="7495a-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="7495a-131">RELATED LINKS</span></span>
