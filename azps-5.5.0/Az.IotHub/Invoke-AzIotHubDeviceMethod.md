---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubdevicemethod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubDeviceMethod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubDeviceMethod.md
ms.openlocfilehash: 78247b26d2f8e6618d3999389efa509e3f8854b9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100135226"
---
# <span data-ttu-id="1cf18-101">Invoke-AzIotHubDeviceMethod</span><span class="sxs-lookup"><span data-stu-id="1cf18-101">Invoke-AzIotHubDeviceMethod</span></span>

## <span data-ttu-id="1cf18-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1cf18-102">SYNOPSIS</span></span>
<span data-ttu-id="1cf18-103">在裝置上喚醒呼叫直接方法。</span><span class="sxs-lookup"><span data-stu-id="1cf18-103">Invoke a direct method on a device.</span></span>

## <span data-ttu-id="1cf18-104">句法</span><span class="sxs-lookup"><span data-stu-id="1cf18-104">SYNTAX</span></span>

### <span data-ttu-id="1cf18-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="1cf18-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubDeviceMethod [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 -Name <String> [-Payload <String>] [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1cf18-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="1cf18-106">InputObjectSet</span></span>
```
Invoke-AzIotHubDeviceMethod [-InputObject] <PSIotHub> [-DeviceId] <String> -Name <String> [-Payload <String>]
 [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1cf18-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="1cf18-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubDeviceMethod [-ResourceId] <String> [-DeviceId] <String> -Name <String> [-Payload <String>]
 [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1cf18-108">說明</span><span class="sxs-lookup"><span data-stu-id="1cf18-108">DESCRIPTION</span></span>
<span data-ttu-id="1cf18-109">在裝置上喚醒呼叫直接方法。</span><span class="sxs-lookup"><span data-stu-id="1cf18-109">Invoke a direct method on a device.</span></span> <span data-ttu-id="1cf18-110">如需詳細資訊，請參閱 https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-direct-methods 。</span><span class="sxs-lookup"><span data-stu-id="1cf18-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-direct-methods for more information.</span></span>

## <span data-ttu-id="1cf18-111">示例</span><span class="sxs-lookup"><span data-stu-id="1cf18-111">EXAMPLES</span></span>

### <span data-ttu-id="1cf18-112">範例1</span><span class="sxs-lookup"><span data-stu-id="1cf18-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubDeviceMethod -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Name "methodName" -ResponseTimeOut 20 -ConnectionTimeOut 15
```

<span data-ttu-id="1cf18-113">喚醒呼叫裝置方法。</span><span class="sxs-lookup"><span data-stu-id="1cf18-113">Invoke a device method.</span></span>

## <span data-ttu-id="1cf18-114">參數</span><span class="sxs-lookup"><span data-stu-id="1cf18-114">PARAMETERS</span></span>

### <span data-ttu-id="1cf18-115">-ConnectionTimeOut</span><span class="sxs-lookup"><span data-stu-id="1cf18-115">-ConnectionTimeOut</span></span>
<span data-ttu-id="1cf18-116">在成功建立連線之前要等待的秒數。</span><span class="sxs-lookup"><span data-stu-id="1cf18-116">Number of seconds to wait until a connection is successfully made.</span></span>
<span data-ttu-id="1cf18-117">預設值為10。</span><span class="sxs-lookup"><span data-stu-id="1cf18-117">Default is 10.</span></span>

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

### <span data-ttu-id="1cf18-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cf18-118">-DefaultProfile</span></span>
<span data-ttu-id="1cf18-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1cf18-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1cf18-120">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="1cf18-120">-DeviceId</span></span>
<span data-ttu-id="1cf18-121">目標裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="1cf18-121">Target Device Id.</span></span>

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

### <span data-ttu-id="1cf18-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1cf18-122">-InputObject</span></span>
<span data-ttu-id="1cf18-123">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="1cf18-123">IotHub object</span></span>

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

### <span data-ttu-id="1cf18-124">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="1cf18-124">-IotHubName</span></span>
<span data-ttu-id="1cf18-125">Iot 中樞的名稱</span><span class="sxs-lookup"><span data-stu-id="1cf18-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="1cf18-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="1cf18-126">-Name</span></span>
<span data-ttu-id="1cf18-127">要在此裝置上調用的方法名稱。</span><span class="sxs-lookup"><span data-stu-id="1cf18-127">The name of the method to invoke on this device.</span></span>

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

### <span data-ttu-id="1cf18-128">-負載</span><span class="sxs-lookup"><span data-stu-id="1cf18-128">-Payload</span></span>
<span data-ttu-id="1cf18-129">要在此裝置上喚醒之方法的負載。</span><span class="sxs-lookup"><span data-stu-id="1cf18-129">The payload for the method to invoke on this device.</span></span>

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

### <span data-ttu-id="1cf18-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1cf18-130">-ResourceGroupName</span></span>
<span data-ttu-id="1cf18-131">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="1cf18-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="1cf18-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1cf18-132">-ResourceId</span></span>
<span data-ttu-id="1cf18-133">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="1cf18-133">IotHub Resource Id</span></span>

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

### <span data-ttu-id="1cf18-134">-ResponseTimeOut</span><span class="sxs-lookup"><span data-stu-id="1cf18-134">-ResponseTimeOut</span></span>
<span data-ttu-id="1cf18-135">在從直接方法接收結果前要等待的秒數。</span><span class="sxs-lookup"><span data-stu-id="1cf18-135">Number of seconds to wait until a result is received from the direct method.</span></span>
<span data-ttu-id="1cf18-136">預設值為10。</span><span class="sxs-lookup"><span data-stu-id="1cf18-136">Default is 10.</span></span>

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

### <span data-ttu-id="1cf18-137">-確認</span><span class="sxs-lookup"><span data-stu-id="1cf18-137">-Confirm</span></span>
<span data-ttu-id="1cf18-138">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1cf18-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1cf18-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1cf18-139">-WhatIf</span></span>
<span data-ttu-id="1cf18-140">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1cf18-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1cf18-141">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1cf18-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1cf18-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cf18-142">CommonParameters</span></span>
<span data-ttu-id="1cf18-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1cf18-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cf18-144">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1cf18-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cf18-145">輸入</span><span class="sxs-lookup"><span data-stu-id="1cf18-145">INPUTS</span></span>

### <span data-ttu-id="1cf18-146">PSIotHub （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="1cf18-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="1cf18-147">System.object</span><span class="sxs-lookup"><span data-stu-id="1cf18-147">System.String</span></span>

## <span data-ttu-id="1cf18-148">輸出</span><span class="sxs-lookup"><span data-stu-id="1cf18-148">OUTPUTS</span></span>

### <span data-ttu-id="1cf18-149">PSCloudToDeviceMethodResult （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="1cf18-149">Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceMethodResult</span></span>

## <span data-ttu-id="1cf18-150">筆記</span><span class="sxs-lookup"><span data-stu-id="1cf18-150">NOTES</span></span>

## <span data-ttu-id="1cf18-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="1cf18-151">RELATED LINKS</span></span>
