---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 44F8EFF4-8E3D-4657-9D17-2A3F49CEA515
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: a1f91c01d3183551cbabf58754fbe628e1feea32
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912306"
---
# <span data-ttu-id="d3b47-101">Set-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="d3b47-101">Set-AzSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="d3b47-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d3b47-102">SYNOPSIS</span></span>
<span data-ttu-id="d3b47-103">修改資料庫伺服器復原群組原則。</span><span class="sxs-lookup"><span data-stu-id="d3b47-103">Modifies a database server recovery configuration.</span></span>

## <span data-ttu-id="d3b47-104">語法</span><span class="sxs-lookup"><span data-stu-id="d3b47-104">SYNTAX</span></span>

```
Set-AzSqlServerDisasterRecoveryConfiguration -VirtualEndpointName <String> [-Failover] [-AllowDataLoss]
 [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3b47-105">描述</span><span class="sxs-lookup"><span data-stu-id="d3b47-105">DESCRIPTION</span></span>
<span data-ttu-id="d3b47-106">**Set-AzSqlServerDsterRecoveryConfiguration** Cmdlet 會修改 SQL 資料庫伺服器復原設定。</span><span class="sxs-lookup"><span data-stu-id="d3b47-106">The **Set-AzSqlServerDisasterRecoveryConfiguration** cmdlet modifies a SQL database server recovery configuration.</span></span>

## <span data-ttu-id="d3b47-107">例子</span><span class="sxs-lookup"><span data-stu-id="d3b47-107">EXAMPLES</span></span>

## <span data-ttu-id="d3b47-108">參數</span><span class="sxs-lookup"><span data-stu-id="d3b47-108">PARAMETERS</span></span>

### <span data-ttu-id="d3b47-109">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="d3b47-109">-AllowDataLoss</span></span>
<span data-ttu-id="d3b47-110">表示容錯移轉作業允許資料遺失。</span><span class="sxs-lookup"><span data-stu-id="d3b47-110">Indicates that the failover operation permits data loss.</span></span>

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

### <span data-ttu-id="d3b47-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d3b47-111">-AsJob</span></span>
<span data-ttu-id="d3b47-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="d3b47-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3b47-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3b47-113">-DefaultProfile</span></span>
<span data-ttu-id="d3b47-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="d3b47-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d3b47-115">-容錯移轉</span><span class="sxs-lookup"><span data-stu-id="d3b47-115">-Failover</span></span>
<span data-ttu-id="d3b47-116">表示此作業為容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="d3b47-116">Indicates that this operation is a failover.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3b47-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3b47-117">-ResourceGroupName</span></span>
<span data-ttu-id="d3b47-118">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d3b47-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="d3b47-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d3b47-119">-ServerName</span></span>
<span data-ttu-id="d3b47-120">指定 SQL 資料庫伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="d3b47-120">Specifies the name of a SQL database server.</span></span>

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

### <span data-ttu-id="d3b47-121">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="d3b47-121">-VirtualEndpointName</span></span>
<span data-ttu-id="d3b47-122">指定虛擬終點的名稱。</span><span class="sxs-lookup"><span data-stu-id="d3b47-122">Specifies the name of a virtual end point.</span></span>

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

### <span data-ttu-id="d3b47-123">-確認</span><span class="sxs-lookup"><span data-stu-id="d3b47-123">-Confirm</span></span>
<span data-ttu-id="d3b47-124">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="d3b47-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3b47-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3b47-125">-WhatIf</span></span>
<span data-ttu-id="d3b47-126">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d3b47-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3b47-127">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d3b47-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3b47-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3b47-128">CommonParameters</span></span>
<span data-ttu-id="d3b47-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d3b47-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3b47-130">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d3b47-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3b47-131">輸入</span><span class="sxs-lookup"><span data-stu-id="d3b47-131">INPUTS</span></span>

### <span data-ttu-id="d3b47-132">System.String</span><span class="sxs-lookup"><span data-stu-id="d3b47-132">System.String</span></span>

## <span data-ttu-id="d3b47-133">輸出</span><span class="sxs-lookup"><span data-stu-id="d3b47-133">OUTPUTS</span></span>

### <span data-ttu-id="d3b47-134">Microsoft.Azure.Commands.Sql.ServerDazsterRecoveryConfiguration.Model.AzureSqlServerDsterRecoveryConfigurationModel</span><span class="sxs-lookup"><span data-stu-id="d3b47-134">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="d3b47-135">筆記</span><span class="sxs-lookup"><span data-stu-id="d3b47-135">NOTES</span></span>

## <span data-ttu-id="d3b47-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="d3b47-136">RELATED LINKS</span></span>

[<span data-ttu-id="d3b47-137">Get-AzSqlServerD區sterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="d3b47-137">Get-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="d3b47-138">New-AzSqlServerDsterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="d3b47-138">New-AzSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="d3b47-139">Remove-AzSqlServerDsterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="d3b47-139">Remove-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="d3b47-140">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="d3b47-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
