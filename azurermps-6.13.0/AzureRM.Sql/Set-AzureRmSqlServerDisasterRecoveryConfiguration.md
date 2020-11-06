---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 44F8EFF4-8E3D-4657-9D17-2A3F49CEA515
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: 19f7d8adf7e8eae48bb85c19c9f01c61dc741da0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448187"
---
# <span data-ttu-id="b98df-101">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="b98df-101">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="b98df-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b98df-102">SYNOPSIS</span></span>
<span data-ttu-id="b98df-103">修改資料庫伺服器的恢復設定。</span><span class="sxs-lookup"><span data-stu-id="b98df-103">Modifies a database server recovery configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b98df-104">句法</span><span class="sxs-lookup"><span data-stu-id="b98df-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerDisasterRecoveryConfiguration -VirtualEndpointName <String> [-Failover] [-AllowDataLoss]
 [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b98df-105">說明</span><span class="sxs-lookup"><span data-stu-id="b98df-105">DESCRIPTION</span></span>
<span data-ttu-id="b98df-106">**AzureRmSqlServerDisasterRecoveryConfiguration** Cmdlet 會修改 SQL 資料庫伺服器的恢復設定。</span><span class="sxs-lookup"><span data-stu-id="b98df-106">The **Set-AzureRmSqlServerDisasterRecoveryConfiguration** cmdlet modifies a SQL database server recovery configuration.</span></span>

## <span data-ttu-id="b98df-107">示例</span><span class="sxs-lookup"><span data-stu-id="b98df-107">EXAMPLES</span></span>

## <span data-ttu-id="b98df-108">參數</span><span class="sxs-lookup"><span data-stu-id="b98df-108">PARAMETERS</span></span>

### <span data-ttu-id="b98df-109">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="b98df-109">-AllowDataLoss</span></span>
<span data-ttu-id="b98df-110">表示容錯移轉作業允許資料遺失。</span><span class="sxs-lookup"><span data-stu-id="b98df-110">Indicates that the failover operation permits data loss.</span></span>

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

### <span data-ttu-id="b98df-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b98df-111">-AsJob</span></span>
<span data-ttu-id="b98df-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b98df-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b98df-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b98df-113">-DefaultProfile</span></span>
<span data-ttu-id="b98df-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="b98df-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b98df-115">-容錯移轉</span><span class="sxs-lookup"><span data-stu-id="b98df-115">-Failover</span></span>
<span data-ttu-id="b98df-116">表示此操作為容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="b98df-116">Indicates that this operation is a failover.</span></span>

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

### <span data-ttu-id="b98df-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b98df-117">-ResourceGroupName</span></span>
<span data-ttu-id="b98df-118">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b98df-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="b98df-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b98df-119">-ServerName</span></span>
<span data-ttu-id="b98df-120">指定 SQL 資料庫伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="b98df-120">Specifies the name of a SQL database server.</span></span>

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

### <span data-ttu-id="b98df-121">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="b98df-121">-VirtualEndpointName</span></span>
<span data-ttu-id="b98df-122">指定虛擬終點的名稱。</span><span class="sxs-lookup"><span data-stu-id="b98df-122">Specifies the name of a virtual end point.</span></span>

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

### <span data-ttu-id="b98df-123">-確認</span><span class="sxs-lookup"><span data-stu-id="b98df-123">-Confirm</span></span>
<span data-ttu-id="b98df-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b98df-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b98df-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b98df-125">-WhatIf</span></span>
<span data-ttu-id="b98df-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b98df-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b98df-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b98df-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b98df-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b98df-128">CommonParameters</span></span>
<span data-ttu-id="b98df-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b98df-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b98df-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b98df-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b98df-131">輸入</span><span class="sxs-lookup"><span data-stu-id="b98df-131">INPUTS</span></span>

### <span data-ttu-id="b98df-132">System.object</span><span class="sxs-lookup"><span data-stu-id="b98df-132">System.String</span></span>

## <span data-ttu-id="b98df-133">輸出</span><span class="sxs-lookup"><span data-stu-id="b98df-133">OUTPUTS</span></span>

### <span data-ttu-id="b98df-134">AzureSqlServerDisasterRecoveryConfigurationModel 中的 [ServerDisasterRecoveryConfiguration]</span><span class="sxs-lookup"><span data-stu-id="b98df-134">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="b98df-135">筆記</span><span class="sxs-lookup"><span data-stu-id="b98df-135">NOTES</span></span>

## <span data-ttu-id="b98df-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="b98df-136">RELATED LINKS</span></span>

[<span data-ttu-id="b98df-137">AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="b98df-137">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="b98df-138">新-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="b98df-138">New-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="b98df-139">移除-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="b98df-139">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="b98df-140">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="b98df-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
