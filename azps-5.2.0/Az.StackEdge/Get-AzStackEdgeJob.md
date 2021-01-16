---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeJob.md
ms.openlocfilehash: 957cc5c7dea0b8ea3215a035f68c2528442a7d52
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98280247"
---
# <span data-ttu-id="77468-101">Get-AzStackEdgeJob</span><span class="sxs-lookup"><span data-stu-id="77468-101">Get-AzStackEdgeJob</span></span>

## <span data-ttu-id="77468-102">摘要</span><span class="sxs-lookup"><span data-stu-id="77468-102">SYNOPSIS</span></span>
<span data-ttu-id="77468-103">取得在裝置上排程的工作。</span><span class="sxs-lookup"><span data-stu-id="77468-103">Gets the jobs scheduled on a device.</span></span>

## <span data-ttu-id="77468-104">句法</span><span class="sxs-lookup"><span data-stu-id="77468-104">SYNTAX</span></span>

### <span data-ttu-id="77468-105">GetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="77468-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzStackEdgeJob [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77468-106">GetByResourceIdObject</span><span class="sxs-lookup"><span data-stu-id="77468-106">GetByResourceIdObject</span></span>
```
Get-AzStackEdgeJob -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77468-107">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="77468-107">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeJob [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="77468-108">說明</span><span class="sxs-lookup"><span data-stu-id="77468-108">DESCRIPTION</span></span>
<span data-ttu-id="77468-109">**AzStackEdgeJob** Cmdlet 會取得堆疊 Edge 裝置上的作用中作業。</span><span class="sxs-lookup"><span data-stu-id="77468-109">The **Get-AzStackEdgeJob** cmdlet gets the active jobs on a Stack Edge device.</span></span> <span data-ttu-id="77468-110">您可以提及 Name 參數來取得特定作業的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="77468-110">You can mention the Name parameter to get details of a specific job.</span></span>

## <span data-ttu-id="77468-111">示例</span><span class="sxs-lookup"><span data-stu-id="77468-111">EXAMPLES</span></span>

### <span data-ttu-id="77468-112">範例1</span><span class="sxs-lookup"><span data-stu-id="77468-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStackEdgeJob -ResourceGroupName resourceGroupName -DeviceName deviceName -Name 1f2d8f1b-9104-49c3-b780-76db9abe7bd1
Name                                   Device-Name    status
------------------                     -------------  -------
1f2d8f1b-9104-49c3-b780-76db9abe7bd1   deviceName    Scheduled
```

## <span data-ttu-id="77468-113">參數</span><span class="sxs-lookup"><span data-stu-id="77468-113">PARAMETERS</span></span>

### <span data-ttu-id="77468-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77468-114">-DefaultProfile</span></span>
<span data-ttu-id="77468-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="77468-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77468-116">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="77468-116">-DeviceName</span></span>
<span data-ttu-id="77468-117">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="77468-117">Name of the device</span></span>

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

### <span data-ttu-id="77468-118">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="77468-118">-DeviceObject</span></span>
<span data-ttu-id="77468-119">請提供相對應的裝置物件</span><span class="sxs-lookup"><span data-stu-id="77468-119">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="77468-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="77468-120">-Name</span></span>
<span data-ttu-id="77468-121">作業的名稱，通常是 GUID</span><span class="sxs-lookup"><span data-stu-id="77468-121">Name of the Job, Generally a GUID</span></span>

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

### <span data-ttu-id="77468-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77468-122">-ResourceGroupName</span></span>
<span data-ttu-id="77468-123">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="77468-123">Resource Group Name</span></span>

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

### <span data-ttu-id="77468-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="77468-124">-ResourceId</span></span>
<span data-ttu-id="77468-125">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="77468-125">Azure ResourceId</span></span>

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

### <span data-ttu-id="77468-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77468-126">CommonParameters</span></span>
<span data-ttu-id="77468-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="77468-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77468-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="77468-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77468-129">輸入</span><span class="sxs-lookup"><span data-stu-id="77468-129">INPUTS</span></span>

### <span data-ttu-id="77468-130">PSStackEdgeDevice （StackEdge）的</span><span class="sxs-lookup"><span data-stu-id="77468-130">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="77468-131">輸出</span><span class="sxs-lookup"><span data-stu-id="77468-131">OUTPUTS</span></span>

### <span data-ttu-id="77468-132">PSStackEdgeJob （StackEdge）的</span><span class="sxs-lookup"><span data-stu-id="77468-132">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeJob</span></span>

## <span data-ttu-id="77468-133">筆記</span><span class="sxs-lookup"><span data-stu-id="77468-133">NOTES</span></span>

## <span data-ttu-id="77468-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="77468-134">RELATED LINKS</span></span>
