---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubdevicetwin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceTwin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceTwin.md
ms.openlocfilehash: 45966042a2c2c6a660f052280039204a1d5eb908
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911061"
---
# <span data-ttu-id="15830-101">Get-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="15830-101">Get-AzIotHubDeviceTwin</span></span>

## <span data-ttu-id="15830-102">簡介</span><span class="sxs-lookup"><span data-stu-id="15830-102">SYNOPSIS</span></span>
<span data-ttu-id="15830-103">獲得裝置支援。</span><span class="sxs-lookup"><span data-stu-id="15830-103">Gets a device twin.</span></span>

## <span data-ttu-id="15830-104">語法</span><span class="sxs-lookup"><span data-stu-id="15830-104">SYNTAX</span></span>

### <span data-ttu-id="15830-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="15830-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeviceTwin [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="15830-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="15830-106">InputObjectSet</span></span>
```
Get-AzIotHubDeviceTwin [-InputObject] <PSIotHub> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="15830-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="15830-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeviceTwin [-ResourceId] <String> [-DeviceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="15830-108">描述</span><span class="sxs-lookup"><span data-stu-id="15830-108">DESCRIPTION</span></span>
<span data-ttu-id="15830-109">獲得裝置支援。</span><span class="sxs-lookup"><span data-stu-id="15830-109">Gets a device twin.</span></span> <span data-ttu-id="15830-110">請參閱 https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twins 詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="15830-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twins for more information.</span></span>

## <span data-ttu-id="15830-111">例子</span><span class="sxs-lookup"><span data-stu-id="15830-111">EXAMPLES</span></span>

### <span data-ttu-id="15830-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="15830-112">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"
```

<span data-ttu-id="15830-113">會返回裝置物件。</span><span class="sxs-lookup"><span data-stu-id="15830-113">Returns the device twin object.</span></span>

## <span data-ttu-id="15830-114">參數</span><span class="sxs-lookup"><span data-stu-id="15830-114">PARAMETERS</span></span>

### <span data-ttu-id="15830-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15830-115">-DefaultProfile</span></span>
<span data-ttu-id="15830-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="15830-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15830-117">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="15830-117">-DeviceId</span></span>
<span data-ttu-id="15830-118">目標裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="15830-118">Target Device Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15830-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="15830-119">-InputObject</span></span>
<span data-ttu-id="15830-120">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="15830-120">IotHub object</span></span>

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

### <span data-ttu-id="15830-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="15830-121">-IotHubName</span></span>
<span data-ttu-id="15830-122">Iot Hub 的名稱</span><span class="sxs-lookup"><span data-stu-id="15830-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="15830-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15830-123">-ResourceGroupName</span></span>
<span data-ttu-id="15830-124">資源組的名稱</span><span class="sxs-lookup"><span data-stu-id="15830-124">Name of the Resource Group</span></span>

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

### <span data-ttu-id="15830-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="15830-125">-ResourceId</span></span>
<span data-ttu-id="15830-126">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="15830-126">IotHub Resource Id</span></span>

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

### <span data-ttu-id="15830-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15830-127">CommonParameters</span></span>
<span data-ttu-id="15830-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="15830-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15830-129">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="15830-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15830-130">輸入</span><span class="sxs-lookup"><span data-stu-id="15830-130">INPUTS</span></span>

### <span data-ttu-id="15830-131">Microsoft.Azure.Commands.management.IotHub.models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="15830-131">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="15830-132">System.String</span><span class="sxs-lookup"><span data-stu-id="15830-132">System.String</span></span>

## <span data-ttu-id="15830-133">輸出</span><span class="sxs-lookup"><span data-stu-id="15830-133">OUTPUTS</span></span>

### <span data-ttu-id="15830-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="15830-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTwin</span></span>

## <span data-ttu-id="15830-135">筆記</span><span class="sxs-lookup"><span data-stu-id="15830-135">NOTES</span></span>

## <span data-ttu-id="15830-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="15830-136">RELATED LINKS</span></span>
