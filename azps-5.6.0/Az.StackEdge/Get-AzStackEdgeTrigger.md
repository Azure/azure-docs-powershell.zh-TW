---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/get-azstackedgetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeTrigger.md
ms.openlocfilehash: a4bcbad5f595efe126ed232b94d5deb368515bc2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907982"
---
# <span data-ttu-id="93a6b-101">Get-AzStackEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="93a6b-101">Get-AzStackEdgeTrigger</span></span>

## <span data-ttu-id="93a6b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="93a6b-102">SYNOPSIS</span></span>
<span data-ttu-id="93a6b-103">在裝置上取得已配置的觸發程式</span><span class="sxs-lookup"><span data-stu-id="93a6b-103">Get the Triggers configured on a device</span></span>
 

## <span data-ttu-id="93a6b-104">語法</span><span class="sxs-lookup"><span data-stu-id="93a6b-104">SYNTAX</span></span>

### <span data-ttu-id="93a6b-105">ListParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="93a6b-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="93a6b-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="93a6b-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeTrigger -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="93a6b-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="93a6b-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="93a6b-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="93a6b-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeTrigger [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="93a6b-109">描述</span><span class="sxs-lookup"><span data-stu-id="93a6b-109">DESCRIPTION</span></span>
<span data-ttu-id="93a6b-110">**Get-AzStackEdgeTriger Cmdlet** 會取得裝置觸發器。</span><span class="sxs-lookup"><span data-stu-id="93a6b-110">The **Get-AzStackEdgeTriger** cmdlet gets the triggers for a device.</span></span> <span data-ttu-id="93a6b-111">您可以在 Cmdlet 中將名稱指定為參數，以抓取特定觸發者的詳細資訊</span><span class="sxs-lookup"><span data-stu-id="93a6b-111">You can specify the name as a parameter in the cmdlet to fetch the details of a specific  specific Triggers</span></span>
 

## <span data-ttu-id="93a6b-112">例子</span><span class="sxs-lookup"><span data-stu-id="93a6b-112">EXAMPLES</span></span>

### <span data-ttu-id="93a6b-113">範例 1</span><span class="sxs-lookup"><span data-stu-id="93a6b-113">Example 1</span></span>
```powershell
PS C:\> Get-AzStackEdgeTrigger -ResourceGroupName resourceGroupName -DeviceName deviceName
Name                  Kind               
----                  ----               
triggerName          PeriodicTimerEvent
```

## <span data-ttu-id="93a6b-114">參數</span><span class="sxs-lookup"><span data-stu-id="93a6b-114">PARAMETERS</span></span>

### <span data-ttu-id="93a6b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93a6b-115">-DefaultProfile</span></span>
<span data-ttu-id="93a6b-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="93a6b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93a6b-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="93a6b-117">-DeviceName</span></span>
<span data-ttu-id="93a6b-118">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="93a6b-118">Device Name</span></span>

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

### <span data-ttu-id="93a6b-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="93a6b-119">-DeviceObject</span></span>
<span data-ttu-id="93a6b-120">請提供對應的裝置物件</span><span class="sxs-lookup"><span data-stu-id="93a6b-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="93a6b-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="93a6b-121">-Name</span></span>
<span data-ttu-id="93a6b-122">資源名稱</span><span class="sxs-lookup"><span data-stu-id="93a6b-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases: TriggerName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93a6b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93a6b-123">-ResourceGroupName</span></span>
<span data-ttu-id="93a6b-124">資源組名</span><span class="sxs-lookup"><span data-stu-id="93a6b-124">Resource Group Name</span></span>

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

### <span data-ttu-id="93a6b-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="93a6b-125">-ResourceId</span></span>
<span data-ttu-id="93a6b-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="93a6b-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="93a6b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93a6b-127">CommonParameters</span></span>
<span data-ttu-id="93a6b-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="93a6b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93a6b-129">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="93a6b-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93a6b-130">輸入</span><span class="sxs-lookup"><span data-stu-id="93a6b-130">INPUTS</span></span>

### <span data-ttu-id="93a6b-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.models.PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="93a6b-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="93a6b-132">輸出</span><span class="sxs-lookup"><span data-stu-id="93a6b-132">OUTPUTS</span></span>

### <span data-ttu-id="93a6b-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.models.PSStackEdgeTrirr</span><span class="sxs-lookup"><span data-stu-id="93a6b-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeTrigger</span></span>

## <span data-ttu-id="93a6b-134">筆記</span><span class="sxs-lookup"><span data-stu-id="93a6b-134">NOTES</span></span>

## <span data-ttu-id="93a6b-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="93a6b-135">RELATED LINKS</span></span>
