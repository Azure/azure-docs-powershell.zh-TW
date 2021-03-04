---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/invoke-aziothubmodulemethod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubModuleMethod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubModuleMethod.md
ms.openlocfilehash: ea2362fc779ada8faf62c863ccffb9e58e078b8f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911013"
---
# <span data-ttu-id="0510b-101">Invoke-AzIotHubModuleMethod</span><span class="sxs-lookup"><span data-stu-id="0510b-101">Invoke-AzIotHubModuleMethod</span></span>

## <span data-ttu-id="0510b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="0510b-102">SYNOPSIS</span></span>
<span data-ttu-id="0510b-103">使用 Edge 模組方法。</span><span class="sxs-lookup"><span data-stu-id="0510b-103">Invoke an Edge module method.</span></span>

## <span data-ttu-id="0510b-104">語法</span><span class="sxs-lookup"><span data-stu-id="0510b-104">SYNTAX</span></span>

### <span data-ttu-id="0510b-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="0510b-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubModuleMethod [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ModuleId] <String> -Name <String> [-Payload <String>] [-ResponseTimeOut <Int32>]
 [-ConnectionTimeOut <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0510b-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="0510b-106">InputObjectSet</span></span>
```
Invoke-AzIotHubModuleMethod [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId] <String> -Name <String>
 [-Payload <String>] [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0510b-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="0510b-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubModuleMethod [-ResourceId] <String> [-DeviceId] <String> [-ModuleId] <String> -Name <String>
 [-Payload <String>] [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0510b-108">描述</span><span class="sxs-lookup"><span data-stu-id="0510b-108">DESCRIPTION</span></span>
<span data-ttu-id="0510b-109">使用 Edge 模組方法。</span><span class="sxs-lookup"><span data-stu-id="0510b-109">Invoke an Edge module method.</span></span> <span data-ttu-id="0510b-110">請參閱 https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-direct-methods 詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="0510b-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-direct-methods for more information.</span></span>

## <span data-ttu-id="0510b-111">例子</span><span class="sxs-lookup"><span data-stu-id="0510b-111">EXAMPLES</span></span>

### <span data-ttu-id="0510b-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="0510b-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubModuleMethod -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Name "methodName" -Payload "method-input" -ResponseTimeOut 20 -ConnectionTimeOut 15
```

<span data-ttu-id="0510b-113">使用 Edge 模組方法。</span><span class="sxs-lookup"><span data-stu-id="0510b-113">Invoke an Edge module method.</span></span>

## <span data-ttu-id="0510b-114">參數</span><span class="sxs-lookup"><span data-stu-id="0510b-114">PARAMETERS</span></span>

### <span data-ttu-id="0510b-115">-ConnectionTimeOut</span><span class="sxs-lookup"><span data-stu-id="0510b-115">-ConnectionTimeOut</span></span>
<span data-ttu-id="0510b-116">等待直到成功建立連接的秒數。</span><span class="sxs-lookup"><span data-stu-id="0510b-116">Number of seconds to wait until a connection is successfully made.</span></span>
<span data-ttu-id="0510b-117">預設值為 10。</span><span class="sxs-lookup"><span data-stu-id="0510b-117">Default is 10.</span></span>

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

### <span data-ttu-id="0510b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0510b-118">-DefaultProfile</span></span>
<span data-ttu-id="0510b-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="0510b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0510b-120">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="0510b-120">-DeviceId</span></span>
<span data-ttu-id="0510b-121">目標裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="0510b-121">Target Device Id.</span></span>

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

### <span data-ttu-id="0510b-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0510b-122">-InputObject</span></span>
<span data-ttu-id="0510b-123">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="0510b-123">IotHub object</span></span>

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

### <span data-ttu-id="0510b-124">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="0510b-124">-IotHubName</span></span>
<span data-ttu-id="0510b-125">Iot Hub 的名稱</span><span class="sxs-lookup"><span data-stu-id="0510b-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="0510b-126">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="0510b-126">-ModuleId</span></span>
<span data-ttu-id="0510b-127">目標裝置模組識別碼。</span><span class="sxs-lookup"><span data-stu-id="0510b-127">Target device's module id.</span></span>

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

### <span data-ttu-id="0510b-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="0510b-128">-Name</span></span>
<span data-ttu-id="0510b-129">此裝置模組上要叫用的方法名稱。</span><span class="sxs-lookup"><span data-stu-id="0510b-129">The name of the method to invoke on this device module.</span></span>

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

### <span data-ttu-id="0510b-130">-有效負載</span><span class="sxs-lookup"><span data-stu-id="0510b-130">-Payload</span></span>
<span data-ttu-id="0510b-131">此裝置模組上所要求之方法的負載。</span><span class="sxs-lookup"><span data-stu-id="0510b-131">The payload for the method to invoke on this device module.</span></span>

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

### <span data-ttu-id="0510b-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0510b-132">-ResourceGroupName</span></span>
<span data-ttu-id="0510b-133">資源組的名稱</span><span class="sxs-lookup"><span data-stu-id="0510b-133">Name of the Resource Group</span></span>

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

### <span data-ttu-id="0510b-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0510b-134">-ResourceId</span></span>
<span data-ttu-id="0510b-135">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="0510b-135">IotHub Resource Id</span></span>

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

### <span data-ttu-id="0510b-136">-ResponseTimeOut</span><span class="sxs-lookup"><span data-stu-id="0510b-136">-ResponseTimeOut</span></span>
<span data-ttu-id="0510b-137">從直接方法收到結果之前要等候的秒數。</span><span class="sxs-lookup"><span data-stu-id="0510b-137">Number of seconds to wait until a result is received from the direct method.</span></span>
<span data-ttu-id="0510b-138">預設值為 10。</span><span class="sxs-lookup"><span data-stu-id="0510b-138">Default is 10.</span></span>

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

### <span data-ttu-id="0510b-139">-確認</span><span class="sxs-lookup"><span data-stu-id="0510b-139">-Confirm</span></span>
<span data-ttu-id="0510b-140">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="0510b-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0510b-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0510b-141">-WhatIf</span></span>
<span data-ttu-id="0510b-142">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0510b-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0510b-143">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0510b-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0510b-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0510b-144">CommonParameters</span></span>
<span data-ttu-id="0510b-145">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="0510b-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0510b-146">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="0510b-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0510b-147">輸入</span><span class="sxs-lookup"><span data-stu-id="0510b-147">INPUTS</span></span>

### <span data-ttu-id="0510b-148">Microsoft.Azure.Commands.management.IotHub.models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="0510b-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="0510b-149">System.String</span><span class="sxs-lookup"><span data-stu-id="0510b-149">System.String</span></span>

## <span data-ttu-id="0510b-150">輸出</span><span class="sxs-lookup"><span data-stu-id="0510b-150">OUTPUTS</span></span>

### <span data-ttu-id="0510b-151">Microsoft.Azure.Commands.management.IotHub.models.PSCloudToDeviceMethodResult</span><span class="sxs-lookup"><span data-stu-id="0510b-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceMethodResult</span></span>

## <span data-ttu-id="0510b-152">筆記</span><span class="sxs-lookup"><span data-stu-id="0510b-152">NOTES</span></span>

## <span data-ttu-id="0510b-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="0510b-153">RELATED LINKS</span></span>
