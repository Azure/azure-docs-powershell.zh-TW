---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/send-aziothubdevice2cloudmessage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Send-AzIotHubDevice2CloudMessage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Send-AzIotHubDevice2CloudMessage.md
ms.openlocfilehash: 41c4f5f4852f499f45b5c765263bdf356dbf90ab
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912389"
---
# <span data-ttu-id="e46c6-101">Send-AzIotHubDevice2CloudMessage</span><span class="sxs-lookup"><span data-stu-id="e46c6-101">Send-AzIotHubDevice2CloudMessage</span></span>

## <span data-ttu-id="e46c6-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e46c6-102">SYNOPSIS</span></span>
<span data-ttu-id="e46c6-103">傳送裝置到雲端訊息。</span><span class="sxs-lookup"><span data-stu-id="e46c6-103">Send device-to-cloud message.</span></span>

## <span data-ttu-id="e46c6-104">語法</span><span class="sxs-lookup"><span data-stu-id="e46c6-104">SYNTAX</span></span>

### <span data-ttu-id="e46c6-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="e46c6-105">ResourceSet (Default)</span></span>
```
Send-AzIotHubDevice2CloudMessage [-ResourceGroupName] <String> [-IotHubName] <String> -DeviceId <String>
 -Message <String> [-TransportType <PSTransportType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e46c6-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="e46c6-106">InputObjectSet</span></span>
```
Send-AzIotHubDevice2CloudMessage [-InputObject] <PSIotHub> -DeviceId <String> -Message <String>
 [-TransportType <PSTransportType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e46c6-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="e46c6-107">ResourceIdSet</span></span>
```
Send-AzIotHubDevice2CloudMessage [-ResourceId] <String> -DeviceId <String> -Message <String>
 [-TransportType <PSTransportType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e46c6-108">描述</span><span class="sxs-lookup"><span data-stu-id="e46c6-108">DESCRIPTION</span></span>
<span data-ttu-id="e46c6-109">該命令支援傳送具有應用程式和系統屬性的郵件。</span><span class="sxs-lookup"><span data-stu-id="e46c6-109">The command supports sending messages with application and system properties.</span></span>

## <span data-ttu-id="e46c6-110">例子</span><span class="sxs-lookup"><span data-stu-id="e46c6-110">EXAMPLES</span></span>

### <span data-ttu-id="e46c6-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="e46c6-111">Example 1</span></span>
```powershell
PS C:\> Send-AzIotHubDevice2CloudMessage -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Message "Ping from PS"
```

<span data-ttu-id="e46c6-112">使用預設傳輸類型將裝置傳送至雲端訊息。</span><span class="sxs-lookup"><span data-stu-id="e46c6-112">Sending device to cloud message using default transport type.</span></span>

### <span data-ttu-id="e46c6-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="e46c6-113">Example 2</span></span>
```powershell
PS C:\> Send-AzIotHubDevice2CloudMessage -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Message "Ping from PS" -TransportType Mqtt
```

<span data-ttu-id="e46c6-114">將裝置傳送至雲端訊息。</span><span class="sxs-lookup"><span data-stu-id="e46c6-114">Sending an mqtt device to cloud message.</span></span>

## <span data-ttu-id="e46c6-115">參數</span><span class="sxs-lookup"><span data-stu-id="e46c6-115">PARAMETERS</span></span>

### <span data-ttu-id="e46c6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e46c6-116">-DefaultProfile</span></span>
<span data-ttu-id="e46c6-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e46c6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e46c6-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="e46c6-118">-DeviceId</span></span>
<span data-ttu-id="e46c6-119">目標裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="e46c6-119">Target Device Id.</span></span>

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

### <span data-ttu-id="e46c6-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e46c6-120">-InputObject</span></span>
<span data-ttu-id="e46c6-121">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="e46c6-121">IotHub object</span></span>

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

### <span data-ttu-id="e46c6-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="e46c6-122">-IotHubName</span></span>
<span data-ttu-id="e46c6-123">Iot Hub 的名稱</span><span class="sxs-lookup"><span data-stu-id="e46c6-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="e46c6-124">-訊息</span><span class="sxs-lookup"><span data-stu-id="e46c6-124">-Message</span></span>
<span data-ttu-id="e46c6-125">要傳送至 IoT 中心的郵件內文。</span><span class="sxs-lookup"><span data-stu-id="e46c6-125">Message body to send to IoT Hub.</span></span>

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

### <span data-ttu-id="e46c6-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e46c6-126">-PassThru</span></span>
<span data-ttu-id="e46c6-127">允許返回布林值物件。</span><span class="sxs-lookup"><span data-stu-id="e46c6-127">Allows to return the boolean object.</span></span> <span data-ttu-id="e46c6-128">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="e46c6-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e46c6-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e46c6-129">-ResourceGroupName</span></span>
<span data-ttu-id="e46c6-130">資源組的名稱</span><span class="sxs-lookup"><span data-stu-id="e46c6-130">Name of the Resource Group</span></span>

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

### <span data-ttu-id="e46c6-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e46c6-131">-ResourceId</span></span>
<span data-ttu-id="e46c6-132">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="e46c6-132">IotHub Resource Id</span></span>

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

### <span data-ttu-id="e46c6-133">-TransportType</span><span class="sxs-lookup"><span data-stu-id="e46c6-133">-TransportType</span></span>
<span data-ttu-id="e46c6-134">要使用的傳輸類型。</span><span class="sxs-lookup"><span data-stu-id="e46c6-134">Transport type to use.</span></span>
<span data-ttu-id="e46c6-135">預設值為 Amqp。</span><span class="sxs-lookup"><span data-stu-id="e46c6-135">Default is Amqp.</span></span>

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

### <span data-ttu-id="e46c6-136">-確認</span><span class="sxs-lookup"><span data-stu-id="e46c6-136">-Confirm</span></span>
<span data-ttu-id="e46c6-137">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="e46c6-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e46c6-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e46c6-138">-WhatIf</span></span>
<span data-ttu-id="e46c6-139">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e46c6-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e46c6-140">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e46c6-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e46c6-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e46c6-141">CommonParameters</span></span>
<span data-ttu-id="e46c6-142">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e46c6-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e46c6-143">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="e46c6-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e46c6-144">輸入</span><span class="sxs-lookup"><span data-stu-id="e46c6-144">INPUTS</span></span>

### <span data-ttu-id="e46c6-145">Microsoft.Azure.Commands.management.IotHub.models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="e46c6-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="e46c6-146">System.String</span><span class="sxs-lookup"><span data-stu-id="e46c6-146">System.String</span></span>

## <span data-ttu-id="e46c6-147">輸出</span><span class="sxs-lookup"><span data-stu-id="e46c6-147">OUTPUTS</span></span>

### <span data-ttu-id="e46c6-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e46c6-148">System.Boolean</span></span>

## <span data-ttu-id="e46c6-149">筆記</span><span class="sxs-lookup"><span data-stu-id="e46c6-149">NOTES</span></span>

## <span data-ttu-id="e46c6-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="e46c6-150">RELATED LINKS</span></span>
