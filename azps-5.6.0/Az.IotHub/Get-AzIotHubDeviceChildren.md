---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubdevicechildren
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceChildren.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceChildren.md
ms.openlocfilehash: ec84ee72caadc4d49c29a72e1e5171e589dc11d3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911074"
---
# <span data-ttu-id="ee228-101">Get-AzIotHubDeviceChildren</span><span class="sxs-lookup"><span data-stu-id="ee228-101">Get-AzIotHubDeviceChildren</span></span>

## <span data-ttu-id="ee228-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ee228-102">SYNOPSIS</span></span>
<span data-ttu-id="ee228-103">列印指定子裝置以逗號分隔的清單。</span><span class="sxs-lookup"><span data-stu-id="ee228-103">Print comma-separated list of assigned child devices.</span></span>

## <span data-ttu-id="ee228-104">語法</span><span class="sxs-lookup"><span data-stu-id="ee228-104">SYNTAX</span></span>

### <span data-ttu-id="ee228-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="ee228-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeviceChildren [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ee228-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ee228-106">InputObjectSet</span></span>
```
Get-AzIotHubDeviceChildren [-InputObject] <PSIotHub> [-DeviceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ee228-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="ee228-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeviceChildren [-ResourceId] <String> [-DeviceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ee228-108">描述</span><span class="sxs-lookup"><span data-stu-id="ee228-108">DESCRIPTION</span></span>
<span data-ttu-id="ee228-109">以逗號分隔清單顯示所有邊緣裝置或指定裝置的所有指派非邊緣裝置。</span><span class="sxs-lookup"><span data-stu-id="ee228-109">Show all assigned non-edge devices as comma-separated list of all edge devices or specified device.</span></span>

## <span data-ttu-id="ee228-110">例子</span><span class="sxs-lookup"><span data-stu-id="ee228-110">EXAMPLES</span></span>

### <span data-ttu-id="ee228-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="ee228-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"

DeviceId  ChildrenDeviceId
--------  ----------------
myDevice1 {device1, device2}
```

<span data-ttu-id="ee228-112">以逗號分隔清單顯示所有指派的非邊緣裝置。</span><span class="sxs-lookup"><span data-stu-id="ee228-112">Show all assigned non-edge devices as comma-separated list.</span></span>

### <span data-ttu-id="ee228-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="ee228-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"

DeviceId  ChildrenDeviceId
--------  ----------------
myDevice1 {device1, device2}
myDevice2 {device3, device4, device5}
```

<span data-ttu-id="ee228-114">以逗號分隔所有邊緣裝置的清單顯示所有指派的非邊緣裝置。</span><span class="sxs-lookup"><span data-stu-id="ee228-114">Show all assigned non-edge devices as comma-separated list of all edge devices.</span></span>

## <span data-ttu-id="ee228-115">參數</span><span class="sxs-lookup"><span data-stu-id="ee228-115">PARAMETERS</span></span>

### <span data-ttu-id="ee228-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee228-116">-DefaultProfile</span></span>
<span data-ttu-id="ee228-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ee228-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee228-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="ee228-118">-DeviceId</span></span>
<span data-ttu-id="ee228-119">邊緣裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="ee228-119">Id of edge device.</span></span>

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

### <span data-ttu-id="ee228-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ee228-120">-InputObject</span></span>
<span data-ttu-id="ee228-121">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="ee228-121">IotHub object</span></span>

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

### <span data-ttu-id="ee228-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="ee228-122">-IotHubName</span></span>
<span data-ttu-id="ee228-123">Iot Hub 的名稱</span><span class="sxs-lookup"><span data-stu-id="ee228-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="ee228-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee228-124">-ResourceGroupName</span></span>
<span data-ttu-id="ee228-125">資源組的名稱</span><span class="sxs-lookup"><span data-stu-id="ee228-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="ee228-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ee228-126">-ResourceId</span></span>
<span data-ttu-id="ee228-127">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="ee228-127">IotHub Resource Id</span></span>

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

### <span data-ttu-id="ee228-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee228-128">CommonParameters</span></span>
<span data-ttu-id="ee228-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ee228-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee228-130">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="ee228-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee228-131">輸入</span><span class="sxs-lookup"><span data-stu-id="ee228-131">INPUTS</span></span>

### <span data-ttu-id="ee228-132">Microsoft.Azure.Commands.management.IotHub.models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="ee228-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="ee228-133">System.String</span><span class="sxs-lookup"><span data-stu-id="ee228-133">System.String</span></span>

## <span data-ttu-id="ee228-134">輸出</span><span class="sxs-lookup"><span data-stu-id="ee228-134">OUTPUTS</span></span>

### <span data-ttu-id="ee228-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice以</span><span class="sxs-lookup"><span data-stu-id="ee228-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceChildren</span></span>

### <span data-ttu-id="ee228-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevices以[]</span><span class="sxs-lookup"><span data-stu-id="ee228-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevicesChildren[]</span></span>

## <span data-ttu-id="ee228-137">筆記</span><span class="sxs-lookup"><span data-stu-id="ee228-137">NOTES</span></span>

## <span data-ttu-id="ee228-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="ee228-138">RELATED LINKS</span></span>
