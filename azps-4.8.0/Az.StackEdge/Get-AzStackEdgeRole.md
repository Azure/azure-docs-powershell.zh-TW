---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeRole.md
ms.openlocfilehash: 56179260dc045b83ed067e92c6aa8bd7f880c38c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94129780"
---
# <span data-ttu-id="b4032-101">Get-AzStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="b4032-101">Get-AzStackEdgeRole</span></span>

## <span data-ttu-id="b4032-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b4032-102">SYNOPSIS</span></span>
<span data-ttu-id="b4032-103">取得裝置的可用角色。</span><span class="sxs-lookup"><span data-stu-id="b4032-103">Fetches the available roles for a device.</span></span>

## <span data-ttu-id="b4032-104">句法</span><span class="sxs-lookup"><span data-stu-id="b4032-104">SYNTAX</span></span>

### <span data-ttu-id="b4032-105">ListParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="b4032-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b4032-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4032-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeRole -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b4032-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4032-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b4032-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4032-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeRole [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="b4032-109">說明</span><span class="sxs-lookup"><span data-stu-id="b4032-109">DESCRIPTION</span></span>
<span data-ttu-id="b4032-110">AzStackEdgeRole Cmdlet 會針對堆疊邊緣裝置 **取得** 可用的 IoT 角色。</span><span class="sxs-lookup"><span data-stu-id="b4032-110">The **Get-AzStackEdgeRole** cmdlet fetches the available IoT roles for a Stack Edge device.</span></span> <span data-ttu-id="b4032-111">您可以提及 Name 參數，以取得特定 IoT 角色的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="b4032-111">You can mention the Name parameter to get the details of a specific IoT role.</span></span>

## <span data-ttu-id="b4032-112">示例</span><span class="sxs-lookup"><span data-stu-id="b4032-112">EXAMPLES</span></span>

### <span data-ttu-id="b4032-113">範例1</span><span class="sxs-lookup"><span data-stu-id="b4032-113">Example 1</span></span>
```powershell
PS C:\> Get-AzStackEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
iotrole ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

## <span data-ttu-id="b4032-114">參數</span><span class="sxs-lookup"><span data-stu-id="b4032-114">PARAMETERS</span></span>

### <span data-ttu-id="b4032-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4032-115">-DefaultProfile</span></span>
<span data-ttu-id="b4032-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b4032-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4032-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="b4032-117">-DeviceName</span></span>
<span data-ttu-id="b4032-118">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="b4032-118">Device Name</span></span>

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

### <span data-ttu-id="b4032-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="b4032-119">-DeviceObject</span></span>
<span data-ttu-id="b4032-120">請提供相對應的裝置物件</span><span class="sxs-lookup"><span data-stu-id="b4032-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="b4032-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="b4032-121">-Name</span></span>
<span data-ttu-id="b4032-122">資源名稱</span><span class="sxs-lookup"><span data-stu-id="b4032-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: RoleName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases: RoleName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4032-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4032-123">-ResourceGroupName</span></span>
<span data-ttu-id="b4032-124">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="b4032-124">Resource Group Name</span></span>

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

### <span data-ttu-id="b4032-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b4032-125">-ResourceId</span></span>
<span data-ttu-id="b4032-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="b4032-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="b4032-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4032-127">CommonParameters</span></span>
<span data-ttu-id="b4032-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b4032-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4032-129">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b4032-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4032-130">輸入</span><span class="sxs-lookup"><span data-stu-id="b4032-130">INPUTS</span></span>

### <span data-ttu-id="b4032-131">PSStackEdgeDevice （StackEdge）的</span><span class="sxs-lookup"><span data-stu-id="b4032-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="b4032-132">輸出</span><span class="sxs-lookup"><span data-stu-id="b4032-132">OUTPUTS</span></span>

### <span data-ttu-id="b4032-133">PSStackEdgeRole （StackEdge）的</span><span class="sxs-lookup"><span data-stu-id="b4032-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="b4032-134">筆記</span><span class="sxs-lookup"><span data-stu-id="b4032-134">NOTES</span></span>

## <span data-ttu-id="b4032-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="b4032-135">RELATED LINKS</span></span>