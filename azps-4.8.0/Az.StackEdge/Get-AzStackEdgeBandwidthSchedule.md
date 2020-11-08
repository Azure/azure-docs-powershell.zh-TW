---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeBandwidthSchedule.md
ms.openlocfilehash: 5f2dfec045364852d9846fa3bb35bd903c78ca5a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93970053"
---
# <span data-ttu-id="79753-101">Get-AzStackEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="79753-101">Get-AzStackEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="79753-102">摘要</span><span class="sxs-lookup"><span data-stu-id="79753-102">SYNOPSIS</span></span>
<span data-ttu-id="79753-103">取得頻寬排程的相關資訊</span><span class="sxs-lookup"><span data-stu-id="79753-103">Gets the information about the Bandwidth schedules</span></span>

## <span data-ttu-id="79753-104">句法</span><span class="sxs-lookup"><span data-stu-id="79753-104">SYNTAX</span></span>

### <span data-ttu-id="79753-105">ListParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="79753-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="79753-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="79753-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeBandwidthSchedule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="79753-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="79753-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="79753-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="79753-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeBandwidthSchedule [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="79753-109">說明</span><span class="sxs-lookup"><span data-stu-id="79753-109">DESCRIPTION</span></span>
<span data-ttu-id="79753-110">**AzStackEdgeBandwidthSchedule** Cmdlet 會取得頻寬排程的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="79753-110">The **Get-AzStackEdgeBandwidthSchedule** cmdlet gets the information about the Bandwidth Schedules.</span></span> <span data-ttu-id="79753-111">您可以指定排程的名稱以及資源群組名稱和裝置名稱，以取得特定頻寬排程的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="79753-111">You can specify the Name of a Schedule along with the Resource Group name and Device name to get the information about a specific Bandwidth schedule</span></span>

## <span data-ttu-id="79753-112">示例</span><span class="sxs-lookup"><span data-stu-id="79753-112">EXAMPLES</span></span>

### <span data-ttu-id="79753-113">範例1</span><span class="sxs-lookup"><span data-stu-id="79753-113">Example 1</span></span>
```powershell
PS C:\>Get-AzStackEdgeBandwidthSchedule -ResourceGroupname resource-group-name -DeviceName device-name

Name              DaysOfWeek         RateInMbps StartTime StopTime
----              ----------         ---------- --------- --------
schedule-name     Sunday,Saturday    unlimited  13:00:00  14:00:00
Schedule-1        Tuesday,Friday     unlimited  00:00:00  23:59:00
Schedule-2        Thursday           50         00:01:00  05:00:00
```

### <span data-ttu-id="79753-114">範例2</span><span class="sxs-lookup"><span data-stu-id="79753-114">Example 2</span></span>
```powershell
PS C:\>Get-AzStackEdgeBandwidthSchedule -ResourceGroupname resource-group-name -DeviceName device-name -Name Schedule-1

Name              DaysOfWeek      RateInMbps StartTime StopTime
----              ----------      ---------- --------- --------
Schedule-1        Sunday,Saturday unlimited  13:00:00  14:00:00
```

## <span data-ttu-id="79753-115">參數</span><span class="sxs-lookup"><span data-stu-id="79753-115">PARAMETERS</span></span>

### <span data-ttu-id="79753-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79753-116">-DefaultProfile</span></span>
<span data-ttu-id="79753-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="79753-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79753-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="79753-118">-DeviceName</span></span>
<span data-ttu-id="79753-119">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="79753-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79753-120">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="79753-120">-DeviceObject</span></span>
<span data-ttu-id="79753-121">請提供相對應的裝置物件</span><span class="sxs-lookup"><span data-stu-id="79753-121">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice
Parameter Sets: GetByParentObjectParameterSet
Aliases: Device

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="79753-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="79753-122">-Name</span></span>
<span data-ttu-id="79753-123">資源名稱</span><span class="sxs-lookup"><span data-stu-id="79753-123">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: BandwidthScheduleName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases: BandwidthScheduleName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79753-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79753-124">-ResourceGroupName</span></span>
<span data-ttu-id="79753-125">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="79753-125">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79753-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="79753-126">-ResourceId</span></span>
<span data-ttu-id="79753-127">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="79753-127">Azure ResourceId</span></span>

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

### <span data-ttu-id="79753-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79753-128">CommonParameters</span></span>
<span data-ttu-id="79753-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="79753-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79753-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="79753-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79753-131">輸入</span><span class="sxs-lookup"><span data-stu-id="79753-131">INPUTS</span></span>

### <span data-ttu-id="79753-132">PSStackEdgeDevice （StackEdge）的</span><span class="sxs-lookup"><span data-stu-id="79753-132">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="79753-133">輸出</span><span class="sxs-lookup"><span data-stu-id="79753-133">OUTPUTS</span></span>

### <span data-ttu-id="79753-134">PSStackEdgeBandWidthSchedule （StackEdge）的</span><span class="sxs-lookup"><span data-stu-id="79753-134">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="79753-135">筆記</span><span class="sxs-lookup"><span data-stu-id="79753-135">NOTES</span></span>

## <span data-ttu-id="79753-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="79753-136">RELATED LINKS</span></span>
