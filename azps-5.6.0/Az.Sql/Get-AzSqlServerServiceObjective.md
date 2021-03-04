---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: AC2D64B9-5BCD-45D3-8650-538633F5BBBC
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlserverserviceobjective
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerServiceObjective.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerServiceObjective.md
ms.openlocfilehash: 031b20aa24c66817d199be5d12049d52222d23b1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906366"
---
# <span data-ttu-id="57208-101">Get-AzSqlServerServiceObjective</span><span class="sxs-lookup"><span data-stu-id="57208-101">Get-AzSqlServerServiceObjective</span></span>

## <span data-ttu-id="57208-102">簡介</span><span class="sxs-lookup"><span data-stu-id="57208-102">SYNOPSIS</span></span>
<span data-ttu-id="57208-103">獲得 Azure SQL Database 伺服器的服務目標。</span><span class="sxs-lookup"><span data-stu-id="57208-103">Gets service objectives for an Azure SQL Database server.</span></span>

## <span data-ttu-id="57208-104">語法</span><span class="sxs-lookup"><span data-stu-id="57208-104">SYNTAX</span></span>

### <span data-ttu-id="57208-105">ByLocation (預設) </span><span class="sxs-lookup"><span data-stu-id="57208-105">ByLocation (Default)</span></span>
```
Get-AzSqlServerServiceObjective [[-ServiceObjectiveName] <String>] -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57208-106">ByServer</span><span class="sxs-lookup"><span data-stu-id="57208-106">ByServer</span></span>
```
Get-AzSqlServerServiceObjective [[-ServiceObjectiveName] <String>] [-ResourceGroupName] <String>
 [-ServerName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57208-107">描述</span><span class="sxs-lookup"><span data-stu-id="57208-107">DESCRIPTION</span></span>
<span data-ttu-id="57208-108">**Get-AzSqlServerServiceObjective Cmdlet** 取得 Azure SQL Database 伺服器的可用服務目標。</span><span class="sxs-lookup"><span data-stu-id="57208-108">The **Get-AzSqlServerServiceObjective** cmdlet gets the available service objectives for an Azure SQL Database server.</span></span>

## <span data-ttu-id="57208-109">例子</span><span class="sxs-lookup"><span data-stu-id="57208-109">EXAMPLES</span></span>

### <span data-ttu-id="57208-110">範例 1：取得服務目標</span><span class="sxs-lookup"><span data-stu-id="57208-110">Example 1: Get service objectives</span></span>
```
PS C:\>Get-AzSqlServerServiceObjective -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
serviceObjectiveName SkuName       Edition          Family Capacity CapacityUnit Enabled
-------------------- -------       -------          ------ -------- ------------ -------
System               System        System                  0        DTU          False
Free                 Free          Free                    5        DTU          True
Basic                Basic         Basic                   5        DTU          True
S0                   Standard      Standard                10       DTU          True
S1                   Standard      Standard                20       DTU          True
P1                   Premium       Premium                 125      DTU          True
P2                   Premium       Premium                 250      DTU          True
DW100c               DataWarehouse DataWarehouse           900      DTU          False
GP_Gen4_1            GP_Gen4       GeneralPurpose   Gen4   1        VCores       True
GP_Gen5_2            GP_Gen5       GeneralPurpose   Gen5   2        VCores       True
BC_Gen4_1            BC_Gen4       BusinessCritical Gen4   1        VCores       True
BC_Gen5_4            BC_Gen5       BusinessCritical Gen5   4        VCores       True
```

<span data-ttu-id="57208-111">此命令會獲得伺服器名稱為 Server01 的服務目標。</span><span class="sxs-lookup"><span data-stu-id="57208-111">This command gets the service objectives for the server named Server01.</span></span>

### <span data-ttu-id="57208-112">範例 2：使用篩選取得服務目標</span><span class="sxs-lookup"><span data-stu-id="57208-112">Example 2: Get service objectives using filtering</span></span>
```
PS C:\>Get-AzSqlServerServiceObjective -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ServiceObjectiveName "P*"
ServiceObjectiveName SkuName       Edition          Family Capacity CapacityUnit Enabled
-------------------- -------       -------          ------ -------- ------------ -------
P1                   Premium       Premium                 125      DTU          True
P2                   Premium       Premium                 250      DTU          True
```

<span data-ttu-id="57208-113">此命令會針對名稱為 「System」的伺服器，獲得服務目標，伺服器名稱為 Server01。</span><span class="sxs-lookup"><span data-stu-id="57208-113">This command gets the service objectives for the server named Server01 that start with "System".</span></span>

### <span data-ttu-id="57208-114">範例 3：取得位置的服務目標</span><span class="sxs-lookup"><span data-stu-id="57208-114">Example 3: Get service objectives for a location</span></span>
```
PS C:\>Get-AzSqlServerServiceObjective -Location "west us"
serviceObjectiveName SkuName       Edition          Family Capacity CapacityUnit Enabled
-------------------- -------       -------          ------ -------- ------------ -------
System               System        System                  0        DTU          False
Free                 Free          Free                    5        DTU          True
Basic                Basic         Basic                   5        DTU          True
S0                   Standard      Standard                10       DTU          True
S1                   Standard      Standard                20       DTU          True
P1                   Premium       Premium                 125      DTU          True
P2                   Premium       Premium                 250      DTU          True
DW100c               DataWarehouse DataWarehouse           900      DTU          False
GP_Gen4_1            GP_Gen4       GeneralPurpose   Gen4   1        VCores       True
GP_Gen5_2            GP_Gen5       GeneralPurpose   Gen5   2        VCores       True
BC_Gen4_1            BC_Gen4       BusinessCritical Gen4   1        VCores       True
BC_Gen5_4            BC_Gen5       BusinessCritical Gen5   4        VCores       True
```

<span data-ttu-id="57208-115">此命令會獲得指定 Azure 地區的服務目標。</span><span class="sxs-lookup"><span data-stu-id="57208-115">This command gets the service objectives for a specified Azure region.</span></span>

## <span data-ttu-id="57208-116">參數</span><span class="sxs-lookup"><span data-stu-id="57208-116">PARAMETERS</span></span>

### <span data-ttu-id="57208-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57208-117">-DefaultProfile</span></span>
<span data-ttu-id="57208-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="57208-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="57208-119">-位置</span><span class="sxs-lookup"><span data-stu-id="57208-119">-Location</span></span>
<span data-ttu-id="57208-120">取得服務目標的位置名稱。</span><span class="sxs-lookup"><span data-stu-id="57208-120">The name of the Location for which to get the service objectives.</span></span>

```yaml
Type: System.String
Parameter Sets: ByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57208-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57208-121">-ResourceGroupName</span></span>
<span data-ttu-id="57208-122">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="57208-122">Specifies the name of a resource group.</span></span>
<span data-ttu-id="57208-123">此 Cmdlet 會針對指派給此資源的 SQL Database 伺服器，獲得服務目標。</span><span class="sxs-lookup"><span data-stu-id="57208-123">This cmdlet gets service objectives for a SQL Database server assigned to this resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServer
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57208-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="57208-124">-ServerName</span></span>
<span data-ttu-id="57208-125">指定 SQL Database SQL Database 伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="57208-125">Specifies the name of a SQL Database SQL Database server.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServer
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57208-126">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="57208-126">-ServiceObjectiveName</span></span>
<span data-ttu-id="57208-127">指定 Azure SQL Database 伺服器的服務目標名稱。</span><span class="sxs-lookup"><span data-stu-id="57208-127">Specifies the name of a service objective for an Azure SQL Database server.</span></span>
<span data-ttu-id="57208-128">此參數可接受的值為：基本、S0、S1、S2、P1、P2 和 P3。</span><span class="sxs-lookup"><span data-stu-id="57208-128">The acceptable values for this parameter are: Basic, S0, S1, S2, P1, P2, and P3.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57208-129">-確認</span><span class="sxs-lookup"><span data-stu-id="57208-129">-Confirm</span></span>
<span data-ttu-id="57208-130">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="57208-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57208-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57208-131">-WhatIf</span></span>
<span data-ttu-id="57208-132">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="57208-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57208-133">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="57208-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57208-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57208-134">CommonParameters</span></span>
<span data-ttu-id="57208-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="57208-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57208-136">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="57208-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57208-137">輸入</span><span class="sxs-lookup"><span data-stu-id="57208-137">INPUTS</span></span>

### <span data-ttu-id="57208-138">System.String</span><span class="sxs-lookup"><span data-stu-id="57208-138">System.String</span></span>

## <span data-ttu-id="57208-139">輸出</span><span class="sxs-lookup"><span data-stu-id="57208-139">OUTPUTS</span></span>

### <span data-ttu-id="57208-140">Microsoft.Azure.Commands.Sql.ServiceObjective.Model.AzureSqlServerServiceObjectiveModel</span><span class="sxs-lookup"><span data-stu-id="57208-140">Microsoft.Azure.Commands.Sql.ServiceObjective.Model.AzureSqlServerServiceObjectiveModel</span></span>

## <span data-ttu-id="57208-141">筆記</span><span class="sxs-lookup"><span data-stu-id="57208-141">NOTES</span></span>

## <span data-ttu-id="57208-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="57208-142">RELATED LINKS</span></span>

[<span data-ttu-id="57208-143">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="57208-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


