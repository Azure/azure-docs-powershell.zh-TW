---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdevicechildren
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceChildren.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceChildren.md
ms.openlocfilehash: 1bc45aa06db70aff6eaec8eb1ff20b12318bb7e2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94129497"
---
# <span data-ttu-id="e27be-101">Get-AzIotHubDeviceChildren</span><span class="sxs-lookup"><span data-stu-id="e27be-101">Get-AzIotHubDeviceChildren</span></span>

## <span data-ttu-id="e27be-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e27be-102">SYNOPSIS</span></span>
<span data-ttu-id="e27be-103">列印以逗號分隔的已指派子裝置清單。</span><span class="sxs-lookup"><span data-stu-id="e27be-103">Print comma-separated list of assigned child devices.</span></span>

## <span data-ttu-id="e27be-104">句法</span><span class="sxs-lookup"><span data-stu-id="e27be-104">SYNTAX</span></span>

### <span data-ttu-id="e27be-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="e27be-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeviceChildren [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e27be-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="e27be-106">InputObjectSet</span></span>
```
Get-AzIotHubDeviceChildren [-InputObject] <PSIotHub> [-DeviceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e27be-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="e27be-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeviceChildren [-ResourceId] <String> [-DeviceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e27be-108">說明</span><span class="sxs-lookup"><span data-stu-id="e27be-108">DESCRIPTION</span></span>
<span data-ttu-id="e27be-109">以逗號分隔的清單顯示所有邊緣裝置或指定裝置的所有已指派非邊緣裝置。</span><span class="sxs-lookup"><span data-stu-id="e27be-109">Show all assigned non-edge devices as comma-separated list of all edge devices or specified device.</span></span>

## <span data-ttu-id="e27be-110">示例</span><span class="sxs-lookup"><span data-stu-id="e27be-110">EXAMPLES</span></span>

### <span data-ttu-id="e27be-111">範例1</span><span class="sxs-lookup"><span data-stu-id="e27be-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"

DeviceId  ChildrenDeviceId
--------  ----------------
myDevice1 {device1, device2}
```

<span data-ttu-id="e27be-112">將所有指派的非邊緣裝置顯示為以逗號分隔的清單。</span><span class="sxs-lookup"><span data-stu-id="e27be-112">Show all assigned non-edge devices as comma-separated list.</span></span>

### <span data-ttu-id="e27be-113">範例2</span><span class="sxs-lookup"><span data-stu-id="e27be-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"

DeviceId  ChildrenDeviceId
--------  ----------------
myDevice1 {device1, device2}
myDevice2 {device3, device4, device5}
```

<span data-ttu-id="e27be-114">以逗號分隔的所有邊緣裝置清單顯示所有指派的非邊緣裝置。</span><span class="sxs-lookup"><span data-stu-id="e27be-114">Show all assigned non-edge devices as comma-separated list of all edge devices.</span></span>

## <span data-ttu-id="e27be-115">參數</span><span class="sxs-lookup"><span data-stu-id="e27be-115">PARAMETERS</span></span>

### <span data-ttu-id="e27be-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e27be-116">-DefaultProfile</span></span>
<span data-ttu-id="e27be-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e27be-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e27be-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="e27be-118">-DeviceId</span></span>
<span data-ttu-id="e27be-119">Edge 裝置的 Id。</span><span class="sxs-lookup"><span data-stu-id="e27be-119">Id of edge device.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e27be-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e27be-120">-InputObject</span></span>
<span data-ttu-id="e27be-121">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="e27be-121">IotHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e27be-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="e27be-122">-IotHubName</span></span>
<span data-ttu-id="e27be-123">Iot 中樞的名稱</span><span class="sxs-lookup"><span data-stu-id="e27be-123">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e27be-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e27be-124">-ResourceGroupName</span></span>
<span data-ttu-id="e27be-125">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="e27be-125">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e27be-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e27be-126">-ResourceId</span></span>
<span data-ttu-id="e27be-127">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="e27be-127">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e27be-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e27be-128">CommonParameters</span></span>
<span data-ttu-id="e27be-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e27be-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e27be-130">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e27be-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e27be-131">輸入</span><span class="sxs-lookup"><span data-stu-id="e27be-131">INPUTS</span></span>

### <span data-ttu-id="e27be-132">PSIotHub （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="e27be-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="e27be-133">System.object</span><span class="sxs-lookup"><span data-stu-id="e27be-133">System.String</span></span>

## <span data-ttu-id="e27be-134">輸出</span><span class="sxs-lookup"><span data-stu-id="e27be-134">OUTPUTS</span></span>

### <span data-ttu-id="e27be-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceChildren</span><span class="sxs-lookup"><span data-stu-id="e27be-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceChildren</span></span>

### <span data-ttu-id="e27be-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevicesChildren []</span><span class="sxs-lookup"><span data-stu-id="e27be-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevicesChildren[]</span></span>

## <span data-ttu-id="e27be-137">筆記</span><span class="sxs-lookup"><span data-stu-id="e27be-137">NOTES</span></span>

## <span data-ttu-id="e27be-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="e27be-138">RELATED LINKS</span></span>