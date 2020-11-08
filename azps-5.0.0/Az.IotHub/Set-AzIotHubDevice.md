---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDevice.md
ms.openlocfilehash: 0779403a23a36c972a0d5597d40231b5cc026b37
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94141695"
---
# <span data-ttu-id="89fcf-101">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="89fcf-101">Set-AzIotHubDevice</span></span>

## <span data-ttu-id="89fcf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="89fcf-102">SYNOPSIS</span></span>
<span data-ttu-id="89fcf-103">更新 IoT 中心裝置。</span><span class="sxs-lookup"><span data-stu-id="89fcf-103">Update an IoT Hub device.</span></span>

## <span data-ttu-id="89fcf-104">句法</span><span class="sxs-lookup"><span data-stu-id="89fcf-104">SYNTAX</span></span>

### <span data-ttu-id="89fcf-105">ResourceSetForStatus (預設) </span><span class="sxs-lookup"><span data-stu-id="89fcf-105">ResourceSetForStatus (Default)</span></span>
```
Set-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-Status <PSDeviceStatus>] [-StatusReason <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89fcf-106">InputObjectSetForAuth</span><span class="sxs-lookup"><span data-stu-id="89fcf-106">InputObjectSetForAuth</span></span>
```
Set-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId] <String> [-AuthMethod <PSDeviceAuthType>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89fcf-107">InputObjectSetForStatus</span><span class="sxs-lookup"><span data-stu-id="89fcf-107">InputObjectSetForStatus</span></span>
```
Set-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId] <String> [-Status <PSDeviceStatus>]
 [-StatusReason <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89fcf-108">InputObjectSetForEdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="89fcf-108">InputObjectSetForEdgeEnabled</span></span>
```
Set-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId] <String> [-EdgeEnabled <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89fcf-109">ResourceSetForAuth</span><span class="sxs-lookup"><span data-stu-id="89fcf-109">ResourceSetForAuth</span></span>
```
Set-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="89fcf-110">ResourceSetForEdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="89fcf-110">ResourceSetForEdgeEnabled</span></span>
```
Set-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-EdgeEnabled <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89fcf-111">ResourceIdSetForAuth</span><span class="sxs-lookup"><span data-stu-id="89fcf-111">ResourceIdSetForAuth</span></span>
```
Set-AzIotHubDevice [-ResourceId] <String> [-DeviceId] <String> [-AuthMethod <PSDeviceAuthType>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89fcf-112">ResourceIdSetForStatus</span><span class="sxs-lookup"><span data-stu-id="89fcf-112">ResourceIdSetForStatus</span></span>
```
Set-AzIotHubDevice [-ResourceId] <String> [-DeviceId] <String> [-Status <PSDeviceStatus>]
 [-StatusReason <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89fcf-113">ResourceIdSetForEdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="89fcf-113">ResourceIdSetForEdgeEnabled</span></span>
```
Set-AzIotHubDevice [-ResourceId] <String> [-DeviceId] <String> [-EdgeEnabled <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89fcf-114">說明</span><span class="sxs-lookup"><span data-stu-id="89fcf-114">DESCRIPTION</span></span>
<span data-ttu-id="89fcf-115">更新 IoT 中心裝置。</span><span class="sxs-lookup"><span data-stu-id="89fcf-115">Update an IoT Hub device.</span></span>

## <span data-ttu-id="89fcf-116">示例</span><span class="sxs-lookup"><span data-stu-id="89fcf-116">EXAMPLES</span></span>

### <span data-ttu-id="89fcf-117">範例1</span><span class="sxs-lookup"><span data-stu-id="89fcf-117">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -EdgeEnabled
```

<span data-ttu-id="89fcf-118">開啟裝置的邊緣功能。</span><span class="sxs-lookup"><span data-stu-id="89fcf-118">Turn on edge capabilities for device.</span></span>

### <span data-ttu-id="89fcf-119">範例2</span><span class="sxs-lookup"><span data-stu-id="89fcf-119">Example 2</span></span>
```powershell
PS C:\> Set-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Status Disabled
```

<span data-ttu-id="89fcf-120">停用裝置狀態。</span><span class="sxs-lookup"><span data-stu-id="89fcf-120">Disable device status.</span></span>

### <span data-ttu-id="89fcf-121">範例3</span><span class="sxs-lookup"><span data-stu-id="89fcf-121">Example 3</span></span>
```powershell
PS C:\> Set-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -AuthMethod "x509_ca"
```

<span data-ttu-id="89fcf-122">更新 Iot 中心裝置的授權類型。</span><span class="sxs-lookup"><span data-stu-id="89fcf-122">Update authorization type of an Iot Hub device.</span></span>

## <span data-ttu-id="89fcf-123">參數</span><span class="sxs-lookup"><span data-stu-id="89fcf-123">PARAMETERS</span></span>

### <span data-ttu-id="89fcf-124">-AuthMethod</span><span class="sxs-lookup"><span data-stu-id="89fcf-124">-AuthMethod</span></span>
<span data-ttu-id="89fcf-125">建立實體的授權類型。</span><span class="sxs-lookup"><span data-stu-id="89fcf-125">The authorization type an entity is to be created with.</span></span>

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

### <span data-ttu-id="89fcf-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89fcf-126">-DefaultProfile</span></span>
<span data-ttu-id="89fcf-127">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="89fcf-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89fcf-128">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="89fcf-128">-DeviceId</span></span>
<span data-ttu-id="89fcf-129">目標裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="89fcf-129">Target Device Id.</span></span>

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

### <span data-ttu-id="89fcf-130">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="89fcf-130">-EdgeEnabled</span></span>
<span data-ttu-id="89fcf-131">指示 edge 啟用的旗標。</span><span class="sxs-lookup"><span data-stu-id="89fcf-131">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="89fcf-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="89fcf-132">-InputObject</span></span>
<span data-ttu-id="89fcf-133">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="89fcf-133">IotHub object</span></span>

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

### <span data-ttu-id="89fcf-134">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="89fcf-134">-IotHubName</span></span>
<span data-ttu-id="89fcf-135">Iot 中樞的名稱</span><span class="sxs-lookup"><span data-stu-id="89fcf-135">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="89fcf-136">-PrimaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="89fcf-136">-PrimaryThumbprint</span></span>
<span data-ttu-id="89fcf-137">要用於主鍵的明確的自我簽署憑證指紋。</span><span class="sxs-lookup"><span data-stu-id="89fcf-137">Explicit self-signed certificate thumbprint to use for primary key.</span></span>

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

### <span data-ttu-id="89fcf-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89fcf-138">-ResourceGroupName</span></span>
<span data-ttu-id="89fcf-139">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="89fcf-139">Name of the Resource Group</span></span>

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

### <span data-ttu-id="89fcf-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="89fcf-140">-ResourceId</span></span>
<span data-ttu-id="89fcf-141">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="89fcf-141">IotHub Resource Id</span></span>

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

### <span data-ttu-id="89fcf-142">-SecondaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="89fcf-142">-SecondaryThumbprint</span></span>
<span data-ttu-id="89fcf-143">用於輔助金鑰的明確的自我簽署憑證指紋。</span><span class="sxs-lookup"><span data-stu-id="89fcf-143">Explicit self-signed certificate thumbprint to use for secondary key.</span></span>

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

### <span data-ttu-id="89fcf-144">-狀態</span><span class="sxs-lookup"><span data-stu-id="89fcf-144">-Status</span></span>
<span data-ttu-id="89fcf-145">在建立時設定裝置狀態。</span><span class="sxs-lookup"><span data-stu-id="89fcf-145">Set device status upon creation.</span></span>

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

### <span data-ttu-id="89fcf-146">-StatusReason</span><span class="sxs-lookup"><span data-stu-id="89fcf-146">-StatusReason</span></span>
<span data-ttu-id="89fcf-147">裝置狀態的描述。</span><span class="sxs-lookup"><span data-stu-id="89fcf-147">Description for device status.</span></span>

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

### <span data-ttu-id="89fcf-148">-確認</span><span class="sxs-lookup"><span data-stu-id="89fcf-148">-Confirm</span></span>
<span data-ttu-id="89fcf-149">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="89fcf-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89fcf-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89fcf-150">-WhatIf</span></span>
<span data-ttu-id="89fcf-151">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="89fcf-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89fcf-152">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="89fcf-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89fcf-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89fcf-153">CommonParameters</span></span>
<span data-ttu-id="89fcf-154">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="89fcf-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89fcf-155">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="89fcf-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89fcf-156">輸入</span><span class="sxs-lookup"><span data-stu-id="89fcf-156">INPUTS</span></span>

### <span data-ttu-id="89fcf-157">PSIotHub （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="89fcf-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="89fcf-158">System.object</span><span class="sxs-lookup"><span data-stu-id="89fcf-158">System.String</span></span>

## <span data-ttu-id="89fcf-159">輸出</span><span class="sxs-lookup"><span data-stu-id="89fcf-159">OUTPUTS</span></span>

### <span data-ttu-id="89fcf-160">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span><span class="sxs-lookup"><span data-stu-id="89fcf-160">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span></span>

## <span data-ttu-id="89fcf-161">筆記</span><span class="sxs-lookup"><span data-stu-id="89fcf-161">NOTES</span></span>

## <span data-ttu-id="89fcf-162">相關連結</span><span class="sxs-lookup"><span data-stu-id="89fcf-162">RELATED LINKS</span></span>
