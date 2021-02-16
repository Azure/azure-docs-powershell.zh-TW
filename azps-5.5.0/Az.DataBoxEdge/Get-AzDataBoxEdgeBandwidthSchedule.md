---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeBandwidthSchedule.md
ms.openlocfilehash: e3453e3359bb800180ebdeb3fa5158b890fd237a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100129582"
---
# <span data-ttu-id="5d001-101">Get-AzDataBoxEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="5d001-101">Get-AzDataBoxEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="5d001-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5d001-102">SYNOPSIS</span></span>
<span data-ttu-id="5d001-103">取得頻寬排程的相關資訊</span><span class="sxs-lookup"><span data-stu-id="5d001-103">Gets the information about the Bandwidth schedules</span></span>

## <span data-ttu-id="5d001-104">句法</span><span class="sxs-lookup"><span data-stu-id="5d001-104">SYNTAX</span></span>

### <span data-ttu-id="5d001-105">ListParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="5d001-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5d001-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d001-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5d001-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d001-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5d001-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d001-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeBandwidthSchedule [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="5d001-109">說明</span><span class="sxs-lookup"><span data-stu-id="5d001-109">DESCRIPTION</span></span>
<span data-ttu-id="5d001-110">**AzDataBoxEdgeBandwidthSchedule** Cmdlet 會取得頻寬排程的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="5d001-110">The **Get-AzDataBoxEdgeBandwidthSchedule** cmdlet gets the information about the Bandwidth Schedules.</span></span> <span data-ttu-id="5d001-111">您可以指定排程的名稱以及資源群組名稱和裝置名稱，以取得特定頻寬排程的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="5d001-111">You can specify the Name of a Schedule along with the Resource Group name and Device name to get the information about a specific Bandwidth schedule</span></span>

## <span data-ttu-id="5d001-112">示例</span><span class="sxs-lookup"><span data-stu-id="5d001-112">EXAMPLES</span></span>

### <span data-ttu-id="5d001-113">範例1</span><span class="sxs-lookup"><span data-stu-id="5d001-113">Example 1</span></span>
```powershell
PS C:\>Get-AzDataBoxEdgeBandwidthSchedule -ResourceGroupname resource-group-name -DeviceName device-name

Name              DaysOfWeek         RateInMbps StartTime StopTime
----              ----------         ---------- --------- --------
schedule-name     Sunday,Saturday    unlimited  13:00:00  14:00:00
Schedule-1        Tuesday,Friday     unlimited  00:00:00  23:59:00
Schedule-2        Thursday           50         00:01:00  05:00:00
```

### <span data-ttu-id="5d001-114">範例2</span><span class="sxs-lookup"><span data-stu-id="5d001-114">Example 2</span></span>
```powershell
PS C:\>Get-AzDataBoxEdgeBandwidthSchedule -ResourceGroupname resource-group-name -DeviceName device-name -Name Schedule-1

Name              DaysOfWeek      RateInMbps StartTime StopTime
----              ----------      ---------- --------- --------
Schedule-1        Sunday,Saturday unlimited  13:00:00  14:00:00
```

## <span data-ttu-id="5d001-115">參數</span><span class="sxs-lookup"><span data-stu-id="5d001-115">PARAMETERS</span></span>

### <span data-ttu-id="5d001-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d001-116">-DefaultProfile</span></span>
<span data-ttu-id="5d001-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5d001-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d001-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="5d001-118">-DeviceName</span></span>
<span data-ttu-id="5d001-119">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="5d001-119">Device Name</span></span>

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

### <span data-ttu-id="5d001-120">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="5d001-120">-DeviceObject</span></span>
<span data-ttu-id="5d001-121">請提供相對應的裝置物件</span><span class="sxs-lookup"><span data-stu-id="5d001-121">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="5d001-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="5d001-122">-Name</span></span>
<span data-ttu-id="5d001-123">資源名稱</span><span class="sxs-lookup"><span data-stu-id="5d001-123">Resource Name</span></span>

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

### <span data-ttu-id="5d001-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d001-124">-ResourceGroupName</span></span>
<span data-ttu-id="5d001-125">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="5d001-125">Resource Group Name</span></span>

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

### <span data-ttu-id="5d001-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5d001-126">-ResourceId</span></span>
<span data-ttu-id="5d001-127">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="5d001-127">Azure ResourceId</span></span>

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

### <span data-ttu-id="5d001-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d001-128">CommonParameters</span></span>
<span data-ttu-id="5d001-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5d001-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d001-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="5d001-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d001-131">輸入</span><span class="sxs-lookup"><span data-stu-id="5d001-131">INPUTS</span></span>

### <span data-ttu-id="5d001-132">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="5d001-132">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="5d001-133">輸出</span><span class="sxs-lookup"><span data-stu-id="5d001-133">OUTPUTS</span></span>

### <span data-ttu-id="5d001-134">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="5d001-134">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="5d001-135">筆記</span><span class="sxs-lookup"><span data-stu-id="5d001-135">NOTES</span></span>

## <span data-ttu-id="5d001-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="5d001-136">RELATED LINKS</span></span>
