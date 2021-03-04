---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/get-azdataboxedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeShare.md
ms.openlocfilehash: 616830906621b673010ca8708b909608c06f93fa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914089"
---
# <span data-ttu-id="b7ff2-101">Get-AzDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="b7ff2-101">Get-AzDataBoxEdgeShare</span></span>

## <span data-ttu-id="b7ff2-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b7ff2-102">SYNOPSIS</span></span>
<span data-ttu-id="b7ff2-103">獲得裝置可用的共用。</span><span class="sxs-lookup"><span data-stu-id="b7ff2-103">Gets the available shares for a device.</span></span>

## <span data-ttu-id="b7ff2-104">語法</span><span class="sxs-lookup"><span data-stu-id="b7ff2-104">SYNTAX</span></span>

### <span data-ttu-id="b7ff2-105">ListParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="b7ff2-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b7ff2-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7ff2-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeShare -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b7ff2-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7ff2-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b7ff2-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7ff2-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeShare [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="b7ff2-109">描述</span><span class="sxs-lookup"><span data-stu-id="b7ff2-109">DESCRIPTION</span></span>
<span data-ttu-id="b7ff2-110">**Get-AzDataBoxEdgeShare** Cmdlet 會取得 Data Box Edge 裝置可用的共用。</span><span class="sxs-lookup"><span data-stu-id="b7ff2-110">The **Get-AzDataBoxEdgeShare** cmdlet gets the available shares for a Data Box Edge device.</span></span> <span data-ttu-id="b7ff2-111">如果提供名稱，就會按名稱取得共用。</span><span class="sxs-lookup"><span data-stu-id="b7ff2-111">If Name is provided this will get the share by Name.</span></span>

## <span data-ttu-id="b7ff2-112">例子</span><span class="sxs-lookup"><span data-stu-id="b7ff2-112">EXAMPLES</span></span>

### <span data-ttu-id="b7ff2-113">範例 1</span><span class="sxs-lookup"><span data-stu-id="b7ff2-113">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-1    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-2    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-3    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-4    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
```

## <span data-ttu-id="b7ff2-114">參數</span><span class="sxs-lookup"><span data-stu-id="b7ff2-114">PARAMETERS</span></span>

### <span data-ttu-id="b7ff2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7ff2-115">-DefaultProfile</span></span>
<span data-ttu-id="b7ff2-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b7ff2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7ff2-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="b7ff2-117">-DeviceName</span></span>
<span data-ttu-id="b7ff2-118">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="b7ff2-118">Device Name</span></span>

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

### <span data-ttu-id="b7ff2-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="b7ff2-119">-DeviceObject</span></span>
<span data-ttu-id="b7ff2-120">請提供對應的裝置物件</span><span class="sxs-lookup"><span data-stu-id="b7ff2-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="b7ff2-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="b7ff2-121">-Name</span></span>
<span data-ttu-id="b7ff2-122">資源名稱</span><span class="sxs-lookup"><span data-stu-id="b7ff2-122">Resource Name</span></span>

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

### <span data-ttu-id="b7ff2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7ff2-123">-ResourceGroupName</span></span>
<span data-ttu-id="b7ff2-124">資源組名</span><span class="sxs-lookup"><span data-stu-id="b7ff2-124">Resource Group Name</span></span>

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

### <span data-ttu-id="b7ff2-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b7ff2-125">-ResourceId</span></span>
<span data-ttu-id="b7ff2-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="b7ff2-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="b7ff2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7ff2-127">CommonParameters</span></span>
<span data-ttu-id="b7ff2-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b7ff2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7ff2-129">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b7ff2-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7ff2-130">輸入</span><span class="sxs-lookup"><span data-stu-id="b7ff2-130">INPUTS</span></span>

### <span data-ttu-id="b7ff2-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="b7ff2-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="b7ff2-132">輸出</span><span class="sxs-lookup"><span data-stu-id="b7ff2-132">OUTPUTS</span></span>

### <span data-ttu-id="b7ff2-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="b7ff2-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span></span>

## <span data-ttu-id="b7ff2-134">筆記</span><span class="sxs-lookup"><span data-stu-id="b7ff2-134">NOTES</span></span>

## <span data-ttu-id="b7ff2-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="b7ff2-135">RELATED LINKS</span></span>
