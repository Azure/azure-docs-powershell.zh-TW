---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/invoke-aziothubdevicemethod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubDeviceMethod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubDeviceMethod.md
ms.openlocfilehash: 4c3782496041be7328ede29fad5ab3818791a0be
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904658"
---
# <span data-ttu-id="6f174-101">Invoke-AzIotHubDeviceMethod</span><span class="sxs-lookup"><span data-stu-id="6f174-101">Invoke-AzIotHubDeviceMethod</span></span>

## <span data-ttu-id="6f174-102">簡介</span><span class="sxs-lookup"><span data-stu-id="6f174-102">SYNOPSIS</span></span>
<span data-ttu-id="6f174-103">在裝置上調用直接方法。</span><span class="sxs-lookup"><span data-stu-id="6f174-103">Invoke a direct method on a device.</span></span>

## <span data-ttu-id="6f174-104">語法</span><span class="sxs-lookup"><span data-stu-id="6f174-104">SYNTAX</span></span>

### <span data-ttu-id="6f174-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="6f174-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubDeviceMethod [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 -Name <String> [-Payload <String>] [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f174-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="6f174-106">InputObjectSet</span></span>
```
Invoke-AzIotHubDeviceMethod [-InputObject] <PSIotHub> [-DeviceId] <String> -Name <String> [-Payload <String>]
 [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f174-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="6f174-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubDeviceMethod [-ResourceId] <String> [-DeviceId] <String> -Name <String> [-Payload <String>]
 [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f174-108">描述</span><span class="sxs-lookup"><span data-stu-id="6f174-108">DESCRIPTION</span></span>
<span data-ttu-id="6f174-109">在裝置上調用直接方法。</span><span class="sxs-lookup"><span data-stu-id="6f174-109">Invoke a direct method on a device.</span></span> <span data-ttu-id="6f174-110">請參閱 https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-direct-methods 詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="6f174-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-direct-methods for more information.</span></span>

## <span data-ttu-id="6f174-111">例子</span><span class="sxs-lookup"><span data-stu-id="6f174-111">EXAMPLES</span></span>

### <span data-ttu-id="6f174-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="6f174-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubDeviceMethod -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Name "methodName" -ResponseTimeOut 20 -ConnectionTimeOut 15
```

<span data-ttu-id="6f174-113">調用裝置方法。</span><span class="sxs-lookup"><span data-stu-id="6f174-113">Invoke a device method.</span></span>

## <span data-ttu-id="6f174-114">參數</span><span class="sxs-lookup"><span data-stu-id="6f174-114">PARAMETERS</span></span>

### <span data-ttu-id="6f174-115">-ConnectionTimeOut</span><span class="sxs-lookup"><span data-stu-id="6f174-115">-ConnectionTimeOut</span></span>
<span data-ttu-id="6f174-116">等待直到成功建立連接的秒數。</span><span class="sxs-lookup"><span data-stu-id="6f174-116">Number of seconds to wait until a connection is successfully made.</span></span>
<span data-ttu-id="6f174-117">預設值為 10。</span><span class="sxs-lookup"><span data-stu-id="6f174-117">Default is 10.</span></span>

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

### <span data-ttu-id="6f174-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f174-118">-DefaultProfile</span></span>
<span data-ttu-id="6f174-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="6f174-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f174-120">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="6f174-120">-DeviceId</span></span>
<span data-ttu-id="6f174-121">目標裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="6f174-121">Target Device Id.</span></span>

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

### <span data-ttu-id="6f174-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6f174-122">-InputObject</span></span>
<span data-ttu-id="6f174-123">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="6f174-123">IotHub object</span></span>

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

### <span data-ttu-id="6f174-124">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="6f174-124">-IotHubName</span></span>
<span data-ttu-id="6f174-125">Iot Hub 的名稱</span><span class="sxs-lookup"><span data-stu-id="6f174-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="6f174-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="6f174-126">-Name</span></span>
<span data-ttu-id="6f174-127">此裝置上要叫用的方法名稱。</span><span class="sxs-lookup"><span data-stu-id="6f174-127">The name of the method to invoke on this device.</span></span>

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

### <span data-ttu-id="6f174-128">-有效負載</span><span class="sxs-lookup"><span data-stu-id="6f174-128">-Payload</span></span>
<span data-ttu-id="6f174-129">此裝置上所要求之方法的負載。</span><span class="sxs-lookup"><span data-stu-id="6f174-129">The payload for the method to invoke on this device.</span></span>

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

### <span data-ttu-id="6f174-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f174-130">-ResourceGroupName</span></span>
<span data-ttu-id="6f174-131">資源組的名稱</span><span class="sxs-lookup"><span data-stu-id="6f174-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="6f174-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6f174-132">-ResourceId</span></span>
<span data-ttu-id="6f174-133">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="6f174-133">IotHub Resource Id</span></span>

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

### <span data-ttu-id="6f174-134">-ResponseTimeOut</span><span class="sxs-lookup"><span data-stu-id="6f174-134">-ResponseTimeOut</span></span>
<span data-ttu-id="6f174-135">從直接方法收到結果之前要等候的秒數。</span><span class="sxs-lookup"><span data-stu-id="6f174-135">Number of seconds to wait until a result is received from the direct method.</span></span>
<span data-ttu-id="6f174-136">預設值為 10。</span><span class="sxs-lookup"><span data-stu-id="6f174-136">Default is 10.</span></span>

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

### <span data-ttu-id="6f174-137">-確認</span><span class="sxs-lookup"><span data-stu-id="6f174-137">-Confirm</span></span>
<span data-ttu-id="6f174-138">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="6f174-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f174-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f174-139">-WhatIf</span></span>
<span data-ttu-id="6f174-140">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6f174-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f174-141">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6f174-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f174-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f174-142">CommonParameters</span></span>
<span data-ttu-id="6f174-143">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="6f174-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f174-144">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="6f174-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f174-145">輸入</span><span class="sxs-lookup"><span data-stu-id="6f174-145">INPUTS</span></span>

### <span data-ttu-id="6f174-146">Microsoft.Azure.Commands.management.IotHub.models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="6f174-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="6f174-147">System.String</span><span class="sxs-lookup"><span data-stu-id="6f174-147">System.String</span></span>

## <span data-ttu-id="6f174-148">輸出</span><span class="sxs-lookup"><span data-stu-id="6f174-148">OUTPUTS</span></span>

### <span data-ttu-id="6f174-149">Microsoft.Azure.Commands.management.IotHub.models.PSCloudToDeviceMethodResult</span><span class="sxs-lookup"><span data-stu-id="6f174-149">Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceMethodResult</span></span>

## <span data-ttu-id="6f174-150">筆記</span><span class="sxs-lookup"><span data-stu-id="6f174-150">NOTES</span></span>

## <span data-ttu-id="6f174-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="6f174-151">RELATED LINKS</span></span>
