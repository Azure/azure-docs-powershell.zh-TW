---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/invoke-aziothubquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubQuery.md
ms.openlocfilehash: 955e09ab17644009f281223581ae2f5f45adfb33
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902082"
---
# <span data-ttu-id="27097-101">Invoke-AzIotHubQuery</span><span class="sxs-lookup"><span data-stu-id="27097-101">Invoke-AzIotHubQuery</span></span>

## <span data-ttu-id="27097-102">簡介</span><span class="sxs-lookup"><span data-stu-id="27097-102">SYNOPSIS</span></span>
<span data-ttu-id="27097-103">使用功能強大的 SQL 類似語言查詢 IoT 中樞。</span><span class="sxs-lookup"><span data-stu-id="27097-103">Query an IoT Hub using a powerful SQL-like language.</span></span>

## <span data-ttu-id="27097-104">語法</span><span class="sxs-lookup"><span data-stu-id="27097-104">SYNTAX</span></span>

### <span data-ttu-id="27097-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="27097-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubQuery [-ResourceGroupName] <String> [-IotHubName] <String> [-Query] <String> [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27097-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="27097-106">InputObjectSet</span></span>
```
Invoke-AzIotHubQuery [-InputObject] <PSIotHub> [-Query] <String> [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27097-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="27097-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubQuery [-ResourceId] <String> [-Query] <String> [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27097-108">描述</span><span class="sxs-lookup"><span data-stu-id="27097-108">DESCRIPTION</span></span>
<span data-ttu-id="27097-109">使用強大的 SQL 類似語言查詢 IoT 中樞，以取回裝置和模組元件、工作和郵件路由相關資訊。</span><span class="sxs-lookup"><span data-stu-id="27097-109">Query an IoT Hub using a powerful SQL-like language to retrieve information regarding device and module twins, jobs and message routing.</span></span>
<span data-ttu-id="27097-110">請參閱 https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-query-language 詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="27097-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-query-language for more information.</span></span>

## <span data-ttu-id="27097-111">例子</span><span class="sxs-lookup"><span data-stu-id="27097-111">EXAMPLES</span></span>

### <span data-ttu-id="27097-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="27097-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubQuery -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Query "select * from devices"
```

<span data-ttu-id="27097-113">在 Azure IoT 中心查詢所有裝置的資料。</span><span class="sxs-lookup"><span data-stu-id="27097-113">Query all device twin data in an Azure IoT Hub.</span></span>

### <span data-ttu-id="27097-114">範例 2</span><span class="sxs-lookup"><span data-stu-id="27097-114">Example 2</span></span>
```powershell
PS C:\> Invoke-AzIotHubQuery -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Query "select * from devices.modules where devices.deviceId = 'myDevice1'" -Top 2
```

<span data-ttu-id="27097-115">查詢目標裝置上前 2 個模組的資料。</span><span class="sxs-lookup"><span data-stu-id="27097-115">Query top 2 module twin data on a target device.</span></span>

## <span data-ttu-id="27097-116">參數</span><span class="sxs-lookup"><span data-stu-id="27097-116">PARAMETERS</span></span>

### <span data-ttu-id="27097-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27097-117">-DefaultProfile</span></span>
<span data-ttu-id="27097-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="27097-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27097-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="27097-119">-InputObject</span></span>
<span data-ttu-id="27097-120">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="27097-120">IotHub object</span></span>

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

### <span data-ttu-id="27097-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="27097-121">-IotHubName</span></span>
<span data-ttu-id="27097-122">Iot Hub 的名稱</span><span class="sxs-lookup"><span data-stu-id="27097-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="27097-123">-查詢</span><span class="sxs-lookup"><span data-stu-id="27097-123">-Query</span></span>
<span data-ttu-id="27097-124">要執行的使用者查詢。</span><span class="sxs-lookup"><span data-stu-id="27097-124">User query to be executed.</span></span>

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

### <span data-ttu-id="27097-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27097-125">-ResourceGroupName</span></span>
<span data-ttu-id="27097-126">資源組的名稱</span><span class="sxs-lookup"><span data-stu-id="27097-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="27097-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="27097-127">-ResourceId</span></span>
<span data-ttu-id="27097-128">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="27097-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="27097-129">-頂端</span><span class="sxs-lookup"><span data-stu-id="27097-129">-Top</span></span>
<span data-ttu-id="27097-130">要返回的元素數目上限。</span><span class="sxs-lookup"><span data-stu-id="27097-130">Maximum number of elements to return.</span></span>
<span data-ttu-id="27097-131">根據預設，查詢沒有上限。</span><span class="sxs-lookup"><span data-stu-id="27097-131">By default query has no cap.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27097-132">-確認</span><span class="sxs-lookup"><span data-stu-id="27097-132">-Confirm</span></span>
<span data-ttu-id="27097-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="27097-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27097-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27097-134">-WhatIf</span></span>
<span data-ttu-id="27097-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="27097-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="27097-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="27097-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27097-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27097-137">CommonParameters</span></span>
<span data-ttu-id="27097-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="27097-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27097-139">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="27097-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27097-140">輸入</span><span class="sxs-lookup"><span data-stu-id="27097-140">INPUTS</span></span>

### <span data-ttu-id="27097-141">Microsoft.Azure.Commands.management.IotHub.models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="27097-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="27097-142">System.String</span><span class="sxs-lookup"><span data-stu-id="27097-142">System.String</span></span>

## <span data-ttu-id="27097-143">輸出</span><span class="sxs-lookup"><span data-stu-id="27097-143">OUTPUTS</span></span>

### <span data-ttu-id="27097-144">System.String</span><span class="sxs-lookup"><span data-stu-id="27097-144">System.String</span></span>

## <span data-ttu-id="27097-145">筆記</span><span class="sxs-lookup"><span data-stu-id="27097-145">NOTES</span></span>

## <span data-ttu-id="27097-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="27097-146">RELATED LINKS</span></span>
