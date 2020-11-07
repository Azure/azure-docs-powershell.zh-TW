---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeTrigger.md
ms.openlocfilehash: 96c9b736398cb981dd055d072091aa24af4d3f6c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795777"
---
# <span data-ttu-id="d7e34-101">Get-AzDataBoxEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="d7e34-101">Get-AzDataBoxEdgeTrigger</span></span>

## <span data-ttu-id="d7e34-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d7e34-102">SYNOPSIS</span></span>
<span data-ttu-id="d7e34-103">取得裝置上設定的觸發程式</span><span class="sxs-lookup"><span data-stu-id="d7e34-103">Get the Triggers configured on a device</span></span>
 

## <span data-ttu-id="d7e34-104">句法</span><span class="sxs-lookup"><span data-stu-id="d7e34-104">SYNTAX</span></span>

### <span data-ttu-id="d7e34-105">ListParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="d7e34-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d7e34-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d7e34-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeTrigger -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d7e34-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d7e34-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d7e34-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d7e34-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeTrigger [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="d7e34-109">說明</span><span class="sxs-lookup"><span data-stu-id="d7e34-109">DESCRIPTION</span></span>
<span data-ttu-id="d7e34-110">**AzDataBoxEdgeTriger** Cmdlet 會取得裝置的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="d7e34-110">The **Get-AzDataBoxEdgeTriger** cmdlet gets the triggers for a device.</span></span> <span data-ttu-id="d7e34-111">您可以將名稱指定為 Cmdlet 中的參數，以提取特定特定觸發程式的詳細資料</span><span class="sxs-lookup"><span data-stu-id="d7e34-111">You can specify the name as a parameter in the cmdlet to fetch the details of a specific  specific Triggers</span></span>
 

## <span data-ttu-id="d7e34-112">示例</span><span class="sxs-lookup"><span data-stu-id="d7e34-112">EXAMPLES</span></span>

### <span data-ttu-id="d7e34-113">範例1</span><span class="sxs-lookup"><span data-stu-id="d7e34-113">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeTrigger -ResourceGroupName resourceGroupName -DeviceName deviceName
Name                  Kind               
----                  ----               
triggerName          PeriodicTimerEvent
```

## <span data-ttu-id="d7e34-114">參數</span><span class="sxs-lookup"><span data-stu-id="d7e34-114">PARAMETERS</span></span>

### <span data-ttu-id="d7e34-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7e34-115">-DefaultProfile</span></span>
<span data-ttu-id="d7e34-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d7e34-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7e34-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="d7e34-117">-DeviceName</span></span>
<span data-ttu-id="d7e34-118">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="d7e34-118">Device Name</span></span>

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

### <span data-ttu-id="d7e34-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="d7e34-119">-DeviceObject</span></span>
<span data-ttu-id="d7e34-120">請提供相對應的裝置物件</span><span class="sxs-lookup"><span data-stu-id="d7e34-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="d7e34-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="d7e34-121">-Name</span></span>
<span data-ttu-id="d7e34-122">資源名稱</span><span class="sxs-lookup"><span data-stu-id="d7e34-122">Resource Name</span></span>

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

### <span data-ttu-id="d7e34-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7e34-123">-ResourceGroupName</span></span>
<span data-ttu-id="d7e34-124">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="d7e34-124">Resource Group Name</span></span>

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

### <span data-ttu-id="d7e34-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d7e34-125">-ResourceId</span></span>
<span data-ttu-id="d7e34-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="d7e34-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="d7e34-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7e34-127">CommonParameters</span></span>
<span data-ttu-id="d7e34-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d7e34-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7e34-129">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d7e34-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7e34-130">輸入</span><span class="sxs-lookup"><span data-stu-id="d7e34-130">INPUTS</span></span>

### <span data-ttu-id="d7e34-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="d7e34-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="d7e34-132">輸出</span><span class="sxs-lookup"><span data-stu-id="d7e34-132">OUTPUTS</span></span>

### <span data-ttu-id="d7e34-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="d7e34-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger</span></span>

## <span data-ttu-id="d7e34-134">筆記</span><span class="sxs-lookup"><span data-stu-id="d7e34-134">NOTES</span></span>

## <span data-ttu-id="d7e34-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="d7e34-135">RELATED LINKS</span></span>
