---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/send-aziothubdevice2cloudmessage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Send-AzIotHubDevice2CloudMessage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Send-AzIotHubDevice2CloudMessage.md
ms.openlocfilehash: 2445ba6a4436af1dad4b940d18c5576bdf9a5bfc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94127844"
---
# <span data-ttu-id="53747-101">Send-AzIotHubDevice2CloudMessage</span><span class="sxs-lookup"><span data-stu-id="53747-101">Send-AzIotHubDevice2CloudMessage</span></span>

## <span data-ttu-id="53747-102">摘要</span><span class="sxs-lookup"><span data-stu-id="53747-102">SYNOPSIS</span></span>
<span data-ttu-id="53747-103">傳送 device to 雲端訊息。</span><span class="sxs-lookup"><span data-stu-id="53747-103">Send device-to-cloud message.</span></span>

## <span data-ttu-id="53747-104">句法</span><span class="sxs-lookup"><span data-stu-id="53747-104">SYNTAX</span></span>

### <span data-ttu-id="53747-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="53747-105">ResourceSet (Default)</span></span>
```
Send-AzIotHubDevice2CloudMessage [-ResourceGroupName] <String> [-IotHubName] <String> -DeviceId <String>
 -Message <String> [-TransportType <PSTransportType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53747-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="53747-106">InputObjectSet</span></span>
```
Send-AzIotHubDevice2CloudMessage [-InputObject] <PSIotHub> -DeviceId <String> -Message <String>
 [-TransportType <PSTransportType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="53747-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="53747-107">ResourceIdSet</span></span>
```
Send-AzIotHubDevice2CloudMessage [-ResourceId] <String> -DeviceId <String> -Message <String>
 [-TransportType <PSTransportType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="53747-108">說明</span><span class="sxs-lookup"><span data-stu-id="53747-108">DESCRIPTION</span></span>
<span data-ttu-id="53747-109">此命令支援使用應用程式和系統屬性傳送郵件。</span><span class="sxs-lookup"><span data-stu-id="53747-109">The command supports sending messages with application and system properties.</span></span>

## <span data-ttu-id="53747-110">示例</span><span class="sxs-lookup"><span data-stu-id="53747-110">EXAMPLES</span></span>

### <span data-ttu-id="53747-111">範例1</span><span class="sxs-lookup"><span data-stu-id="53747-111">Example 1</span></span>
```powershell
PS C:\> Send-AzIotHubDevice2CloudMessage -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Message "Ping from PS"
```

<span data-ttu-id="53747-112">使用預設傳輸類型，將裝置傳送到雲端訊息。</span><span class="sxs-lookup"><span data-stu-id="53747-112">Sending device to cloud message using default transport type.</span></span>

### <span data-ttu-id="53747-113">範例2</span><span class="sxs-lookup"><span data-stu-id="53747-113">Example 2</span></span>
```powershell
PS C:\> Send-AzIotHubDevice2CloudMessage -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Message "Ping from PS" -TransportType Mqtt
```

<span data-ttu-id="53747-114">將 mqtt 裝置傳送到雲端訊息。</span><span class="sxs-lookup"><span data-stu-id="53747-114">Sending an mqtt device to cloud message.</span></span>

## <span data-ttu-id="53747-115">參數</span><span class="sxs-lookup"><span data-stu-id="53747-115">PARAMETERS</span></span>

### <span data-ttu-id="53747-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53747-116">-DefaultProfile</span></span>
<span data-ttu-id="53747-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="53747-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53747-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="53747-118">-DeviceId</span></span>
<span data-ttu-id="53747-119">目標裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="53747-119">Target Device Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53747-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="53747-120">-InputObject</span></span>
<span data-ttu-id="53747-121">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="53747-121">IotHub object</span></span>

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

### <span data-ttu-id="53747-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="53747-122">-IotHubName</span></span>
<span data-ttu-id="53747-123">Iot 中樞的名稱</span><span class="sxs-lookup"><span data-stu-id="53747-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="53747-124">-訊息</span><span class="sxs-lookup"><span data-stu-id="53747-124">-Message</span></span>
<span data-ttu-id="53747-125">傳送給 IoT 中樞的郵件正文。</span><span class="sxs-lookup"><span data-stu-id="53747-125">Message body to send to IoT Hub.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53747-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="53747-126">-PassThru</span></span>
<span data-ttu-id="53747-127">允許傳回布林值物件。</span><span class="sxs-lookup"><span data-stu-id="53747-127">Allows to return the boolean object.</span></span> <span data-ttu-id="53747-128">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="53747-128">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53747-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53747-129">-ResourceGroupName</span></span>
<span data-ttu-id="53747-130">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="53747-130">Name of the Resource Group</span></span>

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

### <span data-ttu-id="53747-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="53747-131">-ResourceId</span></span>
<span data-ttu-id="53747-132">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="53747-132">IotHub Resource Id</span></span>

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

### <span data-ttu-id="53747-133">-TransportType</span><span class="sxs-lookup"><span data-stu-id="53747-133">-TransportType</span></span>
<span data-ttu-id="53747-134">要使用的傳輸類型。</span><span class="sxs-lookup"><span data-stu-id="53747-134">Transport type to use.</span></span>
<span data-ttu-id="53747-135">預設值為 Amqp。</span><span class="sxs-lookup"><span data-stu-id="53747-135">Default is Amqp.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSTransportType
Parameter Sets: (All)
Aliases:
Accepted values: Amqp, Http1, Amqp_WebSocket_Only, Amqp_Tcp_Only, Mqtt, Mqtt_WebSocket_Only, Mqtt_Tcp_Only

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53747-136">-確認</span><span class="sxs-lookup"><span data-stu-id="53747-136">-Confirm</span></span>
<span data-ttu-id="53747-137">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="53747-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53747-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53747-138">-WhatIf</span></span>
<span data-ttu-id="53747-139">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="53747-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53747-140">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="53747-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53747-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53747-141">CommonParameters</span></span>
<span data-ttu-id="53747-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="53747-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53747-143">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="53747-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53747-144">輸入</span><span class="sxs-lookup"><span data-stu-id="53747-144">INPUTS</span></span>

### <span data-ttu-id="53747-145">PSIotHub （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="53747-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="53747-146">System.object</span><span class="sxs-lookup"><span data-stu-id="53747-146">System.String</span></span>

## <span data-ttu-id="53747-147">輸出</span><span class="sxs-lookup"><span data-stu-id="53747-147">OUTPUTS</span></span>

### <span data-ttu-id="53747-148">System.object</span><span class="sxs-lookup"><span data-stu-id="53747-148">System.Boolean</span></span>

## <span data-ttu-id="53747-149">筆記</span><span class="sxs-lookup"><span data-stu-id="53747-149">NOTES</span></span>

## <span data-ttu-id="53747-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="53747-150">RELATED LINKS</span></span>