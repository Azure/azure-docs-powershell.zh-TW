---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdevicetwin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceTwin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceTwin.md
ms.openlocfilehash: 6d8397ff8b22895614c67592460eadf76aa3fb92
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98275220"
---
# <span data-ttu-id="b5efe-101">Get-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="b5efe-101">Get-AzIotHubDeviceTwin</span></span>

## <span data-ttu-id="b5efe-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b5efe-102">SYNOPSIS</span></span>
<span data-ttu-id="b5efe-103">取得 device 雙子。</span><span class="sxs-lookup"><span data-stu-id="b5efe-103">Gets a device twin.</span></span>

## <span data-ttu-id="b5efe-104">句法</span><span class="sxs-lookup"><span data-stu-id="b5efe-104">SYNTAX</span></span>

### <span data-ttu-id="b5efe-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="b5efe-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeviceTwin [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b5efe-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b5efe-106">InputObjectSet</span></span>
```
Get-AzIotHubDeviceTwin [-InputObject] <PSIotHub> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b5efe-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="b5efe-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeviceTwin [-ResourceId] <String> [-DeviceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b5efe-108">說明</span><span class="sxs-lookup"><span data-stu-id="b5efe-108">DESCRIPTION</span></span>
<span data-ttu-id="b5efe-109">取得 device 雙子。</span><span class="sxs-lookup"><span data-stu-id="b5efe-109">Gets a device twin.</span></span> <span data-ttu-id="b5efe-110">如需詳細資訊，請參閱 https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twins 。</span><span class="sxs-lookup"><span data-stu-id="b5efe-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twins for more information.</span></span>

## <span data-ttu-id="b5efe-111">示例</span><span class="sxs-lookup"><span data-stu-id="b5efe-111">EXAMPLES</span></span>

### <span data-ttu-id="b5efe-112">範例1</span><span class="sxs-lookup"><span data-stu-id="b5efe-112">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"
```

<span data-ttu-id="b5efe-113">傳回 device 雙子物件。</span><span class="sxs-lookup"><span data-stu-id="b5efe-113">Returns the device twin object.</span></span>

## <span data-ttu-id="b5efe-114">參數</span><span class="sxs-lookup"><span data-stu-id="b5efe-114">PARAMETERS</span></span>

### <span data-ttu-id="b5efe-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5efe-115">-DefaultProfile</span></span>
<span data-ttu-id="b5efe-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b5efe-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5efe-117">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="b5efe-117">-DeviceId</span></span>
<span data-ttu-id="b5efe-118">目標裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="b5efe-118">Target Device Id.</span></span>

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

### <span data-ttu-id="b5efe-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b5efe-119">-InputObject</span></span>
<span data-ttu-id="b5efe-120">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="b5efe-120">IotHub object</span></span>

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

### <span data-ttu-id="b5efe-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="b5efe-121">-IotHubName</span></span>
<span data-ttu-id="b5efe-122">Iot 中樞的名稱</span><span class="sxs-lookup"><span data-stu-id="b5efe-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="b5efe-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5efe-123">-ResourceGroupName</span></span>
<span data-ttu-id="b5efe-124">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="b5efe-124">Name of the Resource Group</span></span>

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

### <span data-ttu-id="b5efe-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b5efe-125">-ResourceId</span></span>
<span data-ttu-id="b5efe-126">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="b5efe-126">IotHub Resource Id</span></span>

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

### <span data-ttu-id="b5efe-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5efe-127">CommonParameters</span></span>
<span data-ttu-id="b5efe-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b5efe-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5efe-129">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b5efe-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5efe-130">輸入</span><span class="sxs-lookup"><span data-stu-id="b5efe-130">INPUTS</span></span>

### <span data-ttu-id="b5efe-131">PSIotHub （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="b5efe-131">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="b5efe-132">System.object</span><span class="sxs-lookup"><span data-stu-id="b5efe-132">System.String</span></span>

## <span data-ttu-id="b5efe-133">輸出</span><span class="sxs-lookup"><span data-stu-id="b5efe-133">OUTPUTS</span></span>

### <span data-ttu-id="b5efe-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="b5efe-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTwin</span></span>

## <span data-ttu-id="b5efe-135">筆記</span><span class="sxs-lookup"><span data-stu-id="b5efe-135">NOTES</span></span>

## <span data-ttu-id="b5efe-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="b5efe-136">RELATED LINKS</span></span>
