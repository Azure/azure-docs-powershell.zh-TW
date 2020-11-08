---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubQuery.md
ms.openlocfilehash: 6445e6281ff69f4eef54a5694f953beaa08ad098
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94136363"
---
# <span data-ttu-id="d896f-101">Invoke-AzIotHubQuery</span><span class="sxs-lookup"><span data-stu-id="d896f-101">Invoke-AzIotHubQuery</span></span>

## <span data-ttu-id="d896f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d896f-102">SYNOPSIS</span></span>
<span data-ttu-id="d896f-103">使用功能強大的 SQL like 語言查詢 IoT 中樞。</span><span class="sxs-lookup"><span data-stu-id="d896f-103">Query an IoT Hub using a powerful SQL-like language.</span></span>

## <span data-ttu-id="d896f-104">句法</span><span class="sxs-lookup"><span data-stu-id="d896f-104">SYNTAX</span></span>

### <span data-ttu-id="d896f-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="d896f-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubQuery [-ResourceGroupName] <String> [-IotHubName] <String> [-Query] <String> [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d896f-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d896f-106">InputObjectSet</span></span>
```
Invoke-AzIotHubQuery [-InputObject] <PSIotHub> [-Query] <String> [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d896f-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="d896f-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubQuery [-ResourceId] <String> [-Query] <String> [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d896f-108">說明</span><span class="sxs-lookup"><span data-stu-id="d896f-108">DESCRIPTION</span></span>
<span data-ttu-id="d896f-109">使用功能強大的 SQL like 語言查詢 IoT 中樞，以取得裝置和模組 twins、作業及訊息路由的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d896f-109">Query an IoT Hub using a powerful SQL-like language to retrieve information regarding device and module twins, jobs and message routing.</span></span>
<span data-ttu-id="d896f-110">如需詳細資訊，請參閱 https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-query-language 。</span><span class="sxs-lookup"><span data-stu-id="d896f-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-query-language for more information.</span></span>

## <span data-ttu-id="d896f-111">示例</span><span class="sxs-lookup"><span data-stu-id="d896f-111">EXAMPLES</span></span>

### <span data-ttu-id="d896f-112">範例1</span><span class="sxs-lookup"><span data-stu-id="d896f-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubQuery -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Query "select * from devices"
```

<span data-ttu-id="d896f-113">查詢 Azure IoT 中樞中所有裝置資料的資料。</span><span class="sxs-lookup"><span data-stu-id="d896f-113">Query all device twin data in an Azure IoT Hub.</span></span>

### <span data-ttu-id="d896f-114">範例2</span><span class="sxs-lookup"><span data-stu-id="d896f-114">Example 2</span></span>
```powershell
PS C:\> Invoke-AzIotHubQuery -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Query "select * from devices.modules where devices.deviceId = 'myDevice1'" -Top 2
```

<span data-ttu-id="d896f-115">在目標裝置上查詢前2個模組上的資料。</span><span class="sxs-lookup"><span data-stu-id="d896f-115">Query top 2 module twin data on a target device.</span></span>

## <span data-ttu-id="d896f-116">參數</span><span class="sxs-lookup"><span data-stu-id="d896f-116">PARAMETERS</span></span>

### <span data-ttu-id="d896f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d896f-117">-DefaultProfile</span></span>
<span data-ttu-id="d896f-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d896f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d896f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d896f-119">-InputObject</span></span>
<span data-ttu-id="d896f-120">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="d896f-120">IotHub object</span></span>

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

### <span data-ttu-id="d896f-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="d896f-121">-IotHubName</span></span>
<span data-ttu-id="d896f-122">Iot 中樞的名稱</span><span class="sxs-lookup"><span data-stu-id="d896f-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="d896f-123">-Query</span><span class="sxs-lookup"><span data-stu-id="d896f-123">-Query</span></span>
<span data-ttu-id="d896f-124">要執行的使用者查詢。</span><span class="sxs-lookup"><span data-stu-id="d896f-124">User query to be executed.</span></span>

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

### <span data-ttu-id="d896f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d896f-125">-ResourceGroupName</span></span>
<span data-ttu-id="d896f-126">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="d896f-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="d896f-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d896f-127">-ResourceId</span></span>
<span data-ttu-id="d896f-128">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="d896f-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="d896f-129">-上方</span><span class="sxs-lookup"><span data-stu-id="d896f-129">-Top</span></span>
<span data-ttu-id="d896f-130">要傳回的元素數目上限。</span><span class="sxs-lookup"><span data-stu-id="d896f-130">Maximum number of elements to return.</span></span>
<span data-ttu-id="d896f-131">依預設查詢沒有上限。</span><span class="sxs-lookup"><span data-stu-id="d896f-131">By default query has no cap.</span></span>

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

### <span data-ttu-id="d896f-132">-確認</span><span class="sxs-lookup"><span data-stu-id="d896f-132">-Confirm</span></span>
<span data-ttu-id="d896f-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d896f-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d896f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d896f-134">-WhatIf</span></span>
<span data-ttu-id="d896f-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d896f-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d896f-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d896f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d896f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d896f-137">CommonParameters</span></span>
<span data-ttu-id="d896f-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d896f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d896f-139">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d896f-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d896f-140">輸入</span><span class="sxs-lookup"><span data-stu-id="d896f-140">INPUTS</span></span>

### <span data-ttu-id="d896f-141">PSIotHub （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="d896f-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="d896f-142">System.object</span><span class="sxs-lookup"><span data-stu-id="d896f-142">System.String</span></span>

## <span data-ttu-id="d896f-143">輸出</span><span class="sxs-lookup"><span data-stu-id="d896f-143">OUTPUTS</span></span>

### <span data-ttu-id="d896f-144">System.object</span><span class="sxs-lookup"><span data-stu-id="d896f-144">System.String</span></span>

## <span data-ttu-id="d896f-145">筆記</span><span class="sxs-lookup"><span data-stu-id="d896f-145">NOTES</span></span>

## <span data-ttu-id="d896f-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="d896f-146">RELATED LINKS</span></span>