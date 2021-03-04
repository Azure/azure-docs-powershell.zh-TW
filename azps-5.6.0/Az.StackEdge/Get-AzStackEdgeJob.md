---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/get-azstackedgejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeJob.md
ms.openlocfilehash: 14e19068d3634acfd558f976b13661af28495321
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916349"
---
# <span data-ttu-id="d3152-101">Get-AzStackEdgeJob</span><span class="sxs-lookup"><span data-stu-id="d3152-101">Get-AzStackEdgeJob</span></span>

## <span data-ttu-id="d3152-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d3152-102">SYNOPSIS</span></span>
<span data-ttu-id="d3152-103">在裝置上排程工作。</span><span class="sxs-lookup"><span data-stu-id="d3152-103">Gets the jobs scheduled on a device.</span></span>

## <span data-ttu-id="d3152-104">語法</span><span class="sxs-lookup"><span data-stu-id="d3152-104">SYNTAX</span></span>

### <span data-ttu-id="d3152-105">GetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="d3152-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzStackEdgeJob [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d3152-106">GetByResourceIdObject</span><span class="sxs-lookup"><span data-stu-id="d3152-106">GetByResourceIdObject</span></span>
```
Get-AzStackEdgeJob -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d3152-107">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d3152-107">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeJob [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="d3152-108">描述</span><span class="sxs-lookup"><span data-stu-id="d3152-108">DESCRIPTION</span></span>
<span data-ttu-id="d3152-109">**Get-AzStackEdgeJob** Cmdlet 會取得 Stack Edge 裝置上的使用中工作。</span><span class="sxs-lookup"><span data-stu-id="d3152-109">The **Get-AzStackEdgeJob** cmdlet gets the active jobs on a Stack Edge device.</span></span> <span data-ttu-id="d3152-110">您可以提及 Name 參數，以取得特定工作的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="d3152-110">You can mention the Name parameter to get details of a specific job.</span></span>

## <span data-ttu-id="d3152-111">例子</span><span class="sxs-lookup"><span data-stu-id="d3152-111">EXAMPLES</span></span>

### <span data-ttu-id="d3152-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="d3152-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStackEdgeJob -ResourceGroupName resourceGroupName -DeviceName deviceName -Name 1f2d8f1b-9104-49c3-b780-76db9abe7bd1
Name                                   Device-Name    status
------------------                     -------------  -------
1f2d8f1b-9104-49c3-b780-76db9abe7bd1   deviceName    Scheduled
```

## <span data-ttu-id="d3152-113">參數</span><span class="sxs-lookup"><span data-stu-id="d3152-113">PARAMETERS</span></span>

### <span data-ttu-id="d3152-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3152-114">-DefaultProfile</span></span>
<span data-ttu-id="d3152-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d3152-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3152-116">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="d3152-116">-DeviceName</span></span>
<span data-ttu-id="d3152-117">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="d3152-117">Name of the device</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3152-118">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="d3152-118">-DeviceObject</span></span>
<span data-ttu-id="d3152-119">請提供對應的裝置物件</span><span class="sxs-lookup"><span data-stu-id="d3152-119">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d3152-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="d3152-120">-Name</span></span>
<span data-ttu-id="d3152-121">工作名稱，通常是 GUID</span><span class="sxs-lookup"><span data-stu-id="d3152-121">Name of the Job, Generally a GUID</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases: Job

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3152-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3152-122">-ResourceGroupName</span></span>
<span data-ttu-id="d3152-123">資源組名</span><span class="sxs-lookup"><span data-stu-id="d3152-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3152-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d3152-124">-ResourceId</span></span>
<span data-ttu-id="d3152-125">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="d3152-125">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3152-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3152-126">CommonParameters</span></span>
<span data-ttu-id="d3152-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d3152-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3152-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d3152-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3152-129">輸入</span><span class="sxs-lookup"><span data-stu-id="d3152-129">INPUTS</span></span>

### <span data-ttu-id="d3152-130">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.models.PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="d3152-130">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="d3152-131">輸出</span><span class="sxs-lookup"><span data-stu-id="d3152-131">OUTPUTS</span></span>

### <span data-ttu-id="d3152-132">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.models.PSStackEdgeJob</span><span class="sxs-lookup"><span data-stu-id="d3152-132">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeJob</span></span>

## <span data-ttu-id="d3152-133">筆記</span><span class="sxs-lookup"><span data-stu-id="d3152-133">NOTES</span></span>

## <span data-ttu-id="d3152-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="d3152-134">RELATED LINKS</span></span>
