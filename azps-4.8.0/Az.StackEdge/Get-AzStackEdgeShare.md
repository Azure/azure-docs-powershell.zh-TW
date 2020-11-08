---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeShare.md
ms.openlocfilehash: 0e0d0e3b2dfca824d66a9a75f3e22438335c97db
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94129779"
---
# <span data-ttu-id="27e56-101">Get-AzStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="27e56-101">Get-AzStackEdgeShare</span></span>

## <span data-ttu-id="27e56-102">摘要</span><span class="sxs-lookup"><span data-stu-id="27e56-102">SYNOPSIS</span></span>
<span data-ttu-id="27e56-103">取得裝置的可用共用。</span><span class="sxs-lookup"><span data-stu-id="27e56-103">Gets the available shares for a device.</span></span>

## <span data-ttu-id="27e56-104">句法</span><span class="sxs-lookup"><span data-stu-id="27e56-104">SYNTAX</span></span>

### <span data-ttu-id="27e56-105">ListParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="27e56-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27e56-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="27e56-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeShare -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27e56-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="27e56-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27e56-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="27e56-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeShare [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="27e56-109">說明</span><span class="sxs-lookup"><span data-stu-id="27e56-109">DESCRIPTION</span></span>
<span data-ttu-id="27e56-110">**AzStackEdgeShare** Cmdlet 會取得堆疊 Edge 裝置的可用共用。</span><span class="sxs-lookup"><span data-stu-id="27e56-110">The **Get-AzStackEdgeShare** cmdlet gets the available shares for a Stack Edge device.</span></span> <span data-ttu-id="27e56-111">如果提供 Name，就會透過名稱取得共用。</span><span class="sxs-lookup"><span data-stu-id="27e56-111">If Name is provided this will get the share by Name.</span></span>

## <span data-ttu-id="27e56-112">示例</span><span class="sxs-lookup"><span data-stu-id="27e56-112">EXAMPLES</span></span>

### <span data-ttu-id="27e56-113">範例1</span><span class="sxs-lookup"><span data-stu-id="27e56-113">Example 1</span></span>
```powershell
PS C:\> Get-AzStackEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-1    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-2    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-3    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-4    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
```

## <span data-ttu-id="27e56-114">參數</span><span class="sxs-lookup"><span data-stu-id="27e56-114">PARAMETERS</span></span>

### <span data-ttu-id="27e56-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27e56-115">-DefaultProfile</span></span>
<span data-ttu-id="27e56-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="27e56-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27e56-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="27e56-117">-DeviceName</span></span>
<span data-ttu-id="27e56-118">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="27e56-118">Device Name</span></span>

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

### <span data-ttu-id="27e56-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="27e56-119">-DeviceObject</span></span>
<span data-ttu-id="27e56-120">請提供相對應的裝置物件</span><span class="sxs-lookup"><span data-stu-id="27e56-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="27e56-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="27e56-121">-Name</span></span>
<span data-ttu-id="27e56-122">資源名稱</span><span class="sxs-lookup"><span data-stu-id="27e56-122">Resource Name</span></span>

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

### <span data-ttu-id="27e56-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27e56-123">-ResourceGroupName</span></span>
<span data-ttu-id="27e56-124">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="27e56-124">Resource Group Name</span></span>

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

### <span data-ttu-id="27e56-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="27e56-125">-ResourceId</span></span>
<span data-ttu-id="27e56-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="27e56-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="27e56-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27e56-127">CommonParameters</span></span>
<span data-ttu-id="27e56-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="27e56-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27e56-129">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="27e56-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27e56-130">輸入</span><span class="sxs-lookup"><span data-stu-id="27e56-130">INPUTS</span></span>

### <span data-ttu-id="27e56-131">PSStackEdgeDevice （StackEdge）的</span><span class="sxs-lookup"><span data-stu-id="27e56-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="27e56-132">輸出</span><span class="sxs-lookup"><span data-stu-id="27e56-132">OUTPUTS</span></span>

### <span data-ttu-id="27e56-133">PSStackEdgeShare （StackEdge）的</span><span class="sxs-lookup"><span data-stu-id="27e56-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span></span>

## <span data-ttu-id="27e56-134">筆記</span><span class="sxs-lookup"><span data-stu-id="27e56-134">NOTES</span></span>

## <span data-ttu-id="27e56-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="27e56-135">RELATED LINKS</span></span>