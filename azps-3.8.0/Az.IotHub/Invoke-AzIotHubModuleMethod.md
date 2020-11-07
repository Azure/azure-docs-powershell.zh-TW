---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubmodulemethod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubModuleMethod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubModuleMethod.md
ms.openlocfilehash: 818e973d4d7be9fb03e23a23d7264745920f843f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93959761"
---
# <span data-ttu-id="bbafb-101">Invoke-AzIotHubModuleMethod</span><span class="sxs-lookup"><span data-stu-id="bbafb-101">Invoke-AzIotHubModuleMethod</span></span>

## <span data-ttu-id="bbafb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bbafb-102">SYNOPSIS</span></span>
<span data-ttu-id="bbafb-103">喚醒呼叫 Edge 模組方法。</span><span class="sxs-lookup"><span data-stu-id="bbafb-103">Invoke an Edge module method.</span></span>

## <span data-ttu-id="bbafb-104">句法</span><span class="sxs-lookup"><span data-stu-id="bbafb-104">SYNTAX</span></span>

### <span data-ttu-id="bbafb-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="bbafb-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubModuleMethod [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ModuleId] <String> -Name <String> [-Payload <String>] [-ResponseTimeOut <Int32>]
 [-ConnectionTimeOut <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bbafb-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="bbafb-106">InputObjectSet</span></span>
```
Invoke-AzIotHubModuleMethod [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId] <String> -Name <String>
 [-Payload <String>] [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bbafb-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="bbafb-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubModuleMethod [-ResourceId] <String> [-DeviceId] <String> [-ModuleId] <String> -Name <String>
 [-Payload <String>] [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bbafb-108">說明</span><span class="sxs-lookup"><span data-stu-id="bbafb-108">DESCRIPTION</span></span>
<span data-ttu-id="bbafb-109">喚醒呼叫 Edge 模組方法。</span><span class="sxs-lookup"><span data-stu-id="bbafb-109">Invoke an Edge module method.</span></span> <span data-ttu-id="bbafb-110">如需詳細資訊，請參閱 https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-direct-methods 。</span><span class="sxs-lookup"><span data-stu-id="bbafb-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-direct-methods for more information.</span></span>

## <span data-ttu-id="bbafb-111">示例</span><span class="sxs-lookup"><span data-stu-id="bbafb-111">EXAMPLES</span></span>

### <span data-ttu-id="bbafb-112">範例1</span><span class="sxs-lookup"><span data-stu-id="bbafb-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubModuleMethod -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Name "methodName" -Payload "method-input" -ResponseTimeOut 20 -ConnectionTimeOut 15
```

<span data-ttu-id="bbafb-113">喚醒呼叫 Edge 模組方法。</span><span class="sxs-lookup"><span data-stu-id="bbafb-113">Invoke an Edge module method.</span></span>

## <span data-ttu-id="bbafb-114">參數</span><span class="sxs-lookup"><span data-stu-id="bbafb-114">PARAMETERS</span></span>

### <span data-ttu-id="bbafb-115">-ConnectionTimeOut</span><span class="sxs-lookup"><span data-stu-id="bbafb-115">-ConnectionTimeOut</span></span>
<span data-ttu-id="bbafb-116">在成功建立連線之前要等待的秒數。</span><span class="sxs-lookup"><span data-stu-id="bbafb-116">Number of seconds to wait until a connection is successfully made.</span></span>
<span data-ttu-id="bbafb-117">預設值為10。</span><span class="sxs-lookup"><span data-stu-id="bbafb-117">Default is 10.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbafb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbafb-118">-DefaultProfile</span></span>
<span data-ttu-id="bbafb-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bbafb-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbafb-120">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="bbafb-120">-DeviceId</span></span>
<span data-ttu-id="bbafb-121">目標裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="bbafb-121">Target Device Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbafb-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bbafb-122">-InputObject</span></span>
<span data-ttu-id="bbafb-123">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="bbafb-123">IotHub object</span></span>

```yaml
Type: PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bbafb-124">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="bbafb-124">-IotHubName</span></span>
<span data-ttu-id="bbafb-125">Iot 中樞的名稱</span><span class="sxs-lookup"><span data-stu-id="bbafb-125">Name of the Iot Hub</span></span>

```yaml
Type: String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbafb-126">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="bbafb-126">-ModuleId</span></span>
<span data-ttu-id="bbafb-127">目標裝置的模組識別碼。</span><span class="sxs-lookup"><span data-stu-id="bbafb-127">Target device's module id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbafb-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="bbafb-128">-Name</span></span>
<span data-ttu-id="bbafb-129">要在此裝置模組上調用的方法名稱。</span><span class="sxs-lookup"><span data-stu-id="bbafb-129">The name of the method to invoke on this device module.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbafb-130">-負載</span><span class="sxs-lookup"><span data-stu-id="bbafb-130">-Payload</span></span>
<span data-ttu-id="bbafb-131">要在此裝置模組上調用之方法的負載。</span><span class="sxs-lookup"><span data-stu-id="bbafb-131">The payload for the method to invoke on this device module.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbafb-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bbafb-132">-ResourceGroupName</span></span>
<span data-ttu-id="bbafb-133">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="bbafb-133">Name of the Resource Group</span></span>

```yaml
Type: String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbafb-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bbafb-134">-ResourceId</span></span>
<span data-ttu-id="bbafb-135">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="bbafb-135">IotHub Resource Id</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbafb-136">-ResponseTimeOut</span><span class="sxs-lookup"><span data-stu-id="bbafb-136">-ResponseTimeOut</span></span>
<span data-ttu-id="bbafb-137">在從直接方法接收結果前要等待的秒數。</span><span class="sxs-lookup"><span data-stu-id="bbafb-137">Number of seconds to wait until a result is received from the direct method.</span></span>
<span data-ttu-id="bbafb-138">預設值為10。</span><span class="sxs-lookup"><span data-stu-id="bbafb-138">Default is 10.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbafb-139">-確認</span><span class="sxs-lookup"><span data-stu-id="bbafb-139">-Confirm</span></span>
<span data-ttu-id="bbafb-140">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="bbafb-140">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbafb-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bbafb-141">-WhatIf</span></span>
<span data-ttu-id="bbafb-142">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="bbafb-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bbafb-143">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bbafb-143">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbafb-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbafb-144">CommonParameters</span></span>
<span data-ttu-id="bbafb-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bbafb-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="bbafb-146">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bbafb-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbafb-147">輸入</span><span class="sxs-lookup"><span data-stu-id="bbafb-147">INPUTS</span></span>

### <span data-ttu-id="bbafb-148">PSIotHub （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="bbafb-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="bbafb-149">System.object</span><span class="sxs-lookup"><span data-stu-id="bbafb-149">System.String</span></span>

## <span data-ttu-id="bbafb-150">輸出</span><span class="sxs-lookup"><span data-stu-id="bbafb-150">OUTPUTS</span></span>

### <span data-ttu-id="bbafb-151">PSCloudToDeviceMethodResult （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="bbafb-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceMethodResult</span></span>

## <span data-ttu-id="bbafb-152">筆記</span><span class="sxs-lookup"><span data-stu-id="bbafb-152">NOTES</span></span>

## <span data-ttu-id="bbafb-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="bbafb-153">RELATED LINKS</span></span>
