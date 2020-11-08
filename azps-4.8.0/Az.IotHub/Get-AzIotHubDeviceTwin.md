---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdevicetwin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceTwin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceTwin.md
ms.openlocfilehash: 6d8397ff8b22895614c67592460eadf76aa3fb92
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94127910"
---
# <span data-ttu-id="3aeeb-101">Get-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="3aeeb-101">Get-AzIotHubDeviceTwin</span></span>

## <span data-ttu-id="3aeeb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3aeeb-102">SYNOPSIS</span></span>
<span data-ttu-id="3aeeb-103">取得 device 雙子。</span><span class="sxs-lookup"><span data-stu-id="3aeeb-103">Gets a device twin.</span></span>

## <span data-ttu-id="3aeeb-104">句法</span><span class="sxs-lookup"><span data-stu-id="3aeeb-104">SYNTAX</span></span>

### <span data-ttu-id="3aeeb-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="3aeeb-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeviceTwin [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3aeeb-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="3aeeb-106">InputObjectSet</span></span>
```
Get-AzIotHubDeviceTwin [-InputObject] <PSIotHub> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3aeeb-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="3aeeb-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeviceTwin [-ResourceId] <String> [-DeviceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3aeeb-108">說明</span><span class="sxs-lookup"><span data-stu-id="3aeeb-108">DESCRIPTION</span></span>
<span data-ttu-id="3aeeb-109">取得 device 雙子。</span><span class="sxs-lookup"><span data-stu-id="3aeeb-109">Gets a device twin.</span></span> <span data-ttu-id="3aeeb-110">如需詳細資訊，請參閱 https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twins 。</span><span class="sxs-lookup"><span data-stu-id="3aeeb-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twins for more information.</span></span>

## <span data-ttu-id="3aeeb-111">示例</span><span class="sxs-lookup"><span data-stu-id="3aeeb-111">EXAMPLES</span></span>

### <span data-ttu-id="3aeeb-112">範例1</span><span class="sxs-lookup"><span data-stu-id="3aeeb-112">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"
```

<span data-ttu-id="3aeeb-113">傳回 device 雙子物件。</span><span class="sxs-lookup"><span data-stu-id="3aeeb-113">Returns the device twin object.</span></span>

## <span data-ttu-id="3aeeb-114">參數</span><span class="sxs-lookup"><span data-stu-id="3aeeb-114">PARAMETERS</span></span>

### <span data-ttu-id="3aeeb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3aeeb-115">-DefaultProfile</span></span>
<span data-ttu-id="3aeeb-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3aeeb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3aeeb-117">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="3aeeb-117">-DeviceId</span></span>
<span data-ttu-id="3aeeb-118">目標裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="3aeeb-118">Target Device Id.</span></span>

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

### <span data-ttu-id="3aeeb-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3aeeb-119">-InputObject</span></span>
<span data-ttu-id="3aeeb-120">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="3aeeb-120">IotHub object</span></span>

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

### <span data-ttu-id="3aeeb-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="3aeeb-121">-IotHubName</span></span>
<span data-ttu-id="3aeeb-122">Iot 中樞的名稱</span><span class="sxs-lookup"><span data-stu-id="3aeeb-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="3aeeb-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3aeeb-123">-ResourceGroupName</span></span>
<span data-ttu-id="3aeeb-124">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="3aeeb-124">Name of the Resource Group</span></span>

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

### <span data-ttu-id="3aeeb-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3aeeb-125">-ResourceId</span></span>
<span data-ttu-id="3aeeb-126">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="3aeeb-126">IotHub Resource Id</span></span>

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

### <span data-ttu-id="3aeeb-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3aeeb-127">CommonParameters</span></span>
<span data-ttu-id="3aeeb-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3aeeb-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3aeeb-129">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3aeeb-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3aeeb-130">輸入</span><span class="sxs-lookup"><span data-stu-id="3aeeb-130">INPUTS</span></span>

### <span data-ttu-id="3aeeb-131">PSIotHub （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="3aeeb-131">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="3aeeb-132">System.object</span><span class="sxs-lookup"><span data-stu-id="3aeeb-132">System.String</span></span>

## <span data-ttu-id="3aeeb-133">輸出</span><span class="sxs-lookup"><span data-stu-id="3aeeb-133">OUTPUTS</span></span>

### <span data-ttu-id="3aeeb-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="3aeeb-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTwin</span></span>

## <span data-ttu-id="3aeeb-135">筆記</span><span class="sxs-lookup"><span data-stu-id="3aeeb-135">NOTES</span></span>

## <span data-ttu-id="3aeeb-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="3aeeb-136">RELATED LINKS</span></span>
