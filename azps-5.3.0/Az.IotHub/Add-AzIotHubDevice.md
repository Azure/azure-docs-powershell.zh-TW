---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDevice.md
ms.openlocfilehash: e13cd1ba814bc5bea66a6a3d06506b9822dd38bd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98449250"
---
# <span data-ttu-id="6b41a-101">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="6b41a-101">Add-AzIotHubDevice</span></span>

## <span data-ttu-id="6b41a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6b41a-102">SYNOPSIS</span></span>
<span data-ttu-id="6b41a-103">在 IoT 中樞中建立裝置。</span><span class="sxs-lookup"><span data-stu-id="6b41a-103">Create a device in an IoT Hub.</span></span>

## <span data-ttu-id="6b41a-104">句法</span><span class="sxs-lookup"><span data-stu-id="6b41a-104">SYNTAX</span></span>

### <span data-ttu-id="6b41a-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="6b41a-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-Status <PSDeviceStatus>] [-StatusReason <String>] [-EdgeEnabled]
 [-Children <String[]>] [-ParentDeviceId <String>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b41a-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="6b41a-106">InputObjectSet</span></span>
```
Add-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId] <String> [-AuthMethod <PSDeviceAuthType>]
 [-Status <PSDeviceStatus>] [-StatusReason <String>] [-EdgeEnabled] [-Children <String[]>]
 [-ParentDeviceId <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6b41a-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="6b41a-107">ResourceIdSet</span></span>
```
Add-AzIotHubDevice [-ResourceId] <String> [-DeviceId] <String> [-AuthMethod <PSDeviceAuthType>]
 [-Status <PSDeviceStatus>] [-StatusReason <String>] [-EdgeEnabled] [-Children <String[]>]
 [-ParentDeviceId <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6b41a-108">說明</span><span class="sxs-lookup"><span data-stu-id="6b41a-108">DESCRIPTION</span></span>
<span data-ttu-id="6b41a-109">在 IoT 中樞中建立具有不同授權類型的裝置。</span><span class="sxs-lookup"><span data-stu-id="6b41a-109">Create a device with different authorization type in an IoT Hub.</span></span>

## <span data-ttu-id="6b41a-110">示例</span><span class="sxs-lookup"><span data-stu-id="6b41a-110">EXAMPLES</span></span>

### <span data-ttu-id="6b41a-111">範例1</span><span class="sxs-lookup"><span data-stu-id="6b41a-111">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -AuthMethod "shared_private_key" -EdgeEnabled
```

<span data-ttu-id="6b41a-112">使用預設授權建立邊緣啟用的 IoT 裝置， (共用私密金鑰) 。</span><span class="sxs-lookup"><span data-stu-id="6b41a-112">Create an edge enabled IoT device with default authorization (shared private key).</span></span>

### <span data-ttu-id="6b41a-113">範例2</span><span class="sxs-lookup"><span data-stu-id="6b41a-113">Example 2</span></span>
```powershell
PS C:\> Add-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice2" -AuthMethod "x509_ca" -Status Disabled -StatusReason "Some Reason"
```

<span data-ttu-id="6b41a-114">使用已停用狀態和原因，建立含根 CA 授權的 IoT 裝置。</span><span class="sxs-lookup"><span data-stu-id="6b41a-114">Create an IoT device with root CA authorization with disabled status and reason.</span></span>

### <span data-ttu-id="6b41a-115">範例3</span><span class="sxs-lookup"><span data-stu-id="6b41a-115">Example 3</span></span>
```powershell
PS C:\> Add-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -AuthMethod "shared_private_key" -EdgeEnabled -Children device1,device2
```

<span data-ttu-id="6b41a-116">建立啟用邊緣的 IoT 裝置，並將子裝置新增到其中。</span><span class="sxs-lookup"><span data-stu-id="6b41a-116">Create an edge enabled IoT device and add child devices to it.</span></span>

### <span data-ttu-id="6b41a-117">範例4</span><span class="sxs-lookup"><span data-stu-id="6b41a-117">Example 4</span></span>
```powershell
PS C:\> Add-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -AuthMethod "shared_private_key" -ParentDeviceId parentDevice1
```

<span data-ttu-id="6b41a-118">建立 IoT 裝置並設定其上層裝置。</span><span class="sxs-lookup"><span data-stu-id="6b41a-118">Create an IoT device and set its parent device.</span></span>

## <span data-ttu-id="6b41a-119">參數</span><span class="sxs-lookup"><span data-stu-id="6b41a-119">PARAMETERS</span></span>

### <span data-ttu-id="6b41a-120">-AuthMethod</span><span class="sxs-lookup"><span data-stu-id="6b41a-120">-AuthMethod</span></span>
<span data-ttu-id="6b41a-121">建立實體的授權類型。</span><span class="sxs-lookup"><span data-stu-id="6b41a-121">The authorization type an entity is to be created with.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceAuthType
Parameter Sets: (All)
Aliases:
Accepted values: shared_private_key, x509_thumbprint, x509_ca

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b41a-122">-兒童</span><span class="sxs-lookup"><span data-stu-id="6b41a-122">-Children</span></span>
<span data-ttu-id="6b41a-123">[新增子裝置清單] (以逗號分隔) 只包含非邊緣裝置。</span><span class="sxs-lookup"><span data-stu-id="6b41a-123">Add child device list (comma separated) includes only non-edge devices.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b41a-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b41a-124">-DefaultProfile</span></span>
<span data-ttu-id="6b41a-125">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6b41a-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b41a-126">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="6b41a-126">-DeviceId</span></span>
<span data-ttu-id="6b41a-127">目標裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="6b41a-127">Target Device Id.</span></span>

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

### <span data-ttu-id="6b41a-128">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="6b41a-128">-EdgeEnabled</span></span>
<span data-ttu-id="6b41a-129">指示 edge 啟用的旗標。</span><span class="sxs-lookup"><span data-stu-id="6b41a-129">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="6b41a-130">-Force</span><span class="sxs-lookup"><span data-stu-id="6b41a-130">-Force</span></span>
<span data-ttu-id="6b41a-131">覆寫非邊緣裝置的父裝置。</span><span class="sxs-lookup"><span data-stu-id="6b41a-131">Overwrites the non-edge device's parent device.</span></span>

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

### <span data-ttu-id="6b41a-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6b41a-132">-InputObject</span></span>
<span data-ttu-id="6b41a-133">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="6b41a-133">IotHub object</span></span>

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

### <span data-ttu-id="6b41a-134">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="6b41a-134">-IotHubName</span></span>
<span data-ttu-id="6b41a-135">Iot 中樞的名稱</span><span class="sxs-lookup"><span data-stu-id="6b41a-135">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="6b41a-136">-PrimaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="6b41a-136">-PrimaryThumbprint</span></span>
<span data-ttu-id="6b41a-137">要用於主鍵的明確的自我簽署憑證指紋。</span><span class="sxs-lookup"><span data-stu-id="6b41a-137">Explicit self-signed certificate thumbprint to use for primary key.</span></span>

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

### <span data-ttu-id="6b41a-138">-ParentDeviceId</span><span class="sxs-lookup"><span data-stu-id="6b41a-138">-ParentDeviceId</span></span>
<span data-ttu-id="6b41a-139">Edge 裝置的 Id。</span><span class="sxs-lookup"><span data-stu-id="6b41a-139">Id of edge device.</span></span>

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

### <span data-ttu-id="6b41a-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b41a-140">-ResourceGroupName</span></span>
<span data-ttu-id="6b41a-141">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="6b41a-141">Name of the Resource Group</span></span>

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

### <span data-ttu-id="6b41a-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6b41a-142">-ResourceId</span></span>
<span data-ttu-id="6b41a-143">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="6b41a-143">IotHub Resource Id</span></span>

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

### <span data-ttu-id="6b41a-144">-SecondaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="6b41a-144">-SecondaryThumbprint</span></span>
<span data-ttu-id="6b41a-145">用於輔助金鑰的明確的自我簽署憑證指紋。</span><span class="sxs-lookup"><span data-stu-id="6b41a-145">Explicit self-signed certificate thumbprint to use for secondary key.</span></span>

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

### <span data-ttu-id="6b41a-146">-狀態</span><span class="sxs-lookup"><span data-stu-id="6b41a-146">-Status</span></span>
<span data-ttu-id="6b41a-147">在建立時設定裝置狀態。</span><span class="sxs-lookup"><span data-stu-id="6b41a-147">Set device status upon creation.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceStatus
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b41a-148">-StatusReason</span><span class="sxs-lookup"><span data-stu-id="6b41a-148">-StatusReason</span></span>
<span data-ttu-id="6b41a-149">裝置狀態的描述。</span><span class="sxs-lookup"><span data-stu-id="6b41a-149">Description for device status.</span></span>

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

### <span data-ttu-id="6b41a-150">-確認</span><span class="sxs-lookup"><span data-stu-id="6b41a-150">-Confirm</span></span>
<span data-ttu-id="6b41a-151">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6b41a-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b41a-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b41a-152">-WhatIf</span></span>
<span data-ttu-id="6b41a-153">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6b41a-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b41a-154">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6b41a-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b41a-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b41a-155">CommonParameters</span></span>
<span data-ttu-id="6b41a-156">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6b41a-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b41a-157">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6b41a-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b41a-158">輸入</span><span class="sxs-lookup"><span data-stu-id="6b41a-158">INPUTS</span></span>

### <span data-ttu-id="6b41a-159">PSIotHub （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="6b41a-159">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="6b41a-160">System.object</span><span class="sxs-lookup"><span data-stu-id="6b41a-160">System.String</span></span>

## <span data-ttu-id="6b41a-161">輸出</span><span class="sxs-lookup"><span data-stu-id="6b41a-161">OUTPUTS</span></span>

### <span data-ttu-id="6b41a-162">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span><span class="sxs-lookup"><span data-stu-id="6b41a-162">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span></span>

## <span data-ttu-id="6b41a-163">筆記</span><span class="sxs-lookup"><span data-stu-id="6b41a-163">NOTES</span></span>

## <span data-ttu-id="6b41a-164">相關連結</span><span class="sxs-lookup"><span data-stu-id="6b41a-164">RELATED LINKS</span></span>
