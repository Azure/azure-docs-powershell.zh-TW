---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 265600b201a6333b8dcd7c14f0cefe429f92619e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98279137"
---
# <span data-ttu-id="03fe6-101">Remove-AzSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="03fe6-101">Remove-AzSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="03fe6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="03fe6-102">SYNOPSIS</span></span>
<span data-ttu-id="03fe6-103">刪除 Azure SQL Server 虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="03fe6-103">Deletes an Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="03fe6-104">句法</span><span class="sxs-lookup"><span data-stu-id="03fe6-104">SYNTAX</span></span>

```
Remove-AzSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> [-AsJob] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="03fe6-105">說明</span><span class="sxs-lookup"><span data-stu-id="03fe6-105">DESCRIPTION</span></span>
<span data-ttu-id="03fe6-106">這個命令會刪除 Azure SQL Server 虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="03fe6-106">This command deletes an Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="03fe6-107">示例</span><span class="sxs-lookup"><span data-stu-id="03fe6-107">EXAMPLES</span></span>

### <span data-ttu-id="03fe6-108">範例1</span><span class="sxs-lookup"><span data-stu-id="03fe6-108">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Remove-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName
```

<span data-ttu-id="03fe6-109">刪除現有的 Azure SQL Server 虛擬網路規則</span><span class="sxs-lookup"><span data-stu-id="03fe6-109">Deletes an existing Azure SQL Server virtual network rule</span></span>

## <span data-ttu-id="03fe6-110">參數</span><span class="sxs-lookup"><span data-stu-id="03fe6-110">PARAMETERS</span></span>

### <span data-ttu-id="03fe6-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="03fe6-111">-AsJob</span></span>
<span data-ttu-id="03fe6-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="03fe6-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="03fe6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03fe6-113">-DefaultProfile</span></span>
<span data-ttu-id="03fe6-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="03fe6-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="03fe6-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03fe6-115">-ResourceGroupName</span></span>
<span data-ttu-id="03fe6-116">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="03fe6-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="03fe6-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="03fe6-117">-ServerName</span></span>
<span data-ttu-id="03fe6-118">Azure Sql Server 名稱。</span><span class="sxs-lookup"><span data-stu-id="03fe6-118">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="03fe6-119">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="03fe6-119">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="03fe6-120">Azure Sql Server 虛擬網路規則名稱</span><span class="sxs-lookup"><span data-stu-id="03fe6-120">Azure Sql Server Virtual Network Rule name</span></span>

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

### <span data-ttu-id="03fe6-121">-確認</span><span class="sxs-lookup"><span data-stu-id="03fe6-121">-Confirm</span></span>
<span data-ttu-id="03fe6-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="03fe6-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03fe6-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03fe6-123">-WhatIf</span></span>
<span data-ttu-id="03fe6-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="03fe6-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03fe6-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="03fe6-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03fe6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03fe6-126">CommonParameters</span></span>
<span data-ttu-id="03fe6-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="03fe6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03fe6-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="03fe6-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03fe6-129">輸入</span><span class="sxs-lookup"><span data-stu-id="03fe6-129">INPUTS</span></span>

### <span data-ttu-id="03fe6-130">System.object</span><span class="sxs-lookup"><span data-stu-id="03fe6-130">System.String</span></span>

## <span data-ttu-id="03fe6-131">輸出</span><span class="sxs-lookup"><span data-stu-id="03fe6-131">OUTPUTS</span></span>

### <span data-ttu-id="03fe6-132">AzureSqlServerVirtualNetworkRuleModel 中的 [VirtualNetworkRule]</span><span class="sxs-lookup"><span data-stu-id="03fe6-132">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="03fe6-133">筆記</span><span class="sxs-lookup"><span data-stu-id="03fe6-133">NOTES</span></span>

## <span data-ttu-id="03fe6-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="03fe6-134">RELATED LINKS</span></span>
