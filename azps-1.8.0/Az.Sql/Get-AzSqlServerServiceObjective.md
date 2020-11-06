---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: AC2D64B9-5BCD-45D3-8650-538633F5BBBC
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverserviceobjective
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerServiceObjective.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerServiceObjective.md
ms.openlocfilehash: 5b9bd64eb4d83af9ca150e5eb9ac04479c7fdf5c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93614880"
---
# <span data-ttu-id="1a4a7-101">Get-AzSqlServerServiceObjective</span><span class="sxs-lookup"><span data-stu-id="1a4a7-101">Get-AzSqlServerServiceObjective</span></span>

## <span data-ttu-id="1a4a7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1a4a7-102">SYNOPSIS</span></span>
<span data-ttu-id="1a4a7-103">取得 Azure SQL 資料庫伺服器的服務目標。</span><span class="sxs-lookup"><span data-stu-id="1a4a7-103">Gets service objectives for an Azure SQL Database server.</span></span>

## <span data-ttu-id="1a4a7-104">句法</span><span class="sxs-lookup"><span data-stu-id="1a4a7-104">SYNTAX</span></span>

### <span data-ttu-id="1a4a7-105">ByLocation (預設) </span><span class="sxs-lookup"><span data-stu-id="1a4a7-105">ByLocation (Default)</span></span>
```
Get-AzSqlServerServiceObjective [[-ServiceObjectiveName] <String>] -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a4a7-106">ByServer</span><span class="sxs-lookup"><span data-stu-id="1a4a7-106">ByServer</span></span>
```
Get-AzSqlServerServiceObjective [[-ServiceObjectiveName] <String>] [-ResourceGroupName] <String>
 [-ServerName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a4a7-107">說明</span><span class="sxs-lookup"><span data-stu-id="1a4a7-107">DESCRIPTION</span></span>
<span data-ttu-id="1a4a7-108">**AzSqlServerServiceObjective** Cmdlet 會取得 Azure SQL 資料庫伺服器可用的服務目標。</span><span class="sxs-lookup"><span data-stu-id="1a4a7-108">The **Get-AzSqlServerServiceObjective** cmdlet gets the available service objectives for an Azure SQL Database server.</span></span>

## <span data-ttu-id="1a4a7-109">示例</span><span class="sxs-lookup"><span data-stu-id="1a4a7-109">EXAMPLES</span></span>

### <span data-ttu-id="1a4a7-110">範例1：取得服務目標</span><span class="sxs-lookup"><span data-stu-id="1a4a7-110">Example 1: Get service objectives</span></span>
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

<span data-ttu-id="1a4a7-111">這個命令會取得名為 Server01 的伺服器服務目標。</span><span class="sxs-lookup"><span data-stu-id="1a4a7-111">This command gets the service objectives for the server named Server01.</span></span>

### <span data-ttu-id="1a4a7-112">範例2：使用篩選取得服務目標</span><span class="sxs-lookup"><span data-stu-id="1a4a7-112">Example 2: Get service objectives using filtering</span></span>
```
PS C:\>Get-AzSqlServerServiceObjective -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ServiceObjectiveName "P*"
ServiceObjectiveName SkuName       Edition          Family Capacity CapacityUnit Enabled
-------------------- -------       -------          ------ -------- ------------ -------
P1                   Premium       Premium                 125      DTU          True
P2                   Premium       Premium                 250      DTU          True
```

<span data-ttu-id="1a4a7-113">這個命令會取得以「System」開頭的名為 Server01 的伺服器服務目標。</span><span class="sxs-lookup"><span data-stu-id="1a4a7-113">This command gets the service objectives for the server named Server01 that start with "System".</span></span>

### <span data-ttu-id="1a4a7-114">範例3：取得某個位置的服務目標</span><span class="sxs-lookup"><span data-stu-id="1a4a7-114">Example 3: Get service objectives for a location</span></span>
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

<span data-ttu-id="1a4a7-115">這個命令會取得指定 Azure 區域的服務目標。</span><span class="sxs-lookup"><span data-stu-id="1a4a7-115">This command gets the service objectives for a specified Azure region.</span></span>

## <span data-ttu-id="1a4a7-116">參數</span><span class="sxs-lookup"><span data-stu-id="1a4a7-116">PARAMETERS</span></span>

### <span data-ttu-id="1a4a7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a4a7-117">-DefaultProfile</span></span>
<span data-ttu-id="1a4a7-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="1a4a7-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1a4a7-119">-位置</span><span class="sxs-lookup"><span data-stu-id="1a4a7-119">-Location</span></span>
<span data-ttu-id="1a4a7-120">要取得服務目標的位置名稱。</span><span class="sxs-lookup"><span data-stu-id="1a4a7-120">The name of the Location for which to get the service objectives.</span></span>

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

### <span data-ttu-id="1a4a7-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a4a7-121">-ResourceGroupName</span></span>
<span data-ttu-id="1a4a7-122">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1a4a7-122">Specifies the name of a resource group.</span></span>
<span data-ttu-id="1a4a7-123">這個 Cmdlet 會取得指派給此資源之 SQL 資料庫伺服器的服務目標。</span><span class="sxs-lookup"><span data-stu-id="1a4a7-123">This cmdlet gets service objectives for a SQL Database server assigned to this resource.</span></span>

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

### <span data-ttu-id="1a4a7-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1a4a7-124">-ServerName</span></span>
<span data-ttu-id="1a4a7-125">指定 SQL 資料庫 SQL 資料庫伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="1a4a7-125">Specifies the name of a SQL Database SQL Database server.</span></span>

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

### <span data-ttu-id="1a4a7-126">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="1a4a7-126">-ServiceObjectiveName</span></span>
<span data-ttu-id="1a4a7-127">指定 Azure SQL 資料庫伺服器的服務目標名稱。</span><span class="sxs-lookup"><span data-stu-id="1a4a7-127">Specifies the name of a service objective for an Azure SQL Database server.</span></span>
<span data-ttu-id="1a4a7-128">此參數可接受的值為： Basic、S0、S1、S2、P1、P2 及 P3。</span><span class="sxs-lookup"><span data-stu-id="1a4a7-128">The acceptable values for this parameter are: Basic, S0, S1, S2, P1, P2, and P3.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="1a4a7-129">-確認</span><span class="sxs-lookup"><span data-stu-id="1a4a7-129">-Confirm</span></span>
<span data-ttu-id="1a4a7-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1a4a7-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a4a7-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a4a7-131">-WhatIf</span></span>
<span data-ttu-id="1a4a7-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1a4a7-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a4a7-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1a4a7-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a4a7-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a4a7-134">CommonParameters</span></span>
<span data-ttu-id="1a4a7-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1a4a7-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a4a7-136">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="1a4a7-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a4a7-137">輸入</span><span class="sxs-lookup"><span data-stu-id="1a4a7-137">INPUTS</span></span>

### <span data-ttu-id="1a4a7-138">System.object</span><span class="sxs-lookup"><span data-stu-id="1a4a7-138">System.String</span></span>

## <span data-ttu-id="1a4a7-139">輸出</span><span class="sxs-lookup"><span data-stu-id="1a4a7-139">OUTPUTS</span></span>

### <span data-ttu-id="1a4a7-140">AzureSqlServerServiceObjectiveModel 中的 [ServiceObjective]</span><span class="sxs-lookup"><span data-stu-id="1a4a7-140">Microsoft.Azure.Commands.Sql.ServiceObjective.Model.AzureSqlServerServiceObjectiveModel</span></span>

## <span data-ttu-id="1a4a7-141">筆記</span><span class="sxs-lookup"><span data-stu-id="1a4a7-141">NOTES</span></span>

## <span data-ttu-id="1a4a7-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="1a4a7-142">RELATED LINKS</span></span>

[<span data-ttu-id="1a4a7-143">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="1a4a7-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


