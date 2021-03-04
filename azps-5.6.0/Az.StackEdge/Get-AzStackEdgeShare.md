---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/get-azstackedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeShare.md
ms.openlocfilehash: 34ef411b96aaee2a6caa32452c678d888cf62b65
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904573"
---
# <span data-ttu-id="f0943-101">Get-AzStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="f0943-101">Get-AzStackEdgeShare</span></span>

## <span data-ttu-id="f0943-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f0943-102">SYNOPSIS</span></span>
<span data-ttu-id="f0943-103">獲得裝置可用的共用。</span><span class="sxs-lookup"><span data-stu-id="f0943-103">Gets the available shares for a device.</span></span>

## <span data-ttu-id="f0943-104">語法</span><span class="sxs-lookup"><span data-stu-id="f0943-104">SYNTAX</span></span>

### <span data-ttu-id="f0943-105">ListParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="f0943-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f0943-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f0943-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeShare -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f0943-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f0943-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f0943-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f0943-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeShare [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="f0943-109">描述</span><span class="sxs-lookup"><span data-stu-id="f0943-109">DESCRIPTION</span></span>
<span data-ttu-id="f0943-110">**Get-AzStackEdgeShare** Cmdlet 會取得 Stack Edge 裝置可用的共用。</span><span class="sxs-lookup"><span data-stu-id="f0943-110">The **Get-AzStackEdgeShare** cmdlet gets the available shares for a Stack Edge device.</span></span> <span data-ttu-id="f0943-111">如果提供名稱，就會按名稱取得共用。</span><span class="sxs-lookup"><span data-stu-id="f0943-111">If Name is provided this will get the share by Name.</span></span>

## <span data-ttu-id="f0943-112">例子</span><span class="sxs-lookup"><span data-stu-id="f0943-112">EXAMPLES</span></span>

### <span data-ttu-id="f0943-113">範例 1</span><span class="sxs-lookup"><span data-stu-id="f0943-113">Example 1</span></span>
```powershell
PS C:\> Get-AzStackEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-1    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-2    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-3    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-4    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
```

## <span data-ttu-id="f0943-114">參數</span><span class="sxs-lookup"><span data-stu-id="f0943-114">PARAMETERS</span></span>

### <span data-ttu-id="f0943-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0943-115">-DefaultProfile</span></span>
<span data-ttu-id="f0943-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f0943-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0943-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="f0943-117">-DeviceName</span></span>
<span data-ttu-id="f0943-118">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="f0943-118">Device Name</span></span>

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

### <span data-ttu-id="f0943-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="f0943-119">-DeviceObject</span></span>
<span data-ttu-id="f0943-120">請提供對應的裝置物件</span><span class="sxs-lookup"><span data-stu-id="f0943-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="f0943-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="f0943-121">-Name</span></span>
<span data-ttu-id="f0943-122">資源名稱</span><span class="sxs-lookup"><span data-stu-id="f0943-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: EdgeShareName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases: EdgeShareName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0943-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0943-123">-ResourceGroupName</span></span>
<span data-ttu-id="f0943-124">資源組名</span><span class="sxs-lookup"><span data-stu-id="f0943-124">Resource Group Name</span></span>

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

### <span data-ttu-id="f0943-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f0943-125">-ResourceId</span></span>
<span data-ttu-id="f0943-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="f0943-126">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0943-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0943-127">CommonParameters</span></span>
<span data-ttu-id="f0943-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f0943-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0943-129">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f0943-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0943-130">輸入</span><span class="sxs-lookup"><span data-stu-id="f0943-130">INPUTS</span></span>

### <span data-ttu-id="f0943-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.models.PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="f0943-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="f0943-132">輸出</span><span class="sxs-lookup"><span data-stu-id="f0943-132">OUTPUTS</span></span>

### <span data-ttu-id="f0943-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.models.PSStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="f0943-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span></span>

## <span data-ttu-id="f0943-134">筆記</span><span class="sxs-lookup"><span data-stu-id="f0943-134">NOTES</span></span>

## <span data-ttu-id="f0943-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="f0943-135">RELATED LINKS</span></span>
