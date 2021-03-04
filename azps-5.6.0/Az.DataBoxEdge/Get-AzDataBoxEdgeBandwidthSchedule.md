---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/get-azdataboxedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeBandwidthSchedule.md
ms.openlocfilehash: bf41be0619998c030a6aec859ff433a3909af083
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914097"
---
# <span data-ttu-id="9614d-101">Get-AzDataBoxEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="9614d-101">Get-AzDataBoxEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="9614d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9614d-102">SYNOPSIS</span></span>
<span data-ttu-id="9614d-103">獲得有關頻寬排程的資訊</span><span class="sxs-lookup"><span data-stu-id="9614d-103">Gets the information about the Bandwidth schedules</span></span>

## <span data-ttu-id="9614d-104">語法</span><span class="sxs-lookup"><span data-stu-id="9614d-104">SYNTAX</span></span>

### <span data-ttu-id="9614d-105">ListParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="9614d-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9614d-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9614d-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9614d-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9614d-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9614d-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9614d-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeBandwidthSchedule [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="9614d-109">描述</span><span class="sxs-lookup"><span data-stu-id="9614d-109">DESCRIPTION</span></span>
<span data-ttu-id="9614d-110">**Get-AzDataBoxEdgeBandwidthSchedule** Cmdlet 會取得有關頻寬排程的資訊。</span><span class="sxs-lookup"><span data-stu-id="9614d-110">The **Get-AzDataBoxEdgeBandwidthSchedule** cmdlet gets the information about the Bandwidth Schedules.</span></span> <span data-ttu-id="9614d-111">您可以指定排程的名稱，以及資源組名和裝置名稱，以取得特定頻寬排程的資訊</span><span class="sxs-lookup"><span data-stu-id="9614d-111">You can specify the Name of a Schedule along with the Resource Group name and Device name to get the information about a specific Bandwidth schedule</span></span>

## <span data-ttu-id="9614d-112">例子</span><span class="sxs-lookup"><span data-stu-id="9614d-112">EXAMPLES</span></span>

### <span data-ttu-id="9614d-113">範例 1</span><span class="sxs-lookup"><span data-stu-id="9614d-113">Example 1</span></span>
```powershell
PS C:\>Get-AzDataBoxEdgeBandwidthSchedule -ResourceGroupname resource-group-name -DeviceName device-name

Name              DaysOfWeek         RateInMbps StartTime StopTime
----              ----------         ---------- --------- --------
schedule-name     Sunday,Saturday    unlimited  13:00:00  14:00:00
Schedule-1        Tuesday,Friday     unlimited  00:00:00  23:59:00
Schedule-2        Thursday           50         00:01:00  05:00:00
```

### <span data-ttu-id="9614d-114">範例 2</span><span class="sxs-lookup"><span data-stu-id="9614d-114">Example 2</span></span>
```powershell
PS C:\>Get-AzDataBoxEdgeBandwidthSchedule -ResourceGroupname resource-group-name -DeviceName device-name -Name Schedule-1

Name              DaysOfWeek      RateInMbps StartTime StopTime
----              ----------      ---------- --------- --------
Schedule-1        Sunday,Saturday unlimited  13:00:00  14:00:00
```

## <span data-ttu-id="9614d-115">參數</span><span class="sxs-lookup"><span data-stu-id="9614d-115">PARAMETERS</span></span>

### <span data-ttu-id="9614d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9614d-116">-DefaultProfile</span></span>
<span data-ttu-id="9614d-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="9614d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9614d-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="9614d-118">-DeviceName</span></span>
<span data-ttu-id="9614d-119">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="9614d-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9614d-120">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="9614d-120">-DeviceObject</span></span>
<span data-ttu-id="9614d-121">請提供對應的裝置物件</span><span class="sxs-lookup"><span data-stu-id="9614d-121">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9614d-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="9614d-122">-Name</span></span>
<span data-ttu-id="9614d-123">資源名稱</span><span class="sxs-lookup"><span data-stu-id="9614d-123">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9614d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9614d-124">-ResourceGroupName</span></span>
<span data-ttu-id="9614d-125">資源組名</span><span class="sxs-lookup"><span data-stu-id="9614d-125">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9614d-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9614d-126">-ResourceId</span></span>
<span data-ttu-id="9614d-127">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="9614d-127">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9614d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9614d-128">CommonParameters</span></span>
<span data-ttu-id="9614d-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9614d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9614d-130">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9614d-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9614d-131">輸入</span><span class="sxs-lookup"><span data-stu-id="9614d-131">INPUTS</span></span>

### <span data-ttu-id="9614d-132">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="9614d-132">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="9614d-133">輸出</span><span class="sxs-lookup"><span data-stu-id="9614d-133">OUTPUTS</span></span>

### <span data-ttu-id="9614d-134">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDBoxEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="9614d-134">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="9614d-135">筆記</span><span class="sxs-lookup"><span data-stu-id="9614d-135">NOTES</span></span>

## <span data-ttu-id="9614d-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="9614d-136">RELATED LINKS</span></span>
