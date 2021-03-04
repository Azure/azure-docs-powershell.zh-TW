---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/set-aziothubdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDevice.md
ms.openlocfilehash: c164286e71b198ab19dd1928d6ee495014295306
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902889"
---
# <span data-ttu-id="8cace-101">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="8cace-101">Set-AzIotHubDevice</span></span>

## <span data-ttu-id="8cace-102">簡介</span><span class="sxs-lookup"><span data-stu-id="8cace-102">SYNOPSIS</span></span>
<span data-ttu-id="8cace-103">更新 IoT Hub 裝置。</span><span class="sxs-lookup"><span data-stu-id="8cace-103">Update an IoT Hub device.</span></span>

## <span data-ttu-id="8cace-104">語法</span><span class="sxs-lookup"><span data-stu-id="8cace-104">SYNTAX</span></span>

### <span data-ttu-id="8cace-105">ResourceSetForStatus (預設) </span><span class="sxs-lookup"><span data-stu-id="8cace-105">ResourceSetForStatus (Default)</span></span>
```
Set-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-Status <PSDeviceStatus>] [-StatusReason <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8cace-106">InputObjectSetForAuth</span><span class="sxs-lookup"><span data-stu-id="8cace-106">InputObjectSetForAuth</span></span>
```
Set-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId] <String> [-AuthMethod <PSDeviceAuthType>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8cace-107">InputObjectSetForStatus</span><span class="sxs-lookup"><span data-stu-id="8cace-107">InputObjectSetForStatus</span></span>
```
Set-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId] <String> [-Status <PSDeviceStatus>]
 [-StatusReason <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8cace-108">InputObjectSetForEdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="8cace-108">InputObjectSetForEdgeEnabled</span></span>
```
Set-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId] <String> [-EdgeEnabled <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8cace-109">ResourceSetForAuth</span><span class="sxs-lookup"><span data-stu-id="8cace-109">ResourceSetForAuth</span></span>
```
Set-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8cace-110">ResourceSetForEdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="8cace-110">ResourceSetForEdgeEnabled</span></span>
```
Set-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-EdgeEnabled <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8cace-111">ResourceIdSetForAuth</span><span class="sxs-lookup"><span data-stu-id="8cace-111">ResourceIdSetForAuth</span></span>
```
Set-AzIotHubDevice [-ResourceId] <String> [-DeviceId] <String> [-AuthMethod <PSDeviceAuthType>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8cace-112">ResourceIdSetForStatus</span><span class="sxs-lookup"><span data-stu-id="8cace-112">ResourceIdSetForStatus</span></span>
```
Set-AzIotHubDevice [-ResourceId] <String> [-DeviceId] <String> [-Status <PSDeviceStatus>]
 [-StatusReason <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8cace-113">ResourceIdSetForEdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="8cace-113">ResourceIdSetForEdgeEnabled</span></span>
```
Set-AzIotHubDevice [-ResourceId] <String> [-DeviceId] <String> [-EdgeEnabled <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8cace-114">描述</span><span class="sxs-lookup"><span data-stu-id="8cace-114">DESCRIPTION</span></span>
<span data-ttu-id="8cace-115">更新 IoT Hub 裝置。</span><span class="sxs-lookup"><span data-stu-id="8cace-115">Update an IoT Hub device.</span></span>

## <span data-ttu-id="8cace-116">例子</span><span class="sxs-lookup"><span data-stu-id="8cace-116">EXAMPLES</span></span>

### <span data-ttu-id="8cace-117">範例 1</span><span class="sxs-lookup"><span data-stu-id="8cace-117">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -EdgeEnabled
```

<span data-ttu-id="8cace-118">開啟裝置的邊緣功能。</span><span class="sxs-lookup"><span data-stu-id="8cace-118">Turn on edge capabilities for device.</span></span>

### <span data-ttu-id="8cace-119">範例 2</span><span class="sxs-lookup"><span data-stu-id="8cace-119">Example 2</span></span>
```powershell
PS C:\> Set-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Status Disabled
```

<span data-ttu-id="8cace-120">停用裝置狀態。</span><span class="sxs-lookup"><span data-stu-id="8cace-120">Disable device status.</span></span>

### <span data-ttu-id="8cace-121">範例 3</span><span class="sxs-lookup"><span data-stu-id="8cace-121">Example 3</span></span>
```powershell
PS C:\> Set-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -AuthMethod "x509_ca"
```

<span data-ttu-id="8cace-122">Iot Hub 裝置的更新授權類型。</span><span class="sxs-lookup"><span data-stu-id="8cace-122">Update authorization type of an Iot Hub device.</span></span>

## <span data-ttu-id="8cace-123">參數</span><span class="sxs-lookup"><span data-stu-id="8cace-123">PARAMETERS</span></span>

### <span data-ttu-id="8cace-124">-AuthMethod</span><span class="sxs-lookup"><span data-stu-id="8cace-124">-AuthMethod</span></span>
<span data-ttu-id="8cace-125">這是要建立實體的授權類型。</span><span class="sxs-lookup"><span data-stu-id="8cace-125">The authorization type an entity is to be created with.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceAuthType
Parameter Sets: InputObjectSetForAuth, ResourceSetForAuth, ResourceIdSetForAuth
Aliases:
Accepted values: shared_private_key, x509_thumbprint, x509_ca

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cace-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cace-126">-DefaultProfile</span></span>
<span data-ttu-id="8cace-127">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="8cace-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8cace-128">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="8cace-128">-DeviceId</span></span>
<span data-ttu-id="8cace-129">目標裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="8cace-129">Target Device Id.</span></span>

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

### <span data-ttu-id="8cace-130">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="8cace-130">-EdgeEnabled</span></span>
<span data-ttu-id="8cace-131">指出邊緣啟用的標號。</span><span class="sxs-lookup"><span data-stu-id="8cace-131">Flag indicating edge enablement.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: InputObjectSetForEdgeEnabled, ResourceSetForEdgeEnabled, ResourceIdSetForEdgeEnabled
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cace-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8cace-132">-InputObject</span></span>
<span data-ttu-id="8cace-133">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="8cace-133">IotHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSetForAuth, InputObjectSetForStatus, InputObjectSetForEdgeEnabled
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8cace-134">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="8cace-134">-IotHubName</span></span>
<span data-ttu-id="8cace-135">Iot Hub 的名稱</span><span class="sxs-lookup"><span data-stu-id="8cace-135">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSetForStatus, ResourceSetForAuth, ResourceSetForEdgeEnabled
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cace-136">-PrimaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="8cace-136">-PrimaryThumbprint</span></span>
<span data-ttu-id="8cace-137">要用於主鍵的明確自我簽署憑證指紋。</span><span class="sxs-lookup"><span data-stu-id="8cace-137">Explicit self-signed certificate thumbprint to use for primary key.</span></span>

```yaml
Type: System.String
Parameter Sets: InputObjectSetForAuth, ResourceSetForAuth, ResourceIdSetForAuth
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cace-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8cace-138">-ResourceGroupName</span></span>
<span data-ttu-id="8cace-139">資源組的名稱</span><span class="sxs-lookup"><span data-stu-id="8cace-139">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSetForStatus, ResourceSetForAuth, ResourceSetForEdgeEnabled
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cace-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8cace-140">-ResourceId</span></span>
<span data-ttu-id="8cace-141">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="8cace-141">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSetForAuth, ResourceIdSetForStatus, ResourceIdSetForEdgeEnabled
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cace-142">-SecondaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="8cace-142">-SecondaryThumbprint</span></span>
<span data-ttu-id="8cace-143">明確自我簽署憑證指紋，以用於次要金鑰。</span><span class="sxs-lookup"><span data-stu-id="8cace-143">Explicit self-signed certificate thumbprint to use for secondary key.</span></span>

```yaml
Type: System.String
Parameter Sets: InputObjectSetForAuth, ResourceSetForAuth, ResourceIdSetForAuth
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cace-144">-狀態</span><span class="sxs-lookup"><span data-stu-id="8cace-144">-Status</span></span>
<span data-ttu-id="8cace-145">建立裝置時設定裝置狀態。</span><span class="sxs-lookup"><span data-stu-id="8cace-145">Set device status upon creation.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceStatus
Parameter Sets: ResourceSetForStatus, InputObjectSetForStatus, ResourceIdSetForStatus
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cace-146">-StatusReason</span><span class="sxs-lookup"><span data-stu-id="8cace-146">-StatusReason</span></span>
<span data-ttu-id="8cace-147">裝置狀態的描述。</span><span class="sxs-lookup"><span data-stu-id="8cace-147">Description for device status.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSetForStatus, InputObjectSetForStatus, ResourceIdSetForStatus
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cace-148">-確認</span><span class="sxs-lookup"><span data-stu-id="8cace-148">-Confirm</span></span>
<span data-ttu-id="8cace-149">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="8cace-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8cace-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8cace-150">-WhatIf</span></span>
<span data-ttu-id="8cace-151">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8cace-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8cace-152">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8cace-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8cace-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cace-153">CommonParameters</span></span>
<span data-ttu-id="8cace-154">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="8cace-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cace-155">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="8cace-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cace-156">輸入</span><span class="sxs-lookup"><span data-stu-id="8cace-156">INPUTS</span></span>

### <span data-ttu-id="8cace-157">Microsoft.Azure.Commands.management.IotHub.models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="8cace-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="8cace-158">System.String</span><span class="sxs-lookup"><span data-stu-id="8cace-158">System.String</span></span>

## <span data-ttu-id="8cace-159">輸出</span><span class="sxs-lookup"><span data-stu-id="8cace-159">OUTPUTS</span></span>

### <span data-ttu-id="8cace-160">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span><span class="sxs-lookup"><span data-stu-id="8cace-160">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span></span>

## <span data-ttu-id="8cace-161">筆記</span><span class="sxs-lookup"><span data-stu-id="8cace-161">NOTES</span></span>

## <span data-ttu-id="8cace-162">相關連結</span><span class="sxs-lookup"><span data-stu-id="8cace-162">RELATED LINKS</span></span>
