---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeTrigger.md
ms.openlocfilehash: 238290778d47de673f9db89280f500c2fc31ea28
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93971668"
---
# <span data-ttu-id="6831b-101">Get-AzStackEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="6831b-101">Get-AzStackEdgeTrigger</span></span>

## <span data-ttu-id="6831b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6831b-102">SYNOPSIS</span></span>
<span data-ttu-id="6831b-103">取得裝置上設定的觸發程式</span><span class="sxs-lookup"><span data-stu-id="6831b-103">Get the Triggers configured on a device</span></span>
 

## <span data-ttu-id="6831b-104">句法</span><span class="sxs-lookup"><span data-stu-id="6831b-104">SYNTAX</span></span>

### <span data-ttu-id="6831b-105">ListParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="6831b-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6831b-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6831b-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeTrigger -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6831b-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6831b-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6831b-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6831b-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeTrigger [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="6831b-109">說明</span><span class="sxs-lookup"><span data-stu-id="6831b-109">DESCRIPTION</span></span>
<span data-ttu-id="6831b-110">**AzStackEdgeTriger** Cmdlet 會取得裝置的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="6831b-110">The **Get-AzStackEdgeTriger** cmdlet gets the triggers for a device.</span></span> <span data-ttu-id="6831b-111">您可以將名稱指定為 Cmdlet 中的參數，以提取特定特定觸發程式的詳細資料</span><span class="sxs-lookup"><span data-stu-id="6831b-111">You can specify the name as a parameter in the cmdlet to fetch the details of a specific  specific Triggers</span></span>
 

## <span data-ttu-id="6831b-112">示例</span><span class="sxs-lookup"><span data-stu-id="6831b-112">EXAMPLES</span></span>

### <span data-ttu-id="6831b-113">範例1</span><span class="sxs-lookup"><span data-stu-id="6831b-113">Example 1</span></span>
```powershell
PS C:\> Get-AzStackEdgeTrigger -ResourceGroupName resourceGroupName -DeviceName deviceName
Name                  Kind               
----                  ----               
triggerName          PeriodicTimerEvent
```

## <span data-ttu-id="6831b-114">參數</span><span class="sxs-lookup"><span data-stu-id="6831b-114">PARAMETERS</span></span>

### <span data-ttu-id="6831b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6831b-115">-DefaultProfile</span></span>
<span data-ttu-id="6831b-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6831b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6831b-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="6831b-117">-DeviceName</span></span>
<span data-ttu-id="6831b-118">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="6831b-118">Device Name</span></span>

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

### <span data-ttu-id="6831b-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="6831b-119">-DeviceObject</span></span>
<span data-ttu-id="6831b-120">請提供相對應的裝置物件</span><span class="sxs-lookup"><span data-stu-id="6831b-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="6831b-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="6831b-121">-Name</span></span>
<span data-ttu-id="6831b-122">資源名稱</span><span class="sxs-lookup"><span data-stu-id="6831b-122">Resource Name</span></span>

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

### <span data-ttu-id="6831b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6831b-123">-ResourceGroupName</span></span>
<span data-ttu-id="6831b-124">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="6831b-124">Resource Group Name</span></span>

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

### <span data-ttu-id="6831b-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6831b-125">-ResourceId</span></span>
<span data-ttu-id="6831b-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="6831b-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="6831b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6831b-127">CommonParameters</span></span>
<span data-ttu-id="6831b-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6831b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6831b-129">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="6831b-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6831b-130">輸入</span><span class="sxs-lookup"><span data-stu-id="6831b-130">INPUTS</span></span>

### <span data-ttu-id="6831b-131">PSStackEdgeDevice （StackEdge）的</span><span class="sxs-lookup"><span data-stu-id="6831b-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="6831b-132">輸出</span><span class="sxs-lookup"><span data-stu-id="6831b-132">OUTPUTS</span></span>

### <span data-ttu-id="6831b-133">PSStackEdgeTrigger （StackEdge）的</span><span class="sxs-lookup"><span data-stu-id="6831b-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeTrigger</span></span>

## <span data-ttu-id="6831b-134">筆記</span><span class="sxs-lookup"><span data-stu-id="6831b-134">NOTES</span></span>

## <span data-ttu-id="6831b-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="6831b-135">RELATED LINKS</span></span>
