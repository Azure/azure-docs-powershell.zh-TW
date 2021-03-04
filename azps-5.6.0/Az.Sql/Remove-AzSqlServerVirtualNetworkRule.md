---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 766a5bb6777d1c1ef1e077d4345b7034ede82599
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913094"
---
# <span data-ttu-id="fb1a3-101">Remove-AzSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="fb1a3-101">Remove-AzSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="fb1a3-102">簡介</span><span class="sxs-lookup"><span data-stu-id="fb1a3-102">SYNOPSIS</span></span>
<span data-ttu-id="fb1a3-103">刪除 Azure SQL Server 虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="fb1a3-103">Deletes an Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="fb1a3-104">語法</span><span class="sxs-lookup"><span data-stu-id="fb1a3-104">SYNTAX</span></span>

```
Remove-AzSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> [-AsJob] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fb1a3-105">描述</span><span class="sxs-lookup"><span data-stu-id="fb1a3-105">DESCRIPTION</span></span>
<span data-ttu-id="fb1a3-106">此命令會刪除 Azure SQL Server 虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="fb1a3-106">This command deletes an Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="fb1a3-107">例子</span><span class="sxs-lookup"><span data-stu-id="fb1a3-107">EXAMPLES</span></span>

### <span data-ttu-id="fb1a3-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="fb1a3-108">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Remove-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName
```

<span data-ttu-id="fb1a3-109">刪除現有的 Azure SQL Server 虛擬網路規則</span><span class="sxs-lookup"><span data-stu-id="fb1a3-109">Deletes an existing Azure SQL Server virtual network rule</span></span>

## <span data-ttu-id="fb1a3-110">參數</span><span class="sxs-lookup"><span data-stu-id="fb1a3-110">PARAMETERS</span></span>

### <span data-ttu-id="fb1a3-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fb1a3-111">-AsJob</span></span>
<span data-ttu-id="fb1a3-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="fb1a3-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fb1a3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb1a3-113">-DefaultProfile</span></span>
<span data-ttu-id="fb1a3-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="fb1a3-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fb1a3-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb1a3-115">-ResourceGroupName</span></span>
<span data-ttu-id="fb1a3-116">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="fb1a3-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="fb1a3-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="fb1a3-117">-ServerName</span></span>
<span data-ttu-id="fb1a3-118">Azure Sql Server 名稱。</span><span class="sxs-lookup"><span data-stu-id="fb1a3-118">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="fb1a3-119">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="fb1a3-119">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="fb1a3-120">Azure Sql Server 虛擬網路規則名稱</span><span class="sxs-lookup"><span data-stu-id="fb1a3-120">Azure Sql Server Virtual Network Rule name</span></span>

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

### <span data-ttu-id="fb1a3-121">-確認</span><span class="sxs-lookup"><span data-stu-id="fb1a3-121">-Confirm</span></span>
<span data-ttu-id="fb1a3-122">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="fb1a3-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb1a3-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb1a3-123">-WhatIf</span></span>
<span data-ttu-id="fb1a3-124">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fb1a3-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb1a3-125">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fb1a3-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb1a3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb1a3-126">CommonParameters</span></span>
<span data-ttu-id="fb1a3-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="fb1a3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb1a3-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fb1a3-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb1a3-129">輸入</span><span class="sxs-lookup"><span data-stu-id="fb1a3-129">INPUTS</span></span>

### <span data-ttu-id="fb1a3-130">System.String</span><span class="sxs-lookup"><span data-stu-id="fb1a3-130">System.String</span></span>

## <span data-ttu-id="fb1a3-131">輸出</span><span class="sxs-lookup"><span data-stu-id="fb1a3-131">OUTPUTS</span></span>

### <span data-ttu-id="fb1a3-132">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="fb1a3-132">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="fb1a3-133">筆記</span><span class="sxs-lookup"><span data-stu-id="fb1a3-133">NOTES</span></span>

## <span data-ttu-id="fb1a3-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="fb1a3-134">RELATED LINKS</span></span>
