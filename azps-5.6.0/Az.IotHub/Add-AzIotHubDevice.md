---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/add-aziothubdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDevice.md
ms.openlocfilehash: 0f2e7cd2abc61cde9f060eaabf6634385b6ec258
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913885"
---
# <span data-ttu-id="f5aad-101">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="f5aad-101">Add-AzIotHubDevice</span></span>

## <span data-ttu-id="f5aad-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f5aad-102">SYNOPSIS</span></span>
<span data-ttu-id="f5aad-103">在 IoT 中心中建立裝置。</span><span class="sxs-lookup"><span data-stu-id="f5aad-103">Create a device in an IoT Hub.</span></span>

## <span data-ttu-id="f5aad-104">語法</span><span class="sxs-lookup"><span data-stu-id="f5aad-104">SYNTAX</span></span>

### <span data-ttu-id="f5aad-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="f5aad-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-Status <PSDeviceStatus>] [-StatusReason <String>] [-EdgeEnabled]
 [-Children <String[]>] [-ParentDeviceId <String>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5aad-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f5aad-106">InputObjectSet</span></span>
```
Add-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId] <String> [-AuthMethod <PSDeviceAuthType>]
 [-Status <PSDeviceStatus>] [-StatusReason <String>] [-EdgeEnabled] [-Children <String[]>]
 [-ParentDeviceId <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f5aad-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="f5aad-107">ResourceIdSet</span></span>
```
Add-AzIotHubDevice [-ResourceId] <String> [-DeviceId] <String> [-AuthMethod <PSDeviceAuthType>]
 [-Status <PSDeviceStatus>] [-StatusReason <String>] [-EdgeEnabled] [-Children <String[]>]
 [-ParentDeviceId <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f5aad-108">描述</span><span class="sxs-lookup"><span data-stu-id="f5aad-108">DESCRIPTION</span></span>
<span data-ttu-id="f5aad-109">在 IoT 中心中建立具有不同授權類型的裝置。</span><span class="sxs-lookup"><span data-stu-id="f5aad-109">Create a device with different authorization type in an IoT Hub.</span></span>

## <span data-ttu-id="f5aad-110">例子</span><span class="sxs-lookup"><span data-stu-id="f5aad-110">EXAMPLES</span></span>

### <span data-ttu-id="f5aad-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="f5aad-111">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -AuthMethod "shared_private_key" -EdgeEnabled
```

<span data-ttu-id="f5aad-112">建立已啟用邊緣功能的 IoT 裝置，並預設授權 (共用私密金鑰) 。</span><span class="sxs-lookup"><span data-stu-id="f5aad-112">Create an edge enabled IoT device with default authorization (shared private key).</span></span>

### <span data-ttu-id="f5aad-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="f5aad-113">Example 2</span></span>
```powershell
PS C:\> Add-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice2" -AuthMethod "x509_ca" -Status Disabled -StatusReason "Some Reason"
```

<span data-ttu-id="f5aad-114">使用停用狀態和原因的根 CA 授權建立 IoT 裝置。</span><span class="sxs-lookup"><span data-stu-id="f5aad-114">Create an IoT device with root CA authorization with disabled status and reason.</span></span>

### <span data-ttu-id="f5aad-115">範例 3</span><span class="sxs-lookup"><span data-stu-id="f5aad-115">Example 3</span></span>
```powershell
PS C:\> Add-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -AuthMethod "shared_private_key" -EdgeEnabled -Children device1,device2
```

<span data-ttu-id="f5aad-116">建立已啟用 Edge 的 IoT 裝置，並新增子裝置至該裝置。</span><span class="sxs-lookup"><span data-stu-id="f5aad-116">Create an edge enabled IoT device and add child devices to it.</span></span>

### <span data-ttu-id="f5aad-117">範例 4</span><span class="sxs-lookup"><span data-stu-id="f5aad-117">Example 4</span></span>
```powershell
PS C:\> Add-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -AuthMethod "shared_private_key" -ParentDeviceId parentDevice1
```

<span data-ttu-id="f5aad-118">建立 IoT 裝置並設定其父裝置。</span><span class="sxs-lookup"><span data-stu-id="f5aad-118">Create an IoT device and set its parent device.</span></span>

## <span data-ttu-id="f5aad-119">參數</span><span class="sxs-lookup"><span data-stu-id="f5aad-119">PARAMETERS</span></span>

### <span data-ttu-id="f5aad-120">-AuthMethod</span><span class="sxs-lookup"><span data-stu-id="f5aad-120">-AuthMethod</span></span>
<span data-ttu-id="f5aad-121">這是要建立實體的授權類型。</span><span class="sxs-lookup"><span data-stu-id="f5aad-121">The authorization type an entity is to be created with.</span></span>

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

### <span data-ttu-id="f5aad-122">-兒童</span><span class="sxs-lookup"><span data-stu-id="f5aad-122">-Children</span></span>
<span data-ttu-id="f5aad-123">新增子裝置清單 (逗號分隔) 只包含非邊緣裝置。</span><span class="sxs-lookup"><span data-stu-id="f5aad-123">Add child device list (comma separated) includes only non-edge devices.</span></span>

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

### <span data-ttu-id="f5aad-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5aad-124">-DefaultProfile</span></span>
<span data-ttu-id="f5aad-125">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f5aad-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5aad-126">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="f5aad-126">-DeviceId</span></span>
<span data-ttu-id="f5aad-127">目標裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="f5aad-127">Target Device Id.</span></span>

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

### <span data-ttu-id="f5aad-128">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="f5aad-128">-EdgeEnabled</span></span>
<span data-ttu-id="f5aad-129">指出邊緣啟用的標號。</span><span class="sxs-lookup"><span data-stu-id="f5aad-129">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="f5aad-130">-強制</span><span class="sxs-lookup"><span data-stu-id="f5aad-130">-Force</span></span>
<span data-ttu-id="f5aad-131">覆寫非邊緣裝置父裝置。</span><span class="sxs-lookup"><span data-stu-id="f5aad-131">Overwrites the non-edge device's parent device.</span></span>

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

### <span data-ttu-id="f5aad-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f5aad-132">-InputObject</span></span>
<span data-ttu-id="f5aad-133">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="f5aad-133">IotHub object</span></span>

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

### <span data-ttu-id="f5aad-134">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="f5aad-134">-IotHubName</span></span>
<span data-ttu-id="f5aad-135">Iot Hub 的名稱</span><span class="sxs-lookup"><span data-stu-id="f5aad-135">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="f5aad-136">-PrimaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="f5aad-136">-PrimaryThumbprint</span></span>
<span data-ttu-id="f5aad-137">要用於主鍵的明確自我簽署憑證指紋。</span><span class="sxs-lookup"><span data-stu-id="f5aad-137">Explicit self-signed certificate thumbprint to use for primary key.</span></span>

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

### <span data-ttu-id="f5aad-138">-ParentDeviceId</span><span class="sxs-lookup"><span data-stu-id="f5aad-138">-ParentDeviceId</span></span>
<span data-ttu-id="f5aad-139">邊緣裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="f5aad-139">Id of edge device.</span></span>

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

### <span data-ttu-id="f5aad-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5aad-140">-ResourceGroupName</span></span>
<span data-ttu-id="f5aad-141">資源組的名稱</span><span class="sxs-lookup"><span data-stu-id="f5aad-141">Name of the Resource Group</span></span>

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

### <span data-ttu-id="f5aad-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f5aad-142">-ResourceId</span></span>
<span data-ttu-id="f5aad-143">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="f5aad-143">IotHub Resource Id</span></span>

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

### <span data-ttu-id="f5aad-144">-SecondaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="f5aad-144">-SecondaryThumbprint</span></span>
<span data-ttu-id="f5aad-145">明確自我簽署憑證指紋，以用於次要金鑰。</span><span class="sxs-lookup"><span data-stu-id="f5aad-145">Explicit self-signed certificate thumbprint to use for secondary key.</span></span>

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

### <span data-ttu-id="f5aad-146">-狀態</span><span class="sxs-lookup"><span data-stu-id="f5aad-146">-Status</span></span>
<span data-ttu-id="f5aad-147">建立裝置時設定裝置狀態。</span><span class="sxs-lookup"><span data-stu-id="f5aad-147">Set device status upon creation.</span></span>

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

### <span data-ttu-id="f5aad-148">-StatusReason</span><span class="sxs-lookup"><span data-stu-id="f5aad-148">-StatusReason</span></span>
<span data-ttu-id="f5aad-149">裝置狀態的描述。</span><span class="sxs-lookup"><span data-stu-id="f5aad-149">Description for device status.</span></span>

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

### <span data-ttu-id="f5aad-150">-確認</span><span class="sxs-lookup"><span data-stu-id="f5aad-150">-Confirm</span></span>
<span data-ttu-id="f5aad-151">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="f5aad-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5aad-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5aad-152">-WhatIf</span></span>
<span data-ttu-id="f5aad-153">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f5aad-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5aad-154">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f5aad-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5aad-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5aad-155">CommonParameters</span></span>
<span data-ttu-id="f5aad-156">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f5aad-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5aad-157">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="f5aad-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5aad-158">輸入</span><span class="sxs-lookup"><span data-stu-id="f5aad-158">INPUTS</span></span>

### <span data-ttu-id="f5aad-159">Microsoft.Azure.Commands.management.IotHub.models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="f5aad-159">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="f5aad-160">System.String</span><span class="sxs-lookup"><span data-stu-id="f5aad-160">System.String</span></span>

## <span data-ttu-id="f5aad-161">輸出</span><span class="sxs-lookup"><span data-stu-id="f5aad-161">OUTPUTS</span></span>

### <span data-ttu-id="f5aad-162">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span><span class="sxs-lookup"><span data-stu-id="f5aad-162">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span></span>

## <span data-ttu-id="f5aad-163">筆記</span><span class="sxs-lookup"><span data-stu-id="f5aad-163">NOTES</span></span>

## <span data-ttu-id="f5aad-164">相關連結</span><span class="sxs-lookup"><span data-stu-id="f5aad-164">RELATED LINKS</span></span>
