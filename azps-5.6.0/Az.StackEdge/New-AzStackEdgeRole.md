---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/new-azstackedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeRole.md
ms.openlocfilehash: 785c092333d0e083ed3ee356a0c4e76d6188b96b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915770"
---
# <span data-ttu-id="e4e3e-101">New-AzStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="e4e3e-101">New-AzStackEdgeRole</span></span>

## <span data-ttu-id="e4e3e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e4e3e-102">SYNOPSIS</span></span>
<span data-ttu-id="e4e3e-103">為裝置建立新角色</span><span class="sxs-lookup"><span data-stu-id="e4e3e-103">Creates a new Role for a device</span></span>

## <span data-ttu-id="e4e3e-104">語法</span><span class="sxs-lookup"><span data-stu-id="e4e3e-104">SYNTAX</span></span>

### <span data-ttu-id="e4e3e-105">ConnectionStringParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="e4e3e-105">ConnectionStringParameterSet (Default)</span></span>
```
New-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-ConnectionString]
 -IotDeviceConnectionString <SecureString> -IotEdgeDeviceConnectionString <SecureString>
 -EncryptionKey <SecureString> -Platform <String> [-RoleStatus <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4e3e-106">IotParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4e3e-106">IotParameterSet</span></span>
```
New-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-DeviceProperty]
 -IotDeviceId <String> -IotDeviceAccessKey <SecureString> -IotEdgeDeviceId <String>
 -IotEdgeDeviceAccessKey <SecureString> -IotHostHub <String> -EncryptionKey <SecureString> -Platform <String>
 [-RoleStatus <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e4e3e-107">描述</span><span class="sxs-lookup"><span data-stu-id="e4e3e-107">DESCRIPTION</span></span>
<span data-ttu-id="e4e3e-108">**New-AzStackEdgeRole** Cmdlet 為 Stack Edge 裝置建立新角色。</span><span class="sxs-lookup"><span data-stu-id="e4e3e-108">The **New-AzStackEdgeRole** cmdlet creates a new Role for a Stack Edge device.</span></span>

## <span data-ttu-id="e4e3e-109">例子</span><span class="sxs-lookup"><span data-stu-id="e4e3e-109">EXAMPLES</span></span>

### <span data-ttu-id="e4e3e-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="e4e3e-110">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name iotrole -DeviceProperties
 -IotDeviceId iotDeviceId -IotDeviceAccessKey iotAccessKey -IotEdgeDeviceId iotEdgeDeviceId -IotEdgeDeviceAccessKey iotEdgeDeviceAccessKey
 -IotHostHub "ehub.azure-devices.net" -EncryptionKey @SecureString -Platform Linux -RoleStatus Enabled

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
iotrole ehub.azure-devices.net Linux    Enabled iotEdgeDeviceId   iotDeviceId  resourceGroupName
```

## <span data-ttu-id="e4e3e-111">參數</span><span class="sxs-lookup"><span data-stu-id="e4e3e-111">PARAMETERS</span></span>

### <span data-ttu-id="e4e3e-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e4e3e-112">-AsJob</span></span>
<span data-ttu-id="e4e3e-113">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e4e3e-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e4e3e-114">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="e4e3e-114">-ConnectionString</span></span>
<span data-ttu-id="e4e3e-115">提供連接字串</span><span class="sxs-lookup"><span data-stu-id="e4e3e-115">To Provide Connection Strings</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ConnectionStringParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4e3e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4e3e-116">-DefaultProfile</span></span>
<span data-ttu-id="e4e3e-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e4e3e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4e3e-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="e4e3e-118">-DeviceName</span></span>
<span data-ttu-id="e4e3e-119">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="e4e3e-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4e3e-120">-DeviceProperty</span><span class="sxs-lookup"><span data-stu-id="e4e3e-120">-DeviceProperty</span></span>
<span data-ttu-id="e4e3e-121">提供裝置屬性</span><span class="sxs-lookup"><span data-stu-id="e4e3e-121">To Provide Device Properties</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: IotParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4e3e-122">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="e4e3e-122">-EncryptionKey</span></span>
<span data-ttu-id="e4e3e-123">Edge 裝置加密金鑰</span><span class="sxs-lookup"><span data-stu-id="e4e3e-123">Encryption key of the Edge device</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4e3e-124">-IotDeviceAccessKey</span><span class="sxs-lookup"><span data-stu-id="e4e3e-124">-IotDeviceAccessKey</span></span>
<span data-ttu-id="e4e3e-125">Iot 裝置便捷鍵</span><span class="sxs-lookup"><span data-stu-id="e4e3e-125">Iot Device Access Key</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: IotParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4e3e-126">-IotDeviceConnectionString</span><span class="sxs-lookup"><span data-stu-id="e4e3e-126">-IotDeviceConnectionString</span></span>
<span data-ttu-id="e4e3e-127">請提供 IOT 裝置的連接字串</span><span class="sxs-lookup"><span data-stu-id="e4e3e-127">Please provide connection string of IOT Device</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ConnectionStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4e3e-128">-IotDeviceId</span><span class="sxs-lookup"><span data-stu-id="e4e3e-128">-IotDeviceId</span></span>
<span data-ttu-id="e4e3e-129">Iot 裝置裝置識別碼</span><span class="sxs-lookup"><span data-stu-id="e4e3e-129">Device Id of the Iot Device</span></span>

```yaml
Type: System.String
Parameter Sets: IotParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4e3e-130">-IotEdgeDeviceAccessKey</span><span class="sxs-lookup"><span data-stu-id="e4e3e-130">-IotEdgeDeviceAccessKey</span></span>
<span data-ttu-id="e4e3e-131">Iot Edge 裝置上的便捷鍵</span><span class="sxs-lookup"><span data-stu-id="e4e3e-131">Access key of the Iot Edge device</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: IotParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4e3e-132">-IotEdgeDeviceConnectionString</span><span class="sxs-lookup"><span data-stu-id="e4e3e-132">-IotEdgeDeviceConnectionString</span></span>
<span data-ttu-id="e4e3e-133">請提供 Edge 裝置的連接字串</span><span class="sxs-lookup"><span data-stu-id="e4e3e-133">Please provide connection string of Edge Device</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ConnectionStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4e3e-134">-IotEdgeDeviceId</span><span class="sxs-lookup"><span data-stu-id="e4e3e-134">-IotEdgeDeviceId</span></span>
<span data-ttu-id="e4e3e-135">Iot Edge 裝置識別碼</span><span class="sxs-lookup"><span data-stu-id="e4e3e-135">Id of the Iot Edge Device</span></span>

```yaml
Type: System.String
Parameter Sets: IotParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4e3e-136">-IotHostHub</span><span class="sxs-lookup"><span data-stu-id="e4e3e-136">-IotHostHub</span></span>
<span data-ttu-id="e4e3e-137">Hosthub 位址</span><span class="sxs-lookup"><span data-stu-id="e4e3e-137">Hosthub address</span></span>

```yaml
Type: System.String
Parameter Sets: IotParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4e3e-138">-名稱</span><span class="sxs-lookup"><span data-stu-id="e4e3e-138">-Name</span></span>
<span data-ttu-id="e4e3e-139">資源名稱</span><span class="sxs-lookup"><span data-stu-id="e4e3e-139">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RoleName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4e3e-140">-平臺</span><span class="sxs-lookup"><span data-stu-id="e4e3e-140">-Platform</span></span>
<span data-ttu-id="e4e3e-141">提供平臺，例如：Linux</span><span class="sxs-lookup"><span data-stu-id="e4e3e-141">Provide the Platform, for ex: Linux</span></span>

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

### <span data-ttu-id="e4e3e-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4e3e-142">-ResourceGroupName</span></span>
<span data-ttu-id="e4e3e-143">資源組名</span><span class="sxs-lookup"><span data-stu-id="e4e3e-143">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4e3e-144">-RoleStatus</span><span class="sxs-lookup"><span data-stu-id="e4e3e-144">-RoleStatus</span></span>
<span data-ttu-id="e4e3e-145">提供狀態啟用/停用</span><span class="sxs-lookup"><span data-stu-id="e4e3e-145">Provide the status enable/disable</span></span>

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

### <span data-ttu-id="e4e3e-146">-確認</span><span class="sxs-lookup"><span data-stu-id="e4e3e-146">-Confirm</span></span>
<span data-ttu-id="e4e3e-147">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="e4e3e-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4e3e-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4e3e-148">-WhatIf</span></span>
<span data-ttu-id="e4e3e-149">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e4e3e-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e4e3e-150">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e4e3e-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4e3e-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4e3e-151">CommonParameters</span></span>
<span data-ttu-id="e4e3e-152">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e4e3e-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4e3e-153">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e4e3e-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4e3e-154">輸入</span><span class="sxs-lookup"><span data-stu-id="e4e3e-154">INPUTS</span></span>

### <span data-ttu-id="e4e3e-155">沒有</span><span class="sxs-lookup"><span data-stu-id="e4e3e-155">None</span></span>

## <span data-ttu-id="e4e3e-156">輸出</span><span class="sxs-lookup"><span data-stu-id="e4e3e-156">OUTPUTS</span></span>

### <span data-ttu-id="e4e3e-157">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.models.PSStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="e4e3e-157">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="e4e3e-158">筆記</span><span class="sxs-lookup"><span data-stu-id="e4e3e-158">NOTES</span></span>

## <span data-ttu-id="e4e3e-159">相關連結</span><span class="sxs-lookup"><span data-stu-id="e4e3e-159">RELATED LINKS</span></span>
