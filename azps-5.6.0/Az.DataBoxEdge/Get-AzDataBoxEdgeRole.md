---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/get-azdataboxedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeRole.md
ms.openlocfilehash: 9dd4925224f2ed91770caff422b8ab6f5d924754
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914090"
---
# <span data-ttu-id="d77ce-101">Get-AzDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="d77ce-101">Get-AzDataBoxEdgeRole</span></span>

## <span data-ttu-id="d77ce-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d77ce-102">SYNOPSIS</span></span>
<span data-ttu-id="d77ce-103">抓取裝置可用的角色。</span><span class="sxs-lookup"><span data-stu-id="d77ce-103">Fetches the available roles for a device.</span></span>

## <span data-ttu-id="d77ce-104">語法</span><span class="sxs-lookup"><span data-stu-id="d77ce-104">SYNTAX</span></span>

### <span data-ttu-id="d77ce-105">ListParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="d77ce-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d77ce-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d77ce-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeRole -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d77ce-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d77ce-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d77ce-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d77ce-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeRole [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="d77ce-109">描述</span><span class="sxs-lookup"><span data-stu-id="d77ce-109">DESCRIPTION</span></span>
<span data-ttu-id="d77ce-110">**Get-AzDataBoxEdgeRole** Cmdlet 會取得 Data Box Edge 裝置可用的 IoT 角色。</span><span class="sxs-lookup"><span data-stu-id="d77ce-110">The **Get-AzDataBoxEdgeRole** cmdlet fetches the available IoT roles for a Data Box Edge device.</span></span> <span data-ttu-id="d77ce-111">您可以提及 Name 參數，以取得特定 IoT 角色的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="d77ce-111">You can mention the Name parameter to get the details of a specific IoT role.</span></span>

## <span data-ttu-id="d77ce-112">例子</span><span class="sxs-lookup"><span data-stu-id="d77ce-112">EXAMPLES</span></span>

### <span data-ttu-id="d77ce-113">範例 1</span><span class="sxs-lookup"><span data-stu-id="d77ce-113">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
iotrole ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

## <span data-ttu-id="d77ce-114">參數</span><span class="sxs-lookup"><span data-stu-id="d77ce-114">PARAMETERS</span></span>

### <span data-ttu-id="d77ce-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d77ce-115">-DefaultProfile</span></span>
<span data-ttu-id="d77ce-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d77ce-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d77ce-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="d77ce-117">-DeviceName</span></span>
<span data-ttu-id="d77ce-118">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="d77ce-118">Device Name</span></span>

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

### <span data-ttu-id="d77ce-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="d77ce-119">-DeviceObject</span></span>
<span data-ttu-id="d77ce-120">請提供對應的裝置物件</span><span class="sxs-lookup"><span data-stu-id="d77ce-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="d77ce-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="d77ce-121">-Name</span></span>
<span data-ttu-id="d77ce-122">資源名稱</span><span class="sxs-lookup"><span data-stu-id="d77ce-122">Resource Name</span></span>

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

### <span data-ttu-id="d77ce-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d77ce-123">-ResourceGroupName</span></span>
<span data-ttu-id="d77ce-124">資源組名</span><span class="sxs-lookup"><span data-stu-id="d77ce-124">Resource Group Name</span></span>

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

### <span data-ttu-id="d77ce-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d77ce-125">-ResourceId</span></span>
<span data-ttu-id="d77ce-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="d77ce-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="d77ce-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d77ce-127">CommonParameters</span></span>
<span data-ttu-id="d77ce-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d77ce-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d77ce-129">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d77ce-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d77ce-130">輸入</span><span class="sxs-lookup"><span data-stu-id="d77ce-130">INPUTS</span></span>

### <span data-ttu-id="d77ce-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="d77ce-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="d77ce-132">輸出</span><span class="sxs-lookup"><span data-stu-id="d77ce-132">OUTPUTS</span></span>

### <span data-ttu-id="d77ce-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="d77ce-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span></span>

## <span data-ttu-id="d77ce-134">筆記</span><span class="sxs-lookup"><span data-stu-id="d77ce-134">NOTES</span></span>

## <span data-ttu-id="d77ce-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="d77ce-135">RELATED LINKS</span></span>
