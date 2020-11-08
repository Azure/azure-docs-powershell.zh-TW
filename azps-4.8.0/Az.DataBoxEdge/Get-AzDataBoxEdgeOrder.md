---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeOrder.md
ms.openlocfilehash: c1b5c52233b6887dc3221e49174b45d907716c10
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93971165"
---
# <span data-ttu-id="587f0-101">Get-AzDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="587f0-101">Get-AzDataBoxEdgeOrder</span></span>

## <span data-ttu-id="587f0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="587f0-102">SYNOPSIS</span></span>
<span data-ttu-id="587f0-103">取得裝置的訂單詳細資料</span><span class="sxs-lookup"><span data-stu-id="587f0-103">Get the order details for a device</span></span>

## <span data-ttu-id="587f0-104">句法</span><span class="sxs-lookup"><span data-stu-id="587f0-104">SYNTAX</span></span>

### <span data-ttu-id="587f0-105">GetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="587f0-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="587f0-106">GetByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="587f0-106">GetByDeviceObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeOrder -DeviceObject <PSDataBoxEdgeDevice> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="587f0-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="587f0-107">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeOrder -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="587f0-108">說明</span><span class="sxs-lookup"><span data-stu-id="587f0-108">DESCRIPTION</span></span>
<span data-ttu-id="587f0-109">**AzDataBoxEdgeOrder** Cmdlet 會取得資料編輯方塊邊緣裝置的訂單詳細資料。</span><span class="sxs-lookup"><span data-stu-id="587f0-109">The **Get-AzDataBoxEdgeOrder** cmdlet gets the order details for a Data Box Edge device.</span></span> 

## <span data-ttu-id="587f0-110">示例</span><span class="sxs-lookup"><span data-stu-id="587f0-110">EXAMPLES</span></span>

### <span data-ttu-id="587f0-111">範例1</span><span class="sxs-lookup"><span data-stu-id="587f0-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeOrder -ResourceGroupName resourceGroupName -DeviceName deviceName
DeviceName  ResourceGroupName Status    UpdatedDatetime
----------  ----------------- ------    ---------------
deviceName  resourceGroupName Untracked 01-Jan-01 12:00:00 AM
```

## <span data-ttu-id="587f0-112">參數</span><span class="sxs-lookup"><span data-stu-id="587f0-112">PARAMETERS</span></span>

### <span data-ttu-id="587f0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="587f0-113">-DefaultProfile</span></span>
<span data-ttu-id="587f0-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="587f0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="587f0-115">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="587f0-115">-DeviceName</span></span>
<span data-ttu-id="587f0-116">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="587f0-116">Resource Group Name</span></span>

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

### <span data-ttu-id="587f0-117">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="587f0-117">-DeviceObject</span></span>
<span data-ttu-id="587f0-118">請提供相對應的裝置物件</span><span class="sxs-lookup"><span data-stu-id="587f0-118">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice
Parameter Sets: GetByDeviceObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="587f0-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="587f0-119">-ResourceGroupName</span></span>
<span data-ttu-id="587f0-120">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="587f0-120">Resource Group Name</span></span>

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

### <span data-ttu-id="587f0-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="587f0-121">-ResourceId</span></span>
<span data-ttu-id="587f0-122">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="587f0-122">Azure ResourceId</span></span>

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

### <span data-ttu-id="587f0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="587f0-123">CommonParameters</span></span>
<span data-ttu-id="587f0-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="587f0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="587f0-125">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="587f0-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="587f0-126">輸入</span><span class="sxs-lookup"><span data-stu-id="587f0-126">INPUTS</span></span>

### <span data-ttu-id="587f0-127">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="587f0-127">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

### <span data-ttu-id="587f0-128">System.object</span><span class="sxs-lookup"><span data-stu-id="587f0-128">System.String</span></span>

## <span data-ttu-id="587f0-129">輸出</span><span class="sxs-lookup"><span data-stu-id="587f0-129">OUTPUTS</span></span>

### <span data-ttu-id="587f0-130">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="587f0-130">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span></span>

## <span data-ttu-id="587f0-131">筆記</span><span class="sxs-lookup"><span data-stu-id="587f0-131">NOTES</span></span>

## <span data-ttu-id="587f0-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="587f0-132">RELATED LINKS</span></span>