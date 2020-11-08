---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubmodulemethod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubModuleMethod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubModuleMethod.md
ms.openlocfilehash: e9faa07f4addabcb556819e1d45b63a0dec0f6b3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94136361"
---
# <span data-ttu-id="93e75-101">Invoke-AzIotHubModuleMethod</span><span class="sxs-lookup"><span data-stu-id="93e75-101">Invoke-AzIotHubModuleMethod</span></span>

## <span data-ttu-id="93e75-102">摘要</span><span class="sxs-lookup"><span data-stu-id="93e75-102">SYNOPSIS</span></span>
<span data-ttu-id="93e75-103">喚醒呼叫 Edge 模組方法。</span><span class="sxs-lookup"><span data-stu-id="93e75-103">Invoke an Edge module method.</span></span>

## <span data-ttu-id="93e75-104">句法</span><span class="sxs-lookup"><span data-stu-id="93e75-104">SYNTAX</span></span>

### <span data-ttu-id="93e75-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="93e75-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubModuleMethod [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ModuleId] <String> -Name <String> [-Payload <String>] [-ResponseTimeOut <Int32>]
 [-ConnectionTimeOut <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="93e75-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="93e75-106">InputObjectSet</span></span>
```
Invoke-AzIotHubModuleMethod [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId] <String> -Name <String>
 [-Payload <String>] [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93e75-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="93e75-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubModuleMethod [-ResourceId] <String> [-DeviceId] <String> [-ModuleId] <String> -Name <String>
 [-Payload <String>] [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93e75-108">說明</span><span class="sxs-lookup"><span data-stu-id="93e75-108">DESCRIPTION</span></span>
<span data-ttu-id="93e75-109">喚醒呼叫 Edge 模組方法。</span><span class="sxs-lookup"><span data-stu-id="93e75-109">Invoke an Edge module method.</span></span> <span data-ttu-id="93e75-110">如需詳細資訊，請參閱 https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-direct-methods 。</span><span class="sxs-lookup"><span data-stu-id="93e75-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-direct-methods for more information.</span></span>

## <span data-ttu-id="93e75-111">示例</span><span class="sxs-lookup"><span data-stu-id="93e75-111">EXAMPLES</span></span>

### <span data-ttu-id="93e75-112">範例1</span><span class="sxs-lookup"><span data-stu-id="93e75-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubModuleMethod -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Name "methodName" -Payload "method-input" -ResponseTimeOut 20 -ConnectionTimeOut 15
```

<span data-ttu-id="93e75-113">喚醒呼叫 Edge 模組方法。</span><span class="sxs-lookup"><span data-stu-id="93e75-113">Invoke an Edge module method.</span></span>

## <span data-ttu-id="93e75-114">參數</span><span class="sxs-lookup"><span data-stu-id="93e75-114">PARAMETERS</span></span>

### <span data-ttu-id="93e75-115">-ConnectionTimeOut</span><span class="sxs-lookup"><span data-stu-id="93e75-115">-ConnectionTimeOut</span></span>
<span data-ttu-id="93e75-116">在成功建立連線之前要等待的秒數。</span><span class="sxs-lookup"><span data-stu-id="93e75-116">Number of seconds to wait until a connection is successfully made.</span></span>
<span data-ttu-id="93e75-117">預設值為10。</span><span class="sxs-lookup"><span data-stu-id="93e75-117">Default is 10.</span></span>

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

### <span data-ttu-id="93e75-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93e75-118">-DefaultProfile</span></span>
<span data-ttu-id="93e75-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="93e75-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93e75-120">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="93e75-120">-DeviceId</span></span>
<span data-ttu-id="93e75-121">目標裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="93e75-121">Target Device Id.</span></span>

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

### <span data-ttu-id="93e75-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="93e75-122">-InputObject</span></span>
<span data-ttu-id="93e75-123">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="93e75-123">IotHub object</span></span>

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

### <span data-ttu-id="93e75-124">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="93e75-124">-IotHubName</span></span>
<span data-ttu-id="93e75-125">Iot 中樞的名稱</span><span class="sxs-lookup"><span data-stu-id="93e75-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="93e75-126">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="93e75-126">-ModuleId</span></span>
<span data-ttu-id="93e75-127">目標裝置的模組識別碼。</span><span class="sxs-lookup"><span data-stu-id="93e75-127">Target device's module id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93e75-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="93e75-128">-Name</span></span>
<span data-ttu-id="93e75-129">要在此裝置模組上調用的方法名稱。</span><span class="sxs-lookup"><span data-stu-id="93e75-129">The name of the method to invoke on this device module.</span></span>

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

### <span data-ttu-id="93e75-130">-負載</span><span class="sxs-lookup"><span data-stu-id="93e75-130">-Payload</span></span>
<span data-ttu-id="93e75-131">要在此裝置模組上調用之方法的負載。</span><span class="sxs-lookup"><span data-stu-id="93e75-131">The payload for the method to invoke on this device module.</span></span>

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

### <span data-ttu-id="93e75-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93e75-132">-ResourceGroupName</span></span>
<span data-ttu-id="93e75-133">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="93e75-133">Name of the Resource Group</span></span>

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

### <span data-ttu-id="93e75-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="93e75-134">-ResourceId</span></span>
<span data-ttu-id="93e75-135">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="93e75-135">IotHub Resource Id</span></span>

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

### <span data-ttu-id="93e75-136">-ResponseTimeOut</span><span class="sxs-lookup"><span data-stu-id="93e75-136">-ResponseTimeOut</span></span>
<span data-ttu-id="93e75-137">在從直接方法接收結果前要等待的秒數。</span><span class="sxs-lookup"><span data-stu-id="93e75-137">Number of seconds to wait until a result is received from the direct method.</span></span>
<span data-ttu-id="93e75-138">預設值為10。</span><span class="sxs-lookup"><span data-stu-id="93e75-138">Default is 10.</span></span>

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

### <span data-ttu-id="93e75-139">-確認</span><span class="sxs-lookup"><span data-stu-id="93e75-139">-Confirm</span></span>
<span data-ttu-id="93e75-140">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="93e75-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93e75-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93e75-141">-WhatIf</span></span>
<span data-ttu-id="93e75-142">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="93e75-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93e75-143">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="93e75-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93e75-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93e75-144">CommonParameters</span></span>
<span data-ttu-id="93e75-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="93e75-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93e75-146">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="93e75-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93e75-147">輸入</span><span class="sxs-lookup"><span data-stu-id="93e75-147">INPUTS</span></span>

### <span data-ttu-id="93e75-148">PSIotHub （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="93e75-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="93e75-149">System.object</span><span class="sxs-lookup"><span data-stu-id="93e75-149">System.String</span></span>

## <span data-ttu-id="93e75-150">輸出</span><span class="sxs-lookup"><span data-stu-id="93e75-150">OUTPUTS</span></span>

### <span data-ttu-id="93e75-151">PSCloudToDeviceMethodResult （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="93e75-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceMethodResult</span></span>

## <span data-ttu-id="93e75-152">筆記</span><span class="sxs-lookup"><span data-stu-id="93e75-152">NOTES</span></span>

## <span data-ttu-id="93e75-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="93e75-153">RELATED LINKS</span></span>
