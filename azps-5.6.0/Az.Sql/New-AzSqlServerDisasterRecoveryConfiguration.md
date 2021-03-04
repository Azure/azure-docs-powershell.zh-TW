---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 1D8E8599-113C-4852-8416-1F3359071047
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: e9fd76953d4cf760c501370b77be3301cb043524
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907050"
---
# <span data-ttu-id="06342-101">New-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="06342-101">New-AzSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="06342-102">簡介</span><span class="sxs-lookup"><span data-stu-id="06342-102">SYNOPSIS</span></span>
<span data-ttu-id="06342-103">建立資料庫伺服器系統復原組。</span><span class="sxs-lookup"><span data-stu-id="06342-103">Creates a database server system recovery configuration.</span></span>

## <span data-ttu-id="06342-104">語法</span><span class="sxs-lookup"><span data-stu-id="06342-104">SYNTAX</span></span>

```
New-AzSqlServerDisasterRecoveryConfiguration -VirtualEndpointName <String> -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-FailoverPolicy <String>] [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="06342-105">描述</span><span class="sxs-lookup"><span data-stu-id="06342-105">DESCRIPTION</span></span>
<span data-ttu-id="06342-106">**New-AzSqlServerDsterRecoveryConfiguration** Cmdlet 會建立 SQL 資料庫伺服器系統復原組式。</span><span class="sxs-lookup"><span data-stu-id="06342-106">The **New-AzSqlServerDisasterRecoveryConfiguration** cmdlet creates a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="06342-107">例子</span><span class="sxs-lookup"><span data-stu-id="06342-107">EXAMPLES</span></span>

## <span data-ttu-id="06342-108">參數</span><span class="sxs-lookup"><span data-stu-id="06342-108">PARAMETERS</span></span>

### <span data-ttu-id="06342-109">-AsJob</span><span class="sxs-lookup"><span data-stu-id="06342-109">-AsJob</span></span>
<span data-ttu-id="06342-110">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="06342-110">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="06342-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06342-111">-DefaultProfile</span></span>
<span data-ttu-id="06342-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="06342-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="06342-113">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="06342-113">-FailoverPolicy</span></span>
<span data-ttu-id="06342-114">指定容錯移轉政策。</span><span class="sxs-lookup"><span data-stu-id="06342-114">Specifies the failover policy.</span></span>

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

### <span data-ttu-id="06342-115">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06342-115">-PartnerResourceGroupName</span></span>
<span data-ttu-id="06342-116">指定合作夥伴資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="06342-116">Specifies the name of the partner resource group.</span></span>

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

### <span data-ttu-id="06342-117">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="06342-117">-PartnerServerName</span></span>
<span data-ttu-id="06342-118">指定合作夥伴伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="06342-118">Specifies the name of the partner server.</span></span>

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

### <span data-ttu-id="06342-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06342-119">-ResourceGroupName</span></span>
<span data-ttu-id="06342-120">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="06342-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="06342-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="06342-121">-ServerName</span></span>
<span data-ttu-id="06342-122">指定伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="06342-122">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="06342-123">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="06342-123">-VirtualEndpointName</span></span>
<span data-ttu-id="06342-124">指定虛擬結束點的名稱。</span><span class="sxs-lookup"><span data-stu-id="06342-124">Specifies the name of the virtual end point.</span></span>

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

### <span data-ttu-id="06342-125">-確認</span><span class="sxs-lookup"><span data-stu-id="06342-125">-Confirm</span></span>
<span data-ttu-id="06342-126">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="06342-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06342-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06342-127">-WhatIf</span></span>
<span data-ttu-id="06342-128">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="06342-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06342-129">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="06342-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06342-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06342-130">CommonParameters</span></span>
<span data-ttu-id="06342-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="06342-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06342-132">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="06342-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06342-133">輸入</span><span class="sxs-lookup"><span data-stu-id="06342-133">INPUTS</span></span>

### <span data-ttu-id="06342-134">System.String</span><span class="sxs-lookup"><span data-stu-id="06342-134">System.String</span></span>

## <span data-ttu-id="06342-135">輸出</span><span class="sxs-lookup"><span data-stu-id="06342-135">OUTPUTS</span></span>

### <span data-ttu-id="06342-136">Microsoft.Azure.Commands.Sql.ServerDazsterRecoveryConfiguration.Model.AzureSqlServerDsterRecoveryConfigurationModel</span><span class="sxs-lookup"><span data-stu-id="06342-136">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="06342-137">筆記</span><span class="sxs-lookup"><span data-stu-id="06342-137">NOTES</span></span>

## <span data-ttu-id="06342-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="06342-138">RELATED LINKS</span></span>

[<span data-ttu-id="06342-139">Get-AzSqlServerD區sterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="06342-139">Get-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="06342-140">Remove-AzSqlServerDsterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="06342-140">Remove-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="06342-141">Set-AzSqlServerD區sterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="06342-141">Set-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="06342-142">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="06342-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
