---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 44F8EFF4-8E3D-4657-9D17-2A3F49CEA515
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: c49eb386265dff2650ba9bdb0882d25be98fca0c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100132999"
---
# <span data-ttu-id="3fdf5-101">Set-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="3fdf5-101">Set-AzSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="3fdf5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3fdf5-102">SYNOPSIS</span></span>
<span data-ttu-id="3fdf5-103">修改資料庫伺服器的恢復設定。</span><span class="sxs-lookup"><span data-stu-id="3fdf5-103">Modifies a database server recovery configuration.</span></span>

## <span data-ttu-id="3fdf5-104">句法</span><span class="sxs-lookup"><span data-stu-id="3fdf5-104">SYNTAX</span></span>

```
Set-AzSqlServerDisasterRecoveryConfiguration -VirtualEndpointName <String> [-Failover] [-AllowDataLoss]
 [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3fdf5-105">說明</span><span class="sxs-lookup"><span data-stu-id="3fdf5-105">DESCRIPTION</span></span>
<span data-ttu-id="3fdf5-106">**AzSqlServerDisasterRecoveryConfiguration** Cmdlet 會修改 SQL 資料庫伺服器的恢復設定。</span><span class="sxs-lookup"><span data-stu-id="3fdf5-106">The **Set-AzSqlServerDisasterRecoveryConfiguration** cmdlet modifies a SQL database server recovery configuration.</span></span>

## <span data-ttu-id="3fdf5-107">示例</span><span class="sxs-lookup"><span data-stu-id="3fdf5-107">EXAMPLES</span></span>

## <span data-ttu-id="3fdf5-108">參數</span><span class="sxs-lookup"><span data-stu-id="3fdf5-108">PARAMETERS</span></span>

### <span data-ttu-id="3fdf5-109">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="3fdf5-109">-AllowDataLoss</span></span>
<span data-ttu-id="3fdf5-110">表示容錯移轉作業允許資料遺失。</span><span class="sxs-lookup"><span data-stu-id="3fdf5-110">Indicates that the failover operation permits data loss.</span></span>

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

### <span data-ttu-id="3fdf5-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3fdf5-111">-AsJob</span></span>
<span data-ttu-id="3fdf5-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="3fdf5-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3fdf5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fdf5-113">-DefaultProfile</span></span>
<span data-ttu-id="3fdf5-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="3fdf5-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3fdf5-115">-容錯移轉</span><span class="sxs-lookup"><span data-stu-id="3fdf5-115">-Failover</span></span>
<span data-ttu-id="3fdf5-116">表示此操作為容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="3fdf5-116">Indicates that this operation is a failover.</span></span>

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

### <span data-ttu-id="3fdf5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3fdf5-117">-ResourceGroupName</span></span>
<span data-ttu-id="3fdf5-118">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3fdf5-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="3fdf5-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3fdf5-119">-ServerName</span></span>
<span data-ttu-id="3fdf5-120">指定 SQL 資料庫伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="3fdf5-120">Specifies the name of a SQL database server.</span></span>

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

### <span data-ttu-id="3fdf5-121">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="3fdf5-121">-VirtualEndpointName</span></span>
<span data-ttu-id="3fdf5-122">指定虛擬終點的名稱。</span><span class="sxs-lookup"><span data-stu-id="3fdf5-122">Specifies the name of a virtual end point.</span></span>

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

### <span data-ttu-id="3fdf5-123">-確認</span><span class="sxs-lookup"><span data-stu-id="3fdf5-123">-Confirm</span></span>
<span data-ttu-id="3fdf5-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3fdf5-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3fdf5-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3fdf5-125">-WhatIf</span></span>
<span data-ttu-id="3fdf5-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3fdf5-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3fdf5-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3fdf5-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3fdf5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fdf5-128">CommonParameters</span></span>
<span data-ttu-id="3fdf5-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3fdf5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fdf5-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="3fdf5-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fdf5-131">輸入</span><span class="sxs-lookup"><span data-stu-id="3fdf5-131">INPUTS</span></span>

### <span data-ttu-id="3fdf5-132">System.object</span><span class="sxs-lookup"><span data-stu-id="3fdf5-132">System.String</span></span>

## <span data-ttu-id="3fdf5-133">輸出</span><span class="sxs-lookup"><span data-stu-id="3fdf5-133">OUTPUTS</span></span>

### <span data-ttu-id="3fdf5-134">AzureSqlServerDisasterRecoveryConfigurationModel 中的 [ServerDisasterRecoveryConfiguration]</span><span class="sxs-lookup"><span data-stu-id="3fdf5-134">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="3fdf5-135">筆記</span><span class="sxs-lookup"><span data-stu-id="3fdf5-135">NOTES</span></span>

## <span data-ttu-id="3fdf5-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="3fdf5-136">RELATED LINKS</span></span>

[<span data-ttu-id="3fdf5-137">AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="3fdf5-137">Get-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="3fdf5-138">新-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="3fdf5-138">New-AzSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="3fdf5-139">移除-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="3fdf5-139">Remove-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="3fdf5-140">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="3fdf5-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
