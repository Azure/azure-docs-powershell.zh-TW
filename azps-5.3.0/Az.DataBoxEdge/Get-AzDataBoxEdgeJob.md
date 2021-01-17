---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeJob.md
ms.openlocfilehash: c2d97f4a7d713482a5e442e1fcb712ccb18797c0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98449480"
---
# <span data-ttu-id="f1c62-101">Get-AzDataBoxEdgeJob</span><span class="sxs-lookup"><span data-stu-id="f1c62-101">Get-AzDataBoxEdgeJob</span></span>

## <span data-ttu-id="f1c62-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f1c62-102">SYNOPSIS</span></span>
<span data-ttu-id="f1c62-103">取得在裝置上排程的工作。</span><span class="sxs-lookup"><span data-stu-id="f1c62-103">Gets the jobs scheduled on a device.</span></span>

## <span data-ttu-id="f1c62-104">句法</span><span class="sxs-lookup"><span data-stu-id="f1c62-104">SYNTAX</span></span>

### <span data-ttu-id="f1c62-105">GetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="f1c62-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeJob [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f1c62-106">GetByResourceIdObject</span><span class="sxs-lookup"><span data-stu-id="f1c62-106">GetByResourceIdObject</span></span>
```
Get-AzDataBoxEdgeJob -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f1c62-107">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f1c62-107">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeJob [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="f1c62-108">說明</span><span class="sxs-lookup"><span data-stu-id="f1c62-108">DESCRIPTION</span></span>
<span data-ttu-id="f1c62-109">**AzDataBoxEdgeJob** Cmdlet 會取得資料編輯方塊邊緣裝置上的作用中作業。</span><span class="sxs-lookup"><span data-stu-id="f1c62-109">The **Get-AzDataBoxEdgeJob** cmdlet gets the active jobs on a Data Box Edge device.</span></span> <span data-ttu-id="f1c62-110">您可以提及 Name 參數來取得特定作業的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="f1c62-110">You can mention the Name parameter to get details of a specific job.</span></span>

## <span data-ttu-id="f1c62-111">示例</span><span class="sxs-lookup"><span data-stu-id="f1c62-111">EXAMPLES</span></span>

### <span data-ttu-id="f1c62-112">範例1</span><span class="sxs-lookup"><span data-stu-id="f1c62-112">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeJob -ResourceGroupName resourceGroupName -DeviceName deviceName -Name 1f2d8f1b-9104-49c3-b780-76db9abe7bd1
Name                                   Device-Name    status
------------------                     -------------  -------
1f2d8f1b-9104-49c3-b780-76db9abe7bd1   deviceName    Scheduled
```

## <span data-ttu-id="f1c62-113">參數</span><span class="sxs-lookup"><span data-stu-id="f1c62-113">PARAMETERS</span></span>

### <span data-ttu-id="f1c62-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1c62-114">-DefaultProfile</span></span>
<span data-ttu-id="f1c62-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f1c62-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1c62-116">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="f1c62-116">-DeviceName</span></span>
<span data-ttu-id="f1c62-117">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="f1c62-117">Name of the device</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1c62-118">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="f1c62-118">-DeviceObject</span></span>
<span data-ttu-id="f1c62-119">請提供相對應的裝置物件</span><span class="sxs-lookup"><span data-stu-id="f1c62-119">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="f1c62-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="f1c62-120">-Name</span></span>
<span data-ttu-id="f1c62-121">作業的名稱，通常是 GUID</span><span class="sxs-lookup"><span data-stu-id="f1c62-121">Name of the Job, Generally a GUID</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1c62-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1c62-122">-ResourceGroupName</span></span>
<span data-ttu-id="f1c62-123">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="f1c62-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1c62-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f1c62-124">-ResourceId</span></span>
<span data-ttu-id="f1c62-125">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="f1c62-125">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1c62-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1c62-126">CommonParameters</span></span>
<span data-ttu-id="f1c62-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f1c62-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1c62-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f1c62-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1c62-129">輸入</span><span class="sxs-lookup"><span data-stu-id="f1c62-129">INPUTS</span></span>

### <span data-ttu-id="f1c62-130">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="f1c62-130">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="f1c62-131">輸出</span><span class="sxs-lookup"><span data-stu-id="f1c62-131">OUTPUTS</span></span>

### <span data-ttu-id="f1c62-132">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeJob</span><span class="sxs-lookup"><span data-stu-id="f1c62-132">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeJob</span></span>

## <span data-ttu-id="f1c62-133">筆記</span><span class="sxs-lookup"><span data-stu-id="f1c62-133">NOTES</span></span>

## <span data-ttu-id="f1c62-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="f1c62-134">RELATED LINKS</span></span>
