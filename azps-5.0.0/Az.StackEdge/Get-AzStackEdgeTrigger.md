---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeTrigger.md
ms.openlocfilehash: 238290778d47de673f9db89280f500c2fc31ea28
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94138077"
---
# <span data-ttu-id="6f8af-101">Get-AzStackEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="6f8af-101">Get-AzStackEdgeTrigger</span></span>

## <span data-ttu-id="6f8af-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6f8af-102">SYNOPSIS</span></span>
<span data-ttu-id="6f8af-103">取得裝置上設定的觸發程式</span><span class="sxs-lookup"><span data-stu-id="6f8af-103">Get the Triggers configured on a device</span></span>
 

## <span data-ttu-id="6f8af-104">句法</span><span class="sxs-lookup"><span data-stu-id="6f8af-104">SYNTAX</span></span>

### <span data-ttu-id="6f8af-105">ListParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="6f8af-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f8af-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f8af-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeTrigger -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f8af-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f8af-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f8af-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f8af-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeTrigger [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="6f8af-109">說明</span><span class="sxs-lookup"><span data-stu-id="6f8af-109">DESCRIPTION</span></span>
<span data-ttu-id="6f8af-110">**AzStackEdgeTriger** Cmdlet 會取得裝置的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="6f8af-110">The **Get-AzStackEdgeTriger** cmdlet gets the triggers for a device.</span></span> <span data-ttu-id="6f8af-111">您可以將名稱指定為 Cmdlet 中的參數，以提取特定特定觸發程式的詳細資料</span><span class="sxs-lookup"><span data-stu-id="6f8af-111">You can specify the name as a parameter in the cmdlet to fetch the details of a specific  specific Triggers</span></span>
 

## <span data-ttu-id="6f8af-112">示例</span><span class="sxs-lookup"><span data-stu-id="6f8af-112">EXAMPLES</span></span>

### <span data-ttu-id="6f8af-113">範例1</span><span class="sxs-lookup"><span data-stu-id="6f8af-113">Example 1</span></span>
```powershell
PS C:\> Get-AzStackEdgeTrigger -ResourceGroupName resourceGroupName -DeviceName deviceName
Name                  Kind               
----                  ----               
triggerName          PeriodicTimerEvent
```

## <span data-ttu-id="6f8af-114">參數</span><span class="sxs-lookup"><span data-stu-id="6f8af-114">PARAMETERS</span></span>

### <span data-ttu-id="6f8af-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f8af-115">-DefaultProfile</span></span>
<span data-ttu-id="6f8af-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6f8af-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f8af-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="6f8af-117">-DeviceName</span></span>
<span data-ttu-id="6f8af-118">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="6f8af-118">Device Name</span></span>

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

### <span data-ttu-id="6f8af-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="6f8af-119">-DeviceObject</span></span>
<span data-ttu-id="6f8af-120">請提供相對應的裝置物件</span><span class="sxs-lookup"><span data-stu-id="6f8af-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="6f8af-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="6f8af-121">-Name</span></span>
<span data-ttu-id="6f8af-122">資源名稱</span><span class="sxs-lookup"><span data-stu-id="6f8af-122">Resource Name</span></span>

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

### <span data-ttu-id="6f8af-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f8af-123">-ResourceGroupName</span></span>
<span data-ttu-id="6f8af-124">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="6f8af-124">Resource Group Name</span></span>

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

### <span data-ttu-id="6f8af-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6f8af-125">-ResourceId</span></span>
<span data-ttu-id="6f8af-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="6f8af-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="6f8af-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f8af-127">CommonParameters</span></span>
<span data-ttu-id="6f8af-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6f8af-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f8af-129">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="6f8af-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f8af-130">輸入</span><span class="sxs-lookup"><span data-stu-id="6f8af-130">INPUTS</span></span>

### <span data-ttu-id="6f8af-131">PSStackEdgeDevice （StackEdge）的</span><span class="sxs-lookup"><span data-stu-id="6f8af-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="6f8af-132">輸出</span><span class="sxs-lookup"><span data-stu-id="6f8af-132">OUTPUTS</span></span>

### <span data-ttu-id="6f8af-133">PSStackEdgeTrigger （StackEdge）的</span><span class="sxs-lookup"><span data-stu-id="6f8af-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeTrigger</span></span>

## <span data-ttu-id="6f8af-134">筆記</span><span class="sxs-lookup"><span data-stu-id="6f8af-134">NOTES</span></span>

## <span data-ttu-id="6f8af-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="6f8af-135">RELATED LINKS</span></span>
